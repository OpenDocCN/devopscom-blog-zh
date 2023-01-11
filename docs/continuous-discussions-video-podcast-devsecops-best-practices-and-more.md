# 持续讨论视频播客:DevSecOps、最佳实践等

> 原文：<https://devops.com/continuous-discussions-video-podcast-devsecops-best-practices-and-more/>

在持续讨论(#c9d9)播客的最近一集中，一组行业专家讨论了为什么 DevSecOps 不仅仅是一个流行词，如何让组织中的每个人都拥有安全性的技巧，以及他们自己将安全性融入软件交付渠道的一些挑战和经验。

这个小组包括:**艾伦·希梅尔，**DevOps.com 的主编；**王晨曦，**雨露资本执行普通合伙人； **Derek E. Weeks，**Sonatype 的副总裁兼开发总监**；葆拉·付令超，GDIT 国家安全部门首席建筑师； **Geetika Tandon，**联邦民用 CTO 集团技术总监；以及电云公司的**山姆·菲尔和安德斯·沃尔格伦。****

继续阅读他们的一些顶级外卖！

# **为什么是 DevSecOps？**

DevSecOps 实际上更多的是一种文化转变，Shimel 说:“DevOps 就是 DevOps。然而，这不仅仅关系到开发和运营。DevOps 是关于整个组织采用一种共同的文化交互方式，包括安全性，并将安全性带入这种文化，带入软件排序装配线。”

将安全性集成到开发实践中需要大量的协作和沟通，王说:“说安全性应该是过程的一部分很容易。但在实践中，很难做到。当你有一个从输入到输出需要几天时间完成的安全测试过程，然后你的开发团队一天发布 500 个版本，这是两种非常不同的文化。这通常是一个迭代过程，但需要大量的团队沟通，大量的坐下来，解决安全问题，因此这不是一个简单的过程。”

为什么是 DevSecOps 而不仅仅是 DevOps？嗯，安全人员不一定会被邀请参加聚会，付令超解释道:“这是一种文化挑战，安全不一定是 DevOps 转型的一个组成部分。我认为‘DevSecOps’之所以存在，是因为要么我们忽略了安全性，要么他们置身于这场正在发生的变革之外。”

根据 Wallgren 的说法，安全和质量之间真的不应该有所取舍:“我渴望有一天我们不区分安全和质量，因为，是的，在某种程度上它们有不同的规则，但就最终用户而言，一个 bug 就是一个 bug。”

[Weeks](https://twitter.com/weekstweets?lang=en) 想让没有信仰的人知道 DevSecOps 是真实的，而不仅仅是一个时髦的词:“DevOps 和 security 可以相互集成，并在大规模上成功集成。有数百人甚至数千人的组织拥有 DevSecOps 实践，并在不断改进它，添加自动化的安全性，因此它肯定已经超越了时髦的状态。”

根据 Tandon 的说法，在发布过程中包含安全性应该是显而易见的:“我认为这是常识。我甚至不明白安全性是如何被忽略的。我不明白我们怎么会有这些巨大的管道，我们每天发布一百个代码，然后，嘣，我们就停下来了。我们被停下来扫描。”

## **开发团队的常见障碍和开发团队成功的模式**

进步需要时间，但 Shimel 仍然对未来充满希望:“我们不会在一天之内煮沸海水或改变世界，但我们会改变世界，我们会改变软件交付的方式，这样软件和安全就是质量的代名词。”

[Wang](https://twitter.com/chenxiwang?lang=en) 解释了一家公司如何利用自动化成功地将安全性融入到他们的流程中:“我合作过的一家公司是在集装箱领域，他们有一个他们称之为布朗的注册中心。所以他们有开发团队汇编的代码，然后进入布朗的注册表。没有其他代码可以进入布朗的注册表，除非它来自他们自己的团队。然后，安全团队会从布朗的注册表中自动进入并扫描，只有通过扫描的人才会被放入他们所谓的黄金注册表中。然后他们可以将它部署到服务器上。”

组织中的每个人都应该练习并准备好应对安全事件，付令超建议道:“最需要练习应对漏洞的人实际上并不是安全人员。他们习惯于应对安全问题。运营人员和开发人员不习惯于响应安全事件，他们没有准备好，也没有接受过如何响应的培训。因此，当你的弱点出现时，这是一个糟糕的新故事。”

许多安全问题已经存在很长时间了，这是软件交付行业可以改进的地方，Wallgren 说:“大多数漏洞来自哪里？据我所知，其中绝大多数来自众所周知的长期安全问题，这些问题已经存在很长时间了，或者至少按照技术标准来看已经存在很长时间了。所以很多都只是简单的东西，我们需要做得更好。”

安全作为代码是将安全与 DevOps 真正集成的下一步，Weeks 解释道:“我刚刚与欧洲一家大型电信公司的人交谈，他们说，‘我是安全团队的，我们正在与开发部门合作，我们越来越接近了。我们有所有这些开发者需要遵守的规则和事情，我们一直在努力让他们更多地遵守这些规则。我说，‘那真的很酷。这些规则或策略中的任何一个都可以作为代码吗？他斜眼回答说，“什么？“代码？”"

[Tandon](https://www.linkedin.com/in/geetika-tandon-31245b2a) 与一位客户分享了一次令人大开眼界的经历:“我曾见过这样一种情况，我们即将投入生产，这是一个安全性接近尾声的 DevOps，我们获得了 4000 次点击，我们必须投入生产，但大多数都被忽略了。那么，我们这样做是真的保护了我们的系统，还是让我们自己的系统变得更加不安全？”

**看完整集:**

[https://www.youtube.com/embed/aZktvFXzVjk](https://www.youtube.com/embed/aZktvFXzVjk)

想深入了解 DevSecOps 吗？行业专家 John Willis 是《DevOps 手册》和《超越凤凰计划》的合著者，也是 SJ Technologies 的 DevOps 和数字实践副总裁，他计划在伦敦和拉斯维加斯的[devo PS 企业峰会](https://events.itrevolution.com/)之后立即主持一整天的实践研讨会。尽快注册—空间有限！

[注册参加伦敦研讨会](http://electric-cloud.com/blog/2018/05/devops-workshops-at-devops-enterprise-summit-up-your-devops-game/)

[注册参加拉斯维加斯研讨会](http://electric-cloud.com/blog/2018/05/devops-workshops-at-devops-enterprise-summit-up-your-devops-game/)

[![](img/0aeaa50b0d43d21ee6a223f8c8b29f1f.png)](http://electric-cloud.com/blog/2018/05/devops-workshops-at-devops-enterprise-summit-up-your-devops-game/)

-[否则的话壁分支](https://devops.com/author/anders-wallgren/)