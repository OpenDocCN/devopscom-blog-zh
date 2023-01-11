# 快速数据迫使开发运维采取新策略

> 原文：<https://devops.com/fast-data-is-forcing-new-strategies-in-devops/>

DevOps 已经成为一门至关重要的学科，开发和利用独特的工具和流程来更快速、高效和可靠地交付多种类型的应用程序。随着数据成为这些应用程序中更加重要的组成部分，DataOps 开始与 DevOps 携手合作，以更好地支持[数据](https://devops.com/rethinking-data-management-in-a-devops-environment/)在现代企业中的作用。

然而，新一代应用程序(如实时、数据流和微服务应用程序，包括越来越多的在云和数据中心内或跨云和数据中心运行的应用程序)已经开始威胁到作为 DataOps 和 DevOps 协作基础的既定实践和工具。DevOps 是围绕敏捷的思维模式构建的，但是规程本身必须做些什么来适应呢？

这些新应用程序诞生于快速数据的概念:当数据到达企业时，立即采取行动并对其做出反应。传统的大数据应用程序通常批量收集、汇总、存储和处理信息，与之相反，快速数据侧重于即时转换、提炼和分析数据，使用户、应用程序和服务能够快速处理这些信息。在许多情况下，这是为了支持更多种类的智能应用程序，这些应用程序有望在不需要任何人工干预的情况下对数据进行操作。

组织的好处表现为速度和洞察力的提高。虽然前者可能显而易见，但后者同样重要:了解当前正在发生的事情并采取行动，可以显著提高准确性、灵活性和响应能力。

对于 DevOps 来说，在这个快速数据应用的新时代，应用现有的实践和解决方案是不可能取得成功的。它需要一种进化，既包括那些工具/实践本身，也包括团队如何对待和思考成为数据驱动的组织的一部分的整个过程。

这是因为在快速数据世界中，许多事情都在发生变化:

*   应用程序不再是独立的，而是由许多相互依赖的组件组成，这些组件可能跨越地理位置、基础架构和学科。
*   数据流是这些组件之间的关键链接。
*   在数据到达数据湖或数据仓库等传统存储库之前，数据正在被收集、处理、分析和处理。
*   生产中的快速数据应用程序必须始终保持运行，以跟上数据流，并且必须频繁应对重大的扩展挑战，包括向上和向下扩展。

作为这些新考虑事项的一个示例，设想一个经典场景，该场景可能由数据库和内容应用程序组成，中间有中间层逻辑。一个典型的 DevOps 流程可能涉及对中间层逻辑的更新，然后对其进行部署、测试和迭代。

在快速数据领域，您可能有八个不同的数据服务与十几个不同的组件进行通信，所有这些组件都与更多的下游处理应用程序进行通信。在不了解各种数据服务和应用程序接口的情况下，孤立地部署任何更改都可能导致整个系统崩溃。在快速数据的世界中工作需要 DevOps 团队与 DataOps 合作，以验证单个组件可以无损害地更新和部署，或者确定如何将整个系统或部分系统作为一个集合进行部署。当接口点的数量相对较少并且依赖于标准协议或流程时，这些都是不考虑的因素。

幸运的是，DevOps 可以采取一些步骤来成功实现这些新的快速数据应用，包括:

*   认识到交付流/实时/快速数据基础设施的必要性，不仅对于生产环境，而且对于开发环境。单片批处理应用程序的大多数开发和测试都可以使用基本的基础设施来完成。然而，快速数据应用程序的开发和测试需要能够按需传输和处理数据的基础设施。开发运维团队需要部署能够轻松支持这一点的数据基础架构。
*   与 DataOps 专业人员和/或负责人合作实施技术和流程，轻松将快速数据应用程序从测试平台转移到完整的生产环境中。快速数据应用程序通常由一组服务组成，因此将应用程序投入生产需要一个精心协调和编排的过程。DevOps 需要让这个过程对开发人员来说尽可能简单可靠。
*   支持永不停机的环境。顾名思义，快速数据应用程序需要在数据到达时立即对其进行处理。这意味着不允许因升级或重新配置而停机维护。DataOps 团队需要识别和选择设计用于在出现故障以及日常维护和操作时无中断或无破坏性降级运行的技术。
*   从一开始就为云设计。快速数据应用程序通常全部或部分部署在云中，在企业内外收集、处理和分发数据。这使得开发运维团队选择能够提供云原生弹性、可扩展性(向上和向下)、高性能和易于配置/操作的快速数据技术变得至关重要。

如前所述，DevOps 团队调整他们对基础设施支持的数据流的观点也很重要，而不仅仅是考虑应用程序组件。

整体而言，数据通过一系列相互关联的组件流向结果；组件本身只是这个旅程中的过渡步骤。对任何给定组件的更改都必须考虑上游和下游的影响。如果一个组件被改变，上游源是否需要相应地调整？调整是否会影响依赖数据流的下游用户/应用程序？在更大的场景中，这个上游/下游之旅可能需要对不同的系统和业务流程进行多重绑定。不再可能以中断/修复几个互连组件的方式来应对变化，而是必须考虑对可能依赖于大量微服务的整个数据流进行部署或修改。

从零售和制造业到金融服务、媒体/娱乐等领域，快速数据应用不仅仅是未来的事情，它们已经到来，并且正在创造大量新的商机。DevOps 团队需要调整他们的实践和工具，以最好地适应这种新的模式，这种模式同样与数据流和应用程序有关。他们可以通过问一个简单的问题开始为这种新的快速数据环境做准备:如果我知道客户、合作伙伴和系统现在在做什么，我能做什么？

— [Karthik Ramasamy](https://devops.com/author/karthik-ramasamy/)