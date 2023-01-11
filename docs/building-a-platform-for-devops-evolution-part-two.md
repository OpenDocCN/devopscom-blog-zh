# 构建 DevOps 演进平台，第二部分

> 原文：<https://devops.com/building-a-platform-for-devops-evolution-part-two/>

在本系列 的 [介绍中，我们讨论了变更的概念以及它如何应用于开发运维环境和发布经理。](https://devops.com/building-a-platform-for-devops-evolution-part-one/)

在我们的环境和用户需求不断变化的世界中，DevOps 必须维护大型组织中数百个移动的部分，这些人天生就反对变化。这要求发布经理下放权力，从中央集权的指挥官转变为推动者，理解不同的价值流，并不断进行试验。

在这一节中，我们将介绍一些方法和实验类型，DevOps 组织可以使用 DevOps 原则来改进他们的发布管理过程并达到他们的目标。

### 价值流图

[价值流图](https://www.plutora.com/blog/value-stream-mapping?utm_source=ebook_release_manager) 是组织用来提供其客户想要或需要的产品或服务的一系列步骤。从传统的意义上来说，发布和部署过程可能看起来很乏味，特别是当团队必须与发布管理团队沟通来在日程表上安排发布时段的时候。

尽管有优势，价值流图也有一些缺点。这需要很多人，很难协调，也很少重复。

价值流管理平台可以提取四个关键的 [DevOps 指标](https://www.plutora.com/blog/10-essential-devops-metrics-that-really-matter?utm_source=ebook_release_manager) 供团队实时检查和调整。但是，使用这四个指标有一些缺点:

*   **交付周期**的特征是从代码提交到生效的时间；然而，在价值流管理中，我们也考虑一个想法或客户要求达到价值实现所需的时间。
*   当团队偶尔部署但仍在改进时，部署频率变得有趣，但是当团队获得按需发布的能力时，其他度量变得更有帮助。

因此，团队必须随着时间的推移改变度量标准，以匹配团队的能力。这就是为什么让价值流团队发现和衡量他们自己的指标是至关重要的。另一个因素是，人们更有可能为了自己而改变，而不是别人强加给他们。

### 减少批量

批量的减少降低了风险，减少了活动在队列中等待的时间。当变更很小时，它们可以被快速地实现，并且导致中断的危险更小，从而使得阶段之间的区别不那么重要。

虽然一些关键指标可以通过 backlog 或 release automation 等特定工具来访问，但如果没有价值流管理平台，就很难深入了解总体排队时间。

当 DevOps 工具链的所有方面结合在一起时，价值流图就会自动绘制，从而形成一个从想法到实现的统一系统，使团队能够了解他们的周期时间和价值流效率，并观察变化如何改进工作。

### 从整体架构到微服务架构的演变

大多数组织都有整体的、紧密耦合的应用程序，因为这是过去最好的软件设计方法。然而，随着行业的发展，发布经理越来越意识到这种架构方法的局限性:

*   需要大量的工作来构建、测试和部署。
*   依赖关系必须被管理，包括人和系统。
*   依赖导致脆弱。
*   脆弱导致官僚主义(如 [出租车](https://www.plutora.com/blog/cab-and-release-management-whats-the-connection?utm_source=ebook_release_manager) )。
*   官僚主义和交接阻碍了流动。

将应用程序重新架构到微服务，就像改变系统中的人类行为一样，不会在一夜之间发生，在这个过程中经常会遇到瓶颈。这通常是一个“改变或死亡”的对话。如果应用程序没有变得更有能力改变，市场颠覆者将为消费者提供新的体验，客户将跳槽到这些竞争对手。

价值流管理平台可以揭示限制、延迟和依赖性发生在哪里，以及如何减少它们。正如 DevOps 的一个宗旨所说，“不要管理依赖；打破它们。”

然而，对于许多公司来说，通往系统自治或松散耦合系统的道路是漫长的，需要许多渐进的改进步骤。扼杀者模式推荐这种方法:一次一点点地削减整体功能。

在应用程序架构变更期间，我们需要支持价值流团队，这样他们就不会浪费时间在未知依赖关系导致的意外工作上。我们还需要他们看到并欣赏他们在价值流管理平台的支持下取得的进步。

发布经理的部分工作是识别价值流的成功故事，并与其他价值流分享，以便局部的改进可以成为全局的。

### 将发布管理角色转移给价值流团队

当团队在小的变更上独立工作时，他们可以在准备好的时候发布它们。然而，从一个状态转移到另一个状态需要时间来过渡到旅程的那个阶段。

在传统的工作方法中，发布过程很可能由一个发布经理或者一个发布经理团队来协调。发布经理的角色可以转移到价值流团队，该团队提供对系统的访问，该系统向发布经理提供对当前发布的可见性。

跨价值流的操作透明性为传统的发布经理提供了巨大的安慰，减轻了他们的管理压力。它允许个人学习新技能，提炼他们从工作中获得的意义和目的。

通过采用端到端和跨价值流的方法来进行变更和改进，并确保责备成为责任，发布经理可以成为这些改进成功的关键。价值流管理平台提供了支持对话所需的数据，这些对话将导致这种文化和行为的转变。

在本系列的第三部分也是最后一部分，我们将涵盖更多类型的实验，并开发实现变化和推动结果的最佳实践。