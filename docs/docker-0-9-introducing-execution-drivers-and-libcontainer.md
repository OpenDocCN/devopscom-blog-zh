# DOCKER 0.9:介绍执行驱动程序和 LIBCONTAINER

> 原文：<https://devops.com/docker-0-9-introducing-execution-drivers-and-libcontainer/>

[来自 Docker 博客:](https://blog.docker.com/2014/03/docker-0-9-introducing-execution-drivers-and-libcontainer/)

码头工人们，

今天，我们很高兴地介绍 Docker 0.9。在这个版本中，我们将继续关注质量而不是功能，缩小和稳定核心，并为所有主要操作系统提供一流的支持。

除了 [的](https://github.com/dotcloud/docker/issues/4380)[打](https://github.com/dotcloud/docker/issues/4291) [的 bug 修复](https://github.com/dotcloud/docker/issues/728)之外，Docker 0.9 还包括 2 大改进:*执行驱动*和 *libcontainer* 。

像往常一样，要获得完整的改进列表，您可以查看变更日志。

### 执行驱动因素

首先，我们引入了一个*执行驱动程序* API，它可以用来定制每个容器周围的执行环境。这使得 Docker 可以利用众多可用的隔离工具，每种工具都有其特定的权衡和安装基础:OpenVZ、systemd-nspawn、libvirt-lxc、libvirt-sandbox、qemu/kvm、BSD Jails、Solaris Zones，甚至是很好的 chroot。这是对 LXC 的补充，它将继续作为自己的驱动程序提供。

已经有几个项目正在开发更多的驱动程序。想去凑热闹吗？欢迎访问 Freenode 上的#docker-dev，我们将帮助您开始。

### 新的默认驱动程序:libcontainer

[![docker-execdriver-diagram](img/9eb2b48c1bee1e67aa7565deafe2856d.png)](https://blog.docker.com/wp-content/uploads/2014/03/docker-execdriver-diagram.png)

其次，我们引入了一个新的内置执行驱动程序，它与 LXC 驱动程序一起提供。这个驱动程序基于 [libcontainer](https://github.com/dotcloud/docker/tree/master/pkg/libcontainer) ，一个纯粹的 Go 库，我们开发它是为了直接访问内核的容器 API，没有任何其他依赖。

由于 libcontainer，Docker 开箱即用，现在可以操作名称空间、控制组、功能、apparmor 配置文件、网络接口和防火墙规则——所有这些都以一致和可预测的方式进行，并且不依赖于 LXC 或任何其他用户域包。这大大减少了移动部件的数量，并使 Docker 免受 LXC 版本和发行版带来的副作用的影响。事实上，libcontainer 对稳定性的提升如此之大，以至于我们决定将它作为默认设置。换句话说，从 Docker 0.9 开始，LXC 现在是可选的。要切换回 LXC 驱动程序，只需用 **docker -d -e lxc** 重启 Docker 守护进程。当然，我们将继续支持 LXC 车手前进。

**为你的 Go 项目使用 lib container**

我们开发了 [libcontainer](https://github.com/dotcloud/docker/tree/master/pkg/libcontainer) ，希望其他项目能够重用它。如果您对 Linux 的本机容器特性感兴趣——名称空间、cgroups、功能等——那么我们鼓励您开始动手！要开始，请获取 go 包并查看 API 文档:

| 12 | 【go get github . com/dotcloud/docker/pkg/libcontainer】godoc github . com/dotcloud/docker/pkg/libcontainer |

### 目标 1.0

这个版本是向稳定的、生产就绪的 1.0 版本迈出的重要一步。我们计划将下一个版本 0.10 作为 1.0 的第一个候选版本。

如前所述，Docker 1.0 的目标是:

*   生产质量

*   所有主要操作系统的一流支持

*   收缩的核心和稳定的插件架构

*   有据可查

*   能够得到 Docker 和我们的合作伙伴的商业支持

*   Docker 能够提供长期支持

我们已经在努力准备 0.10，有几个令人兴奋的改进，我们认为你会喜欢。如果你想先睹为快，或者你想有所贡献，来打个招呼吧！我们在自由节点的#docker 上。我们欢迎各种水平的爱好者，可以帮助你开始你的第一次贡献。一如既往，感谢我们的贡献者社区，现在已经有 352 人了！

谢谢，祝黑客快乐！

码头工人队