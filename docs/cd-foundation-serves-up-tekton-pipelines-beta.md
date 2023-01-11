# CD 基金会服务于 Tekton 管道测试版

> 原文：<https://devops.com/cd-foundation-serves-up-tekton-pipelines-beta/>

在持续交付(CD)基金会的支持下，负责监督开源 Tekton 管道开发的团队今天宣布[该项目目前处于测试阶段](https://cd.foundation/blog/2020/04/09/tekton-beta-available-now/)。

谷歌软件工程师兼 Tekton 项目负责人 Christie Wilson 表示，Tekton 管道不一定是大多数 DevOps 团队会直接与之交互的工具。相反，它们提供了一个构建 DevOps 平台的基础，这将使 DevOps 团队更容易构建跨多个持续集成/持续交付(CI/CD)平台的工作流。

因此，Tekton 管道不仅在促进互操作性方面，而且在减轻对被锁定在特定 CI/CD 平台上的担忧方面，都应该发挥关键作用。

Tekton Pipelines 的 beta 版意义重大，因为它标志着该项目现在足够稳定，可以集成到 DevOps 平台中，并且从现在开始，在支持以前的版本方面，将遵循与 Kubernetes 相同的弃用政策。然而，Wilson 指出，Tekton 触发器、Tekton Dashboard、Tekton Pipelines CLI 和其他组件仍然是 alpha 版本，因此可能会从一个版本发展到另一个版本，但不一定向后兼容。

与此同时，Tekton Pipeline 团队鼓励所有 Tekton 项目和用户将其集成迁移到最新版本的自定义资源定义(CRD)，这是提供的应用程序编程接口(API)。Tekton Pipeline 团队还提供了一份迁移指南。

Tekton Pipelines 项目是在 CD Foundation 的指导下推进的几个项目之一，CD Foundation 是 Linux 基金会的一个分支。其他项目包括 Jenkins 和 Jenkins X，这是一对由 CloudBees 和 Spinnaker 开发的开源 CI/CD 项目，Spinnaker 是由网飞创建的 CD 平台。Tekton Pipelines 是一个原生运行在 Kubernetes 上的框架，可以追溯到 Google。

CD 基金会的主要成员包括 CloudBees、Google、Circle CI、JFrog、IBM、CapitalOne、Salesforce 和网飞。CD 基金会的其他成员包括 GitLab、Red Hat、Harness 和 Rancher Labs。

威尔逊说，詹金斯 X 已经支持 Tekton 管道，而涉及 Spinnaker 的工作正在进行中。威尔逊说，预计目前使用最广泛的 CI/CD 平台 Jenkins 将无法使用 Tekton 管道。

尚不清楚 Tekton 管道何时会在多个 CI/CD 平台上广泛使用。理论上，随着更多的应用程序建立在 Kubernetes 之上，在 Kubernetes 上本地运行的 CI/CD 平台的使用应该会增加。然而，大多数已经采用 CI/CD 平台(如 Jenkins)的组织仍在继续使用相同的平台来构建和部署整体式和基于微服务的应用程序。然而，在某个时候，预计这些组织最终会迁移到在 Kubernetes 上本地运行的 CI/CD 平台。Wilson 说，在许多情况下，同一组织内的不同团队可能会选择在不同的 CI/CD 平台上实现标准化，同时仍然能够共享工作流。

自然地，DevOps 平台的提供商已经在争夺位置，因为由 CD 基金会指定的支持 Tekton 管道的竞赛已经正式开始。

— [迈克·维扎德](https://devops.com/author/mike-vizard/)