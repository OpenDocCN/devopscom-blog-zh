# DevOps 简介

> 原文：<https://devops.com/introductiontodevops/>

## 什么是 DevOps

你可以向 10 个人询问 DevOps 的定义，可能会得到 10 个不同的答案。

如果你想找到一个自己的定义，你的研究很可能会从问谷歌“什么是 DevOps”开始。自然，维基百科是第一批结果之一，所以这就是我们将开始的地方。维基百科上的第一句话将 DevOps 定义为“一种强调软件开发人员和信息技术(IT)专业人员之间的沟通、协作和集成的软件开发方法。”嗯，这是一个相当密集的定义，但仍然非常模糊。我认为 DevOps 可以简单地解释为运营部门与工程师一起工作，以自动化和可重复的方式更快地完成工作。

因此，让我们深入研究 DevOps 如何工作，以及如何更好地毗邻两个传统上对立的部门。

### 发育期痛

当您负责大型分布式应用程序时，操作复杂性会快速增长。

*   您如何调配虚拟机？

*   你如何配置网络设备和服务器？

*   您如何部署应用程序？

*   您如何收集和汇总日志？

*   你如何监控服务？

*   您如何监控网络性能？

*   您如何监控应用程序的性能？

*   出现问题时，您如何发出警报并采取补救措施？

### 结合开发人员和运营人员的力量

对开发人员/运营协作的关注为管理现实世界运营的复杂性提供了一种新的方法。我认为操作复杂性可以分为几个主要类别:[基础设施自动化](https://en.wikipedia.org/wiki/Cloud_computing)、[配置管理](https://en.wikipedia.org/wiki/Configuration_management)、[部署自动化](https://en.wikipedia.org/wiki/Continuous_integration)、[日志管理](https://en.wikipedia.org/wiki/Log_management_and_intelligence)、[性能管理](https://en.wikipedia.org/wiki/Application_performance_management)，以及[监控](https://en.wikipedia.org/wiki/System_monitoring)。以下是我用来帮助解决这些任务的一些工具。

#### [基础设施自动化](https://en.wikipedia.org/wiki/Cloud_computing)

您不再需要从头构建服务器，购买数据中心的电源和连接，以及手动将机器接入网络。戴上运营帽子几年后，我了解到许多运营任务都是平凡的、手动的，一旦出现问题，往往不得不在凌晨两点完成。DevOps 基于技术基础设施的所有元素都可以通过代码来控制的想法。随着云计算的兴起，这一切都可以通过网络服务实时完成。基础架构自动化解决了必须亲临数据中心来配置硬件和进行网络更改的问题。使用云服务的好处是成本随需求线性增长，并且您可以根据需要自动配置，而无需预先购买硬件。

*   [亚马逊网络服务](https://aws.amazon.com/)

*   [Windows Azure](https://www.windowsazure.com/en-us/)

*   [RackSpace 云](http://www.rackspace.com/cloud/)

*   [惠普云](http://hpcloud.com/)

*   [红帽开班](https://www.openshift.com/)

*   [Ubuntu 云](https://www.ubuntu.com/cloud)

*   [Heroku](https://heroku.com/)

*   [发动机场](https://engineyard.com/)

#### [配置管理](https://en.wikipedia.org/wiki/Configuration_management)

配置管理解决了硬件就位后必须手动安装和配置软件包的问题。使用配置自动化解决方案的好处是服务器每次都以完全相同的方式部署。如果您需要对一万台服务器进行更改，您只需要在一个地方进行更改。

*   [厨师](https://www.opscode.com/chef/)

*   [木偶](https://puppetlabs.com/)

*   [可回答的](http://www.ansibleworks.com/)

*   [盐堆](https://www.saltstack.com/)

*   [托盘](http://palletops.com/)

*   [Bcfg2](http://trac.mcs.anl.gov/projects/bcfg2/)

还有其他特定于供应商的 DevOps 工具:

*   亚马逊的 [OpsWorks](https://aws.amazon.com/opsworks/)

*   右缩放

在我工作过的运营环境中，对于谁可以访问生产环境、谁可以进行更改、何时可以进行更改、谁可以实际接触硬件以及谁可以访问哪些数据中心，总是有严格的控制。在这些高度管制和面向过程的企业中，模糊开发和运营之间界限的想法似乎不可行。有太多的过程和传统阻碍了 DevOps 方法的使用，这看起来几乎是不可能的。从操作角度来看，我的第一反应是理解应用程序架构，这样我就可以开始考虑基础架构组件的适当部署模型。从开发的角度来看，我的第一个里程碑是确保运营团队完全理解应用程序，以及将它部署到预生产环境需要做什么。

DevOps 不仅仅是一套工具，而是一种理念的转变，需要所有相关人员的参与才能真正取得成功。只有通过高水平的合作，事情才会变得更好。