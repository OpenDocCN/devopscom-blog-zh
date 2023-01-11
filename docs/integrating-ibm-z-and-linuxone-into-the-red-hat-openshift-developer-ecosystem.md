# 将 IBM Z 和 LinuxONE 集成到 Red Hat OpenShift 开发者生态系统中

> 原文：<https://devops.com/integrating-ibm-z-and-linuxone-into-the-red-hat-openshift-developer-ecosystem/>

**总经理威利·特哈达&IBM 认知应用首席开发顾问**

[https://developer . IBM . com/blogs/Willie-te jada-red hat-open shift-ibmz/](https://developer.ibm.com/blogs/willie-tejada-redhat-openshift-ibmz/)

我在 IBM 的角色是确保我们为开发人员提供您需要的工具和资源，以及您喜欢的选择和防护栏，以帮助您将精力完全集中在创新上。安全性是释放云真正价值的关键，我们希望这是您在构建高性能解决方案时不必担心的一件事。为此，本周我们宣布了一个重要的里程碑，进一步加强了 Kubernetes 对 IBM Z 和 IBM LinuxONE 上的 Linux 的支持:[面向 IBM Z 和 LinuxONE 上的 Linux 的 Red Hat OpenShift 容器平台现在已经正式推出](https://www.ibm.com/blogs/systems/red-hat-openshift-now-available-ibm-z-linuxone/)。
Kubernetes 已经可以在 IBM Z 和 LinuxONE 上运行一段时间了，详见[这份 LinuxONE 白皮书](https://developer.ibm.com/blogs/idc-white-paper-ibm-linuxone-openshift-hybrid-cloud/)。这已经使客户能够开始将运行在 IBM Z 和 LinuxONE 上的基于 Kubernetes 的微服务集成到他们的基础设施中，以及围绕 Kubernetes 本身的庞大项目生态系统中。
通过此次发布，开发人员现在可以使用基于 Kubernetes 的工具、快速的内置安全性和硬件驱动的加密技术、高正常运行时间和弹性、快速访问数据以及您对 IBM Z 和 LinuxONE 上的 Linux 所期望的一切来访问平台。这为更轻松地与现有解决方案集成打开了大门，这些解决方案已经在混合和多种云模式中使用 OpenShift 无论您的基础架构是驻留在公共云还是私有云，或者两者的结合。这是我们最新的增强功能，可帮助您真正实现一次构建，随处部署。
此外， [IBM z/OS 云代理](https://www.ibm.com/us-en/marketplace/zos-cloud-broker)允许 OpenShift 应用程序轻松地与 z/OS 上的现有数据和应用程序进行交互。您将能够使用[IBM Cloud infra structure Center](https://www.ibm.com/us-en/marketplace/cloud-infrastructure-center)，这是一个基础设施即服务(IaaS)，它在 IBM Z 和 LinuxONE 上的 Linux 上为基于 z/VM 的 Linux 虚拟机提供简化的基础设施管理。OpenShift 是一个平台即服务(PaaS)和容器即服务(CaaS)层，需要底层 IaaS 层，IBM Cloud Infrastructure Center 为 IBM Z 和 LinuxONE 提供了 IaaS 层。
Z 架构上的 OpenShift 可用性允许更轻松地开发跨您的基础架构工作的应用程序。您开发的基于微服务的工作负载可以按照您认为合适的方式进行管理。此外，借助[IBM Cloud Pak for Applications](https://www.ibm.com/cloud/cloud-pak-for-applications)，您将能够访问一系列工具，通过利用与 DevOps 相关的工具，如 [IBM UrbanCode](https://www.ibm.com/cloud/urbancode) 以及对 Java、Node.js、Spring 和其他运行时环境的企业级支持，来帮助推动现代化工作。在这个版本中，Red Hat Enterprise Linux core OS(RHCOS)第一次可以用于 IBM Z 和 LinuxONE 平台上的 Linux。
我们帮助您构建智能，构建安全。
这个版本主要用于评估、开发和测试，所以我们热切希望大家都来看看。现在就参与进来，开始测试您的工作负载，为今年晚些时候计划的生产就绪做好准备。最初，您将需要 z/VM 在平台上实现 OpenShift，作为由 IBM z/VM 管理的虚拟机，其他选项将在以后推出。我们还致力于支持 HiperSockets、SMC-D、安装程序提供的基础设施(IPI)以及除 NFS 之外的持久存储，您可以期待对所有这些东西的支持。
我邀请您参加我们 3 月 5 日的[网络研讨会](https://event.on24.com/eventRegistration/EventLobbyServlet?target=reg20.jsp&partnerref=blog&eventid=2176040&sessionid=1&key=10580F9362892DE87ABF39472D96D7AB&regTag=&sourcepage=register)，了解 OpenShift 的敏捷性、IBM Z 的安全性和可伸缩性以及 IBM Cloud Paks 的容器化软件如何推动创新。