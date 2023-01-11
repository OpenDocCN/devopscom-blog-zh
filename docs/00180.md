# DevOps 安全自动化:给我看看代码！

> 原文：<https://devops.com/security-automation-devops-show-code/>

上周，Andrew Storms 在[SecDevOps:Security Automation By Example–The Firewall Change]中发表了一篇很好的帖子，暗示了安全自动化的前景。他举了一个在防火墙规则改变时自动执行一系列操作的例子。这是一篇好文章，虽然我越来越相信没有 SecDevOps 这种东西。在我的书中，都是 DevOps，但那是另一篇文章的素材(当我不与胃虫作战时)。然而，安德鲁描述的更多的是我认为的*自动辅助*。它不一定是完全自动化的，因为它会触发手动防火墙规则更改。理想情况下，我们很少手动更改防火墙(或安全组)规则，而是更多地依赖基于策略的自我配置。是的，我知道，通常的分析师废话，所以这里有一点过程，和一点代码。让我们换一种方式来处理这个问题。采用 Andrew 的流程，但是让安全组或主机防火墙根据资产进行自我配置。我的例子是针对 Amazon Web Services 的，因为我有一些代码片段来展示它是如何工作的。(不好意思，我今天没有时间或者肠道刚毅把所有代码都写出来；说真的，这个 bug 是哪里来的？！？)我通常认为有两种技术构成了动态安全组策略实施的核心:

1.  标签
2.  配置管理集成

有些云服务，比如 AWS，支持对象(在本例中是实例)级别的标记。这些标签可以在内部绑定到策略，同时也可供外部工具使用。下面是我使用的一个策略，如果“SecurityStatus”标记是“IR”(表示“事件响应”)，则限制对对象的访问:

```
{  
  "Version": "2012-10-17",  
  "Statement": [  
    {
      "Action": "*",
      "Condition": {  
        "StringEquals": {
          "ec2:ResourceTag/SecurityStatus": "IR"
          }
          },
          "Resource": [
          "*"
                      ],
          "Effect": "Deny"
      }
      ]  
    } 
```

我可以手动或自动应用该标记，无论是哪种情况，该实例都不能再由应用该策略的任何帐户管理。现在，这并不能帮助我们改变防火墙/安全组规则，因为您不能在 EC2 中基于标签直接管理这些规则(但是我手头有一个策略可以演示，所以就这样吧)。为此，您需要编写自己的代码来扫描标签，然后采取行动。我手头没有准确的代码示例。但是这里有一些片段可以让你更接近。其中大部分都是抄袭我在 GitHub 上的[security quirrel 概念证明。都是 Ruby 的，用的是 AWS 2.0 开发者预览版 SDK。首先，要获取带有某个标签的所有实例的列表，可以使用以下代码:](https://github.com/Securosis/SecuritySquirrel)

```
def testing
 # testing some tag code
 instancelist = @@ec22.describe_tags(
 filters: [
 {
   name: "key",
   values: ["SecurityStatus"]
 }
 ]
 )
 puts instancelist.to_h
end 
```

这显示了带有 SecurityStatus 标记的所有内容(实例和值，显示为一个散列)，但是您也可以根据值进行过滤。从那里，您可以使用一个映射来提取实例 id(您可能希望只对实例进行进一步的过滤，但是如果您已经做到了这一步，您就可以弄清楚这一点):

```
 instances = instancelist.map(&:resource_id) 
```

然后，您可以将它们注入一个方法来更改安全组。下面是 SecuritySquirrel 的一个例子，它将一个实例放入“隔离”组:

```
def quarantine
  #this method moves the provided instance into the Quarantine security group defined in the config file.
  puts ""
  puts "Quarantining #{@instance_id}..."
  quarantine = @@ec22.modify_instance_attribute(instance_id: "#{@instance_id}", groups: ["#{@QuarantineGroup}"])
  puts "#{@instance_id} moved to the Quarantine security group from your configuration settings."
end 
```

想触发扫描吗？下面是一个代码片段，用于从您的 AWS 帐户中的虚拟设备触发对实例的 Qualys 扫描(请记住，我跳过了一些重要的部分，如配置服务和身份验证):

```
 instance_IP = instance_details.reservations.first.instances.first.private_ip_address
 timestamp = Time.new
 scan =(HTTParty.post("https://qualysapi.qg2.apps.qualys.com/api/2.0/fo/scan/",
      :basic_auth => @qualysauth,
      :query => { 
        :action => "launch",
        :scan_title => "SecuritySquirrel Scan at #{timestamp}", 
        :ip => "#{instance_IP}",
        :option_title => "Initial Options",
        :iscanner_name =>  "us-west-2" 
      },
      :headers => { "X-Requested-With" => "ruby httparty"}))
      puts "Launching Qualys scan named: SecuritySquirrel Scan at #{timestamp}" 
```

还是想改变 CloudPassage Halo 主机防火墙规则？好吧，这些代码使用了他们的 Ruby SDK 的预发布版本，所以我将把它留到以后再说(我没有受雇于他们，但是他们允许我使用预发布版本的 gem)。这些例子都是基于标签的，但是请记住，如果您使用像 *Chef* 或 *Puppet* 这样的工具，您可以根据实例中配置和运行的软件做完全相同的事情。例如，您可以创建一个策略，通过关闭运行易受攻击的 OpenSSL 软件包的任何服务器上的端口 443，在 Heartbleed 漏洞出现时隔离所有 SSL，然后在规则更新为修补版本时删除规则。我有点生疏了，因为我不是每天都写代码，但是我可以在一两个小时内完成，这并不难。此外，我的工具是为演示设计的，并不在后台运行，但显然你可以让它一直运行，根据实例中部署的软件的标签甚至属性进行调整。安全自动化非常强大。它可以完全自动化复杂的安全任务，或者像 Andrew 的例子一样，补充手动活动和策略更改。希望我的片段能给你一些启发，如果你愿意分享的话，给我一些好的例子。