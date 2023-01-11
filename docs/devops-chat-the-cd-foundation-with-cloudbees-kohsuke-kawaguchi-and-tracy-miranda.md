# devo PS Chat:CD 基金会，CloudBees 的 Kohsuke Kawaguchi 和 Tracy Miranda

> 原文：<https://devops.com/devops-chat-the-cd-foundation-with-cloudbees-kohsuke-kawaguchi-and-tracy-miranda/>

一个新的基金会，CD 基金会，已经在 Linux 基金会的支持下成立，作为一个厂商中立运动的大本营，致力于使跨多个持续集成/持续交付(CI/CD)平台构建和重用 DevOps 管道更加容易。

CD 基金会赞助的第一批项目包括 Jenkins(开源 CI/CD 系统)和 Jenkins X(Kubernetes 上的开源 CI/CD 解决方案)。两者都是由 CloudBees 开发的。与此同时，网飞和谷歌正在贡献 Spinnaker，一个开源的多云 CD 解决方案。Google 还增加了 Tekton，这是一个用于创建 CI/CD 组件的开源项目和规范。

CD 基金会的创始成员包括 Alauda、Alibaba、Anchore、Armory、Autodesk、Capital One、CircleCI、CloudBees、DeployHub、GitLab、Google、华为、JFrog、网飞、Puppet、Red Hat、SAP 和 Snyk。

在这次 DevOps 聊天中，我们采访了 Jenkins 的创始人兼 Cloudbees 的首席技术官 Kohsuke Kawaguchi(又名 KK)和 CloudBees 的开源社区总监 Tracy Miranda。他们让我们了解了 CD 基金会背后的情况，以及詹金斯、詹金斯和 CloudBees 的未来。

像往常一样，下面是流媒体音频，然后是我们的谈话记录。尽情享受吧！

[https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/tracks/589597599&color=%23ff5500&auto_play=false&hide_related=false&show_comments=true&show_user=true&show_reposts=false&show_teaser=true](https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/tracks/589597599&color=%23ff5500&auto_play=false&hide_related=false&show_comments=true&show_user=true&show_reposts=false&show_teaser=true)

## 成绩单

**艾伦·希梅尔:**大家好。我是 DevOps.com 的艾伦·希梅尔。您正在收听另一个 DevOps 聊天。今天的 DevOps 聊天是关于 DevOps 持续集成/持续部署世界 CI/CD 中的一些重大新闻。这就是 CD 基金会的成立，它是 Linux 基金会的一部分。今天下午刚刚宣布的。我很高兴有来自创始成员之一——实际上是裁谈会基金会的关键创始成员之一 CloudBees 的几个人参加。来自 CloudBees，加入我们今天加入我们的是 Tracy Miranda，她是 CloudBees 开源社区的主任，不是别人，正是 KK 本人，他是 Jenkins 项目和社区的创始人，也是 Cloudbees 的创始人兼首席技术官。Kohsuke，Tracy，欢迎来到 DevOps 聊天。

小佑川口 : 感谢您再次邀请我们。

Kohsuke，和你在一起是我的荣幸。特蕾西，我知道你是新手，但谢谢你加入我们。

**特蕾西·米兰达:**是的，*【听不清】*。

伙计们，今天有大新闻。Linux 基金会启动 CD 基金会。CloudBees 是创始公司之一，如果我没弄错的话，也是 CD 基金会的董事会成员。对吗？

**川口 :** 对，没错。我们是——我想是 20 个中的一部分。

米兰达:是的，我想我们现在有 23 名成员了。

希梅尔:我想可能是 25 岁。

米兰达:哇*【咯咯】*我认为它在持续增长。

**Shimel:** 很搞笑。在声明发布后，我今天和几家公司谈了谈。他们提到他们想参加。那是给他们的。我想了解，也许，KK，这是一个问题给你。将 Jenkins 和 Jenkins X——我们正在谈论的两个重要项目——移交给这个新基金会和 Linux 基金会的动机是什么？

**川口 :** 来自詹金斯——我身兼数职，但从詹金斯项目的角度来看，它的一个关键部分是我们希望创造一个公平的竞争环境，从而加速詹金斯家族的创新。如你所知，詹金斯家族让每个组织中的每个人都受益匪浅，有很多公司都在关注詹金斯。我们想让他们更多地参与这个项目。我们一起推进这个项目。那样的话，我想我们可以做得更快。以 Jenkins X 为例，它在 CNCF 的许多项目中得到了严格的设计，该基金会是 Linux 基金会的姐妹基金会。我们将这些项目拉近，这样我们可以更快地再次合作，这是很有意义的。所以我认为，这是两个项目非常令人信服的明显优势。

作为 CloudBees 的首席技术官，CloudBees 一直是 Jenkins 项目背后的最大贡献者。这一举措对我们来说也很有意义，因为首先，我们的客户依赖于许多开源项目和生态系统。当这些基础资源项目的驱动力很强时，显然会使 CloudBees 和我们的客户受益。我认为这对我们来说也是相当明显的举措。同样重要的是，我与我们的客户和潜在客户组织中的许多人交谈过，这些技术人员了解客观性真正带来的需求和好处。我经常看到他们在挣扎，而组织中的其他人在他们周围。在这里，我谈的是投入这些努力的资金、人员和时间。它会产生必要的业务影响。

我觉得我真正期待 CDF 发挥的作用的一部分是倡导持续的实践，将其提升到技术实践之外。同样，就像云原生的 CNCF 一样，我们可以在世界上产生更大的影响。这是单个供应商无法轻易做到的事情，因为人们会自动假设这些事情背后的意图或背后的推销。开源基金会，有多家供应商，还有像 _____ 和 _____ 这样的终端用户公司，为这一信息增加了很多可信度和真实性。出于所有这些原因，我认为这是一个显而易见的双赢局面。我就是这么想的。

Shimel: 我认为这是一个很好的看待问题的方式。Tracy，让我问你，你是开源社区的联络员。在这种情况下，我们实际上是在谈论 Jenkins 社区和 Jenkins X。这次发布怎么样——这还是一个新消息，但是社区对此有什么反馈呢？

米兰达:是的，非常非常积极。我们一直在与詹金斯社区，嗯，詹金斯董事会成员，泰勒和 Kohsuke，一年多前的启动对话。自从我也加入进来后，我们一直渴望让每个人都参与进来，看看会如何发展。我们听到了许多令人兴奋的事情。一些我们一开始都没有预料到的事情。举个例子，詹金斯有一个非常新兴、非常强大和热情的中国社区。他们对使用 CDF 作为在中国真正扩张的方式感到非常兴奋。我认为我们可以借此寻找我们想拓展的新领域。所以，是的，总的来说，非常积极。热情高涨，这太棒了。

绝对的。事实上，我对中国的詹金斯社区有些熟悉。去年我在那里的时候，我们的一个合作伙伴举办了北京詹金斯日。所以我有机会第一时间见到很多这样的人。这是一个非常热情的团体。他们在 DevOps 和 CD 上也做得很好。我肯定它和 Jenkins X 一样被使用过。实际上，Jenkins X 项目的创始人之一那天也在那里演示。他从澳大利亚回来。它非常非常受欢迎。回到这个话题，对于特雷西和 KK 来说，我认为人们真正钦佩 CloudBees 的一点是它不是通常的供应商开源项目经理关系。

许多由单一供应商管理的开源项目都倾向于只为该供应商的利益而运行，无论是 OpenCore 还是 Razor-Razorblades 之类的。决策的制定是为了商业供应商的利益，通常是以社区为代价的。CloudBees 总是在那之上。这些年来一直有一个独立的董事会。开源社区和项目有独立的指导和治理。KK，既然已经有了，这是否否定了你需要一个独立基金会的一些理由，或者只是加速了它？

**川口 :** 嗯，谢谢你的美言。我们已经为我们参与詹金斯项目的方式感到自豪。我认为这有两个因素。一是创建 CloudBees 的人数。他们都来自开源背景，即 _____ 人、RedHat 人。我们分享很多——就像一个共同的身体。这对于认识和理解开源社区是如何运作的起到了至关重要的作用。需要指出的另一个重要部分是，Jenkins 项目不属于 CloudBees。这是一个独立的项目，有自己的决策过程。这个项目，请注意，它是和——嗯，某个公司合作的电视剧。我不会指名道姓。

**米兰达:** *【笑声】*

**川口 :** 所以我认为社区里的人们对他们的独立性有着强烈的感受。所以我们讨论了一下。因此，在迁移到 CDF 的过程中，许多人脱离了 CloudBees，他们也继续他们的 _____ CloudBees。他们也非常渴望和偏好 CDF，因为他们认为这是治理的下一步，以确保公平的竞争环境，这一点我早些时候提到过。我认为这是——这被视为非常有价值的特征。我认为 CloudBees 在过去的一年里为这个项目做了很多好事。我认为是时候把它整理成更加稳定和基本的东西了。我认为这就是向 CDF 转移的意义。

Shimel: 我认为那是真的。我认为还有另一个因素，KK。当我们回顾詹金斯的历史时，当某件事如此成功时，你不会看到很多竞争者。詹金斯就是如此。当 Jenkins 突然出现时——我们不需要进入它的历史，但是 Jenkins 突然出现，它很快成为首选的 CI 和 CD 工具，不仅对于 DevOps 社区，而且对于软件开发和 Ops 社区。所有人都用詹金斯。最近，在过去的一两年或三年里，我们看到了其他竞争者的出现，其中许多是商业竞争者。

他们中的一些人有一个开源的，开放核心的，类似程序的商业计划，但是尽管如此，人们有这样的想法，“嗯，詹金斯老了，或者是昨天。这是明天。”我认为把它放在这样的基础上，它保证了明天。这是一个古老的故事，“这么多人关注代码，它一定会变得更好”。底池中有这么多手牌，它会加速前进。所以这是件好事。但是我觉得我们忽略了。我们应该提到除了 Jenkins 和 Jenkins X 之外，还有其他一些伟大的软件程序被捐赠给了今天的 CD 基金会，对吗？

米兰达:是的，没错。你想听更多关于这些的信息吗？

希梅尔:好的，请吧。

米兰达:我们非常兴奋。另一个项目是 Spinnaker，这是网飞最初为持续交付而组装的。在这个领域，这是一个众所周知、广受欢迎的项目。我们真的很兴奋，他们接受了这个愿景，并希望成为其中的一部分。然后是另一个项目，去年谷歌宣布了 Knative 无服务器平台。作为该项目的一部分，它有一个构建和管道部分，已被重命名为 Tekton。Tekton 是 Knative 背后的管道和制造部分。这个项目真正令人兴奋的是，我们正在寻找作为 CDF 愿景的一部分，真正专注于集成和共享概念，并使工具协同工作。Tekton 将成为管道引擎，为 Jenkins X 的发展设定定义。Spinnaker 也将关注它，对于 Jenkins 的下一代管道，工作中有许多令人兴奋的事情。只是对即将到来的所有可能性感到兴奋。

Shimel: 当然可以。我们应该提到 Spinnaker 和 Tekton 都是由 Google 贡献的。

**米兰达:**谷歌和网飞

席梅尔:网飞:是的，是大三角帆。但这还不是全部。一旦技术监督委员会被引入，可能会有其他的项目也在 CDF 的管理之下，对吗？

米兰达:是的。绝对的。我认为我们在章程中概述的事情之一是我们想要关注整个软件交付生命周期。我们希望有一整套的配套项目。所以我们正在寻找——在移动和其他领域也有一些真正令人兴奋的项目。不仅仅是云。所以有很多很多令人兴奋的项目。随着我们的发展，以及我们的正常运作，我们期待着欢迎和接纳他们。

**Shimel:** 我们还应该——我只想提一下，作为该 CDF 创始成员参与的其他一些公司有:Alibaba、Autodesk、Capital One、CircleCI、CloudBees、显然、DeployHub、GET Lab、Google、华为、JFrog、网飞、Puppet、Red Hat、SAP。这些都是家喻户晓的名字。这真的是一个重量级的贡献者名单，我想伙计们，这真的说明了 CI/CD 在现代软件工厂中变得多么重要。

**川口 :** 就像我说的，它正处于从单纯的技术发展到更大的商业影响的尖端。CloudBees 一直在努力，所以我真的很兴奋，这个使命，这种激情被这么多公司分享。我认为这让信息变得更加重要。

这是另一面。因为这让 CloudBees 可以真正专注于商业方面。虽然你没有——cloud bees 没有管理詹金斯。社区和詹金斯社区管理自己。CloudBees 发挥了——很明显，这是一个重要的作用，帮助——确保——KK，你身兼两职。现在 CloudBees 已经摆脱了这一点，你认为我们会从 CloudBees 的发展中看到什么？

**川口 :** 实际上，我们在开源方面比以往做得更多。Nginx 背后的许多关键人物都在 CloudBees _____。所以，为了确保这不完全是 _____ 的一个举动，试图让我们洗手不干。其实恰恰相反。也是最后一次，CloudBees 变得越来越大。我们正在开发一些产品和服务。所以我并不认为这些事情是相互排斥的。我认为 CloudBees 的每个人都明白这两者都是我们业务的重要组成部分。

**Miranda:** 是的，如果我再加上一个具体的例子，DevOptics 项目，它非常关注分析，以及您正在进行的软件交付的这些关键措施。这是 CloudBees 将要做得更多的一个领域，你将会看到更多，并且上升到下一个级别是非常令人兴奋的。

**希梅尔:**优秀。我想你会的。特蕾西，如果你不介意的话，这将是对你和你如何处理 *o* 笔源社区的一个改变，或者你认为不是真的，不是太多？

米兰达:没有，绝对没有。我认为会有很大的不同。我们有很多不同的人一起工作。我认为这是真正令人兴奋的地方，只是有不同的视角，不同的想法。我总是说，就像开源一样，我最兴奋的是意想不到的事情，直到它们发生时你才真正知道它们是什么，创新，或者两个人聚在一起说，“嘿，让我们朝着这个方向发展。”它充满了各种可能性，令人兴奋不已。

Shimel: 我认为会的，而且我认为肯定会的。你知道吗，我还没有读到——谁，尤其是 CloudBees 的谁，将在裁谈会基金会中占据董事会席位？已经宣布或决定了吗？

米兰达:所以我将代表 CloudBees 参加董事会，但 Kohsuke 也将领导技术监督委员会，这意味着他也将是董事会成员。我们模仿了 CNCF 的许多章程和基金会规则。

**希梅尔:**妙极了。那真的很好。詹金斯社区委员会的其他成员呢？像泰勒和其他人那样的人？他们会——如果你知道，他们今后会参与什么？

**川口 :** 我想章程会定义结构。它刚刚推出，我想，在接下来的几天里，我们将会有人们的名字等等。我只是不想给出错误的信息，但是泰勒，举个例子，他在这件事上起了很大的作用。所以我希望他能以某种形式继续参与进来。

绝对的。我知道这是今天才宣布的。你不知道所有的答案，但我想我应该问一下。最后一个问题，因为我们的时间不多了，这是一个——你称 CNCF 为姐妹基金会，很难说这不是莱纳斯基金会真正成功的努力，不仅仅是 Kubernetes。Kubernetes 似乎是明星学生，或明星青睐的孩子。CNCF 有很多项目做得非常非常好。对我来说，CNCFCon 和 KubeCon 是过去六个月里我参加过的最激动人心的活动，当然是自 Jenkins World 以来。CD 基金会现在会有类似的活动吗？或者你可以和 CNCF 一起为一个大型会议搭一个大帐篷？对此有什么想法吗？

**Miranda:** 首先，我们将举办首届持续交付峰会。我们将把它和巴塞罗那的新 KubeCon 放在一起。

**Shimel:** 五月。

米兰达:没错。是啊，进展很快。这将是我们第一次有机会将许多贡献者聚集在一起，还有许多最终用户社区。我们只是喜欢 CNCF 的项目。我们希望继续与这些人密切合作。我认为这将是一个伟大的第一次事件。我们今天刚刚听说巴塞罗那的活动预计有 12，000 人参加。CDCF 的超级超级粉丝。

**希梅尔:**是的。我会在那里，我们会在那里做视频。希望我们能见到 Tracy 本人，也许还能亲自做些视频采访。

米兰达:是啊，那太棒了。

希梅尔:嗯，那太好了。然后，我们会——我忘了下一次是什么时候了。在那之后，七月份是上海，然后秋天是 KubeCon 回到北美。这将是一个持续的合作，还是之后，你可能会做你自己的？

**川口 :** 我想我们还不知道。

Shimel: 待定。好吧，伙计们，首先祝贺你们，今天所有的新闻。这听起来太令人兴奋了。这是好东西。Kohsuke，我能说什么呢，伙计？你只要继续做下去。恭喜你。保持下去。特蕾西，恭喜你。我想在未来的岁月里，我们会听到更多关于裁谈会基金会的消息。

米兰达:是的，绝对的。非常感谢艾伦。这太棒了。

你知道吗？我听起来像科伦坡。最后一个问题。你可能太年轻了，记不起来了，但无论如何，为什么不是 CI/CD 基金会？CI 是不是要过时了，过时了，我们不参考了？还是我们太专注于 CD 了？对此有什么想法吗？

**川口 :** 围绕持续集成的实践仍然存在。我只是把它看作是向前发展的前沿，因此这个概念包含了越来越多的东西。当我们说连续 _____ 时，那么 _____ 包括我们作为 CI 谈到的所有东西。我认为它只是扩大成了更大的东西。

是的，好吧，很公平。伙计们，再次感谢，特蕾西，KK。CloudBees 的 Kohsuke 在宣布 Linux 基金会成立 CD 基金会和 Jenkins，Jenkins X 的一部分。我是 DevOps.com 的艾伦·希梅尔，您刚刚听到的是 DevOps 的一分钟聊天。

— [Alan Shimel](https://devops.com/author/ashimmy/)