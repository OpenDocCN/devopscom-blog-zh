# Lightstep 宣布了新的 GitHub 动作，将可观测性数据直接引入 GitHub，以避免部署有问题的代码

> 原文：<https://devops.com/lightstep-announces-new-github-action-bringing-observability-data-directly-to-github-to-avoid-problematic-code-deploys/>

*   GitHub Actions 通过在开发人员编码和协作拉请求的同一个地方自动化任务，使开发人员的工作流程现代化
*   Lightstep 将在现有的 GitHub 工作流中显示相关的可观察性数据，以确保开发人员交付高质量的软件

cdCON——2020 年 10 月 7 日——由前谷歌工程师创立的前沿分布式追踪工具 Lightstep 今天宣布了他们新的 GitHub 行动，名为 Lightstep 预部署检查。通过自动将相关的可观察性数据直接引入 GitHub 上的开发工作流，软件开发人员可以在软件实际部署之前确保其质量和性能。

Lightstep 的联合创始人兼首席技术官丹尼尔·斯普恩豪尔(Daniel Spoonhower)说:“这是开发人员对可观测性的看法的一次重大转变。“DevOps 就是要承认，发布代码而不担心它在现实世界中的表现是不够好的。我非常相信‘你构建它，你拥有它’——但我也相信，我们需要尽可能地将解决方案融入现有的开发工作流，尽可能地实现自动化，从而使这一点变得更容易。”

根据 OverOps 发布的《2020 年软件质量状况报告》,三分之二的开发人员每周至少花一天时间来排查他们代码中的问题，并对将新代码部署到基于云的分布式架构中所带来的未知感到沮丧。尽管根据 GitHub 的年度 Octoverse 报告，有 8700 多万个合并的 pull 请求，但迄今为止，pull 请求中对系统健康状态的可见性为零。

GitHub 的 GitHub Actions 产品经理克里斯·帕特森(Chris Patterson)表示:“在部署可能影响生产系统和服务的代码之前，自动确认生产系统和服务是确保可靠性的重要一步，同时不会影响开发速度。“通过将可观察性数据直接引入 GitHub 上的 pull 请求流程，开发人员可以避免上下文切换，获得对其代码在生产中如何执行的更多所有权，并更好地支持其组织内的开发运维。”

Lightstep 预部署检查利用 Lightstep 的公开可用 API，在代码更改进入生产环境之前提供部署风险摘要。然后，通过 GitHub 动作，来自风险评估的信息被自动直接拉入 GitHub pull 请求。

Lightstep 还与 Rollbar 和 PagerDuty 合作，将更多信息直接引入 GitHub。例如，如果 Lightstep 完成了风险评估并确定系统不健康，它可以自动实时拍摄生产行为的快照并将其发送到 PagerDuty，这样即使问题开始时开发人员不在，也可以检查问题的完整细节。

“我们看到了 Lightstep 预部署检查对开发人员效率的直接价值，”Pagerduty 战略生态系统开发高级总监 Steve Gross 说。“现在，开发人员在一个屏幕上就可以轻松获得拉取请求中的寻呼值班呼叫详细信息，以及系统运行状况详细信息。”

关于 Lightstep

Lightstep 的使命是为那些开发、操作和依赖当今强大的软件应用程序的人提供大规模的信心。其产品利用分布式跟踪技术——最初由谷歌的 Lightstep 联合创始人开发——为大规模采用微服务或无服务器的组织提供最佳的可观察性。Lightstep 由 Redpoint、Sequoia、Altimeter Capital、Cowboy Ventures 和 Harrison Metal 提供支持，总部位于 San

加利福尼亚州弗朗西斯科。欲了解更多信息，请访问[https://lightstep.com](https://lightstep.com/)或关注@LightstepHQ