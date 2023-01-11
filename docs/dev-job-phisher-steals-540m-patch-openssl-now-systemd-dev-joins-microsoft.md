# Dev Job Phisher 窃取了 5 . 4 亿美元|立即修补 OpenSSL | Systemd Dev 加入微软

> 原文：<https://devops.com/dev-job-phisher-steals-540m-patch-openssl-now-systemd-dev-joins-microsoft/>

欢迎来到[![](img/578e017469da523d7cc421e1c2dcbfde.png)](https://devops.com/tag/the-long-view/)*——在这里我们细读本周新闻，并将其剥离至要点。让我们弄清楚**什么是真正重要的**。*

*本周:鱼叉式网络钓鱼造成了 5.4 亿美元的损失，OpenSSL 中一个严重程度很高的错误可能“比心脏出血更糟糕”，Lennart Poettering 现在为微软工作。*

 *## 1.不要被钓鱼欺骗

本周第一件事:一名高级开发人员允许黑客通过打开电子邮件附件来侵入他们公司的网络。开发者信任发送者，因为它看起来是一家提供丰厚工作的公司。

### 分析:不要放松警惕

DevOps 的员工通常最容易意识到打开电子邮件附件的风险。但是，即使是最细心的人也可能看不出像这只这样聪明、耐心的攻击者。

[瑞恩·威克斯](https://www.theblock.co/post/156038/how-a-fake-job-offer-took-down-the-worlds-most-popular-crypto-game "read the full text") : **一份虚假的工作邀请如何搞垮世界上最流行的密码游戏**

很少有求职申请的事与愿违，比一名高级工程师的情况更令人震惊……他对加入一家虚构公司的兴趣导致了(加密货币)行业最大的黑客攻击之一——与以太坊相关的 side chain……损失了 5.4 亿美元。…一位消息人士补充道,(招聘)是通过职业社交网站 LinkedIn 进行的。
…
这份虚假的“报价”是以 PDF 文档的形式发送的，工程师下载了这份文件，从而让间谍软件渗透到 Ronin 的系统中。从那里，黑客能够攻击并接管…浪人网络。

PDF？这怎么可能呢？ [zrobotics](https://news.ycombinator.com/item?id=32009699 "read the full text") 看到了类似的场景:

网络钓鱼者要求雇员签署一份与海关有关的文件。网络钓鱼者认为该员工处理运输索赔和退货，并推测他们需要处理需要签名的海关文件。

PDF 里有一个链接，链接到一个欧洲云服务上托管的 exe，标题是“安装假签名证书公司签署这个文件。”这导致了一个基本勒索软件可执行文件的下载。这确实通过了我们的反病毒软件，对员工的机器进行了加密，但幸好被阻止传播到网络的其他地方。

该员工的机器坏了，但我能够从前一天的备份中恢复，并且没有发生重大损害……但他们确实损失了半天的工作，我更新了我们的培训。从社会工程的角度来看，攻击本身是聪明的，但技术上的利用是任何脚本都可以从公开网站上下载的，根本不先进。但是 Gmail 并不总是扫描 pdf 格式的链接，所以一个聪明的诡计绕过了谷歌的扫描和我们的本地扫描。

然而，社会工程 FTW。这是瑞秋·托巴:

基于工作的网络钓鱼攻击是一个巨大的挑战，原因有很多:很难验证与你没有关系的人的身份/真实性，工作机会实际上会安排面试/发送信息，因此攻击方法与现实生活相符，等等。

* * *

## 2.OpenSSL Bug“比 Heartbleed 还糟糕”？

OpenSSL 3.0.4 引入了一个棘手的漏洞，使得攻击者能够破坏服务器内存。CVE-2022-2274 可能会让这样的骗子**远程执行代码**。

### 分析:现在打补丁，obvs。

3.0.5 修复了漏洞，现在已经可以上游了。如果你的服务器支持 AVX512IFMA 指令，你应该在你的发行版有了它之后尽快获取它。

[圭多·弗兰肯](https://guidovranken.com/2022/06/27/notes-on-openssl-remote-memory-corruption/ "read the full text") : **OpenSSL 远程内存损坏**

奇怪的是，几乎没有人谈论这一点:……OpenSSL 3 . 0 . 4 版……容易受到远程内存损坏的影响，攻击者可以轻易地触发这种损坏。…支持 AVX512 的 x64 系统受到影响。如果 RCE 有可能被利用，这比心脏出血还要糟糕。…除了代码执行之外，还可能出现隐私数据泄露给攻击者的情况。

当有更好的选择时，为什么我们还在使用 OpenSSL？ggm :

OpenSSL 代表“API/ABI”依赖性。人们对此进行编码。随着时间的推移，随着人们添加和删除内容，OpenSSL 也“随着增长而增加”。最初的内核 SSLEAY 是内核加密社区之外的某个人的一个典型实例……并且被手工编码以在算法上忠实于出口限制(ITAR)和机器代码优化:它是*快*。

这里有点讽刺的是[siren](https://news.ycombinator.com/item?id=31997447 "read the full text"):

英特尔在一个令人震惊的举动中，通过在 12 个月前弃用 AVX512，先发制人地在芯片中修补了这个漏洞。

* * *

## 3.Systemd Dev 现在为微软工作

Systemd 就像 Marmite …或起亚灵魂:你要么爱它，要么恨它。现在它的创造者是一名微软员工，会有更多人讨厌它吗？。

### 分析:拥抱，延伸，熄灭？

微软长期以来一直宣扬其对开源的热爱和支持。但是人们的记忆力很差——所以很难赢得信任。但是 Lennart Poettering 加入了一个长长的杰出名单，包括现任和前任 FLOSS 开发者。

[迈克尔·拉贝尔](https://www.phoronix.com/scan.php?page=news_item&px=Systemd-Creator-Microsoft "read the full text") : **Systemd 创造者登陆微软**

Lennart 安静地吟诗…离开了 Red Hat，在那里领导 PulseAudio 和其他项目 15 年，并最终开始了 systemd，它从根本上重塑了现代 Linux 发行版。…他加入了雷德蒙公司…事实证明这不是一个笑话。这位杰出的开源开发者继续致力于 systemd 开发。虽然有些人可能并不总是赞同他的观点或处理一些事情的方法，但他对 Linux/开源世界的巨大贡献是毋庸置疑的。
…
随着时间的推移，微软雇佣了许多 Linux 开发者和其他著名的开源开发者。[例如] Python 创造者吉多·范·罗苏姆、GNOME 创造者米格尔·德·伊卡萨、纳特·弗里德曼、Gentoo Linux 创始人丹尼尔·罗宾斯、史蒂夫·弗伦奇、马特奥·克罗齐、马修·威尔科克斯、泰勒·希克斯、希亚姆·普拉萨德 N、迈克尔·凯利等等。…也是在今年早些时候，另一位长期的 Linux 内核开发人员 Christian Brauner 加入了微软。

“悄悄”？ [em-bee](https://news.ycombinator.com/item?id=32010350 "read the full text") 并不惊讶:

我对他悄悄地做出这一举动并不感到惊讶。Poettering 的工作吸引了不成比例的批评，搬到微软并不完全是一个有助于平息批评的举动。由于他继续从事 systemd 的工作，批评家们现在开始指责 systemd 是微软的产品。……这一举动很可能会加强反 systemd 阵营。

无论微软做什么，有些人永远不会信任这家公司。比如[拉布科尔](https://www.phoronix.com/forums/forum/phoronix/latest-phoronix-articles/1333032-systemd-creator-lands-at-microsoft?p=1333062#post1333062 "read the full text"):

Systemd 很棒，尽管它被人讨厌……因为它的整体结构，这是一个很蹩脚的理由。…我确信我们将开始看到更多的发行版脱离 systemd，纯粹是因为对微软的不信任——这是一件好事，因为多样性和选择是好事。虽然我真的不介意坚持使用 systemd，即使是在 Micro$oft 上做诗，我的意思是我讨厌微软，我肯定****不会把宠物石托付给他们，但是 systemd 是一个开源项目，如果他们把一些可疑的****强加到 systemd 上，那么有人会把它叉掉并删除，我们都会使用它。
。

* * *

## 这个故事的寓意:
**行动要伟大，就像你一直在想的那样**

*你一直在读[里奇·詹宁斯](https://www.richi.uk/)的*远景*。你可以通过 [@RiCHi](https://twitter.com/richi) 或者 [【邮箱保护】](/cdn-cgi/l/email-protection#e99d859fa99b808a8180c78a86c79c82d69a9c8b838c8a9dd4c4bda5bfc4) 联系他。*

图片:[布鲁诺·范德克朗](https://unsplash.com/photos/T9_UAyOI4hc)(经[Unsplash](https://unsplash.com/license "Some rights reserved")；平整和裁剪)*