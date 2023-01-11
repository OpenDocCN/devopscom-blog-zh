# ScyllaDB 将兼容 Amazon DynamoDB 的 API 添加到数据库即服务产品中

> 原文：<https://devops.com/scylladb-adds-amazon-dynamodb-compatible-api-to-database-as-a-service-offering/>

### Scylla Cloud 简化了 DynamoDB 用户的迁移，增加了 Grafana 集成并扩展了灵活的新部署选项

加利福尼亚州 PALO 阿尔托，2020 年 6 月 10 日(环球新闻网)——Scylla db 今天宣布，它已经将最近推出的亚马逊 DynamoDB 兼容 API、 [交流发电机](https://www.globenewswire.com/Tracker?data=OqrcwowT2kOxdNDxWO_H1CeUt3uatvT63r81h_bUjTGf0ruO-_mGW81sse1htFiqeUkFEqaPfRfRk6DJqNWD9BhM7UfIWCAtdKeNVA1S5nI=) 添加到 Scylla Cloud，这是其 NoSQL 数据库的完全托管版本。Scylla Cloud 中的其他新功能包括与流行的开源监控工具 Apache Grafana 的集成，以及用户在自己的 AWS 帐户上运行 Scylla Cloud 的能力。

Scylla Cloud 为其他数据库即服务(DBaaS)选项提供了一种经济高效的替代方案。运行与 Amazon DynamoDB 和 Google Cloud BigTable 相同的工作负载，Scylla Cloud 的成本约为其五分之一。构建于 Scylla Enterprise 之上的 Scylla Cloud 能够处理数 Pb 的数据，每秒执行数百万次操作，具有可预测的低延迟。它允许应用程序的快速原型制作、部署和扩展，而没有数据库管理开销，最大限度地减少停机时间，并允许开发人员将高性能应用程序快速投入生产。

“我们对 Scylla Cloud 的性能和易用性印象深刻，”热门在线发布平台 Medium 的工程总监 David Zhao 表示。“Scylla Cloud 为我们提供了一个完全托管的数据库，让我们不必在数据库操作上花费宝贵的工程时间。我们是 ScyllaDB 的粉丝已经很久了。对于我们的应用程序，与其他 RDBMS 或 NoSQL 数据库相比，它提供了最佳的性价比。”

其他最近的锡拉云更新包括:

*   **在您自己的 AWS 帐户中运行 Scylla Cloud:**Scylla db 现在允许用户选择在哪里部署他们完全托管的 Scylla Cloud 数据库:通过他们的 Scylla Cloud 帐户或在他们自己的 AWS 帐户中。这个新选项允许锡拉云用户保留所有锡拉资源(EC2，VPC，S3 桶，等等。)同时保持自己的 AWS 定价、公司政策和地理法规。
*   **Grafana 集成:** Scylla Cloud 现在直接与广泛使用的 Grafana 多平台开源解决方案集成，用于运行数据分析，提高 Scylla 云集群性能的可观察性。
*   **提取普罗米修斯指标:** Scylla Cloud 现在支持以[普罗米修斯](https://prometheus.io/)格式提取集群指标。提取的统计数据可以用 [Scylla 监控栈](https://docs.scylladb.com/operating-scylla/monitoring/)或者任何其他支持 [Prometheus 格式](https://github.com/prometheus/docs/blob/master/content/docs/instrumenting/exposition_formats.md)的监控工具查看，比如 [Datadog](https://www.datadoghq.com/blog/monitor-scylla-with-datadog/) 。

ScyllaDB 联合创始人兼首席执行官 Dor Laor 表示:“DynamoDB 用户经历了高数据库成本带来的巨大冲击，现在可以轻松地迁移到更具成本效益的替代方案，这种方案有更多的部署选项。"他们现在也可以利用其他开源工具，如 Grafana 和 Prometheus . "

如需了解更多关于锡拉云的信息，或注册账户，请访问[【scylladb.com】](https://www.globenewswire.com/Tracker?data=tFnSmFVN2uwKgkyqTqGMPMO_87oFh6WChyDs3kdy1VsNm7Mi7DyHx7RzmaxLdxbERd-cUZqwtfWhj-Pa3dTPuA==)。

**关于 ScyllaDB**
Scylla 是实时大数据数据库。API 兼容 Apache Cassandra 和 Amazon DynamoDB，Scylla 采用无共享方法，将吞吐量和存储容量提高到 Cassandra 的 10 倍，同时显著降低总拥有成本。Comcast、Starbucks、Ola Cabs、Samsung、IBM、Grab、MediaMath、AppNexus、Medium、Santander 和[更多的领先公司](https://www.globenewswire.com/Tracker?data=GZfZQg8cnFdl1uzt82ZrTRu_5vFnm3iGJ_GsMGEuFj5o2Uk9qzkdLLQ4LYzkfcOEuQ7Y08VJxDlHcvBgmaSwJgA9mbiCLHVgmHAuMa_tNq58PIzOtE1sWwjhrs6amC9J)已经采用 Scylla 实现数量级的性能提升并降低硬件成本。ScyllaDB 由负责 KVM 虚拟机管理程序的团队创建，并得到 Bessemer Venture Partners、Eight Roads Ventures、Innovation destinations、Wing Venture Capital、Qualcomm Ventures、TLV Partners、Magma Venture Partners、西部数据资本和 Samsung Ventures 的支持。更多信息:ScyllaDB.com