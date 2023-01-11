# 从质量保证到持续测试

> 原文：<https://devops.com/qa-continuous-testing/>

我之前的博客“[DevOps–这都是关于持续测试的](%20https://devops.com/blogs/devops-continuous-testing/)”认为 QA 测试人员不需要害怕 DevOps，因为持续测试 QA 是根据最佳实践实现的 devo PS 基础设施的核心部分。然而，这并不是说持续测试与传统的 QA 测试完全相同，或者 QA 测试工程师可以在 DevOps 和持续测试的新世界中安于现状。

传统的 QA 测试是一个连续的过程，它构成了开发阶段之后的一个独特的阶段，并由“独立于”开发团队的 SQA 测试团队进行。Glenford Myers 在他分别于 1976 年和 1979 年出版的开创性著作《软件可靠性——原则和实践》和《软件测试的艺术》中清楚地描述了这一思想。根据 Myers 的“测试的第四公理”，“测试你自己的程序是不可能的”。迈尔斯觉得程序员不应该做任何测试，甚至是单元测试。虽然这个公理在单元测试中的应用并没有被软件行业的大多数从业者所遵循，但是独立的软件功能和系统级测试的想法已经被广泛接受了很多年。潜在的基本原理是，对于同一个人(开发人员)来说，客观地测试他/她自己的代码是“不可能的”,因为固有的偏见想要代码工作，而一个好的 QA 测试人员必须有相反的态度想要打破它以发现代码中的 bug。如果你遵循这种逻辑，只有“不寻常的”开发人员能够成功地扮演这两个角色，因此基于这种罕见的个人品质建立一个团队基本上是不现实的。

尽管“独立 QA 测试”概念的逻辑显而易见，许多没有独立 QA 测试团队的非常复杂的软件项目产生了极高质量的产品。有许多高质量的开源软件产品在每个发布版本背后都没有独立的测试组织。与此同时，有无数的例子表明，拥有大量独立测试资源的软件项目导致了产品的悲惨失败。怎么会这样呢？也许重要的不是“谁”在做测试，而是测试本身的质量和频率。

持续测试，其基本概念是“早期失败，经常失败”，是新的 QA 测试方法的选择。当然，测试仍然是必不可少的，在测试设计的最佳实践中最熟练的 QA 测试专家是有价值的，因为他们将生产出质量最好的产品。多年的软件工程经验表明，如果有人教，开发人员可以学习这些技能，甚至“普通”开发人员也可以做好测试工作。取代“开发之后”的 QA 测试，随着软件的开发，一个构建一个构建，一个特性一个特性地进行测试。显然，早一点发现 bug 比晚一点好。那么，为什么我们不总是将持续测试作为开发过程的一部分呢？

几个行业的发展融合在一起，使得连续测试成为软件工程质量保证的成功方法。众多的“现代”测试方法，例如敏捷测试、测试驱动开发、行为测试方法、基于模型的测试和自动化回归测试等等，描述了如何在不需要独立的 QA 测试团队的情况下完成高质量的软件。敏捷开发流程和 DevOps 基础设施的出现加快了自动化和流程编排工具和方法的开发和采用，其中开发构建测试周期被加速到几分钟或几小时，而不是几天或几周。除非测试本身和测试环境得到编排工具的支持，并且可靠的回归测试随着产品的开发而系统地自动化，否则没有其他方法可以在每个构建测试周期中完成合理数量的测试。

与此同时，虚拟化技术使得各种各样的产品测试拓扑能够以与快速构建测试周期相兼容的速度按需建立，而不需要昂贵的专用设备配置。正是这种改进的测试方法、敏捷的流程、自动化和流程编排工具提供的持续集成速度，以及虚拟化提供的低成本测试动态可配置基础设施的结合，造就了 DevOps。

持续测试是“新的质量保证”

在思必驰，我们认为测试在 DevOps 有着光明的未来。你可以在[spirent.com/solutions/devops](http://www.spirent.com/solutions/devops)了解更多我们的观点