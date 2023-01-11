# DevOps 聊天:IBM z14，与 Hayden Lindsey 一起为 DevOps 从头开始构建

> 原文：<https://devops.com/devops-chat-z14-built-devops-ground-w-hayden-lindsey/>

IBM 最近发布了可能是近十年或更长时间以来最大的 zSystems 大型机版本。IBM 的 z14 大型机也是为支持 DevOps 而从头开始设计的。从 API 和其他集成到语言支持，z14 是 IBM 有史以来最先进的大型机。我有机会与 IBM devo PS 企业系统副总裁 Hayden Lindsey 谈论 z14。

海登向我们介绍了 z14 是如何在混合动力环境中工作的。它还可以很好地与现代 CI/CD 工具(如 Urban Code 等)配合使用。此外，API 使 it 能够集成许多不同的环境、工具和应用。它确实是今天和未来的大型机。海登很好地描述了这一切。

像往常一样，下面是我们谈话的音频流，后面是我们谈话的文字记录。尽情享受吧！

## 声音的

[https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/tracks/342499028&color=%23ff5500&auto_play=false&hide_related=false&show_comments=true&show_user=true&show_reposts=false](https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/tracks/342499028&color=%23ff5500&auto_play=false&hide_related=false&show_comments=true&show_user=true&show_reposts=false)

## 副本

***海登卟**

*海登卟，副总裁&杰出工程师——企业系统开发工程师。Hayden 负责该产品组合的开发、产品管理、销售支持和服务。他在 IBM 工作了 28 年，担任过各种职务，包括软件开发人员、产品架构师、产品经理、Eclipse 工具平台的联合领导，以及 WebSphere Studio/Rational 建模和构造工具的主管。他拥有北卡罗来纳大学教堂山分校的数学科学学士学位。*T17

*

艾伦·希梅尔:大家好，我是 DevOps.com 的艾伦·希梅尔，来参加另一个 DevOps 聊天*。*本期聊天的嘉宾是我们的好朋友，IBM 企业开发副总裁海登·林赛。嗨，海登，欢迎来到 DevOps 聊天。

海登·林赛:嗨，艾伦。很高兴再次和你在一起。

很高兴你能来这里。海登，这是个大日子——对 IBM 企业团队的人来说是个大日子。现在 z14 已经上市了，不是吗？

琳赛:的确是。是的，我们早在 7 月中旬就宣布了这一点，现在我们已经开始提供我们的产品。上周晚些时候，我的很多产品都已上市，现在，这个盒子本身也上市了。所以——重要的一天。

**希梅尔:**妙极了。海登，只是——你知道，我们的观众太专注于 DevOps，他们可能没有意识到 z14 发布的全部内容。它是什么，它是硬件的组合—正如您提到的，是一个新的盒子。有一大堆软件，有一种整合的基调——里面塞满了各种各样的好东西。你能给我们一个大概的 z14 的范围吗？

**琳赛:**当然。我认为你所看到的是将软件，包括中间件和工具，从我们曾经拥有的各个部门，如 Rational 和 WebSphere，转移到一个单一的 z 或大型机品牌的结果。

因此，与大多数以前的硬件版本相比，你会听到速度和馈送，你知道，z13 拥有地球上最快的处理器，这一次，重点更多地放在涉及硬件以及软件和工具的整个解决方案上。所以我认为——我们致力于此，我们进行设计思考，我们有赞助商用户，我们完成了从硬件到操作系统、中间件和工具的整个九个方面，我认为这产生了很大的影响。

例如，这一次，我们有了一种叫做普遍加密的东西。我们都知道安全性有多重要，我们都听说过正在发生的这些违规事件——Experion 是最多的，Equifax 是最新的一个。而且，在所有被盗的记录中，我认为自 2013 年以来大约有 90 亿份，其中只有 4%被加密。这款新的大型机让您可以对 100%的数据进行加密，而不会影响性能。这只是一个例子。很明显，这里有硬件的东西，但是也有中间件必须参与到这个解决方案中。这是一个例子，真的很酷。

海登，这其实是一个很大的例子，因为你知道吗？加密已经存在—我的意思是，我在安全领域工作了 20 年，加密已经存在了大部分时间。问题是，当您加密，然后必须解密和重新加密时，性能会受到影响，而且—

Lindsey: 程序员不得不这么做。*【笑声】*或者数据库管理员必须为数据库设置它，但是当它在应用程序中被使用时呢？这就是我们正在解决的问题，人们不会受到时间的限制，也不会因系统不可用而影响性能。

所以，我认为这对于全世界处理敏感数据的公司和政府机构来说是一个突破。

当然，我们现在都这么做了。海登，你说了一些我想重点关注的东西，那就是离开速度和馈送，如果你愿意的话，衡量任何东西的价值的指标。我曾经和一个女人一起工作过，她称之为潜水。对吗？你知道，当你开始进入速度和饲料，以显示你的产品的价值，你潜入你的包，而不是谈论真正的价值。

**卟:**对。

**Shimel:** 所以，我很高兴看到这是 IBM 正在走的道路，谈论价值，但我也认为这是因为，正如你所说，这里加入了太多东西，对，从围绕整个版本的设计思想，如果你愿意，到与云等东西的集成，与 IBM 和其他人开发的 DevOps 整套工具集和方法。

这不仅仅是“哦，我们把——这是下一代处理器更快的 iPhone。”这不是下一个处理器更快的 z，远不止如此。我想我——也许你早些时候说过，或者我们私下谈过。这可能是 z 至少十年来最具实质性的一次发布。

**Lindsey:** 我认为是的，当然，市场会告诉我们我们的愿望是否会实现，但我当然认为加密元素只是——嗯，我认为它是非凡的，它可能对几乎任何公司都非常、非常、非常重要。

然后我们有了更多的机器学习和分析，这样你就可以在交易分析中做，而不是在事后做，不得不试图退出或只是注销欺诈性交易。当然，我们已经用 DevOps 组合编译器做了很多工作。但是我真的认为，也许，自从我们把 Linux 放在这个平台上，它就那么重要了。

**Shimel:** 哇。巨大的。所以，海登，我们是关于 DevOps 在这里，所以让我们集中一点点。我的意思是，其中一个好处是，我看到了一些关于如何将新型 z14s 与 IBM Enterprise DevOps 解决方案结合使用的简介，我不想使用术语“双峰多速”这样的废话。利用将您的 z 系统与云系统集成到一个连贯的业务战略中。听起来怎么样？*【笑声】*那么，谈谈吧。

**Lindsey:** 是的，所以这次发布的三个主题之一是开放和连接，这显然与混合云战略有关。它与数字经济或数字转型紧密相连。它与 API 经济性密切相关—无论您想从哪个角度看，您都必须能够让数据驻留在大型机中，据估计，世界上大约 80%的企业数据驻留在大型机中并由大型机管理，大约 70%的业务事务也是如此。

所以，如果你想的话，可以把它应用到你的新 iPhone X 应用上，就像我们昨天看到的那样——你知道，或者 10 或者其他他们会叫它什么的。

**Shimel:** 嗯嗯。是的，他们称之为 10。

琳赛:他们用罗马数字称之为 10。

希梅尔:是啊。

**Lindsey:** 但是，你知道，如果你要这么做，你必须让访问数据和交易变得容易，找到那些交易，理解它们，因为很有可能，它们是由某个人写的，这个人已经不在了，或者已经转到了其他工作岗位。因此，你需要一些工具，使 API 的启用、开放和连接到大型机变得简单而高效，就像你在 Linux 平台上开放某些东西一样简单而高效——当然，你也可以在 z 上使用 Linux——或者使用 Windows box 或其他任何东西。因此，我们必须让 z 参与更广泛的数字经济，即 API 经济，这也是我的团队和 IBM 的其他团队一直关注的问题。

Shimel: 当然可以。所以，现在，海登，在同样的情况下，你知道，仍然有大型机的态度，你知道，我们不开放我们的大型机对所有这些 API，也许我们不想挂钩到我们的参与系统，你知道，在云上或你有什么。

对于在那里收听的客户来说——我们的许多听众是企业级的，他们在企业级组织中工作——他们真正考虑向你所说的 API 经济开放他们的大型机有多重要？

**Lindsey:** 当然，我越来越认为，IT 和业务线高管，也就是我与之共事的客户，正在意识到他们拥有巨大的资产，如果他们能够提供这些资产，他们就可以利用这些资产。没人——至少我所知的公司或政府机构没有资源从头开始重建一切。我认为，如果你回顾一下在 SOA 时代分析师们所说的话，他们说，你知道，利用已经存在的东西来创建一个服务比从头开始创建它要快 5 倍，更不用说，如果它已经工作了，你还可能有更高的质量。我认为完全相同的分析将被证明是正确的，因为我们现在谈论的更多的是 RESTful APIs。

所以，我认为越来越多的客户意识到他们需要展示这种价值。关键是，当你有——你知道，估计有 250，000，000，000 行 COBOL，更不用说 PL/I 和汇编程序和 4gl 等等时，这有时会令人望而生畏。它让你拥抱那些可能是以一种更加单一的、结构不太好的方式创建的应用程序。你需要进行重构。您需要发现那里有什么，然后制定一个实现 API 的计划。

但我认为人们知道他们需要这样做，只是有时这被视为一项艰巨的任务，他们必须想出如何开始，我们推出了一种称为数字化转型模型的东西，以帮助我们的客户制定计划。

**Shimel:** 明白了，我同意。所以，你只是为我在这里的下一件事情做准备，但是——所以，这是我们在 DevOps.com 听到的最大的问题，海登，这是——嘿，这一切都很棒。我们如何开始？我们该怎么做？我如何获得高管的认可？我们如何——有一个，两个，三个吗？有我能遵循的蓝图吗？

那么，z14，让我把它扔给你——我们从哪里开始？他们是如何带着这个移动的？他们是如何——具体来说，他们是如何开始将 DevOps 和 API 融入其中的？

**Lindsey:** 是的，这是我几乎从每个交谈过的客户那里听到的问题，我正准备下周去欧洲旅行，我确信它会出现在每一次会议上。事实是，每个顾客都是不同的，所以没有唯一的答案。而且，在任何给定的客户中，他们的应用程序涵盖了从接近生命周期的应用程序到正在开发或全新开发的应用程序。所以，我们已经——但是，当然，客户端和应用程序类型之间存在模式和相似性，并且存在我们多年来通过与客户端合作收集的最佳实践，这就是我提到的称为数字化转型模型的东西。

我们已经转向这种与客户合作的方式，将重点放在应用程序上，而不是企业的一个答案上——嘿，你应该从部署自动化开始，或者你应该从测试自动化开始。这个答案不应该是企业的答案，而应该是针对这一套应用程序的，因为它们的当前状态、现状以及您希望的未来状态是什么。如果您只是需要高效运行的产品，并且您打算在几年后更换或淘汰它，那么您希望它能够高效运行。

所以，使用我们最新的编译器，但你知道，事实是，投入一个全自动的管道可能是一种浪费。然而，在光谱的另一端，对于处于非常活跃的开发中的事物，那是你想要最充分地进行 DevOps 的地方，实际上，这只是你采取什么步骤到达那里的问题。

所以，我们提出的这个模型有四个层次——我描述的第一个层次，只是编译，运行——只是运行它。高效运行就好。下一步是维护，下一步是暴露，下一步是进化。所以，我的意思是，我不知道我们是否有世界上最好的名字，但事实是，对于业务来说，您确实需要考虑，对于给定的应用程序或应用程序套件，您需要多大程度的 DevOps 采用。所以，我认为这是我们今年对客户使用的更现实的答案，也是我们使用的不同于往年的工具。

**希梅尔:**优秀。所以，海登，我的意思是，为了说明这一点，我记得去年在互连，你知道，我们有整个小 DevOps 电视展位，我采访了一些 IBM 客户。其中一家是银行，我忘了他们现在是来自波兰还是荷兰，或者甚至是澳大利亚。他们是 IBM 的 z 系统客户，我想说，他们刚刚从 COBOL 4 升级到 5——可能是 5 到 6，我现在记不清了。

但是他们刚刚更新了他们的 COBOL 版本，这在性能方面给他们带来了巨大的变化

琳赛:是啊。是啊，没错。你知道，我们——我们的编译器团队每发布一个版本都会做的事情之一，从最早的时候开始，我们就在想象新的大型机或新的 power 平台会是什么样子。我们与硬件人员携手合作。

而且，你知道，特别是对于 COBOL，世界上大约 70%的商业交易都在运行 COBOL，显然，性能很重要，所以这是你可以了解一些信息和速度的地方。主要是因为，而不是因为——有些数字并不惊人，但这是因为你可以更好地响应你的客户。但对于一些计算密集型应用程序，它们在最新的编译器上运行速度提高了 16 倍，而不是%倍，这是 6.2 倍，而 4.2 倍可能是该客户端的来源。所以，我们跳过了第 5 版，但我们的大多数客户仍然使用 4.2 版。

所以，速度非常快，但这是通过联合开发实现的。你知道，如果你在硬件中加入新的指令或新的向量支持，而编译器没有生成这些新的指令，那么很明显，没有客户能够利用它，除非他们想写自己的汇编程序。所以，你知道，我们的编译器提供了巨大的价值，我给了你一个 COBOL 的例子，但你可以用 PL/I 和我们的自动二进制优化器得到类似的结果，它基本上只是做，试图做编译器做的工作，但只是在二进制上工作，而不是让你回到源代码。

所以，这是件大事。你知道，越少——可能越平凡。是的，那东西跑得更快，就像你说的，跳进袋子里。*【笑声】*但是，你知道，当你有 16X 或 5X 或诸如此类的数字时，那是巨大的。

Shimel: 没错，没错。所以，海登，你知道，我也提到了互连，因为我们的时间不多了，我想快速提示你一下，让我们的听众现在。

因此，今年，互连是 IBM 举办的一个更大的统一会议的一部分，该会议名为 Think—Think 2018，我相信它的名称是 Think 2018，如果我没有弄错的话，它是三月。

**琳赛:**是的。

希梅尔:请讲。

琳赛:你可能会看到一种趋势。*【笑声】*因为，你知道，互联是冲击和创新的结合。创新——我想这就是它的名字。我有点忘记了，但是不管怎样，我们有一个 Rational 会议，我们有一个 WebSphere 会议，我们有物联网的东西等等。现在我们将它们结合成互连——至少是 WebSphere 和 Rational 的东西。它变得越来越大，现在我们正在做一些或多或少在 IBM 范围内的事情，它被称为 Think。将于 3 月 19 日在拉斯维加斯的曼德勒湾举行，所以像我们最近的其他会议一样，仍然在拉斯维加斯举行。

因此，我认为有一个更广泛的有利和不利因素，在那里我们可以讲述完整的 IBM 故事，这是重点，而且你有来自全国所有不同地区的中小企业，无论是云、认知、Zpower 等等。但我认为这很好，但因为你确实有这些专家，我们将在特定领域举行分组会议或主题会议，无论是 DevOps 或 z，还是编译器或 UrbanCode 等部署自动化。

因此，仍然会有这些专业会议，但你得到了大的图片。我想问各位听众的一件事是，论文征集是公开的，你知道，我们争取在各种途径中进行 100%的会谈，要么仅作为客户或合作伙伴，要么作为客户和/或与 IBM-er 共同合作的合作伙伴，但我们真的想摆脱 IBM-er 在没有合作伙伴或客户在场的情况下讲故事，讲述他们在现实生活中使用给定领域的给定解决方案所做的事情。

所以，我们真的希望有尽可能多的合作伙伴和客户提名。

Shimel: 我喜欢这个主意。你知道，我在过去的两年里分享了一个小组，海登，关于 Dev——我想他们是在 DevOps 和 SecOps 上。但是，你知道，我真的很努力地去平衡——是的，我们有一个来自 IBM 的人，但我们也有一个分析师，然后我们有一个合作伙伴，然后是一个从业者。我认为这种平衡让它，让它—

**Lindsey:** 它为整个事情和不同的视角增加了一些合法性。

是的。很快的，如果你去了 IBM.com/events/Think,，你可以得到所有的独家新闻，然后点击链接提交。正如海登所说，如果你有话要说并与人分享，它——参加过三四次或更多，这是一个很好的平台。所以，我鼓励每一个想参与的人都这样做。即使你不想说，但如果你想去真正了解正在发生的事情，无论是沃森或 z 系统或混合云或 Bluemix 或任何这些事情。你知道，如果这些对你来说很重要，我认为这是一个很好的节目。

海登，我们快没时间了——我们实际上是超时了，但没关系。非常感谢您在繁忙的一天抽出时间与 z14 的通用 GA 在一起。祝你好运。让我们看看，我不知道，也许在年底之前，市场对这些特性和功能的反应如何，我们将看到橡胶在哪里遇到了困难。

听起来不错，艾伦，再次感谢你抽出时间。

**Shimel:** 感谢您的宝贵时间。企业副总裁 Hayden Lindsey 在 z Systems z14 发布日与 IBM 合作。谢谢，海登，祝你愉快。

好的。再见了。

席梅尔:我是艾伦，谢谢你。我是 DevOps.com 的艾伦·希梅尔。我们将在下一次 DevOps 聊天中再见。

— [Alan Shimel](https://devops.com/author/ashimmy/)