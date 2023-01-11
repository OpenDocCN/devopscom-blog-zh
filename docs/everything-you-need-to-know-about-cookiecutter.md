# 关于 Cookiecutter 你需要知道的一切

> 原文：<https://devops.com/everything-you-need-to-know-about-cookiecutter/>

[Cookiecutter](http://cookiecutter.io) 是一个模板库，用于以任何[编程语言](https://devops.com/?s=programming+languages)创建项目样板。当个人、团队和组织创建项目时，他们必须遵循一致的标准，以便这些项目易于阅读和搜索。模板也加速了代码编写过程，因为开发人员可以在设置上花费更少的时间，并且可以直接进入实际的实现。

Cookiecutter 是一个 Python 包，使用 pip 或其他包管理器可以轻松地 [安装](https://cookiecutter.readthedocs.io/en/2.0.2/installation.html) 。它使您能够为微服务和其他软件项目创建和使用模板。它是一个命令行工具，使用起来不需要 Python 知识。Cookiecutter 广泛应用于软件工程师、研究人员、数据科学家和其他技术角色。

创建一个模板很简单，需要更新一个cookiecutter . JSON*文件。使用模板需要在适当的目录下运行 cookiecutter 命令来创建一个新项目。*

*这里有一个由 Cookiecutter 团队维护的 Python 包的 [示例模板](https://github.com/audreyfeldroy/cookiecutter-pypackage) 。要使用该模板，首先安装 Cookiecutter，然后在终端中运行以下命令:*

*cookiecutter https://github . com/au Rey field Roy/cookiecutter-pypackage . git*

*浏览一系列提示，然后*瞧*！几分钟后，您就有了一个功能完整的 Python 包的框架。将模板换成其他东西，你就可以轻松地在你最喜欢的云服务上运行一个移动应用、一个数据科学笔记本或任何其他项目。有一整个社区有 [成千上万的模板](https://github.com/search?q=cookiecutter&type=Repositories) 可供选择。*

*创建自定义模板以满足您和您的组织的需求也是简单而强大的。我们将在下面介绍如何做到这一点。*

## *Cookiecutter 是给谁的？*

*Cookiecutter 是为个人，团队和公司标准化他们的项目开发过程，并加快新项目的创建。*

*示例用例包括:*

*   ***学习新框架** : Cookiecutter 降低了不熟悉特定框架的开发人员的入门门槛。您可以为您正在学习的框架找到专家模板，并快速开始使用已知有效的配置。*
*   ***入职**:标准化让协作变得更加易于管理。新团队成员可以立即遵循最佳实践，而没有复制、粘贴和尝试编辑正确变量的风险。*
*   *在组织中实施标准:一致的文件夹、文件命名约定和其他模式使得大型团队能够维护一个有组织的代码库。*

## *Cookiecutter 功能*

### *模板*

*模板的核心是 cookiecutter.json 文件，它可能看起来像这样:*

*`{`*

*“全名”:“爱丽丝曲奇”，*

*“邮件”:“[【邮件受保护】](/cdn-cgi/l/email-protection)”，*

*“项目名称”:“Django 样板文件”，*

*【版本】:“0.1.0”*

*}*

*这些键值对决定了开发人员在使用模板时需要回答的提示。命令行界面遍历按键，提示开发人员设置各种参数。如果开发人员没有指定某些内容，Cookiecutter 将使用默认值。*

*模板需要有值得复制和重用的文件和目录，比如特定框架的框架代码。Cookiecutter 使用这些输入来修改模板。为了将这个样板文件连接到输入，Cookiecutter 使用了 [Jinja2](https://palletsprojects.com/p/jinja/) 模板语言。使用 Jinja2，Cookiecutter 识别文本 `{{cookiecutter.variable_name}}` 的所有实例，并用变量的实际值替换样板文件。这既适用于文件内部，也适用于文件名和目录名。*

### *循环和条件逻辑*

*Jinja2 非常强大，它能做的不仅仅是文本替换。它带有 [控制结构](https://jinja.palletsprojects.com/en/3.0.x/templates/%23list-of-control-structures) ，包括 for 循环和 if 语句。它甚至有类似于编程语言中函数的宏。因为 Cookiecutter 的所有模板都使用 Jinja2，所以它可以利用相同的控制流特性。这带来了巨大的可能性。例如，您可以提示开发人员指定他们正在为哪些设备类型构建应用程序，并根据响应具有独特的行为。*

### *钩住*

*[前/后生成钩子](https://cookiecutter.readthedocs.io/en/2.0.2/advanced/hooks.html) 让您在生成项目之前和/或之后运行 Python 或 shell 脚本。来自模板提示的输入在钩子中是公平的，其工作方式与 Jinja2 语法在项目中的其他地方相似。这意味着您可以运行一个脚本来验证开发人员对提示的响应。钩子的其他应用包括清理不需要的文件或者使用逻辑，而仅仅使用 Jinja2 会使这些变得复杂。*

## *有哪些局限性？*

*从设计上来说，模板是关于项目设置的规定，提供了上面讨论的各种优势。另一方面，模板可能会固执己见，既不符合个人开发人员的偏好，也不符合组织的偏好。在这种情况下，可能值得选择另一个模板或修改现有的模板。在没有意义的情况下强制使用模板是不太理想的。*

## *有哪些替代或扩展？*

### *特定框架的样板文件*

*虽然 Cookiecutter 几乎与任何框架兼容，但有些框架确实有现成的定制样板文件。例如，如果你要启动一个 React 应用程序，有一个 [很好的样板](https://github.com/react-boilerplate/react-boilerplate) 可以作为起点，其他社区也经常保持类似的入门方式。样板文件与 Cookiecutter 并非不兼容，您也可以从流行的样板文件中找到您可以使用的模板。*

### *[Cruft](https://cruft.github.io/cruft/) 保持模板有序*

*与任何新的过程一样，使用 Cookiecutter 保持有组织性会有一些开销。当一个团队开始管理几十个甚至更多的模板时，保持模板最新就显得尤为重要。Cruft 与 Cookiecutter 一起工作，不仅制作项目，还随着模板的发展更新现有的项目。Cruft 还具有模板验证功能，以确保项目与模板的最新版本相匹配。*

## *了解关于 Cookiecutter 的更多信息*

*Cookiecutter 社区有很多资源可以帮助你深入挖掘。*

*   *[cookiecutter . io](http://cookiecutter.io)*
*   *[官方文件](https://cookiecutter.readthedocs.io/en/2.0.2/)*
*   *[模板](https://www.cookiecutter.io/templates)*
*   *[](https://github.com/cookiecutter/cookiecutter)*