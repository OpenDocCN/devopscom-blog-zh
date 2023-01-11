# ElasticBox Jenkins 插件–简单的持续集成设置

> 原文：<https://devops.com/elasticbox-jenkins-plugin/>

**詹金斯和 ElasticBox 简介**

ElasticBox 最近发布了一个 Jenkins 插件，它可以在不编写任何代码或脚本的情况下配置持续集成或持续部署场景！你会问我们是如何做到这一点的？很简单，这是魔法。严肃地说，如果您将 ElasticBox 和 Jenkins 与您选择的源代码控制软件集成在一起，那么神奇就是最终结果。

对于那些依赖 Jenkins 进行日常工作的人来说，执行集成构建、编排复杂的大规模场景以测试或管理跨多个环境的具有许多配置的应用程序的连续交付并不罕见。这些类型的场景需要大量时间来设置从设备，并执行手动步骤来配置云提供商的供应。当您将多个云或混合云环境考虑在内时，保持跨环境的一致性变得异常复杂。

通过将 ElasticBox 与 ElasticBox Jenkins 插件结合使用，您可以减少手动配置和脚本的数量，同时抽象基础设施的供应。这意味着您可以使用 ElasticBox 以最快、最一致和最可靠的方式解决复杂的持续集成或部署用例。

**工作原理:**

在 ElasticBox，我们在拉请求和合并时触发测试、构建和部署，这是一个非常常见的用例。这些动作启动工作流，导致 Jenkins 触发测试、构建和实例部署。有关我们内部持续部署场景的更多信息，请查看我们今年早些时候展示的这张[幻灯片分享](http://www.slideshare.net/ElasticBox/ramiro-glucon)幻灯片。

首先要理解的是，我们将 Jenkins 作为一个实例来管理，并通过 ElasticBox 部署到我们的私有数据中心。我们有一个盒子，可以在您选择的提供商上安装 Jenkins 服务器。这使得在多个构建减慢速度时可以方便地进行扩展，或者在某个部分崩溃时可以简单地进行重新部署。

拼图的第二块是所需的插件，如最近发布的 [ElasticBox Jenkins 插件](https://wiki.jenkins-ci.org/display/JENKINS/ElasticBox+CI)，它与 [Github Jenkins 插件](https://wiki.jenkins-ci.org/display/JENKINS/GitHub+Plugin)一起，使得在不编写任何代码的情况下建立持续集成或部署服务器完全可能。

**设置 Jenkins 和 ElasticBox:**

首先你要在 Jenkins 的配置页面设置 ElasticBox 为云。您只需输入 ElasticBox URL([http://elasticbox.com](http://elasticbox.com/))、最大实例数、保留时间(分钟)以及您的 elastic box 用户名和密码。正确输入所有这些信息后，您就可以继续测试连接了。

[![Screenshot 2014-07-01 17.57.13](img/7e7285c1881befd766a9348c6c9c3148.png)](http://elasticbox.com/blog/wp-content/uploads/2014/07/Screenshot-2014-07-01-17.57.13.png)

**ElasticBox Jenkins 示例:**

在这个基本的例子中，我们将向你展示我们如何测试我们网站的变化。当一个分支作为一个拉请求被提交时，我们部署一个新的 web 站点盒子的暂存实例。在将拉请求合并到我们的主分支之前，我们在生产环境的副本实例上验证更改。当代码被合并时，我们触发一个 Jenkins 作业，用最新的代码变更重新安装我们的生产实例(在这个演示中没有显示)。现在，我们的网站变更工作流程几乎完全自动化，减去了拉取请求和合并！

1)第一步是创建一个新的 Jenkins 条目，我们选择“构建一个自由风格的软件项目”

[![Screenshot 2014-07-02 11.34.50](img/8c9018a56174dc1a01a6a44e15e1bfb2.png)](http://elasticbox.com/blog/wp-content/uploads/2014/07/Screenshot-2014-07-02-11.34.50.png)

2)一旦我们创建了一个新项目，我们添加 Github 项目 URL 并选中“这个构建是参数化的”框。虽然这一步不是必需的，但它允许您手动触发构建并执行特定分支的代码。

[![Screenshot 2014-07-02 11.46.36](img/070019b0f985d244ebef94f67c44b39b.png)](http://elasticbox.com/blog/wp-content/uploads/2014/07/Screenshot-2014-07-02-11.46.36.png)

3)在源代码管理部分，我们指定源代码管理工具“存储库 url”，以用户名/密码的形式提供凭证，对于分支说明符，使用“${sha1}”，它表示在拉请求中提交的分支的提交 URL。Jenkins Git 插件极其复杂，我们强烈推荐阅读关于该插件的 [Wiki](https://wiki.jenkins-ci.org/display/JENKINS/Git+Plugin) 。

在构建触发器部分，您需要选择“Github Pull Request Builder ”,这将触发 ElasticBox 中的 Jenkins 构建和实例部署。

![Screenshot 2014-07-02 11.48.44](img/8446e6fdad86576fb76d64b21dc375aa.png)

4)最后一步是配置构建步骤。有了 ElasticBox 插件，你就可以访问所有的[工作区](http://elasticbox.com/documentation/core-concepts/workspaces-and-collaboration/)、[盒子](http://elasticbox.com/documentation/core-concepts/boxes/)和[部署概要文件](http://elasticbox.com/documentation/deploying-and-managing-instances/deploying-managing-instances/)。有关这些特性的更多信息，请查看我们的[文档](http://elasticbox.com/documentation/ "documentation")的链接。指定您想要使用的工作空间、框和部署配置文件。在我们的例子中，我们指定了我们的生产工作区、我们的网站框和我们的临时部署概要文件。

[![Screenshot 2014-07-02 13.31.32](img/6a3ecf0f2ff80d4fe1db927711bbab34.png)](http://elasticbox.com/blog/wp-content/uploads/2014/07/Screenshot-2014-07-02-13.31.32.png)

结论:

一旦设置了所有这些配置，您就可以通过提交 pull 请求在新的临时实例上测试更改。尽管这是一个基本的例子，但是根据持续集成标准，您可以看到 ElasticBox Jenkins 插件如何大大减少设置持续集成服务器所需的配置数量。

有了 ElasticBox 对基础设施供应进行抽象，并允许您重用现有的应用程序或基础设施组件，以可重复和可靠的方式扩展流程就容易多了。我们将继续发布博文，提供更多关于如何使用 Jenkins 和 ElasticBox 进行集成构建、测试和持续交付模型的技术示例。