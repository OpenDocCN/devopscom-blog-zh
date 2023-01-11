# Puppet 为云原生、事件驱动的自动化引入 Relay 公测版

> 原文：<https://devops.com/puppet-introduces-public-beta-of-relay-for-cloud-native-event-driven-automation/>

### Relay 监听信号、触发工作流并协调数百个云提供商、工具和 API

俄勒冈州波特兰市。，2020 年 6 月 24 日(环球新闻网)——[木偶](https://www.globenewswire.com/Tracker?data=TuJn_lRepG-olj9W5wkHQayBl-UpqGBx4zHD_i5dMYQExDezftNMfv9YjyTV7JVLM80vVRJs3kkGvVqr1hliZw==) ，基础设施自动化的行业标准，今天推出了 Relay 的公开测试版，这是一个事件驱动的自动化平台。Relay 可跨任何云基础架构、工具和 API 实现流程自动化，目前开发人员、DevOps 工程师和 sre 需要手动管理这些流程。

向云的转变带来了巨大的复杂性。除了现有的基础设施之外，DevOps 工程师现在还负责监督数十种新工具和技术，从容器和虚拟机到无服务器应用程序和 API。随着票证、监控警报和事件报告数量的不断增加，工程师的工作效率已经到了临界点。工具泛滥已经形成了一个“DevOps 转储场”，工程师要么跨不同的服务手动执行操作，要么拼凑自己开发的解决方案来帮助管理涌入的工作。Relay 通过听取来自不同工具的信号来自动化工作流程，从而将工程师从手动流程中解放出来，腾出时间专注于更有价值的计划。

Puppet 首席技术官 Deepak Giridharagopal 表示:“如果没有一种方法来管理和自动化大量事件和开发人员使用的数百个 API，时间、金钱和精神资本都将被浪费掉。“许多工程师试图创建自己的一次性自动化工具或集成中心，但这既低效又有风险。Relay 用可重复使用、成熟的自动化工作流程取代了这种自制的数字管道胶带。这就像 IFTTT，但对于 DevOps 来说。”

Relay 连接了 DevOps 工程师已经在使用的几十个云平台、工具和 API，包括 PagerDuty、GitHub、Datadog、吉拉、Terraform、Slack 等等。通过侦听来自这些服务的触发器，Relay 可以处理各种各样的云自动化用例，包括:

*   **安全性:**在您的整个基础架构中实施安全控制，例如确保云存储桶是安全的，卷是加密的，或者从帐户中删除未使用的 SSH 密钥。
*   **成本优化:**主动删除 AWS、Azure 和 GCP 上未充分利用的云资源，如未连接的卷、未使用的负载平衡器和未标记的实例，它们会导致每月费用昂贵。
*   **事件响应:**当出现新的事件时，Relay 通过自动修复已知问题或使用 Bolt 运行诊断操作来扩展 PagerDuty 或 VictorOps。
*   **持续交付:**将 Relay 连接到 Docker Hub 或 GitHub，使用 Terraform 或 Pulumi 自动调配云基础设施，并将您的最新版本的微服务部署到 Kubernetes、Google Cloud Run、AWS Lambda 等平台。
*   **操作:**删除旧快照、配额使用警报、资源利用报告等。

“今天的工具侧重于分析和响应历史数据。相比之下，Relay 能够在事件发生时做出实时反应，”Puppet 增长副总裁 Alex Bilmes 说。“Relay 通过在单一平台中将基于事件的触发器与强大的工作流引擎相结合，智能地响应外部信号。”

优步高级软件工程师 Stan Chan 表示:“我曾在大规模数据中心环境中工作过，并管理过现代混合云部署的复杂性，因此我亲眼目睹了随着当今技术采用的快速发展，优化成本和效率有多么重要。“Relay 为企业提供解决这些问题以及更多问题的解决方案。它通过让组织更智能地构建，以现代、优雅和有效的方式解决现实世界的业务流程，实现了自动化未来的承诺。”

随着 Relay 的加入，Puppet 为跨任何基础设施(内部或云)的任务驱动、模型驱动和现在的事件驱动自动化提供了市场领先的产品。使用 Puppet，您可以通过与一些最重要的企业基础架构供应商(如 Hashicorp、ServiceNow、Atlassian、Splunk 等)进行集成来提高生产率、消除错误并加快交付速度。

RedMonk 首席分析师 Stephen O'Grady 表示:“随着 DevOps 的兴起，旨在满足开发者和运营商需求的工具组合在过去十年中出现了爆炸式增长。“这反过来导致了严重的碎片化和高度复杂、脱节的工作流程。因此，重视速度的组织开始重新思考他们的开发人员体验，并寻找自动化和集成不同接触点的方法。这是继电器制造的机会。”

如需了解更多关于接力赛的信息，请访问我们的 [网站](https://www.globenewswire.com/Tracker?data=j4SS2SWLJENy1bfjdcpoQd6qDP8VryK1svcVTnnQzkjruQbe6andX2zuc_ZbBZ52DjQtcp_4Ju3hSPx2oUqu2Q==) 。

**附加资源**

*   了解更多关于 [傀儡](https://puppet.com/)
*   跟随木偶上[Twitter](https://twitter.com/puppetize?lang=en)T3和[LinkedIn](https://www.linkedin.com/company/puppet/)
*   阅读 [我们的博客](http://relay.sh/blog)

**关于 Puppet**
Puppet 让基础设施变得可操作、可扩展、智能。从数据中心到云，Puppet 帮助企业实现基础设施的现代化和管理，通过持续的自动化提供创新和效率。超过 40，000 家组织(包括全球 5000 强中的 80%以上)受益于 Puppet 的开源和商业解决方案，以确保业务连续性、优化成本、提高合规性和确保安全性，同时加快开发运维实践的采用和自助服务的交付。总部设在俄勒冈州波特兰市，是一家私人控股公司，在伦敦，贝尔法斯特，新加坡和悉尼设有办事处。在[puppet.com](http://puppet.com/)了解更多信息。