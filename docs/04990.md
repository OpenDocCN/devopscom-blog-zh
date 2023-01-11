# 构建实时应用程序:你现在应该跟踪的 13 个开源项目

> 原文：<https://devops.com/building-a-real-time-app-13-open-source-projects-you-should-be-tracking-right-now/>

开源是当今时代软件消费的主导模式。新锐公司和老牌公司都发现开源软件开发和社区建设是他们整体商业战略的重要组成部分。

对于许多开源项目，独立的指导委员会确保项目保持稳定，不受制于某个公司或利润动机。或者，对于由一家公司提供资金支持并贡献绝大部分开源代码的开放核心项目来说，开源使项目对潜在的新用户公开可用。向公众开放一个项目可以扩大潜在用户和贡献者的范围，从而确保比商业软件提供更快的创新。

## **为你的实时应用选择合适的开源项目**

似乎有无限的开源项目需要评估。更复杂的是，每个项目都有自己的领域能力和文化差异。考虑到单个分布式应用程序将有数十个或更多的开源依赖项，开发团队必须不断测试新的开源产品并磨练使用这些解决方案的新技能，同时构建他们的应用程序。

为了帮助理清这些混乱，我为这篇文章查看了六类开源项目:数据存储、消息系统、服务网格、REST 框架和流框架。对于每个类别，我将确定任何主导者以及其他一些值得注意的项目。

以下是按类别排列的前 13 个开源项目。

## **数据存储:Cassandra，Hazelcast**

[Apache Cassandra](https://cassandra.apache.org/)，最初开发于脸书，是实时应用最广泛的开源项目之一。在功能上，它是一个分布式 NoSQL 数据库管理系统。但实际上，它已经成为大多数大规模实时应用的关键。这是因为 Cassandra 旨在处理许多服务器上的大量实时数据，并具有强大的集群支持。

对于要求极低延迟或具有极高数据速率的应用，[](https://hazelcast.org/)hazel cast 或许可以提供一个有用的替代方案。与 Cassandra 不同，Hazelcast 是一个内存数据网格数据库，它使开发团队能够受益于内存计算的延迟优势。

## **信息系统:卡夫卡、脉冲星、NATS**

[Apache Kafka](https://kafka.apache.org/) 是当今应用开发团队使用的主流开源消息传递系统。Kafka 起源于 LinkedIn，现已发展成为高性能开源消息系统的事实标准。对于流媒体用例，Kafka 用户还可以求助于[Kafka Streams](https://kafka.apache.org/documentation/streams/)。

[阿帕奇脉冲星](https://pulsar.apache.org/) ，雅虎开发是另一个备选的消息传递系统，已经针对流数据源进行了优化。Pulsar 通过共享订阅进一步区分了 TTL 消息支持和队列。

对于延迟是关键考虑因素的应用，[NATs . io](https://nats.io/)([a CNCF 项目](https://www.cncf.io/projects/) )是最快的发布-订阅消息系统之一。

## **服务网格:Istio，Linkerd**

微服务、无服务器和混合云部署等趋势导致分布式应用的架构复杂性不断增加。对于成百上千的分布式应用服务，服务网格提供了一种机制，将所有不同的服务整合成一个可管理的、内聚的整体。

最引人注目的开源服务 mesh 提供的是 [Istio](https://istio.io/) 。作为最受欢迎的开源服务网格项目之一，Istio 主要用于构建在[Kubernetes](https://kubernetes.io/)之上的应用程序。另一种替代方案是 [Linkerd](https://linkerd.io/) ，一种针对 Kubernetes 或其他框架的灵活服务网格解决方案。

## **REST 框架:Node.js，Spring**

[Node.js](https://nodejs.org/en/) 是一个流行的 JavaScript 框架，用于构建可伸缩的 web 应用。在比较 web 开发框架时，Node.js 通常位列前三(与前端框架[react . js](https://reactjs.org/)和 [Angular。JS](https://angularjs.org/) )。虽然 Node.js 可以支持大规模的应用程序，但它不能很好地支持大规模的实时用例。

[Spring](https://spring.io/) 是另一个应用框架，针对分布式微服务风格的架构进行了优化。像 Node.js 一样，Spring“专注于应用程序的‘管道’,这样团队就可以专注于应用程序级的业务逻辑，而不必与特定的部署环境有不必要的联系。”

## **流媒体框架:swimOS**

[SwimOS](https://www.swimos.org/start/) 是一个面向分布式流媒体应用的软件框架。与基于 REST 的框架不同，swimOS 利用了一种独特的轻量级 Web 代理架构，针对实时合成和转换许多数据流进行了优化。面向 DevOps 的项目，如 [Spinnaker](https://www.spinnaker.io/) ，寻求提供一个抽象层来聚合分布式云服务，而 swimOS 提供了跨分布式数据流的抽象，因此团队可以通过在单个网格环境中组合许多分布式数据流来构建应用程序。

为了确保分布式服务的实时一致性，swimOS 自动确保所有 Web 代理之间的最终一致性。有了 UI 工具包和自己的有状态消息协议[【WARP】](https://github.com/swimos/swim/tree/master/swim-system-java/swim-core-java/swim.warp)，swimOS 是构建有状态流应用程序的最快方式。

## **奉献:库柏人、纺纱人、牧场主**

[Kubernetes](https://kubernetes.io/) 是世界上最受关注的开源项目之一。Kubernetes 将自己描述为“自动化部署、扩展和管理容器化应用程序的开源系统”

不管对错，Kubernetes 可能只是一个容器编排平台，但总体上来说，它已经成为 DevOps 的替身。尽管它占据主导地位，但 Kubernetes 也有替代者，例如有 [牧场主](https://rancher.com/) 来管理码头集装箱。

此外，随着应用架构变得越来越分布式和复杂，需要能够融合多个分布式边缘和云环境的平台。[Spinnaker](https://www.spinnaker.io/)提供了一个抽象层来连接各种环境，并提供了一个简单的持续集成/持续交付(CI/CD)机制。

## **最终想法**

您自己的特定用例应该为您团队的实时应用程序确定合适的开源技术。无论您是在构建超高性能的低延迟应用程序，还是只是试图驯服大量实时数据，了解您的选择并选择正确的框架或平台都可以节省您大量的时间和精力。  

开源软件的前景每天都在变化。如果你对上述技术有什么要补充的，或者认为我跳过了下一个 OSS 突破，我很乐意听听。请在下面的评论区告诉我你的想法。

— [克里斯·萨克斯](https://devops.com/author/chris-sachs/)