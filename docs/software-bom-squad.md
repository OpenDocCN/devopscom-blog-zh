# 软件爆炸小组

> 原文：<https://devops.com/software-bom-squad/>

在我的上一篇文章“当好代码变坏时的 T1 T2”中，我分享了一项新的研究，显示大型开发组织平均每年消耗超过 15，000 个已知的易受攻击的 T4 和有缺陷的组件。虽然我们不能阻止软件变坏，但我们可以利用传统制造商的实践来提高召回和修复“坏”软件组件的能力。

## 软件 BOM

物料清单(BOM)在传统制造供应链中用于列出产品中使用的供应商和零件，而"[软件物料清单](http://www.sonatype.com/assessments/application-health-check/guide) " (BOM)是用于构建应用程序的第三方和开源组件的清单。

[![Screen Shot 2015-07-17 at 10.06.03 AM](img/fe1f3e326f7bbab1d8aa9e874b396c16.png)](http://www.sonatype.com/assessments/application-health-check/guide)

A sample software bill of materials lists all open source and third party components, including their version, age, license type, and any known security vulnerabilities.

正如维基百科中提到的，“BOM 的概念在传统制造业中作为供应链管理的一部分已经根深蒂固。制造商使用 BOM 来跟踪它用来创建产品的部件。如果后来在特定部件中发现缺陷，BOM 可以很容易地找到受影响的产品。

“软件 BOM 对于软件产品的开发组织(制造商)和购买者(客户)都是有用的。构建者通常利用可用的开源和第三方软件组件来创建产品；软件 BOM 允许构建者确保这些组件是最新的，并快速响应新的漏洞。购买者可以使用软件 BOM 来执行漏洞或许可证分析，这两者都可以用来评估产品的风险。了解软件的供应链，获得软件 BOM，并使用它来分析已知的漏洞对于管理风险至关重要。”

软件材料清单不仅列出了所使用的内容，而且在某些情况下，它还与实时组件缺陷数据同步，以指示哪些组件具有已知的漏洞或许可风险。各种软件供应链自动化工具进一步扩展了软件清单，当缺陷警报出现时，会自动提醒涉众。在高级工具中，整个软件生命周期都是自动化的，以确保避免有缺陷的组件，并且只要发现新公布的漏洞，持续监控就能立即识别它们。

## **绝命毒师**

在我之前的帖子里提到过，[当好代码变坏](https://devops.com/2015/07/22/good-code-goes-bad/)，没有办法阻止软件“变坏”。没有人能免受这些问题的影响。因此，我们需要集中精力应对这些问题。

套用文斯·隆巴迪的话，“重要的不是你如何被击倒，而是你如何站起来”。在 2014 年 OpenSSL 漏洞公告之后(或者挑选任何其他新的安全漏洞，无论是否有指定的徽标)，地球上的每个开发和 IT 运营团队都在问两个问题:

1.  我们曾经使用过开源组件吗？
2.  如果有，在哪里？

对于那些用软件材料清单跟踪组件使用的组织来说，答案很容易找到。对于其他组织，需要数周甚至数月的研究。为了了解可追溯性实践缺乏成熟度的情况，请看 Sonatype research 的这张图片，它显示了 2014 年 4 月首次漏洞披露后产品中 OpenSSL 漏洞的公告。

## [![Screen Shot 2015-07-17 at 10.07.09 AM](img/6a2d9ffc6c542c822b67033f9b2c6ab7.png)](http://www.slideshare.net/SonatypeCorp/devops-connect-josh-corman-and-gene-kim-discuss-devopssec) 
**自动化软件供应链的可追溯性**

软件供应链的复杂性，加上开源和第三方组件在其中流动的数量和速度，迫使我们以不同的方式思考我们当前的开发和运营实践。我们不是第一个面临这些挑战的公司，我们可以从其他高速制造组织和行业的成熟实践中学到很多东西。

有一点很清楚。手动监控或不定期检查点的做法跟不上消耗组件的数量和速度。如果您将这些考虑扩展到开源组件之外，并扩展到容器、微服务或开发和运营中使用的其他映像，问题将进一步超出手动流程的范围。我们的软件供应链中的数量和速度不会减少——如果没有新的方法，被消费的未经检查的质量和完整性零件的数量将继续增加，成为技术债务。

但是今天答案就在这里:自动化。自动化可以释放组织开发能力的潜力。很少有机会同时提高速度、效率和质量。促进全面软件供应链自动化的解决方案将迎来下一波开发生产力浪潮——其收益与敏捷、精益和开发运维的收益相当，甚至更高。

有关软件供应链实践的当前状态以及软件开发团队所采用的最佳实践示例的更多信息，可在 [2015 年软件供应链报告](http://www.sonatype.com/speedbumps)中找到。

[![Screen Shot 2015-07-22 at 9.26.05 AM](img/fba8ddc2af34debe80fadaf4658c16e6.png)](www.sonatype.com/speedbumps)