# Cosmonic 推出用于构建 Wasm 应用的 PaaS

> 原文：<https://devops.com/cosmonic-unveils-paas-for-building-wasm-applications/>

Cosmonic 今天在 [KubeCon + CloudNativeCon 北美](https://events.linuxfoundation.org/kubecon-cloudnativecon-north-america/)大会上发布了[一个平台即服务(PaaS)环境](https://www.prnewswire.com/news-releases/cosmonics-webassembly-paas-removes-complexity-from-large-scale-cloud-and-edge-deployments-preview-now-open-to-developers-everywhere-301655208.html)，用于使用 Web 组装构建云原生应用。

Cosmonic PaaS 基于开源 wasmCloud 分布式计算环境，该环境目前在云本地计算基金会(CNCF)的支持下得到发展，它为开发人员提供了一个轻量级环境，可以更简单地快速构建可以在任何地方运行的应用程序。

Cosmonic 首席执行官 Liam Randall 表示，PaaS 使开发人员能够通过抽象层提供数据库和其他非功能性服务来实现这一目标，这种抽象层消除了开发人员自己提供这些资源的需要。

Cosmonic PaaS 旨在部署在任何云服务或内部 IT 环境中，它还允许开发人员通过组合资源创建星座来定义自己的笔记本电脑、云资源或整个数据中心。Cosmonic 还使开发人员能够通过向 Cosmonic 提供的服务添加客户托管的组件来构建超级星座。

Wasm 最初是在万维网联盟(W3C)的支持下开发的，用于构建浏览器应用程序，它是一种可移植的二进制指令格式，用于构建描述内存安全的沙盒执行环境的软件。Cosmonic 创建了 wasmCloud 项目，以提供一个开放源代码的应用程序运行时，该运行时托管编写为 Wasm 模块的组件，然后可以松散地连接这些组件来构建应用程序。据 Cosmonic 报道，wasmCloud 社区现在有 100 多名成员。

Cosmonic PaaS 扩展了 wasmCloud 提供的功能，因此开发人员现在可以通过 Cosmonic 定义的抽象层更轻松地构建 Wasm 应用程序。这些应用程序也比使用以前的软件构件构建的应用程序更安全，因为所有 Wasm 代码都在无状态和反应式沙箱中执行，从而防止恶意软件从一个软件组件转移到另一个软件组件。

Wasm 成为构建应用程序的首选产品可能还需要一段时间，但很明显，将一个 It 平台与另一个平台分隔开来的墙即将倒塌。每一种早期的构建应用程序的格式都将开发人员锁定在一个特定的平台上。Wasm 是第一个允许应用程序在任何平台上运行的软件产品，包括 Linux 和 Windows，不需要任何修改。

一旦应用程序变得更加可移植，编写一次应用程序，然后将其部署到任何地方的长期目标可能最终会实现。同样重要的是，这些应用程序将在内存安全的沙箱中运行，这比在传统 IT 平台中运行的沙箱更加安全。事实上，随着越来越多的组织审查其[软件供应链](https://devops.com/?s=software+supply+chain)的安全性，他们可能会决定加速采用 Wasm 来构建更安全的应用程序。

显然，Wasm 对 DevOps 团队具有重大意义，Randall 说 Cosmonic 正在努力将其 PaaS 与多个持续集成/持续交付(CI/CD)平台集成在一起。

尚不清楚 Wasm 将多快推动向另一个计算时代的过渡，但在下一个云原生计算时代如何管理它的影响可能是深远的。开发人员愿意多快接受另一个软件产品来构建和部署应用程序还有待观察。显而易见的是，有越来越多的平台将使更容易接受 Wasm 成为可能。