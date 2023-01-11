# GridGain 8.8 改进了它的多层数据库引擎，可以扩展到可用的内存容量之外，并满足不断增长的客户需求

> 原文：<https://devops.com/gridgain-8-8-advances-its-multi-tier-database-engine-to-scale-beyond-available-memory-capacity-and-meet-growing-customer-demand/>

### 提高存储利用率降低总体拥有成本；SQL 的扩展内存配额支持复杂的实时分析；增强的安全性允许静态数据加密

**加利福尼亚州福斯特市，2021 年 1 月 14 日**–[grid gain^(Systems)](https://www.gridgain.com/)，由 Apache Ignite 分布式数据库支持的企业级内存计算解决方案提供商，今天宣布了该公司最新发布的内存计算平台 [GridGain 8.8](https://www.gridgain.com/docs/8.8.1/release-notes/8.8.1/release-notes_8.8.1) 。该版本增强了对 GridGain 的多层数据库引擎的支持，该引擎可以跨内存和磁盘进行伸缩。这些变化使客户能够利用数据库的磁盘层来查询更大的数据集，降低总体拥有成本，并保护静态的敏感或个人数据。公司现在可以将 GridGain 用于更多的生产用例，从复杂的实时分析到关键任务的事务性工作负载。

GridGain 总裁兼首席执行官 Abe Kleinfeld 表示:“随着我们的客户扩大对 GridGain 的使用，他们越来越需要灵活性，以扩展超出可用内存容量的工作负载。“因此，我们将继续发展我们的数据持久性技术，以简化网格集群管理、减少磁盘需求和提高性能，同时降低总拥有成本和加快价值实现。更有效的磁盘利用率和更高的 SQL 内存配额相结合，使 GridGain 能够支持更大、更复杂的实时分析用例。”

GridGain 的多层数据库引擎使公司能够通过使用 Apache Ignite 作为可扩展到可用内存容量之外的数据库，来构建支持同一数据集上的事务和分析工作负载的现代应用程序。每当应用程序查询冷记录时，Ignite 都会为热数据分配内存并访问磁盘层。

### GridGain 8.8 的主要特性

*   *数据压缩*–减少存储数据所需的内存和磁盘空间。基于字典的缓存条目压缩建立在 Zstandard 库的基础上，一个预先训练的字典在现实场景中可以允许高达 60%的压缩率。如果负载模式受 I/O 限制，那么启用本机持久性可以节省空间，同时还可以提高性能。可在 GridGain 终极版。
*   *高级无缝磁盘空间碎片整理*–改进 GridGain 的持久性管理。碎片整理缩小数据文件并回收磁盘空间，同时仍将当前缓存的数据持久地存储在磁盘上。所有 GridGain 版本均有提供。
*   *节点或查询级别的 SQL 内存配额*–防止在执行需要大量内存空间的 SQL 查询时出现内存不足问题。对将数据卸载到磁盘层的支持使贪婪或复杂的分析查询能够在执行并将结果返回给应用程序的同时提取和处理千兆字节的数据。所有 GridGain 版本均有提供。
*   *透明数据加密*–通过加密静态数据提高存储在集群中的数据的安全性。管理缓存和主加密密钥的新过程支持生产环境中的数据加密。所有 GridGain 版本均有提供。

GridGain 将于 2021 年 2 月 3 日 10:00 PST / 1:00 EST 举办一场名为[“grid gain 多层数据库引擎的新进展”](https://www.gridgain.com/resources/webinars/new-advances-in-gridgains-multi-tier-database-engine)的网络研讨会。

### 有效性

GridGain 8.8 现已在[https://www.gridgain.com/resources/download](https://www.gridgain.com/resources/download)发售。

### 额外资源

要了解关于 GridGain 内存计算平台的更多信息:

*   [注册参加 2 月 3 日的网络研讨会](https://www.gridgain.com/resources/webinars/new-advances-in-gridgains-multi-tier-database-engine)“grid gain 多层数据库引擎的新进展”
*   查看[数据压缩演示](https://youtu.be/b6ZqqTYV4VA)
*   查看[透明数据加密演示](https://www.youtube.com/watch?v=EXiyih1x0DE)
*   阅读“[介绍网格内存计算平台](https://www.gridgain.com/resources/papers/introducing-gridgain-in-memory-computing-platform)”白皮书
*   从 [GridGain 开发者门户](https://www.gridgain.com/developer)和 [GridGain 网络研讨会](https://www.gridgain.com/resources/webinars)中获取知识
*   了解 GridGain 如何帮助[CTO&CIO](https://www.gridgain.com/persona/ctoscios)、[架构师](https://www.gridgain.com/persona/architects)、[业务决策者](https://www.gridgain.com/persona/business-decision-makers)和[开发人员](https://www.gridgain.com/persona/developers)
*   阅读 GridGain [客户成功案例](https://www.gridgain.com/experience/featured-customers)和[行业使用案例](https://www.gridgain.com/experience/industries)

### 关于网格系统

GridGain Systems 通过提供基于 Apache Ignite 的内存计算平台，正在彻底改变实时数据访问和处理。GridGain 平台的常见用例包括[应用程序加速](https://www.gridgain.com/experience/common-use-cases/application-acceleration)和作为[数字集成中心](https://www.gridgain.com/experience/common-use-cases/digital-integration-hub)，用于跨数据源和应用程序的实时数据访问。GridGain 解决方案被金融服务、软件、电子商务、零售、在线业务服务、医疗保健、电信、运输和其他主要行业的全球企业所使用，其客户包括 ING、Raymond James、美国运通、Finastra、UPS、惠普企业、微软、美国航空、安捷伦和联合医疗保健。

GridGain 为传统和新建应用程序提供了前所未有的速度、巨大的可扩展性和实时数据访问。部署在商用服务器的分布式集群上，GridGain 软件可以驻留在应用程序和数据层(RDBMS、NoSQL 和 Apache Hadoop )之间，不需要淘汰和替换现有的数据库，或者它可以部署为内存数据库。更多信息，请访问 gridgain.com 的[。](https://www.gridgain.com/)