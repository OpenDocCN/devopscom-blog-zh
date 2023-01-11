# JAMstack 板企业

> 原文：<https://devops.com/jamstack-boards-the-enterprise/>

通过 JavaScript、API 和标记设置开发路线。参与。

近年来，JAMstack web 开发趋势引起了前端 web 设计人员的兴趣。Netlify2020 年的一项研究发现，服务一百万用户的网站中，有三分之一使用 JAMstack。

JAMstack 一直被视为博客和创业公司的一种开发风格，但最近，一些支持者认为是企业采用的时候了。那么，JAMstack 和无服务器能给企业架构带来什么好处呢？我最近与 [Stackery](https://www.stackery.io/) 的工程和产品副总裁 [Ryan Coleman](https://www.linkedin.com/in/ryanycoleman) 进行了交谈，以找出答案。

## 定义 JAMstack

首先，什么是 JAMstack？ **JAM** 代表 **J** avaScript， **A** PIs， **M** arkup。这是一种基于现代工具和无服务器网络架构的新型网站和应用程序。在过去五年左右的时间里，我们看到它的采用呈指数级增长。

正如在[jamstack.org](https://jamstack.org/)所定义的，JAMstack 支持快速安全的网站，直接从 CDN 预渲染文件。这避免了客户机和服务器之间的紧耦合，也称为 headless。如果应用在正确的环境中，它可以带来性能、安全性、可伸缩性和开发人员体验方面的好处。

诚然，这种风格的实现有一些变化——PayPal 的 Jamund Ferguson 简单地将它们称为[静态应用](https://www.infoq.com/presentations/jamstack-enterprise/)——但是，“它们的共同点是它们不依赖于网络服务器，”jamstack.org 指出。Jekyll，Hugo，Nuxt，Next 和 Gatsby 都在众多 JAMstack 框架和[静态站点生成器](https://www.staticgen.com/)之列，这里列出了众多采用者[。](https://jamstack.org/examples/)

## JAMstack 优势

IT 团队不再经营网络农场。相反，他们正在将与实时网络服务器交互的过程向左转。根据科尔曼的说法，JAMstack 更符合这些全面的现代实践。因此，他看到了在企业环境中使用它的许多潜在好处。

### 无服务器

使用 JAMstack，网页是在附加到 CDN 管道的构建过程中构建的。科尔曼指出:“你不是在运行一个服务器场，而是在将它外部化。”“是 CDN 的问题。”

JAMstack 很好地适应了无服务器的心态。“JAMstack 有助于重新思考生产足迹的实际情况，”科尔曼说。通过减少活动服务器的占用空间，无服务器实施降低了基础架构成本。

### 安全性

随着[网络漏洞](https://containerjournal.com/topics/container-security/common-container-and-kubernetes-vulnerabilities/)的扩散，公司正在寻找新的方法来限制它们的暴露和[避免灾难性的破坏](https://devops.com/how-devsecops-can-help-avoid-catastrophic-breaches/)。他说，JAMstack 可以帮助企业跟上步伐，提供一个“更紧密的应用安全控制的地方”。

它允许团队将他们的安全基础设施分成更小的部分，这为诸如授权之类的事情提供了更好的控制和可伸缩性。“无服务器架构有助于将基于 SAML 的企业级身份验证绑定到您的堆栈中，”Coleman 指出。

### 民主化效应

科尔曼也看到了小团队利用信息技术瓦解主导者的机会。“公司需要快速行动，实现企业级架构，并在一开始就以较少的投资保护产品，”他说。例如，这些能力可以让一家金融科技初创公司与一家老牌银行在同一个竞技场上竞争。

“你如何创造一个活的建筑，你如何确保它尽可能的安全和干净？”他问。“你如何召集整个团队，而实际上不必使用 1000 条 YAML 线路，我们如何继续维护？”

由于 JAMstack 采用了 API，公司可以快速地将高性能的应用程序缝合在一起。此外，通过将[低代码工具](https://devops.com/7-forces-driving-the-low-code-movement/)和 JAMstack 配对，团队可以非常快速地拖放 AWS 管理的服务片段来构建 web 应用程序。

## 双向互动

JAMstack 以创建引人注目的面向用户的应用程序而闻名。然而，Coleman 承认一个常见的误解:JAMstack 是静态的，因此不适合企业。

但是，JAMstack 可以不仅仅是一个静态的 app 该结构可以支持安全的交互能力。他说，通过采用 cdn 和桶，并利用 API 连接到 AWS 托管服务等丰富的功能，它基本上可以达到与其他开发风格相同的企业级能力。

## JAMstack:不再只针对博客

“无服务器+ JAMstack 是 web 应用架构的发展方向，”科尔曼在最近的一篇博客文章中写道。虽然许多人认为它是一个静态的应用程序，但使用这种开发方法来实现具有动态交互性的应用程序的潜力越来越大。“有了后端的 AWS，你可以创建一个交互式的企业级应用。”

JAMstack 的另一个好处是客户机和服务器之间的解耦特性。这个抽象层有助于构建跨[多云](https://devops.com/3-key-issues-with-hybrid-cloud-transformation/)安排的 web 应用。随着 web APIs 越来越容易通过[低代码](https://devops.com/apis-the-secret-sauce-for-low-code-platforms/)访问，连接到 MySQL 或 Postgres 数据库的门槛——例如处理身份管理——正在降低。

随着 API 和无服务器变得越来越普遍，JAMstack 曾经只被视为对博客有好处，现在它在企业架构中获得了更多的信任，提供了提高性能、加快 web 应用程序交付和解决企业环境中其他问题的潜力。

科尔曼将 JAMstack 描述为使开发人员能够“以您想要的方式构建 web 应用程序”那么，你想怎么建？