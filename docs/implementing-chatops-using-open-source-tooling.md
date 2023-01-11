# 使用开源工具实现 ChatOps

> 原文：<https://devops.com/implementing-chatops-using-open-source-tooling/>

ChatOps 是组织运营沟通的一个令人兴奋的提议。在聊天对话中加入开发和操作工具可以简化开发流程，增加透明度，并通过简化 bug 检测和修复工作来提高安全性。

ChatOps 的核心是机器人、脚本和聊天客户端；许多都是预建的和开源的。在本文中，我们将回顾一个完全开源的构建 ChatOps 设置的方法。我们将介绍与 Hubot 集成、使用 CoffeeScript 命令，以及构建定制脚本如何在您自己的环境中启动 ChatOps。

## 为什么要为 ChatOps 开源？

关于开放源码的好处，已经有很多争论。基于开源的构建本质上避免了供应商锁定，实现了更高的安全性和服务寿命。此外，为了避免重新发明轮子，分叉现有的开源 ChatOps 项目自然会比纯粹的绿地项目更有效。

## 开源聊天机器人

有很多聊天机器人可供使用；每一种都有独特的功能，不同类型的现成集成，以及使用定制脚本扩展功能的不同方式。以 Lita 为例，这是一个用 Ruby 构建的开源聊天机器人。它可以与 IRC、HipChat 和 Campfire 一起使用。还有许多其他开源聊天机器人选项存在，比如 T2、错误机器人、T4、贾维斯和拉兹洛。

### 例如:Hubot

到目前为止，最受欢迎的开源 ChatOps 伙伴是 Hubot。Hubot 由 Github 设计并开源，在 ChatOps 讨论中占据市场份额。Hubot 被描述为“一个可定制的生活改善机器人”，它是用 Node.js 编写的，并通过 CoffeeScript 接受命令。

使用 Hubot，开发人员可以使用 [Hubot 脚本](https://github.com/github/hubot-scripts)启动命令，以执行发布图像、翻译语言和与地图集成等操作，还可以启动您最喜欢的 DevOps 云工具的重要命令。完整的脚本目录可以在[这里](https://hubot-script-catalog.herokuapp.com/)找到，你也可以很容易地编写自己的 CoffeeScript 命令。

### Hubot 脚本示例

支持 Hubot 的社区脚本同样是开源的，这意味着您可以重新打包这些实现以满足自己的需求。让我们浏览一下 Github 支持的 Hubot 脚本目录,看看我们可以向 Hubot 环境无缝添加什么样的预构建扩展。

有了 Hubot，你可以 ping 通你的主要云开发平台，比如 [Heroku](https://github.com/github/hubot-scripts/blob/master/src/scripts/heroku-status.coffee) 。在 Heroku 上返回问题状态的一些示例命令包括:

```
 hubot heroku status - Returns the current Heroku status for app operations and toolshubot heroku status issues &lt;limit&gt; - Returns a list of recent &lt;limit&gt; issues (default limit is 5)hubot heroku status issue &lt;id&gt; - Returns a single issue by ID number
```

或者，您可能希望方便地从您的聊天客户端检查 PagerDuty，以查看您的事件响应团队中谁在待命，或者收集当前事件的详细信息。Hubout 有一个脚本。使用[page duty . coffee](https://github.com/github/hubot-scripts/blob/master/src/scripts/pagerduty.coffee)，一些示例请求可能是:

```
 hubot who's on call - return the username of who's on callhubot pager me trigger &lt;msg&gt; - create a new incident with &lt;msg&gt;hubot pager me incidents - return the current incidentshubot pager me notes &lt;incident&gt; - show notes for incident #&lt;incident&gt;hubot pager me problems - return all open incidents
```

另一个例子是与 Twilio API 直接交互来发送 SMS。使用 [sms.coffee](https://github.com/github/hubot-scripts/blob/master/src/scripts/sms.coffee) 您可以使用以下语法启动一个命令:

```
 hubot sms &lt;to&gt; &lt;message&gt; - Sends &lt;message&gt; to the number &lt;to&gt;
```

配置 sms.coffee 很容易，您只需要插入:

```
 HUBOT_SMS_SIDHUBOT_SMS_TOKENHUBOT_SMS_FROM
```

当然，也不乏 gif、猫迷因和其他脚本来为你的工作日添加一些幽默，比如使用图像检测的[小胡子插入](https://github.com/github/hubot-scripts/blob/master/src/scripts/auto-stache.coffee)。

## 生成您自己的 Hubot 脚本

除了使用第三方脚本，你也可以自己编写脚本。要成为一个可执行的 Hubot 脚本，你的代码必须在`.coffee`或者`.js`中，并且必须在正确的目录中(默认为 src/scripts 和 scripts)。它还必须导出一个函数，如下所示:

```
 module.exports = (robot) -&gt;# your code here
```

本质上，Hubot 监听所有聊天交流；它会听到命令并做出相应的反应。要配置它必须监听与您的脚本相关的内容，您必须指定要监听的内容以及要响应的内容。例如:

```
 module.exports = (robot) -&gt;robot.hear /badger/i, (res) -&gt;# your code hererobot.respond /open the pod bay doors/i, (res) -&gt;# your code here
```

更多详情，请参见处的[脚本文档。](https://hubot.github.com/docs/scripting/)

## 充分利用聊天机器人

一旦集成到 Slack 这样的聊天平台中，你的聊天机器人配置就可以真正发展壮大。考虑到社区生成和 Github 维护的脚本的广泛性，DevOps 团队有无限的潜力将他们的工具整合到一个单一的、人类可读的 CLI 中。为这类项目选择开源工具的另一个好处是，您可以分离您的 bot，并与您喜欢的任何聊天客户端集成。

ChatOps 可以为远程工作空间增添乐趣和效率。我们已经介绍了在您的团队空间中采用这种技术的高级方法，并且希望为简化 ChatOps 的功能提供一个有用的基础。

— [比尔·多菲尔德](https://devops.com/author/bill-doerrfeld/)