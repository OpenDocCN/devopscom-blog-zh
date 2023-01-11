# Red Hat 应对数据管理挑战

> 原文：<https://devops.com/red-hat-rises-data-management-challenges/>

Red Hat 正在通过 Red Hat Enterprise Linux (RHEL)的测试版更新来减少或消除 DevOps 团队经常遇到的许多手动任务，该更新解决了与 DevSecOps 和 DataOps 相关的多个数据管理问题。

RHEL 的首席产品经理 Steve Almy 表示，RHEL 的 7.5 版本增加了对 Ansible IT automation framework(红帽现在捆绑在 RHEL 操作系统中)和 OpenSCAP(T1)之间集成的支持，OpenSCAP 是一种最初由国家标准和技术研究所(NIST)开发的安全审计工具。OpenSCAP 为 IT 管理员提供了安全设置的基准，以便与他们的 Linux 部署的当前状态进行比较。Almy 说，然后他们可以调用声明性 Ansible 框架来自动解决 OpenSCAP 审计提出的任何问题。

同样，Red Hat 还使在启动时安全解锁网络绑定的磁盘加密设备变得更加容易，同时通过为精确时间协议(PTP)和网络时间协议(NTP)添加绑定接口，增加了时间戳和同步需求。

此外，为了减少数据管理难题，Red Hat 现在基于去年收购 Permabit 获得的技术，嵌入了对重复数据删除和压缩软件的支持。Alby 说，目标是使 IT 组织能够在数据存储到磁盘之前，对运行在服务器上的数据执行这些任务。在许多情况下，这可能消除了为存储系统购买、部署和管理单独的重复数据消除和压缩软件的需要。这种方法也间接有利于 DataOps，这是一个新兴学科，许多组织正试图通过它来实现数据管理和将数据输入应用程序的管道的现代化。

RHEL 7.5 中添加的其他管理功能包括更易于使用的驾驶舱管理员控制台，用于管理存储、网络、容器和其他服务，以及“已知良好”的可启动快照，有助于在修补软件后加快恢复和回滚。

Almy 说，Red Hat 更加注重消除阻碍 IT 管理员在特定时间内完成更多任务的许多摩擦。我们的目标不是消除对 IT 管理员的需求，而是消除那些使 IT 管理变得更加耗时的任务。Red Hat 的大部分策略都基于一个可行的自动化框架，该框架不要求 IT 管理员知道如何编程来自动化底层 IT 环境的管理。

尚不清楚数据管理的简易性对 It 决策的影响有多大。然而，在相对平等的条件下，敏捷编程时代的 IT 管理员正试图管理比以往更多的工作负载。大多数组织没有增加额外的 IT 运营人员，主要是因为很难找到并留住他们。这意味着通过随时随地采用 IT 自动化来简化开发运维流程，确保现有 IT 管理员比以往任何时候都更加高效。

— [迈克·维扎德](https://devops.com/author/mike-vizard/)