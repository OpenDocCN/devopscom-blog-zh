# Rockset 在实时分析性能方面树立了行业标准

> 原文：<https://devops.com/rockset-sets-industry-standard-in-real-time-analytics-performance/>

***根据查询性能的星型模式基准*** 进行测量，Rockset 比备选方案快 9.4 倍

**加州圣马特奥，2021 年 2 月 18 日—** [实时索引数据库公司 Rockset](https://rockset.com/) 今天宣布，它发布了新的基准测试结果，显示了针对星型模式基准测试(SSB)的毫秒级延迟查询性能。当与测量数据延迟的基准测试工具 [RockBench](https://rockset.com/blog/rockset-1-billion-events-in-a-day-with-1-second-data-latency/) 结合使用时，Rockset 是唯一一个发布基准测试的实时分析解决方案，该解决方案显示其执行查询的速度比其他解决方案快 9.4 倍，并且每天接收 10 亿个事件，数据延迟仅为 1 秒。

实时分析解决方案的性能可以从两个方面来衡量:数据延迟和查询延迟。随着对实时分析的需求变得越来越重要，技术堆栈需要一个能够实现高写入速率和低延迟查询的数据库，从而使应用程序能够实时运行。一旦数据变得可查询，应用程序必须迅速采取行动，为最终用户提供即时的洞察力。未能满足延迟要求可能会导致错失机会、无法检测到威胁或用户体验不佳。低延迟是目前依赖实时分析的各种用例的关键要求，包括商业网站、实时供应链物流和交付跟踪系统、游戏排行榜、欺诈检测系统、健康和健身跟踪器、社交媒体新闻源等。

作为一个被广泛认可的行业标准基准，SSB 旨在测量分析应用程序的数据库性能，从而对 Rockset 在一系列常见分析查询上的查询性能提供有价值的见解。对 SSB 的研究结果显示，Rockset 执行的每个查询都有亚秒级的延迟，所有查询的平均响应时间为 254 毫秒。Rockset 平均比开源替代方案快 1.5 倍，其中一个查询的执行速度快 9.4 倍，大多数查询的执行速度快 2 倍、3 倍或 4 倍。SSB 的 13 个查询在 4，146 毫秒内完成。

Rockset 的主要竞争优势在于，它在 Converged Index 中索引所有字段，包括嵌套字段，Converged Index 结合了倒排索引、列索引和行索引。SQL 优化器并行使用这些索引，利用选择性查询模式并加速大量记录的聚合，以显著降低的计算成本实现毫秒级延迟。Rockset 的执行引擎是使用矢量化技术从头开始构建的，与传统的基于行的引擎相比，它提供了数量级的加速。此外，新版本支持基于列的集群，用户可以根据他们指定的集群键来存放数据。这最大化了顺序访问的机会，并减少了每次查询需要扫描的数据量。

虽然这些发现证明了 Rockset 提供实时分析所需的低延迟查询的能力，但该公司还在 2020 年 9 月[发布了 RockBench](https://rockset.com/blog/rockset-1-billion-events-in-a-day-with-1-second-data-latency/) :一种衡量从数据产生到可以查询的时间的基准，显示了应用程序的数据延迟——这是目前大多数数据库基准中很少优先考虑的因素。根据 RockBench 衡量 Rockset 表明，Rockset 4XLarge 虚拟实例可以支持每天流入的 10 亿个事件，同时将数据延迟保持在 1 秒以内。

“实时分析需要对新数据进行快速查询。Rockset 首席执行官兼联合创始人文卡特·文卡塔拉马尼(Venkat Venkataramani)表示:“我们的使命是让实时分析比当前的替代产品(如 Elasticsearch 和 Apache Druid)更快、更灵活、更简单。“当今的现代数据应用需要速度和规模。作为一个大规模分布式系统，Rockset 是为云规模而设计的。我们的 SSB 结果证明，Rockset 是当今市场上最快的实时分析解决方案之一。”

有关 Rockset 上 SSB 的更多信息，请阅读该公司的[博客](https://rockset.com/blog/rockset-up-to-9x-faster-than-apache-druid-star-schema-benchmark/)和[白皮书](https://rockset.com/star-schema-benchmark)以了解有关结果和方法的更多信息。

**支持资源**

*   Blog: [在星型模式基准测试中，Rockset 比 Apache Druid 快 9.4 倍](https://rockset.com/blog/rockset-up-to-9x-faster-than-apache-druid-star-schema-benchmark/)
*   白皮书:[基于星型模式基准的 Rockset 性能评估](https://rockset.com/star-schema-benchmark)
*   [Rockset 网站](https://rockset.com/)
*   [Rockset 博客](https://rockset.com/blog/)
*   [Rockset 最新消息](https://rockset.com/company/)
*   [在 Twitter 上关注我们](https://twitter.com/rocksetcloud)
*   [在 LinkedIn 上加入我们](https://www.linkedin.com/company/rocksetcloud/)

**关于 Rockset**

Rockset 是一个云中的实时数据库，由一个行业资深人士团队构建，他们在脸书、雅虎、谷歌、甲骨文和 VMware 等公司的网络规模数据管理和分布式系统方面拥有数十年的经验。Rockset 得到了 Greylock 和 Sequoia 的支持。更多信息，请前往[rockset.com](https://rockset.com/)或关注 [@RocksetCloud](https://twitter.com/rocksetcloud) 。