# 确保 SD-WAN 和 AIOps 的网络连接

> 原文：<https://devops.com/ensuring-network-connectivity-with-sd-wan-and-aiops/>

最近， [脸书经历了一次](https://engineering.fb.com/2021/10/05/networking-traffic/outage-details/) 的停电。如果公司依赖该应用开展业务，他们的 IT 团队可能会被最终用户的投诉电话淹没。

团队通常会如何回应？他们会深入兔子洞，逐案分析问题，问无数的问题，包括:

*   企业网络会不会有问题？
*   服务提供商是否遇到了问题？
*   是只有少数用户受到影响，还是该问题更具系统性？

传统上，这种手动流程需要大量的知识共享和时间来完成，因为团队会将问题分成更小的部分来三角分析问题的根本原因。

[经常是企业网络遇到连接问题](https://www.techradar.com/news/5-of-the-worlds-biggest-network-outages)——而不是像脸书这样的应用。

一些公司为了利用高度可靠的广域网链路，如 MPLS，来连接到互联网和将分支机构连接到他们的数据中心，付出了高昂的代价。相反，他们可以通过使用可靠性较低的商品链接，如电缆或 DSL，节省一两美元。这两种选择都引入了艰难的权衡 — 还有比这更好的方法来确保企业范围内的连通性吗？

输入 SD-WAN。

SD-WAN 将作为可靠 WAN 链路的相同服务级别协议(SLA)与商用链路的经济性相结合，专门处理电力不足的情况，重新路由链路流量以保持网络连接 — 确保用户能够访问他们的必备应用。

通过将人工智能融入 IT 运营( [AIOps](https://devops.com/?s=AIOps) )，团队可以利用分析的力量从根本上减少他们的响应时间，确保如果问题确实发生，他们可以快速修复。事实上， [90%的 IT 专业人员承认，通过 AIOps 为网络管理提供动力将改善他们公司的业务成果](https://www.networkworld.com/article/3624635/survey-aiops-driven-network-management-can-make-your-business-run-better.html) 。

### 淹没在数据中:了解传统网络问题调查难题

为了确定服务中断的根本原因，团队会花费大量时间评估人们使用的所有不同应用的情况以及他们使用这些应用的链接。这些应用程序可能位于任何地方——迫使团队在庞大的数据堆中寻找针头，以确定哪里出错了。

这些数据正以如此高的速度爆炸，以至于任何人都几乎不可能跟踪所有这些数据 。只有利用像 AIOps 这样的高级分析系统，团队才能获得必要的洞察力来快速解决问题。

### **SD-WAN 和 AIOps:解决问题的梦之队**

SD-WAN 和 AIOps 如何协同工作以实现高度可靠、始终连接的网络？

SD-WAN 可快速解决所有潜在的本地问题，并优化多条 WAN 链路的性能和连接，甚至是可能不可靠的单个 WAN 链路。SD-WAN 还可确保业务关键型应用程序获得正确的优先级，并提供精确的纠错能力，从而尽可能避免 WAN 上的任何问题或中断。

AIOps 在哪里发挥作用？它在更精细的级别上分析全局拓扑中更长时间的数据。它在找什么？一切。它正在研究影响单个应用的新兴模式。它正在全球范围内搜索同时影响多个 SD-WAN 边缘设备的系统问题。它还可以调查边缘或应用程序在特定时间段内如何受到影响。

通过呈现所有这些数据，AIOps 分析的内容比 SD-WAN 多得多。通过从这些数据中获得洞察力，它可以突出影响一切的问题，从单个应用程序的单个用户到影响更广泛用户群的应用程序的系统性问题。在某些情况下，AIOps 可以提示 SD-WAN 自我修复并自动修复问题，然后验证问题是否已修复。因此，最终用户仍然与他们的网络保持连接。

### 在完全采用的 SD-WAN/AIOps 环境中

假设您是一名 IT 管理员，支持一个极其复杂的企业网络，跨越数千个不同的站点，这些站点使用不同的安全服务来连接应用程序。即使你在一个负责监控网络的大型团队中，也几乎不可能完全了解整个网络并在问题发生时解决问题。

通过采用 SD-WAN 和 AIOps，您获得了一种超能力。不，你将不能飞行或隐形，但 AIOps 将使你*无所不知*，使你能够:

*   利用强大的分析能力，在用户投诉之前，即时准确地找到并修复网络故障点——在某些情况下，甚至在用户察觉之前
*   了解哪些网站比其他网站表现得更好，以找出可以改进的地方
*   提出有助于网络自我优化和自我修复的配置更改
*   检测和优化降级链路，提升用户体验

如果出现问题，AIOps 会在全天候监控网络的同时立即向您提供建议，为您提供全面的态势感知和洞察力，在问题出现时解决问题。

### SD-WAN 和 AIOps:通过自我修复保持连接

脸书事件不同寻常，因为它在全球范围内影响了世界用户，他们无法通过任何脸书数据中心访问该应用程序。在这种情况下，AIOps 只需确定应用程序中断并指出根本原因。

但是如果情况有所不同呢？例如，想象一下，如果脸书的美国西海岸数据中心被认为不可用，但其东海岸数据中心仍在运行。通过将 SD-WAN 与 AIOps 相结合，类似受影响的公司可以让执行诊断并确保应用程序连接。

这怎么可能发生呢？

首先，AIOps 会发现问题及其根本原因。它会报告西海岸的用户无法访问该应用程序，但东海岸的用户可以使用。最后，SD-WAN 可以通过将最终用户应用流量重新路由到东部数据中心来保持应用连接，从而实现自我修复。

对于大多数 IT 团队来说，使用传统的手动监控和排除网络故障的方法几乎是不可能的。相反，团队依赖于 SD-WAN 和 AIOps。这种组合能力给团队带来了无与伦比的超能力，使他们能够显著提高整个企业的连通性，并在问题发生时快速做出响应。