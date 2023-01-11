# DevOps 聊天:现代软件工厂和 CD 管道 w/斯科特王绍博，加州汽车

> 原文：<https://devops.com/devops-chat-the-modern-software-factory-and-cd-pipelines-w-scott-wilson-ca-automic/>

这次 DevOps 聊天的特色是 CA Automic 的斯科特·王绍博谈论 CD 管道和现代软件工厂。软件工厂的概念对一些人来说可能是新的，而其他人可能听说过这个术语，但没有真正想过它的含义，还有一些人可能非常熟悉这个术语，并在自己的工作中实践过。但是软件工厂利用管道持续交付的想法是 DevOps 的核心。

这真的是一次很棒的聊天，我很喜欢和 Scott 一起参与。我希望你也能发现这一点。

像往常一样，下面是我们谈话的音频流，后面是我们谈话的文字记录。

## 声音的

[https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/tracks/417063456&color=%23ff5500&auto_play=false&hide_related=false&show_comments=true&show_user=true&show_reposts=false&show_teaser=true](https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/tracks/417063456&color=%23ff5500&auto_play=false&hide_related=false&show_comments=true&show_user=true&show_reposts=false&show_teaser=true)

## 副本

艾伦·希梅尔:大家好，我是 DevOps.com 的艾伦·希梅尔，您正在收听的是 DevOps Chat 的另一集。今天聊天的主角是我的朋友，CA Automic 公司的斯科特·王绍博。斯科特是 DevOps Chat 的常客，原因是他实际上有真正的，通常是好的东西要说，他是一个有趣的人。斯科特，欢迎再次来到 DevOps 聊天室。

斯科特·王绍博:谢谢你，艾伦。一如既往，很高兴来到这里。

很高兴你能来，我的朋友。那么，Scott，我们今天要深入研究一些我们的观众中可能有很多人非常熟悉并且喜欢深入研究的东西，但是可能有人听说过这些术语，但是他们不太确定它是什么意思。因此，我今天想谈的是管道，特别是在持续交付管道方面，以及它如何融入一个概念中–实际上，CA 创造了它，并以它为先导，但它是现代软件工厂，对企业而言。这是一种工厂方法，几乎就像一条装配线，如果你愿意，开发和部署软件和所有需要的东西。

斯科特，如果可以的话，我们从基础开始吧。什么是–当我们谈到 CI/CD 渠道时，您会如何向他人解释？

王绍博:非常好。因此，CI/CD 管道基本上只是接受任何更改的概念或隐喻，对吧，这是开发人员编写的任何更改——配置更改、数据更改以及当前对环境配置的任何更改——都需要回到起点，然后进行某种挑战，在那里对其进行审查、测试、担保，然后在生产环境中提供。有一系列的事情需要发生，这个顺序被称为“管道”从逻辑的角度来看，管道通常被分成几个阶段，但是在这些阶段中有一些特定的任务，这些任务必须按顺序发生，以使您的软件最终能够安全地部署和交付到生产环境中。

是的。听起来很棒。现在，Scott，我们已经看到的一件事情是，例如，随着 Jenkins 2.0 的出现，我认为管道和 CD 管道的概念在市场中已经真正呈现出一种新的庄严感。人们现在对此越来越认真了。在 Automic 怎么样？而且，除了 Automic，CA 的其余部分甚至？这整个管道的事情适合在哪里？

王绍博:非常好。所以，你知道，Jenkins 真的是一个持续集成工具。它意味着运行一系列“全有或全无”的任务——我的意思是，“全有或全无”，如果五个步骤中的第三个失败，那么整个构建将被标记为失败。他们意识到，“嗯，你知道，也许我们应该把它扩展到一个连续的交付的东西，即。将我们自己从仅仅构建软件中解放出来，并尝试将其推向其他环境。现在，当然，这方面存在一些挑战，所以许多供应商，包括 CA Automic 的一个自动化平台，以及其他几家供应商，都已进入该领域，帮助协调连续交付渠道，连续交付有点像是在 CI 结束的地方。

这正是 CA Automic release automation 的用武之地，它设置为从 CI 停止的地方开始编排和自动化管道，在那里构建基本上结束并将东西存放在安全的存储库中，然后它帮助将它一直移动到生产。CA，以及其他进入这个领域并为发布自动化提供工具的供应商，正在努力让相同的自动化机制在每个环境中运行，从开发一直到生产。

事实上，这是连续交付的正式原则之一——使用相同的自动化机制。如果你不这么做，你还是会把东西扔过墙，对吗？您正在错过测试、QA 和审查自动化机制本身的机会，这样您就可以对它们在生产中的工作有很高的信心，因为它们本身在新版本或即将发布的新变化之前已经测试了几十次。

很公平。很公平。现在，斯科特，我想这有点回避问题，为了理解，这个概念有多强大，你能给我们一点历史的视角吗？你知道，在管道出现之前会发生什么？在这个软件工厂的概念之前？

王绍博:嗯，对。有些事情是手动完成的。您将使用 Jenkins 来运行您的构建，不仅仅是编译您的小更改，而是重新编译它集成的所有其他部分。你知道，融合。持续集成的集成部分。并确保所做的更改不会破坏聚合应用程序。所以，一旦完成了，就真的交给了 QA，QA 会做他们的事情。有很多手动移交。电子表格被用来跟踪进度或图表。Microsoft Project 和其他 PM 工具被用来帮助迁移和管理，更确切地说，是生产路径，其中包含大量手动指令集。

以前，我在以前的生活中工作过，在那里生产环境或暂存环境会被交给一组操作团队必须遵循的指令。你可以想象，总是有问题。这些指令中总会遗漏一些小步骤，一些小配置。因此不可避免地会有错误。所以它非常容易出错和失败，实际上，我会说，所以 CD 是这方面的发展，试图以自动化、可重复、可预测的方式，以及安全可靠的方式移动事物。这就是我们进入这个市场的原因。

我会说，你知道，我在翻看一些旧笔记。很多人不知道这一点，但是，在 Automic 被 CA 收购之前，Automic 是真正启动 ARA 市场的人。我们接触了 Gartner 和 Forrester，试图向他们解释这个市场实际上是有需求的，我不会透露是哪个分析师，但是，你知道，像这样的对话，“嗯，你说的这个东西是什么？这需要自动化吗？”我们说，“嗯，我们喜欢称之为‘应用程序发布自动化’，”这个术语被分析师们所接受。因此，分析师所说的“应用发布自动化”，有趣的是，实际上来自我们，当我们开始这个旅程的时候。事实上，当我开始的时候，我和 Automic 一起，我是帮助建立这一切的团队的一部分，这很有趣，你去参加会议，我一次又一次地听到，在世界各地，实际上是全球范围内，Alan，我听到这样的评论，“哇，我们不知道有这样的东西存在。”这就是我们开始的地方。

现在，不到两年，一切都变了。两年之内，出现了几个竞争对手，Nolio、UrbanCode，它们都像 Automic 一样被收购了。当今世界已经理解了连续交付自动化的整个概念。但是，当我们开始的时候，这是新的。而且，你知道，Automic 实际上处于最前沿，并命名了这个市场，所以我认为这是-知道这一点很酷。

绝对的。绝对的。你知道，斯科特，我只是坐在这里，想，你知道，我们都在这个行业很长一段时间了，所以，在 90 年代末，网络时代，我帮助创办了一家名为“Interliant”的公司，我们是早期的 ASP 之一。对吗？我们做了 Lotus Notes 托管和 PeopleSoft 托管，Oracle apps，以及其他一些已经不存在的软件，但这是在云出现之前。我们必须定制每一个安装，每一个——你知道，因为应用程序需要定制。我只是在回想当时我们是如何开发和部署的。首先，你知道，这似乎是 100 年前，而不是 20 年前，但当你想到我们在如此短的时间内所看到的变化时，这是令人惊讶的。

王绍博:是的，但是你知道吗？很有趣，艾伦。所以我也记得那些日子，周末工作和进行大规模部署的痛苦，但现在有趣的是，我们看到所有的事情都变了，但许多事情仍然保持不变。Alan，在我访问的许多大型企业中，他们都在使用新的基于云的应用程序进行开发运维，持续交付，甚至他们还在使用一个大型应用程序，比如他们为一家银行开发的在线银行应用程序，我不会说出这家银行的名称，他们正在 Node.js 中重写它。太好了。他们这样做是因为它在云中。他们能够做所有这些新的事情-敏捷、开发运维、持续交付-但他们仍然在后台的应用程序中拥有所有这些基础架构，我称之为“经典架构”，对吗？你的 IIS，JBoss，WebSphere，WebLogic 等等，客户端服务器。然后你还有你的遗产——你的大型机，也许还有大型的打包系统，比如 Sable 等等。

因此，尽管他们正在做很多事情，我们听到了很多关于新的做事方式的信息，但我访问的许多企业仍然没有走上这条道路，因为他们还没有在云中迁移太多的东西，他们仍然在按照艾伦，你和我在 90 年代看到的方式做事。

**Shimel:** Mm-hmm.

**王绍博:**从某些方面来说，这是一种恐慌。这种恐惧就像，“嗯，你永远不知道，伙计。如果事情败露，将会有很多钱处于危险和危急之中”，所以他们改变得很慢。我要告诉你的是，在我第一次开始我的旅程的这些年里，大约八年前，甚至就在去年，它有点——我不想说令人耳目一新，我不想说令人惊讶，但它确实令人大开眼界，看到许多大企业基本上仍然以他们在 90 年代末的方式做事。

**Shimel:** Yep.

王绍博:他们在问，“我们如何前进？我们如何做到这一点？”

**Shimel:** 同意。

王绍博:所以，艾伦，所有这些新东西都不是既定的，我想这就是我想说的。

不，这不是给定的。这不是必然的。但是你也必须问问你自己，斯科特，对，从根本上说，这是一个生存威胁，还是对那些没有跟上形势的公司的生存的威胁，对吗？斯科特，你看到的是，坦率地说，可能有些行业、公司和企业并不那么重要。对吗？重要。他们可以做他们想做的事情，如果他们不接受，他们就不会接受，这没关系。你需要——你知道，他们可能永远不会采用这些做事方式，这可能不会产生巨大的影响，但我认为，对于这些组织中的绝大多数来说，我的意思是，如果他们不能跟上形势，他们就真的开始落后了，我认为这就是我们今天在市场上看到的情况。

王绍博:绝对是。不适应就有危险。如果他们不改善他们的客户体验，他们绝对会发现自己要破产了。我记得在 90 年代中期读过很多关于比尔·盖茨的报道，他是多么疯狂地关注和担心他可能会在两三年内破产。当我很小的时候读到这篇文章，我想，“哇，这是一个很好的教训，第一，但是，第二，我认为他有点夸大其词了。”他没有。结果，正如我们从 2000 年以来所看到的，大公司已经消失了，这是非常重要的，那些还没有开始这样做的组织开始现代化他们交付软件的方式。他们必须这么做。

**Shimel:** 明白了。明白了。我想我们会看到这一幕，对吗？就像“要么发展，要么死亡”或者随便你怎么称呼它。不管怎样，斯科特，我们快没时间了。在我们结束之前，有什么来自 Automic 的消息可以和我们分享吗？

**王绍博:**很明显，我们有新的东西出现，但我真的认为新的东西——它并不那么新，但我加入 CA 后感到非常兴奋的一件事就是现代软件工厂的整个概念，加入 CA 后，Automic 团队是这一战略不可或缺的一部分，他们正在努力帮助这些大型企业，对吗？因为企业，就像我说的，不是云原生的东西。他们有所有的古典和传统的东西，他们想登上持续交付，他们也在努力。

关于这个现代软件工厂的整个事情，我认为更多的是集中在工具上，对吗？这是 DevOps 和连续交付的另一个层面，它着眼于组装和组织工具，使您的所有平台以连续交付的速度运行。这肯定是可能的，但我对这个现代软件工厂以及我们可以帮助 CA 实现它的地方感到非常兴奋和充满激情。我认为这真的是一个很好的心态，是啊，这整个想法就是你只需在一端插入你的输入，而你的目的地在另一端，让事情发生并让你到达希望之地。

是的。我听到了。好吧。斯科特·王绍博，感谢你作为这一集的嘉宾来到 *DevOps Chat* 。希望你很快回来。我知道你在做一些事情，斯科特，在适当的时候，我们会让你在这里向世界简要介绍一下，但是，在那之前，跟你聊聊总是很棒的。CA 和 Automic 取得了巨大成功，我们很快会与您联系。

王绍博:听起来不错，艾伦，在每年的这个时候，我只会说，祝你好运。*【笑】*

席梅尔:对外面的每个人都是。好吧。嘿，斯科特·王绍博，加州汽车软件公司，你今天 DevOps 聊天的嘉宾。我是艾伦·希梅尔，您刚刚听到的是 DevOps 聊天。祝大家今天愉快。我们很快会再见的。

— [Alan Shimel](https://devops.com/author/ashimmy/)