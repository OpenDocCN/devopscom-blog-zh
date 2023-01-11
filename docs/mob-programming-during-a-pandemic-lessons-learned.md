# 疫情期间的暴民规划:经验教训

> 原文：<https://devops.com/mob-programming-during-a-pandemic-lessons-learned/>

***尽管有局限性，乌合之众编程还是可以有效的，甚至在新冠肺炎**T3 期间也是如此*

新冠肺炎疫情让我们许多人考虑对我们个人和工作生活的长期影响。与新同事或客户握手？自助午餐？我最近想知道社交距离将如何影响 mob 编程，这是我们去年年底在 Bonitasoft 实现的一种开发实践。

什么是 mob 编程？根据[敏捷社区组织敏捷联盟](https://www.agilealliance.org/glossary/mob-programming/)的说法，这是一种软件开发方法，整个团队同时聚集在一个键盘和一个投影屏幕周围。这是结对编程思想的延伸，包括两个团队成员在同一空间合作完成一个开发任务。

在 2013 年 8 月《CodeBetter.com 邮报》的一篇文章中，瑞典应用技术学院质量&课程负责人 Marcus Hammarberg 将 mob 编程等同于驾驶。驱动程序使用键盘，编写代码并遵循编码标准。其他团队成员是导航员、顾问和研究人员，他们协助司机，专注于更高层次的任务，如确定团队是否在解决正确的问题。他们也加入进来接替司机的工作。

“我并不是说群居编程适合所有人，结对编程也是如此，”哈马尔贝格写道。“这可能也不适用于所有类型的任务……但我想说的是，让你的团队进入一个只有一台电脑和一个屏幕的房间，整个团队都在一起开发一个功能，没有比这更有效的方法来实现这个功能了。”

当然，在过去的几个月里发生了很多变化，包括人们对近距离接触的舒适度。在我对 mob 编程在当前情况下如何工作提出建议之前，让我先分享一下 Bonitasoft 最初为什么采用它，以及它给我的公司带来的好处。

## 拥抱暴民编程

大约一年前，我看到敏捷教练 Woody Zuill 在 MixIT 2019 上发表了题为“Mob 编程:整个团队的方法”的演讲。我被我认为有前途的开发方法所吸引。然而，我怀疑把五个人聚集在一个屏幕前的有效性和后勤工作。我还怀疑它与远程工作不兼容——这是今天形势的预兆？

在 sprints 中运行开发项目是一项低风险的投资，所以我向我的五人团队的其他成员介绍了 mob 编程，该团队负责开发用于交付应用程序的 Bonita 平台门户，由内向和外向的人组成。该团队采用了 mob 编程方法来设计和测试应用程序页面。这是一个中等复杂程度的项目，由 Gradle 构建，使用 UI Designer 网页开发工具，用 Cypress 测试。

在讨论了项目的目标和方法后，团队在开放的办公空间中使用笔记本电脑和标准尺寸的屏幕。优点:快速开发完成，更好的实现和良好的测试覆盖率。缺点:由于冗长的讨论和电话通知的干扰，沟通方式的差异和暂停的交叉话题，注意力下降。

我和我的团队成员喜欢 mob 编程的结果，但需要解决格式问题。在尝试 mob 编程的兴奋中，我们也跳过了敏捷的第一阶段:从一个强大的框架和基本规则开始。其中包括阐明飞行员、导航员和研究人员在团队中的角色。

在其他调整中，我们搬到了办公室里一个更安静的地方工作。我们把小屏幕换成了大屏幕，把笔记本电脑换成了台式机、键盘和鼠标。我们安排了更多的休息时间。我们遵守基本规则。我们每 15 分钟轮换一次角色，这意味着所有团队成员都更加专心和投入。意识到胆怯的团队成员可能不会发言，我们更加公平地分配了发言时间。我们在为 mob 编程方法选择项目时更有选择性(例如，错误修复最好通过结对编程来解决)。

## 我们如何从 Mob 编程中获益

这个过程在开始时需要一点调整，但这是非常值得的。我们已经从 mob 编程方法中认识到了很多好处。最大的好处之一是我们节省了开发项目的所有时间。Mob 编程消除了合并冲突，减少了在站立会议和拉式请求审查上花费的时间，并减少了外部干扰(人们不太愿意打断整个团队，而只是一个开发人员独立工作)。

这里还有一些 mob 编程的好处:

*   全球知识共享:mob 编程开发团队的所有成员都获得了相同水平的新开发知识。新的团队成员能够快速掌握遗留代码。
*   高质量的解决方案:来自 mob 编程工作的解决方案倾向于在最终产品中通过较少的错误得到更好的测试。因为代码是模块化的，所以如果需要的话很容易修改。
*   团队成长:Mob 编程教会了我们以最适合每个团队成员的方式进行交流。我们欣赏团队成员思想和个性的多样性，而不是将其视为劣势。

## 暴民编程能在疫情工作吗？

现在你知道我为什么推荐 mob 编程了，让我们看看在疫情期间是否有可能继续安全地使用这种方法。Bonitasoft 的开发人员都是远程工作，所以我基于经验。我们使用视频会议工具应用基本规则，并为每个人复制开发环境。通过视频会议交流是一种调整，但它很有效。每个团队都可以通过多次迭代来调整 mob 编程，使之最适合他们，无论他们是在同一个空间工作还是远程工作。

以下是一些 mob 编程技巧:

*   定义何时涉及远程工作，何时涉及所有人在同一空间工作(当然，要有适当的社交距离程序)。
*   严格应用基本规则，这样您就有了构建 mob 编程实践的坚实基础。
*   在安静的地方选择大屏幕、鼠标和键盘，限制潜在的干扰。
*   将空闲时间纳入你的非 sprint 工作日程，这样团队成员就可以查看电子邮件和处理其他项目。
*   定义休息时间(番茄工作法可能是一种选择)。

## Mob 编程值得探索…即使是现在！

在过去的几个月里，我学到了很多关于 mob 编程的知识，并且相信它有一定的魔力。在 Bonitasoft，聪明的实现是开发团队接受集体智慧和 mob 编程的价值的结果。我们更快地交付项目，在工作中享受更大的满足感。经过一些调整，通过将它添加到您的开发方法选项中，实现它的价值是可能的。