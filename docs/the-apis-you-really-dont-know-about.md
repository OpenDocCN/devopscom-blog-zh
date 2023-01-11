# 你真的不知道的 API

> 原文：<https://devops.com/the-apis-you-really-dont-know-about/>

几年前，我们得到了关于我们的 API 所产生的暴露量的警告。一个大规模的攻击面，通常使用“隐蔽安全”作为其主要的保护方法。从那时起，我们已经走了很长的路，在我们的 API 接口中构建了秘密、令牌、RBAC 等等。

我们在获取全面的 API 列表方面仍然落后，但随着时间的推移，这一点正在变得更好。API 管理和 [DevSecOps](https://devops.com/?s=DevSecOps) 市场正越来越多地帮助对新的 API 进行分类，API 管理和应用以及 API 保护市场正通过跟踪网络中的调用来帮助保护未知的 API。通过使用代理，捕捉对 API 的调用并报告 API 列表(有时更多；例如，关于参数和数据传输)给安全或操作人员。

总而言之。API 管理和安全市场已经做了大量的工作，搜索出在我们的系统中活跃的各种 API，并在创建新的 API 时对它们进行编目。这让我们对当前的 API 环境以及如何保护它有了一个舒适而完整的了解。这些工具中的大多数都有助于保护目前没有得到很好保护的内容。

要是我们网络中的所有 API 都是真的就好了。不幸的是，事实并非如此。因为不在这个“完整列表”中的可能是最阴险的。和往常一样，你不知道的东西会带来最大的风险。

你看，有一些 API 目前没有被维护，也没有被主动访问。假设您有一个从第三方安装的应用程序——开源的或购买的——然后停止访问。它还在外面。API 是可用的——不一定有文档记录，也不一定是安全的。对于安保人员来说，噩梦就是这样开始的。

从历史上看，我们可以指望这些接口是私有的。在混合环境中，那些日子早已一去不复返。它们可能是私有的，但是“私有”的定义比历史上宽松得多，如果有从互联网到 API 的路径，它就不是私有的，并且对于众所周知的应用程序来说，这是一个定时炸弹。

这是清除旧版本和/或冗余安装的 web 服务器和数据库的另一个原因。不要找借口——只要将它们升级到最新版本或者完全删除它们。为此，您可以将他们所做的与更新/更好保护的安装合并，或者停止他们并修复受此影响的应用程序。“关掉它，看看有什么东西坏了”诚然是一个冒险的步骤，但有时会被证明是锁定环境所必需的。如果你不知道是什么在使用它，我会说你的安全风险比无保护的 API 更大，但那是另一个博客的话题。

同时，继续摇摆。在你的权限范围内有如此多的东西，以至于我们不得不讨论在你是专家的领域内你所不知道的东西。这不是你的弱点，这是一个声明，说明在使组织更具竞争力的同时，你的盘子里扔了多少垃圾。你正在处理这件事。所以微笑，继续踢，锁定可怕的部分。