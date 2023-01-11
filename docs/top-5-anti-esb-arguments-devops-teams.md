# DevOps 团队的五大反 ESB 论点。

> 原文：<https://devops.com/top-5-anti-esb-arguments-devops-teams/>

Unix and Mac. Developers are always in combat. My last verbal combat was a “discussions” around ESB and Microservices. They are fun because both supporters tend to have very strong opinions about what they think is best and both want to fight each other. I recently got involved in one of those discussion about ESB vs. Microservices and the ESB guy throw lots of arguments at me. “ESB is magic” got almost burnt into my mind until I started to investigate a bit: “How to fight ESB discussions in combat?”. Here are my top 5 findings that may help in your next verbal ESB combat situation.

## ESB 紧密耦合服务。

[![JBoss in 5 minutes (from Installation to Deploy) - Quickstart - by Sven Malvik ](img/b99102fa005bfe61ff2d9b551376b3d6.png)](https://www.youtube.com/watch?v=jP0g6vLeMDQ)

[JBoss in 5 minutes (from Installation to Deploy) – Quickstart – by Sven Malvik](https://www.youtube.com/watch?v=jP0g6vLeMDQ)

ESB 与微服务，这就像是 Windows 之间的圣战，有时很难对一个通过 ESB 与其他服务紧密耦合的服务进行更改，这令人沮丧。每当我们做出改变，我们都有需要调查的副作用。这些副作用有时会出现在我们无法掌控的领域。维基百科上指出，这是 ESB 的主要缺点之一:“-紧密耦合整个系统，这导致更有影响力的部署……”。ESB 具有更改请求和响应的能力，例如，如果我们希望响应采用某种格式，ESB 往往是可以实现这一点的解决方案。ESB 还可以将两个或多个服务聚合成一个，我们称之为编排。它可以在不改变连接服务的情况下满足特殊需求。ESB 可以做很多事情。服务所依赖的 ESB 中发生了很多神奇的事情。这意味着在一个改变之后仅仅测试一个服务是不够的。我们被迫总是通过 ESB 测试整个请求/响应链，以确保 ESB 内部的所有依赖项和逻辑仍然按预期工作。因为我们只拥有自己的服务，所以我们依赖他人。紧密耦合的服务是痛苦的，因为更改和部署比它们独立服务要危险得多。

## 管理 SOAP 非常耗时。

SOAP 使用 WSDL，它是一种重量级的冗长的 XML。它通过强类型消息来完成工作，这使得 SOAP 感觉是一种脆弱的格式。每当您更改一个类型时，所有的客户端都将中断，并且必须更改为新的规范。即使很小的名称空间更改也会中断两个服务之间的整个通信。这也使得版本管理变得极其困难，而版本管理是服务发展的核心部分。当你需要花时间去想该做什么的时候，管理 SOAP 是很困难的。因此，一般的经验法则是:“除非你有明确的理由使用 SOAP，否则就使用 REST”。

## ESB 专家是瓶颈。

> 阅读:[http://devops.town/better-off-with-microservices-or-esbs/](http://devops.town/better-off-with-microservices-or-esbs/)

我们所依赖的忙碌的人永远是我们的瓶颈。而 ESB 专家大部分时间都很忙。他们很忙，因为 ESB 是一个非常复杂的组件，它需要非常优秀的人的知识。它做许多不同的事情，如路由、消息传递、监控、安全、协调和许多其他事情。作为服务开发人员，我们不时需要这些人的帮助。当我们试图将服务连接到 ESB 时，我们需要帮助。我们在管理 WSDL 档案时需要帮助。当我们想要跟踪从一个服务到另一个服务的请求时，我们需要帮助。很明显，具有许多连接服务的 ESB 在每个组织中都是一个挑战。这取决于我们是否想要这种挑战，或者我们是否想要摆脱这种挑战，而是选择拥有我们服务的整个价值链。

## ESB 中的服务编排是昂贵的。

服务编排要么改变业务逻辑，要么让用户通过流程。它是作为一个单一的聚合服务公开的多个服务的协调。服务编排是属于服务而不是 ESB 的代码。当业务需要改变或新功能时会发生什么？这个特性的某些部分已经完成，并且在连接到 ESB 的服务之一中可用。企业最终会询问实现服务的团队是否可以添加这个特性。如果团队因为没有时间而拒绝会发生什么？或者他们说不，因为他们不能实现这个特性，因为它不适合服务？业务可能会与 ESB 专家交谈，询问他们是否可以“仅仅”向服务响应添加一些逻辑。这个新的 ESB 逻辑现在依赖于服务，服务中的任何变化都将影响 ESB，并最终影响使用聚合响应的客户端。改变将变得耗时且昂贵，因为依赖总是令人沮丧且昂贵的。

## 供应商利用 ESB

ESB 许可证可能非常昂贵。构建像 ESB 这样的复杂软件组件是一种业务模型。安迪·海吉说得很好。"[为了销售软件许可证，关键是要有大而贵的东西，而且最重要的是一旦实施，对客户来说是至关重要的。没有比 ESB 更好的例子了。](https://blog.hedges.net/2014/03/31/soa-vs-microservices/)”。Oracle 服务总线可能是一个很好的例子。许可证每年要花费数千美元。你得到的是一个复杂的产品和一个巨大的支持。事情是这样的，一些产品非常复杂，以至于公司雇佣专家来管理它们。这些专家通常不利用供应商的支持。我个人喜欢这种商业模式，因为它既有趣又悲伤，是一种奇妙的对比。

## 结论

你可以用来反驳 ESB 支持者的 5 个论点。将它们与使用微服务的 5 个积极论点结合起来，你有望赢得每一场 ESB 与微服务的讨论。即使您作为一名 DevOps 顾问对 ESB 不感兴趣，了解它们也是有好处的，因为讨论即将到来，您最好做好准备。[阅读斯文·马尔维克关于 devops.com 的所有文章](https://devops.com/author/svenmalvik/)

[/Sven mal vik–来自奥斯陆/挪威的 DevOps 顾问](http://sven.malvik.de)