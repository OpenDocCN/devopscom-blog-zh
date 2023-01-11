# 管理开源软件组件

> 原文：<https://devops.com/managing-open-source-components-software/>

构建任何软件都需要大量的努力，包括资源、时间、金钱等等。当它上线或发布时，真的是一件非常愉快的事情。与此同时，即使在多轮测试之后，bug 仍然有可能使发布陷入困境。团队可以修复与软件特性或功能相关的错误，但是最糟糕的是

*   安全漏洞。
*   开源组件的许可风险。
*   过时的开源组件。

世界正以极快的速度向开源迈进，开源在软件中的使用越来越多，成为应用程序中的组件。开源组件对我们来说是免费的，但是在使用它们的时候可能会有更多的风险。付费和商业化的产品一定会修复问题，并为任何漏洞或安全问题提供足够的支持和许可，但开源软件可能有更高的风险，因此更新新版本和可用的错误修复非常重要。

如果开源组件没有得到适当的监控和更新，可能会导致软件变得易受攻击。

以上检查需要在开发阶段完成，并排除任何与安全或法律相关的差异。这种检查可以作为构建过程的一部分，以确保它不会通过第一道关卡，甚至在进入测试阶段之前就被发现。最终这可以节省开发和测试工作以及他们的时间。

有一些工具可以在不同的阶段处理一些/所有的开源组件的验证。

该工具可以验证开源组件的许可，并检查其与各种定义的兼容性。您甚至可以根据需要添加自己的许可证定义。

**Sonatype[Nexus](http://www.sonatype.com/nexus/product-overview)**和**[white source](http://www.whitesourcesoftware.com/)**

这些工具将验证许可证并保持组件信息最新。他们将检查任何更新，任何漏洞问题的错误修复，并通知用户。这些工具可以使用最新的可用信息进行组件安全漏洞和许可证分析。

安全问题是任何软件开发人员最不希望看到的。即使是很小的法律或安全问题也会将您的系统/软件置于危险的境地。最好先保护软件，然后再修复它。

**参考- >**

[http://www . scmtechblog . net/2015/06/managing-open-source-component . html](http://www.scmtechblog.net/2015/06/managing-open-source-component.html)

[http://www . scmtechblog . net/2015/03/maven-repository-tools-comparison . html](http://www.scmtechblog.net/2015/03/maven-repository-tools-comparison.html)