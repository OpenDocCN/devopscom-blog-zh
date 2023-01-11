# Groovy 对 JFrog Artifactory & Bintray 以及 Gradle 和 TeamCity 的使用

> 原文：<https://devops.com/slice-groovys-hip-use-jfrog-artifactory-bintray-gradle-teamcity/>

宝贝儿。

Groovy 的支持者将 Groovy 编程语言描述为动态和静态类型的，支持函数式编程和 OOP 作为一个包含 Java 编程语言的超集。“如果你愿意的话，这是一种兴奋剂！”Guillaume Laforge 说，他是 [Apache](https://www.apache.org/) Groovy 项目 PPMC 成员。Groovy 的几个常见应用示例将有助于说明它在编程领域的地位。

开发人员在各种项目的构建和测试阶段使用 Groovy，即使他们没有用 Groovy 编写应用程序。编码人员发现 Groovy 是一种编写和维护测试的诱人语言，因为它简明易懂。Laforge 说:“开发人员使用 Groovy 和 Spock 框架进行单元测试和行为驱动开发，使用 T2 Geb 进行 Web 集成测试。

程序员使用 Groovy 脚本来实现集成、配置、定制和插件的应用程序可扩展性。Laforge 说:“ [Jenkins](https://jenkins-ci.org/) Build Flow 插件是一个很好的例子，因为它使用户能够通过使用 Groovy 语言提取作业的流程逻辑来编排作业。Groovy 的其他用途包括特定领域语言、管理、自动化以及 Web、桌面和移动应用程序开发。

DevOps.com 探讨了 Groovy 从手工到自动化开发之旅的要素。

手动流程，不太好

当 Groovy 语言的开发人员从个人开发机器上发布软件并使用其他手工过程时，这就产生了几个问题。如果一个开发人员忽略了产生一个专用的发布分支，这可能等同于在加入主线源代码树之前将未提交的文件和本地变更直接转移到发布中，绕过谨慎的源代码控制需求。

“或者我们可能只是忘记为发布设置标签，或者我们可能会提交错误的版本号数据，”Laforge 说；虽然发布的版本是 x.y.z，但清单中的版本将是 x.y.w

在某些情况下，对于单独的开发人员机器，新开发人员会遇到差异。例如，执行项目构建的新开发人员可能会看到与依赖关系相关的挑战，例如当一个项目依赖于另一个已损坏“pom”(项目对象模型)文件的项目时。“本地存储库会充满奇怪的依赖关系，”Laforge 说。还有其他问题。

Groovy 完全自动化了它的发布过程

Groovy 在自动化方面的进步之一是在版本控制领域。Groovy 最终从 [CVS](https://www.nongnu.org/cvs/) 转移到 [Subversion](https://subversion.apache.org/) 到 Git，并从 Codehause 转移到 Github 作为其存储库。Laforge 说:“最近，随着 Groovy 进入 Apache 软件基金会孵化过程，我们将源代码转移到 Apache 的 Git 中。

今天，Groovy 开发人员向开源的 [Maven](https://maven.apache.org/) 仓库 Artifactory 发送快照，以测试他们的 bug 修复和特性。根据 Laforge 的说法，Groovy 应用了 [JetBrains](https://www.jetbrains.com/) TeamCity CI 服务器来构建工件和发行版；TeamCity 的 Artifactory 插件使 Groovy 能够使用 Artifactory 发布版本。Artifactory 和 Bintray 的集成使 Groovy 能够将所有东西都推送到 Bintray。依赖管理发生在 Bintray 的 JCenter Maven 存储库上。与 Maven Central 的同步支持正在检索依赖项的开发人员。

[Gradle](https://gradle.org/) 构建自动化工具支持 Groovy 的成熟构建设置，允许语言开发人员引导自己的编译器，使其能够构建 Groovy 代码。“这是我们可交付成果的一部分，也就是说，Groovy 基本上是自己编译的，”Laforge 说；"使用其他构建解决方案会更加困难."

深入研究，让 Gradle 和 TeamCity 协同工作有更多的好处。首先，它让 Groovy 有机会在不同的平台和环境上测试 Groovy 的不同风格和功能。“我们可以使用从 6 到尚未发布的版本的不同 JDK 版本来做到这一点。Laforge 说:“9，根据我们自己的快照进行测试，使用不同的标志来测试和构建 Groovy，从 JDK 7 开始，使用或不使用 invoke 动态支持，使用不同的分支。

为 Apache 重建手动流程

在进入 Apache Software Foundation 时，Groovy 不得不重新引入手动步骤，以满足 Apache 准则，该准则规定 Apache 提交者必须自己构建项目，并且他们需要用自己的密钥签署他们的交付物。“我们仍在使用 Gradle、JetBrains Team City、JFrog Artifactory 和 Bintray，但自动化程度不如以前，”Laforge 说。