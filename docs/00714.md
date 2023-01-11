# Linux 容器和安全含义

> 原文：<https://devops.com/linux-containers-security-implications/>

“容器”这个词是不是暗示着容器是安全的？如果是这样，任何这样的安全假设可能是迄今为止最广泛的 Docker 漏洞。

[![aaron cois](img/1461e68ffd53661e0e91ecee01da4bf5.png)](https://devops.com/wp-content/uploads/2015/03/aaron-cois.jpg) “我认为 Docker 最大的威胁之一是它的定位和语言中隐含的安全性。卡耐基梅隆大学软件工程学院 CERT 部门的研究员亚伦·科伊斯说:“事实是，这些容器不包含任何东西。然而，这就是其中的含义。

正如那些认为 Linux 或 VMs 本身就足够安全的人错了一样，那些认为容器限制了安全性的人也将大失所望。今天，Linux 环境需要网络、操作系统/主机安全、互联网安全和 web 应用程序安全措施，类似于其他平台所使用的措施。越来越需要安全审计/ PEN 测试、防火墙/ WAFs、防病毒和防恶意软件工具、DLP、IDS/IPS、补救工具等工具，以及类似于微软环境所需的所有安全措施来保护 Linux 环境中的数据。“同样，运营部门可以为开发人员提供登录 VSphere 控制台的工具，以创建和更改虚拟机，同时限制他们的权限，”科伊斯说。

因此，集装箱也需要适当的安全措施。“开发人员和非管理操作人员不需要登录到主机命令行来工作，没有人在安全方面希望他们这样做，”科伊斯说。但是今天的码头工人工作流程不仅允许而且要求这样做。

问题的根源…

# [–此故事已被移至《集装箱杂志》–](http://containerjournal.com/2015/06/05/linux-containers-security-implications/)

* * *