# 手动过程给开发周期带来风险的三种方式

> 原文：<https://devops.com/3-ways-manual-processes-risking-development-cycle/>

在我从事 IT 的二十年中，我看到了对敏捷及其相关方法的需求在增长。然而，与此同时，我目睹了数据库被遗忘。

我是 DBmaestro 的联合创始人兼首席技术官，该公司最近进行了一项名为“[数据库部署&开发风险](http://www3.dbmaestro.com/database-deployment-and-development-risks-survey-report)的调查，以深入了解与各种数据库开发实践相关的风险。调查的重点是整个开发周期中使用的手动流程。

结果揭示了两个不同的现实:尽管来自不同部门的受访者普遍认识到与数据库的手动过程相关的风险，但许多组织继续使用不能完全自动化开发周期的过程和解决方案。

这一点特别明显的一个方面是源代码控制。开发团队必须能够信任他们的源代码控制。但是，即使使用了标准的源代码控制解决方案，70%的被调查者仍然在插入手动过程。

这意味着，即使这些专业人士中的许多人都有某种类型的解决方案，他们仍然会看到明显的现实风险，因为:

**1。**当集成变更时，一个开发人员可能会错误地用来自其他开发分支的旧版本覆盖有效的变更，这是一个潜在的问题，近 90%的调查受访者将此与风险联系在一起。尽管如此，超过一半(53 %)的被调查 IT 专业人员集成了变更，创造了这种覆盖可能发生的可能性。

将近四分之三(70%)的人报告说他们有数据库源代码控制，但是 53%的人报告说他们仍然有一些问题，需要一个更合适的源代码控制解决方案来解决。在这种情况下，实现的源代码管理工具有问题。

**2。**数据库可能与版本控制库不同步。接受调查的 90%的 IT 专业人员将这些来源与风险不同步的可能性联系在一起。此外，72%的被调查者承认他们的数据库可能与版本控制库不完全同步。

**3。**在没有首先验证每个数据库对象及其版本控制修订以确保每个数据库对象是最新的情况下引入更改是一个过程，近 90%的调查参与者将此过程与风险联系在一起。尽管人们普遍意识到在引入变更之前不验证数据库对象和数据库源代码控制之间的准确性是一种危险的做法，但仍有 53%的人继续这样做。

这意味着剩余的 47%的受访者不信任他们关于数据库代码的源代码控制解决方案，并在引入更改之前实施步骤来验证它与数据库匹配。

虽然插入手动步骤有助于降低与覆盖数据库中的关键更改的可能性相关的风险，但这非常耗时，并且手动中断连续交付周期会带来自身的风险。当您不能完全信任源代码控制时，当脚本在数据库中更新时，处理相同数据库代码或对象的两个开发人员可以很容易地覆盖或恢复另一个开发人员引入的关键更改，有时会带来灾难性的后果。

只有覆盖从开发到构建和部署的数据库生命周期管理(DLM)的[数据库强制源代码控制](http://www.dbmaestro.com/product/database-enforced-source-control/)解决方案，才能为您的数据库开发资产创建“单一真实来源”。这允许您获得对您的源代码控制的信任，并实现当今开发周期需求的快速变化——而不用用耗时的手动步骤来堵塞流程。数据库强制源代码控制促进了对源代码的完全信任，允许开发人员同时处理相同的数据库对象，而没有在更新脚本时覆盖重要更改的风险，促进了分散的开发团队之间的真正同步。

下载 2015 " [数据库部署&开发风险](http://www3.dbmaestro.com/database-deployment-and-development-risks-survey-report)的完整结果

**关于作者:**
[![image001](img/8e89bd6995b28794378071ce48f5ad84.png) ](https://devops.com/wp-content/uploads/2016/01/image001.jpg) Yaniv Yehuda 是 [DBmaestro](http://www.dbmaestro.com/) 的联合创始人兼 CTO，这是一家专注于数据库开发和部署技术的企业软件开发公司。Yaniv 也是以色列市场 IT 服务提供商 Extreme Technology 的联合创始人和开发主管。他是以色列国防军计算机中心 Mamram 的队长，在那里他担任软件工程经理。