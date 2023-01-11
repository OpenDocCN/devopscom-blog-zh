# DevOps 聊天:提高交付速度，可发布

> 原文：<https://devops.com/devops-chat-increasing-delivery-velocity-with-launchable/>

Jenkins 创始人 Kohsuke Kawaguchi (KK)和受人尊敬的 DevOps 资深人士 Harpreet Singh 创办了一家名为 [Launchable](https://launchableinc.com/) 的新公司。

Launchable 旨在通过优先考虑和应用一些 ML 和智能来帮助您提高交付速度。仍有许多工作要做，但有这两位行业名人的支持，人们对一些有影响力的东西抱有很高的期望。

风险投资界和蓝筹股投资者已经加入进来。

是的，这意味着 KK 不再是 CloudBees(几位 CloudBees 高管是 Launchable 和 Jenkins 的投资者)和 Jenkins 的员工，尽管他仍然是一名顾问。但是，随着 Jenkins 现在在 CDF 和 Linux 基金会的有力支持下，CloudBees 已经建立起来，他觉得这是一个追求他认为需要解决的问题的好时机。

在这个伟大的播客中，听听 KK 和 Harpreet 他们自己。

[https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/tracks/748166725&color=%23ff5500&auto_play=false&hide_related=false&show_comments=true&show_user=true&show_reposts=false&show_teaser=true](https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/tracks/748166725&color=%23ff5500&auto_play=false&hide_related=false&show_comments=true&show_user=true&show_reposts=false&show_teaser=true)

## 副本

Alan Shimel: 嘿，大家好，我是 DevOps.com 的 Alan Shimel，我在这里，你们正在收听的是另一个 DevOps 聊天。在这次 DevOps 聊天中我们有一些非常棒的突发新闻。我真的很高兴在 DevOps 领域抓住了一对充满活力的行业资深人士，他们刚刚开始了有望成为 DevOps 行业游戏规则改变者的事业。但他们会告诉我们更多，我不知道。

让我给你介绍哈普瑞特·辛格。

哈普瑞特·辛格:你好。

嗨，哈普瑞特，你好吗？

辛格:很好，谢谢。

**Shimel:** 谢谢。Harpreet 是新公司的联合首席执行官，他的联合首席执行官不是别人，正是我的朋友 Kohsuke，K.K .，Jenkins，CloudBees 和所有这些好东西的创始人。好的，欢迎。

**川口幸介:**你好。谢了。

**Shimel:** 好了，那么，我们来说说大新闻吧。我们在 DevOps 领域成立了一家名为 Launchable 的新公司。

**川口:**是啊。

**Shimel:** 是这样吗——你们两个都是联席首席执行官？

**辛格:**没错。

当然，以你的记录，我敢肯定，你知道，这并不像第一次创业那么难，但 Launchable 已经筹集了一些风险资本来帮助它起步，包括一些高调的天使。

**川口:**是啊。我们非常幸运。

**Shimel:** 简单介绍一下——谁参与其中，谁投入了一些资金？

**川口:**所以，有两大机构投资者。一个是巴克莱风险投资公司，这来自 Harpreet 与他们的合作伙伴 Gomesh 的长期关系。我想，事实上，你们的妻子互相认识。就像，感觉像是内部人员。*【笑声】*

另一个风险投资是非常规风险投资，它是由非常规风险投资发起的，由约翰·弗里奥尼斯发起。约翰实际上也是 CloudBees 的投资者，所以他的人看到了我们的行动，对我们足够了解，所以，你知道，你得到他们的认可，然后你努力去做。我真的很感激。

Shimel: 当然可以。我对电池很熟悉，那是电池投资公司的一个叫格里·康伦的人。我不知道你们是否认识 Gerry，但他在 Battery 的早期很有帮助。但是，是的，他们是一个伟大的公司。这听起来像两个，你知道，那种贵族风险投资公司。

还有一些高调的天使，包括 Sacha——Sacha laboury，CloudBees 的首席执行官，对吗？

辛格:是啊，是啊。所以，我认为，当我们与人们交谈时，让我们兴奋的是，你知道，我们从投资者以及——你知道，这些大牌投资者以及个人天使投资者那里获得了惊人的支持，对吗？所以，我们都去过 CloudBees。

所以，我不喜欢认为我们是第一次创业，因为我们从不到 10 个人建立了 CloudBees，直到今天。

**Shimel:** Yep.

我在 Atlassian 逗留了一段时间，在那里我花了大约一年半的时间向这家杰出的公司学习。所以，当来自 CloudBees 的人，比如萨查，米歇尔-米歇尔·古森斯，他曾经是那里的销售副总裁，来投资的时候，我们非常幸运。鲍勃·比克尔，一位在美国投资的行业老手。在 Atlassian 方面，首席技术官是 Sri Viswanath 和 Noah，他们是技术团队的负责人，包括吉拉、Bitbucket、Opshimi 和所有这些对我们的能力和使命进行投资的人。

绝对的。别搞错了，你们不是第一次创业，因为第一次创业没那么容易筹集到资金，伙计们。

**辛格:** *【笑声】*

**川口:** *【笑声】*

**Shimel:** 我的意思是，我认为会有很多第一次创业的人听了这个播客后会说，“伙计，如果我们有他们的背景、简历和经验，事情就不会这么难了。”我想很多第一次创业的人都很纠结——纠结于这样做。

但那很好。当你开始创业时，在银行里有一笔钱总是好的，因为它是必需的，但正如我们在镜头之外谈论的那样，我从未见过一个成功的创业企业家不认为他们所做的事情在某种程度上改变了世界，让世界变得更好。

所以，我想问你们每一个人——是什么真正让你们兴奋不已？你们在 Launchable 所做的事情中，真正让你们感到兴奋的是什么？

**川口:**当然可以。好吧，那我开始了。所以，你知道，我开始的事情之一——我创造了这种想法，我觉得我把自动化和软件开发能力的状态提高到了世界的下一个水平。这种自动化产生了大量的数据。过了一段时间，我意识到，你知道，在世界的其他地方，在商业世界的其他地方，数据正越来越有效地被用来推动决策，让人们更有效率等等。

但是在软件开发中，我觉得这实际上并没有发生。我觉得这是一个巨大的耻辱，你知道，作为一个帮助人们用这些自动化系统产生大量数据的人，但是，你知道，我们是数字人，我们是数据人，对吗？我们是 ____ 的骄傲，至少我是这样认为的。

**Shimel:** Mm-hmm.

然而，无论在哪里，我都觉得我们在做决定，是基于直觉和本能的工程决定，这种情况不能再继续下去了。所以，过了一段时间后，我开始思考这个问题，然后这个想法在我身上越来越多。所以，是的——所以，那可能是我的，我的果汁开始流动的地方。

**希梅尔:**优秀。

辛格:是的，非常相似。我想 Kohsuke 和我曾经在 CloudBees 的同一个办公室里坐在一起，我们曾经一直在谈论这个问题。我们有机会看到销售和营销真的完全由数字驱动，我们会回来说，“哦，如果我们只能在我们的工程产品方面这样做，那会好得多。”答案总是，“嗯，这是一门手艺。”我们认为把数据带进来是很重要的。

**Shimel:** 对。

辛格:所以，这就是我们两个前进的动力。我个人的轶事是，在我离开并搬到 Atlassian 后，我与我的客户群中的一些人交谈，他们面临着交付速度缓慢的挑战，你知道，他们的目标是让一些工程师进去看看如何改进它。有了 DevOps 的背景，并且你了解 CI/CD，我觉得应该有更好的方法来做这件事，而不仅仅是“让我们分配几个工程师，看看会有什么结果。”

**Shimel:** 对。

辛格:这就是问题所在，也是让我们兴奋的地方。

**希梅尔:**优秀。事实上，当你仔细想想，这几乎是讽刺或矛盾的，对吗？

**辛格:**对。

Shimel: 因为——所以，我的背景是信息安全，对吗？我们在安全领域看到的一个现象是信息过载，比如数据过载。

**辛格:**对。

**Shimel:** 信噪比。但是，在过去的五年或七年里，有很多安全初创公司真的尝试过微调这个刻度盘，以获得更多的信噪比，能够自动处理成堆的日志数据，例如，对吗？

**辛格:**嗯嗯。

**Shimel:** 所以，像 Splunk 这样的公司可以从任何地方获取大量数据。然后试着用自动化的方式计算出来——因为有太多东西需要手工处理——

**川口:**正是。

**Shimel:** 从安全角度，甚至从网络运营角度来看，什么是重要的？但是正如你们所说的，我在想——我们在软件开发中并不真的这么做，不是吗？

**川口:**是啊。我的意思是，当你描述它时，它可能听起来有点抽象，但是理想化了，它实际上在很多方面与我作为开发人员每天遇到的挫折有关，对吗？

我给你举个例子。你知道，我正在做这个 Jenkins 项目，这是一个相当大的项目，有很多测试案例，这很好，但这意味着每当有人想做，比如说，一个 ____ 的改变，首先发生的是，CI 系统进来，他们在代码审查发生之前运行整个一个小时的测试周期，然后有人提出一些观察或建议，“哦，你应该把这部分改成别的。”然后你接着又进行了整整一个小时的测试。实际上，如果你想换零钱的话，两个小时是很长的等待时间。那个地区整天都在发生这种事。

不，不——我的意思是，让我成为一个半杯满的人。这比——一个小时比我们自动化之前的一天要好，对吗？

**川口:**确实如此。

**Shimel:** 我记得在我的 StillSecure 时代，我们甚至没有足够大的基础设施来进行测试，我们必须外包，比如单元测试和所有这些东西。

**川口:**对，所以，我们来谈谈那件大事，对吧？因为这实际上可能是一个更大的项目。你说那是在自动化之前，但是我每天都看到团队实际上运行超过一天的测试，你知道，*【相声】*。

**Shimel:** 带自动化？

川口:对，就像汽车制造商公司组装汽车一样，需要很多大型软件。如果你对它们都进行测试，这种循环会持续数周。因此，有许多软件被组装成一个大的东西，这个测试变得更大。

所以，我开始做的是——好的，所以，每次你这样做的时候，并不是所有的事情都在同时改变，对吗？只有系统的一小部分在改变，然后当我们重新运行整个测试周期时。那么，如果我们能够为测试运行选择正确的子集，会怎么样呢？它们很可能是独立的程序，所以它们不仅完成得快，而且运行起来也很便宜，而且你还会得到相当可观的、有意义的反馈。你知道，你不会得到 100%的覆盖率，但你可能会得到 95%，这是非常好的，这将执行减少一半。

所以，这些是我认为数据实际上能够实现的事情，我已经看到了一些先前的工作，我已经与似乎处于做这些事情的尖端的团队交谈过，我觉得——是的，这显然是有道理的。越来越多的人需要，我也需要。所以，这成了 Launchable 背后的创始理念。

Shimel: 所以，就像我说的，这就是你想要抓的痒处，对吗？

**川口:**对，对。

**辛格:**然后你问，像*【相声】*——

**Shimel:** 不好意思，说吧。

**辛格:**是的，当我们在思考这个问题时，我们发现了这个问题，我们在思考，比如说，公司的使命是什么，对吗？我们意识到，未来甚至今天的每一种软件团队都将推动人类的每一项重大成就。真的很难想象任何不是软件交付的东西。

我们现在的任务是带领这个工匠团队，让他们成为数据驱动的科学家，推动他们的速度，你知道，自信地交付软件。所以，这是我们最大的渴望，也是我们最大的使命。

**Shimel:** 当然，知道了。所以，让我来唱唱反调。你知道，我们过去经常听到的一件事——我在安全部门听到过，在质量保证部门也听到过——是，“看，我们没有足够的时间进行全面的测试，全面的测试。让我们来测试一下 80%、70%、90%”—随便你选，我不在乎你选什么数字。

你知道，墨菲定律说，无论你不测试什么，它都会以某种方式坏掉，对吧，或者引起问题。当我们说，“哦，我的上帝，因为我们没有测试”——为什么我们没有测试呢？

**川口:**对。所以—

**Shimel:** “为什么不能完成呢？”没错。

**川口:**是啊。所以，如果你认为测试是孤立的，那么是的，这自然是一个问题，因为，你知道，我们需要从测试中得到的每一个帮助和每一个信心。所以，你为什么要跳过这个？这说不通。

但我认为它确实有意义的地方是，如果你仔细想想，软件开发生命周期是由许多不同点上的许多不同测试组成的。所以，总的来说，它们应该被视为一个整体系统，对吗？我的意思是，这就像——那么，代码审查，对吗？如果这是您运行测试的唯一点，那么您希望运行所有的测试。但是发生的是，在感冒得到审查和合并，然后另一组相同的测试将进来。所以，在代码评审之前运行所有的测试并花一个小时是非常重要的，或者你可以接受 80%的信心发生在五分钟内，对吗？然后知道剩下的 20%会立即得到代码。

我认为有一个论点是，总的来说，你会更好，即使一些程序滑入了 ____，只要它最终在客户看到一切之前被发现，所以。

**Shimel:** 所以，我想这就引出了一个问题——这能实现吗？为了实现这一目标，需要做些什么？

川口:嗯，是的，这就是我们正在做的。我想，你知道，我有一些初步的数据，看起来不错。因为如果你想一想，我们与之竞争的基线基本上是人们以随机的顺序运行所有的测试，因此，从字面上看，你不能做得比这更差。因此，作为一名开发人员，我本能地知道某些测试是为了在某些特定的事情上捕捉某些程序而设计的。

所以，真的，唯一的问题是机器学习模型可以在多大数量的数据上学习这些东西。随着时间的推移，我想我肯定会变得更好。我不知道我们到底能创造出什么样的影响或者什么样的产品，但是总的来说，我感觉很有信心。你知道，它只需要足够好，开始产生影响，它只会从那里上升。

哈普瑞特，对你来说成功是什么样子的？

辛格:嗯，在我们筹集资金的时候，有人问过我们这个问题。我喜欢从——所以，我们以前做过这个。我们帮助公司获得成功。对我来说，实际上是为客户解决一个问题。

因此，如果你能够在任何地方获得并解决软件团队的问题，首先将他们的产品送到客户手中——这对我来说就是成功。我知道这不是典型的硅谷 1 亿到 2 亿的 arr。我们不在那里。这不是我的想法。它真的帮助了那些为交付软件而奋斗的人们。

**Shimel:** 明白了。K.K？

川口:所以，你知道—

**Shimel:** 你呢？

**川口:**有一次我在旧金山机场工作，你知道，有人在我后面工作，她说，“哦，你有詹金斯的东西。真好。在哪里可以得到？”对吗？对我来说，这就是成功。所以，这将是一个很难再被打败的对手，但是你知道，我觉得值得一试。

我的意思是，这是一种——我想我认为这是一种迹象，表明你对世界和一些人产生了足够大的影响，并以相当深刻的方式感动了一些人。对我来说，这就是成功。这就是我渴望的，是的。

希梅尔:好的。让我——让我把你的双脚放在火上一点。所以，你现在启动了，这是——你知道，它在外面，网站在 Launchable Inc .外面，那是 L-A-U-N-C-H-A-B-L-E-I-N-C . com，对吗？人们什么时候可能希望看到测试版？你认为你什么时候能推出人们可以真正开始使用的东西？

辛格:你真的让我们陷入困境，对吗？

**川口:** *【笑声】*

Singh: 这里有一名产品经理和一名工程师。我希望我的工程主管给我交付日期。*【笑声】*

你知道吗？经典。你会做一个*【相声】*。

**辛格:**小子，你和我站在同一边，在这里。

**Shimel:** 这是一个伟大的 CEO 举措。

**辛格:** *【笑声】*

好吧，联合首席执行官先生，他把你丢下了。你怎么想呢?

**Singh:** 玩笑归玩笑，我认为我们目前正在做的事情之一是，我们正在积极地与潜在客户和客户交谈。我们多年来学到的一个教训是，不要在真空中制造产品，然后希望我们已经解决了问题。

所以，我们实际上——我们的网站上实际上有一个测试版邀请列表按钮。我们寻找的实际上是合作伙伴，他们可以和我们一起，告诉我们是否正在解决正确的问题，并与我们一起解决正确的问题，对吗？这就是我们今天的处境。我就说到这里，我会把日期告诉你。

川口:是的，正如我提到的，我们有初步的数字。我们制作了一些模型，产生了一些影响，现在我真正希望找到的是活动合作伙伴，我们可以在他们的系统、项目和源代码中应用相同的技术，看看它会产生什么样的影响。然后，这是——你知道，这可能是那些愿意与我们密切合作的团队的基础，而且——

辛格:这是你能分享的初步数据吗？

**川口:**是啊。所以，我的意思是，不能保证它适用于你的系统。但是，举例来说，虽然我能够做到这一点，但选择 10%的子集用于最佳情况，它将立即捕获大约 40%的 ____。所以，我想，你知道，那是——是的，对我来说，那是一个非常有希望的数字，你只能从这里向上，所以。

**希梅尔:**优秀。所以，你看，你们两个已经获得了大量的善意，不仅在你的同龄人中，正如天使投资人所证明的，你知道，在这里的投资者名单中，而且在整个社区中，还有 k . k——我的意思是，不用说在詹金斯社区中有多受尊重，我不想用“受崇拜”这个词，那会冲昏你的头脑，*【笑声】*但是你知道，你在社区中有多荣幸。

什么，人们可能从社区听，他们能做些什么来帮助，在这里？

川口:是的，我认为给我们反馈可能是最重要的。你知道，我们正在做一些我们认为非常令人兴奋的事情，然后我们希望听到这些，或者如果不是这样，那么听到这些也很好。因此，到目前为止，我们与对这一领域感兴趣并正在考虑这一领域的人进行的对话非常有价值。

所以，如果—你知道，如果你觉得我们在这里讨论的是你和你的挑战，我们希望听到你的意见。此外，我们正在招聘——眨眼，眨眼。所以你知道。*【笑声】*

每个人都在招聘。

川口:对，所以如果你-

好的。网站上有吗？

**川口:**正是。你知道，我对 CloudBees 和 Jenkins 更有热情的一件事就是把它传递给下一批人，对吗？我觉得我从与初级工程师和同事的交谈中获得了更多的乐趣，我们指导他们。所以，我觉得我们可以提供什么——我知道 Harpreet 也是如此，所以我觉得我们现在有一个难以置信的工作机会，你知道，和这些人并肩坐在一起，你知道，像我们这样的人，我认为他们有创造力。我们也热衷于指导他人。所以，你知道，我想如果它听起来像你的那杯茶，那么…

辛格:我马上就去。所以，我认为，CloudBees 是一家非常棒的公司。艾伦，你了解沙夏，他是一个伟大的领导者。他建立了一个了不起的公司。因此，我们学到了很多关于成为一家好公司意味着什么的好经验。

然后我去了 Atlassian，在那里，你知道，我从 Scott Farquhar 和其他人那里学到了同样的东西，我们试图把这两家公司的所有优点都带到这家公司，对吗？我们有点受价值观驱动。我们真的认真考虑过我们想要建立的公司，我们想要在世界上产生的影响，我们正在寻找分享这种使命感的人，对吧，加入我们的团队，对吗？如果你能在我们的团队中找到这样的人，那就太好了。

在房子的前一面，我们再次寻求为顾客解决问题。我们不希望在真空中这样做。所以，一般来说，人们会说，“是的，我听说了。我希望我能和某人合作，帮你定义什么——帮我解决这个问题。”如果你是那个人，我们很想和你谈谈，我们很想和你一起经历这些事情。

**希梅尔:**妙极了。伙计们，我们已经超时了。我答应给你 15 分钟。我们可能会在半小时后到达。我道歉。

但是让我以这样一句话来结束我的演讲——你知道吗？恭喜你。有人曾告诉我，新公司就像船——最好的日子是你第一次得到它们和卖掉它们的日子。*【笑声】*不过话虽如此，驾驶它们也很有趣。所以，享受航行吧，伙计们——改变世界。当然，如果有任何事情，我们可以在 MediaOps 这里做，你知道你可以指望它。我想不出有两个人比我更适合这个新的冒险和接受这个挑战。

Harpreet Singh，k . k .——launch able 的联合创始人和联合首席执行官，你可以在 Launchable Inc .找到更多信息。这是艾伦·希梅尔为[DevOps.com](https://devops.com/)带来的报道。您刚刚听到了另一个 DevOps 聊天。

— [Alan Shimel](https://devops.com/author/ashimmy/)