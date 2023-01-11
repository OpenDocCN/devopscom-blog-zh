# 为什么服务网格是安全工具

> 原文：<https://devops.com/why-service-meshes-are-security-tools/>

服务网格是否言过其实，或者它们解决了企业 IT 系统的一个真正难题？服务网格是一项相对较新的技术，许多人发现将它们归入预定义的工具类别是一项挑战。这是因为服务网格有各种各样的功能，从负载平衡到[保护流量](https://devops.com/service-meshes-improving-security-delivery-and-availability/)。但是服务网格不仅仅是通过 mTLS 保护您的流量，它们对于您的企业来说是非常重要的安全工具。

服务网格帮助组织改善其安全状况，通过加密和访问控制主动预防攻击，并在安全事件发生时提供对异常行为的可见性。服务网格是对组织安全工具的有力补充，对于保护既有云原生组件又有遗留组件的应用程序尤其重要。

在过去，当涉及到网络安全时，控制网络的边界被认为是“足够好的”。这有两个问题:首先，即使在遗留系统中，通过防火墙也不是很难，一旦进入，攻击者就可以访问整个系统。同样重要的是，这种方法根本不适用于分布式的云原生应用程序，这些应用程序甚至没有明确的边界需要保护。服务网格可以加强对虚拟网络内部流量的控制，因此即使恶意行为者进入，也更容易检测到其存在，并且可以限制损害的程度。

## 服务网格和安全性

这就是为什么服务网格应该被视为安全工具，以及它们如何保护现代企业应用程序的原因。

### 对通信的集中控制

现代工程组织需要给个体开发者自由选择他们在应用中使用什么组件，以及如何管理他们自己的工作流。同时，企业需要确保有一致的方法来管理应用程序的所有部分如何在应用程序内部以及与外部依赖关系进行通信。

服务网格提供了服务之间的统一接口。因为它是作为边车附加的，充当服务网格中每个组件的微数据平面，所以它可以为服务之间的通信添加加密和访问控制，即使该服务本身不支持这两者。

同样重要的是，服务网格可以集中配置和控制。个人开发者不必设置加密或配置访问控制；安全团队可以建立组织范围的安全策略，并通过服务网格自动实施这些策略。

开发人员可以使用他们需要的任何组件，并且不会因为安全考虑而变慢。安全团队可以确保加密和访问控制得到适当配置，完全不依赖于开发人员。

### 跨环境微分段

控制对基础架构不同部分的访问的能力是任何组织的安全态势的关键部分。但是在大多数现代企业中，每个业务部门都将有应用程序在内部和云中运行——可能在多个云中运行。

有了一个不可知的服务网格来桥接环境，组织可以以一种仍然为用户创建无缝体验的方式来划分网络，并且不会变得太复杂而使安全团队无法有效管理。

在每个细分市场中，服务网格可用于创建基于属性的访问控制(ABAC)、基于角色的访问控制(RBAC)，甚至是下一代访问控制(NGAC)。服务网格允许组织非常精细地调整这种访问控制，包括在单个网段内部和跨不同的部署环境。

### 详细遥测

除了提供一致的加密和访问控制之外，服务网格还可以提供组织识别潜在安全事件并对异常做出适当响应所需的遥测技术。

因为所有流量都通过服务网格，所以网格能够收集和显示有关网络流量的粒度信息。这包括跟踪通过网格发送的每个请求的来源和目的地的能力，这对于安全性和通过合规性审核都很重要。

通过连接传统环境和云原生环境的服务网格，可以获得整个系统的详细流量信息。安全团队可以使用单个控制面板来查看流量如何在系统中移动，并在流量从一个环境移动到另一个环境时将信号与用户、IP 地址和内容关联起来。将所有信息放在一个位置可以降低通信在不同环境之间移动时的错误沟通或错误关联的风险，从而掩盖真正的安全风险或不必要地发出危险信号。

### 一致的跨环境安全态势

大多数现代企业都拥有混合/多云 IT 系统，包括数据中心中的传统单体、私有云中的云原生基础架构以及至少在一个公共云中运行的工作负载。所有这些基础架构选择都有合理的业务原因，但组织需要对所有这些基础架构采取强大、一致的安全态势。服务网格技术允许组织连接系统中的所有服务、应用程序和组件，无论环境如何，并确保加密、访问控制和流量可见性扩展到整个系统。

## 结论

向您的安全工具包添加服务网格是确保整个异构系统的一致性和合规性的一种方式，无论您拥有什么样的环境和部署架构。最终，您的安全状况取决于您最脆弱的部署。服务网格是确保基础设施的每个部分都符合内部安全策略的最佳方式。