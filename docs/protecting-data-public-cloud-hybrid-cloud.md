# 保护公共云和混合云中的数据

> 原文：<https://devops.com/protecting-data-public-cloud-hybrid-cloud/>

30 多年来，备份、业务连续性(BC)和灾难恢复(DR)一直是 IT 的重要组成部分，从我们开始依靠技术来运营业务开始。传统解决方案是为内部基础架构、结构化应用程序和关系数据库而设计的。但是世界在变。在上一篇博客中，我谈到了数字化转型的[时代](http://datos.io/era-digital-transformation-next-gen-cloud-applications-means-databases/)，以及它对重新思考和重新发明基础备份和恢复架构的推动作用，这些基础备份和恢复架构适用于迁移到云的工作负载和诞生在云中的应用程序。

## 导致彻底改造备份和恢复的动机

应用和数据平台正在经历自计算出现以来最大的变革。有几种力量在起作用:

*   **新应用。**第三代应用程序是地理分布式的，可跨多个系统扩展，始终可用，通常部署在云优先模式中。
*   现有的应用程序正在向云迁移。它们不会消失，但公司会将它们中的一部分或全部转移到云上。他们仍然需要备份和恢复。
*   **RPO 和 RTO 窗口正在缩小:**企业希望“永不停机”，您可以进行夜间备份的日子已经一去不复返了。
*   较小的公司将全力投入公共云。中小型企业不想涉足 IT 行业。他们一直在推动云应用和平台的快速增长。
*   **企业将构建混合云。**企业将在内部和公共云环境中部署应用和数据。规模、合规性和其他因素意味着他们需要在本地保留一些系统。
*   **每个人都会使用多个云。**没有人会将他们的业务押在一个云或一个提供商身上。即使是现在，企业也在将工作负载分散到不同的云中或云和内部。开发和测试可能使用一个云，而相同的应用程序可能部署在私有云或不同的公共云中。

## 云对备份、恢复和连续性的影响

云为组织带来了更大的灵活性、运营成本节约和按需购买模式。公共云提供商也可以构建更具弹性的基础设施。亚马逊保证 EC2 的可用性为 99.95%，S3 为 99.99%；S3 设计用于 11 个 9 的数据持久性，具有多个可用性区域。因为云非常可靠而且便宜，所以它很快成为内部数据的备份目标。但是，当我们在云中运行应用程序时，这不应该欺骗我们相信备份和恢复是“内置的”。甚至亚马逊自己[也推荐所有 AWS 原生应用和云数据库的备份服务](https://publish.awswebcasts.com/content/connect/c1/7/en/events/event/private/23850344/41359021/event_registration.html?sco-id=47927990&campaign-id=emlong_23862)。

虽然服务可用性和数据弹性解决了基础架构业务连续性和灾难恢复问题，但它并不提供时间点恢复或应用程序级备份和恢复智能。尽管云平台很好，但它们不能防止逻辑错误。研究表明，10 个错误中有 8 个是逻辑错误——数据损坏、用户错误。

## 但是现有的备份产品不能在云中运行吗？

正如我们上面提到的，传统的备份和恢复产品无法满足云应用程序的需求，即使对于已经迁移到云的现有应用程序也是如此，这不仅仅是因为它们是在不同的时代构建的。云和分布式架构带来了其他几个挑战:

*   **云打破了传统解决方案中基于媒体服务器的架构。**云应用和数据不驻留在特定的阵列或磁盘上，所以你不能轻易备份你看不到的东西。备份也不会在云端捕获配置数据，比如 AWS 云形成模板。
*   云说的不是同一种语言。传统解决方案与磁带、磁盘或虚拟磁盘对话。云中的备份和恢复意味着集成正确的协议，如 S3 API 或谷歌云存储。
*   **备份设备不能移动到云中。**现有的在内部运行良好的备份设备不能被挑选出来并迁移到云中。
*   **传统备份代理无法扩展。**如果您可以在云中运行备份代理，它将无法跨数十个甚至数百个节点进行扩展。
*   **虚拟机不是正确的抽象层:**寻找能够提供可扩展的以应用为中心的数据管理和数据保护视图的技术，反省应用数据并使用全局语义重复数据删除来实现存储效率，而不是依赖传统的重复数据删除技术。这种方法的好处是细粒度和高度节省空间的数据保护，可以跨越网络链路上的云。
*   **云网关或迁移服务:**仅单向。

*云应用程序的备份和恢复问题很新颖，云备份和恢复架构应具备三个关键要素:*

*   ***仅弹性计算。**该架构应在弹性计算实例上高效扩展。服务器或设备不应有任何资本支出成本。*

*   ***没有媒体服务器。**备份大型横向扩展数据库需要直接并行流体系结构，以便在数据库和辅助存储之间移动数据。传统备份体系结构依赖于媒体服务器，这很快会成为瓶颈。直接并行流还允许数据以原生格式保持可用。*

*   ***语义去重。**横向扩展应用程序数据库通常具有 3 倍的复制系数。如果备份单个节点，甚至设法对整个数据库进行快照，三分之二的备份数据都是冗余的。随着时间的推移，如果没有跨分布式架构工作的语义重复数据删除，备份将会有 75%到 80%的*效率低下*。*

*— [布莱恩·尹](https://devops.com/author/brian-yin/)*