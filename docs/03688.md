# Aqua 3.0 为 AWS Fargate 和 Azure 容器实例提供了运行时安全性

> 原文：<https://devops.com/aqua-3-0-delivers-runtime-security-aws-fargate-azure-container-instances/>

*Aqua Security 正在申请专利的 MicroEnforcer 架构保护在
“零基础设施”容器即服务环境*上运行的容器

**马萨诸塞州波士顿，2018 年 3 月 7 日**–市场领先的基于容器和云原生应用安全平台提供商 Aqua Security 今天宣布推出其平台的 3.0 版本，该版本采用了一项正在申请专利的新技术，可为在容器即服务(CaaS)环境中运行的应用提供运行时安全控制，如微软的 Azure Container Instances (ACI)和亚马逊 Web 服务(AWS) Fargate。Aqua 3.0 还引入了大量新的 Kubernetes-原生控件，这些控件利用了流行的编排软件的最新版本-在此单独发布。

AWS Fargate 和 Microsoft ACI 都是在去年年底发布的，它们提供了一种新的基于云的服务，使用户能够按需运行容器，而不需要配置或管理虚拟机实例。从安全的角度来看，依靠主机级控制来保护运行时环境的方法对于这些容器是无效的，因为主机不再是可见的、可管理的实体。

Aqua 新的正在申请专利的 micro forcer*技术通过在开发生命周期的早期将安全控制插入到容器中来解决这个问题。当构建容器映像时，微强制器以某种方式嵌入其中，以便以后允许它监视和控制实例化的容器，包括防止特定的未授权容器活动的能力。*

*“毫无疑问，容器变得越来越容易使用，越来越普及，虽然技术堆栈的某些方面正在整合，但部署的选项变得更加多样和灵活。”Aqua Security 的联合创始人兼首席技术官阿米尔·杰尔比说。“云原生应用程序提供了一个机会，可以提供更加精细的安全控制，并且无论应用程序在哪里运行都可以统一应用这些控制，这是我们为将工作负载迁移到混合云环境的企业带来的主要优势之一”。*

*Aqua MicroEnforcer 的工作原理:*

*   *MicroEnforcer 在构建过程中被添加到容器映像中；*
*   *安全图像保存在私有或公共注册表中；*
*   *当映像在 CaaS 环境中运行时，容器在映像运行时策略的约束下运行，并向 Aqua Command Center 报告。*

*Aqua MicroEnforcer 可保护容器运行的任何地方:*

*   *它识别恶意活动，如访问未经授权的网络或试图将代码注入容器，并在运行时阻止这些尝试；*
*   *它安全地将秘密注入到授权在运行时使用它们的容器中，利用现有的企业秘密存储，包括 Hashicorp Vault、Cyberark Password Vault、AWS KMS 和 Azure Vault*
*   *MicroEnforcer 生成的所有警报都被发送到 Aqua Command Center，该中心还可以将它们发送到 SIEM 和分析工具，如 Splunk、MicroFocus ArcSight 或 Sumologic。*

*Aqua 的 MicroEnforcer 增强了 Aqua 现有的 Enforcer，这是一个“sidecar”容器，可以对在定义的主机(运行 Linux 或 Windows 2016 的虚拟机或裸机服务器)上运行的容器进行安全控制。这两种机制——Enforcer 和 micro forcer——相辅相成，使 Aqua 客户能够从一个控制台管理多种云技术的部署。*

*Aqua 的平台目前正被数十家全球 1000 强客户使用，为保护基于容器和云的原生应用提供了最全面的全生命周期解决方案，可在本地或云中运行，并支持 Linux 和 Windows 运行时环境，以及最近宣布的 Pivotal Cloud Foundry 公共测试版。该平台推动了 DevSecOps 自动化，并为运行时应用提供了可见性和安全性，包括主机级和网络级控制。*

*Aqua 3.0 与 Kubernetes 1.8 或更新版本的实现兼容，可供现有 Aqua 客户使用。欲了解更多信息:*

*   *Fargate 博客*
*   *ACI 博客*
*   *网络研讨会:在 CaaS 世界中保护集装箱*

***关于 Aqua Security***

*Aqua Security 使企业能够从开发到生产保护其容器和云原生应用，从而加快应用部署并弥合开发运维与 IT 安全之间的差距。Aqua 的容器安全平台提供了对容器活动的全面可见性，允许组织实时检测和防止可疑活动和攻击。Aqua 平台与容器生命周期和流程编排工具相集成，提供了透明、自动化的安全性，同时有助于执行策略和简化法规遵从性。Aqua 成立于 2015 年，由光速创投(Lightspeed Venture Partners)、微软创投(Microsoft Ventures)、TLV 创投(Bernstein Partners)和 IT 安全领域的领军人物提供支持，总部位于以色列和马萨诸塞州的波士顿。欲了解更多信息，请访问[www.aquasec.com](http://www.aquasec.com)或关注我们的[twitter.com/AquaSecTeam](https://twitter.com/aquasecteam?lang=en)。*