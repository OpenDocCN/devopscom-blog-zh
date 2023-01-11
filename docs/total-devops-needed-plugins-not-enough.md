# 总 DevOps 是必要的，插件是不够的

> 原文：<https://devops.com/total-devops-needed-plugins-not-enough/>

[Trace3](http://trace3.com) 很荣幸成为上个月在旧金山举行的[CloudBees Jenkins World 2017](https://www.cloudbees.com/jenkinsworld/home)活动的[金牌赞助商、参展商、DevOps Institute 领导力认证课程的培训师](https://www.youtube.com/watch?v=UGy22ddIJZ8)以及 cloud bees 的最新合作伙伴。詹金斯世界 2017 吸引了 [54 家赞助商/参展商](https://www.cloudbees.com/jenkinsworld/sponsors)，比 2016 年增长了 80%。

对这一事件的兴趣和赞助者的增长表明，用于创建连续工具链以实现连续交付和 DevOps 的可用工具选择的数量正在增长。我们从 Jenkins World 2017 中获得的一个重要信息是:[插件是不够的](https://trace3.com/devops/)！

事实上，XebiaLabs 的“工具周期表”是一个勇敢的尝试，用来说明 DevOps 工具的类别和特定工具的属性。元素周期表第二版现在发布了，听说第三版已经在路上了。虽然表格显示了令人印象深刻的 15 类工具，但我估计实际上有 29 类，如果你考虑用于云管理、测试管理、测试创建、代码分析、代码协作、ALM 系统、仪表板、安全和其他的工具。

XebiaLabs 的表格显示了每个工具的五个属性:开源、免费、免费增值、付费和企业。在我看来，至少还有另外两个类别:生态系统和云就绪性。虽然表格显示有 120 个工具，但我自己估计有 300 多个 DevOps 工具，包括 CloudBees、Electric Cloud、Perforce、Scalyr、Service Now、Tricentis。SmartBear，SonarQube，Parasoft，Coverity，赋格，QA Symphony 等等。

虽然工具类别、工具和属性的确切数量是有争议的，但是对于连续交付工具链来说，有许多工具可供选择。将工具集成到无缝工具链中的实践状态是插件或自己编写脚本。任何实现过工具链的人都知道，工具插件的存在虽然有用，但还不够。每个插件的质量和完整性差别很大。一些现成的插件是如此的基础，它们只不过是市场架构。即使最好的插件也仅限于特定版本对的工具之间的成对匹配，而不是通用的工具或版本。例如，带有 Jenkins X 版插件的工具可能无法与 Jenkins Y 版或任何版本的 CloudBees Enterprise 或其他工具一起使用。

由 14 家参与厂商在 Jenkins World 2016 上宣布的 [DevOps Express](https://devops.com/introducing-devops-express/) 协作计划是解决插件问题的一次尝试。一年后， [DevOps Express 网站显示 18 个类别的 123 个工具已经增长](https://www.devops-express.com/the-ecosystem/)。然而，就像 XebiaLabs 工具周期表一样，值得注意的是，对于特定企业的工具链可能需要的任何工具组合来说，不全面(并且缺乏插件兼容性)的工具类别和工具的数量是没有保证的。

每个企业都有独特的工具链需求和偏好。选择和集成 DevOps 工具并不像购买一盒“标准的”乐高积木，制造商保证这些积木可以组装在一起。每个工具和插件都是不同的。

工具的选择、工具的组合以及所选工具的集成都必须仔细选择，以满足特定的客户需求。更重要的是，必须对集成进行架构设计，以确保所选择的组合能够在无缝工具链中很好地协同工作。

除非有一个绝对标准的插件架构，保证所有的工具插件都符合这个架构，否则专家咨询服务将是做出工具选择和确保工具链工作的关键。

面对如此快速增长的工具和供应商列表，只有具备深刻洞察力且与最广泛的工具供应商建立了合作关系的最有能力的咨询团队，才能恰当地解决企业 DevOps 解决方案。

[马克·霍恩布洛尔](https://devops.com/author/marc-hornbeek/)