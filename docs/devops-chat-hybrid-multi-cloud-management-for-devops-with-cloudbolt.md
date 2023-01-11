# DevOps Chat:使用 CloudBolt 为 DevOps 提供混合、多云计算管理

> 原文：<https://devops.com/devops-chat-hybrid-multi-cloud-management-for-devops-with-cloudbolt/>

敏捷、开发运维、多个云提供商、无服务器、当代云原生应用、使用信用卡的影子 IT–任何 IT 组织都难以响应内部客户需求。更难的是要积极主动，走在时代的前面。进入云管理平台(CMP)。

在本期 DevOps Chat 中，我们将与伯纳德·桑德斯——不，不是总统候选人——cloud bolt 的首席技术官进行对话。我们的对话探讨了 IT 如何使用 CMP 来提供 IT 和自助服务功能，以便开发人员和敏捷团队不会感受到过去的痛苦和缓慢。

像往常一样，下面是流媒体音频，然后是我们的谈话记录。

[https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/tracks/639713814&color=%23ff5500&auto_play=false&hide_related=false&show_comments=true&show_user=true&show_reposts=false&show_teaser=true](https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/tracks/639713814&color=%23ff5500&auto_play=false&hide_related=false&show_comments=true&show_user=true&show_reposts=false&show_teaser=true)

## 副本

米奇·阿什利:大家好。我是米奇·阿什利和 DevOps.com，您正在收听的是另一个 DevOps 聊天。今天，我邀请到了 CloudBolt 的首席技术官 Bernard Sanders。我们今天的主题是面向混合和多云环境的 DevOps。伯纳德，欢迎来到 DevOps 聊天室。

伯纳德·桑德斯:谢谢你，米奇。很高兴来到这里。

阿什莉:非常高兴你能上播客。你能从自我介绍开始吗？告诉我们一些关于你和 CloudBolt 的事情。

**桑德斯:**当然可以。我是 CloudBolt 的首席技术官兼联合创始人 Bernard，我职业生涯的大部分时间都在数据中心自动化/开发运维/云管理领域度过，从 2000 年我进入该行业开始，这个领域在各个时代都广为人知。我已经看到了许多不同的企业 IT 部门以及它们是如何工作的——什么顺利，什么出错。我在 IT 商店、金融服务行业、零售和政府部门呆了很长时间，看到这些行业之间的共性很有意思。

正是通过对这些共性的观察以及与我的一位同事 Augie 的交谈，我们决定在 2011 年启动 CloudBolt 软件，并开始开发该软件，在那一年发布了第一个 GA 版本。CloudBolt 是一个混合云管理平台，有时也称为 CMP。从本质上来说，它可以帮助拥有数据中心并希望使用公共云的大型组织。这有助于他们通过一个界面同时使用这两种产品。

阿什利:酷。嗯，首先，我不得不称赞你——任何有一个叫 Augie 的朋友的人一定是个好人。

**桑德斯:** *【笑声】*

阿什莉:奥吉听起来是个不错的人。*【笑声】*所以，这就像，有点像是从你的车库开始，有点像是从你们两个最初开始并使这家公司运转起来的地下室类型的创业公司？

桑德斯:基本上就是这样。我们有一个优势，那就是我们当时在华盛顿特区外的一家名为奥古斯特·谢尔的咨询公司工作，我们将这家公司从奥古斯特·谢尔分离出来。因此，一开始，我们两人和我们带来的其他人能够专注于技术和解决方案，去争取一些客户，我们不必太担心后台办公室的事情——人力资源和薪资。我们在很大程度上依赖母公司的基础设施，所以—

阿什利:不错。所以，这是从母体中衍生出来的。

桑德斯:没错，没错。

阿什莉:非常好。好吧，你知道，并不是每个人都以云原生格式开始做云应用，甚至只是在一个云中。你知道，我们经常被复杂性和现有的应用程序所拖累，我不是说这不好，这只是业务的现实，或者我们是向云迁移的数字化转型的一部分，这就是我们获得混合和多云环境的原因。

您看到了哪些挑战，促使您开始“让我们创建这家公司，构建这个云管理平台。”

桑德斯:对，对。所以，这里有几个方面需要讨论，你知道，你提到的第一点是，不是每个人都有启动绿地的奢侈。你知道，如果你用几个人和几个对服务器的需求开始一个全新的软件公司，你可以用最新的技术完全集装箱化，无服务器。但是我们接触的许多公司仍然问我们，“哦，你们支持大型机吗？你支持艾克斯吗，你支持 HQX 吗？”*【笑声】*这些问题的答案都是否定的，对我们来说，你知道吗？我们得划清界限。但是在这些企业公司里有一条很长的技术尾巴。需要稳定性和连续性，他们不能放弃一切，将所有应用程序迁移到最新的平台。

阿什利:你知道，我喜欢说一代又一代的技术永远不会消失。

**桑德斯:**没错。

阿什利:这可能是我大学毕业时写的代码，想想就够吓人的了。但没错，的确如此。你必须适应你所拥有的。我们不能重写一切。

**Sanders:** 你知道，你问题的另一部分是，我们看到了什么问题促使我们创建 CloudBolt，Augie 和我每次去这些大型机构时，我们都看到大型公司或组织的 IT 部门与其最终用户之间的沟通出现了故障。

阿什莉:我听说过这种事。我从未见过，但我听说过。

**桑德斯:** *【笑声】*耶。这种事情发生得太多了，几乎成了一个笑话，但你知道，如果终端用户想要在他们的私有数据中心或有时甚至在公共云中获得一个虚拟机，他们将不得不为此开一张罚单。然后，IT 团队必须执行许多手动步骤，而且团队之间经常会有许多交接工作，以最终构建出该环境或单个虚拟机或网络存储，然后将其返还给用户。这是一个黑匣子，每个人都会对彼此感到沮丧。

阿什利:嗯。

桑德斯:我们认为——应该有更好的方法来做这件事。

**Ashley:** 那么，组织如何更有效地合作，让我们也梳理一下这方面的云计算和混合云。那么，多重云，你会不会发现这是因为有些东西是自己启动的，不同的团队会出去，有些人从 Azure 开始，因为它们是微软的代码，有些人从亚马逊或谷歌或其他地方开始，然后有一天，其他人会说，“为什么我们不把这些放在一起？”或者它更像是一种意识，“不，我们需要这些不同的云环境是有充分理由的，所以让我们为如何实现这一点制定一个有凝聚力的策略或架构？”那些东西是如何进化的？

桑德斯:我认为两者都是。我会说大概是 60/40。很多时候，公司会说，“哦，我们都在亚马逊上。”然后他们去收购另一家做 Azure 的公司，再收购另一家做其他东西的公司。所以，很多时候，就是那种无意的成长。

阿什利:嗯。

**Sanders:** 但我越来越认为，你会看到每一个云提供商，他们随着时间的推移都在分化，他们都有自己的优势和劣势。因此，说“嘿，我们将在这一方面使用谷歌云，在另一个使用案例中使用 AWS，因为这是这些平台的强项”是完全正确的

**阿什利:**有意思，有意思。那么，谈谈混合动力部分吧。你知道，每当有新的一代或新的发光物体，它就像，一切都将去那里。因此，所有东西都将被云覆盖，当然，许多东西已经被完全覆盖，有些东西只是部分覆盖。

**桑德斯:**嗯嗯。

阿什莉:而且这种需求总是存在的。例如，您谈到了大型机。有必要拥有一个混合环境。您如何定义混合环境？

**Sanders:** 是的，所以我将混合定义为同时使用私有云与公共云。因此，私有云意味着您自己的数据中心，或者，您知道，可能是您托管或以某种方式出租的数据中心。但基本上，你自己的设备，你自己的硬件和基础设施，但同时也使用公共云。你知道，我认为这是过去五六年来最大的挑战之一，如果你回到五六年前，听许多行业分析师说，你会认为我们会在一两年后退出公共云。否则我们会被解雇—

阿什利:私人的，是的。

桑德斯:–那会彻底灭绝。

**阿什利:**当然。

**Sanders:** 我们将完全使用公共云。但我认为这是不切实际的期望。今年早些时候，高盛的一项研究表明，26%的工作负载位于公共云中。所以，剩下的很大一部分仍然是私有环境中的绝大多数。

对混合动力车的需求越来越大，你知道吗？人们不想完全不连贯地使用两者，他们想以某种方式一起使用它们。这就是我所说的混合云。

**Ashley:** 这为我们讨论云计算管理平台提供了一个背景。为我们定义一下，什么是云管理平台？

**Sanders:** 是的，云管理平台是一种工具，它可以提供单一平台或界面以及 API 来管理不同的 IT 环境，可以是公共云、私有云、容器、虚拟机、物理环境。它可以包括无服务器，它可以包括公共云服务，以及基本上任何您对它的请求。这就是我所说的云管理平台或 CMP。另一个主要特征是，it 需要为终端用户提供自助服务。它必须是一种工具，最终用户可以自己去获得他们想要的东西，而不是要求 It 为他们做这些。

**Ashley:** 实际上，IT 不仅能够管理其环境，还能够提供门户访问，如果你愿意，如果你这样想，人们可以在任何地方进行自助服务、API、STK，因此开发运维团队可以绑定到该平台。

**桑德斯:**正是。没错。

阿什莉:好的。所以，我们去那里吧。让我们来谈谈 DevOps 如何融入—它想要组织事情，对吗？IT 部门希望能够参与其中，并且至少能够管理—您知道，不一定是控制或约束，但是您知道，他们要对组织中发生的技术负责，因此，他们希望对此进行某种形式或表面上的管理控制。

你如何做到这一点，同时让 DevOps 团队茁壮成长？

**桑德斯:**没错。是的，所以，真正重要的是让 it 团队为他们提供一个工具，让他们可以制定政策、制定标准，但向这些团队的不同部门或团队公开一个或多个接口，让这些团队中的开发人员在需要时获得他们需要的东西，并在 IT 部门提供的基础上自动化他们想要的东西。

因此，在大多数云管理平台的情况下，IT 团队将带来它，购买它，安装和设置它，然后将该 UI 和 API 公开给能够针对它进行编码的这些部门。例如，某个特定部门的 DevOps 团队可能有一个 CI/CD 管道，它调用 IT 部门公开的云管理平台。

所以，两个群体都被赋予了权力。IT 部门负责设置配额、审批流程和主机名称标准，例如，与云计算管理平台内的所有策略相关的内容，终端用户和开发人员可以在需要时调配所需资源。

**Ashley:** 我不想让它听起来像是灵丹妙药，但听起来这将是一个 it 组织的一条道路，他们可能已经失去了控制，或者感觉不到他们已经掌握了组织中正在发生的一切，他们可以成为云计算基础设施资源的提供商。

**桑德斯:**绝对是。

阿什利:这可能是他们的一条道路，走在正在发生的事情的前面，而不仅仅是反动。

桑德斯:当然，是的。我们看到的另一个影响是，无论是 CloudBolt 还是不同的 CMPs，私有数据中心在接口方面都落后于公共云。比如，去亚马逊控制台或谷歌云订购一台虚拟机，这是一个相当简单、相当自助的过程。OpenStack 或 VMware 和 Nutanix 则不是这样。我知道它是人们使用的私有虚拟化系统之一。

拥有云管理平台可以将您的私有数据中心提升到类似于公共云的水平，人们可以在私有数据中心进行自助服务，而不再仅仅是公共云。

阿什利:好吧，冒着我听起来像是快乐的耳朵和扔给你软球的风险—

**桑德斯:** *【笑声】*

**Ashley:–**实施 CMP 最困难的部分是什么？

**桑德斯:** *【笑声】*

阿什利:这不可能是所有的玫瑰和，“这里有一张信用卡和下载——噗，你的 NPS 分数从 10 到 56。”

桑德斯:哦，我只能说出一样东西吗？

阿什莉:是的。*【笑声】*从“生活很艰难”到“现在我们有了这个平台，我们的处境好多了”，有哪些挑战？

桑德斯:是的。因此，对于引入云管理平台的人来说，我认为挑战往往不是技术性的，而是组织性的，因为它影响了如此多的不同群体。你必须让人们接受，“嘿，我们要做这件事。我们将把它作为我们的通用接口。”这很有挑战性。我认为如果界面是好的，它会变得更容易，你让它更有吸引力，更强大，并在界面上给他们所需要的东西，人们就会来找它。但是，在这些大型组织中进行任何形式的变革仍然是困难的。

阿什利:那么，在中型或大型的小型组织中工作更容易吗？我可以想象，在大型企业中，制定标准和流程可能更容易，或者中型企业可能更难，因为养猫更难？我不知道，你有什么经验？

桑德斯:这是个好问题。我认为，一般来说，任何时候你把更多的人聚集在一起，就很难做出改变，也很难让他们做同样的事情。是的，如果你在一个大组织中有高管的支持，这可以使事情变得更容易，但我认为调动更多的人比调动更少的人去做新的事情更难。

阿什莉:好的。因此，另一个更难的问题是——为什么 CloudBolt 比市场上的其他 CMP 更好？为什么是比较好的捕鼠器？

**桑德斯:** *【笑声】*好问题。你知道，我自己不做很多竞争分析，但我从我们的客户那里听说，他们可以安装并运行 CloudBolt，并比其他平台更快地从中获得价值。你知道，我们以前做过演示，在演示结束时，你知道，在 GoToMeeting 或 Zoom meeting 中，或者我们向客户展示产品时，他们会问我们，“哦，X 按钮在哪里？”我们必须停下来说，“等等，那边怎么了？”在半小时内向他们演示所需的时间内，他们已经下载、安装、连接到他们的 VMware 环境，就像是在调配虚拟机。我认为这是一个相当不错的酒吧，我们在消费能力方面达到了目标。他们还谈到可扩展性非常强大。

我们试图建立各种各样的挂钩点和扩展点，让他们能够扩展它来做他们需要它做的任何事情。许多这样的 IT 部门都有非常具体的要求、系统、标准和运营方式，所以他们喜欢这种可扩展性。

**Ashley:** 嗯，做敏捷的团队，DevOps 团队，你知道，他们围绕他们建立一个环境，在那里他们可以快速执行，因为他们可以快速访问资源，你可以去亚马逊信用卡——噗，我什么都有。围绕他们建立这样的流程和环境是非常好的。当然，我们会遇到让他们慢下来的事情，比如说，或者一些新的东西，闪亮的新 CMP 之类的东西。

你如何让一个 DevOps 团队参与进来，他们去亚马逊、谷歌和 Azure 以及其他任何人那里获得他们需要的东西，而现在他们需要通过摆在他们面前的这个 IT 东西？

桑德斯:是的。我认为，真的，你需要做的是解决他们遇到的问题，而 CMP 就是这样做的。你知道，当他们看到一个界面，一个可消费的 API，符合他们的标准，并允许他们部署到任何不同的云和私有数据中心时，通常没有比这更有说服力的了。他们说，“哇，我们不得不建立它，”因为我们刚刚被授权做两个不同的云或者做 VMware 加 Azure。

现在，我们不必自己去做，这很好。我们可以构建更多的功能，只需在这个伟大的平台之上构建。

**Ashley:** 你能进来与现有的自主开发的自动化系统合作吗，或者他们是否已经开发了一些构建和自动化工具来部署代码和云？你能使用 DevOps 团队已经设置好的工具工作吗，或者你必须重新调整他们正在做的部分工作吗？

桑德斯:通常很少重组。通常会发生双向整合。你知道，如果有人要在 Jenkins 或 Concourse 构建管道，他们经常会调用 CloudBolt 来完成这些构建，如果他们自己直接调用基础架构来完成这些工作，他们有时可以消除系统的一些复杂性。

然后，类似地，CloudBolt 可以调用他们现有的工具。我们的许多客户都有自己开发的云管理或变更管理数据库(CMDBs ),他们希望 CloudBolt 在配置过程中的某个时候调用这些数据库，以便在其中注册新的服务器或 CI。

阿什利:嗯。你的产品下一步会发生什么，你会把它带到哪里？

**Sanders:** 云管理领域正在发生许多事情，你知道吗？这个领域还不算太老，所以它仍在定义自己，行业仍在寻找他们需要这种工具的原因。因此，我们引入了更多的成本管理和分析，向您展示您的公共云支出是多少，您可以节省多少，并为您提供如何节省的建议。所以，这是一个常见的改进领域，继续使它变得越来越可扩展和可消费，当然，加倍我们的容器化支持，我们在 2015 年开始支持 Kubernetes，我们在每个版本中都提高了这一水平。

此外，除了支持公共云提供商的所有不同发展方向，他们还试图进行分流；我们试图提供一个公共平台。因此，这是我们要解决的一个持续的挑战，这是一个有趣的挑战，也是工程团队蓬勃发展的一个挑战，它为人们提供了一个与日益不同的底层技术的通用接口。

**Ashley:** 我可以想象，很明显，你为 Kubernetes 到 Jenkins 或任何在 DevOps 环境中使用的下一代神奇工具提供的工具支持越多，就越好。此外，如果您正在解决“这是日志聚合，这是审计跟踪，这是开发运维团队不必设置的访问控制”的问题，这将是—您可以通过编程接口来完成—这对他们来说将是一个胜利。

**桑德斯:**绝对是。是的，安全性也是我们越来越关注的焦点，通过提供工具和集成，他们可以确保部署的每个虚拟机都符合标准和合规性，并且可以获得整个企业的安全报告。

阿什利:是的，如果你能帮助他们通过安全审计或审查，我想他们会喜欢你的。

**桑德斯:**是的。

阿什利:如果我们愿意，我们可以再谈 40 分钟。不幸的是，我们没有那么多时间。感谢 CloudBolt 的 Bernard Sanders 加入我们。

桑德斯:谢谢你，米奇。真的很开心。

阿什利:我想感谢我们的听众，当然，感谢他们今天和我们在一起。我是 DevOps.com[的米奇·阿什利。您已经听到了另一个 DevOps 聊天，在那里要小心。](http://DevOps.com)

— [米切尔·阿什利](https://devops.com/author/mitchellashley/)