# NodeSource 获得 Node.js 问题的来源

> 原文：<https://devops.com/nodesource-gets-source-node-js-issue/>

世界上并不缺少 Node.js 的变体，但是 NodeSource 正在做一个与 DevOps 相关的案例，说明为什么 IT 组织应该标准化其运行时实现。

NodeSource 发布了 N|Solid 的 2.3 版本[，它增加了对事件循环延迟通知的支持，该通知基于 JavaScript 的 Node.js 变体，可以精确定位应用程序中需要解决的问题发生在哪里。](http://www.businesswire.com/news/home/20170727005279/en/NSolid-2.3-Improves-Performance-Issues-Resolution-Times)

NodeSource 的产品经理 Pravin Halady 说，N|Solid 独特地提供了 Node.js 的运行时实现，提供了这种能力。Halady 说，结合基于 N|Solid 的应用程序监控工具、额外的可视化工具和可配置的基于 webhooks 的集成来创建可以通过 Slack 等协作平台共享的警报，N|Solid 是唯一一个专门为企业 IT 环境优化的 Node.js 运行时。

他指出，采用 Node.js 的组织面临的一个更棘手的问题是，任何阻塞事件循环的长期同步活动都会阻止其他传入请求到达服务器。过不了多久，应用程序就会挂起或崩溃。Halady 说，通过实时洞察事件循环延迟何时发生，IT 组织不必浪费时间试图重现问题。结果是更快地解决 Node.js 应用程序问题。

一旦开发人员采用 Node.js，DevOps 团队就会发现他们处理这类问题的频率要高得多。随着最广泛使用的 JavaScript 变体的采用增加，IT 组织管理的应用程序比以往任何时候都多。事实上，Node.js 基金会最近发布的一项调查发现，四分之三的受访者计划在未来 12 个月内增加 Node.js 的使用量。额外使用的主要原因是提高了开发人员的工作效率(68%)；提高开发人员的满意度(65%)；降低开发成本(58%)；并提高了应用程序性能(50%)。在企业 IT 组织中工作的近一半受访者(47%)表示，他们使用 Node.js 已经超过三年。相比之下，超过一半的开发人员(58 %)报告拥有超过 10 年的 Node.js 工作经验。

IT 组织通常对 Node.js 应用程序内部发生的事情知之甚少，这使得很难应用 DevOps 流程。事实上，目前大多数 DevOps 流程都是围绕用更成熟的语言(如 Java)编写的应用程序进行的。使用 JavaScript 的开发人员往往不太了解程序员在集成的 DevOps 流程环境中理想的角色。

在缺少这些流程的情况下，拥有实时调试应用程序所需的工具对于需要将特定问题的根本原因告知开发人员的 IT 运营团队来说变得更加重要。否则，开发人员会一个接一个地运行测试，希望重现问题。不幸的是，在大多数组织中实现这一目标的可能性通常相对较低。仅仅因为这个问题，实时发出的事件循环延迟通知很可能在几个小时内收回成本。

— [迈克·维扎德](https://devops.com/author/mike-vizard/)