# Hazelcast 提升领先地位，降低采用内存数字集成集线器的障碍

> 原文：<https://devops.com/hazelcast-advances-leadership-lowers-barrier-of-adoption-to-in-memory-digital-integration-hubs/>

*最新版本的 Hazelcast IMDG 增加了 SQL 支持，提高了可靠性，简化了云中的集群发现等等*

**加州圣马特奥，2020 年 9 月 9 日**–[领先的开源内存计算平台 Hazelcast](https://hazelcast.com/) 今天宣布了其内存数据网格(IMDG)[hazel cast IMDG](https://hazelcast.com/products/imdg/)的一项新的主要功能和多项增强功能。这些更新包括对使用 SQL 管理分布式数据的预览支持、对 Kerberos 的开箱即用支持、针对英特尔 Optane DC 持久内存模块的额外调整选项以及更快的集群重新平衡。借助最新版本的 Hazelcast IMDG，数字集成中心等用例获得了更高的性能、可扩展性和弹性。

业务领导者需要定制的数据视图，而数据源的激增给传统架构和基础设施带来了压力。应对这些挑战的一个新兴解决方案是一种新的架构，即数字集成中心，这是一种提供单一接入点和标准化 API 的数据架构，可由多个应用程序调用。这些中枢通常被部署来减少后端系统上的工作负载，加速对后端数据库和大型机中托管的数据的访问，并为各种数据源提供公共 API，以将新技术集成到遗留架构中。Hazelcast 通过提供 RAM 中的对象存储、直写缓存、分布式处理和到许多流行数据源的预定义连接器，增强了成熟的内存数字集成中心。

“向新的数据通道发展遗留架构，特别是那些具有异构后端的架构，提出了一个技术挑战，即如何将所有部分组合在一起，同时保持整体复杂性的可维护性。Hazelcast 首席执行官 Kelly Herrell 表示:“数字集成中心为多个应用程序可以统一调用的后端数据源提供了一个中央访问点。“鉴于集线器是这些架构的核心组件，它需要快速、可扩展、可靠和安全。Hazelcast 内存计算平台提供了必要的功能，不仅能够满足大型企业的需求，而且在使用这些创新的新型数字集成中心架构时，能够显著简化部署和运营体验。”

**引入 SQL 支持**

为了补充包括 Java 在内的语言的现有 API。NET，Node.js，Python，C++和 Go，Hazelcast IMDG 正在引入 SQL 支持。将这一功能添加到哈泽卡斯特 IMDG 公司使数字集成中心能够使用一个通用的众所周知的 API 来检索数据。使用索引来加速查询，以及根据属性过滤结果的能力，将 Hazelcast IMDG 扩展到基本键值存储的有限的按键查询能力之外。熟悉等同于简化开发和降低实现成本。

Hazelcast 首席产品官 David Brimley 表示:“鉴于开发人员对 SQL 的广泛熟悉，SQL 支持的增加大大缩短了学习曲线，并为企业利用内存计算平台的优势开辟了新的机会。“有了 SQL，让哈兹卡斯特 IMDG 公司并行地从多个节点检索数据并确保正确性而不引入额外的开发成本就更简单了。”

在此版本中，SQL 支持旨在对已经填充了数据的 Hazelcast IMDG 地图进行“选择”查询。在未来的版本中，将会添加附加功能，如连接、聚合和排序。

**加速集群重新平衡和改进网络故障检测**

由于数字集成中心是业务关键型应用程序的主要访问点，任何停机都可能带来重大损失，包括潜在的收入和/或客户损失。如果发生硬件故障，如计算机崩溃，群集必须通过升级丢失分区的备份来立即恢复丢失的数据。但是，恢复过程仍然需要跨集群重新平衡分区。在此版本中，Hazelcast 引入了并行分区迁移，可加速集群重新平衡，并将处于次优状态的时间减少一个数量级。例如，如果网络断开负责存储 4tb 数据的 10 节点群集中的一个节点，Hazelcast IMDG 公司将能够在大约 2 分钟内完成分区重新平衡，而以前需要至少 33 分钟。

为了进一步降低停机的可能性，哈泽卡斯特 IMDG 公司利用 Bron–ker bosch 算法的实施提高了其部分网络故障检测能力。这种增强意味着在 Hazelcast IMDG 集群必须从难以检测的网络故障中恢复的情况下，提高了高可用性。

**现成的 Kerberos 认证**

Hazelcast 正在引入对 Kerberos(一种广泛使用的身份验证协议)的一流的开箱即用支持。通过将 Kerberos 支持集成到 Hazelcast IMDG 中，大大减少了与手动集成相关的工程时间和风险。Kerberos 协议补充了 Hazelcast IMDG 企业的企业级安全套件。

**经济高效的数据、云友好更新等**

通过与英特尔的持续合作工程活动，Hazelcast 继续优化其平台，以充分利用英特尔 Optane DC 持久性内存模块。此版本的特点是能够使用系统中安装的所有英特尔 Optane 持久性内存模块，从而使企业能够构建经济高效的 TB 级内存部署。此外，Hazelcast 增加了性能调整选项，可将系统吞吐量提高 50%，在特定使用案例中以一半的成本获得接近 RAM 的速度。

作为应用程序现代化计划的一部分，最新版本提供了更简单的方法将哈泽卡斯特 IMDG 公司整合到现有架构中。特别是，IMDG 黑兹卡斯特公司现在能够:

*   使用一行配置在云中形成一个集群，将设置时间缩短到几秒钟
*   在不接触配置文件的情况下调整配置，以减少分布式设置(如 Kubernetes)的 DevOps 开销

**可用性**

[Hazelcast IMDG 4.1 测试版今天上市](https://hazelcast.org/imdg/download/)，预计将于今年晚些时候正式上市。

**附加资源**

*   Hazelcast IMDG 4.1 测试版发布了！【博客】
*   [Hazelcast IMDG 产品页面](https://hazelcast.com/products/imdg/) [Web]
*   [Hazelcast 和 IBM 边缘到云应用](https://hazelcast.com/resources/hazelcast-ibm-edge-to-cloud-applications/)[白皮书]
*   [多云部署:随时随地运行 Hazelcast 指南和视频]](https://hazelcast.com/resources/multi-cloud-deployments-run-hazelcast-anywhere-and-everywhere/)

**关于 Hazelcast 公司**

Hazelcast 提供内存计算平台，支持全球 2000 强企业在任何规模下实现超快应用性能。Hazelcast 的云原生内存数据存储和事件流处理软件技术专为低延迟数据处理而构建，受到了摩根大通、Charter Communications、Ellie Mae 和澳大利亚国家银行等领先公司的信任，可加速以数据为中心的应用。

Hazelcast 总部位于加利福尼亚州圣马特奥，在全球各地设有办事处。要了解更多关于 Hazelcast 的信息，请访问 https://hazelcast.com。