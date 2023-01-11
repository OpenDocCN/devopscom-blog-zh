# 了解您的微服务在做什么

> 原文：<https://devops.com/observability-knowing-what-your-microservices-doing/>

微维修不容易，但很有必要。在云原生世界中，将你的整体分解成微服务是必须的，但这不会自动让一切变得更容易。有些事情实际上变得更加困难。增加复杂性的一个明显领域是服务之间的通信；服务到服务通信的可见性可能很难实现，但对于构建优化的弹性架构至关重要。

监控的想法已经存在一段时间了，但是可观察性在云环境中变得越来越重要。监控旨在给出系统整体健康状况的概念，而可观察性旨在提供对系统行为的洞察。可观察性是关于数据暴露和轻松访问信息，当您需要一种方法来查看通信何时失败、何时没有按预期发生或何时不应该发生时，这一点至关重要。需要监控、管理和控制服务在运行时相互交互的方式。这从可观察性和理解微服务架构行为的能力开始。

微服务的一个主要挑战是试图理解整个系统的各个部分是如何交互的。单个事务可以流经许多独立部署的微服务或 pod，发现哪里出现了性能瓶颈可以提供有价值的信息。

这取决于你问的是谁，但是许多考虑或实现服务网格的人说，他们寻求的首要特性是可观察性。一个网格还提供了许多其他的特性，但那是另一个博客的内容。在这里，我将介绍服务网格提供的顶级可观察性特性。

## **追踪**

关于您的微服务架构，需要了解的一件极其重要的事情是，用户事务中涉及哪些微服务。如果许多团队都在部署他们的数十个微服务，并且彼此独立，那么很难理解跨服务的依赖性。服务网格提供了一致性，这意味着跟踪是与编程语言无关的，解决了多语言世界中的不一致性，在这个世界中，每个团队都有自己的微服务，可以使用不同的编程语言和框架。

分布式跟踪对于调试和理解应用程序的行为非常有用。理解所有跟踪数据的关键是能够关联来自与单个客户端请求相关的不同微服务的跨度。为此，应用程序中的所有微服务都应该传播跟踪头。如果您使用的是构建于 Istio 之上的 Aspen Mesh 之类的服务网格，那么入口和侧柜代理会自动添加适当的跟踪头，并将范围报告给跟踪收集器后端。Istio 提供了现成的分布式跟踪，使得将跟踪集成到您的系统中变得很容易。在应用程序中传播跟踪头可以提供很好的分层跟踪，以图形显示微服务之间的关系。这使得很容易理解当您的服务交互时发生了什么，以及是否有任何问题。

## **指标**

服务网格可以从整个网格收集遥测数据，并为每一跳生成一致的度量。通过网格部署您的服务流量意味着您自动收集细粒度的指标，并提供高级应用程序信息，因为它们是为每个服务代理报告的。遥测数据是从任何提供网络和 L7 协议指标的服务舱中自动收集的。服务网格指标通过生成统一的指标来提供一致的视图。您不必担心协调各种运行时代理发出的不同类型的指标，也不必添加任意代理来收集遗留应用的指标。也不再需要依赖开发过程来正确地检测应用程序以生成指标。服务网格看到所有流量，甚至进出传统“黑盒”服务的流量，并为所有流量生成指标。

服务网格收集和标准化的有价值的指标包括:

*   成功率。
*   请求音量。
*   请求持续时间。
*   请求大小。
*   请求和错误计数。
*   潜伏。
*   HTTP 错误代码。

这些指标使您更容易理解整个体系结构中发生了什么，以及如何优化性能。

微服务领域的大多数故障都发生在服务之间的交互过程中，因此查看这些事务有助于团队更好地管理架构以避免故障。服务网格提供的可观察性使您更容易看到服务相互交互时发生的情况，从而更容易构建更高效、更具弹性和更安全的微服务架构。

——Zach jory