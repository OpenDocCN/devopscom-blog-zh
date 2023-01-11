# 保护 CI/CD 管道以确保软件供应链的安全

> 原文：<https://devops.com/protecting-ci-cd-pipelines-to-secure-the-software-supply-chain/>

云原生应用变得越来越复杂。今天的[软件供应链](https://devops.com/?s=software+supply+chain)由混搭代码的基础设施栈、数百个开源和商业组件、服务和 API 组成，充满了安全风险。与此同时，管理现有应用程序需求，同时进行创新和承担新的责任领域(如安全性)的能力让 DevOps 团队力不从心。对整个软件供应链中 c 连接和可利用弱点数量的关注现在要求组织采取主动的方法来保护他们的持续集成和持续交付(CI/CD)系统，因为它们已经成为攻击者渗透多个生产系统的目标。但是满足这一要求并不容易，因为它通常需要组织在构建周期中选择实施多少安全性，同时量化他们快速构建和部署的风险。

最近的一项 [调查](https://info.jupiterone.com/resources/scar-report-2022) 显示，一个组织几乎所有(97%)的资产和安全问题现在都在云中。然而，一个组织只有 29%的资产与特定于云的策略相关联。解决这一差距需要组织采取积极主动的方法来保护其技术基础设施，尤其是保护其软件供应链的动脉:CI/CD 管道。通过在其治理方法中采用新的安全性和合规性策略，组织可以更好地保护其 CI/CD 渠道和云应用。

越来越多地转向可编程的基础设施和基础设施即代码(IaC)实践来构建基础设施和管理配置文件。但是随着这种实践而来的是暴露应用程序凭证、API 密钥、加密密钥和数字证书的风险增加。支持 CI/CD 管道的工具现在已经成为云应用的动脉，安全地存储、传输和审计数据变得越来越具有挑战性。此外，当 CI/CD 工具与 DevOps 环境中的其他系统交互时，会增加暴露配置文件的风险。例如，构建系统中的漏洞可被用来访问生产系统，这可能导致敏感信息的暴露或恶意代码的注入，从而破坏整个 CI/CD 管道，进而破坏软件供应链。

最近的 42 号机组云威胁 [报告](https://www.cybersecuritydive.com/news/unit-42-cloud-misconfigurations-software-supply-chain-security/607290/) 显示，过度宽松的凭证在 CI/CD 渠道中创造了额外的风险机会。研究发现，63%的 IaC 模板包含错误配置，91%的容器图像包含高度或严重的安全漏洞。为了解决这个问题，组织需要在配置云工作负载之前，在构建过程中发现安全问题。例如，在网络安全管理软件产品妥协案中，攻击者使用为公司构建周期设计的定制恶意软件来观察每一步。对于 DevOps 和 DevSecOps 专业人员来说，这种攻击在软件构建过程中的复杂性是一个重要的教训，并揭示了需要如何实现安全性。

解决这个问题的一个方法是能够识别 CI 管道的错误配置，这可以提高软件供应链的安全性。因为 CI 管道是在代码中配置的，所以可以使用相同的策略-代码方法来识别 IaC 错误配置或开源漏洞，以暴露 CI/CD 弱点。开发运维团队和开发人员团队可以保持配置只对为产品发布而构建的小组开放。通过建立对管道的强制许可，可以更好地控制谁可以向存储库提交代码更改、创建容器以及将代码部署到不同的环境。

如今，构建周期中强大的信任链并不常见。但是随着组织寻找通过向左转移来加强其风险态势的方法，安全和开发团队可以通过正确的 CI/CD 工具和框架来主动强化管道，并将行业推向更安全的软件供应链。