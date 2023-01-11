# 视频并没有杀死电台明星——IT 运营仍在继续

> 原文：<https://devops.com/it-ops-continues-on/>

Buggles 的经典歌曲“视频杀死了电台明星”可能是一首热门歌曲，也是 80 年代初备受争议的想法，但回顾过去 40 年，我们知道视频没有杀死电台明星-它只是改变了他。就像 MTV 没能干掉电台明星一样，DevOps 也会没能干掉 IT Ops。

当今动态的虚拟化和充满云的世界极大地改变了 IT。借助软件定义的“一切”和虚拟化的计算、网络、存储等。，一切都是流动的。最重要的是，带宽是无限的，而且不贵；让卸载和搬运物品变得更加容易，这在几年前是我们无法想象的。因此，支持这些技术的基础设施是高度分布式的，不再能够从一个地方提供服务。所有这些都极大地改变了 IT 运营的方式。为了了解 IT 运营的变化，我们需要回顾一下过去。然而，我们不需要回顾太久。

大多数组织都有独立的业务部门。无论是拥有独立业务的大型组织，还是拥有独立部门的小型组织，这些业务部门经常会发现自己在争夺共享的 it 资源。五年前，业务部门争夺 IT 部门共享应用程序开发人员的时间。现在，随着快速交付应用程序开发技术的爆炸式增长和成熟，以及越来越多的在线收入产生或影响，这些业务部门向首席信息官游说，将应用程序开发人员和应用程序支持职能纳入他们的控制范围是有道理的。如今，应用程序开发已经成为大多数企业的重要组成部分..

一旦发生这种情况，预算的分配也发生了变化，从 IT 运营中完全控制了 IT 预算。如今，多达 30%的 IT 预算由各个业务部门决定。这是因为业务部门没有从共享应用程序开发人员方法中获得他们想要的优先级。在业务部门看来，IT 部门的发展速度不够快，或者没有业务部门那样的优先级。没有人满意。因此，管理团队将应用程序开发和支持预算转移到各自的业务部门，部分是为了停止争吵。

其中一些业务部门拿走了他们的资金，并将其用于外包开发或购买软件即服务应用程序。一旦云平台和廉价、无限的带宽到来，业务部门就有了替代方案，并且使用了它们。

对于业务部门来说，这一切都合乎逻辑，但对组织来说，这并非没有风险。由于应用程序是在 IT 运营部门的权限之外开发、控制和交付的，人们担心这些应用程序是否符合 HIPAA 或 PCI 合规性标准、IT 安全标准、业务连续性保证或备份计划。需要妥协。大多数组织想出的办法是让 IT 运营部门处理一般的基础架构，并允许每个业务部门利用其余部分(约占预算的 30%)做他们想做的事情。这个看起来怎么样？

今天的大多数应用程序都是组件化的。以零售应用为例，产品浏览、购物车、支付页面以及确认和履行都是独立的应用。虽然底层基础设施(应用的配置、监控和支持方式)需要由 IT 运营部门来处理，但每个组件都有自己的更新计划，并有自己的团队来维护和微调这些应用，以确保它们对业务目标负责。但是，您可能会问，如果不是 IT 运营，团队由谁组成？

**DevOps:开发和运营的交集**

进入 DevOps。DevOps 是那些对不同的人有不同含义的术语之一，但从最简单的定义来看，DevOps 是开发和运营的融合。Forrester 分析师 Mike Gualtieri 一针见血地说道:“DevOps 的目标是让部署应用程序的过程更快、更顺畅。”

没有“开发运维”,所有应用程序问题(停机等。)将发送给 IT 运营部。因为 IT 运营是共享的，有其他优先级，不一定知道每个业务部门的目标，所以这不是最实际的选择。当然，IT 运营人员是精明能干的人，但他们擅长维护基础设施，他们不是专业的应用专家。一些组织有数百个不同的应用程序分布在十几个业务部门中。任何人都不可能指望 IT 运营人员了解每个特定应用程序的特定需求和行为。

应用程序开发人员最了解应用程序，他们知道需求以及如何诊断问题。他们需要一个深入的解决方案来跟踪交易和终端用户体验。而且，从一般意义上来说，他们最了解应用程序需要什么。多少 CPU，多少存储，多少 RAM 等等。但是，他们不具备 VMware vSphere、Cisco UCS、VCE vBlock、FlexPod、IBM 硬件、NetApp 存储、EMC 存储等方面的专业知识。他们是开发商。他们可以操作性地管理他们的应用程序，但是当他们遇到基础架构问题时会发生什么呢？这就是 IT 运营的用武之地。

Gualtieri 还说:“DevOps 是一套松散定义的新兴实践，旨在让开发人员和运营专业人员一起工作。开发人员和运营专业人员经常意见相左。开发者希望更频繁地发布软件；运营专业人员希望保护基础架构的稳定性。”

这就是为什么 IT 预算中从 IT 部门转移到各个业务部门的部分持续增长。当人们开始谈论 It 运营的终结，或者在某些情况下，谈论运营的终结(NoOps)时，这并不奇怪。

然而，尽管组织正在从监督 100%预算的 it 运营转向现在由单个业务部门管理的大部分 it，但如果没有 IT 运营，每个部门都将控制自己的所有 IT。想象一下没有 IT 运营的统一通信。你真的希望每个业务部门都负责这个吗？不，你想要规模经济。您希望共享它—网络、带宽、存储—IT 运营部门将继续管理所有这些。

正如 Gualtieri 指出的，“开发人员和操作人员需要团结一致，以最好地满足业务需求。”最近的研究证明了这一点。Puppet Labs 对 DevOps 状态的一项研究发现，IT 性能与 DevOps 实践密切相关，如主动监控、持续交付和集成。事实上，根据研究，开发运维实践可以提升 IT 性能，并最终提高企业的利润。

IT 团队采用更具咨询性和战略性的方法，与开发人员和 IT 基础设施的其他用户合作，确保他们都能获得他们需要的东西，没有瓶颈或进入障碍。尽管事实上组织内的 IT 运营和开发运维似乎都有发展空间，但很明显，这种转变正在发生。

**IT 运营:转向大型服务提供商**

利用最新的技术创新和规模经济，许多组织现在都在使用服务提供商，而不是拥有自己的基础架构。有人可能会说这是在排挤 IT 运营人员，他们是对的，但不要担心他们不会成为濒危物种。IT 运营专业人员不再为大型企业工作，而是为大型服务提供商工作。他们没有离开，只是离开了现场。

内部 IT 运营的预算可能会继续下降，但托管基础架构的成本会上升，因此 IT 运营的预算会持平。IT 运营没有消失，而是在转变。

在这个时代，老年退休金已经成为时尚，关于条款的激烈辩论已经引起了技术界的关注，这并不奇怪，我们大多数人都不知道未来会发生什么。有一点是肯定的，无论是 DevOps、IT Ops 还是 SecDevOps，组织内都会继续有 Ops 的位置。