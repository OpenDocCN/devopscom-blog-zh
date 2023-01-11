# 现场可靠性工程(SRE)将于 2022 年成熟

> 原文：<https://devops.com/site-reliability-engineering-sre-comes-of-age-in-2022/>

站点可靠性工程师(SRE)的角色仍然在组织间聚集力量。在 2022 年 1 月的[日，领英将 SRE 列为过去五年全球需求最高的第 21 个职位。对于这样一个特定的技术角色来说，这是相当高的。展望未来，SRE 实践作为一种支持高可用性、可靠性和改善数字客户体验的方法，似乎只会继续获得采用。SRE 方法对于满足服务级别协议(SLA)和内部服务级别目标(SLO)也很重要。](https://www.linkedin.com/pulse/linkedin-jobs-rise-2022-25-us-roles-growing-demand-linkedin-news/)

我最近会见了 SRE 建筑师 Kurt Anderson 和来自《无可指责》的内容作家 Emily Arnott，听取他们对 2022 年 SRE 实践的主要趋势和预测。根据无可指责的团队，2022 年可能会看到整个公司和内部部门越来越多地采用 SRE 的角色。

正如制造业为其质量保证设定高标准一样，数字应用现在也需要同样高的可靠性来满足[膨胀的用户期望](https://accelerationeconomy.com/business-apps/study-shows-digital-apps-only-have-one-shot-to-win-users/)。为了应对这些新的现实，sre 有自己的工作要做，他们必须面对如何统一不同的 DevOps 工具，并且必须深入挖掘以发现特定的用户体验疑虑，而这一切都不会增加警报疲劳。

## 增加 SRE 的采用

如上所述，[SRE 的角色](https://devops.com/how-the-sre-role-is-evolving/)近年来有了巨大的增长，而且没有放缓的迹象。SRE 作为一种实践在 2015 年由[谷歌](https://cloud.google.com/blog/products/devops-sre/how-to-start-and-assess-your-sre-journey)首次推广。今天，他们简单地将其定义为“当你要求软件工程师解决一个操作问题时会发生什么。”这相当于通过创建错误预算、设计 SLA/SLO 以及随着时间的推移优化流程自动化来保持数字服务的高可靠性。

对阿诺特来说，随着越来越多的公司接受谷歌的 SRE 主义，我们仍然看到 SRE 的采用呈指数级增长。“在疫情期间，越来越多的公司被迫采用数字化战略。可靠性是这一战略的基础。”阿诺特预计 SRE 将成为初创公司中富有成效的角色，初创公司最初可能会被这种前景吓倒。

“SRE 的做法是一个尺度问题，”安德森解释道。对于时间紧迫的公司来说，当他们的注意力已经如此分散时，很难实施 SRE 计划。然而，随着新的需求推动超高速创新，我们看到更多的 DevOps 被采用。因此，SRE 的角色变得越来越重要。

## 多工具条件更加统一

大多数 DevOps 专业人士都会同意——我们生活在一个[多工具的世界](https://containerjournal.com/features/kubernetes-sprawl-is-here-contain-your-excitement/)。例如，[对多集群管理的关注](https://containerjournal.com/features/cncf-radar-highlights-kubernetes-multi-cluster-preferences/)带来了过多的新工具。计算环境也是多种多样的，通常结合多个云，由容纳各种微服务集群的[混合产业](https://devops.com/3-key-issues-with-hybrid-cloud-transformation/)组成。即使在同一个组织中，不同的团队也可能选择不同的 DevOps 工具。安德森认为，SREs 可以“为单个公司分散的 DevOps 采用带来更多的统一。”

安德森说，随着公司采用更多的软件，不可避免地会有某种程度的工具蔓延。例如，可能有竞争的方法来[监控](https://devops.com/why-observability-and-monitoring-matter-to-sres/)数字服务的使用。平台团队可能在用 Datadog，一个 app 团队可能在用 New Relic，另一个团队可能在用 Prometheus。这些工具使用不同的语言，生成不同的日志，形成了孤岛。

对于阿诺特来说，未来包括接受微服务时代固有的复杂性，并使用可以从任何地方接收数据的不可知层来识别有意义的事件。

## UX 更加强调可观测性

安德森说:“SRE 的角色无疑是一种趋势，其重要性一直在增长，并将继续增长。”。随着越来越多的组织转向数字化，这变得很有必要；这种转变带来了超越用户体验预期的巨大压力。阿诺特说:“现在竞争和人们的期望都很高。“如果你不可靠，这年头让人无法接受。”

DevOps 更侧重于将应用程序*投入生产*，而 SRE 则采取了一种更侧重于 UX 的方法。以网飞为例，该公司在 SRE 的核心团队上进行了大量投资，以确保面向用户的服务稳健可靠。据[网飞科技博客](https://netflixtechblog.com/keeping-customers-streaming-the-centralized-site-reliability-practice-at-netflix-205cc37aa9fb)称，“保持我们的客户满意和流媒体的一个关键基础是对可靠性的高度关注”。

阿诺特说，为了迎合这种新范式，团队需要对基于特定用户群的可观察性有更深入的理解。sre 需要精确的用户体验环境，例如延迟的增加或错误响应的增加。但是他们也必须发现这些错误背后的促成因素。“SLO 和错误预算就像是给你量体温——如果有什么不对劲，它们会告诉你*。他们不会告诉你*为什么*你发烧了。”*

## SRE 从制造业中得到启示

安德森解释说，随着可靠性越来越成为公司品牌存在的核心，如此重要的东西被提升到高管层是很自然的事情。作为一个参考例子，他指出，制造业通常会任命一名首席可靠性官。在传统制造业中，生产线通过严格的测试进行统计过程控制，以确保质量。类似的职位在各行各业都存在，比如金融服务业的首席质量官。

结论是，随着可靠性越来越多地成为定义竞争指标的标准，科技公司可能需要一个类似的高级管理层职位，以符合这一理念，并指导团队实施 SRE 实践。当然，这样一个头衔的必要性将完全取决于组织的规模和构成。

## 更加依赖 SLO 以避免违反 SLA

服务水平协议(SLA)通常是与外部合作伙伴围绕数字服务的可靠性建立的正式合同，如果违反，可能会导致经济处罚或其他形式的赔偿。这种协议可以存在于软件提供商和最终用户之间，但是在 B2B 环境中执行起来更加严格。

另一方面，服务级别目标(SLO)更像是一个内部目标。SLO 的门槛通常比 SLA 低。例如，也许 SLA 可以确保用户登录失败的次数不超过一百万次中的十次，但是 SLO 被设置为一百万次中的两次。

设置内部 SLO 有助于工程师及时了解适度的客户体验问题，以免这些问题成为导致罚款的重大事件。“一些公司将 SLO 视为另一种警示；他们应该是用户体验的代表，”安德森说。随着 SRE 计划开始成熟，公司将慢慢开始采用更具竞争力的目标来提供卓越的用户体验并避免不满意的合作伙伴，这是有道理的。

## 最后一点:不要玩指责游戏

SRE 教义的很大一部分是“无可指责的死后尸体”的概念。因为当你身处事故之中时，最糟糕的事情就是指指点点。安德森说:“责备会触发一种防御机制，当你处于防御模式时，你无法做出良好的反应。”

相反，在进行这些回顾时，最好保持开放的心态——接受发生的事情是有原因的，并寻求发现原因以做出积极的改进。"为了变得更有弹性，我们可以在系统层面上改变什么？"阿诺特问道。“那个错误的起源是什么？缺少什么信息？应该发生了什么沟通来防止这种情况？”

通常情况下，事故的发生不是故意的，也不是由于不称职，而是由于过程中的漏洞。通过不玩指责游戏，公司可以更好地解决问题，因为他们会逐步发布新功能。然后，希望有了正确的 SRE 方法，团队可以推进他们的数字服务，以满足当今现代用户体验期望的高风险。