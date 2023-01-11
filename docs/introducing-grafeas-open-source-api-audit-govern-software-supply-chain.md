# Grafeas 简介:一个用于审计和管理软件供应链的开源 API

> 原文：<https://devops.com/introducing-grafeas-open-source-api-audit-govern-software-supply-chain/>

Stephen Elliott，开发者平台和郭嘉宁产品经理，容器安全产品经理

大规模构建软件需要对软件供应链进行强有力的治理，而强有力的治理需要良好的数据。今天，Google 与 JFrog、Red Hat、IBM、Black Duck、Twistlock、Aqua Security 和 CoreOS 一起，很高兴地宣布推出 Grafeas，这是一项开源计划，旨在定义一种审计和治理现代软件供应链的统一方法。Grafeas(希腊语中的“scribe”)为组织提供了一个集中的事实来源，用于在不断增长的软件开发团队和管道中跟踪和执行策略。构建、审计和遵从工具可以使用 Grafeas API 来存储、查询和检索各种软件组件的综合元数据。

作为 Grafeas 的一部分，Google 还引入了 Kritis，这是一个 Kubernetes 策略引擎，帮助客户执行安全的软件供应链策略。Kritis(希腊语中的“judge”)使组织能够在部署 Kubernetes 集群时，基于存储在 Grafeas 中的容器映像属性(例如，构建来源和测试状态)的证明，实时执行容器属性。

“Shopify 正在寻找一种全面的方法来跟踪和管理我们运送到生产现场的所有集装箱，”Shopify 的高级安全工程师 Jonathan Pulsifer 说。“我们每个工作日运送超过 6，000 个构建，并维护一个包含超过 330，000 个容器图像的注册表。通过将 Grafeas 和 Kritis 集成到我们的 Kubernetes 管道中，我们现在能够自动存储漏洞并构建我们创建的每个容器映像的信息，并严格执行由 Shopify 构建的策略:我们的 Kubernetes 集群仅运行由我们的构建者签名的映像。Grafeas 和 Kritis 实际上帮助我们实现了更好的安全性，同时让开发人员专注于他们的代码。我们期待更多的公司参与 Grafeas 和 Kritis 项目。”(在 Shopify 的博文中了解更多。)

**大规模治理的挑战**

保护现代软件供应链对于各种规模的组织来说都是一项艰巨的任务，以下几个趋势加剧了这一任务:

*   **不断增长、支离破碎的工具集**:随着组织规模和范围的增长，它倾向于使用更多的开发语言和工具，这使得维护其开发生命周期的可见性和控制变得困难。
*   **开源软件的采用**:虽然开源软件提高了开发人员的工作效率，但也使审计和管理变得复杂。
*   **分散化和持续交付**:分散化工程和持续交付软件的趋势(例如，“推进绿色”)加快了开发速度，但是使得遵循最佳实践和标准变得困难。
*   **混合云**
*   **微服务架构**:随着组织将大型系统分解为基于容器的微服务，跟踪所有部分变得更加困难。

因此，组织会生成大量的元数据，这些元数据来自不同的供应商，格式各异，并且存储在许多不同的位置。没有统一的元数据模式或集中的事实来源，首席信息官们很难管理和保护他们的软件供应链，更不用说回答诸如“软件组件 X 现在部署了吗？”"是否所有部署到生产的组件都通过了要求的符合性测试？"以及“漏洞 Y 会影响任何生产代码吗？”

**格拉夫阿斯接近**

Grafeas 为组织保护其软件供应链所需的关键元数据提供了一个集中的结构化知识库。它反映了 Google 在构建跨越数百万个版本和数十亿个容器的内部安全和治理解决方案时学到的最佳实践。其中包括:

*   **使用不可变的基础设施**(例如，容器)建立针对持续高级威胁的预防性安全态势
*   **基于全面的组件元数据和安全证明，在软件供应链中构建安全控制**，以保护生产部署
*   **保持系统的灵活性**并确保开发者工具围绕通用规范和开源软件的互操作性

Grafeas 的设计是为了帮助组织在现代软件开发环境中应用这些最佳实践，使用了以下特性和设计要点:

*   **全面覆盖:** Grafeas 根据软件组件的唯一标识符存储结构化元数据(例如，容器图像摘要)，因此您不必将它与组件的注册表放在一起，因此它可以存储来自许多不同存储库的组件的元数据。
*   **混合云友好的**:正如您可以使用 JFrog Artifactory 作为跨混合云部署的中央通用组件存储库一样，您也可以使用 Grafeas API 作为中央通用元数据存储库。
*   **Pluggable** : Grafeas 可以轻松添加新的元数据生产者和消费者(例如，如果您决定添加或更改安全扫描器，添加新的构建系统等。)
*   **结构化**:通用元数据类型(例如，漏洞、构建、证明和包索引元数据)的结构化元数据模式允许您添加新的元数据类型和提供者，依赖 Grafeas 的工具可以立即理解这些新的来源。
*   **强大的访问控制** : Grafeas 允许您仔细控制多个元数据生产者和消费者的访问。
*   **丰富的查询能力**:使用 Grafeas，您可以轻松地查询所有组件的所有元数据，因此您不必解析每个组件的单一报告。

**整理和集中元数据**

在软件供应链的每个阶段(编码、构建、测试、部署和操作)，不同的工具生成关于各种软件组件的元数据。示例包括开发人员的身份、代码的检入和构建时间、检测到的漏洞、通过或未通过的测试等等。这些元数据然后被 Grafeas 捕获。请参见下图，了解 Grafeas 如何为软件开发、测试和运营团队以及首席信息官提供可见性的用例。

![](img/8419519a75ea31b1c6987745691a8fa0.png)

为了给出这种元数据的全面、统一的视图，我们构建了 Grafeas 来促进跨供应商的协作和兼容性；我们将它作为开源软件发布，并与整个生态系统的贡献者合作，进一步开发该平台:

*   **JFrog** 正在 JFrog Xray API 中实现 Grafeas，并将支持混合云工作流，这些工作流需要在一个环境中(例如，在 Xray 中的内部)将元数据用于其他地方(例如，在 Google 云平台上)。在 JFrog 的博客上阅读更多内容。
*   **Red Hat** 计划在 OpenShift 和 Grafeas 中增强 Red Hat Enterprise Linux 容器技术的安全特性和自动化。阅读更多关于红帽的博客。
*   IBM 计划将 Grafeas 和 Kristis 作为 IBM Cloud 上的 IBM 容器服务的一部分，并将我们的漏洞顾问和 DevOps 工具与 Grafeas API 集成。阅读 IBM 博客上的更多内容。
*   **黑鸭**正在与 Google 合作实现 Grafeas 的 Google artifact metadata API 实现，为 **[Google 容器注册表](https://cloud.google.com/container-registry/)** 和 **[Google 容器引擎](https://cloud.google.com/container-engine/)** 带来企业级开源安全。在黑鸭的博客上了解更多。
*   **Twistlock** 将与 Grafeas 集成，将详细的漏洞和合规性数据直接发布到编排工具中，让客户对其容器操作有更多的了解和信心。在 Twistlock 的博客上阅读更多内容。
*   **Aqua Security** 将与 Grafeas 集成，以发布漏洞和违规，并基于组件元数据信息实施运行时安全策略。阅读更多关于[阿卡的博客](https://blog.aquasec.com/governance-and-control-for-the-container-supply-chain-using-aqua-security-and-google-grafeas)。
*   **CoreOS** 正在探索 Grafeas 与其企业 Kubernetes 平台之间的集成，使其能够扩展其图像安全扫描和应用程序生命周期治理能力。

已经有几个贡献者正在计划本季度的 Grafeas 发布和集成:

*   JFrog 的 Grafeas API 的 x 射线实现
*   Grafeas 的 Google 工件元数据 API 实现，以及 Google 容器注册表漏洞扫描
*   JFrog Xray 和 Google 工件元数据 API 之间的双向元数据同步
*   Black Duck 与 Grafeas 和 Google 工件元数据 API 的集成

在这一势头的基础上，我们预计 2018 年初 Grafeas 项目将收到大量其他捐款。

加入我们吧！

我们构建和部署软件的方式正在发生根本性的变化。如果规模化的组织想要获得容器、微服务、开源和混合云的好处，他们需要一个强大的治理层来支撑他们的软件开发流程。以下是您可以了解更多并为项目做出贡献的一些方法:

*   注册参加 JFrog-Google 网络研讨会
*   现在就试试 Grafeas，加入 GitHub 项目:[https://github.com/grafeas](https://github.com/grafeas)
*   参加 10 月 17 日在多伦多举行的[谷歌云峰会和 12 月在 T2](https://cloudplatformonline.com/summit-toronto-2017-schedule.html)举行的【KubeCon】上的 Shopify 讲座
*   填写[此表格](https://docs.google.com/forms/d/e/1FAIpQLSdr8kDTkAkml5f9TW_kzz06C0s0QuV_sWYzHC7NM90F5CZ2bQ/viewform)以了解更多关于即将发布的版本或与我们谈论集成
*   [注册](https://groups.google.com/forum/#!forum/grafeas-users)加入 Grafeas 讨论组， [【邮件保护】](/cdn-cgi/l/email-protection#d0b7a2b1b6b5b1a3fda5a3b5a2a390b7bfbfb7bcb5b7a2bfa5a0a3feb3bfbd)
*   参见 [grafeas.io](http://grafeas.io/) 获取文档和示例

我们希望你能加入我们！