# 为什么 GraphQL 会称王

> 原文：<https://devops.com/why-graphql-will-reign-king/>

经过多年的开发， [GraphQL](https://graphql.org/) 将成为数据获取的首选 API。但是 GraphQL 是什么呢？简而言之，它是一种查询语言，允许您从任何服务器获取数据，并且它是其他 web 服务开发风格的一种值得注意的替代方式，如[表述性状态转移](https://devops.com/smoothing-the-transition-from-rest-to-graphql/) (REST)和简单对象访问协议(SOAP)。GraphQL 将主宰 DevOps 世界的原因有几个，包括其整体效率、与任何服务器协同工作的能力以及整体易用性。

### 了解 GraphQL

GraphQL 是一种用于 API 的查询语言，也是用现有数据完成查询的运行时。GraphQL 为 API 中的数据提供了一个完整且易于理解的描述，让客户能够准确地询问他们需要什么，使 API 更容易随时间发展，并支持强大的开发工具。

### GraphQL 的主要优势

GraphQL 解决了许多经常拖开发人员后腿的痛点，开发人员在构建应用程序时优先考虑适应性和快速高效地工作。

首先，它比其他数据查询语言灵活得多，允许用户精确地指定他们想要的数据以及数据的格式。其他数据查询语言要求用户检索特定格式的所有数据，而不管他们是否真正需要这些数据。过量的、不必要的摄入会导致延误和混乱。

由于其简单直观的语法，GraphQL 的易用性也是非常宝贵的。这种语言是强类型的，这意味着开发人员可以在代码投入生产之前的开发过程中尽早发现错误。从长远来看，这可以节省急需的时间和金钱。

另一个好处是，它可以用于从多个数据源获取数据，因为它使用了一个模式来定义不同类型的可用数据。这意味着，如果开发人员在模式中有一个字段可能从多个来源返回数据，他们可以指定从哪个来源获取数据。开发人员没有从其他数据查询语言中获得这种好处，其他数据查询语言通常只允许从单一来源获取数据。

### DevOps 团队相对于其他数据查询语言的优势

随着软件开发世界的不断成熟，DevOps 团队用来构建和操作他们的应用程序的工具和技术也在不断成熟。

REST 和 SOAP 是流行的 web 服务技术，但是它们有一些主要的缺点。值得注意的是，REST 和 SOAP 都严重依赖 URL 结构和冗长的 XML 有效负载，这使得在不破坏现有客户端的情况下发展 API 变得很困难。因为每个端点都是一个唯一的 URL，所以在 API 的不同部分提供一致的体验是一个挑战。REST 和 SOAP 也很繁琐，很难优化性能。

与 REST 相比，GraphQL 为所有数据请求提供了一个端点，并且比许多 HTTP 请求要快得多。GraphQL 的声明式查询语言精确地指定了所需的数据——不多也不少——增加了带宽并提高了性能。应用程序可以运行得更快，使用的资源更少，这对于需要轻量级和快速的移动应用程序尤为重要。

理解数据对于 DevOps 团队来说至关重要，GraphQL 允许开发人员在图形中可视化数据。团队可以更容易地看到不同点之间的关系，从而就操纵数据的最佳方式做出更明智的决策。

进行 API 调用时效率的提高也是 GraphQL 的一个优点，它可以帮助团队通过一个 API 调用检索他们需要的所有信息。传统的 REST API 通常需要多个 API 调用，这主要是因为 REST API 中的每个资源都由自己唯一的 URL 表示，同时还有自己的权限集和需要检索的数据。GraphQL 可以消除这个瓶颈。

总的来说，当开发人员使用 GraphQL 时，处理复杂性大大降低。当使用传统的 REST APIs 时，编写大量代码来处理不同的边缘情况和错误情况是正常的。但是 GraphQL 简化了这一点——大部分复杂性可以由服务器本身处理，为更简单、更易维护的代码库让路。DevOps 团队还能够通过使用基于模式的方法来分离他们的前端和后端开发工作。GraphQL 使前端和后端组件可以分开开发，而不用担心中断更改，这意味着更快的开发周期和更少的错误。

未来几年，组织需要理解、组织和查询的数据量只会增加。DevOps 团队可以利用 GraphQL 及其无与伦比的能力，为数据获取和操作提供高效、强大和灵活的 API，从而在持续的数据和信息冲击中领先一步。