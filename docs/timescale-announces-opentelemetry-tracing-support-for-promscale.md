# 时标宣布开放 Promscale 遥测跟踪支持

> 原文：<https://devops.com/timescale-announces-opentelemetry-tracing-support-for-promscale/>

*继最近的*[*【1.1 亿美元 C 轮投资*](https://tsdb.co/series-c) *之后，时标宣布在 Promscale 中全面提供 OpenTelemetry 跟踪支持，它的统一可观察性后端由 SQL 提供支持。随着今天的公告，时标进一步推进其使命，使世界各地的开发人员能够有效地分析他们的时间序列数据；让他们知道发生了什么，为什么会发生，以及如何修复。*

**纽约州纽约市，2022 年 5 月 16 日—**今天， [时标](https://www.timescale.com/)——PostgreSQL 内建的时间序列行业领先关系数据库 TimescaleDB 的创建者——宣布在 Promscale 中全面提供 OpenTelemetry 支持。Promscale 是 Prometheus metrics 和 OpenTelemetry traces 的统一可观测性后端，由基于 TimescaleDB 和 PostgreSQL 的 SQL 提供支持。它为云原生应用的用户提供了使用他们已经知道的查询语言询问他们的可观测性数据的能力和灵活性，并获得关于他们的分布式系统的前所未有的洞察力，以更快地解决问题并构建更好的软件。随着跟踪现在普遍可用，Promscale 为度量、跟踪和业务数据提供了单一数据库和统一的查询语言。

2021 年，时标 [公布了 Promscale 中 OpenTelemetry traces 的 beta 版本](https://www.businesswire.com/news/home/20211011005420/en/Timescale-Announces-Support-for-OpenTelemetry-Traces-in-Promscale) 。随着今天的发布，对 OpenTelemetry traces 的支持现已完全可用，这使得跟踪数据对开发人员来说更容易访问和更有价值，因此他们可以更好地监控、维护他们的分布式系统并对其进行故障排除。

### **这对开发者意味着什么**

OpenTelemetry 是由云原生计算基金会(CNCF)托管的云原生服务和基础设施工具的开源可观测性框架。作为仅次于 Kubernetes 的活动和贡献者最多的项目，它专注于通过使遥测数据非常容易收集和普遍可用来解决操作分布式系统的挑战。

由于众多组件、交互、自动扩展和频繁部署，当今的云原生架构通常会遇到调试问题。这使得很难识别这些系统中的问题区域。可观察性通过提供对它发生的地点和原因的洞察来解决这个问题。它通过以三种信号(指标、日志和轨迹)的形式从现代软件系统收集全面的遥测数据，并通过实时灵活地分析遥测数据的能力来实现这一点。可观测性本质上是一个分析问题。

度量和日志是众所周知的，并且已经通过 Nagios、Prometheus 或 ELK stack 等工具被广泛采用了很多年。然而，它们是脱节的，并且不提供识别分布式系统中异常行为所需的细节水平。另一方面，跟踪捕捉整个系统如何协同工作来处理请求的关联视图。这使得用户能够了解问题的全部范围以及不同系统组件的实时行为和交互。

有了跟踪支持，Promscale 为每个开发人员提供了由 SQL 驱动的可观察性。可观察性是一个数据分析问题，SQL 是一种强大的数据分析语言:通过使用 SQL 来分析跟踪数据，开发人员可以获得关于他们的分布式系统的前所未有的洞察力，更快地识别生产问题，并减少平均恢复时间。

### **最新消息**

prom scale 中的 OpenTelemetry tracing 支持包括以下特性:

*   【Grafana 内完全可定制的开箱即用体验，帮助用户了解其分布式系统的性能，从而深入了解微服务的行为。
*   【OpenTelemetry traces 的本机摄取端点，理解 OpenTelemetry 协议(OTLP)以轻松摄取 OpenTelemetry 数据。
*   跟踪数据压缩和可配置的保留以管理磁盘使用。
*   无缝集成，使用 Jaeger 和 Grafana 可视化 Promscale 中存储的分布式轨迹，用户无需学习新工具或改变现有工作流程。
*   支持通过 OpenTelemetry Collector 摄取 Jaeger 和 Zipkin 格式的轨迹，因此用户也可以从新功能中受益。

“可观察性是一个分析问题；SQL 是可观察性的通用语言。通过将 SQL 与 OpenTelemetry traces 相结合，您可以获得现有可观测性查询语言无法实现的新见解。Promscale 是唯一一款能够实现这一点的可观测性解决方案，这要归功于它对 SQL 的全面支持以及对 OpenTelemetry traces 的支持。随着这项功能的推出，用户可以访问现成的控制面板，这将有助于他们了解其应用程序的行为，因此他们可以立即开始故障排除

### **展望未来**

随着完全 OpenTelemetry 支持的发布，Promscale 现在更加强大，适合简单的企业级部署；为 Prometheus Metrics 和 OpenTelemetry traces 提供统一存储，全面的 SQL 和 PromQL 支持，使用户能够创建独特的仪表板，并提出旨在更好地了解被监控系统的问题。这是实现以下目标的重要一步:使每个工程师能够将所有可观测性数据(指标、日志、跟踪、元数据和其他未来数据类型)存储在一个成熟且可扩展的存储中，并通过一个统一且完整的 SQL 界面对其进行分析。更多详情 [此处](https://www.timescale.com/blog/what-are-traces-and-how-sql-yes-sql-and-opentelemetry-can-help-us-get-more-value-out-of-traces-to-build-better-software/#anatomy-of-an-opentelemetry-trace)

立即开始在您的环境中部署 Promscale[](https://docs.timescale.com/promscale/latest/installation/)或 [安装轻量级 OpenTelemetry 演示](https://github.com/timescale/opentelemetry-demo/) ，其中包括一个微服务应用程序和一个在 prom scale 上运行的完整 OpenTelemetry observability 堆栈。

**关于时间刻度**

Timescale 是 TimescaleDB 的创造者，time scale db 是业界领先的时间序列关系数据库，Promscale 是 SQL 支持的可观察性后端。如今，成千上万的组织信任 TimescaleDB，将其用于关键任务时序应用程序，Promscale 基于 TimescaleDB 构建，为云原生应用程序提供完整的可观察性堆栈。时标是一家拥有全球员工的远程优先公司，得到了 Tiger Global、Benchmark Capital、New Enterprise Associates、Redpoint Ventures、Icon Ventures、两家适马风险投资公司和其他主要投资者的支持。详情请访问 www.timescale.com[](http://www.timescale.com/)或关注[@ TimescaleDB](https://twitter.com/timescaledb)。

**联系人** 凯尔文史蒂夫 高级通讯经理 [【邮件受保护】](/cdn-cgi/l/email-protection#24545641575764504d494157474548410a474b49)