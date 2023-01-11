# SRE(第一部分):现代概述

> 原文：<https://devops.com/sre-part-1-a-modern-overview/>

在过去的几年里，工厂可靠性工程(SRE)已经成为我接触过的许多公司的热门话题。这篇文章是我乐于分享的两篇文章中的第一篇，因为我遇到过许多试图建立和实施这种意识形态的组织，而他们都在问同样的问题——什么是 SRE？谁是 SREs？我们如何得到它？我们从哪里开始？

和其他人一样，我也对这个话题有自己的看法。然而，我们之间有一个共同点。SRE 不仅仅是关于工具和技术，不仅仅是关于你可以雇佣的独角兽，它主要是公司内部的文化转变。它改变了开发人员、产品所有者、管理员、普通工程师等的方式。，都是相互作用的。你必须改变你的运营模式和你在组织中的建设方式。

现在，作为免责声明，这些只是我在建立这样的组织以及与已经实施或正在实施的其他公司交谈时的看法和经验。建设 SRE 没有处方。每家公司都将按照自己的节奏和内部理念来实施。随着时间的推移，您会以适合您的组织和内部运营模式的方式来构建它。不要走得太快，不要试图将模型强加到您的组织中。失败，但要优雅地失败，并从失败中吸取教训。总有一天你会到达你的纳尼亚。

## **定义**

让我们从我们将使用的缩略语的一些快速定义开始。这些将是简短的解释，但给你一个大致的轮廓。

*   **SRE:** 现场可靠性工程师，对基础设施和运营感兴趣的个人，有软件工程背景。
*   **SWE:** 软件工程师，写应用/服务软件的人。
*   **基础设施 SRE:**SRE 的变体，从事基础设施相关项目(监控、供应、IaaS 等)。).
*   **应用/服务 SRE:** 专用于特定应用/服务组的 SRE 的变体。这些是为你的公司创造收入的团队(希望如此)。

SRE 的定义相当分散，我认为没有人真正理解/知道它的意思——不，独角兽不会出现在下面。

这就是 SRE 对我的意义:

*   SRE 是一个拥有多种技能的核心团队。与其说他们是专家，不如说他们是技术通才。这些技能包括运营、基础设施、网络、开发、硬件、分布式系统、监控、稳定性、容量规划、软件工程等。
*   sre 负责技术基础设施和支持服务的架构和实施，重点关注这些平台的稳定性、安全性和可扩展性。
*   sre 应该建立标准的最佳实践、平台、服务、基础设施等。，到达全球组织。
*   SRE 不仅仅是科技。SRE 是一种思维模式、思维过程和文化转变。
*   SRE 不应该成为你公司每个人的强制性要求。如果需要/想要，团队可以选择资助 SRE。

## **职责范围**

技术有如此多不同的方面，以至于似乎很难缩小 sre 实际应该花费时间和精力的范围。由于这些人可能不会直接构建面向公众的产品或功能(当然，这取决于你的公司)，他们具体会做些什么呢？

这绝不仅限于下面的列表，而应该是你开始关注你的 SRE 组织的一般领域。如果这些基础设施管道没有得到正确的构建、监控和扩展，就很难向外部团队成员宣扬这种新的文化心态。以下项目可能看起来非常依赖基础设施，有些可能确实如此。其中许多可以在应用程序 SRE 和基础设施 SRE 之间进行划分。一个是初级生产者，一个是初级消费者。

*   监控。
*   配置管理和自动化。
*   基础设施服务/网络/平台/架构(包括硬件和通用计算)。
*   基础设施工具和产能规划。
*   大数据/数据仓库/数据分析。
*   文档和操作手册。
*   事故响应和事故管理流程。

## SRE 是一支球队还是多支球队？

没有处方，结果会因多种因素而异。然而，我建议，如果你有足够的人员来适应的话，这可以合理地分成多个团队。你可以从小处着手，组建一个涵盖多个领域的通才团队，最终分成更小、更易管理的部分。这些区域是:

*   基础设施(虚拟机管理程序、存储、操作系统、容器、自动化、SDN)。
*   可观察性(监测、遥测、事件关联、趋势分析，在& IM 中)。
*   工具(定制工具、配置管理、开发者体验工具)。
*   服务(数据库、消息队列、编排、微服务)。
*   应用程序(主要是应用程序方面的知识和支持/故障排除的能力)。

即使从某种意义上来说它们是分离的，报告链也必须在整个组织中保持集中。在我看来，分散会破坏团队的有效性和沟通，并导致 SRE 实施的失败。SREs 应向志同道合的个人汇报，他们的使命是推动 SRE 议程和理念。议程不是唯一的原因。中央层次结构允许围绕工具、最佳实践和一般技术/架构指导进行治理。由此，你可以允许这些人在其他团体和团队中交叉授粉，并全面传播这些标准。结构和通信的崩溃将不可避免地导致任务的恶化。

集中化的另一个原因是，它可以让你确保你在 SRE 雇佣的员工不会成为应用团队不想做或已经推掉的运营工作的垃圾场。我过去见过这种情况；这阻碍了新员工，并孤立了他们。他们没有一个任务或一个核心团队来合作，最终只能靠自己去构建那些只适合他们所支持的人的需求的东西，而看不到更大的图景。

应用软件软件工程师应该还在做与运营相关的工作，因为他们是创造需求的人。应用程序 SRE 可以帮助卸载一些工作，并通过中央链找到其他人正在使用什么工具来卸载的方法。对于应用程序团队来说，运营问题可能会很快变成错误的预算。

您的 SREs 可能会分为两个领域:应用 SRE 和基础设施 SRE。这允许你在所有团队中推动同一任务的同时兼顾双方。基础设施 sre 就在那里，而且有很多。我认为这是开发人员、系统工程师和系统管理员的自然发展。你应该专注于建立你的内部人才库，然后去外面招聘。

让团队中的一些软件工程师自愿将工作转移到 SRE，有助于加快特定应用的流程。您可以利用他们对代码库的了解，让他们学习并理解集中的任务和工具，并将其引入他们的堆栈。这些人也可以在应用堆栈上培训中心团队。

然而，并不是你公司的每个团队都需要专门的 SRE 支持。本系列的第二部分将深入探讨应用程序和基础设施 SRE，以及如何从管理的角度组织您的团队。

安东尼·卡亚法