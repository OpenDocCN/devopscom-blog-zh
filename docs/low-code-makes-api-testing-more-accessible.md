# 低代码使得 API 测试更加容易

> 原文：<https://devops.com/low-code-makes-api-testing-more-accessible/>

原料药的数量和商业价值都在上升。但是随着这种增长而来的是越来越多的[漏洞](https://devops.com/tips-to-strengthen-api-security/)，这可能会影响云服务的依赖性和内部 API。随着云服务用新版本发展他们的 API，功能和正常运行时间也会受到影响。因此，API 端点测试对于确保可靠的后端至关重要。随着整个组织对稳定这些集成越来越感兴趣，我们如何以非开发人员可以掌握的可重复的方式测试 API？

[低代码平台](https://devops.com/7-forces-driving-the-low-code-movement/)——利用可视化编程模型实现工作流的工具——正在为[公民开发者](https://devops.com/how-to-foster-a-culture-of-citizen-developers/)打开大门，以可视化模式构建应用程序。类似地，低代码概念可以通过提供一种更简单的方法来创建 API 测试以验证功能和正常运行时间，从而有助于 API 测试。这可以用一种更简单的方法来测试高价值的集成和它们的 UI 表示，来武装质量保证、DevOps 和站点可靠性专业人员。

在日益增长的无头运动中，API 正在为许多终端用户体验提供动力。然而，在[开发人员短缺](https://devops.com/low-code-an-oasis-during-developer-drought/)期间，寻找具有集成知识的人才可能是一个挑战。

我最近会见了来自 Mabl 的 Dan Belcher，讨论如何将低代码和 API 测试结合起来。在这里，我们将揭示为什么非工程师很难进行 API 测试，并考虑 API 测试必须解决的问题，以确保今天的软件满足明天的数字创新需求。

## API 测试的低代码方法

近年来，软件领域发展迅速。“许多力量结合起来创造了令人难以置信的大量变化，”贝尔彻说，引用 DevOps、CI/CD、API economy 和敏捷企业作为例子。在这个时代，应用程序变得更加动态，破坏了团队进行端到端质量测试的方式。

基于 API 的云服务是这一新领域的一部分，成为现代应用程序中受欢迎的构件。然而，随着云服务的发展和升级，集成需要维护。如果没有对基于 API 的云服务的持续测试，组织很容易遭受重大变更和糟糕的可用性。

不幸的是，就目前的情况来看，典型的 QA 团队没有很好地准备来处理正在进行的 API 回归测试。相反，“历史上，开发人员是唯一理解 API 测试的人，”Belcher 解释道。多年来，API 测试一直被归入开发人员的领域，他们使用像 Postman 这样的工具来执行单元级测试。但是为什么 API 测试对别人来说那么难呢？

## 是什么让 API 测试变得困难？

首先，非工程师通常更习惯于基于 UI 的测试。贝尔彻解释说，这些环境使用一种为任何人设计的结构，使定位字段和确认值变得容易。说到 API 测试，您经常必须处理大量的 JSON 响应来匹配字段和表面问题。Belcher 解释说，测试 API 响应通常需要编写代码，解析 JSON 并将其写入变量，这对于非开发人员来说可能很难实现。

或者，在测试异步端点时会出现困难，Belcher 补充道。异步 API 通常涉及后台服务器进程，需要一段时间来响应。这是在事件驱动架构(EDA)成为发展趋势的时候出现的。以最近[加入 Linux 基金会](https://www.linuxfoundation.org/en/press-release/linux-foundation-will-host-asyncapi-to-support-growth-and-collaboration-for-industrys-fastest-growing-api-spec/)的 [AsyncAPI](https://www.asyncapi.com/) 为例，它是 EDA APIs 的标准 API 规范。一份[最近的报告](https://rapidapi.com/developer-survey/)发现，AsyncAPI 生产使用率从 2019 年的 5%增至 2020 年的 19%,增长了两倍。按照 Belcher 的说法，测试这样的异步服务需要一个持续测试的基础设施来预测这些新出现的场景。

## API 测试的四个关键领域

那么 API 测试应该关注什么呢？Belcher 强调了在整个 API 测试过程中需要仔细检查的四个方面:

*   **功能**:这是核心功能。API 做了它承诺的事情了吗？它返回正确的数据吗？
*   正常运行时间:API 的可用性如何？所有端点在生产中都可用吗？
*   **速度**:这确保了云依赖满足 SLA。什么是延迟？API 性能是否会随着时间的推移而发生漂移？尽管像 [Api.expert](https://www.api.expert/industry/corpinfra) 这样的 API 监视器有助于汇总行业绩效，但它们可能并不总是反映您特定的客户层面的现实。贝尔彻建议不要相信所谓的表现，而是记录你自己的表现。
*   **端到端**:贝尔彻强调了 API 在面向客户的存在中所扮演的角色。端到端的工作流应该包括 API 端点、它们之间的交互方式以及最终的可视化表示。“就像我们对 ui 进行端到端测试一样，我们也应该对 API 进行端到端测试，”他说。

API 测试并不总是与用户体验的其他部分相结合，但 Belcher 认为，未来，端到端测试将是确保所有工作流协调运行的关键。例如，如果用户配置文件是在浏览器中创建的，团队也应该验证用户配置文件是在 API 级别创建的。

## 低代码 API 测试和左移

API 有利于避免重复发明轮子。然而，100%的正常运行时间是不可能的。应用程序不可避免地会遇到 API 问题，包括中断、技术故障和功能错误。开发人员也经常依赖可能没有正式记录的生产行为，这种效应被称为 [Hyrum 定律](https://www.hyrumslaw.com/)。随着时间的推移，这可能会导致 API 版本的不稳定集成。

因此，出于这些以及更多的原因，采用持续的 API 测试是一个好的实践。随着对[站点可靠性工程](https://devops.com/how-the-sre-role-is-evolving/)兴趣的高涨，尽早发现 API 错误将成为缩短平均恢复时间的一个重要方面(MTTR)。测试第三方 API 也可能暴露生产延迟，以通知[云投资](https://devops.com/how-to-respond-to-rising-cloud-costs/)。

“随着变革步伐的加快，我们如何为客户提供高质量的产品？”贝尔彻问道。API 测试是解决这种快速变化的一个答案，并且对于软件交付生命周期越来越重要。对于无头前端体验来说尤其如此，API 驱动的后端对于 QA 测试人员来说是不透明的。

API 测试的低代码能力可以帮助打破开发过程中固有的孤岛，让更多的人参与到测试集成中来。Belcher 还强调了提高 API 测试对开发人员和非开发人员的可用性的重要性。“我们需要整合开发人员已经在使用的验证工具，”他补充道。