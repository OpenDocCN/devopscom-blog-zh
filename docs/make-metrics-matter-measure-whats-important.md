# 让度量变得重要:衡量什么是重要的

> 原文：<https://devops.com/make-metrics-matter-measure-whats-important/>

在数据驱动的社会中，组织严重依赖一系列指标来评估他们在特定任务、计划或资源分配方面的表现。度量对于 DevOps 团队尤其重要，他们的职能与协作和持续改进等概念紧密相关。

但是，尽管度量有助于提高效率，但是它们也会将开发团队引入歧途。仅仅因为你在测量特定的事物并不意味着你在测量正确的事物。如果你增加了更多的指标，并不一定意味着你创造了更多的价值；你可能只是越转越快，却一事无成。

关键是选择正确的指标，为您的组织带来正确的结果。但是，如何选择正确的指标呢？你如何衡量你创造的真正价值？成功应对这一挑战的组织不仅将建立成功的 DevOps 文化，还将提高他们在日益苛刻的商业环境中的整体竞争力。

## 可衡量——可操作

首先，选择客观可测量的指标。从您的度量调色板中消除个人主观性。而不是问“我的 UI 有多好看？”关注可测量的数据，如“用户界面对残疾人来说是可访问的吗？”或者“它带来了更多的点击吗？”

重要的是选择可操作的指标，而不仅仅是“虚荣指标”早在 20 世纪 70 年代，麦当劳曾经用实际数字更新其餐厅外面的标志:“30 亿份服务；“40 亿服了。”现在，标语上写着:“亿万人服务。”这是最终的虚荣心衡量标准——不容易审计，也不可操作。多少个亿？麦当劳应该以万亿为目标吗？DevOps 虚荣指标的一个很好的例子是服务器正常运行时间。事实上，这实际上是一个相反的指标:云实例扮演着如此重要的角色，您可以证明低服务器正常运行时间实际上是更可取的。

[指标](https://devops.com/?s=metrics)应关注团队间和团队内的绩效和成果。DevOps 是一个跨职能团队——开发、测试、运营和信息安全，等等——一起工作以交付商业价值。因此，不要关注像“代码行数”这样的单个指标，而要关注像“获得客户的成本”、“新客户注册”或“总收入”这样的结果。如何移动指针可能并不总是显而易见的，但这正是实验发挥作用的地方。

## 避开噪音

关注尽可能少的指标，保持较高的信噪比。当一切都是优先的时候，没有什么是优先的。如果你向董事会展示你的指标，屏幕上有 50 个不同的图表，你更关注的是展示的样子，而不是展示真实的战术信息。选择与您当前目标一致的指标，并毫不留情地确保这些指标准确、及时且专注于战略目标。

期望目标——以及你跟踪的指标——随着时间的推移而发展。您可能想要缩短特性交付时间，但是要做到这一点，您可能会从测量诸如构建时间、回归测试时间、部署时间等事情开始。您将会影响功能交付指标，但会以迂回的方式进行。关键策略是选择一个你想要实现的结果。一旦你解决了这个问题，你就可以保留这个标准，但是你会想把它降低。你可以给它设置一个警报，这样如果它越过了你不希望它越过的门槛，你就可以采取行动了。

工程组织应该关注四到五个他们当时正在积极尝试改进的度量，这样他们就可以实现那些结果。当他们实现这些成果时，他们可以让它们退役或者将这些指标放在后台。然后，他们可以选择下一个目标，确定要实现的下一个结果，并分配一些新的衡量标准。

## 根据您的优先事项调整指标

衡量标准可以视情况而定。如果你在网络运营中心工作，你会有一些想一直拥有的东西。您会想知道拒绝服务攻击发生的时间，或者错误率开始上升的时间。但是对于一个软件交付管道来说，你不能只是抛出一堆度量标准，然后希望正确的标准会出现在最前面。您希望关注与您今天、下周、下个月、本季度或今年的优先事项一致的指标。

那么，对于 DevOps 组织来说，追求哪些指标是最重要的呢？Google DevOps 研究和评估( [DORA](https://cloud.google.com/devops) )团队确定的一系列指标已经成为确定一家公司在 DevOps 方面有多成功的行业标准。这些测量包括部署频率(DF)；变革的平均准备时间(MLT)；平均恢复时间(MTTR)和变更失败率(CFR)。这些度量显示了开发团队如何更好、更快地向客户交付更好的软件。

我想补充第五个指标:平均发现时间。从一个问题被注入到一个项目中，到我们发现它需要多长时间？是我们的组织发现的还是客户发现的？在此基础上，我们可以制定策略，用最便宜的方法自己发现特定的错误。我们是否可以编写一个运行 100 毫秒的五行单元测试来捕捉这个问题？还是更复杂？UI 是否没有对齐，以至于无法自动捕捉？

软件交付过程的不同部分将涉及不同的度量集合。虽然 Dev/CI 实践关注开发提前期、周期时间和工作进展/技术债务，但是 QA 团队更关注空闲时间、发现和逃脱的缺陷，以及前面提到的平均发现时间。虽然部署小组的目标是提高部署频率和变更成功率，但是运营却因为研究停机的成本和频率而变得活跃起来。

度量是开发运维组织的有用工具。他们可以推动团队变得更有效率，更负责任。但是，要真正优化他们从人和特定计划中获得的价值，仔细选择指标是很重要的。认识到度量标准不是一个放之四海而皆准的机制，更多的度量标准并不总是等同于更好的性能。选择正确的指标——并在一致的基础上重新评估它们——是长期改进的最佳途径。