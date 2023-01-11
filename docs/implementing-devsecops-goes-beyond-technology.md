# 实现 DevSecOps 超越了技术

> 原文：<https://devops.com/implementing-devsecops-goes-beyond-technology/>

虽然技术对于实施 DevSecOps 至关重要，但推动它向前发展的是人、流程和文化。就在去年，一项调查发现 58%的技术领导者认为现有文化和缺乏技能是在软件开发过程中嵌入安全测试和评估的障碍。该报告发现，只有大约四分之一的公司强烈认同其组织的文化和实践支持开发、运营和安全方面的协作。

最近与 DevOps.com 合作进行的另一项关于开发人员技能的调查发现，70%的受访者表示他们接受的安全教育不足以满足他们当前职位的要求。

可以找到大量类似的统计数据，它们指向一个反复出现的主题——在实施 DevSecOps 时，对开发人员和安全团队的教育、培训和支持与现代应用安全解决方案一样重要。

## 自动化有助于克服挑战

大多数开发人员希望创建高质量、安全的代码。通常，问题是开发人员从未接受过什么是安全编码的正式培训，无论是在传统教育中还是在工作中。好消息是越来越多的组织开始为开发团队提供这种培训。随着开发和发布周期的加快，开发人员需要找到以更少干扰的方式进行安全测试的方法。

此外，开发团队正在获得对应用程序安全工具预算的一些控制权。用于测试代码和评估应用程序安全风险的传统工具并不能满足 DevOps 测试所需的速度。每当为开发团队评估新的安全分析工具时，自动化应该是首要考虑的。静态分析测试应用程序代码的各种安全缺陷，它可以完全自动化地集成到 IDE 和持续集成(CI)过程中。在 IDE 中，它通过强调潜在的漏洞和建议最佳实践，在软件工程师编码时为他们提供早期的安全指导和教育。

公司还可以通过确保开发人员不必特意运行安全工具来减少摩擦。开发团队应该能够查看和筛选结果，并利用插件和/或 API 将安全工具无缝集成到他们已经在使用的工具链中。这意味着没有一种放之四海而皆准的方法可以应用于任何开发团队；相反，花点时间去了解该团队目前是如何工作的，并与他们一起以最少干扰的方式引入安全工具。

## 转变心态

最大的挑战之一是要求开发人员做一些他们以前没有做过的事情。使用 DevSecOps，看起来好像开发团队被要求承担更多的工作，但是实际上，组织正在用计划好的工作替换计划外的工作。开发团队不是在发布周期的后期解决缺陷，而是在早期扫描并解决缺陷。这种文化转变可能会很缓慢，但是开发人员和开发经理应该认识到，以这种方式嵌入安全性将会更有效、更安全，同时还会减少他们计划外的工作。

让开发团队在安全任务上有更多的自主权对于安全从业者来说也是令人畏惧的，但是为了促进更短的开发迭代，安全必须放弃一些控制，并且还要重新考虑他们如何在业务环境中考虑风险承受能力。从历史上看，开发人员和安全从业人员之间的关系一直是敌对的，但是 DevOps 和 DevSecOps 方法使这种关系变得更加合作。尽管如此，许多安全团队对放弃控制权的想法感到不安。

## 适应以避免增加新的技术债务

即使理解了生成更安全的代码对开发和安全性都有好处，减少技术债务也是渐进的，从将安全性直接集成到开发过程开始。将安全发现与技术债务放在一起，以备将来某一天使用，这似乎很方便，但是让安全债务堆积起来是不实际的。

组织正在分散安全工作，特别是通过安全冠军:每个开发团队中有一到两个人作为产品安全的耳目，负责一些以前会在安全团队中成为瓶颈的日常任务。安全冠军可以帮助检查安全代码，或者指导团队中的其他人如何修复安全问题。以这种方式分担安全责任可以进一步缩小安全团队和开发团队之间的差距，减少安全团队的工作量，同时允许开发团队更加自给自足。

对于开发人员来说，上下文切换是有生产成本的。如果他们在积极处理特定功能或代码部分时发现了安全缺陷，这只会造成最小的破坏，并且可以快速修复。相比之下，如果他们在两个星期后发现了同样的安全缺陷，在他们转移到一个完全不同的特性之后，在他们能够正确地修复缺陷之前，他们将承担上下文切换回早期特性的成本。从长远来看，在 SDLC 的早期发现并修复缺陷不会显著延迟上市时间。

下面是在您的组织中实现 DevSecOps 的一些最佳实践。

## 1.在开发周期的早期嵌入安全流程

确保在软件开发过程的每个阶段都进行扫描，并与您的开发团队合作，将安全性集成到现有的工作流和工具中。当软件投入生产时，代码应该已经被扫描了多次，所有的漏洞都应该被修复了。[研究](https://www.veracode.com/state-of-software-security-report)表明，开发过程中安全扫描的频率与修复速度相关。具体来说，进行每日扫描的企业修复漏洞的速度是典型组织的 11.5 倍。

## 2.将安全责任直接交给开发团队

开发人员需要对他们的应用程序的安全性负责。这是将安全性无缝集成到他们现有工作流中的唯一方法。感觉有人进来并强迫调整他们的代码可能会令人沮丧，但这并不是说安全团队应该放手不管。他们需要扮演顾问的角色，与开发人员一起确保代码安全。培训是这里的关键。开发人员很可能不熟悉最新的安全策略。安全专家需要就已知的漏洞、威胁和工具对开发人员进行培训。

## 3.在每个开发团队中确定一个安全冠军

在开发团队中找到一个能够超越自动化测试工具的人作为安全团队的眼睛和耳朵同样重要。不要将该角色分配给已经承担额外责任的成员，而是选择对安全感兴趣的人。因为工程师可能经常更换团队，所以每个开发团队中最好至少有两个安全冠军。如果一个人继续前进，机构知识将留在团队中，新的安全冠军将被培养出来。

## 4.自动化安全扫描

安全不能成为发展的阻碍。如果是这样，开发人员将无法实现适当的安全策略。有了自动化工具，开发团队可以在整个软件开发生命周期(SDLC)中高效地测试代码，确保更安全的应用，同时按时交付软件。

## 5.采取数据驱动的方法来跟踪进展

展示进展是至关重要的，对于希望看到安全性对其软件的影响的开发人员和需要清楚了解应用程序安全性投资回报的管理团队来说都是如此。具有引人注目的可视化功能的分析通过提供快速直观的数据来支持这一价值，因此组织可以评估其当前状态并采取措施改善其风险状况。复杂的分析使组织能够根据特定的风险承受能力定义自定义安全策略，从而锁定关键应用程序并修复关键发现。

— [克里斯·英格](https://devops.com/author/chris-eng/)