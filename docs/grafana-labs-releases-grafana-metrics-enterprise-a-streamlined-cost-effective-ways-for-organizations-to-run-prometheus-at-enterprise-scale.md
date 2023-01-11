# Grafana Labs 发布了 Grafana Metrics Enterprise，这是一种简化的、经济高效的企业级运行 Prometheus 的方法

> 原文：<https://devops.com/grafana-labs-releases-grafana-metrics-enterprise-a-streamlined-cost-effective-ways-for-organizations-to-run-prometheus-at-enterprise-scale/>

***Grafana Metrics Enterprise 还允许公司为内部客户提供 Prometheus 即服务。***

**纽约州，2020 年 9 月 17 日** —今天， [Grafana Labs](http://www.grafana.com/) 宣布发布 [Grafana Metrics Enterprise](https://grafana.com/products/metrics-enterprise/) ，这是一款现代化的 Prometheus 即服务解决方案，旨在满足企业在扩展其可观测性计划时的规模、架构和安全需求。Grafana Metrics Enterprise 为大公司提供了一种更简单、更具成本效益的方式来大规模运营 Prometheus。

Prometheus 是围绕 Kubernetes 的云原生生态系统的事实上的监控系统，已经大受欢迎，但在企业级采用该技术存在许多挑战。Grafana Labs 已经帮助大量客户通过 Grafana Cloud 大规模运行 Prometheus，降低了运营复杂性，Grafana Cloud 由开源、可横向扩展的 Prometheus 实施 [Cortex](https://cortexmetrics.io/) 提供支持。

这些经验构成了 Grafana Metrics 企业产品的基础。Grafana Metrics Enterprise 也是基于 Cortex 构建的，Cortex 最近[被提升为云本地计算基金会孵化器](https://grafana.com/blog/2020/08/20/cortex-the-scalable-prometheus-project-has-advanced-to-incubation-within-cncf/)——这标志着该项目已经达到了成熟和采用的健康水平。Grafana Labs 重金投资 Cortex 项目；八名维护者中的五名，包括该项目的共同创建者，都受雇于 Grafana Labs。

借助 Grafana Metrics Enterprise，大公司可以受益于:

可扩展性和更低的成本。世界领先的效率、可扩展性和性能使企业能够经济高效地将其所有应用和基础设施指标存储在一个集中式集群中，或跨多个 Grafana Metrics 企业集群。同类最佳的查询性能意味着用户可以驱动整个组织的实时仪表盘和洞察力。

为企业构建的架构。Prometheus 的拉式架构可能很难在企业环境中采用，并且通常与他们的网络拓扑和防火墙规则不兼容。Grafana Metrics Enterprise 带来了 Prometheus(灵活的多维数据模型；强大而简洁的 PromQL 查询；复杂的 SRE 级警报)以更符合企业架构需求的方式提供给企业。集中式、可水平扩展的复制架构是企业所熟悉的。而且依赖性极小:组织只需要提供与 S3 兼容的存储。

安全。Grafana Metrics Enterprise 增加了企业大规模采用 Prometheus 所需的安全功能:本机多租户、内置身份验证、数据访问策略和集群联合允许管理员控制其指标的位置以及谁可以使用它们。数据可以保存在当前所在的任何地方——无论是在欧盟、中国还是其他地方——用户仍然可以查询其指标的全球视图。

易用性。Grafana Metrics Enterprise 包括嵌入在 Grafana Enterprise 中的 API 驱动的管理 UI。还有一个简化的 UI 用于管理集中式 Prometheus 警报，因此无需手动编辑和管理配置文件。Grafana Metrics Enterprise 订阅包括帮助组织实施 Prometheus 和 Grafana Metrics Enterprise 的支持。

可组合的解决方案。通过 Grafana Metrics Enterprise，企业可以将 Graphite 和 Prometheus 监控统一起来，作为现代化、可组合的可观测性解决方案的一部分。还可以有选择地将指标运送到数据湖或其他存储系统中，以满足数据湖的需求，从而帮助组织迁移和现代化现有系统。

“在 Grafana Labs，我们一直在帮助世界上一些最大的企业采用 Prometheus。通过这次经历，我们了解了应对这些挑战需要什么，并将解决方案融入 Grafana Metrics Enterprise。如果你想在一个大型组织中采用普罗米修斯，这款软件正适合你。”— Tom Wilkie，Grafana Labs 产品副总裁，Prometheus 维护者和 Cortex 共同创造者

有关 Grafana Metrics Enterprise 的更多信息，请参加 Grafana Labs 9 月 23 日的网络研讨会[在企业中采用 Prometheus](https://grafana.com/go/webinar/adopting-prometheus-enterprise/)。

8 月，Grafana 宣布投资[5000 万美元](https://grafana.com/about/press/2020-08-17-series-b-announcement/)，并承诺优先进行研发投资，包括加速 Grafana Metrics Enterprise 的发展，现已上市。