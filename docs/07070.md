# 随着 InfluxDB 2.0 的全面发布，InfluxData 提高了时间序列数据的可能性

> 原文：<https://devops.com/influxdata-advances-possibilities-of-time-series-data-with-general-availability-of-influxdb-2-0/>

领先的开源软件具有增强的物联网和边缘功能&公司推出创新存储引擎的新项目

旧金山— [时间序列数据库 InfluxDB 的创建者 InfluxData](https://www.influxdata.com/) ，今天宣布面向时间序列数据的下一代开源平台 InfluxDB 2.0 正式上市。开发人员现在可以在一个统一的平台上接收、查询、存储和可视化时间序列数据，利用新的工具和集成，并使用熟悉的技能，使开发和部署现代基于时间的应用程序比以往任何时候都更快、更容易。此外，该公司宣布了一个新的开源项目，以重塑存储。

产生的数据量预计将从 2019 年的 45zb 呈指数级增长到 2025 年的 175ZB，主要来自应用程序、网络、容器和预计的 600 亿物联网设备，其中大部分是带时间戳的数据( [IDC](https://www.seagate.com/files/www-content/our-story/trends/files/dataage-idc-report-final.pdf) ，2020)。虽然组织有巨大的机会利用这些数据来改善客户体验、提高员工和流程生产率，并创造竞争优势，但存储和分析大容量和高频率的数据流将是一项挑战。这些工作负载将需要快速接收、高级查询和边缘处理，以保持资源和成本效率，并最大限度地提高对最终用户的价值。InfluxDB 2.0 旨在应对未来的这些数据挑战。

InfluxDB 2.0 是一个时序平台，用于构建由时序数据驱动的物联网、分析和监控应用程序。InfluxDB 2.0 中的新功能旨在减少开发人员编写代码以开始使用和管理现有项目的时间，包括:

*   flux——第一个专门为时间序列数据构建的函数式查询和编程语言，它使得丰富和转换数据、构建预测以及识别异常和相关性成为可能

*   InfluxDB 模板–针对常见使用情形(如网络和物联网传感器监控)的单文件监控配置的不断增长的图库，允许用户分享他们的专业知识，并在几分钟内启动和监控

*   边缘功能—能够在摄取时聚合和分析时间序列数据，在这种情况下采取行动最有价值

*   客户端库——支持用流行语言编写和查询，极大地简化了与其他应用程序的集成，并使团队能够使用现有的编程语言技能

InfluxDB 2.0 还与 [InfluxDB Cloud](https://www.influxdata.com/blog/influxdb-cloud-2-0-launches-as-a-serverless-platform-for-time-series-data/) 紧密集成，InfluxDB Cloud 是一个无服务器、可弹性扩展、完全托管的时序数据库平台。通过共享 API，可以轻松地在 InfluxDB 2.0 和 InfluxDB Cloud 之间移动数据和工作负载，并且可以作为单个时序平台的组件一起使用，该平台旨在为开发人员提供灵活性和工具，以满足不断变化的业务和应用程序需求。

RedMonk 联合创始人 James Governor 表示:“如今，开发人员正在寻找作为托管服务交付的开源软件。“InfluxDB 2.0 通过集成 OSS、edge 和云服务来应对这种融合，旨在简化基于时间序列的大规模应用程序的构建和管理。”

该公司还公布了下一代存储引擎——project InfluxDB I0x 的计划。InfluxDB I0x 是一个新的强大的存储引擎，旨在执行不断增加的查询工作负载。InfluxDB I0x 取消了 InfluxDB 2.0 开源版本中固有的基数、数据大小和集群大小的限制，从而扩展了跨数千台服务器和数 Pb 数据的工作负载的可能性，这是对当前和其他产品许可的重大突破。大多数时序解决方案都是围绕严格的数据库结构设计的，这限制了处理高基数数据的能力，但 InfluxDB I0x 通过使用对象存储作为持久性层和管理层来控制 Kubernetes 中短暂运行的许多无状态查询、摄取和索引服务器，从而将存储与计算分开。它还使用行业标准协议和持久性(如 Apache Arrow Flight 和 Apache Parquet)显著扩展了 InfluxDB 生态系统。InfluxDB I0x 项目扩展了开源的允许性，并获得了 MIT 和 Apache 2.0 的双重许可，以强调 InfluxData 对纯开源的承诺。Dix 在 InfluxDays North America 的演讲中开放了 InfluxDB I0x 项目代码库，现在欢迎评论。

“我们致力于提高开发人员的工作效率，并渴望我们的社区开始使用 InfluxDB 2.0，这样他们就可以开始用时间序列数据做更多的事情，”InfluxData 的首席技术官兼创始人 Paul Dix 说。“但 InfluxDB 2.0 只是我们旅程的开始。我们希望开发者用我们的开源软件开发出令人敬畏的应用，不受许可限制和约束。”

InfluxDB 2.0 是 MIT 许可的——最自由的开源许可之一。InfluxDB 2.0 是 [InfluxDB 1.0](https://www.influxdata.com/blog/influxdb-1-0-ga-released-a-retrospective-and-whats-next/) 的继任者，后者于 2016 年 9 月正式上市。在过去的四年中，开源软件的下载量达到了数百万次，目前全球每天有超过 40 万个活跃实例。

InfluxDB 2.0 入门快速简单。对于现有的 InfluxDB 用户，这是从 1.x 版本的无缝升级，可以通过下载 InfluxDB 2.0 并运行单个命令来传输数据。新用户可以通过[下载并安装 InfluxDB 2.0](https://portal.influxdata.com/downloads/) 开始使用，并且可以在一分钟内收集时间序列数据。

关于 InfluxData
InfluxData 是领先的时间序列平台 InfluxDB 的创建者。我们支持思科、IBM、乐高、西门子和特斯拉等开发商和组织构建变革性的物联网、分析和监控应用。我们的技术是专为处理传感器、应用程序和计算机基础设施产生的大量带时间戳的数据而构建的。InfluxDB 易于启动和扩展，让开发人员有时间专注于赋予其应用程序竞争优势的特性和功能。InfluxData 总部位于旧金山，员工遍布美国和欧洲。更多信息，请访问[www.influxdata.com](http://www.influxdata.com/)并关注我们 [@InfluxDB](https://twitter.com/influxdb) 。

![](img/7c4dc8c5dc51e5e682e2e057462b3f35.png)