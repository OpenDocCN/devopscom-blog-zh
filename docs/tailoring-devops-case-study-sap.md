# 为您的 IT 量身定制开发运维:SAP 案例研究

> 原文：<https://devops.com/tailoring-devops-case-study-sap/>

经常有人问我，DevOps 原则是否可以应用于 SAP 等传统环境。通过一些[裁剪](http://offers.automic.com/tailor-devops-july2015)，他们显然可以。但是你应该意识到某些限制。

从传统 IT(SAP 软件交付流程在业务分析师、开发、QA 部门和 IT 运营部门之间划分)向[敏捷开发运维](http://automic.com/devops)组织的敏捷转型需要以下步骤:

1.  根据业务能力而不是技术来组织开发团队——在定义结构时，确保团队尽可能独立自主地工作。
2.  提升业务分析师对产品负责人的技能。
3.  使用 SCRUM 或看板，按照敏捷原则组织开发输出。
4.  连续地将 QA 转移到开发团队中——一个独立的 QA 团队可以负责回归、安全和性能测试的自动化，但是不应该参与日常的测试活动。
5.  用作业调度的专业知识不断扩充开发团队。
6.  引入自动化工具来简化升级(传输)过程，以适应上层环境的变化，并最终投入生产。
7.  添加单元测试和静态代码分析(例如，用于安全性和性能检查)。
8.  自动化回归、安全性和性能测试。
9.  将 SAP 平台团队的职责集中在管理平台上(监控、修补、升级、环境供应和更新、性能测试)，并将变更的传输(“部署”)留给开发团队。
10.  使用自动化工具进行环境克隆和刷新。
11.  将 SAP 平台团队推向看板。

虽然这些步骤类似于其他技术环境中的敏捷开发运维转换，但是具体的自动化工具链是非常不同的。

您不再使用 Git、Jenkins、Ansible 或 Chef，而是使用 SAP 和第三方供应商的工具进行代码检查和分析、传输管理、测试自动化、环境刷新、性能测试等等。这需要很难找到的技能。此外，不同的工具可用于覆盖不同的 SAP 平台(“ABAP 堆栈”和“Java 堆栈”)。

SAP 还有另一个特点:尽管新技术支持隔离的 SAP 环境的快速克隆以及用当前数据持续刷新，但这受限于某些基础架构。调配和管理单一 SAP 环境的成本和交付周期仍然相对较高。

因此，出于开发、测试或发布的目的，几个团队通常不得不共享一个 SAP 环境。这需要协调，并对连续交付设置了限制。在最好的情况下，可以通过打开生产前环境进行几个小时的传输和应用程序测试，然后再锁定几个小时进行回归、性能和安全性测试(包括批处理)以及生产交付，来实现日常生产部署。

总之，如果考虑到特殊性，DevOps 的许多原则可以应用于 SAP 应用程序交付。

虽然针对 SAP 环境的[持续部署](http://offers.automic.com/how-to-achieve-continuous-delivery-without-downtime-on-demand)仍是一个目标，但每日发布现在已经可以实现。

**DevOps 十几个奖项！** Automic 目前获得了发布管理和持续交付类别的 DevOps 十二项大奖提名。[今天就为我们投票吧！](https://bit.ly/DOVote)