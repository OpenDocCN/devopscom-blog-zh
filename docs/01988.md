# 应用商店如何解决 Linux 生态系统中的碎片化问题

> 原文：<https://devops.com/how-app-stores-are-addressing-fragmentation-in-the-linux-ecosystem/>

根据 [DistroWatch](https://distrowatch.com/search.php?ostype=Linux&category=All&origin=All&basedon=All&notbasedon=None&desktop=All&architecture=All&package=All&rolling=All&isosize=All&netinstall=All&language=All&defaultinit=All&status=Active#simple) 的数据，目前有 273 个 Linux 发行版在运行，另外 56 个处于休眠状态，521 个已经停止运行。虽然其中一些有共同的基础，但对于公司和开发者来说，它仍然是一个极其多样化的景观。

这意味着开发人员必须创建他们的应用程序的多个版本，以便能够向所有 Linux 用户提供他们的软件，或者仅仅针对一小部分市场。此外，开发人员需要多个版本的构建工具，这不可避免地会导致巨大的资源开销。

一般来说，跨所有操作系统的桌面应用程序分发是复杂的；在 Linux 中，软件打包和分发中的这种碎片化和相互依赖性进一步加剧了这种情况。

例如，Fedora 使用 RPM 打包格式，而 Debian 使用。deb 格式。此外，为一个版本的 Linux 发行版构建的包通常与同一发行版的其他版本不兼容，需要为每个版本单独构建。

开发人员需要同时满足所有这些需求，才能成功地向用户提供他们的产品，这在资源有限的情况下是很难做到的。

从某种程度上来说，Linux 软件的发行选择和后续推广是一个先有鸡还是先有蛋的问题。最初，公司和开发者必须决定他们要瞄准 Linux 桌面系统的哪一部分。然后，一旦他们通过一个或多个分销渠道向最终用户提供了他们的产品，他们仍然必须投入单独的努力来推广他们的应用程序并获得使用。

不幸的是，没有足够的数据来帮助选择和优化分销或促销过程。Linux 软件开发人员通常缺乏对其软件的使用和流行程度的足够直接的可见性。

传统上，创作者分发软件有多种方式:官方网站，公司和开发者在他们自己的领域提供软件下载；GitHub、GitLab、SourceForge 等代码库；和应用程序存储库，其中基于 Linux 的操作系统通常通过自托管存储位置提供软件。

为了实现最高水平的渗透，软件开发人员通常会使用上述一些或全部方法来分发他们的应用程序。同样，大多数用户会利用多种方法来获得他们需要的软件。虽然这让开发人员在如何向最终用户交付应用程序方面有了更多的自由，但它也造成了更多的碎片。

近年来，通过建立软件中心，为解决打包中的碎片化和简化软件分发做出了重大努力，其中一些 Linux 分发版提供了类似商店的目的地，具有图形前端、软件评级、屏幕截图、描述和其他以用户为中心的数据，以便更好地进行搜索和发现。

目前，在 Linux 领域有三个这样的应用——app image、Flatpak 和 snaps。他们每个人都以不同的方式处理可用性的各个方面。

AppImage 和 Flatpak 技术的设计主要是为了支持 GUI 桌面应用程序。除了桌面应用程序之外，快照还设计用于服务器、云基础架构和[物联网](https://devops.com/3-ways-iot-developers-can-make-their-applications-more-secure/)设备。

snaps 发行商 Spotify 是从这种方式中获益的一个例子。一方面，它要求 Spotify 工程团队同时维护 snap 和传统的 Deb 包。另一方面，snap 版本更容易发布，这也有助于 Deb 版本的简化。

主要原因是能够使用简单的回滚，这一点已经得到了应用。这个特性消除了 Linux 桌面客户端应用程序的一个可能损坏的版本可能被推送给用户的不确定性。Spotify 的工程师首先发布 snap 版本，在确定它能够正常工作和运行后，他们也构建了 Debian 包。Snaps 使 Spotify 团队能够更密切地跟踪 Windows 和 Mac 版本的每周发布节奏。

自包含打包和分发机制的出现解决了 Linux 应用程序生态系统中的一个主要问题——由于打包和分发的挑战，很难建立一个成功的商业模型。新格式减少了碎片，因为它们最大限度地减少了开发人员支持其应用程序所需的排列数量。

向不特定于任何特定 Linux 发行版的集中式[应用商店](https://ubuntu.com/engage/shift-to-app-store-experience?utm_source=PR&utm_medium=PR&utm_campaign=CY19_IOT_Snaps_Whitepaper_ShifttoAppStore)的转变提供了更高的可发现性和更好的用户体验一致性。

开发人员需要更少的资源来支持多个目标平台，这允许他们将精力集中在核心产品上，因为他们知道他们的软件将对更广泛的桌面受众可用，而不必依赖于特定于发行版的依赖。

由于 Linux 中新的、完善的推广和分销模式仍相对年轻，我们看到了改进，但仍有机会开发和采用更好的、数据驱动的实践。

随着这一领域的不断发展，商店模式将有助于推动 Linux 桌面的增长和使用，为软件开发人员提供比以往任何时候都更精致、更切实的体验。

— [马丁·温普莱斯](https://devops.com/author/martin-wimpress/)