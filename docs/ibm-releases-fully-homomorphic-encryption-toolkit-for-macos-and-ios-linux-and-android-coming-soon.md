# IBM 发布 MacOS 和 iOS 全同态加密工具包；Linux 和 Android 即将推出

> 原文：<https://devops.com/ibm-releases-fully-homomorphic-encryption-toolkit-for-macos-and-ios-linux-and-android-coming-soon/>

2020 年 6 月 4 日|作者:[弗拉维奥·贝尔加玛斯基](https://www.ibm.com/blogs/research/author/flavio-bergamaschi/ "Posts by Flavio Bergamaschi")

通常，当我第一次开始向某人解释[全同态加密](https://www.research.ibm.com/labs/uk/fhe.html) (FHE)时，我会说我已经在这个领域工作了近十年，然而，我仍然必须停下来拼写正确。所以，就叫它 FHE 吧。

半开玩笑地说，当你第一次听说 FHE 时，它听起来真的很神奇，但它实际上是基于非常可靠的数学。主要区别在于，FHE 要求我们习惯的编程范式发生转变，这使得集成到应用程序中变得更加困难。这要归功于我们正在为 MacOS、iOS 以及即将到来的 Linux 和 Android 开发的新工具包。事实上，熟悉基本平台工具的开发人员可以按照几个简单的指令很快上手并运行*(见下面的视频)*。将 11 年来顶尖的密码学研究成果整合到一个简化的开发人员体验中，这是一个不小的壮举，在大多数人泡一壶咖啡或整理桌子的时间里，任何人都可以访问和免费使用这个体验。

什么是 FHE？

与同事和合作伙伴存储和共享敏感数据的常用方法存在薄弱环节。如今，文件通常在传输和存放时被加密，但在使用时会被解密。这为黑客和内部人员提供了反复泄露未加密数据的机会。FHE 堵住了这些漏洞。它允许被许可方在数据保持加密的情况下对其进行操作，从而最大限度地缩短数据处于最脆弱状态的时间。

结合其他技术，FHE 还使得有选择地限制解密能力成为可能，因此人们只能看到他们有权看到的文件部分，以及他们工作所必需的部分。

**20 世纪 70 年代&超越**

FHE 在 20 世纪 70 年代末首次被讨论，但真正的突破是在 2009 年 5 月 31 日举行的第 41 届^第 ACM 计算理论研讨会上，密码学家 Craig Gentry 在他被高度引用的开创性论文 [*中首次展示了使用理想格的全同态加密*](https://www.cs.cmu.edu/~odonnell/hits09/gentry-homomorphic-encryption.pdf) 。

虽然这篇论文是令人兴奋的消息，但业内许多人认为 FHE 将继续留在加密书架上，因为由于计算的复杂性和它需要的巨大计算能力，它对于日常使用来说太慢了。值得庆幸的是，IBM Research 的一个小团队将此视为一项挑战，十年后，FHE 的性能已经提高到足以满足某些应用的水平，这只会随着算法的进步和未来的硬件加速器而提高。

**用例**

FHE 为许多用例带来了巨大的希望，例如从私有数据中提取价值；数据集交集；基因组学分析；明显的查询(即不透露意图的查询)和安全外包。

FHE 特别适合那些受到监管并使用私人、机密和“皇冠上的宝石”数据的行业，如金融和医疗保健，因为该技术可以广泛共享财务信息或患者健康记录，同时限制对除必要数据之外的所有数据的访问。

例如，我们最近[与](https://eprint.iacr.org/2019/1113.pdf)[巴西的 Banco Bradesco SA](https://medium.com/@IBMResearch/top-brazilian-bank-pilots-privacy-encryption-quantum-computers-cant-break-92ed2695bf14) 发表了一篇论文，在论文中，我们对数据和模型进行了同态加密，并证明了在没有加密的情况下也能以同样的精度和足够的性能进行预测。结果，银行可以安全地将运行预测的任务外包给不可信的环境。

向我展示工具包

适用于苹果操作系统(MacOS)和苹果操作系统(iOS)的新 FHE 工具包已经在 GitHub 上发布，Linux 和安卓系统预计将在几周内发布。每个工具包都基于 [HELib](https://github.com/homenc/HElib) ，世界上最成熟和最通用的加密库，包括样本程序，使编写基于 FHE 的代码更容易。

iOS 工具包包括一个简单易懂的演示，演示了对加密数据库的隐私保护搜索。该数据库是一个关键值存储库，预先填充了欧洲各国及其首都的英文名称。选择国家将执行匹配首都的搜索。

我应该指出，这些都不是完美的或最终的。我们希望快速地将它们发布出来，让技术进入早期采用者的手中，他们希望在我们寻求建立用户和用例社区时，使这些概念不那么抽象，而是更加具体。

从开发者的角度来看，请阅读我的同事伊莱·道的这个 [Q & A，如果你有任何问题，请加入我们的](https://developer.ibm.com/blogs/new-open-source-security-tools-let-you-develop-on-encrypted-data.) [Slack 社区。](https://fhekit.slack.com/join/shared_invite/zt-e35rax8l-_ZbB2XuF3WcXCM2mDe~AZQ#/)

对持续培训、知识转移和联合开发感兴趣的客户可以注册[订阅](https://www.zurich.ibm.com/securityprivacy/securitysubscription.html)FHE 2020-研究参与计划。