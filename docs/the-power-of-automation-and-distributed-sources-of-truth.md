# 自动化和分布式真相来源的力量

> 原文：<https://devops.com/the-power-of-automation-and-distributed-sources-of-truth/>

企业网络是庞大而复杂的系统，具有多种存储配置和状态信息的方法。随着新应用、服务或其他更新的增加，这些网络的配置也在不断变化。当您考虑企业网络的复杂性和动态性时，您可能会惊讶地发现有多少数据(包括大多数网络配置)仍在手动更新，而且经常是在半夜。为了使这一过程效率更低，更新人员需要手动将这些更新记录在电子表格上或定制的数据库中。

依靠手动过程来维护和管理企业网络的状态不仅为错误敞开大门，而且还会导致网络电子表格或数据库与网络的实际当前状态不同步。网络正确吗？还是电子表格正确？我们应该让网络看起来像电子表格吗？还是应该更新电子表格以反映网络？真实的实际来源是什么？

好消息是现代网络的现实已经改变了范式。随着可编程网络的广泛部署，不再需要手动 CLI 界面。读写网络配置和读取网络状态可以用机器和自动化快速方便地完成。

### 真理的来源

越来越多的企业开始采用[网络自动化](https://devops.com/?s=network+automation),因为他们认识到了网络自动化在管理复杂网络时可以带来的效率，以及这些效率可以增加利润的好处。但是如果您打算自动化您的基础设施，您的自动化解决方案将需要从某处收集关于它的权威信息。这一事实来源包含了使自动化对网络做出改变所需的知识。

许多企业网络团队认为他们需要依靠单一的事实来源来了解网络的真实状态。他们认为，建立一个能够与整个网络中所有设备的配置和状态信息同步的单一系统/服务器/数据库是一个可行的解决方案。但这样的解决方案目前还不存在。鉴于当今网络的多样性，依赖单一来源不仅不切实际，而且可能成本高昂。

而不是问“真理的唯一来源是什么？”也许更好的问题是“什么将提供更好的数据:创建一个试图与整个网络同步的单一真实来源？或者访问实时完成自动化所需的分布式事实来源？”

企业不应该依赖于单一的事实来源，而应该关注于访问多个事实来源，以进行适当和有意义的自动化。

### 撒开更大的网

例如，如果你在运营一个服务提供商网络，你的业务就是你的网络。如果您已经在网络资产上花费了数百万甚至数十亿美元，那么就值得花时间建立一个系统来准确地管理和维护这些资产。单一的真相来源无法提供这一点。

此外，随着网络规模和复杂性的扩大，将真实来源同步到网络所需的时间也会增加，从而限制了同步的频率，并导致同步状态之间的时间差异更大。

最后，试图创建单一来源的过程也没有解决真正的问题，即企业仍然依赖手动过程，这几乎总是会导致真实来源[数据库](https://devops.com/of-devops-databases-and-dbas/)和实际网络状态在某些时候不同步。这也会对企业产生严重的负面影响。

访问多个真实来源的情况相对简单:它允许更大的灵活性，并使企业能够更容易地利用数据来使其业务受益。

随着可编程网络(机器与机器之间的对话)的出现，最新的自动化解决方案可以访问多个分布式事实来源(负责网络不同部分的事实来源的不同 API 和数据库),并实时联合和同步来自这些系统的数据，从而提供更真实的网络状态窗口和更准确、可操作的数据，为企业带来商业价值。

### **自动化犹豫**

那么，为什么有些企业仍然不愿意实施全面的网络自动化项目呢？这有各种各样的原因，但很明显，有人担心没有网络数据的单一真实来源(或可能不是 100%准确的数据)会影响自动化流程。这是一个经典的“[恐惧、不确定和怀疑](https://www.kenrockwell.com/business/fud.htm)”思维过程:“如果数据只有 70%的准确性呢？如果我们试图自动处理不良数据，我们将有 30%的时间会中断网络。”

一些网络团队可能认为他们不能自动化任何事情，直到他们能够将他们的五六个真实来源合并成一个巨大的数据库。与此同时，领导层可能会推动这些网络团队推进自动化，以从网络中获得更多价值。如果选择等到最终拥有一个“原始的”数据库，他们可能会损失几个月甚至几年的时间，这对谁都没有好处。

解决方案是采取增量方法。查看所有各种网络资产–可编程、云、传统等。–在存在良好数据且不需要建立事实来源的领域启动自动化流程。与此同时，您可以清理其他数据，并在数据准备就绪时添加自动化。

能够利用多个真实来源比担心拥有一个“完美的”真实来源和阻碍自动化计划要好。从长远来看，对网络团队和业务都有好处。

部署正确的自动化解决方案与致力于能够集成多种真实来源以做出决策的自动化解决方案同样重要。最有效的自动化解决方案将包括:

● **API 优先**–将多个真实来源整合为一个统一来源的唯一方法是通过 API 优先的方法，允许系统之间相互对话。
● **数据联合和转换**——只有当团队能够将数据完全集成在一起，同时确保它们使用相同的语言时，拥有统一的真实来源才是有效的。
● **统一视图**–来自集成系统的数据、流程和逻辑的抽象和联合视图支持整个网络的单一平台，以及用于简化整个组织自动化的管理工具。

### 多个来源意味着更多可操作的数据

在当今现代化、可编程的网络环境下——以及企业访问准确、实时的网络数据的绝对必要性——依赖单一来源的事实是基于一个有缺陷的假设，即我们总是可以拥有一个同步的数据库，因此这不是一个可行的策略。

通过采用网络自动化，组织可以采用分布式真实源解决方案，使多个记录系统及其收集的数据充当真实源，从而减少数据质量问题和手动错误。

随着企业实施其自动化战略，在网络中拥有多个真实来源将为自动化的成功提供更加准确、及时和可操作的数据，从而提高效率并推动业务向前发展。