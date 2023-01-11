# Grafana 实验室寻求简化可观测性

> 原文：<https://devops.com/grafana-labs-looks-to-simplify-observability/>

Grafana Labs 在今天的在线[observibility con](https://grafana.com/about/events/observabilitycon/)会议上公布了一个名为 Grafana Tempo 的[分布式追踪](https://devops.com/?s=distributed%20tracing)平台，该平台使[利用现有的对象存储平台和服务来分析痕迹](https://grafana.com/blog/2020/10/26/observabilitycon-2020-your-guide-to-the-newest-announcements-from-grafana-labs/)成为可能。

与此同时，Grafana Labs 宣布了 Loki 的 2.0 版本，该版本规范了不同的结构化、非结构化或 JSON 日志格式，允许 DevOps 团队提取额外的标签，并支持额外的过滤和分组。IT 团队也不需要预先定义标签并将这些标签存储在数据库中。

Loki 2.0 查询还可以使用新的分布式规则评估引擎直接生成警报语句。在此之前，Loki 必须被配置为 Prometheus 数据源，这将允许 Prometheus 的分布式实例 Grafana 生成警报。

Grafana Labs 的产品副总裁 Tom Wilkie 表示，Loki 2.0 还可以使用于实时观察事件的数据库变得更小，从而加快查询速度。他说，结果是一种比传统平台便宜得多的分析日志数据的方法，并指出 DevOps 团队应该期待看到 Grafana Labs 也使用 Loki 来解决安全用例。

Wilkie 表示，Loki 和 Grafana Tempo 都旨在减少实现可观测性的障碍，这种方式不需要 DevOps 团队花费太多的时间、精力和技能。Grafana Tempo 支持与 Loki 使用的相同的 Tempo 数据发现引擎，以及基于 Prometheus 构建的开源 Prometheus 监控平台和 Grafana 平台。这种程度的集成使 it 团队更容易使用 Jaeger、Zipkin 和 OpenTelemetry 等开源跟踪协议来缩小特定跟踪的范围。他说，该平台的用户可以很容易地在日志和跟踪之间切换。

Wilkie 补充说，也没有必要建立和维护 IT 团队必须维护的单独索引。此外，Tempo 与云服务上常见的对象存储系统兼容，因此与依赖专有数据库的平台相比，实现可观测性的总成本显著下降，他说。

尽管可观察性是 DevOps 的核心原则，但它仍然是大多数 it 组织难以实现的目标。用于监控单个应用和系统的工具并不缺乏，但是将这些工具生成的所有数据整合成可操作的情报需要大量的时间和精力。Wilkie 说，Loki 使在正确的时间分析相关日志变得更加容易，普通 it 管理员可以导航，而不必成为更复杂平台的超级用户。

现在说可观测性战争将如何结束还为时过早。从 IT 角度来看，好消息是至少现在不缺乏选择。