# Twistlock 引入了混合云服务发现，并扩展了 Istio、Kubernetes 和无服务器功能支持

> 原文：<https://devops.com/twistlock-introduces-hybrid-cloud-service-discovery-and-expands-istio-kubernetes-and-serverless-functions-support/>

*此外，Twistlock 的第 15 版扩展了 Prometheus 的监控功能，以及 PagerDuty、AWS Security Hub 和 IBM Security Advisor 的警报功能*

俄勒冈州波特兰，2018 年 12 月 10 日—[twist lock](https://www.twistlock.com/)，容器和云原生安全的领导者，今天宣布发布 Twistlock 18.11。这一重大更新现在使客户能够轻松发现云本机服务，以防范混合环境中的威胁，并了解潜在漏洞如何相互联系。它还为 Kubernetes 引入了安全可视化，为 Istio 引入了业界首创的合规性和安全配置检查，并包括与 PagerDuty、Amazon Web Services (AWS)安全中心和 IBM Security Advisor 的新警报集成。

451 Research 的安全分析师 Fernando Montenegro 表示:“虽然生产工作负载对 Kubernetes 和云原生技术的采用呈指数级增长，但安全性和合规性仍是大规模生产部署的主要障碍。“Twistlock 已经显示出云提供商、ISV 和开源工具推动云原生运动的势头。我们相信，在未来的一年里，我们将看到对容器和云原生应用安全性的重视程度超过以往任何时候。”

跨混合云环境发现和保护服务

Twistlock 18.11 引入了云平台合规性，允许客户集中发现跨 AWS、微软 Azure 和谷歌云平台(GCP)、跨所有账户和每个地区使用的所有云原生服务。云平台合规性持续监控这些帐户，以检测何时添加流氓服务，并提醒最终用户避免流氓部署、废弃环境和不受 Twistlock 保护的环境带来的风险。

Istio 服务网格的符合性和安全性配置检查

Istio 提供负载平衡、细粒度流量路由、相互 TLS 和以服务为中心的 RBAC，但缺乏一种简单的方法来可视化和理解服务之间的互连性。Twistlock 现在与 Istio 集成，以丰富雷达仪表板，提供与 Istio 服务网格一起使用的协议和服务角色的详细信息，并为 Istio 引入了一套业界首创的合规性和安全配置检查。这增加了 Twistlock 对 Docker、Kubernetes 和 Linux 的 300 项单独合规性检查，并使客户能够实施安全的 Istio 配置，并覆盖关键风险，如配置错误的 TLS 设置和通用范围的服务角色。

Kubernetes 服务帐户监控和可视化

Twistlock 现在包括了第一个针对 Kubernetes 服务帐户的发现和监控工具。通过集成到 Radar dashboard 中，可以轻松查看与集群中每个资源相关联的每个服务帐户，因此安全人员可以轻松了解角色配置、评估为每个服务帐户提供的访问级别，并降低与过于宽泛的权限相关的风险。对于每个帐户，Twistlock 显示详细的元数据，描述它可以访问的资源以及对每个资源的访问级别。

扭锁 18.11 的其他改进包括:

*   新的监控和警报提供商:客户可以使用 Prometheus 进行监控，基于 Twistlock 数据构建高级的、类似仪表板的统计数据。新的警报提供者包括 PagerDuty、通用 webhooks、AWS Security Hub、IBM Security Advisor 和登录到 stdout。

*   扩展对 Pivotal 的支持:Pivotal 客户现在可以通过 Pivotal Cloud Foundry (PCF)上的 Pivotal 应用程序服务保护应用程序免受威胁，只需单击 Pivotal 网络中的一个图标即可。

*   仪表板 UX 改进:Twistlock 的自动生成雷达视图现在是该产品的主界面。此集中视图可让您一目了然地了解客户整个云原生环境的应用程序拓扑、风险和合规性状态

*   改进的凭据管理器集中的产品级凭据管理器可以轻松安全地存储和重用外部服务的帐户和密钥。