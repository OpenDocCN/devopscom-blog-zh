# 安全策略管理和采用 Tufin 的混合云

> 原文：<https://devops.com/security-policy-management-with-tufin/>

在本次[TechStrong TV](https://digitalanarchist.com/videos/featured-guests/colby-dyess-techstrong-tv)/[devo PS Chats](https://devops.com/category/devops-chat/)采访中， [Tufin](https://tufin.com) 的云产品管理总监 Colby Dyess 与 Mitch Ashley 共同探讨了混合云、多云和云原生安全的安全策略管理。在 2020 年末录制的视频中，Colby 分享了在 2020 年快速迁移到云的过程中与客户合作的一些经验。

下面是对话的视频和播客音频，后面是文字记录。尽情享受吧！

#### TechStrong 电视视频

[https://player.vimeo.com/video/510712524](https://player.vimeo.com/video/510712524)

#### DevOps 聊天播客音频

[https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/tracks/992512045&color=%23ff5500&auto_play=false&hide_related=false&show_comments=true&show_user=true&show_reposts=false&show_teaser=true&visual=true](https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/tracks/992512045&color=%23ff5500&auto_play=false&hide_related=false&show_comments=true&show_user=true&show_reposts=false&show_teaser=true&visual=true)

[DevOps.com](https://soundcloud.com/devopschat "DevOps.com") · [Security Policy Management and Hybrid Cloud, Tufin](https://soundcloud.com/devopschat/security-policy-management-and-hybrid-cloud-tufin "Security Policy Management and Hybrid Cloud, Tufin")

## 副本

**Mitch Ashley:**Tufin 的云产品管理总监 Colby Dyess 今天和我在一起。欢迎你科尔比。欢迎，很高兴和你谈话。你能介绍一下你自己吗，告诉我们一点关于你的情况，当然，也告诉我们关于 Tufin 的情况。

戴斯:是的，你知道我的名字和头衔，所以我是从气候宜人的新罕布什尔州南部打来的。我曾在 Tufin Technologies 工作过，Tufin 在业界因提供安全策略管理而闻名，主要是在像全球 2000 强这样的复杂环境中，您需要对网络环境进行更改，并且您需要能够快速、安全地完成这些更改，理想情况下，您可以自动完成这些更改，而且是安全的。Tufin 产品套件可以帮助组织做到这一点，我们已经在传统领域做到了这一点。当然，我们的客户已经采用了云、云原生平台、Kubernetes，我们也一直在利用这些相同的功能来保护环境并将其引入云中，因此无论您将工作负载放在哪里，我们都可以帮助您，这也是我们一直关注的重点。

阿什莉:好东西。伙计，很多人的宇宙中心。说到这个，想想我们所处的时间，你知道，有很多统计数据。我经营着一家分析公司，是 MediaOps 组织的一部分，名为加速战略集团。无论如何，我们有大量数据显示，在过去的六到九个月里，数字化转型和向云的迁移都在加速。我不认为这对任何人来说是新闻，对吗？我不知道你是否需要数据来说明这一点，因为这可能发生在大多数人的组织中。

没错。

**Ashley:** 如果我戴上我的安全帽子一会儿，当我们做出改变、做新项目和加速事情时，我们总是会得到很多注意——讽刺——所以，我肯定有很多安全人员仍然在努力，不仅要跟上步伐，还要确保我们都在保护我们的开发人员正在使用的环境，确保我们了解我们现在可能会使用的服务，我们以前没有过的云服务。我相信你已经看到了很多发生在你的顾客身上的事情。

是的。这并不奇怪。组织迁移到公共云环境已经有很长一段时间了，至少从技术上来说，在过去的 15 年里，他们一直在这样做，但并不总是得到批准，对吗？比方说，在过去的五、八年里，组织已经开始有意采用云。今年，当然，每个人都以最快的速度转向了云计算。

我们所看到的，至少是我经常看到的是，安全部门现在正争先恐后地试图获得一些可见性，即这些云环境中到底发生了什么，并试图在开发团队使用的服务周围设置某种护栏。这是一个真正的挑战，因为他们一直非常关注如何保护大部分内部环境或使用防火墙来保护云空间，但现在他们意识到他们必须更深入一些，因为威胁确实存在，而且非常动态。如果您不确定如何保护云环境的安全，您将使自己暴露在威胁面前。

因此，安全部门真的花了很多时间来尝试了解更多关于云和云原生安全控制的信息。我们花了大量时间帮助客户弄清楚云本地安全控制和本地安全控制之间的区别，然后如何将它们结合起来，以便他们可以确信一切都是安全的。我们看到了很多，是的。

阿什利:嗯，你知道，我的意思是，我们都在做防火墙、入侵防御和访问控制，这样的例子不胜枚举。

是的。

阿什利:所以，这个话题并不新鲜，但是环境和服务都不同。这不像你可以进入云—不，让我们使用我在本地环境中通常使用的所有东西。也许你可以得到一些软件版本。有时使用更好，因为它集成得更好，通过使用云提供商提供的东西，您花费更少的时间来使环境工作。

是的。这种模式在任何地方都一样。我已经看到你将要去一个新的环境，你想要带走一些过去对你有用的东西，并把它们发扬光大。很多时候，当您试图快速迁移到云中时，这是有意义的。如果您不熟悉云原生安全控制，您可能会想，“我将只使用防火墙和管理云中防火墙的过程。”有很多选择可以做到这一点，该领域的许多传统供应商都试图在云环境中提供相同的服务和相同的功能。所以，我们看到大量这样的例子并不奇怪。

与此同时，管理所有这些东西的过程仍然需要很长时间。如果您迁移到云，您是为了获得灵活性，对吗？您希望快速构建应用程序，并尽快将其推向市场。但是，如果您必须填写一张票来更改防火墙，并且需要三天时间来处理这些内容，您就不再像以前那样敏捷了，因为您可以在 Terraform 模板中旋转一点配置，重新部署，然后—噗，您又可以重新开始运行了。这是安全团队——

阿什利:如果你再花两天时间来回答这个问题，你可能会在第三个 _____ 之后再有第四个，对吗？有些开发人员会说，“我要走了，让我去设置下一个环境。”

黛丝:是啊，太难了。你等不及了。您不想再看到 IT 受到影响，因为响应时间太长，但您必须尊重它的存在，IT 的安全网站只是在努力帮助保护业务。

但你知道，你也看到了亚马逊和 AWS，他们都宣布了自己的防火墙，对不对？Azure 做了一点点，AWS 在过去的一个月里刚刚做了。我认为这实际上是向那些真正好的技术致敬。防火墙技术确实是好东西，它不仅仅是安全组织或 NSG，它还不止于此，企业确实需要这些。这些确实解决了客户的问题。因此，我们看到许多人询问他们如何采用云提供商的新技术，以及如何将它们集成到非常敏捷的流程中？我希望我们会看到更多这样的例子。

事实上，我们发现我们经常做的是尝试帮助组织了解如何从云原生安全控制中获得最大价值，因为这些云环境真的非常稳固。正如你所指出的，安全控制被集成到服务中。因此，使用这些服务是非常有意义的，它们可以保护您的资产，而且它们与服务如此集成，您真的应该尝试使用它们，但这是一个安全学习曲线，因此尝试帮助他们获得可见性，然后开始影响对这一点的控制，这样他们就不必减慢其余业务的速度，比如说，用传统控制替换云原生控制*【Cross talk】*。

阿什利:嗯。这是一种权衡，我认为这是其中之一，我认为它将安全团队置于这样一个位置，我们是坚持我们的观点，这是我们在所有环境中运营的一致环境，还是为了速度而不牺牲安全性，我们可能会考虑一些其他选项，这些选项是否可以集成到监控和管理系统中，而不是在每个环境中使用相同的防火墙，对吗？

是的，是的。

阿什莉:说起来容易做起来难。我知道这不是一件容易的工作。

没错。你知道，无论你决定使用云原生安全控制还是使用传统的 kinda 控制、虚拟化版本或它们的组合，我认为我们分享的一件事是，我们看到许多关于如何采用哪些技术以及如何实际管理这些技术的对话。

从我的角度来看，我们似乎太专注于具体的安全控制，作为一名安全人员，我认为退一步，尝试专注于整体安全策略是很有意义的。与其考虑我应该使用什么防火墙，我应该使用来自云的防火墙还是我应该使用我的传统供应商的防火墙，也许帮助组织保持敏捷的更好的问题是安全能够专注于什么是安全策略，什么是防护栏，然后开始根据这些防护栏检查云环境，根据这些策略作为您的 CI/CD 管道的一部分，这是 shift left 的整个流行词。

这是真的，对吧？那真的很重要。安全部门可以专注于定义他们有实力的安全策略，但实施安全策略的实际实现可能由云运营部门或任何真正玩弄安全控制的人来处理。就像，如果你能把这两件事结合在一起，你能在 CI/CD 管道中做到这一点，那么这就是一个巨大的胜利。

我们已经看到组织的行动速度大大加快，因为安全关注他们所做的事情，他们以一种可以在管道中播放的方式将它整理成文，现在应用程序团队可以对应用程序或云操作进行更改，他们可以更改环境的配置，并收到警告，指出它不符合安全策略。太好了。不再选择您想要使用哪种安全设备，而是专注于事情是否符合安全策略？这是一个重大转变，对组织来说似乎很难做到。我认为现在应该摆脱安全控制，转而关注策略—我认为是信任，但也是验证。

**阿什利:** *【笑声】*回到那句老话，对吧？

是的。

**Ashley:** 你知道，在某种程度上，这也归结于——你知道，我们习惯于，让我们先做一个清单，确保我们知道我们要保护的所有东西。

当然可以。

**Ashley:** 但同样重要的是，无论是变更管理实践还是能够帮助您在变更发生时发出通知或了解变更的软件，那么当变更发生时，它如何映射回我们已有的策略，我们是否仍然保持一致，是否存在我们必须解决的差距？因为环境不再——不再是我们控制一切的环境。它会自己改变，因为其他人会和我们一起改变它。所以，如果你稍微回想一下，这似乎是一个比我们 10 年前更有活力的环境。

**Dyess:** 故意更动感吧？企业必须加快步伐，我们还必须对客户需求或竞争威胁等做出更快的反应。因此，事实上，我们已经有了这些动态环境，这只是我们实际需要建立的反映。现在，我们需要找到一种方法，将它重新纳入我们的常规实践中。

所以，你说能够跟踪什么改变了，什么时候改变了，等等，但是如果你采用更多的基础设施作为代码模型，你已经有了。你不需要 CMDB——也许你需要，但是当你可以回到你的 Git 日志并看到，哦，这是我们所做的改变的拉请求，允许这个安全组打开或这个 Azure 防火墙有这个特殊的规则时，你不需要有一个 CMDB。你可以看到这些信息，但是从安全角度来看，这些是新工具。作为一名安全人员，您上一次查看 Git repo 以了解配置是什么时候？*【笑声】*

阿什利:回购——对，GitOps 和安全，对吗？

没错。没错，但我们必须在这方面有所作为，作为一个集体，无论我们是编写代码、管理运营还是集体管理安全，我们都必须能够协作并使用这些工具，我不能说它们正在融合，它们已经存在很长时间了。Terraform 和 Helm，Ansible，Chef，Puppet，所有这些东西已经存在了一段时间，但现在将它们纳入我们的安全实践对人们来说是一个相当大的飞跃。

阿什利:嗯。

**Dyess:** 所以，正如你所指出的，我们真的尽力鼓励安全团队获得他们需要的可见性，这是第一件事，对吗？您绝对需要了解部署了什么，什么在与什么对话，以及事情是否被适当地分割。

你必须首先获得这种可见性，但我认为在你开始投入之前，让我们在那里投入一堆其他控制点，考虑那里有什么资源，以及你如何在安全方面参与自动化，参与你的 CloudOps、DevOps、SRE 等任何人设置的这些流程。因为现在有一个很好的机会让安全性成为这个敏捷过程的一部分，让业务变得安全，但要以不影响开发人员工作效率的方式进行。

阿什利:嗯。

**Dyess:** 那就是，不舒服，因为这是一个很大的改变，但这是一个我知道可以成功完成的改变。我们曾与这样做的公司合作，你知道，做出有意识的决定。

阿什利:我几乎希望我们退后一步，重新定义 shift left，因为如果，你知道，我是世界之王，我会认为，这不仅仅是让安全人员在软件生命周期的早期与软件团队合作，是的，就是这样。但是，从这个角度来想，旧的世界是，制定政策，然后我们如何实施执行机制，以确保这些政策得到遵守。

**戴斯:**嗯嗯。

**Ashley:** 我认为在我们现在所处的世界中，安全人员是，如果你今天要在一个组织中建立一个安全实践，我会做的是，让我们从如何创建软件开始，让我们与团队合作，了解整个工具链是如何建立的，流程是如何发生的，对于应用软件来说， 还包括基础设施，以及如何创建基础设施，我们谈论的是测试环境和生产环境，如果基础设施真的是动态平台或任何类型的环境，你可能会以代码的形式进入基础设施。

但是从这里开始，因为如果你知道怎么做，现在你知道如何保护它。你知道如何与团队合作来帮助他们保护它，那么下一层将进入围绕微服务的软件架构本身，以及比我们习惯的更容易渗透的东西，有点像过去的整体应用程序的坚硬外壳。

对我来说，这是一种心理转变，对于一个安全团队来说，这是一种巨大的心理转变，不一定要成为所有这些方面的专家，但要明白这才是你现在真正要保护的。

**戴斯:**所以，有两件事很突出，比如我可以想象人们现在的反应，那就是，我没有时间去学习所有这些东西。*【笑声】*我已经拿到了 20 张其他优先事项的票。我现在就要开始，所以我不能去学那些东西。有效，这肯定是很多组织的情况。

与此相关的另一个问题是，安全团队可能确实想知道，可能有时间去做，但却苦于应用程序团队自己甚至不知道应用程序是由什么组成的，以及他们需要什么连接。因此，即使你认为他们会知道，因为他们建造了它，你会认为他们会知道其中一些问题的答案，但事实证明他们不知道——在大量令人震惊的场景中，情况就是这样。

阿什利:嗯。

**Dyess:** 因此，如果你要向左转，你必须解决的不仅仅是安全团队在这方面获得可见性的问题，或者实际上，这是一回事。应用程序团队必须能够走到桌前说，“这就是应用程序的样子。这是如何组合在一起的。这里有它需要的资源，这里有依赖它的服务。”

阿什利:嗯。

**Dyess:** 因此，如果应用程序组可以参与进来，那么安全团队通常可以很快地查看它，查看地图并说，哦，我可以看到它需要这样划分。我可以看到他是一个资源，有太接近 PII，PCI，对不对？因此，如果这是您正常计费实践的一部分，那么对话可以更快开始，您可以生成这些视图，您有一些方法来生成网络团队或安全团队可以查看的项目，对吗？他们不需要看源代码，他们需要看你的网络拓扑，他们需要了解你在连接什么。

因此，如果你能弥合这一差距，那将大有裨益。所以，对你来说，这不仅仅是“我只需要检查它是否符合政策。”有时，它甚至只是试图在一开始就定义策略。

阿什莉:是的，在你试图保护的东西上。

**Dyess:** 是的，但是，虽然安全部门似乎从来没有注意到正在发生的事情，这是你在开始时开的玩笑，但也有这样的情况，当应用程序团队正在构建他们并不真正拥有所有规则的东西时，他们不确定所有的限制是什么，如果你给他们访问权限，他们可以从 API 中获取大量的防护栏和指导方针来进行自己的检查。

所以，你知道，有一个模型。我们以前在行业中做过这种事情，回到我写代码的时候，我们有一个单独的 QA 团队，所以我们会写代码，我们会做一点点测试，但坦率地说，足够让我们通过构建，对吗？然后我们把它扔到墙那边，它就被送到了 QA 那里。幸运的是，我们的开发实践成熟到一定程度，我们意识到我们实际上需要将测试作为我们工作的一部分。因此，作为开发人员，我们必须拥有一些测试，一些更多的测试，但同样重要的是，测试团队在应用程序生命周期的早期介入，也就是您谈到的模型。因此，QA 团队可以进来学习更多的知识，并开始设置一些额外的测试，并参与构建过程，所以他们所做的在 NMake 中显示出来。

因此，我认为安全性也在这样的道路上。我认为安全，而不是应用程序团队只是把它扔到墙上，让安全人员想出如何锁定它，我认为我们会，在一些地方，一些客户肯定会转移到安全是早期过程的一部分的地方，如果他们可以说，“这是一些测试”，那么现在护栏，他们可以贡献一些，他们可以进入这个构建过程，那么现在你真的开始转变了。

但我知道这是可能的。我们以前见过这种情况。现在 QA 是我们工作的一部分。你甚至无法想象，如果没有 QA 作为构建过程的一部分，测试很早就开始，测试计划也很早就开始，你会推出一个产品。我想安全也是如此。

阿什利:是的，当然 Tufin 在这个领域已经有一段时间了，我想他已经积累了很多这方面的知识。如果您要向新客户或现有客户提供建议，好吧，我们总是在追赶，我们现在真的在追赶，组织在如此短的时间内使用了多少云服务，有哪些最佳实践或建议，“首先要做的是确立第一件事，其次要做的是下一件事。”

是的。

阿什莉:对此有什么建议吗？

当然可以。我们有完整的爬行、行走、运行方法，旨在帮助组织采取这些小步骤来实现真正安全的环境。第一步是获得可见性，这是一种“不，废话”的说法，但这实际上是组织面临的一个大问题。您必须能够看到在您的云中部署了什么，在您的集群中部署了什么，哪些资源正在相互通信，依赖关系在哪里。

因此，理解这一点是非常重要的第一步。对于应用程序团队来说是这样，但是对于安全性来说，需要知道事情是否被适当地分割，最大的风险在哪里？所以，意识到这一点，这才是真正的爬行阶段。在走查阶段，您将了解到已部署了什么，什么与什么进行了对话，以及事情是否被正确划分，然后开始隔离。这是我们需要解决的具体问题，或者这是我们需要解决的集群，例如，专注于更高优先级的项目，并开始为这些云原生环境定义安全策略。

当您开发云原生策略时，您将与应用程序团队或云运营商分享这些策略，无论是谁负责配置这些策略。当你发展那种技能时，你必须进入运行阶段，而运行阶段就是你开始自动化的时候。您可以自动生成安全策略，自动验证安全策略，但是在最开始，大多数组织现在所处的位置是，首先获得可见性，然后是定义安全策略的第二步。不是定义我的安全组定义是什么，不是定义我的 AWS 防火墙定义是什么，而是定义我的安全策略是什么？哪些规则应该管理对某些类别的应用程序、资产和资源的访问？这是马上要采取的两大步骤。

阿什莉:我认为这是一些很棒的建议。我很好奇，有什么想法，因为我们——我想我们都想翻过 2020 年这一页，来到 2021 年，希望我们看到的是不一样的一年。但是关于 2020 年的一件事是，我不认为我们会回到过去。我们不会回到，让我们回到一月份，在那个环境中重新开始工作，对吗？远程工作或我们使用云的程度改变了一切。

展望未来 6 到 12 个月，你对 2021 年有什么期待？你是否认为这将是 2021 年还没有被讨论过但会更热门的话题？我只是在问你—

你是在问 2021 年的预测吗？

阿什利:你知道，我没看到它，但我很确定，在你的椅子后面可能有一个水晶球，只要往回看一点，然后再检查一下。*【笑声】*

**戴斯:** *【笑声】*我认为，鉴于公共云环境在市场上的成熟应用，我认为我们将会看到更多的安全团队致力于帮助保护这些云环境，而不必总是依赖传统设备。我们现在已经开始看到这一点了。因此，我认为我们将会看到更多云原生安全控制的采用。我知道组织已经看到了这样做对降低运营成本的好处，只是总拥有成本更低，还有一个好处是，当出现问题时，我可以打电话给我的云供应商，我不必担心供应商之间相互指责。所以，我认为我们会看到更多。

我认为 Kubernetes 空间可能是最有趣的，因为它在安全方面最不为大多数人所知。

阿什利:嗯。

**Dyess:** 所以，我想说也许在过去的一年里，有很多重点，就像云一样，在其上安装防火墙，我们稍后会解决微分段的问题，但稍后会很快发生，我预计在 2021 年，你会看到证券开始更多地参与到获得集群的可见性，然后寻求定义安全策略。

同样，不要试图定义单个群集的策略，而只是一般规则，因为我们无法跟上群集中实际运行的数千个服务。

阿什莉:是的。

戴斯:所以，我们会看到。我认为我们将会看到更多的组织在安全方面不得不应对变化的规模和速度，并开始参与开发团队用来管理它的自动化过程。

阿什莉:也许这是我们会更经常听到的话。如果——让我们把它看作是云原生安全性，而不仅仅是安全性，把它看作是你如何实现安全性的一种架构方法，我不会感到惊讶。

**Dyess:** 云原生。云提供商的本地控制——是的，我认为这对人们来说是一个巨大的转变。

阿什莉:是的。我们将会看到类似的事情是否会发生。我觉得你说的很有道理。嗯，和你聊天很愉快，这是我们第一次有机会聊天，而且——

是的，很高兴和你聊天，米奇。

阿什莉:非常有趣。请告诉我们人们可以在哪里了解更多关于 Tufin 的信息。

是的，当然，你可以去 Tufin.com，那是 T-U-F-I-N . com。在云方面，像与我们在这里所做的事情真正相关的东西，我们在 Tufin.com/try-securecloud 的[有很多资源。这是云原生安全控制。它旨在帮助您获得可见性并控制云原生安全组件。那里有很棒的东西，可以免费使用。人们有一个很好的尝试。Tufin.com 应该是个好地方。](http://Tufin.com/try-securecloud)

阿什利:太好了。完美。谢了。好吧，我们祝你一切顺利，2021 年更好，我们期待着。

是的。从你的嘴里，伙计。

**阿什利:** *【笑声】*

Dyess: 祝大家 2021 年好运。

阿什莉:给你。抓住那个，抓住那个。好吧，好吧，保重。很高兴与你交谈，科尔比——来自图芬的科尔比·戴斯。