# 谷歌修改混合云战略

> 原文：<https://devops.com/google-revamps-hybrid-cloud-strategy/>

在 [Google Cloud Next 2019](https://cloud.withgoogle.com/next/sf) 大会上，谷歌宣布将在其自有云和内部平台以及第三方云服务上以 Anthos 品牌提供基于 Kubernetes 的云服务。比如亚马逊网络服务(AWS)和微软 Azure。谷歌还宣布了一个名为 Anthos Migrate 的工具，它可以将任何虚拟机封装在一个容器中，然后可以迁移到 Anthos Migrate 上。包括思科系统、惠普企业(HPE)、联想、戴尔 EMC、VMware 和英特尔在内的 30 多家供应商合作伙伴宣布支持谷歌混合云战略的最新扩展。

谷歌现在也在为 Apigee API 管理平台提供测试版运行时，可以在任何地方使用。被称为 [Apigee hybrid](https://cloud.google.com/blog/products/api-management/choose-your-own-environment-with-apigee-hybrid-api-management) 的谷歌在 2016 年收购了 API 管理平台。

此外，谷歌正在与 Confluent、MongoDB、Elastic、Neo4j、Redis Labs、InfluxData 和 DataStax 合作，提供一组托管的数据库服务。

该公司还宣布了 [Cloud Run](https://cloud.google.com/blog/products/serverless/announcing-cloud-run-the-newest-member-of-our-serverless-compute-stack) ，这是一种基于 Knative 中间件的托管无服务器计算产品，谷歌开发该产品是为了使运行在 Kubernetes 集群上的应用程序能够动态调用无服务器计算框架。谷歌还宣布，它正在更新其应用引擎无服务器计算框架，以增加对 Node.js 10、Go 1.11 和 PHP 7.2 运行时的支持，以及对 alpha 中 Ruby 2.5 和 Java 11 运行时的支持。

最后，谷歌更新了其功能编程框架和用于创建虚拟专用网络的虚拟专用连接(VPC)软件，同时还透露其在盐湖城和韩国首尔增加了[个地区](https://cloud.google.com/blog/topics/infrastructure/google-cloud-announces-new-regions-in-seoul-and-salt-lake-city)。现在总共有 22 个 GCP 地区。

像其他云服务提供商一样，谷歌继续大力投资托管服务，通过托管服务，谷歌基本上充当应用程序开发人员的 it 运营团队。就谷歌作为托管服务提供的数据库而言，这些服务与众不同之处在于，它们是与监管维护和更新这些数据库的开源项目的公司合作提供的。

当然，DevOps 团队需要确定他们希望在云中部署和管理开源数据库的程度，而不是依赖 Google 及其合作伙伴。谷歌云基础设施合作伙伴关系负责人马文德·辛格(Mavinder Singh)预测，长期趋势将是更加依赖作为服务提供的数据库，以允许组织将更多资源集中在开发应用程序上。

DevOps 团队日益面临的挑战是，云计算的下一个阶段比前一个阶段要复杂得多。在云计算的第一阶段，大多数组织将基于 VMware 虚拟机的内部 IT 环境替换为可用于云基础架构的虚拟机。第二个阶段更加复杂，因为单一应用程序现在被所谓的云原生应用程序所取代，这些应用程序基于运行在虚拟机上的 Kubernetes 集群实例，这些虚拟机通过无服务器计算框架得到增强。大多数 IT 组织尚不具备独自部署、管理和保护这些云服务所需的技能。然而，随着运行云原生应用程序所需的平台的自动配置变得越来越容易，许多 it 组织可能更喜欢依赖他们自己的内部 DevOps 团队，而不是签订托管服务合同，特别是如果这些托管服务不容易符合这些组织已经采用的 DevOps 流程。

组织可能需要一段时间来确定哪条道路最终最适合他们。但有一点是明确的，云服务提供商正在大力投资，直接向开发人员提供托管服务，以在迅速成为商品的 IT 基础设施服务之上增加价值。

— [迈克·维扎德](https://devops.com/author/mike-vizard/)