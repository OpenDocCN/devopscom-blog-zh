# 基础设施即代码，旧游戏的新规则

> 原文：<https://devops.com/infrastructure-as-code/>

关于 DevOps 及其在通过提高自动化水平来促进质量和持续改进方面的作用，已经有了很多讨论。反过来，这种自动化是通过新兴的基础设施和软件架构来促进的，这些基础设施和软件架构公开了控制平面和管理编程接口，这在许多圈子里被称为基础设施即代码。

这种移动允许开发和运营人员与用于交付应用程序和数据的底层环境(网络、服务器、操作系统和存储)进行实时交互。这还意味着，随着环境变得更加程序化，企业必须将这种努力视为一流的应用程序开发过程，并确保相应的资产遵循通用的编码实践，并符合一致且可持续的架构。

那些不熟悉系统管理员活动和数据中心运营的人在阅读了关于 DevOps 的新兴文献后，可能会有一种错误的想法，即运营商一直在纯手动流程的基础上运营业务。即使作为一名终身 IT 人员，直到我开始将基础设施和运营作为我工作的一部分，我也不知道在保持数字位在组织中流动的巨大帷幕背后发生了什么。

事实是，运营和管理员多年来一直在开发脚本来自动化日常任务。这些脚本通常用于动态生成或更新重新启动后应用的配置文件。这种对基础设施即代码的改变是很重要的，因为现在这些配置的改变可以在运行中进行，并且通常可以立即执行，而不必使系统离线。如果你现在意识到这可能带来的潜在灾难性后果，你会用手捂住嘴，你会理解这种力量的影响。

借助软件定义的网络、虚拟机管理程序甚至软件定义的存储，运营商可以通过编程方式改变应用底层的整个环境，而无需将这种改变通知应用。从建筑学上来说，这是一件美妙的事情。务实？嗯，有很多糟糕的代码对底层基础设施做出了假设，并且在迁移到这些现代基础设施时即将暴露出来。

因此，构建、测试和部署基础设施控制应用程序必须成为整个软件开发生命周期(SDLC)的一部分，并开始使用相同的受控技术进行构建、测试、部署和管理，这些技术有望用于应用工程开发的任何应用程序。

您可能会问，“等等，这难道不意味着我的 QA 环境必须拥有与我的生产环境相同的基础架构组件吗？”我的回答是，“也许吧！”在某些情况下，这可能有利于确保生产部署可以支持连续的部署过程，这将确保从用户接受到部署的有限人工干预，这将有望导致有限的生产失败机会。然而，由于我们正在转向一个更加程序化的基础设施，许多供应商也可以提供他们的基础设施代码的虚拟实例用于测试，这可能会满足您的需求。

值得注意的是，有许多企业不开发自己的软件。他们主要使用商业现货(COTS)应用程序。因此，这些企业可能没有既定的 SDLC 实践。同样，这些企业可能不相信 DevOps 对他们是相对的，因为他们不做“开发”。如果您的企业属于这一类别，那么迁移到基础架构即代码和软件定义的数据中心应该被视为采用 DevOps 以及正式采用一种定义良好的 SDLC 方法的驱动因素。即使这些组件在几年内不会对您产生影响，直到您的下一个更新周期，DevOps 带来的提高交付质量和一致性的优势现在对您的业务肯定有价值。

基础架构即代码是运营部门在向企业交付计算和存储资源的能力方面的一项重大变化。这将使他们能够更深入地了解硬件，进行预测性维护，根据需求将应用程序迁移到各种资源，并调整整体环境以满足特定时刻的业务需求。简而言之，它将使 it 部门能够交付具有高度可用性和安全性的计算服务。它还将暴露现有应用程序中的缺点，这些应用程序对其运行的底层环境做出了假设。因此，如果运营和应用工程没有协同工作，并且包括基础设施控制应用在内的整个应用环境没有作为一个单元进行测试和部署，那么失败的可能性将会很高。