# 如何处理 DevOps 微服务(提示:小心)

> 原文：<https://devops.com/how-to-handle-devops-microservices-hint-carefully/>

> 考虑到开发管道中可能涉及到的令人眼花缭乱的同类最佳工具，一个编写良好的微服务只需足够的代码就可以拯救一切。但是任何东西太多都不是好事。以下是如何以及何时使用微服务。

微服务现在风靡一时:这些迷你应用程序被用来集成分布式应用程序，可以更容易地修改。微服务就像胶水一样，将 DevOps 自动化工作流中的流程和系统粘在一起。这意味着更快、更自动化的周期，更好地实施连续交付，并提高对开发运维流程和部署的可见性。

对于开发人员和测试人员来说，他们通常喜欢使用他们喜欢的工具来完成工作，微服务允许他们通过在 DevOps 管道中连接许多不同的开源和商业工具来实现这一点。虽然其中一些工具内置了与其他流行工具的集成，但这些集成可能无法完全满足您的需求。要求供应商为您构建定制集成可能成本过高，并且在您的组织希望实施的时间框架内可能不可行。

因此，借助微服务，开发团队可以灵活地构建自己的工具堆栈，并集成一切以实现对开发流程的全面了解。同样有用的是，与遗留 API 相比，REST APIs 非常容易使用；开发人员可以编写微服务，而不需要集成产品的专业知识。这些只是微服务方法的几个极其强大的优势。

然而，就像所有其他酷技术一样，也有一些小问题，如下所示:

1.  **难以处理。**微服务依赖于供应商的 API，当这些 API 发生变化时，服务就会中断。然后，您必须从头开始重建服务。这是一项耗时的任务，会影响手头的主要工作:编写和提炼代码。在一个拥有数百个微服务的环境中，很快，开发人员就会将大部分时间花在更新 devops 管道中那些讨厌的迷你应用上，而不是构建新的用户功能。成本上升，时间表延误。
2.  **草率的过程。**让我们面对现实吧，当你只为你的团队编写微服务时，你会尽可能快地完成，从而跳过一些可以使微服务不那么脆弱的步骤。与此同时，一个供应商编写了一个微服务来帮助数百名客户——因此，它必须是防弹的。通过微服务进行集成的内部方法更容易出现问题。一旦一个服务中断，不可避免地会对其他集成点产生多米诺骨牌效应，这意味着您的开发过程会停止。

那么，现在怎么办？让这一切变得简单一点是可能的。首先，确保你已经把经济学搞清楚了。开发微服务作为您的集成策略是否比让供应商为您开发成本更低(考虑员工时间)？如果成本不是主要考虑因素，拥有定制开发运维工具堆栈的好处是否超过了复杂性问题，包括服务中断时的停机风险？定制集成比采用供应商不太完美的集成有明显的优势吗？在选择微服务途径之前进行分析，并记住将所有这些与业务优势联系起来。

**下面是一些降低微服务复杂度的方法:**

**Go hybrid** :在大多数情况下，组织会发现使用供应商集成和微服务的组合通常是答案。

**外包**:对于业务关键型应用程序，让外部开发公司为您处理微服务部分并不是一个坏主意。这将降低您的风险，并解放您的开发人员，使他们专注于构建产品，而不是管理集成。

**工具和语言:**选择能够很好地与 REST APIs 配合的语言来编写微服务，比如 Python 和 Ruby。此外，当你在内部做这件事的时候，留意一些有用的工具，比如 Zapier 或者 TaskTop。我们预计，随着公司扩大使用微服务和容器来优化开发运维，这些自动化选项只会越来越多。

***作者简介/邓恩***

[![AAEAAQAAAAAAAAPqAAAAJDcwMjVkYzMyLTQ1ZGQtNDAwNC1hNWRkLTVjZGJmYTNlZGQwNA](img/a61538bfe115d78a5239231518360894.png) *凯文·邓恩是* ](https://devops.com/wp-content/uploads/2015/10/AAEAAQAAAAAAAAPqAAAAJDcwMjVkYzMyLTQ1ZGQtNDAwNC1hNWRkLTVjZGJmYTNlZGQwNA.jpg) * [QASymphony](http://www.qasymphony.com/) 的战略和业务发展副总裁。他对软件开发和测试的新兴趋势有浓厚的兴趣。Kevin 从 Deloitte 加入 QASymphony，在那里他管理大型政府和财富 500 强项目的测试，交付 ERP 实施和定制软件开发。你可以在 LinkedIn 和 Twitter 上找到他。*