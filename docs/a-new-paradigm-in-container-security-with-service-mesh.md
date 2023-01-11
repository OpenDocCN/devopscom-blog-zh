# 基于服务网格的容器安全新范式

> 原文：<https://devops.com/a-new-paradigm-in-container-security-with-service-mesh/>

容器已经存在了一段时间，但是直到最近，这项技术才变得足够成熟，可以让大型企业在内部和云中采用。对开发人员来说，显而易见的好处包括能够显著缩短生产时间，以及能够降低运营负担。这通过实施服务网格来进一步支持，该服务网格在集装箱化的基础设施之间提供快速、可靠和安全的通信。

## **Kubernetes 的崛起及其对安全的影响**

2014 年末推出的 Kubernetes (k8s)为云和本地环境带来了大规模的容器编排。使用 k8s 的好处是显而易见的，主要是因为它能够独立于基础架构。基于 k8s 的应用程序可以轻松地从您的数据中心扩展到多个云提供商，反之亦然。然而，Kubernetes 面临的挑战是它给安全运营带来了巨大的问题。试图使用传统的防火墙模型在大型 k8s 集群上实施微分段是不可行的。

随着向容器的转移，基于容器的网络安全攻击也会增加。犯罪黑客将一直在寻找利用这一领域的新方法。因为容器操作本质上依赖于开发管道(CI/CD ),所以它们的安全属性也应该如此。任何其他交互点都是事后的想法，会导致操作变慢或安全性降低。迁移到容器和 k8s 的组织应该先发制人，因为规模会导致复杂性不断增加。

## **进入服务网格**

实现服务网格层可以确保容器化基础设施服务之间的通信快速、可靠和安全。它是一个可配置的低延迟基础架构层，处理服务对服务的通信。它负责通过复杂的服务拓扑可靠地传递请求，这些服务组成了一个现代的云原生应用程序。在实践中，服务网格通常被实现为一组称为 sidecars 的轻量级网络代理，它们与应用程序代码一起部署，而应用程序并不知道。网格提供了关键的功能，包括服务发现、负载平衡、加密、可观察性、可跟踪性、认证和授权，以及对断路器模式的支持。

## **标准和安全最佳实践**

*   图像的预扫描是不够的。对容器服务实施运行时微分段应该在运行时解决，因为它们引入了更容易、更显著的攻击媒介。
*   易于与开发管道集成。如上所述，替代方案将影响业务敏捷性或安全质量。
*   微分段应该与基础设施和网络分离，否则，它将需要某种应用程序到 IP/端口/协议的映射。

建议实施为 k8s 环境构建的安全性，并在使用 Istio(由 Google 开发的著名开源服务网格)的本地和公共云中运行。Vet 解决方案通过增强的安全功能直接连接到代码管道，例如对将在代码阶段部署到 k8s 集群的工件进行签名，并具有生成签名身份的能力。当工作负载启动时，管理员将看到服务能够控制它们在哪里运行，而不是查看机器和 IP。

这也将使您能够直观地创建基于身份的微分段。这是一个优势，因为微分段一直是一项复杂的任务，需要管理员将应用程序映射到网络，同时跟踪环境中正在运行的内容。

有了身份和服务网格层，只需要关注您的业务逻辑。身份是在 CI/CD 管道中生成的，这一事实提供了无需服务发现即可控制应用程序的能力。身份通过源自 CI/CD 管道的业务上下文名称来表示，因此运营商可以轻松地将它们组合在一起，并在不同的粒度层分配策略。

K8s 是一项伟大的技术，能够实现集装箱化环境的收获。采用 it 可以显著加快您组织的数字化转型，但这也要求您采用新的应用程序安全方法。与以 k8s 为重点的安全组织签订合同将允许企业以最自动化的方式加速迁移到本地和云中的云原生应用程序。

通过提供所需的安全性和操作能力，k8s 集群管理员可以获得企业级微分段解决方案，该解决方案具有策略编排、多/混合云部署中集群的单一控制台，以及在容器化集群和传统应用程序以及集群外部的其他资源之间进行连接的能力。

— [Ran Ilany](https://devops.com/author/ran-ilany/)