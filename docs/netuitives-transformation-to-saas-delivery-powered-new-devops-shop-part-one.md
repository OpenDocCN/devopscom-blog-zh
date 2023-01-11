# Netuitive 向 SaaS 交付的转变，由 DevOps 提供支持，第 1 部分

> 原文：<https://devops.com/netuitives-transformation-to-saas-delivery-powered-new-devops-shop-part-one/>

Netuitive 工程副总裁 Brian Spindler 表示:“Netuitive 为云基础设施、应用和服务提供自适应监控解决方案，由获得专利的自学式关联引擎提供支持。该引擎使用多元回归分析，根据收集的时间序列数据计算指标之间的相关系数，利用数据中指标变量之间特定关系的重要性。

Netuitive 技术建立了衡量标准及其历史关系的基线。Netuitive 策略使开发和运营团队能够发现显著高于历史基线且与 AWS EC2、Linux OS、MySQL 和其他系统和技术相关的异常。

“我们已经推出了我们产品的 SaaS 版本，现在我们每周都向产品交付代码，”Spindler 说。部署速度的提高得益于该公司新的 DevOps 流程。以下是 Netuitive 两部分故事的第一部分。

在搬到 DevOps 商店之前

在转向包括持续交付在内的 DevOps 软件开发方法之前，Netuitive 使用 Scrum 框架以及 Jenkins 和 Ant 产品和公司内部开发的脚本来开发 Netuitive 软件和其中获得专利的自学关联引擎。“我们很早就认识到了自动化的价值——使用简单的 shell 脚本和我们自己的 Web API，我们能够编排相当多的内容，”Spindler 说。

尽管如此，这些方法仍然存在挑战。广泛的计划过程，包括召唤出 Scrum 为 Sprints 所需要的开发时间估计，是具有挑战性的。除此之外，尽管进行了所有的计划，围绕着软件复杂性和集成管理产生的测试和部署问题发生了许多中断。“这些中断降低了我们的速度，影响了我们的燃烧率，”Spindler 说。(烧钱率计算的是企业支出超过收入的速度。)

大量的错误修复也是一个问题。由于花费了过多的时间来修复只会在罕见的边缘情况下出现的错误，Netuitive 在构建方面投入了太多的精力，而在改进或新功能方面投入太少。“当我们寻求反馈回路问题的解决方案时，很明显这需要更敏捷的方法。Spindler 说:“我们从 DevOps 中寻找灵感，引导我们从 Scrum 迁移到看板。看板是一个说明性的过程，用于管理目标生产目标，包括开发什么，何时开发以及开发到什么程度。

正如采用 DevOps 的企业经常提到的，迁移到 DevOps 方法所需的文化变革是最具挑战性的。特别是，让每个人都参与自动测试来证明软件的有效性是非常棘手的。QA 和开发人员等内部团队必须转变他们现有的关系。“多年来，这些团体是对手；现在我请求他们成为盟友。这要求开发人员承担编写测试的责任，同时 QA 验证并确保测试足够广泛，”Spindler 说。

目标、结果和危险:通向疯狂的方法？

Netuitive 对转向更完整的 DevOps 商店有具体的想法。质量和生产率的提高是重中之重。事实上，这两者必须相互包容，紧密结合，以确保两者。为了实现这一点，Netuitive 每周进行一次部署，使用完整的 Atlassian 套件进行协作和问题跟踪，并结合使用 Bamboo、Gradle 和 Salt 堆栈来自动化配置、管理基础架构和管理部署操作。这种编排有助于质量和生产力和谐共舞。

结果不仅仅是美观。“我们正在通过持续的流程改进来提高部署速度，”Spindler 说。通过解构 Netuitive 产品并将其划分为独立的服务模块和组件，公司可以通过分别和同时改进每个单独的组件来更快地推进整体进展，从而比等待最终完成单个完整的产品更新更快地逐步取得进展。

Netuitive 在转变为 DevOps 商店的过程中经历了三次完全不同的颠簸或“危险”。“自动化测试、改变组织工作流程以适应自动化，以及将产品分解为足够精细的服务以便我们可以独立部署，这些都是相关的问题，”Spindler 说。这些都与产品生产整体自动化的愿望有关。Netuitive 不断努力，在跨这些粒度服务的附加测试分层和删除一些测试层以提高部署速度之间寻求必要的平衡。

下次当 DevOps.com 再现相对按时间顺序排列的网络开发过程时，请收听，从一个版本到另一个版本，以及公司没有预料到的差异、好处和回报。