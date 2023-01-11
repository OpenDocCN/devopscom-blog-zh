# SPIFFE/SPIRE 简介

> 原文：<https://devops.com/introduction-to-spiffe-spire/>

长期以来，人们一直通过密码或密码管理器登录他们使用的应用程序。市场上的许多开放标准和身份提供商继续改进用户通过网站和应用程序进行身份验证和授权的方式。问题是软件服务也存在同样的问题——当应用程序与应用程序对话时，我们如何证明服务到服务连接的可信度？

进入 [SPIFFE](https://github.com/spiffe/spiffe) 和[尖顶](https://github.com/spiffe/spire)。SPIFFE 是实现工作负载身份的规范，SPIRE 是在实践中实现这个规范的代码。这些项目共同创建了一种标准化、安全的方法来识别软件服务并对其进行认证。SPIFFE 和 SPIRE 最近获得了云原生计算基金会(CNCF)的[毕业资格](https://www.cncf.io/announcements/2022/09/20/spiffe-and-spire-projects-graduate-from-cloud-native-computing-foundation-incubator/)，巩固了项目作为顶级开源标准机制的成熟度，为云原生和传统工作负载提供加密运行时身份。

SPIFFE 和 SPIRE 已经在许多大型公共部署中使用。然而，并不是所有的开发人员都熟悉它们的复杂性。下面，我将看看这两个项目，以及它们是如何运作的，以提供更多的背景信息。我还与 SPIFFE/SPIRE 维护者 Evan Gilman 进行了交谈，以收集关于项目历史及其未来目标的更多见解。

## 什么是 SPIFFE？

[![](img/9f649577001c697a81dc90e5dd5fc6ca.png)](https://containerjournal.com/wp-content/uploads/2022/10/spiffe-logo.png) 面向所有人的安全生产身份框架( [SPIFFE](https://spiffe.io/) )是工作负载身份的规范。根据吉尔曼的说法，最简单的方法就是把斯皮夫当成护照。类似于如何向人们发放带有条形码和标准信息的通用形状的护照，SPIFFE 规定了证明和验证服务身份的标准方法。他补充道，这就像把“登录谷歌”的体验带到了软件服务本身。

SPIFFE 中有三个关键组件。首先，SPIFFE 规定服务应该用所谓的 SPIFFE ID 来标识自己，sp iffe ID 被定义为一个格式为`spiffe://trust-domain-name/path`的 URI。这些 ID 然后被编码成可验证的身份文件或 SVID。SVIDs 本身并不是一种文档类型，相反，它们支持 X.509 或 JWT 文档类型。最后但同样重要的是，SPIFFE 指定了一个工作负载 API 来发布和循环这些 SVIDs，以及验证它们所需的密钥。

## 什么是尖顶？

SPIRE 是实现 SPIFFE 规范的代码——你可以把它看作一个生产就绪的 SPIFFE 运行时环境。SPIRE 是“旗舰 SPIFFE 实现”，是 SPIFFE 的真正端到端实例化，它安全地发布 svid、更新 svid 并执行证明等功能。吉尔曼说，如果 SPIFFE 定义了什么是护照，那么 SPIRE 就是签发护照的机构。

SPIRE 代理运行在一个节点上，并公开工作负载 API，该 API 与每个工作负载挂钩。由 SPIFFE 文档定义的工作负载[可以是 web 服务器、MySQL 数据库的实例、工作程序或由独立部署的系统组成的 web 应用程序。通过以这种方式通信，SPIFFE/SPIRE 可以解决“秘密零”的问题，这是指向新发现的系统证明第一个凭证的难题。](https://spiffe.io/docs/latest/spiffe-about/spiffe-concepts/#spiffe-id)

## 关于 SPIFFE/SPIRE 的更多背景

Kubernetes 的联合创始人 Joe Beda 在 2016 年的 GlueCon 上首次提出了 SPIFFE。当时，谷歌正在考虑它拥有哪些可能对更广泛的行业有所帮助的内部技术。据说启发 SPIFFE/SPIRE 的技术可以追溯到 AT & T 和贝尔实验室带给谷歌的安全和身份子系统。

如今，SPIFFE/SPIRE 被许多组织积极维护，我们继续看到令人印象深刻的生产用例。“SPIRE 在一些非常大的案例中使用，”吉尔曼解释道。SPIFFE/SPIRE 在 GitHub、网飞、Pinterest、Square、Transferwise、优步和许多其他大型科技公司中都有应用。在所有权方面，吉尔曼表示，SPIRE 最多被平台工程师、基础设施工程师或安全工程师使用，这取决于组织的角色。

## SPIFFE 和 SPIRE 的未来展望

SPIFFE/SPIRE 似乎拥有保持稳定实现的资源和支持，因此这两个项目的前景看起来都很光明。在新功能方面，2022 年年中，与 SPIRE 的一流集成被合并到 [Istio 服务网格](https://blog.spiffe.io/hardening-istio-security-with-spire-d2f4f98f7a63)中，作为对 Istio 内置 SPIFFE 实现的更灵活的替代。另一个最近的更新是在[窗口](https://blog.spiffe.io/spire-now-runs-on-windows-7e4c7933210b)上对 SPIRE 的实验性支持。关于未来的计划，SPIFFE/SPIRE 维护者可能会继续通过频繁的更新来迭代地改进规范和实现。