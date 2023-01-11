# 您可能已经在软件定义的数据中心进行开发运维了

> 原文：<https://devops.com/might-already-devops-software-defined-data-center/>

我在网上阅读，偶然看到了 EMA(企业管理协会)关于软件定义的数据中心(SDDC)2014 年状况的报告。在仔细阅读了这些数据和亮点之后，我惊讶地(但本不应该)发现了这么多与 DevOps 相关的内容和概念。我也不会对软件定义的网络(SDN)被大量提及感到惊讶。从某种意义上来说，SDDC 包含软件定义的操作和软件定义的网络(可能还有软件定义的存储，但现在考虑*和*还为时过早)。

无论如何，根据该报告，相当大比例的组织(今天)利用软件定义的操作和网络:

> 您的组织利用了以下哪些技术、结构或流程？
> 
> 4.协调存储、网络和服务器资源的调配和管理的跨职能流程(57%)
> 5。服务器管理员配置自己的存储卷的解决方案(56%)
> 6。物理、虚拟和云资源的持续/集中容量管理(55%)
> 9。基于策略的基础设施自动化，无需人工干预即可进行日常调整(50%)
> 10。软件定义网络(虚拟覆盖网络)(48%)
> 11。软件定义网络(控制平面与交付平面分离)(46%)
> 13。供开发人员调配自己的应用环境(服务器、网络和存储)的 API(42%)
> 14。配置管理解决方案(Puppet、Opscode Chef、SaltStack、ServiceMesh 等。) (41%)

更能说明 DevOps 对实现 SDDC 有多重要的是，它不仅强调自动化，还强调流程。当被问及受访者认为“软件定义的数据中心最重要的方面”是什么时，第二和第三个问题集中在应用程序和基础架构的部署和自动化上:

*   用于工作负载部署的软件和基础架构的最佳实践、可重复配置(46%)
*   流程编排和自动化可以轻松地跨孤岛部署应用程序(44%)

如果你不完全相信，那么“运营分析”(在 DevOps land，我们可以称之为“测量”或“指标”)以 42%的受访者排名第四。

报告中还有更多，一些不太相关，但在大多数情况下，阅读这份 SDDC 报告给我留下了明确的 DevOps 后的味道。这是一种薄荷巧克力咖啡的味道，如果你想知道的话。

通常与 DevOps 相关的概念不一定是 DevOps 或 SDN 所特有的。它们通常是更大趋势的一部分，即[将所有东西](http://www.slideshare.net/lmacvittie/operationalize-all-the-network-things)操作化:网络、存储、计算、安全。SDDC 的业务目标与 DevOps 和 SDN 倡导的目标惊人地相似——降低风险、降低运营支出、提高稳定性和加快上市时间。通过创建接口来促进组间可重复的、一致的(和可测量的)移交的协作在 SDDC 和在 DevOps 一样普遍。

关键是，DevOps 实际上可能正以另一个名字的伪装，在你附近或你周围的组织中处于采用过程中。如果你听到有人说软件定义的*什么的*，那就去看看。你可能会惊讶地发现有人用不同的名字从另一扇门溜进了 DevOps。