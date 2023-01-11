# Kubernetes 是通用的云基础设施

> 原文：<https://devops.com/kubernetes-universal-cloud-infrastructure/>

在我创办牧场主实验室之前，我创建了一家名为 Cloud.com 的公司，在那里我们开发了 Apache CloudStack。我们受到亚马逊网络服务(AWS)早期成功的启发，希望让每个人都有可能为自己建立类似 AWS 的云基础设施。

虽然 CloudStack 成功地支持了许多公共云和私有云，但它未能实现大规模采用。相反，今天的云基础设施越来越集中于少数非常大的公共云提供商，如 AWS 和微软 Azure。这有几个原因:

1.  运营云基础设施需要大量的资本投资和运营专业知识。只有大玩家才能从规模经济中获益。
2.  不同的云基础设施提供商之间没有一致性。即使较小的提供商可以在价格上击败成熟的竞争对手，客户也越来越难以将工作负载从一个云迁移到另一个云。
3.  云基础设施服务的范围在不断扩大。它不再足以提供基本的计算、存储和网络服务。AWS 等领先提供商提供越来越多的数据处理、分析和人工智能服务。

尽管存在云锁定的缺点，但随着组织采用云计算，他们在云基础架构方面面临的选择越来越少。

# 输入容器和 Kubernetes

我们创建了 Rancher Labs，因为我们看到容器有可能改变云计算的游戏。Docker 是一个通用的应用程序打包标准，使应用程序可移植。Kubernetes 向 Docker 添加集群管理。很多人认为 Kubernetes 的强大之处在于其管理应用和微服务的能力。我们完全同意。然而，我们认为，Kubernetes 也通过隐藏云基础设施提供商之间的差异带来了巨大的好处。Kubernetes 附带了丰富的存储、网络和负载平衡插件生态系统。因此，在哪里部署 Kubernetes 并不重要。只要驱动程序配置正确，无论用户使用哪家云提供商，他们都可以获得一致的云基础架构视图。

除了提供一致的存储、网络和负载平衡之外，Kubernetes 还为开发人员带来了丰富的高级服务生态系统。[云原生计算生态系统](https://github.com/cncf/landscape/tree/master/landscape)包括所有主要的系统级和平台级软件提供商。Kubernetes 已经成为云计算创新的重心。新功能的出现速度比其他任何地方都要快。

在早期，设置和运行 Kubernetes 是相当具有挑战性的。Rancher 等公司创建了 Kubernetes 发行版，使开发人员和 it 团队能够轻松部署和操作 Kubernetes 集群。如今，许多云提供商提供 Kubernetes 即服务。在 Rancher，我们现在更专注于管理 Kubernetes 集群。我们预计大多数(如果不是全部的话)主要的云提供商将来都会支持 Kubernetes。到那时，Kubernetes 将成为通用的云基础设施。

如果使用云计算，没有理由不使用 Kubernetes。无论您走到哪里，都能获得最完整的生态系统支持和一致的体验。云锁定将成为过去。

## 关于作者/盛亮

盛是 Rancher Labs 的联合创始人兼首席执行官。在创办 Rancher 之前，盛是 Citrix Systems 收购后云平台集团的首席技术官，他是该公司的联合创始人兼首席执行官。盛拥有超过 15 年的创新技术开发经验。他是 Teros 的联合创始人，Teros 于 2005 年被 Citrix 收购，并领导了 SEVEN Networks 和 Openwave Systems 的大型工程团队。Sheng 的职业生涯始于在 Sun Microsystems 担任 Java 软件工程师，在那里他设计了 Java 本机接口(JNI)并领导了 Java 2 平台的 Java 虚拟机(JVM)开发。盛拥有中国科学技术大学学士学位和耶鲁大学博士学位。在推特上关注他。