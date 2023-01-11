# ThycoticCentrify 宣布了治理和管理云平台特权访问的新解决方案

> 原文：<https://devops.com/thycoticcentrify-announces-new-solution-to-govern-and-manage-privileged-access-to-cloud-platforms/>

**加州圣克拉拉和华盛顿州 DC** 、**2021 年 5 月 18 日**―[thycoticccentrify](https://www.centrify.com/)由特权访问管理(PAM)领导者 Thycotic 和 Centrify 合并而成的云身份安全解决方案领先提供商，今天发布了其云提供商解决方案，以实时集中管理 AWS 计费账户、身份和访问管理(IAM)账户以及 AWS EC2 实例。

组织正在快速将内部应用程序迁移到云，通常采用“提升并转移”的方法将虚拟机(VM)和应用程序迁移到他们首选的云提供商。这样做时，他们通常会为每个应用程序项目或部门创建几个不同的 AWS 帐户，其中每个 AWS 帐户都有自己的 root/billing 帐户、IAM 用户帐户和服务帐户，以及为支持应用程序而创建的虚拟机(VM)帐户。管理 AWS 根/计费帐户凭证很困难，因为任何更改都必须由人工协助，AWS 的最佳实践是为 AWS 服务强制执行驱动的帐户配置多因素身份验证(MFA)。虽然自动化工具可以将新的 AWS EC2 实例集成到 PAM 解决方案中，但运营、员工和审计人员需要一种方法来确保和验证所有托管的虚拟机都得到考虑和适当的保护。

ThycoticCentrify 的 AWS 云提供商解决方案通过扩展一组现有的 PAM 功能来自动连续发现所有 AWS EC2 实例，从而解决这些挑战，即使在弹性自动扩展组中也能提供实例的完全可见性。AWS root/billing 帐户仅用于紧急访问，通过 AWS 管理控制台、AWS CLI、SDK 和 API 对 AWS 帐户的交互式访问受到严格控制。AWS IAM 帐户和相关的访问密钥被消除或存储以减少攻击面，基于 SAML 的联合单点登录提供了一种更安全、维护成本更低的替代方案。连续的 EC2 发现和发现后自动化确保了完整和准确的可见性，并且 EC2 实例及其特权帐户立即得到保护并置于集中管理之下。

ThycoticCentrify 首席技术官 David McNeely 表示:“就可扩展性和可用性而言，云改变了游戏规则，但它也改变了网络攻击者的游戏规则，他们希望利用不同控制措施产生的新漏洞以及由此带来的身份管理挑战。“我们面向 AWS 的云提供商解决方案可在添加和删除云工作负载时提供实时可见性，自动执行特权密码和身份管理，确保实施管理和访问控制，同时降低复杂性和风险。”

ThycoticCentrify 的云提供商解决方案的基础是以 Centrify 平台和轻量级 Centrify 网关连接器为中心的云原生“中心辐射式”架构，这些连接器将云工作负载注册到 Centrify 平台中。该解决方案还可以在发现的 Windows 和 Linux 实例上自动部署 Centrify 客户端，以实现细粒度的访问控制、审计和可视会话记录，并通过“使用我的帐户”利用 Centrify 平台的临时证书实现无密码登录

ThycoticCentrify 的云提供商解决方案最初面向 AWS，很快将扩展到微软 Azure 和其他云提供商平台。欲了解更多关于 ThycoticCentrify 的 AWS 云提供商解决方案的信息，请访问[https://www.centrify.com/resources/solution-briefs/aws/](https://www.centrify.com/resources/solution-briefs/aws/)。

****关于 thycoticscentrify****
thycoticscentrify 是领先的云身份安全厂商，实现规模化数字化转型。ThycoticCentrify 行业领先的特权访问管理(PAM)解决方案可降低风险、复杂性和成本，同时保护组织在云、内部和混合环境中的数据、设备和代码。ThycoticCentrify 受到全球超过 14，000 家领先组织的信任，其中包括超过一半的财富 100 强企业，客户包括全球最大的金融机构、情报机构和关键基础设施公司。

Thycotic 软件有限责任公司和 Centrify 公司 2021。Centrify 和 Thycotic 分别是 Centrify Corporation 和 Thycotic Software，LLC 在美国和其他国家的注册商标。