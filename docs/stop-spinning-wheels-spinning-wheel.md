# 应用程序开发:停止纺车上的纺车

> 原文：<https://devops.com/stop-spinning-wheels-spinning-wheel/>

说到网站和应用，速度很重要；今天的消费者想要昨天的一切。最近的研究表明，没有比制作一个性能低下的应用程序更能失去消费者信任的方法了。最近，亚马逊[报告](https://mashable.com/2011/04/05/site-speed/)称，每*十分之一秒*的延迟，销售额就会下降百分之一。此外，几乎一半(48%)的消费者[表示](http://www.cio.com/article/2903142/mobile-apps/mobile-app-users-prioritize-performance-over-price.html)在应用程序运行缓慢后，他们立即卸载了该应用程序。这是一笔巨大的成本，直接转化为利润。

今天的网站和应用程序在用户体验方面竞争非常激烈(UX)。消费者受过教育——如果数字体验不吸引人、不有效，他们就会转向能提供这种体验的数字渠道。

问题在于 UX 设计师和业务线团队之间的协作。UX 的设计师们在他们的网站和应用程序中加载酷酷的内容和热门的第三方 JavaScript，以获得强烈的视觉吸引力。接下来，查看竞争对手数字财产的团队要求添加更多内容，希望应用程序会更加有用。不幸的是，采用这种策略，最终的结果是一种难以置信的体验，可能介于“嗯”和“糟糕”之间。消费者离开是因为他们最讨厌的东西比无聊的东西还糟糕？缓慢的东西。

所以，做一名设计师很难。与普遍的看法相反，事实是，在全球范围内，平均网页加载速度实际上正在变得越来越慢。随着越来越多的用户涌向社交媒体和电子商务网站来获取图片、视频和互动插件，网速一直在下降。考虑到美国现在有 5000 万人在手机上观看流媒体视频，这个问题就变得很明显了。高速互联网已经不足以及时向消费者提供内容。事实上，你必须假设高速是不相关的，因为现在很多互动都是“空中”移动的。

现在的问题是，在一个性能缓慢下降的世界里，设计师、开发人员和组织可以做些什么来最大限度地提高体验和保持速度？

**测试是关键任务**

在一个网站或应用程序发布之前，需要对其进行测试，然后以一种可以监控的方式进行部署，以检查其性能问题或任何可能让用户再也不会查看它的错误，这并不是什么火箭科学。过去那种“它会变得更好”的模式已经过时了。你必须第一次就做对。

然而，测试和监控一次是不够的；因为第三次聚会内容引入了太多的变量——从付费广告时段到图片，到社交账户登录，再到各种营销标签。这些来源中的任何一方出现故障都会损害性能。此外，这些第三方部分本身就是基础设施长链的一部分，有许多暴露的弱点。如果你的第三方社交媒体登录 JavaScript 对象无法与它的房子通信，或者它的房子用来与脸书通信的管道出现故障，消费者只知道他们不会回来了。

尽管这个想法看起来很好，增加了一个营销或广告功能来增加应用程序产生的收入，但它需要首先进行测试和监控，以确保它不会产生相反的效果。如果没有充分评估与增加这些服务相关的风险，就很难评估它会帮助还是伤害业务。

最后，确保在不同的流量级别进行负载测试。将测试重点放在最好的场景可能很容易，但要知道，一旦发布，应用程序需要在一系列不同的网络条件下运行。

保持简单，但不要愚蠢

设计总是在为消费者提供更多功能的愿望和更具交互性和友好性的用户界面之间寻求平衡。对于许多组织来说，这意味着提出一些时髦的东西，然后让开发人员和运营人员理解它以提高性能。因此——通常是为了避免潜在的争论点——偏向于安全和以最小的成本确保性能。

最终，最好的体验将意味着更多的销售、更多的浏览、更多的消费者和更好的投资回报。它实际上植根于经济事实——这种体验能够并将推动更多收入，但只有通过投资支持才能实现。

那么，如何在不影响性能的情况下保持和扩展体验呢？关键是通过花时间进行研究，评估不同的选项并不断测试它们，以了解什么可以提供体验和性能的正确平衡，从而实现可预测性。仅仅因为你一直在使用来自一个众所周知的来源的相同的社交媒体 JavaScript 对象，并不意味着你不应该总是将它与其他替代方案进行比较。鉴于至少 30%的网页来自第三方，这意味着有很多持续的监测和研究要做。

## **科学方法**

最终，我们在这里所做的是采取艺术家最大化创造力的心态，并应用科学方法。在向 DevOps 团队展示之前，研究所有这些第三方选项并检查它们的性能，这为证明以经济实惠的方式提供出色的性能和体验提供了有力的证据。然后，与 DevOps 合作持续监控第三方内容，确保在第一次出现性能下降迹象时，备份提供商就在一旁等待部署。

***关于作者/亚当·蒂尔***

[![adam-thier](img/77714f04f58ef3bfc163b04000f3caf4.png)](https://devops.com/wp-content/uploads/2015/08/adam-thier.jpg)Adam Thier is the Executive Vice President of Engineering at Keynote Systems. He brings Keynote over 25 years of software development and product experience ranging from a number of successful startups through engineering leadership roles at industry leaders such as SAP. In particular, he is an expert in analytic applications, predictive analytics, massively parallel in-memory databases, and columnar store processing.Prior to Keynote, Thier was the Senior Vice President of Frontline applications at SAP, and prior to that ran development for Hyperion’s applications portfolio prior to its acquisition by Oracle. Thier is an avid proponent and practitioner of design thinking and credits most of the success of the products he has been responsible for to deep engagement with customers and continuous co-innovation.  Thier has a BA from Marist College.