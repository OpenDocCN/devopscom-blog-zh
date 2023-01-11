# 开发人员必须了解的威胁建模知识

> 原文：<https://devops.com/what-developers-must-know-about-threat-modeling/>

威胁建模是一个似乎很少有开发人员追求的过程，但它是一个帮助您和您的团队对您的应用程序的所有潜在威胁建模的过程。从本质上说，威胁建模是您对应用程序面临的所有潜在威胁的思考。这样做实际上就像以结构化的方式将威胁列表放在一起一样简单，让您可以评估任何感知到的风险，让您可以制定如何应对威胁。

最终，通过威胁建模，您可以通过识别目标和漏洞并创建措施来防止威胁对系统的影响，从而优化网络安全。根据这个定义，任何被描述为威胁的东西都有可能对您的组织和数据系统具有恶意；例如，像存储设备故障这样的偶发事件会危及整个企业的完整性。

威胁监控的原因可能很明显，但任何缺乏进展的情况都很常见。

威胁是导致公司在企业安全解决方案上花费 891 亿美元的重要因素之一。 Gartner 预测，到 2018 年底，威胁将达到 963 亿美元。根据雷神公司 2018 年关于网络安全全球大趋势的研究，36%的高级 IT 和网络专业人士将恶意或犯罪内部人员视为首要网络威胁。即使了解了这一点，许多组织仍然缺乏内部威胁策略和策略实施工具，他们努力协调安全和 IT 职责以有效应对威胁。

威胁监控使您能够确定您的应用程序可能存在哪些威胁。知识就是力量，事先知道什么样的危险会等着你总是更好。了解这些威胁可以让您决定是否接受风险。

对于存在的威胁，必须存在以下组合，其中组合的可能性和影响足够大，可以采取措施。理解威胁建模的框架包括:询问你正在做什么，什么可能出错，如何处理，以及工作是否完成得很好。

根据开放网络应用安全项目(OWASP)的说法，威胁建模是一个让您基于迄今为止所做的事情不断完善您的过程的过程:“从所有可能的漏洞开始通常是没有意义的，因为它们中的大多数不会被威胁代理攻击，不会受到安全措施的保护，或者不会导致后果。因此，一般来说，最好从造成很大差异的因素入手。”

这些步骤包括评估范围、识别威胁因素、现有对策、识别漏洞、确定风险优先级以及确定减少威胁的对策。

在评估范围内，您必须了解风险的代价。识别有形资产，如信息数据库或敏感文件，通常很简单，并实现应用程序提供的功能。

接下来，识别可能的威胁或攻击。威胁模型的一个关键部分是描述可能攻击您的应用程序的不同人群的特征——这可能包括内部人员和外部人员，他们执行无意的错误和恶意攻击。在开发的这个阶段，考虑现有的对策，这些对策允许您确定存在哪些必须解决的可能被利用的漏洞。通过您的搜索，寻找弱点，并将您发现的任何攻击与您发现的负面后果联系起来。

一旦确定，就可以对风险管理进行优先排序。对于每个威胁，确定可能的结果及其影响，以了解如何缓解这些问题。接下来，寻找降低未来风险的方法。

虽然许多威胁可能看起来与安全有关，但许多其他威胁有更自然的解释。威胁评估可能包括停电，甚至是被淹没的服务器机房。这些因素和其他因素会给您的组织带来严重威胁。

## **何时对威胁建模？**

在项目开始时进行威胁建模通常是最好的，但是在项目进行到一半甚至结束时进行威胁建模总比根本不进行要好。在项目结束时进行威胁建模可能会有好处，例如理解架构以及数据如何在其中流动。然而，在项目结束时的威胁监控可能会导致发现可能需要更多的工作来修复在开始时没有发现的糟糕的设计决策。

对于那些进入威胁建模的人来说，在现有项目上进行第一次会议，让您尝试威胁建模会议，以便您可以熟悉所需的一切。通过这种方式，您可以更好地准备分析所有资产和数据流以评估风险。一旦这个过程完成了，你就有更好的机会在你的新项目的威胁建模中获得成功。您还可以更好地为项目设计阶段可能存在的威胁做准备。从这里开始，随着时间的推移，您将开始在新功能的初始设计阶段考虑威胁。

## **接近威胁模型**

每种方法都取决于组织及其目标。大型组织通常预先建立了威胁建模流程。不熟悉威胁建模的较小组织可以从雇佣有经验的人来启动任务开始，或者从专家或可以为该计划提供建议的人那里寻求外部支持。

接下来，您需要了解系统中的用户是谁——普通用户、管理员、外包承包商，或许还有使用应用程序或其他工具在网络中寻找漏洞的黑客。还有其他演员，包括心怀不满的前员工。

定义用户参与者非常重要，因为缺少一个组可能意味着您可能缺少整个威胁类别。此外，考虑模型中各种类型的黑客或黑客团体。

## **数据和信息流**

在威胁建模过程的这一点上，跟踪流经系统的各种数据流。对于其中的每一项，您都需要知道数据的去向。一路上它与什么互动或者遇到什么？然后找出数据可能泄漏的地方或可能暴露的地方。更多的数据组件为黑客获取信息创造了更多的机会。

个体数据意味着基于体系结构和具体情况的信息流是不同的。一个例子可能包括来自用户浏览器的请求，其中 cookie 被发送并与多个组件交互。

对于每个数据流，搜索任何参与者获得有价值信息的机会。如果有什么事情让你皱眉，退回到这个过程中，把这个威胁转移到你能减轻皱眉的时刻。

## **威胁列表完成**

当观察到威胁列表并使其完整时，将列表的优先级从非常不可能、不太可能到不可能。不管风险的可能性有多大，都要把风险当作一种真实的可能性来对待。这样做是为了考虑威胁的实际影响及其对组织的意义。这家公司会彻底破产吗？每一点数据都会被卷入勒索的情况吗？设置影响的数字或优先级，如低、中、高。

当您有了风险列表后，通过以下方式管理风险:

1.  **接受**:如果风险相当低，接受潜在影响。也有可能你会发现潜在的负面用户影响更重要。你也可以稍后重新评估。
2.  **转移**:也许另一个团队负责管理某个特定的风险。如果团队可以轻松完成防守，那就外包出去。
3.  **回避**:不要这样。如果必须的话，考虑对数据流进行完全的结构性改变，以避免完全避免风险。这可能意味着需要架构上的改变，或者为了避免危险而完全扼杀一个特定的特性。
4.  **降低**:采取行动，通过降低风险的可能性或影响来降低风险。您可能需要采取多个步骤来减少威胁。无论采取何种行动，都需要努力降低风险。

威胁建模完成后，不要停止。继续工作，因为威胁和参与者在变化。列出所有必须解决的潜在问题或风险，并将其纳入你的计划。

最后，请记住，您应该小心与谁分享您的威胁建模计划。您永远不知道这些信息最终可能会出现在哪里，或者谁会对您的组织及其数据构成威胁。

最后一点:威胁建模的最终结果和有用性几乎完全取决于所建立的参数。定义威胁和影响的概率值可能是主观的，但是让您的经验、同事和专家的意见以及您的直觉来指导您。

-[耶隆拳击](https://devops.com/author/jeroen-boks/)