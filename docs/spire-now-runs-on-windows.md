# SPIRE 现在在窗户上运行！

> 原文：<https://devops.com/spire-now-runs-on-windows/>

在其核心， [SPIRE 项目](https://github.com/spiffe/spire/) 旨在解决大规模安全发布工作负载标识的问题，无论工作负载在哪里运行。它通过一个由插件组成的可扩展架构来实现这一点，该架构允许 SPIRE 根据支持不同平台、云提供商等的需求而增长。到目前为止，SPIRE 只能部署在 Linux 平台上。但是现在，随着 SPIRE 1.3.0 中新的实验性 Windows 支持，这已经成为过去！

## 正在引入哪种支持？

这些年来，SPIRE，一个已经可以生产的 [SPIFFE](https://spiffe.io/) 标准的实现，已经在 Linux 平台上获得了高度的成熟度。在 SPIRE 如何部署、操作和集成到各种 Linux 环境方面，我们学到了很多。

Windows 支持正在作为一个 [实验性功能](https://github.com/spiffe/spire/blob/main/doc/upgrading.md#experimental-features) 逐步引入。我们预计，随着 Windows 操作体验的发展，将需要引入影响用户体验或功能的变化。在接下来的几个 SPIRE 版本中，我们将努力填补空白并稳定 Windows 支持。

1.3.0 版本增加了对在 Windows 上运行 SPIRE 服务器和代理的支持。现有的插件已经适应了 Windows 下的工作，如果适用的话。此外，还添加了一个新的特定于 Windows 的工作负荷证明者(类似于现有的 Unix 工作负荷证明者)，用于为 Windows 工作负荷提供特定于 Windows 的属性。

## 有什么区别？

SPIRE 项目的一个指导原则是力求易用和直观的配置。考虑到这一点，在 Windows 上运行 SPIRE 感觉与在 Linux 上运行非常相似。配置差异仅限于使用平台特定功能的领域(例如，Unix 域套接字、命名管道等)。

## 我们面临的工作

在额外的操作系统上支持 SPIRE 并非易事。正如我们所指出的，SPIRE 在 Linux 平台上的成熟度和稳定性在过去几年里一直在增长。我们知道，我们将需要跨几个版本工作，以提供与我们今天在 Linux 平台上所拥有的相似级别的特性。我们在多个方面还有很多工作要做:

*   [sp iffe 工作负载端点](https://github.com/spiffe/spiffe/blob/main/standards/SPIFFE_Workload_Endpoint.md) 标准尚不支持将工作负载 API 公开为命名管道端点。我们将与 SPIFFE[SIG Spec group](https://github.com/spiffe/spiffe/tree/main/community/sig-spec)密切合作，更新规范，使 sp iffe 实现者(如 SPIRE)可以使用命名管道来服务和消费工作负载 API 的方式标准化。
*   Windows 上尚不支持 K8s 工作负载证明器插件，原因是对我们用来证明基于 K8s 的工作负载的关键 K8s 功能的支持存在差异。我们正在积极研究替代方法来证明在 K8s 中运行的 Windows 工作负载。
*   虽然 go-spiffe 库已经更新到支持在 Workload API 中使用命名管道，但其他语言库还没有。这部分是由于 C/C++ gRPC 库中缺乏对命名管道传输的支持。我们有工作要做来提供这种支持，这可能包括与生态系统中的其他人合作来开发和上游必要的库更改，如 gRPC。

## 我们希望收到您的来信

虽然对 Windows 的支持是非常新的，但我们已经与感兴趣的社区成员合作来设计和验证当前的功能集。SPIRE 已经在测试环境中运行，并计划部署到数千台 Windows 主机上。这一早日通过已经并将继续是稳定我们支持的组成部分。我们非常渴望从社区和早期采用者那里了解更多信息，了解我们如何更好地支持为在 Windows 环境中运行的工作负载提供安全的服务身份。

如果您对这项新支持有任何要求或想说什么，我们希望听到！请不要犹豫，在 [GitHub 资源库](https://github.com/spiffe/spire/issues) 中提出问题，询问特性或报告错误。还有，你可以加入 Slack 上的牛逼 SPIFFE 社区:[https://slack.spiffe.io/](https://slack.spiffe.io/)。我们很乐意回答您的问题并讨论您的请求。最后，如果你想获得该项目的最新消息，加入 SPIFFE Announce 邮件组，这是一个低频率的项目公告列表:[https://groups.google.com/a/spiffe.io/g/announce](https://groups.google.com/a/spiffe.io/g/announce)。