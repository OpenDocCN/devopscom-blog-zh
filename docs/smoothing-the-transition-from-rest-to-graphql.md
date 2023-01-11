# 平滑从 REST 到 GraphQL 的过渡

> 原文：<https://devops.com/smoothing-the-transition-from-rest-to-graphql/>

自 2015 年开源发布以来，GraphQL 在开发界掀起了风暴。最初由脸书开发的查询语言 GraphQL 对前端开发人员来说是一大福音，因为它使你能够通过一个请求获得你需要的确切数据。这就解决了经典 REST APIs 容易出现的取多和取少的问题。GraphQL 还通过一致的模式和文档提供了良好的开发体验。有些人甚至将 GraphQL 视为一个方便的[元层](https://devops.com/graphql-as-a-meta-layer/)，来聚合多个底层服务，并用简单的命令抽象它们的接口。

出于这些以及更多的原因，许多开发团队正在考虑从 REST 转向 GraphQL。甚至[企业](https://nordicapis.com/6-examples-of-graphql-in-production-at-large-companies/)也开始在[大型生产环境](https://devops.com/managing-graphql-at-scale/)中使用 GraphQL。但是，这些团队如何在不破坏现有集成的情况下进行转换呢？我们如何确保开发人员体验、安全性和访问控制都保持稳定？

我最近会见了 StepZen 的联合创始人 Anant Jhingran，了解从 REST 过渡到 GraphQL 的技巧。根据 Jhingran 的说法，大多数组织看到了采用 GraphQL 的好处，但是对于放弃对 RESTful 架构的多年投资犹豫不决。但是根据 Jhingran 的说法，很少出现“非此即彼”的情况——更多的时候，他看到项目同时运行两种风格，或者将一种风格放在另一种之上。下面，我们将探讨一些在投资 GraphQL 时需要记住的事情。

## 开发者的十年

我们已经在大大小小的公司中实现了无处不在的 web APIs。“事实证明，API 对于软件供应链来说是非凡的，”Apigee 的前首席技术官 Jhingran 说。它们有助于合作伙伴之间共享数据，并使平台生态系统蓬勃发展。Jhingran 描述了在过去的十年中，API 和 [API 管理](https://devops.com/how-are-api-management-and-service-mesh-different/)如何在采用方面达到了[近乎无处不在的顶峰](https://devops.com/api-sprawl-a-looming-threat-to-digital-economy/)。

但是并不是所有的 API 都以相同的方式运行。虽然[表述性状态转移](https://nordicapis.com/all-you-need-to-know-about-rest-api-design/) (REST)是最流行的风格，但它仍然是 web APIs 的一个非常通用的架构指南——数据如何从每个服务中出来仍然是非常微妙的。请求和响应的结构因服务而异，导致[开发者大规模体验停滞](https://devops.com/low-code-opens-api-integration-potential-for-citizen-developers/)。

另一方面，GraphQL“是一种很棒的结构化数据的方式，”Jhingran 说。只需一次调用，您就可以以预期的格式返回客户端所需的显式信息。例如，对于电子商务应用程序，这可能是客户信息、订单号和交付状态。对于前端开发人员来说，通过一个调用显示所有这些内容是一种很棒的体验。而且，GraphQL APIs 易于探索和导航，因为模式是内置的。这是对 REST APIss 的改进，在 REST API 中，文档可能不总是与实际的生产实现相匹配。

“这十年是开发者的十年，”金格兰说。随着企业努力扩大在云市场的影响力，满足开发人员的体验已经变得越来越重要，GraphQL 就是这一运动的一部分。“对于开发应用程序的人来说，这只是更好，”Jhingran 说。

但是仅仅因为前端团队要求 GraphQL 的易用性，并不意味着后端团队可以围绕它轻松地重构他们的整个框架。Jhingran 解释说，正确地做这件事需要很多技巧，而且过程可能会很艰难。

## 很少是 REST Vs. GraphQL

REST 和 GraphQL 经常相互对立，以至于它们看起来像是两极对立。但是在实践中，团队经常使用 GraphQL 来构建已经存在的 API。Jhingran 将最常见的模式描述为“GraphQL 作为一个层来连接各种 REST APIs 之间的点。”要么直接消费 GraphQL，要么作为 GraphQL 之上的 REST 层。“这可能是任何一种方式，”他说。

GraphQL 是一个极好的数据基础设施层，因为它可以混合和匹配数据库后端。本质上，它可以成为构建应用程序的新管道。虽然 GraphQL 在内部构造方面可能很出色，但是在将服务外部化时，游戏的名字是稳定性。REST 的主要目标是减少崩溃的客户端，并确保每个资源的高级安全性。因此，Jhingran 预见了某些用例，在这些用例中，使用围绕 GraphQL 服务的 REST 包装器来交付固定的 JSON 响应将是首选。

另一点是，GraphQL 不仅仅是为了满足前端开发者——它也有一些后端潜力。Jhingran 说:“GraphQL 是一个重塑前端的机会，GraphQL 是一个重塑后端基础设施的机会。这个概念如今很有分量，例如，[网飞的工程师使用 GraphQL 作为微服务架构的后端](https://netflixtechblog.com/beyond-rest-1b76f7c20ef6)。

## 从 REST 过渡到 GraphQL

并不是所有的应用都会在第一天就被改造。团队可能会遇到对新技术的文化抵制。界面的重新设计，尤其是那些向第三方公开的外部应用程序，也必须要求额外的预防措施来保持应用程序的兼容性，以避免破坏性的变化。

因此，有效过渡可能需要时间。“开始和做好不是一回事，”金格兰说。他说，由于最佳实践和工具的竞争，开始使用 GraphQL 的人可能会挣扎几个月。例如，Jhingran 在研究 GraphQL 时确定了两个主要观点:编程和声明性。

*   **编程**:团队使用诸如 Apollo 之类的 GraphQL 库，在 GraphQL 端点之外进行编程。在这种方法中，你只需开始写作。“开始很快,”金格兰说,“但最终你会描述你所做的一切，并在过程中遇到许多突发事件。”。
*   **声明性**:另一种选择是更声明性的方法——不是告诉系统*如何做，*你告诉它*做什么*。比如这个子系统要做 X，这个子系统要做 Y 等等。根据 Jhingran 的说法，采用带有声明性代码片段的工具来创建 GraphQL 端点“从短期*和长期*来看更好。”

## GraphQL 安全性

Salt Labs 2022 年 3 月的一份报告发现，在过去的 12 个月里，基于 API 的网络攻击数量惊人地增长了 681%。现在有许多关于 API 安全性的担忧——这些有价值的端点容易出现[破坏访问控制](https://owasp.org/Top10/A01_2021-Broken_Access_Control/)，数据过度暴露和过度许可状态。

正如我在之前的中[提到的，GraphQL 的安全性与 REST 相比有些微妙。在 REST 范式中，您可以轻松地分配权限，并限制每个资源的调用次数。但是有了 GraphQL，就没那么简单了。因为您可以批量处理多个查询，所以调用者拥有更大的权力，如果没有适当的授权，黑客可能会滥用这种权力。](https://devops.com/graphqls-greatest-strength-is-also-its-greatest-weakness/)

公司可能有理由担心 GraphQL 会带来另一个麻烦。但是根据 Jhingran 的说法，这些担忧都是可以解决的。一个全面的 GraphQL 端点可能需要另一个层来唯一地分割授权，以便为所有资源和后端端点保留一个[最小特权模型](https://accelerationeconomy.com/cybersecurity/understanding-and-deploying-least-privilege-security-models/)。

## GraphQL 的未来

迄今为止，GraphQL 已经获得了适度的重视。但是，金格兰预测在未来两到三年内会出现一个拐点。“多米诺骨牌开始倒下了，”他说。

现在市场上已经充斥着 API，功能之外的特性将会使服务与众不同，并赋予它竞争优势。这包括性能、安全性和开发人员体验，后者使 GraphQL 成为一个有吸引力的提议。这与 GraphQL 工具的[爆炸相结合，无疑将帮助开发人员更好地完成他们的工作。](https://graphcms.com/blog/best-graphql-tools-2021)

展望未来，Jhingran 预测开发人员使用 GraphQL 的可用性和抽象性将会增加。他把它比作网络上杂乱无章的网页是如何通过链接变得相互联系和可搜索的。他解释说，我们在 API 领域也看到了类似的想法，在这个领域，脱节的 API 需要更好的连接。与谷歌如何简化搜索类似，他预见到 GraphQL 和与之一起工作的工具通过用声明性命令抽象复杂性来帮助减少认知负荷。