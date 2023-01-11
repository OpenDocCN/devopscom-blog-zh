# 公共云安全工具指南

> 原文：<https://devops.com/guide-public-cloud-security-tools/>

为什么服务器的排列——由硬金属构成，容易发热，重达数千磅——被称为“云”？只有从工程图的角度来看才有意义，在工程图中，数据从起点到终点通过一条未定义的路径传输。在这方面，云指的是作为现代计算基础的随机化分组传输协议。

虽然没有人能确切地知道“云”这个术语的起源，但它所代表的含义是很清楚的。“云是互联网的隐喻，”云营地的联合创始人鲁文·科恩在 2011 年告诉《麻省理工科技评论》。“这是互联网的重塑。”但是对于那些安全第一的人来说，这个比喻是个问题。互联网是一个危险的地方，充满了恶意的人，他们喜欢盗用或破坏数据。如果没有适当的安全控制措施，在互联网上的任何地方存储私人公司和客户数据都是一种潜在的危险行为。

**私有云与公有云**
私有云是单个企业专属的——比如企业公司的内部存储系统。它们通常更容易保护，但在快速可伸缩性方面没有那么灵活。私有云也往往具有更高的资本和运营成本。另一方面，公共云由通常提供云即服务的第三方运营。一些最知名的名字是[亚马逊网络服务](https://aws.amazon.com/)、[微软 Azure](https://azure.microsoft.com/) 和 [Rackspace](http://www.rackspace.com/) ，此外还有[谷歌云平台](https://cloud.google.com/)和 [IBM 的云服务](https://www.ibm.com/services/us/en/it-services/cloud-services/)。

**私有云安全:比你想象的风险更大**
正如 Roger A. Grimes 在 InfoWorld 上指出的，私有云和公共云[都伴随着风险](http://www.infoworld.com/article/2614369/security/the-5-cloud-risks-you-have-to-stop-ignoring.html)。私有云一开始可能看起来更安全，因为它们处于企业的严密控制之下，但最大的缺点之一是许多公司负担不起与亚马逊或 IBM 相同的安全级别。甚至公司自己的员工也是风险因素——他们可能做出恶意行为或造成意外事故。私有云网络很少有地理故障转移选项，因此其所有有价值的数据都面临更大的风险。另一方面，公共云由世界各地的数据中心支持，这通常使它们更加安全和高效。

**公共云安全:仍面临挑战**
尽管如此，企业在决定是否使用公共云时通常会考虑以下三个具体的安全问题:

*   **[多租户](https://en.wikipedia.org/wiki/Multitenancy) :** 与其他企业——尤其是竞争对手——共享云是许多企业高管最关心的问题。公共云中的公司必须确信，他们的私有数据和客户数据都不会泄露给该空间中的其他用户。
*   **[虚拟化](https://en.wikipedia.org/wiki/Virtualization) :** 漏洞攻击越来越频繁地占据头条。随着跨设备的身份变得越来越不稳定，访问和认证系统不得不更加努力地批准正确的用户。
*   **[所有权](https://en.wikipedia.org/wiki/Cloud_computing_issues) :** 许多公共云提供商在他们的用户协议中对所有权问题保持沉默——例如，他们可能会尝试从数据存储中获利。

有许多方法可以应对这些挑战。例如，美国国家公路交通安全管理局找到了一种方法，通过使用一些最新的云安全工具，在不到一个月的时间内[使公共云变得安全和可访问](http://www.cio.com/article/2393260/software-as-a-service/10-ways-to-ease-public-cloud-security-concerns.html)。云安全公司和相关软件行业(如下所列)的快速增长证明了云安全正在进入一个新时代。寻求公共云解决方案的企业可能希望探索这些选项，作为保护其数据的额外方法。

## 顶级公共云安全资源

*   **[批准者](https://www.appriver.com/)**–查看基于 SaaS 的电子邮件和 web 工具的消息安全
*   **[感知技术](https://awarenesstechnologies.com/)**——利用其位于 SaaS 的 DLP 模型来分析移动和云
*   梭鱼网络安全服务——提供恶意软件防护、网址过滤和应用程序控制
*   **[Bitglass](http://www.bitglass.com/)**–充当云访问安全代理，保护应用和移动设备
*   ——处理 BYOD 和 BYOA 的身份和访问管理
*   **[BitSight Technologies](https://www.bitsighttech.com)**——分析安全行为数据，并对公司的安全有效性进行评级
*   -集中于跨设备和应用的身份管理
*   **[cipher cloud](http://www.ciphercloud.com/)**–直接在业务网关处理数据加密或令牌化
*   **[dome 9](https://dome9.com/)**–检查防火墙规则、IP 地址表和端口，寻找异常的 web 流量
*   **[evident . io](http://evident.io/)**—与 AWS 合作提供云安全
*   **[forge rock](https://www.forgerock.com/)**–通过身份访问管理保护企业、云、社交和移动应用
*   **[hy trust](https://www.hytrust.com/)**—提供访问控制、策略实施、虚拟机管理程序强化和日志记录
*   **[IntraLinks](https://www.intralinks.com/)**—保护关键内容并支持客户端控制数据
*   **[Kismet](https://www.kismetwireless.net/)**–被动跟踪云机器，同时不留下日志或可跟踪的数据包
*   **[logz . io](http://logz.io)**–用户可以针对选定的事件和相关仪表板创建主动警报，以汇总和查看数据趋势并监控安全威胁，包括密码暴力检测、访问控制和网络访问
*   **[Metasploit](http://www.metasploit.com/)**–获取云 IP 地址并测试渗透以确保安全到位
*   **[my permissions](http://mypermissions.com/)**–每当应用程序或服务试图访问个人数据时发出警报
*   **[Nessus](https://www.tenable.com/products/nessus-vulnerability-scanner)**——作为开源漏洞评估工具运行
*   **[Nmap:网络映射器](https://nmap.org/)**—通过扫描网络拥塞和延迟来测试渗透率
*   **[Netskope](https://www.netskope.com/)**–发现您网络上使用的任何云应用和影子
*   **[Okta](https://www.okta.com/)**–管理所有云应用的登录，包括 Google Apps、Salesforce、Workday、Box、SAP、Oracle 和 Office 365
*   **[证明点](https://www.proofpoint.com/)**—专门关注电子邮件以保护入站和出站数据
*   **[Qualys](https://www.qualys.com/)**–扫描任何和所有使用过的网络应用，寻找 SaaS、IaaS 和 PaaS 工具中的漏洞
*   **[SilverSky](http://www.baesystems.com/en/cybersecurity/home)**–为 HIPAA 和 PCI 合规性提供电子邮件监控和网络保护
*   **[Skyhigh Networks](https://www.skyhighnetworks.com/)**–利用来自现有防火墙、代理和网关的日志发现、分析和保护云应用
*   **snoop wall**–标记并阻止对网络摄像头、麦克风、GPS 和 USB 等高风险数据端口的访问
*   **[怀特哈特安全](https://www.whitehatsec.com/)**—模仿威胁以避免网站上的编码漏洞
*   **[保险库](http://vaultive.com/)**–加密从网络传输到应用程序的任何数据
*   **[z scaler](https://www.zscaler.com/)**–监控进出您网络的所有流量，同时保护 iOS 和 Android 设备

随着时间的推移，公共云安全只会变得越来越重要。让我们看看来自福布斯记者路易斯·哥伦布的这些数据:

*   预计 2015 年全球基础设施即服务(IaaS)支出将达到 165 亿美元，比上一年增长近 33%
*   到 2019 年，云应用将占全球移动数据流量的 90%，而 2014 年底为 81%

那么，考虑到这些趋势，您打算如何保护您的公共云呢？我邀请你在下面的评论中发表你的想法。