# 通过 Lightstep 事件响应，Lightstep 超越了可观察性–tech strong 电视

> 原文：<https://devops.com/lightstep-extending-beyond-observability-with-lightstep-incident-response-techstrong-tv/>

本·西格曼和 RJ·杰恩德拉讨论 ServiceNow 的最新公告，即 Lightstep 正在超越[的可观察性](https://devops.com/?s=observability&sort=newest)，并随着 [Lightstep 事件响应](https://lightstep.com/)的全面上市，为应用程序开发创建差异化的产品组合，帮助组织的数字产品和服务变得更加可靠和有弹性。下面是视频，后面是对话的文字记录。

[https://player.vimeo.com/video/685155661?h=270785fba2&badge=0&autopause=0&player_id=0&app_id=58479](https://player.vimeo.com/video/685155661?h=270785fba2&badge=0&autopause=0&player_id=0&app_id=58479) 

艾伦·希梅尔:大家好。欢迎来到 Techstrong 电视台今天的节目。我们有一些突发新闻要告诉你，我真的很高兴有两位先生加入，他们将告诉你这个消息。我以前有幸戴过。

他们是 ServiceNow 的两个非常聪明的人。让我给你介绍一下来自“服务现在”的本·西格曼和 RJ·杰恩德拉。RJ，我想我在第二或第三个音节中漏掉了一个“N ”,但是我们会让你改正。我要请你先来，RJ。向观众介绍你自己。

RJ·杰恩德拉:嘿，艾伦，很高兴再次见到你。不，你说对了，RJ·杰恩德拉。我是 ServiceNow 的副总裁兼总经理，负责推动公司的产品增长。很高兴来到这里。

*艾伦·希梅尔:*优秀。很高兴再次见到你。当然，RJ，你是总经理，但你的投资组合包括可观察性。我相信它也包括价值流，是吗？

*RJ·杰恩德拉:*所以，ServiceNow 确实有价值流管理产品，它将许多不同的产品线结合在一起。我们的 IT 业务管理，我们最近更名为服务组合管理，SPM，就是其中之一。第二，它还引入了 devops 和 ITSM 产品的元素，以提供价值流管理。

但今天我要讲的是 Lightstep 事件响应。这是我们已经构建了一段时间的产品线，准备今天在这里发布。

Alan Shimel: 没错，所以我们要谈谈 Lightstep。本应该在这里。本，欢迎你。你为什么不给人们一点–给人们一点你的背景？

本·西格曼:是的，谢谢你邀请我们，艾伦。我是本·西格曼。我是 Lightstep 的联合创始人之一，直到去年我们被收购时，我一直是首席执行官。收购后，ServiceNow 不愿意让我继续担任首席执行官，所以现在我和 RJ 一起担任副总裁兼总经理。

Lightstep 的品牌，当然还有我们的产品和我们文化的许多方面，实际上都被有意保留下来，作为收购的一部分，这个品牌实际上已经扩展为一个多产品品牌，这就是我们今天所谈论的。

我每天的大部分时间都在思考产品愿景，特别是 Lightstep 的可观察性，以及 ServiceNow 的长期战略，以及我们可以通过将 ServiceNow 与 Lightstep 倾向于参与的高容量面向客户的应用程序相结合来为我们的客户做些什么。

艾伦·希梅尔:当然。我认为 ServiceNow 团队已经有了一个很好的 CEO，但是嘿。

本·西格曼:实际上，当我在收购过程中与比尔交谈时，我告诉他，作为一家大得多的公司的首席执行官，我向他表示哀悼。我知道 Lightstep 的压力有多大，所以我只能想象他的感受。但他是个很棒的人。

艾伦·希梅尔:当然。是的，直到你成为首席执行官，我不在乎它是一个非常非常大的公司还是一个非常小的公司，是的，这是很多。无论如何，伙计们，让我们谈谈光步，可观测性。再来说说资料片。就像你们都提到的那样，Lightstep 是这场可观测性革命或浪潮的领导者之一，我们可以说，在过去的三、四年里，它确实火了起来。

我相信，Lightstep，Ben 和你的两位共同创始人都来自谷歌，并在许多方面帮助启动了那里的整个可观测性革命。然后利用开源和开源工作，开放遥测等等，真的建立了一个相当大的社区和追随者。

ServiceNow 是我们行业中最具活力的公司之一，它认识到了这一点，并将 Lightstep 和 observability 作为 ServiceNow 产品的重要组成部分。但是从我所听到的和读到的字里行间是为什么停在那里，对吗？还有更多。

不仅如此，ServiceNow 的专业知识、市场情报和技能组合的结合，以及 Lightstep 平台可以做得更多，今天标志着这一点的显著扩展。所以，你们都是总经理。谁想先来说说这个新资料片是什么？

*RJ·杰尼安德拉:*我可以谈一点什么是扩张，我想本可以谈一谈为什么它很有意义，我们在做什么。我们在市场上看到的事情只是投入所谓数字化转型的投资金额。

它正在显著增长，我认为根据 IDC 的预测，到 2025 年，这一数字将超过 10 万亿美元。因此，马克·安德森很久以前说过的话，我认为已经成为现实，即每家公司都是软件公司，随着云的采用，组织越来越重视云运营和他们建立的软件开发团队，他们运行着数百万新的面向客户、创收的应用程序和服务。

因此，从这个角度来看，真正负责保持应用程序可靠性和弹性的 sre 和开发人员，他们真正开始影响业务成果。在这种情况下，如果发生事故，可能是一个错误或某种中断或性能不佳，它会对收入、客户忠诚度和品牌认知度产生重大影响。

这就是为什么您会在市场上看到围绕事件响应推出新产品的选项，这确实利用了 ServiceNow 平台的强大功能，但它将 Lightstep 拥有的观察能力整合到一个整体产品中，我们可以将其引入市场，以帮助客户更主动、更有效地解决问题。本，你想从可观察性的角度补充一下你的观点吗？

本·西格曼:是的，当然。我想我会用可观察性来解释它，Alan，我同意你的说法，这是一种浪潮，但它非常混乱，分散——现在它是一片水域，你可能很难理解，坦率地说，你有很多我称之为遗留可观察性的公司试图利用他们所拥有的东西，称之为可观察性，因为这比改造它更容易。

所以，花一个 30 秒的小片段来谈谈可观测性在架构上到底是什么，可能会有所帮助。在集成和数据采集的底层有一些层。你之前提到过开放式遥测。我们今天发布的 Lightstep 事件响应产品也围绕它构建了一个集成生态系统。

但是你有数据的获取，你有某种存储数据的平台，我现在不会详细谈论这个，但我认为这是一个有趣的话题，有点遥远。然后，你已经用你的全部知识和工作流建立了工作流，这就是真正的价值所在。

今天，关于可观测性的很多讨论都是关于你的公制系统有一个筒仓，你的日志系统有一个筒仓。也许你添加了某种跟踪或预防性维护系统，然后将它们集成到浏览器中。

然后你还有这个事件响应的事情。那是另一个供应商，没有任何意义。当我们与客户交谈时，他们优先考虑的三件事是整体性能、速度，实际上，最重要的是事件响应和限时解决。

对于可观察性来说这是最重要的。然后，您就不只是有一个单独的选项卡，而是有一个单独的产品来进行事件管理和事件响应，从工作流的角度来看，这是不明智的。

因此，对于品牌来说，这是一件非常明显和自然的事情，将事件响应和可观察性整合到单一体验中，特别是秒钟很重要的事件响应，这样的上下文切换非常昂贵。所以，无论如何，这就是为什么这对我们来说很有意义。

这是 MPTR 问题的核心，即在可观察性方面和事件响应方面，用单一平台来管理事件管理的整个生命周期。

Alan Shimel: 当然，你知道，Ben，说到你的观点——首先，我想你称他们为“遗留可观察性供应商”实际上，他们是 APM，应用性能管理供应商—

*Ben Sigelman:* 更确切地说，是基础设施监控供应商。

*Alan Shimel:* 对，或者说基础设施——

本·西格曼:这不是

艾伦·希梅尔:你知道，每个人都喜欢好名字。

本·西格曼:对。

Alan Shimel: 我创办了一家公司，我们推出了一款产品，Gartner 后来将这款产品命名为 NAC，即网络访问控制。我们以前有一些愚蠢的名字，但高德纳，你知道，做到了这一点。

突然之间，所有这些做着完全不同事情的人开始称他们所做的事情为 NAC。可观察性也发生了类似的事情，对吗？

本·西格曼:是的。

*Alan Shimel:* 任何进行监控的人，突然间都变得可以观察了。但我认为，也是你的观点，可观察性被局限在观察中。几乎根据定义，观察，可观察性，是不可操作的。这就好像可观察性是一个被动词，而可操作性是一个主动词。

本·西格曼:你说得很对，这是一个非常好的观点。如果你去——我倾向于有点学术，但我认为这是一个有趣的观点。可观察性实际上起源于 20 世纪 60 年代的控制理论，它是可控性的一个更小、更小的表亲，这就是你们所说的。

可控性才是真正重要的事情。如果你能控制一个系统，就有科学的方法来谈论它。用数学的方法来讨论这个问题。在一定程度上，您可以将事件响应视为我们在此讨论的可控性方面。

这就像我们正在利用关联响应产品使可观测性的见解变得可行，这是实际上闭合现代分布式系统控制理论环路的一个非常重要的部分。你的见解很深刻，艾伦。

艾伦·希梅尔:好的，谢谢。偶尔，即使是瞎松鼠也会有所发现，对吧？那么，RJ，让我们来谈谈这个。ServiceNow 不是一家规模很小的公司。据我所知，在此之前，市场上并没有真正的事件响应解决方案。我不是所有服务的专家，但我不知道。

好吧，我们将把它作为 Lightstep 平台的下一个逻辑步骤来构建，只是惯性有时在像您这样规模的组织中，这是很困难的。让我们听听你的观点，是什么让这一切发生，让船转向。

*RJ·杰恩德拉:*是的，艾伦，通过我们的 IT 服务管理和 IT 运营管理产品，我们在 ServiceNow 平台上确实拥有一些功能，比如围绕事件关联的事件技术，能够从可观察性工具中获取大量事件，并理解这些事件的含义。

我们在 ITSM 也有通知相关人员的功能。但实际上，ServiceNow 技术已被 IT 组织和大量客户广泛采用。但我们真正看到的是，随着我们的客户正在经历数字化转型，他们正在重组，而那里的产品团队是被派去采用这些可观测性技术的人。

这就是为什么我们认为，我们要把一个产品带入市场，可以被团队采用。因此，Lightstep 事件响应的整个体验就是一个现代的 SaaS 应用程序。如果你是团队中的一名开发人员——我们现在发现，我们的很多初始客户都是小公司。

他们是后收入的早期增长阶段的公司。他们有客户，他们希望确保他们的系统高度可用。所以，我们发现他们可以上网，注册，几秒钟内就可以进入系统，开始使用，如果他们发现有价值，他们就可以刷信用卡，然后去参加比赛。

因此，这是一个非常不同的动议，非常适合小公司的团队采用技术的方式。当然，今天的创业公司会在明天成为独一无二的公司，所以这就是我们正在做的有点不同的事情。但对于 ServiceNow 客户来说，他们需要在 ServiceNow 平台中具备这些功能。

*艾伦·希梅尔:*优秀。所以，伙计们，我们来谈谈吧——如果你们不介意，我要在这里做点肉和土豆。你们今天宣布了这个。有吗？什么时候能买到？

*RJ·贾因德拉:*它现在已经在 Lightstep.com 上市。所以，我们的产品已经上市一段时间了。去年早些时候，我们进行了一次试运行。因此，它已经过实战检验，我们有许多客户已经上线。他们在生产中使用它。因此，它现在就可以使用，只需一封电子邮件就可以注册并开始使用。

艾伦·希梅尔:提供什么？它是如何定价的？如果你是现有的 Lightstep 或 ServiceNow 客户，你如何–发送电子邮件，是的，但是我如何–这将设置什么–你知道，这里涉及什么？

*RJ·贾南德拉:*是的，所以，实际上，这并不比我刚才说的复杂多少，就像你在网上注册了很多消费者类型的服务一样，开发者和 sre 可以通过电子邮件开始。我们确实有几个不同的层次。因此，我们确实有一个免费层，如果您刚刚起步，并且您可能只有几项正在监控和解决事件管理问题的服务，这是免费的。

现在，如果你要开始扩大规模，并且你有两个以上，这时候价格就开始起作用了。我们在定价方面采取了创新的方法，即基于使用情况。因此，我们看一个团队拥有的活动服务的数量，然后我们按活动服务的数量收费，这与市场上的其他一些解决方案非常不同，后者按系统中开发人员的数量收费。

我们真的认为，我们希望与我们的客户试图提供的价值保持一致，最终，如果你是一名开发人员或 SRE，你的目标是提供这些有弹性、可靠的服务。因此，我们认为，与服务保持一致，无论您是想让整个团队参与进来，还是想让更多人参与到解决方案中来，以便能够协作并找出问题所在。

所以，我们不想让座位的数量成为障碍。我们真的希望让我们的客户在整个团队中推动这种服务所有权的概念，而不是由几个关键人物拥有，因为会发生很多倦怠。

因此，有不同的模式，但在 30 天的免费试用后，如果客户看到了价值，并且他们有这些活跃的服务，那就是计费开始的时候。都是用信用卡完成的，所以是相当精简的体验。

*Ben Sigelman:* 我要补充的是，Lightstep observability 几年前试验了座位定价，后来放弃了，因为向客户提供价值对我们来说非常重要，没有什么比听到人们说，哦，我们真的想使用这个，但我们不想再增加一个座位许可证等等更令人沮丧的了。

我认为，特别是在大型组织中，对于事件响应来说，想要偶尔使用某些东西，可能每隔几个月使用一次，然后因为对席位许可的担忧而被阻止使用，这是非常令人沮丧的。

因此，对于 Lightstep 事件响应，实际上没有任何限制。你可以有一个千头工程组织，并把它们放入产品中，这根本不会改变你的账单。定价与我们认为我们提供的价值以及服务本身的弹性更相关。

艾伦·希梅尔:当然。所以，我要问一个问题。我要问你，本。正如你提到的，这是把可观察性带到控制中的一个步骤，控制路径，为了完全的控制。下一步是什么？

本·西格曼:这是个好问题。我们将进入加密阶段。不，我开玩笑的，我们没有。

RJ·杰恩德拉:加入人群，耶。

*Ben Sigelman:* 我在这里不是要谈论具体的产品，但是从 Lightstep 作为一个品牌的方向来看，我认为我们看到了一个完整的生态系统，我想你可以从我的工作流程中推断出来。

我认为我们——实际上，Lightstep 和 ServiceNow 在我们对工作流至关重要的信念方面非常相似，而且还有许多其他工作流，当人们参与为云原生应用程序和面向客户的应用程序实现可靠性和速度的工作时，他们必须进行重大的上下文切换。我认为，这是对我们未来产品走向的一种暗示。但这肯定不是最后一个。

艾伦·希梅尔:太好了。伙计们，我们已经过了 15 分钟了，但是对于那些想要今天就开始运行 Lightstep 和 Lightstep observability 的人来说，他们要去哪里呢？

www.Lightstep.com 的 RJ·贾南德拉。

艾伦·希梅尔:这正是我想要的，RJ。嘿，先生们——本，RJ——非常感谢你们前来宣布这个激动人心的消息和产品，Lightstep/ServiceNow 团队的新产品。保持联系，祝你好运。听起来像是赢家。我们希望很快听到更多。

RJ·杰恩德拉:谢谢你，艾伦。

本·西格曼:谢谢你，艾伦。

艾伦·希梅尔:谢谢大家。好吧，去看看，Lightstep.com，他们新的可观察性和事件响应现在是其中的一部分，来自 ServiceNow。我们要休息一下。我们马上回来。