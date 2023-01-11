# 在 YAML 的支持下，木偶潜入更深的 DevOps

> 原文：<https://devops.com/with-yaml-support-puppet-dives-deeper-into-devops/>

Puppet 本周宣布了对 Puppet Enterprise 的更新，增加了额外的 DevOps 功能，包括与 Bolt 的集成，Bolt 是一个开源的无代理任务运行程序，Puppet 使用它来使 IT 管理员更容易实现 IT 自动化。

Puppet 产品副总裁 Matt Waxman 表示，增加与 Bolt 的集成将使集成依赖 YAML 部署应用程序的 DevOps 流程变得更加容易。

Waxman 表示，本月通过 Puppet Enterprise 2019.1 更新推出的 Bolt 提供了一种无代理的自动化方法，使 IT 团队能够在 IT 自动化框架的环境中执行以任何语言编写的现有命令和脚本，该框架旨在供普通 IT 管理员使用。

与此同时，Puppet 正在提供建立管道的能力，以便直接从 Puppet Enterprise 内部部署自动化代码。Puppet 没有建立单独的持续集成/持续部署(CI/CD)平台，而是嵌入了它在 2017 年收购 Distelli 时获得的能力。通过这样做，Puppet 使得加速自动化软件的部署成为可能，这种方式不需要每一个更改都经过主 Puppet 管理员的批准。默认管道通过在不到 30 分钟的时间内建立他们的第一个管道，引导组织开始连续交付实践。

Puppet 还包含了一个影响分析功能，使团队能够在部署之前评估 Puppet 代码变更的影响。

阻碍采用 DevOps 实践的问题之一是大多数 IT 管理员的编程技能有限。Waxman 说，通过提供一个能够在更高抽象层次上操作 YAML 文件的 it 自动化框架，组织应该更容易将 IT 管理员纳入他们想要定义的任何 DevOps 流程集。

通过此次升级，Puppet 还扩展了无代理 Bolt 框架的范围，以支持运行 Cisco NX-OS 和 Cisco IOS 的网络设备，以及 Palo Alto Networks 的防火墙。Waxman 表示，随着网络运营与 DevOps 流程的集成程度越来越高，IT 组织越来越需要能够跨计算、存储和网络平台应用工作流。

许多 IT 组织现在在实现这一目标方面面临的挑战是，每个平台提供商都创建自己的自动化框架，这最终会在整个企业中形成自动化孤岛。从长远来看，Waxman 说，除了调用许多平台已经公开的应用程序编程接口(API ), Puppet 将致力于将特定领域的自动化框架与其跨平台框架相集成。

总体而言，Waxman 表示，Puppet 仍然致力于根据需要自动化的 IT 任务的性质，提供无代理和基于代理的 IT 自动化方法的组合。将由每个 It 组织决定何时采用这些选项中的一个。但是不管选择哪条路，Puppet 显然是想让它的核心自动化平台更容易被每个人使用。

— [迈克·维扎德](https://devops.com/author/mike-vizard/)