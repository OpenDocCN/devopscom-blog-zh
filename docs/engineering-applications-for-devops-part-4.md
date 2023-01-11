# DevOps 的工程应用(四)

> 原文：<https://devops.com/engineering-applications-for-devops-part-4/>

这个博客系列解释了如何为 DevOps 设计应用程序。

本博客系列涵盖的主题:
·决定一个应用程序是否适合 DevOps 的因素。
·devo PS 工程设计实践。
devo PS 应用于企业应用和软件服务。
·适用于 COTS 系统的 DevOps。
devo PS 应用于制造(嵌入式)系统软件。
·应用成熟度的五个级别。

本博客涵盖了应用于商用现货(COTS)系统的 DevOps。你可以在这里阅读第一部分、[第二部分](https://devops.com/engineering-applications-for-devops-part-2/)和[第三部分。](https://devops.com/engineering-applications-for-devops-part-3/)

## **应用于 COTS 系统的 DevOps】**

我经常听说 DevOps 不适用于使用商业现成(COTS)软件的系统。坦率地说，DevOps 不能用于 COTS 系统的想法是一种逃避。仅仅因为其他人设计和开发了应用程序的源代码，并不是避免开发 DevOps 解决方案的充分理由。

考虑来自源供应商的活动的价值流链，通过集成和部署到您的环境中。在处理 COTS 应用程序时，DevOps 实践可能引入的自动化水平、自动化投资回报以及对开发生命周期的影响都有限制和约束。

COTS 应用程序通常具有预定义的和受支持的接口，用于管理配置或访问数据。这些端点可能无法访问，或者与您现有的工具链或自动化变更管理实践不兼容。

### COTS 应用的类型

COTS 应用程序通常有三种风格；即封闭式、开放式和平台式，每一种都应该有不同的评价。

**封闭式 COTS 应用**不允许对其功能和/或界面进行定制。它们通常有预定义的管理控制台和发布的命令或 API 列表，允许外部应用程序与 COTS 应用程序进行交互。封闭的 COTS 应用程序的一个很好的例子是 Microsoft Exchange。

**采用封闭式 COTS 应用的开发运维的关键考虑因素如下:**

配置可以编写脚本并与现有自动化和流程编排工具链集成吗？可以在外部版本控制系统中管理和维护配置脚本吗？
·如何应用和管理更新、补丁和服务包？这些实践可以自动化吗？
什么开发工具(API，软件开发包[SDK]等。)是否可用于扩展应用程序和/或数据和/或与之交互？
这些工具与企业中现有的工具和专业知识兼容吗？
这些开发工具可以集成到现有的工具链中吗？
？对基础产品进行更改的频率如何？

如果这些应用程序可以由外部系统管理，并且为自动化部署和配置而开发的代码和/或集成可以通过版本控制管道进行管理，那么封闭的 COTS 应用程序是开发运维及持续交付(CD)的良好候选。通过应用 CD 原则，COTS 二进制文件被版本化并存储在工件库中；安装和配置脚本通过版本控制进行管理，IaaS 工作流和应用以及集成端点通过部署管道进行自动测试。

只有当 COTS 应用程序的消费者与 COTS 平台的操作者合作，以确保解决方案与项目组合管理相关的企业目标、目的和标准一致时，这才有可能。

**开放式 COTS 应用**允许对功能、数据和/或接口进行重大修改。这些平台通常具有丰富的 SDK、API 和嵌入式开发工具，使用户和开发人员能够修改应用程序的所有层；即表示、业务逻辑和数据。开放的 COTS 应用程序通常有一个由核心服务、数据和/或 GUI 定制、嵌入式应用程序等组成的大而复杂的足迹。开放式 COTS 解决方案的经典例子包括 ERP/ CRM 平台(如 SAP 或 Oracle)或门户平台(如 SharePoint、ServiceNow 或 WebSphere)。

**考虑 DevOps 是否适用于开放 COTS 应用时要问的关键问题:**
定制(通过内部设计编辑器、逻辑构建器或数据模式扩展创建)如何进行版本控制？这些配置是存储在数据库中还是代码中？
如何通过内部工具创建定制，并在更高级别的环境(如试运行或生产)中打包、安装和配置？
用内部工具创建的定制的开发生命周期是什么样的？需要什么质量关？建筑标准怎么样？
定制的嵌入式应用/小程序是如何打包、安装和配置的？
这些定制应用程序/小应用程序可以与底层 COTS 应用程序分开运行和测试吗？使用外部工具创建定制的开发生命周期是什么样的？需要什么质量关？建筑标准怎么样？
·COTS 应用程序是否为测试外部依赖关系提供了测试框架、模拟和/或存根？平台支持哪些自动化测试套件(单元、功能、回归、容量测试等)。)?
？定制的升级途径是什么(历史上)？可以想象，开放的 COTS 应用程序增加了复杂性。

当考虑采用开放式 COTS 解决方案的 DevOps 和 CD 时，建议您在价值流的开发或持续集成(CI)阶段构建多个管道来支持应用程序的每一层。后续阶段，如阶段化和生产，将使用从开发和 CI 阶段的已知良好工件构建的聚合管道。

在实现解决方案之前，在构建工具链之前，研究目标 COTS 应用程序的开发生命周期和实践是很重要的。了解最终状态平台是如何创建的，以及如何引入变化，将会极大地影响您的工具链和管道设计。

**平台 COTS 应用**提供一组服务和工具，以及专有运行时，使用户能够在平台上构建和运行定制应用。这些是最难集成到现有 DevOps 实践和 CD 工具链中的应用类型，因为版本控制、测试和构建等常见实践是通过平台完成的，而不是使用外部工具。

平台 COTS 是打包的应用程序，使客户能够在基础平台上构建应用程序。作为封闭系统和开放系统的混合体，前面所有的考虑都是正确的。在大多数情况下，基础平台充当封闭系统，而顶层定制开发的应用程序充当开放系统。

对于这种类型的应用程序，了解哪些挂钩和服务可用于支持 DevOps 实践和 CD 至关重要。其中许多平台不适合您现有的工具链，并且可能无法使用您在当前工具链中已经习惯的工作流、仪表盘和报告。

## **这意味着什么**

这个博客是解释如何设计最适合 DevOps 的应用程序的系列之一。这个博客系列解释了如何为 DevOps 设计应用程序，包括:

用于决定应用程序是否适合开发运维的因素。DevOps 的工程设计实践。
·devo PS 应用于企业应用和软件服务。
devo PS 应用于 COTS 系统。
·devo PS 应用于制造(嵌入式)系统软件。
应用成熟度的五个层次。

这篇博客介绍了应用于 COTS 系统的 DevOps。你可以在这里阅读第一部分、[第二部分](https://devops.com/engineering-applications-for-devops-part-2/)和第三部分。

有关如何开发开发应用的更多信息，请参考我的书[工程开发应用](http://mybook.to/engineeringdevops)。