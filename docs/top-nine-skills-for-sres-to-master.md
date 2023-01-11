# sre 需要掌握的九大技能

> 原文：<https://devops.com/top-nine-skills-for-sres-to-master/>

很容易从高层次谈论[站点可靠性工程师做什么](https://rootly.io/blog/what-is-an-sre) :他们确保 It 系统达到可用性和性能要求。

但是 sre 到底需要哪些技能来[完成他们的工作](https://devops.com/?s=SRE)？这是一个更复杂的问题。

为了回答这个问题，我们来看看现代 sre(或有抱负的 sre)应该掌握的九大现场可靠性工程师技能。尽管根据管理的系统类型和面临的可靠性挑战的主要类型，SRE 技能可能会因团队而异，但几乎所有 sre 都需要一套核心的标准技能，使他们能够理解和管理他们在当今典型组织中必须支持的 [复杂分布式系统](https://rootly.io/blog/the-unique-reliability-engineering-requirements-of-microservices) 。

下面是 SRE 的几项顶级技能。

## sre 的网络专业知识

网络在连接现代分布式环境方面发挥着关键作用。因此，当出现问题时，它往往是罪魁祸首——例如，脸书在一个网络问题 导致其 [整个全球基础设施](https://rootly.com/blog/what-sres-can-learn-from-facebook-s-largest-outage) 瘫痪时就吸取了这一教训。

像这样的情况是 sre 应该掌握网络概念的原因。即使他们的组织也雇用网络工程师，站点可靠性工程师也需要对网络有深入的了解，才能知道网络何时是事件的根本原因，以及如何有效地解决网络引起的问题。

## Linux 和 Unix

如果你有 Windows 背景，但你想成为一名 SRE，这是无法回避的:除了 Windows，你还需要学习如何使用 Linux 和其他类似 Unix 的系统。

这是因为，即使在不太依赖 Linux 服务器的组织中，你也可能会发现 Linux 和 Unix 的概念已经深深地嵌入到你必须使用的其他系统中。例如，大多数公共云管理工具都遵循 Linux CLI 工具的惯例。像 Docker 和 Kubernetes 这样的系统也是如此，即使你在 Windows 环境下运行它们。

## 云计算

与 Linux 和网络一样，云计算是现代 sre 不可或缺的另一类技能。

原因几乎不言而喻:大约 90%的企业 [使用云](https://techjury.net/blog/how-many-companies-use-cloud-computing/) ，如果你不了解云架构、云网络、云数据存储、云可观测性等等，你就无法很好地管理云环境的可靠性。

## CI/CD 管道

sre 通常不会帮助开发软件，但他们仍然需要对软件如何编写和部署有深刻的理解——在今天的大多数组织中，这是一个通过 CI/CD 管道发生的过程。

如果你不知道如何解决应用程序源代码或部署过程中出现的可靠性问题，就很难设计可靠性。了解 CI/CD 流程是如何工作的，以及哪些工具驱动着它们，这对于当今几乎每个 SRE 来说都是关键。

## 质量保证和软件测试自动化

sre 通常也不能帮助测试软件的预部署。这项任务落在了开发人员或质量保证工程师的身上。

尽管如此，理解如何测试软件——以及如何使用测试自动化来加速测试和扩大测试覆盖面——是 SRE 的一项重要技能。毕竟，您的团队测试软件越彻底和有效，您在部署前发现可靠性问题的机会就越大，因为它们更容易修复，对业务造成的风险也更低。

## 安全工程和响应

安全是 sre 不“拥有”的另一个领域，但他们仍然需要重要的技能。

的确， [好的可靠性工程让安全性成为优先考虑的事情](https://rootly.io/blog/when-you-do-devsecops-don-t-forget-the-sres) ，反之亦然。不了解安全基础知识的 sre 面临着实施可靠性解决方案的风险，这些解决方案从可靠性角度来看是有效的，但不一定是安全的。

## DevOps

【SREs 虽然不是 DevOps 工程师，但是 [SRE 和 DevOps 是密切相关的领域](https://rootly.io/blog/sre-vs-devops-what-are-the-differences) 。如今，大多数组织的 sre 都应该理解 DevOps 概念，并且在许多情况下，与 DevOps 团队一起工作。

因此，计划掌握 [DevOps 技能](https://devops.com/survey-shows-increased-devops-skills-among-salesforce-developers/)作为你的站点可靠性工程师技能获取策略的一部分。

## 事故管理

也许 SREs 需要学习的最重要的技能是 [事件管理](https://rootly.io/blog/incident-management-vs-incident-response-what-s-the-difference) 。尽管许多角色可能会参与事件响应，但 sre 通常会牵头 组织事件响应团队 ，与利益相关方沟通，并设计出尽快解决每个事件的最佳策略。

这意味着 SREs 应该知道 [事件响应角色是如何构成的](https://rootly.com/blog/an-introduction-to-incident-response-roles) 并了解事件响应概念。他们还应该熟悉事件响应平台，这些平台能够自动执行复杂的流程，以确保快速、有效地解决事件 。

## 管理尸检

除了监督事故响应，SREs 还可能负责管理事后验尸。知道如何进行验尸[](https://rootly.com/blog/beginners-guide-to-incident-postmortems)—以及何时验尸是必要的，何时使用“无可指责的”验尸方法是 SRE 的一项基本技能。

SRE 技能的清单还可以继续列下去。以上只是 sre 在大多数现代环境中需要的最基本的技能类型。但是，如果你刚刚开始成为一名 SRE 的旅程，上面描述的九个技能领域是一个很好的开始获取知识的地方，你需要在 SRE 的职业生涯中脱颖而出。