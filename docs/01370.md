# mLab 在 AWS 上推出私有环境

> 原文：<https://devops.com/mlab-launches-private-environments-aws/>

*Developers can now peer their AWS VPCs to their mLab Private Environments to create their own private networks isolated from the rest of the cloud datacenter*
**San Francisco – June 22, 2016 –** [mLab](http://www.mlab.com/), the fully managed cloud database service featuring automated provisioning, scaling, and management of MongoDB databases, today announced the private beta of Private Environments. mLab Private Environments are virtual private networks that customers can provision to house their various database deployments hosted with mLab.Private Environments provide the security benefits of self-hosting database deployments without the headache of self-hosting. With Private Environments, customers can use all of the traditional network security best-practices and techniques for designing their application. Customers can:

*   将他们的数据库与公共网络隔离，同时允许对他们的应用程序基础架构进行安全访问

*   使用 CIDR 范围和 AWS 安全组创建复杂的网络拓扑，以确保对其数据库部署的最低权限访问

*   自动扩展其应用程序层，而无需修改数据库防火墙规则

Lyft 首席技术官克里斯·兰伯特表示:“作为私有环境的早期测试用户，我们非常欣赏它提供的额外安全级别。“私有环境创建的私有网络在我们不断发展的过程中保持了我们基础设施的安全，并使我们的团队能够轻松配置新的应用服务器和自动扩展，而无需修改数据库防火墙规则。我们已经使用 mLab 的云托管 MongoDB 好几年了，它在帮助 Lyft 扩展方面发挥了很大作用。”

新解决方案旨在为客户提供一种通过 DBaaS 提供商使用虚拟专用网络的全新方式。对于私有环境，mLab 创建了一个独立的自包含解决方案，该解决方案可以安全、无缝地集成到现有堆栈中，就像数据库位于客户自己的 VPC 中一样。其结果是网络安全既易于操作又灵活。

mLab 的云数据库即服务平台托管超过 300，000 个 MongoDB 部署，为 Turner、Lyft 和 Whole Foods Market 等公司提供支持。随着 mLab 继续推出新的云基础架构功能，Private Environments 是计划于 2016 年发布的几个版本中的第一个。

mLab 首席执行官 Will Shulman 表示:“mLab 无疑是在 AWS 上运行 MongoDB 的最简单方式。“我们认为，持续管理数据库基础设施不是大多数开发人员应该担心的事情；mLab 的平台和工具旨在自动供应、托管、扩展、监控和备份您的 MongoDB 数据库。私有环境是一项强大的新功能，有助于 mLab 实现提供简单安全的云基础架构解决方案的目标。我们很期待开发人员能试用它。”

**资源**

*   [mLab](https://mlab.com/)
*   [mLab 支持](/cdn-cgi/l/email-protection#9ae9efeaeaf5e8eedaf7f6fbf8b4f9f5f7)
*   [mLab 推特](https://twitter.com/mlab)

**关于 mLab**

mLab 是一种完全托管的云数据库服务，其特点是自动化配置和扩展 MongoDB 数据库、备份和恢复、全天候监控和警报、基于 web 的管理工具以及专家支持。mLab 的数据库即服务平台为 AWS、Azure 和谷歌的数十万个数据库提供支持，并允许开发人员将注意力集中在产品开发上，而不是运营上。

mLab 总部位于旧金山的 Mission/Potrero 地区，由主要的风险投资者和天使投资者支持，包括 Foundry Group、Baseline Ventures、professional Ventures、Freestyle Capital 和 TechStars 的 David Cohen。