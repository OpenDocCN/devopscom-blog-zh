# 通用代码搜索组合

> 原文：<https://devops.com/universal-code-search-combinations/>

*潜在搜索比宇宙中的恒星还多。*

源代码搜索不像在网上搜索文本——它更复杂，有许多细微差别。当我们着手创建一个通用代码搜索引擎时，我们知道有许多排列需要考虑——太多了。所以我们开始猜测我们需要考虑多少种搜索排列。

首先，让我们了解一下什么是通用代码搜索。今天的搜索不仅仅是“Grep and go”现代大代码时代要求代码搜索覆盖多个维度:存储库、文件格式、编程语言等。通用代码搜索将来自许多工具的信息联系在一起，从您的代码主机上的存储库到您的项目之间的依赖关系和应用程序运行时信息，为开发人员提供了一个快速浏览和更好地理解所有代码的单一位置。

通用代码搜索必须满足以下要求:

*   搜索任何主要代码主机上的存储库。
*   搜索所有提交，使当前(最新)和过去的代码库都可以被发现。
*   支持所有编程语言。
*   支持所有主要语言的代码智能。

为了量化通用代码搜索的扩展程度，最佳指标是搜索组合的数量。

开发人员可以搜索超过 18 个维度的代码来导航、探索和理解代码。

## **储存库**

Sourcegraph 可以搜索任何存储库，除了其他源代码版本控制系统之外，还可以搜索所有 Git 提供者。GitHub 托管 [超过 1 亿个储存库](https://github.blog/2018-11-08-100m-repos/) ，所以用一个 [17.31%的市场份额](https://www.datanyze.com/market-share/source-code-management--315) ，我们可以估计有 577，700，751 个可搜索的储存库。

## **提交**

Sourcegraph 可以搜索任何存储库，以及存储库中的任何提交。例如，如果平均每个存储库有五个开发人员在五年内每年 300 天提交五个提交，Sourcegraph 将能够使用**repo:<REPONAME>@<COMMIT>**搜索所有 37，500 个提交。

## **分支机构**

与提交一样，Sourcegraph 可以搜索存储库的所有分支。使用相同的方法，我们可以假设五个开发人员中的每一个在五年内每个月从事五个特性分支的工作。这将导致存储库中的 1500 个分支可以使用**repo:<repo name>@<branch name>**进行搜索。

## **文件类型**

除了其他文本文件，Sourcegraph 还支持所有编程语言和开发人员文件。在 [文本](https://fileinfo.com/filetypes/text) 和 [开发者](https://fileinfo.com/filetypes/developer) 文件之间，我们保守估计这一数字为总共支持 1155 种文件类型。

## **图案类型**

Sourcegraph 允许以三种方式解释您的搜索:字面上，作为正则表达式(regex)或作为结构化搜索模式。 [结构化搜索](https://docs.sourcegraph.com/user/search/structural) 让您匹配更丰富的语法模式，特别是在代码和 JSON 等结构化数据格式中。

## **搜索类型**

允许四种搜索类型 。无论您是否需要在给定时间点搜索所有代码、代码更改或提交消息(diffs 或 commits)，Sourcegraph 都可以让您访问代码库的所有深度，包括过去和现在。*文件* *回购*

## **回购分叉和归档**

在您的搜索中包含存储库分支，或者不包含。包括存储库档案，或者不包括。这些是在 Sourcegraph search 中你的代码库中搜索分叉和归档 的 四个选项。*是，否，仅*

## **案例**

Sourcegraph 搜索支持不区分大小写和敏感搜索。 在执行 diff 或 commit 搜索类型时，您可以使用另外五个过滤器。

## **开发商**

搜索代码的作者或提交者。这是执行比较或提交搜索时的两个选项。

## **时间**

Sourcegraph 支持在一个时间段前后都进行搜索，如 [前:“上周四”](https://sourcegraph.com/search?q=repo:sourcegraph/sourcegraph$+type:diff+author:nick+before:%22last+thursday%22) [后:“6 周前”](https://sourcegraph.com/search?q=repo:sourcegraph/sourcegraph$+type:diff+author:nick+after:%226+weeks+ago%22) 或 [后:“2019 年 11 月 1 日。”](https://sourcegraph.com/search?q=repo:sourcegraph/sourcegraph$+type:diff+author:nick+after:%22november+1+2019%22)

## **消息**

您还可以搜索 diff 和 commit 搜索，其提交消息包含特定的字符串。

## **这里**

[支持四种 IDE 集成](https://docs.sourcegraph.com/integration/editor):VS 代码、Atom、IntelliJ、Sublime Text。这有助于通过减少上下文切换来提高开发人员的生产率。source graph 的 IDE 集成限制在执行结构化搜索、使用过滤器和搜索过去的提交。 因此，上面描述的大部分维度并不适用于 ide。

这意味着什么？ [**2，702，343，531，371，460，001，448**](https://docs.google.com/spreadsheets/d/11gcF6xvEP6Uhe55XoWKF4v00LFB_LXJdbwQrEB9Ruws/edit#gid=0) 跨所有 repos、所有编程语言、所有代码变更、所有文件格式、所有代码宿主的潜在代码搜索。通用代码搜索使探索、导航和更好地理解所有代码变得更容易和更快，无论在哪里。不信？你自己去看看吧。改变假设以符合您的组织。

— [奎恩·斯莱克](https://devops.com/author/quinn-slack/)