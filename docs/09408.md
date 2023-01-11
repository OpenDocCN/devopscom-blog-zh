# 基于拉的 Kubernetes 部署迁移到 GitLab 免费层

> 原文：<https://devops.com/pull-based-kubernetes-deployments-moving-to-gitlab-free-tier/>

在即将发布的版本中，GitLab 将在平台的免费层中包括对基于拉的部署的支持，这将在云原生环境中为用户提供更高的灵活性、安全性、可扩展性和自动化。借助基于拉的部署，DevOps 团队可以使用用于 Kubernetes 的 [GitLab 代理](https://cms-blog-posts-2022-05-05-pull-based-kubernetes-deployments-com.about.gitlab-review.app/blog/2020/09/22/introducing-the-gitlab-kubernetes-agent/)来自动识别和实施应用程序变更。

“所有级别的 DevOps 团队都受益于在其云原生环境中利用 GitOps 策略，如基于拉的部署。GitLab 配置组产品经理 Viktor Nagy 表示:“通过在 GitLab 的免费层中提供这一功能，我们可以向更多组织介绍这一安全且可扩展的功能的威力和效用。

作为一家开放核心公司，GitLab 很乐意为 GitOps 社区做出贡献，并支持采用行业最佳实践。

**什么是拉式部署？**

基于拉和基于推的部署是 GitOps 的两种主要方法，GitOps 是一种运营框架，采用了用于应用程序开发的 DevOps 最佳实践，如版本控制、协作、合规性和 [CI/CD](https://cms-blog-posts-2022-05-05-pull-based-kubernetes-deployments-com.about.gitlab-review.app/topics/ci-cd/) 工具，并将它们应用于基础设施自动化。

通过利用自动化和可伸缩性，GitOps 使运营团队能够[像他们的应用程序开发对手](https://cms-blog-posts-2022-05-05-pull-based-kubernetes-deployments-com.about.gitlab-review.app/blog/2021/04/27/gitops-done-3-ways/)一样快速地移动，而不牺牲安全性。

基于推送的部署(即无代理部署)依靠 CI/CD 工具将更改推送至基础架构环境，而基于拉取的部署则使用安装在集群中的代理，在偏离所需配置时拉取更改。在基于拉的方法中，部署目标仅限于 Kubernetes，并且必须在每个 Kubernetes 集群中安装一个代理。

Nagy 说:“只要您的基础设施上的 GitLab agent for Kubernetes 在您的集群中拥有必要的访问权限，您就可以自动配置一切，从而减少 DevOps 的工作量和引入错误的机会。”。

**基于拉的部署与基于推的部署**

基于推的部署和基于拉的部署各有利弊。以下是每种 GitOps 实践的优缺点列表:

基于推送的部署优势:

*   易用性
*   作为 CI/CD 的一部分广为人知
*   更灵活，因为部署目标可以在物理服务器或虚拟容器上，而不限于 Kubernetes 集群

基于推送的部署缺点:

*   要求组织向群集开放防火墙，并授予对外部 CI/CD 的管理员访问权限
*   要求组织在引入新环境时调整其 CI/CD 渠道

基于拉动的部署优势:

*   安全的基础设施–无需打开防火墙或授予外部管理员访问权限
*   无需人工干预即可自动检测和应用更改更容易扩展相同的群集

基于拉动的部署缺点:

*   代理需要安装在仅限于 Kubernetes 的每个集群中

**拉式部署如何影响自由层体验**

在 GitLab 的免费层中包括对基于拉的部署的支持，为较小的组织提供了巨大的竞争优势，因为他们现在可以以安全和可扩展的方式将自动化应用于他们的云原生基础架构，包括虚拟容器和集群。此外，对于试图通过最大限度地减少基础架构生态系统中的工具数量来快速起步的组织，此功能包含在一个 DevOps 平台中，而不是作为单点解决方案。

Nagy 说:“DevOps 团队不必为新的基础设施元素持续编写代码，他们可以在单个 DevOps 平台内编写一次代码，并让代理自动找到、提取和应用代码，以及配置更改。

此外，随着基于拉的部署在这一入门层中的可用性，GitLab 的新用户将能够立即实现应用程序开发的现代化，并降低与配置此类基础架构相关的安全风险。”

*这篇博客文章包含与即将推出的产品、特性和功能相关的信息。值得注意的是，所提供的信息仅供参考。请不要将此信息用于采购或计划目的。与所有项目一样，这篇博文中提到的项目和链接页面可能会更改或延迟。任何产品、特性或功能的开发、发布和时间安排均由 GitLab Inc.* 全权决定