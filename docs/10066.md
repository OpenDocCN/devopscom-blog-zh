# 2022 年最佳:我们必须杀死‘恐龙’JavaScript |微软开源 3D 表情符号

> 原文：<https://devops.com/kill-javascript-microsoft-emoji-richixbw/>

随着 2022 年的临近，我们 DevOps.com 想要突出今年最受欢迎的文章。以下是我们 2022 年最佳系列的最新内容。

欢迎来到[![](img/c268d97111ccb0d9a88f9b023f1d3349.png)](https://devops.com/tag/the-long-view/)*——在这里我们细读本周新闻，并将其剥离至要点。让我们弄清楚**什么是真正重要的**。*

 *本周:JavaScript 是进步的臃肿障碍，微软的表情符号在 GitHub 上。

## 1.DC 讨厌 JS；爱 E

本周首先:我们需要用“专门为安全分布式编程设计的”东西来取代 JavaScript。JSON 背后的人道格拉斯·克洛克福特如是说。他暗示了自己最新的火焰，**[E 语](https://en.wikipedia.org/wiki/E_(programming_language))** 。

### 分析:大爆炸式的变革很少成功

克罗克福德不太可能带 devs 一起去。浏览器制造商也不会合作。进化通常比革命更有效。TypeScript 和 Wasm 是动作为的**。**

[蒂姆·安德森](https://devclass.com/2022/08/04/retire_javascript_says-json-creator-douglas-crockford/ "read the full text")引导罪犯:**“我们今天能对 JavaScript 做的最好的事情就是让它退役”**

**`Flaws cannot be corrected`**
JSON 的创始人道格拉斯·克洛克福特表示，世界上最流行的编程语言…已经成为进步的障碍…到处都在使用的序列化数据的规范。…“二十年前，我是 JavaScript 的少数拥护者之一。…但从那以后，人们对进一步膨胀这种语言产生了浓厚的兴趣，而不是对它进行改进。”
…
布伦丹·艾希(Brendan Eich)在 1995 年为网景公司发明了这种语言:…“5 月份我做了 10 天的艰苦工作，我没有睡多少，”艾希在 2018 年[说]。(他)称这项工作是“一项仓促的工作”[并表示]“我知道会有错误，会有差距。”
…
随着功能的增加……JavaScript 不断发展出许多新特性……尽管兼容性的要求意味着一些缺陷无法纠正，另一方面，特性膨胀是一个持续的风险。…今天的典型应用包括使用 WebPack、Rollup 或其他捆绑器的构建过程，这与 Eich 的最初概念相去甚远。

克罗克福德与[尤里·古尔兹伊](https://evrone.com/douglas-crockford-interview "read the full text")交谈:

JavaScript 和其他恐龙语言一样，已经成为进步的障碍。我们应该专注于下一种语言，它应该看起来更像 E 而不是 JavaScript。下一种语言……需要是一种基于最小能力的 actor 语言，它是专门为安全分布式编程而设计的。不能少考虑。

等等，我们不是已经用 TypeScript 解决了这个问题吗？这是一种目光短浅的观点，斯瓦特德尔说:

TypeScript 很棒:对 JavaScript 的巨大改进，也是 web 开发的福音。…但克罗克福德在这里看得更远。像 E 这样的语言首先是为安全并发而设计的，这将是一件大事，因为我们将继续看到客户端处理核心和高度分布式后端部署的爆炸式增长。将[并发性]作为设计核心部分的语言需要更少的约束，可以提供更智能的自动化优化。我不知道 E 是否会在这个领域站稳脚跟，但这是我们前进的方向，在这个领域使用 TypeScript 并不是最自然的事情。

u/MINUS-one 说，这比坚持使用“愚蠢的”JavaScript 要好:

但他说的没错。…类、生成器、代理和… "# "私有字段(都是用函数式语言编写的，你知道，函数式语言有第一类函数，可以完成上述所有功能和几乎所有其他功能)。
…
反正反正神智正常的人都不会用 JS。至少人们使用 TypeScript。

那么，WebAssembly 呢？离开基赛的草坪:

大部分人提议将东西编译成 Wasm，这是一个巨大的错误。如果我控制了互联网，Wasm 将会是最需要被攻击的东西。为什么有人会如此愚蠢地尝试将一些东西低效地交叉编译成一种被 JavaScript 本身束缚住的伪汇编语言呢？这太愚蠢了。
…
现在 Flash 已经被“canvas 标签”所取代，[所以]你现在需要一个 300MB 的浏览器来玩一个用 JavaScript 编写的游戏，这个游戏只使用 Canvas 标签。*那是愚蠢的。* …画布标签本身就很蠢。我们有了 SVG，然后决定再次重新发明它。
……
问题不在于 JavaScript，而在于“网络浏览器”……怪明尼苏达大学毁了地鼠。

但是[u/barelyarborne](https://www.reddit.com/r/javascript/comments/wgx63z/comment/ij2npms/?utm_source=reddit&utm_medium=web2x&context=3 "read the full text")射杀信使:

我试着读过他的一本书。一次。多么令人难以忍受的****。

* * *

## 2.混合微软的表情符号

微软为其 1500 多个“流畅”3D 表情符号集申请了麻省理工学院的许可。首先在团队中看到，然后被 Windows 11 采用，雷德蒙现在希望*你*在**他们**的基础上构建。

### 分析:因为……混合工作？？？

微软表示，这样做是因为工作正在发生变化。我想这个理由和其他理由一样有道理。

[汤姆·沃伦](https://www.theverge.com/2022/8/10/23299527/microsoft-emoji-open-source-creators "read the full text") : **微软开源其 3D 表情符号**

**`Remote and hybrid work`**
微软正在开源其超过 1500 个 3D 表情符号，让创作者免费混合和制作。几乎所有微软的 1538 个表情库都将在 Figma 和 GitHub 上提供……微软希望此举将鼓励表情空间的更多创造力和包容性。
…
创作者将能够将微软大部分鲜艳多彩的 3D 表情符号重新混合成贴纸，在内容中使用，或创建独特的表情符号集。…微软的设计团队现在期待看到创作者社区如何建立其表情库。微软称其表情符号开源的部分原因是工作状态的变化。远程和混合工作迫使企业和员工以不同的方式工作，如何通过文本表达自己变得更加重要。

血统来自团队的产品。脱凡[齐格正义](https://arstechnica.com/gadgets/2022/08/microsoft-open-sources-its-cute-3d-emoji-albeit-without-clippy/?comments=1&post=41141796#comment-41141796 "read the full text"):

他们不久前袭击了我们。…他们在这里受到普遍的厌恶。
…
你见过他们为章鱼找的可怜借口吗？我不知道那是什么，但我非常确定那是什么*不是:*一只章鱼。…头足类动物统治！微软的某些人应该为此受到惩罚。

请腾出属于这个[无名懦夫](https://news.slashdot.org/comments.pl?sid=21870236&cid=62777622 "read the full text")的草坪:

表情符号正迅速成为越来越多永远依赖智能手机的人表达自己的主要方式。那些最好保持忙碌以免他们开口说粗话的人——那些具有高度敏感、前卫敏感的人——可能喜欢也可能不喜欢，可能——可能。

* * *

## 这个故事的寓意:
**魔鬼有能力呈现令人愉快的形状**

*你一直在读[里奇·詹宁斯](https://www.richi.uk/)的*远景*。你可以通过 [@RiCHi](https://twitter.com/richi) 或者 [【邮箱保护】](/cdn-cgi/l/email-protection#27534b5167554e444f4e09444809524c185452454d4244531a0a736b710a) 联系他。*

图片:[托马斯德卢泽](https://unsplash.com/photos/SQ-A6fzu3tg)(via[Unsplash](https://unsplash.com/license "Some rights reserved")；平整和裁剪)*