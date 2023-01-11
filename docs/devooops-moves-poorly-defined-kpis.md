# 开发人员的行动:定义不明确的关键绩效指标

> 原文：<https://devops.com/devooops-moves-poorly-defined-kpis/>

DevOps 的最终目标是在软件交付过程中创造效率。但是，事情并不总是这样。有时开发计划会导致错误——我们亲切地称之为“开发计划”CloudBees 最近对一些同事进行了民意调查，并提出了五个实施减贫的例子。以下是产品营销人员由尼·慕克吉提交的关于定义不清的关键绩效指标(KPI)的讨论。

**场景:**

我们如何定义 KPI 可以改变游戏规则。例如，一个质量工程团队将每个 sprint 执行的测试数量定义为一个成功的度量。人类受到激励的驱使，团队的自然趋势是添加越来越多的测试，甚至没有考虑过时测试的存档。想想看:我们可以用更少的测试产生更大的影响，更重要的是，更少的测试降低了测试周期时间。因此，我们应该关注测试的覆盖面和有效性，而不是单纯的数量。类似地，一个发布工程团队将每个 sprint 的发布数量定义为一个成功的度量。发布的数量当然反映了速度。然而，发布将比特从 A 点移动到 B 点，而没有评估对业务的增值。结合业务 KPI(如获得的新客户数量、收入增长百分比等)至关重要。)到速度，这样我们就知道我们投资的是有价值的速度，而不是自杀性的速度。

管理顾问彼得·德鲁克将他的整个哲学归结为以下几个字:“如果你不能衡量它，你就不能改进它。”

成功的 DevOps 领导者会牢记这句话。为了了解他们要去哪里、如何到达那里以及最终他们已经走了多远，这些领导者知道建立符合其 DevOps 转型总体目标的 KPI 是多么重要。KPI 提供了适当的、持续的洞察力，并且它们绘制了一条路线来帮助你到达目的地。

最大的问题是:你在衡量正确的事情吗？如果不是，你可能是在转动他们的轮子。

为了避免这种“脱欧”的情况，你需要从建立 KPI 开始，这些 KPI 不仅要与你的目标一致，而且要建立起来，这样它们才能形成一个连续的反馈循环。随着项目的进展，随着您的成熟和了解的更多，您可能需要维护、监控并可能调整和更新这些 KPI。

什么是合适的测试覆盖目标？团队都想提高质量。但是增加多少呢？七成？八成？百分之百？这是一个 KPI 的例子，需要在您的应用环境中考虑，并根据您的真实目标进行衡量。

您可以拥有 70%的测试或代码覆盖率，但是如果这只是作为测试尽可能多的代码的一种方法，您可能会错过目标。如果您覆盖了 70%的错误代码，而缺少的 30%是关键代码，那么您已经付出了巨大的努力，但却冒着质量水平回报很少或没有回报的风险。

就您的目标而言，增加和监控测试覆盖率可能是质量的指标，但它可能无法衡量您的实际工作质量。在这种情况下，您需要一个衡量结果而不是活动的 KPI。看看什么是生产中的严重性 1 和严重性 2 缺陷率。您可以看到代码覆盖率达到了 90 %,但是如果您没有看到严重性 2 缺陷的减少，您就不会真正看到我们的代码覆盖率度量的改进。

**外卖:**

*   你实现 DevOps 并不是为了说你在做；您需要为您的计划制定目标，并与它们保持一致。
*   一旦定义了目标，您需要将 KPI 和成功指标与这些目标相匹配。正确定义这些成功指标和 KPI 将决定在构建管道时优先考虑什么。

— [布莱恩·道森](https://devops.com/author/bdawson/)