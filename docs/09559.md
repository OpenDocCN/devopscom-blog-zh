# 寻求与现代数据 API graph QL 的统一

> 原文：<https://devops.com/the-quest-to-unify-with-graphql-the-modern-data-api/>

企业软件有一个正在发展的趋势:使用 GraphQL 作为聚合层来统一对底层数据源和 REST APIs 的访问。有人称之为[超图](https://devops.com/supergraph-one-graphql-schema-to-rule-them-all/)，也有人称之为[元层](https://devops.com/graphql-as-a-meta-layer/)。这个想法是，通过向广泛的内部资源提供一个更易消费的层，前端开发人员可以更好地访问他们在构建应用程序时需要的任何数据。但是，将所有数据源统一到一个单一模式的探索并非没有尝试。

GraphQL 的采用正在稳步增长，一些早期采用者中有[大型企业](https://nordicapis.com/6-examples-of-graphql-in-production-at-large-companies/)。例如，[网飞的工程师](https://netflixtechblog.com/beyond-rest-1b76f7c20ef6)最近分享了一种获得关注的方法是“将 GraphQL 微服务(GQLMS)作为后端平台来促进快速应用程序开发”然而，随着 GraphQL 在大型企业中使用的增加，[可伸缩性](https://devops.com/managing-graphql-at-scale/)和[安全障碍](https://devops.com/graphqls-greatest-strength-is-also-its-greatest-weakness/)出现了。这些包括在多个层中保留适当的[授权](https://devops.com/does-graphql-introduce-new-security-risks/)，以及降低固有开放模式的风险。

我最近会见了 Hasura 首席执行官 Tanmai Gopal，讨论了为什么 GraphQL 应该被用作访问和公开底层数据集和 API 的中间件元素。根据 Gopal 的说法，GraphQL 正在成为现代应用程序的数据 API 这可能是一个巨大的积极转变。然而，潜在的缺点是集成所涉及的时间。因此，关键将是自动化数据源的集成，以便开发人员和 DevOps 团队可以专注于他们正在构建的应用和服务，而不是维护数据模型本身。

## 根本问题:数据访问

“数据访问是一个瓶颈，”Gopal 说。“需要自助服务。”

一方面，有数据生产者，如数据库、内部服务和外部 SaaS 服务。另一方面，还有消费这些数据的客户端，比如移动应用、web 应用、微服务和面向第三方开发者的 API。

根据 Gopal 的说法，问题在于双方之间的联系越来越难以实现。集成基于 HTTP 的 API 和解析 JSON 有效负载需要时间。交换协议是不同的，您必须解决数据访问中的性能问题、缓存和并发性。此外，必须为所有数据源维护授权上下文。这些问题变得更加严重，因为不是所有的开发人员都习惯于维护集成的细微差别。

前端开发人员希望与集中式数据存储进行通信，但也需要混合和匹配各种来源。Gopal 解释说，在这一点上，需要一个数据访问层来处理双方之间的通信。这样一个层需要一些集成自动化来真正地将 API 提供给边缘的开发人员。它还需要一个简单、统一的模式——这就是 GraphQL 的用武之地。

## 解决方案:基于 GraphQL 的数据 API

“GraphQL 是一个绝对令人愉快的 API，”Hasura 的联合创始人拉乔希·戈什(Rajoshi Ghosh)说。“使用 GraphQL 作为数据 API 可以消除对集成系统以及如何安全获取数据的传统知识的大量需求。”

这个概念涉及到使用 GraphQL 作为中间数据 API——这将使用所有来源，无论它们是 RESTful APIs、GraphQL 服务、Amazon Aurora 数据库还是 PostgresSQL 风格的数据库——并将它们统一在一个更容易访问、更令人满意的结构中。Gopal 解释说，为了在这些不同的来源上创建统一的 API，中间件解决方案必须将 API 资源映射到逻辑模型和方法，并向逻辑模型添加授权规则。

尽管 GraphQL 支持开发人员的灵活性，但它是难以组装的中间部分。Ghosh 说，从头开始构建这些连接器需要大量的重新学习和繁琐的维护。他补充说，为了真正迎合所有数据源，组织可能需要为遗留数据源制作定制插件。

## 解决统一图问题

[数据驱动的计划](https://devops.com/quality-is-a-top-challenge-for-data-driven-projects/)是一个常见的技术目标，但是数据源的广度正在增加。GraphQL 在整合这些资源和为前端开发人员提供准确调用所需内容的灵活性方面可以发挥重要作用。因此，统一的图形有利于开发人员的体验，但从头开始设置会很有挑战性。

可以说，将 GraphQL 作为多个 API 的聚合层时，授权是最大的挑战。任何统一多个后端 API 的系统都必须确保只有拥有正确权限的人才能访问底层数据。统一的 GraphQL 层必须保留以端点为中心的、特定调用者独有的粒度权限。

“大多数企业没有一个好的授权故事，”Gopal 说。Gopal 说，实现数据 API 的授权很难，因为它不像 REST 那样可以在 URL 请求中指定用户 id。这些种类的细粒度属性级别授权必须作为策略引擎重新创建，并应用于 graph API。例如，Hasura 通过使用一个令牌来实现授权，这个令牌将整个体验限定在特定用户的范围内。

## 统一 API 策略的未来

展望这一领域的未来，Ghosh 指出，前端堆栈变得更加健壮，后端代码实质上正在成为作为无服务器功能部署的业务逻辑。在这个不断增加的抽象的新现实中，建模专家的角色可能会变得更加重要。

此外，GraphQL 必须超越只读功能，以适应另一种趋势— [实时](https://devops.com/how-stream-processing-goes-beyond-real-time/)。Gopal 说，尽管大多数 GraphQL APIs 检索持久数据，但随着实时数据和基于事件的订阅变得越来越普遍，基于 GraphQL 的数据代理也必须发展以实现流。

今天，您可能不需要一下子将所有的数据源统一到一个统一的数据模型中。此活动可能会被归入特定的业务领域或产品，以帮助他们加速和展示概念验证。但 Gopal 表示，在未来几年，采用统一方法的压力将越来越大。“几年后，如果你没有一个统一的 API 策略，你将面临一个巨大的问题。”