# 当 IT 灾难来袭时，第 3 部分:进行无可指责的事后分析

> 原文：<https://devops.com/when-it-disaster-strikes-part-3-conducting-a-blameless-post-mortem/>

在这个由三部分组成的系列的第一部分和第二部分中，我们了解了[组织如何有效地解决事件](https://devops.com/disaster-strikes-part-1-resolving-incidents/)以及每个人在解决过程中的[角色](https://devops.com/disaster-strikes-part-2-gonna-call/)。在这最后一篇文章中，我们将看看组织在事件发生后必须做些什么，以便更好地了解问题所在，并从他们的响应中学习。

在发生的时候，停机是每个 IT 从业者最可怕的噩梦。然而，在尘埃落定之后，每个事件都提供了一个团队学习的机会，对您的流程产生影响并改进您的产品。这意味着即使你找到了解决方案，你的工作还没有完成。

# 输入事故事后分析

一旦你成功地解决了一个主要问题，混乱的局面也逐渐平息，是时候和你的团队一起进行一次事故分析，调查问题并找出问题所在。没有事后分析，你无法认识到你做得对的地方，你可以改进的地方，最重要的是，如何避免在未来犯同样的错误。

以下是我为一个成功的事后分析过程所尝试的三个真实步骤:

### 指定一个验尸负责人

为了开始事后分析，事故指挥官应在事故结束时指派一名负责人。该负责人负责安排事后分析会议，该会议应在事故发生后五个工作日内举行。所有者还负责填写事后分析文档、调查事故、召集其他人来协助和促进事后分析会议。在需要公开博客帖子的情况下，所有者还将负责创建内容，并对其进行必要的内部审核。

### 填写事后分析文档并进行分析

一旦指定了所有者，团队就应该开始用可用信息更新事后分析文档，包括状态变化的时间表和事件响应者采取的关键措施。事件响应中的每个参与者都应包含在此页面中，因此请务必回顾所有沟通并添加相关方。用完整的行动时间表更新页面后，您需要为每个事件构建详细信息。对于时间线中的每一项，确定数据来自的指标或第三方页面。这可以是任何东西，从数据狗图的链接或 Splunk 搜索到相关推文，只要它显示了你试图说明的数据点。

有了时间表，您就可以开始分析事件了。获取关于发生了什么、什么导致了问题、有多少客户受到影响、他们经历了什么影响等所有可用数据。，以确定事故的根本原因。此信息应详细，因为它将决定您的团队将使用的后续行动单，以防止事件再次发生并改进事件响应流程。它也会在事后总结会议中被检查，所以你在分析中包含的背景越多越好。

在需要外部沟通的严重事故中，这也是事后分析所有者和团队应该开展客户沟通的时候。**专业提示:**在沟通中，尽可能避免使用“中断”一词。许多人看到单词 outage 时会认为您的整个系统都瘫痪了，但实际情况可能并非如此。这里要精确，因为这对内部学习和更大的 it 社区内的共享都很重要。

下面是一个通用模板，说明在事后分析页面上应该包含哪些内容:

*   概观
*   发生了什么
*   根本原因(或促成因素)
*   解决
*   影响
*   参与的响应者
*   时间表
*   我们表现如何？
*   行动项目
*   沟通(内部和外部)
*   召开事后汇报会议

流程的最后一步，即事故分析会议，应包括事故指挥官、服务负责人、关键工程师/响应者和客户联络员(针对严重事故)。把你的事后分析文件作为一个议程来帮助事情顺利进行。讨论应围绕发生的事情、团队可以做得更好的地方以及需要采取的任何后续行动。关于事实、分析或建议行动的任何分歧都应在此期间得到澄清，每个人离开会议时都应更好地了解影响您服务可靠性的问题，并对相关服务有更多了解。

对事故进行事后分析的首要原则是保持事故无可指责。汇报过程的目标不是相互指责，而是了解发生了什么，以及如何作为一个团队来改进。

不要犯在重大事件后忽视事后分析过程的错误。一个设计良好、无可指责的事后分析使您的团队能够不断学习，并提供一种迭代地改进您的基础设施和事件响应过程的方法。这不仅有助于你的团队，也有助于创造令人惊叹的软件和服务。

埃里克·西格勒