# AWS 中断愤怒| Rusty Linux | ARM 最新

> 原文：<https://devops.com/aws-outage-outrage-rusty-linux-arm-latest/>

欢迎来到[](https://devops.com/author/richi/)*——在这里，我们细读本周新闻，并将其剥离至要点。让我们弄清楚**什么才是真正重要的**。*

*本周:亚马逊网络服务(Amazon Web Services)遭遇惨败，Linux 向 Rust 迈出了新的一步，美国联邦贸易委员会(FTC)在可怕的 Arm/Nvidia 交易中又捅了一刀。*

 *## AWS *us-east-1* 打破互联网

本周第一件事:亚马逊网络服务在周二的中断让许多 DevOps 团队手忙脚乱。但是原因是什么呢？

### 分析:DNS DDoS？

虽然我们还没有正式知道，但有一些传言可以推测。会不会是 AWS 的 DNS 基础设施容易受到 **DNS 反射攻击**？

你好。是[戴夫·李](https://www.ft.com/content/6eff4cae-5df7-4746-a068-d4f6a18ba285 "read the full text") : **从愤怒的阿黛尔粉丝到坏掉的机器人吸尘器**

周二早上开始的。机器人吸尘器停止了吸尘，Wi-Fi 摄像头停止了监视，热切的约会对象无法“向右滑动”在亚马逊内部……不可思议的事情发生了:就在圣诞旺季开始到来之际，被困的送货司机无法装载包裹并送货上门。…全国各地多家工厂的司机都被送回家了…有些人担心接下来会有什么工作量。
……
亚马逊网络服务的中断……已经波及到网络经济，使数百万人使用的服务陷入瘫痪。…亚马逊表示，美国东部 1 号的“几个网络设备受损”是此次中断的“根本原因”。

我在想开发人员学到了什么？输入[麦克斯·罗森](https://onlineornot.com/onlineornot-aws-outage-retrospective "read the full text"):

AWS 花了大约一个小时来更新他们的状态页面，以表明**任何事情**正在发生。…虽然我们的基础架构托管在 20 个 AWS 地区，但单点故障托管在 us-east-1。
……
我们学到了:……我学到了一句谚语，“朋友不让朋友部署在 us-east-1。”因此，我们将首先把一些东西转移到 us-east-2。其次，我们将增加冗余和故障转移到另一个 AWS 区域的能力。

进入正题，下面是[尤金·金和凯瑟琳·朗](https://www.businessinsider.com/amazon-aws-outage-cause-problem-with-network-device-traffic-virginia-2021-12?r=US&IR=T "read the full text")，*为大家讲解一切*:

即使在 AWS 内部……关于断电的信息仍然是粗略的，谣言在工作人员中传播。一名 AWS 员工推测，中断是由“精心策划的 DNS 攻击”引起的，而另一名员工淡化了这些担忧。
…
根据一份 AWS 内部公报的截图…“防火墙正在不堪重负。”…一份单独的内部说明称…网络问题“特别影响”了亚马逊的内部 DNS 服务器。

* * *

## Linux 正式获得 Rust 代码

Rust 语言已经朝着成为 Linux 内核开发的一部分迈出了下一步。一些用 Rust 写的“驱动和其他非核心内核程序”现在可以被 PR'ed 了。但是仍然没有进一步发展的计划。

### 分析:仍需润滑

对于编写内存安全的代码和编写*可证明的*实现，Rust 比 C 好得多。然而，引导工具链仍然是**愚蠢的困难**。

史蒂文·j·沃恩-尼克尔斯 : **Linux 越来越生锈了**

就在不久前，除了 C 语言之外，在 Linux 内核中使用另一种语言的想法还会遭到嘲笑。(但)这种情况已经持续好几年了。…为什么？因为它比 C 安全得多，尤其是在处理内存错误方面。下一个“补丁系列[增加]了对 Rust 作为 Linux 内核第二语言的支持。”…虽然他鼓励以缓慢但稳定的方式将 Rust 引入 Linux，但[Linus Torvalds]也说过为驱动程序和其他非核心内核程序使用 Rust 接口是有意义的。[但是]没有人会在 Rust 中重写内核的 2500 万行 C 代码。
…
为内核提出的 Rust 代码现在依赖于稳定的 Rust 编译器，而不是 beta 编译器。…正如 Linux 内核和 Linux 上的领先 Rust 开发人员 Miguel Ojeda 所说，“通过升级编译器，我们已经能够去掉我们正在使用的一些不稳定的功能。”

如何做到“比 C 更安全”？[索科洛](https://forums.theregister.com/forum/all/2021/11/10/where_rust_fits_into_linux/#c_4365594 "read the full text")分享了这一有趣的见解:

Rust 试图通过良好的 API 设计来鼓励这一点，它允许在编译时证明不变量将得到支持，从而避免了在安全性和性能之间进行选择的需要。我最喜欢的例子是“类型状态模式”,它可以让你教 Rust 编译器证明任何状态机的正确遍历。一个更普通的例子是迭代器 API:如果迭代器在开始时查找一次长度，那么就不需要边界检查，API 可以防止你偏离它提供给你的每个条目。… Rust 程序往往比它们的 C 和 C++对应物运行**更快**，因为开发人员乐于引入和维护更激进的优化。

[然后奇迹出现了](http://www.sciencecartoonsplus.com/pages/gallery.php "with apologies to Sidney Harris")， [@dave_universetf](https://twitter.com/dave_universetf/status/1468653443053092867 "read the full text") 讽刺道:

我对此很感兴趣，但我不禁为那些从事自助工作的人感到遗憾。c 很难引导，但是 Rust 是一种全新的痛苦。
…
Rust 实际上不是源代码可引导的。[编译器]目前有效的是 Rust 1.39。所以你必须再编译 18 个 Rust 编译器才能升级到当前版本。

* * *

## 英伟达的 ARM 灾难仍在继续

正如我在之前[说过](https://devops.com/wth-we-wanna-wfh-dod-dual-sources-jwcc-more-nvidia-arm-woes/) [的话，这笔交易真的不应该通过。拥有 ARM ISA 和核心设计将是击败英伟达竞争对手的巨大战略筹码。ARM 芯片越来越成为数据中心的固定设备，尤其是那些重视每瓦性能的芯片](https://devops.com/wth-we-wanna-wfh-dod-dual-sources-jwcc-more-nvidia-arm-woes/)

### 分析:插个叉进去

英伟达从软银收购 Arm 的尝试正遭遇千刀万剐。而最新的伤口来自于 **FTC 的*小野上*刀**。

[保罗·瑟罗特](https://www.thurrott.com/hardware/259859/ftc-sues-to-block-sale-of-arm-to-nvidia "read the full text") : **联邦贸易委员会起诉阻止向英伟达出售 Arm**

美国美国联邦贸易委员会提起诉讼，以竞争问题为由阻止英伟达以 400 亿美元收购 Arm。一年多前，即 2020 年 9 月，Nvidia 宣布打算以约 400 亿美元的价格从软银手中收购 Arm。但是，这项交易立即遭到了依赖 Arm 设计的主要行业参与者的批评，英国政府宣布将出于国家安全原因进行“干预”。
……
现在，可能根本不会发生。“我们将继续努力证明这项交易将有利于行业和促进竞争，”英伟达说。

像我 5 岁一样解释？这是斯威尔登:

ARM 在数据中心的份额不小，而且还在不断增加。… ARM 比手机大得多… Arm 是英特尔和 AMD 的重要竞争对手。……Arm 授权 IP 给高通、英伟达、联发科、优尼科、三星、苹果、谷歌等。，对许多技术领域都很有帮助。Arm 作为一群不同芯片厂商的共同设计者，对 CPU/SoC 设计的进步非常有益。…如果行业中的许多人都转向 x86，消除我们从许多 ARM 芯片制造商那里获得的所有硬件功能竞争，那将是非常不幸的。

但是软银呢？[伊恩·金](https://www.bloomberg.com/news/articles/2021-12-03/softbank-poised-to-lose-74-billion-payday-if-arm-deal-is-halted "read the full text")经营着这些数字:

华尔街分析师几乎认为这笔交易已经失败。…据花旗银行分析师称，英伟达收购完成的可能性现在只有 5%。该公司面临着损失大约 740 亿美元的前景。…其他追求者不太可能提供这样的报价。…因此，软银的最佳选择很可能是对 Arm 业务进行首次公开募股——但这可能会使公司估值达到…. 198 亿美元——仅约为**英伟达交易价值的 27%** 。

* * *

## 这个故事的寓意:**众所周知，我们俩的时间都不多了**

*你一直在读[里奇·詹宁斯](https://www.richi.uk/)的*远景*。你可以通过 [@RiCHi](https://twitter.com/richi) 或者 [【邮箱保护】](/cdn-cgi/l/email-protection#c3b7afb583b1aaa0abaaeda0acedb6a8fcb0b6a1a9a6a0b7feee978f95ee) 联系他。(说我自己太典型了——[对不起](https://www.musixmatch.com/lyrics/Adele-3/Hello)。)*

图片:[ləmanşirinzadə](https://unsplash.com/photos/7XRdzXHANsI)(通过 [Unsplash](https://unsplash.com/license "Some rights reserved")*