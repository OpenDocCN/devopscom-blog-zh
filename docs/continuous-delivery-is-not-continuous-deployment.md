# 连续交付不是连续部署

> 原文：<https://devops.com/continuous-delivery-is-not-continuous-deployment/>

每隔一段时间，重温一个在大多数人的雷达下飞行的话题是值得的。持续交付和持续部署之间的区别就是其中之一。虽然那些沉浸在开发运维中的人很清楚软件可以每天(甚至更频繁地)交付，但部署却不那么频繁，而且更依赖于开发和营销周期。

大多数 CI/CD 工具可以并且确实每天都在制作“可部署”的应用程序，甚至在每次代码被检入的时候。理论上，这些构建中的每一个都是部署的候选，并且每一个都至少经过了某种程度的测试。

但是设置托管这些应用程序的环境是一个单独的步骤。如今，这通常是由脚本处理的一个步骤，脚本配置/移动一切以将应用环境构建到一个具有网络、数据源、存储等知识的综合系统中。

我之所以重提这个话题，是因为新人们经常听到“CD”，并认为这是最终状态。当然不是；必须部署应用程序——至少要部署到测试和生产环境中，在许多企业中还要部署到试运行环境中。

虽然这些环境几乎总是不同的(例如，Test 不与 Prod 共享 IP 空间)，但是部署必须尽可能相互镜像，以使 Test 能够代表 Prod 的情况。

与 DevOps 工具链中的任何步骤一样，用于实现持续部署的脚本并不是一个很好的解决方案。它们当然是很好的第一步——将以前手工完成的工作自动化——但是有一些工具可以使体验更简单、更动态，应该考虑使用。

无论是显式的连续部署工具还是应用程序发布自动化(ARA)工具(或者是调用连续部署工具的 ARA，正如我们已经看到的一些工具)，出于多种原因，消除对手动编辑的脚本的依赖是有用的，首先是为测试和生产维护单独的脚本，并且当对应用程序进行更改时，必须在两个地方进行更改(例如更改数据库的位置或切换到专用的 AAA 服务器)。这使得脚本变得脆弱。工具可以提供共享部署和定制部署部分，以便可以将多个更改限制在那些真正需要单独处理的事情上。

部署在很大程度上是一项目标练习。代码已经生成；部署只是给它一个家。从历史上看，这要求代理分散在数据中心，以帮助目标部署。越来越多的无代理工具可用，它们允许连续部署的适应性，同时不需要在可能参与部署活动的每台机器上安装代理。

从脚本转移到持续部署工具的另一个主要好处是巨大的:其他一切都是受版本控制的，这提供了内置的回滚。一个开发人员把修复那个 bug 搞得一团糟，事情变得更糟？回滚更新，直到问题得到解决。像 Git 这样的工具使这一点变得特别容易。在部署端，需要相同的功能。“7.2 版被认为违反了 GDPR”可能需要回到以前的版本。但是基于脚本的部署总是前瞻性的。修改脚本反映当前环境就够了，而且是很少的需要并行开发回退脚本的组织。然而，这种功能是由连续部署工具免费提供的——它所构建的功能可以撤销，因为它是自动版本化的。

版本控制的好处不仅仅是回滚:它允许 AB 测试的多个版本部署，并允许尽可能向前和向后跳转，以满足当前的目标。

是灵丹妙药吗？当然不是。每项技术都会带来新的挑战。但是持续部署解决的问题比它产生的问题多。它所产生的大多数问题(例如，希望在非云环境中与网络和存储服务更好地集成)都将在任何脚本编写之前由这些工具以一致和可重复的方式解决。因为这些工具旨在创建一致且可重复的结果。

当你在那里踢它的时候，考虑实现持续部署工具来处理 DevOps 的最后一英里。它们会让你的生活更轻松，让你的环境不那么脆弱。

唐·麦克维蒂