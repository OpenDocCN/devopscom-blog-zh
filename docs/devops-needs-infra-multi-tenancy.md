# DevOps 需要基础设施多租户

> 原文：<https://devops.com/devops-needs-infra-multi-tenancy/>

无论你给它起什么名字，开发运维都将继续进入网络基础设施，因为它最终是应用部署生命周期的一部分。虽然开发运维人员称之为“应用交付”，但实际情况是，在所有必需的服务[完成调配和配置](https://devops.com/blogs/provisioning-vs-configuration/)之前，应用还没有准备好交付给用户(内部或外部)。

是的，基础设施和网络设备越来越多地支持 API，并支持各种工具和框架，这些工具和框架通常与 DevOps 相关联——Puppet、Chef、OpenStack、VMware——以及更常见的仅与网络相关联的工具和框架——Arista、Cisco ACI 和 OpenDaylight。

但是它需要的不仅仅是 API。API 本身并没有赋予设备支持多租户的能力。也就是说，在传统的共享环境中有效部署支持应用程序的基础设施服务所需的团队(或应用程序)特有的服务隔离。

根据[ThoughtWorks Technology Radar(2015 年 1 月)](https://www.thoughtworks.com/radar/techniques)的说法，按照团队界限划分基础设施对于消除应用部署生命周期中的障碍来说是必不可少的:

> 我们的许多客户已经在他们的组织中实现了开发运维，交付团队构建、部署和支持他们自己的应用和服务。不幸的是，这个过程中的一个常规障碍是允许团队在生产环境中拥有超级用户特权。在大多数组织中，生产环境是共享的，因此广泛提供访问是有风险的。当我们能够**沿着团队边界划分基础设施时，这是有效的，**这样那些团队就可以安全地、隔离地进行工作，而不会有影响其他系统的风险。在使用云环境的情况下，这更容易实现，使客户结构与团队边界保持一致。**【重点地雷】**

这一直是一个依赖共享服务的问题。支持一个应用程序(或团队)的更改可能会对另一个应用程序或团队造成干扰或问题。因此，大多数基础设施和网络团队坚决拒绝让应用或操作部门的任何人玩他们的玩具。

他们是网络忍者；用他们的生命来保护他们的结构。

如果我们作为一个统一的 It 组织要实现缩短上市时间和提高部署频率的目标，就需要解决这种冲突。如果因为超负荷的网络和基础设施工作人员而需要 3 个月才能交付给客户，那么应用团队是否能在 3 周内交付一个应用并不重要。

这个问题有两个好的解决方案。

1.对更多与应用相关的基础设施服务(负载平衡、缓存、代理等)的治理必然会向应用靠拢，并在应用和运营团队的控制之下。这得到了网络服务虚拟化等概念的支持，这些概念在 [Lippis 报告 217](http://lippisreport.com/2014/02/lippis-report-217-its-network-service-virtualization-in-the-enterprise-rather-than-network-function-virtualization/) 中提出，并且开源的基于代理的(虚拟和软件)服务越来越多地被采用。这种模式假设持续的共享网络和基础设施服务是适当的，同时将基于应用的服务迁移到更灵活、可操作的架构。

2.在基础设施架构中引入多租户提供了一种类似的方法，同时仍然维护共享资源(硬件)。单个高容量系统能够托管其服务的多个虚拟实例，每个实例根据组织的需要专用于团队或应用程序。这种方法将硬件资源的成本分摊到整个组织中，同时允许对供应、配置和最终成本采取更加基于应用的方法。隔离解决了共享资源和配置的问题，这些问题可能会引起网络和基础设施团队的恐慌，因为底层共享系统由他们管理，而对应用服务的基于角色的控制则提供给团队或指定的负责人。

这两种方法都是有效的，并且在许多情况下，这两种体系结构解决方案都将用于解决由传统共享基础架构引起的问题。

这里的关键要点是，对于支持开发运维驱动的工作流和流程的分区基础架构的需求，我们已经找到了答案，并且肯定能够提供一种方法来确保更无缝、对时间更敏感的端到端应用部署流程。

*哦，我肯定还有更多，但目前这两个似乎是最好的选择。