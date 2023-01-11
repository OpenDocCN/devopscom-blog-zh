# 我们真正需要的扫描仪

> 原文：<https://devops.com/the-scanner-we-really-need/>

它有扫描所有东西的扫描仪。我说的一切，是指一切。我们扫描源代码寻找漏洞和数据泄露。我们扫描应用程序的漏洞。我们扫描网络寻找漏洞。我们扫描我们的卡进行访问…好吧，最后一个不适合，但你得到的想法。

知道我们不扫描什么吗(我建议我们立即开始扫描什么)？秘密。哦，有些应用程序将寻找秘密作为其功能集的一部分，但只是一部分，它们只扫描其领域内的秘密。我们真正需要的是包罗万象的东西。秘密有办法出现在任何地方——Git、平面文件、数据库、源代码、电子邮件……如果它可以存储文本，你的秘密可能就在那里。组织越大，越是如此。

很久以前，我开始在一家公司工作，该公司将大型机管理员凭据存储在网络上的平面文件中。我不是信息安全公司的员工，但我能很容易地嗅到不安全感，我告诉他们别再这样了。

我没有提到这家公司的名字，因为这并不代表他们今天的做法，我也没有提到我的职位或市场，因为任何感兴趣的人都可以使用我的 LinkedIn 个人资料来找出是谁。

以我在那里的角色，我有权告诉他们停止，但他们给了我一个现成的回应:“我们的网络是安全的，所以我们不必担心。而且我们监控文件…有些…”

同样类型的心态似乎渗透到今天。关于秘密，默默无闻的安全性仍然存在，但我们作为一个行业知道(从辛苦获得的经验)这在很大程度上是一个神话。

因此，我们需要一个工具，可以访问所有秘密可能隐藏的地方，并找出它们——我认为像一个简单的 UI，可以获取秘密并在所有配置的地方搜索它——将是完美的。嗯，几乎完美。迭代 2.0 将报告在那个位置什么正在访问秘密。

获取[机密管理](https://devops.com/?s=secrets+management)。一些市场将秘密管理作为工具集的一部分提供，你甚至可能拥有一个可以为你做这件事的产品。然后，给定搜索工具和良好的机密管理解决方案，您可以搜索出所有实例并替换对它们的访问。在迭代 2.0 出来之前，您可以在测试环境中替换它们，看看有什么问题——尽管我们也有来之不易的经验，知道这不是万无一失的，所以您会希望大量记录从现在起 20 个月内发生的奇怪事情的变化。

这不是一个很难设计和制造的产品；找到每个秘密是从哪里获取的将是最困难的部分。但是用我们当前的开发工具这仍然是可行的。你们中的一个应该建造它并且变得富有。

但与此同时，一如既往，继续摇摆。无论秘密存储在不那么秘密的地方与否，你都在让公司日复一日地运转。这让你成为商业明星。继续努力。