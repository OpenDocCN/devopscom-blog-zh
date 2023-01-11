# Chef 启动了新的开源项目 Habitat，以实现应用程序自动化

> 原文：<https://devops.com/chef-launches-habitat-new-open-source-project-automate-applications/>

经过 9 个月的潜行开发，这个同类项目中的第一个开源项目将自动化与应用程序打包在一起，可以在任何地方部署，从裸机到容器

SEATTLE—2016 年 6 月 14 日—Chef<[https://www . Chef . io](https://www.chef.io/)>，DevOps < [自动化领域的领导者 https://www.chef.io/<wbr>solutions/devo PS](https://www.chef.io/solutions/devops)>，今天宣布了 Habitat<[https://Habitat . sh](https://habitat.sh/)>，这是一个开源项目，引入了应用自动化的新方法。与 Habitat 打包在一起的应用程序具有自组织和自配置的智能。Habitat 使应用程序独立于底层基础设施，因此可以轻松地在日益多样化的环境中运行应用程序，如容器、PaaS、云基础设施和内部数据中心。

如今，公司通过许多定制应用程序广泛开展数字化业务。随着这些应用程序的复杂性增加，管理它们的负担也随之增加。传统上，基础设施决定了应用程序的设计。Habitat 持相反的观点，第一次将应用程序放在了最前面和最中心的位置。因此，公司可以专注于业务价值和使其产品脱颖而出的规划功能，而不是基础设施和特定运行时环境的限制。

无论是新建还是遗留，任何使用 Habitat 包部署的应用程序都具有感知其环境并对其做出反应的智能。Habitat 新颖的打包方法允许应用程序独立于任何特定的基础设施环境。Habitat 还提供了一个定义良好的接口，简化了常见任务，例如监控、新功能的安全部署以及生产系统所需的对等关系的创建。

从开发人员的角度来看，通过将应用程序包装在 Habitat 包中，应用程序团队在准备好部署之前不必担心特定的运行时。因为 Habitat 灵活地处理应用程序的管理，团队不再负责一遍又一遍地创建他们自己的管理解决方案。有了 Habitat，开发人员可以专注于推动业务发展的新产品和新功能。

Chef 的联合创始人兼首席技术官 Adam Jacob 将通过 livestream < [https://bignews 为 Habitat 揭幕。<wbr>chef.io/](https://bignews.chef.io/)T7今天太平洋时间 上午八点半。该演示将包括一个现场演示，随后是 Twitter 上的现场问答。使用#habitat 标签向@chef 发送问题。

新闻集锦:

Habitat 是同类项目中的第一个开源项目，它提供了一种全新的应用程序管理方法。Habitat 将应用程序及其自动化作为部署单元。当应用程序被包装在一个轻量级的“栖息地”中时，运行时环境，无论是容器、裸机还是 PaaS，都不再是焦点，也不再约束应用程序。生境的特点包括:

*   对现代应用程序的支持:Habitat 包包含了应用程序在整个生命周期中运行所需的一切。人居中心的核心组成部分是:
*   包装格式。Habitat 包中的应用程序是原子的、不可变的和可审计的。

*   主管。Habitat supervisor 运行应用程序包，并了解包的对等关系、升级策略和安全策略。生境管理者为任何存在的环境配置和管理应用程序。栖息地生态系统还提供构建服务，该服务采用栖息地构建计划，创建栖息地包，并将其发布到仓库。

*   在任何地方运行任何应用程序:使用 Habitat，应用程序可以在任何运行时环境中运行，无需修改，从裸机和虚拟机到 Docker 等容器和 Mesosphere 或 Kubernetes 等集群管理系统，以及 Pivotal Cloud Foundry 等 PaaS 系统。

*   轻松移植遗留应用程序:当遗留应用程序被包装在一个 Habitat 包中时，它们就独立于最初为其设计的环境。它们可以快速转移到更现代的环境中，比如云和容器。此外，因为 Habitat 包有一个标准的面向外的接口，遗留应用程序变得更容易管理。
*   改善容器体验:Habitat 降低了在生产环境中管理容器的复杂性。通过自动化容器内的应用程序配置，Habitat 解决了开发人员在将基于容器的应用程序从开发环境转移到生产环境时所面临的挑战。
*   融入大厨的 DevOps 工作流程:栖息地项目由大厨赞助。Habitat 利用 Chef 在基础设施自动化方面的丰富经验，为应用程序带来前所未有的自动化功能。Chef 将为 Habitat 提供商业支持，并确保 Habitat 和 Chef 交付之间的无缝集成，以实现从开发到部署的应用程序发布周期的完全自动化。

可用性:
Habitat 是 Apache 2.0 许可下的一个开源项目。您可以在[https://www.habitat.sh/docs/<wbr>get-Habitat/](https://www.habitat.sh/docs/get-habitat/)立即下载 Habitat。Chef 通过其 Chef Enterprise 订阅为人居主管提供商业支持。

支持语录
“我们必须让应用摆脱对基础设施的依赖，才能真正实现 DevOps 的承诺。世界上有如此多的开源软件需要编写，我们非常高兴将 Habitat 发布到野外。我们相信，以应用为中心的自动化可以给现代开发团队带来他们真正想要的东西——构建新的应用，而不是在管道中瞎折腾。”

*   Adam Jacob，联合创始人兼首席技术官，厨师

“每年，我们都看到在应对大规模应用管理挑战方面取得了稳步进展，
但我认为我们必须特别关注那些持续提供所需最终状态的技术，
以及跨不同生产环境的技术，否则我们只是在加速翻墙过程。”

*   Mark Burgess，技术专家，作者，CFEngine 的创建者，奥斯陆大学学院网络和系统管理名誉教授

“像 Habitat 这样的开源项目能够帮助 DevOps 团队在任何地方的容器中运行他们的应用程序。社区可以利用 Habitat 在 CoreOS Linux 上以应用程序为中心的自动化，core OS Linux 是为容器设计的轻量级操作系统，而 architectural 是使用 Kubernetes 在所有环境中运行分布式应用程序的首要基础设施平台，同时受益于安全性、可靠性和可扩展性。”

*   CoreOS 产品负责人党微

“传统企业应用向混合云的扩散有限。通过简化构建可在任何地方运行的应用程序，混合云平台、容器及其管理的价值可以得到充分实现。Habitat 是使企业 IT 充分受益于云计算的便携性和效率的重要一步。”

*   英特尔数据中心事业部软件定义基础设施副总裁 Jonathan Donaldson

“开源是推动当今数字经济的现代应用原则的核心。Habitat 和 DC/OS 共同支持组织将这些原则(包括自主性、可移植性和可扩展性)应用于新的和传统的应用程序，从而更容易在任何环境中实现应用程序堆栈的自动化。”

*   鸢·克纳普，中间层联合创始人兼首席技术官

“现代应用程序团队希望能够自由选择基础架构，而不必担心这些选择对其应用程序的影响。Habitat 的应用程序自动化与我们的容器管理平台相结合，使开发团队能够在从裸机到云的任何设备上轻松构建、部署和管理他们的容器化应用程序。”

*   Rancher Labs 首席执行官盛亮

额外资源

*   观看 Adam Jacob 揭开并演示栖息地<[https://big news . chef .<wbr>io/](https://bignews.chef.io/)>今日上午8:30 PT。
*   通过互动演示体验栖息地<[https://www . Habitat .<wbr>sh/try/](https://www.habitat.sh/try/)>。
*   了解一下 Habitat<[https://www . Habitat .<wbr>sh/about/](https://www.habitat.sh/about/)>，它的做法，还有组件。
*   通过一系列教程<[https://www . Habitat .<wbr>sh/tutorials/](https://www.habitat.sh/tutorials/)>学习如何使用 Habitat。
*   用 Habitat 的文档来掩饰自己。<wbr>habitat.sh/docs/>。
*   下载栖息地<[https://www . Habitat .<wbr>sh/docs/get-Habitat/](https://www.habitat.sh/docs/get-habitat/)>。

关于 Chef
成立于 2008 年的 Chef Software 正在改变公司构建和交付软件以取悦客户的方式。Chef 是 DevOps 自动化的领导者，devo PS 是一个文化和专业运动，专注于我们如何建立和运营高速组织，从其从业者的经验中诞生。建立在强大的开源基础上，我们已经将快速和可扩展软件开发的成熟模式和实践提炼到我们领先的 IT 自动化平台中。Chef 实现了应用和基础设施的连续统一交付的自动化，使全球企业能够以最小的风险更快地交付软件。我们拥有数百家商业客户和数以万计的开源社区成员，引领着当今世界上最强大的技术运动之一。敬请关注[www . chef . io](http://www.chef.io/)<[http://www . chef . io](http://www.chef.io/)<wbr>>。

谢尔比·利奇利特
里维尔| [【电子邮件保护】<wbr>co](/cdn-cgi/l/email-protection#d98ab1bcb5bba0f795b0bab1b5b0adbcab99abbcafbcabbcb8bebcb7baa0f7bab6)<[mailto:【电子邮件保护】<wbr>revereagency.co](/cdn-cgi/l/email-protection#cc9fa4a9a0aeb5e280a5afa4a0a5b8a9be8cbea9baa9bea9adaba9a2afb5e2afa3)>|[925 . 216 . 5303](tel:925.216.5303)

Attachments area