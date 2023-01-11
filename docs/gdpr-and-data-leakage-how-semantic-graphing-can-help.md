# GDPR 和数据泄漏:语义图形如何帮助

> 原文：<https://devops.com/gdpr-and-data-leakage-how-semantic-graphing-can-help/>

推动软件开发生命周期效率的现代应用开发的许多标志(敏捷、CI/CD、微服务、云基础设施、开源库和第三方 API)也带来了巨大的数据泄露风险。与此同时，于 5 月 25 日生效的欧盟《通用数据保护条例》( GDPR)提出了保护比以往更多类型数据的需求，并对违规行为处以最严厉的处罚:€2000 万欧元，或高达公司全球收入的 4%。

## **防止数据泄露越来越难** 

数据泄露对开发人员来说变得更具挑战性有三个主要原因:复杂性、速度和外部服务。

随着组织采用微服务架构，应用程序本身变得更加复杂。虽然这使开发人员更有效率，但也经常导致应用程序的视图更加孤立，而数据流变得更加复杂。例如，在更广泛的应用中，有多少组织了解每个微服务的每个入口点、出口点和变量处理？此外，采用开源来提高效率而不必重新发明无差异代码的组织通常无法全面深入地理解第三方代码。这使得理解数据流更加困难。

不断加快的发布速度加剧了复杂性问题。许多组织现在每月、每周甚至每天发布。由于除了满足功能期限之外，关注任何事情的时间越来越少，映射数据流经常成为事后的想法。此外，即使一个组织能够在任何给定的时间点完整地映射其数据流，变化的速度也使得它不可能保持领先。

随着组织采用第三方服务来实现代码库、日志记录、数据库和分析等关键功能，数据泄露的后果变得非常严重。例如，优步将 AWS 凭据泄露到 GitHub，坏人可以通过登录 GitHub 发起攻击，导致 5700 万条记录被泄露。

## **为什么 GDPR 与众不同**

GDPR 在许多方面都是对以前的数据保护法规的重大扩展。与美国的健康保险流通与责任法案(HIPAA)和支付卡行业数据安全标准(PCI DSS)不同，GDPR 适用于全球和各行各业。任何持有或处理欧盟居民数据的公司都要遵守该法规。基于云的软件本质上更加全球化，许多美国或亚洲组织的用户是欧盟居民。

GDPR 大大扩展了需要保护的东西的定义。HIPAA 和 PCI DSS 制定了保护医疗保健和信用卡数据的正式规则。然而，GDPR 将必须保护的数据扩展到可以用来识别个人身份的任何内容，包括姓名、照片、电子邮件地址、银行详细信息、社交网站上的帖子、医疗信息或计算机 IP 地址。

GDPR 有真正的牙齿。对公司的罚款最高可达其全球年收入的 4 %,对严重违规公司可罚款 2000 万€，对轻微违规公司可罚款全球收入的 2%。鉴于现代云应用的全球性，GDPR 的潜在影响是深远的。

## **防止数据泄露的传统方法**

防止数据泄露的传统方法主要集中在充当应用程序和世界其他部分之间的代理。在这种情况下，代理可以尝试过滤数据并寻找模式。这些方法是由外向内的。他们并不试图理解应用程序本身；相反，它们检查来自应用程序的流量，而不考虑上下文。

首先，让我们澄清一下，尽管听起来名称相似，但防止数据泄漏并不等同于数据丢失防护(DLP)。Vontu(现在的赛门铁克)和云访问安全代理(CASBs)等传统 DLP 供应商正在解决一个不同的问题。它们是一种以 IT 为中心的解决方案，用于防止恶意或意外的数据泄露，这些数据泄露通常是由最终用户通过电子邮件或文件共享移动文档引起的。这些工具并不是为了防止应用程序本身泄漏数据而设计的，它们对开发人员来说用处不大。

更多特定于应用程序的识别数据泄漏的尝试是通过 web 应用程序防火墙(WAFs)进行的。作为代理，WAFs 通常采用模式匹配技术，例如在假设它可能是支付卡的情况下寻找 16 位数字、关键字匹配、指纹识别和其他统计内容分析技术。实际上，这些方法是无效的，因为它们产生了太多的假阳性。此外，加密是有问题的，因为晶片不能检查数据，或者必须在中间设置解密人，这在计算上是昂贵的，并且会增加等待时间。对于监控电子邮件的传统 DLP 解决方案来说，延迟可能无关紧要，但对于管理云应用的开发人员来说，延迟至关重要。

一种识别数据泄漏的传统方法是污点跟踪，它评估预先存在的二进制文件。实际上，污点跟踪是不切实际的，因为过多的性能成本和由于污点扩散(从应用程序到 web 框架再到内核)而导致的大量误报。

污点和信息流分析方法跟踪程序中的数据流，假设数据来自不可信的来源。源是这些数据流进入程序的地方，接收器是它们离开程序的地方。

一些出版物将汇非正式地定义为“离开系统的数据”，这对于训练基于机器学习的分类器来说太不精确；这样的分类器只能和它们的训练数据一样好。

通过简单的仪表化仿真进行动态污点跟踪是非常昂贵的，并且会降低系统的速度。这样的减速在实践中是不可接受的，并且严重阻碍了动态污点跟踪系统在日常使用中的采用。这种污点扩散会极大地损害运行系统的性能。

## **用语义图形映射数据流**

要真正防止数据泄漏，您必须首先映射数据流。您必须理解应用程序的构造块，包括它的安全 DNA。然而，困难来自于平衡全面性和速度。简而言之，为了解决快速发展的应用程序中所有可能的漏洞，您必须自动化。

![](img/fe3426ad669aac3608acc8fa03b374a8.png)

语义图形化基于一个简单的观察:代码有许多不同的图形表示，代码中的模式通常可以表示为这些图形中的模式。这是一个图表的图表，第一次能够自动创建理解应用程序上下文的概要文件。语义图形是为代码查询设计的语言中立的中介表示，它关注程序被设计来做什么，它不应该做什么，以及它如何工作。因为语义图形识别了哪些变量是敏感的，以及它们如何在每个微服务中流动，所以可视化地表示数据路径和身份泄漏/违规成为可能。

![](img/c2c72ad5aeb5eb927374be3df17c1ad8.png)

在这种情况下，我们试图理解数据流并防止泄漏。然而，理解代码中应用程序上下文的能力是 DevSecOps 的基础。AppSec 仍然是手动的，主要是因为人类必须通过配置规则集或费力地通过误报来应用应用程序的上下文，这两者都是不可能的任务。除了数据泄露，语义图形化还有可能以 DevOps 的速度提供安全性。

— [切坦·科尼基](https://devops.com/author/chetan-conikee/)