# 安全软件开发生命周期:同步开发和安全性

> 原文：<https://devops.com/the-secure-software-development-life-cycle-syncing-development-and-security/>

在过去的五到十年里，软件开发的本质已经发生了巨大的变化。在过去，每 6 到 18 个月就会发布一次大型软件，而现在的发布时间表已经变得更加频繁了。软件开发的瀑布模型已经演变成我们现在所知道的 DevOps 模型。

因此，DevOps 对传统的瀑布式安全接触点进行了变革。本质上，DevOps 已经改变了应用程序安全性需要实现的本质。为了避免开发过程中的摩擦，应用程序安全活动必须适应 DevOps 实践的新世界。它必须超越基本的威胁建模、设计审查和两周的笔测试。

在 DevOps 下，一些开发组织现在每天、每周或每两周发布一次软件。但他们仍在努力应对旧的应用程序安全模型。因此，开发和安全测试可能会不同步——您不能对每周发布的软件进行为期两周的笔式测试。这些组织需要在其 SDLC 中获得有效的安全保证，即良好、快速、早期以及最重要的自动化。

## **软件开发不断变化的本质**

软件开发的方式一直在变化。而且还在不断加速。应用程序安全性需要改变才能跟上。自动化将在支持应用安全以保持开发运维节奏方面发挥关键作用。DevOps 需要自动化来有效地处理每天、每周和每两周发生的软件发布节奏，并提高 SDLC 内的敏捷性。

例如，当自动化管道将应用安全扫描嵌入提交前检查时，DevOps 加速。这样，每次开发人员签入代码时，都会应用一致级别的应用程序安全测试，从而实现完全自动化的签入过程。但是自动化并没有为每一次代码变更将开发人员锁定在相同的安全级别上。例如，如果变更仅涉及更改徽标的颜色，就没有必要进行大量的安全扫描和人工操作。至少不会像应用程序访问敏感数据时那样。

因此，自动化不再给开发人员提供季度 SAST 结果，而是在开发人员签入代码时(通过某些 IDE 插件)将代码分析放在他们面前。当开发人员仍在代码中时，向他们展示代码分析结果有几个好处:

*   开发人员对这些代码仍然记忆犹新。
*   当开发人员还在思考代码时，编码问题可以更早更容易地被发现。
*   它减轻了开发人员日后忘记代码上下文的风险。

总的来说，应用安全的自动化程度越高，就越有利于开源验证、容器扫描、QA 测试、API 安全等。

## **自动化安全保障和带外活动**

在开发运维中实施测试时，您必须平衡自动化安全保证和带外活动。这意味着有时放慢自动化安全流程是合适的。即使在完全自动化的开发运维流程中，您也可能需要放慢速度来进行必要的更改。诚然，代码的改变，比如仅仅改变一个 web 应用程序的背景颜色，可能不会有太大的风险。自动化 DevOps 步骤并推出变更是没有问题的。但是，如果您的 web 应用程序与客户数据交互，您应该谨慎地放慢速度，带外进行下一次应用程序安全测试，并确保您的程序是正确的，因为它的风险要大得多。

在应用程序的每个版本中，都有不同级别的风险和严重性。开发组织需要接受这一点，并适应每个版本的潜在风险和严重性级别。然后，他们需要提供适当级别的安全保证和安全覆盖，无论是在 DevOps 工作流中自动执行、带外执行还是两者的某种组合。

## **快车道上的生活**

对于 DevOps 组织来说，有两种途径吸引他们:安全快车道或安全慢车道。您可以在整个开发组织中创建一个自动化的 DevSecOps 过程——安全快车道。但是，对于企业来说，没有一种通用的 DevSecOps 流程。这是因为在一个企业中可能有数百个开发团队。而且并不总是有一个所有开发团队都可以遵循的标准化过程。 让自动化安全适应每个开发团队是一个挑战。在安全快车道上的人应该使用安全冠军与开发团队合作，并成为帮助他们了解应用程序安全需求和补救指导的关键人物。

在安全慢车道上，单个开发团队仍然可以快速前进。不同之处在于，他们会选择对该团队最有意义的 SDLC 工具。然后，他们还应该选择最适合自己的应用程序安全工具。组织的底线是，应用程序安全性需要包含一个可接受的开发人员摩擦水平，以使 [DevSecOps](https://devops.com/survey-surfaces-root-causes-of-devsecops-tension/) 工作。如果有太多的摩擦，开发人员将绕过应用程序安全性，以利于加快编码活动。