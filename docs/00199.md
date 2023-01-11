# 可信图像的开源管道

> 原文：<https://devops.com/open-source-pipeline-trusted-images/>

使用可信映像(又名“基础映像”)有很多好的理由，包括可靠性、减少启动时间、安全配置。[我们已经在之前的中[讨论过它们]](https://devops.com/uncategorized/trust-the-trusted-image/)

在本文中，我们将描述一个制作可信(又名“基础”或“黄金”)映像的开发和质量保证过程。

首先，这是要使用的工具集。

*   源代码控制跟踪你所有的脚本。图像将建立 100%的脚本，而不是手动键控。因此，源代码控制至关重要。
*   **虚拟机**当您对您的方法做出与您机器的当前状态不兼容的更改时，您需要定期从空白状态开始。使用虚拟机使我们能够快速重置到已知状态并重新应用脚本。
*   **vagger**vagger 是一款虚拟化工具，可以轻松快速启动和重新启动虚拟机，使用基础包和 ssh 配置引导虚拟机，并将您的文件同步到客户操作系统。
*   **持续集成(CI)服务器**为了实现可靠性和可重复性，CI 服务器运行预定的自动化作业，这些作业获取并合并最新代码、生成输出、运行测试、应用标签和其他元数据。
*   **Packer** 提供了从一组脚本构建许多面向不同云环境的映像的能力。

现在，让我们进入创建可信映像所需的三个步骤:

1.  在本地计算机上创建和测试映像；
2.  建立形象，以及；
3.  验证和提升形象。

**步骤 1:在本地创建并测试您的可信映像**

受信任的图像不应该手动构建，否则您很快就会失去对其中内容的跟踪！首先，使用受版本控制的脚本来构建一个根据您的规范工作的虚拟机。当您控制目标操作系统时，您可以使用基本的 shell 脚本。如果您正在为多个目标操作系统构建，像 Chef 或 Puppet 这样的配置管理工具将使您能够编写一组独立于平台的脚本。vagger 是一个非常有用的工具，它将虚拟化和配置管理技术无缝地结合在一起。

通过读取你为你的项目创建的一个流浪者文件来工作。它描述了您想要的基本映像(操作系统)、您需要安装的软件以及您想要访问机器的方式。

然后，您可以使用 VirtualBox(一种跨平台虚拟化工具)之类的虚拟化工具在您的笔记本电脑/工作站上启动本地虚拟机，或者您可以使用 EC2 之类的远程虚拟机。vagger 将本地文件夹同步到虚拟机，这样你就可以在本地或虚拟机上编辑你的脚本，因为脚本就在虚拟机上，你可以在编辑和保存时实时测试它们。这使得代码/测试周期尽可能地快，并且很容易将脚本和 VM 配置(lavong file)保持在源代码控制中。下面是一个从 Ubuntu Precise 开始并使用 chef-solo 构建图像的流浪文件示例:

```
Vagrant.configure("2") do |config|
  *The base operating system that you’ll start from*
  config.vm.box = "precise64"
  config.vm.box_url = "http://files.vagrantup.com/precise64.box"
  *If you install software using Git, you’ll want to forward your ssh key*
  config.ssh.forward_agent = true
  *We are using chef-solo as the “provisioner” to execute the configuration scripts.
  You can also use shell scripts, Puppet, SaltStack, etc.*
  config.vm.provision :chef_solo do |chef|
  *This configuration is specific to Chef. Other provisioners have their own options.*
	chef.roles_path = "roles"
	chef.add_role 'myapp'
  end
end 
```

在您的置备程序脚本(在本例中为 Chef)中，您将在虚拟机上实现以下功能:

*   安装和配置第三方软件包
*   下载和安装自己公司的软件，例如从 Git 下载和安装
*   应用系统范围的配置设置，如 iptables、日志轮转、syslog 等
*   安装您可能希望虚拟机信任的任何自定义 SSL 证书

一旦有了构建所需虚拟机的脚本，并且提交了代码，就该构建映像候选对象了。

**步骤 2:构建和管理映像**

为了构建一个映像候选，您将从一个新的虚拟机开始，运行您的脚本，并从中捕获一个映像。

构建映像与任何其他软件“构建”工作大致相同；像 Jenkins 这样的持续集成工具非常适合这项任务。创建一个 Jenkins 作业来构建您的映像。当您提交对脚本的更改时，推送至源代码控制库并触发构建新映像的作业。您可以用构建作业号和其他元数据标记您的图像。随着图像库的增长，这些元数据将非常有用。特别是，您总是需要能够准确地识别您的配置脚本的哪个版本用于构建特定的映像。

与启动和管理虚拟机相比，vagger 不太适合构建映像，因此对于构建映像，我们将使用一个名为 Packer 的专用工具。Packer 是一个工具，用于从单个源配置文件为多个平台创建相同的机器映像。

Packer 可以获取您的脚本，并为 EC2、GCE、OpenStack、VirtualBox、Docker、Digital Ocean 等平台制作各种不同的图像。Packer 的 JSON 格式包含的信息与流浪者文件非常相似:

```
 {
  "variables": {
    "aws_account": "",
    "aws_region": "us-east-1",
    "ssh_username": "",
    "source_ami": "",
    "access_key_id": "{{env `AWS_ACCESS_KEY_ID`}}",
	"secret_access_key": "{{env `AWS_SECRET_ACCESS_KEY`}}"
  },
  "builders": [
	{
  	"type": "amazon-ebs",
      "ssh_timeout": "3m",
      "access_key": "{{user `access_key_id`}}",
      "secret_key": "{{user `secret_access_key`}}",
  	"region": "{{user `aws_region`}}",
      "ssh_username": "{{user `ssh_username`}}",
      "source_ami": "{{user `source_ami`}}",
      "instance_type": "m3.medium",
      "ami_name": "myapp-{{timestamp}}"
	}
  ],

  "provisioners": [
	{
  	"type": "chef-solo",
  	"roles_path": "roles",
      "cookbook_paths": ["vendor/cookbooks"],
      "run_list": [ "role[myapp]", "recipe[myapp::ami-cleanup]" ]
	}
}
```

**第三步:形象验证和推广**

因为您的映像与您用来开发配置脚本的浮动环境并不完全相同，所以您需要对每个候选映像执行软件测试和质量保证(QA)。通过测试的图像将被提升并发布到下游工作流程(开发/阶段/生产)。

这听起来应该是一个熟悉的问题！同样，它非常适合像 Jenkins 这样的自动化持续集成系统。与任何其他构建作业一样，您的映像构建作业有一个构建号，可以触发下游作业(用于对映像执行 QA)，并且可以运行提升脚本。使用这些工具来验证您的映像，跟踪哪些映像已经过全面测试，并使用重要的元数据对它们进行标记，例如构建映像的脚本的分支/sha。

**结论**

借助这一“可信”或“基础”映像，您可以轻松创建经验证的映像并将其推送到多个云环境中。这可以减少构建和启动单个机器的等待时间，以及那些重复的人工组件可能带来的问题。自动化不就是 DevOps 的全部吗？

鸣谢:Kevin Gilpin、Hleb Rubanau 和 Lucia Capano 是本文的合著者。