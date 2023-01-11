# Postman 推出新的 Web 客户端以简化 API 开发

> 原文：<https://devops.com/postman-launches-new-web-client-to-simplify-api-development/>

客户现在可以从网络浏览器访问 Postman，从而更容易地提高 API 开发的速度和范围。

旧金山—2020 年 9 月 2 日— [领先的 API 开发平台 Postman](https://cts.businesswire.com/ct/CT?id=smartlink&url=https%3A%2F%2Fwww.postman.com%2F&esheet=52185411&newsitemid=20200309005161&lan=en-US&anchor=Postman&index=1&md5=c70b661972f820308336437f84cb9f68) 宣布推出 Postman for web，这是 Postman 的一款新浏览器界面，可为用户提供简化的访问和卓越的协作。这一举动在某种程度上标志着回归邮递员的本源。

“Postman 一开始是一个网页上的 Chrome 插件，然后以惊人的速度转向桌面应用程序，”Postman 首席执行官兼联合创始人 Abhinav Asthana 说。“我们现在回归网络，利用互联网的全部力量，让 API 开发更快、更具协作性、更具可扩展性。”

**Postman** 上 API 开发的快速增长自 2015 年上线以来，Postman 已经看到[API 请求和收藏数量的巨大增长](https://blog.postman.com/api-growth-rate/)。Postman 现在已经处理了超过**10 亿个 API 请求**，并且 API 集合的数量也有了大幅增长，现在有超过**4800 万个 API 集合**在 Postman 上运行。

这种惊人的增长，以及随之而来的对高规模和高性能 API 开发工具需求的增长，导致了新的 web 版本 Postman 的诞生。

“构建 API 的公司现在希望以五年前根本不可能的方式来提升他们的 API 开发过程的速度和范围。Asthana 说:“网络邮差是满足这些需求的理想解决方案。

**网络邮差** 直到今天，邮差用户都是通过桌面应用程序访问邮差。通过浏览器访问 Postman 是用户要求最多的功能之一；他们说，下载桌面应用程序会减慢入职速度，还会让你很难保持最新版本。此外，浏览器方法允许某些协作功能，这在应用程序中是不可能的。Postman 的 web 版本通过提供以下功能解决了所有这些问题:

*   **简化的用户访问和登录:**用户无需安装应用程序即可通过浏览器进行即时访问、自动更新，并且用户登录速度更快(即只需粘贴网址即可登录)。
*   **通过深度链接优化协作:**现在，Postman 在 web 上，Postman 中的所有内容都有一个 URL，因此用户可以轻松地将 URL 共享到粒度 API 元素，以实现卓越的协作。
*   **从浏览器大规模发送请求的能力:**由 Postman 工程师独家开发的独特代理架构(详见下文)有助于从浏览器可扩展地发送 API 请求。

试试网页版的邮递员[这里](https://go.postman.co/build)。

**邮差代理** 紧紧连接着邮差为 web 客户端启动的是邮差代理。该代理是专门为克服浏览器的跨源资源共享(CORS)限制而设计的，允许从浏览器界面可扩展地发送 API 请求。通过创建一个代理微应用程序来促进大规模的 API 请求发送，代理以一种前所未有的方式克服了浏览器的挑战。

“Postman 在构建出色的浏览器体验时面临的一个基本限制是 CORS 限制，这使得它无法从浏览器大规模发送 API 请求；这种限制最终是为什么 Postman 决定首先建立一个桌面应用程序，”Postman 首席福音传道者 Kin Lane 说。“邮递员代理是该公司的一项重大技术突破，它克服了基于浏览器的应用程序的一个基本限制，这些应用程序需要大规模连接到 API。”

点击了解更多关于创建邮递员代理[的细节。](https://blog.postman.com/introducing-the-postman-agent-send-api-requests-from-your-browser-without-limits/)

**桌面和 web 上的高性能 API 开发** 随着 API 开发的规模和范围迅速增加，Postman 团队一直在不断努力为每个用户提高 Postman 的性能。下面的图表(表 1)显示了桌面应用程序和 web 版本的 Postman 的这些性能增强的示例。

(表 1)

|  | **Postman desktop****v7.18.0****(2020 年 2 月)** | **Postman desktop****v7.28.0****(2020 年 8 月)** | **Postman on the web****(2020 年 8 月)** |
| 开业邮递员 | 6.5 秒 | 4.5 秒 | 3.2 秒 |
| 加入团队工作区 | 大约 5 秒 | 大约 2 秒 | 大约 2 秒 |
| 在繁忙的团队工作区恢复工作 | 大约 5-10 秒 | 大约 3 秒 | 大约 3 秒 |
| 切换工作空间 | 大约 5 秒 | 大约 2 秒 | 大约 2 秒 |
| 使用多个工作空间时的内存使用情况 | 350MB – 1150MB | 130MB – 430 MB | 130 MB – 430 MB |
| 在活动工作空间中键入 URL | 300-800 毫秒 | 60 毫秒 | 60 毫秒 |
| 打开新标签页 | 300 毫秒 | 100 毫秒 | 100 毫秒 |
| 在边栏中搜索 | 500 毫秒 | 50 毫秒 | 50 毫秒 |
| 打开环境快速查看 | 60 毫秒 | 25 毫秒 | 25 毫秒 |
| 下载大量回复 | 30 兆字节 | 高达 150 MB | web 上尚未启用的功能 |

**关于邮递员**

Postman 是领先的 API 开发协作平台，被全球超过 1200 万开发人员和 500，000 家公司使用。Postman 是一个优雅、灵活的平台，用于通过 API 快速、轻松、准确地构建互联软件。Postman 的总部设在旧金山，在公司成立地班加罗尔设有办事处。Postman 是一家私人控股公司，资金来自 Insight Partners、Nexus Venture Partners 和 CRV。在[http://www.postman.com](https://cts.businesswire.com/ct/CT?id=smartlink&url=http%3A%2F%2Fwww.getpostman.com%2F&esheet=52185411&newsitemid=20200309005161&lan=en-US&anchor=http%3A%2F%2Fwww.postman.com&index=7&md5=90bbbd3bd5d661afa0745c158ac50103)了解更多信息，或通过@getpostman 在 Twitter 上联系 Postman。