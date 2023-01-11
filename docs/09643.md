# 军械库扩大了 Spinnaker CD 发行范围

> 原文：<https://devops.com/armory-extends-scope-of-spinnaker-cd-distribution/>

Armory 今天[更新了其开源 Spinnaker 连续交付(CD)平台发行版的自托管版和托管版](https://www.prnewswire.com/news-releases/armorys-new-continuous-deployment-self-hosted-and-managed-2-28-empowers-devops-growth-and-scale-301598802.html)。这些更新支持并发管道，并提供了与开源 Terraform 基础设施即代码(IaC)的更紧密集成，以更好地实施策略。

此前，这两个平台被称为军械库企业和军械库企业管理。他们现在被重新命名；Armory Continuous Deployment Self-Hosted 成为 Armory Continuous Deployment Managed，部分是为了提供与该公司上个月推出的 CD 云服务[的更多区别，该云服务不基于 Spinnaker](https://devops.com/armory-aims-to-turn-continuous-delivery-into-a-service/) 。

Armory 产品副总裁 Adam Frank 表示，该平台增加的其他功能包括为 Spinnaker 平台做出贡献的额外测试工具，以及针对可能影响 Spinnaker 平台的常见漏洞和暴露(CVE)的增强插件和补救功能。

Frank 说，尽管推出了一个不基于 Spinnaker 的声明式 CD-as-a-service 平台，Armory 仍然致力于支持那些喜欢继续依赖开源平台的组织。

经常使用专用光盘平台的组织数量仍然相对较少。虽然组织已经在 CI/CD 平台中采用了持续集成(CI ),但是利用这些平台的 CD 元素已经被证明是具有挑战性的。用于运行应用程序的每个平台都是独一无二的，因此自动化交付一直是个问题。在某些情况下，CI 平台已经使用定制脚本进行了扩展，以自动化应用交付，但这些工作通常不会扩展到整个扩展企业。Frank 指出，例如，许多试图扩展开源 Jenkins CI/CD 平台的组织现在正在寻求更松散地耦合 CI 和 CD 流程，以使 DevOps 工作流不那么脆弱。

当越来越多的组织开始在 [Kubernetes](https://containerjournal.com/?s=Kubernetes) 集群上构建基于微服务的应用程序时，Armory 正在为一个独特的 CD 平台提供理由，这些应用程序公开一组标准的应用程序编程接口(API ),而不管它们部署在什么基础设施上。Frank 指出，在许多情况下，随着应用环境变得越来越复杂，这些组织现在需要并行管理多个管道，而不是依赖于单个管道。

毫无疑问，随着应用程序开发的步伐不断加快，自动化 CD 的需求将成为一个更加紧迫的问题。Frank 说:DevOps 团队正在发布大量较小的应用程序更新，同时还需要能够在遇到意外问题时轻松回滚这些更新。

目前还不清楚有多少组织将采用专用 CD 平台，但是随着应用程序开发的继续发展，许多 DevOps 团队将至少重新审视他们现有的流程。与此同时，也有许多组织刚刚开始他们的 DevOps 之旅。这些组织中的大多数并不致力于一种 CI/CD 方法而不是另一种。

然而，不管采用哪种方法，在[数字业务转型](https://digitalcxo.com)的时代，人们期望组织能够及时交付软件更新。然而，实现这一目标的唯一方法是拥有某种类型的 CD 功能，它能够按照需要像真正的软件公司一样运营的组织所要求的规模可靠地运行。