# Azure 中的 DevSecOps

> 原文：<https://devops.com/devsecops-in-azure/>

DevSecOps 无处不在，您的组织很可能正在向这种开发、安全和运营的融合转变。在内部环境中，您可以通过混合和搭配现有的和新的工具来构建自己的 DevSecOps 流程。然而，在云中，大部分环境是由您的云提供商决定的。 微软的 Azure 云以其强大的安全能力而闻名。具体来说，Microsoft 开发了一套功能和服务，可以帮助您轻松地进入 DevSecOps 工作流。这些工具是预先集成的，支持从 CI/CD 到身份管理的所有内容。让我们看看它们是如何工作的。

## 什么是 DevSecOps？

安全性是 DevOps 的重要组成部分。但是要确保在 CI/CD 过程中开发的软件是真正安全的，这是一个挑战。

DevSecOps 是一种组织模式，即使在高开发速度下，它也能使这成为可能。DevOps 团队可以使用这种方法从开发生命周期的一开始就防止安全问题，确保他们的软件不仅是高质量的，而且是安全的，对失败有弹性的。

DevSecOps 是一个将应用程序开发、安全性、运营和基础架构代码(IaC)与自动化连续交付周期相结合的学科。这里有三个实践可以帮助团队走向 DevSecOps 过程:

*   **关注平均检测和恢复时间 —** T 这些指标显示了检测漏洞和恢复所需的时间。这可以通过连续的现场测试来跟踪。在评估可能的政策时，改进这些指标应该是一个重要的考虑因素。
*   **纵深防御 —** E 架构中的每个组件都应该是安全的，以便当攻击者设法破坏系统时，有多种安全措施和控制来阻止他们。这终结了组织必须不惜一切代价捍卫的“安全边界”的概念。每个组件都必须有自己的安全微边界，这是一种零信任方法。
*   **持续学习****—**TEAM 应定期对安全实践及其环境进行评估，尤其是在发生安全事件之后。每次发现并解决安全事件时，团队都必须评估开发生命周期中的错误，探索它是如何引发事件的，并确定改进流程的方法。

## 在 Azure 中启用 DevSecOps 的特性和服务

Azure 云提供了几个内置功能，使得采用 DevSecOps 流程成为可能。

### 1。 蔚蓝 DevOps

Azure DevOps 提供开发者服务，使团队能够规划任务、协作开发代码、构建和部署应用。Azure DevOps 支持一种协作文化和过程，在这种文化和过程中，开发人员、项目经理和贡献者一起开发软件。您可以在云中或 Azure DevOps 服务器内部使用 Azure DevOps 服务。

### 2。 用 Azure 管道构建和部署容器

您可以将 Azure Pipelines(Azure 云的 CI/CD 解决方案)与您的 Kubernetes 集群集成。使用相同的 YAML 文件建立多级 CI/CD 管道。

Azure Pipelines 允许你跟踪元数据，比如提交散列和问题号，从 Azure Boards 到容器映像。这提供了从任何安全问题到开发中特定变更的直接可追溯性。它还提供了清晰易读的文档，可以改善开发、运营和安全团队之间的反馈循环。

### 3。运行和调试带有开发空间的容器

开发 [Kubernetes](https://webinars.devops.com/common-kubernetes-challenges-solved) 应用程序时，需要在本地测试应用程序，并了解它们如何与相关服务交互。您可能需要与其他开发人员或团队合作开发和测试多个服务。

Azure 提供了到 Kubernetes 的桥梁，这允许你在连接到你的 Kubernetes 集群时在你的开发机器上运行和调试代码。您可以端到端地测试您的代码，在集群上运行的代码上设置断点，并在团队成员之间共享您的开发集群。这使得在部署到生产环境之前，可以在真实环境中测试和解决 [Kubernetes 安全问题](http://www.tigera.io/learn/guides/kubernetes-security/) 。

### 4。使用 Azure AD 管理身份和访问

微软身份平台将 Azure Active Directory (Azure AD)开发者平台向前推进了一步。它允许应用程序接受来自任何 Microsoft 身份的登录，并获得可用于调用 Microsoft APIs 或其他开发人员创建的 API 的令牌。这创造了一个大的、可互操作的生态系统。

Azure Active Directory B2C 提供 B2C 身份服务——客户使用其首选的社交、企业或本地帐户 ID 获得对应用程序和 API 的单点登录(SSO)访问。另一种选择是将 Azure AD 与本地 Active Directory 集成，用于 [混合和 Azure 迁移](https://cloud.netapp.com/blog/enterprise-migration-to-azure-keys) 场景。

你也可以使用 Azure 基于角色的访问控制(RBAC)来管理对云资源的访问。RBAC 让你可以管理谁可以访问你的 Azure 资源，他们可以做什么，以及哪些地区可以访问它们。

你也可以使用微软身份平台来保护 DevOps 工具本身，包括对 Azure DevOps 的原生支持以及与 GitHub Enterprise 的集成。

### 5。 用 Azure Key Vault 管理密钥和秘密

暴露秘密是现代应用中非常普遍的严重安全问题。Azure Key Vault 允许您通过将机密集中存储在 Azure Key Vault 中来管理机密的分发。密钥库大大降低了意外[泄露机密](https://devops.com/thycoticcentrify-strengthens-devsecops-capabilities-with-addition-of-advanced-reporting-in-devops-secrets-vault/)的几率。有了 Key Vault，应用程序开发人员不再需要在其应用程序代码中存储凭据或其他敏感信息。

### 6。Azure 策略和 Azure 安全中心

Azure Policy 允许您指定一个默认的允许配置，该配置会自动应用到所有云资源。这可以避免违反安全策略的错误配置。Azure 策略基于所需的状态配置(也称为声明性配置)工作，让您指定资源和服务的安全程度，以及如果不符合策略，是否在 Azure 中警告或阻止/修改部署。

在多租户模式下使用 Azure 时，可以在管理组、订阅或资源组级别应用策略。您可以为测试、试运行和生产环境定义特定的策略并实施法规遵从性要求。

Azure 安全中心(ASC)和顾问也可以轻松集成到开发运维流程中。ASC 使得用第三方安全工具的威胁情报或分析来扩充 Azure 中的事件流成为可能。

### 7。渗透测试

渗透测试是检查您的环境的基础设施或应用程序配置漏洞的推荐方法，这些漏洞可能会产生攻击者可以利用的漏洞。

Azure 渗透测试应该检查端点上的漏洞，应用模糊化(畸形输入)来发现业务逻辑漏洞，并执行端口扫描来识别网络漏洞。

微软为 Azure 中的 渗透测试提供具体指导，推荐产品和渗透测试服务提供商。

### 8。配置和基础设施扫描

为了确保云订阅和跨多个订阅的资源配置的安全性，您可以使用 Secure DevOps Kit for Azure (AzSK)的租户安全解决方案部分。

此外，您还可以利用 Microsoft Defender for Cloud 和 Microsoft Sentinel 等微软安全技术。这些解决方案提供监控和安全功能，旨在检测和警告需要调查和可能补救的异常事件或配置。

### 结论

在本文中，我介绍了 DevSecOps，并展示了 Azure cloud 如何提供一系列服务，让您轻松实现 DevSecOps 实践。这些包括:

*   Azure DevOps: T 它是一个古老的工具集，对 DevSecOps 环境提供了强有力的支持。
*   天蓝管道:T 何国产 CI/CD 产品。
*   Azure AD: 全面的零信任身份管理解决方案。
*   Azure Policy and Security Center:实现对安全策略的统一控制，以实现云自动化和云工作负载的安全可见性。

我希望这将有助于您迈出实践云中 DevSecOps 的第一步。