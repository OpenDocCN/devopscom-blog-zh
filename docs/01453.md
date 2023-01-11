# devo PS Chat:GitHub Enterprise as a Hosted Service，Jean-Louis Vignaud

> 原文：<https://devops.com/devops-chat-github-enterprise/>

我最近和 IBM 的项目经理 Jean-Louis Vignaud 坐在一起，讨论最近在 Bluemix 上推出的新的 GitHub 企业托管服务。GitHub Enterprise as a hosted service 对于由于合规性或其他安全需求而无法使用共享的公共 GitHub 服务的企业来说是一个很好的选择。

这种 GitHub 企业托管服务是第一个可用的此类服务，托管在 Bluemix 服务上，作为内部和混合环境。您可以从以下网址获得更多信息:

1。博客: [推出首个 GitHub 企业托管服务](https://developer.ibm.com/bluemix/2016/06/16/github-enterprise-hosted-service-on-bluemix/)

2。视频:[GitHub 企业与 IBM Bluemix 专用的好处](https://www.youtube.com/watch?v=AxGTFZzZ7vU)

3。slide share:[IBM Bluemix Dedicated–GitHub Enterprise](http://www.slideshare.net/IBMDevOps/ibm-bluemix-dedicated-github-enterprise)

此外，我们将举办一场网络研讨会，深入探讨这一问题。更多信息请访问:[http://webinars.devops.com/scaling-devops-github/](http://webinars.devops.com/scaling-devops-github/)

同时，这是这次谈话的音频文件，下面是我们谈话的文字记录。

[https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/tracks/273800206&color=ff5500&auto_play=false&hide_related=false&show_comments=true&show_user=true&show_reposts=false](https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/tracks/273800206&color=ff5500&auto_play=false&hide_related=false&show_comments=true&show_user=true&show_reposts=false)

**Alan Shimel:** 大家好，我是 DevOps.com 的 Alan Shimel，我在这里与另一位 DevOps 聊天。今天 DevOps Chat 的嘉宾是 IBM 的项目经理 Jean-Louis Vignaud。Jean-Louis，我希望我没有把这个名字搞砸。

让-路易·维格诺:不，没关系。谢谢你艾伦。

希梅尔:好的。Jean-Louis，欢迎来到 DevOps Chat，正如我提到的，你是 IBM 的项目经理，现在，无论如何，你非常积极地参与到 GitHub Enterprise 作为托管服务产品的工作中，我们希望专门就此与你谈谈。

**Vignaud:** 好的。

Jean-Louis，我想这里的每个听众都熟悉 Git 和 GitHub，但他们可能不熟悉 GitHub 企业即服务的概念，所以我们为什么不从这里开始，如果你能向我们的观众解释一下这是什么的话。

好吧，也许我们可以先从 GitHub 开始。

希梅尔:好的。

GitHub 非常知名，到今天为止，它已经有大约 1500 万用户，这是一个非常知名的用户体验。这是一个协作平台，它基于 Git，所以它运行在 Git 之上，但它在 Git 之上有许多其他服务。GitHub 的目的是提供一个协作平台，让世界各地的人们能够在一个商业项目甚至是一个私人项目上进行协作。

这个非常著名的协作平台对于希望在自己的组织内提供相同级别协作的企业来说非常有吸引力。GitHub 在 2011 年底和 2012 年初推出了 GitHub Enterprise。GitHub Enterprise 是 GitHub 的内部版本。同样的一套功能，但是您可以在您的本地环境中安装它，并让它在您的防火墙内工作。这使得团队能够——你知道，让组织和不同的团队能够以一种安全的方式相互协作。

这就是背景，也是我们介绍产品之前的情况。

**Shimel:** 嗯嗯，还有*【相声】*——不好意思。我不是有意打断的。

**Vignaud:** 是的，我想说的是，通常，在一个组织中，一旦你必须安装你的产品，你必须运行它，你必须管理它，你必须提供你的基础设施，你必须安排人来管理 GitHub Enterprise 产品，这意味着进行备份，进行升级，监控它的运行，并做一切需要做的事情，以符合企业安全要求。

这需要时间，而且大多数内部组织，你知道，人们正在寻求迁移到云，利用云设施的优势，他们今天可以在 GitHub 中找到，但这是一个公共云，不符合组织的安全要求，他们想要相同的 GitHub 体验，但在他们的组织内。这就是我们围绕 GitHub Enterprise 提供服务的地方——在组织内提供 GitHub 的用户体验，同时仍然由 IBM 管理。

**Shimel:** 明白了。让我澄清一下，Jean-Louis，据我所知，IBM 是唯一一家真正提供 GitHub 企业托管服务的公司，对吗？

是的，这是首款此类产品。我知道如果你调查 GitHub 提供了什么，GitHub 提供了 GitHub Enterprise，所以你可以在本地运行它。你也可以把它作为服务安装在基础设施上，所以你可以在 AWS 内部运行它，你可以在 Azure 内部运行它，但是没有人围绕 GitHub Enterprise 提供服务。因此，对于 IBM，它由 IBM 托管和管理，因此“和管理”是独一无二的。

**Shimel:** 明白了。我想强调的另一件事是，正如我们在开始今天的广播之前所说的，这是与 Git 合作的，对吗？

**Vignaud:** 对，就是和 GitHub 的合作，对。今年 2 月初，我们在 InterConnect 上宣布了合作伙伴关系，因此自宣布以来，我们一直在努力开发这一产品。所以我们花了 12 个月的时间来构建和发布它。

**Shimel:** 明白了。我认为这很重要，因为你知道，拿一些开源项目作为托管服务提供是一回事，对吗？任何人都可以这样做，这是开源的。

**Vignaud:** 是的。

**Shimel:** 但是，我认为，真正与 Git 合作是让企业拥有自己的 Git 环境，真正作为托管服务的最好机会。

Jean-Louis，我想谈谈该产品的另一个方面，那就是，它也是集成 Bluemix 专用产品的一部分，对吗？

**Vignaud:** 是的。

**Shimel:** 那么让我们从什么是 Bluemix 专用开始吧？

**Vignaud:** 好的，IBM 平台即服务产品是 Bluemix。因此，Bluemix 由一组庞大的服务组成，用于移动应用程序和认知应用程序，因此大约有 150 多个 API 组织可以用来构建云原生应用程序，以将这些应用程序与后端系统集成。因此，Bluemix 可以在公共云中使用，但也可以作为客户的单租户专用云使用。

这是 Bluemix 专用的。因此，这意味着，对于我们的客户来说，所有这些 API、所有这些平台使您能够构建和运行您的应用程序，是一个大杂烩。它基于 Cloud Foundry，它支持容器、码头工人等等。因此，它提供了一套非常广泛的技术，使组织能够快速构建应用程序。

作为 Bluemix 的一部分，有一组 DevOps 服务，因此我们提供工具来帮助组织构建这些 Bluemix 应用程序。这就是我们 GitHub 企业产品的位置。这是一个 DevOps 产品，是 Bluemix 的一部分。

**Shimel:** 明白了。Jean-Louis，我的意思是，不幸的是，我们只有 12 到 15 分钟的时间，但我们可以从很多层面来了解 GitHub Enterprise 产品可以做些什么？特别是，在我看来，如果您正在开发应用程序，并且您只是希望您的整个平台即服务具有同类最佳的东西，如 Git，如 Cloud Foundry，所有这些元素在平台即服务论坛中为您提供了同类最佳的应用程序开发，看起来所有的部分都在这里汇集在一起了。这是活着的好时光。这是一个很好的时机，如果你想开发应用程序，让它触手可及。

**Vignaud:** 是的，在 Bluemix 专用的单租户环境中，它与您的企业网络完全集成，因此它使您能够安全地与您的后端系统集成。所以你真的有一个非常先进的平台，使你能够以一种安全的方式发展；你知道，非常创新的应用。

希梅尔:是啊。让·路易，我有两个问题要问你。第一，就使用 GitHub Enterprise hosted 相对于 public Git 的优势而言，GitHub 是我们许多人使用的，我认为有 5000 万人使用——明显的优势是，这是一个更安全的环境，它只属于你。但是有什么不好的地方吗？有没有一些托管服务中没有的功能可以在公共服务中使用？

不，不是真的。要知道，GitHub Enterprise 的设计初衷就是提供和 GitHub 一样的用户体验。我要说的是，GitHub Enterprise 的价值在于 GitHub 的用户体验，但你可以为你运行它，所以它对作为客户的你来说是单租户，利用 IBM 的云基础设施，你可以在你想去的数据中心运行它，地理上你可以在你所属的国家本地化它。因此，如果您有法规遵从性要求，要求您在国内托管源代码，您可以这样做。

因此，我认为，在部署产品时，没有任何限制，而且更加灵活。

**希梅尔:**优秀。下一个问题，我只是想确认一下——今天公开发布了吗？因为我记得—

**Vignaud:** 是，是的。今天可以买到。我们在 6 月 17 日宣布了这个消息。我们在 6 月 17 日正式宣布了它，所以是的，它今天就可以使用，任何 Bluemix 专用客户都可以将其作为产品的一部分使用。

哦，太好了。Jean-Louis，我还应该提到，在不久的将来，实际上——我想我们现在正在最后确定时间表——我们实际上将与 GitHub 和 IBM 一起举办一次完整的网络研讨会，我们将对这一产品进行更深入的探讨，对于那些可能感兴趣的听众，我强烈建议您参加这次网络研讨会。

但是 Jean-Louis，如果人们不想等待网上研讨会，我知道 IBM 已经发布了几个内容片段，人们可以从中获得更多信息。一个是介绍 GitHub Enterprises 服务的博客，有一个视频展示了它的好处，我想 SlideShare 上也有一些关于 IBM Bluemix Dedicated 和 GitHub Enterprise 的内容。我会试着—

**Vignaud:** 是的。

**Shimel:** —是的，当我们发布这个聊天内容时，我会试着加入这些内容的链接，但是我再次强调，如果你对他的有疑问，如果你是一个 Git 用户，并且想拥有自己的 GitHub 企业专用服务，我会试着把这些内容放在那里。

你知道吗，吉恩·路易斯，不幸的是我们快没时间了。你有什么要补充的吗？

**Vignaud:** 我觉得这样挺好的。艾伦，非常感谢你在这里接受采访。

**Shimel:** 谢谢。

我真的很期待有很多顾客来购买这款产品。

你知道，我认为这是市场需要的。有那个真好。正如我所说，今天是一个开发人员的大好时机，对吗？这么多工具，这么好用。

**Vignaud:** 是的。

**Shimel:** 无论如何，IBM 项目经理 Jean-Louis Vignaud 非常感谢您今天的参与，我们期待听到更多关于 GitHub 企业即服务的信息。

我是 DevOps.Com 的艾伦。感谢您的收听，我们将在下一期 *DevOps 聊天室*再见。

**Vignaud:** 谢谢。