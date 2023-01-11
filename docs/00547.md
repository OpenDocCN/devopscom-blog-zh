# 开放网络标准的研究

> 原文：<https://devops.com/look-open-networking-standards/>

开源标准在网络方面有很大的潜力。由于英特尔等主要厂商的贡献，OpenStack 和 OpenDaylight 等计划已经获得了相当大的发展势头，这些厂商最近加入了 OpenDaylight，成为白金会员。这种势头甚至刺激像美国电话电报公司这样的电信公司开始他们自己的开源努力，如开放网络实验室。

从这篇文章开始，我将研究各种开放网络标准，以及它们如何影响电信业务、IT 策略和网络工程。在元层面上，公平地说，由于开源开发的影响，网络团队越来越关注 API、DevOps 自动化，以及从人工方式转向自动化方式的工程和操作网络的需求。当然，每个标准都会带来不同的东西。让我们看看开放日光。

**OpenDaylight:开放 SDN 控制平面项目**

Linux 基金会管理 OpenDaylight，其目标是加速软件定义的网络和网络功能虚拟化的发展。尽管只有大约两年的历史，OpenDaylight 已经是世界上最大的开源项目之一，在过去一年左右的时间里有 266 名开发人员参与，该项目在 2014 年初已经超过了 100 万行代码。

OpenDaylight 具体针对什么？或许最好理解为提供一个开放的控制平面解决方案来支持多层 SDN 技术:

*   数据平面层由网络中的物理和虚拟设备组成，这些设备使用各种协议连接到控制层。这包括但不限于 OpenFlow。
*   在此之上是 OpenDaylight 控制器平台，它具有应用程序/编排层的北向 API，以及暴露于底层数据平面层硬件的大量南向协议和 API
*   最上面是编排和应用层。例如，这一层可能看起来像 OpenStack Neutron 的插件。

OpenDaylight 试图充当一种控制器的“瑞士”，允许通过许多不同的协议和接口(如 OpenFlow、路径计算元素协议(PCEP)、NetConf 等)与任何类型的交换硬件兼容。OpenDaylight 控制器运行在自己的 Java 虚拟机上，支持开放服务网关倡议。

**供应商和 OpenDaylight 的未来**

大量的网络供应商已经涌入 OpenDaylight，以至于批评者认为，尽管该项目有开源的名字，但实际上可能最终会保留网络在位者的地位。思科和 IBM 创建了 OpenDaylight，Brocade、Juniper、微软、英特尔和其他公司也是其成员。OpenDaylight 的很大一部分代码是由大型网络供应商贡献的。

特别是 OpenDaylight，由于思科对 SDN 的独特见解以及应该使用何种类型的控制器，思科的贡献经常受到审查。网络世界的 Jim Duffy 此前曾将思科 OpFlex 称为“OpenFlow 杀手”，这可能有点夸张，但很明显，思科对 OpenDaylight 的核心未来有着除 OpenFlow 之外的想法。OpFlex 可能是继 OpenDaylight 氦之后锂释放的关键部分。然而，开放网络实验室主任 Guru Parulkar 认为 OpFlex 将设备细节暴露给应用程序是不必要的复杂化，也是创建 OpenDaylight 替代方案的原因之一。

当然，对于供应商来说，在他们自己的产品和服务线上创新和参与开源社区之间很难取得平衡。像 OpenDaylight 这样的项目展示了开源软件在支持 SDN 编排方面的承诺，开放的“狂野西部”性质以及现有供应商由于纯粹的实力而成为狂野西部景观中事实上的新警长的风险。显然需要一条中间道路。

“供应商在开源网络项目中的角色[应该是与社区其他成员的共生角色](http://techcrunch.com/2014/12/05/separating-the-opportunities-from-the-obstacles-in-open-source-networking/)，”Mike Cohen 为 TechCrunch 写道。“这包括为社区的利益贡献开源努力，同时继续创新和构建更好地满足用户需求的差异化产品。供应商还应该将其中的一些创新回馈给社区，以帮助推广有助于市场持续增长的新标准。”

结果是:由思科和 IBM 在 2013 年发起，现在由 Linux 基金会托管的 OpenDaylight 不仅是一个重要的开放网络标准，也是最重要的开源软件运动时期之一。它定义了一个开放的控制器，为不同类型的基础设施和北向集成提供了广泛的南向协议 API。厂商对 OpenDaylight 的贡献以及与 open daylight 的关系对其在交付功能方面的快速进展至关重要，对其未来作为一项改善 SDN 和 NFV 流程编排及网络开发运维的包容性工作也至关重要。

* * *

## 关于作者/亚历克斯·亨索恩-伊万

[![](img/58b8acce4611dc75421900f4b58540e9.png) ](https://devops.com/wp-content/uploads/2015/03/Alex.jpg) Alex Henthorn-Iwane 于 2013 年 2 月加入 QualiSystems，负责全球营销和公共关系。在加入 QualiSystems 之前，Alex 是网络管理软件提供商 Packet Design，Inc .的营销和产品管理副总裁，在网络和安全初创公司担任高级管理、营销和技术职务方面拥有 20 多年的经验。

通过在 QualiSystems、Packet Design、CoSine Communications、Corona Networks 和 Lucent Technologies 的任职，他获得了云计算、软件定义的网络和网络功能虚拟化、DevOps、ITaaS 以及 IT 自动化和流程编排方面的专业知识。他为《嵌入式计算》、《虚拟战略杂志》、《数据化》、《SDN 中心》、《数据中心知识和信息周刊》撰稿。

这些天来，Alex 围绕新的可编程基础设施技术(云、SDx、NFV)、DevOps 以及实现所有这些技术所需的流程编排和自动化支持的交叉点撰写了大量文章，无论是在企业还是在服务提供商/运营商领域。

在[LinkedIn](https://www.linkedin.com/in/alexhenthorniwane)|[Twitter](https://twitter.com/heniwa)|[slide share](http://www.slideshare.net/AlexHenthornIwane1/followers)上与他联系