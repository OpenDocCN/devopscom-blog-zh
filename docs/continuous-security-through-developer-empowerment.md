# 通过开发人员授权实现持续的安全性

> 原文：<https://devops.com/continuous-security-through-developer-empowerment/>

每个组织都在不同程度上采用 DevOps。快速发布软件和适应市场需求的商业影响是如此巨大，以至于它已经成为一种需求——你要么走向 DevOps，要么走向破产。然而，随着我们对速度的需求增加，我们对安全性的需求也在增加——而将两者结合起来绝非易事。

实现 DevOps 速度的关键是开发者自治。开发人员和他们周围的应用程序团队需要每天决定构建什么和如何构建，他们需要自己完成这些工作。当团队被要求获得外部批准时，瓶颈就出现了，减缓了过程并消除了开发团队的主人翁意识。由此产生的结果是应用程序的不良结果和优秀开发人员的流失。

然而，不幸的是，安全实践常常依赖于这样的审查。安全审计和审查是大多数安全组织的基本工作，需要专家来确定决策是否安全。为了让安全性跟上开发的速度，这种做法必须改变，并给予开发人员做出安全决策的权力。唯一的选择是不安全的软件和软件版本开发的减速。

为了持续的安全软件开发，我们如何实现这样的开发者授权？让我们回顾一些关键实践，并从运营实践中寻找灵感。

## **思维转变:从超级英雄操作员到乘数工程师**

站点可靠性工程(SRE)团队与之前的系统管理员一样，对服务的正常运行负有相同的责任。角色的变化来自于他们如何获得这种弹性。sre 不处理大多数事件，也不审查所有影响可靠性的代码。相反，他们设计工具，使开发人员能够处理 oncall，并以正确的方式构建可操作的软件。SRE 应该只在极端情况下使用，无论是事件还是架构审查。

安全团队必须以同样的方式运作。他们的工作必须是战术性的，努力减少他们在过程中的参与，给开发人员更多的责任。在需要他们的专业知识的情况下会出现，但是一般的调查应该保持在最低限度。

## **工具变化:从安全工具到开发者工具**

在 DevOps 投入使用之前，应用性能监控(APM)归 IT 部门所有，他们使用来自世界各地的综合测量数据来评估和监控应用的性能。这些解决方案很强大，但是他们的开发者体验很糟糕。它们非常昂贵，这限制了开发人员可以运行的测试。他们擅长于通过聚集测试来解释状态，但是对于试图解决性能问题的开发人员来说没有什么价值。因此，开发人员很少使用它们。

然后，New Relic 出现了，引入了一种不同的 APM 方法。他们的工具一开始是免费或便宜的，使得所有开发团队都可以使用。他们使用插装在开发人员术语中提供丰富的结果(调用栈、代码行)，使它们更好地修复问题。这种新方法彻底改变了 T2 的 APM 行业，将性能监控嵌入到开发实践中，使网络速度更快。

应用安全也需要如此。如果开发人员是做出有影响力的安全决策的人，那么安全工具最重要的用户不再是安全人员，而是开发人员自己。因此，安全工具应该首先关注开发人员的采用，即使这是以相关安全人员付出更多努力为代价。

## **治理变革:从阻止到监控**

我最喜欢的 DevOps 格言之一是，“如果它移动，测量它。如果它不动，就测量一下，以防它动”。它体现了成功监控您正在运行的应用程序是多么重要。虽然 CI/CD 管道帮助您将软件投入生产，但监控让您有信心快速完成这项工作。当你确信你会很快发现错误并恢复或推出解决方案时，你就不需要太担心发布错误了。

安全需要采用这种方法。发现一个刚刚被部署的安全漏洞并采取行动，几乎与在它被部署之前阻止它一样好，而且破坏性要小得多。但是要接受这一点，你需要在监控上投资。

开发人员是申请流程的第一步。他们也是安全解决方案的工程师，这是有道理的。让开发人员能够做出安全第一的决策，使 IT 团队和安全专业人员能够处理业务的不同部分，节省开发过程中的时间，并最终创建更强大的应用程序和成果。