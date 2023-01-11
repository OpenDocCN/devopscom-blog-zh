# 美国心理协会发现 CI & CD 有治疗作用

> 原文：<https://devops.com/american-psychological-association-finds-ci-cd-therapeutic/>

美国心理学协会(APA) 是美国最大的心理学科学和专业组织，出版 PsycINFO 数据库，其中有 400 万份记录和 90 多份同行评审的期刊、书籍和其他出版物，APA IT 架构高级主管 Beverly Jamison 说道。“我们维护着一个心理测试和测量以及心理治疗演示视频的数据库，”贾米森说。APA 还公布会员信息和其他数据。

因为包括研究人员、从业人员、其他专业人员、学生、媒体和公众在内的广泛受众使用这些数据，所以 APA 对数据及其元素进行精确的清点，检查其质量，并以多种方式交付，包括作为 B2B 和 B2C 环境中的集成和多媒体材料。

CI 和 CD 前后的 APA 开发和运营

当 Jamison 加入 APA 时，一些像她一样的基于 perl / shell 的程序员使用 VI 编辑器作为他们的 IDE，而其他 ColdFusion 成员使用 Dreamweaver 作为他们的 IDE。Jamison 说，开发人员在非工作时间直接部署到实时系统，在部署完成后，开发人员和一个 QA 人员进行测试。

今天，APA 使用 [svn](https://subversion.apache.org/) 对他们已经习惯的遗留开发项目进行版本控制，并使用 Git 和 [BitBucket](https://bitbucket.org) 对似乎从中受益的新项目进行版本控制。“我们使用 Ant 作为脚本，从版本控制中部署代码。贾米森说:“对于单元测试，我们对 xquery 使用 X-Ray，对 java 使用 [JUnit](https://junit.org) ，对 javascript 使用 [mocha](https://mochajs.org) 。

Jamison 解释说，APA 使用 [Roxy](https://github.com/marklogic/roxy) 社区工具部署到 MarkLogic，以处理 MarkLogic 数据库实例和配置，这提供了 MarkLogic 数据库的一致性。

开发和运营团队中每个团队的性质和目的决定了工具的使用。MarkLogic 团队的工作决定了一种应用程序的使用，而身份和集成服务团队的工作重点需要另一种应用程序。MarkLogic 团队处理通常很复杂的数据服务和数据模型；Jamison 解释说，因此他们大量使用单元测试来确保单一的改变不会导致整个软件崩溃。Identity and integration services 使用 Jenkins 编写构建脚本，并确保每个构建都是最新的；Jamison 说，QA 分析师通过测试来确保他们的复杂场景是可靠的。同样，UI 团队还有另一组优先级和用法。

APA 新功能开发过程的全景

Jamison 解释说，首先，开发人员将检查从 subversion 到本地 IDE 的分支，制作并测试修改后的代码，对现有代码运行单元和回归测试，并更新单元测试、配置脚本和任何所需的脚本更改。然后，该过程将包括更新任何 JIRA 票证，并为即将发布的版本标记适当的版本号。

Jamison 说，代码将从 svn 部署到给定的 IDE 进行 QA 测试，开发人员或工程师将根据系统的规模和复杂性以及当前系统状态来运行这些测试。

然后，代码将被部署到集成的 UAT 环境中，供业务团队进行测试。一旦获得批准，我们将安排一个产品发布，由系统工程师处理面向公众的服务器的部署，”Jamison 说。

CI & CD 如何影响/推动这一发展过程

CI & CD 过程让开发人员和工程师在添加新特性时有更大的自由，减轻了他们对现有软件版本造成大范围破坏的担心。一个小的特性变化或错误修复可以看到上述过程中的步骤紧密地连续发生，因为 CI 和 CD 过程避免了必须恢复代码的风险。Jamison 说:“一个主要的新特性或数据模型的变化将意味着在不同的日子里采取这些步骤，并在每一天都有明确和正式的签署。”

最后的想法

简而言之，Jamison 提醒说，虽然工具很重要，但是团队如何致力于在有纪律的 CI 和 CD 实践中使用它们才是最重要的。