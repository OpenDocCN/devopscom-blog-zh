# 适合这项工作的工具:容器版

> 原文：<https://devops.com/the-right-tool-for-the-job-container-edition/>

我已经反复写过关于“工作的合适工具”的文章。因为(再次)我们在其中是绝对主义者。我的父亲是一个古董修复者，涉足翻转房屋，并强烈主张“合适的工作工具”。当我离开军队并加入它的时候，对我来说有点震惊的是“合适的工作工具”被认为是视情况而定的。

当时，有大量热爱 Visual Basic 的微软狂热者，也有大量偏爱 C 或 Java 的非狂热者。这就是我的第一篇“正确的工具”文章的由来。VB 在 UI 和记录处理方面非常强大，而 to-the-metal 是 C 的强项，Java 介于两者之间——两者都不完美。所以我的文章说。前端数据库？用 VB。写驱动和底层流程？使用 C/C++。需要简单的网页生成吗？用 Java。

多年以后，是时候发表一篇对我来说同样显而易见的文章了，但是是在一个不同的 It 领域。我们都听说过三种架构:数据中心、云和混合/多云。我们也听说了在这个快速变化的开发运维、敏捷和容器的世界中，不同的组织如何使用不同的部署方法。到目前为止一切都好。正如今天可用的各种编程语言在许多方面都是额外的好处一样，多种部署和操作选项也是如此。

当人们在谈话中提到“我们是 X 店”时，事情就变得棘手了。或者尝试用这些方法中的一种来做世界上所有的事情。对我们许多人来说，集装箱基础设施是完美的。使用类似于 [Kubernetes](https://containerjournal.com/?s=Kubernetes) 的 orchestrator，构建系统和安全实践，然后不必太在意它运行的 Kubernetes 实例是在本地、托管还是云上。当然你得关心*一些*。网络必须连接等等。但是大部分工作已经完成。

还有一些人的用例不符合这个模型，并且还没有承认这个事实。这个博客是给你的。我们都听说过有些公司的集装箱的预期寿命是以秒计算的。除此之外，有人告诉我有一家公司正在使用[容器](https://devops.com/?s=containers)作为消息队列。说实话。使用启动命令创建一个容器，并将其放入队列。当它被拉出队列时，它执行那个命令，然后离开。我们将这一人群称为“过度用户”。

最后，有些人不能或不愿意将他们的系统移动到任何地方。这有多种原因，但这些公司知道他们的应用程序将在可预见的未来继续在数据中心运行。我们称这个群体为“无需求者”。

对于 100 多名用户来说，这就是无服务器的真正用途.在无服务器环境中创建一个调用 API 的队列(小得多),然后就完成了。更少的配置问题，更少的维护，更少的一切，除了代码。添加触发器，删除整个操作系统/网络/配置生成和维护。对这个建议最可能的抵制是“但是我们有投资……”是的。对于大多数组织来说，这是对不必要的技术债务的投资。撤资。保留好的部分——一个容器架构意味着可以在短时间内存在的许多容器中穿梭，这是一个好的架构。

不需要，在你把所有东西都移植到容器之前——我通常完全支持——你应该考虑你是否需要；想一想这样做是否有好处，以及这样做的投资回报率是多少。说实话。对于需要高度便携解决方案的开发密集型商店或组织来说，容器的投资回报是快速而明显的。对于那些应用程序没有太大变化并且不太可能迁移到任何地方的组织来说，投资回报要模糊得多。“但这给了我们选择！”是对“我们现在不需要这个”最可能的否定回答但这就是问题所在——你现在有这些选择。它给你的是成本的转移，从未来可能需要它的地方转移到今天已经紧张的预算。如果有可证实的需求——通常是可移植性，但任何可证实的需求——那么就采取行动。在此之前，花时间和金钱让这些应用程序摇滚起来。

你做到了。灯亮着，应用程序有用。使用对您试图实现的目标有意义的架构。正如我父亲常说的，这是适合工作的工具(当我认为凿子是螺丝刀时，他说得更有力了，但那是另一回事)。继续摇摆，专注于需求。