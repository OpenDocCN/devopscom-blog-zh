# 十字路口的云铸造厂

> 原文：<https://devops.com/cloud-foundry-at-the-crossroads/>

在构建 Cloud Foundry 平台即服务(PaaS)环境时，唯一可用的基础架构抽象形式包括虚拟机。时至今日，已经存在多个抽象层，其中一些可能不需要内置到 Cloud Foundry 中的功能。

Cloud Foundry Foundation (CFF)现在正试图通过致力于与 Kubernetes 和开放容器倡议(OCI)等技术的互操作性来应对所有这些变化。Cloud Foundry 开发了自己的容器格式(Garden)和相关的容器编排软件(Diego)。目前，CFF 致力于继续支持这些技术，同时也提供与 OCI，Kubernetes，容器网络接口(CNI)和特使，一个开源服务代理的互操作性，CFF 执行董事 Abby Kearns 说。

CFF 还率先开发了一个开放的 Service Broker 应用编程接口(API ),该接口迅速被 Cloud Foundry 和 Kubernetes 社区所接受，并开始评估其他开源项目，如 Istio，这是一个由 Kubernetes 社区成员开发的负载平衡微服务框架。

很明显，所有这些互操作性是更紧密集成的第一步。毕竟，像云计算原生计算基金会(CNCF)和 Linux 基金会这样的财团投入到 Kubernetes 和 OCI 的技术资源之多，让 CFF 自己可能能够匹敌的任何东西都相形见绌。

事实上，对 CFF 来说，真正的机会可能是建立 Cloud Foundry 平台，提供 Kubernetes 上最好的应用程序体验。Red Hat is 已经通过将 Red Hat OpenShift PaaS 与 Kubernetes 紧密集成在一起，打下了基础。到目前为止，CFF 所能做的最好的事情就是认证一个由 SUSE 创建的可以封装在 Docker 容器中的 Cloud Foundry 发行版。

自然，让 Pivotal Software、IBM、SAP 和其他公司领导的 CFF 财团及时就战略技术方向达成一致是一项挑战。例如，在决定将 Red Hat OpenShift 与 Kubernetes 整合之前，Red Hat 不必与公司外部的任何人进行磋商。然而，到目前为止，很明显，这不再是 Cloud Foundry 是否会与 Kubernetes 集成的问题，而是集成到什么程度的问题。CFF 去年创建了一个 Cloud Foundry 容器运行时环境，IT 组织可以在其上部署应用程序，作为原生运行时的替代方案。

在未来，区分 Cloud Foundry 和其他形式的抽象之间的界限开始和结束可能会更加困难，或者，就此而言，它将部署在什么平台上。Kearns 指出，已经有了 Cloud Foundry 的裸机实例，因此已经有了在没有虚拟机管理程序的情况下部署它的先例。

然而，无论采用何种底层技术，只要开发人员享受云铸造体验，开源 PaaS 环境将在未来许多年内继续存在的可能性就很大。

— [迈克·维扎德](https://devops.com/author/mike-vizard/)