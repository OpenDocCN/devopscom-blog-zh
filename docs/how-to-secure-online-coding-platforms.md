# 如何保护在线编码平台

> 原文：<https://devops.com/how-to-secure-online-coding-platforms/>

## **在线编码平台的威胁建模**

DevOps 团队的发展和对基于云计算的更大依赖已经完全改变了编码过程。现在，有了集成开发环境(ide)，编码可以完全在线完成。这很方便，但是在线 ide 安全吗？为了回答这个问题，我们将关注两个流行的基于云的 ide:AWS cloud 9 和 Visual Studio Online。

在在线编码中，IDE 在您的浏览器中呈现，浏览器 JavaScript 引擎使用 WebSockets 在后台启动与您链接的设备的安全外壳(SSH)连接，例如虚拟专用服务器(VPS)，为您提供熟悉的终端界面来执行命令。环境——指链接的云 VM/VPS 或 SSH 可访问设备——包括工具配置(如包含哪些令牌或云配置文件)、源代码副本、编译器和您想要使用的其他工具。

![](img/584b14a97cb209769532fa0602850ce2.png)

Figure 1\. Local versus cloud-based IDE. Source: Trend Micro.

本地和基于云的编码平台之间的主要区别在于大部分环境驻留在哪里。在云 ide 中，环境是云提供商内部的一个虚拟机实例。就安全性而言，这意味着您将信任委托给云提供商，但您有责任防止任何后门打开或向虚拟机引入错误配置问题。如果您将自己的设备与 AWS Cloud9 配合使用，您有责任安全地配置设备。

## **链接的设备/虚拟机并不总是安全的**

后端运行的内容通常决定了链接的设备和虚拟机是否安全。如前所述，SSH 链接设备是使用这些在线编码平台所必需的。在 Visual Studio Online 的情况下(在撰写本文时仍处于预览模式)，我们可以发现一个 [Visual Studio (VS)代码服务器](https://code.visualstudio.com/docs/remote/remote-overview) 正在机器上运行。

代码服务器本身是一个 Node.js 应用程序，您的浏览器将连接到该应用程序。也可以整体下载~/。vscode-remote 文件夹，并在本地环境中运行服务器。

作为链接设备的所有者，您有权将自己升级为 root 用户，并安装或配置您认为需要的任何设备。默认情况下，您还预装了 Docker 和 Git。

在 AWS 托管的 Cloud9 中，情况稍微复杂一些。平台通信所必需的后端位于链接的设备内部，而前端保持托管在不同的位置。但是，就像在 VS 中一样，你也可以将自己提升为 root。

这让我们想到了第一个安全问题: 关联设备/虚拟机的安全性或私密性如何？

链接的设备包含机密信息——访问令牌、应用配置、源代码等。，应该防止未经授权的访问。

默认情况下，平台由提供商保护。但是，您应该记住，除了您的根访问可用性之外，您还负责防止错误配置问题，尤其是在使用第三方插件时。AWS 不为非其开发的插件提供插件支持。

您可能会做出一些错误的配置，这会导致安全问题。例如，如果您有意或无意地将 IDE 设置为可从外部访问，这种更改可能会产生重大影响。

此外，将访问令牌存储在加密令牌库中并不常见。其中很多可以通过明文配置文件查看。如果没有额外的安全措施，您的访问令牌最终可能会暴露给外人。

一旦网络罪犯获得了未经授权的访问权限，他们就可以为了自己的利益而损害您的代码。一个例子是针对用恶意软件修改软件更新的软件公司的 [供应链攻击](https://www.wired.com/story/inside-the-unnerving-supply-chain-attack-that-corrupted-ccleaner/) 。

## **浏览器可能引入恶意扩展或漏洞**

下一个安全问题是浏览器本身。由于在线编码平台是从 web 浏览器访问的，所以当从公共的、非域的、共享的或未受保护的计算机访问这些站点时，您应该非常小心。

恶意浏览器扩展是一种众所周知的现象。虽然可能感染了恶意软件的不受信任的计算机存在明显的风险，但攻击者也有可能使用恶意的 web 浏览器扩展来窃取代码。

## **代码扩展和插件也可能包含恶意软件**

Visual Studio Online 和 VS 代码平台的主要优势是可用的扩展数量。这本身就是另一个可能的攻击面。

让我们想象一个恶意的 VS 代码扩展——一个看起来有用的带有嵌入式后门的扩展。缺乏权限检查(如磁盘访问、网络访问、进程访问等。)成为一个安全问题。在 [扩展发布](https://code.visualstudio.com/api/working-with-extensions/publishing-extension) 期间的安全检查的范围限于具有有效的发布者 id 和一些与图像相关的限制。这意味着你必须完全信任扩展开发者。

## **没有一个软件应用是没有错误的**

任何种类的软件都可能存在漏洞，这一点也必须考虑在内。在在线编码平台的情况下，它们会受到 web 类漏洞的影响，因为 ide 是 web 应用程序。例如，允许攻击者执行自己的 JavaScript 代码的漏洞可以控制 IDE 或远程链接的设备。

最近一个影响[Visual Studio Live Share 扩展](https://portal.msrc.microsoft.com/en-US/security-guidance/advisory/CVE-2019-1486) 的漏洞表明，我们可以期待在不久的将来看到另一个影响在线编码平台的漏洞。

## **保护云 ide 是 DevOps 的必备条件**

威胁建模使我们能够了解影响计算环境整体安全性的不同因素。云 ide 应该与其他软件没有什么不同，如果不是更安全的话。

以下是针对我们提出的每个安全问题的一些建议:

*   为了联网设备的安全性—安装值得信赖的软件。保持软件更新。不要乱开端口上网。
*   对于浏览器——在可信和安全的环境中工作。尽量避免使用共享电脑。仅安装来自可信供应商的浏览器扩展。
*   对于 VS 代码扩展——避免安装来自未知来源或作者的扩展。
*   针对一般漏洞—确保您的环境更新到最新版本。

— [大卫·费瑟](https://devops.com/author/david-fiser/)