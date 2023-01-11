# 新的 Jupyter 笔记本使数据科学家和政策制定者能够分析实时新冠肺炎数据

> 原文：<https://devops.com/new-jupyter-notebooks-enable-data-scientists-and-policy-makers-to-analyze-real-time-covid-19-data/>

新的开源新冠肺炎笔记本提供了一个工具包，帮助开发人员和数据科学家回答关于疫情的重要问题。

**作者** **Frederick Reiss，IBM 开源数据和人工智能技术中心首席架构师**

对于正在分析新冠肺炎效应并试图根据数据制定可行计划的数据科学家和政策制定者来说，信息领域势不可挡。来自调查研究、新闻媒体、社交媒体和卫生组织的数据几乎源源不断，这使得将数据分析成有用行动的任务变得几乎不可能。开发人员和数据科学家需要关于数据源、工具以及如何从不断变化的数据中得出有意义的、统计上有效的结论的问题的答案。

政策制定者面临类似的挑战。美国有 3000 多个县，每个县都有一个独特的故事，讲述新冠肺炎是如何影响其社区的。政策制定者提出的问题包括:总的来说，我们能讲述什么故事？我们在全国范围内看到了什么模式吗？哪些地区或人口受疫情的影响最大？

**开源 Jupyter 笔记本提供可操作的数据**

为了提供帮助，IBM 的开源数据和人工智能技术中心(CODAIT)创建了 [COVID 笔记本](https://github.com/CODAIT/covid-notebooks) ，这是一个帮助开发人员和数据科学家回答关于疫情的重要问题的工具包。我们已经处理了一些比较普通的任务，包括:

*   获取关于疫情当前状态的权威数据
*   清理最严重的数据质量问题
*   将数据整理成易于使用 Pandas 和 Scikit-Learn 等工具进行分析的格式
*   构建一组初始的示例报告和图表

处理这些任务使开发人员和数据科学家能够专注于高级分析和建模任务，而不是担心数据格式和数据清理之类的事情。我们的存储库使用开发人员友好的 [Jupyter 笔记本](https://jupyter.org/) 来涵盖这些初始数据分析步骤中的每一步。

值得注意的是，新冠肺炎的基础数据每天都在变化。当您构建自己的分析时，您会希望经常更新自己笔记本上的结果。但是，重新运行一系列互联笔记本电脑是一项挑战。分析有多个阶段，一个步骤的输出通常会反馈到其他多个步骤。为了简化使用最新数据更新结果的过程，我们使用 [Elyra 笔记本管道可视化编辑器](https://elyra.readthedocs.io/en/latest/getting_started/overview.html#notebook-pipelines-visual-editor) 和 [KubeFlow 管道](https://www.kubeflow.org/docs/pipelines/overview/pipelines-overview/) 创建了数据处理管道。例如，下面是美国县级时间序列数据的管道:

通过这些管道，您只需单击一个按钮，就可以重新运行整个提取-转换-分析工作流。

**权威数据来源**

我们存储库中的工具使用权威来源来获得政策制定者可以用来做出实时关键决策的总体见解。对于美国县级数据，我们的数据提取笔记本从约翰霍普金斯大学系统科学与工程中心(CSSE)的[](https://github.com/CSSEGISandData/COVID-19)新冠肺炎数据仓库下载最新数据。这个数据集是许多与疾病控制中心合作的组织使用的 [预测模型](https://www.cdc.gov/coronavirus/2019-ncov/covid-data/forecasting-us.html) 的主要来源。

我们的笔记本用来自美国 储存库的*纽约时报* [冠状病毒(新冠肺炎)数据(关于罗德岛和犹他州更完整的数据)和纽约报纸*纽约市*](https://github.com/nytimes/covid-19-data) [文摘](https://github.com/thecityny/covid-19-nyc-data) 的 [每日报道](https://github.com/nychealth/coronavirus-data) 的额外数据(关于纽约市的区级数据)填补了这一原始资料中已知的空白。我们的笔记本使用欧洲疾病预防和控制中心关于全球范围内新冠肺炎病例地理分布的数据作为他们在单个国家范围内的数据来源。

笔记本会在运行时下载所有这些数据集，原因有两个。首先，这些数据集每天都在变化。第二，数据集的许可条款不允许商业实体再分发数据。如果您在商业应用程序中使用我们的开源代码，请确保您遵守底层数据的许可条款！

您可以使用我们的代码作为更深入、更有趣的分析的起点。例如，您可能希望分析数据以找出贫困水平和感染率之间的相关性。开源开发人员和数据科学家可以轻松地构建这些工具，将分析扩展到他们各自的用例。

**向开发人员和数据科学家解释所使用的技术**

我们存储库中的笔记本是 [Jupyter](https://jupyter.org/) 笔记本。我们使用常见的 Python 数据科学库，包括 [【熊猫】](https://pandas.pydata.org/)[Numpy](https://numpy.org/)[Matplotlib](https://matplotlib.org/)[seaborn](https://seaborn.pydata.org/)和[scipy . optimize](https://docs.scipy.org/doc/scipy/reference/optimize.html)。

大多数清理和数据分析都是使用 Pandas dataframes 完成的，该框架是数据科学家完成的大多数分析的基础。IBM 也在努力扩展 Pandas 的自然语言处理用例。我们的新冠肺炎时间序列分析笔记本的一部分使用我们的熊猫 [文本扩展](https://github.com/CODAIT/text-extensions-for-pandas) 库中的 [TensorArray 扩展类型](https://github.com/CODAIT/text-extensions-for-pandas) 在熊猫数据帧的单元格中存储时间序列张量。我们的团队还利用了我们作为 [Elyra 项目](https://github.com/elyra-ai/elyra) 的一部分构建的 [图形工作流编辑器](https://elyra.readthedocs.io/en/latest/getting_started/overview.html#notebook-pipelines-visual-editor) ，将我们的笔记本电脑绑定到工作流中，当有新数据可用时，您可以每天运行这些工作流。

**利用开源工具和数据集**

IBM 和我们的团队相信技术民主化的重要性，用最新的数据集和工具激活开发人员，这可以帮助政策制定者为公民的福祉做出最明智的决定。

你可以通过 [开始贡献，使用回购](https://github.com/CODAIT/covid-notebooks) 在你的社区、县和国家建立分析。开发人员和数据科学家也可以通过向我们的 [GitHub 存储库](https://github.com/CODAIT/covid-notebooks) 发出拉请求，直接为用于进行这种分析的工具做出贡献。