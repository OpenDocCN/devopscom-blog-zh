# Xen 项目推进虚拟机管理程序项目

> 原文：<https://devops.com/xen-project-advances-hypervisor-project/>

Xen 项目本周宣布，[最新版本的开源管理程序](https://www.prnewswire.com/news-releases/xen-project-hypervisor-4-13-brings-improved-security-hardware-support-and-features-to-increase-embedded-use-case-adoption-300977022.html)现在可以利用核心调度，这是一项实验性技术，使 Xen 能够将多个处理器组合在一起，创建一个虚拟中央处理器单元(CPU)。

Xen 项目顾问委员会主席 Lars Kurth 表示，这种能力也代表了开发更安全的超线程技术的重要的第一步。自今年早些时候以来，[许多 IT 组织出于网络安全考虑关闭了超线程技术](https://devops.com/linus-torvalds-sees-lots-of-hardware-headaches-ahead/)。然而，这样的决定已经导致许多应用程序的显著性能损失。

除了增加对核心调度的支持之外，Xen Project Hypervisor 4.13 版本还增加了对实时补丁和后期 uCode 加载的支持，使得在运行时安装更新而无需重新启动 Hypervisor 成为可能。最新版本的 Xen 还增加了对额外处理器的支持，包括 AMD 第二代 EPYC、Hygon Dhyana 18h、Raspberry Pi4 和基于英特尔 AVX512 的平台。

最后，Xen 的 4.13 版本增加了对 OP-TEE 的支持，使所有来宾可以在 TrustZone 上并发运行可信应用程序，ARM 创建的用于隔离同一系统上处理器的固件，以及对 Dom0less 的改进，使并行运行的处理器分区成为可能。

Xen 项目组还宣布，它已经创建了一个功能安全工作组，该工作组致力于使 Xen 虚拟机管理程序与 ASIL-B 要求兼容，这是汽车行业定义的一组合规性要求。这项工作是一项重大挑战，因为它要求代码和开发流程符合 ISO 26262 的关键原则，这是一套将电子设备嵌入任何道路车辆的标准。

Xen 集团也在致力于开发一种无秘密的系统管理程序，Kurth 表示，这将在挫败旁路网络安全攻击方面发挥关键作用。网络犯罪分子可以通过测量和分析处理器产生的辐射量等物理属性，利用旁道攻击来破解加密算法。

Kurth 说 4.13 版本代表了 Xen 持续发展的一个重要里程碑。在未来，Xen 还将能够利用由英特尔领导的 Rust-vmm 项目，该项目将使处理器能够以模块化的方式运行多种类型的虚拟机管理程序。除了提供更灵活的隔离虚拟机的方式，Rust-vmm 还将减少启动虚拟机所需的时间。具体来说，英特尔正在努力使处理器能够更容易地运行不同类别的虚拟机管理程序，这些虚拟机管理程序针对传统单片应用程序和基于容器的云原生应用程序进行了优化，这些应用程序需要更轻量级的虚拟机管理程序。

尚不清楚核心调度等技术的进步会在多大程度上影响虚拟机管理程序和虚拟机的选择。然而，从 DevOps 的角度来看，很明显，添加到下一代虚拟机管理程序中的核心功能不仅会提高应用程序性能，而且还会显著推进最佳 DevSecOps 实践。

— [迈克·维扎德](https://devops.com/author/mike-vizard/)