# Sysdig 推出 PromCat，每次集成节省开发人员一周时间

> 原文：<https://devops.com/sysdig-launches-promcat-saves-developers-a-week-per-integration/>

*业内首个经审查的 Prometheus 集成文档、配置和支持的存储库*

**旧金山—2020 年 3 月 24 日** —安全开发运维领导者 Sysdig，Inc .今天发布了 PromCat.io。PromCat 是 Prometheus Catalog 的缩写，是一个经过审查的 Prometheus exporters、仪表盘和警报的管理库，用于监控云中运行的任何基础架构、应用程序和服务。Sysdig 提供文档、建议配置和 Sysdig 客户支持。有数百个处于不同完成水平的 Prometheus exporters 从云供应商提供的各种应用和服务中收集指标。通过文档验证集成(导出器、仪表板和警报)有助于客户决定使用哪种集成、如何配置它们以及跟上变化。通过减少这项研究，DevOps 团队可以节省数周的时间。今天，PromCat 为 Kubernetes 控制平面、Isteo 和越来越多的 AWS 服务提供集成。

在今天的另一份公告中，该公司宣布了业界首个云规模、完全兼容 Prometheus 的监控解决方案。与 PromCat 一样，Sysdig 继续帮助组织在采用云和 Kubernetes 时更快地发布应用程序。

**博客** : [PromCat:企业级普罗米修斯监控资源目录](https://sysdig.com/blog/promcat-prometheus-catalog/)

当开发人员进行协作和共享时，他们可以提高可见性并增强环境的安全性。普罗米修斯的流行带来了丰富的共享资源；然而，很难确定哪些资源已经准备好投入生产，并且能够为企业提供支持。

实施可扩展的 Prometheus 监控系统是一项挑战，需要指标源和收集、仪表板、警报和保留之间的紧密集成。这是一个需要导航兼容性差异的难题，需要花费时间来设置和维护。PromCat 的目标是让开发者更容易获得云原生社区的集体专业知识。

用户可以从 PromCat 获得集成，并将其用于 Sysdig Secure DevOps 平台或他们自己的 Prometheus 服务器。开发人员不必使用商业 Sysdig 产品来使用 PromCat 存储库，除非他们需要支持。在接下来的几个月里，PromCat 将扩展到包括更多在 [2019 Sysdig 容器使用报告](https://sysdig.com/blog/sysdig-2019-container-usage-report/)中按受欢迎程度排序的应用和服务。

“网上有丰富的代码共享；然而，很难知道去哪里找，质量也不一致，”Sysdig 创始人兼首席技术官洛里斯·德吉奥安尼说。“开发人员可能会花费数小时测试仪表板或导出器，结果却发现它有问题。通过验证、改进和记录，我们希望在整个社区中增长专业知识，从而为每个人提高 Kubernetes 的可见性和安全性。”

Sysdig 建立在这样一种信念上，即当核心技术被单一供应商控制时，创新就会被扼杀。Sysdig 业务模型依赖于在开源之上添加服务和支持，以增强可伸缩性、性能和易用性。随着新的集成被添加到 PromCat 中，所有的增强和 bug 修复都会反馈到开源社区。

基于对开源力量的这种信念，Sysdig 对社区进行了大量投资。该公司在 2014 年推出了开源容器故障排除项目 sysdig。从那以后，该公司创建了另外两个开源工具——Falco 和 Sysdig Inspect——以及其他开源项目，包括 Prometheus 和 eBPF。Falco 是 CNCF 孵化级托管项目，是 CNCF 唯一的运行时安全项目。

**可用性**

PromCat.io 现已上线，并将继续添加新的经过验证的集成。