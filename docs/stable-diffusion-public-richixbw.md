# 稳定扩散公开化——互联网吓坏了

> 原文：<https://devops.com/stable-diffusion-public-richixbw/>

欢迎来到[![](img/7f2530df5c3f9aa2f4621cff38e5dcff.png)](https://devops.com/tag/the-long-view/)*——在这里我们细读本周新闻，并将其剥离至要点。让我们弄清楚**什么是真正重要的**。*

## *本周:一场*稳定扩散*特别*

*除非你过去一周一直生活在岩石下，否则你会看到关于稳定扩散的某些东西。这是新的开源机器学习模型，用于从文本**甚至其他图像**中创建图像。*

 *### 分析:开源是关键

就像 DALL-E 和 Midjourney 一样，你给它一个文本“提示”,它就会生成令人惊奇的图像(或者有时完全是垃圾)。与其他模型不同，它是开源的，所以我们已经看到了创新的爆发。

马克·哈奇曼称之为****新杀手级应用****

****`Fine-tune your algorithmic art`**
艾的艺术令人着迷。输入一个提示，算法将生成一个符合您要求的图像。一般来说，这一切都发生在网络上，有 DALL-E 这样的算法[但是]稳定。Ai 及其稳定的扩散模型打破了这种模式……一个公开可用的模型*和*可以在消费级 GPU 上运行。
…
目前来说，稳定。Ai 建议你拥有至少 6.9GB 显存的 GPU。遗憾的是，目前只支持 Nvidia GPUs。(但)如果你拥有一台功能强大的电脑，你可以尽情地调整你的算法艺术，想出一些真正令人印象深刻的东西。**

 **从马嘴里说出来的，是[艾玛德莫斯塔克](https://stability.ai/blog/stable-diffusion-public-release "read the full text") : **稳定扩散公开发布****

****`Use this in an ethical, moral and legal manner`**
我们荣幸地宣布稳定扩散的公开发布。…在过去的几周里，我们都被回应所淹没，并一直在努力工作，以确保安全和道德的发布，整合来自我们的 beta 模型测试和社区的数据，供开发人员采取行动。
…
由于这些模型是在广泛的互联网搜索中对图像-文本对进行训练的，因此模型可能会重现一些社会偏见并产生不安全的内容，因此开放的缓解策略以及对这些偏见的公开讨论可以让每个人都参与到这场对话中来。…我们希望每个人都能以符合伦理、道德和法律的方式使用它，并为社区和围绕它的讨论做出贡献。**

 ***对，对。*你上过互联网吗？[凯尔·威格斯](https://techcrunch.com/2022/08/24/deepfakes-for-all-uncensored-ai-art-model-prompts-ethics-questions/ "read the full text")听起来很担心:**为所有人做假动作****

****`90% are of women`**
稳定扩散…现在被 Artbreeder、Pixelz.ai 等艺术生成器服务使用。但是这个模型未经过滤的特性意味着并非所有的使用都是光明正大的。其他人工智能艺术生成系统，如 OpenAI 的 DALL-E 2，已经对色情材料实施了严格的过滤。…此外，许多人没有能力创造公众人物的艺术。……不幸的是，女性最有可能成为这种情况的受害者。2019 年进行的一项研究显示，在 90%至 95%的非自愿深度假货中，约 90%是女性。**

**为什么这是一件大事？问问[西蒙·威廉森](https://simonwillison.net/2022/Aug/29/stable-diffusion/ "read the full text"):**

****`Science fiction is real`**
稳定扩散确实是一件大事。如果你没有注意到正在发生的事情…你真的应该注意了。…它类似于 Open AI 的 DALL-E 等模型，但有一个关键的区别:他们发布了整个东西。短短几天内，围绕它的创新出现了爆炸式增长。人们正在建造的东西绝对令人震惊。…从文本生成图像是一回事，但从其他图像生成图像是另一回事。…想象一下，有一个按需的概念艺术家，可以生成任何你可以想象的东西，并可以与你一起迭代，实现你的理想结果。科幻小说现在是真实的了。机器学习生成模型在这里，它们改进的速度是不真实的。值得真正关注。**

**它与 DALL-E 相比如何？只要问一下[比昂多](https://petapixel.com/2022/08/22/ai-image-generators-compared-side-by-side-reveals-stark-differences/#comment-5960401911 "read the full text"):**

**个人认为稳定扩散比较好。… OpenAI 听起来像是他们创造了图像生成模型的圣杯，但他们的图像不会给任何使用稳定扩散的人留下印象。**

 **[@fabianstelzer](https://twitter.com/fabianstelzer/status/1561019187451011074 "read the full text") 做了一堆对比测试:**

**这些图像合成器就像乐器一样——令人惊讶的是我们会有这么多这样的合成器，每一个都有独特的“声音”… DALL-E 非常适合面部表情。[Midjourney]与其他人一起擦地板，当涉及到…针对纹理细节的提示时。… DALL-E 通常是我在涉及两个或更多明确“演员”的场景中使用的… DALL-E 和 SD 更擅长拍照…稳定的扩散可以拍出令人难以置信的照片…但你需要小心不要让场景“过载”。当你把“艺术”放进提示时，中途就发疯了。… DALL-E 的不完美看起来非常数码化，不像 MJ 的。…说到复制特定的风格，SD 绝对是🤯🤌 (但是)达勒不会让你画一幅波提切利的川普像。**

 **那么训练数据呢？这是安迪·拜奥:**

**文本到图像生成人工智能模型的最大挫折之一是，它们感觉像一个黑匣子。我们知道他们是在网上的图片上接受训练的，但是是哪些图片呢？Stable Diffusion 背后的团队对于他们的模型是如何被训练的非常透明。自从上周公开发布以来，稳定扩散已经大受欢迎，很大程度上是因为它的免费许可。西蒙·威廉森[和我]收集了超过 1200 万张用于训练稳定扩散的图像数据。它是由 LAION 收集的三个大规模数据集训练出来的。LAION 的所有图像数据集都是基于 Common Crawl 构建的，[它]每月抓取数十亿个网页，并将其作为海量数据集发布。……近一半的图片，约 47%，仅来自 100 个领域，其中来自 Pinterest 的图片数量最多。… WordPress 托管的 wp.com 和 wordpress.com 博客占所有图片的 6.8%。其他照片、艺术和博客网站包括……Smugmug……Blogspot……Flickr……DeviantArt……Wikimedia……500 px 和……Tumblr。**

**与此同时，它是如何工作的？对她来说，Letitia Parcalabescu 说起来容易:**

**潜在扩散模型是如何工作的？如果你想知道这些问题的答案，我们已经为你准备好了！**

 **[https://www.youtube.com/embed/J87hffSMB60?feature=oembed](https://www.youtube.com/embed/J87hffSMB60?feature=oembed)** 

* * *

## **这个故事的寓意:
**这些凡人多么愚蠢****

 ***你一直在读[里奇·詹宁斯](https://www.richi.uk/)的*远景*。你可以通过 [@RiCHi](https://twitter.com/richi) 或者 [【邮箱保护】](/cdn-cgi/l/email-protection#c4b0a8b284b6ada7acadeaa7abeab1affbb7b1a6aea1a7b0f9e9908892e9) 联系他。***

**图片:稳定扩散，via [安迪拜奥](https://waxy.org/2022/08/exploring-12-million-of-the-images-used-to-train-stable-diffusions-image-generator/) ( [创意 ML OpenRAIL-M](https://huggingface.co/spaces/CompVis/stable-diffusion-license "Some rights reserved")；平整和裁剪)***