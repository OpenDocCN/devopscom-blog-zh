# 跟随独角兽:转变您的企业应用程序

> 原文：<https://devops.com/follow-the-unicorn-transform-your-enterprise-applications/>

对于我们这些在大型主机等企业系统上工作的人来说，独角兽公司^([1])做出的声明可能会相当令人震惊。像网飞^(和 Etsy^(这样的大公司一天发布几十个，有时几百个，这很难理解。但是仔细观察，您会发现关键的区别在于向客户发布变更的方式，而不是变更的总量。一个传统的企业应用程序在 3 到 6 个月的时间里可能会有数以千计的变更，但是所有这些变更都是一次性发布的。独角兽通常能够一次发布非常少量的变更，因为它们能够非常高效地开发、构建、测试和部署这些变更。向客户小批量发布具有重要的价值。它使您能够非常快速地获得反馈，并且因为变更没有与其他变更混合在一起，所以验证起来非常容易。))

那么，您如何转换您的开发环境来交付小批量的变更呢？我喜欢像处理任何其他计算机科学问题一样处理这个问题，毫无疑问是因为我的背景。将大问题分解成一系列更小的问题，然后解决那些更小的、不那么令人畏惧的问题:

**第 0 步:从概念验证开始**

选择一个概念证明(PoC)开始，这很重要，但不是关键任务。PoC 可用作学习基础，并有望作为后续 PoC 的模板。确保你有一个在文化上愿意变革的团队。通常最难解决的问题与技术无关，而是文化问题。

**第一步:了解你的申请**

您需要很好地理解您的应用程序由什么组成。不仅源代码构成了应用程序，而且使用什么源文件、中间件配置可能是什么、构建和部署应用程序可能需要什么脚本以及使用什么数据文件(例如平面文件、数据库)也很重要。其中一些组件可能与其他应用程序共享，因此您也需要了解这些依赖关系。一旦您很好地掌握了应用程序，您就可以自动化应用程序的构建和部署过程，以便团队的所有成员都可以高效地工作。

**第二步:理解你的测试用例**

如果您可以快速构建和部署应用程序，但是仍然需要几天或几周的时间来测试，那么测试会阻止您向客户交付。测试的一个重要转变是从测试整个应用程序到测试变更。您需要专注于运行正确的测试，以确保更改是正确的，并且不会导致回归。不执行代码更改的测试是不相关的，可以跳过。对于许多现有的应用程序，测试套件可能包含数百个甚至数千个测试用例。这些测试用例中的许多可能是没有被改变的代码的副本或测试区域。

**第三步:了解你的流程**

您能以多快的速度向客户提供更新？如果你的 bug 修复和增强在客户得到之前不得不搁置几天、几周或几个月，他们将不会满意。不仅要简化开发流程，还要简化组织中的运营流程。

要借助真实案例了解更多相关信息，请观看最近一次网络广播的[回放](https://devops.com/2015/04/28/variable-speed-ibm2/)，IBM 与 DevOps.com 合作，与加拿大抵押贷款住房公司(Canada Mortgage Housing Corporation)的 Jeff Blackadar 共同主持了这次网络广播，内容是打破 IT 孤岛如何帮助他们加快大型机开发。

此外，一定要让我知道你对博客和主题的想法。

¹ 诞生于网络技术的团队

²[http](http://www.slideshare.net/jedberg/devops-at-netflix-reinvent)[://](http://www.slideshare.net/jedberg/devops-at-netflix-reinvent)[www.slideshare.net/jedberg/devops-at-netflix-reinvent](http://www.slideshare.net/jedberg/devops-at-netflix-reinvent)

³[http](http://www.slideshare.net/beamrider9/continuous-deployment-at-etsy-a-tale-of-two-approaches)[://](http://www.slideshare.net/beamrider9/continuous-deployment-at-etsy-a-tale-of-two-approaches)[www . slide share . net/beam rider 9/continuous-deployment-at-etsy-a-tale-of-two-approach](http://www.slideshare.net/beamrider9/continuous-deployment-at-etsy-a-tale-of-two-approaches)

**关于作者/麦克·富尔顿**

[![MikeFaceMedium-150x150](img/4e417965d97125bcffc96c438c9fa88c.png)](https://devops.com/wp-content/uploads/2015/06/MikeFaceMedium-150x150.jpg)Mike 是 IBM 杰出的工程师，在 IBM 担任 CTO Enterprise DevOps，是一名软件开发专家，专门从事编译器、调试器、剖析器和虚拟机方面的工作。在 IBM，Mike 致力于理解和影响企业 IT 的趋势和方向，将新技术引入 DevOps 产品组合。他还忽略了 DevOps 产品组合与 IBM 和企业软件解决方案的集成。Mike 是 IBM 的发明大师，拥有多项专利。

他是一个狂热的博客写手，定期在他的博客网站上写东西——makingdevelopersliveseasier.wordpress.com

[![linkedin](img/456db676b88f9564e5cdc9b2caf9a833.png) ](https://ca.linkedin.com/in/mikesfulton) [ ![twitter](img/461b7b316da6107c5e5467b56d32e217.png)](http://@mikesfulton)