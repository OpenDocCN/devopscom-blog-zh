# 反对数据中心的力量越来越大

> 原文：<https://devops.com/the-forces-massing-against-the-data-center/>

在过去的几十年里，我们走过了漫长的道路。即使是在过去的五年里，很多事情都发生了变化。这是真的，唯一不变的是变化。

我们希望能够控制我们的环境，提供最稳定的平台，让用户满意，并在出现问题时简化故障排除。但是，即使是这样一个简单的愿望也在我们面临的变革洪流中被剥离了。可以肯定的是，大多数企业中的一些 IT 领域是非常稳定的环境，只有在仔细考虑后才会发生变化，但其余的大部分领域——无论是企业内部还是外部——又变成了蛮荒之地。

这个周期有很多好处。尝试新事物解决老问题，推动创新，这是毋庸置疑的。我们所做的改变解决了“从来没有足够的测试”或“我们没有安全人员”这样的问题，这意味着我们的应用程序因为我们目前正在经历的变化而变得更好。即使在最保守的企业中，云也是新开发的标准选项，一些企业在时间允许的情况下将旧应用程序迁移到云。

这最后一点将迫使未来做出一些艰难的选择。正如你们许多人所知，我花了几年时间专门写关于存储的文章，所以当我看到存储领域发生的事情时，我就会产生兴趣。我的一位前同事最近从一个我以前没有考虑过的角度写了一篇关于 Kubernetes 存储选项的文章，这促使我更深入地了解今天发生了什么。

如果您没有注意到，存储(具体来说是数据重力)已经将大量应用程序绑定到企业[数据中心](https://devops.com/?s=data+center)。应用程序需要访问数据；如果数据在数据中心，应用程序必须在那里，并以某种方式安全、方便地访问数据。云和容器提供了一些解决这个问题的选择/方法，但是它们远远落后于敏捷基础设施的其他部分。

这种情况正在改变。更高速的分布式数据集已经出现并正在使用。我没有密切关注这个领域，但我的第一个想法是，“它们必须得到证明。”他们将不得不表明，他们与数据中心的 DBMS 一样稳定和安全，并且无论如何您都可以从他们那里获取数据。归根结底，数据是一种公司资源，一种非常宝贵的公司资源。在某些情况下，公司拥有的数据比公司的产品更有价值。因此，对数据的全面控制和安全性是必不可少的，并且必须经过实地验证。

但是会的。因为有需要。这将是使数据中心对普通企业不再那么重要的最后一步。一些企业已经不需要数据中心，但大多数仍然需要，主要是因为数据控制和由此产生的数据重力。应用程序可以通过 Kubernetes 从云转移到云，或从云转移到内部，或从云转移到托管，这几乎是事后的想法。但是数据远没有这么灵活。最终，数 TB(或数 Pb，取决于数据集)的数据并不只是被扔进一个新的云中。虽然是分布式的；复制可以高速并行进行，使它们更具移动性。

供应商已经认识到订阅模式更容易销售，用户维护问题更少。IT 人员无需查看大量的清单来确保所有支持软件都是最新的正确版本，这是一种享受——在托管环境中，一切都会为您完成。企业已经认识到相当数量的应用程序可以是云原生的，并且正在将它们发布出去。慢慢地，随着时间的推移，越来越多的应用程序(甚至是数据密集型应用程序)将在云中适用于您的普通组织。在我看来，瓶颈将是云存储成本。云存储比其他云成本更神秘，也更昂贵。入口、出口、存储、实例…所有这些加起来，实现并行所需的实例越多，成本就越高。在这个问题解决之前，不要指望会有大规模迁移。但是迁徙终究会到来。Kubernetes 正准备尽自己的一份力量，让数据更容易使用和移动；云供应商将不得不寻找一种方法来合理化带宽的影响与我们，用户，被收取的费用。

但随着时间的推移，针对单个企业生产硬件和软件的利润将会减少。我们已经看到了一些向托管模型的转移，这应该会让您看到您的供应商的发展方向——例如，Atlassian 和几乎整个源代码扫描行业都会出现在您的脑海中。

对于大多数已经存在一段时间的组织来说，采取行动的关键来自内部动机。他们必须弄清楚如何在其数据中心内部管理具有虚拟存储的容器，然后才能放心地将该架构发布到公共云上。这是一条很好的道路，但就中短期而言，数据重力将减缓甚至停止“向云迁移！”核心应用收费。

对于大多数大型已建立的组织来说，投资回报并不是用来移动大量数据的。工作的核心系统将被保留，并可能被改进，只有当它们需要被替换时，才会考虑像全容器架构这样的东西。但是，再一次，这很可能是一个内部架构，首先，(并且经常，将永远)仅仅是因为重要的数据在那里。

对于较新的组织来说，中短期的情况正好相反。随着云中数据湖的增长，保持数据湖的成本以非线性方式增长，最终会影响盈利能力。这个小组还想了解如何在内部运行一个完全敏捷的容器基础设施，包括虚拟数据访问。

无论你属于哪一组，考虑将现场 [Kubernetes](https://kubernetes.io) 或本地云技能添加到你的天赋技能中。这些是重叠的技能。所有这些路径似乎交叉的接合点，以及带存储的全面容器自动化提供的敏捷性不会对组织产生负面影响。

继续摇摆。我们喜欢你的应用。谢谢你让他们一直哼着歌！