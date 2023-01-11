# 为什么需要 GitHub 备份？

> 原文：<https://devops.com/why-do-you-need-github-backup/>

你可能听过这样一个笑话:IT 界有两种人:做备份的人和将要开始做备份的人。尽管这个笑话仍然有效，但它已经变得与企业和专业人士不那么相关了。多年来，IT 行业一直在增加安全支出，备份是一个关键领域。然而，尽管人们越来越意识到备份的必要性，并且现代备份解决方案广泛可用，但问题仍然存在。安全漏洞的数量正在增加，数据安全的话题看起来像一场无休止的军备竞赛。那么组织能做些什么呢？

首先，我们来分析一些数据和趋势。年复一年，网络攻击，尤其是勒索软件的数量在增加。2020 年，由于疫情和远程工作的突然转变，攻击加剧，不幸的是，并不是每个人都做好了准备。一旦组织在实现有效的在家工作模式方面变得更好，一切都有望进入新常态。不幸的是，新的标准变成了这些增加的攻击。

这有点像形而上学的阴阳——两种对立但互补的力量。一个驱动另一个。可以说，2021 年勒索软件造成的全球损失估计高达 200 亿美元！全球平均每 11 秒钟就有一次勒索攻击发生。

根据身份盗窃资源中心(ITRC)的报告，到 2021 年 9 月底，此类事件比 2020 年全年都多。该报告的作者强调，他们发现了 26 个云数据库不安全的案例。结果，黑客能够访问属于 9900 万人的机密数据。

## Git 威胁:我的 Bitbucket/GitLab/GitHub 库安全吗？

回到 2019 年 5 月，勒索软件攻击影响了 GitHub、GitLab 和 Bitbucket 上的数百个存储库。这次攻击抹去了所有数据，只留下一条信息:索要的赎金数量和支付方式。最终，大部分数据都被恢复了，但是从攻击中恢复所花费的成本和时间是巨大的。

根据思科基准研究，大约 40%的公司由于重大故障经历了超过 8 小时的停机时间。39%的受访者表示，他们的系统中至少有一半受到了严重违规的影响。根据 IBM 的数据，全球范围内数据保护漏洞的平均总成本高达 386 万美元，2020 年网络犯罪分子索要的最高赎金为 1500 万美元。这些数字很吓人。另一方面，在大部分勒索软件攻击成功的案例中，最终并没有支付赎金；即使组织不支付赎金，仅仅是他们成为受害者和经历故障或停机的事实就可能非常昂贵。

## GitHub 作为备份工具

GitHub 提供了许多有用的安全工具。但是，我们必须清楚两件事:GitHub backup 到底是什么意思，它有什么特点？相对于用户的安全责任，云服务提供商的责任是什么？先说后者。

大多数云服务提供商(包括亚马逊、微软、谷歌、IBM、Salesforce、GitHub 或 Atlassian)都是在所谓的共同责任模式的基础上运营的。云服务用户通常认为提供商对他们的保护负有全部责任。但是，提供商主要只负责确保基础设施、软件和访问的安全性和可用性。用户负责作为这些服务的一部分存储的业务数据的安全性。因此，用户自己必须负责备份和灾难恢复计划和解决方案。简而言之:提供商负责云本身的安全，用户负责云中的数据安全。而在这一点上，值得指出的是，根据英国 CybSafe 的数据，在 2019 年，90%的数据泄露是由用户错误造成的。

它可能发生在我们任何人身上——勒索软件攻击、网络钓鱼、无法访问 GitHub 帐户或整台计算机，或者只是在存储库中覆盖另一个开发人员的工作。它既影响个人用户，也影响大公司。2019 年 7 月， [Ubuntu Security 报告了](https://twitter.com/ubuntu_sec)一个公司所有的 GitHub 帐户的凭据遭到了破坏。黑客使用这些泄露的凭据创建存储库、问题、拉式请求等。这次攻击没有造成大的崩溃，但是修复损坏需要一些工作，并且将一些存储库或问题跟踪器恢复到以前的状态是很困难的。

任何好的备份都应该具有一些共同的特征:

*   自动化(即每日备份)
*   使用自己的加密密钥进行 AES 加密
*   版本控制
*   长期数据保留
*   灾难恢复过程
*   易于监控(审计日志、电子邮件通知)
*   中央管理
*   多租户(管理管理员、权限和角色)
*   可量测性

根据这些标准，GitHub(和其他类似的托管服务)不能被认为是一个合适的备份工具。GitHub 是一个很棒的开源项目，但是它的目的完全不同。

## 如何手动备份

既然云服务本身不够用，那如何打理 GitHub 备份呢？你可以自己做。通常，尤其是在小型企业中，这是首选方法。乍一看，这似乎是个好主意。了解 Git 之后，我们可以创建适当的脚本来为我们创建备份，这样我们就可以完全控制正在发生的事情，而无需向任何人付费。但从长远来看，这是非常冒险且无利可图的。磁盘空间要花钱；我们员工创建脚本和执行备份的时间是另一项成本。在这种情况下，最重要的是，这些脚本必须一直维护和更新，因此它们不断产生额外的成本。这种脚本中的任何改变都可能导致错误，并因此剥夺组织的工作备份。当然，您也可以创建一个适当的机制来测试它，但这是一个额外的成本。手动 GitHub 备份不会以编写一个脚本结束。

我自己也经历过这种情况。在一个项目中，使用这样的脚本生成备份，然后保存在我们自己的服务器上。这样更便宜。但是我们没有对创建的备份进行任何验证。有一天，在更新备份脚本时，我们做了一个手动测试，结果发现我们有一个严重的问题——备份创建正确，但其名称没有改变，所以我们不断地覆盖同一个归档文件！效果？原来我们一个月以上的都没有！幸运的是，我们并不需要它们，因为当时系统和数据库工作正常，没有发生任何事故，但这让我一想到“如果……”就感到害怕

总而言之，出于多种原因，手动编写备份脚本并不是一个好主意。这种解决方案的低成本只是理论上的；随着时间的推移，维护这种机制的成本会增加，而且在实践中，通常只有一两个人负责这种机制，这就产生了额外的风险。好吧，你可能有更多的控制权，但总的来说你是在浪费时间和金钱。备份本身也是不够的，因为在发生事故时，您需要一个适当的系统或数据恢复解决方案。还有一个问题是，如何为创建备份的脚本创建备份？你确定你不能更好地利用员工的工作时间吗？

## 这要花多少钱？

这一点很难准确衡量；这完全取决于系统的复杂程度、存储库的数量、团队的技能等等。然而，你*可以*估计缺少对服务的访问或者程序员的停机时间会造成多大的损失。您还可以计算编写、测试、维护和更新您自己的备份脚本的开发和维护成本。GitHub 攻击和崩溃的历史表明，数据通常是可恢复的，这是一个好消息。另一方面，当服务不可用或团队无法工作时，成本会非常高。

## 第三方 GitHub 备份工具

另一个解决方案，也是我认为更好的一个，是使用第三方备份软件。

事实上，在 GitHub 文档中，建议:

备份存储库:您可以使用 API 或第三方工具来备份您的存储库

如果可以使用 GitHub API，为什么还需要第三方 GitHub 备份工具？首先，这类应用程序是由特定领域的专家创建的，他们拥有知识和经验，并紧跟当前的安全趋势。第二，这些解决方案是现成的，可以马上使用；你不必花费时间和金钱去重新发明轮子。是的，这是有成本的，但从长远来看(考虑到前面描述的因素)，成本通常会比定制解决方案低得多。外包备份管理职责可能会带来难以置信的好处，并允许我们专注于发展我们的业务，而不是重新管理 GitHub 存储库备份。

说到备份，要聪明。如果外部第三方工具可以让我们更快更高效地开发产品，那么我们应该毫不犹豫地使用它们。永远不要忘记实施适当的备份和灾难恢复计划。今天照顾好它将有助于确保一个更安全的未来。