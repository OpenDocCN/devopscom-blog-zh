# 孔向捐赠服务网

> 原文：<https://devops.com/kong-donates-kuma-service-mesh-to-the-cncf/>

云计算原生计算基金会(CNCF)今天宣布接受由孔开发的开源服务网格(T1)作为沙盒级项目。

与此同时，Kong [宣布了对基于单片和微服务的应用的服务网格](https://konghq.com/press-release/kong-releases-new-version-kuma-bring-service-mesh-hybrid-workloads/?utm_source=pressrelease&utm_medium=referral&utm_campaign=kuma-cncf-donation)的更新，这使得跨多种类型的网络环境部署库马的多租户实例变得更加容易。

服务网格提供了跨网络环境的抽象层，简化了分布式应用程序的部署。服务网格自动地跨多个网络底层路由应用流量，而不必为特定网络手动配置每个应用服务。

![](img/0f232e091d89f983a9f29014afdb8a01.png)

库马是基于 Envoy 的，这是一个在 CNCF 支持下开发的开源代理服务器。库马将是继 Linkerd 之后，CNCF 接受的第二个服务网格项目。然而，Linkerd 并不是基于 Envoy 的，所以 CNCF 增加了另一个服务网格项目。

Kong 首席技术官 Marco Palladino 表示，Envoy 提供了一个创建轻量级服务网格的机会，这种网格更容易在分布式计算环境中部署。

可以说，服务网格最著名的例子是 Istio，它是由 Google、IBM 和 Lyft 为 Kubernetes 集群开发的。然而，Istio 的部署和管理很复杂，而且它没有受到任何开源联盟的支持。

Palladino 说，鉴于 Envoy 的受欢迎程度，添加一个轻量级、可伸缩性更好、可扩展性更强的服务网格是有意义的。他说，例如，库马的最新版本增加了对跨越数十万个数据平面代理的全局/远程控制平面复制的支持。

此外，还增加了一个入口数据平面模式，可自动进行跨平台和跨集群服务网格通信，以及一个本机通用 DNS 服务发现应用程序编程接口(API)，使多个服务看起来都共享同一个集群。

作为由 CNCF 管理的沙盒级项目，Kong 现在邀请其他组织为库马服务的开发做出贡献。哪些服务网格最终会获得广泛的支持还有待观察。除了库马、Istio 和 Linkerd，来自 HashiCorp 的开源咨询服务 mesh 也在争夺支持。还有其他代理服务器，比如 NGINX，可以在其上构建服务网格。

很少有 IT 组织在生产环境中部署任何类型的服务网格。然而，随着部署的微服务数量稳步增加，IT 组织需要一种更简单的方法来支持应用程序调用网络资源。库马提供了一个服务网格来解决这个问题，新兴的基于微服务的应用程序和传统的单片应用程序都可以采用这个网格。

Palladino 说，库马还可以更容易地保护流量，建立服务连接权限，并使用可以使用 API 设置的路由规则组合来捕获指标。它还为最常见的服务网格用例提供了开箱即用的策略。

服务网格还应该在网络运营(NetOps)和最佳开发运维实践的最终融合中发挥重要作用。仍然需要网络专家来部署物理网络底层。然而，网络服务本身正在成为一种虚拟的抽象，开发人员可以在中央 IT 组织定义的策略参数内调用它。

现在的挑战是将服务网格平台推进到普通企业 IT 团队能够部署和管理它们的程度。