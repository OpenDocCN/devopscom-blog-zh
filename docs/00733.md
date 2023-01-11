# HashiCorp 将开源 DevOps 工具与 Atlas 结合在一起

> 原文：<https://devops.com/hashicorp-unites-open-source-devops-tools-with-atlas-2/>

开源和 DevOps 走在一起就像巧克力和花生酱，或者像牛奶和饼干(这些隐喻让我感到饥饿)。基本上，它们是不可分割的，虽然每一个本身都是好的，但当它们结合在一起时会更好。HashiCorp [今天宣布，Atlas](http://www.marketwired.com/press-release/hashicorps-atlas-leaves-beta-with-triple-digit-monthly-revenue-growth-mozilla-cisco-2036398.htm) ，一个各种领先开源工具的平台，现已向公众开放，以帮助组织将 DevOps 做得更好。

HashiCorp 拥有许多流行的、行业领先的开源工具。[流浪者](https://devops.com/2014/04/10/automation-versus-orchestration/)管理开发环境。[打包器](https://devops.com/2014/05/27/open-source-pipeline-trusted-images/)自动构建 Docker 容器、OpenStack 映像和 VMware 映像等工件。Consul 是一个运行时编排工具。Serf 是 Consul 在服务器集群中用于故障检测和消息分发的协议。Terraform 在微软 Azure 和亚马逊 Web 服务等云平台上实现了基础设施供应的自动化。它们本身都是很好的工具，但是 Atlas 将它们结合成一个强大的、有凝聚力的整体。

Atlas 已经推出测试版一段时间了，取得了巨大的成功。在测试期间，管理的节点每月都翻一番，像 Mozilla 和 Cisco 这样的重量级公司也加入进来进行测试。

DevOps 寻求加速开发和部署。DevOps 的主要属性之一是自动化，以促进例行的、可重复的功能的自动的、无错误的、可审计的实现。许多组织努力采用 DevOps 工具和原则，并利用 Consul 或 vagger 等开源工具，但使用手动、耗时、易出错的流程，这些流程难以扩展且难以有效管理。

HashiCorp 认为 Atlas 是解决方案，它是一个平台，将所有这些整合在一起，使组织能够跨多个云环境进行从配置管理到容器部署的端到端管理。每个开源工具单独使用都很好，但是将它们作为一个整体进行管理和编排的能力非常强大。

“我们最初推出了自己的基础架构 CI 和部署解决方案。Mozilla 内部工具和系统架构师 Chris Lonnen 表示:“随着团队的壮大，我们的自制解决方案很难集中管理配置、平台状态和访问控制。“Atlas 为我们解决了所有这些挑战，并为审计日志、基础设施历史、系统范围的监控等提供了一个漂亮的界面。我们从未在哈希公司的产品上输过 9 分。”

根据 HashiCorp 的新闻稿，您可以从今天开始使用 Atlas 的托管版本，但 Atlas 的内部部署要到 2015 年底才会发生。如果您想了解更多关于内部 Atlas 的信息，您可以点击此链接注册:[https://atlas.hashicorp.com](https://atlas.hashicorp.com/)。开发功能，如流浪盒构建和托管和包装构建和工件存储是免费的，前 10 个节点也是免费的。超过前 10 个节点后，定价为每月每节点 40 美元。