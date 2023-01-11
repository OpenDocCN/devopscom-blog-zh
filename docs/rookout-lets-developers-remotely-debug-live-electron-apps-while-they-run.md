# Rookout 允许开发者在运行时远程调试实时电子应用程序

> 原文：<https://devops.com/rookout-lets-developers-remotely-debug-live-electron-apps-while-they-run/>

特拉维夫——2018 年 7 月 17 日—[快速生产调试公司 Rookout](https://www.rookout.com/) 今天宣布了其电子远程现场调试解决方案。内置工具让软件工程师能够从终端用户机器上的实时电子应用程序中全面了解数据和代码上下文，而不是依赖于本地测试。

Electron 是为 Windows、MacOS 和 Linux 构建桌面应用程序的最流行的框架之一。它最初由 GitHub 创建，也被 Slack、Discord 和 WordPress 等领先供应商用来制作功能更丰富的基于浏览器的 web 应用程序的桌面版本。电子应用程序建立起来很快，通常要经过许多快速部署才能直接应用到最终用户的电脑上。

尽管电子是基于网络技术，但它不得不面对桌面软件的挑战；每个用户的计算机都有自己独特的“生产环境”，这使得故障诊断变得棘手，尤其是在远距离的情况下。电子应用程序经常与用户系统上的设备交互，如网络摄像头、麦克风或更多外来输入，增加了异常错误的可能性。

传统上，调试电子应用程序意味着依赖用户的错误报告和异常管理工具来报告问题，然后试图在开发人员的本地计算机上重建生产环境。不过，通常情况下，不寻常的问题不会重现，这使得确定原因非常困难。

使用 Rookout，软件团队可以从最终用户的计算机上实时运行的电子桌面应用程序中获得调试器级别的可见性。通过 Rookout 的 IDE，开发人员可以远程设置不间断的“断点”，以查看实时应用程序的完整状态或代码执行过程中任何时间点的任何变量状态，而应用程序照常运行。

Rookout 的解决方案意味着软件公司可以现场和远程调试他们的电子应用程序。他们可以通过 Sentry 这样的异常管理器(Rookout 也可以向 Sentry 本身发送警报)获得问题警报，使用 Rookout 在创纪录的时间内跟踪实时软件中的问题，然后像往常一样开发并推出修复程序，而无需在最终用户的计算机上安装任何额外的软件或派任何人到现场。

Rookout 首席执行官兼联合创始人 Or Weis 表示:“像 Electron 这样的终端用户软件必须在数百万个不同的生产环境中运行。“再加上非常快速的部署周期，很难确切了解单次安装中发生了什么或重现了一个外来的错误。Rookout 为 electronic 带来了即时可见性，让开发人员只需点击几下鼠标，就可以前所未有地深入了解终端用户计算机上应用程序的完整状态。”

Aidoc 是一家为分析医学图像提供医疗保健人工智能解决方案的公司，它使用一种基于电子的应用程序向医生提供他们的解决方案。

“Aidoc 的应用程序运行在医院的本地网络上，不会不断地将数据发送回我们的服务器，所以为不同大陆的客户跟踪漏洞并不总是很容易，”Aidoc 的 R&D 副总裁盖伊·雷纳说。

“Rookout 使得无需花费数小时收集日志和尝试模拟特定医院网络的独特真实环境就能找到漏洞”。

Rookout 首席技术官兼联合创始人 Liran Haimovitch 表示:“桌面软件是无法在生产中真正调试的典型例子，因为每次安装都是不同的。“能够远程调试实时电子应用程序意味着开发人员可以快速找到并修复错误，从而释放 R&D 的资源来开发新功能。”

**关于 Rookout**

Rookout 是快速生产调试解决方案，它根据需要从实时代码中收集数据，并将其立即传输到任何目的地，如警报和监控工具。

借助 Rookout 的实时工具技术，公司无需编码、重新部署或重启应用程序，就能解决 bug 和问题。Rookout 目前支持所有云环境中的 Python、JVM 和 NodeJS，包括无服务器应用程序。