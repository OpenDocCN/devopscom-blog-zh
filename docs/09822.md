# Linux 6.0 更快、更酷| Debian 成为专利|谷歌非洲地区

> 原文：<https://devops.com/linux-60-debian-non-free-google-africa-richixbw/>

欢迎来到[![](img/2fa3361d65c0baeb39bbbf03af0d994b.png)](https://devops.com/tag/the-long-view/)*——在这里我们细读本周新闻，并将其剥离至要点。让我们弄清楚**什么是真正重要的**。*

*本周:Linux 6.0 升级为稳定版，Debian 12 将包含闭源二进制文件，谷歌云开放首个非洲地区。*

 *## 1.下一站:6.1

本周第一位:Linus " [我把 Linux 读作 Linux](https://www.youtube.com/watch?v=y6dtdRY31xE&list=UUPpWcTthLKQcUZsR-U79wjw "Hello! This is Linus Torvalds.") " Torvalds 按下了 Linux 6.0 的按钮。新内核有大约**15000 个非合并提交**。

### 分析:多云善

Linux 6.0 中值得注意的更新包括对服务器 CPU 的更好支持——新的*和旧的*。不仅仅是为了新的热点——最新的至强处理器，最新的 EPYC 处理器，最闪亮的 ARM 处理器，RISC-V——的改变，也是为了修复一个古老的电源管理解决方案的令人讨厌的副作用，这个解决方案**抑制了 AMD perf** 。

[西恩·迈克尔·肯纳](https://venturebeat.com/data-infrastructure/linux-6-0-kernel-enhances-security-with-runtime-verification-improves-cpu-energy-efficiency/ "read the full text") : **Linux 6.0 内核增强安全性【和】能效**

**`Formal specification`**
Linux…是云必不可少的组成部分。…甚至微软也提供基于 Linux 的计算。…“希望每个人都清楚，主要版本号的变化与其说是任何重大的根本性变化，不如说是我的手忙脚乱。(但是)6.0 是更大的版本之一，”Linus Torvalds 写道。
…
Linux 调度程序中删除了一个限制 CPU 间进程迁移的能量余量启发式规则，总体上提高了能量利用率。arm64 芯片架构现在终于可以正确地将透明大页面交换为内存，从而显著提高某些工作负载的吞吐量。…运行时验证(RV)是一种轻量级但严格的正式验证方法…分析系统实际执行的跟踪，并将其与系统行为的正式规范进行比较。

还有什么值得注意的？[凯文·波弟](https://arstechnica.com/gadgets/2022/10/linux-6-0-arrives-with-support-for-newer-chips-core-fixes-and-oddities/ "read the full text")张口说道:*【你被解雇了——艾德。]*

其中最值得注意的可能是一个补丁，它阻止了 AMD 芯片近 20 年的减速，该补丁基于 21 世纪初的电源管理工作代码，该代码存在了太长时间。…普通的桌面用户不会看到巨大的收益，但是处理密集型输入/输出应用程序的大型系统应该会受益。
…
Linux 6.0 包括几个值得注意的硬件驱动程序:第四代英特尔至强服务器芯片，并不十分出色的第 13 代 Raptor Lake 和 Meteor Lake 芯片，以及 EPYC 系统。Sapphire Rapids CPUs 的 ACPI 和电源管理改进。…更多关于 RISC-V、OpenRISC 和 LoongArch 技术的工作。英特尔 Habana Labs Gaudi2 支持，允许机器学习库的硬件加速。“来宾 vCPU 停止检测器”,可以在虚拟客户端冻结时通知主机。
……
一个小而古怪的补充说明了 Linux 内部正在发生更大的事情:基于 ARM 驱动的高通骁龙芯片的联想 ThinkPad X13s 在 6.0 中获得了一些早期支持。ARM 支持是托沃兹渴望看到的——他最近从他的 M2 驱动的 MacBook Air 上写了内核版本的发行说明。

来点真实世界的测试怎么样？下面是 [TNZfr](https://www.phoronix.com/forums/member/112010-tnzfr "read the full text") 的印象:

编译，安装和非常高兴为 office @ home，我用一个 ryzen 5950x 和一个 5850u。上一次 5.19 和 6.0 的差别很大。(我在别的地方有一台旧的英特尔酷睿 i5 2400 差别不大，好一些，但不太明显。)
……
火狐显示更快，
LibreOffice 启动更快。…
盗墓者之影 3072*1728 全选项… 5.19.12: 62 fps / 6.0.0: 68 fps 少急动。

* * *

## 2.Debian 投票使用封闭 blob——是的， *Debian*

在一个惊人的大转变中，Debian 社区已经打破了三十年来对非自由软件的 Kanute 式的否定。这主要以预编译、**专有设备驱动程序**的形式出现。

### 分析:最后，Debian 社区明白了

猪会飞。地狱结冰了。**猫和狗一起生活**。

Steven j . Vaughan-Nichols:**Debian Linux 接受专有固件**

**`This is not your dad's Debian`**在 Debian Linux 29 年的历史中，有一点是不变的:Debian 将完全由自由软件构成。…直到现在。从下一个版本开始，Debian 12，又名书虫，Debian Linux 将包含专有固件。
…
九月，该组织投票决定加入非自由固件。…令人惊讶的是，它很容易就通过了。… Debian 现在将包含非自由固件包，当需要它们时，默认情况下会启用它们。…这对于早期的 Debian 开发者来说可能是令人震惊的。
…
这不是你爸的 Debian。…将于 2023 年推出带有新闭源软件的 Debian Linux 12。……时代在变。

具体来说，比如？听到的声音:

似乎是一个务实的想法。例如，如果你的互联网连接是通过 Wi-Fi，那么默认的 Debian ISO 很有可能无法连接 Wi-Fi。

我和 Debian 一直处于这个位置。虽然我知道如何解决这个问题，但我很容易想象这对一个不熟悉 Debian 或 Linux 的人来说是多么神秘。我赞赏 Debian 对自由/开源软件的清教徒式态度，但这让他们多年来付出了沉重的代价。当有人只想上网时，谈论自由/开源软件固件是一个失败的争论。

但是唐巴里不是粉丝:

对于 Debian 来说这是非常悲伤的一天。维护自由软件和非自由软件之间的清晰划分一直是这种发行版的优势。他们没有让那些绝对需要非自由选项的人更容易看到这些选项，同时明确表示它们不是 Debian 的一部分，而是抹去了这条线，开始走下坡路。我几乎觉得哀悼是合适的。

* * *

## 3.南非将成为谷歌在非洲大陆的首个地区

谷歌将开设其首个非洲数据中心。它的第一个地区将在南非。

### 分析:莱克尔

如果您在非洲需要边缘工作负载或数据存储，这非常有用。看起来对南非和整个非洲大陆来说都是一个巨大的进步。

[安妮·恩詹贾和塔格·肯-奥卡弗](https://techcrunch.com/2022/10/05/google-picks-south-africa-for-its-first-cloud-region-in-africa/ "read the full text") : **谷歌选择南非作为其在非洲的第一个云区**

**`Increasingly critical`**
云区域在南非的推出，让 AWS 和微软 Azure 等其他顶级提供商开始追赶。……目前还不清楚为什么谷歌一直没有涉足非洲。…其早期采用者包括大型企业公司和电子商务公司，如南非的 TakeAlot 和肯尼亚的 Twiga。
…
谷歌…还在内罗毕(肯尼亚)、拉各斯(尼日利亚)和南非(开普敦和约翰内斯堡)建设专用的云互联网站，将用户的内部网络与谷歌的网格连接起来。…谷歌计划利用其连接非洲和欧洲的私有海底电缆 Equiano 为这些站点供电。
…
随着肯尼亚等国家实施隐私和数据法，要求公司将数据存储在境内，并通过本地托管的服务器进行处理，用户选择存储数据的能力变得越来越重要。…根据谷歌云委托进行的研究…到 2030 年，南非云地区将为南非的 GDP 贡献超过 21 亿美元，并支持创造超过 40，000 个就业岗位。

但是他们将如何为它提供动力呢？南非的电网并不以可靠性著称。这位[匿名懦夫](https://tech.slashdot.org/comments.pl?sid=22168713&cid=62943085 "read the full text")思索道:

我想知道他们需要多少电力，以及拥有自己的发电站(也许使用比液化石油气或柴油更便宜的能源)或大型太阳能装置是否有意义？…另一方面，在豪登省和开普敦有相当多的数据中心(例如，标准银行在米德兰特的全非洲数据中心),所以人们会认为有办法解决这个问题。…在下一届 braai 上与我的一些工程师朋友交谈，看看他们提出了哪些仍被视为有利可图的东西，可能会很有意思。

在非洲，真的还有其他选择吗？T2 提出了一个建议:

我可以把埃及看作一个潜在的选择，但是这个也有道理。

* * *

### 这个故事的寓意:
**傻瓜自以为聪明，但聪明人知道自己是个傻瓜**

*你一直在读[里奇·詹宁斯](https://www.richi.uk/)的*远景*。你可以通过 [@RiCHi](https://twitter.com/richi) 或者 [【邮箱保护】](/cdn-cgi/l/email-protection#47332b3107352e242f2e69242869322c783432252d2224337a6a130b116a) 联系他。*

图片:[维克多朱琳](https://unsplash.com/photos/LL1m3ThSR6I)(通过[Unsplash](https://unsplash.com/license "Some rights reserved")；平整和裁剪)*