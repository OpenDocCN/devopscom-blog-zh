# 其他行动的开发工作

> 原文：<https://devops.com/devops-for-the-rest-of-ops/>

IT 专业演出通常包括基本的逆风。他们是成本中心的一部分，资源和人员的预算受到设计的限制，除非他们正在管理一个战略计划，至少在一段时间内，这是一个更慷慨的资助。

开发运维、敏捷或站点可靠性工程(SRE)团队的早期采用者是转型项目的预算受益者——高可见性 IT 计划的情况一直如此。 幸运的是，DevOps 已被证明比其他一些“下一件大事”更有帮助和粘性，对于一些组织来说，它是增长甚至实际数字化转型成功背后的引擎。

IT 专业人士——一如既往地注重实效——已经注意到开发运维的潜力，即使是在保持正常运转、系统正常运行和可靠地提供企业几十年来一直依赖的关键服务的同时。IT 领导者面临的问题是，IT 团队如何在传统 IT 组织内部运营的同时实现开发运维的一些优势？

随着 DevOps 最终从宣传的巅峰滑落到有用工具的棚子里，经验总结出了几个结论。首先，DevOps 的原则——打破壁垒、共享反馈循环和学会热爱自动化——不仅仅适用于新的或酷的应用程序。它们在传统 IT 中甚至更有帮助。例如，自动化的兴起不是由用机器人取代管理员的阴谋推动的，而是减少手动争论所有云和云本地技术的新复杂性的辛劳的必要性。

其次，开发运维背后的许多想法以及由此产生的实践都是为了直接解决困扰 IT 团队多年的 IT 问题。询问任何 IT 专业人员是否愿意将所有部署时间从周一到周四上午 9 点到下午 4 点，而不是周六晚上的午夜。那个队会为 CI/CD 疯狂的。更好的是，事实证明您不必做 DevOps 的所有事情就能获得它的许多优势。

但是，即使您的业务仍然从最高管理层开始运作，带来季度预算支出、[](https://www.techopedia.com/definition/14025/waterfall-model)瀑布模型和许多封闭的筒仓，也有机会调整开发运维流程和文化，以在真正的变革性计划上取得进展，从而帮助业务增长。诀窍是找出哪些 DevOps 实践是有价值的，哪些对开发人员更有用。

幸运的是，专注于四个方面可以让你的团队获得最大的好处而不会(太)中断，开发团队渴望分享其不断增长的新技术和成功。我们正处于 IT 历史上一个有趣的时代，这是一个面向所有人的开发运维的潜在民主化时代。

## **连续交货**

直到最近，一些 IT 专业人士仍持怀疑态度，甚至怀疑开发团队的目标是将他们从职业生涯中自动化出来。其他人认为开发人员要求每个人学习如何进行全栈编程，并发明一种方法来快速移动和破坏东西，就像他们可以(更安全地)做的那样。当一些管理员表现出兴趣时，他们甚至与一些 DevOps 支持者有过不愉快的遭遇。没有人喜欢条件反射式的回答，比如“你用 Oracle 和 DB2？切换到 MongoDB，稍后再回来”来回答 101 个急切的问题，即使它们只是来自少数社区成员。这对于开发人员和 It 专业人员来说尤其不愉快，因为这不是运营的方式。我们分享，我们开放，我们乐于助人。我们来到 tech 是为了帮助最终用户从技术中获得更多。

相反，成功的团队通常从确定支持基本运营目标的工具开始，不受任何特定技术或供应商的干扰，并寻求开发人员和运营人员的支持。因为如果你在运营部门，你就是那个必须:

1.  找到让软件进入可靠生产的方法。
2.  维持功能性的、有用的治理。
3.  将应用程序维护数年，比任何人认为它们可能上线的时间都长。

运营知道这一点，因为它一直是交付和部署的最后一英里，它关心可用性和 SLA，并定义早餐流程。

与 DevOps 相关的首批工具之一是 CI/CD 管道，它实际上是关于代码如何从起源到生产的自动化策略的实现。但是，许多 DevOps 博客忽略了 CD 的最后一步，因为它不适合心脏虚弱的人。这很不幸——运营部门擅长计算最后一英里。

当运营团队采用 CI/CD/连续部署时，他们在自动化方面的投资会以最好的方式得到回报:减少夜间和周末的工作。因此，他们建立的管道不是短暂的实验，而是生产级 CI/CD，因为它是生产本身的一部分。随着变更速度的提高和错误率的降低，许多团队拒绝回到手动部署，除非他们已经用尽了所有其他选择。管道不会取代 IT 专业人员，它们可以改善工作与生活的平衡。

当运营团队向开发人员展示标准化的、经过实战检验的喷嘴时，他们的反应通常是兴奋，通过这些喷嘴可以更快地部署变更，同时减少错误。它允许开发人员将他们的构建、单元测试、打包和交付前端与通常复杂的交付/部署操作管道相匹配。 最重要的是，运营团队倾向于将监控、安全甚至成本管理纳入他们的流程，从而自动、可靠地实施有效的控制。此外，ops 指标创建并丰富了开发人员需要的反馈循环，以便根据(而非开发或测试数据)随时改进代码。在这样的环境中，基于共同的目标、成功和让每个团队做他们最喜欢的事情的灵活性，文化变革更加有机。

## **开始快速打碎东西**

在打破常规方面，运营团队可能会有点嫉妒。他们是技术专家，就像开发人员一样，而且像大多数被技术吸引的人一样，他们喜欢通过分解、重组或破解技术来学习它如何工作的复杂细节。但与开发人员测试代码、实验性配置或其他常规笔记本电脑环境不同，操作人员绝对不能进行实验。根据戒律，它是规避风险的，理由很充分。

“弄个实验室！”听起来像是一个显而易见的建议，事实也确实如此——但这是一个说起来容易做起来难的好例子。因为它是一个成本中心，实验室经常被视为重复和浪费，因为它们的价值很难在预算中得到证明。但是对你已经拥有的监控数据进行一点非常规的使用，那就不一定了。在不断寻求提高可靠性的过程中，运营部门定期将变更事件与性能直方图相关联。首先考虑在实验室环境中测试的变更中添加前后指标。您可能会发现，部署前测试越真实，系统的错误率就越低，性能就越高。

但是，提高质量背后的机制不是实验室本身或它产生的数据。这是团队的实验——以及一些流血、流汗和流泪——在生产环境中是不可能的。它还允许运营部门邀请开发人员继续进行部署和调试。开发人员可以使用他们喜欢的任何工具，根据需要进行更改、探测或拆卸实验室堆栈。从沟通和文化的角度来看，这是有帮助的。

运营实验室环境还允许 IT 专业人员自己区分宣传和现实。他们可以安装最新的全新评估工具，尝试新的方法，甚至测试重要的平台架构重新设计。简而言之，他们可以在不影响生产的情况下破坏任何他们想要的东西，并向开发人员提供反馈和一个让开发人员试验变化的地方。在这方面，运营可以再次发挥主导作用，为沟通、合作和文化变革提供新的途径。

## **监控你的成功**

大多数开发人员不是数据驱动的，他们是功能驱动的。他们热爱数据信息设计，擅长使用工具将数据转化为有用的东西，但归根结底，他们的工作是构建有用的代码。IT 专业人员在 DNA 中有 监控 ，因为随着时间的推移收集的详细性能数据是他们最初验证预感的方式，但也打破了结论偏差。但是，尽管每个人似乎都理解指标和数据的价值，但它通常不被视为 DevOps 沟通的工具。

如前所述，反馈回路是 DevOps 的基本原则。变更进入生产环境，生产环境生成数据并发送给开发人员，以指导未来的变更，从而进一步提高服务质量。这是一个良性循环，两个团队都高度重视。诀窍是在开发人员和运营人员之间创建一种语言，来表达要收集什么、如何使用以及如何管理长期反馈。第一步是扫除双方的先入之见，重新开始。

一种常见的方法是召集一个小型团队，从空白白板开始。我们的目标是将已经可用的东西和有用的东西汇总起来，然后找出两个团队之间的差距。开发团队渴望运营能够提供的令人难以置信的丰富覆盖，而运营则渴望挖掘开发团队用于故障排除和内部应用性能监控(APM)的新工具。

面向混合应用的 APM 是两个团队学习如何创建混合本地/云原生服务整体可见性的绝佳范例。高绩效的运营团队确保他们添加开发团队需要的指标，开发人员发现调试讨厌的应用程序的“不可能”信息已经收集了多年，并且是一个 API 调用。再一次，一个小小的谈话可以导致放松，并赢得心灵和思想的改变。

## 用远大的梦想奖励成功

开发人员和 IT 专业人员的最终共同体验永远不会真正完成。代码总是可以改进的，服务交付总是可以变得更好。但因为我们是人，有时我们会累，停滞不前或无聊，很容易休息一下，尤其是在大获全胜之后。那是自然的。有数年的延期工作和技术债务，没有时间追求完美主义，尤其是在企业 IT 领域。开发运维的这一关键方面需要成为任何采用开发运维技术的团队的焦点——记住开发运维永远不会结束。这是一种持续协作改进和发展的文化。这种共识维系着开发人员和运营人员之间的纽带。

当团队创新时，当他们继续打造更紧密的关系时，当他们随着团队文化的改变而分享改进时，他们开始提出更大的问题。我们习惯于接受某些事情不能实现是因为，原因。因此，有时可能最终解决团队最棘手的挑战的建议和问题可能并不总是被提出或询问。

跟踪你那些推动进步的“不可能”的想法，然后推广那些成功的想法，同时分享它们为什么有效的细节。这反过来有助于将开放带来的成功价值社会化，并鼓励可能已经在板凳上坐了很长时间的伟大想法。

同样，您正在投资更多的指标和信号，但不仅限于绩效数据。当你胸怀大志时，尤其是当你将数字化转型的巨大期望转化为运营变革时，你将开始依赖新的指标。例如，与公司目标相关联的业务指标、准确反映 CSAT 的行为信号、帮助团队决定何时添加新内容、何时修复的变更和错误率数据，以及确保领导层运营一切尽在掌控的新方法。当管理人员确信 IT 专业人员可以在不中断业务的情况下安全地转变设备、服务和员工时，最受欢迎的 DevOps 目标就可以成为焦点:快速创新的新自由。

帕特里克·哈伯德