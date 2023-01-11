# 新的复杂性

> 原文：<https://devops.com/the-newish-complexity/>

由 Agile 和 DevOps 领导的 API 经济和[微服务架构](https://devops.com/?s=microservices)引入了大量隐藏的复杂性。我称之为隐藏的复杂性，因为我们倾向于关注我们面前的问题，解决它们，然后关注我们面前的新问题。这使得技术债务在我们身后堆积如山，就像从扫雪机刀片末端脱落的碎片(或者为我们的南方朋友挤压出压路机尾部的沥青)。

当我调查你们大多数人是如何处理可伸缩性的时候，我就在思考这个问题。可伸缩性的复杂程度令人惊讶。过去，我们预先投资，为扩展到我们需要的级别做好准备。如今，我们允许费用随着用户的增长而增长。如果用户与收入挂钩，这是一个很好的模式。如果用户与收入之间存在任何可替代性(几乎总是存在)，这将是一场潜在的灾难。“我们的流量飙升了 200%，但收入只增长了 20%，”这几乎是企业领导最不想听到的话。因为在“随增长付费”的世界里，200%的用户高峰意味着管理费用的大幅增长。当然，多少开销变化很大，所以我只说“有保证的和重要的”，就这样吧。

这是一个众所周知的复杂性，但我与之交谈过的你们中的一些人几乎没有采取任何措施来防范它。那……很有趣。还有多少隐藏的地雷被我们忽视了？

你能做什么？这很大程度上取决于你的业务。有了内部系统，你在使用上很有发言权。外部系统是潜在的问题所在。你可以付钱给你的提供商来阻止 [DDoS](https://securityboulevard.com/?s=DDoS) ，所以如果发生这种情况，至少你不用为带宽付费——我采访过的大多数人确实有某种形式的 DDoS 保护，在流量变成收费攻击之前阻止流量。但对于实际的增长，你能做的最好的事情就是和商业领袖接触，并确定是什么影响了用户和收入之间的相关性。是什么让那些增加你流量的人在增加你流量的同时实际上花钱了呢？你能做些什么来说服更多的人花钱？你*没有*提供哪些服务可能对那些客户有用，并且不会显著增加开销。基本上，这是转换问题的现代等价物。他们在你的网站上，你如何将他们转化为你网站的付费用户。

我们真的没有比这更详细的了——你知道你的业务，例如，媒体网站和零售网站是不同的模式——所以你必须超越这一点。但是要有一个计划，尽你所能确保支出增加时，收入也随之增加。

继续摇摆。我们已经超出了历史 IT 领域——因为你们做得太好了，我们有新的事情要担心。给这些客户提供 rockstar 应用程序，并想办法让他们成为付费客户。发展与商界领袖的关系；你们确实需要对方。