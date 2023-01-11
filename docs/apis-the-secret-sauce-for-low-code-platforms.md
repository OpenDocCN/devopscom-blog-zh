# API:低代码平台的秘方？

> 原文：<https://devops.com/apis-the-secret-sauce-for-low-code-platforms/>

随着公司越来越缺乏人才，应用编程接口正在推动低代码运动，以帮助他们保持竞争力

低代码平台有可能改变软件的构建和交付方式。通过关注可视化流程和拖放式 ui，低代码平台极大地降低了软件开发的障碍。

然而，任何涉足无代码领域的人都会告诉你，这个领域充满了不确定的承诺。你能用零代码扩展整个企业软件架构吗？*大概不是*。一个低代码平台能独自创建和公开引人注目的基础设施吗？*也许是*。

我最近会见了西门子公司 Mendix 的架构和治理经理 Jon Scolamiero，他将自己标榜为低代码的替代者，来探究低代码现象的根源。

请继续阅读，了解为什么低代码平台会成为下一个大事件。我们将讨论低代码的好处和注意事项，低代码在敏捷应用交付中的使用，以及 API 优先的重点如何让一些低代码提供者脱颖而出。

## 什么是低代码？

低代码平台使用拖放工具来帮助非开发人员组装软件解决方案。低代码用户不用编写每一行代码、与数据库集成和编程网络集成，而是用默认容器可视化地构造应用程序模型，这些容器启动他们需要的逻辑过程和数据存储能力。

通过这种方式，低级代码被戏剧性地从标准软件开发中抽象出来。市场上低代码平台的例子包括西门子的 [Mendix](https://www.mendix.com/) ，亚马逊的 [Honeycode](https://aws.amazon.com/blogs/aws/introducing-amazon-honeycode-build-web-mobile-apps-without-writing-code/) ，谷歌的 [AppSheet](https://www.appsheet.com/) ，微软的 [Power App](https://powerapps.microsoft.com/en-us/) 和 [OutSystems](https://www.outsystems.com/) 。在这些解决方案中，默认配置和定制能力各不相同。

## 低代码优势

随着对更多应用程序需求的增长，公司转向生产力解决方案，如低代码开发，以加快速度。理论上，低代码或“无代码”平台还有许多其他好处:

*   **欢迎“公民开发者”加入进来**:低代码平台为不太懂技术的人提供了前所未有的可用性。通过降低准入门槛，外行可以参与复杂的应用开发。
*   **打破孤岛，改善协作**:由于非技术角色会变得更加复杂，低代码可以让团队之间更好地协作。它为组织提供了一种通用语言。
*   **缩短价值实现时间**:一些低代码平台允许您即时构建、部署和运行，从而大幅减少开发时间。特别是如果与 CI/CD 功能集成，使用低代码平台意味着大大减少价值实现时间。
*   **解决人才缺口**:在一个工程需求高但开发人员少的世界里，低代码开发在有限的劳动力中刺激持续增长。
*   **与云无关**:低代码可以提供与云无关的功能，使公司能够在 SAP cloud、Azure 上运行应用程序，或者“移植”到其他云供应商。
*   **平台无关**:低代码平台还提供设备无关的功能，这意味着应用可以运行本地移动代码。低代码层也有助于迎合其他体验，如语音、聊天机器人或智能电视。

低代码还可以支持内部非商业解决方案的数字化转型计划。例如，制造商可以利用低代码能力快速构建互联数字解决方案，帮助工厂生产运营化。

## 低代码警告

尽管低代码意味着许多积极的结果，但 Scolamiero 说，在整个行业范围内，还存在一些问题:

*   安全性:用低代码实现良好的安全性是可能的，但实现起来很复杂。低代码平台必须在整个应用生态系统中小心处理访问管理和委托身份。
*   正常化期望:低代码不是魔法。这些平台有其局限性，需要时间来适应。Scolamiero 鼓励有一个强大的训练计划准备就绪，并提供“教每个人如何捕鱼。”
*   **咨询服务** : Scolamiero 提醒 IT 领导要小心一些贴着低代码或无代码标签的解决方案，但它们更像是咨询部门。他说，购买大批服务人员“不是一种尊重顾客的商业模式”。
*   **没有通用标准** : Scolamiero 指出，低代码行业尚未就大规模数据集成方法达成一致。

## 引擎盖下的 API:秘密酱

2002 年，亚马逊首席执行官杰夫·贝索斯发布了一项全公司范围的命令，非正式地被称为“API 宣言”在这篇文章中，他声明“所有的团队将从此通过服务接口公开他们的数据和功能。”

这种 API 优先的策略提高了内部效率和可重用性，并最终使亚马逊能够转售自己的基础设施，创造了一个全新的令人印象深刻的收入流。Lyft 是微服务驱动产品的另一个优秀例子。

许多开发人员现在完全理解了将所有东西包装在 web 服务中的强大功能。然而，根据他与客户的谈话，Scolamiero 估计六分之一的首席信息官仍然没有意识到这一点。

“如果是的话，我们现在会有 10 个亚马逊人，而不是一个，”他说。“认为数据有价值确实很容易，但现在重要的是基础架构。”

对 API 的额外强调符合当前事件驱动、基于消息的系统的趋势。他说，能够将 API 暴露于不同的云增加了 API 的弹性。

## 隐藏 API 和低代码

低代码和无代码解决方案承诺任何人都可以成为开发人员。虽然现实稍微复杂一点，但是有了合适的框架，也许团队可以更接近那个理想。

对包含低代码平台的系统使用 API 优先的方法，并提供通过 API 公开数据的能力，可以给低代码平台带来优势。

根据 Scolamiero 的说法，技术领导者仍然在“数字化传统的纸张流程”他们通常不会想到简化事件驱动的架构，或者基础设施本身如何具有外部价值。

不管怎样，如果它成功地执行了一个业务案例，那么它就工作了。也许商业领袖不一定要知道引擎盖下是什么。这就是低代码的意义所在，不是吗？