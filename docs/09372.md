# Envoy Gateway 使开发人员更容易使用 Envoy 代理，并逆转了碎片化

> 原文：<https://devops.com/envoy-gateway-makes-using-envoy-proxy-easier-for-developers-and-reverses-fragmentation/>

**加利福尼亚州三藩市和西班牙瓦伦西亚—2022 年 5 月 16 日—** 特使网关(EG)指导小组的成员，包括特使创建者 Matt Klein 以及来自大使实验室、富达投资、Tetrate 和 VMware，Inc .的代表今天宣布了他们对该项目的共同承诺，该项目于今天在云本地计算基金会(CNCF)的赞助下在 2022 年欧洲 KubeCon + CloudNativeCon 上启动。Envoy Gateway 是 Envoy 代理开源项目中的一项新成果，旨在简化 Envoy 在云原生应用程序开发中的使用。

Envoy Gateway 将减少围绕 Envoy 的现有冗余工作，并使应用程序开发人员更容易将 Envoy 用作“开箱即用”的基本 API 网关和 Kubernetes 入口控制器。公开一组简化的 API，并实现 Kubernetes 网关 API，EG 使得扩展 Envoy 变得更加容易。开发人员现在将有一种免费的、不受约束的方式来提供对他们正在进行的工作的外部访问。同时，Envoy Gateway 不会取代目前商业产品中的 API 管理功能。

“自从我们在 2016 年首次发布以来，特使已经取得了巨大的成功，”特使代理项目的创始人马特·克莱恩说。“社区从一开始就是特使的核心。通过社区驱动的 Envoy Gateway 项目，我们看到了通过添加简化的 API 和明确针对南北/边缘代理用例的新功能，让更多用户可以访问 Envoy 的机会。”

Envoy 已经广泛用于微服务应用中不同服务之间的流量传输，即东西向流量传输。有了 Envoy Gateway，Envoy 还可以很容易地用于南北流量——应用程序和外部世界之间的流量，就像应用程序 API 的消费者一样。

**Envoy Gateway——面向云原生未来的核心开源基础设施**

世界各地的 IT 组织都希望在 Linux 基金会和 CNCF 等组织的管理下，建立并使用丰富、强大、现代的开源软件栈来开发和交付云原生应用。然后，每个 IT 团队中的商业产品和项目可以在这个核心基础设施之上增加价值。

Envoy 正迅速成为这一现代云原生体系中的首选网络基础。然而，最近，对 API 访问、流量路由和其他入口功能的需求导致了 Envoy 生态系统的分裂。Envoy Gateway 将把这一所需的功能带回主要的 Envoy 项目，并使开发人员访问 Envoy 时不那么困惑和耗时。

**通过 Kubernetes 网关 API 实施**

特使网关将公开 Kubernetes-native [网关 API](https://gateway-api.sigs.k8s.io/) 的一个版本，具有特使特定的扩展。这是一个富于表现力、可扩展、面向角色的 API，非常适合开发人员使用。对于 Istio、Contour 项目(起源于 VMware)、使者入口(起源于 Ambassador Labs)等，网关 API 已经实现或正在开发中。

当用户创建网关 API 资源时，它们将被翻译成原生 Envoy API 调用，因此 Envoy 及其原生 API xDS 将不需要进行更改来添加这一新支持。

**开发人员、基础设施管理员和业务决策者的优势**

应用程序开发人员将体验到 Envoy Gateway 带来的最积极的影响。他们将能够运行 Envoy Gateway 并开始将流量路由到他们的应用程序。他们将不再需要构建自己的控制平面，或者扩展现有的控制平面，如 Go 或 Java 控制平面，或者在项目的早期阶段引入供应商解决方案。他们可以只为应用程序配置路由并共享它们。

基础设施管理员将能够轻松地为应用团队提供特使式的体验，而无需仅仅为了获得基本的网关功能而采用供应商解决方案。他们将能够管理 Envoy Gateway 的实例，而不会干扰开发人员对它们的访问。Envoy Gateway 将允许他们跨异构环境提供一致的应用程序网络功能。

高管和决策者将会把 Envoy 作为 API 访问和 Kubernetes 入口的标准和广泛使用的解决方案。他们还将受益于更快、更容易开发和交付更安全、更健壮的软件和服务。

**附加资源**

*   探索 CNCF[公告 T5。](https://www.cncf.io/announcements/)
*   回顾特使项目官方 [博客](https://blog.envoyproxy.io/) 。
*   了解更多关于特使网关 [目标](https://gist.github.com/danehans/22aada2fe63470d4b78ddd7f7cfbc971) 。

**关于特使**

Envoy 最初由 Matt Klein 创建，在 Lyft 构建，是一款高性能 C++分布式代理，专为单一服务和应用而设计，也是一款通信总线和“通用数据平面”，专为大型微服务“服务网格”架构而设计。基于对 NGINX、HAProxy、硬件负载平衡器和云负载平衡器等解决方案的学习，Envoy 与每个应用程序一起运行，并通过以平台无关的方式提供通用功能来抽象网络。当基础设施中的所有服务流量都流经 Envoy mesh 时，通过一致的可观察性来可视化问题区域、调整整体性能以及在单一位置添加底层功能变得非常容易。

联系马特·克莱恩 [【邮件保护】](/cdn-cgi/l/email-protection#99f4f8ededf2f5fcf0f7a8abaad9fef4f8f0f5b7faf6f4) 。

**关于大使实验室**

Ambassador Labs 是云原生开发人员体验的领导者，使开发人员能够比以往更快、更轻松地编码、测试、交付和运行应用。作为顶级云本地计算基金会(CNCF)开源项目(包括使者入口和网真)的制造商，Ambassador Labs 为 Kubernetes 提供了一个开发人员控制平面，该平面为全球的开发人员和组织(包括微软、PTC、NVidia 和 Ticketmaster)集成了开发、部署和生产基础设施。大使实验室得到了包括 Insight Partners 和 Matrix Partners 在内的顶级投资者的支持。在[www . getambassador . io](http://www.getambassador.io/)了解更多，免费上手。

通过 [【电子邮件保护】](/cdn-cgi/l/email-protection#1f73766c7e68767373767e726c5f7b7e6b7e68766d7a317670) 联系大使实验室的 Lisa Williams。

**关于富达投资**

富达的使命是为我们服务的客户和 企业创造更美好的未来和交付更好的成果。截至 2022 年 3 月 31 日，我们管理着 11.3 万亿美元的资产，其中包括 4.2 万亿美元的可自由支配资产 ，我们专注于满足多元化 客户的独特需求。富达是一家拥有超过 75 年历史的私营企业，拥有 57，000 多名员工，他们专注于我们客户的长期成功。更多关于富达投资的信息， 访问www.fidelity.com/about-fidelity/our-company。

通过 [【电子邮件保护】](/cdn-cgi/l/email-protection#95fef4e1fdf9f0f0fbbbf7f0fbe1f9f0ecd5f3f8e7bbf6faf8) 联系富达投资的 Kathleen Bentley。

**关于四分体**

Tetrate 是一家企业服务网络公司，由 Istio 创始人创立，旨在重塑应用网络，管理复杂的现代混合云应用基础设施。其旗舰产品 Tetrate Service Bridge 提供了一个从边缘到工作负载的应用程序连接平台，为企业从传统单体到云的旅程提供业务连续性、敏捷性和安全性。客户可以在任何环境中获得一致、固定的可观察性、运行时安全性和流量管理。Tetrate 仍然是开源项目 Istio 和 Envoy Proxy 的主要贡献者。更多详情请点击[www . tetrate . io](http://www.tetrate.io/)。

在 [【电子邮件保护】](/cdn-cgi/l/email-protection#73121d1d1a1633111c000312015d101c1e) 联系 Bospar 的 Annie Fink。

**关于 VMware**VMware 是面向所有应用的多云服务的领先提供商，通过企业控制实现数字化创新。作为加速创新的可信基础，VMware 软件为企业提供了构建未来所需的灵活性和选择。VMware 总部位于加利福尼亚州帕洛阿尔托，致力于通过公司的 2030 议程建设更美好的未来。更多信息请访问[](https://www.vmware.com/company)。

通过 [【电子邮件受保护】](/cdn-cgi/l/email-protection#42272d2c362b3427302d3102342f352330276c212d2f) 联系 VMware 全球通信部的埃洛伊·翁蒂维罗斯。