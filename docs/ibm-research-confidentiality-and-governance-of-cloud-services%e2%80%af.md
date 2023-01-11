# IBM 研究——云服务的保密性和治理

> 原文：<https://devops.com/ibm-research-confidentiality-and-governance-of-cloud-services%e2%80%af/>

我们的团队花了几个月的时间来开发、调整和完善一个复杂的深度神经网络，以对重要的金融、医疗或政府数据进行分类。应用程序已经被容器化、打包，并最终准备好作为公共服务部署在云上，但是有一件事阻碍了它。您如何确保您的商业秘密代码以及它处理的高度敏感的数据能够保持机密和隐私？此外，您如何在高度监管的行业中提供工作负载和数据治理？

隐私、保密和治理问题是 IBM 研究所要解决的中心问题。为了改进容器和云技术的这些方面，我们最近贡献了两个开源项目: ***加密的容器映像*** ，它确保容器映像保持加密和私密，以及 ***可信服务身份*** ，它确保这些映像处理的数据保持安全。

我们将首先介绍这些技术如何实现代码和数据的机密性，然后展示它们如何提供治理。

**保护工作负荷和秘密的机密性**

为了提供高保证，我们希望确保数据和代码都被加密，这分别由加密的容器映像和可信服务身份提供。

**加密的容器映像**通过使用*+加密的*媒体类型扩展 OCI(开放容器倡议)容器映像规范来保护工作负载/代码的机密性，该规范允许开发人员加密容器映像，以便它们只能由授权方(开发人员、集群、机器等)解密。).这确保了工作负载从构建到运行时都是加密的。如果没有合适的密钥，即使在注册表受损的情况下，图像的内容仍然是保密的。

确保工作负载得到加密只是事情的一个方面。每个工作负载都需要访问数据源或其他服务。为了做到这一点，它必须使用密码、API 密钥或证书进行自我认证。如今，这通常是通过 Kubernetes secrets 完成的。Kubernetes 秘密的问题是，一旦它们被存储，它们也将对管理员、云操作员或任何有权访问这个名称空间的人可用。然而，管理员可能只是管理资源的第三方员工，可能没有获得访问数据的认证，或者可能没有安全许可。

**可信服务身份**通过确保只有经过验证的服务能够获得凭证来保护敏感数据访问。这是通过使用工作负载标识来实现的，工作负载标识由各种运行时度量组成，如映像和集群名称、数据中心位置等，以识别应用程序。这些测量由运行在每个托管节点上的服务使用在环境的安全引导期间安装的信任链安全地签名。

**扩展治理:地理围栏执行和基于 Location++的数据政策**

对于高度监管的行业，工作负载和数据的保密性只是冰山一角。通常，需要实施更细粒度的控制。上述技术解决了这些问题。

*   The first type of control is geofencing execution. How do we ensure that this workload is only run in particular clusters or regions? How do we enforce export control or digital rights management? These are natural uses of **Encrypted Container Images**. By only providing the appropriate decryption keys through attestation, authorization and key management, we can create a trust binding between certain clusters/workers and workloads. This will provide assurance of knowing WHERE workloads are running.Another control is to be able to express, enforce and audit data access via location (or other properties) of the workloads, i.e. GDPR. **Trusted Service Identity **provides just that. By exposing the properties of workloads in the definition of policies governing secrets, it provides the ability to create policies such as “*Only workload X (with this image), running in datacenter DAL05, in kube cluster hipaaCluster <wbr>can access medical records in this Cloudant database*“. This method of governance has very fine-grained controls, that might apply to a wide spectrum of use-cases. In addition, the entire audit trail is retained, tracking every interaction and what process received what secret and when.

    这些只是这些技术如何用于增强容器云生态系统中的治理的几个例子。

    **了解更多信息**

    在本文中，我们仅仅触及了探索这些技术的皮毛。如果您想了解这些技术的更多信息。