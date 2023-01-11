# Platform9 的托管 Kubernetes 解决方案增加了“套利”功能，可以在 Amazon EC2 Spot 实例上动态运行集群中的节点

> 原文：<https://devops.com/platform9s-managed-kubernetes-solution-adds-arbitrage-capabilities-to-dynamically-run-nodes-in-a-cluster-on-amazon-ec2-spot-instances/>

*解决方案自动优化* *成本和基础架构利用率通过持续评估云成本并以最低的可用价格动态分配容量，同时确保满足可用性和性能 SLA*

加利福尼亚州森尼维尔–2018 年 8 月 28 日–平台 9([https://platform9.com/](http://icm-tracking.meltwater.com/link.php?DynEngagement=true&H=3ZUQjNycMu7D%2Fe%2Bm%2FOmi3Qi1eTNrfRb0HcFplK3KYerw%2B6SfjwwI9kh3P9QdM4DUAoT0FMaTY8rJ504VtPlujmGEB4Kq05t1aeA4jBjO0YED22OjsP6SAQ%3D%3D&G=0&R=https%3A%2F%2Fplatform9.com%2F&I=20180828130351.000000335759%40mail6-53-ussnn1&X=MHwxMDQ2NzU4OjViODRiOThiOGEzYTA5MjdmMmJlNTA4YTs%3D&S=dZGEK-ilegp6F9n7zAk1ysDsdr1IxSDzdTAWC9nqTCY))，t 他是 SaaS 管理的混合云的领导者，今天宣布套利–平台 9 管理的 Kubernetes 的新功能 。该解决方案允许公司定义 Kubernetes 集群中节点总数的百分比，以可调整的 Spot 投标价格在 Amazon EC2 上部署 Spot 实例，以及保持什么级别的容错和性能。它还通过根据目标 SLA 不断评估云资源的定价，以自动决定是部署 Spot 实例还是标准 EC2 实例，从而为组织提供改进的云成本控制。当与裂变、开源无服务器框架([【https://fission.io/】](http://icm-tracking.meltwater.com/link.php?DynEngagement=true&H=3ZUQjNycMu7D%2Fe%2Bm%2FOmi3Qi1eTNrfRb0HcFplK3KYerw%2B6SfjwwI9kh3P9QdM4DUAoT0FMaTY8rJ504VtPlujmGEB4Kq05t1aeA4jBjO0YED22OjsP6SAQ%3D%3D&G=0&R=https%3A%2F%2Ffission.io%2F&I=20180828130351.000000335759%40mail6-53-ussnn1&X=MHwxMDQ2NzU4OjViODRiOThiOGEzYTA5MjdmMmJlNTA4YTs%3D&S=1uRXdJKh93VnPacaR-du2M8WEYC1xWooYcPYHhF_OLc))结合时，套利的优势被进一步实现，用于使用比更昂贵的 EC2 实例或公共云提供的专用 Kubernetes 服务更便宜的云资源来执行 Kubernetes 的功能。

**了解有关套利和其他平台 9 Managed Kubernetes 功能的更多信息，请访问:(**[**【https://platform9.com/managed-kubernetes/】**](http://icm-tracking.meltwater.com/link.php?DynEngagement=true&H=3ZUQjNycMu7D%2Fe%2Bm%2FOmi3Qi1eTNrfRb0HcFplK3KYerw%2B6SfjwwI9kh3P9QdM4DUAoT0FMaTY8rJ504VtPlujmGEB4Kq05t1aeA4jBjO0YED22OjsP6SAQ%3D%3D&G=0&R=https%3A%2F%2Fplatform9.com%2Fmanaged-kubernetes%2F&I=20180828130351.000000335759%40mail6-53-ussnn1&X=MHwxMDQ2NzU4OjViODRiOThiOGEzYTA5MjdmMmJlNTA4YTs%3D&S=oBAJ6b4SBLmPYh3Ca7b6MXU2a17bhVCZwOt2_JaIOug)**)。**

Platform9 的联合创始人兼首席执行官 Sirish Raghuram 表示:“通过套利，组织可以显著降低其亚马逊 EC2 成本，而不会牺牲基于 Kubernetes 的任务关键型应用程序的容错能力。“套利是我们为客户提供的自动化管理功能的另一个例子，使他们能够利用新技术，如 Kubernetes，同时降低基础设施成本和管理开销。”

Platform9 Managed Kubernetes 是业内唯一的企业级 SaaS 管理解决方案，不受基础设施限制，可在任何公共云和内部基础设施上运行。这种远程管理的服务通过提供 it 即服务(包括部署、监控、升级、容错和故障排除)来消除使用 Kubernetes 处理企业工作负载的操作复杂性，所有这些都是自动处理的。Platform9 Managed Kubernetes 使企业能够在一小时内从任何基础架构环境下的强大生产级 Kubernetes 解决方案中受益，该解决方案内置了所有企业功能，如 SSO、备份、故障转移和 HA 集群、自动修复等，所有这些都由该公司的 247x7x365 SLA 提供支持。

为了让用户更快地利用 Kubernetes 实现价值，Platform9 创建了 [裂变](http://icm-tracking.meltwater.com/link.php?DynEngagement=true&H=3ZUQjNycMu7D%2Fe%2Bm%2FOmi3Qi1eTNrfRb0HcFplK3KYerw%2B6SfjwwI9kh3P9QdM4DUAoT0FMaTY8rJ504VtPlujmGEB4Kq05t1aeA4jBjO0YED22OjsP6SAQ%3D%3D&G=0&R=https%3A%2F%2Ffission.io%2F&I=20180828130351.000000335759%40mail6-53-ussnn1&X=MHwxMDQ2NzU4OjViODRiOThiOGEzYTA5MjdmMmJlNTA4YTs%3D&S=1uRXdJKh93VnPacaR-du2M8WEYC1xWooYcPYHhF_OLc) ，这是业界领先的开源无服务器框架，是 Kubernetes-native，在 Apache 许可下可以免费使用。有了裂变，开发人员可以轻松地编码、部署和操作无服务器应用程序，这些应用程序从一开始就是生产就绪的，而无需了解任何有关 Kubernetes 的知识。它允许运营商在自己的后院，在任何基础设施上实现类似 Lambda 的体验(AWS 的无服务器服务),而没有锁定风险或产生额外的云成本。

此外，Platform9 的混合云解决方案提供了单一管理平台，提供了跨虚拟机、Kubernetes 和无服务器功能的统一体验。这确保了企业在其内部和云中的所有技术堆栈和环境中拥有一致的管理和可见性。

**关于平台 9**

平台 9([platform9.com](http://icm-tracking.meltwater.com/link.php?DynEngagement=true&H=3ZUQjNycMu7D%2Fe%2Bm%2FOmi3Qi1eTNrfRb0HcFplK3KYerw%2B6SfjwwI9kh3P9QdM4DUAoT0FMaTY8rJ504VtPlujmGEB4Kq05t1aeA4jBjO0YED22OjsP6SAQ%3D%3D&G=0&R=https%3A%2F%2Fwww.platform9.com%2F&I=20180828130351.000000335759%40mail6-53-ussnn1&X=MHwxMDQ2NzU4OjViODRiOThiOGEzYTA5MjdmMmJlNTA4YTs%3D&S=ZdlToNLoWev6qNzpeLOaFyr8nNEVVMIrPR_0MeYjUjo))提供 SaaS 管理的混合云解决方案，将现有基础架构立即转变为云。我们帮助企业推动数字化转型，使他们能够管理任何基础设施上的虚拟机、容器和无服务器功能，无论是在内部、公共云中还是在边缘，并提供简单统一的自助式体验。Cadence、Autodesk、Splunk、EBSCO、Bitly、LogMeIn 和 Aruba 等客户的 IT 效率提高了 300 %,上市时间缩短了 33 %,数据中心利用率提高了 50 %- 80 %,成本降低了。该公司总部位于加利福尼亚州森尼韦尔，由红点风险投资公司、门洛风险投资公司、Canvas 风险投资公司和 HPE 公司提供支持。

###