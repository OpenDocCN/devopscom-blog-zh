# HashiCorp 为 IT 运营添加 Terraform 工作流工具

> 原文：<https://devops.com/hashicorp-adds-terraform-workflow-tools-it-ops/>

HashiCorp 本周通过使共享 Terraform 配置文件变得更容易来实现自动化 IT 操作的模板化，这使得在不知道如何编码的情况下以编程方式调用暴露应用编程接口(API)的基础设施变得更简单。

HashiCorp Terraform Enterprise 提供内部版本或软件即服务(SaaS)应用程序，供 IT 运营团队使用。添加了一个 [HashiCorp Terraform 企业模块注册表](http://www.globenewswire.com/news-release/2017/12/12/1253349/0/en/HashiCorp-Releases-Next-Generation-of-Terraform-Enterprise-for-Provisioning-Cloud-Infrastructure.html)功能，使 IT 运营团队能够实现 Terraform 配置文件的发布和订阅机制。

公司首席技术官 Armon Dadgar 表示，HashiCorp Terraform Enterprise 旨在使 IT 运营团队能够更快地响应开发者对基础设施资源的请求，而无需他们开发编程技能。他说，为传统企业 It 组织工作的开发人员不太可能很快接管 IT 基础设施的控制权，Hashicorp Terraform Enterprise 允许 IT 组织在其工作流程中注入一定程度的灵活性，而不需要 IT 运营团队完全重新设计现有流程。

Dadgar 说，hashi corp Terraform Enterprise Module Registry 进一步扩展了这种能力，使开发了使用声明性 terra form 配置文件的专业知识的 it 运营专业人员更容易与团队的其他成员共享这些文件。

* * *

**相关内容:**

[hashi corp terra form Enterprise 增强了 IT 管理员的能力](https://devops.com/hashicorp-administrators-terraform-enterprise/)

[运营管理将“运营”置于开发运维中](https://devops.com/operations-management-puts-ops-devops/)

* * *

同时，希望在 HashiCorp Terraform Enterprise 上构建工作流应用的 IT 运营团队可以使用 HashiCorp 公开的一套应用编程接口(API)。此外，该公司还改进了 Terraform 的用户界面，现在可以通过将 Terraform 文件组合成模块化组件来创建工作区，这些组件可以分配给特定的 IT 团队。通过支持安全访问标记语言(SAML)以及 HashiCorp 开发的 Sentinel 策略管理软件来提供访问权限。

HashiCorp 实现 IT 运营自动化的方法击中了企业中 DevOps 争论的核心。虽然网络规模的公司通常有能力雇用具有编程技能的 IT 专业人员来管理 IT 基础架构，但一般的企业 IT 组织仍然依赖管理员来管理服务器、存储和网络。不仅 IT 管理员供不应求，如果他们知道如何编程，他们中的大多数也不会在 IT 运营部门工作——他们会编写和测试应用程序。

自动化 IT 基础设施管理的竞争方法尽管已经存在多年，但尚未获得主流认可，主要是因为它们需要编程技能。声明性方法允许 IT 基础设施仍然作为代码来管理，IT 运营团队的阻力较小，他们更倾向于使用声明性工具。事实上，对于向现代 DevOps 实践的过渡需要组织先获得新工具还是先获得新工具的程度，一直存在先有鸡还是先有蛋的争论。HashiCorp 方法通过提供使 IT 运营团队首先变得更高效的工具，最终使他们能够实施对现有 IT 文化破坏性更小的新流程，从而达到了折中的目的。

— [迈克·维扎德](https://devops.com/author/mike-vizard/)