# 提升网络和应用性能的 14 种工具

> 原文：<https://devops.com/14-tools-raise-web-app-performance/>

在 [DevOps 时代](http://logz.io/learn/what-is-devops/)，团队越来越多地转向各种工具进行集成、加速和自动化。速度和效率至关重要。这在连续交付(CD)中尤其突出，它使 IT 团队能够实现快速可靠的发布。如果成功，CD 可以加快上市时间，提高运营效率，并以高性能水平尽快将正确的产品和功能投入生产。

那么，有哪些工具可以帮助提高软件性能呢？以下是我们在日志管理平台 [Logz.io](http://logz.io/) 喜欢的 14 个列表，其中一些对你来说是全新的。

## 持续集成工具

### 詹金斯

一个可扩展的持续集成(CI)引擎， [Jenkins](https://jenkins-ci.org/) 是 DevOps 工程师想要监控重复作业执行情况的顶级工具。有了 Jenkins，DevOps 工程师可以更轻松地将变更集成到项目中，并在出现问题时轻松访问输出。它不是最快或最花哨的工具，但它真的很容易使用，而且它有一个很棒的插件和附加组件生态系统。它还经过优化，易于定制。

### TeamCity

[TeamCity](https://www.jetbrains.com/teamcity/) 是一款主要的一体化、可扩展、持续集成服务器。该平台用 Java 编写，帮助开发人员不断构建和测试软件，并监控外部运行的作业，如 cron 作业和 procmail 作业。它增加了自动化的规模，并在 DevOps 圈子里迅速流行起来。该平台由 100 个现成的插件支持其他框架和语言。TeamCity 的安装非常简单，不同的操作系统有不同的安装包。

### 竹子

由 Atlassian 开发的 [Bamboo](https://www.atlassian.com/software/bamboo) 不仅仅运行构建和测试。它将问题、提交、测试结果和部署联系在一起，因此整个产品团队，从项目经理到开发人员、测试人员到系统管理员，都可以看到全貌。Bamboo 支持使用任何构建工具(如 Ant、Maven 和 make)以及任何命令行工具在任何编程语言中进行构建。构建通知可以基于事件的类型进行定制，并在基于 Eclipse 的 ide 和 IntelliJ IDEA 中通过电子邮件、即时消息、RSS 或弹出窗口接收。

(更多信息，我的一个同事已经出版了一个指南，介绍[持续集成工具](http://logz.io/blog/continuous-integration-tools/)。)

## 负载和性能测试工具

### JMeter

Apache 基于 Java 的开源 JMeter 有一个用户友好的 GUI，使得测试开发和调试更加容易。JMeter 已经被广泛使用了 15 年，现在是 Silk Performer 和 HP LoadRunner 等专有解决方案的流行开源替代方案。JMeter 的一个主要优点是它是可伸缩的。当您需要的负载高于单台机器所能产生的负载时，JMeter 可以以分布式模式执行——这意味着一台主 JMeter 机器控制许多远程主机。JMeter 还具有多协议支持和对 HTTP、SMTP、POP3、LDAP、JDBC、FTP、JMS、SOAP 和 TCP 的开箱即用支持。

### 火焰测量器

尽管 JMeter 带来了很多好处，但作为独立工具使用时，它的功能是有限的。或者，查看一下 [BlazeMeter](https://www.blazemeter.com/) ，这是一个很好的工具，允许您在云中运行 JMeter，进一步提高可伸缩性，并以易读的图形提供全面的测试结果。借助 BlazeMeter，软件交付和 DevOps 团队可以通过与同行无缝共享测试脚本来提高生产力，从而获得更快的反馈、更深入的学习和更高的性能。BlazeMeter 还可以轻松集成领先的 CI 工具，包括 Jenkins 和 TeamCity。

### 金牛星座

继续前面的观点，JMeter 是一个很好的工具，但是它并不完美。自动化和与其他系统的集成有时很困难，这是另一个需要学习和掌握的工具。这就是像金牛座这样的工具的用武之地。除了 JMeter 之外，流行的免费和开源工具还包括其他选择，如 [The Grinder](http://grinder.sourceforge.net/) 、 [Gatling](http://gatling.io/#/) 或 [Locust](http://locust.io/) (也是一个很好的负载测试工具，基于 Python)，每种工具都有自己的优缺点。Taurus 是一个自动化友好的测试工具，它扩展并抽象了上述工具(以及 Selenium)，并有助于克服各种挑战。Taurus 提供了一种创建、运行和分析性能测试的简单方法。Taurus 的想法是以一种更加用户友好的方式提供语言创建/配置脚本(JSON 或 YAML)。你不仅可以用 Taurus 创建脚本，它的一个额外好处是你可以使用预先存在的脚本。

## 应用程序性能监控工具

### 新遗迹 APM

应用程序性能监控(APM)工具允许您定位应用程序框架的瓶颈。New Relic 是目前的市场领导者，这是有充分理由的。它可以让您精确定位瓶颈出现的位置和时间。DevOps 工程师可以使用该工具减少监控应用的时间，将更多时间用于构建和部署。新遗迹提供网络请求监控。NET、Java 等等。它自动显示最重要请求的基于组件的细分。New Relic APM 是一款受欢迎的可靠工具，是 DevOps 工程师的绝佳选择。

### 应用动力学

AppDynamics 也是一个很棒的工具，可以让你监控 Java。NET、PHP 和 Node.js 应用程序。AppDynamics 提供性能管理解决方案，使开发人员能够实时诊断和修复应用程序性能问题。AppDynamics 的监控功能还有助于简化复杂的关键业务应用的管理。

### Dynatrace

Dynatrace 帮助用户监控应用服务器、数据库服务器和网络服务。其功能集体现在。NET 提供代码级监控(包括 CPU 和等待时间)、端到端跟踪和用户体验监控。它支持整个应用程序生命周期，从开发环境到负载测试再到生产。

## 基础设施工具

### AWS 云观察

亚马逊提供了 [AWS CloudWatch](https://aws.amazon.com/cloudwatch/) ，使运营部门能够通过他们的 API 查看使用和性能信息。AWS CloudWatch 提供了有关数据传输、磁盘使用和 CPU 利用率的指标，还可以配置这些指标，以便在超过阈值时触发通知和警报。AWS 用户还可以通过 CloudWatch APIs 注入自己的指标，生成全面的交叉分析。

### 谷歌云监控(StackDriver)

[Google Cloud Monitoring](https://cloud.google.com/monitoring/) 为您的云计算应用提供仪表盘和警报。团队可以审查云服务、虚拟机和常见开源服务器(如 MongoDB、Apache、Nginx 和 Elasticsearch)的性能指标。您还可以使用云监控 API 来检索监控数据并创建自定义指标。

## 虚拟化和容器

### 码头工人

面向分布式应用的开放平台， [Docker](https://www.docker.com/) 是一款面向希望“在任何地方构建、发布和运行任何应用”的 DevOps 工程师的应用 Docker 使开发人员和系统管理员能够更容易地将代码从开发推向生产，而没有在整个应用程序生命周期中使用不同的冲突环境所带来的不可避免的问题。Docker 正在推动微服务的趋势，在微服务中，应用程序被分成更小的自包含组件，这些组件作为容器独立打包和部署。

(对于那些喜欢平台的人，我们有一个使用 ELK Stack 的 [Docker 监控指南。)](http://logz.io/learn/docker-monitoring-elk-stack/)

## 配置管理工具

### Ansible

最近被 RedHat 收购的 Ansible 是一个基于 Python 的 IT 自动化和配置框架，允许用户在没有配置或设置的情况下管理他们的系统。DevOps 工程师可以利用 Ansible 在应用程序部署、配置管理和持续交付以及管理系统方面节省时间。它最近发布了最新版本的[。](https://www.ansible.com/blog/ansible-2.0-launch)

### 厨师

[Chef](https://www.chef.io/) 是一个系统和云基础架构框架，它通过称为“配方”的简短、可重复的脚本来自动化基础架构的构建、部署和管理但是 Chef 的真正强大之处在于它使用了可插拔的配置模块(也称为 cookbooks)，在 Chef 社区中有近 2000 个这样的模块。Chef 可以与 Rackspace、Internap、Amazon EC2、Google Cloud Platform、OpenStack、SoftLayer 和 Microsoft Azure 等基于云的平台集成，自动供应和配置新机器。

所以，就这样了！你觉得这些工具怎么样？你还有其他更喜欢的选择吗？我很想在下面的评论中听到你的想法。