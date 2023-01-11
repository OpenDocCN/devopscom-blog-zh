# 是出站的傻逼！

> 原文：<https://devops.com/its-the-outbound-stupid/>

尽管“出口”这个词听起来不错，但我更喜欢“外出”。出站是防火墙“可信”端发起的流量的核心防火墙，目的地是未知的流量。然而，在过去的 20 年中，网络管理员更加重视什么可以进入他们的网络，而不是担心从网络中输出什么。原因有很多，但最关键的一点是，如果没有东西可以进来，那么我们就不必担心会有什么东西出来。对吗？是的，对…

Fast Forward 2014 we have firewalls everywhere. On our smartphones, laptops and home broadband wifi routers. In the cloud, any typical IaaS setup has a firewall for every group of instances, usually called **Security Group** and every instance has its own, internal firewall that is controlled by the instance OS. We are starting to see more and more people that use them as a core building block, in a  network security architecture, and as a fundamental element of it. But as most of you (us) actually spend time, energy and concern about inbound firewall rules, **only 15% of you (us) even bother with the Outbound**. That’s true, and its about time we change that.

### 计划。为成功做计划。

一个精心设计的入站防火墙策略可以给坏人一个真正的挑战，但是当他们进入防火墙而没有出站策略时会发生什么呢？这是一个吃到饱的自助餐。有了精心策划的出站策略，他们很有可能会离开，或者很容易被发现——这对您的时间来说是一个巨大的投资回报！这一切都始于一个书面的(英语，而不是 Erlang 或 Java)安全策略，该策略概述了服务器组之间以及与外部世界的交互方式。首先是入站/入口，这应该很容易制定。接下来是出站/出口的棘手部分——让我们仔细看看应用服务器。
通常，应用服务器位于中间层之一，信任来自 web 层的流量，并在将回复发送回 web 服务器之前向数据库层发起请求。
入站:允许来自 Web 服务器的流量，通常只针对 HTTP 或 HTTPS，具体取决于 Web < >应用程序的设置。
Outbound:允许特定数据库端口上的数据库的数据库流量，例如，MySQL 的 TCP3306。

### 别忘了监控

您可能使用的任何监控解决方案都会影响您的安全策略。安装在机器上的基于代理的监控解决方案必须被允许连接到外部，而从外部探测您的服务器的外部监控服务必须被允许进入以完成其工作。
**基于代理的监控:允许特定协议上的出站**到特定 IP 或 IP 列表
**外部监控:允许特定协议和特定 IP 或 IP 列表的入站**

### 出站时还有什么？黑仔规则

我们的应用服务器运行 ubuntu，所以它可能需要访问 Ubuntu 更新服务，也需要 DNS 才能快乐地生活。现在常见的主题是允许访问 https (TCP443)上的出站更新服务，并允许出站 DNS (UDP53)。对吗？不对。为什么不仅限于我们的操作系统需要的特定存储库服务呢？强硬的 DevOps 将完全取消更新，声明应用程序的任何部分都不应该自我更新。您可以随时烘焙/启动一个全新的更新实例，而不是搞乱一个工作实例。
**结果:没有出站 HTTPS TCP443**
现在为 DNS。如果您担心安全问题，建议完全停止使用 DNS，而使用/etc/hosts。一个不太激烈的方法是只允许 DNS 访问你信任的 DNS 服务器(例如谷歌的 8.8.8.8)，这样做是为了确保使用 DNS 查询泄露的数据只能到达谷歌，他们已经知道一切。结果:没有出站 DNS UDP53 或允许 DNS (UDP53)到 8.8.8.8，如果你必须。

### 你的反馈回路:网络日志

在设置了这个严格的出站策略之后，我们最终可以识别出那些被搁置的服务，因为我们刚刚切断了它们的生命线。它可能是一个我们应该卸载的非关键代理，或者，但愿不会如此，是某个坏人编写的一段流氓代码，现在无法连接到其 C&C 服务器——下次将详细介绍。

祝你快乐，佐哈尔