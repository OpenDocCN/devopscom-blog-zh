# Docker 对 Docker Hub 进行修补以提高性能

> 原文：<https://devops.com/docker-tinkers-docker-hub-performance-improvements/>

Docker 正在加强其基础设施组件，以适应这种曲棍球棒式增长不可避免地会出现的使用量和广泛的用例。根据该公司昨天发布的公告，最新的改进来自于过去一个月对 Docker Hub 的改进。

[Docker Hub 团队报告](https://blog.docker.com/2015/01/docker-hub-improvements/)在添加了安全增强功能以防止暴力登录尝试后，许多变化是由 2014 年底遇到的性能问题引发的。他们报告说，这些增强增加了“登录过程的开销”

他们写道:“在正常负载下，差别不大，但随着登录尝试次数的增加，网站性能开始下降。”性能下降不仅影响了 Docker 引擎登录、推送和拉入，还影响了整个 Docker Hub 网站

在确定导致问题的直接问题的过程中，Docker 的工程师审核了整个系统，并正在重新构建授权、推拉系统以提高性能，并隔离系统以实现隔离效果，确保不会出现级联问题。

在短期内，已经做出的一些修复包括扩大基础设施容量，包括将 Docker 集群中的服务器增加两倍，以获得四倍的计算能力，以及将生产数据库升级为 20 倍的 RAM。它还改进了登录基础设施，增加了数据库索引和缓存。该团队还调整了查询速度，并修复了导致数据库锁定的问题。Docker 还将其后台工作队列代理从 Redis 切换到 RabbitMQ，并将后台工作队列转移到他们自己的服务器集群。此外，还对监控和指标收集以及搜索功能进行了改进。

与此同时，他们希望进一步改进，包括 API 节流、分解较大的服务以提高可伸缩性、用性能更好的库替换暴力防御库，以及添加 API 指标和监控以尽早阻止性能问题。

“我们已经取得了一些良好的进展，但我们还没有完成，我们还有很多计划，”Docker Hub 团队写道。“我们将继续对每个版本进行改进，以便 Docker Hub 随着时间的推移变得更快、更可靠。”

鉴于 Docker 社区的飞速发展，12 月份出现的这类问题是可以理解的。甚至就在 6 个月前，Docker 的总下载量还不到 300 万次。到 12 月，这个数字已经上升到 1 亿。尽管 Docker 容器的安全性存在一些问题，但 Docker 的发展轨迹似乎很有希望。就在 9 月份，该公司获得了红杉资本(Sequoia)4000 万美元的 C 轮投资，在过去的几个月里，它宣布了许多高水平的合作伙伴关系，包括与 VMware、微软和 AWS 的合作。

Docker 最近的合作关系是在上周宣布的，当时它与谷歌合作，以便这家在线巨头可以在其云平台上为 Docker 提供私人注册服务。目前处于测试阶段，Google Container Registry 将为 Google cloud 客户提供安全的托管、共享和管理私有容器库，其中将包括强大的访问控制和服务器端加密。