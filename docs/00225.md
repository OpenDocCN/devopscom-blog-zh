# 云和开发运维自动化的五大技巧

> 原文：<https://devops.com/five-top-tips-cloud-devops-automation/>

不久前，我无意中听到有人问为什么许多“多云的人”都搬到了 DevOps。

一个原因当然是云是 DevOps 的核心。DevOps 的许多基础原则——快速迭代、敏捷开发、自动化测试、持续交付和持续集成——在没有云的情况下几乎不可能实现。然而，我认为它比这更深刻。DevOps 和云都是由我整个职业生涯一直从事的同一项技术从根本上实现的，即自动化。

当 IT 领导者对云感到兴奋时，主要是因为自动化。当然，云提供商对广泛的网络接入和资源共享等基本特征感到兴奋，因为这是他们最大化覆盖范围和最小化成本的方式。类似地，首席财务官对计量服务感到兴奋，因为这意味着他们只为他们使用的服务付费。

然而，根据 Luth Research 最近的一项研究[，大多数 IT 领导者优先考虑由按需自助服务和快速弹性实现的更高价值——更快的创新、卓越的性能、更好的可扩展性和更高的弹性。这些功能深深植根于调配、部署、配置、纵向扩展/横向扩展和其他流程的自动化。](https://www.ca.com/us/register/forms/collateral/techinsights-report-cloud-succeeds-now-what.aspx)

类似地，devo PS——超越某一点——也建立在自动化的基础上。正如 Rackspace 的首席技术官 John Engates 在本刊最近的专栏文章[中指出的，“DevOps 不仅仅是一套自动化工具。”当然，他是对的。通过文化和结构的改变，你可以取得很大的成就——更好的合作、共同的目标、团队建设、过程改进等等。](http://www.informationweek.com/strategic-cio/executive-insights-and-innovation/devops-its-only-chance-of-keeping-up/d/d-id/1127845)

然而，用于发布自动化、配置自动化、流程自动化、测试自动化、服务虚拟化和配置的工具(仅举几例)正在通过快速成熟的 DevOps 自动化工具链增加巨大的价值。事实上，在 Vanson-Bourne 最近的研究中，全球超过一半的高级 IT 决策者将自动化视为最重要的 DevOps 组件，高于敏捷开发、协作团队和流程调整等公认的中坚力量。

回顾企业自动化的历史，并考虑我自己的经验，我相信有许多共同的原则可以应用于云和 DevOps。以下是我的五个最佳建议:

## 不要自动化糟糕的流程

自动化糟糕的流程只会让糟糕的事情发生得更快。这似乎是显而易见的，但是我经常看到自动化只会编码(并加速)一个糟糕的现有实践。为了避免一场[高速列车事故](https://en.wikipedia.org/wiki/2010_Flash_Crash)，首先要识别、编目、记录、审查和提炼关键的手动流程，以确保你在正确的时间以正确的方式自动化正确的活动。解决简单性、速度和吞吐量问题，甚至在应用自动化之前。消除部门、技术和纪律之间的摩擦。从简单开始，保持好奇心，有条不紊地迭代。然后确保你自动化的深度、彻底和有效。

## 跨技能现有资源

[优秀的人才很难找到](http://www.ca.com/us/news/press-releases/na/2013/ca-technologies-top-5-it-predictions-for-2014.aspx)和[云计算和开发相关技能的薪水](http://techhub.dice.com/2014-Dice-SalarySurvey-Landing.html)是 IT 行业中最高的。这解释了为什么，根据同一个 [Vanson Bourne research](https://www.ca.com/us/register/forms/collateral/techinsights-research-what-smart-businesses-know-about-devops.aspx) ，超过 70%的 DevOps 领导在重新培训现有人员，而只有 50%的人在招聘新的资源。在简历中寻找有自动化历史、经历过多次技术变革的员工，而不是某个自动化技术或产品的专家。找一个相当于[“优秀运动员”的 IT，而不是“位置球员”](https://enterprisersproject.com/article/skills-gap-hire-flexible-athletes-not-single-position-players)。

## 安全不能是事后的想法

无论是自动化大型机 IPL 还是编写产品代码发布脚本，自动化系统和负责自动化系统的人员总是需要高特权(并且经常共享)的用户 id。这是一个审计危险信号，[可能导致高影响事件](https://aws.amazon.com/message/680587/)，无论是意外的还是恶意的。身份和访问管理提供了基本的[审计和控制](https://en.wikipedia.org/wiki/Information_technology_audit)，同时让用户(包括自动化工具和 API)在需要时能够轻松访问他们需要的资源(本地和云中)。

## 记录、测量和备份

如果你做得好，自动化很快就会变得无处不在和至关重要。没有文档，你会在你的云或 DevOps 机器上创建难以理解的系统、部落知识、[英雄](http://www.infoq.com/articles/scalability-worst-practices)和其他[反模式](http://blog.devopsguys.com/2013/02/20/twelve-devops-anti-patterns/)。没有测量，你无法知道复杂的自治系统是否(或何时)失控或停止工作。如果没有备份，关键系统很容易出现不可恢复的故障。云和 DevOps 团队必须重视并证明文档、测量和备份等传统学科，尽管这可能会很痛苦。

## 将意识融入自动化

随着自动化变得至关重要，它必须对错误、故障、异常和其他意外情况具有弹性，并且仍然能够提供正确的结果。还记得当[“自主计算”](https://en.wikipedia.org/wiki/Autonomic_computing)还是一件事的时候，当我们梦想“自我感知”系统的时候吗？类似地，像[、【期望状态】和【幂等性】](https://blogs.msdn.com/b/powershell/archive/2013/11/01/configuration-in-a-devops-world-windows-powershell-desired-state-configuration.aspx)这样的概念至少可以追溯到大型机和服务器自动化。类似的概念也适用于云计算和 DevOps。在这两种情况下，自动化例程意识到自己的状态和周围的环境是至关重要的，以便它们可以测试和适应意外情况，并仍然交付预期的结果。

鉴于自动化历史的深度，以及与现代计算的许多相似之处，有些人可能会说云并不新鲜，我们从大型机开始就一直在这么做；而其他人会对 DevOps 说一些类似的话。我认为他们是错的，但肯定有相似之处，乔治·桑塔亚纳说得有道理——如果我们要试图书写未来，同时避免过去的错误，我们至少应该了解历史。