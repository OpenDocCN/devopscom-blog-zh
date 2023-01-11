# 成功的失败

> 原文：<https://devops.com/successful-failure/>

在软件开发中，成功就是失败。

这听起来好像我们将“快速失败，艰难失败”的理念带得有点远了，但是您更愿意发生哪种情况呢？是可以识别、重复和分析的快速、明确的失败，还是让您的应用程序和数据处于损坏和不稳定状态的一系列半失败和部分恢复？任何花了很多时间测试或调试软件的人都应该知道答案:被接近恢复掩盖的错误几乎和间歇性错误一样难以跟踪——而且通常这两者之间没有真正的区别。被部分恢复掩盖的缓慢故障表现为时断时续的错误。

是的，我们正在谈论向前失败——但是在你说你以前已经听说过这一切之前，让我们看看这意味着什么。在软件开发中(或者就此而言，在其他任何事情上)，向前失败是以一种允许你识别并克服潜在问题的方式失败，这样你就可以前进，越过给你带来麻烦的地方。

一旦你认识到它们的本质，那些太常见的向前失败的替代方案通常是相当没有吸引力的:未能(甚至拒绝)认识到问题，在不理解它的情况下修补它，尝试立即修复和变通办法，从长远来看使事情变得更糟，与几个步骤的后续症状无休止地斗争，旨在使问题看起来正在处理的表面错误陷阱，等等。

他们都有一个共同点，那就是他们不会积极地解决问题，也不会系统地解决问题；事实上，他们认为这是一场潜在的无休止的斗争——这种方法对于一个开发项目来说是致命的。太多时候，除了向前失败，真正的选择是到处失败，而且永无止境。

因此，除了其他方面之外，前向故障意味着让用户清楚地知道发生了错误，并标识错误位置的错误，包括所有潜在感兴趣的项目的日志，以及诸如正常故障或自动错误恢复之类的非常有限的用途。如果外部资源或文件不可用，或者如果程序遇到损坏的数据，正常恢复并继续运行是一回事，但是当程序内部出现故障时进入正常恢复模式则完全是另一回事(而且不是一件好事)。当这种情况发生时，你只是在掩盖一个可能会一次又一次出现的错误。

但是如此明显的失败有什么坏处呢？这难道不会损害客户的商誉吗？简短的回答是肯定的，否定的，也许——是的，如果你习惯于把你的整个客户群作为 beta 测试者，这可能会造成损害(虽然我们可能都可以说出一些非常大和著名的公司似乎就是这样做的)，不，这不会比发布性能缓慢下降的软件所失去的信誉更糟糕，也许有比让你的所有客户处理你最引人注目的失败更好的方法。

事实证明，有更好的方法来实现故障前向开发；这些方法中最好的(也是最广泛使用的)一个是金丝雀释放策略(以煤矿工人的金丝雀命名，如果空气开始变坏，它的工作就是死去)。

有了 canary 版本，您的应用程序的当前版本仍然保留在您的主服务器系统上，并且您的大多数客户继续使用它。您在一组独立的服务器上安装新版本，并测试它的基本稳定性、功能和明显的错误。此时，您将一小组用户路由到新版本。这允许您在真实环境下测试部署，知道如果它确实以一种非常明显和不优雅的方式失败了，那么失败只会对那些用户可见。当您对初始测试组的新版本的性能感到满意时，您可以将它推广到更大的用户子集，并解决在更重的负载下变得明显的任何剩余的 bug。之后，您可以将它部署到您的普通用户群，替换旧版本。

这意味着，即使新版本在高负载下运行一段时间后会出现真正灾难性的、引人注目的故障，也只有小的初始测试组(或更大的二级测试组)可能会遇到这种情况，回滚将主要包括将那些用户路由回主要的、稳定的版本。

当然，在实践中，事情并不那么简单。隔离一组服务器并将一小组用户切换到这些服务器的过程需要您操作负载平衡系统。它需要过滤出一组特定的测试用户，并将他们路由到指定的测试服务器，而不是严格根据标准的负载平衡标准将用户路由到服务器，同时继续对其余的用户和服务器执行其通常的负载平衡功能——在不降低性能的情况下完成所有这些工作。除了实际的软件测试部署之外，最初设置这个系统可能需要它自己的一个重要的设计-实现-测试周期。

您还需要考虑选择测试组的过程。您的第一个小组应该为您提供现实的负载和使用条件，因此，虽然在某些情况下它可能是内部的，但通常最好通过某种方法(通常是随机或半随机的)从您的用户群中选择人员，这种方法不太可能使结果产生偏差。在实践中，这需要足够大且活跃的用户群，即使这样，canary 部署也不一定适合所有应用程序或用户(例如，财产损失/生命损失的关键任务应用程序)。

然而，考虑到这些限制，故障前向开发和 canary 发布的组合可以作为一个非常强大的策略，用于实现连续部署和维护高软件质量标准，而不会使您的用户面临重大风险或不便。