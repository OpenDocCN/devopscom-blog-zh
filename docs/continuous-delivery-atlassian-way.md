# 持续交付:亚特兰蒂斯之道

> 原文：<https://devops.com/continuous-delivery-atlassian-way/>

*Sonatype 的* [*马克米勒*](https://www.linkedin.com/in/seniorstoryteller)*(@ TSWAlliance)赶上了* [*伊恩布坎南*](https://www.linkedin.com/in/ianbuchanan?authType=NAME_SEARCH&authToken=0HvZ&locale=en_US&trk=tyah&trkInfo=clickedVertical%3Amynetwork%2CentityType%3AentityHistoryName%2CclickedEntityId%3Amynetwork_1196681%2Cidx%3A1) *(@devpartisan)为我们的 2016 DevOps 领导力系列。Ian 讨论了他在*[*Atlassian*](https://www.atlassian.com/)*的经历，包括持续交付、ChatOps、使用 Bamboo、Nexus、Puppet、Datadog 等工具。*

[https://www.youtube.com/embed/MgRaYKHGqeQ?feature=oembed](https://www.youtube.com/embed/MgRaYKHGqeQ?feature=oembed)

布坎南:我是伊恩·布坎南。我是 Atlassian 的一名开发者党员，Atlassian 是我们开发工具的开发者代言人。

**Miller:** Ian，大多数人都是从 JIRA 和 Bitbucket 这样的解决方案中知道 Atlassian 的。

布坎南:是的，我主要关注 Bitbucket 和竹子。Bamboo 是我们的持续集成和部署工具。

**米勒:**好。昨晚吃饭时我们稍微谈到的一个话题是 Atlassian 如何使用 Nexus。你能给我们一些这方面的背景吗？

布坎南:对，没错。我们是一家大型 Java 商店。我们已经有很长一段时间了，由于外部原因，我们有很多对 Maven 的依赖；我们还在 Nexus 存储库中存储了许多我们自己内部开发的库。

_________________

我们是一家大型 Java 商店。我们已经有很长一段时间了…我们在我们的 Nexus 库中存储了许多我们自己内部开发的库。

_________________

Miller: 就二进制库而言，除了组件之外，你还在用它做什么吗？

据我所知没有。我知道我们最近开始涉足 Docker，Nexus 也非常适合。我还不知道我们在多大程度上使用了 Nexus，因为 Docker 对我们来说还很新。

**Miller:** 你的持续集成管道是什么样子的？

布坎南:当然在细节上因产品而异。当然，我们有自己的持续集成产品，竹子。竹子是我们拥有的最普遍的工具。

对于 Java 来说，这是一个非常简单的管道，其中库被构建并发布到 Nexus 中，以便可以在下游使用。我们也有一些有趣的、更新的云产品，它们是用 Python 构建的。许多部署，不管是 Java 还是 Python，都是由 Bamboo 的部署项目处理的。他们从 Nexus 中提取工件并投入生产。

_________________

许多部署，无论是 Java 还是 Python，都是由 Bamboo 的部署项目处理的。他们从 Nexus 中提取工件并投入生产。

_________________

**Miller:** 你们在工作流程中使用连续内部交付吗？

布坎南:我们处在一个有趣的位置，我想我看到很多公司都处在这个位置。我们有一些防火墙后产品(我们的服务器产品)，还有云产品。在云端，当我们想走得很快时，使用连续交付。但是，我们还必须平衡我们对服务器产品采取的方法，以便它们不会出现严重的分叉。我们有连续交货，直到有一个产品交付。在这一点上，有另一种选择——云产品与其他东西如[木偶](https://puppet.com/)和 [Ansible](https://www.ansible.com/) 结合，用其他人可以选择和运行的产品来配置环境。

米勒:我和你在旧金山的团队聊过。你们是如何通过 HipChat 使用 [ChatOps](https://www.pagerduty.com/blog/what-is-chatops/) 的？

布坎南:我已经谈论 ChatOps 很长时间了。我们用 ChatOps 做了很多非常有趣的事情。他们在我们的持续交付管道中扮演着非常重要的角色，因为我们在那里发布构建结果。人们可以看到拉取请求何时准备好，并检查这些请求。我们还可以看到生产过程中发生了什么。我们已经集成了[Datadog](https://www.datadoghq.com/)；它告诉我们一些正在进行的监控。不仅仅是信息进入聊天室。人们还可以发出一些命令来使连续交付管道向前移动。在某些阶段，您可以向我们的 ChatOps 键入命令，它们将执行必要的操作。许多部署和变更管理都发生在 ChatOps 上下文中。

_________________

在某些阶段，您可以向我们的 ChatOps 输入命令，它们会执行必要的操作。许多部署和变更管理都发生在 ChatOps 上下文中。

_________________

**米勒:**你们正在研究的未来会有什么有趣的事情吗？

**布坎南:**嗯，很多创新确实发生在我们的季度“Ship It”活动上。这是我们的开发人员花 24 小时做他们感兴趣的任何创新的地方。很多时间都花在搔他们的痒处。我在那里看到的一些事情是关于有更多的信息返回上游，不仅仅是进入聊天室，而是进入 [JIRA](https://www.atlassian.com/software/jira) ，在那里更多的长期跟踪正在进行。他们正在尝试将更多的信息放入 JIRA。

米勒:不错。最后一个问题，如果你要成为超级英雄，你会选择 Dev、Sec 还是 Ops？

**Buchanan:** 我扮演过开发人员和运营人员的角色，我几乎觉得自己对这些角色了解得更多。但是从 DevNexus 的许多会议中，我不得不觉得 Sec 是超级英雄。他们是超级英雄，因为他们用很多方法解决了一些无法解决的问题。但是我自己现在还没准备好扮演这个角色。

米勒:很有意思。我同意你的看法，他们是无名英雄。大多数时候，他们只是因为自己的所作所为而受到打击。

布坎南:确实如此。昨天我参加了一个关于保护 REST 端点的会议。演讲者讲述了基本关闭、消化关闭和 J2EE 的问题，所有这些都是我们在产品中使用的。最后我们只剩下“答案是什么？”

答案是，对于每一种，都有不同的问题。所以我们必须确定正确的背景。我们必须了解一些东西在哪里坏了，知道这些东西并不完美，并针对这种不完美进行设计。这是我们必须在开发、运营和安全部门贯彻的心态。我希望更多的安全人员站出来，开始讲述这些故事。