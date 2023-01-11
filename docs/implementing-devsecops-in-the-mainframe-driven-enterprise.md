# 在大型机驱动的企业中实现 DevSecOps

> 原文：<https://devops.com/implementing-devsecops-in-the-mainframe-driven-enterprise/>

DevSecOps 正在成为企业 IT 的一个重要趋势。有道理。随着时间的推移，越来越多的应用服务于更大的用户群。在过去，典型的业务应用程序只能从企业内部网络的范围内访问，而今天，软件即服务(SaaS)范式使数百万用户能够使用单个应用程序。

在 SaaS 模式中，一个应用程序将服务于许多公司，并根据给定公司的订阅计划为公司中的每个用户提供对数据和功能的访问。以 Saleforce.com 为例:只有一个 Salesforce.com 为全球数千家公司提供服务，每家公司都有一至数千名员工。每个公司和公司内的每个员工都有特定的应用程序访问权限。一个应用程序服务于数百万甚至数十亿用户的范例需要一种全面的安全方法。最轻微的破坏都会导致大混乱。想象一下，如果一个 SaaS 应用程序包含一个缺陷，允许一家公司看到其竞争对手的财务数据，而竞争对手也订阅了 SaaS，会发生什么？

鉴于互联网是全世界所有人的事实上的网络，今天的安全问题远远超出了限制网络访问。让坏演员远离变得越来越困难。可悲的事实是，一个看似好的参与者可能会立即变成坏的参与者，不仅会对网络服务器造成严重破坏，就像 DDos 攻击一样，还会对应用层造成严重破坏。事实上，根据 IBM 的说法，一个企业的网络层比应用层的要脆弱一半，然而却有更多的钱花在保护网络上。

这是一个令人大开眼界的事实，但大多数应用程序开发人员并没有想到这一点。但是，如果开发人员能够受益于在应用程序级别实现防弹安全性所需的专业知识和持续指导，这是有可能的。

这让我们找到了主机。

在当今基于 web 的现代云计算世界中，大型机是主要参与者。70%的公司数据存储在大型机上。此外，现在 Linux 操作系统在大型机环境中无处不在，企业级应用程序开发人员可以——也确实——为大型机编写 Java、Python 和 NodeJS 代码，就像他们为 X86 商业环境编写代码一样。IBM 的 [z/OS Connect EE](https://developer.ibm.com/mainframe/2016/11/21/using-the-api-editor-in-ibm-zos-connect-ee/) 和 [StrongLoop](https://strongloop.com/) 等技术使得使用行业标准规范(如 [OpenAPI](https://www.openapis.org/) )将大型机服务公开为 REST API 成为可能，而无需进行大量低级的修改。

这是好消息。

坏消息是应用程序开发人员并不擅长安全最佳实践。他们没有 CISSP 职业的 [经验，后者已经在网络空间的战壕里与坏人战斗了数年，如果不是数十年的话。但那是过去，现在是现在。今天我们有 DevSecOps。](https://en.wikipedia.org/wiki/Certified_Information_Systems_Security_Professional)

DevSecOps 是下一代 IT 转型。DevOps 的目标是创造一种统一的、自动化的和自我修正的 IT 文化。DevOps 将开发和运营结合到一个组织中，专注于以不断增长的速度创建和部署高质量的软件。DevSecOps 增加了安全性。DevSecOps 活动的范围不局限于基于商品的 X86 服务器和移动设备的软件开发。DevSecOps 旨在应用于企业的所有方面，从移动设备到大型机。

DevSecOps 是关于很多事情的。它是关于诸如 IBM 的 [AppScan](https://www.ibm.com/us-en/marketplace/ibm-appscan-enterprise/details#product-header-top) 等工具的采用，这种工具允许企业在一个统一的仪表板中实现和监控各种测试(web、移动、 [动态](https://www.techopedia.com/definition/30958/dynamic-application-security-testing-dast) 、 [静态](https://www.gartner.com/it-glossary/static-application-security-testing-sast) 和 [交互](https://en.wikipedia.org/wiki/Application_security) )。它可以包括利用 [安全服务容器](https://devops.com/when-it-comes-to-mainframe-computing-theres-more-to-containers-than-containers/) 来确保外部安全和免受内部威胁。

DevSecOps 是关于建立一套策略，以及适当的操作检查和平衡，以确保企业始终遵循安全最佳实践。它是关于遵循超越阶段性安全测试的实践。这意味着持续分析 IT 基础架构以识别漏洞，并定义降低风险的方法，相应地确定预防活动的优先级。也就是说要遵守诸如[【GDPR】](https://www.eugdpr.org/)[PCI-DSS](https://www.pcisecuritystandards.org/)[PA-DSS](https://en.wikipedia.org/wiki/PA-DSS)[ISO 27001](https://en.wikipedia.org/wiki/ISO/IEC_27001)和[ISO 27002](https://en.wikipedia.org/wiki/ISO/IEC_27002)[HIPAA](http://www.dhcs.ca.gov/formsandpubs/laws/hipaa/Pages/1.00WhatisHIPAA.aspx)[GLBA](https://www.ftc.gov/tips-advice/business-center/privacy-and-security/gramm-leach-bliley-act)和 [巴塞尔协议 III 等法规](https://www.investopedia.com/terms/b/baselii.asp)

DevSecOps 是通过使用自动化来严格检查所有代码以发现潜在的危险，从而主动采取行动。这意味着使用 HTTPS 作为面向公众的 URL 的默认协议。这意味着确保所有第三方组件在可能的情况下都是从源代码构建的——如果不能从源代码构建，则确保第三方组件和库被公认的权威机构认证为安全的。

DevSecOps 是关于很多事情的，但是有一个原则高于所有其他原则:

对于 DevSecOps，要遵循的最重要的原则是确保安全专家是参与为企业开发软件的任何团队的创始成员。

无论该公司是在大型机上运行了 30 年还是使用原生云服务才 30 天，从一开始就必须有安全专家作为其开发工作的一部分。

这听起来很明显，但是说起来容易做起来难。

这不是新的挑战。企业花了很长时间让 QA 人员参与到开发过程的开始。在开发运维/敏捷敏感性扎根之前，QA 人员在发布周期结束时出现，在代码硬化之后很久。

发布人员也是如此。在 DevOps 之前，发布管理得到了一些代码，并被告知要尽快发布。人们对该准则的内容及其对基础设施的潜在影响知之甚少。结果，周末都是在作战室里度过的，努力部署那些被稀疏记录和神秘测试的代码。你可以打赌，一旦发布管理出现在第一次项目计划会议上，事情就变了。

现在，随着 DevSecOps 的出现，轮到不倒翁中的安全性了。安全性一直是企业 IT 的重要组成部分。账本上合规条例的数量证明了这一事实。然而，安全性通常是法规遵从性部门的责任，而不是整个 IT 组织的一部分。对于许多公司来说，安全性唯一一次成为关注的焦点是在审计期间。因此，安全实践是被动的，而不是主动的。而且，对于许多公司来说，他们仍然是——回想一下对 [Equifax](https://www.consumer.ftc.gov/blog/2017/09/equifax-data-breach-what-do) 和 [Target](https://www.nytimes.com/2017/05/23/business/target-security-breach-settlement.html) 违规事件的反应。

然而，DevOps 的成功并没有被忽视。DevOps 的标准特性——将团队统一到一个共同的目标上，尽可能实现自动化，并使用 sprints 和回顾来促进快速发布和快速解决缺点——已经产生了积极的效果。有远见的公司明白 DevOps 是可行的，它的继任者 DevSecOps 也将是可行的，只要遵循基本原则:确保安全专家从一开始就有一席之地。

对许多公司来说，这意味着从经理们充当看门人和权力掮客的孤岛文化，转变为统一开放的团队文化，在这种团队文化中，经理的工作是组建自我指导的团队，并确保所有合适的人从项目一开始就参与进来。这是一种完全不同的做生意方式。

当谈到实现 DevSecOps 的承诺时，工具很重要。过程也是如此。但是，最重要的事情是确保安全性被构建到开发生命周期的结构中，从开始到发布。

DevSecOps 将填补软件开发链中缺失的一环。必须的。除此之外别无选择。坚持 DevSecOps 最重要的原则——从流程的一开始就让安全作为平等的参与者参与其中——将大大有助于确保所有软件，从移动和物联网到原生云安装和大型机实例，都将提供必要的安全性和可靠性，以负责任地满足现代世界数字经济中用户和公司的需求。

鲍勃·雷瑟曼