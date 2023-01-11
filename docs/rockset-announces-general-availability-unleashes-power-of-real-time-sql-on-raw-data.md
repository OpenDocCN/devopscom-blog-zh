# Rockset 宣布全面上市；在原始数据上释放实时 SQL 的威力

> 原文：<https://devops.com/rockset-announces-general-availability-unleashes-power-of-real-time-sql-on-raw-data/>

## *行业首款无服务器搜索和分析引擎让开发人员和数据科学家从 ETL 中解放出来*

**加州圣马特奥——2019 年 3 月 19 日——**[无服务器搜索和分析公司 Rockset](https://www.rockset.com/) 今天宣布业内首款云服务全面上市，该服务允许开发人员和数据科学家在几分钟内而不是几周内将复杂的数据集投入使用。

当前的技术趋势——智能设备、数字借贷、欺诈检测、全渠道零售、机器学习、微服务和实时业务仪表盘——都需要来自多个来源的干净数据。然而，企业正在数据湖、NoSQL 数据库和数据流等分散系统中处理大量高价值、低质量的数据。越来越多的数据来自不同的来源，往往是 JSON、CSV、XML 和 Parquet 格式的机器数据或 XLSX 和 PDF 等业务数据。Rockset 使团队能够使用来自多个来源的各种数据格式来服务数据密集型应用程序，而不必对模式建模或管理脆弱的提取-转换-加载(ETL)管道。

“现代数据集杂乱无序。Rockset 的联合创始人兼首席执行官 Venkat Venkataramani 说:“传统的数据管理系统迫使团队花费超过 50%的时间来准备和加载这些数据集。“如果不能立即使用新数据并快速迭代，收集新数据又有什么意义呢？Rockset 以一种新的开发人员友好的方式重新设计了堆栈，对原始数据使用快速 SQL，因此您可以在几分钟内从数据转到应用程序。”

Rockset 是业内首个无服务器数据后端，可在生成原始数据时持续接收原始数据，并大规模提供实时 SQL 查询。其正在申请专利的 Converged Indexing 结合了倒排索引、分栏索引和文档索引，针对开箱即用的键值、时间序列、文档、搜索、聚合和图形类型查询进行了优化。它由 RocksDB 提供支持，结合其云原生分布式查询引擎，提供实时操作应用程序和交互式数据科学所需的性能和规模。

此版本提供了新的功能，包括:

*   从包括 Apache Kafka、Amazon Kinesis、Amazon DynamoDB、Amazon S3 和 Google 云存储在内的数据湖、数据库和流中进行持续的无模式接收
*   JSON、XML、CSV、Parquet、Excel 和 PDF 的智能模式
*   SQL，包括 1000 多个 QPS 的连接
*   面向 Java、Python、Node.js、Golang 和 REST API 的 SDK
*   通过自助式访问交付“即服务”

**开发人员和数据科学家社区采用 Rockset**

“我们需要实时仔细地监控我们的增长。是不是某个产品突然卖多了？是否存在欺诈交易？我们每天轻松生成 2000 万到 3000 万个事件，都是在 Kafka 流中捕获的。我们的应用程序每隔几秒钟就查询一次数据。通过将我们的原始事件数据直接从 Kafka 发送到 Rockset，我们节省了大量的时间和精力。我们实时跟踪 40 多项指标，并不断采取即时行动。”

-Amboj Goyal，Fynd 首席工程师，该公司是线上线下零售领域的领导者，拥有一个时尚电子商务门户，帮助数百万顾客从当地商店找到时尚产品。

“我们从许多不同的来源以许多不同的格式接收数据——每种格式都有不同的分隔符、标题和转义符。将数据加载到多个系统、单独推断模式和处理格式错误的数据非常耗时。当接收到新版本的数据时，我们还要处理不断变化的模式。Rockset 有可能解放我们的数据科学家，让他们在原始数据上运行专门的 SQL 查询，同时最大限度地减少 ETL 工作和维护。”

-科技行业对冲基金 Coatue 的数据科学主管亚历克斯·伊兹多尔奇克(Alex Izydorczyk)，该基金以数据能力著称，投资于公共和私人股本市场。

**正式上市**

Rockset 是由一个行业资深人士团队创建的，他们在网络规模数据管理和分布式系统方面拥有数十年的经验，曾供职于脸书、雅虎、谷歌、甲骨文和 VMware 等公司。11 月，公司[从隐身状态](https://www.rockset.com/press/rockset-reimagines-data-driven-apps/)中脱颖而出，宣布[获得 2150 万美元的资金](https://www.rockset.com/press/rockset-raises-series-a-greylock-sequoia/)。Rockset 通常立即可用。更多信息，请通过 [【电子邮件保护】](/cdn-cgi/l/email-protection#5139343d3d3e11233e323a2234257f323e3c) 联系 Rockset。

**关于 Rockset**

Rockset 是一个无服务器的搜索和分析引擎，可以轻松地从数据到应用程序。Rockset 由脸书的前工程领导者创建，由 Greylock Partners 和红杉资本提供支持。更多信息，请前往[rockset.com](https://rockset.com/)或关注[的 Rockset @ Rockset cloud](https://twitter.com/rocksetcloud)。