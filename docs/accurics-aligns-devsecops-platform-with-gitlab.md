# Accurics 使 DevSecOps 平台与 GitLab 保持一致

> 原文：<https://devops.com/accurics-aligns-devsecops-platform-with-gitlab/>

Accurics 今天宣布，它已将其用于发现违反安全策略的工具与持续集成和持续交付( [CI/CD](https://devops.com/?s=CI%2FCD) )平台和 GitLab 的静态应用安全评估测试(SAST)工具相集成，当开发人员将基础设施作为代码供应时，会发生违反安全策略的情况。

Accurics 首席信息和安全官(CISO)兼首席技术官 Om Moolchandani 表示，这两种集成都使开发人员能够更容易地发现安全问题，作为使用该公司 Terrascan 工具的 DevSecOps 工作流的一部分。

如今，组织在云安全方面遇到的许多问题都可以追溯到开发人员在使用 Terraform 等工具配置基础架构时造成的错误配置。Accurics 创建了 Terrascan 来识别这些错误配置。

Moolchandani 说，与 GitLab 的集成使得将 Terrascan 整合到 DevOps 工作流中变得更加容易，同时还可以聚合从 SAST 和动态应用安全测试(DAST)工具收集的数据。他补充说，这种方法有效地统一了今天两个独立的云基础设施和应用程序开发管道，使 DevOps 团队能够利用威胁分数来实施安全策略，因为代码被认为太危险，无法与块构建一起部署。

Moolchandani 指出，与此同时，与 SAST 和 DAST 工具的集成为开发人员提供了在生产环境中部署应用程序之前确定补救工作优先级所需的环境。

各种规模的组织现在都试图在两个相互冲突的议程之间找到平衡。一方面，Terraform 等基础设施即代码(IaC)工具在帮助开发人员更快地构建和部署应用程序方面发挥了关键作用。问题在于，在网络犯罪分子越来越积极地寻求破坏软件供应链的时候，开发人员缺乏确保基础设施安全所需的安全专业知识。组织很可能不会放慢应用程序的部署速度，以确保软件供应链不受损害。然而，在缺乏最佳 DevSecOps 实践的情况下——这种实践仍然没有得到广泛实施——将应用程序的责任转移给开发人员可能会遭到强烈反对。

带来的挑战是，大多数组织没有足够的安全专业知识来在部署应用程序之前及时审查应用程序，这导致他们希望在应用程序更新周期内发现并补救安全问题，以免网络犯罪分子找到利用漏洞的方法。

当然，希望并不意味着应用程序安全策略。组织将需要找到一些方法，使开发人员能够更好地保护应用程序，同时使网络安全团队能够更轻松地维护零信任 it 环境，从而降低组织被入侵的可能性，例如，通过网络钓鱼攻击窃取开发人员凭据。

无论 DevSecOps 工作流和零信任 IT 架构是如何实施的，很明显，组织已经没有时间来解决长期存在的安全问题，这些问题现在成为了没人想看到的头条新闻。