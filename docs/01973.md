# Cameyo 引入了 RDP 端口屏蔽技术，以保护远程服务器免受暴力攻击和勒索软件，进一步简化云迁移

> 原文：<https://devops.com/cameyo-introduces-rdp-port-shield-technology-to-protect-remote-servers-from-brute-force-attacks-and-ransomware-further-easing-cloud-migration/>

***公司还发布了一款免费的开源 RDP 监控工具，帮助所有组织识别其环境中的攻击***

**北卡罗来纳州卡里——2019 年 9 月 18 日——**[Cameyo](http://cameyo.com)，云原生虚拟应用交付平台，将任何 Windows 应用从浏览器带到任何设备，今天推出了其新的 [RDP 端口盾](https://cameyo.com/rdp-port-shield/) 安全技术，以主动保护客户免受整个行业 RDP 漏洞急剧增加的影响，包括暴力攻击和勒索软件。为了让所有组织在使用 RDP 或 Citrix 时能够获得更多关于其网络潜在威胁的数据，Cameyo 还发布了一款免费的开源 RDP 监控工具—[RDPmon](https://cameyo.com/rdp-monitoring/)——任何组织都可以使用它来识别其环境中发生的 RDP 攻击。通过帮助组织识别和主动防范这些威胁，Cameyo 寻求通过帮助缓解相关的安全问题来进一步简化云迁移。

2019 年，勒索软件和暴力攻击急剧增加，最新的 [迈克菲实验室威胁报告](https://www.mcafee.com/enterprise/en-us/assets/reports/rp-quarterly-threats-aug-2019.pdf) 显示，勒索软件在 2019 年第一季度增加了 118%，并且越来越多地通过暴力攻击获得访问权限，以开放和暴露远程接入点，如 RDP。Cameyo 自己对暴力攻击的研究显示，目前平均每台联网服务器每周面临 15 万次暴力触发的密码尝试。

***动态保护用 RDP 端口屏蔽***

为了保护客户免受这些基于 RDP 的漏洞的影响，Cameyo 的 RDP 端口防护是同类产品中第一个内置的安全技术，它可以自动对整个世界关闭 RDP 端口，然后根据白名单中的 IP 地址，仅在需要时动态地专门为经过身份验证的用户打开和关闭这些端口。Cameyo RDP 端口防护通过 Windows 防火墙在服务器上实时创建和管理 RDP 白名单规则。

企业战略集团(ESG)高级分析师 Mark Bowker 表示: “随着企业采用云技术，并以虚拟桌面和虚拟应用交付技术的使用案例为目标，为其用户提供关键应用的访问，他们面临着将 RDP 港口向世界开放的风险，从而产生了导致暴力攻击和勒索软件的漏洞。“Cameyo 的 RDP 安全方法扩展并强调了他们对确保客户网络、数据和用户安全的承诺。”

***可见性对于所有拥有开源 RDPmon 的***

为了帮助每个组织更好地监控和识别其环境中的暴力攻击，并帮助抵御勒索软件，Cameyo 还发布了一款名为 RDPmon 的免费开源工具。RDPmon 为整个行业提供了一个强大的免费工具来监控攻击，以便 IT 专业人员可以快速识别和了解这些威胁，从而提供缓解问题所需的关键数据。

任何组织都可以从 GitHub 免费下载开源的 RDPmon 并安装在 RDS/cloud 服务器上。快速指导配置后，IT 管理员将获得两个视图:

*   一个标签，显示尝试连接到其服务器的总次数
*   标识每个服务器上正在使用的应用程序、使用 RDP 的人数以及每个用户正在使用的程序的标签。

RDPmon 还将提供对服务器上正在使用的任何非故意或未经批准的软件的洞察。RDPmon 收集的所有信息都是完全保密的，因为它保留在用户环境中——Cameyo 无法访问任何数据。

Cameyo 的联合创始人兼首席执行官 Andrew Miller 说:“各种规模的组织在数字化转型的道路上都面临着无数的障碍，围绕云迁移的安全问题——尤其是在 RDP 攻击事件急剧增加的情况下——是每个行业的高管们最关心的问题。“Cameyo 明白，虚拟应用交付的生产率提高不能以安全性为代价，我们从头开始构建 Cameyo 平台，以保护我们的客户及其用户。我们创建了 RDPmon，因为我们相信，识别您环境中与 RDP 相关的漏洞的能力应该免费提供给所有人。RDP 港盾只是我们最新的安全进步，因为我们不断保护我们的客户免受不断变化的威胁。”

***定价和供货***

[Cameyo RDP 港盾](https://cameyo.com/rdp-port-shield/) 技术已经向 Cameyo 平台的所有用户铺开。Cameyo 客户无需采取任何措施即可使用该功能，该功能现已对该平台的所有用户开放，并且免费提供。开源的 RDPmon 工具可以在[https://cameyo.com/rdp-monitoring/](https://cameyo.com/rdp-monitoring/)免费下载，源代码可以在 GitHub 的[https://github.com/cameyo/rdpmon](https://github.com/cameyo/rdpmon)下载。

**关于 Cameyo**

Cameyo 是一个云原生虚拟应用交付平台，支持从任何浏览器向任何设备安全交付 Windows 桌面应用。随着组织追求数字化转型，他们在向云迁移的过程中遇到了一个常见的障碍，即无法从云中交付传统的 Windows 应用程序。Cameyo 解决了这个问题，它让每个人都可以在任何设备上从任何 HTML5 浏览器无缝访问他们的 Windows 生产力应用程序。数百家企业和组织利用 Cameyo 的虚拟应用交付平台向全球数万名用户交付 Windows 应用。要了解更多，请访问 cameyo.com。