# 一个德沃普斯的蜕变回响在 Reverb.com，第二部分

> 原文：<https://devops.com/devops-metamorphosis-echoes-reverb-com-part-two/>

[上一次](https://devops.com/features/devops-metamorphosis-echoes-reverb-com-part-one/)，亲爱的读者，我们发现了 Reverb.com 电子商务平台如何连接想要购买和销售设备的音乐人，寻求自动化其工作流程软件开发过程，加速部署和错误修复，同时满足想要在尽可能高效和无错误的在线环境中交易的客户。现在，关于 Reverb.com 如何采用 DevOps 来实现其目标的结论。

Reverb.com 裁谈会进程的一次往返旅行

如今，Reverb.com 将 DevOps 的理念集中在开发流程上，让主厨[https://www.chef.io/chef/]负责配置管理，让詹金斯[https://www.cloudbees.com/jenkins/about]负责持续交付和基础设施自动化任务。开发人员使用 Capistrano[http://capistranorb.com/]来推出新的代码更改和运行数据库迁移，circle ci[https://circleci.com/]用于单元测试代码，DataDog[https://www.datadoghq.com/]用于度量和监控。“我们还将 Logstash [http://logstash.net/]、elastic search[http://www . elastic search . com/about/]和 Kibana 一起用于日志聚合和可视化，”Reverb.com 高级基础设施工程师 Adam Enger 说。

在 Reverb.com 的一个典型部署中，一名工程师在 Jenkins 中点击 build 按钮，这触发了一个 Chef 在所有 web heads 上的聚合。这将推出开发人员计划进行的任何配置更改，如 NGINX 配置更新或 app config 更新。

完成后，系统会通知应用程序执行零停机部署，在该部署中，应用程序会重新加载，而不会丢弃任何请求。“如果该过程成功完成，Jenkins 将使用 Capistrano 开始代码部署，同时将新代码部署到我们的 web 应用服务器。Enger 说:“如果计划运行数据库迁移，这也将发生在我们的一个工作箱上。

到目前为止，这听起来像是一个标准部署。但这正是 DataDog 和 ELK stack 发挥作用的地方。“这是我们真正从 CD/CI 和 DevOps 中获益的地方，”Enger 说。开发团队每次收敛 Chef，都会使用一个 Chef 处理程序向 DataDog 提交一个事件。一旦 Capistrano 开始和结束，另一个事件将发生在 DataDog。该团队已经配置了 Logstash 来监视 web heads 上的应用程序日志，并在系统出现错误时向 DataDog 发送一个事件。Enger 说:“单点信息现在变成了 DataDog，因为我们可以看到我们的配置和代码变化，并立即知道什么时候会有不好的变化出现。”。

开发团队最后要查看的是 Kibana 中的性能日志，根据生成的日志来查看应用程序的执行情况。“有了 ELK 堆栈，团队可以回答这样的问题:是否有任何 500 错误？如果有，发生的次数和频率是多少？开发增加还是减少了应用程序的响应时间？人们喜欢在/my/feature 推出的新功能吗？恩格尔说。

障碍

迁移到 DevOps 的最大障碍是您必须从传统的系统管理员或开发人员转变为更加基于 DevOps 的心态。这意味着操作方学习编码，而开发方学习负载平衡器。

“如果我们在我们的计算机系统中传播不断的变化，我们也应该期望不断地改变我们的思维模式，以适应新的做事方式，”恩格尔说。

你能看透的好处

透明度是 Reverb.com 开发者从新 CD 方法中获得的第一件事。" Capistrano 告诉 hip chat[https://www . hip chat . com/]"嘿，代码要出了！Enger 说:“我知道在 Kibana 和 DataDog 中调出我的仪表板，以观察任何异常情况。不能总是期望人类能够高效地相互交流。计算机通过程序通知帮助 Reverb.com 团队在整个组织内进行沟通，通知他们何时进行变更。

代码部署现在是可预测的和自动化的。再也不用担心由于连接不良而导致部署失败。“当失败确实发生时，我们能够打开 Jenkins 构建输出并很快找到错误，”Enger 说。

一个惊喜

在实现 CD/DevOps 之后，一个令开发团队惊讶的积极结果是，他们了解了很多关于用户行为和流量模式的信息。“现在我们知道凌晨 4:30 是网站上最慢的时段，”Enger 说。

团队确切地知道何时是推出大的配置或代码变更的最佳时机。他们立即知道部署如何影响用户，尤其是他们是否破坏了站点中的关键路径，如结帐或注册功能。DevOps 提供的自动化方法使他们能够在最初部署的几分钟内修复糟糕的更改。

粉丝反馈的肯定吼声

Reverb.com 最近引入了更多的自动化和监控，以防止网站停机和被机器人滥用。反馈:客户不关心 DevOps 他们关心网站的可操作性和效率。但是是 DevOps 让这一切发生的！