# 原料药行业的趋势

> 原文：<https://devops.com/trends-in-the-api-industry/>

应用编程接口 [(API)经济](https://devops.com/api-sprawl-a-looming-threat-to-digital-economy/)正在全速前进。到 2025 年，仅 [API 管理](https://devops.com/how-are-api-management-and-service-mesh-different/)市场就有望扩大 [35%，这是由大量 web APIs 进入市场支撑的。API 已经在微服务架构、公共产品计划、SaaS 平台产品、物联网和合作伙伴集成中无处不在。](https://www.marketwatch.com/press-release/api-management-market-size-share-growth-demand-trends-and-forecast2021--2030-2022-01-27)

该行业已经激增并继续变化，在所有行业中引入了新的 API 用例。这种无处不在的情况增加了对 API 程序的需求，以维持高质量的开发者体验并保持竞争力。市场上还有不同的风格和规范选项，这意味着设计正确的 API 策略是一个不断变化的目标。此外，在[高峰网络攻击](https://securityboulevard.com/2021/07/api-attack-traffic-grew-300-in-the-last-six-months/)中，开发者现在有一个强烈的要求来保持这些集成点的高安全性和可靠性。

我最近会见了 Stoplight 的首席执行官 Steve Rodda，讨论了上述趋势以及推动 API 行业在 2022 年向前发展的其他力量。下面，我们将深入这些趋势，看看它们是如何影响 API 策略的，以及开发人员需要知道什么才能在他们的应用程序上保持领先。

## 非软件公司拥抱 API

随着软件蚕食世界，更多的公司正在成为软件公司。而且， [API 策略](//devops.com/digital-business-transformation-driving-more-api-adoption/)是这个[数字化转型](https://devops.com/the-role-of-apis-in-digital-transformation/)的重要组成部分。Rodda 认识到的一个大趋势是传统的非软件公司增加了 API 策略。

例如，Rodda 解释了一家大型饮料制造商如何在全公司范围内采用 API 来更好地使用和扩展他们的数据。Rodda 说，API 开发和设计过程的标准化有助于避免自定义代码的“老鼠仓”。“API 不再是副产品；他们是设计的人工制品，”他说。

API 也不再是 Stripe 或 Twilio 等云原生初创企业的专利。我们现在看到许多行业和部门，如供应链管理、医疗保健、[航运、](https://nordicapis.com/apis-at-maersk-a-case-study/)、建筑环境和[大型机现代化](https://devops.com/the-role-of-apis-in-mainframe-modernization/)都采用 API 方法。金融服务部门尤其热衷于开放 API，因为开放银行业是由地区监管或市场压力推动的。

## 内部 API 首次采用的增加

最全面的 API 目录 ProgrammableWeb ，在撰写本文时列出了超过 24，000 个 API。毫无疑问，面向公众的 API 是有据可查的。但是这只是 API 采用总数的一小部分。

2021 Postman[API 状态报告](https://www.postman.com/state-of-api/api-first-strategies/#api-first-strategies)发现只有 15%的 API 是公开可用的。根据该报告，大多数 API 要么面向合作伙伴(27%)，要么是私有的(58%)。事实上，API 最流行的用例是内部应用程序、程序或系统之间的集成。随着内部 API 使用的增长，API 优先的思想正在得到认可。Postman 将 API-first 定义为“在开发依赖的 API、应用程序或集成之前，定义和设计 API 和底层模式。”

Rodda 说，内部用例较少被讨论，但是对于大型企业来说是普遍存在的。在过去，开发团队不太关注内部服务的风格指南和文档，但是他现在注意到这些[实践正在转变](https://devops.com/when-to-use-api-management-and-service-mesh-together/)。[零信任方法](https://containerjournal.com/features/zero-trust-architecture-zta-to-secure-a-nation/)正在影响团队，如果内部 API 是面向外部的，那么在将内部 API 定义和标准化为*时要更加小心。这也缓解了消费。罗达说:“你需要照顾好你隔壁的人，给予他们同样的尊重。”。*

## 对健壮的 API 安全性的日益增长的需求

API 有一个[安全问题](https://securityboulevard.com/2021/07/for-hackers-apis-are-low-hanging-fruit/)。许多人没有正确处理授权，暴露了太多的信息。黑客通常可以提升他们的权限，或者简单地将不同的用户 ID 换成 API 调用，以返回大量敏感数据，甚至对数据进行更改。许多被认为是私有的 HTTP API 端点实际上并不是私有的。因此，OWASP 将破坏对象级授权列为[顶级 API 漏洞](https://owasp.org/www-project-api-security/)。

近年来，我们已经看到了 API 配置不当会发生什么。例如，[脸书 API](https://apisecurity.io/issue-116-facebook-parler-api-vulnerabilities-clairvoyance/) 缺乏对未列出帖子的授权检查，允许客户代表任何用户发帖。类似的授权问题也出现在 [Peleton](https://salt.security/blog/the-peloton-api-security-incident-what-happened-and-how-you-can-protect-yourself) 上，它允许黑客修改任何用户的后端账户。API 不断地处理敏感数据，并且必须小心地遵守全球的各种数据隐私法规。

根据 Rodda 的说法，设计第一的思想对于在 API 生命周期的早期避免安全灾难是至关重要的。这意味着在编码之前，决定一个具有共同设计的结构，并选择合适的[风格指南](http://apistylebook.com/)。“好的文档、好的设计指南和围绕构建具有跨功能性质的东西的良好纪律将增加安全性和可伸缩性，”罗达说。他补充说，当你知道发生了什么，你就有更多的控制权，事情本身就更安全。

## OpenAPI 占上风

OpenAPI 规范，原名 Swagger，是描述 REST web APIs 的行业标准规范。OpenAPI 可以帮助指导 API 的设计和开发。OpenAPI 工具还可以帮助生成有用的文档、沙箱和 SDK，使其成为在合作伙伴之间创建互操作性的有价值的规范。

“OpenAPI 将在一段时间内占据上风，”罗达说。OpenAPI 倡议已经得到了科技行业知名人士的支持。然而，Rodda 估计只有 40%的公司在生产中采用了 OpenAPI。Rodda 说，他相信工具将使更多的组织更容易在他们的组织中保持 OpenAPI 的采用，减少编写“又一个 YAML 文件”的冗余

REST 仍然是迄今为止最被采用的 API 设计风格——根据 RapidAPI 的【2021 年 API 开发者调查报告显示，59.7%的开发者将 REST 用于生产 API。然而，异步事件驱动的通信协议越来越受欢迎，这些协议倾向于选择替代的描述格式，如 [AsyncAPI](https://www.asyncapi.com/) 。Websockets、gRPC 和 [GraphQL](https://devops.com/managing-graphql-at-scale/) 是其他被大量 API 开发者持续使用的选项。

## 开发者体验与用户体验相匹配

另一个主要趋势是开发者体验(DX)越来越重要。DX 类似于用户体验，但都是为了提高开发者消费者的可用性，并改善他们与软件即服务的持续关系。“如今，DX 就像 UI/UX 一样重要，如果不是更大的话，”罗达解释道。"开发人员的经验直接转化为效率和可重用性."

在 API 的上下文中，对开发人员体验的更多考虑意味着减少入门工作并维护更可靠的连接。例如，如果第三方 API 的正常运行时间很短，并且经常引入重大变化，用户可能会寻求其他解决方案。更好的 DX 也可能等同于增加抽象层和更多的代码生成。罗达指出 [GitHub 的 CoPilot](https://copilot.github.com/) 是在未来开发者的工作流程中使用人工智能和自动化的一个例子。

“我们已经发展成为一个开发者社会，”罗达说。正如消费者期望高质量的实时应用程序一样，开发人员也期望高性能的 API。为了帮助实现这一点，一个越来越流行的理念是 [API 即产品视角](https://www.youtube.com/watch?v=dMpI35UXlIU)。“如果你把它当作一个产品来对待，你就是在用与外部共享相同的标准和质量来构建它，”他解释道。"然后，没有注意到遗漏的细节."

## 最终想法:设计第一的心态

比以往任何时候都有更多的行业正在利用 API，API 正在渗透到传统的非技术公司，以帮助他们的内部集成工作。但是，在开放数据时，数据隐私是一个紧迫的问题，需要谨慎的措施。对 OpenAPI 等标准采取设计优先的方法可以帮助组织保持警惕，并确保其服务组合的一致性。

API 经济中还有其他趋势在起作用。例如，一个有趣的 [Web3 计划](https://api3.org/alliance)试图通过让链上智能合约与传统 HTTP APIs 交互来结合区块链和 API 的世界。围绕 GraphQL 也有很多开发活动，它可以作为使用多个 API 的[命令行，从而使集成更加容易。](https://devops.com/graphql-as-a-meta-layer/)

罗达说，最大的收获是，原料药不应再被视为副产品。他把它比作一个建筑工程:当你盖房子时，你必须先有一个蓝图，然后再安装地基、墙壁、屋顶或电气系统。类似地，API 需要坚实的远见来确保稳定性和可伸缩性。