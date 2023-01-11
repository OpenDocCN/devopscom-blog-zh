# Hasura 为 GraphQL 引擎添加了连接功能

> 原文：<https://devops.com/hasura-adds-join-capability-to-graphql-engine/>

Hasura 今天宣布，它已经扩展了它的 GraphQL 引擎，使其能够连接多个来源生成的数据。

Hasura 首席执行官 Tanmai Gopal 表示, [GraphQL Joins](https://hasura.io/blog/introducing-graphql-joins-for-federating-data-across-graphql-services/) 使得连接来自不同 GraphQL 服务的数据成为可能，然后可以通过单个 GraphQL 应用程序编程接口(API)访问这些数据。他补充说，Hasura GraphQL 引擎支持的联邦功能扩展消除了对连接数据所需的自定义代码的需求。

Hasura 引擎自动从数据源生成 GraphQL 模式，然后可以用来加速 API 的开发。Gopal 说，GraphQL Joins 扩展了这种联合能力，现在包括多个 GraphQL，并最终包括通过例如遗留 REST APIs 访问的其他数据源。他补充说，这种能力将使更广泛的开发人员更容易构建跨多个来源聚合数据的应用程序。

核心的 Hasura 引擎基于开源软件，该公司声称该软件现已被下载超过 5 亿次。Hasura 提供了一个基于核心引擎的云服务。Gopal 指出，这种方法消除了 IT 团队在将 GraphQL APIs 添加到已经有一系列内部 IT 团队需要支持的 API 的应用程序环境时遇到的后端复杂性。

GraphQL 最初是由脸书创建的，现在还不清楚 GraphQL APIs 会在多大程度上取代 REST APIs。开发人员倾向于使用 GraphQL APIs，因为它们对访问哪些数据提供了更细粒度的控制。挑战在于公开 GraphQL APIs 的后端服务的数量仍然相对有限。大多数 IT 团队不会在一夜之间用基于 GraphQL 的 API 替换 REST APIs，但是依赖 GraphQL APIs 的新应用程序的比例将稳步增长。DevOps 团队正在寻找更简单的方法，通过 GraphQL API 为开发人员提供对后端服务的访问，他们可以使用 Hasura 引擎来自动化这个过程。

总体而言，随着更多基于微服务的应用程序的部署，IT 环境中采用的 API 数量正在快速增长。每个微服务都生成自己的 API。随着时间的推移，IT 团队会发现自己管理着一系列类型的 API，以支持一个组织可能同时启动的多个数字业务转型计划。除了构建 API 之外，这些组织中的许多现在都通过另一个组织公开的 API 来消费数据。随着时间的推移，API 和应用程序之间的相互依赖程度将使应用程序环境变得更加复杂。好消息是，API 使得升级——甚至替换——后端服务变得更加容易，而不会中断应用服务。

然而，并不总是清楚 It 组织中谁将管理这些 API。它们通常由开发人员创建，然后由 IT 运营团队来维护。用不了多久，it 团队就会发现自己管理数百个，甚至数千个 REST 和 web 服务 API——很快，这可能包括许多使用 GraphQL 构建的 API。