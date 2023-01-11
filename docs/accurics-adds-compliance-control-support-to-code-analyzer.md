# Accurics 为 Code Analyzer 增加了合规控制支持

> 原文：<https://devops.com/accurics-adds-compliance-control-support-to-code-analyzer/>

Accurics 在今天的在线 [KubeCon + CloudNativeCon 2020 大会](https://events.linuxfoundation.org/kubecon-cloudnativecon-europe/)上发布了[其开源 Terrascan 静态代码分析器](https://www.businesswire.com/news/home/20200817005085/en/Accurics-Releases-Open-Source-Software-Terrascan-Upgrade)的更新，增加了对开放策略代理(OPA)引擎的支持，使开发人员可以更轻松地创建自定义合规策略，此外还利用了 500 多种基于 CIS 基准的现成策略。

此外，Terrascan 现在可以作为 GitHub 动作使用，并包含在流行的 Super-Linter GitHub 动作中。它可以作为预提交挂钩安装，以帮助在代码作为 DevOps 工作流的一部分被推入存储库之前检测问题。

Accurics 开发者权益负责人塞萨尔·罗德里格斯(Cesar Rodriguez)表示，最新版本的 Terrascan 也用 Go 编程语言进行了重写，以提高整体性能。

Terrascan 将为管理基础设施而创建的代码作为漏洞代码以及偏差指标进行分析。然后，它会为云应用程序工作负载创建一个威胁模型，并在必要时与第三方工具共享数据，以自动将云设置回滚到其上次已知的批准状态。模型构建完成后，Accurics 会监控应用程序工作负载中会带来风险的变化，并实时生成每个工作负载的拓扑，以识别任何潜在的偏差指标。

![](img/639c752d83109d5bb86412d7acac56d6.png)

一份基于 Accurics 发布的云服务分析的最近报告发现，在所分析的令人震惊的 93%的云部署中，错误配置的云存储服务司空见惯，大多数还至少有一次网络暴露，其中安全组处于开放状态。

该报告还发现，在所分析的部署中，有 72%出现了硬编码私钥。在这些部署中，有一半发现了存储在容器配置文件中的未受保护的凭据。总共有 41%的组织拥有与硬编码密钥相关的高特权。在 100%的部署中，更改的路由规则会将包含敏感资源(如数据库)的私有子网暴露给互联网。

总体而言，该报告表明，只有 6%的云配置问题通过手动补救流程得以解决。

理想情况下，开发人员在云中部署应用程序时，应该实施网络安全和合规性控制。面临的挑战是，虽然开发人员已经可以使用工具来自动配置这些服务，但他们中没有多少人拥有工具来验证这些服务是否已经正确实现。

IT 组织仍然需要扫描运行时环境中的漏洞。然而，诸如 Terrascan 之类的工具将使 IT 团队能够通过向开发人员提供可轻松集成到持续集成(CI)工作流中的扫描工具来推进最佳 DevSecOps 实践的采用。

当然，DevSecOps 最大的问题仍然是文化。然而，大多数开发人员并不想部署不安全的云应用程序。如果获得了正确的工具，大多数开发人员都会做正确的事情，只要这感觉像是现有工作流的自然扩展，而不是由网络安全团队定义的不自然的行为，该团队对应用程序实际上是如何构造的知之甚少或一无所知。