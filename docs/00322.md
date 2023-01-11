# 确保企业开发中的安全性和管理风险

> 原文：<https://devops.com/ensuring-security-managing-risk-enterprise-devops/>

本系列中今天的问题来自典型大型企业中的开发人员——规避风险、严格控制、高度安全——这是任何开发运维转型的主要挑战:

问:我在一个大型政府部门工作，该部门的安全措施非常严格。我们有严格的职责分离政策，不能共享用户 id 或密码，难以共享代码，不能使用 AWS 或 Azure，审计一切，等等。DevOps 如何在我的环境中工作？

如果 DevOps 是关于协作和消除瓶颈，那么它必须包括安全性，从规划到编码到测试到运营；构建、交付和运行设计安全的应用程序。不幸的是，对于许多企业来说，安全性是应用程序交付生命周期中的主要障碍。

然而，安全性并不一定是 DevOps 的瓶颈。的确，这些具体问题都是解决了的问题。虽然我并不吹嘘自己有深厚的安全专业知识，但我可以根据我的经验(以及一些进一步的阅读，见下文)提出解决方案:

## 保持职责分离

大型企业必须保持职责分离，以防止(例如)流氓开发人员在没有检查和平衡的情况下给新代码添加后门并将其投入生产。但是，员工仍然可以在需要时获得所需的访问权限，仅此而已。当角色发生变化时，例如开发人员访问操作“飞行甲板”，或者操作员被借调到开发部门，[身份管理](https://www.google.com/search?q=Identity+Management)和访问控制可以根据需要自动提供适当的访问权限，并经过审核和符合政策。

## 保护特权用户 id 和密码

对于大型企业来说，共享密码是不可接受的，尤其是像[云控制面板管理员](https://arstechnica.com/security/2014/06/aws-console-breach-leads-to-demise-of-service-with-proven-backup-plan/)这样的特权账户。然而，[特权身份管理](https://www.google.com/search?q=Privileged+Identity+Management)允许员工从安全池中“检出”特权 id，根据需要使用它们(例如，用于中断修复)，然后在完成后将其检入。根据政策规定，访问可能需要额外的批准、时间限制、访问限制、击键记录、会话捕获等。这允许按需访问敏感 id，同时保持严格的审计和控制。

## 提供安全的跨团队界面

DevOps 的一部分是共享-流程、技能、知识…但也通过共享 API(无论是公共的还是专有的)重用代码和服务(或微服务)。这种共享加快了交付并降低了成本，但也可能带来风险。为了防止在共享代码和服务时出现[意想不到的后果](http://www.layer7tech.com/blogs/index.php/the-snapchat-breach-api-security/),[API security](https://www.google.com/search?q=API+Security)可以实现内部和外部共享，但具有用户认证(例如 OAuth)、粒度访问控制、容量/速率限制、阻止等控制。

## 支持安全的按需云访问

大多数企业员工无法在公司卡上启动 AWS 或 Azure 实例。甚至申请“批准”访问也可能需要数周时间。相反，安全专家可以针对“已知良好”或“企业级”服务设置自动化自助供应，并事先获得安全、人力资源、财务等部门的批准。这有助于维护必要的审计和控制，同时使 DevOps 员工能够快速轻松地采用云和其他服务。

## 使用自动化来维护安全性和治理

自动化是降低风险、确保法规遵从性和维护治理的强大方法。例如，发布自动化允许开发人员在没有个人访问生产系统的情况下部署新代码(工具获得访问权，而不是个人)。它还可以通过“已知良好的流程”限制对此类系统的访问，以确保部署符合策略。跟踪谁启动了部署维护了治理和报告的基本审计跟踪。测试自动化、数据管理、流程自动化、配置管理和其他自动化工具在整个应用交付生命周期中都提供了类似的安全优势。

## 拥有安全文化

当然，除了技术解决方案之外，还有更多的东西可以保护 DevOps。正如 DevOps 需要新的协作文化一样，良好的治理最终需要安全文化。在服务交付生命周期的每一步，安全都是每个人的责任。安全仍然是一个专家角色，所以安全专家应该在敏捷计划、站立和分类会议中占有一席之地，但是良好的治理是每个人的角色。开发人员、运营人员、测试人员、QA 人员和其他人员都需要应对安全挑战；安全专家应该与 DevOps 团队的其他成员分享他们的需求、知识、最佳实践和工具。

## 进一步阅读

在编写这篇文章的过程中，我依靠了许多其他人，他们帮助建立了[devopsec](https://www.google.com/search?q=devopssec)/[SecDevOps](https://www.google.com/search?q=secdevops)和 [Rugged DevOps](https://www.google.com/search?q=Rugged+DevOps) 的概念。关于这个主题的更多专业细节的一个很好的起点是 DevOps.com 上的 [SecDevOps 内容，特别是 Rich Mogull (](https://devops.com/?s=secdevops) [@rmogull](https://www.twitter.com/rmogull) )和 Andrew Storms ( [@st0rmz](https://twitter.com/st0rmz) )的工作。关于早期介绍，请查看 Gartner 的笔记，[devopsec:创建敏捷三角](http://blogs.gartner.com/neil_macdonald/2012/01/17/devops-needs-to-become-devopssec/)和 James Wickett ( [@wickett](https://twitter.com/wickett) )关于 [Rugged DevOps](http://ruggeddevops.org/) 的开创性工作。对于最近的想法，尝试一下 Threatstack 博客和 Edward Haletky([@ texi will](https://twitter.com/Texiwill))的端到端视图。最后，关于 DevOps 可审计性的一个很好的资源，请查看 Gene Kim ( [@RealGeneKim](https://twitter.com/RealGeneKim) )项目，即 [DevOps 审计防御工具包](https://plus.google.com/communities/103372669680429508474)。