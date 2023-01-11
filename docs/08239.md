# DevOps 的工程应用(五)

> 原文：<https://devops.com/engineering-applications-for-devops-part-5/>

这个博客系列解释了如何为 DevOps 设计应用程序。

本博客系列涵盖的主题:

决定应用程序是否适合开发运维的因素。DevOps 的工程设计实践。
·devo PS 应用于企业应用和软件服务。
devo PS 应用于 COTS 系统。
·devo PS 应用于制造(嵌入式)系统软件。
应用成熟度的五个层次。

本博客涵盖了应用于制造(嵌入式)系统软件的 DevOps。你可以在这里[阅读](https://devops.com/engineering-applications-for-devops-part-2/)[第一部分，在这里](https://devops.com/engineering-applications-for-devops-part-1/)[第二部分，在这里](https://devops.com/engineering-applications-for-devops-part-3/)阅读[第三部分，在这里](https://devops.com/engineering-applications-for-devops-part-4/)阅读第四部分。

## **应用于制造(嵌入式)系统软件的 DevOps】**

七十年代末(没错，四十年前！)作为一名年轻的工程师，我被分配了一项任务，那就是研究如何加快北方电信公司生产的一种创新型分组交换机 SL-10 的软件开发和交付周期。每个 SL-10“节点”由数百万行原始嵌入式软件源代码和定制硬件组成，这些硬件配置有许多互连的处理器以及与其他节点、主机设备和终端设备接口的协议。

鉴于系统的复杂性和缺乏自动化的构建、测试和部署工具，生成系统的每个版本需要超过 12 个月的时间，而且即使在版本发布后，通常也会有许多错误。在不太了解 DevOps 的情况下(DevOps 这个词直到 29 年后才被发明)，我们开始实施一个连续交付系统，其中包括自动化构建、测试和交付工具以及工作流。

结果是显著的。从发布到生产的交付时间减少了 10 倍以上，从 12 个月减少到 1 个月，而且质量也降低了 10 倍，质量是指客户在每次发布中发现的缺陷。这种性能和能力上的巨大转变使得工程和制造团队有可能加快创新速度并击败竞争对手。SL-10 产品及其更名后的 DPN 版本迅速主导了面向连接的分组交换市场，并成为北电公司和加拿大民族的骄傲。更酷的是，我得到了一个漂亮的总统徽章和晋升，这为我的职业生涯铺平了道路，后来我写了一本书和一系列博客！如果这个现实生活中的例子不足以证明 DevOps 可以应用于制造的嵌入式软件产品，那么我不知道什么是。

有许多其他已发布的示例显示了应用于嵌入式制造系统的 DevOps 实践如何获得类似的优势。一个著名的例子是 2013 年 Gary Gruver 在 *[中发表的《大规模敏捷开发的实用方法:惠普如何转变 LaserJet FutureSmart 固件](https://www.oreilly.com/library/view/a-practical-approach/9780132980982/)* 。

这并不是说应用于制造软件嵌入式系统的 DevOps 与应用于企业应用程序或 COTS 系统的 DevOps 是一样的。CloudBees 博客上发表的一篇论文[Five Aspects that Make Continuous Delivery for Embedded Different](https://www.cloudbees.com/blog/5-aspects-makes-continuous-delivery-embedded-different)，解释了嵌入式系统使用的一些关键 DevOps 实践。

## DevOps 为嵌入式系统带来的优势

DevOps 对于嵌入式系统的优势总结如下:

将传统嵌入式软件系统中常见的庞大代码库改造成 DevOps 模型并不容易。这可能会很昂贵，但几乎可以保证是值得的努力，特别是如果你有一个长期的愿景，并打算让你的产品在未来保持竞争力。嵌入式软件的开发人员需要访问大量的计算机资源，以便在强大的硬件模拟器上测试他们的实时嵌入式代码。
·开发人员和测试人员需要访问物理产品硬件来运行他们的二进制文件，以进行不能单独在模拟器上运行的系统测试。协调真实设备测试拓扑的实验室即服务(LaaS)系统可以改善关键资源的共享。LaaS 系统提供了一个测试框架，可以通过 API 集成到一个连续的交付管道中。
长时间的构建和测试过程可能需要重新设计，以通过扩展构建和测试资源来缩短序列化的交付周期，从而缩短构建时间。
嵌入式系统的长期合规性和一致性测试流程需要通过自动化和资源扩展来加速。
专注于持续交付而非持续部署，在持续部署中，可交付的产品版本经常交付给制造部门进行验证，但向最终客户部署的频率由其他业务因素决定。

## **这意味着什么**

这篇博客是解释如何设计最适合 DevOps 的应用程序的系列文章之一。这个博客系列解释了如何为 DevOps 设计应用程序，包括:

决定应用程序是否适合开发运维的因素。DevOps 的工程设计实践。
·devo PS 应用于企业应用和软件服务。
devo PS 应用于 COTS 系统。
·devo PS 应用于制造(嵌入式)系统软件。
应用成熟度的五个层次。

本博客涵盖了应用于制造(嵌入式)系统软件的 DevOps。你可以在这里[阅读](https://devops.com/engineering-applications-for-devops-part-2/)[第一部分，在这里](https://devops.com/engineering-applications-for-devops-part-1/)[第二部分，在这里](https://devops.com/engineering-applications-for-devops-part-3/)阅读[第三部分，在这里](https://devops.com/engineering-applications-for-devops-part-4/)阅读第四部分。

有关如何开发开发应用的更多信息，请参考我的书[工程开发应用](http://mybook.to/engineeringdevops)。