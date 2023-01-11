# ScyllaDB 宣布发布其开源 NoSQL 数据库 4.0 版本

> 原文：<https://devops.com/scylladb-announces-4-0-release-of-its-open-source-nosql-database/>

### 新版本增加了 DynamoDB 兼容的 API 以及一致性、流和管理的高级功能

加利福尼亚州 PALO 阿尔托，2020 年 5 月 7 日(环球新闻通讯社)——[ScyllaDB](https://www.globenewswire.com/Tracker?data=bvUq-akKVg81ByeODxLTH9LK7npNlYAkPr0uRjvkgQhk2E19ncNuh3pxKFQpJU9ZIneiYXXa__7kM2V-3uabFA==)今天宣布推出 Scylla 开源 4.0，这是其针对实时大数据工作负载的高性能 NoSQL 数据库的最新主要版本。这一版本标志着一个重要的里程碑，因为该公司已经超越了与 Apache Cassandra 的功能对等，现在也作为 Amazon DynamoDB 的开源插件，无锁定替代品。

Scylla 开源 4.0 建立在 Scylla 的接近硬件的设计之上，这使得现代服务器基础设施的最佳使用成为可能。Scylla 是用 C++从头开始编写的，在单个节点上提供数百万次操作的性能，可扩展到数百个节点，并始终实现 99%的尾部延迟不到 1 毫秒。

作为 Cassandra 和现在的 DynamoDB 的替代产品，Scylla 提供了更好、更一致的性能，显著降低了总拥有成本(TCO)和更大的部署灵活性。Scylla 开源 4.0 中的生产就绪型新功能扩展了 Cassandra 已经令人印象深刻的一系列优势，包括扩展到任意数量的内核、将数据传输到 60TB 兆节点、内置调度程序、统一缓存和自调优操作。

性能比较显示，Scylla 开源 4.0 比 5X 提供了更高的吞吐量，比即将发布的 Apache Cassandra 4.0 版本的 P99 延迟低近 10 倍。此外，基准测试表明，Scylla 的总成本大约是 Amazon DynamoDB 的 1/8。

机器人先驱库卡公司的首席软件工程师 Devin Rose 说:“Scylla 比我们评估的其他 NoSQL 数据库更快、更容易管理。“我们考虑了其他几种选择，但事实证明 Scylla 更划算。我们对锡拉增加的新功能感到兴奋。他们新的 DynamoDB 兼容 API 将使用户更容易享受 Scylla 的性能优势、经济性和更灵活的部署选项。”

**Scylla 开源 4.0 的新功能**

*   **交流发电机，兼容 DynamoDB 的 API:** Scylla 4.0 提供了一个生产就绪的兼容 Amazon DynamoDB 的 API，允许 DynamoDB 用户切换到 Scylla，而无需更改一行应用程序代码。Scylla 显著降低了总拥有成本，提供了更低、更一致的延迟，并扩展了 DynamoDB 对对象大小、分区大小等的限制。开发人员不再局限于某个平台，他们可以使用新的开源选项。他们可以在内部运行，在他们首选的云平台上运行，或者在 Scylla 完全托管的数据库服务上运行， [Scylla Cloud](https://www.scylladb.com/product/scylla-cloud/) 。他们可以自由地访问他们的数据，不需要支付每次操作的费用，并且有更多的部署选项，包括开源的 Docker 和 Kubernetes。
*   **轻量级事务(LWT):** Scylla 的轻量级事务(LWT)扩展了 Scylla 的数据一致性选项。通过使用 Paxos 两阶段提交,“锡拉 LWT”使操作高度一致。
*   **变更数据捕获(Beta):** 允许用户跟踪其数据的变更，将原始数据值和新值记录到记录中。借助 CDC，Scylla 将更改流式传输到标准的 CQL 表中，该表可以被索引或过滤，以找到数据的关键更改。新的 API 提供了优于 Cassandra 和 DynamoDB 的功能。
*   **Kubernetes Operator for Scylla(Beta):**[Kubernetes](https://kubernetes.io/)支持云原生容器化应用的自动化供应，支持部署、扩展和管理的整个生命周期。 [Scylla Operator](https://github.com/scylladb/scylla-operator) ，现在是 Scylla 4.0 的测试版，是对 Scylla 集群管理的 Kubernetes 扩展。它目前支持部署多区域集群，扩展或添加新机架，缩小和监控带有 Prometheus 和 Grafana 的 Scylla 集群。

“Scylla 4.0 是我们有史以来最大的版本，从易用性到新的 API、功能和性能都有所改进，”ScyllaDB 首席执行官兼联合创始人 Dor Laor 说。“我们欢迎开发者发现 Scylla 提供的开箱即用、价格合理且不受限制的卓越性能。”

更多关于锡拉开源 4.0 的信息，请访问[scylladb.com](http://scylladb.com/)。

**即将举行的网络研讨会:** ***介绍 Scylla 开源 4.0***
5 月 21 日，与 Scylla 联合创始人 Dor Laor 和 Avi Kivity 一起概述 Scylla 开源 4.0，包括与即将发布的 Apache Cassandra 4.0 的比较。注册:[https://go . scylladb . com/WBN-Scylla-open-source-4.0-registration . html](https://go.scylladb.com/wbn-scylla-open-source-4.0-registration.html)

**关于 ScyllaDB**
Scylla 是实时大数据数据库。API 兼容 Apache Cassandra 和 Amazon DynamoDB，Scylla 采用无共享方法，将吞吐量和存储容量提高到 Cassandra 的 10 倍。康卡斯特、星巴克、Ola Cabs、三星、IBM、Grab、MediaMath、AppNexus、Investing.com 和 [更多的领先公司](https://www.globenewswire.com/Tracker?data=on4xq9SPl4XD06eVyyVPJK6_G_znHSFFCA7H3_k9UoeGOutql9mqVx1vyUQgoirJCnvU1vuUqweCg4ut0HC7IhSaIycDdZUk8BoWEl1vxf8nr6PNvmFWhj_2a9O4DNo6) 已经采用 Scylla 实现数量级的性能提升并降低硬件成本。ScyllaDB 由负责 KVM 虚拟机管理程序的团队创建，并得到 Bessemer Venture Partners、Eight Roads Ventures、Innovation destinations、Wing Venture Capital、Qualcomm Ventures、TLV Partners、Magma Venture Partners、西部数据资本和 Samsung Ventures 的支持。更多信息:[ScyllaDB.com](https://www.globenewswire.com/Tracker?data=bvUq-akKVg81ByeODxLTH6wMVH93Rj_jvM_4OXQwwSlgh-IfRepmzjIp6vmALwqq3uLDSil2OAzt_85iM_Z0UQ==)