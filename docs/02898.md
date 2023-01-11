# Redis 实验室引入 RedisGraph 和 Streams 来支持零延迟的未来

> 原文：<https://devops.com/redis-labs-introduces-redisgraph-and-streams-to-support-a-zero-latency-future/>

*Redis Enterprise 巩固了其作为即时经济领先数据库的地位*

[Redis Labs](https://redislabs.com/) ，Redis 的总部和 [Redis Enterprise](https://redislabs.com/redis-enterprise/) 的提供商，今天在伦敦 Redis Day 上宣布了 Redis Enterprise 的最新版本，它具有两个关键功能:RedisGraph 和 Streams。RedisGraph 是一个新的模块，旨在实时解决复杂的实际图形问题。Streams 是一种新的数据结构，支持接收和分析以极快速度生成的大量非结构化数据。这两种功能都支持企业更快地做出决策，并有望为客户加速零延迟应用和服务的到来。

Redis Labs 的 CMO 马尼什·古普塔(Manish Gupta)表示:“有许多新兴环境需要零延迟来实现它们的承诺——自动驾驶汽车、面部识别、智能家居等等。“然而，阻碍这些创新被大众消费者采用的一个关键因素是数据库处理数据的速度。RedisGraph 和 Streams 将帮助公司让他们的应用、设备和系统提供消费者期望的即时体验。”

**介绍世界上最快的图形数据库:RedisGraph**

RedisGraph 构建于 GraphBLAS 之上，这是一个采用线性代数(包括矩阵乘法)的开源库，根据基准测试结果，RedisGraph 完成计算的速度比任何其他图形解决方案快 600 倍。

RedisGraph 的主要功能和使用案例包括:

*   GraphBLAS 的首次应用，通过以前所未有的速度执行计算，专注于解决现实世界的问题，如追踪污染或分析交通流量。
*   旨在使执行基于图形的关键计算变得简单高效，并使企业能够做出决策以快速解决问题。
*   最大限度地减少对专门数据库的需求，以满足不同的使用情形。
*   消除了手动逐步计算的需要，并允许用户存储值，搜索数百万个图节点和边，并同时执行多个计算。
*   示例用例包括跟踪复杂供应链中的污染源，跟踪用户行为以提高推荐引擎的效率，或者同时分析多条道路上的交通流量。

“RedisGraph 是一个非常高效的图形数据库，”Bloor 的高级研究员丹尼尔·霍华德说。“由于它使用的矩阵表示和它实现的线性代数算法，它能够在不到半秒的时间内创建超过 100 万个节点，并在同一时间内形成 300 万个关系。Redis 实验室进行的早期基准测试表明，他们的图形处理时间比竞争对手快几个数量级。”

“我们期待在现有 Redis Enterprise 实施的基础上更进一步。Malwarebytes 的高级工程副总裁 Mark Patton 说:“我们预计 RedisGraph 将在快速检测、高级警告和恶意软件数据探索方面开辟新的可能性。“我们相信 RedisGraph 将加快对威胁缓解和整体安全态势的实时洞察。”

group . PS 的首席执行官兼创始人 Emre Sokullu 表示:“我们已经使用 Redis 十多年了，很高兴看到我们的团队在这方面取得了成功。凭借 Redis 凭借其多租户架构和数据存储的紧凑性所提供的简单性和规模，我们已经能够大幅减少我们的基础架构占用空间。有了对 Cypher 查询语言的支持，从我们现有的 graph 实现到 RedisGraph 的转换变得非常简单。现在，随着我们查询速度的预期提高，我们可以比以往更快地获得我们所依赖的见解。”

支持快速处理和分析的新数据结构:Streams

Streams 是一种新的数据结构，[在开源 Redis 5.0](https://redislabs.com/blog/redis-5-0-is-here/) 中引入，现在可以在最新版本的 Redis Enterprise 中使用。借助流的力量，简单的监控工具可以转变为处理和处理实时生成的数据。例如，婴儿监视器可以从传输婴儿床的实时信息到分析婴儿的实时状态和健康状况，包括在孩子的呼吸或心跳不规则时发出警报。

Streams 的优势和特性包括:

*   实时处理大量以极快速度生成的数据。
*   允许创建队列，以便在不同的应用程序和系统之间共享信息，或者统一来自不同系统的日志。
*   示例用例包括社交媒体反馈的实时情绪分析，处理来自环境和其他周围环境的数据以通知和指导自动驾驶汽车的行动，面部识别技术，机器学习，评估实时事件以发现欺诈或网络攻击，以及支持更好的物联网和智能家居设备。

**附加资源**

有关新 RedisGraph 模块的介绍，请访问[此处](https://redislabs.com/redis-enterprise/redis-modules/redis-enterprise-modules/redisgraph/)并在公司博客上找到一份[绩效基准研究](https://redislabs.com/blog/new-redisgraph-1-0-achieves-600x-faster-performance-graph-databases/)。

此外，可从独立分析公司 Bloor Research 获得关于再贴现的[摘要。](https://redislabs.com/docs/redisgraph-in-brief/)