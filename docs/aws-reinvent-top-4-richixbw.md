# AWS re:Invent——我们本周学到的 4 件大事

> 原文：<https://devops.com/aws-reinvent-top-4-richixbw/>

欢迎来到[![](img/209b5cd0a4d4da216206f2a69faa2a5e.png)](https://devops.com/tag/the-long-view/)*——在这里我们细读本周新闻，并将其剥离至要点。让我们弄清楚**什么是真正重要的**。*

*本周，从亚马逊网络服务的 *re:Invent 2022* 发布会上引起我注意的四件事:SnapStart 涡轮增压 Lambda、Graviton3E ARM HPC SoC、AWS 继续招聘以及 AWS 的起源故事。*

 *## 1.Lambda SnapStart 加速 FaaS

本周第一个话题:Java 函数慢得可笑，你不知道吗？SnapStart 旨在改变这种情况，通过缓存引导运行时所需的大量重复启动。

[Steef-Jan Wiggers](https://www.infoq.com/news/2022/12/aws-lambda-snapstart-accelerate/ "read the full text"):**AWS Lambda SnapStart 加速 Java 函数**

**`Cached snapshots`**AWS 宣布了对… Lambda 的更新，增加了 SnapStart 特性，减少了 Java 函数的冷启动。据该公司称，有时启动该功能的运行时间需要长达 10 秒钟。
…
在为函数启用 SnapStart 的情况下，发布函数的新版本将触发优化过程[创建]缓存快照。… AWS 表示，Lambda SnapStart 是同步 API、交互式微服务或数据处理应用的理想选择。…目前，Lambda SnapStart 已在美国东部(俄亥俄州、弗吉尼亚州)、美国西部(俄勒冈州)、亚太地区(新加坡、悉尼、东京)和欧洲(法兰克福、爱尔兰、斯德哥尔摩)推出。

*Java schmava。*那其他运行时呢，[迪帕克·辛格](https://devclass.com/2022/11/30/what-is-the-best-way-to-run-a-container-on-aws-and-will-lambda-snapstart-come-to-other-runtimes/ "read the full text")？

Java 是一个很好的起点……因为 Java 函数的冷启动问题比其他函数更明显。但是 SnapStart 并不是…特定于 Java 的。现在它已经出来了，一旦我们对人们如何使用它有了更好的了解，我们就会发现他们希望我们添加支持的下一个运行时，我们会这样做的。我们希望进入一个不用考虑冷启动的世界。"

* * *

## 2.重力 3E:用于 HPC 的臂

AWS 的“Graviton”ARM 实例又向前迈进了一步，有几个类型针对高性能计算进行了调整。但是引力子 4 在哪里？

[Frederic Lardinois](https://techcrunch.com/2022/11/28/aws-launches-graviton3e-its-new-arm-based-chip-for-hpc-workloads/ "read the full text"):**AWS 发射 Graviton3E**

**`35% better performance`**
在 re:Invent 的传统晚间主题演讲上，AWS[宣布]了其定制的基于 Arm 的 Graviton 芯片的新版本。…这些新芯片显然将支持新的 AWS EC2 实例类型。…所有这些新实例都将利用 AWS 新的 Nitro 5 硬件管理程序，该公司也宣布了这一点。[它]承诺显著改善延迟，性能功耗比提高 40%，PPS 提高 60%。
…
Graviton3E …专为支持高性能计算工作负载而设计。[它]承诺显著提高性能，包括将严重依赖矢量指令的工作负载的性能提高 35%。

道格·布莱克带来了更多的细节:

AWS 表示，其 Hpc7g 实例由新的 AWS Graviton3E 芯片提供支持，与 C6gn 实例相比，浮点性能提高了 2 倍，与 Hpc6a 实例相比，性能提高了 20%。这些实例支持 CFD、天气模拟、基因组学、分子动力学和其他 HPC 工作负载，适用于多达数万个内核的集群。这些实例拥有… 200 Gbps 的弹性光纤适配器(EFA)网络带宽。
…
AWS 表示自推出以来…2013 年，该公司已经开发了多种 AWS 设计的硅，包括…三代 Graviton 芯片。… AWS 使用基于云的电子设计自动化作为 AWS 芯片设计和验证的敏捷开发周期的一部分。

* * *

## 3.招聘冻结？什么招聘冻结？

AWS 表示，它不会停止招聘——不像贝佐斯帝国的其他部分。而且它肯定不会阻止**建造新的数据中心**。

[马特日](https://www.bloomberg.com/news/articles/2022-11-29/amazon-s-cloud-unit-expects-to-keep-expanding-hiring-in-2023 "read the full text") : **亚马逊的云部门计划增加员工**

**`We’re gonna keep building`**
负责监督亚马逊网络服务销售和营销团队的高级副总裁马特·加曼(Matt Garman)表示，他预计他的组织和更广泛的 AWS 业务将在 2023 年增加员工:……“我们的业务仍在快速增长。”公司其他部门的招聘冻结并没有影响其最赚钱业务的投资计划。…“当需求放缓时，我们将放缓数据中心的增长，”Garman 说。…“我们有很多供应链模型告诉我们要继续建设数据中心，所以我们会继续建设。”

让我们置身其中，[托拜厄斯·曼](https://www.theregister.com/2022/11/30/aws_hiring_datacenters/ "read the full text"):

上周，亚马逊宣布将在印度投资 44 亿美元，增设第二个地区。截至本月，该公司在澳大利亚、加拿大、以色列、新西兰和泰国开发了超过 15 个可用区域。该公司还有五个数据中心，价值 120 亿美元，正在俄勒冈州建设中。
…
尽管经济形势不断恶化，AWS 并不是唯一一家继续扩大数据中心规模的云提供商。微软本周表示，将在北卡罗来纳州投资 10 亿美元建设数据中心。…与此同时，谷歌继续向美洲、欧洲、中东和亚太地区的新地区扩张。

## 4.AWS 的早期历史——“由胜利者书写”？

以下是杰夫·科尔文迷人故事的片段:**亚马逊如何将一个尴尬的副业项目发展成 AWS**

**`That decision was the turning point`**… AWS 的崛起不太可能，因此需要一个解释。…这家在线零售商的分支是如何统治利润丰厚的云计算行业的？AWS 最知名的起源故事…不会死，但不是真的。到 2000 年代初，亚马逊……已经从零开始建立了世界上最大的网站之一，但是增加新功能的速度慢得令人沮丧。…团队花了 70%的时间来构建任何项目都需要的基本元素。…每个项目团队都在做同样的苦差事。…公司领导开始思考，“让我们构建一个所有团队都可以依赖的共享基础架构服务层。”亚马逊迫切需要解放其软件开发人员。…各地的开发者*，不仅仅是它自己的开发者，都渴望有新的工具来做这件事。…但这是亚马逊的业务吗？…那个决定是一个转折点。…2006 年 3 月，当 AWS 最终推出其首个服务——S3 时，有 12，000 名开发人员注册。…革命已经开始。*

 *对此，微软的[胡安·何塞·阿莫尔](https://twitter.com/JuanJAmor/status/1598317676874682371 "read the full text")在推特上写道:*

*我喜欢了解成功的商业故事，但这个故事尤其打动我，因为我每天都在与 AWS 竞争。称赞每一个企业家，称赞每一个提出正确问题的人，称赞每一个愿意挑战现状的人，称赞那些相信自己可以塑造未来的人。*

* * *

##  *故事的寓意:**浑浑噩噩的生活不值得过***

**—苏格拉底*

*你一直在读*由[里奇·詹宁斯](https://www.richi.uk/)所著的《长观*。你可以通过 [@RiCHi](https://twitter.com/richi) 或者 [【邮箱保护】](/cdn-cgi/l/email-protection#37435b4177455e545f5e19545819425c084442555d5254430a1a637b611a) 联系他。**

*图片:[马苏德·阿斯拉米](https://unsplash.com/photos/6gJcS68SjcA)(via[Unsplash](https://unsplash.com/license "Some rights reserved")；平整和裁剪)**