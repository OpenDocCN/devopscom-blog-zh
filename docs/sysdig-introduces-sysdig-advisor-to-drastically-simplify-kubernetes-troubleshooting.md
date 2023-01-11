# Sysdig 引入了 Sysdig Advisor，大大简化了 Kubernetes 的故障排除

> 原文：<https://devops.com/sysdig-introduces-sysdig-advisor-to-drastically-simplify-kubernetes-troubleshooting/>

*单一性能和事件视图将 Kubernetes 故障排除速度提高了 10 倍*

**西班牙巴伦西亚(KubeCon + CloudNativeCon Europe)，2022 年 5 月 16 日—** 统一容器和云安全领导者 Sysdig 宣布推出 Sysdig Advisor，这是一项 Kubernetes 故障排除功能，可整合并优先考虑[Sysdig Monitor](https://sysdig.com/products/monitor/)中的相关性能细节。通过提供性能和事件信息的单一视图，Sysdig Advisor 使运营、开发人员和现场可靠性工程(SRE)团队能够更快地解决问题，同时减少所需的工具数量。

**视频** *:实时、* [*观看有无*Sysdig*Advisor*](https://youtu.be/FEVs051I1iE)*同一个问题的故障排除。*

Kubernetes 的复杂性——包括无数的组件和变量——使得调试问题和确定行动的优先次序变得极其困难。知道如何调试，从哪里开始，或者寻找什么是一个挑战。运营团队和 sre 经常被迫打开命令行界面，并运行 kubectl 等工具来检查情况并寻找根本原因。由于基于 Kubernetes 的应用程序中有如此多的移动部件，修复可能需要数小时或更长时间，从而降低可用性并影响最终用户体验。

只需点击一个按钮，Sysdig Advisor 就会显示所有相关的容量、事件、警报和故障排除信息。因为这些信息是在 Kubernetes 对象的上下文中呈现的，所以用户可以在查找性能问题的来源时快速地深入。Sysdig Advisor 显示问题的优先列表和相关的实时日志，以发现最大的问题领域，并加快问题的解决。

**Sysdig****顾问的主要优势**

*   **将故障排除速度提高 10 倍** : Sysdig Advisor 会生成一个按优先顺序排列的问题列表，让管理员能够了解应该首先解决哪些问题。与传统方法相比，借助 Sysdig Advisor，团队解决 Kubernetes 问题的速度提高了 10 倍，因为它减少了查找关键信息所需的时间，包括集群、命名空间、工作负载和单元的容量、利用率、事件和警报数据。
*   **减少故障排除资源数量:** Sysdig Advisor 减少了对排除 Kubernetes 环境故障所需的博客、仪表盘、日志和命令行输出的并行比较的依赖。简单的用户界面在一个统一的工具中展现了所有重要的细节，并提供了一组精心策划的、可操作的补救步骤。
*   **在不增加安全风险的情况下增加故障排除权限:** 安全团队通常关心提供对命令行工具的广泛访问，例如 kubect l 。Sysdig Advisor 为整个组织的用户提供了对相同级别信息的快速访问，而没有过分的限制。

Kubernetes 很复杂，有无数的组成部分和变量，很难理解什么时候、为什么以及如何出错。Sysdig 的创始人兼首席技术官洛里斯·德吉奥安尼说:“任何 SRE 都知道在对警报进行故障排除时，费力通过多种工具并让多个团队参与的痛苦。”“现在有了 Sysdig Advisor，他们可以高效地调试问题，并重新开始部署新版本。”

**Sysdig 方法**

Sysdig 正在推动统一云和容器安全的标准，因此开发人员和安全团队可以放心地保护容器、Kubernetes 和云服务。Sysdig 提供了两种产品，Sysdig Secure 和 Sysdig Monitor，Sysdig 平台架构支撑着这两种产品。Sysdig Monitor 提供完全开源的 Prometheus 兼容的云和 Kubernetes 监控。借助 Sysdig Secure，团队可以发现软件漏洞并确定其优先级，检测和应对威胁，以及管理云配置、权限和合规性。Sysdig 提供了从源头到运行的单一风险视图，没有盲点，没有猜测，没有黑箱。

**可用性**

Sysdig 监控用户现在可以免费使用 Sysdig Advisor。其他故障排除功能将在未来几周内推出。

**资源**

*   博客:[【Kubernetes】有了 Sysdig Advisor](https://sysdig.com/blog/kubernetes-troubleshooting-advisor) ，故障排除变得简单多了。
*   视频: [用 Sysdig](https://youtu.be/FEVs051I1iE) 加速 Kubernetes 故障排除。
*   阅读更多关于[crash loop back off](https://sysdig.com/blog/debug-kubernetes-crashloopbackoff/)。
*   了解更多关于 [Kubernetes 故障排除](https://sysdig.com/resources/webinars/crashloopbackoff-four-other-k8s-troubleshooting-tips-everyone-should-know/) 。

**关于 Sysdig** Sysdig 正在推动云和容器安全的标准。该公司通过创建 Falco 和 Sysdig 作为开源标准和 Sysdig 平台的关键构建模块，开创了云原生运行时威胁检测和响应的先河。借助该平台，团队可以发现软件漏洞并确定其优先级，检测和应对威胁，以及管理云配置、权限和合规性。从容器和 Kubernetes 到云服务，团队从源头到运行获得单一的风险视图，没有盲点，没有猜测，没有黑盒。全球最大、最具创新性的公司都依赖 Sysdig。

**媒体联系** 阿曼达·麦金尼·史密斯 [【电子邮件保护】](/cdn-cgi/l/email-protection#1c7d717d72787d326f717568745c6f656f78757b327f7371) 703-473-4051