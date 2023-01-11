# DevOps:是时候让开发人员参与进来了

> 原文：<https://devops.com/devops-time-developers-dig/>

在 Gartner Catalyst 展会上，Jenkins World 和 Atlassian Summit 与开发人员和项目经理交谈，揭示了大多数 it 专家如何看待 DevOps 的一些见解。是的，我有一个繁忙的夏末日程安排，参加各种活动，与各种各样的开发人员和项目经理谈论 DevOps。

![](img/89cab236fb985dbbadf7805326383543.png)

two dogs digging together in one hole in the ground

我了解到的是，大多数人还没有搞清楚 DevOps 是什么意思。大多数人告诉我，他们正在做开发工作，解释他们有 CI/CD 渠道。当进一步询问他们如何看待 DevOps 时，他们认为 DevOps 是关于创建一个 CI 工作流，开发人员和有时测试团队可以执行该工作流来自动化构建、部署和测试。这些对话中最具讽刺意味的是项目经理声称他们的 CI 服务器执行构建和部署。

各位，DevOps 不是关于 CI/CD 管道的。与流行的观念相反，您的 CI 服务器不执行构建和部署，就像它不执行自动化测试一样。您的 CI/CD 管道编排构建和部署过程的方式与它执行外部测试自动化工具的方式相同。丑陋的事实是，您的 CI/CD 管道正在执行一次性的构建和部署脚本，与您的瀑布实践中使用的脚本相同，但只是由您的 CI/CD 流程触发。这些脚本不容易适应连续交付管道。测试和生产环境的配置不同。构建和部署脚本必须以瀑布实践中相同的方式进行调整、维护和调试。一旦准备就绪，您的 CI/CD 工作流就会调用它们。DevOps 不一样。

DevOps 要求您的开发人员和运营团队从项目的最早阶段就开始共享和协作。本质上，这需要将更多的操作职责转移到开发人员的肩上。这正是责任和控制应该在的地方。运营团队需要知识和透明度，以便他们能够尽早地、经常地向开发人员传达基础设施需求。最终，我们将会看到运营资源数量的减少。一位管理生产部署的“发布工程师”说，“如果我们正确地定义了我们的 DevOps 过程，我的工作在未来将不复存在。相反，自动化将取代手动操作脚本，允许开发团队完成我 70%的工作。”我的朋友，这才是真正的 DevOps。

## 开发者们，开始吧

所以是时候让开发人员真正深入到 DevOps 中了。我的意思是，开发人员必须开始摆脱通过一次性脚本实现大部分流程自动化的做法，并开始整合工具来执行开发运维任务，包括持续部署、安全扫描和性能监控。不同的平台需要不同的工具。项目团队将需要权力来选择适合他们的工具。企业购买单一工具的“传统”时代已经一去不复返了。高成本的操作工具是高风险的，并且当开发者选择使用不同的解决方案时会招致技术债务。DevOps 意味着给予开发团队更多的控制和购买自动化工具的权力，这些工具可以在项目级别而不是企业级别进行管理。这些工具必须支持一个过程，在这个过程中，开发人员处理声明，然后进行测试和生产，以良好的透明度使用这个过程。脚本无法实现这一点，即使由 CI 触发。

我们的未来变得越来越复杂。我采访过的大多数公司仍然管理着超过 70%的单一应用程序。墙上的字在 30%里。有了微服务和容器，运营任务将变得更复杂，而不是更简单。开发人员越早成为运营任务的核心所有者，就越容易采用微服务架构。管理微服务不是运营团队的工作。这将需要由熟悉其应用程序的开发人员来完成。

从 CI/CD 到 DevOps 的成熟需要仔细观察 CI/CD 引擎下的引擎。当开发人员和项目经理开始真正深入了解并看到引擎如何运行时，很明显实现 DevOps 是一件遥远的事情。在这个过程中有紧迫性。更精简、更好的编写和发布代码的方式正在向我们走来。我们中的大多数人只是没有准备好抛弃瀑布实践中的一些旧习惯。

一些离别的思绪:

*   承认 CI/CD 是一个好地方，但它不是 DevOps。
*   仔细查看 CI/CD 调用的底层流程。它们对您的生产环境的支持程度如何？
*   您在开发部门的 CI/CD 工作流能否支持生产部署？如果不花时间去了解原因。
*   您的开发人员是否工作到很晚才把代码更新投入生产？
*   你是否有一个清晰的连续反馈循环来显示代码更新在哪里运行，以及在什么端点上运行？
*   您的开发人员知道当今生产中正在进行哪些基础设施更新吗？
*   您的开发人员如何向生产团队传达基础设施的更新？他们能独自完成吗？

现在是时候对您的核心运营任务的自动化程度进行自我检查和明确诚实的评估了。如果它们是基于一次性脚本构建的，您应该假设您有一些工作要做，以真正开始转移到开发人员可以声明、所有运行时环境可以使用并且对所有人透明的 DevOps 实践。

还有记住，微服务在追你。

## 关于作者/特雷西·拉冈

![](img/a0602b930b3c5fba2f8646773c154a2a.png)特雷西·拉冈是首席运营官和 [DeployHub](https://www.deployhub.com/continuous-delivery-vs-continuous-deployment/) 的联合创始人。她在商业应用程序的开发和实施方面拥有丰富的经验。正是在她的咨询经历中，拉冈女士认识到分布式平台缺乏构建和发布管理过程，而这种过程长期以来被认为是大型机和 UNIX 的标准。在创建 [OpenMake 软件](http://www.openmakesoftware.com/)的四年中，她与开发团队一起实施了以团队为中心的标准化构建到发布流程。在 [LinkedIn](https://www.linkedin.com/in/tracy-ragan-oms) 上和她联系。