# Morpheus 通过 Kubernetes 和 Terraform 增强功能打破了混合云管理平台模式，简化了企业 IT

> 原文：<https://devops.com/morpheus-breaks-the-hybrid-cloud-management-platform-mold-with-kubernetes-and-terraform-enhancements-to-simplify-enterprise-it/>

**科罗拉多州格林伍德村，2021 年 6 月 9 日—**[混合云应用编排公司 Morpheus Data](http://www.morpheusdata.com/) 发布了今年最大的软件更新，此举将帮助企业客户简化向容器的过渡，并简化在单一自助服务平台内采用基础设施即代码的过程。2020 年，Morpheus 通过帮助复杂企业降低云成本和简化混合云基础架构的管理，增长了 70%以上。随着今天的发布，Morpheus 宣布推出业界首个统一控制平面，以帮助平台工程团队整合云和容器管理以及基础设施自动化。

Morpheus v5.3.1 的亮点包括:

*   Morpheus Kubernetes 更新简化了客户端在混合云和混合平台环境中构建、管理和使用容器集群的方式。
*   Morpheus Terraform provider 和新的 Terraform 实例类型消除了自动化孤岛，同时简化了内部基础设施即代码。
*   数十项云管理更新，包括扩展的 Google 云平台和 VMware 集成，以及自定义 UI 和报告插件。

今天的基础设施和运营团队正面临着一个重大的复杂性和技能差距危机，因为他们努力支持开发人员，管理混合云，并促进向容器的转移。结果是快速变化的市场以及云和容器产品的融合。有关详细信息，请参见《2021 年高德纳云计算管理工具市场指南》、 ¹ ，该指南将 Morpheus 列为代表性厂商。

Morpheus Data 首席营销官 Brad Parks 表示:“It 团队几乎不可能管理日益复杂的云服务、容器平台和自动化工具，”。*“客户正涌向 Morpheus，因为我们消除了技术孤岛，为云、容器和自动化混乱带来了秩序。”*

**简化企业在任何云上构建、管理和使用 Kubernetes 的方式**

大多数公司现在报告说，容器的采用越来越多，部署跨私有云和公共云混合运行。不幸的是，管理虚拟化和混合云基础架构的团队现在在应对 Kubernetes 时已经到了极限。不足为奇的是，缺乏熟练的资源和运营复杂性经常被认为是最大的挑战。

Morpheus 已经帮助数百家企业降低了混合云的复杂性，同时避免了供应商锁定，并在其统一且独立的自助服务平台中为容器管理带来了同样的优势。更新包括:

*   CNCF 认证的 Morpheus Kubernetes 引擎(MKE)已更新至 1.20，可将一致的普通 Kubernetes 简单部署到数十个受支持的云。
*   在点击式 Kubernetes 配置向导中简单添加 Prometheus、Grafana、Istio 等软件包和服务。
*   支持棕色地带的 Kubernetes 集群，如 AKS、EKS、OpenShift、Rancher 等。已更新至 Kubernetes 1.20，消除了“仅 Kubernetes”工具开销。
*   针对集群访问、节点、工作负载、网络、存储等整合管理数十个新的 Kubernetes 对象，以提高运营效率。

这意味着企业平台团队可以消除在与其虚拟化和云原生平台即服务完全不同的控制平面中构建、管理和使用 Kubernetes 的需求。当客户评估 VMware Tanzu 或 Red Hat OpenShift 等专有堆栈时，它还可以减少锁定。

**通过将基础设施作为代码缺口来消除自动化孤岛**

随着企业通过 Terraform 采用基础设施即代码(IaC ),他们报告了管理工作流以及弥合基础设施自动化和应用程序配置之间的差距所面临的挑战。当您将 Terraform Enterprise 的成本与 Ansible Tower 的成本相结合，再加上企业已经在传统 VMware 自动化上的支出，将 Ansible 等工具链接到 Terraform 可能会非常困难和昂贵。

Morpheus 自成立以来一直处于基础设施自动化的前沿，支持原生 IaC 语法和第三方 IaC，包括 AWS CloudFormation、Azure ARM 和 HashiCorp Terraform。Morpheus 是 GitOps 的早期支持者，它能够将 IaC 和配置脚本链接到存储库，以实现版本控制和持续自动化。注重效率的企业还通过使用 Morpheus 消除与 Ansible Tower 和 Terraform Enterprise 相关的支出，大幅降低了成本。

在 Morpheus v5.3.1 中，客户现在可以利用 Terraform 实例类型，为 Terraform 模块提供一个目录前端，并将 IaC 提供的资源直接链接到 Ansible、Chef、SaltStack、Puppet 等自动化工具。通过将基于阶段的自动化附加到 IaC，运营团队可以完全控制 Terraform 资源的生命周期，并简化调配后任务。这些 Terraform 实例甚至可以暴露给 ITSM 工具，如 ServiceNow，只需点击几下鼠标，成本为零。

Morpheus 还通过开发自己的 Morpheus Terraform 提供商，简化了 Terraform 在内部环境中的使用。传统上，在内部使用 Terraform 需要为运营团队在内部使用的数十种工具提供单独的提供商，包括 IPAM、DNS、虚拟机管理程序等。Morpheus Terraform provider 将使 Terraform 用户拥有一个统一的提供商，可以跨任何内部或公共云使用，而不会增加复杂性。

**在内部带来云体验，并将控制权扩展到公共云**

在过去的 18 个月中，Morpheus 在主要行业分析公司的[混合云管理](https://morpheusdata.com/hybrid-cloud-management/)分析中被评为领先的供应商和强劲的表现者。这种认可很大程度上来自一个功能集，该功能集涵盖了自助供应、治理和安全性、开发人员支持以及云资源优化。

在最新版本中，Morpheus 通过几项核心混合云管理平台更新延续了这一市场领先轨迹，包括:

*   [谷歌云平台](https://docs.morpheusdata.com/en/5.3.1/integration_guides/Clouds/google/google.html) (GCP)增强功能，包括更灵活的区域范围，以及项目、安全组和网络对象(包括网络、子网、路由器和防火墙)的创建和管理。
*   [VMware 为从 NSX-V 迁移到 NSX-T 的用户提供更新](https://docs.morpheusdata.com/en/5.3.1/getting_started/guides/vmware_guide.html)，包括在单租户和多租户部署中创建和管理 NSX-T 负载平衡器、DHCP 对象和分布式防火墙的能力。
*   [Morpheus 插件框架](https://developer.morpheusdata.com/)增强功能使系统集成商、客户和联盟合作伙伴能够为服务器选项卡和实例创建定制报告和定制用户界面扩展。

潜在客户可以要求定制产品演示，并在[www.morpheusdata.com/demo](http://www.morpheusdata.com/demo)与自动化专家进行财务论证会议。在 451 Research 的这份[报告中，也可以找到对最新发布的 Morpheus 的独立评论。](https://www2.morpheusdata.com/Analyst-451-Morpheus-v5_3_1)

1.  Gartner 云计算管理工具市场指南，丹尼斯·史密斯，Padraig Byrne，John Chessman，2021 年 4 月 8 日。

**关于 Morpheus Data，LLC**

Morpheus Data 是[混合云应用编排](https://morpheusdata.com/hybrid-cloud-management/)领域的市场领导者，为全球数百家企业、公共部门组织和服务提供商提供服务。

Morpheus 软件平台为客户提供了一个可定制的自助式应用供应目录，该目录可涵盖数十种内部虚拟机管理程序、私有云和公共云。其基于角色的功能集可满足平台工程、安全、应用开发和财务团队的需求，这些团队寻求实现由裸机、虚拟机、容器和公共云平台即服务组成的应用的现代化。

凭借比任何其他平台更多的内置集成和本机功能，客户可以标准化工作流、减少工具蔓延，并跨不同团队和技术统一流程。