# IBM 借助 IBM Cloud 上的 Red Hat OpenShift 4.3 提高安全性和生产力

> 原文：<https://devops.com/ibm-boosts-security-and-productivity-with-red-hat-openshift-4-3-on-ibm-cloud/>

随着越来越多的企业转向云计算，他们需要能够在公共云、私有云以及内部环境中轻松安全地部署和管理其关键工作负载的方法。当面临支持远程工作人员的持续需求时，这一点尤为重要。

IBM 公共云是在开源创新、安全领先和企业级基础设施的基础上重建的，这使得客户可以更轻松地快速开发新的应用程序，并降低管理团队和技术的复杂性。这也是我们的公共云成为 [企业运行其最复杂工作负载](https://newsroom.ibm.com/2019-10-22-Aegean-Airlines-BNP-Paribas-Elaw-Tecnologia-SA-and-Home-Trust-Select-IBM-Cloud-for-Mission-Critical-Workloads) 的首选目的地的原因。

今天，随着 OpenShift 4.3 的推出，我们通过宣布对 IBM Cloud 上的 [Red Hat OpenShift 的增强而更进一步——我们是第一家提供此功能的主要云提供商。这项工作是由 IBM 和 Red Hat 联合设计和支持的。](https://www.ibm.com/cloud/openshift)

最值得一提的是，对于我们的客户，我们增加了独特的安全性和生产力功能，旨在帮助消除在更新、扩展、保护和配置等持续维护上花费的大量时间。我们正在提供应对意外使用量激增所需的弹性，以及针对导致违规或停机以及潜在生产力损失的攻击的保护。现在，开发团队可以将更多精力放在重要的事情上——加速云原生应用程序的开发，从而推动新的、有竞争力的功能。

借助这种完全云管理的产品，集群的主服务器受到 IBM Cloud 独特的架构、配置和工具的保护。以下是旨在帮助节省时间、减少停机和提高安全性的技术优势。

**通过自动恢复保护您的主人**
我们正在自动恢复，这样您就不会在客户支持和其他任务上浪费时间，否则您可能不得不自己完成这些任务(如战略、人员配备、存储)。)
通过持续备份 etcd，我们最大限度地降低了在主服务器完全中断的情况下数据丢失的威胁。默认情况下，主服务器高度可用，您可以通过添加多区域集群来进一步保护主服务器免受单个数据中心故障的影响。因此，如果一个数据中心停机，对可用性没有影响，因为 IBM Cloud 运行一个主动-主动-主动主服务器。
**带内置保护的完全管理员访问**
只有 IBM Cloud 上的 Red Hat OpenShift 提供集群管理员访问，而没有管理员能够关闭主服务器的风险。IBM Cloud 上 Red Hat OpenShift 的主节点与工作节点在物理上是网络隔离的。因此，不能从集群内的任何工作节点访问主节点( [网络图](https://cloud.ibm.com/docs/openshift?topic=openshift-service-arch) )。

有了这一新功能，您不再需要将恢复作为唯一可行的宕机解决方案，而且您的访问也不会像使用其他产品时那样受到限制。这意味着更好的控制访问和更简单的集群管理。

**通过自动扩展主服务器**
提高工作效率 IBM Cloud 上的 Red Hat OpenShift 在多区域地区为自动扩展主服务器提供了业界领先的 99.99% SLA 。这意味着您的工作负载可以快速扩展，而无需担心容量问题。您还可以 [自动缩放您的工人](https://cloud.ibm.com/docs/openshift?topic=openshift-ca) 以满足您的应用程序的容量需求。
例如，在交付大型功能的热潮中，管理员可能会忽略手动扩展主组件，如果没有这一新功能，您将没有 SLA，并且您的管理员将面临随着您的增长扩展主组件的问题，这将导致生产力的巨大损失。
IBM 自动化了工作人员管理和供应，以帮助确保您将工作负载与适当的资源相匹配。
其他供应商可能会限制您提供更多节点类型和风格的能力，因此您无法轻松地自动化用户获取资源的方式和时间。现在，您可以轻松混合节点类型和风格，以实际匹配需要混合数据、计算和服务的工作负载。

主机及其组件(计算、网络和存储)由 IBM 站点可靠性工程师(SREs)持续监控。他们应用最新的安全标准来检测和补救恶意活动，并努力帮助确保 IBM Cloud 上的 Red Hat OpenShift 的可靠性和可用性。此外，他们还遵循互联网安全中心(CIS)发布的 Kubernetes 主基准中的相关网络安全实践。回顾一下 IBM 在安全方面的职责。
在 OpenShift 安全性和合规性方面，没有其他云供应商能像 IBM 那样为您提供如此多的帮助，其中包括 PCI、HIPAA、inquid k、SOC1 和 SOC2 Type 2 的杂务。
这些优势源自我们为客户解决的常见企业用例:安全性、弹性和工作效率。在 IBM Cloud 上的 Red Hat OpenShift 中，我们利用了多年来运行 Kubernetes 所获得的经验，现在已经有 20，000 多个集群投入生产。

此外，借助 OpenShift 4.3，用户可以访问以下 [新功能](https://docs.openshift.com/container-platform/4.3/welcome/index.html) 即服务:
运营商:专注于应用开发，对部署到 OpenShift 中的工具进行自动更新和健康检查
功能:基于事件的工作负载的无服务器应用开发
服务网格:分布式组件化应用的微服务管理
增强的安全性:内置认证、审计和秘密管理

IBM Developer advocation Program 还分享了他们对 IBM Cloud 上的 Red Hat OpenShift 的改进的看法。你可以在这里查看博客。

此外，为了支持今天的发布并加强 IBM 对推动开源创新的持续承诺，IBM Research 推出了两个基于容器的开源项目，这两个项目将实现代码和数据的机密性。你可以在这里阅读更多关于加密容器图像和可信服务身份的信息。

今天就开始:
如果您有任何问题或意见，请通过 Slack 联系我们的团队。可以 [在这里](https://cloud.ibm.com/kubernetes/slack) 注册，在[https://IBM-cloud-success 上的#openshift 频道加入讨论。<wbr>slack.com。
了解关于 IBM Cloud 上的](https://ibm-container-service.slack.com/) [Red Hat OpenShift 的更多信息](https://www.ibm.com/cloud/openshift)
在 IBM Cloud 上的 Red Hat OpenShift 4.3 上查看免费集群进行 [快速试驾](https://developer.ibm.com/edge/dte/) 或进行 [教程](https://cloud.ibm.com/docs/openshift?topic=openshift-tutorials-ov)