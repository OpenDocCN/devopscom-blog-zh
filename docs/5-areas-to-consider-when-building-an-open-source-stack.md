# 构建开源堆栈时要考虑的 5 个方面

> 原文：<https://devops.com/5-areas-to-consider-when-building-an-open-source-stack/>

开源软件已经成为主流，这是由许多社区和工具的日益成熟推动的，这些社区和工具与寻求更快、更便宜地部署软件的组织合作。根据 Gartner Research 的调查，超过 95%的公司正在部署开源软件，虽然它带来了许多好处，但也带来了一系列全新的挑战，首先是选择正确的开源软件。存在多种风险，包括令人失望的软件性能、[无法与其他工具良好连接的工具](https://devops.com/but-wait-theres-more-the-trouble-with-devops-tools/)、令人惊讶的额外成本、缺乏控制和安全问题。

选择正确的开源堆栈并不容易。许多组织缺乏内部专业知识，不知道要寻找什么，或者没有时间充分研究开源软件。不能指望软件工程师一夜之间成为开源市场专家。

几年前，我和一个团队一起工作，认证开源解决方案用于生产。我们创建了一个需要考虑的 42 个必要资格的列表，这是(至少是部分)答案:从知道选择开源软件时要问什么问题开始。

## 开源考虑因素

以下是选择开源软件时要考虑的五个方面:

**时间**:虽然下载开源软件并让它快速运行的能力可能很诱人，但最好还是进行尽职调查，或者考虑与能够进行研究的外部专家合作。花点时间为您的使用案例构建合适的解决方案。值得注意的是，开放源码通常是目的驱动的，被选择来执行特定的任务；您可能需要将几个不同的项目组合在一起，以达成一个完整的解决方案。

**支持者**:虽然志愿者在成功的开源中扮演着重要的角色，但事实是大多数最知名的工具都有赞助。拥有一个有着良好记录的忠实支持者对于长寿和软件质量来说都是一个好兆头。我经常举的例子是[云原生计算基金会](https://www.cncf.io/)，它的背后是 Kubernetes、Linux 和 Prometheus。

**社区**:社区的承诺和响应至关重要。要问的基本问题包括:

*   社区对查询或错误的响应速度有多快？
*   其成员在记录和分享集体知识方面做得如何？
*   社区有多活跃，多庞大，多稳定？它可能存在足够长的时间来支持软件被选择的需求用例吗，或者社区和软件可能被地平线上的其他东西推到一边吗？

**不同的类型**:即使是一些非常博学的 CTO 也不能正确理解不同类型的开源软件，尤其是左版权许可和许可许可之间的区别。每一个对一个组织都有非常不同的含义。第一种要求贡献者与相关的软件社区共享他们的变更，而第二种则没有这个义务。企业对不得不共享他们专有的部分源代码和可能的知识产权感到紧张，尽管这仅适用于企业修改代码的情况。

不可预见的成本隐含在以下所有类别中:

*   **时间**:如果解决方案最终与用例不匹配，可能会浪费而不是节省。
*   **解决方案更新**:一个没有“支持者”的项目面临着死亡的风险，并且不会收到更多的更新，迫使企业花费精力选择新的解决方案。社区也是如此。
*   **法律后果**:如果企业修改和发布版权所有的源代码而不共享，他们将面临昂贵的法律诉讼。
*   **可用性和支持**:组织是否会得到第三方、社区和自己团队的支持？考虑所有选项的潜在成本。

软件质量和集成:关注编码实践是很重要的(它们符合组织自己的标准吗？)，可用性和对分布式资源的支持。最重要的是，仔细检查集成，因为构建开源堆栈的最大风险之一是最终会有一堆工具不能一起工作，或者不能在用例上保持一致。

检查整个堆栈的集成:平台、数据库、中间件、应用程序运行时和监控工具。寻找有很多支持的解决方案，并且众所周知这些解决方案可以与很多其他解决方案很好地互操作，比如 Kubernetes。专注于广泛采用的语言发行版，比如 OpenJDK，它可以在上面运行大量其他企业级开源软件。

这可能很难，但为开源堆栈选择正确的组件将有助于使未来的监管更容易，好处更明显。花时间做研究，从一开始就问正确的问题，可以在将来省去很多麻烦。