# DevOps 安全性:弥合团队间差距的五个步骤

> 原文：<https://devops.com/devops-security-five-steps-to-bridging-the-gap-between-teams/>

企业安全和 DevOps 团队传统上是分开运作的，很少或根本没有参与，这通常使得快速识别和响应应用程序和软件中的潜在漏洞变得困难。在我的上一篇专栏文章中，我强调了在 DevOps 过程中引入安全性的价值，以便在代码投入生产之前减少 bug 和漏洞。通过将安全性尽可能地靠近代码和数据，再加上紧密的反馈循环，组织将能够更好地支持日益增长的构建软件的复杂性。

DevOps 强调灵活的基础设施，它可以随着新代码的部署而快速变化，如果不考虑安全性，它就会成为错误和漏洞的滋生地。那么，如何在您的组织内缩小 DevOpsSec 差距呢？秘诀是从简单开始，小步前进，轻松取胜。以下是五个建议:

1.  建立一个在生产中关心代码的开发团队。在开发过程中，当开发人员编写代码、添加新功能、在生产中的表现以及创建问题修复程序时，他们必须关心代码。团队应该对代码拥有完全的所有权，我喜欢称之为“代码之爱”，并且能够像保护他们的孩子一样保护它。
2.  实施同行代码评审。鼓励“热爱代码”的最初方式是通过同行代码评审，这允许开发人员看到其他人写的东西，鼓励他们一起工作，并促进团队中关于如何改进流程的讨论。此外，通过这些审查过程，团队将能够在早期识别不良实践，并改进它们。
3.  **引入测试驱动的开发环境。**测试驱动的开发环境意味着可重复的测试，然后可以利用持续集成(CI)服务器来鼓励团队在每次提交代码时运行安全测试。许多组织不一致地这样做，做得不好或完全绕过这一步。通过让开发人员做更多的测试和审查，您可以在组织内更紧密地集成开发运维与安全性。
4.  扩展自动化。一旦建立了以上内容，就该扩展自动化了。鼓励你的团队做代码风格和质量测试，这是自动化“代码之爱”的附加工具。易于阅读的好的干净的代码总是有较少的错误。此外，将静态安全分析引入 CI 服务器，以帮助识别容易实现的结果和早期实施问题。另一种选择是通过让您的团队编写恶意用户故事来引入滥用案例。这是一个很好的方法，可以确保同样的问题不会再次出现，同时也可以作为新团队成员的培训材料。
5.  建立消防队。为了确保所有人都关心这一流程，将开发运维团队和安全团队的成员召集起来，让他们每周随叫随到。这种协作将允许每个团队成员看到其他团队面临的问题以及他们的需求如何重叠，从而加深对彼此角色和流程的理解。在“代码爱”之后，这是你可以引入到你的组织中的第二个最重要的反馈循环。

为了在组织内成功启动 DevOpsSec，开发人员需要有明确的工作参数，以便将安全团队包括在软件开发生命周期(SDLC)中。通过打破组织孤岛并鼓励开发运维团队和安全团队的交叉融合，他们将能够更好地了解各自处理的问题，并自然地引入联合解决方案。