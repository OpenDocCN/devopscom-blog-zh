# 什么是 DevSecOps，如何在 SDLC 上启用它？

> 原文：<https://devops.com/what-is-devsecops-and-how-to-enable-it-on-your-sdlc/>

在过去的三到四年里，IT 世界的所有公司都采用了敏捷和不同的应用程序开发方法，这些方法利用不同部门或领域的工作，帮助他们开发新产品和发布新功能，以改善他们的流程和基础设施。

在这个新的敏捷和 DevOps 世界中，团队中的每个人都参与到他们应用程序的快速变化和发展中，我们正在促进每个人在安全方面的责任——这就是 DevSecOps 加入的原因。

## **什么是 DevSecOps？**

DevSecOps 是一个新模型，它为应用程序中的安全实现提供了责任；从规划、设计、开发、QA/测试，到发布以及在生产环境中操作。

当在软件开发生命周期(SDLC)上实现 DevSecOps 时，组织将经历持续的集成，并将注意到合规性的成本降低了，代码不断地被正确地分析、测试、交付和发布。

DevSecOps 让每个人都能实施安全流程，并让他们负起责任。

## 为什么它很重要？

正如我之前在博客中提到的，在这个快速变化的时代，一切都在以非常快的速度发展。我们不断发现跨平台和操作系统的漏洞和违规，补丁程序不断发布，但我们作为公司运营团队的一部分，无法承受 IT 系统/应用程序的任何一方存在漏洞的风险。

## **主要优势**

*   减少代码中存在的漏洞。
*   减少您的 IaC 技术中存在的漏洞。
*   减少利用您的应用程序的方式
*   减少停机时间。
*   提高应用程序的稳定性、可用性和安全性。

## 如何在我当前的 DevOps 管道或 SDLC 上启用 DevSecOps？

DevSecOps 是一种必备的方法，需要集成到您的 DevOps 流程/管道中，以帮助您提高 SDLC 的安全性。

为了在当前 DevOps 管道或 SDLC 中启用 DevSecOps，需要遵循五个重要阶段。以下是实现它的关键阶段:

第一阶段:确保地方发展。 从实现安全的工作环境开始。当你开发一个应用程序时，大多数情况下你会使用开源技术。Docker 在这一阶段是一个很好的帮手，因为它自动化了本地机器上的基础设施和服务部署。因此，当您使用这个现成的 docker 环境时，请确保您使用的是最新/更新版本的 Docker 映像，并扫描它们是否存在漏洞。甚至官方提供的图片也有需要修补的漏洞。

第二阶段:版本控制和安全分析。 上传源代码时启用漏洞。让多只手或多人处理一段代码可能会导致漏洞，尤其是当他们处于远程时。Git 系统对于团队成员和代码之间的协作是一个很大的改进。当团队成员上传一段代码时，我强烈建议您对代码依赖项和核心启用自动化安全性测试。一些很好的替代品是 Snyk 或 Sonatype 的 Nexus。

第 3 阶段:持续集成和构建。 当创建开发映像/包时，您需要确保您的构建工具或系统具有适当的安全性。它使用 https://协议，经过适当的强化和保护，可用于攻击缓解，甚至无法通过互联网访问。这里可以使用的工具有 Jenkins，Circle CI，AWS CodeBuild，Google Cloud Functions，Azure DevOps。

第四阶段:推广和部署。 当部署到一个环境中时，通过您的 CI/CD 工具插入环境变量，并尝试将它们作为秘密进行管理。为了增强您的安全协议，建议对它们进行适当的加密和管理。

第 5 阶段:基础设施安全。 当你的 app 部署完毕，确保你有一个 IDS(入侵检测系统)。像 OSSEC 或 Wazuh 这样的工具将有助于保护你所有的主机。

![](img/513a776ca8005fce5535cb970d7c2a7c.png)  一旦你的代码进入生产阶段，并不意味着它将是 100%安全的。每天都有新的漏洞出现，但这一周期将帮助您和您的团队在监控、配置、重新配置、调整和部署环境解决方案时，针对所有已知漏洞库测试您的代码。

## **工具和流程**

这些是您需要在 DevSecOps 流程中启用的工具:

*   CI/CD 工具。
*   秘密经理。
*   版本控制系统。
*   Docker 编排工具。
*   安全分析工具。

这些是过程:

*   自动化回归测试。
*   动态测试。
*   自动化漏洞评估。
*   自动化集成。
*   升职。
*   自动化部署。

## DevSecOps 的理想工作流程是怎样的？

1.  开发人员创建一个新代码，并将其集成到 VCS 中。
2.  来自 QA 团队的成员检索代码来执行静态代码分析，以识别安全缺陷或功能任务。
3.  使用 IaC(如 Terraform、CloudFormation、Chef 或 Puppet)自动创建测试环境，并将安全配置添加到系统中。
4.  测试自动化套件是通过一个工具(通常是 Selenium 或任何其他执行后端、UI、集成、安全性和 API 测试的工具)来执行的。
5.  测试套件执行成功后，新的更改将被发送到生产环境。
6.  新版本的代码现在将在生产环境中使用 APM 或云原生监控工具进行监控。

遵循这些要点，您可以确保您的应用程序遵循 TDD 实践，从而提高代码质量、合规性、增加生产代码的发布数量并缩短上市时间，这对于任何组织都是至关重要的。

## **启用 DevSecOps 有哪些挑战？**

*   **启用太多工具:启用太多工具会成为 SDLC 的一个问题，尤其是当您的团队不习惯处理开发运维/安全任务时。这里的主要建议是慢慢开始。开始时，只启用必要的工具来让您的团队熟悉流程，当您觉得您的团队准备好了时，再添加更多的工具。**
*   **习惯方法:所有团队都需要一些时间来适应 DevSecOps 方法/文化，并继续遵循它，以符合您的业务需求的规范。努力保持最新状态，并指导您的团队掌握最新技术。**
*   **在过程上追求完美:要记住，所有的 DevSecOps 过程都不会完美，但随着时间的推移，它会变得成熟。团队总是试图追求完美，这只会导致更多的集成或依赖带来更多的问题。**

## **结论**

最后，我认为每个组织都必须努力转向 DevSecOps 方法或流程，并组建一个专注于安全性的多学科团队。这就是组织如何从开发运维过渡到开发运维的方式。允许他们所有的合作者对他们正在积极开发的部分负责。

——[吉列尔莫自行车](https://devops.com/author/guillermo-velez/)