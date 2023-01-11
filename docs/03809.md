# 波特沃克斯和 HPE 发布新的解决方案，用于在 HPE 协同上快速部署集装箱化应用程序

> 原文：<https://devops.com/portworx-hpe-release-new-solution-rapid-deployment-containerized-applications-hpe-synergy/>

**波特沃克斯和 HPE 发布新的解决方案，在 HPE 协同** 上快速部署集装箱化应用

*新的参考配置，用于在云规模上自动化和管理运行 Kubernetes 的企业应用*

**加州洛斯阿尔托斯—2018 年 1 月 18 日—**[Portworx](https://portworx.com/)，在生产中运行有状态容器的解决方案，和[惠普企业](https://www.hpe.com/us/en/home.html) (HPE)今天宣布了一个基于参考配置的解决方案，允许各种规模的企业轻松部署、扩展和管理有状态容器工作负载。这种新的解决方案使 IT 团队能够使用 HPE Synergy composable system、Kubernetes 和 Portworx 的云原生存储平台的组合，在裸机上部署横向扩展容器平台。因此，该解决方案可以在 30 分钟或更短时间内快速部署，具有高度的容器和存储弹性，并且可以扩展到许多具有裸机性能的节点。

随着按需应用程序(如优步和网飞)为即时响应用户需求设立了新标准，企业正在转向更高效的云原生和以容器为中心的应用程序架构，以满足用户对速度、可靠性和性能日益增长的需求。将应用程序迁移到这种架构中，可以为企业提供更大的灵活性，以及快速向客户交付创新服务的能力。HPE 和波特沃克斯一起工作，将部署这种架构的最佳实践与部署自动化脚本和行动手册封装在一起。

**参考配置利用:**

*   Kubernetes 是一个高效的横向扩展容器编排器和调度器
*   Portworx PX-Enterprise 作为高度可靠的、云原生的、以容器为中心的存储平台，运行有状态的容器工作负载
*   HPE 协同作为可组合的基础设施，为容器应用提供灵活的计算和存储，并使基础设施成为自动化的代码

“大规模运行企业集装箱工作负载需要高度灵活、可扩展和可用的计算和存储，”HPE 生产管理副总裁 McLeod Glass 表示。“波特沃克斯和 HPE 在 HPE Synergy 的可组合基础设施之上提供了一个完全集成的云原生存储层，为 Kubernetes 集群上的容器提供可扩展的数据和计算服务。这将极大地简化客户通过部署自动化和在 HPE 的可组合系统上运行原生容器存储来交付有状态容器服务的能力。”

Portworx 首席执行官 Murli Thirumale 表示:“针对集装箱化工作负载的 HPE-Portworx 解决方案在自动化和控制之间为企业 IT 实现了重要的平衡。“HPE Synergy 自动化了硬件供应，而 Kubernetes 和 Portworx 自动化了应用程序生命周期管理，这对企业 IT 来说是一个福音。同时，PX-Enterprise 使 IT 部门能够使用 Portworx 的可配置服务等级、加密和备份策略来保持对其存储环境的完全控制。”

从应用角度来看，针对 Kubernetes 和 Portworx PX-Enterprise 的 HPE 协同解决方案具有以下优势:

*   **性能**:容器应用和后端数据库既可以在裸机上运行，也可以在 HPE Synergy SY 480 硬件上的虚拟机上运行，从而确保容器化计算和存储的卓越性能。
*   **App Services** : Kubernetes 提供负载均衡、DNS 和内置服务。
*   **快速部署** : Synergy image streamer，用于计算和存储资源的无缝扩展和收缩，以优化容器基础设施的资源需求。
*   **自我修复**:Kubernetes 根据服务器和应用程序级别的检查来替换和重新安排容器。
*   **高可用性数据** : Portworx 创建容器粒度的卷，这些卷被复制并保持高可用性，包括跨维护操作。
*   **容器数据生命周期**:Portworx PX-Enterprise 可以自动对容器卷进行加密、快照和备份到对象存储。

有关这一基于参考配置的解决方案的更多信息，[单击此处](http://h20195.www2.hpe.com/V2/GetDocument.aspx?docname=a00039700enw)。

**关于波特沃**

Portworx 是在生产中运行有状态容器的解决方案，设计时考虑到了 DevOps。有了 Portworx，用户可以使用任何容器调度器管理任何基础设施上的任何数据库或有状态服务，包括[【Kubernetes】](https://portworx.com/use-case/kubernetes-storage/)[meso sphere DC/OS](https://portworx.com/use-case/persistent-storage-dcos/)和 [](https://portworx.com/use-case/docker-persistent-storage/) [Docker Swarm](https://portworx.com/use-case/docker-persistent-storage/) 。Portworx 解决了 DevOps 团队在生产中运行有状态服务时遇到的五个最常见的问题:持久性、高可用性、数据自动化、安全性以及对多个数据存储和基础设施的支持。Portworx 非常适合垂直解决方案，如数据库、消息队列、持续集成和持续部署(CICD)、大数据和内容管理。客户包括 TGen 汉莎系统公司、《财富》全球 500 强中的八家公司，以及医疗保健、全球制造、电信和联邦政府等行业的其他《财富》1000 强客户。