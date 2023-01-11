# 交叉点:开发运维、发布工程和安全

> 原文：<https://devops.com/intersections-devops-release-engineering-security/>

随着创意、创新和人才的涌现，开发运维、发布工程甚至安全之间的界限正在迅速模糊。我邀请你和首席顾问 j·保罗·里德坐一会儿，听听他对这些曾经各自独立的领域之间的交集的看法——甚至可能是预示。

德里克·威克斯:早上好，保罗。那些追求开发运维的人可以从发布工程实践中学到很多东西。我知道你有很多经验要分享，所以让我们开始吧。

j .保罗·里德(j . Paul Reed):早上好，很高兴来到这里。我的背景是发布工程，虽然现在我实际上被称为 DevOps 顾问。我在这方面有 15 年的经验。这就是[我的演讲](https://www.youtube.com/watch?v=HK4RzzYbXag&index=11&list=PLotLY1RC8HovW-XnZbItSBupjbTzFkfJw)的内容:开发运维、加固开发运维以及发布工程之间的交集，并希望与安全和加固开发运维社区一起探索这一点。

![J. Paul picture](img/b9c9ca3e8da576192a3ea97bc64adadf.png)

**周:**在您的演讲中，您谈到了安全与开发运维之间的文化，以及许多组织面临挑战的发布工程，这就是“不文化”。有很多人说，“嘿，我们希望以更高的速度更快地前进。我们有新的要求，我们正在努力推向市场，我们有这些新的实践，我们正在向前推进。保安能来和 DevOps 队一起玩吗？”

**里德:** 实际上，我在 [我的一张幻灯片](http://www.slideshare.net/SeniorStoryteller/release-engineering-and-rugged-devops-an-intersection) 上贴了一条很多人喜欢的推文:“如果你对每个问题的答案都是‘不’，当人们开始努力甚至不去问的时候，不要感到惊讶。”这种观点认为，如果你对所有事情的回答都是“不”，那么这就像在互联网上一样，被视为一个错误或障碍，组织只会绕过它。我认为保安以一种发自内心的艰难方式发现了这一点。在发布工程中，这是同样的事情。

**—**

如果你对每个问题的答案都是“不”，当人们开始努力甚至不去问的时候，不要感到惊讶

**—**

[Git](https://en.wikipedia.org/wiki/Git_(software)) 变得如此流行的原因之一是因为开发者不必询问是否有创建分支的许可。他们创造了一整套无需询问的基础设施和生态系统。我认为这是我们面临的风险之一，也是相似之处之一。

我们在 DevOps 中发现的一个有趣的事情是——因为获得新的牵引力的想法和人们确实希望更快地移动——我们可以在管道的背景下设计我们所做的工作。通过识别和优化管道中的一些商业价值，企业是可以接受的。开发者容易接受。业务的不同部分以我职业生涯中几乎从未见过的方式接受，成为其中的一部分很棒。从坚固的 DevOps 或安全角度来看，我认为如果我们可以将这项工作转移到管道中，我们不仅可以在成本和权衡方面看到它，而且我们还可以做得更多。这是整体的一部分。有很多演讲都在谈论左移的想法，你可以把你的视角进一步转移到流中，这样你就可以更早地解决它，实际上有机会解决问题。

在与 Josh Corman 和许多经验丰富的 DevOps 人员交谈时，他们总是谈到在这个过程结束时，他们会盖上橡皮图章:“是的，这是安全的。”因为即使真的不安全而且很糟糕，你又能做什么呢？作为一名发布工程师，这引起了我的共鸣，因为我们一直都有这种感觉。我们在最后做了一堆工作，没有时间做好。所以很多时候，它被克扣。

**周:**当您想到传统安全的工作方式时，我们可以提前多久想到 rugged DevOps 向左转？

里德:是的，从本质上来说，我不认为一开始就把一切都做好有多重要。我认为，问题是我们能在这一进程中前进多远。我认为如果你能从头开始，这是可能的。开始是你定义管道的地方。

许多人将管道定义为提交，即开发人员编写代码。有些人会在产品管理阶段定义它，甚至更早。或者那种敏捷故事阶段，我认为你肯定可以在那里集成它。这就是我在演讲中探索的东西。我以幻灯片开始，介绍了发布工程和加固开发运维的交集，我说我其实不知道。这是一个非常新兴的领域。

**—**

“生产没有捷径……他们投入财力和工程资源来构建管道，让代码快速通过。”

**—**

我将在接下来的几张幻灯片中讨论制作这种酒吧的交叉方式。有很多相似之处。我认为，当你谈论推动这种东西前进时，它是关于你可以成为管道一部分的更多工具，比如发布工程工具。所以对我们来说，这可能是这样的:我们如何跟踪开发人员在他们正在做的工作中创建的依赖关系？那么，我们如何让他们更容易地说，“是的，我正在使用这个版本，它是从发布工程的角度集成在这里的。”然后，从安全角度来看，您可以利用这些信息来进行不同类型的安全测试或渗透测试。如果您能在流程的早期移动它，它就会这样做。那么你多早做这件事，实际上是你在这类事情上有多擅长的一个函数。

我认为我们还没有完全看到这种安全性。我们仍然认识到发布工程的价值，并且公司正在全力以赴。他们只是把一切都放在那里，继续输送管道。生产没有捷径可走。没有后门可以部署东西。他们投入财务资源和工程资源来构建管道，使代码快速通过管道。一旦你做到了这一点，如果你愿意，你可以用越来越多的特性来扩充这个管道。其中之一可能是在这一过程中推进安全措施。

在新的世界里，旧的做事方法是否不再适用，你必须采用新的工具或实践？

**Reed:** 我确实听到了很多，“嗯，我们不能做 X，因为 Y”——“Y”是你所说的那些过时的方式之一。我们在会议上不断看到的一件事是，答案的想法是，“我们不能做 X，因为旧的方式。”事实上，在安全领域，你经常会看到这样的话:“因为审计兼容的东西，我不能做 X。”但一个又一个案例研究表明:如果你愿意重新思考审计合规和与审计师合作的方式——如果你愿意以稍微不同的方式看待问题——那么你就可以取得这些结果。因为我们有所有这些证明，当人们说，“哦，我们不能做 X，因为老方法，”我的问题是，“我们是在一个旧框架中思考问题，还是在一个缝得不够的更传统的框架中思考问题？”

这并不意味着人们提出的担忧是无效的。这是你最初的问题，是关于人的。如果他们有很多知识，他们可能会担心，“好吧，我不能像测试那样自动操作。”我在演讲中谈到了发布工程正在经历一场根本性的转变。我非常坦率地说，如果你是一名发布工程师，你没有建立持续交付管道，也没有参与持续交付管道的支持和服务，你的工作可能在 5 到 10 年内都不会存在。这就是世界运转的方式。很多人会想，“哦，好吧，那真不幸，”或者其他什么。

**—**

“如果你是一名发布工程师，而且你没有建立持续的交付管道，也没有参与持续管道的支持和服务，你的工作可能在 5 到 10 年内都不会有。”

**—**

我给你举一个 QA(质量保证)的例子，我认为它很有创意。

组织花费大量的时间来自动化测试，最初的反应是，“如果你自动化所有的测试，QA 工程师会做什么？”事实证明，因为 QA 工程师非常擅长观察产品并提出需求，所以他们需要将大量完全有价值的知识转移到价值流中。他们让 QA 工程师进行需求分析，并与产品管理部门合作，以确定进入持续交付管道的实际需求。令人着迷的是，这个组织并不是这样，“我们会自动让你失业，然后我们会解雇你，所以去把你自己自动变成一个脚本。”人们会说，“我是人，不是机器。”你有整个对话，他们最终做更有趣的工作。

他们把他们放在需求分析中的连续交付管道上。这和你想象的完全不同。安全和发布工程也是如此。尤其是在安全性方面，我们将会看到大量的工作。您可以以自动化方式完成一系列法规遵从性工作。一旦实现自动化，我会看到很多关于红队、蓝队的讨论……类似战争游戏之类的东西。这样可以腾出时间来做这件事，并以这种方式作为一个团队来工作。因为你不能自动化所有这些事情，或者至少今天你不能。我想安全领域的每个人都会同意，如果你有一个巨大的项目，有一个黑色的活页夹，上面有一堆规则，这比东奔西跑更有趣。

**周:**真正引起你共鸣的概念之一是软件供应链。这一概念与正确实施发布工程、正确实施加固开发操作系统或者将安全性融入开发操作系统有什么关系？

里德: 是的，供应链的想法是我第一次听到时就着迷的东西。事实上，这是我和乔希第一次见面时花了很多时间讨论的事情之一。我认为这是一个很好的解决问题的方法。我很难过我没有想到这一点，事实上，原因是因为发布工程师一直在想这个问题。我们认为这是我们 20 到 30 年来的职责，只要发布工程存在。这就是了解依赖项是什么、依赖项管理跟踪并试图确保您不会引入不良依赖项的想法——无论它们是因为许可证还是包含恶意软件而受到污染。这个问题在开源软件中变得更加严重，从供应链的角度来看，这也是我们经常谈论的事情。

**—**

“我讲述了一个工程师的故事，他在构建中丢失了一个 DLL。他们只是谷歌了 DLL 并下载了它，然后把它扔到了所有的构建机器上。这太可怕了。”

**—**

这是我认为不会让发布工程师像让安全工程师一样夜不能寐的事情之一。我们的软件来自哪里，它可能有什么问题？不管出于什么原因，这似乎不是传统开发人员考虑的事情，这并不是贬低他们。很多时候，他们和我们一样，都有最后期限。他们去上网。他们抓取任何版本的库。事实上，我通常看到的是升级版本，因为他们需要一些 API 或类似的东西。当你思考这个问题的时候，你会担心这个问题是从哪里来的。我讲述了一个工程师的故事，他是构建中缺失的 DLL。他们只是谷歌了 DLL 并下载了它，然后把它扔到了所有的构建机器上。那真是太可怕了。

我认为演示中非常关键的一张幻灯片是:“如果你的产品中有一个易受攻击的库，那就是安全问题。如果你有同一个库的多个版本，而这些版本又容易受到攻击，这就是发布工程的问题。”这是发布工程师可以为加固型 DevOps 做出贡献的最佳方式之一，也是在帮助解决该问题方面为安全领域做出贡献的最佳方式之一。更有趣的是，一旦你解决了这个问题，你必须想办法让它不再变成意大利面条。

顺便说一下，我已经多次解决了这个问题，通常不是在安全环境中，而是在许可环境中。

**—**

如果你的产品中有一个易受攻击的库，那就是一个安全问题。如果你有同一个库的多个版本，而这些版本又容易受到攻击，这就是发布工程的问题。”

**—**

你这样做的方法是，再一次向左移动。向前推进，当开发人员将库放入产品时，新的代码不是由他们编写的，因为那里有一个很好记录的依赖关系。您可以以一种连续方式进行审计，因此您构建的工件可能是库转换的列表。然后，从自动化安全测试的角度来看，我们可以将其与 CD(连续交付)使用或已知问题的列表进行比较。

**周:**我在 Sonatype 做了很多关于软件供应链的研究，有一个数据让我大吃一惊。在下载量排名前 100 的组件中，每种组件平均一年下载 27 个版本。当你考虑到复杂性和技术债务时，如果其中有安全债务，你只需要 100 个部件，但你使用了 2700 个部件。你为什么想这么做？

我要指出的一件事是，我认为从某种意义上来说，这个行业正朝着错误的方向发展。也就是说，你已经有了内置的 Java，让它变得非常、非常、非常简单。从命令行，你只需从互联网上获取库。谁知道他们从哪里来。[节点](https://nodejs.org/en/)使这变得微不足道。事实上，Node 是围绕 npm(包管理器)构建的。所有这些都是在线的。事实上，更糟糕的是。这些天我被叫去帮忙的一件事是——我对此有点傻笑，只是因为二分法——人们对 Git 如此感兴趣如此之久，因为它就像离线 Git，离线 commit。很棒，对吧？你可以离线构建，人们总是用这个例子，当我在回家的火车上，我可以提交等等，这是我这么做的主要原因。

现在，我们已经使用了 Node 和一些围绕 Java 的工具，因此我们的软件构建实际上需要我们与互联网通信来下载包。线下运营有很大的推动力。但是没有下载需要 680 亿个版本的库也没问题，一切都是“自含式”的。但是如果你要看一个节点包，它里面有这些东西的版本。那是功能，不是 bug。对吗？在某些平台上——你可以在 RubyGems 上看到这一点，当 Ruby Gems 站点关闭时，没有人能够部署他们的 web 应用程序。在我看来，这是一个根本性的工程设计。对于开发者来说，这并不容易。但是我们的构建过程，我们的部署过程，依赖于这些东西。他们依赖我们这些开发人员说，“我想要那个库的 1.2.4 版本，还有那个 1.2.4 版本。与您使用的版本相同。”

我贴了一张关于版本控制的幻灯片，这是一个非常大的发布工程问题。例如， [Open SSL](https://www.openssl.org/) 在他们的版本控制中犯了一个错误，他们没有像应该的那样修改版本，而是重新打包了二进制文件。我怀疑他们这样做的原因是因为他们发布了所有带有该版本号的 CVE(常见漏洞和暴露),每个人都像老鹰一样盯着开放 SSL。所以他们不能轻易篡改版本号。开放 SSL 在他们的发布工程中不能再灵活了，因为他们在传统上是如此的糟糕。对吗？我们已经很容易地将所有这些组件塞进我们的产品中，但我们真的不知道我们在里面塞了什么。

如果你看看，我们最终会担心很多相同的事情。我认为，如果你愿意的话，在崎岖不平的 DevOps 社区中，可能有 50%到 80%的工程问题需要解决。加强安全的额外功能，使其成为安全的一部分，特别是在供应链方面，将会非常有效。

**—**

**“如果你愿意的话，在崎岖不平的 DevOps 社区中，可能有 50%到 80%的人会遇到工程问题。加强安全的额外功能，使其成为安全的一部分，特别是在供应链方面，将会非常有效。”**

**—**

**周:** J .保罗里德，非常感谢。和你谈话很愉快，我真的很喜欢这次谈话。我们期待很快再次见到你。

**芦苇:** 牛逼。谢谢你。

如果你喜欢这个采访，并且正在寻找更多关于加固开发应用程序的好材料，我邀请你下载来自 Forrester 的 Amy DeMartine 的这篇很棒的研究论文，“加固开发应用程序的七个习惯”

![Amy DeMartine](img/3ec88b45ad57bcafbdd9f4e1b992d63b.png)

正如 Amy 指出的，“没有安全和风险(S&R)专家的专业知识，DevOps 实践只能在一定程度上提高速度和质量。旧的应用程序安全实践阻碍了快速发布，而安全漏洞代表的缺陷可能会使公司面临网络攻击。但是 DevOps 实践者可以通过在 DevOps 反馈循环中包括 S&R pros 和在自动化生命周期中包括安全实践来提高速度和质量。这些新的实践被称为坚固的 DevOps。"