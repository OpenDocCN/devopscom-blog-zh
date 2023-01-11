# Storj 实验室推出分散存储服务

> 原文：<https://devops.com/storj-labs-unfurls-decentralized-storage-service/>

Storj Labs 根据从服务器到个人台式机等设备上的剩余容量，推出了一个分布式存储平台。

公司首席执行官 Ben Golub 表示，目标是为 IT 组织提供一种替代方案，使用经过 Storj 实验室审查的存储资源来廉价地存储数据。

Storj Labs 提供的 [Tardigrade 分散式云存储服务](https://www.prnewswire.com/news-releases/storj-labs-announces-production-launch-and-general-availability-of-tardigrade-the-worlds-first-enterprise-grade-decentralized-cloud-storage-service-301026694.html?tc=eml_cleartime)的核心是一个开源对象存储系统，它与亚马逊网络服务(AWS)定义的 S3 应用编程接口(API)兼容。该对象存储系统将文件的 80 个切片分布在成千上万个节点的子集上，每个节点仅包含在需要时重建该文件所需的数据切片。重建一个文件只需要其中的 29 个切片，所以 Golub 说，确保数据安全相对简单，无需管理加密密钥。

在对 Tardigrade 进行广泛的测试后，该公司声称已经实现了 99.95%的可用性，在耐用性方面达到了 99.9999999%的服务级别协议。Golub 表示，Tardigrade 利用擦除编码来确保数据以高度弹性的方式分布。

![](img/a2440586c49c09bac58cfd27b033659b.png)

Golub 说，Storj Labs 对拥有者和数据中心以及使用大量多余存储容量的个人进行补偿，以使容量可用。大多数存储驱动器都没有接近满容量，Golub 指出，这使得 Storj Labs 可以相对容易地为其 Tardigrade 服务积累 19PB 的存储空间。每个存储容量提供商都需要在一段时间内通过一系列数据管理测试，然后才能被允许成为 Tardigrade 服务的成员。

Storj Labs 还建立了一个开源合作伙伴计划，通过该计划，任何带有 Tardigrade 连接器的开源项目都将获得该软件用户产生的存储收入的一部分。Golub 说，这种方法允许项目参与者作为云服务提供商的替代方案获得部分补偿，云服务提供商通常将开源软件商业化，而不帮助资助其开发。根据他以前担任 Docker Inc .首席执行官的经验，他指出许多开源项目之所以夭折，仅仅是因为创建它的团队无力维持它。

他说，鉴于过去三年云存储服务价格没有出现有意义的下降，对于某些用例来说，对作为公共云替代方案的缓步分散云存储服务的兴趣可能很高。应该证明特别有吸引力的使用案例包括数据保护和图像保留。Storj Labs 还提供了一个绑定库，可用于 Go、Android、C。NET/Xamarin、Node.js、Swift 和 Python 来让开发者更容易地调用 Tardigrade 存储服务作为代码。

It 组织完全接受分散存储服务作为公共云的替代方案可能还需要一段时间。然而，随着需要存储的数据量持续增长，可能很快就需要存储数据的每一个可用选项。

— [迈克·维扎德](https://devops.com/author/mike-vizard/)