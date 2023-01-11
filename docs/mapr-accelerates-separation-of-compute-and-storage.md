# MapR 加速了计算和存储的分离

> 原文：<https://devops.com/mapr-accelerates-separation-of-compute-and-storage/>

*新的进步使得在 Kubernetes 中部署本地 Spark 和 Drill 应用变得更加容易*

**加州圣克拉拉–2019 年 4 月 2 日—[MapR 技术公司](https://mapr.com/?utm_source=press-release&utm_medium=referral&utm_campaign=wpr-body)** 。是人工智能和分析的下一代数据平台的富有远见的创造者，今天宣布了 MapR 数据平台的创新，通过与 Kubernetes 核心组件的新深度集成，加速了 Spark 和 Drill 上主要工作负载的计算之旅。这些创新使得更好地管理高弹性工作负载变得更加容易，同时还促进了及时部署以及分别扩展计算和存储的能力。通过轻松利用此类集群的弹性和敏捷性，重组其应用程序或构建下一代实时数据湖的组织将受益于 Kubernetes 模型中的这些新功能，以及 Spark 和 Drill。

ESG 高级分析师 Mike Leone 表示:“我们最近对组织使用容器支持人工智能和分析计划的情况进行了调查，很明显，大多数组织都在探索在生产中使用容器和 Kubernetes。我们还看到，由于以计算为中心的应用程序和工作负载的不可预测性，计算需求正在快速增长。MapR 正在解决这种独立扩展计算的需求，同时与 Kubernetes 紧密集成，以应对组织对容器的快速采用。"

2019 年初，MapR 通过一个符合 CSI 的卷驱动插件，为 Kubernetes 管理的容器中运行的计算启用了持久存储。通过此次发布，MapR 进一步扩展了其功能组合，并允许将 Spark 和 Drill 部署为由 Kubernetes 编排的计算容器。这种部署模式允许包括数据工程师在内的最终用户在独立于数据存储或管理位置的 Kubernetes 集群中运行计算工作负载。此版本包括以下核心功能:

*   **租户操作符**:为运行计算应用程序创建租户名称空间(Kubernetes 名称空间)，允许以简单的方式在 Kubernetes 的容器中启动复杂的应用程序。最终用户可以在这些名称空间中运行 Spark、Drill、Hive Metastore、Tenant CLI 和 Spark History Server。这些租户又可以指向位于其他位置的存储集群。
*   **Spark Job Operator** :创建 Spark 作业，允许将不同版本的 Spark 部署在不同的 pod 中，从而简化数据工程师工作流程中常见的开发、测试和 QA 等多个阶段。
*   **Drill Operator** :启动一组钻头，允许根据需求自动扩展查询。
*   **CSI 驱动操作员**:安装持久卷的标准插件，以便在 Kubernetes 中运行有状态的应用程序。

“MapR 为企业组织轻松完成两件关键事情铺平了道路:开始分离计算和存储，并在运行分析性 AI/ML 应用程序时快速采用 Kubernetes，”MapR SVP 工程公司的 Suresh Ollala 说。“与 Kubernetes 核心组件的深度集成，如操作符和名称空间，允许我们定义多个具有资源隔离和限制的租户，所有租户都运行在同一个 MapR 平台上。这不仅对于需要灵活性和弹性的应用程序，而且对于需要在云之间来回移动的应用程序，都是一个重要的推动因素。”

在此版本中，MapR 提供了六大优势:

*   通过旋转额外的计算容器来处理计算突发，而无需添加更多的物理主机服务器；
*   通过对配额设置粒度限制，以及通过使用 Spark 作业操作符来创建不同的 Spark 集群，隔离资源并防止应用程序彼此缺乏资源；
*   根据负载和需求动态增加钻头，以适应不断变化的查询工作负载；
*   在同一平台上运行不同版本的 Spark 和 Drill，
*   允许多个租户共存；和
*   在包括私有云、混合云和公共云在内的多种云环境中部署 Spark 和 Drill 容器应用程序以及 MapR 卷；

这些功能将在 2019 年 Q2 奥运会上提供。

**支持资源**

**博客**:[https://mapr . com/Blog/deploying-native-spark-and-drill-applications-in-kubernetes-just-get-easy/](https://mapr.com/blog/deploying-native-spark-and-drill-applications-in-kubernetes-just-got-easier/)

**图片**:[https://mapr . com/products/whats-new/compute-storage/assets/supported-deployment-models-SDM . jpg](https://mapr.com/products/whats-new/compute-storage/assets/supported-deployment-models-sdm.jpg)

**发这条微博:** [【电子邮件保护】](/cdn-cgi/l/email-protection)加速计算和存储的分离# containers # Kubernetes[https://mapr . com/company/press-releases/mapr-Accelerates-Separation-of-Compute-and-Storage/](https://mapr.com/company/press-releases/mapr-accelerates-separation-of-compute-and-storage/)

**关于 MapR 技术**

[MapR Technologies](https://mapr.com/?utm_source=press-release&utm_medium=referral&utm_campaign=wpr-footer) 是一家富有远见的硅谷软件公司，是人工智能和分析的下一代数据平台的创造者，具有企业级关键任务部署所需的规模和可靠性。MapR 数据平台提供了 dataware 的强大功能来加速数据驱动的创新。思科、飞利浦和兴业银行等具有前瞻性的公司能够创造新的数据驱动型解决方案，从而在竞争中脱颖而出。了解更多:【mapr.com】。

MapR 是 MapR Technologies，Inc .在美国和其他国家的注册商标。其他名称和品牌可能是其他人的财产。

###