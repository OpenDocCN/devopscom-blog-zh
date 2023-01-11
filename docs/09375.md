# Loft Labs 通过新的开源项目简化了虚拟 Kubernetes 集群管理

> 原文：<https://devops.com/loft-labs-simplifies-virtual-kubernetes-cluster-management-with-new-open-source-project/>

*部署虚拟 Kubernetes 集群，就像在云中、边缘或内部部署集群一样*

**加利福尼亚州三藩市，2022 年 5 月 16 日—** [Loft Labs](https://loft.sh) ，一家为 Kubernetes 开发开发工具和多租户解决方案的风险投资支持的初创公司，今天宣布为流行的开源 [vcluster](https://www.vcluster.com/) 技术发布一个[集群 API 提供商](https://loft.sh)。现在，部署虚拟集群与在云平台或内部数据中心部署物理 Kubernetes 集群完全一样。

除了 Loft Labs 之外，Cluster API 项目还获得了众多公司的技术支持，包括 VMware、Microsoft、Weaveworks、Google、Mattermost、IBM、RedHat、D2iQ、Equinix、Apple、Talos Systems、Spectro Cloud、Daimler TSS、Ericsson、Giant Swarm、AppsCode、Intel、Twilio、New Relic、Amazon 等等。

Loft Labs 的联合创始人兼首席执行官 Lukas Gentele 表示:“集群 API 简化了重复性任务，同时保持了一致性和可重复性，从而使集群生命周期管理变得枯燥乏味。"它有助于通过自动化和标准化整体管理 Kubernetes 基础设施."

来自 Twilio [的高级首席工程师 Kris Nó va 和首席工程师 J. Brandt Buckley 在 CNCF 博客](https://www.cncf.io/blog/2021/10/06/kubernetes-cluster-api-reaches-production-readiness-with-version-1-0/)上评论了他们使用集群 API 的经历。“在 Twilio，我们在分布于不同地理数据中心的裸机服务器上运行超过 100 个生产 Kubernetes 集群。我们发现了集群 API 整体拓扑的价值，特别是拥有管理集群的范例。我们利用管理集群作为我们的专用基础设施，团队可以在此基础上构建、管理和保护管理我们公司不断增长的 Kubernetes 集群的应用套件。”

vcluster 开源软件发展迅速，在首次发布后不到一年的时间里，GitHub 上的下载量超过 300 万次，星级超过 1，500 个。vcluster 于 2021 年 4 月首次发布，用于创建轻量级 Kubernetes 集群，在底层 Kubernetes 集群的命名空间内运行。使用虚拟集群解决了 Kubernetes 的大多数多租户问题，因为它们提供了:

*   比简单的基于名称空间的多租户更好的隔离；
*   降低云计算成本，因为虚拟集群比独立的单租户集群更加轻量级和资源高效；
*   应用程序工作负载与底层群集的共享基础架构工作负载(如共享入口控制器或网络插件)的逻辑分离和封装。

同时，虚拟集群用户可以预期他们的虚拟集群的行为就像任何常规的 Kubernetes 集群一样，因为 [vcluster 是经过认证的 Kubernetes 发行版](https://loft.sh/blog/vcluster-becomes-first-certified-kubernetes-distribution-for-virtual-kubernetes-clusters/)，这意味着它通过了 [CNCF 要求的所有一致性测试](https://www.cncf.io/certification/software-conformance/)。当工程师构建、测试和调试云原生软件时，虚拟集群经常被用作开发环境，但它们也经常被用作执行持续集成/持续交付(CI/CD)管道的短暂环境。![page1image46808640](img/105881fef2f8474d1fab362afbbc9add.png)

要了解更多信息，请访问托管用于 vcluster 的集群 API 提供程序的 Kubernetes [GitHub 项目。Loft Labs 将于 5 月 16 日至 20 日在](https://github.com/loft-sh/cluster-api-provider-vcluster) [KubeCon Europe](https://events.linuxfoundation.org/kubecon-cloudnativecon-europe/) 的 SU15 号展位展出。

**关于 Loft Labs**

Loft Labs 成立于 2019 年，旨在为 Kubernetes 创建开源开发工具和虚拟集群技术，目标是提高开发人员的生产力，并帮助工程师安全但不受阻碍地访问云基础设施。

**媒体联系** 约瑟夫·埃克特为 Loft Labs
[T5【邮件受保护】](/cdn-cgi/l/email-protection#fd8d8fbd91929b89d38e95)