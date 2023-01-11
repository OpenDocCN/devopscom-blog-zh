# 基础设施测试多米诺骨牌

> 原文：<https://devops.com/infrastructurre-testing-dominos/>

理解给定技术组件的工件对于企业级 DevOps 服务产品至关重要。第二重要的是理解给定组件之间的依赖关系。测试有助于阐明这些依赖性。

例如，假设我有一台运行以前版本的 Windows 操作系统(OS)的服务器，现在我想将其升级到最新版本。这个版本的操作系统以前的部署包将是一个工件。它还应该包括我运行的所有测试自动化，以验证在我安装之后操作系统的版本正在工作。工件还可能包括我在这类环境中这种类型的服务器上安装该版本的操作系统时部署的配置文件。将这些自动化功能捆绑在一起，可以让我在许多服务器上成功安装我的操作系统(假设没有硬件错误)。

当我为最新的 Windows 操作系统创建一个新的工件时，我会记住我在上一个版本中拥有的所有东西。我可能会包含一个更新的配置文件和一组测试(尽管是新的)，以确保它在我完成时能够工作。将所有这些部分捆绑在一起，我就有了一个新的 Windows OS 工件或包，我可以在这类环境中的这类服务器上反复使用。我的想法是创建一个单一类型的工件或包来覆盖这种技术——在这个例子中是最新版本的 Windows OS 操作系统。我所有的工件都应该是版本控制的。因此，当我完成时，我有一个用于以前 Windows 操作系统的工件和一个用于最新版本的工件。每个工件版本都嵌入或包含了测试(指向或谨慎的自动化)来验证安装的有效性，也许还会证明操作系统工作正常。

在我的 DevOps 工具中，我可能有某种工件管理系统。它可能不像一个完整的配置管理数据库(CMDB)系统那样正式，但是我使用的任何工具都有某种数据库来按版本管理我的工件或包。我将这些工件保留多长时间将在我的保留政策中定义，但是很可能我将保留今天在我的公司中使用的每个版本。这是第一步，它为我下一步编目工件之间存在的依赖关系奠定了基础。

## **进入蜘蛛网** 

在我描述的场景中，当我部署以前的操作系统或最新的操作系统时，我会运行一系列特定于该版本的测试，以确保操作系统正常工作。作为一名基础设施工程师，我倾向于认为我的工作已经完成了。但事实并非如此。为了真正验证我的操作系统是否在工作，我真的需要知道我刚刚部署到的服务器上正在运行什么。如果我的服务器是空的或新的，那么我真的完了。但是，如果我的服务器上运行着中间件，那么直到我在新的操作系统上重新部署正确版本的中间件并验证它仍然正常工作，这项工作才算完成。

为了实现这一点，我需要一个相互依赖的技术目录。操作系统的例子很简单，因为它位于服务器的底层。但是在操作系统之上可能存在一个中间件平台(可能是消息传递或数据库)。在中间件之上可能驻留一个或几个应用程序，这取决于所讨论的服务器的能力。升级操作系统组件意味着我要重新部署中间件层，然后再部署应用层。

进入全栈工程。它采用以应用程序为中心的观点，但这意味着单一的以应用程序为中心的观点。它从上到下查看一个应用程序，并将整个堆栈视为一个受版本控制的工件。但是，如果您的遗留环境在同一个物理机器上运行多个应用程序，也许是在同一个虚拟实例上，那么您就有了依赖关系的蜘蛛网。据我所知，目前还没有全栈解决方案能够解决如何在同一个栈顶集成多个应用程序，在中间集成不同的中间件，以及在一个物理机箱上运行“n”个虚拟实例。相反，技术的每一部分都倾向于单独处理。因此，需要某种目录来跟踪它们之间的相互依赖性。

## **开始多米诺骨牌测试** 

因此，一旦我对每种类型的技术组件进行了版本控制(或关联)的谨慎测试，如果任何“在我之下”的东西发生了变化，我将不得不重新执行那些测试。例如，如果我的 WebSphere 版本升级了，除了发生的核心 WebSphere 测试之外，我真的应该执行与每个应用程序相关的测试，以确保“那个应用程序”在升级后仍然工作。您可以将这个前提应用到数据库层(例如，升级 Oracle 的当前版本)。要真正知道数据库升级是否成功，您应该运行每个依赖应用程序的测试，并确保“该应用程序”在升级后仍然工作。结果可能会令人惊讶。

要执行这种类型的 domino 测试，即使您已经定义了依赖关系网，并且管理了工件或包，您也可以采取两种方法中的一种:重新部署所有内容，尽管这种方法可能不会真正开始测试，如果它检测到版本与上次部署相比没有变化(智能覆盖)，或者在您的发布编排软件中设置谨慎的测试作业来执行整个依赖关系网并跟踪结果。无论是哪种情况，您都需要人工来判断是保留新版本好还是回滚到旧版本好。只有人类才能区分给定应用程序或一系列应用程序的看似微小或灾难性(基于人类视角)的影响。

## **冲击底线** 

真正的质量只能通过测试来评估。打破筒仓式思维的一部分是对您的组织所支持的技术采取整体观点。仅仅因为操作系统支持工程师的测试通过并不意味着升级成功。要想升级成功，依赖该技术支撑的其他人必须通过测试，证明它有效。当底层基础设施发生变化时，整个团队都需要验证。测试的多米诺骨牌必须从一端传到另一端。只有这样才能衡量真正的质量或真正的成功。

当然，大多数工程师不愿意让“应用软件”人员影响他们是否正确地完成了自己的工作。毕竟大部分软件质量问题都出在代码上，而不是因为基础设施错误。但是，如果您的业务所依赖的应用程序无法工作，不管是什么原因，在基础架构升级之后，这是整个业务的问题，而不仅仅是软件人员的问题。为了打破孤岛，我们需要着眼于影响跨边界变化的事件，并推动整体结果，而不仅仅是部门的结果。当这种情况发生时，质量成本就会显著降低。

要继续对话，请随时[联系我](/cdn-cgi/l/email-protection#afe4ddc6dcdbc6cec181e1cac3dcc0c1efc7c0dbc2cec6c381ccc0c2)。