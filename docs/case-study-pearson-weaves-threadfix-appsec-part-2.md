# 案例研究:Pearson 将 ThreadFix 编入 AppSec，第 2 部分

> 原文：<https://devops.com/case-study-pearson-weaves-threadfix-appsec-part-2/>

在[第一部分](https://devops.com/2016/02/12/case-study-pearson-weaves-threadfix-appsec-part-1/)中，我们讨论了教育内容出版商[培生](https://www.pearson.com/)如何将 [ThreadFix](http://www.threadfix.org/) 应用于其 AppSec 请求工作流需求。接下来的故事是这样的。

## ThreadFix 实现

高级软件安全工程师 Matt Tesauro 通过以下步骤将 ThreadFix 添加到 Pearson 的工作流程中:

1.  使用 [FPM，](https://github.com/jordansissel/fpm) Tesauro 在内部创建了一个 [Debian Linux](https://www.debian.org/) 包来部署 ThreadFix [Tomcat](https://tomcat.apache.org/) 包(ThreadFix 也为此提供了自己的 Debian 包)。
2.  Tesauro 使用 ThreadFix 理解的工具扫描文件格式将 ThreadFix 与 Pearson 的每个工具集挂钩。
3.  使用 ThreadFix 内置的导入器，特索罗将其连接到皮尔森使用的 [Checkmarx](https://www.checkmarx.com/) 、 [Veracode](https://www.veracode.com/) 、 [BurpSuite](https://portswigger.net/burp/) 、 [ZAP](https://www.owasp.org/index.php/OWASP_Zed_Attack_Proxy_Project) 、WhiteHat、 [AppScan](https://www-03.ibm.com/software/products/en/appscan) 和 [Qualys](https://www.qualys.com/) 测试工具。
4.  为了实现这一点，Tesauro 将 ThreadFix 指向了一个 API。
5.  然后特索罗设置了一个 API 密匙。
6.  然后，系统被设置为获取测试结果。
7.  如果有必要，Tesauro 编写 glue 代码将结果上传到 ThreadFix。

Pearson 使用 ThreadFix 对来自手动评估、应用程序动态扫描和源代码静态代码分析的内容进行标准化和重复数据删除，并将这些输出导入 ThreadFix。“因此，如果一个静态工具和一个动态工具都发现了相同的跨站点脚本问题，我们将这些问题输入 ThreadFix，它会对这些问题进行重复删除，并只给我们一个问题来报告，这样我们就不会因为修复同一个编码错误而埋葬两个团队，”Tesauro 说。

“ThreadFix 成为我们团队所有产出的一个知识来源，对我们来说，就是我们在自己创建、购买或让第三方创建的应用程序中发现的安全漏洞，”Tesauro 说。这使得 Pearson 的 AppSec 团队能够将开发团队的订单输入到 JIRA 的积压订单中，这使得生成指标和做报告变得更加容易。ThreadFix 使向治理、风险和合规工具(如 [RSA Archer](http://www.emc.com/security/rsa-archer-governance-risk-compliance/index.htm) )提供数据变得更加容易。“这使得我们能够了解正在进行的工作和工作流程，以及影响 AppSec 工作的业务领域，”Tesauro 指出。

## ThreadFix 的附加功能

Tesauro 最终将 ThreadFix 扩展到 AppSec 以外的其他部门，以受益于它的功能和它可以产生的关于应用程序进度的指标。

Tesauro 注意到了 AppSec 管道中“持有的袋子”和 ThreadFix 之间的一点，这需要一些工作。他使用了一个 [StackStorm](https://stackstorm.com/) orchestration 和分层 [ChatOps](https://github.com/StackStorm/showcase-ansible-chatops) 在流程的这一点上支持新的开发者功能。

“现在，您可以进入我们的私人渠道，使用 [HipChat](https://www.hipchat.com/) 询问系统，例如，为特定业务部门的特定应用程序设置 Checkmarx。您给它一个指向该单元的 Git 存储库的 URL 指针，然后系统开始运行，在 Holding 包和 ThreadFix 中设置应用程序配置文件，然后与 Checkmarx 对话，设置对位于主分支上的代码的每周扫描。它在一分钟内就完成了所有的设置，”特索罗说。

HigherEd 是 Pearson 内部第一个从 ThreadFix metrics 中获益的小组。根据 Tesauro 的说法，其中一个指标是在组合中加入 JIRA 集成后，修复时间减少了 44%。“一旦我们开始产生这些数字，我们有许多其他业务单位问，‘嘿，为什么 HigherEd 得到这些伟大的时间修复数字？我们希望我们的应用程序也能使用它们，”“这是获得认同的好方法，”特索罗说。

## 进一步的结果

Tesauro 指出，AppSec 的请求工作流吞吐量增加了 5 倍，从 2014 年的 44 项应用评估减少到 2015 年的不到 200 项。

“2015 年，我们失去了两个半人，但仍加快了进程，”他表示。