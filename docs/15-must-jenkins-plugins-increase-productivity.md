# 15 必须有詹金斯插件，以提高生产力

> 原文：<https://devops.com/15-must-jenkins-plugins-increase-productivity/>

Jenkins 是 IT 行业广泛使用的持续集成工具，它是围绕插件构建和使用的。它的核心是 Jenkins 工具，有 100 个插件可以增强它的功能和可用性。

让我们来看看几个最好的插件来提高生产力。

1.  **Global Build Stats Plugin—**了解您当前的容量、使用情况和功能对于准备容量规划或系统需求至关重要，因为第一个问题是“您当前的容量是多少？”【T2![global-build-stats](img/cb22d0701a6d2fa5b4a04968bc7bf7c0.png)

您需要知道每天和每周有多少构建发生。各种构建花了多少时间，等待周期是多少。这个插件给你足够的数据来回答这个问题。这个插件可以为你提供可以进一步消费的图表数据。

2.  **Job generator plugin–**在大型或成长中的组织中，当开发人员在不同的分支和发布上工作时，维护项目的工作有点困难。你想让开发人员创建他们自己的工作，同时你不希望开发人员创建可能不符合公司标准的任意工作。这个插件给你定义模板的灵活性，开发者可以在作业生成器模板的帮助下创建新的作业。可以通过基于滚动的授权插件禁用配置访问。
3.  **Disable-failed-job–**在快速开发环境中，由于各种不必要的原因导致作业失败是一件痛苦的事情，很难跟踪这些作业并禁用/删除它们。这个插件可以通过定义连续失败构建的上限，然后自动禁用来解决这个问题。
4.  **embedded able-build-status–**这个插件可以给你一个可以粘贴到任何地方的链接(例如 github 项目),以展示构建的状态，用户可以在查看项目时获得任务的当前状态。
5.  **排除-**此插件使您能够处理作业之间的冲突。您可以在多个作业中分配一个资源(或锁),当执行构建时，它将获取锁，而其他构建(如果触发)将等待直到锁被释放。
6.  **GitHub/GitLab Pull Request Builder-**这是我发现的最好的插件之一，在 GitHub/git lab 中提供了一定程度的自动化代码审查支持。一旦为项目定义了这个插件，它会做令人惊奇的工作。对于任何新的拉取请求，该插件都会进行 fox 合并，并对代码运行构建，同时收集必要的静态分析(如果已配置)或构建结果，并将状态反馈给拉取请求。这有助于评审人员了解将要合并的代码的健康状况。如果构建通过，您甚至可以定义自动合并。
7.  **Hudson Extended Read Permission Plugin-**在 Jenkins 设置配置的最初几天，任何开发人员都无法访问配置以确保他们不会更改任何内容，但开发人员过去常常要求查看配置以了解作业是如何设置的，他们可能希望查看构建步骤。扩展读取插件可以为开发人员提供查看配置的选项，而不给他们写权限。
8.  **Post+build+task–**可能需要根据构建的结果执行一些操作，例如，如果构建通过，您可能想要将工件(如 debian)上传到某个 repo (apt)或执行一些打包部分或类似操作。在失败的情况下，您可能想要回滚一些东西(比如 release)。这个插件帮助你定义通过/失败的标准，让你决定之后做什么。
9.  **JDK 参数插件–**这个插件对于许多项目使用不同版本 java 的组织来说很有用。这个插件让你在构建运行时选择 java 版本。
10.  **作业配置历史插件-** 啊！这是我最喜欢的插件之一。这个插件可以让你跟踪每个版本中的配置变化，包括谁做的。如果您愿意，您可以很容易地恢复到任何以前的配置。
11.  **多 SCMs 插件–**默认的 SCM 部分只提供一个源代码控制工具/URL 选项，如果您想从多个源代码控制工具(如 svn 和 git)的两个以上的 repos 中检出，该怎么办。这个插件在这种情况下会派上用场。这个插件将方便用户添加任意数量的 SCM URLs 来检查代码。
12.  **参数化触发插件**——另一个我最喜欢的插件。这个插件允许你将用户输入作为一个变量并在运行时使用。这是动态环境中最常用的插件，在动态环境中，你有很多选项和用户定义的值可以在不断变化的构建中使用。
13.  **Pre SCM BuildStep 插件-** 就像 post build task 插件一样，您可能需要在任务签出之前执行一些操作，例如，您可能希望在构建之前执行分支合并，然后再签出。这个插件可以在各种条件下派上用场，并在运行作业时为您提供灵活性。
14.  **SCM 同步配置插件-** 备份，这是任何管理员最重要的任务。没有定期备份，整个系统就不可能可靠；这个插件为你提供了将实时 Jenkins 配置备份到任何源代码控制工具的功能。一旦有任何变化，它将继续提交配置文件(包括 Jenkins 和 jobs)到 SCM 库。
15.  **配置切片插件–**当您想要在多个作业中进行批量更改时，这个插件非常方便。这个插件允许你一次改变各种字段的值，如电子邮件，定时器，外壳脚本，配置等。

这些是我最喜欢的，但是就像我写的，有 100 个插件可供 Jenkins 使用。你最喜欢的是什么？