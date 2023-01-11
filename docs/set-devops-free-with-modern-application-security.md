# 借助现代应用程序安全性解放开发人员

> 原文：<https://devops.com/set-devops-free-with-modern-application-security/>

开发团队越来越多地使用云计算和[微服务](https://devops.com/?s=microservices)等技术，结合 DevOps 原则，以更快地创新并保持竞争力。

但是这种进步是有代价的。DevOps 的快节奏让安全团队不得不努力跟上步伐并安装适当的安全护栏。传统的安全实践通常发生在发布前的最后阶段。敏捷软件开发的快速发布周期经常使这变得困难，如果不是不可能的话。

开发速度超过了安全团队检查配置和扫描漏洞的速度，尤其是现在开发人员的数量超过了安全专业人员的数量 [500 比 1](https://portswigger.net/daily-swig/githubs-nico-waisman-security-is-not-just-an-opportunity-but-a-responsibility-for-us) 并且现代应用程序环境代表了一个巨大的攻击面。

保持安全的压力已经导致了 DevOps 作为 DevSecOps 的逐渐重构，其中安全性被“左移”并在软件开发生命周期的早期引入。

不幸的是，尽管大多数企业理解 DevSecOps 的意图，但他们仍然不确定如何将该意图转化为行动。事实上，[只有 14%在整个软件开发生命周期中完全集成了安全性](https://portswigger.net/daily-swig/githubs-nico-waisman-security-is-not-just-an-opportunity-but-a-responsibility-for-us)。

[最近的研究](https://about.gitlab.com/developer-survey/)还显示，虽然 65%的安全团队报告向左移动，但不到五分之一的团队正在进行必要的扫描，以验证这种移动是否确实发生。同一份报告表明，大多数安全团队没有监控和保护尖端应用技术的流程，如微服务、API 和云本机/无服务器。

当生产中出现问题时，这种缺乏可见性会使安全组织视而不见。漏洞在开发周期中被发现的时间越长，修复它们的成本就越高。IBM 系统科学研究所的一项研究表明，修复在实现过程中发现的缺陷的成本是在早期设计阶段发现的缺陷的六倍。生产中发现的一个缺陷的成本可能是它的 100 倍。更令人不安的是，[将近一半的企业](https://www.prnewswire.com/news-releases/devsecops-study-finds-that-nearly-half-of-organizations-consciously-deploy-vulnerable-applications-due-to-time-pressures-301107632.html)承认部署易受攻击的应用程序，只是为了满足紧迫的期限。

很明显，为了支持更快、更频繁的部署，法规遵从性和安全监督经常被忽视，甚至被故意回避。

## 德沃普斯-德夫塞科普斯大分水岭

最重要的问题之一在于开发者根深蒂固的观念。在过去，团队是独立工作的，在不同的开发阶段之间有严格的时间表。安全操作(SecOps)团队经常在开发和发布过程的最后阶段引入安全功能，这导致了延迟。

成功地将“Sec”放入 DevSecOps 依赖于改变旧的文化偏见，强化拥抱安全性的需要，并为团队提供正确的工具和自动化，以在不减慢整个组织的情况下做出更明智的决策。本质上，DevOps 和安全团队都是为了同一个目标——高质量、及时的产品。区别在于他们如何衡量和定义“高质量”和“及时”。

事实是，发展不会很快放缓。现在，38%的开发者每月发布一次或更快的版本，54%的容器只能使用 5 分钟或更少。将安全性视为固定在代码上的独立实体，而不是必须端到端嵌入的关键特性，会减慢开发过程并降低效率。

## 提供速度和安全性

组织必须回答的提高应用程序安全性的核心问题是:什么使开发运维团队和应用程序安全团队更容易协作？内置安全性到底是什么样子的呢？

对于希望提高 DevOps 安全性的组织，这里有一些提示:

*   尽可能实现安全自动化。投资可自动化并直接嵌入 CI/CD 渠道的安全解决方案。这使得保护应用程序变得更加容易，而不会为了安全而牺牲开发速度。采用静态代码分析、动态分析和渗透测试等技术可以降低风险，并提醒开发人员注意潜在的问题。永远不会有足够的安全专业人员独自处理所有的安全问题，所以尽可能使用自动化。
*   把安全建成护栏，而不是大门。提供适当的引导和工具，让安保成为护栏而不是大门。例如，确保开发运维团队能够访问模板化的策略，使他们能够从一开始就使应用程序符合安全要求，而不会增加不必要的开发时间。应用程序和安全策略也可以作为 CI/CD 管道的一部分进行测试，因此它们像任何其他功能规范一样接受检查。简而言之，为开发人员提供创建和测试应用了适当安全控制的应用程序所需的一切非常重要，否则他们不会这样做。让开发团队更好地理解安全性和自助合规性，可以减少组织的漏洞和风险。开发人员总是想走得更快，所以让他们安全地“加速”成为可能。
*   **实现更主动的责任。**不能指望普通开发人员拥有跟上所有最新安全趋势所需的专业知识水平——他们很难保持自己的编程技能与时俱进。通过选择在 CI/CD 反馈循环中提供简化、易于理解的见解的解决方案，降低复杂性并更容易获得开发人员的认可。
*   使安全性具有适应性、可扩展性和可靠性。利用可为任何环境提供一致、集中和自助式安全性的解决方案来保护应用。例如，人工智能驱动的安全策略引擎是实现必要的适应性的一种方式，以支持由 CI/CD 方法产生的应用程序的快速变化。能够调整安全策略以应对最新的攻击并识别依赖性，可以更容易地评估风险并更快地采取行动。

## 无摩擦和适应性安全的黎明

安全不能再是事后的想法，附加在流程上。如今，集成安全性必须成为任何 DevOps 实施的正常组成部分。使安全无摩擦且适应性强，使开发团队能够无所畏惧地向前推进。现代应用程序安全性可以成为一个强大的支持系统，使组织能够安全地实现其业务目标。