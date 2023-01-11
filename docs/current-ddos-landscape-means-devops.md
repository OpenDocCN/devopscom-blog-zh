# 当前的 DDoS 环境对 DevOps 意味着什么

> 原文：<https://devops.com/current-ddos-landscape-means-devops/>

企业、政府、医院、学校、慈善机构甚至个人——对 DDoS 犯罪者来说都是一样的。如果你有一个网站，它很可能在某个时候成为分布式拒绝服务(DDoS)攻击的目标。

DDoS 有可能让你的网站关闭几天，给组织造成严重破坏。它们可能很贵，而且最令人担忧的是，如果你的网站在任何特定场合都不可用，它们可能会损害你的声誉，让用户和客户不再光顾。

众所周知，攻击者会利用网络数据包和所有类型的漏洞，包括编写专用于破坏特定应用程序或服务的自定义代码，使系统过载或完全停止运行。

## 攻击动机

有很多威胁者准备发起 DDoS 攻击。其中一些包括:

*   黑客行动主义者使用 DDoS 来表达他们对企业、政府和个人的不满。
*   网络罪犯依靠预先制作的脚本和工具来关闭网站。一些煽动者只是在寻找一种发泄愤怒或沮丧的方式。一些人可能使用常见的 DDoS 租用网站，而不是从自己的网络运行攻击。
*   勒索网站的敲诈者，以停止(或不执行)DDoS 威胁为交换条件索要钱财。
*   商业竞争对手想方设法将竞争对手排除在重大活动之外(如网络星期一)，或试图完全关闭这些活动。
*   国家资助的威胁行动者参与网络战以压制批评者和反对者。他们也可以攻击市政基础设施来削弱敌对国家。
*   攻击者进行攻击只是因为他们可以，或者没有明显的原因，而不是为了测试他们实施攻击的能力。

## DDoS 类型和趋势

但是 DDoS 事件不仅仅是中断服务。根据“[云安全联盟云计算指南](http://searchcloudsecurity.techtarget.com/feature/CSA-Guide-to-Cloud-Computing)”的说法，黑客还利用它们来窃取信息和感染计算机，以达到各种各样的邪恶目的。

此外，DDoS 攻击在数量和规模上都在快速增长。国际商业时报称，它们已经变得越来越普遍，因为随时可用的工具和廉价的在线服务让任何人都可以针对公司或个人服务器发起攻击。

DDoS 攻击可以分为三种类型，每种类型都有许多(独特的)变种。

**基于容量的攻击**使网站的带宽饱和。基于云的安全和加速提供商 Imperva Incapsula 在 2016 年 2Q 面临了有史以来最大的此类攻击，峰值为 [470 Gbps](https://www.incapsula.com/blog/keep-calm-and-mitigate-470-gbps-ddos-attack.html) 。像许多其他复杂、高速率的攻击一样，攻击者使用小有效载荷来实现高包转发率——这是一种[危险的新战术](https://www.incapsula.com/blog/throughput-forwarding-rate-ddos-attacks.html)，已经变得很常见。

这种攻击的主要目的是通过以许多反 DDoS 设备无法处理的速度发出快速数据包来关闭缓解服务。

**协议攻击**(针对 OSI 第 4 层)消耗防火墙、负载平衡器等服务器资源。网络层攻击的规模、数量和复杂性都在增长。据《公共科学图书馆》报道，那些使用多种媒介的人已经攀升至创纪录的 36.1%。平均而言，该季度每三天就能缓解一次 50+的 Mpps 攻击。

在同一时期，网络层攻击的持续时间增加了，13%的攻击持续了一个多小时。最长的连续坚持了 10 多天。虽然大多数属于肇事逃逸类别——使用针对同一目标的短脉冲发射——但上升趋势表明持续时间超过 6 小时的事件普遍存在。

**应用层攻击**(以第 7 层为目标)由看似合法的 HTTP 请求组成，归因于日益复杂的恶意机器人。来自大量被屏蔽的 IP 地址的持续不断的请求会对 web 服务器、数据库服务器或 web 应用程序的其他元素造成压力，从而使您的 web 应用程序立即停机。

2Q 的 Incapsula 缓解的最大此类事件的峰值为 108，288 RPS(每秒请求数)。最长的跑了 67 天，而 59%的跑了不到 30 分钟。该公司将此归因于“偶然”违规者数量的增加。

## 检查风险

开放 Web 应用安全项目( [OWASP](https://www.owasp.org/index.php/Denial_of_Service) )简要介绍了风险评估:

*   *“…资源不足，需要注意，如果系统架构的设计不能满足流量需求溢出…如果不加检查，[它可能]导致没有实际攻击的 DoS 症状。*
*   *“…也许最大的风险因素不是技术上的…组织应该避免采取可能使自己成为 DoS 攻击目标的行动，除非这样做的好处大于潜在的成本或缓解控制措施已经到位。*
*   “根据[你的]具体环境，还可能存在其他风险因素。”

以上第一条可以适用于任何网站。虽然有人可能认为第二种可能只适用于政治实体，但基于竞争性定价的电子商务网站呢？除非有强有力的 DDoS 防御措施，否则这样的网站在当今竞争异常激烈的数字世界中不会存在太久。

那么，组织可以做些什么来抵御 DDoS 攻击呢？随着攻击变得越来越容易发动且日益复杂，必须及时了解不断变化的威胁形势。

## 保护您的应用

使用应用了最新安全补丁的软件和插件是一个良好的开端。在上线之前，渗透测试是一个强烈推荐的关键步骤。在这里，OWASP 提供了一个完整的[在线指南](https://www.owasp.org/index.php/Testing_for_Denial_of_Service)来帮助你的努力。

OWASP 还提供了几个例子，展示代码漏洞可能被忽略的地方，从用户指定的对象分配到锁定客户帐户。

一旦你的应用上线，监控网站流量以衡量流量和访问者类型有助于确保其可靠性，因为不必要的流量可以被检测到并迅速解决。评估流量摘要是一个开始，接下来的任务包括检查 IP 源地理位置和访问您站点的唯一源 IP。

但是数据分析只是一个开始。SANS Institute 提供了本指南来帮助您了解更多关于成功缓解 DDoS 攻击的信息。

最重要的是，您的运营团队可以创建一个[响应计划](https://lp.incapsula.com/ddos-response-playbook.html)来最小化攻击的影响。一个有效的计划包括为您的客户支持和沟通团队制定的程序，以及让 CxO 高管随时了解情况。

## 选择正确的缓解方案

找到最适合您特定业务需求的缓解策略。规划包括对您的顾虑进行优先级排序，并根据您的安全预算检查各种缓解方案的优势。在这种情况下，使用专业安全服务(及其专业团队)可能比“自己动手”更具成本效益

确保您当前拥有的 DDoS 保护提供所需的可扩展性和安全性，以防止您的站点和服务器在受到攻击时崩溃。

## 关于作者/本·赫尔茨贝格

本·赫尔茨贝格是 T2 imper va 公司 Imperva Incapsula 产品线的安全研究小组经理。Ben 是一名开发人员、黑客和技术经理，对不同的技术非常感兴趣，并专注于信息安全。他喜欢开发以前没有的新东西，或者用不同的方式解决难题。在 [LinkedIn](https://il.linkedin.com/in/sysadmin) 和 [Twitter](https://twitter.com/KernelXSS) 上与他联系。