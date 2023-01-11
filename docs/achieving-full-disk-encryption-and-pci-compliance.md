# 实现全磁盘加密和 PCI 合规性

> 原文：<https://devops.com/achieving-full-disk-encryption-and-pci-compliance/>

全磁盘加密(FDE)是当今现代网络中的一项重要安全措施。随着数据安全性变得比以往任何时候都更加重要，许多 IT 管理员都在考虑如何在其跨平台系统群中实施全磁盘加密。许多组织还受到包括 PCI DSS 在内的合规性法规的约束，这些法规要求将 FDE 作为其合规性要求的一部分。

## 什么是 FDE？

全磁盘加密锁定计算机的硬盘驱动器时，所说的计算机是关闭或休息。如果一台启用了 FDE 的计算机被盗，窃贼唯一会拿走的就是硬件；系统上的数据将被加密，很难获取。

FDE 程序(BitLocker for Windows、FileVault for Mac)使用恢复密钥作为身份验证方法。当用户登录到他们受 FDE 保护的系统时，使用他们相关的用户名和密码解锁驱动器。但是，如果用户忘记了密码、被锁定或者出于任何原因需要移除和访问硬盘，IT 管理员可以使用恢复密钥来解密硬盘。鉴于恢复密钥的关键性质，IT 管理员需要将它们存储在第三方托管中；也就是说，相对于它所属的系统安全地存储和分类。

## 什么是 PCI？

支付卡行业数据安全标准(PCI DSS)是一项合规性法规，旨在确保处理这一重要客户财务信息的公司能够保护信用卡数据的安全。PCI 围绕保护持卡人数据环境(或称 CDE)展开，该环境存储了通过合规公司传递的所有信用卡信息。PCI 法规下有 12 个主要要求，但[要求 3](https://www.pcisecuritystandards.org/documents/PCI%20SSC%20Quick%20Reference%20Guide.pdf) 专门处理数据加密。

## 将 FDE 用于 PCI

PCI 要求 3 的核心是要求安装适当的安全措施来保护 CDE 中的数据。这可以说是 PCI 最重要的需求之一。FDE 是确保符合要求 3 的理想方式。通过锁定静态系统，IT 管理员可以防止因笔记本电脑或硬盘被盗而导致的未经授权的访问。

关于加密，要求 3 还要求安全地存储和维护密钥。使用恢复密钥托管，IT 管理员可以确保只有正确的人才能访问加密密钥，还可以监控何时使用它们以及谁在使用它们。

## 如何实施 FDE 以实现 PCI 合规性

当谈到在 Mac 和 Windows 上强制实施 FDE 以实现 PCI 合规性时，it 管理员可能会发现他们的选择有限。市场上的许多 FDE 工具只能执行 Bitlocker 或 FileVault，而不能同时执行两者。由于当今的许多 IT 组织在系统平台方面都是异构的，因此只能实施其中一种的 FDE 解决方案是行不通的，管理员也不愿意实施多种解决方案来达到预期目的。

此外，IT 组织需要他们的 FDE 解决方案来安全地将加密恢复密钥存储在托管中。这种需求进一步限制了理想 FDE 选项的列表。最终，有了这些要求，就有了一个绝佳的选择，可以为 IT 管理员提供适合 PCI 合规性的低开销 FDE 体验。使用 [JumpCloud 的策略](https://support.jumpcloud.com/support/s/article/policies-2019-08-21-10-36-47)，IT 管理员可以在其 Windows 和 Mac 系统群中大规模实施 FDE，安全地保管各个恢复密钥。

— [扎克·德迈尔](https://devops.com/author/zach-demeyer/)