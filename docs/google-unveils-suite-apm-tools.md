# 谷歌推出 APM 工具套件

> 原文：<https://devops.com/google-unveils-suite-apm-tools/>

谷歌今天宣布，它正在提供应用性能管理(APM)工具，该工具基于它用来管理其内部 it 环境的相同技术。

谷歌的产品经理 Morgan McLean 说, [Stackdriver APM](https://cloudplatform.googleblog.com/2018/03/introducing-Stackdriver-APM-and-Stackdriver-Profiler-Distributed-tracing-debugging-and-profiling-for-your-performance-sensitive-applications.html) 是基于谷歌最初为其 DevOps 团队开发的开源 Stackdriver 跟踪和调试器工具。

APM 产品(beta 版)还包括 Stackdriver Profiler，这是 Google 开发的一个工具，用于帮助 DevOps 团队探索他们的代码如何在生产环境中运行。

谷歌还表示，它已经将 Stackdriver Debugger 与 GitHub Enterprise 和 GitLab 集成在一起，以增加开发者可以用来创建代码镜像的存储库数量。

DevOps 团队可以选择在内部或公共云上部署 Google APM 工具。

McLean 指出，Stackdriver Profile 使 DevOps 团队能够发现和修复问题，并最终降低成本，而不是在性能问题上投入额外的计算资源。为了最小化 Stackdriver Profile 对生产应用程序性能的影响，Google 选择使用统计方法来创建一段代码的概要。具体来说，Stackdriver Profiler 通过在应用程序的每个实例中运行的基于轻量级采样的工具来收集数据。例如，显示 CPU 时间、墙时间、使用的 RAM 和争用的数据会显示在火焰图上。

谷歌 APM 工具包的核心是该公司开发的 Stackdriver 跟踪软件，用于收集分布式计算环境中部署的应用程序的延迟数据。McLean 说，在微服务时代，管理现代分布式应用程序而不具备任何工具化能力是不可行的。然而，对于许多 IT 组织来说，购买 APM 软件或采用云服务的成本迫使他们将 APM 技术的使用仅限于最关键的应用程序。

谷歌正试图消除成本这一重要的 APM 因素，这最终将导致部署在谷歌云平台(GCP)上的应用程序变得更加强大和可靠。Google APM 工具可以应用于虚拟机和容器上运行的应用程序，以及 Google AppEngine，这是 Google 在其云服务上发布的一个框架，用于开发和托管应用程序。实际上，谷歌让组织更容易使用开源工具，而以前 it 运营部门不得不自己拼凑这些工具。

依赖 APM 工具是任何开发运维流程的核心。但是 DevOps 过程并没有被普遍采用，主要是因为除了获得新的工具，组织必须发展他们的过程和文化。他们中的许多人所进行的辩论归结为一个争论，即他们是否需要在改变那些过程之前购买工具，或者改变他们的过程来证明购买工具的合理性。大多数情况下，是少数开发人员的主动性导致了这个问题。只有当团队成功时，高级管理人员才开始考虑在组织的其余部分复制该团队采用的 DevOps 过程。通过 Stackdriver APM，Google 显然希望加快向 DevOps 过渡的速度。

— [迈克·维扎德](https://devops.com/author/mike-vizard/)