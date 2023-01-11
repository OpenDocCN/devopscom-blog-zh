# 容器、服务网格和 API 网关:从边缘开始

> 原文：<https://devops.com/containers-service-mesh-and-api-gateways-it-starts-at-the-edge/>

任何采用容器技术的人，比如 Docker 或 T2，都一定听说过相关的下一件大事:服务网格，它承诺使微服务之间的内部网络通信同质化，并提供跨领域的非功能关注，比如可观察性和容错。然而，支持服务网格的底层代理技术也可以在您的系统边缘提供很多价值——尤其是在 API 网关内。

尽管服务网格技术似乎是一夜之间突然涌现出来的，但事实是许多组织已经使用我们现在称为服务网格的技术相当长一段时间了(包括[威瑞森](https://getnelson.github.io/nelson/)、[易贝](https://fabiolb.net/)和[脸书](https://code.facebook.com/posts/1906146702752923/open-sourcing-katran-a-scalable-network-load-balancer/))。Lyft 就是这样一个组织，它是一家总部位于美国的拼车服务公司，年收入 10 亿美元。Lyft 也恰好是开源[特使代理](https://www.envoyproxy.io/)的创造者，该代理为服务网格领域的大量开发提供动力，例如 Kubernetes-native [Istio 控制平面](https://istio.io/docs/concepts/what-is-istio/overview/)和 [Ambassador API 网关](https://www.getambassador.io/)。

## SOA 网络的现状

在去年的一次谈话中，特使代理的创始人之一马特·克莱恩(Matt Klein)将 2013 年面向服务的架构(SOA)和微服务网络的状态描述为“[一个真正令人困惑的大混乱](https://www.microservices.com/talks/lyfts-envoy-monolith-service-mesh-matt-klein/)”调试是困难的或不可能的，每个应用程序公开不同的统计数据和日志，并且无法跟踪在参与生成响应的整个服务调用栈中请求是如何处理的。对基础架构组件(如托管负载平衡器、缓存和网络拓扑)的了解也很有限。

“这很痛苦，”他说。“我认为大多数公司和组织都知道 SOA(微服务)是一种未来，实际做它会带来很多灵活性，但在日复一日的基础上，人们会感到很受伤。这种伤害主要与调试有关。”

维护基于 web 的分布式应用程序的可靠性和高可用性是大型组织面临的核心挑战。这些挑战的解决方案通常包括重试逻辑、超时、速率限制和断路的多次或部分实施。许多定制和开源解决方案使用特定于语言(甚至可能是特定于框架)的解决方案，这意味着工程师无意中“基本上永远”将自己锁定在技术堆栈中克莱恩和他在 Lyft 的团队认为一定有更好的方法。最终，特使代理项目被创建为这种更好的方式。

## 由外向内工作:优势代理优势

尽管 Envoy Proxy 项目的开源发布让 Klein 和 Lyft 工程团队看起来像是在 2016 年 9 月的[一夜成名，但事实是，从最初的混合 SOA Lyft 架构到他们当前的微服务和服务网格支持系统，这四年的旅程充满了挑战。在 2017 年](https://eng.lyft.com/announcing-envoy-c-l7-proxy-and-communication-bus-92520b6c8191)[微服务从业者虚拟峰会](https://www.microservices.com/talks/mechanics-deploying-envoy-lyft-matt-klein/)的最近一次演讲中，Klein 谈到了展示面向服务网状网络拓扑的技术迁移的商业价值的基本需求以及相关挑战。

克莱恩的第一条来之不易的建议是，“从边缘代理开始。”基于微服务的 web 应用程序需要边缘反向代理，以避免暴露内部业务服务接口(这将违反松耦合原则)和通过独立的 URI 或 RPC 端点暴露每个服务的高操作开销。现有的云产品在这个边缘代理或网关领域“不太好”，或者作为一系列不同产品的潜在混淆呈现给工程师。相反，Klein 建议在边缘开始实施现代代理技术，因为这以改进的可观察性、负载平衡和动态路由的形式提供了商业价值。一旦工程团队理解了如何在边缘操作代理技术，好处就可以向内滚动，最终创建内部服务网格。

## 边缘的演变:从代理到 API 网关

AppDirect 是一个端到端的商务平台，用于管理基于云的产品和服务，估计年收入为 5000 万美元，它已经开始了与 Lyft 类似的旅程，正如最近的一篇博客文章“[AppDirect Kubernetes 网络基础设施的演变](https://www.appdirect.com/blog/evolution-of-the-appdirect-kubernetes-network-infrastructure)”中所强调的那样。云技术和容器编排器(如 Kubernetes)的动态性和短暂性在可伸缩性和弹性方面提供了许多好处，这意味着它们是公开公共端点以实现通过微服务组合提供的业务功能的额外挑战。

AppDirect 工程团队采取了审慎的方法来解决这些挑战，首先将配置的核心部分设为静态(如暴露的服务端口)，并在每个应用程序前放置一个负载平衡器。他们的第二次迭代使用 HashiCorp 的[consult](https://www.consul.io/)分布式键/值存储和 HAProxy 反向代理，支持在运行时更改配置的“热重新加载”,从而实现了更多的动态性。然而，最终，该团队热衷于利用一个功能更全面的 API 网关所提供的更丰富的功能。

“我们的 API gateway 的目标是让公开的公共 API 不受影响，甚至可以访问传统的 URL 和合作伙伴定制的域，但允许我们通过一个接一个地‘注入’和替换旧组件来增长，”根据博客帖子。

在评估了一系列开源和商业产品后，AppDirect 团队部署了 Kubernetes-native Ambassador API 网关，该网关构建于特使代理之上:

“Ambassador 完全依赖 Kubernetes 原生 API，这是我们所熟知和喜爱的，它是轻量级的、无状态的，并且不使用外部数据存储。大使独家使用 Kubernetes 注释来驱动活动路线配置(即，它是[特使的数据平面](https://blog.envoyproxy.io/the-universal-data-plane-api-d15cec7a)的控制平面)，”该团队在博客帖子中指出。

尽管 AppDirect 尚未完全实现用于内部通信的服务网格，但该公司已经了解了诸如特使代理等技术的好处，以及关键的是，如何在生产中处理这种部署。

## 理解这一切

在云原生实现和迁移中采用服务网格技术才刚刚开始，但已经有可能发现这种技术填补了目前基于现代容器的应用平台(如 Kubernetes)的空白。服务网格的所有优势——如速率限制、断路和可观察性——也可以在系统的边缘加以利用。如果您想探索和了解这项技术，从系统的边缘开始，向内工作可能是一个有效的策略。这还可以让技术在尝试从内向外工作之前展示价值，例如改进的可观察性和弹性。

— [丹尼尔·布莱恩特](https://devops.com/author/daniel-bryant/)