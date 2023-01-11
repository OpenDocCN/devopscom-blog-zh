# 如何为成功的数据迁移做准备

> 原文：<https://devops.com/prepare-successful-data-migration/>

很难找到有用的、具体的建议来帮助您进行企业级数据迁移项目。有很多地方会出错。关于寻找合适的人、最小化风险或使用自动系统为你做一切的常见建议提供的帮助有限。

你真正需要的是一份你可以逐步完成的清单。

数据迁移的成功或失败在很大程度上取决于您准备的彻底和仔细程度。如果我们分析大型迁移项目，我们总是会发现成功有许多共同的特征。如果您正在计划数据迁移，这些是您真正需要回答的问题:

*正在迁移什么类型的数据？*

并非所有数据都是平等的。有各种不同类型的数据，所以你需要清楚你到底想移动什么。

*   **基于 NAS 的**—网络共享从一个系统迁移到另一个系统。
*   **基于 LUN 的**—磁盘(LUN)在数据块级别从一个地方迁移到另一个地方。
*   **基于虚拟机的**—将整个虚拟主机从一个虚拟机管理程序迁移到另一个虚拟机管理程序。
*   **特定应用**–将一组数据库或对象从一台主机迁移到另一台主机。

这是什么类型的迁移？

数据的去向会对您的整体计划产生重大影响。这是同一数据中心内的本地迁移，还是将数据从一个中心转移到另一个中心的远程迁移，还是云迁移，即将数据从一个云提供商转移到另一个云提供商？

*目前的存储环境如何？*

在移动单个文件之前，您需要对您当前的存储环境有一个全面的了解。如果您使用的是 SAN，那么就操作系统和应用程序而言，请考虑一下涉及到哪些主机。什么是 FC 交换机和 RAIDs？您对 SAN 中的所有相互依赖关系有清晰的了解吗？对环境及其复杂性的深刻理解，会让你有更好的机会避免灾难。

*迁移了多少数据？*

准确估计需要移动的数据量是绝对重要的。您需要考虑所有主机、LUN 和存储系统。光说需要迁移多少 TB 的数据是不够的，您需要了解这些数据是如何分解的，然后才能确定所需的时间和精力。

你有多少时间？

任何项目都有最后期限。您的时间框架可能最终取决于数据量和迁移率，但您只能在全面了解数据、应用程序和环境的情况下确定迁移率。可以各个击破的方式迁移吗？您了解的越多，就越容易控制运营复杂性和降低成本。

*数据有多活跃，可能会停机多长时间？*

为了确定迁移能否按时完成，您需要知道数据的活跃程度。对生产的影响有多大是可以容忍的？一些停机时间是不可避免的，但必须提前制定并达成一致。与所有关键利益相关者一起提前制定正确的策略，将极大地增加你成功的机会，并降低当天的压力水平。

什么是适合这项工作的工具？

这真的取决于你到目前为止的所有回答。选择的正确方法是拟定一份评估标准清单。考虑你需要的所有东西，并创建一个可以与候选人相互参照的列表。

例如，对于 s an 迁移，您可能需要提供以下功能的产品:

*   不中断生产环境的无缝安装。
*   清楚地显示自动发现的 SAN 配置，包括所有要迁移的主机和 LUN(以及那些不可接触的主机和 LUN)的身份、状态和 I/O 统计信息，因此可以准确无误地组织迁移操作。
*   能够在非生产时段迁移，或自动让位于生产流量，强度/调节可调。
*   一个集中的报告系统，提供您需要的统计数据。
*   在转换之前对中间映像进行数据完整性检查，以便在问题引发之前及早标记出来。
*   数据成功迁移后，对数据磁盘进行安全擦除。

当你制定了一个清单，你可以应用它，并看看不同的选择如何比较。

谁是这项工作的合适人选？

成功的数据迁移需要一定水平的专业知识。理想情况下，您希望有经验的人员来处理这样的过程，并且您可能需要从外部寻找他们。如果他们能给你解决我们在这篇文章中提出的问题所需的答案，那么你就知道他们能胜任这份工作。

## 作者简介/林伟德

[![CTOWaiLamCirrus](img/004afc537d748c6b5a844e3c7fe213d0.png)](https://devops.com/wp-content/uploads/2015/09/CTOWaiLamCirrus.jpg)

Wai T. Lam 是 Cirrus Data Solutions 的联合创始人兼首席技术官，该公司是一家为存储区域网络(San)开发数据迁移服务器和数据缓存服务器的公司。他之前是飞康公司的首席技术官和工程副总裁，该公司是他在 2000 年联合创立的。在那里，他是首席架构师，拥有 21 项公司专利中的 18 项。Wai 于 2013 年获得了享有盛誉的中国国家“1000 名顶尖技术领袖”奖。