# Akamai:收购 Linode | Firefox:不太好|消失:谷歌疫苗授权

> 原文：<https://devops.com/akamai-buying-linode-firefox-not-ok-gone-google-vaccine-mandate/>

欢迎来到[](https://devops.com/author/richi/)*——在这里，我们细读本周新闻，并将其剥离至要点。让我们弄清楚**什么才是真正重要的**。*

*本周:Linode 被 Akamai 收购，Firefox 的市场份额“少得可怜”，谷歌将员工带回办公室。*

 *## 1.Akamai + Aker = '协同作用'

本周的第一个问题是:Akamai 为什么要收购 Linode？不管原因是什么，对它唯一的股东来说，这是一个巨大的发薪日:十亿美元已经不远了。

### 分析:邻居走了？

边缘计算和 CDNs 的 100 磅大猩猩承诺不会扰乱 Linode 的开源云公式:不变，稳定，等等。但是我们以前听过多少次了？

这里有一个当地的涂鸦者 [Paige Gross](https://technical.ly/2022/02/16/linode-acquisition-akamai-game-changer-cloud-service-providers/ "read the full text") : **Linode 被 Akamai 以 9 亿美元收购是一个“游戏规则改变者”**

费城科技界的一个家喻户晓的名字…首席执行官克里斯托弗·阿克于 2003 年创建了该公司，从那时起，该公司一直在发展壮大，员工人数已增至约 250 人。…自创建以来，Aker 拥有 100%的 Linode 股份。Aker 表示，随着云服务变得无所不包，包括计算、存储、安全和从核心到边缘的交付，该交易使公司更接近解决不断发展的挑战。…我们一直在谈论‘替代云’—替代大家伙，现在我们已经在这个市场上验证了自己。”
……
这家位于老城区的公司保持着“超过 100 万个账户”，但在任何特定时间，其平台的活跃用户都在 15 万左右。利诺德的总部，位于第三大街和拱门大街的银行大楼依然存在。……对于客户和 Linode 员工来说，不会有太多明显的变化[Linode]说。

Akamai 为什么要 Linode？[乔纳森·格雷格](https://www.zdnet.com/article/akamai-ceo-linode-acquisition-makes-company-worlds-most-distributed-cloud-services-provider/ "read the full text")问首席执行官:

Akamai 首席执行官 Tom Leighton 解释说，Linode 拥有强大的客户支持，已经在 11 个地方开展业务，Akamai 将“大幅”扩展这些业务。… Leighton 还提到了 2021 年 9 月对总部位于以色列的网络安全公司 Guardicore 的收购，该公司提供微分段解决方案，以减少企业网络的潜在攻击面，保护应用程序并满足合规性标准。根据 Leighton 的说法，该公司预计云计算类别——包括边缘应用程序、网络存储业务和 Linode——将在 2023 年达到“超过 5 亿美元”。…我们是边缘计算领域的先锋，现在我们通过 Linode 在云计算领域向前迈进了一大步。”

但是这里有一个令人担忧的消息[zoid.com](https://it.slashdot.org/comments.pl?sid=20803779&cid=62271657 "read the full text"):

这对他们很好，但我希望[Akamai]不要搞砸了。Linode 是一家很棒的托管公司。

* * *

## 2.火狐不好

上周，一名记者天真地问道:“火狐可以吗？”人们失去了理智。

### 分析:不，不好——这对 DevOps 和 web 来说是个大问题。

我们需要火狐和壁虎。铬单一文化对网络和开发者都不利。(在你问之前:不，WebKit 的存在并不能改变什么，这要感谢苹果荒谬的政策)。尽管上个月我试图对 Firefox 说些好话，但坦率地说，它的市场份额是,**可怜的**。

马特·伯吉斯 : **火狐可以吗？**

自从 Firefox 在 Netscape 的阴影下推出以来的 20 年里……浏览器已经下滑到不到 4%的市场份额——在移动领域更是少得可怜，只有 0.5%。…它的命运对整个网络也有更大的影响。谷歌每年向 Mozilla 支付数亿美元的版税。…在 2020 年的财务结果中… Mozilla 列出的总收入为 4.96 亿美元。…谷歌与 Mozilla 的交易最后一次续签是在 2020 年，预计将于 2023 年到期。… Mozilla 和 Firefox 承认，从长远来看，它需要使赚钱的方式多样化。
……
火狐仍然举足轻重:……浏览器市场由谷歌的 Chromium 代码库及其底层浏览器引擎 Blink 主导。…微软的 Edge 浏览器、Brave、Vivaldi 和 Opera 都使用 Chromium 的改编版本。苹果有自己的 WebKit 浏览器引擎，但除此之外，火狐的 Gecko 浏览器引擎是唯一的选择。

火狐，我们如何爱你？让 [not_count_zero](https://arstechnica.com/gadgets/2022/02/is-firefox-ok/?comments=1&post=40677614#comment-40677614 "read the full text") 统计一下方式:

我仍然使用 Firefox，因为:a)我记得 Internet Explorer 和标准之战。…
b)我不信任谷歌。…
c)大多数网站运行良好。
……
不过我确实有问题。…他们现在有一辆半 *billion‽* 他们*在用它做什么*？…这看起来真的是假的，真的是假的。

但是注意到一个深深忧虑的人:

Firefox 的衰落和潜在的消亡是一个大问题，每个人似乎都在小心翼翼地回避——太害怕承认如果 Firefox 真的消失了，我们就完了。我们将回到 20 年前的起点，Chrome 将成为新的 IE6。对于……Linux 用户、开发者和发行商来说，形势尤其严峻。… Gnome 浏览器或 KDE 的 Falkon 几乎不能被认真对待，而且…基于苹果的 WebKit，这不是一个很好的位置。

* * *

## 3.谷歌重返工作计划放弃疫苗授权

谷歌正在计划“庆祝活动”来欢迎完全远离公司的员工。实际上，与 IBM 的不同，这个*并不意味着**疫苗授权**。*

### 分析:直言不讳的少数派赢了——还是他们赢了？

就在三个月前，谷歌表示“坚定支持我们的疫苗接种政策。”什么变了？这不太可能是因为极少数员工**发表了一份宣言**。

[詹妮弗·伊莱亚斯](https://www.cnbc.com/2022/02/23/googles-relaxes-mandates-opens-amenities-for-return-to-office.html "read the full text") : **谷歌放宽指令**

该公司将不再要求将接种疫苗作为雇用条件…因为它准备让工人回到办公室…至少一周三天的“混合”工作模式。…该公司(以前)告诉员工，他们必须遵守疫苗政策，否则他们将面临减薪，并最终失去工作。根据谷歌发言人 Lora Lee Erickson 的说法，该公司在取消了 1 月 18 日为员工设定的要么接种疫苗要么获得豁免批准的最后期限后，取消了这一要求。她拒绝提供政策的更多细节，也拒绝透露政策改变的原因。
……
如果情况继续改善，谷歌房地产和工作场所服务副总裁大卫·拉德克利夫(David Radcliffe)准备开始向混合工作周的 30 天过渡期。他说，他的团队正在计划“庆祝活动”来欢迎员工回来。…获准进入办公室的未接种疫苗的员工仍需遵守附加协议，包括检测和佩戴口罩。

说反政府组织也是反暴力者，这太简单了。比如 [raxxorrax](https://news.ycombinator.com/item?id=30452556 "read the full text") :

我接种了疫苗，HR 也知道这一点。…但如果他们正式要求出具证明，我想我会放弃。许多人没有这个选择，但这种不合理的要求是有后果的。
…
我理解在某些与健康相关的职业中接种疫苗的要求。如果你想在这个领域工作，这是你必须亲自接受的。

虽然其他几个人都以*的方式*结束了钟形曲线。格雷戈·金克森:

别激动，[谷歌]还是邪恶愚蠢的。…现在他们出于某种原因做出了让步，[但]就限制措施的撤销而言，这几乎没什么值得注意的。这不是什么令人鼓舞的消息。

* * *

## 这个故事的寓意是:失败是成功的基础，也是获得成功的手段。

*你一直在读[里奇·詹宁斯](https://www.richi.uk/)的*远景*。你可以通过 [@RiCHi](https://twitter.com/richi) 或者 [【邮箱保护】](/cdn-cgi/l/email-protection#4430283204362d272c2d6a272b6a312f7b3731262e212730796910081269) 联系他。![](img/c20b7a37f8ba20f40b8509adf5290dfb.png)*

图片:[阿列克谢·库普里科夫](https://unsplash.com/photos/tE0pFP3cLE8)(经[Unsplash](https://unsplash.com/license "Some rights reserved")；平整和裁剪)*