# 安全开发者播客:Chef 的持续安全性

> 原文：<https://devops.com/secure-developer-podcast-continuous-security-chef/>

欢迎来到 Secure Developer，这是一个关于开发人员安全性的播客，涵盖了您可以并且应该在开发工作流程中采用的安全工具和实践。安全开发者由 [Snyk](https://snyk.io/) 的首席执行官兼联合创始人[盖伊·波德贾尼](https://twitter.com/guypod)主持。

在本期安全开发者中，Guy 与 Chef CTO Adam Jacob 讨论了安全在开发运维以及持续集成/部署中的作用。它们涵盖了内置和外加安全性之间的差异，以及 Habitat 的自动化如何改变开发人员处理安全编码的方式。 [Adam Jacob](https://twitter.com/adamhjk) 是 [Chef](https://www.chef.io/) 的联合创始人兼首席技术官，前身为 Opscode，他在那里编写了开源、自动化应用程序项目 [Habitat](https://www.habitat.sh/) 。

本播客由 heavy bit(T1)为您带来，这是一个帮助开发产品公司将其产品推向市场的项目。

[soundcloud url=”https://api.soundcloud.com/tracks/295763125?secret_token=s-AfcYk” params=”auto_play=false&hide_related=false&show_comments=true&show_user=true&show_reposts=false&visual=false” width=”100%” height=”166″ iframe=”true” /]

* * *

**Guy Podjarny:** 大家好，欢迎回到安全开发者。今天我们节目中有一位很棒的嘉宾，《大厨》的亚当·雅各布。亚当，谢谢你加入我们。

亚当·雅各布:嗨。

**Guy:** 我们将讨论我们提出的各种很酷的话题，我认为这些话题与安全领域、DevOps 和 CI/CD 领域以及一些非常有趣的新包管理、构建来自 Chef 的系统功能非常相关。

在我们开始之前，对于你们中可能不知道 Adam Jacob 或厨师 Adam 的人，你想简单介绍一下你的背景吗？

当然，我想可能有很多人不知道我是谁。我是亚当。我最初写的是厨师。我是 Chef 的 CTO，不久前我写了一个叫做 Habitat 的东西，它实现了应用程序自动化。这是一种新的东西。

然后，大部分所有这些都可以归结为，我花了过去 10 年去和像脸书、谷歌和雅虎这样的大网络公司交谈，我也花了很多时间和创业公司在一起。然后我也去参观了真正的大企业，从大银行到保险公司，零售公司，像诺德斯特龙，沃尔玛。

所以我可以四处走走，看看每个人都在做什么，看看他们在担心什么，并尝试帮助他们在所需时间或交付速度，或者他们的组织或文化方面做得更好。所以有一部分是软件，但大部分只是帮助人们理解如何更好地建立他们的组织。

**Guy:** 是的，我想总会有关于开发运维以及持续部署是否更具体一点的讨论，但是开发运维实际上更多的是关于工具，更多的是关于人，这是一个共识。

**亚当:**都是吧？就像，如果你有一个伟大的文化，说你想有一个好的文化真的很容易。“哦，我想授权给人们，”或者“我们想简化一个过程”，或者诸如此类，这真的很容易。它不需要任何东西。只是文字而已。

> 通常，是技术强化了那些拖你后腿的文化行为。

所以，一个很好的例子是，“哦，我想做连续交付，但是我们使用了一个糟糕的源代码控制系统，这使得几乎不可能做有效的连续交付。但因为这是我们使用的源代码控制系统，我们永远不会改变。”

因此，哪个是真的？你是想做持续交付，还是爱你糟糕的源码控制系统？所以这里面隐藏着一个强化圈，我想你在安全领域也一直看到，同样的圈，同样的行为。

每个人都说，“哦，我们想要安全。”我和一家银行合作，我不想透露这家银行的名字，我已经订婚几个星期了。我的第一个问题将帮助他们实现持续交付，他们希望，他们的第一个目标是强化操作系统。

我问他们，“好吧，你们有强化规范吗？你知道你要硬化什么吗？”他们说，“哦，是的，是的，我们当然知道。我们是一家全球性银行。”我说，“太棒了，太棒了！我很乐意看到这一点。”他们说，“哦，我们会在你到达的那天给你准备好的。”

三周后我离开了，他们一直没有找到它。他们意识到它并不存在。每个人都认为是别人建的，这是别人的工作，但实际上没有人这样做。这只是理论上他们应该做的事情的松散聚合，但实际上没有人能够跟踪或知道。这是一家全球性银行。这可能很重要。

Guy: 我认为有时这是关于混乱或者工具可以帮助表面信息并以一种可访问的方式保存信息的事实。有时，当您谈论关于容器如何操作或一些机器如何编排的深层操作主题时，这只是许多这些更复杂主题的纯粹障碍。

或者在安全领域，当您谈论更深入的安全时，了解什么是攻击，什么不是，以及那种不断变化的情况。从根本上说，你必须有工具。你不能仅仅通过教育来克服这些问题。与此同时，

> 如果你有工具，而人们不知道如何使用它们，或者他们不知道它们的用途，那么你最终将无法实现你的目标。

亚当:语境决定一切，对吗？明面上很棒，但还不够。我们在 Chef 和安全领域做的事情之一是我们有一个叫 InSpec 的东西，这是一种让你描述安全状态和代码的语言。

所以你可以说，“这台特定的机器应该有这个特定的策略。该策略意味着端口 25 应该打开，您应该能够以这种方式进行身份验证，您不应该以这种方式进行身份验证。”您应该能够谈论正在安装的软件包，您应该能够谈论所有这些事情，然后将它们与实际的安全项目联系起来，并谈论它们的严重性。

我们关心这个东西是因为 HIPAA 这一块，或者我们关心它是因为 CIS 这一块，或者别的什么。这些工具很棒，因为它们结合了文档，这就是标准，以及实际可执行的检查，“我们达到标准了吗，是还是不是？”

我认为，无论是 InSpec 还是 InSpec 之类的工具，当您考虑安全的操作部分以及它如何应用于那些大型企业，尤其是大型企业以及大型 web 时，越来越多的人认为该策略是可执行的。

因此，安全性与开发人员和操作员之间的对话变成了围绕代码的对话，而不是围绕文档和控件的对话，我认为这是大多数人现在的对话。

某个安全人员编写了一个控件，然后这里有一个人员列表，他们说他们可以验证这个控件。但是控制有什么好处吗？

盖伊:这真的发生了吗？

亚当:不，我是说，不是的，对吧？

盖伊:是的。

亚当:在任何地方都是如此。我们写了一个控件。这是 10 个你可以去采访的知道如何控制的人的名单。好吧，那另外 10 个也可以这么做的人呢，他们不在去年没有更新的面试名单上。他们总是以正确的方式做手术吗？

> 他们总是让这个过程正确吗？当然，答案是否定的。但我们只是让它顺其自然，因为审计员通过了。

Guy: 是的，这是保护自己免受审计，而不是攻击的概念。

**亚当:**正是！

盖伊:它变得越来越有吸引力。我喜欢这个想法。因此，对于 InSpec，或者总的来说，对于安全性，一个关键的挑战是它是不可见的。所以如果你没有做，你真的没有直接的迹象表明它没有发生。

如果你愿意的话，不监控、不监视某个漏洞的用户体验，和监视它却什么也没发生的用户体验是一样的，也就是说，什么也没发生，对吗？

亚当:是啊，这没什么。

盖伊:这是个好消息。因此，我认为任何有助于定义和阐明应该发生的控制的东西，都会给你一些机制来了解已经采取的行动，这样你就知道检查、锁定或任何东西，如果我们使用一个简单的例子，限制端口被打开，它已经被这里的工具明确阐明和明确跟踪，你可以得到通知，它已经发生。

我们在 Snyk 经常看到这种情况。我们观察项目的漏洞，脆弱的依赖性，然后你真的，再一次，回到你有相同的用户体验的事实。如果你没有在关注一个项目，或者如果你在关注一个项目的漏洞，而那里什么都没有发生，我们今天与用户进行了很多这样的对话，关于“你想如何了解它？你怎么知道你正在看它？”

今天，我们仍然相当简单。我们只是停留在这份正在进行的报告中，向您展示“嘿，您正在监控五个项目”之类的东西，他们有这些东西。

**亚当:**对，说明它经常反应，或者什么的，我们可以衡量变化。

**Guy:** 但是越来越多的拥有这些东西，对你的 Chef 和 InSpec 有一些要求，这很好，这也定义了它，项目 X 被监控 X，Y，Z，所以你知道它正在被强制执行。

亚当:对，然后你把它插在管道里。

> 当您考虑连续交付和安全性时，安全性和符合性的验证是软件投入生产的过程的一部分。

这是软件一旦存在就得到维护的方式的一部分，也是构建过程的一部分。你在整个 SDLC 中烘焙它，而不是在最后发生的事情。

这显然是个好主意。所以，当你一听到它，你会说，“哦，当然，安全应该融入整个过程，贯穿整个过程。”

**Guy:** 整体内置 vs 外挂。

亚当:对，对吗？算是吧。但实际上，这样做实际上完全是——

盖伊:一场完全不同的比赛。

亚当:完全是另一回事。我们真正意识到的事情是，特别是使用 InSpec，但一般来说，如果您不能找出如何像管理您所做的其他事情一样管理该安全状态，那么就很难告诉软件开发人员确保该状态是好是坏是他们的责任。因为，当然，他们可以让自己写出“好代码”你听不到引号，但是我可能在脑子里画了些小引号。

盖伊:我可以证明这一点。

Adam: 这很好，但你不能真的要求他们了解它部署后的情况。

因为从软件开发人员做出决定到软件开发人员谈论软件应该如何投入生产，以及它的状态应该是什么，这两者之间的距离是如此之大。他们影响 it 的能力如此之低，以至于很难回头对他们说，“哦，这是你的责任。”很明显是因为你。

当这些工具让你有能力把它当作代码来谈论时。他们允许人们参与，你可以对他们进行代码审查。您可以让安全人员审核代码，而不是审核您的文档，然后将这些内容作为部署模型的一部分，我认为一切都会变得更好，并且会变得更加安全。

以这种方式做事的一个困难之处在于，这与目前大多数安全机制的建立方式完全不同。如果你去和一个安全官员谈话，你问他们，“嘿，我们能继续遵守任何标准吗，HIPAA？”如果我们所做的每件事都被持续交付，十有八九，答案是否定的。

有趣的是，有十分之一的保安会说，“我不知道，也许吧。请告诉我更多有关如何运作的信息。”我想如果我把时间倒回到三年前，10%的人说不，这太疯狂了。现在十有八九是这样。我预测六个月后，会是十分之六。然后在两年内，这就像在谈论“你应该做连续交付还是应该做敏捷？”

**Guy:** 实际上，有时会涉及到评论，甚至是大银行没有的文件或其他东西。就像，这些事情最终会回到文件和指导方针上。最终，你会走上合规之路，实际上合规文档中写着，如果你使用连续交付，那么为了符合 HIPAA，你需要确保你正在做这些事情，而不仅仅是有一个目标。

这些法规中的许多都有同样的缺陷，同样的概念说，“好吧，你必须做这些行动，”而不是“你必须实现这些目标。”所以他们给出了模糊的目标，但是每个人都规定了建议的行动，因为这使得通过审计变得最容易。

是的，我的意思是，

> 审计员和您的安全状况之间的关系非常紧密。

在大多数情况下，对您的安全状况的真正考验是审计员。不像笔测试，或者人们真的试图打破你。我是说，他们是，但是你没有主动去做。

我认为，当您考虑这些 CD 管道时，它们会持续应用，随着应用程序的变化，您会重新应用安全状态，以查看该应用程序是否做了违反该状态的事情，当您改变安全状态时，您会重新验证应用程序，并且您会在整个周期中这样做，这非常强大。这是人们开始能够做到的。我认为你还没有看到很多，但它是未来的一种。

Guy: 我认为理解这一点很有意思，潜在与正在发生的事情，对吗？高级别的持续部署和您的整个基础架构的代码，事实上，您已经规定了它，内置了它，允许您获得可预测性。你知道什么是哪里，你知道某个测试或者某个执行已经做到了 bug 的程度。但至少，不是人为错误。

另一方面，它要求安全审计员改变他们的行为方式。这不仅仅是法规遵从性的问题，事实上，今天，你举了一个安全审计员审查你的代码的例子，其中许多安全审计都是作为 gates 完成的。

> 它们是以一种方式完成的，意思是“停在这里”，这是连续的反义词。

持续的整个概念就是，你滚出去。停顿片刻没关系，但不能停下来。你不能积累积压，因为否则它会恶化，除非你自动化。

**亚当:**是也不是，对吧？有持续的部署，然后有持续的交付，它们不太一样。所以，是的，在持续部署中，没有停顿的地方。我觉得在持续交付中，是有的。

在连续交付中，想法是当你应该能够发货时，在业务需要发货或有理由发货的任何时候发货。这与说“我们只是在您每次提交时发货”是不同的，对吗？所以在连续交付中，我认为有足够的空间说，“嘿，这个项目，为了交付，需要安全审查。”并且该过程仍然可以是连续的。

问题是，这应该是你和生产之间的唯一大门。如果他们同意，你能发货吗？接下来的问题是，对于每个提交都是这样吗？比如，如果今天是时候，你能今天发货吗？答案很少是肯定的，所以这就是困难所在。

盖伊:是的，我认为这是一个有趣的评论。我接受持续交付和持续部署之间的差异，但在我看来，从安全的角度来看，首先，即使从质量的角度来看，持续交付和部署的价值之一是，在任何给定的时间，当错误很小时，你可以发现错误。

因此，毫无疑问，对于持续部署，当您发布每一个小的代码更改时，无论如何，在一些低分辨率下，当问题发生时，更容易查明问题是什么，问题的来源。

这个价值主张在安全性方面也很有说服力，对吧？如果你正在寻找一个安全漏洞，能够只在 100 行代码与 100，000 行代码或 1 亿行代码之间的范围内寻找漏洞是非常有价值的。如果您积累了这些变更，并且您现在需要进行安全审计，我认为您实际上还没有准备好交付。

本播客由 [Heavybit](http://heavybit.com/) 为您带来，这是一个帮助专注于开发者的公司将其产品推向市场的项目。在整个项目中，创始人致力于开发者牵引、产品市场匹配和客户开发。如果你喜欢你所听到的，一定要在 iTunes 上订阅 [Heavybit 的播客网络。](https://itunes.apple.com/artist/Heavybit/id1110471754?mt=2)

— [玛利亚·鲍尔斯](https://devops.com/author/mpowers/)