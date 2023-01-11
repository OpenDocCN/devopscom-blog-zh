# 软件开发人员需要物料清单的 4 个原因

> 原文：<https://devops.com/4-reasons-software-developers-need-a-bill-of-materials/>

最近的 Log4j/Log4Shell 漏洞敲响了警钟，威胁不会等到行业跟上软件供应链安全的步伐时才出现。虽然 Log4j 开源组件漏洞让我们措手不及，但它确实凸显了软件供应商在披露其产品组成方面更加主动的必要性。很明显，分析开源库和第三方代码应该成为理解它们的构成和它们在商业软件应用中引入的潜在风险的标准实践。

不幸的是，依靠开源项目来提供对安全漏洞的可见性是行不通的。在大多数情况下，这些项目资金严重不足。例如，在 Heartbleed 漏洞出现时，OpenSSL 获得的资金非常少。然而，开源的使用每年都在增加。商业软件组织必须为他们使用的开源项目做出贡献，并为这些产品的安全性分担责任。

除了开源库，大多数供应商都从承包商或雇佣开发组织获得第三方代码。如果没有第三方开发的代码组成的文档，商业软件供应商就不可能在开发周期中实现风险之前主动识别和管理风险。

## 使用软件组合分析(SCA)工具

如果没有提供[软件材料清单](https://www.cisa.gov/sbom) (SBOM)，商业软件供应商有责任创建一份。这可以使用软件组合分析(SCA)工具来完成，这些工具可以分析二进制文件，并且不需要访问源代码。他们可以生成 SBOMs 来识别使用中的开源或第三方组件，以及跟踪和管理软件 供应链中的安全风险。

创建一个全面的 SBOM 提供了其他好处，因为大多数开源项目和合同开发者只可能发布直接的依赖关系(如果有的话),而不会进一步查看依赖关系的依赖关系，等等。

## **要考虑的四个好处**

与此同时，商业软件供应商可以期待他们的客户很快开始要求 SBOMs，因为这将是网络安全行政命令的要求。鉴于这种不断发展的格局，商业软件供应商应该考虑以下四个好处，以便主动实施 SBOM 计划来管理他们所构建的产品:

*   获得软件供应链风险的可见性，以识别、减少和消除重用软件(即开源软件和第三方软件)中的漏洞。SBOMs 为您重复使用和购买的软件的业务决策提供数据。最好在您的客户发现这些风险之前发现它们。
*   先发制人的供应链认证，以确保符合未来的要求。SBOMs 将很快成为与美国联邦政府做生意的一项要求。在采购过程中满足 SBOM 要求的供应商将获得优惠待遇。
*   随着[风险管理](https://devops.com/leading-cyber-insurance-provider-coalition-launches-free-risk-management-platform-to-help-organizations-combat-ransomware-and-cyber-risk/)和风险缓解而来的安全性和下游效益的提高。在安全风险嵌入产品之前避免、检测和补救安全风险在开发和部署过程中会带来巨大的收益。您将为下一次安全事件做好更充分的准备。
*   开发者、供应商和开源项目共享的标准化 SBOM 带来了对软件资产的共同理解。SBOM 成为组织内外交流软件内容和依赖关系的一种方式。

通过创建 SBOMs 并向供应商提出同样的要求，对软件供应链采取积极主动的方法，将使商业开发人员能够为下一个 Log4j/Log4Shell 漏洞做好更充分的准备。这也将允许他们改善其终端客户的软件供应链安全状况。