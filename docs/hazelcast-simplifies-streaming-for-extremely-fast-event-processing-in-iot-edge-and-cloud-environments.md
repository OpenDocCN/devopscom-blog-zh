# Hazelcast 简化了流媒体，可在物联网、边缘和云环境中实现极快的事件处理

> 原文：<https://devops.com/hazelcast-simplifies-streaming-for-extremely-fast-event-processing-in-iot-edge-and-cloud-environments/>

*Hazelcast Jet 是一款轻量级、可扩展的实时流媒体引擎，适用于持续智能应用*

**加州帕洛阿尔托，2019 年 4 月 16 日**–[领先的内存计算平台公司 Hazelcast](https://hazelcast.com/) 今天宣布 Hazelcast Jet 正式上市，这是唯一一款不依赖外部系统的流媒体引擎。其结果是业界最快的流处理引擎，大大简化了从最小到最大规模部署的实施。

无论是部署在物联网传感器等受限环境中，还是云规模应用中，Hazelcast Jet 都能以超低延迟吸收、分类和处理大量数据，以支持持续的情报实践。

“SigmaStream 专注于高频数据，与一些在最受限制的环境中运营的全球最大公司合作。SigmaStream 首席执行官 Hari Koduru 表示:“通过将 Hazelcast Jet 的高性能流媒体引擎与我们的蜂鸟可视化和处理平台相集成，我们可以处理来自数十个频道的高频数据，并实时解决效率低下的问题。“如此出色的性能和优化使 SigmaStream 的客户缩短了项目时间，最终为他们节省了数百万美元。”

**单一系统设计**

通常，部署其他流引擎需要企业投入时间并忍受集成来自不同来源的多个组件的复杂性。例如，Flink 实现需要集成 Kafka、ZooKeeper、RocksDB、Hadoop 文件系统和资源管理器的组合来摄取、分类和处理数据。

Hazelcast Jet 极大地简化了部署，因为它是一个单一的轻量级系统，完美地解决了一系列复杂的架构需求。Hazelcast Jet 独特的单一系统设计能够快速实现价值，消除与多组件架构相关的成本和复杂性，并减少对多种技能组合的需求。

**行业最快的流媒体**

内部基准测试证明了 Hazelcast Jet 在极端规模下保持毫秒级速度的能力，而其他基于开源的项目则下降到秒级。由于分布式架构和内存处理，Hazelcast Jet 保持了超低延迟，无论规模如何。

“Hazelcast 再次为行业带来了强大的飞跃，这一次是通过从根本上简化流事件处理的实施方式，”Hazelcast 首席执行官 Kelly Herrell 说。“时间就是金钱，无论数据是在哪里生成的，只要能够在生成的那一刻就对其进行处理，无论是在金融交易柜台还是基于边缘的传感器，都会产生可衡量的商业效益。当时间很重要时，公司选择 Hazelcast，现在他们有了一个引人注目的灵活的流解决方案，可以在 Hazelcast Jet 中快速处理数据。”

重要的是，Hazelcast Jet 提供低延迟性能，无论规模如何，无论是在小格式硬件中的物联网边缘运行，还是作为数据中心和云中的大规模集群运行。

**随处跑**

Hazelcast Jet 的架构同时具有轻量级和高度可伸缩性，允许它在客户需要高性能流处理的任何地方运行。其较小的文件大小和架构提供了众多部署选项，包括 Kubernetes 微服务环境、私有数据中心、公共云和嵌入式应用。

它进一步简化了 Hazelcast Jet 的部署，可支持容器化工作负载，并经过验证可在 Pivotal Cloud Foundry 和 Red Hat OpenShift 云环境中运行。

**有弹性且有回弹力的**

随着工作负载的增加，Hazelcast Jet 的集群模型可以在不中断作业的情况下扩展和缩减。

Hazelcast Jet 集群可以离线运行而不会丢失数据，并且可以在不中断处理的情况下升级作业，这对于长期运行的连续流应用程序来说是一项重大优势。在发生故障时，内存中的数据复制提供了一种强大而高性能的容错方法，通过热重启实现快速恢复。内存中的数据也可以持续保存到磁盘，以备维护性停机或熄灯事件。

**机器学习建模**

大多数流媒体引擎使用批处理来管理数据，而 Hazelcast Jet 能够在接收时处理事件。通过实时处理，Hazelcast Jet 是服务于机器学习模型的可靠解决方案，这些模型需要最新的信息来为决策提供信息。

此外，Hazelcast Jet 与 TensorFlow 集成，可大规模运行实时分类和预测工作负载。客户可以选择是使用嵌入式、进程内 Java runner 还是远程 TensorFlow 服务选项。

**内存计算平台**

将 Hazelcast Jet 与 Hazelcast IMDG 相结合，使企业能够部署高性能、可扩展的内存计算平台，处理动态和静态数据。

Hazelcast 独特地为客户提供了利用通用架构和技能组合来接收和处理流数据的能力，同时还提供数据存储和计算，所有这些都具有行业领先的低延迟。

**可用性和资源** Hazelcast Jet 3.0 今天[可供下载](https://hazelcast.com/download/)。

有关 Hazelcast Jet 3.0 的更多信息，请访问以下附加资源:

*   [Hazelcast Jet 3.0 发布](https://hazelcast.com/blog/jet-3-0-is-released)
*   [Hazelcast Jet 产品页面](https://hazelcast.com/products/jet/)
*   [下载 Hazelcast Jet](https://hazelcast.com/download/)

**关于 Hazelcast，Inc.** 总部位于美国硅谷的 Hazelcast 是一家领先的内存计算平台公司，致力于满足日益增长的应用性能、数据处理速度和可扩展性需求。

Hazelcast 的内存计算平台由两个核心产品组成:Hazelcast IMDG 和 Jet。Hazelcast IMDG 是一个内存数据网格，经证明可提供世界上最大的组织所需的大规模性能。Hazelcast Jet 是一个超快速、可嵌入应用程序的流和批处理引擎，能够支持实时流数据。该公司还提供 Hazelcast Cloud，这是一个完全托管的低延迟数据层，适用于任何规模的基于云的工作负载。

Hazelcast 的客户包括世界 10 大银行中的 6 家和财富世界 500 强中的 36 家；几乎每一家主要的信用卡公司、世界上最大的五家电子商务公司和四家最大的电信公司都部署了它的技术。

欲了解更多信息，请访问[hazelcast.com](http://www.hazelcast.com/)或在 Twitter 上关注我们 [@Hazelcast](https://www.twitter.com/hazelcast) 。