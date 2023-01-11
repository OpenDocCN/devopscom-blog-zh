# BlueData 通过 Spark、R 和 Python 为数据科学操作带来了 DevOps 敏捷性

> 原文：<https://devops.com/bluedata-brings-devops-agility-data-science-operations-spark-r-python/>

**加州圣塔克拉拉** [领先的大数据即服务(BDaaS)软件平台提供商 BlueData](http://www.bluedata.com/) 今天宣布了针对 [BlueData EPIC 软件平台](http://www.bluedata.com/product)的冬季新版本。这个新版本为数据科学运营提供了几个新的增强功能，为数据科学团队带来了 DevOps 敏捷性和协作，并支持新的机器学习用例。

越来越多的组织现在正在建立数据科学团队，数据科学家的角色连续第二年成为美国的第一职业。数据科学家非常擅长开发高级分析模型和原型；他们的数据驱动创新可以改变游戏规则。但是，单个数据科学家的孤立工作和定制原型可能难以扩展、复制和在多个用户之间共享。在开发中适用于特定模型的不一定适用于生产；笔记本电脑上的一次性原型在分布式计算环境中可能无法作为一致且可重复的过程。

数据科学越来越成为一项团队运动，通常涉及多名拥有不同技能和不同专业工具的数据科学家、数据工程师、数据分析师和开发人员。我们需要的是一种能够为这些数据科学和工程团队带来开发运维敏捷性、自动化和协作的方法。他们需要以简化且可重复的方式运营数据科学生命周期。他们需要敏捷和精益的过程，使他们能够快速迭代和快速失败。他们需要能够在安全的[分布式环境](http://www.bluedata.com/blog/2016/11/data-science-spark-python-r-h2o-docker/)中轻松共享数据、模型和代码。他们需要灵活地使用自己喜欢的工具，并在快速变化的数据科学领域尝试新技术。

[BlueData EPIC 软件平台](http://www.bluedata.com/product)提供了这种敏捷性和灵活性，提供了一个易于使用的自助服务界面，允许数据科学团队为他们的首选工具快速构建基于 Docker 的环境——在内部或公共云中的共享基础架构上运行，安全访问公共数据(例如，在 HDFS 数据湖或亚马逊 S3 中)。EPIC 平台的冬季新版本解决了上述许多挑战。这一新版本的一些亮点包括:

*   **协作和生产力，选择基于网络的笔记本电脑**:为数据科学团队提供使用 JupyterHub、RStudio Server 和/或 Zeppelin 笔记本电脑的选项。这些笔记本电脑中的每一台都在 BlueData EPIC [应用商店](https://www.bluedata.com/product/appstore)中作为 Docker 映像进行了预先配置和预先测试，并且可以通过自动化的一键式部署进行安装。BlueData EPIC 确保了治理、安全性和身份验证，同时为用户提供了在公共基础设施上的多租户环境中共享数据、模型和代码的能力。

*   **支持各种数据科学工具的灵活性**:blue Data EPIC 中的数据科学环境已针对 R 和 Python 支持进行了预配置，无论有无 Spark。这使数据科学团队能够使用他们喜欢的语言、包和工具，而没有测试和验证配置或版本依赖性的操作挑战。例如，数据科学家可以很容易地从 R standalone(例如 RStudio、Shiny Server)开始，然后在其他用例中选择将 R 与 Spark(例如 SparkR 和 sparklyr)一起使用；这同样适用于 Python(即使用 JupyterHub 和 PySpark)。其他工具也可以添加到 BlueData EPIC 应用商店，使用[应用工作台](https://www.bluedata.com/product/appstore)来创建新的基于 Docker 的图像。

*   **简化的作业提交，只需点击几下鼠标或以编程方式:**允许用户从 BlueData EPIC 基于 Web 的 UI 或 REST API 轻松提交 R、Python、Spark、Hadoop 或 SQL 作业——针对持久性或暂时性集群。这有助于数据科学团队快速响应动态业务需求，只需点击几下鼠标或使用简单的代码，即可针对数据运行从分析 SQL 到激发机器学习脚本的各种作业。

*   **引导和其他动作脚本，用于自动化数据科学操作:**提供了在运行环境中轻松修补和更新部分或所有节点的能力，只需单击一下鼠标。BlueData EPIC 中的引导操作脚本可以在创建环境期间和之后执行，例如安装附加软件或更改配置。这有助于消除设置、配置和管理数据科学环境的端到端生命周期的运营开销。

*   **支持机器学习和广泛的其他数据科学用例:** BlueData 继续向其平台添加新的大数据框架和工具，包括预集成的 H2O 以及 Spark MLlib 和其他机器学习工具。借助 BlueData EPIC 应用商店中为 H2O 预先配置的 Docker 映像，客户现在可以快速部署 H2O 的机器学习库集——包括 H2O 的 R、H2O 的 Spark(即“苏打水”)，以及 H2O 的 Flow 用户界面。

数据科学从来没有真正采用“一刀切”的解决方案。借助 BlueData EPIC 平台，数据科学团队可以使用 Scala、Python、R 或 SQL 分析数据；用 R，Python，Spark MLlib，或者 H2O 建立模型；使用 RStudio 或 JupyterHub 或 Zeppelin 笔记本电脑运行和可视化他们的分析——所有这些都在同一个 Spark 集群上，使用共享数据。数据科学家和其他用户可以灵活地利用各种工具和算法来解决日益复杂的用例集。

这一新版本建立在 BlueData 过去一年持续[产品创新的基础上。最近，BlueData 宣布](http://www.bluedata.com/article/increased-demand-for-big-data-as-a-service-and-triple-digit-growth/) [BlueData EPIC on AWS](https://www.bluedata.com/article/bluedata-delivers-ultimate-flexibility-choice-big-data-deployments-amazon-web-services/) 为亚马逊云上的大数据部署提供终极灵活性和选择，包括利用亚马逊 S3 和内部存储的能力。BlueData 提供了唯一一个可以在内部、公共云中或混合架构中部署的大数据即服务解决方案。

BlueData 的联合创始人兼首席执行官 Kumar Sreekanti 表示:“企业是时候将 DevOps 的好处扩展到他们的数据科学和工程团队，无论是实时分析和机器学习还是其他用例。“BlueData 客户可以为其数据科学运营带来这种敏捷性和速度，只需点击几下鼠标即可创建完全集成的数据科学环境，包括内部和公共云中的环境。”

BlueData 将于 2 月 8 日和 9 日在波士顿举行的 [Spark Summit East](https://spark-summit.org/east-2017) 活动中在 K8 展台展示这一新功能。BlueData 的联合创始人兼首席架构师 Thomas Phelan 将于 2 月 8 日(T6)周三中午 12:20在 Spark 峰会上发表关于“[从记录 Spark 工作负载](https://spark-summit.org/east-2017/events/lessons-learned-from-dockerizing-spark-workloads)中吸取的教训”的演讲。

——[儒勒·路易斯](https://devops.com/author/jules/)