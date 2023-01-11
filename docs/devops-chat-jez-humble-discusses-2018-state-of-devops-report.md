# DevOps 聊天:Jez Humble 讨论 2018 年“DevOps 报告状态”

> 原文：<https://devops.com/devops-chat-jez-humble-discusses-2018-state-of-devops-report/>

朵拉每年的“发展状况报告”是我每年都期待的。没有其他报告能像这份报告一样给我们提供对这个行业的看法和见解。我知道我并不孤单。这就是为什么与 DORA——DevOps 研究和评估部门——的一位同事谈论“devo PS 报告状况”并获得一些真正的收获总是一件乐事。

在这次 DevOps 聊天中，我和 DORA 的首席技术官兼联合创始人 Jez Humble 谈论了今年“加速 DevOps 报告状态”中的一些发现——一个新名称，但同样有价值的信息。

像往常一样，下面是流媒体音频，然后是我们的谈话记录。

[https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/tracks/507902631&color=%23ff5500&auto_play=false&hide_related=false&show_comments=true&show_user=true&show_reposts=false&show_teaser=true](https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/tracks/507902631&color=%23ff5500&auto_play=false&hide_related=false&show_comments=true&show_user=true&show_reposts=false&show_teaser=true)

艾伦·希梅尔:大家好。我是艾伦·希梅尔，DevOps.com，您正在收听的是另一个 DevOps 聊天。今天的 DevOps 聊天是我每年都期待的一次，也是我们谈论最新的“DevOps 报告状态”的一次帮助我，或者实际上是我们今年的“DevOps 报告状态”审查的嘉宾和明星，不是别人，正是 Jez Humble，DORA、DevOps 研究和评估的联合创始人兼首席技术官，也是 DevOps 的全能伙计和交谈的好对象。Jez，欢迎来到 DevOps 聊天。

艾伦，非常感谢你邀请我。总是很荣幸。

**Shimel:** 谢谢。Jez，你知道，你们，Nicole，你和 Gene 以及团队的其他成员在今年的“DevOps 报告”中做了另一项出色的工作。今年它的命名有点不同。它实际上是——如果我搞砸了，纠正我——“加速 DevOps 报告的状态”？

**卑微:**对，没错。这是今年的“加速 DevOps 报告状态”,但继续了与往年相同的严格研究，并在这一次扩展了一些令人兴奋的新发现。

希梅尔:是啊。我要提到的另一件事是，让我们早点说清楚，今年的报告钻石赞助商是谷歌云，对吗？

**谦逊:**对，没错。我们也有 15 个金牌赞助商，但我们今年的主要合作是与谷歌云。没错，谢谢。

**希梅尔:**妙极了。好了，现在我们已经把广告搞定了，Jez，让我们开始吧。这是你们做 DevOps 报告的第五年还是第六年了？

是的，这是多拉第五年参与或领导 DevOps 报告的研究了。没错。

**Shimel:** 所以，你知道，当我们从那个角度来看时，你知道，事后来看，确实有大量的数据需要挖掘，但让我们专注于今年的报告，Jez。让我们从你对我们听众的看法开始，你认为他们最大的收获是什么？

**huble:**所以，正如你所说，这是同类研究中最大的研究项目，研究 DevOps 意味着什么，为什么它很重要，以及预测你快速稳定交付能力的因素。你可能会想，你知道，这是我们做这项工作的第五年了，我们已经没有什么可谈的了。绝对不是这样的。这是迄今为止最大最全面的一次。我认为一些大的外卖。

第一，我们再次发现我们对软件交付性能的度量仍然有效。那就是看速度和稳定性。我们再次发现，高绩效者并没有在两者之间进行权衡。他们实际上提高了交付过程的速度和稳定性。我们还将这一衡量标准扩展到了可用性方面。所以可用性就是生产中的可用性。这是对运营绩效的一种衡量。因为我们也在关注这一点，所以我们现在讨论软件交付和操作性能。因此，我们涵盖了从开发到生产运营的整个交付生命周期。同样，我们发现高绩效者不会在这方面做出取舍。他们还实现了高水平的吞吐量、稳定性和可用性。

我们还研究了推动高性能的关键技术实践，今年我们进一步研究了监控和可观察性，以了解持续测试的影响、数据库变更管理以及不断变化的网络安全性。我们也更深入地研究了文化。我们已经研究了塑造文化以提高绩效的管理实践。今年，我们还探讨了领导者通过给予团队自主权和建立信任来影响文化的作用。我们发现，通过回顾学习回顾促进文化学习对文化有影响。表现最好的人有 1.5 倍的可能性坚持进行回顾，并利用它们来改进他们的工作，这是至关重要的。

我们还研究了云基础设施。许多人正在转向云计算。这是非常热门的，它已经在许多不同的行业中被广泛采用，但我们发现如何做很重要。现在，美国国家科学技术研究所(National Institute of Science and Technology)对云基础设施有了一个定义，他们谈到了您必须实施的五项基本功能，比如按需自助服务，客户可以通过这种服务单方面调配云资源。我们发现，高绩效员工使用 NIST 所说的五个基本特征的可能性是普通员工的 23 倍。因此，有很多人在使用云，但实际上并没有实施这些功能。这是个问题。你如何做这些事很重要。只是把你的东西放在云中，假装它是一个数据中心，实际上是行不通的。您还需要实际使用云提供的功能。

我们发现使用开源软件可以提高性能。最后，再一次，我们证明了工业并不重要。我们在所有不同的市场群体、所有不同的行业中发现了高表现者，无论是金融服务、医疗保健还是其他高度监管的群体，以及低表现群体中的初创公司和小公司。所以任何人都可以做这个东西。

绝对的。*【清嗓子】*你知道，Jez，我觉得这并不令人欣慰，但我们听到你谈论，你谈论，嗯，正在向云迁移的公司等等。你知道，我想大概是在 2005 年左右，突然之间，云真的开始出现了，现在我们已经发展了 13 年，可能 15 年了，你知道，这就像是，我们什么时候才能真正看到——我们是否正处于——这当然是主流，但我们是否已经看到——我们在云迁移中处于什么位置，这将如何影响我们？像是大部分已经发生了还是大部分就在我们面前？

**卑微:**是啊。我的意思是，这是一个很好的问题，我认为我们在 DevOps 和持续交付方面也看到了同样的趋势。人们说他们在做，问题是他们真的在做吗，因为每个人都想做，然后说他们完成了，下一件大事是什么？我的意思是，如果我们看看我们的数据，我们看到 17%的受访者根本没有使用云，其余 83%的受访者使用云，其中 40%使用多家云提供商。但是如果我们看看谁实际上做得对，只有很少一部分人说他们实际上在做。22%的受访者表示他们符合所有这些基本特征。所以我想说还有一段路要走。我的意思是，这是字面上的帕累托原则，对不对？百分之八十的人都在做；只有 22%的人做对了。

所以我认为所有这些东西都有一条长尾巴。无论是采用 DevOps，还是采用云，我们都在不断学习。改变需要时间。很难。要做好这件事，你需要——这在技术和开发人员中也很普遍——你需要改变做事的方式。你需要改变你的做法。你需要改变你的流程。这很难，也是需要时间的部分。很复杂。人们非常热衷于采用新技术，你知道，Kubernetes，Docker，Cloudstaff，他们采用了它；但是改变他们的流程和实践，这是一项艰巨的工作；但这也是重要的工作。我们在研究中非常清楚地看到了这一点。

希梅尔:是啊，是啊。你是对的。我的意思是，我经常认为，DevOps 和我们在过去十年中看到的许多大趋势之间存在先有鸡还是先有蛋的关系，这些大趋势包括云和无处不在的连接，以及向移动和应用程序驱动的 IT 世界的转移。我不知道，你知道，如果没有包括 DevOps 在内的任何其他事情，这些事情中的任何一件都会发生，坦率地说，这使得它变得如此重要。那么 Jez，当我们从历史的角度来看今年的调查结果与前几年相比，有没有任何异常，有没有任何突出的迹象表明，天哪，这似乎与前几年不同，这似乎不是沿着我们前几年看到的那条轨道前进？

**谦逊:**是啊，很棒的问题。这么几件事。首先，我们有一个新的高性能组，精英演员。因此，在过去的几年里，我们的聚类分析表明，有三个组——高绩效、中等绩效和低绩效。因此，当我们今年进行聚类分析时，我们发现了几个有趣的趋势。因此，首先，我们有一个精英性能组，这表明该行业继续改善其软件开发和交付实践。

我们的高绩效团队在受访者中的比例有所增长，这表明高绩效对于行业中的许多团队来说都是可以实现的，而不仅仅是为具有独特特征的团队保留的。因此，高水平的执行者继续以最高水平交付和操作软件，但卓越的标准在整个行业中继续发展，第四组执行者，精英执行者仍在优化和变得更好。这就是我们普遍看到的情况。最好的组织是那些不断努力变得更好并且永不满足的组织。

我们在聚类分析中看到的另一个有趣的趋势是，我们发现了一个小群体，大约 7%我们称之为被误导的执行者。所以被误导的表演者也很有趣。所以这是一个基本上为慢行而优化的团队。他们做出了安全的选择，但他们付出了非常昂贵的代价。所以他们采取了这种非常谨慎的方法，他们希望不频繁地发布，他们认为这是一种有效的策略，并且在部署之间有额外的时间进行测试和质量检查，但他们报告说，当出现中断时，恢复服务需要很长时间，例如几个月甚至几个月的时间，这是一个巨大的问题。

因此，我们的研究表明，进行大批量、不频繁的更改会给部署过程带来风险；在复杂系统中，失败是不可避免的；当大故障确实发生时，当试图理解故障或者当处理整个系统的灾难性或连锁故障时，这些大批量变化会增加复杂性。抱歉，5%的团队正在这样做，并看到了后果。这些是我们在今年的数据中看到的一些有趣的事情。

绝对的。所以你知道，Jez，当然自从 DORA 成立，创建和推出以来，调查就没有承担更大的使命，但它与 DORA 本身的工作密切相关，对，在很大程度上。我不知道我们的观众是否——我想他们多年来一直在阅读这项调查。他们可能听说过朵拉。他们认识妮可。他们认识你。他们当然知道吉恩。但是把它摆出来。为我们把这些点联系起来。调查是如何进行的，不管是手挽手还是手牵手，多拉和它的使命。

**卑微:**是的。所以我们的使命，作为 DORA，DevOps Research and Assessment，我们的使命是帮助行业在软件交付方面创造卓越。我们真的想帮助组织变得更好。我们有一个产品。我们的产品是一个评估工具，可以帮助你看到你做得如何，以及在你变得更好的能力方面有哪些限制。现在有很多评估产品。我们真的想用科学的方法来解决这个问题。四年来我一直在做这件事，之前是在 Puppet，现在是在 Nicole 领导的 Google——Nicole 是一名学者。她是终身教授。从学术角度来看，她有很长的研究背景。她真的找到了一种方法，以科学的学术严谨的方式来解决什么是重要的。

我们所做的所有这些研究实际上让我们可以说，这就是你如何衡量绩效，这就是我们如何证明它对你所关心的组织成果有影响，这就是预测你利用速度和稳定性的能力的东西，这是技术、文化和基于过程的能力的结合。所以我们可以说这些事情真的很重要。所以这里有一些重要的事情。这是你衡量它们的方法。这里是它们如何影响你的软件交付性能，这里是它们如何预测组织的性能。所以这实际上是关于采取科学的方法来衡量这些东西并加以改进。

实际上，今年我们出了一本书，“加速”，这本书谈到了那个研究项目和我们在过去四年做那个项目中发现的结果。所以这是关于采取基于科学研究的方法来提高交付软件的技术能力。

绝对的。绝对的。Jez，信不信由你，我们已经快没时间了。正如我提到的，它走得很快。但是我想为那些不明白的人多做一些关于朵拉的事情。我知道你在公开场合工作过——我想已经宣布 DORA 在其他企业中与 Capital One 合作过。再次向我们的观众介绍一下多拉的使命，以及你如何帮助那里的公司。

**卑微:**是啊。嗯，我的意思是非常感谢给我机会谈论这个。我们有很多公司是我们的客户，他们来自各种行业，包括非常大的、高度监管的行业，包括金融和政府，他们对如何变得更好感兴趣。我们基本上应用我们在过去几年中收集的研究，帮助他们了解是什么在阻碍他们，他们的限制是什么，然后如何以研究数据库的方式实际改善这一点。

所以这是一个适用于任何地方的东西。这是可以应用的东西——这项研究的伟大之处之一是它表明任何人都可以做这件事。所以这适用于任何地方。你知道，我经常听到人们说，“你知道，好吧，我们不能这样做。这在这里行不通。DevOps，无论什么云，连续交付，听起来很棒，在这里行不通。”我们真的可以进来说，“嗯，实际上，你知道，事实并非如此。任何人都可以变得更好，这里的数据显示，不同行业、不同规模的人都可以变得更好。”同样，我们已经能够帮助公司找到他们的位置，找出他们的限制，并了解如何改进。

从这个角度来看，这是非常有帮助的，不仅仅是——这是一个关于在 DORA 工作的很好的想法，我喜欢的是，它不仅是基于科学和研究的，它也是务实和实用的，它对寻求改善其软件和开发能力的公司具有真正的影响。因此，不仅能够做研究，还能够将其应用于实践，这真的是一件非常愉快和有趣的事情。对我来说，能够以这种方式应用它是一种真正的特权。

绝对的。嗯，Jez，你知道，我期待着与 DORA 继续取得成功，哦，我的上帝，我忘了说，Jez，如果人们想下载报告，他们可以去哪里获得它？

**卑微:**是的，太感谢了。这是一个非常好的问题。所以你可以去我们的网站。DevOps-research.com。如果你去研究，它在头版。在我们的研究页面上。从 Google Cloud 下载报告的链接。您也可以前往 bit.ly/2018-devops-report.，直接进入注册页面，下载报告。还需要提醒的是，我们已经讨论了过去四年的研究以及我们在*加速*中的研究计划，这本书是我们今年早些时候出版的。但是是的，请去看看报告。显然，我们在这次讨论中只能触及冰山一角。如果我自己说的话，那里有很多非常有趣的东西。所以我鼓励你去下载并检查它。

绝对的。好吧，杰兹·汉布尔，我的朋友，很高兴你能来我们的节目。非常感谢你做这个报告。持续的成功。向 Nicole 博士和 Gene 以及其他成员问好，我们将很快让您再次参与 DevOps 聊天。

非常感谢，艾伦。总是很高兴。谢谢你。

我的荣幸。我是 DevOps.com 的艾伦·希梅尔。您刚刚听到了另一个聊天。祝大家有美好的一天。

— [Alan Shimel](https://devops.com/author/ashimmy/)