# DevOps 聊天:Rundeck，把行动在 DevOps，与达蒙爱德华兹

> 原文：<https://devops.com/devops-chat-rundeck-putting-ops-devops-w-damon-edwards/>

在这次 DevOps 聊天中，我们采访了 Damon Edwards， [Rundeck](http://www.rundeck.com) 的联合创始人兼首席产品官。我想说的是，Rundeck 将运营放在 DevOps 中。但是达蒙不需要向那些熟悉 DevOps 的人介绍。他是 DevOps 社区的早期领导人之一，并继续在世界各地传播 DevOps。事实上，他将于 7 月 25 日在新加坡 RSA APJ 的 DevSecOps 活动上发表演讲，您可以在这里找到。

我个人一直希望达蒙能成为 DevOps Chat 的嘉宾。除了是一个伟大的采访，达蒙和 Rundeck 是一个伟大的故事，一个开源项目有机增长，催生了一个伟大的商业业务。这比你想象的要难，达蒙在这次采访中告诉了我们一些。

和往常一样，流媒体音频在下面，文字稿在下面。尽情享受吧！

## 音频

[https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/tracks/332867040&color=ff5500&auto_play=false&hide_related=false&show_comments=true&show_user=true&show_reposts=false](https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/tracks/332867040&color=ff5500&auto_play=false&hide_related=false&show_comments=true&show_user=true&show_reposts=false)

抄本

艾伦·希梅尔:嗨，大家好，我是《DevOps.com》的主编艾伦·希梅尔，我们在这里进行另一次 DevOps 聊天。我们有一位非常非常特别的嘉宾参加这次 DevOps 聊天，他是我在 DevOps 运动中的英雄之一，从我第一次开始研究 DevOps 是什么以及它是关于什么的。我很高兴他能出现在我们今天的 DevOps 聊天中，不是别人，正是达蒙·爱德华兹。达蒙欢迎。

达蒙·爱德华兹:谢谢你，艾伦。谢谢你邀请我，也谢谢你的赞美，我很高兴来到这里。

**Shimel:** 谢谢。所以达蒙，我猜我们的观众中有很多人听说过达蒙·爱德华兹，他在组织 DevOps 日方面发挥了重要作用，尤其是在硅谷的 DevOps 日推动了这一趋势多年。达蒙，你有几家不同的公司，既有开源公司也有咨询公司，可能还不止这些，你已经出现在多少个不同的 DevOps 日活动或其他 DevOps 相关活动中，你在这些活动中发表过演讲。我是说，你知道吗？你跟踪了吗？

爱德华兹:我不知道，*【笑】*。我知道它比约翰·威利斯少，因为他在我们的播客中提醒了我，但 DevOps Café，我将为此给出一个交叉插头。艾伦，我们只是邀请你作为嘉宾，你太棒了。是啊，我算是幸运地来到了正确的地方/正确的时间。我们对如何快速发展非常感兴趣——我们内部称之为 Dev2Ops，我们过去称我们的咨询业务为 d to 解决方案。这实际上是关于如何帮助组织更快地发展？很长一段时间，规模是个问题。嘿，你是怎么部署的，连上一千台服务器，对吧？一千台服务器曾经是件大事。然后突然发现，嘿，我们可以将任何东西部署到任何地方，这不是真的-部署规模不是真正的问题，速度才是问题。组织不能足够快地移动，管道被堵塞，组织就像被水泥卡住了一样。那些能够解放自己，分离自己，并以这种新的快速方式前进的组织拥有战略优势，他们真的打败了那些被束缚在原地的传统大公司。

所以我们开始问自己，为什么会这样？我们的客户开始问我们，为什么会这样？这真的让我们进入了精益和所有这些事情。与此同时，约翰·奥斯鲍在《速度》杂志上发表了他的重要演讲，我看到，你知道，约翰·威利斯和撒切尔·迪布瓦以及其他人都赞同，于是德沃普斯运动诞生了。我们被认为是那些擅长采用你在舞台上看到的设计模式，并将其转化为大企业的人。这就是 DTO 解决方案。

然后，在这个过程中，我们有一个名为 Rundeck 的附带项目，这是一个开源工具，我一会儿会谈到它，但它真的刚刚起飞。过了一段时间，有足够多的人打电话给我们关于 Rundeck，我们真的很兴奋，有两个原因为什么我们决定双脚跳进 Rundeck。首先，我觉得运营是 DevOps 尚未真正探索的前沿领域。我认为在许多大型组织的开发方面，他们让开发更好地与 QA 沟通，他们让构建管道运行，小的开发测试周期变得更快。也许部署会快得多。但是这些 DevOps 原则还没有真正进入全面运作模式。许多大型运营组织还未能实现自我转型，我们看到了 DevOps，尤其是 Rundeck 作为一种工具正被用来实现这一点。首先，我认为我们本质上一直是产品人，我们想看看我们能把它带到哪里。但第二，我真的觉得它有助于推动 DevOps 运动到一个新的地方。

是的，我同意你的观点。达蒙，再补充一点颜色，你实际上有一个视频，这是 DevOps 的简史。对于任何真正想知道 DevOps 是如何开始的听众，我强烈推荐达蒙的一个很棒的视频。但是让我们跳到甲板上。达蒙，正如你提到的，这是你和 DTO 合作的一个附带项目。它是开源的，不是吗？

是的，Rundeck 的核心是它是一个开源产品，一个开源社区。我想上次我们做了一些估算。大约有 25，000 个不同的开源用户。所以它变得有点沉默——对我们来说，我们有一天醒来说，哇，很多人真的在使用 Rundeck，他们打电话给我们说，“嘿，我们真的想用 Rundeck 做更多的事情，”这导致了现在 Rundeck Inc .的形成。

如果你想谈论 Rundeck 实际上是什么，从根本上说，从技术角度来看，它是一个编排和调度平台。目前，许多流程编排发生在不同的孤岛中，因此有容器流程编排、配置管理流程编排，诸如此类。有企业作业调度程序。但我们注意到，随着人们转变他们的运营组织，这一层需要跨越所有不同的工具孤岛、所有不同的自动化孤岛以及所有不同的系统。他们希望创建跨越所有这些不同孤岛的程序和操作程序。他们希望有一个地方，可以使用他们想要的任何脚本语言来定义这些过程。他们希望能够定义工作流，他们希望能够围绕工作流设置安全性，这是非常重要的，因为许多人在这些程序中所做的不仅是帮助他们的运营团队更加高效和有效，而且他们开始开放更多的自助服务模式。我认为自助式运营是真正推动我们前进的大设计模式。

也就是说，在我的整个组织中，所有这些需要做运营工作的人，当我开始转变我的组织时，我如何安全地让他们做可能是部署的事情，但通常是补救活动、诊断工作，只是做我需要做的运营工作，我如何让运营团队定义并负责这些工作，并决定谁可以在何时何地做什么，但允许其他人参与？我所说的参与，意味着两件事。一种是给他们按钮或 API，让他们自己去做他们需要完成的操作性工作，但也给他们一种机制，让这些不同的团队(通常在不同的业务部门)可以为他们自己创建的工作定义那些操作性程序，然后有一种标准的机制将其交给运营部门，运营部门和安全部门可以审查他们，然后运营部门和安全部门的审查流程可以转而允许其他团队访问。这就像我们如何让操作分离，让更多的人参与到操作中，并以一种安全、理智、可靠、审计和记录的方式来完成这一切？这就是 Rundeck 的亮点。

**Shimel:** 明白了。我是说，达蒙，你在这里打开了一堆不同的东西我希望你能充实一下。所以第一就是整个行动计划，对吧？我个人的观点是，在很长一段时间里，DevOps 都是以开发人员为中心的，实际上，归根结底，由于各种不同的原因，尤其是在我们生活的这个世界中，Ops 才是它所在的位置。很明显你在里面工作。但我们不是要重建发射井，对吧？有开发团队的位置吧？他们在 Rundeck 内部与运营人员进行互动，对吗？这不仅仅是为了行动。

**爱德华兹:**对，对。如果你看看今天的组织，这又回到了我们之前的说法，即规模不再是问题，但组织速度是导致 DevOps 运动的问题。如果你看看运营中发生了什么，这是非常相似的事情。导致问题的不是基础架构的规模，而是组织的复杂性和规模。因此，在许多大型企业中，几乎每个大型企业都有一个叫做运营的中心。在这一点上，把团队放在一边，想想运行所有这些东西的动作。你有所有这些不同的活动流进入这个中心，所有这些活动流必须结合在一起形成这个企业。这就是操作。这就是生意。所有的钱都是在那里赚的。所有这些开发活动，本质上都是供应商的一部分，所以下一个版本，机器中的下一个齿轮必须运行，但这一切都必须结合在一起，否则我们就赚不到钱，除非你真的卖软件，而现在很少有公司这样做，你运行服务就是业务。所以运营很重要。但同样，运营，因为事情是如此紧密地耦合在一起，而且都落在一个通常是中心的团队身上，这就成为一个巨大的瓶颈和大问题，最终真的会阻碍或阻碍开发运维。这些组织想要实现的分离转型被传统运营领域的僵化所阻碍。

因此，我们看到这些飞得很高的组织，他们现在正在做什么，高绩效者，他们正在做的是如何打开和分离所有运营活动的框架。在这样做的过程中，他们意识到你正在做的事情有三个关键部分。有能力——谁来定义程序？谁为他们将要运行的东西定义程序。第二个问题是，谁可以通过 GUI 或 API 按下这些过程的按钮。第三，谁拥有该行动的辅助或操作、管理控制权？

传统上，所有这一切都落在一个小组或一个团队身上，他们的数量远远超过了组织中的其他人，这成为了一个大的运营瓶颈。他们的整个心态就是让我们保护自己不被蹂躏。让我们保护自己，因为人们把事情推给我们，他们真的不知道所有的事情将如何结合在一起，他们没有定义事情的责任。因此，ops 处于非常非常艰难的境地，并尽了最大努力。我们看到这些组织做了一点汤姆·索亚油漆我的篱笆或柔道动作，说，嘿，让我们重新定义谁在哪里做什么。让我们接受这个定义。让这些队伍。他们创造了这些东西，让我们允许他们参与这些操作程序的定义。然后，让我们也让他们按下那个按钮——对于某些事情，而不是所有事情——也许只是某些非破坏性的事情，或者也许某些团队可以部署，但某些团队我们不想部署，因为这是不同类型的系统或不同的安全要求。您可以移动这些内容，最终您可以保留第三部分，即管理、法规遵从性和审核安全控制，由想要控制这些内容的传统运营组织、传统运营技能组合或管理技能组合来完成。

因此，在这种自助服务设计模式中，它是关于将这三件事情划分开来，即自动化的定义、自动化的执行以及对自动化的管理安全合规性控制，并允许将这些事情转移到组织中对业务流程、速度、利用您所拥有的劳动力最有意义的部分。这些运营组织正在用这种心态来转变他们的组织。当我们看到这种情况发生时，我们喜欢，哇，这真的很酷，我们和 Rundeck Inc .一起跳了进去。

绝对的。让我们谈谈你所说的 Rundeck 公司。那么达蒙，是九个月前，或者更久，或者一年前，你和你的——我一片空白，我道歉——

爱德华兹:亚历克斯大人。

没错，亚历克斯·奥诺瑞，从我认识你开始，你和亚历克斯就一直在跑甲板。但大约九个月或一年前，你引进了一位职业 CEO，一位我认识多年的人，一位在硅谷工作的了不起的人，斯蒂芬妮·福恩，作为你的 CEO。它真的从 Rundeck 的 DTO 解决方案的一个附属项目变成了 Rundeck 公司。

爱德华兹:是的，我们跳得很快。我们幸运地签下了斯蒂芬妮，这对我们来说是一个巨大的成功。我想她把我们的情况描述为“财富的尴尬”，我不确定她强调的是尴尬还是财富。我们创办了现在的 Rundeck 公司，作为一种实验，看看会发生什么？这是亚历克斯，我自己，格雷格舒勒，作为 Rundeck 的首席开发人员。亚历克斯是 Rundeck 项目的创始人。我们有一个小团队，我们有一些分散的工程师，一切都在运转。但接下来，我们发现有一大堆大型企业在向我们支付 Rundeck Pro 的早期版本，这是一种企业增强版。如果你大规模地做这些事情，有各种各样的特性和额外的插件真的很重要。开源的真正定义是，如果你只是一个团队，你需要定义按钮和按钮，那么开源是全功能的，并为你服务。Rundeck Pro 实际上是在它的周围和顶部添加一些老板和大组织关心的东西。

所以我们抬头一看，一切都很好。斯蒂芬妮进来说，嘿，我们这里真的有一些东西，我想成为其中的一部分。所以这对我们来说是一个重大的突破。她在房子的安全方面是非常有名的，在那里有许多伟大的成功。她发现运营和安全是非常相似的思维模式，非常相似的人群，她真的很喜欢它。是的，很好，她带来了更多的专业人士。

Shimel: 它已经成长为一家公司。

**Edwards:** 是的，到目前为止，我们已经有了 50 多家企业客户，而且我们在快速增长，所以这是一次非常酷、非常有趣的经历。

**Shimel:** Damon，你现在在 Rundeck Inc .的角色，如果我们可以这样称呼它的话，就是你是首席技术官，显然也是联合创始人，但你是首席技术官，也是传道者，但你的手仍然会在与客户交谈和提供帮助时弄脏。

爱德华兹:是的，我会说这是我正在做的大部分事情。事实上，亚历克斯是首席技术官，我想我是首席产品官，或产品负责人，这些名字，你知道，这是一个典型的初创公司，对不对？我非常注重宣传，非常注重产品方面，非常注重帮助客户弄清楚，首先，弄清楚他们在用 Rundeck 做什么，其次，帮助他们弄清楚他们想从 Rundeck 得到什么，并推动其向前发展。因此，我仍然密切参与 DevOps 社区，并在路上做这些事情，因为我相信这是下一个前沿，这是你必须去的地方。理顺您的部署管道并在其中进行自动化测试是一件很棒的事情，但是如果您是任何规模的任何组织，这是下一个主要问题。您需要转移运营，否则您将无法真正实现 DevOps 的全部愿景。这些公司比你有明显的优势。

达蒙，你知道吗，对我来说，DevOps 仍然很像是一个目标，你解决了一个瓶颈，却发现了下一个瓶颈。这就是我们所做的，我们不断击倒他们。当你打倒一个，另一个就会出现。我认为这就是我们在 DevOps 中看到的，随着我们在 CICD 领域和配置管理领域消除瓶颈，Ops 成为下一系列瓶颈所在，这显然是 Rundeck 在那里遇到的问题。

达蒙，我想谈谈其中的一部分，那就是 DevSecOps。我想你可能几乎不经意地回到了我们现在称之为网络安全或信息安全或任何你想叫它的东西的美妙世界。这一运营使命的内在理念是安全部署、保持安全的基础设施并保护您的应用。这是 Rundeck 花费越来越多的时间，越来越多的资源，越来越多的关注，我已经看到，无论如何都是围绕这个 DevSecOps 任务。对此有何评论？

**Edwards:** 是的，我想说这是安全和运营的交集。真正的安全、运营和治理。如果你想想现在正在发生的事情——特别是，嗯，两大趋势。这是数字化转型的趋势，实际上就是说，我的所有系统现在都需要互联，以获得一致的客户体验，这是企业想要的。然后是所有这些新的服务器列表、容器、新的 API 世界，其中一切都是 API。因此，现在我们必须定义这些过程，这些过程跨越所有这些不同的系统，这些系统过去是独立的烟囱。而且，一切都变成了 API，所以我必须有一种方法来保护它，我必须有一种方法来确定谁是谁，谁可以做什么。因此，我们陷入了这种情况，人们使用 Rundeck 作为工具，说，嘿，我在那里有我的厨师自动化，我在那里有一些 Kubernetes 的东西，我在那里有一些传统的东西，我只是有一堆我需要在那里运行的脚本，我有我需要点击的这些不同的亚马逊服务，Akamai 和诸如此类的东西。所以他们有所有这些不同的东西，他们需要按的按钮，他们每个人都有自己的登录，每个人都有自己的管理安全策略的方式。

因此，他们看着 Rundeck 说，嘿，这是一个我们可以实施策略或实施身份验证和安全控制的地方。通过定义这些 Rundeck 作业，可以说他们可以调用所有这些东西，这是一个很好的抽象，很容易将它们串在一起，然后我可以定义谁可以在哪里做什么，我有完全的访问权限。在很多方面，我们称之为钥匙卡和照相机。你可以通过 Rundeck 定义谁可以做什么，run deck 是你办公大楼里的一种钥匙卡。但是还有一堆摄像头，对吧？不是我们不信任你，而是我们必须证明你没有用你的钥匙卡做任何坏事。所以这种钥匙卡和照相机的比喻，我们在内部讨论，但我们可能应该在外部讨论。这是我们在这个新世界中看到很多人用 Rundeck 实现的东西。这是一种既能满足安全和治理需求，又能完成新的运营任务的方式。

**Shimel:** Damon，我们已经有点超时了，但我想简单地说一下，你将参加 RSA APJ 展会，这是亚太地区最大的信息安全或网络安全相关展会。我们将推出一个完整的——我们指的是 Sonatype、DevOps Connect 和其他几个——run deck 是赞助商，将在那里推出一个 DevSecOps day，你和 John Willis 是主角，对于我们在新加坡或新加坡周围的任何听众来说，这是 7 月 25 日。7 月 26 日，我想我们会尝试在新加坡组织一个大型聚会，几个聚会，不同的聚会。也是在 RSA APJ，您和 John 也将在那里进行演示。

是的，我们会的。你们做了一个非常好的活动。我们已经在旧金山做了这个，很高兴能在新加坡做这个。新加坡实际上是一个很棒的 DevOps 社区，拥有所有的银行和金融等等。那里的工作做得很好。这个活动很棒。我认为这不仅仅是为了安全，而是真正着眼于端到端的管道。这更像是你如何将这些企业问题带入 DevOps 的故事中。我不希望人们认为这只是，嘿，如果我不在安全部门，我就不需要参加这个。我认为这对任何在企业中工作的人来说都是非常好的，他们希望思考我们如何完成这些事情的具体细节，以便我们可以快速行动，并确保我们所做的事情安全可靠。

绝对的。你提到了 RSA，Damon，实际上我希望下周能有一些相关的消息，RSA San Francisco 明年将于 4 月在旧金山举行，我想我们也会在那里举办一个 DevSecOps 日。我想你已经展示了，我们已经做了三四个，我想你已经展示了所有的。

爱德华兹:我是支持者。我是艾伦节目的支持者。

Shimel: 嗯，你知道吗，对我来说，这是为了让这两个部落走到一起。这是吉恩·金和乔希·科尔曼试图做的事情，我也试图帮助他们，还有马克·米勒和 Sonatype 乐队的成员。达蒙，你知道吗，这是有回报的，因为我花了更多的时间在安全上，仅仅是因为我的背景，而且我听到——我不再像以前那样受到人们对 DevOps 的排斥。他们明白了。或者他们开始明白了。上帝希望。不管怎样，达蒙·爱德华兹，我们已经过了我们的时间，但没关系，每一分钟都是值得的。感谢您成为本期 DevOps Chat 的嘉宾。我们会在新加坡见到你。你知道吗？对于想要 Rundeck 相关信息的人来说，从哪里可以获得更多的信息？

爱德华兹:Rundeck.com。Pro 有免费试用版。你可以随时使用开源软件。我们在 IRC 上，我们有空，所以我们在附近。请随时联系我们，我们喜欢谈论这些事情。

**Shimel:** 爽。Rundeck Inc .的联合创始人兼首席产品官达蒙·爱德华兹(Damon Edwards)也是 DevOps 的杰出福音传道者。感谢您参加 DevOps Chat，我们将尽快与您联系。

爱德华:谢谢你，艾伦。

好的。我是 DevOps.com 的艾伦·希梅尔，DevOps 聊天，我们下次聊天再见。

— [Alan Shimel](https://devops.com/author/ashimmy/)