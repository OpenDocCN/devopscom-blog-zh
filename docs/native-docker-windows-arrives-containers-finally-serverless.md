# Windows 的原生 Docker 到来:容器最终是无服务器的吗？

> 原文：<https://devops.com/native-docker-windows-arrives-containers-finally-serverless/>

Docker 最终为无服务器计算时代做好准备了吗？这是本周发布的对 Windows Server 2016 的原生 Docker 容器支持的消息。

如果您已经关注 Docker 有一段时间了，您会知道 Docker 容器最初只支持 Linux 操作系统。然后，Docker 也为 Windows 用户提供了它的平台——但是有一个主要的警告，Docker 引擎运行在基于 Linux 的虚拟机镜像之上。所以，你可以在 Windows 上运行 Docker，但是 Linux 仍然是中间人。

## 真正的码头集装箱

本周，一切都变了。9 月 26 日，Docker 宣布在 Windows Server 2016 上全面提供原生 Docker 容器支持。Docker 所说的“本机”是指容器使用内置于 Windows 内核本身的新原语(相当于 Linux 中的名称空间)运行。不再有虚拟化。

但这还不是全部。完整的 Docker 工具集现在也可以在 Windows 上本地运行。Docker CLI、Swarm orchestration、数据卷和 Docker 化基础架构的所有其他构建模块以及 Docker 容器本身都是官方兼容的。

这种支持是 Docker 和微软两年多合作的结果，微软现在是 Docker 开源项目的五大贡献者之一。

## 警告

对 Docker 的原生支持是一大成就。但是仍然有一些限制，包括:

*   Docker 容器只能在 Windows Server 2016 和 Windows 10 上原生运行。Docker 首席运营官公司的 Scott Johnston 在一次采访中解释说，其他版本不能与 Docker 一起工作，因为它们缺乏支持 Docker 容器所必需的内核增强。
*   Johnston 说，Docker 的一些高级网络配置功能还不支持，因为使这些功能工作所需的“管道”在内核中不完整，并补充说微软正在努力改变这一点。
*   最值得注意的是，Windows 上的 Docker 容器只能在容器内部运行 Windows 应用程序。换句话说，你不能在 Windows 上运行的 Docker 容器中运行一个为 Linux 编译的应用程序。你需要一个 Windows 主机来完成这项工作。(反之亦然:你不能在 Linux 主机上的 Docker 容器中运行 Windows 应用程序。)约翰斯顿认为，这是不会改变的。

## Docker 变得无服务器

该公司正在庆祝的支持，作为一个机会，以扩大 Docker 生态系统。对 Docker partners 来说，对 Windows 的支持“将潜在的市场机会翻倍”，该公司在一份关于该公告的陈述中表示。(顺便说一句，Docker 有充分的理由通过给合作伙伴提供一个更大的生态系统来让他们满意。今年早些时候将 Swarm 整合到 Docker 中削弱了 Docker 一些合作伙伴产品的价值。但是我跑题了。)

然而，从 DevOps 的角度来看，这个消息最有趣的一面是，它意味着 Docker 现在更加没有服务器了。Docker 容器的很大一部分价值在于它们简化应用交付的能力。只要你能把你的应用打包成 Docker 容器，你就可以把它部署在任何运行 Docker 的服务器上。

您不必考虑底层服务器硬件或配置。换句话说，Docker 允许您变得无服务器，因为您不再需要过多考虑您要部署到的服务器。

然而，在以前，这种灵活性受到这样一个事实的限制，即您必须考虑服务器操作系统。现在，有了 Windows 的原生 Docker 支持，就不再是这样了。无论您的基础架构是由 Windows 服务器、Linux 服务器还是两者组成，都没有关系。只要在它们上面安装 Docker，就可以部署到任何服务器上。

当然，还有一个问题是必须确保你的应用程序是为正确的操作系统编译的。但是在构建过程中的大多数情况下，这是很容易管理的。

— [克里斯·托齐](https://devops.com/author/chris-tozzi/)