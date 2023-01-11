# DevOps 聊天:容器安全和 Aqua 3.5 与 Rani Osnat 和 Andy Feit

> 原文：<https://devops.com/devops-chat-container-security-and-aqua-3-5-with-rani-osnat-and-andy-feit/>

在短短三年多一点的时间里，Aqua Security 在集装箱安全领域树立了自己的品牌。随着 Aqua 3.5 的发布，该公司再次提高了无服务器和容器加密升级和功能集的标准。

我与 Aqua Enforcer 本人、Rani Osnat 和“波士顿”Andy Feit 坐下来讨论了这次重大发布的细节。拉妮和安迪给了我们一个内幕。

像往常一样，下面是流媒体音频，然后是我们的谈话记录。

[https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/tracks/529832667&color=%23ff5500&auto_play=false&hide_related=false&show_comments=true&show_user=true&show_reposts=false&show_teaser=true](https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/tracks/529832667&color=%23ff5500&auto_play=false&hide_related=false&show_comments=true&show_user=true&show_reposts=false&show_teaser=true)

## 副本

艾伦·希梅尔:大家好，我是 DevOps.com 的艾伦·希梅尔，您正在收听的是另一个 DevOps 聊天。今天的话题是关于网络安全、容器安全、Kubernetes 以及我们在 Aqua 的朋友即将发布的一个重要的新版本 Aqua Security。我很高兴能加入 Aqua 公司充满活力的营销二人组，Andy Feit 和 Rani Osnat。安迪，拉妮，欢迎。

你好，艾伦，谢谢你。

Andy Feit: 你好，Alan，很高兴与你交谈。

Shimel: 安迪，正如大家所知，你今天将从波士顿加入我们的节目。拉妮，你在以色列。对吗？

**Feit:** 是的。是的。今天我在 ____ _____ *【相声】。*

**Osnat:** 对。

**Shimel:** 现代科技。我们有一个全球专家组。但是伙计们，大新闻是，Aqua 刚刚宣布了他们的平台工具套件的 3.5 版本。你知道，Aqua 不是一个每次都有新版本发布的公司，DevOps 的口号是，你不能对任何一个版本都太兴奋。对吗？因为总会有下一次，下一次，再下一次。但这是一个令人兴奋的，是吧？

绝对的。

我们当然这么认为。

那么，我们为什么要兴奋呢？

拉妮，你想坐那个吗？

是的，我就要这个。所以，我们的每一次发布，特别是在开始的时候，一切都是新的。但是我们已经在这个领域发展了三年。这不是很长的时间，但在这个空间里，这是很长的时间。所以现在我们有很多大型企业客户在使用我们的产品。我们有一个寻求创新的市场。

对于每一个新版本，我们都试图平衡这些因素，你知道，提供市场需要的新东西。但同时确保我们的企业客户可以利用我们的平台，因为他们自己也在发展他们的云原生容器实施。因此，这里既有成熟因素，也有创新因素。

因此，在创新方面，我们推出了几项重大创新。首先也是最重要的，无服务器功能的风险评估。除了容器之外，这是我们向无服务器技术领域的一种横向扩展。你知道，我们所看到的，基本上是人们期望从无服务器容器中获得的相同的团队和相同的好处，这只是获得相同结果的另一种方法。

因此，我们希望为我们的客户提供他们所需的所有控制，以应对他们在保护这些技术方面遇到的任何挑战。不管他们是使用容器还是无服务器，或者两者兼而有之，或者任何混合环境。我们还添加了该领域的创新内容，即容器加密，我们可以就此展开讨论。

在企业可扩展性和易用性方面，我们增加了一个相当重要的方面，我认为是对我们如何管理平台上的管理控制以及用户在访问方面可以做什么的重新架构。以及策略引擎，使其在多云、多流、多应用使用方面更具可扩展性。

**Shimel:** 明白了。明白了。安迪，拉妮有没有留下什么你想补充的？

不，我的意思是，这些都是即将发布的重要产品。正如他所说。我的意思是，这在很大程度上是由我们的客户群和他们的发展方向决定的。你知道，在某些方面，这是技术元素。比如添加无服务器。在其他方面，它实际上是与解决方案共存。你知道，作为我们的客户，我们现在拥有我们认为是企业中最大的容器部署客户。

我们有一些非常大的用户和不同行业的跨度。当他们寻求推广时，他们发现他们有多个团队在这些项目上工作。他们需要实施不同级别的安全措施。在许多情况下，他们在不同的技术堆栈上实现这一点。有些使用容器，有些使用无服务器环境。

他们甚至可能使用某些基础设施的不同底层提供商。无论是开发工具还是云提供商本身。因此，就我们需要支持的内容而言，我们真的变得非常多样化。对于我们的客户来说，在安全方面，他们正试图查看整个环境并管理整个环境，并拥有一致的策略，我们对所有环境的一致报告，而不是监控 17 个不同的控制面板。重要的是，要容易做到，能够看到整个活动网络。这也是这个版本的主要内容。

**Shimel:** 伙计们，你们提到的一件事，你们两个都提到了，就是无服务器的那一块。这就是我们，我们从我们的读者和我们交谈过的人那里听到了很多。你知道，多快，我们生活在疯狂的时代，对不对？因此，如果您在虚拟机管理程序上备份，整个容器革命。现在，你知道，无服务器多快就获得了一个立足点，人们正在围绕这种类型的基础架构进行构建。

**Osnat:** 对。

**Shimel:** 让我们先了解一下，你们在这方面遇到了哪些安全挑战？

**Osnat:** 对。所以我会先说，你知道，只是增加一件事。你知道，就其在云中的当前应用而言，无服务器几乎和容器一样早就存在了。但是，使用案例完全不同。虽然它越来越受欢迎，但用例比容器要有限得多。你知道，在容器的支持者和无服务器的支持者之间有一场宗教战争。就我个人而言，我不认为这是一个零和游戏。我认为这两者最终都会被使用，并且最终都会被用于混合架构中。

Shimel: 对，我觉得不是非此即彼。

奥斯纳特:是的，我知道，但有些人希望你这么认为。我觉得不是。我觉得两者都有。我们也是如此，但是当涉及到安全性时，容器和无服务器之间有一些基本的区别。首先，今天发生的大多数无服务器工作负载都是基于云的，并且特定于云提供商，对吗？主要是亚马逊，因为亚马逊通常是更大的云提供商，尤其是在 Lambda 的无服务器领域。

但基本上你运行这些功能，它是非常云特定的。这是一个不同的地方。另一个当然是你知道的，这些是非常小的单一功能实体，可以运行几分之一秒。因此，当我们谈到无服务器的运行时安全性时，例如，与使用容器相比，要做的事情要少得多。

容器是可以运行的应用程序，它们可以运行一分钟，但通常会运行很长时间。对于只运行一秒钟的东西，当它已经在运行时，你能做的真的只有这么多。所以你需要做的很多事情是在它运行之前。你想确保你运行的东西是安全的，通过了你的政策，而且你知道，对不对？

所以当你看到挑战时，其中之一实际上是发现。你的库存中有哪些功能，你用它们做什么？第二是确保其中的内容是安全的，不容易受到攻击，配置得当。这也包括许可。所以，当你定义一个运行在 AWS 上的 Lambda 函数时，你可以给它一组权限。

取决于你如何配置它，这可能是非常自由的，也可能不是。当然，你希望它越少越好，越少越好。以便不允许它做任何超出它应该做的范围的事情。因此，现在我们主要关心的是预防性控制，这也是我们的客户所在之处。基本上确保你是，当你运行某个东西时，你实际上知道它是什么。你知道你已经批准了。你可以安全地运行它。这是我们认为保护无服务器功能的正确方法的第一步。

很公平，很公平。回到你一开始说的非此即彼的话。关于容器会取代管理程序之类的东西，也有同样的争论。我认为我们看到的是，大多数人希望虚拟机管理程序上有容器。

**奥斯纳特:**确实如此。这是-

**Feit:** 是的，我还要补充一点，拥有大量 VMware 和 hyper-v 的数据中心也没有消失。他们不会的。它们可能永远不会完全消失。今天的新发展是云原生开发。你的大部分移动客户面临发展。

在云中这样做是有意义的，只要你在做新的开发，为什么不在最新最好的上做呢？但是，在容器或无服务器或混合方法上做一些事情所获得的灵活性，使它变得更加平滑、容易、可伸缩。你会得到所有这些好处。但是我们没有看到人们大规模地走进去说，我现在必须清理这个数据中心。所以我认为——

**Shimel:**_ _ _ _ _ _*【相声】*把婴儿和洗澡水一起倒掉。人们——

是啊。

奥斯纳特:对。所以我认为这是我们做的一件事。另一个，我认为我们宣布的非常有趣和创新的功能是容器加密。我想解释一下这个用例。所以我们和很多组织合作。比如我们工作，我们的一些客户是 ISV，他们创造软件给客户使用。

这些软件是他们开发和投资的专有知识产权。出于这些原因以及管理原因，他们通常希望确保只使用最新的东西，等等，他们可以控制它在哪里运行以及谁在使用它。因此，我们在这里提供的一项功能是加密，基本上就是在构建容器映像时对其进行加密。

然后为了运行它，你需要解密它的所有内容，所以基本上有一个密钥，客户会有，最终用户会有。这将在图像运行时解密图像。如果您没有该密钥，映像将无法运行。所以容器本身一旦运行就不会被加密。但在那之前，它是加密的，你必须解密才能运行它。当然，这可以防止有人重复使用或转发您的软件，您可以想象除 ISV 之外的各种使用案例，在 ISV 中，公司希望对其容器进行这种深度安全控制。

Shimel: 当然可以。当然可以。我觉得这很有趣，拉妮。我想你一开始就说过，在过去的三年里，Aqua 取得了进步，整个行业在保护容器方面也取得了进步。就像之前的所有产品一样，对，每一个新版本，每一个灯泡，_____ security 都被应用了更多的修饰。

所以，对我来说，容器加密的想法是，你知道，也许首先我们必须专注于让容器以某种安全的方式工作。但现在我们可以开始考虑下一个层次，下一步，你知道，我们如何把它提高一个档次？比如容器 _____。我在想什么词。就像标准一样，随着时间的推移，容器加密变得无处不在？

**Osnat:** 不知道会不会变得无处不在。我的意思是，当然今天你有很多加密发生 TLS 和所有的东西，所有的管道处理容器。但至于代码本身，你知道，即使在高度监管的环境下，我也不一定看到每个人都加密所有的东西。但肯定有一些皇冠上的宝石，你会想要加密。

尤其是那些你不谈论可重用组件的领域，对吗？我们的客户使用的许多容器都是基于开源组件的可重用容器，这很好。你不需要加密你的 NGINX webserver 容器吧？也就是说，它和人们使用的其他 NGINX 容器是一样的。但是，如果你有专有的东西，那就是你想要的，或者是特别敏感的东西，无论是出于任何类型的安全、保密原因，还是出于知识产权原因。这时你会想使用类似的东西。

但是你所说的实际上把我带到了我想谈论的另一个话题，即这些技术的使用在我们合作的一些更领先或更具开拓性的公司中是如何变得成熟的，这就是为什么我们在这些可扩展性、可管理性特性上进行了投资。所以我想解释一下它在客户环境中的样子。

所以当我们开始的时候，我们和市场一起开始，我们与之交谈的公司，甚至更大的公司，通常会有一两个实际使用容器的团队，对吗？所以，你说的是孤立的项目。这是做事的一个层面。但是随着我们的发展，你知道，现在我们的客户有数百个开发团队在使用容器。他们每天制作数千张图片，因为这些都在 CI 流程中。

所有这些都进入这个大型搅拌机，最后通过 Kubernetes 或 mesosphere，基本上通过一个管弦乐队到达各种交付平台，无论是云还是云，或者两者的混合。如果从企业的角度来看，他们想要的是一种应用安全策略但保持职责分离的方式。维护他们拥有的条块分割和多依赖模型。因此，我们所做的是真正改变我们的管理访问模式和策略引擎，以实现这一点。

所以基本上，你说的是使用 Aqua 平台的人。他们安装了一个 Aqua 平台。但是他们基本上可以区分不同的团队可以看到和做什么，不同的角色可以看到和做什么，以及那些策略如何应用。

我举个例子。假设您有一个与 PCI DSS 相关的应用程序。处理信用卡交易。因此它必须符合 PCI DSS 标准要求的某些标准。你想要，你是，但在基础上你使用一些基本的元素，比如，我不知道，MongoDB 或 MySQL。您在 PCI 上下文中应用策略的同一个 MySQL 映像将具有与非 PCI 上下文不同的策略。因此，制定有针对性的政策非常重要。

这是一个方面。另一个方面是谁有权访问什么。因此，处理 PCI 应用程序的人员、开发人员、DevOps 团队当然需要处理某些方面的问题。但是他们不一定需要控制政策。这将由安全和法规遵从性团队来完成。同理，他们不需要访问，或者其他团队不需要访问那个 PCI 应用。

因此，我们谈论的是一个矩阵，它根据特定的应用程序或地理位置，或者它在什么云上，或者它使用什么注册中心，真正区分谁可以访问什么，以及他们可以使用该访问权限做什么。所有这些参数。我们已经做到了这一点，现在这两个模型结合在一起，基本上为您提供了这个矩阵，也就是说，每个方面都有几十个参数，基本上决定了谁可以访问什么，谁可以做什么，是查看访问权限还是编辑访问权限，或者只是对日志的访问权限，例如，对审计员等。因此，在使这些大型部署能够在企业环境中工作方面，这确实是一个进步。

绝对的。好东西。伙计们，我想跟你们探讨另外两个话题或领域。一个具体到 3.5，一个具体到市场。我们的时间快结束了。所以你知道，我们听说过不可变的基础设施，你知道容器环境的优势之一。

那么，你如何部署，你知道，现在你有一群客户。他们想升级到 Aqua 3.5。简单谈谈您实际上是如何升级或运行这一升级部署的。这是一个抛弃你所拥有的，重新站起来的问题吗？因为 Aqua 本身就是容器化的。或者是，什么，给我们一点见解，螺母和螺栓，如果人们想升级。你知道我在说什么吗？

奥斯纳特:对。所以我们的升级过程很简单，因为我们使用了容器，对吗？所以没什么好装的。您只需运行新的容器。我们确实向后兼容以前的版本，所以当任何人使用旧版 Aqua 升级到这个版本时。

实际上，我们是最后一个，我们不，我的意思是，我们发布软件的频率比我们的一些客户希望遵循的升级时间表要高，对吗？我们不会强迫他们这么做。但是在最近的版本，最近的主要版本 3.2 中，我们实际上有很多客户转向了它。所以从这方面来说，我们的情况很好。

他们当然可以在月底 3.5 发布时升级到 3.5。因此，他们没有什么特别需要做的，当然，我们总是建议他们首先在测试环境中做这件事。一旦你看到一切正常，你就可以把它投入生产。

**希梅尔:**优秀。非常好。所以让我补充一下——

**Feit:** 现在还有一件事我想插一句，那就是我们所说的组织规模，特别是如果他们有多个团队在不同的平台上工作，并且需要实施不同的策略。在一些较大的企业中，甚至很难真正看到一切，了解一切，跟踪谁在哪里运行什么，谁是这些所有者。因此，该产品的一个新特点是界面非常漂亮。

这可能是我们产品目前最漂亮的部分。仪表板看起来总是很棒。但是您现在可以进入并执行我们称之为工作负载资源管理器的操作。直观地查看所有正在运行的工作负载，无论它们是在 Kubernetes、Docker 还是 OpenShift 上，您都可以看到在大型分布式运行时环境中运行的一切。深入了解它们，您可以开始做一些事情，比如突出显示那些易受攻击或高风险的组件，那些符合 PCI 的组件可以通过编码跳出来，您会更容易看到这些组件。

然后你可以做表格机制。开始过滤。只给他们看那些在这个平台上运行的。假设某个组件暴露了一个漏洞。你可以给我看这些，然后开始深入观察它们，看看它们在往哪里跑？这是本地的吗？这个是在云上吗？它运行于哪个云提供商？

你知道，随着公司变得多团队、多云、多堆栈，你所看到的矩阵变得相当复杂。作为工作负载探索者，这是在大型企业中四处走动的好方法。看看你有什么，明白你现在需要做什么。

Shimel: 你知道，我们不要轻视它。我们不要轻视。我很难理解这个词。我们不要轻视它。你百分之百正确，安迪。今天的组织是多元化的。

奥斯纳特:我同意。

**Shimel:**_ _ _ _ _ _ _ _ _ _ _ _ _ 分布在这么多不同的层面上，可以 360 度全方位地观察土地的布局，所有这些在哪里，它们是如何相互作用的。就其本身而言，有人可以制造出一种产品。我是说，这太疯狂了。

顾客大开眼界了。就在最近，我们已经和一些早期用户一起使用这个产品一个月或六个星期了。我们的一些销售工程师已经在概念验证环境中实施了它。当客户看到这张地图时，他们会说，等一下，这是哪里？给我看看那个。

他们正在发现他们没有意识到他们拥有的东西，因为你现在可以想象和看到它。你知道，当它作为另一个警报或文本字段进入你的 SIM 系统时，那是一回事。您必须查看日志并知道要键入的查询。但是当你看到它的时候，你跳进去开始环顾四周，说等等，那是什么？

人们大开眼界。好吧，我要去和那个人谈谈。从字面上看，人们正在发现他们不知道他们的环境中存在的东西。这就是在一个大环境中，这个工具如何非常有助于组织事物并向您展示那里有什么。

**Shimel:** 绝对，绝对。伙计们，你们的最后一个问题与 3.5 无关，而是与分数有关。你知道，我们似乎正在经历一个，嗯，这是不变的。但是最近，我们已经看到越来越多的容器内的技术载体整合，围绕 Kubernetes，你知道，IBM 的 Red Hat

**Feit:** 云吧？

***Shimel:*** IBM 的红帽收购，340 亿美元。我是说，是它的国王。但是我们看到，例如，CA 或 Broadcom CA，不管他们现在叫它什么，以将近 10 亿美元的价格在 _____ 上旋转。敬汤姆或布拉沃。我们看到，谁，有人刚买的，是不是 _____ 刚买了一个-

**奥斯纳特:**后来的见识，没错。

***Shimel:*** 集装箱里的东西。

**Osnat:** 对。

**Shimel:** 我的意思是，在某个时候，巩固 Aqua 已经在这里宣扬了三年多的东西。你认为这会有什么影响，我是说现在，3.5，你又提高了标准。让其他人努力赶上。但是在这种氛围下，跟我们说一点。这在 Aqua 周围意味着什么？或者你只是继续做你的事情？

奥斯纳特:嗯，这是个好问题，艾伦。我是说真的，我觉得你一直在做你的事情。因为你的任务是了解客户的发展方向，并构建解决他们真正需要的解决方案。我们努力盯着那个球。从早期开始，我们就大力提倡支持多平台的概念。

我们最初是 Docker，但今天我们支持各种东西，包括一些不太广泛使用的技术。但是 pivotal 和微软容器。支持所有云。所以你要把目光放在那个球上，目标是建立一个客户群，这个客户群对你的产品感到满意和喜爱，对与你合作感到兴奋。

对我们来说很重要的一点是，我们的客户将继续与我们续约并留住我们。你知道，我们才相处了三年。但是我们看到，我们最大的客户非常高兴使用我们，并扩大他们对我们的使用。他们两年前让我们进行了试点，现在他们已经投入生产，他们已经让我们生产了五个应用程序。现在他们出现在 50 个应用程序中。所以这一切都很好。我们不是很关注嘿，我们必须在某个时候被收购，或者我们必须在某个时候上市。

让我们制造正确的产品，继续看到采用。无论是在我们的客户群中，还是在部署更多产品的客户中，以及在使用我们的解决方案的新名称、新徽标中，我们都在快速发展。这对我们来说很重要。市场，你知道，市场就是市场。如果有人说等等，我不能让这些家伙变得更大。我要试着把它们抢购一空。那可能会发生。但这不是我们真正关注的事情。我们专注于以正确的方式有机地构建业务。

我不得不说，我们都已经老得足以经历网络泡沫了。你知道，那时候的狂热。我认为保持头脑冷静很重要。我们已经存在三年了。我们刚刚突破了 100 名员工的大关。庆祝一下。你知道，我们和客户一起工作，我们对此很高兴。我们保持头脑冷静，继续工作。你知道，有人来出价 350 亿美元收购我们，比如 Red Hat，我肯定董事会会同意的。

**Shimel:** 他们可能会认为

你知道，他们会考虑几天的。但与此同时，我们努力保持理智。

希梅尔:我听到了。伙计们，最后一次提醒，趁你们俩还在。我会在 TubeCon Native、cloud native、Linux foundation 活动上看到你们，还有 Red Hat，对吗？赞助周一的集装箱安全会议。我想我们上次已经谈过了。我只是，我不想把日期搞砸，但我以为是 12 月 9 日^第号，或者 10 日^第号。

不是，12 月 10 日^日。这是 KubeCon 开幕前的星期一，与西雅图的活动同时举行。当你注册 KubeCon 的时候，你可以在 CNCF 网站上注册，或者如果你已经注册了，你可以回到那里添加这些并置的活动之一。我们的峰会非常关注企业安全，因此被称为 KubeSec 企业峰会。

因此，对于较大的组织来说，面对您知道的法规遵从性需求并在生产中部署容器，这是了解其他人在做什么的一个很好的方式。我们有一个很棒的演讲者阵容。我们有，JPNC 正在讲话。我们有火绒说话。我们让星巴克谈论他们的安全容器之旅。我们有 Liz Rice 和 Michael Hassenboss，他们最近写了一本关于 Kubernetes 安全性的书。这本书甚至还没有出版，它仍然是一本电子书，但它将首次以纸质形式在 KubeCon 上发布。我们会让他们在我们的展位上，他们会在那里签名售书。

因此，这是一件大事，人们可以接触到所有这些技术，并听取许多不同人的意见。我们公开征集演示文稿，因此我们拥有从技术到合规性再到最佳实践的所有内容。这将是一件大事。我们已经有几百人报名了。我们只能容纳 300 人。所以，如果你的读者想参加，他们应该尽快参加。

绝对的。嗯，我也会去的。我们会报道的。安迪，拉妮，我们像往常一样超时了。我 _ _ _ _ _ _ _ _ _ _，我们需要到此为止。恭喜 Aqua 3.5。我相信这将是一个很大的好处，客户群会非常感激，我们期待在西雅图与您见面。

期待见到你，艾伦。和你聊天总是很开心。和你的听众分享正在发生的事情。

**Shimel:** 谢谢。安迪·费特，拉尼·奥斯纳特，水上保安。我是 DevOps.com 的艾伦·希梅尔，您刚刚听到的是另一个 DevOps 聊天。

— [Alan Shimel](https://devops.com/author/ashimmy/)