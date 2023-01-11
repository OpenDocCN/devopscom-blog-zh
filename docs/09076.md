# 如何将现有基础设施迁移到 Terraform

> 原文：<https://devops.com/how-to-migrate-existing-infrastructure-to-terraform/>

基础设施即代码(IaC)支持通过代码而非手动流程来管理和配置基础设施。IaC 对于 DevOps 团队来说至关重要，因为它允许他们管理基础设施组件，如网络和负载平衡器，并在开发周期的早期在类似生产的环境中测试应用程序。它允许 DevOps 团队以安全、一致和可重复的方式构建、更改和管理基础架构。

虽然基础设施作为代码传统上可能令人沮丧，因为它需要手动创建云基础设施， [Terraform 将现有基础设施置于代码管理之下](https://devops.com/building-on-terraform-evolution-not-revolution/)，同时消除了手动流程。Terraform 是最受欢迎的开源 IaC 工具之一，因为它允许用户在可读的声明性配置文件中定义资源和基础架构，并轻松管理基础架构的生命周期。它还提供了其他一些优势，如管理多个云平台上的基础架构、快速编写基础架构代码、轻松跟踪整个部署过程中的资源变化、版本控制功能等。Terraform 可以在 AWS、GCP 和 Azure 等所有云提供商上运行，并且很容易安装在机器或远程构建服务器上。

## terra form 有何不同？

通过跨多个云部署基础设施来提高容错能力是一种常见的做法，因为使用单个云提供商可能会导致单点故障。多云部署可以轻松恢复一个地区或整个提供商的损失。但这可能很有挑战性，因为许多现有的基础架构管理工具都是特定于云的。

Terraform 解决了这些挑战，因为它与云无关，并且允许使用单一配置来管理多个提供商。它还可以通过简化管理和编排来处理跨云依赖关系。

Terraform 提供了一种灵活的资源抽象，使 DevOps 团队能够轻松地代表从物理硬件、虚拟机和容器到 DNS 提供商的一切。这种灵活性还可以管理单个应用程序，甚至整个数据中心，这使得它比其他 IaC 工具更受欢迎。

## 从现有基础设施迁移到地形

Terraform 以安全和渐进的方式将现有基础设施置于 as-code 管理之下。按照以下步骤，用户可以轻松地从现有基础设施进行迁移:

从以下链接安装 Terraformer】

[Terraformer 安装](https://github.com/GoogleCloudPlatform/terraformer#readme)

要从所有服务导入资源，请使用`-- resources="*"`

要排除某些服务，可以结合参数`-- excludes`从服务中排除资源。例如，`--resources="*" --excludes="iam"`

在机器上下载 Terraformer 后，用户可以将现有基础设施迁移到 Terraform 中。为了顺利迁移，所有内容都必须包含在一个命令中；否则，状态文件可能会丢失或被替换。要迁移手动创建的资源，您需要在一个命令中指定所有内容。

例如，为了在 Google Cloud 上设置它，必须从 Google Project 访问信息，并通过设置环境变量“Google_Application_Credentials”以及包含服务帐户密钥的 JSON 文件的文件路径来提供认证信息。在本例中，我们迁移了 GCP 的 GKE 集群。

T2`terraformer import google --resources=gke --filter=container_cluster=<Clusters-name separated by :> --filter=container_node_pool=<node-pools name separated by :> --regions=<region-name> --projects=<project-name>`

运行这个命令会将 GKE 的所有资源提取到本地机器上。但是，这需要更改后端来对 Terraform cloud 进行这些更改。下面是如何做到这一点:

T2`backend "remote" {`

T2`organization = "<organisation-name>"`

T2`workspaces {`

T2`name = "<Your workspaces>"`

后端应该保持在远程设置中。上述步骤确保 GKE 集群迁移到 Terraform 时不会出现任何中断。

## 迁移基础设施的挑战

虽然 Terraformer 是实现基础设施自动化并降低手动管理资源的复杂性的重要工具，但将基础设施迁移到 Terraform 也有其自身的挑战。 在导入命令中包含所有的服务是很重要的。如果做不到这一点，可能需要通过编写单独的文件来迁移基础架构，这可能是一项令人生畏的任务。 另一个挑战是，在导入不同的服务时，必须替换后端文件，否则可能会导致丢失远程后端的第一个基础架构备份。

## 迁移现有基础设施的重要性

将现有基础设施迁移到 Terraform 有几个好处，例如:

*   将所有现有基础设施轻松迁移到云中，不会造成任何中断
*   轻松管理云资源，同时跟踪变化
*   在 Terraform 云中安全部署资源

还有一点需要注意:Terraform 是一项相对较新的技术，采用它来管理组织的云资源可能需要一些时间和精力。使用 Terraform 有效管理云基础设施需要专业技能和培训。在处理像远程后端这样的概念时，使用它可能也是一个挑战。尽管存在这些问题，Terraform 为 DevOps 团队提供了巨大的优势，可以轻松管理基础设施。