# OpenStack 和开源 MANO:NFV 部署技术

> 原文：<https://devops.com/openstack-and-open-source-mano-technologies-for-nfv-deployment/>

我们经历了开源软件技术如何革新应用程序开发流程，最终导致各种垂直行业的数字化转型。开源技术现在正在扰乱电信部门建设 5G 互联网，5G 互联网将由网络功能虚拟化(NFV)和软件定义的网络(SDN)提供支持。借助 NFV 和 SDN，电信网络中的多种网络功能以及控制和管理操作将由软件驱动；支持云原生和开发运维方法。

出现了各种社区来创新 NFV 和 SDN 技术背后的软件堆栈，如 OpenStack、ONAP、ETSI 开源 MANO (OSM)、OPNFV、OpenDaylight、开放网络基金会(ONF)、Open Contrail、Open Baron、on。在本文中，我们将了解数据中心管理平台 management platform、OpenStack 和 ETSI 开源 MANO (OSM)的组合如何有助于 NFV 部署。

## **面向 NFV 的 OpenStack】**

众所周知，OpenStack 是最大的开源项目库，它们共同构成了云计算基础设施的软件平台。许多企业在私有云用例中广泛使用这种基础架构。在 ETSI 介绍了 NFV 之后，OpenStack 已经成为 NFV 的一个关键基础设施平台。在大多数 NFV 部署中，OpenStack 在 VIM(虚拟基础架构管理器)层使用，为管理、监控和评估 NFV 基础架构内的所有资源提供标准化界面。

各种 OpenStack 项目(包括 Tacker、Neutron、Nova、Astara、Congress、Mistral 和 Senlin)能够管理 NFV 环境的虚拟化基础架构组件。例如，Tacker 用于构建通用 VNF 管理器(VNFM)和 NFV 协调器(NFVO)，这有助于在 NFV 基础架构内部署和运行 VNFs。此外，集成 OpenStack 项目为 NFV 基础设施引入了各种功能，包括性能功能，如大页面、CPU 锁定、NUMA 拓扑和 SR-IOV；服务功能链、网络切片、可扩展性、高可用性、弹性和多站点支持。

已经使用 OpenStack 实施其 NFV 环境的电信服务提供商和企业包括美国电话电报公司、中国移动、SK 电讯、爱立信、德国电信、康卡斯特和彭博。

## **为 NFV 开源 Mano(OSM)**

管理和协调(MANO)层负责硬件资源和虚拟网络功能(VNFs)的协调和完整生命周期管理。换句话说，MANO 层协调 NFV 基础设施(NFVI)资源，并将它们高效地映射到各种 vnf。MANO 的三维软件堆栈有多种选择。但是，由于社区级别的大型活动以及其高度成熟的框架、生产准备就绪、易于启动和成员不断提供用例，ETSI 主办的 OSM 在很大程度上是首选。

虚拟网络功能(VNFs)构成网络服务，可能需要更新以添加功能或修补功能。OSM 提供了一种调用 VNF 升级操作的方法，对正在运行的网络服务影响最小。

随着社区对功能创新的持续支持和参与，OSM 现在已经发展到在 MANO 层引入持续集成和持续交付(CI/CD)框架。

最新的 OSM 第 4 版为 OSM 框架带来了大量的功能和增强，影响了功能、用户体验和成熟度，从可用性和互操作性的角度为 NFV 马诺带来了各种增强。

OSM 已经稳定地采用了云原生原则，并且可以轻松地部署在云中，因为安装是基于容器的，并且在容器编排引擎的帮助下运行。新的北向接口符合 ETSI NFV 规范 SOL005，并提供 OSM 系统的专用控制。监控和闭环功能也得到了增强。

下一版本的 OSM 第 5 版预计将于 11 月推出，并将捆绑更多 5G 相关功能，如网络切片和基于容器的 VNFs。

## **为什么 NFV 的 MANO 层采用 OpenStack 和开源 MANO？**

OpenStack 和 OSM 都有一个庞大的社区，以其创新 NFV 的快速步伐和所有规模的公司对增强当前功能和开发核心项目新功能的更大贡献而闻名。

对于 NFV，OpenStack 标准化了 NFV 元素和基础设施之间的接口。OpenStack 用于 Canonical/Ubuntu、思科系统、爱立信、华为、IBM、Juniper、Mirantis、Red Hat、SUSE、VMware 和 Wind River 等公司的商业解决方案产品。很大一部分 VIM 部署都是基于 OpenStack 的，这是因为 open stack 在处理和操作各种旨在为 NFV 提供全部潜在存储、计算和网络的项目时非常简单。

在最近的两个版本(3 和 4)中，OSM 通过将 CI/CD 框架支持到流程编排层中，支持云原生方法的集成。OSM 的云就绪性参与是 OpenStack 的主要优势，open stack 已经为私有云和公共云提供了成熟的架构。OSM 部署到 NFV 的基础设施已经变得非常精简，在那里可以从进口码头集装箱到生产开始。另一方面，OpenStack 以简化虚拟化和容器化基础架构的管理而闻名。由于精简和简单的管理和部署，组织可以像 NFV·马诺一样使用 OSM 和 OpenStack 来实现集成的全部好处。

## **结论**

自 NFV 和 SDN 推出以来，电信服务提供商和厂商一直在评估为电信网络提供的使用案例，由于这两者的应用，电信服务提供商和厂商都处于不成熟阶段。服务提供商和供应商关心基础架构部署的动态编排和自动化，以及不断升级虚拟网络功能(VNFs)。但由于 OpenStack 和开源 MANO (OSM)等开源社区的贡献，他们现在正处于将云原生原则应用于 5G 网络实施和运营的阶段。此外，随着社区对 OpenStack 和 OSM 项目的贡献，我们将看到 5G 网络增强技术的更多增强，包括网络切片、移动边缘计算(MEC)和云无线电接入网络(cRAN)，这将有利于新兴技术，包括物联网、人工智能/机器学习、实时分析、增强现实(AR)和虚拟现实(VR)，具有低延迟和高带宽特性。

-[萨加尔族的所有者](https://devops.com/author/sagar-nangare/)