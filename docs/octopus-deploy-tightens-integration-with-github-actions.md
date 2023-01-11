# Octopus Deploy 加强了与 GitHub 操作的集成

> 原文：<https://devops.com/octopus-deploy-tightens-integration-with-github-actions/>

Octopus Deploy 今天宣布，它已经加强了其自动部署平台和 GitHub Actions 持续集成/持续部署(CI/CD)平台之间的集成。

Octopus Deploy 收入高级副总裁 Harsh Sabikhi 表示，GitHub Actions for Octopus Deploy v2 增加了对 GitHub 添加到其平台的推送-构建-信息-操作功能的支持，使 DevOps 团队能够跟踪提交、构建和问题。该信息现在也与 Octopus Deploy 的 DevOps Insights 工具同步，该工具基于 Google 定义的 DevOps 研究和评估( [DORA](https://devops.com/?s=DORA+metrics) )指标来显示指标。

添加到集成中的其他功能包括支持工作流中的语义版本发布标签、工作摘要和改进的用户界面，使 GitHub 更容易从 Octopus Deploy 中访问。

Sabikhi 表示，虽然 GitHub Actions 提供了一些部署功能，但 Octopus Deploy 创建的自动化平台可以跨多个云和内部 IT 环境自动进行应用发布管理。他补充说，GitHub Actions 针对在 Git 工作流环境中管理 CI 流程进行了优化，该工作流源自 GitHub 管理的云服务。

Sabikhi 指出，与 GitHub Actions 的集成使得跨多个部署平台扩展那些基于 Git 的工作流变得更加简单。

从本质上讲，GitOps 是一种更加固执己见的 DevOps 方法，它依赖于开源 Git 存储库的一个实例作为关于环境的真实信息的单一来源，而不是一组应用程序或服务器配置文件。GitHub 将 GitOps 视为使用 GitHub Actions 平台将代码库扩展到 DevOps 工作流领域的一种方式。

然而，随着组织采用 GitOps，许多组织发现更松散地耦合 CI 和 CD 平台是有利的。集成的 CI/CD 平台已经存在了十多年，但是很少有组织能够使用这些平台真正自动化应用程序的交付。诸如 Octopus Deploy 之类的平台是为专门管理应用程序的部署而从头开始创建的。Sabikhi 说，除了 GitHub Actions，Octopus Deploy 还提供了与多个其他 CI 平台的集成，使 DevOps 团队能够以他们认为最合适的方式混合和匹配 CI 平台。

目前还不清楚有多少 DevOps 团队愿意购买单独的 CD 平台，但随着应用程序在云原生时代的构建和部署变得越来越具有挑战性，许多组织正在重新审视他们用于构建和部署整体应用程序的 DevOps 流程。面临的挑战是，他们中的许多人花费了数年时间来定义基于传统 CI/CD 平台的工作流，因此在采用专用 CD 平台时，需要克服许多现有的惰性。

很明显，使用自动化大部分过程的平台，CD 最终变得更容易实现。每个 DevOps 团队将需要决定他们想要多少员工专门负责管理这些 CD 平台；随着应用程序发布管理变得更加自动化，应用程序的部署速度应该会加快。