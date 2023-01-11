# AWS 最终采用内部 IT

> 原文：<https://devops.com/aws-finally-embraces-on-premises-it/>

亚马逊网络服务(AWS)本周宣布，它将在内部 it 环境中提供其 IT 基础设施的实例，然后代表客户进行管理。这一消息是在 AWS re:Invent 2018 大会上宣布的。

AWS 首席执行官 Andy Jassy 表示，计划于 2019 年推出的 AWS 前哨平台将有两种版本:一种将运行 AWS 用于管理其公共云的相同软件堆栈，而另一种将基于 VMware 目前在 AWS 云上提供的软件堆栈。

[VMware 宣布，除了在 AWS EC2 实例上提供 VMware Cloud Foundation 形式的管理和网络软件外，它还将为基于其整个平台堆栈的 AWS 前哨站](https://www.vmware.com/company/news/releases/vmw-newsfeed.VMware-to-Drive-Adoption-of-As-A-Service-Model-for-On-Premises-Data-Centers-with-New-Solutions-for-AWS-Outposts.1658510.html)提供自己的托管服务。这一举措代表了 VMware 混合云计算方法的重大扩展，因为 AWS EC2 基于开源的基于内核的虚拟机(KVM ),而不是 VMware 虚拟机管理程序。

无论选择哪种方式，每个前哨平台都将作为亚马逊虚拟私有云(VPC)服务的扩展，通过距离该内部平台最近的 AWS 区域提供连接。亚马逊 VPC 和 AWS 前哨都将被捆绑到 AWS 控制塔服务中，以创建一个公共管理平面。

经过多年将所有工作负载迁移到公共云的努力，Jassy 本周承认，在某些情况下，性能和合规性问题将导致一些工作负载永远不会迁移到公共云。Jassy 说，为了响应客户的需求，他们希望能够在内部部署和管理与云中相同的基础设施，AWS 现在正致力于通过 AWS 托管服务提供系统机架。

开发运维团队现在面临的挑战是确定他们希望在多大程度上将其开发运维流程与 AWS、VMware 或任何第三方服务提供商提供的托管服务相集成。在某些情况下，DevOps 团队可能会简单地认为额外的管理层会增加复杂性。在其他情况下，决策可能更倾向于为应用程序开发分配更多资源，因为跨混合云的 IT 运营越来越多地成为由外部供应商提供的自动化服务。

进入 2019 年，关于公共云和内部 it 环境的似是而非的辩论似乎即将结束。在可预见的未来，不仅会有工作负载在这两种环境中运行，而且国际数据公司(IDC)最近进行的一项研究指出，80%的受访 IT 组织已经将工作负载从公共云迁移回内部 IT 环境。让事情变得更加复杂的是，全新一代所谓的云原生应用程序基于在 Kubernetes 集群上运行的容器所支持的微服务，这给 IT 环境增加了更多的复杂性。

当然，目标是让现代企业更加敏捷。具有讽刺意味的是，实现这一目标似乎需要让 IT 环境变得比以往更加复杂。

— [迈克·维扎德](https://devops.com/author/mike-vizard/)