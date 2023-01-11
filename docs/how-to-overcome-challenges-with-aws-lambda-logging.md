# 如何克服 AWS Lambda 日志记录的挑战

> 原文：<https://devops.com/how-to-overcome-challenges-with-aws-lambda-logging/>

监控 AWS Lambda 可能是一项复杂且潜在成本高昂的工作。以下是你需要知道的保持在预算范围内

组织已经在经历向无服务器云计算的转变。根据 O ' Reilly "[2019](https://www.oreilly.com/radar/oreilly-serverless-survey-2019-concerns-what-works-and-what-to-expect/)无服务器调查，约 40%的受访者表示他们已经实施了无服务器架构。Forrester "[Global Business techno graphics](https://go.forrester.com/analytics/business-data/)" Developer 2019 发现，49%的公司正在使用或计划在未来 12 个月内使用它。

AWS 在这一领域处于领先地位。据 Serverless.com 称，96%的受访者选择 AWS Lambda，而不是 Azure 功能和谷歌云功能。AWS Lambda 帮助我们设计了一个轻量级的、健壮的应用程序架构，可以轻松地构建和部署。然而，没有免费的东西。在监控 AWS Lambda 时，有几个潜在的高成本复杂性。幸运的是，有一系列的解决方案。

## 记录

默认情况下，AWS Lambda 的 stdout 和 stderr 消息被发送到 CloudWatch 日志，其中每个函数都有自己的*日志组*。日志组是日志流(日志事件序列)的集合，可以存储任意长的时间。日志存储成本为 0.03 美元/GB，数据接收成本约为 0.50 美元/GB。

通常的做法是将你的 Lambdas 分解成单一的责任职能。这意味着，举例来说，如果你需要一个 Lambda 来读取一个特定的对象，另一个来写它，你就建立了两个独立的函数。然而，这也意味着两个日志组。

当您想要分析应用程序的输出日志时，这就带来了挑战。没有跨多个日志组记录查询的直接方法。对此，AWS 启用了 CloudWatch Log Insights 来进行跨日志查询。虽然这带来了许多用户想要和需要的改进，但是一起分析多个日志组意味着更高的查询成本。这种令人望而却步的成本模式鼓励许多人寻求外部服务。

## 描摹

AWS X-Ray 使您能够跟踪应用程序的底层组件，并帮助您挖掘分布式问题背后的根本原因。它已迅速成为工程师的重要故障排除和优化工具。

例如，对于启动时间慢的 AWS Lambda 功能，冷启动延迟可能是个问题。虽然您可以通过启用预配并发来解决这个问题，但是您需要支付额外的费用。

如果您有预算限制，但仍想解决问题，X 射线可能会通过消除瓶颈来帮助您消除或至少优化您的应用程序。它让您知道，除了别的以外，您的应用程序在初始化或调用期间是否消耗了更多的时间。你可以在 AWS Lambda 上找到适用于 Go、Java、Node.js、Python 和. NET 的 X-Ray SDK。

## 排除故障

传统架构和[无服务器架构](https://devops.com/predictions-2020-infrastructure-and-ops-trends-to-watch-in-2020/)天壤之别。无服务器需要改变整个软件工程领域，包括调试。

无服务器应用程序是基础架构内各种服务或资源的组合，可以包括 AWS API Gateway、CloudWatch 和 SNS 等工具。web 服务的这种分布有助于避免单点故障(SPOF)，但是这种设计产生了一个问题。在本地机器上调试或复制问题并不总是可行的，并且调试生产应用程序总是一件危险的事情。

此外，AWS Lambda 的抽象使得调试变得复杂，因为您不能直接访问底层操作系统。搜寻分散的日志会增加开销。随着无服务器基础架构的扩展，确定根本原因变得越来越困难。

为了解决这个问题，开发人员可以使用 AWS 原生工具，如 CloudWatch、X-Ray 或无服务器应用模型(也称为 SAM)。这些工具中的任何一个本身都难以使用；然而，它们一起形成了一个强大的调试套件。

在 AWS 原生工具集之外，一些工具提供了进一步的调试帮助。例如，无服务器框架是一个通过 AWS 开发和部署无服务器应用程序的开源工具，它允许您查看您的[实时应用程序的功能日志](https://www.serverless.com/framework/docs/providers/aws/cli-reference/logs/)，例如:

**[![](img/fe3a18182813c3e623e9a249c07fd01e.png)](https://containerjournal.com/wp-content/uploads/2020/06/Screen-Shot-2020-06-25-at-12.52.54-PM.png)**

## 监视

强大的监控可确保应用程序的平稳运行，并有助于快速检测问题。在传统的基础设施中，指标只出现在少数来源中，因此将它们收集在一起并不困难。在无服务器架构中，这个问题要复杂得多。

AWS 让您可以自由地将 CloudWatch 日志转换成指标。这些指标可以被过滤、测量，当超过阈值时，[在](https://coralogix.com/log-analytics-blog/10-alerts-and-visualizations-for-s3-server-access-logs-to-take-control-of-aws-infrastructure/)发出警报。您可以通过选择由无服务器功能创建的日志组来定义度量过滤器，并将日志流作为目标。这使您能够为日志事件创建可视化参考。您创建的每个自定义指标每月将花费 0.30 美元/10000 个指标。

度量过滤器可能是一个强大的工具，但是设置所有的东西也可能有点令人不知所措，并且也存在某些瓶颈。例如，您不能参数化指标名称，这迫使您为想要跟踪的每个定制指标创建一个过滤器。每个日志组还有 100 个度量过滤器的硬性限制，这限制了您对应用程序的发展。

除此之外，AWS 资源彼此紧密耦合，这使得当您需要监控单个 AWS 资源或 Lambda 函数时，AWS 原生监控工具是一个不错的选择。为了获得基础设施范围的视图并监控其他第三方工具，需要一种[集中式](https://coralogix.com/log-analytics-blog/aws-centralized-logging-guide/)日志记录方法来充分利用日志数据。

## 结论

不可否认，无服务器工具可以快速实现高可用性、可伸缩性和成本优化。为了充分利用这种新模式，工程师需要构建一个强大而可靠的监控系统。管理来自许多组件的日志数据流、即时检测和跟踪问题以及提供准确的见解以持续改进应用程序的能力对于保持在线和竞争力至关重要。

虽然无服务器解决方案提供了我们需要的许多技术功能，但如果您想要顺利扩展您的组织及其基础架构，则必须考虑供应商锁定的危险和第三方提供商的力量。