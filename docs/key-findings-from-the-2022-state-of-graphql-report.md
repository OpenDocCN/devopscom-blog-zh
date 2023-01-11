# 2022 年 GraphQL 报告的主要发现

> 原文：<https://devops.com/key-findings-from-the-2022-state-of-graphql-report/>

开源查询语言 GraphQL 在过去的几年里越来越受欢迎。这种语言非常适合前端开发，因为它创建了一个[可用接口](https://devops.com/getting-started-with-graphql-apis/)来精确地获取特定客户端所需的数据。您还可以使用它来聚合多个后端服务和数据源。

研究表明，围绕 GraphQL 的[生态系统正在成熟——它拥有非常全球化的用户群，并且有越来越多的工具可以帮助它的采用。](https://devops.com/managing-graphql-at-scale/) [2022 年 GraphQL 状态报告](https://2022.stateofgraphql.com/)发现，61.8%的开发者对生态系统的整体状态感到满意。然而，许多原生 GraphQL 特性没有被开发人员使用，这表明从新手到高级用户，使用该技术的经验层次非常广泛。这表明增长和知识共享的空间很大。

下面，我将回顾 2022 年 GraphQL 状态报告的关键要点，考虑总体使用数据并关注特定功能的受欢迎程度。我们还将强调与 GraphQL 结合使用来完成工作的标准工具的状态。

## 分析总体使用统计数据

首先，在今天的生产中，GraphQL APIs 的类型有很大的差异，从私有端点到公共端点。该报告发现，47.9%的开发人员使用 GraphQL 来公开用于个人网站或应用程序的 API，40.4%的开发人员将其用于内部使用的私有未公开 API，19.5%的开发人员使用 GraphQL 公开用于第三方开发人员消费的 API。这证明了它适应多种情况的灵活性。虽然大多数连接到 GraphQL APIs 的客户端包括浏览器(62.3%)，但它通常由其他客户端类型使用，如本地移动应用程序、其他服务器和桌面应用程序。

之前，我们讨论了使用 GraphQL 作为[组合层](https://devops.com/graphql-as-a-meta-layer/)来组合底层 API 和服务。该报告支持这一观点，即开发人员通常使用它来聚合各种数据源:55.4%的 GraphQL APIs 访问数据库，而 35%使用 REST APIs，14.6%使用*其他* GraphQL 端点。

就好处而言，一个优点是能够为 API 中的每个对象实施和验证类型。用户发现其他最大的好处是避免[过度消耗](https://nordicapis.com/how-to-avoid-overfetching-and-underfetching/)和聚集请求。然而，一些障碍仍然存在。这些主要缺点包括错误处理、性能问题、客户端缓存和[安全问题](https://devops.com/graphqls-greatest-strength-is-also-its-greatest-weakness/)。

关于用户群统计，大多数用户使用 GraphQL 不到五年。如果我们看看使用 GraphQL 的行业类型，我们会发现它主要用于编程和技术行业。其次是电子商务和零售(16.4%)、金融(8.9%)和新闻、媒体和博客(7.2%)。

## 许多高级功能没有被使用

大多数用户仍然没有注意到许多更高级的 GraphQL 特性。例如，live queries 是一个帮助从 GraphQL 服务器获取实时数据的特性，然而只有 25%的人知道它并使用过它。超过一半的受访者从未听说过`@skip`，这是一种根据传递给它的值跳过某个字段的指令。类似地，其他指令如`@specifiedBy`、`@defer`和`@stream`也很少或根本不知道或使用。

如果我们考虑未调整的安全性和性能特性，那么分析特性使用情况就变得有点严肃了。例如，只有 43.2%的受访者禁用了查询自省。禁用查询自省是[建议的安全最佳实践](https://www.apollographql.com/blog/graphql/security/why-you-should-disable-graphql-introspection-in-production/)以限制黑客执行监控的能力。但是正如我们之前报道的，[模糊的安全性不足以保护 GraphQL](https://devops.com/graphql-security-by-obscurity-just-isnt-enough/) ，通常还需要额外的安全性强调。

由于大多数 GraphQL APIs 是为个人或私人场景设计的，您可能会认为应该利用更多的安全特性来限制自省和拒绝服务攻击的威胁。然而，该报告发现，查询超时、查询速率限制和[查询成本分析](https://blog.devgenius.io/a-principled-approach-to-graphql-query-cost-analysis-8c7243de42c1)等安全和性能特性的使用率和认知度较低，所有这些特性都可以用来遏制恶意行为。

## 与 GraphQL 结合使用的工具

开发人员经常寻求组合、聚合或合并来自不同 API 的 GraphQL 模式。为此，Apollo Federation 是最常见的解决方案，有 22.5%的受访者使用。其次是模式拼接(16.9%)、GraphQL 模块(4.4%)和 GraphQL Mesh (2.9%)。

看看 connection 中使用的其他技术，Next.js 是最流行的框架，PostgreSQL 是最常用的数据库。TypeScript 和 JavaScript 是编写 GraphQL 后端最常用的语言。开发人员还使用 ide 的平衡组合来查询和测试端点，包括 GraphQL、GraphQL Playground、Postman、Apollo Studio 和失眠症。

该报告还发现，GraphQL 代码生成器模式构建器、Apollo 客户端和 Apollo 服务器等工具的使用率和保留率相对较高。数据显示了一个拥挤的解决方案市场，其中 Apollo 是一个行业领先的异常值，许多其他客户端、服务器、API 生成器和模式构建器具有中高保留率，但使用量却少得多。

## 最后的想法

[2022 年 GraphQL 状态报告](https://2022.stateofgraphql.com/)揭示了一些关于 GraphQL 状态的有趣信息，证实了我们最近在博客上报道的许多兴趣和趋势。当然，在许多领域还有更多要说的，比如[平滑过渡到 GraphQL](https://devops.com/smoothing-the-transition-from-rest-to-graphql/) 。

一个关键的发现是开发人员利用的安全特性数量很少。需要更加重视 API 安全性，以[避免事故](https://securityboulevard.com/2022/11/more-api-inventory-auditing-necessary-to-limit-incidents/)并保持[零信任方法](https://nordicapis.com/understanding-the-need-for-zero-trust-architecture/)。这种强调是应对持续的[软件供应链威胁](https://accelerationeconomy.com/cybersecurity/why-and-how-the-software-supply-chain-is-increasingly-under-threat/)的重要组成部分，将需要围绕 [GraphQL 安全最佳实践](https://devops.com/does-graphql-introduce-new-security-risks/)的更多意识和思想领导力。

2022 年 GraphQL 状态调查从 2022 年 6 月 15 日持续到 2022 年 7 月 15 日，收集了 3094 份回复。以上分析只是触及了表面，还有许多其他见解。更多的发现，你可以[在这里](https://2022.stateofgraphql.com/en-US/usage)阅读完整的结果。