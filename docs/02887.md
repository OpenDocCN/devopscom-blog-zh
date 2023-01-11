# Databricks 统一分析平台简化了分布式深度学习

> 原文：<https://devops.com/databricks-unified-analytics-platform-simplifies-distributed-deep-learning/>

*统一分析领导者支持新的 Apache Spark 2.4 引入新功能简化分布式深度学习*

旧金山—([美国商业资讯](https://www.businesswire.com/))—[统一分析领域的领导者、由 Apache Spark 的创始人创立的 Databricks](https://databricks.com/) 今天宣布支持 Databricks 统一分析平台中新发布的 Apache Spark 2.4.0。Databricks 是第一家支持 Apache Spark 2.4 的统一分析供应商。它作为 [Databricks Runtime](https://databricks.com/glossary/what-is-databricks-runtime) 5.0 的一部分受到支持，该版本现已全面上市。Databricks 还在 Runtime 5.0 中引入了一个关键功能 HorovodRunner，以进一步简化分布式深度学习。

Apache Spark 社区为 2018 年 11 月 8 日推出的 Spark 2.4 版本做出了多项宝贵贡献。在这个版本中，Project Hydrogen 大幅提高了 Spark 上分布式深度学习和机器学习框架的性能和故障恢复能力。氢项目直接解决了数据团队面临的挑战，因为大数据作业和深度学习作业的执行方式存在显著差异。Spark 擅长大规模数据处理，而深度学习假设任务之间完全协调和依赖，这是为了持续通信而不是可扩展性和容错而优化的。

“创新在 Apache Spark 社区中继续蓬勃发展。“氢项目是最近的一项重大举措，旨在为 Apache Spark 上流行的分布式机器学习框架提供一流的支持，”Apache Spark 成员、Databricks 的联合创始人 Reynold Xin 表示，他是该项目的主要贡献者。

在 Apache Spark 2.4 中，Project Hydrogen 引入了 Barrier Execution，这是一种新的调度模式，允许从业者将分布式深度学习培训作为 Apache Spark 工作负载适当嵌入。Xin 补充道，“这是自项目开始以来 Spark 调度程序的最大变化。在 Databricks，我们还发现了其他机会来简化机器学习工作负载的复杂性。在 Databricks 的统一分析平台(由 Spark 2.4 提供支持)中，我们进行了进一步的优化，以简化分布式深度学习。"

**Databricks 简化运行时分布式深度学习 5.0**

在根据需要扩展计算之前，模型实验通常在本地或云中的单节点机器上进行。从单节点工作负载迁移到 CPU 或 GPU 集群上的分布式培训往往需要重新编写完整的代码，从而增加了迁移到分布式培训的复杂性。为了加速向分布式深度学习的迁移，Databricks 刚刚发布了 HorovodRunner。新功能提供了一种简单的方法来将深度学习训练工作负载从单台机器扩展到大型集群，将整体编程和训练时间从数小时减少到数分钟。

为了帮助进一步简化深度学习，Databricks 还提供了与最受欢迎的框架(包括 TensorFlow、Keras 和 Horovod)的原生集成，以及与来自 MLlib 和 GraphFrames 的最受欢迎的机器学习算法的性能优势。这为从业者提供了一种便捷的方式，让机器学习集群在几秒钟内启动，并预先配置了最新的机器学习框架、库及其依赖关系。

**附加资源**

*   Databricks 博客:[宣布 Databricks 运行时 5.0](https://databricks.com/blog/2018/11/16/announcing-databricks-runtime-5-0.html)
*   Databricks 博客:[介绍 Apache Spark 2.4](https://databricks.com/blog/2018/11/08/introducing-apache-spark-2-4.html)

**关于数据块**

Databricks 的使命是通过统一数据科学、工程和业务来加速客户的创新。Databricks 由 Apache Spark 的原始创建者创建，为数据科学团队提供了一个统一的分析平台，以便与数据工程和业务线合作来构建数据产品。通过创建从 [ETL](https://databricks.com/glossary/extract-transform-load) 和交互式探索到生产的分析工作流，用户可以利用 Databricks 更快地实现价值。该公司还通过提供全面管理、可扩展且安全的云基础架构来降低运营复杂性和总拥有成本，从而使用户更容易专注于他们的数据。Databricks 得到了安德森·霍洛维茨、NEA 和 Battery Ventures 等公司的风险投资支持，其全球客户群包括维亚康姆、壳牌和惠普。

Apache、Apache Spark 和 Spark 是 [Apache 软件基金会](https://www.apache.org/)的商标。