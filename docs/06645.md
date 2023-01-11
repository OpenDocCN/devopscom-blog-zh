# Elyra 达到 1.0.0

> 原文：<https://devops.com/elyra-reaches-1-0-0/>

**IBM CODAIT 开源人工智能平台架构师 Luciano Resende**

Elyra 是一个开源项目，它扩展了 JupyterLab 用户界面，以简化数据科学和 AI 模型的开发。

Elyra 自豪地宣布其 1.0.0 版本。如果这是你第一次听说 Elyra，查看我们的 [公告博客](https://developer.ibm.com/technologies/artificial-intelligence/blogs/open-source-elyra-ai-toolkit-simplifies-data-model-development/) 了解更多关于该项目的细节。

Elyra 的 1.0.0 版本包括:

*   笔记本管道可视化编辑器
*   能够将笔记本电脑作为批处理作业运行
*   可重用代码片段(新)
*   混合运行时支持(基于 Jupyter 企业网关)
*   编辑器中的 Python 脚本执行功能
*   使用自动生成的目录的 Python 脚本导航
*   笔记本导航使用自动生成的目录
*   基于 Git 集成的笔记本版本管理
*   运行时的可重用配置和编辑器(新)
*   支持 JupyterLab 2.x(新)
*   JupyterHub 支持(新)
*   能够从活页夹中尝试 Elyra(新)
*   支持 JupyterLab 黑暗主题

**笔记本管道**

Elyra 的笔记本管道编辑器简化了将多个笔记本转换为批处理作业或工作流的过程。通过利用基于云的资源来更快地运行他们的实验，数据科学家、机器学习工程师和人工智能开发人员的工作效率会更高，因此能够花更多的时间专注于他们的技术技能。

基于 Elyra 用户群的巨大反馈，此版本带来了许多错误修复和可用性增强，例如:

*   增强的内嵌用户文档
*   管道编辑器的验证功能，通知用户配置值缺失或无效
*   优化的依赖关系处理提供了更快的管道提交
*   从 Pipeline 编辑器更容易地访问以前提交的实验
*   支持将“自带映像”用作在外部运行时执行笔记本的环境

**可重用的代码片段**

代码片段使您能够节省时间并重用面向任务的代码块。Elyra 的新代码片段扩展支持直接从 JupyterLab 工作区轻松发现、创建和插入可重用的代码片段到您的笔记本、Python 脚本甚至用于文档的 Markdown 文件中。这使得编写代码的过程更加有效和容易。

可用代码片段的列表位于左侧窗格中，包括每个代码片段的预览，以及复制代码片段或直接内联插入代码片段的选项。

还可以在 JupyterLab 中方便地创建和编辑代码片段。

**利用笔记本目录和 Python 脚本**

导航大型文件以查找笔记本中的特定部分或 Python 脚本中的函数定义可能是一项艰巨的任务。为支持导航 Python 脚本而增强的内容列表扩展提供了一个简单的内容大纲，从而实现了轻松导航。

为了简化 python 开发，Elyra 的 python 编辑器现在附带了一个自动生成的目录，允许在大型 python 脚本中高效导航。

**运行时可重复使用的配置和编辑器**

Elyra 引入了“共享配置服务”,简化了工作区配置管理，使诸如访问外部运行时的信息等内容只需配置一次，就可以在多个组件之间共享。

在 Elyra 1.0 中，这个服务现在被多个组件使用，并通过基于模式的验证功能和全套 REST APIs 得到了增强。在 Elyra 的这个版本中，用户还可以在 JupyterLab 用户界面中轻松地浏览、创建和编辑这些配置。

**JupyterHub 支持**

在 Elyra 1.0.0 中，我们还创建了一个 docker 映像，并提供了必要的[配置步骤]([)https://Elyra。【readthedocs.io/en/latest/】<wbr>配方/部署-elyra-in-a-<wbr>jupyterhub-endvironment.html](https://elyra.readthedocs.io/en/latest/recipes/deploying-elyra-in-a-jupyterhub-endvironment.html))将 Elyra 与 JupyterHub 整合。

**试试活页夹里的 Elyra】**

要在本地不安装 Elyra 的情况下进行实验，只需点击 binder 链接:
 [https://mybinder.org/v2/gh/<wbr>Elyra-ai/Elyra/v 1 . 0 . 0？URL path =<wbr>lab/tree/binder-demo](https://mybinder.org/v2/gh/elyra-ai/elyra/v1.0.0?urlpath=lab/tree/binder-demo)

**在真实分析和人工智能场景中使用 Elyra**

在构建 Elyra 的过程中，我们与数据科学家、机器学习工程师和人工智能开发人员密切合作，我们一直在构建一些场景，以验证使用 Elyra 开发模型和其他应用程序时的用户体验。

**分析新冠肺炎时间序列数据**

其中一个例子创建了一个管道来分析来自美国和欧洲的新冠肺炎时间序列数据集，这个管道在[covid-notebook github repository]([https://github 中是开源的。<wbr>com/CODAIT/covid-notebooks](https://github.com/CODAIT/covid-notebooks)

**分析 NOAA 天气时间序列数据集并探索预报**

另一个例子是利用[DAX–数据资产交换]([)https://developer。【ibm.com/exchanges/data/】](https://developer.ibm.com/exchanges/data/))NOAA 数据集，产生一个管道，消费并应用 ETL 到数据集，然后着手分析和试验不同的预测能力。

**Elyra 社区收养**

Elyra 社区正在非常努力地促进采用，并围绕该项目创建一个健康社区。在过去几个月中，我们开始看到过去几周的一些势头，以下是一些细节:

**Github Stars** :截至 2020 年 8 月，Elyra 主存储库已接近 500 颗星星，请继续支持该项目，并给予我们更多星星。

**依赖于 elyra 的项目:**除了上面提到的两个示例场景之外，我们开始看到其他社区在他们的项目中采用 Elyra，CalPoly 已经在他们的暑期实习生项目中使用 Elyra 代码片段扩展，其他社区也在试验 Elyra。

**下载:**在过去的几周里，我们也看到了 Elyra npm 包下载量的增长，我们的周下载量在 60k 到 70k 之间浮动。

**企业中的 Elyra**:Elyra 的组件集成在 IBM Cloud Pak 中，可用于数据和 Watson Studio 产品。

**总结**

Elyra 1.0.0 建立在 Jupyter Notebooks 基础上，是数据科学家、机器学习工程师和人工智能开发人员的事实上的工具，为 JupyterLab 提供了一套以人工智能为中心的扩展，旨在帮助用户解决模型开发生命周期的复杂性，使 JupyterLa <wbr> b 对人工智能从业者来说更好。

我们希望您能参与到[Elyra 项目]([https://github.com/elyra-ai/<wbr>Elyra/](https://github.com/elyra-ai/elyra/))中来。阅读我们的[投稿指南]([https://elyra.readthedocs.io/<wbr>en/latest/index . html](https://elyra.readthedocs.io/en/latest/index.html))，如果你有问题，对新功能有建议或者报告任何 bug，就创建新的问题。我们也欢迎通过 GitHub pull 请求投稿。