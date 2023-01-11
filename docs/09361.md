# 特使网关简介

> 原文：<https://devops.com/introducing-envoy-gateway/>

今天，我们激动地宣布 [特使网关、](https://github.com/envoyproxy/gateway) 特使代理家族的新成员，旨在显著降低使用特使 API 网关(有时称为“北南”)用例的门槛。

**历史**

特使 [于 2016 年秋季](https://medium.com/lyft-engineering/announcing-envoy-c-l7-proxy-and-communication-bus-92520b6c8191) 作为 OSS 发布，令我们惊讶的是，它很快在整个行业获得了牵引力。用户被该项目的许多不同方面所吸引，包括它的包容性社区、可扩展性、API 驱动的配置模型、强大的可观察性输出和日益广泛的功能集。

尽管在早期，Envoy 成为“服务网格”的同义词，但它在 Lyft 的首次使用实际上是作为 API 网关/边缘代理，提供深入的可观察性输出，帮助 Lyft 从整体架构迁移到微服务架构。

在过去 5 年多的时间里，我们已经看到 Envoy 被大量最终用户采用，既作为 API 网关，也作为“服务网格”角色中的边车代理。与此同时，我们已经看到了一个围绕 Envoy 的大型供应商生态系统，在 OSS 和专有领域提供了大量的解决方案。Envoy 的供应商生态系统对项目的成功至关重要；如果没有对所有在 Envoy 上兼职或全职工作的员工的资助，这个项目肯定不会有今天的样子。

作为许多不同架构类型和供应商解决方案的一个组成部分，Envoy 的成功的另一面是其固有的低水平；Envoy 不是一个容易学习的软件。虽然该项目已经在世界各地的大型工程组织中获得了巨大的成功，但它只是在较小和较简单的用例中被轻微采用，其中 [nginx](https://nginx.org/) 和[ha proxy](https://www.haproxy.org/)仍然占主导地位。

特使网关项目的诞生源于这样一个信念，即让特使以 API 网关的角色“面向大众”需要两件主要的事情:

*   针对较轻用例的简化部署模型和 API 层。
*   将现有的[【CNCF】](https://www.cncf.io/)API 网关项目( [轮廓](https://projectcontour.io/) 和 [使者](https://github.com/emissary-ingress/emissary) )合并到一个公共核心中，该核心可以提供最佳的入职体验，同时仍然允许供应商基于特使代理和特使网关构建增值解决方案。

我们坚信，如果社区围绕一个单一的 Envoy 品牌 API 网关核心聚合，它将:

*   减少围绕安全性、控制平面技术细节和其他共享问题的重复工作。
*   允许供应商专注于在 Envoy 代理和 Envoy 网关之上以扩展、管理平面 UI 等形式分层增值功能。
*   导致一种“水涨船高”的现象，世界各地更多的用户享受到特使的好处，无论他们的组织是大是小。更多的用户带来更多潜在客户的良性循环，对核心特使项目的更多支持，以及更好的整体体验。

**项目概述**

从较高的层面来看，Envoy Gateway 可以被视为 Envoy 代理核心的包装器。它不会改变核心代理， [xDS](https://www.envoyproxy.io/docs/envoy/latest/api-docs/xds_protocol) ，[go-control-plane](https://github.com/envoyproxy/go-control-plane)等。以任何方式(除了潜在的驱动功能、错误修复和一般改进！).它将提供以下功能:

*   网关用例的简化 API。该 API 将是带有一些特定于特使的扩展的 [Kubernetes 网关 API](https://gateway-api.sigs.k8s.io/) 。之所以选择这个 API，是因为在 Kubernetes 上部署一个入口控制器是这个项目最初的关注点，也因为这个 API 拥有广泛的行业认同。
*   一种“包含电池”的体验，使用户能够尽快启动并运行。这包括提供控制器资源、控制平面资源、代理实例等的工具。
*   一个可扩展的 API 表面。虽然该项目旨在提供现成的通用 API 网关功能(例如，速率限制、认证、 [、加密](https://letsencrypt.org/) 集成等)。)，供应商将能够提供所有 API 的 SaaS 版本，提供额外的 API 和增值功能，如 WAF、增强的可观测性、混沌工程等。
*   高质量的文档和入门指南。我们使用 Envoy Gateway 的主要目标是使最常见的网关用例变得简单，便于普通用户理解。

关于 API 的话题，我们认为导致重大混乱的一个领域是在针对高级用例的其他项目中有效地重新实现 Envoy 的[【xDS】](https://www.envoyproxy.io/docs/envoy/latest/api-docs/xds_protocol)API。这种模式导致用户必须学习多种复杂的 API(最终会转换回 xDS)才能完成工作。因此，Envoy Gateway 致力于“沙上的硬线”,其中 Kubernetes Gateway API(以及该 API 中任何允许的扩展)是唯一受支持的附加 API。更高级的用例将由“xDS 模式”提供服务，在这种模式下，现有的 API 资源将为最终用户自动翻译，然后最终用户可以直接转而使用 xDS APIs。这将导致一个更清晰的主 API，同时为那些可能超越主 API 的表达能力并希望通过 xDS 利用 Envoy 的全部功能的组织提供一个逃生出口。

**接下来的步骤**

今天，我们感谢特使网关的最初赞助商( [大使实验室](https://www.getambassador.io/) ， [保真](https://www.fidelity.com/) ，[Tetrate](https://www.tetrate.io/)，[VMware](https://www.vmware.com/))，并激动地与大家一起开始这一新的旅程。该项目非常早期，到目前为止，重点是就 [目标](https://github.com/envoyproxy/gateway/blob/main/GOALS.md) 和 [高级设计](https://github.com/envoyproxy/gateway/blob/main/docs/design/SYSTEM_DESIGN.md) 达成一致，因此，无论是作为最终用户还是作为系统集成商，这都是一个很好的参与时机。

我们还想非常明确地表示，Contour 和使者的现有用户不会被落下。该项目(以及 [VMware](https://www.vmware.com/) 和[Ambassador Labs](https://www.getambassador.io/))完全致力于确保这些项目的用户最终顺利迁移到 Envoy Gateway，要么通过翻译和替换，要么通过这些项目成为 Envoy Gateway 核心的包装器。

我们对通过特使网关项目将特使带给更多用户感到非常兴奋，我们希望您将 [加入我们](https://github.com/envoyproxy/gateway#contact) 的旅程！