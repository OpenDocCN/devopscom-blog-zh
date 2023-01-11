# 苹果断电愤慨| Linux 随机重做| Okta 被黑(或不被黑)

> 原文：<https://devops.com/apple-outage-outrage-linux-random-redo-okta-hacked-or-not/>

欢迎来到[![](img/befdd855cce9b8a12f7926a999f9e33c.png)](https://devops.com/tag/the-long-view/)*——在这里我们细读本周新闻，并将其剥离至要点。让我们弄清楚**什么是真正重要的**。*

*本周:为什么苹果服务被关闭，Linux 得到一个巨大的 RNG 检修，我们想知道 Okta 是否再次被黑。*

 *## 1.烂苹果行动？

本周第一条消息:昨天苹果的大部分服务都停止了(至少在一些地区)。在至少两个小时的时间里，几乎没有东西在工作，包括开发网站和一些内部应用程序。

### 分析:“总是 DNS”

尽管有传言，但这不是俄罗斯黑客。也不是 BGP 攻击。虽然库比蒂诺还没有承认，但看起来很像是 DNS ( *quelle surprise* )。

Joe Rossignol 爆料: **iCloud 和许多其他苹果服务停止**

受影响的服务和应用程序包括 App Store、iCloud、Siri、iMessage、iTunes Store、Apple Maps、Apple Music、Apple Podcasts、Apple Arcade、Apple Fitness+、Apple TV+、Find My、FaceTime、Notes、Stocks 和许多其他应用程序。
…
苹果的开发者网站也无法访问。…苹果的一些内部系统也瘫痪了。

哪里出了问题？[动画师](https://news.ycombinator.com/item?id=30757316 "read the full text")补充道:

苹果自己的 DNS 服务器将 developer.apple.com 重定向到 Akamai 运营的“akadns.net”上。但是苹果自己的 DNS 服务器拒绝解决这个问题，可能是因为它不在 apple.com 区。很明显这是一个拙劣的 DNS 配置。不清楚意图是什么。…无论如何，这看起来像是试图将某些东西外包给 Akamai，但却大错特错。

ofc，“是*总是* DNS，”amirite？萨迪克·赛义夫说:

据我所知，这个问题是由 aaplimg.com 的 DNSSEC 验证失败引起的。我注意到在我本地的 pihole 日志里有很多 DNSSEC 的虚假信息，比如从 CNAME 到 aaplimg.com 的 proxy.safebrowsing.apple。

这里有更多来自利马的消息:

看起来他们的 DNS 服务器有响应，但拒绝提供记录。…很可能是一个配置错误，一旦他们找到了在 DNS 关闭时如何重新部署 DNS 服务器的方法，这一错误就会被消除。

* * *

## 2.重构了 Linux 随机数生成器

正确的、不可猜测的随机数是开发诸如强加密和安全 TCP 等固有特性的关键。Linux 已经落后于其他操作系统，在熵收集、VM 安全和**过时散列**等领域。

### 分析:技术债——滚蛋！

Jason Donenfeld 不仅改进了这些领域，还解决了几十年来的代码缺陷——改进了可读性、可维护性和文档。我同意他的观点，这种“不性感的改进”是极其重要的投资。

[Michael Larabel](https://www.phoronix.com/scan.php?page=news_item&px=Linux-5.18-RNG "read the full text") 一直在关注事态发展: **Linux 5.18 带来许多随机数生成器改进**

WireGuard 首席开发人员 Jason Donenfeld 最近带头对 Linux 内核的随机数生成器进行了许多改进。这些 RNG 改进提供了更好的虚拟机安全性、巨大的性能提升等等。

马嘴会是[杰森·a·唐恩菲尔德](https://www.zx2c4.com/projects/linux-rng-5.17-5.18/ "read the full text"):

这是一种尝试，旨在使所使用的代码和加密技术现代化。…我们的目标是在不改变任何基本设计的情况下，尽可能提高 RNG 现有设计的严谨性。…重点是从进化的角度改进现有的 RNG 设计。将…熵源转化为密码安全随机数的基础算法已经被彻底改造。…最显著的外部变化是/dev/random 和/dev/urandom 现在是完全相同的东西。…我一开始把 SHA-1 换成了布雷克 2…SHA-1 已经被无情地摧毁了，这是一个很容易做出的改变。…这一变化使我们能够将熵输入池的前向安全性从 80 位提高到 128 位，并为我们能够使用哈希和密钥哈希做更多有趣的事情创造了条件…从而进一步提高安全性[和]性能。
…
random.c 是在 1.3.30 中引入的……在当时是一个非常令人印象深刻的驱动程序，但是经过几十年的调整，文件的一般组织以及一些编码风格方面都显得有些过时了。…因此，在一般代码可读性和可维护性以及更新文档方面已经做了大量的工作。我认为这些非常不性感的改进和各种花哨的现代密码改进一样重要，甚至更重要。

但是 [sinij](https://linux.slashdot.org/comments.pl?sid=21003443&cid=62373977 "read the full text") 担心新的和闪亮的:

SP 800-90B 符合性如何？这些变化——尤其是向 BLAKE2s 的转变——几乎保证了 Linux 将无法获得 NIST 认证(并因此在需要认证的政府、医疗保健、金融应用中被采用)。所以干得好，让红帽有更多的理由完全放弃 RHEL 9 的内核。

* * *

## 3.“内部人员即服务”骗子声称又一个受害者

LAPSUS$ group 表示，他们已经入侵了 Okta，一家大型身份和认证提供商。如果是真的，对于任何使用 Okta 的 DevOps 团队来说，这都是一个令人不安的发展。

### 分析:Hack redux 还是 APT？

到目前为止，Okta 的公开声明旨在将问题最小化，称共享的截图只是 1 月份被盗数据的翻新。但是该组织声称它在俄克拉荷马州是持久的。无论真相如何，像 LAPSUS$这样的组织可以如此容易地贿赂员工和承包商的事实应该引起每个 DevOps 专业人士的注意。

[Raphael Satter](https://www.reuters.com/technology/authentication-services-firm-okta-says-it-is-investigating-report-breach-2022-03-22/ "read the full text") : **Okta 调查报告数字泄露**

黑客发布了截图，显示他们声称是[Okta]的内部公司环境。黑客攻击…可能会产生重大后果，因为成千上万的其他公司，如联邦快递、穆迪和 T-Mobile，都依赖这家总部位于旧金山的公司来管理对他们自己网络和应用程序的访问。… Okta 将自己描述为“互联网的身份提供商”,并表示其平台上有超过 15，000 名身份服务客户，如单点登录和多因素认证。这些截图是由一个名为 LAPSUS$的勒索黑客组织发布的。[他们包括]似乎是 Okta 的内部门票和它的…松弛的照片。
…
在一份声明中，俄克拉荷马州官员克里斯·霍利斯(Chris Hollis)表示，此次违规事件可能与今年 1 月发生的一起事件有关，他说这起事件已经得到控制。霍利斯说，Okta 当时发现有人试图侵入第三方客户支持工程师的账户:“我们认为网上分享的截图与今年 1 月的事件有关。…除了 1 月份检测到的活动之外，没有任何持续恶意活动的证据。”

这个团体最近怎么会不断出现？通过贿赂内部人士，正如 [nstart](https://news.ycombinator.com/item?id=30763440 "read the full text") 解释的那样:

他们利用链条中最薄弱的一环。…他们专门招聘能够访问 VPNs 内部支持系统的人员。这次 Okta 违约似乎也是通过类似的方式发生的。该组织已经向游戏公司、主机提供商、电信公司、呼叫中心和 BPM 提供商发出了具体的访问请求。不难看出，一些工作过度、收入微薄的支持代理人(甚至是一个收入颇丰的心怀不满的代理人)可能会决定这么做。只需要一个合适的代理给 creds，这个团体就可以立即进入一个巨大的攻击面。这听起来可能有点反应过度，但是未来的公司可能需要将最低权限访问和访问日志记录作为优先事项。

这么说是监守自盗，罪犯被控制了两三个月？吓人，以为 [upuv](https://it.slashdot.org/comments.pl?sid=21017421&cid=62379405 "read the full text") :

这将是一个野蛮的混乱。…我在许多组织和企业中的同事现在都在努力识别和遏制任何违规行为。…我猜所有其他 MFA 提供商都处于完全恐慌状态。

* * *

## 这个故事的寓意是:最重要的是，对你自己要真实。

*你一直在读[里奇·詹宁斯](https://www.richi.uk/)的*远景*。你可以通过 [@RiCHi](https://twitter.com/richi) 或者 [【邮箱保护】](/cdn-cgi/l/email-protection#8efae2f8cefce7ede6e7a0ede1a0fbe5b1fdfbece4ebedfab3a3dac2d8a3) 联系他。*

图片:[罗马博洛赞](https://unsplash.com/photos/96vZSIQQpfk)(via[Unsplash](https://unsplash.com/license "Some rights reserved")；平整和裁剪)*