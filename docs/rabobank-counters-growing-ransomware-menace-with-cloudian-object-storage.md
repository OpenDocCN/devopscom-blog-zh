# Rabobank 通过云对象存储应对日益增长的勒索病毒威胁

> 原文：<https://devops.com/rabobank-counters-growing-ransomware-menace-with-cloudian-object-storage/>

*Cloudian S3 对象锁使数据不可变，确保无需支付赎金即可快速轻松地恢复数据*

**加利福尼亚州圣马特奥，2022 年 4 月 6 日** — Cloudian 今天宣布，[荷兰跨国银行和金融服务公司 Rabobank](https://www.rabobank.com/en/home/index.html) 已经部署了 Cloudian [对象存储](https://www.cloudian.com/)，作为其针对勒索软件攻击的多层保护解决方案的一部分。结合 Veeam 备份软件，Cloudian 的 S3 对象锁解决方案使 Rabobank 能够使备份数据副本不可变，因此不受网络犯罪分子加密或删除的影响。这种数据不变性已经过美国政府认证测试 [*](https://outlook.office.com/mail/id/AAQkAGIwNGI5ZTMxLWNhZjItNGUzMS1iN2IyLWI3NjA2Yjg4MGJjZQAQAJu4wRmLCDtFhCLWCo2%2FWHo%3D#_ftn1) 的验证，可确保在遭遇勒索软件攻击时快速、可靠地恢复。

**从纵向扩展到横向扩展存储**

Rabobank 成立于 125 年前，是一家总部位于荷兰的合作银行，为私人和商业客户提供各种金融产品，包括房地产、抵押贷款和租赁解决方案。该银行是食品和农业融资以及以可持续发展为导向的银行业的全球领导者，在 38 个国家拥有 43，000 名员工。

2020 年年中，荷兰合作银行部署了其针对勒索软件攻击的分层保护的第一步。该银行开始担心传统的备份目标存储解决方案容易受到这种不断增长的威胁，并开始有条不紊地在整个体系中构建强大的防御和恢复功能。这促使该公司最终寻找一种具有数据不变性的横向扩展对象存储解决方案。

Rabobank 存储了来自其欧洲实体的超过 10.5 PB 的备份数据，这一数字每年增长 25%。此备份池的关键要求包括容量和性能的可扩展性。容量可扩展性对于容纳不断增长的数据量至关重要。性能对于满足备份 RTO 和 RPO 目标至关重要，因为正在处理的 Veeam 数据会产生大量输入/输出负载，并且会随着时间的推移而增加。可扩展的处理能力对于管理 20 多亿个对象的数据不变性也很重要，这些对象通常会被创建，然后随着备份的自然过期而被删除。

“出于这个原因，我们迅速关注了云横向扩展解决方案。凭借其点对点架构，每增加一个新的 Cloudian 节点都会提高系统的性能和处理能力，”荷兰合作银行欧洲存储服务经理 Colin Chatelier 说道。“我们还进行了概念验证，从经验和功能上比较了 Cloudian 与使用生产备份的其他解决方案，结果令人印象深刻。与其他花费数周时间建立的系统相比，Cloudian 系统在一天内就建立并运行了。它与 Veeam 无缝集成，性能与其他产品一样好，甚至更好，安全性符合所有要求。”

Rabobank 在其两个欧洲数据中心部署了 Cloudian 的 HyperStore 对象存储和 S3 对象锁。除了提供数据不变性之外，HyperStore 还锁定了对托管数据的系统的特权(根)访问，因此没有人能够破坏这种不变性。在 Cloudian 设备上实施被视为一个明显的优势，因为它在技术上将“故障安全拷贝”与标准基础设施分开，而标准基础设施可能已经在勒索软件攻击成功的情况下受到损害。HyperStore 还通过动态和静态加密、集成防火墙、RBAC/IAM 和 SAML 访问控制以及符合最严格监管要求的认证来保护数据，包括通用标准、FIPS 和 SEC 规则 17a-4(f)。

**全面的勒索病毒防护和全面的数据控制**

Rabobank 对 Cloudian 解决方案以及与 Cloudian 团队合作的体验非常满意。

“最大的好处是安心，”Chatelier 说。“我们已经委托进行渗透测试，但未能侵入云集群，也未能影响数据的不变性。它也在我们的自动化备份工作流中实施，因此易于管理。当问题出现时，正如任何解决方案都会发生的那样，Cloudian 的响应速度非常快，包括提供我们要求的新报告和安全功能。”

Cloudian 解决方案是 Chatelier 倡导的更广泛的勒索软件保护框架的一部分。他和他的团队利用 VMware 和 Cisco 技术，为管理数据恢复和恶意软件删除建立了一个“净化室”。

“我们知道总会有人建议使用公共云来保护勒索软件，”Chatelier 说。“虽然公共云备份非常适合基于云的数据，但它们不适合本地数据。按照我们需要的时间和方式将这些卷从云中恢复到本地是不可能的。此外，为了恢复您的内部系统而在公共云中建立一个干净的房间有一个明显的缺陷——您访问云的能力可能已经受到攻击的影响。”

展望未来，Rabobank 希望在大洋洲和美洲扩展 Cloudian 解决方案。

Chatelier 说:“不可变备份是公司最后的保险政策。”。“如果我们召唤他们，他们就必须成功，因此与我们的主要供应商的信任和合作是无价的。此时此刻，我们比任何其他人都更需要我们的供应商成为真正的合作伙伴 ， 如果我们需要他们 ， ，Cloudian 已经通过从概念验证到实施的承诺和灵活性证明了这一点。”

**关于 Cloudian**

Cloudian 是混合云数据管理软件的领导者。凭借军用级别的安全性、无限的可扩展性和无缝的云集成，Cloudian 的 S3 兼容对象存储允许用户优化数据访问，满足数据主权要求，并通过将信息整合到单个类似云的平台来削减成本。Cloudian 的地理分布式架构管理和保护传统和现代应用程序的边缘、核心和云中的对象和文件数据。更在[cloudian.com](https://www.cloudian.com/)。