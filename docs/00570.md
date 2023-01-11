# 厨师最佳实践

> 原文：<https://devops.com/chef-best-practices/>

**厨师最佳做法**

这篇文章是关于厨师的第二部分。请参考[自动化、供应&配置管理(CHEF)](https://devops.com/blogs/automation-provisioning-configuration-management-chef/ "Automation, Provisioning & Configuration Management (CHEF)") 进行介绍。

事实上，厨师确实是一个令人震惊的工具。它让烹饪隐喻继续活跃。

以下是我想在本文中介绍的最佳实践列表:

*   项目创建和“readme 驱动的开发”
*   一种带有耙子健全的建筑系统
*   与 Travis 的持续集成
*   带 Chefspec 的 TDD
*   spark 工作流
*   用 Minitest 验证

**入门:**

**1)。**第一步也是最重要的一步是**创建一个新项目**。在这个部分中，所有的东西都应该是源代码控制的。在这个例子中，已经为所有代码创建了一个 Github repo，用于验证或查看开发的分步过程以及错误，它们可以很容易地从**提交历史**中查看。遵循所有步骤，并对您的项目进行同样的操作:

```
git init
```

第二个目标是执行**源代码管理**。通过运行下面的命令，您可以使用 git flow 来管理您的特性，方法是选择所有默认设置，如果您没有使用它，那么您应该开始使用它了。

```
git flow init
```

使用 Readme 驱动开发是最佳实践，可以从 **README.md** 文件开始。这个练习非常重要，因为它可以帮助你集中注意力，让你像用户一样思考。

这里 **Rake** 被用于一个已经构建好的系统。以下是需要考虑的任务列表:

*   **Rake check:** 这个负责检查所有其他依赖项。
*   Rake build:Rake build 的主要目标是管理和运行测试套件。
*   **Rake start:** 它的作用相当于一个 envelope up。

**2)。**另一个最佳实践是**为项目建立一个 Ruby 版本**。这是通过创建两个版本文件来完成的:**。rvmrc** 和 **.rbenv.**

创建 Ruby 文件后，下一步是**创建一个 Gemfile** 。创建这个文件的主要目的是建立所有的项目依赖关系。

以下是帮助您创建 Gemfile 的命令示例:

```
source "http://rubygems.org"
```

拼音' 1.9.3 '

宝石'耙子'，' 10.0.4 '

创建完成后，安装这些依赖项是必不可少的关键步骤，使用下面提到的说明可以做到这一点:

```
bundle install
```

创建一个新的 **Rakefile** 也是必要的。根据我们的自述文件中已经定义的内容，它包含一个占位符任务。

通过使用 **Rake** 来建立一个构建系统，有助于自动化一些常见的任务。

**3)。** **与特拉维斯**的持续融合是另一种精英做法。

但是在我们继续下一步之前，在存储库和 Travis 之间创建一个链接是很重要的。在用户已经创建了代码存储库作为系列的一部分的情况下，这是必不可少的一步。

链接完成后，您可以通过创建新的 Travis 文件来配置 Travis，即:项目目录根目录下的 **.travis.yml** 。

配置 Travis 有助于消除开发 gem 依赖性，从而加快 CI 服务器上的工作和测试。此外，它还测试主分支和开发分支。

更新您的 gem 文件也很重要，以确保正确排除任何未来开发相关的 gem。将此添加到您的 **Gemfile:**

**组:开发办**

**结束**

Travis 配置完成后，您可以通过添加 Travis 通知来更新您的 **README.md** 以指示构建的状态。

**4)。**另一个最佳实践是使用 Chefspec 执行 **TDD 来“规范”**菜谱。

第一步是通过更新文件将 chefspec 添加到你的 **Gemfile** 中，当然也要做**包更新**。

更新完成后，您可以**自动创建 Chefspec Cookbook。**根据 Chefspec 文档，您可以创建一个 cookbook，另一方面使用另一个命令创建 spec 目录。

根据用户或您的不同需求，您甚至可能希望创建一个**新食谱。**

例如:建立一个新的 rake 任务:new_cookbook 下面是需要遵循的说明

```
desc "Creates a new cookbook."
```

```
 task :new_cookbook, :name do |t, args| sh "bundle exec knife cookbook create #{args.name}" sh "bundle exec knife cookbook create_specs #{args.name}" end
```

一旦你生成了新的食谱，你也可以创建你的示例食谱

```
rake new_cookbook motd
```

此时，您有了一个新的空白食谱，可以使用 **rspec 食谱运行基本测试。**您甚至可以添加一个 rake 任务，并为使用升级构建任务。最后，您可以通过创建一个**失败规范，将 motd cookbook 的规范添加到**motd/Spec/default _ Spec . Rb**文件中。**通过执行 rake，build 应该能够显示**“现在失败”**。此后，你需要实现食谱。

制作您的 Spec Pass 和**templates/default/motd . tail . erb**文件:

最后，测试驱动的指南完成了，因为 Travis 文件已经引用了构建任务，所以当我们发布代码时，CI 将运行这个测试并验证您的工作。

**5)。与 Spork** 合作是 Chef 的另一项实践。这个工具有助于协作食谱的开发。它也有助于单个开发人员控制和整理遇到的版本。

因此，为了测试这一点，最初我们将安装 knife-spork，并对你的 motd 食谱做一个小编辑，以使用它的功能。第一步是通过将 spork gem 添加到 Gemfile 中来更新您的 Gemfile。这不是 CI 服务器所要求的，而是放在开发模块下:

以下示例举例说明了该指令:

```
group :development do
```

```
 gem "knife-spork", "~> 1.0.17" end
```

更新后，下一步是通过创建一个 **config/spork-config.yml** 文件来配置您的 Spork，将其放入默认配置中。虽然有一个小问题，即在不同的地方有大量的配置，并且经过一段时间的整合。

按照以下说明配置您的 Spork:

```
mkdir config
```

```
 touch spork-config.yml
```

运行 **rake build** 任务表明我们的测试失败了，只需更新模板就可以纠正。当你完成你的更新和测试通过的时候，我们应该通过**捆绑执行刀 spork bump motd 补丁来修改食谱的版本号。**最后，您将利用上传功能将它上传到 chef 服务器，同时“冻结”它。

spork 的另一个伟大的特性是 [**spork promote**](https://github.com/jonlives/knife-spork#spork-promote) 命令，它允许你将一个特定版本的食谱约束到一个特定的环境中。一个用例可能是:

*   正在您的开发环境中验证 Cookbook 2.0 。
*   **Cookbook 1.9** 在生产环境中。
*   当情况看起来不错时，就可以开始生产了。

**6)。**最后但并非最不重要的是**建立迷你测试套件**在真实的服务器上验证你的食谱。这可以通过将您的文件放在正确的位置并将 default 添加到您现有的 cookbook 中来实现:

```
mkdir -p cookbooks/motd/files/default/tests/minitest
```

```
 touch cookbooks/motd/files/default/tests/minitest/default_test.rb
```

为了避免上述行为，您还有另一个选择。您可以简单地修改 **new_cookbook** rake 任务，使这部分 cookbook 构建完成。最后一步是**部署食谱并测试它**。这有助于您构建一个在服务器上使用时实际有效的食谱。它们还充当一个安全网，因为它们在服务器被供应时运行。

**结论:**

上面提到的是 Chef 的最佳实践，它将帮助你以一种真实的、测试驱动的方式构建食谱。实现所有这些将有助于通过在新的食谱中保留您的定制食谱更改，并毫无问题地能够创建有针对性的拉请求以与社区共享，来帮助您摆脱所有主要的难题。

我希望你能聪明地从这里学到一些好的做法。

祝你生日快乐！