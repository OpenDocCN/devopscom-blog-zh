# 网飞，猿人军队，以及自由和责任文化

> 原文：<https://devops.com/netflix-the-simian-army-and-the-culture-of-freedom-and-responsibility/>

如果您的整个业务依赖于通过网络向数百万客户提供流媒体视频内容，并且没有可遵循的范例或可使用的工具，您会怎么做？如果你是网飞，你要树立榜样，制造工具。

网飞凭借其独创的商业模式获得了巨大的成功，这种模式将 DVD 电影以商标红包的形式发送给客户。航运物流的精确性以及网飞满足用户需求和确保快速交付的效率本身就是一个案例研究。但是，网飞也看到了不祥之兆，并成为第一批通过互联网流式视频传送电影的人之一。

网络协议相当有弹性，最终能够从 A 点到 B 点获取数据，但音频或视频等流媒体内容就不那么宽容了。数据需要高速传输，数据包需要到达，以避免缓冲或播放时出现故障。

网飞选择亚马逊网络服务(AWS)为其流媒体内容提供云服务器基础设施。亚马逊是可靠的，有弹性的，但它不是绝对正确的。当亚马逊经历大规模停机时——就像过去发生的几次一样——这可能意味着网飞客户的停机时间。然而，网飞非常努力地防止受到这类问题的影响，而且——多亏了猿猴军队——它相当成功。

**猿猴军**

我最近与网飞平台工程总监鲁斯兰·梅森伯格和运营工程总监乔希·埃文斯进行了交谈，以了解网飞如何采用 DevOps 和开源来开发工具，帮助它向全球客户提供高质量的流媒体视频内容。

网飞给其自动化工具套件起了个名字叫“猿猴军”,这套工具旨在对网飞的基础设施进行压力测试，并主动识别弱点，以便网飞能够解决它们。猿人军队由类似 ChaosMonkey、ChaosGorilla 和 ChaosKong 的工具组成。

乔希解释说，当你处理像网飞云基础设施这样的大规模分布式系统时，不可避免地会遇到错误。网飞没有坐等问题浮出水面，而是使用猿猴军队按照自己的方式有意诱发失败，这样问题就可以在影响客户之前被识别和解决。

ChaosMonkey 在单个服务器或集群级别上造成严重破坏——随机关闭服务器以确保自动恢复正常工作，冗余系统收拾残局，因此内容交付不会中断。ChaosGorilla 通过关闭整个 AWS 区域来实现更大规模的工作，ChaosKong 通过随机关闭 AWS 的东海岸或西海岸区域来确保交通自动重定向到其余区域，从而将这一概念提升到国家层面。

猿人军队里还有其他工具。JanitorMonkey 通过清理未使用的 EC2 资源来保持一切整洁。顾名思义，它的工作就是在开发者之后自动清理。然后是 ConformityMonkey，它检查不符合预定义的最佳实践规则的 EC2 实例。

网飞让猿猴军团自由活动，造成随机混乱，但只是在周一到周五的上午 9 点到下午 3 点之间，经理和开发人员会出现，解决任何可能因疏忽而导致的紧急情况。在某些情况下，这些工具会自动采取纠正措施，而在某些情况下，它们只会生成警报并将问题升级到适当的小组或个人。

**拥抱开源**

猿人军队的独特之处之一是网飞出于需要创造了这些工具。网飞在从云中提供内容的前沿开辟了一条道路，而且根本没有商业工具来做网飞需要做的事情。

在扩展云服务以满足需求的早期阶段，网飞经常被绊倒并碰壁。网飞是在这种规模上通过云交付内容的先驱，但是开源社区有经验，并且对使用分布式环境有既定的理解。

通过整理开源社区的资源，网飞能够对代码有更多的关注，并获得成百上千开发人员的志愿支持，以帮助完善和改进猿人军队中的工具，以及网飞开发的其他工具。Ruslan 和 Josh 还解释说，与开源社区合作有一个意想不到的好处:当内部开发人员知道他们编写的代码将被公开时，他们会更加勤奋。

网飞不仅仅利用开源社区；它还通过 Github 上的[网飞开源软件中心向公众开放其工具。有可用性工具(如猿人军队)、云管理、持久系统、基础设施服务、开发人员生产力等等——所有这些工具对任何想使用它们的人都是免费的。](https://netflix.github.io/#repo)

**自由和责任文化**

许多组织谈论一个好游戏。很容易想出一个深刻的使命宣言，或者一套有见地的公司价值观。然而，实际上达到这些标准是一个完全不同的故事。网飞以建立自由和责任文化而自豪。

网飞文化是公司如此成功的部分原因，也是网飞在 DevOps 和开源领域取得成功的原因。网飞相信找到高技能、经验丰富的工程师和开发人员，并允许他们自主完成工作，对自己的产品负责。

其他组织可以从网飞学到很多东西。网飞为 DevOps 铺平了新的道路，为与开源社区的合作设立了标杆，并建立了一种任何公司都可以从中受益的成功文化。