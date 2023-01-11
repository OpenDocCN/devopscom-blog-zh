# 用分布式账本统一合作伙伴生态系统

> 原文：<https://devops.com/unifying-partner-ecosystems-with-a-distributed-ledger/>

区块链近年来因推动加密货币热潮而闻名。但是区块链背后的基本原理也可能对数据经济的其他领域有所帮助。因为，随着数据价值的上升，对跨多个合作伙伴的准确、实时数据共享的需求也在增加。

正如我们最近看到的，全球贸易变化无常，令人惊讶。如果一艘 1300 英尺长的货船最终会阻塞苏伊士运河整整一周，想象一下航运和物流行业每天要整理多少记录不一致的数据。类似地，其他合作伙伴网络，例如食品分销或航空公司，必须不断地来回共享数据才能保持业务。

由于分布式账本是外部的，但可以与合作伙伴共享，因此它提供了一些有趣的数据共享可能性。与协作软件的合并类似，合作伙伴将检索和操作分布式分类帐，这将作为物理对象或数据的状态的真实来源。从本质上讲，这一过程可以减少人工协调工作，并避免出现问题时的纠纷。

我最近与“无服务器之父”和 AWS Lambda 的发明者 Tim Wagner 进行了交谈。现在执掌 Vendia 的 Wagner 与我分享了他为什么预见分布式分类账是实时的、企业对企业的数据共享的未来。“供应链惊人地脆弱，”瓦格纳说。为了解决这个问题，我们需要一个“不再集中的自动化工作流程，”他说。

## 分布式分类帐的角色

分布式分类账可能与多方供应链特别相关。在多合作伙伴协议中，数据跟踪很复杂，许多合作伙伴很难走到一起。“公司正在为缺乏真相而挣扎，”瓦格纳说。“每个人都想要自己的数据副本，但他们希望它被锁定到每个人同时看到的内容。”

例如，以供应链管理为例。假设一家汽车零部件制造商生产一款底盘。他们将它发送给运输物流提供商，后者再将其发送给汽车制造商，以完成汽车的组装。如果机箱在这些移交过程中的某个点损坏了，是谁的错？瓦格纳解释说，如果没有记录系统，就会产生很大的不信任问题。

或者，考虑一个航空公司生态系统。伙伴航空公司必须经常协调多承运商航班计划、申请折扣或结算未使用的旅行优惠券。通常，很难跟踪组织之间这些交易的过程。外部化的分类账可以帮助伙伴航空公司跟踪单个乘客的路线，有助于简化财务结算。

瓦格纳说:“这不仅仅是分享，这已经够难了，但这真的是有控制的分享。”如今，跟踪数据的沿袭是至关重要的，就像实时了解对象的状态一样。分布式账本可以帮助这些伙伴生态系统拥有一份他们都可以信任的记录。瓦格纳将此描述为防篡改、不可改变的记录——一个“无懈可击的真理来源”

## 这会取代合作伙伴 API 吗？

对于有集成思想的人来说，特别有趣的是分布式分类帐概念可能会取代现有的企业对企业的通信模型。在过去的几十年里，大多数合作伙伴的集成都转向了 RESTful API 连接。一家公司开放数据访问，另一家经过认证的合作伙伴调用 HTTP API 将数据集成到他们自己的应用程序中。

然而，这里的问题是 API 只是提供者拥有的私有数据库之上的一层。闭门造车，没有行业范围的实时数据同步。Wagner 说，API 调用有利于数据检索和操作，但是将成千上万的事务串在一起是困难的。对于同步调用来说，保持复杂数据库的时序完整性有点太难了。

瓦格纳认为分布式账本更适合某些企业对企业的机器自动化，而不是通过 API 开放对内部平台的访问。“任何你看到 API 级协议发展成熟的地方都是一个好迹象；他说:“分布式总账很有可能会获得更快的速度。“试图通过 API 提取信息并祈祷找到正确的数据是很难管理的。”

例如，Wagner 提到了一些动物收容所如何创建一个全球信息库来避免孤立的记录。通过这样做，他们正在为一个统一的数据库制定一个全球动物救助计划，有望帮助每只宠物找到一个家。

与分类帐通信仍然会涉及到调用，但可能不是典型的 RESTful 请求。Wagner 提倡使用 GraphQL 作为更好的方法，让客户参与到变更中来。有了 GraphQL API，利益相关者可以查询、变异和订阅分布式系统中的变化。Wagner 说，GraphQL 并不完美，但其简单的数据机制使其成为 REST 和 SQL 之间的一个金发女孩式的中间地带。

## 获得认同

同步的分布式分类账有助于解决争议，减少人工检查。但是，我们如何获得认同呢？如何说服整个合作伙伴生态系统围绕分布式账本作为事实的来源？

瓦格纳说，通常有一个领导者或单一制造商带头冲锋陷阵。在这个过程中，这个人物可能是一个更突出、更受尊敬的角色。Wagner 说，但是要使数字分类账系统成功，它还必须满足其他标准:

*   **数据模式预先考虑**:就共享数据模式达成一致可能是一个挑战。在设计长期数据模型时，生态系统将需要深谋远虑。
*   **合规性**:有许多新的数据法规需要考虑，例如 GDPR、CCPA 和 PCI。“你不能像过去那样盲目复制数据，”瓦格纳说。
*   **治理**:当企业处理跨越边界的数据时，它们必须应用治理措施来满足合规性并维护安全性。这种治理需要与数据紧密关联，并提供细粒度的控制。
*   **高性能**:Wagner 指出，分布式分类帐需要大对象的操作灵活性，例如 5 TB 的文件。
*   编辑能力:尽管一些合作伙伴必须看到所有的字段，但是根据法律，其他合作伙伴可以查看的内容有限。因此，分类帐必须包括编辑字段的能力。瓦格纳将此描述为“对个人客户记录的有意编辑或可见性控制。”

当然，不同的行业在其数字化之旅中处于非常不同的阶段，有些行业比其他行业更先进。比如，对于支持 ACH 支付技术的金融服务来说，变化可能更容易，瓦格纳将其描述为“自然有机扩展为以数据为中心的方法的时机已经成熟。”

## 穷人的区块链

接入相同的 feed，一个广泛的合作伙伴生态系统可以使用区块链式的安排来保持一致。这有助于减少通常通过电子邮件或电话进行的人工对账。

然而，Wagner 说，由于分布式系统专家很少，实施这种技术很可能涉及云平台解决方案。他开玩笑地称之为“穷人的区块链”这种解决方案必须是云友好的、以企业为中心的，并且易于集成和部署。

随着越来越多的关键数据开始驻留在公司之外，“组织必须重建这些数据，以便与合作伙伴合作，”Wagner 说。事实上，分布式分类帐可以充当一种外包的集中式 IT，为无服务器环境提供数据模型。