# Docker 使容器编排自动化和大众化

> 原文：<https://devops.com/docker-automates-democratizes-container-orchestration/>

SEATTLE–(Business Wire)–**DockerCon –** [Docker](http://cts.businesswire.com/ct/CT?id=smartlink&url=http%3A%2F%2Fwww.docker.com%2F&esheet=51365497&newsitemid=20160620005482&lan=en-US&anchor=Docker&index=1&md5=d41eeb23d3659ae9ea098bc836b79017) today announced Docker Engine 1.12 with built-in orchestration, a powerful combination that provides Developers and IT Operations with a simplified and automated experience to deploy and manage Dockerized distributed applications –both traditional apps and microservices –at scale in production. By adding this additional intelligence to Docker Engine, it becomes the orchestration building block, creating a model for engines to form a self-organizing, self-healing pool of machines on which to run multi-container distributed applications. When integrated into Docker Engine, these new capabilities optimize ease of use, resiliency, performance-at-scale and security – all key requirements that are missing in other orchestration systems. As a result, organizations can be assured that their dev and ops teams are aligned on unifying the software supply chain to release applications into production more rapidly and frequently.“Orchestration is at the same stage today as containerization was before Docker. You either need an army of experts to build it, or you lock yourself to a monolithic platform which will drastically reduce your choice of suppliers,” said Solomon Hykes, founder and CTO at Docker. “Three years ago we brought containerization into the mainstream by making it usable for non-experts, without lock-in. We think it’s time to do the same for orchestration. This is a necessary step for the industry to move forward, and as the leaders of the containerization market it’s our responsibility to lead this change.”

与所有 Docker 工具一样，这种集成总是与用户的选择和灵活性有关。“群体模式”是一个可选功能，用户可以选择“打开”内置的编排，或者他们也可以选择使用自己的定制工具或运行在 Docker Engine 上的第三方编排器。这种方法与 Docker 平台的电池内置但可交换的架构相一致，这刺激了充满活力的协作生态系统的发展。

RedMonk 的行业分析师 Fintan Ryan 表示:“随着 Docker 的采用曲线继续增长，开发人员在大规模编排方面遇到了越来越大的困难。随着 1.12 版本中包含安全的内置流程编排，Docker 为开发人员提供了一个易于使用但功能极其强大的流程编排工具，同时进一步投资于一致、易于管理的操作体验

随着组织开始增加在容器化方面的投资，并且超过 60%的组织在生产中运行 Docker，他们正在寻求更复杂的编排工具来扩展跨应用程序和团队的部署。Docker 1.12 通过跨计算、网络和存储的整个应用堆栈的功能来满足这些要求。

**易用性**

Docker 1.12 极大地简化了创建 Docker 引擎组(也称为集群)的过程。群集的自我组织、自我修复能力现在得到了自动化服务发现和内置分布式数据存储的支持。因此，只需一个命令就可以添加一个 Docker 引擎并横向扩展一个群。

**弹性**

新的服务部署 API 用一个命令描述了所有的资源和组件，允许运营团队运行和扩展服务。通过 API，swarm 了解定义的应用程序，并在发生不利情况时，根据应用程序的要求不断检查和协调环境。与其他系统不同，swarm 本身没有单点故障。所有服务的状态在一组管理器中实时复制，因此在任何节点故障后都可以重新调度容器。

**规模化性能**

Docker orchestration 包括一个独特的内存缓存层，用于维护整个集群的状态，提供一个无阻塞的架构，即使在高峰时间也能确保调度性能。此外，该系统具有内置的路由网格技术，解决了如何提供容器感知负载平衡的挑战。路由网格确保请求被发送到正确的容器，而不管它们在群中被调度到哪里。

**默认安全**

每个引擎被自动分配一个密码身份，以确保只有经过验证的引擎才能加入群。此外，Docker Engine 附带相互认证的 TLS，在参与群的每个节点之间提供认证、授权和端到端加密通信，而运营商无需采取任何步骤来启用它。

**可用性**

用户可以通过三种方式获得 Docker 1.12，该版本目前是一个候选版本，计划于 2016 年 7 月正式上市。首先，它现在可以作为新开放的 Mac 版 Docker 和 Windows 版 Docker 公开测试版的一部分在 https://www.docker.com/getdocker[获得。其次，它可以通过云优化的体验获得，这些体验捆绑了定制插件，这些插件提供了 Docker 和目标平台功能之间的深度集成，包括网络、负载平衡和 SSH 密钥管理。Docker for AWS 和 Docker for Azure 是在这些平台上部署 Docker Engine 的最佳方式，可在 https://beta.docker.com](http://cts.businesswire.com/ct/CT?id=smartlink&url=https%3A%2F%2Fwww.docker.com%2Fgetdocker&esheet=51365497&newsitemid=20160620005482&lan=en-US&anchor=https%3A%2F%2Fwww.docker.com%2Fgetdocker&index=2&md5=59b35b305fb0d70d33e3f9643d76316a)[的](http://cts.businesswire.com/ct/CT?id=smartlink&url=https%3A%2F%2Fbeta.docker.com&esheet=51365497&newsitemid=20160620005482&lan=en-US&anchor=https%3A%2F%2Fbeta.docker.com&index=3&md5=91222bbbe951e5b33639874247ae055d)进行私人测试。最后，Docker 1.12 也可以在 https://docs.docker.com/engine/installation/linux[的所有主要 Linux 发行版中以二进制下载或打包的形式获得。](http://cts.businesswire.com/ct/CT?id=smartlink&url=https%3A%2F%2Fdocs.docker.com%2Fengine%2Finstallation%2Flinux&esheet=51365497&newsitemid=20160620005482&lan=en-US&anchor=https%3A%2F%2Fdocs.docker.com%2Fengine%2Finstallation%2Flinux&index=4&md5=a3c5ec96a87eaf6d9c1041dc93f7b921)

**更多信息:**

*   博客:Docker 1.12:现在有内置的编排！[https://blog . docker . com/2016/06/docker-1-12-内置编排/](http://cts.businesswire.com/ct/CT?id=smartlink&url=https%3A%2F%2Fblog.docker.com%2F2016%2F06%2Fdocker-1-12-built-in-orchestration%2F&esheet=51365497&newsitemid=20160620005482&lan=en-US&anchor=https%3A%2F%2Fblog.docker.com%2F2016%2F06%2Fdocker-1-12-built-in-orchestration%2F&index=5&md5=a6f5c969111117b351a8b5a85f4f677b)
*   博客:宣布 Mac 和 Windows 的 Docker 公开测试版-[https://blog . Docker . com/2016/06/Docker-Mac-Windows-Public-Beta/](http://cts.businesswire.com/ct/CT?id=smartlink&url=https%3A%2F%2Fblog.docker.com%2F2016%2F06%2Fdocker-mac-windows-public-beta%2F&esheet=51365497&newsitemid=20160620005482&lan=en-US&anchor=https%3A%2F%2Fblog.docker.com%2F2016%2F06%2Fdocker-mac-windows-public-beta%2F&index=6&md5=73cdb305dfa0908668e0bb206bd56295)
*   博客:介绍 AWS 和 Azure Beta 版的 Docker-[https://blog.docker.com/2016/06/azure-aws-beta/](http://cts.businesswire.com/ct/CT?id=smartlink&url=https%3A%2F%2Fblog.docker.com%2F2016%2F06%2Fazure-aws-beta%2F&esheet=51365497&newsitemid=20160620005482&lan=en-US&anchor=https%3A%2F%2Fblog.docker.com%2F2016%2F06%2Fazure-aws-beta%2F&index=7&md5=7ba30952cbe972704b11334dbf12f2f9)
*   Docker 应用捆绑:[https://blog.docker.com/2016/06/docker-app-bundle/](http://cts.businesswire.com/ct/CT?id=smartlink&url=https%3A%2F%2Fblog.docker.com%2F2016%2F06%2Fdocker-app-bundle%2F&esheet=51365497&newsitemid=20160620005482&lan=en-US&anchor=https%3A%2F%2Fblog.docker.com%2F2016%2F06%2Fdocker-app-bundle%2F&index=8&md5=faaa3b13d46d9fc6cc39e8d350009b2e)
*   [Docker 1.12 在线聚会](http://cts.businesswire.com/ct/CT?id=smartlink&url=http%3A%2F%2Fwww.meetup.com%2FDocker-Online-Meetup%2Fevents%2F232021130%2F&esheet=51365497&newsitemid=20160620005482&lan=en-US&anchor=Docker+online+meetup+for+1.12&index=9&md5=3b3955720730d75e703460d112cb7356)
*   注册我们的[简讯](http://cts.businesswire.com/ct/CT?id=smartlink&url=https%3A%2F%2Fwww.docker.com%2Fsubscribe_newsletter%2F&esheet=51365497&newsitemid=20160620005482&lan=en-US&anchor=newsletter&index=10&md5=f88c82d8d670992110a9b11b8b35f15f)

**关于 Docker 公司**

Docker，Inc .是 Docker 开源平台背后的公司，也是 Docker 生态系统的首席赞助商。Docker 是开发人员和系统管理员构建、发布和运行分布式应用程序的开放平台。借助 Docker，IT 组织可以将应用交付时间从几个月缩短到几分钟，在数据中心和云之间顺畅地移动工作负载，并可以将计算资源的使用效率提高 20 倍。受活跃社区和透明、开源创新的启发，Docker 容器已被下载超过 41 亿次，Docker 被世界上数千家最具创新性的组织的数百万开发人员使用，包括 ADP、百度、BBC、高盛、Groupon、ing、Yelp 和 Spotify。Docker 的快速采用催生了一个活跃的生态系统，产生了超过 4，300，000 个“Docker 化”的应用程序，超过 100 家与 Docker 相关的初创公司，以及与 AWS、Cloud Foundry、Google、IBM、Microsoft、OpenStack、Rackspace、Red Hat 和 VMware 的集成合作伙伴关系。

![](img/cba3e5ffc33d8a2d824a36908447994c.png)

在 businesswire.com 上查看源代码版本:[【http://www.businesswire.com/news/home/20160620005482/en/】](http://www.businesswire.com/news/home/20160620005482/en/)

传立公关
希瑟菲茨西蒙斯，650-279-4360
[【电子邮件保护】](/cdn-cgi/l/email-protection#1b6b697e68685b7f7478707e6935787476)