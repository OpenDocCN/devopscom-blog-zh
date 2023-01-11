# SIOS 技术自动重启 AWS EC2 虚拟机实例

> 原文：<https://devops.com/sios-technology-automates-rebooting-of-aws-ec2-vm-instances/>

SIOS 科技公司本周推出了 SIOS AppKeeper，这是一款能在 EC2 虚拟机出现故障时自动重启的工具。

SIOS 产品和营销高级副总裁 Michael Bilancieri 表示，SIOS AppKeeper 是 SIOS 历史上为实现服务器和集群故障转移所做工作的延伸。Bilancieri 说，然而，许多组织不需要这种级别的可用性，所以 SIOS 开发了 AppKeeper，以提供一种自动重启云中虚拟机的方法。

他说，SIOS AppKeeper 还提供了一个仪表板，DevOps 团队可以通过它集中管理 EC2 问题产生的警报流。SIOS AppKeeper 是一个软件即服务(SaaS)的应用程序，所以没有软件安装。相反，组织登录到他们的 AWS 帐户，并选择要监控的实例和服务，以及他们希望 SIOS AppKeeper 提供的保护级别。

SIOS AppKeeper 的定价从每个 EC2 实例 40 美元起。默认情况下提供监控和警报功能。重启服务、重启实例和仅当服务重启失败时重启实例都是选项。Bilanieri 说，组织可以选择通过提供的图形用户界面或应用编程接口(API)访问 SIOS AppKeeper。

此前，SIOS AppKeeper 仅在日本可用。根据这些客户的数据，只有三个 AWS EC2 实例的普通客户每个月至少经历一次停机。Bilancieri 指出，使用 SIOS AppKeeper，客户能够减少 90%的停机时间。

他说，SIOS 将根据客户需求考虑增加对其他公共云的支持。

云服务提供商与“宠物对抗牲畜”的风气保持一致，倾向于将虚拟机视为一次性的。然而，Bilancieri 说，每当出现问题时，IT 团队中的一些人仍然需要花时间重启虚拟机。

尽管在开发运维时代，IT 管理出现了无情的自动化趋势，但仍有许多任务需要手动执行。随着云计算环境中工作负载数量的不断增加，这些任务一起降低了 IT 运营的速度。当然，有许多方法可以在云中自动化 IT 流程。SIOS 正在为一种更简单的管理 EC2 实例的方法提供案例，这种方法不需要 IT 团队建立一个完整的 IT 自动化框架。

许多 IT 团队会选择创建自己的脚本来管理 EC2 实例。然而，经常出现的情况是，这些脚本没有得到很好的记录，并且随着时间的推移不能很好地扩展。此外，每当编写了组织所依赖的脚本的 IT 专业人员离开组织时，就没有人来更新和维护该脚本，IT 团队的新成员最终会编写另一个脚本来执行相同的功能。

在 IT 环境中总会有某种类型的脚本。然而，在 DevOps 时代，开始减少那些需要支持的脚本数量的时间可能就在眼前。

— [迈克·维扎德](https://devops.com/author/mike-vizard/)