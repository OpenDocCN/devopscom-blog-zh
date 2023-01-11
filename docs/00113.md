# MongoDB 2.6:迄今为止最重要的 Mongo 版本？

> 原文：<https://devops.com/mongodb-2-6-significant-release-mongo-yet/>

MongoDB 昨天发布了流行的 NoSQL 数据库的最新版本，2.6 版。我有机会与 Mongo 的产品总监 Kelly Stirman 就发布事宜进行了交谈。这个版本对 Mongo 用户来说充满了好东西。对我来说，其中最重要的是下面新闻稿中强调的新安全功能。此外，MMS 功能使得大规模运行 Mongo 更加容易。Kelly 告诉我的一件事是让第一次使用 MongoDB 的用户更容易安装和运行 MongoDB。这是 2.6 中提到的另一件事。你可以在下面看到完整的细节。

### 宣布 MongoDB 2.6:世界上增长最快的数据库的巨大飞跃

MongoDB 迄今为止最重要的版本带来了操作的简单性和可靠性，主要服务器组件的完全重新架构和企业级安全性

NEW YORK and PALO ALTO, Calif.—April 8, 2014 – [MongoDB](https://www.mongodb.com/) today announced the general availability of MongoDB 2.6, the newest release of the database that defines the standard in modern application development. The release builds on five years of innovation and hundreds of thousands of deployments to simplify provisioning and operating MongoDB deployments, making the database developers love for building apps, the database organizations love to run.

MongoDB 使构建应用程序变得自然而直观——这个版本使运行这些应用程序变得同样自然，释放出任何组织最有价值的资产来创新和推动世界前进，一次一个应用程序。

“MongoDB 的核心在过去五年里为社区提供了很好的服务，”MongoDB 的联合创始人兼首席技术官艾略特·霍洛维茨(Eliot Horowitz)说。“2007 年，我们开始证明新的数据模型可以从根本上改善开发人员构建和运行应用程序的方式。现在，我们通过管理服务推动行业向前发展，改善我们运行应用的方式，让组织专注于他们最擅长的领域。我们有机会设计使用了几十年的主要数据管理系统。这是一项艰巨的任务，但我们有社区、工程人才和必要的资金来实现我们面前的承诺。”

“这个版本将我们构建和运行应用的方式向前推进了一大步。我们正在向彩信引入自动化功能，目前正在对部分用户进行测试。在过去两年中，超过 35，000 名社区成员开始依赖彩信服务。用户现在可以通过一个简单而复杂的界面来配置、升级和管理他们的系统。操作 MongoDB 现在比以往任何时候都更加可靠和轻松。我们已经改进了数据库的几个关键领域的可伸缩性，并完成了对核心的基本更改，这将允许我们在 MongoDB 2.8 及更高版本中改进并发性。我们将添加一些新功能的工作量减少了 100 倍，构建了一个具有巨大创新潜力的复杂查询规划器，重新设计了写操作，并极大地简化了 MongoDB 的维护。这是我们有史以来最大的发行。”

凭借文本搜索、企业级安全性和同类最佳的分析能力，MongoDB 2.6 实现了新的用例类别。该版本的主要功能包括:

[MMS](https://mms.mongodb.com/?pk_campaign=press-release-2dot6)–MongoDB 管理服务简化了组织大规模运行 MongoDB 系统的方式。MMS 现在包括连续、增量备份；时间点恢复；100 多个参数的监控、可视化和警报；面向 MongoDB 用户的本地部署和云中的完全托管解决方案。Alpha 功能包括简单的单击式配置和热升级。

[Index Intersection](http://docs.mongodb.org/master/core/index-intersection/)–Index Intersection 提供了更加灵活、适应性更强的分析功能，使得运行即席分析来回答不断发展的业务问题变得更加容易。开发人员不再需要预先预测所有的数据访问模式，因为可以使用多个索引来优化查询。

[改进的可扩展性&性能](http://docs.mongodb.org/master/release-notes/2.6/#new-write-commands)—组织可以更轻松、更低的成本进行扩展。MongoDB 2.6 提供了更高效的网络资源利用；操作日志处理速度提高了 75%；类的扫描、排序、$in 和$all 性能都有显著提高；用于写入的批量操作符将更新速度提高了 5 倍。

[文本搜索](http://docs.mongodb.org/master/reference/operator/query/text/#op._S_text)–用户已经开始期望搜索成为访问应用程序中数据的主要手段。开发人员现在可以将搜索作为一项功能来提供，而不会增加单独的专用搜索引擎的复杂性。MongoDB 2.6 将文本搜索集成到 MongoDB 查询语言和聚合框架中，并提供了 15 种语言的强大搜索。

[企业安全](http://docs.mongodb.org/master/release-notes/2.6/#security-improvements)–保护数据安全是许多组织的头等大事，MongoDB 2.6 提供了一流的安全功能。基于 MongoDB Enterprise 2.4 对角色、Kerberos 身份验证和 SSL 加密的支持，MongoDB Enterprise 2.6 增加了[字段级编辑](http://docs.mongodb.org/master/reference/operator/aggregation/redact/#pipe._S_redact)、可定制审计、LDAP 和 x509 身份验证、集合级授权和[用户定义的角色](http://docs.mongodb.org/master/core/authorization/#authorization)。

[批量更新操作员](http://docs.mongodb.org/master/reference/method/Bulk/#Bulk)–组织现在可以比以往更高效地处理大量数据。新的批量操作使得在 MongoDB 中加载、更新和删除大量数据变得简单而高效。批量操作会在整个系统中自动并行更新，并返回一个失败操作的报告，应用程序可以重试该报告。

[流水线数据转换](http://docs.mongodb.org/master/release-notes/2.6/#out-stage-to-write-data-to-a-collection)–可以对数据进行汇总、增强、聚合和提炼，以便更好地为数据库中的用户提供服务。MongoDB 2.6 使用简单的声明性接口在数据库中提供多步数据丰富和转换。有了新的 [$out 阶段](http://docs.mongodb.org/manual/release-notes/2.6/#out-stage-to-write-data-to-a-collection)，来自聚合管道的结果集可以写入一个命名的集合，而没有输出大小的限制。

[简化操作](http://info.mongodb.com/rs/mongodb/images/10gen-MongoDB_Operations_Best_Practices.pdf)–MongoDB 2.6 简化并降低了大规模运营 MongoDB 的成本。可以在后台进行[，让位于前台操作，重启后自动恢复；使用 MaxTimeMS，操作员和开发人员可以指定查询的自动取消，从而更好地控制资源利用；](http://docs.mongodb.org/master/core/index-creation/#index-creation-building-indexes-on-secondaries)[混合 SSL](http://docs.mongodb.org/master/tutorial/upgrade-cluster-to-ssl/) 连接；扩展的 [SNMP 支持](http://docs.mongodb.org/manual/tutorial/monitor-with-snmp/)；更高效的维修操作；新的默认空间分配配置提供了更可预测的性能。

MongoDB 首席执行官 Max Schireson 表示:“在短短的五年时间里，MongoDB 社区改变了数据管理格局，创造了 40 年来第一个引人注目的关系数据库替代方案。“我们创建了一个全新的、解放性的数据模型，展示了巨大的吸引力，极大地改善了工程师构建和运行现代应用程序的方式，并获得了资金来确保 MongoDB 在未来几十年内继续运行。随着这一版本的发布，我们在数据库方面进行了大量投资，以确保为持续创新奠定坚实的基础。”

MongoDB 有一个蓬勃发展的全球社区，其开源数据库的下载量超过 700 万次，有 1，000 名客户，150，000 名在线教育注册，30，000 名用户组成员和 20，000 名 MongoDB 日参与者。

立即注册参加 6 月 23 日至 25 日在纽约市举行的 [MongoDB World](http://world.mongodb.com/) ，与来自世界各地的开发人员、运营专业人员和高管一起参加有史以来最大的 MongoDB 活动。

**支持语录**
“2.6 版是一个重要的里程碑。它包含了许多新特性和全面的增量改进。它取消了聚合框架中用于查询大数据的 16MB 输出限制。我们现在可以构建高效、复杂的数据处理工作流，因为 2.6 允许将聚合管道的结果直接存储在另一个集合中，而无需一直发送到客户端。此外，新的网络格式和批处理 API 支持更高效的客户端驱动程序实现，包括更简化的异步 API，可提高客户端吞吐量。我们期待着 MongoDB 的持续创新和稳定执行。”–易贝企业架构师 Yuri Finkelstein

“彩信就像心跳，你根本离不开它。它很容易上手——安装非常合理，整个学习过程非常简单。如果你在生产中使用分片集群，你真的需要 MMS。”–Janne Keskitalo，Polar 公司高级系统经理

“MMS 是我们 MongoDB 工具链中的一个重要组件。监控为我们提供了 MongoDB 的所有信息，我们需要这些信息来确保我们所有客户的系统都是健康的。它还帮助我们看到即将到来的问题，以便我们能够主动接触我们的用户。备份功能与监控无缝集成。我们喜欢它为我们提供的巨大灵活性，包括定制快照、时间点恢复，最重要的是跨分片系统的一致备份。“–约翰内斯·布兰德施泰特，MongoSoup 的厨师长

**资源**
–立即注册参加 MongoDB 首席技术官 Eliot Horowitz 的[“MongoDB 的新功能”](https://bit.ly/1qg9xz0)网络研讨会
–满怀信心地运行 MongoDB，立即设置您的免费[彩信帐户](https://bit.ly/1hcjWJJ)
–观看彩信自动化功能的[演示](https://bit.ly/1gHMBl5)
–下载[“MongoDB 2.6 的新功能”](https://bit.ly/1lNEWJY)白皮书
–[发行说明](http://docs.mongodb.org/master/release-notes/2.6/)

**关于 MongoDB，Inc.**
MongoDB 让开发变得简单而美好。对于成千上万的组织来说，MongoDB 提供了灵活性和扩展的自由。财富 500 强企业、初创公司、医院、政府和各种组织都使用 MongoDB，因为它是现代应用程序的最佳数据库。通过简单性，MongoDB 改变了构建的含义。通过开放性，MongoDB 提升了与软件公司合作的意义。