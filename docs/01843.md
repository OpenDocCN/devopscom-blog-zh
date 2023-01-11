# CNCF 推进云事件规范

> 原文：<https://devops.com/cncf-advances-cloudevents-specification/>

云本地计算基金会(CNCF)今天宣布，用于描述事件数据的开源[Cloud events](https://www.cncf.io/announcement/2019/10/28/serverless-specification-cloudevents-reaches-version-1-0/)规范已经实现了 1.0 版本的里程碑，这预示着未来云互操作性计划的良好前景。

IBM 高级技术人员兼 CNCF 无服务器工作组和 CloudEvents 项目的联合主席 Doug Davis 表示，CloudEvents 不仅可以定义事件的公共属性以促进互操作性，还可以更容易地在 GitHub 等存储库和需要消费这些事件的应用程序或工具之间共享这些属性。

他补充说，有了这个基础，构建跨无服务器和事件驱动架构的工具应该会变得更容易。

CloudEvents 规范的工作始于 2018 年 5 月，是一个沙盒项目。随着 CloudEvents 1.0 的发布，CNCF 技术监督委员会(TOC)现在将 CloudEvents 指定为一个孵化项目。CloudEvents 项目的积极贡献者包括亚马逊网络服务(AWS)、谷歌、微软、IBM、SAP、红帽和 VMware。事实上，CloudEvents 已经被植入 Knative 的 Eventing 框架中，Knative 是由 Google 领导的一个开源中间件项目，旨在将 Kubernetes 与各种无服务器计算框架集成在一起。其他支持 CloudEvents 的平台包括微软 Azure Event Grid、Red Hat EventFlow、Eclipse Vert.x 和 Debezium、SAP Kyma 和 Serverless.com 的 Event Gateway。

Davis 表示，鉴于对 CloudEvents 项目的支持水平，有理由对未来的云互操作性倡议持乐观态度。令人眼花缭乱的应用程序编程接口阻碍了云的互操作性，这些接口通常是专有的。CloudEvents 是少数几个获得所有主要云服务提供商支持的互操作性项目之一。他指出，CloudEvents 在这方面取得的部分成功可以归功于该倡议的有限范围。

组织可能还需要一段时间才能不必担心被锁定在云中。然而，一般来说，他们越关注 Kubernetes 等平台公开的事实规范和应用程序编程接口(API ),就越容易将应用程序从一个平台迁移到另一个平台。在许多情况下，如今的 DevOps 团队通常会努力将可能在公共云上开发的应用程序迁移到内部生产环境中。从长远来看，预计 it 领导者将希望能够通过威胁在云服务提供商之间转移工作负载，从云服务提供商那里获得更低的费率。

与此同时，随着无服务器计算框架等事件驱动的架构继续变得越来越受欢迎，IT 领导者可以对跨这些架构的互操作性不断提高这一事实感到些许安慰。当然，现在说 CloudEvents 规范何时会成为一个完全毕业的 CNCF 项目还为时过早，但很明显，许多云服务提供商在实施它之前不会等待官方的认可。DevOps 团队现在面临的挑战和机遇是找出如何最好地利用这种能力来创建新的应用程序，这在以前是难以尝试的。

— [迈克·维扎德](https://devops.com/author/mike-vizard/)