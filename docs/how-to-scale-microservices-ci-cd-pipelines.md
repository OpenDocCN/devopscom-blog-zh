# 如何扩展微服务 CI/CD 管道

> 原文：<https://devops.com/how-to-scale-microservices-ci-cd-pipelines/>

与传统的整体架构相反，微服务架构理论上可以带来许多好处。微服务将软件元素解耦，支持可重用的组件，并允许独立的开发周期。然而，在实践中，微服务容易出现许多问题。

例如，习惯于传统整体构建过程的团队可能会发现很难重塑他们已建立的实践。此外，随着微服务的数量增加到数百个，为每个服务管理单独的 [CI/CD 管道](https://devops.com/how-to-implement-an-effective-ci-cd-pipeline/)变得难以为继，特别是当 DevOps 组件并不总是优化以精确适应每个管道时。

Codefresh 的首席技术传道者 Dan Garfield 在 DevNetwork Dev Professional 系列第五集的[中提出了一些现实世界中的问题。在本文中，我们将跟随他的演讲，探讨微服务的优势、它们在真实 CI/CD 案例研究中的障碍，以及随着复杂性和数量的增加而扩展交付的解决方案。](https://www.bigmarker.com/devnetwork1/CI-CD-for-Microservices-Best-Practices-and-Lessons-From-the-Trenches)

## 太空中的巨石

为了更好地理解我们为什么需要微服务，加菲尔德使用了一个来自太空的类比——阿波罗 13 号任务。阿波罗 13 号由两艘船组成:登月舱和指令舱。用软件术语来说，这实际上是两块巨大的巨石。

当指令舱出现氧气故障时，它的乘员需要重新使用登月舱的氧气过滤器。然而，登月舱工程师设计了不同的氧气过滤器，导致重新组装和改造这些部件非常令人头痛。

这个类比显示了单一风格的开发是如何创造出狭隘的视野的。当团队采用只适用于整体的指导方针时，他们通常在外部是不兼容的。这扼杀了可重用组件的可能性，从而降低了代码价值并扩展了整体开发工作。

“能够重用组件和独立扩展是微服务的好处，”加菲尔德说。

## Expedia 的微服务之旅

以 Expedia 为例，看看真实世界的微服务架构。以前，Expedia 服务存在于 monoliths 中，这意味着大量的重复。服务被不利地束缚住了，这意味着如果一个服务中断了，你必须修复整个整体。

加菲尔德描述了 Expedia 如何将其架构隔离到单个微服务中，以表示汽车搜索、汽车分类、预订、航空公司搜索等功能。虽然这有助于提高弹性和可用性，但微服务之旅也带来了一些问题。

## 微服务天堂的问题

Expedia 在他们的微服务之旅中遇到了多个问题。尽管 Expedia 有充分的商业理由采用微服务，但“他们没有一个现实的如何扩展 CI/CD 的计划，”Garfield 表示。

首先，随着微服务的数量增加到成百上千，标准化 CI/CD 变得相当困难。该组织对每个服务使用一个 CI/CD 管道，这意味着他们现在必须支持数千个管道，每个管道都连接到一个单独的 Git 存储库。一个微服务还可能有不同的管道用于生产、内部使用或测试环境，从而导致更多的重复。

当您扩展微服务时，您还会遇到一系列与网络和存储相关的新障碍。当 Expedia 意识到在数以千计的独立 CI/CD 管道上运行验证和集成测试的巨大网络带宽和相关成本时，这一点变得非常明显。

“自动化的规模本身就是大多数人遇到最大瓶颈的地方，”加菲尔德说。

用插件和共享库整合代码库成为一个普遍的问题。Expedia 开发人员遇到了 Jenkins 的问题，被迫以编程方式或手动方式编辑每个管道，从一个管道向另一个管道复制和粘贴代码。简而言之，流动并不容易，团队之间不同的方法导致了它的阴影。

## 扩展微服务的解决方案

为了帮助缓解大规模微服务环境和 CI/CD 管道，Garfield 建议采取以下几种方法:

*   使用基于容器的管道:【Garfield 建议的第一个原则是使用基于容器的管道。如果管道是容器化的，你可以用不同的语言版本独立运行它。根据 Garfield 的说法，“共享库不是解决方案”，因为它们会产生特定版本的冲突。使用 Docker 映像比共享库更好，因为用户可以自助使用他们想要的任何版本的映像。

在 [Docker Hub](https://hub.docker.com/search?q=&type=image) 上有许多资源可以简化常见的 CI/CD 步骤，例如构建 Docker 映像、git 克隆、运行单元测试、林挺项目和安全扫描。使用这些图像有助于避免开发工作的浪费。

*   **整合到一个可根据环境运行的单一管道:**Garfield 建议您不要为所有微服务管理数千个管道，而是为所有集成和部署使用一个可延展的管道。他的方法包括触发器，它携带信息来指导行动。

在这种设置中，触发器携带上下文或元数据，允许管道相应地更改其行为。这些触发器可以是基于时间的，也可以是以 repo Git commit 或推送新映像等操作为中心的。当一个触发器被启动时，触发器引入相关的依赖来执行一个动作，比如克隆一个存储库或者克隆一个代码库。接下来的步骤可以使用这些唯一的标准。

Garfield 展示了这是如何在 Codefresh CI 平台中通过本地 Kubernetes 集成实现的。该平台还允许您根据特定标准进行筛选和查看；进入提交和更改的窗口。

加菲尔德承认，这一总体战略确实意味着让微服务更加统一，但或许部署的便利性会超过开发的限制。

*   **采用 canary release 测试:**如果一个组织拥有数百或数千个微服务，让每个微服务运行独立的测试很快就会变得成本高昂。正如 Garfield 指出的，“随着基础设施复杂性的增加，早期测试变得不那么有用了。”

为了解决这个问题，团队可以采用金丝雀释放策略。金丝雀发布是一种实践，在这种实践中，新软件首先在一小组用户中发布和测试。加菲尔德说，这是一个“限制错误变化的爆炸半径”的好方法。

## 持久形象:管道可重复使用

采用单个基于容器的 CI 管道有助于解决大规模微服务测试和部署中日益增多的问题。通过模板化管道，许多微服务可以抽象出复杂性并重用相同的模块化组件。本质上，使 CI/CD 像微服务一样可重用。