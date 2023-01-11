# Cloudflare 中断愤怒|更多 FAA 5G 愚蠢

> 原文：<https://devops.com/cloudflare-outage-outrage-yet-more-faa-5g-stupidity/>

欢迎来到[![](img/aaa2b944c95aeff25eb4baacc6c045b8.png)](https://devops.com/tag/the-long-view/)*——在这里我们细读本周新闻，并将其剥离至要点。让我们弄清楚**什么是真正重要的**。*

*本周:Cloudflare 遭受了又一次大规模停电，而 FAA 和 FCC *仍然*在机场附近的 5G/NR 上存在分歧。*

 *## 1.又是一周——又一次 Cloudflare 故障

本周首先:这“仅仅”是一个小时，但当如此多的服务依赖于 Cloudflare 的基础设施时，你知道将会有哀号和咬牙切齿。

### 分析:如果不是 DNS，就是*总是* BGP

验尸报告出来了。从一个旨在提高其客户可用性的服务来看，这也令人尴尬。您的运营团队能学到什么？

[马尼什·辛格](https://techcrunch.com/2022/06/20/cloudflare-outage-knocks-popular-services-offline/ "read the full text") : **Cloudflare 修复了导致热门服务离线的中断**

Cloudflare 周二表示，它解决了当天早些时候发生的“大范围”中断，影响了大量服务，包括 FTX、Discord、Omegle、DoorDash、Crunchyroll、NordVPN 和 Feedly。在用户开始面临访问一些热门网站(包括 Zerodha、Medium、[The] Register、Groww、Buffer、iSpirt、Upstox 和 Social Blade)的问题后，互联网基础设施公司解决了这个问题。根据 DownDetector 的数据，用户还表示，他们很难使用比特币基地、Shopify 和英雄联盟。[Cloudflare]上周在世界上的一些地方也面临类似的中断。

Cloudflare 的 Tom Strickx 和 Jeremy Hartman 坦白— **[Cloudflare 停运](https://blog.cloudflare.com/cloudflare-outage-on-june-21-2022/ "read the full text")** :

Cloudflare 遭遇了一次中断，影响了我们 19 个数据中心的流量。不幸的是，这 19 个地点处理了我们全球流量的很大一部分。这次停机是由一个长期项目中的一项变更引起的…将我们所有最繁忙的位置转换为一个更灵活、更有弹性的架构…称为多色彩 PoP (MCP)。
…
在对我们的[BGP]前缀广告政策进行变更时，术语的重新排序导致我们撤销了前缀的一个重要子集。由于这种撤出，[我们]在到达受影响的地点以恢复有问题的变更时遇到了更多的困难。…尽管这些位置仅占我们总网络的 4%,但中断影响了总请求的 50%。…[它]还导致我们的内部负载平衡系统…停止工作。…这意味着我们较小的计算集群…接收的流量与我们最大的集群相同，导致较小的集群过载。
……
在这起令人痛心的事件中，我们显然没有达到客户的期望。…我们已经确定了几个需要改进的领域，并将继续努力发现任何其他差距…以确保这种情况不会再次发生。

T2 认为，这是整个行业的系统性问题:

在这个时代，大多数网络设备的默认管理方式是疯狂的。[它]是每个网络管理员在经历了惨痛的教训后都必须定制实现的东西。
…
我曾亲眼目睹管理员更改路由，任何错误都会切断他们与所管理设备的联系，并阻止他们回滚，这与这里发生的情况非常相似。…许多设备仍然依赖于“不保存”配置，通过电源循环回滚到以前保存的状态。这是将小停电变成大停电的好方法。

玻璃房子里的人等。下面是[的掌声 314](https://forums.theregister.com/forum/all/2022/06/21/cloudflare_oops/#c_4480738 "read the full text") :

把这些事情做好很难。…这一事件再次提醒我们，在堆栈的每个级别上*都会发生弹性。*

* * *

## 2.5G:新无线电，旧规则

早在一月份，我就告诉过你关于 FTC 和 FAA 在机场附近的 5G/NR 塔休战的最后一分钟的小插曲。你可能还记得，联邦航空局和航空公司担心 5G band 77 和安装在**老式飞机**上的雷达高度计之间的干扰。

### 分析:FCC 失去耐心

波段 77 和高度计分配的频率之间没有重叠——事实上，两者之间有一个丰富的“保护波段”。联邦通信委员会的论点是，遭受干扰的高度计一开始就没有正确设计，所以再推迟 5G 的推出是不合理的。因此，美国联邦航空局现在要求航空公司安装过滤器，以减轻干扰风险。联邦航空局希望这项工作在今年年底前完成。

[乔恩·戈尔德](https://www.networkworld.com/article/3664828/telecom-companies-faa-strike-deal-on-5g-interference-for-airplanes.html "read the full text") : **电信公司，美国联邦航空局就 5G 干扰达成协议**

老飞机的新设备是主要电信公司和美国联邦航空局(FAA)之间持续争端的最新进展，监管机构同意采取进一步措施，旨在降低 5G 带来的感知安全风险。…无线电高度计系统使用的频率是着陆飞机的一个重要安全功能，接近某些种类的 5G 使用的频率。
…
一项交易…概述了对运营商的新要求…为他们的飞机增加无线电频率滤波器，并设定了 2022 年底的最后期限。…电信公司一直在通过降低 5G 接入点的传输功率来减轻潜在的干扰。……新政将使缓解持续到 2022 年底。
…
然而，航空业对该交易的条款并不感兴趣…称替换高度计设备缺乏技术细节和监管批准。

国际航空运输协会 SVP 运营、安全和安保部的 Nick Careen 告诉 [Robert Silk](https://www.travelweekly.com/Travel-News/Airline-News/5G-near-airports-rollout-draws-IATA-criticism "read the full text") 他对此不以为然:

国际航空运输协会的卡伦说，目前还不清楚飞机制造商是否能在截止日期前提供所有需要的高度计过滤器。“联邦航空局声称在这个日期上有共识，但事实并非如此。…我现在愿意打赌…我们将会看到大规模的中断。”他提醒人们注意法国的规则。他说，法国的缓冲区比美国电话电报公司和威瑞森同意的临时让步大 4.8 倍。此外，法国要求天线向下倾斜，同时将机场附近的传输功率限制在美国电信公司广播功率的一半以下。

但乔恩·布罗德金看不出这有什么大惊小怪的——**[高度计修复将让 AT & T 和威瑞森在 C 波段频谱](https://arstechnica.com/tech-policy/2022/06/faa-details-plan-to-fix-airplane-altimeters-that-cant-filter-out-5g-signals/ "read the full text")** 上全面部署 5G:

联邦通信委员会在 2020 年 2 月批准了 C 波段的移动使用，具体是从 3.7 到 3.98 GHz。由于飞机高度计依赖于 4.2 GHz 至 4.4 GHz 的频谱，因此留下了 220 MHz 的保护频带来保护高度计。今年实际上是 400 MHz，因为美国电话电报公司和威瑞森尚未部署 3.8 GHz 以上的频率。
…
FCC 发现，考虑到 FCC 要求的保护频带大小和功率限制，“在合理的情况下”不太可能发生对高度计的有害干扰。…联邦通信委员会还敦促航空业进行更多的研究…“鉴于设计良好的设备通常不应受到任何重大干扰。”…航空业的缓慢…可能会导致新的接收器法规，类似于已经要求无线设备只能在其许可频率内传输的规则。

我们是如何陷入这种困境的？ [drinkypoo](https://tech.slashdot.org/comments.pl?sid=21578418&cid=62641658 "read the full text") 补充观点:

我们有关于频率分配的规则，特别是为了避免这样的问题。设计这些高度计的工程师和在设计上签字的经理是这里的过错方。他们为了利益，合作制造了一个未来问题。在当时，频率分配可以被转售用于其他目的，这是法律的一部分。良好的工程设计会考虑监管环境。…这些设备[还不至于]老到在频率分配之前就存在了。

Butbutbutbut …这是*安全关键！*这种说法与 [dooferorg](https://arstechnica.com/tech-policy/2022/06/faa-details-plan-to-fix-airplane-altimeters-that-cant-filter-out-5g-signals/?comments=1&post=41012966#comment-41012966 "read the full text") 的说法不一致:

航空公司和飞机制造商很懒。认真地，忘掉你自己。如果这些东西如此“安全关键”，那么从一开始就应该设计得更好。

* * *

## 这个故事的寓意:
**看起来像一朵无辜的花，但在它下面是一条蛇**

*你一直在读[里奇·詹宁斯](https://www.richi.uk/)的*远景*。你可以通过 [@RiCHi](https://twitter.com/richi) 或者 [【邮箱保护】](/cdn-cgi/l/email-protection#f98d958fb98b909a9190d79a96d78c92c68a8c9b939c9a8dc4d4adb5afd4) 联系他。*

图像:[表面](https://unsplash.com/photos/AnzxhCjE1v0)(通过[去飞溅](https://unsplash.com/license "Some rights reserved")；平整和裁剪)*