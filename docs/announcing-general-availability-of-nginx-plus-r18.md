# 宣布 NGINX Plus R18 正式上市

> 原文：<https://devops.com/announcing-general-availability-of-nginx-plus-r18/>

简化开发运维的配置工作流，并大规模增强应用的安全性和可靠性

**加利福尼亚州旧金山——2018 年 4 月 9 日—**NGINX，Inc .是一家基于流行的开源项目并提供一套旨在开发和交付现代应用的技术的公司，今天宣布 NGINX Plus R18 正式上市。NGINX Plus 是唯一一款集负载平衡器、内容缓存、web 服务器、代理、API 网关和 Kubernetes 入口控制器于一体的产品。这种多功能性使您能够简化您的架构，以交付传统应用和基于微服务的新应用。

NGINX 的灵活性、可移植性以及与 CI/CD 自动化工具的无缝集成有助于加快企业对 DevOps 的采用。NGINX Plus R18 通过简化配置工作流程和增强应用程序的安全性和可靠性来推进这一目标。

R18 中引入的新功能包括:

*   **简化配置工作流程**:

○ **动态证书加载:** NGINX Plus 引入了 TLS 证书的惰性加载。对于延迟加载，只有在请求匹配的主机名时，TLS 证书才会加载到内存中。这简化了 NGINX Plus 的配置，并减小了它的大小，因为在一个服务器块中可以处理多个证书。此外，通过使用 NGINX Plus API 将证书和私钥自动上传到键值存储，您可以节省时间和精力。这对于具有大量证书的部署或频繁重新加载配置的情况尤为理想。

○ **支持服务器配置的端口范围:**在此版本中，用户可以指定端口范围，而不仅仅是特定的端口。可以为 HTTP 和 TCP/UDP 应用程序(流模块)指定端口范围。这也允许 NGINX Plus 在被动模式下充当 FTP 服务器的代理。

○ **简化的集群管理:** NGINX Plus R15 引入了 NGINX Plus 实例集群的运行时状态同步。此版本通过为集群的每个成员使用单一配置来增强集群。这特别适合动态环境，如自动扩展组或集装箱化集群。

○ **使用 NGINX JavaScript 模块的模块化代码组织:**NGINX JavaScript 模块现在支持 JavaScript 导入和导出模块，使您能够将您的 JavaScript 代码组织到多个特定于功能的文件中，而不是像以前那样组织到单个文件中。这极大地提高了可读性并简化了维护，尤其是在多个团队都在贡献 JavaScript 代码的情况下。

*   **增强的安全性:**

○ **最大限度地减少证书暴露:**管理安全站点和应用程序的 TLS/SSL 证书时，用户配置 NGINX Plus，将证书和相关私钥指定为磁盘上的文件。在这个版本中，NGINX Plus 直接从内存中的键值存储加载证书。对文件系统保密使得攻击者很难获得服务器证书的私钥。

○ **对不透明会话令牌的支持** : NGINX Plus 支持 OpenID Connect 认证和后端应用的单点登录。在这个版本中，NGINX Plus 支持 OpenID Connect 发布的不透明会话令牌。不透明令牌不包含关于用户的个人可识别信息，因此没有敏感信息存储在客户端。

*   **可靠性提高:**

○ **支持客户端在运行状况检查失败时重新连接** : NGINX Plus 主动运行状况检查会持续探测上游服务器的运行状况，以确保流量不会被转发到离线的服务器。在此版本中，当主动运行状况检查失败时，可以终止现有的客户端连接。这使得客户端应用程序能够重新连接，此时它们被代理到一个健康的后端服务器，从而提高了应用程序的可靠性。

要深入了解这些特性并了解 R18 中的更多特性，请阅读我们的博客。要开始免费试用 NGINX Plus R18 和 NGINX 控制器，请访问[https://www.nginx.com/free-trial-request-nginx-controller](https://www.nginx.com/free-trial-request-nginx-controller)。

**关于 NGINX，Inc.** NGINX，Inc .是广受欢迎的开源项目背后的公司，该项目受到超过 4.5 亿个网站的信任。我们为开发和交付现代应用提供了一套技术。NGINX 应用平台使正在进行数字化转型的企业能够更新传统的单片应用，并交付基于微服务的新应用。像网飞、星巴克和麦当劳这样的公司依靠 NGINX 来降低成本、提高弹性和加速创新。NGINX 的投资者包括:Blue Cloud Ventures、e.ventures、Index Ventures、高盛、MSD 资本、NEA、Runa Capital、Telstra Ventures。

我们的总部设在加州三藩市，EMEA 总部设在爱尔兰的科克，APAC 总部设在新加坡。在[https://www.nginx.com/](https://www.nginx.com/)了解更多信息，或在 Twitter 上关注@nginx 加入讨论。