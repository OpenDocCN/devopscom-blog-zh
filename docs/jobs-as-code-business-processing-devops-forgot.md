# 按代码作业:业务处理开发人员忘记了

> 原文：<https://devops.com/jobs-as-code-business-processing-devops-forgot/>

开发网络和移动应用很酷。但正如一首流传已久的歌谣所说:“不要忘记谁会带你回家，你会在谁的怀抱里……”正是后端服务支撑了许多酷应用，并使它们成为可能。所以，是的，服务器、关系数据库和企业应用程序，有时甚至大型机肯定是一个东西。在这些环境中，脚本、批处理、应用程序集成和操作可见性是非常重要的事情，通常由工作流和作业调度工具来管理。

我认为用于交付所有这些功能的“某些东西——应用程序、代码、其他”元素在逻辑上是应用程序的一部分，并且应该被如此对待。“流程 X”只需要在某些数据到达、清理并插入到某个数据库中之后才开始，这一事实与计算发票金额或确定库存需要补充一样，都是应用程序的一部分。

如果你还在阅读，那么我认为你需要代码式工作。

简而言之，作业即代码意味着作业(业务应用程序的自动化规则)需要在生产中管理和执行记录系统、后端应用程序组件和数据管道，其构建和管理方式与 Java、Python、C++或任何其他业务逻辑代码相同。换句话说，作为应用程序一部分的所有东西都应该包含在软件开发生命周期(SDLC)中。

当然，这种说法说起来很简单，但做起来并不容易，因为传统的工作流、作业和批处理解决方案已经存在于(并且大多数将继续存在于)运营领域。企业调度的实践者倾向于更喜欢强调易用性和对访问的严格控制的图形界面。传统上，诸如开发人员自助服务、自动化构建、测试和部署之类的功能在大多数企业作业调度新功能需求愿望列表中并不重要。大多数商业解决方案，如果他们做任何事情，添加一个或两个 API，并认为工作已经完成。开源作者构建的工具迎合了开发人员的需求，很少或根本不考虑依赖批处理工作负载的大量其他用户类型。

行业中的结果是，开发人员花费大量时间构建“雪花”操作管道，这可能很难测试，很难嵌入到自动化交付管道中，并且要么必须返工以准备生产，要么成为运营团队保持运行的瓶颈。是时候让 DevOps 社区和行业认识到有一种更好的方法，我们都本能地知道它是什么。

## 工作代码

为了理解作业即代码，让我们从开发人员和 DevOps 的角度来研究传统的开发人员到运营人员的交接。

我写了一些代码，现在我想测试。执行起来很简单；我想从关系后端提取一些数据，运行我的代码来操作数据，并将结果集推到其他位置，作为不同应用程序的数据源。我需要一个 SQL 查询，运行我的 Java 代码和 ftp 或 sftp 的结果。

我使用了一些交互式工具来提取我的测试数据，在 Eclipse 中调试我的代码，并用 Notepad++浏览输出。现在我想构建一个流，我或我的任何一个队友都可以随时运行它。

今天，我可能会放弃我的脚本技能，bash 或 perl 或其他什么，编写一个快速脚本来运行 SQL 查询，运行我的 java 代码，然后运行文件传输。很简单，对吧？

也许不是。

以交互方式连接到数据库是如此的简单，我甚至没有考虑过，但是在脚本中这样做是一个完全不同的练习。我必须正确引用和转义字符；我必须确保我的连接不损害登录数据库所需的凭证；我甚至必须弄清楚我得到的是什么返回代码，以及如何处理它们。当然，我需要添加一些通知，以便在出现问题时通知我。

好了，都做完了。现在运行我的 Java 代码是小菜一碟，对吗？嗯，在我的机器上用我的凭证运行时是这样，但也许我的队友有不同的环境。或者他是个. net 的家伙，没有像我一样配置 Java。或者更糟，可能根本没有安装。最好添加代码来检查所有这些问题和通知。当我收到失败通知时，我该看什么来找出哪里出错了？我最好把所有事情都放到一个日志*和*中，确保其他人也可以查看日志，所以我确保把它放在一个其他人可以访问的共享文件系统中。

让我们不要从文件传输开始！或者，当您必须添加额外的步骤时，或者当您必须在凌晨 3 点运行此操作作为另一个小组正在进行的测试的一部分时，或者当您必须确保您所依赖的数据库已经启动并正在运行时，等等。等。等。

最终，在比我想象的要长得多的时间之后，这个庞大的脚本完成了。我运行它通过一些测试案例，我完成了。

在剩下的交付阶段，进行更多的测试，可能还会有更多的扩展，让这个脚本真正成为史诗。

在进入生产的最后几个阶段，有人可能会提出这样的问题，即这个新应用程序会与由某个生产自动化工具管理的其他应用程序交互。好了，让返工——或者，真的，全新的计划外工作——开始吧。开发人员不熟悉该工具，工具管理员也不熟悉应用程序，因此您可以想象这些对话进行得有多顺利。然而，他们都是专业人员，最终设法完成工作，应用程序进入生产阶段。

如果这个冗长的故事还没有让你感到不安，你可能已经发现了一个巨大的失败，它正等着在我们众所周知的脸上爆炸。大多数(如果不是全部的话)测试已经完成。在最后时刻完成的新工作变得很少，如果有任何测试的话，被部署，并且-令人惊讶！—生产中的故障率很高。

雪上加霜的是，在所有部署应用程序的英雄事迹被遗忘很久之后，失败发生了，这是很自然的，也是可以预料的。可怜的随叫随到人员必须通过他们不熟悉的生产工具进行谈判，这些工具不属于他们的世界。然后他们遇到了巨大的史诗般的剧本。那个东西里面发生了什么，故障发生在哪里？日志在哪里？我们是否拥有所有需要的日志？把最好的留到最后，在问题被识别后，当一半的处理已经完成时，我们如何在中间重新开始这个过程？

## 那么涅槃会是什么样子呢？

如果您可以通过编写 SQL 语句、从逻辑名称列表中选择您想要的数据库并在出错时请求通知来创建数据库查询，并且您可以用几条简单的语句来表达这些需求，那会怎么样？如果您想在凌晨 3 点运行它，您只需添加该要求，然后说“运行”检查数据库的可用性，凭证是安全的，没有脚本，日志和输出是自动捕获的(不仅仅是这次运行，而是任意多次运行，您可以比较一次运行和另一次运行，等等。)并获得您请求的任何通知。这种逻辑是可靠的，因为它已经被像您这样的组织使用了很多年，而不是在压力下为了赶时间而写的。

您可以用一些您已经熟悉的简单符号(比如 JSON)来编写您的自动化规则(作业),将它与您的 Java 代码一起存储在 git 或您使用的任何 SCM 中。作业可以与您的应用程序的其余部分以及您的构建、配置管理和测试工具打包在一起，并可以将您的整个应用程序(包括您的作业)推入整个交付管道，因此在部署到生产环境之前不会出现意外或需要额外的工作。提供运营可见性、支持问题分析以及日志和输出管理的设施将是首屈一指的，因为它们一直在随着社区和 IT 专业人员的投入而发展。

想象一下，如果 github 和其他公共资源能够提供这种听起来很神奇的实现“按代码工作”的解决方案，会怎么样？您可以在几分钟内下载、安装并访问 Jobs-as-Code。您不必向 it 人员提交访问请求，没有采购申请，没有杂乱复杂的安装。

你不用想象。工作即编码的解决方案已经存在。如果你正在使用的工具不能给你这些能力，那就换吧！至少开始和你的同龄人交谈，让他们知道更好的方式已经到来。如果社区有足够的需求，实现无数作业管理工具的供应商和作者可能正好适合您。

— [乔·戈德堡](https://devops.com/author/joe-goldberg/)