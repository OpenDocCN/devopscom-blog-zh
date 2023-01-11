# 继承建筑之美

> 原文：<https://devops.com/devops-beauty-inheritance-architectures/>

剧透:这篇文章不是关于继承你曾祖父母的遗产。而是关于如何将继承的原则嵌入到您选择的 DevOps 工具集的架构中，从而产生指数级的结果。是的，我认识到，作为客户，您与供应商在什么基础上构建工具架构没有什么关系。但是，作为客户，你可以用脚投票，搜索出提供继承等特性的产品，奖励拥有这些特性的供应商，惩罚没有这些特性的供应商。这里要解决的简单问题是，客户为什么要关心？

像任何可以生长的东西一样，规模的可持续性是一个关键问题。当我在这个特定的 DevOps 工具集上维护 6，000 个应用程序时，相对于我开始时的 6 个应用程序，我将花费多少？您也可以推断维护更多的技术具有相同的需求。例如，如果我需要在“x”个不同版本的操作系统上维护三个不同类型的数据库、两个不同的中间件、四个不同的硬件平台……您会明白的。应用程序组合越大(就应用程序的数量而言)，或者技术组合越复杂(就应用程序中技术组件的数量而言)，最终会让您担心在您选择的 DevOps 工具集中维护这些应用程序有多容易。

您选择的 DevOps 工具集的功能将决定您的服务的初始采用以及您所服务的应用程序组合的持续维护的成本。当企业开始看到每考虑一个新的应用程序或技术风险，开发运维工程人员就会一对一地增加时，就很难向企业推销开发运维的价值。然而，驱动大型 DevOps 支持人员组织的罪魁祸首之一归结于最初选择的工具中缺乏继承架构。

## **设定共同语言** 

因此，在我们讨论继承将如何使我们受益之前，首先让我们就什么是“应用程序”达成共识。当你对某人说“应用”这个词时，你会得到各种各样的反应，从你手机上的东西到主机上的一群东西。让我们首先通过在 DevOps 服务集(不考虑平台)上加载和维护“应用程序”来研究什么是“应用程序”。

考虑一下我们用来描述软件结构的层次结构。从层次结构的角度来讨论软件如何工作是相对容易的。首先，在最低层，我们可以描述拥有多个技术组件(或者在构建中必须解决的特定技术的最低层)。接下来，将这些组件组装在一起，就形成了单个应用程序的样子。最后，将具有共同对称性或共同目的的多个应用程序组装在一起，形成一个系统或一系列应用程序。

一个不完美但快速的例子可能是其 Office 应用程序的 Microsoft 组织结构图组件。为了举例，我们将论证组织结构图、剪贴画管理器和公式编辑器都是应用程序 Microsoft Excel 的组件。为了构建应用程序 Excel 的新版本，我们将不得不处理每一个单独的组件，一旦在我们的构建中组装，将创建 Excel 的新版本。当你把更多的应用程序——Excel、Word、Outlook 和 PowerPoint——组合在一起时，你就得到一个系统，或者说一个系列，叫做 MS Office。(是的，我知道这是一个不太理想的例子，但这只是为了说明一点。)

## **评估工作成果**

以这种方式讨论软件的原因允许我们开始讨论使软件自动化的努力程度。通过处理自动化每个组件的工作(按类型)，我们可以开始估计完成“软件的自动化”需要多长时间例如，如果我自己开发的应用程序有一个源代码组件、一个配置文件组件、一个数据库组件和一个中间件组件，那么我有四个组件必须自动化(或包含在构建和部署过程中)来组装我的应用程序的新版本。

这给了我们一种“最小公分母”语言来评估自动化一个给定的应用程序需要多少努力。我见过大多数常见的应用程序只有两到三个组件。但我也见过一些应用程序，由于其独特的架构和构造，每个程序有 30 到 50 个组件。显然，自动化一个只有三个组件的应用程序比自动化一个有 50 个组件的应用程序更容易。我们需要在自动化的易用性上应用的另一个因素是，在我之前的自动化工作中，我是否遇到过这种特定的组件技术。

比方说，我评估的应用程序包含 Java 组件。如果我在此之前遇到过 Java 自动化，我应该已经为 Java 类型的组件自动化构建了一个模板，我可以在类似这样的情况下使用它。在这种情况下，一个熟悉的技术组件比一个新的组件(或者说，对我来说是新的)更容易自动化。然而，如果这是我第一次看到 Java，那么我可能会花更长的时间来为这个应用程序构造我想要的模板，并且为我将来遇到的应用程序，也使用这种技术类型。

## **传承之美** 

这就是继承开始发挥其关键作用的地方。如果我的 DevOps-build 构造工具包含继承，那么我可以为我遇到的每种技术类型构造一个“主”模板或框架。例如，SQL 数据库或 Oracle 或 DB2 的主模板。或者，我可以为 WebSphere 或 SharePoint 类型的技术制作一个主模板——为我店里的每种编程语言制作一个主模板。你明白了。

这样做允许我拥有有限数量的主模板，我可以在其中维护公司希望我为给定技术类型执行的所有关键步骤和流程。如果不同的业务组织或开发组织需要一个变体，他们可以创建一个我的主人的“孩子”，并根据自己的需要进行变体。只要保持与我的父/主模板的关联，我就可以根据公司的要求做出重大的、全局性的改变，而业务部门可以继续根据他们的独特需求改变项目。

在这种情况下，拥有继承允许我通过简单地调整组件的主模板，为给定的技术向整个组织推出变更，例如安全补丁或过程。继承自动地将我的变化传递给我主人的所有“孩子”，如果需要的话，还可能传递给他们所有的“孩子”。另一种选择是，必须检查每个具有目标技术组件的应用程序的特定自动化，并手动更新它，希望我不会错过任何一个，并希望我可能需要调整的步骤不会破坏旧的自动化，而不是按照我需要的方式改变它。

想象一下，有一个 WebSphere 主题专家能够通过简单地调整一个主模板来调整使用您的 WebSphere 公司安装的每个客户端应用程序。或者让网络专家或数据库专家对所有使用其特定技术组件的应用程序一次做同样的事情。继承保留了现实世界中对同一公司内相同技术类型的有限变更的需求，将变更从父代传递到子代。

一刀切是不切实际的。使用复制/粘贴需要手动重复更新每个受影响的模板或框架。但是，如果能够从一个主干创建分支，并且不会失去与主干的连接，就可以从一个中心控制点进行公司范围的变更。维护或管理的成本是巨大的；遗传可以减少它们。这允许由更少数量的工程人员支持更高比例的应用程序或技术组件。

## **影响更广的遗产** 

继承在发布编排软件时也非常有用。大多数供应商都提供剪切粘贴的方法:你复制你所做的最后一个版本，稍微修改一下，然后再使用它。这可能对一些组织有用。但是拥有继承特性会在如何为给定的业务线构建版本以及如何以最小的努力实现公司治理方面创造全新的动力。在这种情况下，可以构建一个公司主发布模板，子发布可以从主发布继承所有需要的主要治理，而没有遗漏的风险。

我意识到在评估 DevOps 工具解决方案时，继承架构可能不在您的列表的顶端。但我认为这是一个战略家的工作(如果你需要，让我知道，我正在寻找🙂)指出长期可持续性如何从这一架构特性中获得巨大好处——即使供应商非常希望引导您远离它。如果您已经承诺了一个工具解决方案，那么您可能希望在下一次供应商特性性能会议上提出这个问题。如果没有，您至少应该考虑拥有它对您的内部成本结构意味着什么，以及没有它会增加任何提议的解决方案的真实拥有成本。

要继续对话，请随时[联系我](/cdn-cgi/l/email-protection#82e9f0ebf1f6ebe3ecacece7eef1edecc2eaedf6efe3ebeeace1edef)。