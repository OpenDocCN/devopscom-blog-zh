# TypeScript 是新的 JavaScript 吗？

> 原文：<https://devops.com/is-typescript-the-new-javascript/>

虽然 JavaScript 经常是各种规模的前端和后端应用程序的首选语言，但它不是唯一的选择；也不一定是最高效或最划算的。TypeScript 逐渐成为应用程序开发的首选语言——尤其是对于大型应用程序。节省时间和成本的好处是显著的，一些组织甚至将最初用 JavaScript 开始的项目移植到 TypeScript。

## 什么是 TypeScript？

虽然用 JavaScript 编写的程序数量呈指数级增长，但这种编程语言表达不同代码单元之间的关系并在早期减少编码错误的能力却没有跟上。加上 JavaScript 不一致的语义，这使得 JavaScript 驱动的应用程序开发难以大规模管理。

TypeScript 于 2012 年发布，旨在解决 JavaScript 在开发大规模应用程序方面的不足。它是一种开源的强类型编程语言，通过添加可选的静态类型在 JavaScript 上构建。类型支持在代码执行前对其进行结构化和验证，这在开发大型应用程序时非常有益。它们还提供了关于代码的附加信息，这些信息为其他开发人员提供了更好的文档，并促进了协作。

TypeScript 是 JavaScript 的超集，这意味着任何 JS 代码也是有效的 TS 代码——只要 TS 配置设置为与之兼容。它输出纯 JavaScript 代码，允许开发者自由使用 JS 库、工具和框架。它运行在 Node.js 或任何支持 ECMAScript 3 或更高版本的浏览器上。它还支持面向对象的编程特性。

## JavaScript 的缺点

JavaScript 是世界上最流行的编程语言之一，非常适合小型项目。然而，它的缺点——其中许多会影响项目成本和代码交付时间——为考虑诸如 TypeScript 之类的替代方案提供了强有力的理由，尤其是对于较大的项目。

这些缺点大多与缺乏类型和编译时错误检查有关，这使得 JavaScript 不太适合企业和大型代码库中的服务器端代码。以下只是它的一些缺点:

*   JavaScript 采用动态类型，这意味着脚本可以编译，即使它们包含可能阻止它们正常运行的错误。
*   因为 JavaScript 是动态类型的，所以它允许一个变量分配多个属性。它不会让开发人员立即知道一个变量可以包含什么。这很容易分配错误的属性。
*   由于 JavaScript 是一种解释型语言，错误只能在运行时发现。代码需要在被测试和验证之前运行，所以在 JavaScript 代码中发现 bug 和错误需要花费相当长的时间。
*   为了消除不准确性，有必要手工验证代码的类型和语法正确性。这延长了开发时间，延长了产品的交付周期，增加了开发成本。
*   JavaScript 代码在客户端执行，因此用户可以看到。因此，漏洞和疏忽有可能被恶意利用。
*   由于开发人员必须弄清楚他们正在使用的结构的属性以及数据类型，因此可能会导致新开发人员漫长的入职时间。虽然 JSDoc 可以用于记录代码和注释类型，但是仍然需要同步实际的代码和文档。缺乏同步反过来会误导开发人员，并使新的业务需求特性的引入复杂化。
*   JavaScript 是基于原型的，而不是基于类的。它不被认为是一种纯粹的面向对象编程语言，尽管它可以遵循一些面向对象的编程原则。

## 打字稿的优势

TypeScript 是 JavaScript 的超集。如果开发人员了解 JavaScript，那么利用 TypeScript 提供的特性(这些特性弥补了 JavaScript 的许多不足)并没有太多的学习曲线，而且它还可以提供额外的好处。

例如，使用 JavaScript，变量可以从一个属性开始，然后变成一个对象或字符串。这些不一致会产生在大型应用程序中难以解决的问题。另一方面，TypeScript 分析代码并试图在运行时之前确定正确的变量类型。一旦变量类型被赋值，它就保持不变。TypeScript 的编译器还有助于缩短开发后期的 QA 和测试过程。

TypeScript 还帮助开发人员快速找出代码中变量的用途。它还可以建议函数、类或组件中的可用属性。能够快速查找变量非常重要，因为它减少了调用错误函数或意外跳过变量声明的可能性。bug 和错误的减少减少了修复这些问题所需的时间，因此减少了总的开发时间。这让开发人员有更多的时间来处理应用程序逻辑和修复可能对应用程序性能和可用性有害的错误。根据 [Airbnb](https://www.typescriptlang.org/) 的事后分析，在公司在整个组织中采用 TypeScript 后，他们遇到的 38%的错误是可以预防的。

作为一种静态语言，TypeScript 在编译时执行类型检查，标记类型错误并帮助开发人员在开发的早期发现错误。使用大型代码库时减少错误可以节省数小时的开发时间。

清晰易读的代码易于维护，即使对于新加入的开发人员也是如此。因为 TypeScript 要求分配类型，所以代码立即变得更容易使用和理解。本质上，TypeScript 代码是自文档化的，允许分布式团队更有效地工作。团队(和个人开发人员)不必花费过多的时间来熟悉一个项目。

由于上下文感知的建议，TypeScript 与编辑器的集成也使得验证代码变得更加容易。TypeScript 可以确定哪些方法和属性可以分配给特定的对象，这些建议有助于提高开发人员的工作效率。

TypeScript 广泛用于自动化后端和 web 应用程序的基础结构和 CI/CD 管道的部署。此外，客户端部分(例如，当使用 Angular 时)和后端可以用同一种语言编写—TypeScript。这种灵活性允许懂一种编程语言的工程师覆盖系统的所有部分。

因为 TypeScript 本质上是将文件转换成 JavaScript，所以将现有代码迁移到 TypeScript 既简单又快速。这通常可以简单地通过运行编译器并在语言无法识别的地方添加类型来完成。没有必要对代码进行修改。

开发人员已经注意到了 TypeScript 的好处。在 JS 的 [2020 状态受访者中，有 78%的人使用过 TypeScript，其中 93%的人表示他们会再次使用它。TypeScript 越来越受欢迎。在 2020 年开发者调查](https://2020.stateofjs.com/en-US/technologies/javascript-flavors/)[Stack Overflow](https://insights.stackoverflow.com/survey/2020#most-loved-dreaded-and-wanted)中，它被评为第二受欢迎的编程语言。

## TypeScript & AWS:一起更好

大规模应用程序开发项目考虑 TypeScript 还有另一个令人信服的原因。它得到了 AWS 的全面支持，AWS 是现代应用程序设计和开发的领先云平台，这在 Gartner 的云基础架构和平台服务魔力象限 中有所提及。

以下服务和工具与 TypeScript 无缝集成，使您能够将这种语言用于大量任务:

*   [AWS CDK](https://aws.amazon.com/cdk/) 提供基础设施即代码(IaC)，一键自动部署整个基础设施。您还可以自动创建 CI/CD 管道，以便将来按需启动特定作业。
*   [AWS Lambda](https://aws.amazon.com/lambda/)允许您使用自动缩放和高效的定价方案在无服务器模式下运行计算任务。
*   亚马逊 [EC2](https://aws.amazon.com/ec2/?ec2-whats-new.sort-by=item.additionalFields.postDateTime&ec2-whats-new.sort-order=desc) 、 [ECS](https://aws.amazon.com/ecs/?whats-new-cards.sort-by=item.additionalFields.postDateTime&whats-new-cards.sort-order=desc&ecs-blogs.sort-by=item.additionalFields.createdDate&ecs-blogs.sort-order=desc) 和 [EKS](https://aws.amazon.com/eks/) 可以覆盖你的任何任务，并为运行用 TypeScript 编写的应用程序提供广泛的解决方案——从裸机服务器到数百个 Docker 容器的复杂集群。

## 优化您的应用程序开发项目

应用程序开发项目期间做出的所有决策都会影响总体成本和上市时间。这包括使用正确的编程语言，使用最合适的云平台和资源。

在处理应用程序开发项目时，一刀切的方法很少奏效。花些时间来定义你的需求和优先事项，选择最好的资源来交付最好的结果。