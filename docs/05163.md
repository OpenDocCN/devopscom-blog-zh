# CNCF 推进耶格分布式追踪项目

> 原文：<https://devops.com/cncf-advances-jaeger-distributed-tracing-project/>

开源的 Jaeger 分布式追踪平台已经正式进入由云计算本地计算基金会(CNCF)管理的顶级项目。

Jaeger 设计用于任何 DevOps 环境中，是一个用于跨复杂分布式计算环境监控事务的工具。它包括一个用于跟踪收集和分析的后端，以及多个以各种语言实现 OpenTracing 应用程序编程接口(API)的客户端库。

由优步开发的 Jaeger 现在集成了 OpenTracing、OpenTelemetry、Envoy 和 Prometheus 等工具，以便在复杂的 it 环境中更容易发现影响交易的问题的根本原因。例如，DevOps 团队可以应用数据挖掘技术和机器学习算法来分析来自特定集群的数据。

从事 Jaeger 项目的优步软件工程师 Yuri Shkuro 表示，组织可能会依赖 Prometheus 等工具来监控环境，但一旦发现问题，通常需要 Jaeger 等工具来确定问题的根本原因。他说，这种方法的主要原因是分布式跟踪工具如果连续运行，将会存储大量的数据。

已经在生产环境中使用 Jaeger 的组织包括 GrafanaLabs、Northwestern Mutual、SeatGeek、Symantec、Ticketmaster、优步、Weaveworks 和 Zenly。

Jaeger 也开始与其他平台捆绑，如[Red Hat open shift Service Mesh](https://containerjournal.com/topics/container-management/red-hat-makes-service-mesh-play/)。随着这一趋势的继续，越来越多的组织可能会将 Jaeger 作为调试各种问题的工具。

Shkuro 说，虽然最初开发 Jaeger 是为了解决与微服务相关的内在复杂性，但它也可以应用于单片应用程序。他指出，虽然许多这些单片应用程序最终可能会被解构为一组微服务，但其中许多应用程序不会很快消失。

Jaeger 现在有来自四家公司的 15 名活跃的维护者，超过 1200 名贡献者和 375 名提交和拉取请求的作者。它还拥有超过 9000 颗 GitHub 星星，并被从 Docker Hub 中拉出超过 1000 万次。

虽然分布式跟踪作为一个概念已经存在了一段时间，但微服务的兴起正迫使 IT 团队寻找能够进行更深入取证的工具。微服务之间的依赖性加上容器的短暂性，常常使 it 组织难以发现间歇性问题的根本原因。在采用 Kubernetes 运行这些容器的 IT 环境中，使用 Kubernetes 模板、操作员软件和舵图等工具部署 Jaeger 也变得更加容易。

随着开发人员对应用程序的责任越来越大，对可编程取证工具的兴趣也在增加。开发人员曾经认为性能问题应该由不知名的 IT 运营人员来解决，现在开发人员可以更快地解决这些问题。因此，现在应用程序体验已经得到改善，开发人员正在寻找像 Jaeger 这样的工具来识别阻止他们专注于编写额外代码的问题。考虑到 IT 漫长而艰难的历史，很多 IT 领导都想知道为什么他们花了这么长时间才弄明白。

— [迈克·维扎德](https://devops.com/author/mike-vizard/)