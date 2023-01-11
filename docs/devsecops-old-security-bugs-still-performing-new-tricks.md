# DevSecOps:旧的安全漏洞仍在上演新把戏

> 原文：<https://devops.com/devsecops-old-security-bugs-still-performing-new-tricks/>

***新的安全漏洞潜入可靠的旧系统*** 

在网络安全中，我们经常像猎人一样。我们的眼睛紧紧盯着地平线，扫描下一个爆发的漏洞(以及正确的设计工具、技术和策略来阻止它)。然而，这种前瞻性的关注可能会产生令人惊讶的效果，削弱我们的整体安全意识，使我们对周围存在的根深蒂固的危险视而不见，而攻击者非常乐意利用这些危险。

我经常把现代网络安全比作一套凯夫拉尔盔甲。凯夫拉纤维看似轻盈的特性可以阻挡高速子弹和各种现代强力武器。它甚至会让佩戴者感到有些不可战胜。然而，一种相对古老的弓箭武器系统，最早制作于公元前 1000 年左右，通常可以穿透这种保护。一把锋利的刀，可能是世界上仅次于岩石的第二古老的武器，可以轻松地切开凯夫拉尔纤维，就像撕碎一件棉运动衫一样。还有一个小问题，凯夫拉尔不能保护人体的每一毫米。如果攻击者可以找到任何漏洞来进行破坏性的打击，他们就会这样做——就像软件中的小的、可利用的区域一样。

在网络安全领域，许多组织同样容易受到使用了 8 年或 10 年的系统缺陷的影响，用现代计算术语来说，这些系统足以让他们获得金表和养老金。但是如果你认为这些老系统的缺陷是无害的，那么你很可能在未来遇到一两次蓝屏死亡。

## **一个老兵的漏洞**

最古老和最常用的 JavaScript 库之一是 jQuery，它是一个开源资源，可以帮助完成从事件处理、DOM 树遍历和操作到生成动画的所有事情。这是一个相当大的工作量，并已使用多年。人们认为，因为这个库在这一点上已经建立起来了，所以它一定已经被完全检查过了，所有的漏洞都被删除了。

可悲的是，事实并非如此。默认情况下，大多数依赖 jQuery 的应用程序使用内部库的指令进行身份验证。例如，对于 Apache 服务器，这意味着检查。htaccess 文件。很少有开发人员在设计使用 Apache 的程序时会想到检查以确保 Apache 服务器更新包含. htaccess。毕竟，Apache 为什么要删除这个关键的组件，而这个组件多年来一直是安全的基石呢？

尽管看起来很奇怪，但这正是 Apache 在版本 2.3.9 中所做的。很明显，必须检查。每次程序需要运行时，htaccess 配置文件会大大降低速度。删除它提高了 Apache 的整体性能，但是也产生了一个大多数人不知道的漏洞。如果开发人员懒得检查他们的应用程序是否还能到达。htaccess 文件，大多数请求会被简单地接受，没有审查。

最近，专家 [发现了这个缺陷](https://blogs.akamai.com/sitr/2018/10/having-the-security-rug-pulled-out-from-under-you.html) ，并指出使用它将允许未经授权的用户上传和运行外壳或几乎任何类型的代码在据称安全的系统上。这导致 10 月份创建了一个名为 CVE-2018-9206 的漏洞警报。但是，安全研究人员很容易就发现了这个漏洞，这意味着专业黑客可能已经发现了这个漏洞，他们的唯一目标就是搜索这样的漏洞。毕竟，尽管随后进行了宣传、修补和修复，但仅几周之后，一次类似的高影响力攻击发生了，在那次攻击中， [盗窃比特币的恶意软件](https://www.theregister.co.uk/2018/11/26/npm_repo_bitcoin_stealer/) 被释放到一个每周有数百万人下载的流行的 NPM 库上。

## **管家做到了**

像 jQuery 一样，Jenkins 是一个开源产品，也是同类产品中最受欢迎的产品之一。凭借其有用的仆人般的名字，Jenkins 被许多行业的开发团队用作自动化服务器是有道理的。当 Jenkins 正常工作时，这是一个非常有用的工具。然而，新发现的漏洞，以及最近发现的规模真正庞大的 加密挖掘操作 [，表明詹金斯也在为坏人做大量工作。](https://www.csoonline.com/article/3256314/security/hackers-exploit-jenkins-servers-make-3-million-by-mining-monero.html)

最危险的 Jenkins 漏洞之一叫做 Java 反序列化， [被指定为](https://www.exploit-db.com/exploits/41965/) 为 CVE-2017-1000353。这是一种复杂的攻击，但已经存在了一段时间。攻击者必须提交两个请求。第一个启动双向下载通道，最初被服务器拒绝。但是，第二个请求添加了一个上传通道，其中包含一个带有攻击者想要的任何命令的有效负载，并利用了 payload.jar 脚本。一旦发送了第二个请求，就允许在未打补丁的 Jenkins 服务器上进行通信。

即使在打补丁的服务器上，漏洞也是存在的。例如，在 Windows 环境中运行 Jenkins 时，默认情况下它使用 NT AUTHORITYSYSTEM 帐户来授权用户。这很危险，因为系统在 Windows 服务器上被授予完全权限。开发人员可以更改权限帐户，但通常不会。他们不这样做的逻辑是基于这样一个事实，即 Jenkins 一直存在，所以人们认为任何漏洞在很久以前就已经被修补了。

最近，一名黑客利用这些老化的 Jenkins 漏洞危害了几台服务器。目标是在他们能找到的每个易受攻击的 Jenkins 实例上添加一个加密挖掘程序。矿工们在不断寻找加密货币的过程中占用了宝贵的计算资源。到目前为止，他们 [已经发现](https://www.csoonline.com/article/3256314/security/hackers-exploit-jenkins-servers-make-3-million-by-mining-monero.html) 大约 10800 枚莫内罗加密硬币，价值将近 350 万美元。

## 旧的又是新的

在这两个例子中，许多人认为安全的平台上的漏洞正被机会主义攻击者利用。从防御的角度来看，缺乏安全意识的开发让这些黑客给老把戏注入了新的活力。尽管利用老化漏洞取得了新一轮的成功，但许多组织还没有制定计划来阻止这种恶性循环。

仅仅因为一些东西是旧的并不意味着它是无害的。并且仅仅因为通用库和资源已经存在多年并不意味着它们是完全安全的(例如，当前 OWASP top 10 中的第 9 项是专门使用具有已知漏洞的组件 来处理 [)。只有通过勤奋和持续的安全训练，我们不仅可以保护自己免受潜在的危险威胁，还可以抵御那些已经潜伏在我们后院的威胁。](https://www.owasp.org/index.php/Top_10-2017_A9-Using_Components_with_Known_Vulnerabilities)

彼得·丹纽斯