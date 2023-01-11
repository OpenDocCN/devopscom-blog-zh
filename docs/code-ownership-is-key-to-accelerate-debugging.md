# 代码所有权是加速调试的关键

> 原文：<https://devops.com/code-ownership-is-key-to-accelerate-debugging/>

应用稳定性是每个应用体验的基础部分。广义而言，应用程序稳定性是对无崩溃应用程序会话总数或每日活跃用户中未出现错误的用户百分比的衡量。终端用户对崩溃或失败的应用程序没有耐心。每个应用程序，不管是面向 B2B 还是面向 B2C 的，都有一定程度的不稳定性，偶尔会失败。理想情况下，组织应该[以接近 99.999%的应用稳定性](https://www.bugsnag.com/research/app-stability-index-report)分数为目标。为了达到这种性能质量，软件工程师必须快速有效地修复经常导致应用程序崩溃的编码错误。

但是使用传统的方法来调试 T1 是一个很大的挑战。大多数主要的应用程序都有各种各样的工程师，包括完全独立的工程团队，他们都在一个代码库中工作。每个团队通常使用他们自己的[特有的问题跟踪器](https://www.bugsnag.com/blog/bugsnag-issue-tracker-streamline-debugging)来监控错误，比如吉拉或阿萨纳。此外，团队通常在协作平台中使用自己的渠道进行内部沟通，如 Slack 或微软团队。这导致了不同工程团队之间的孤岛，限制了每个团队之间的沟通和可见性。

当一个错误发生时，所有的工程团队都会通过他们自己的问题追踪器得到警告。从那里，他们找出代码中的错误发生在哪里，以及谁具体负责修复它。这需要每个团队在试图定位错误时手动检查代码，这浪费了宝贵的时间，因为工程师们重复彼此的工作。因为团队使用不同的沟通渠道，在这个过程中，不同的工程团队之间很少或没有协作或协调。总的来说，这种调试方法既麻烦又低效，会减慢修复应用程序的过程，最终损害最终用户体验。

考虑一个真实世界的例子。假设您的团队是十几个工程团队中的一个，所有人一起开发一个创建手机游戏的应用程序。也许你的团队负责维护应用内购买功能集，而另一个团队负责帐户设置流程，还有一个团队负责角色定制功能。如果一个 bug 突然让相当一部分用户的应用崩溃(导致应用稳定性分数明显下降)，每个团队都会通过他们的问题跟踪器收到一个错误警报，通知他们一个编码问题导致了应用失败。没有人会知道他们团队的代码是否有责任。因此，每个团队都不得不经历上述艰苦的过程。如果错误出现在角色定制代码中，那么负责应用内购买和帐户设置的团队就浪费了宝贵的时间和资源来搜索错误。

唯一应该被通知 bug 的团队是负责产生 bug 的那部分代码的团队。新兴的代码所有权概念使这成为可能，提供了一种更快更容易的调试方法。使用这种方法，组织创建代码所有者文件，以确定哪些工程师或团队负责代码、特性标志或实验的每个部分。如果代码中的 X 部分失败了，那么 X 团队将负责解决这个问题。在上面的例子中，只有负责与角色定制相关的代码的团队需要找到并修复 bug。

这使得响应应用程序问题和分配正确的资源来补救这些问题变得更加容易。对于最终用户来说，代码所有权意味着故障应用将被更快地修复，从而改善客户体验并提升业务指标。从内部的角度来看，工程团队变得更加节省成本和时间，让开发人员能够从事他们真正喜欢的新项目。

代码所有权文化也有助于工程团队采用其他调试的最佳实践。一个主要的例子是错误优先级。并非所有的错误都会导致应用程序严重不稳定，需要立即修复。当一个团队可以忽略与他们的代码无关的错误时，他们就有更多的时间来充分磨练和评估他们所负责的错误。使用这种集中的方法，他们可以建立度量标准，确定他们是需要立即修复一个 bug，还是可以等待。

简而言之，代码所有权消除了与调试过程相关的混乱和猜测，允许工程团队轻松地识别、拥有、优先化和补救错误。拥抱代码所有权对于公司提高应用程序稳定性至关重要，这是衡量应用程序健康状况的最基本的标准。这与业务成果直接相关，因为应用稳定性与客户维系、客户增长、销售和收入密切相关。通过加速调试工作，代码所有权对稳定性有显著的积极影响，提高了这些指标。