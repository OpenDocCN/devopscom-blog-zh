# 低代码开发有安全风险吗？

> 原文：<https://devops.com/is-low-code-development-a-security-risk/>

根据 Gartner 的预测，2021 年全球低代码开发市场预计将达到 138 亿美元，比 2020 年大幅增长 22.6%。Gartner 还预测，尽管削减了预算并努力优化成本，但新冠肺炎期间远程开发的激增将继续推动低代码的采用。

## 低代码在专业开发人员和普通开发人员中的流行

低代码不再是街区里的新生事物。从简单的仪表板到复杂的应用程序，低代码应用程序正变得越来越多样化，成为企业世界的主流应用。本质上，低代码是应用程序开发的一个可视化范例，它包括拖放预先构建的组件和集成，从而实现快速、简单且不易出错的开发。

低代码的优势在于，它使非传统开发背景的用户能够参与到应用程序开发过程中，从而使开发民主化并加快项目进度。它还缩小了组织在资源有限和开发人员稀缺的情况下满足不断增长的数字化需求时出现的供需差距。许多低代码平台使得普通开发人员(例如，业务分析师、业务线用户、初级开发人员)可以轻松构建应用程序，同时与传统的编码方法相比，大大减少了交付时间。

但是公民开发人员的生产力和速度并不是低代码开发的唯一好处。如今，低代码平台还附带了专门为从企业 IT 团队到 ISV 的专业开发人员构建的功能。这些平台针对企业使用进行了强化，能够利用复杂应用程序的可扩展性和安全性需求，并且具有足够成熟的集成功能，可以无缝地适应现有的工具和技术。在新冠肺炎疫情期间，许多企业通过采用低代码平台和应用程序重塑了自己，帮助他们适应向远程工作场景的突然转变，并实现随之而来的必要的现代应用程序需求。

## 低代码和远程工作的安全挑战

与传统的开发相比，低代码涉及到各种各样的角色一起工作来构建应用程序，同时处理自动生成的代码、现成的组件和内置的默认配置。环境的这种转变揭示了一些需要解决的独特挑战。基于低代码构建的远程团队面临一些常见的安全挑战。

## 应用开发和远程团队协作

*   **缺乏安全意识:**低代码用户既有商业背景，也有技术背景。一些从业者不熟悉应用程序安全最佳实践，缺乏对潜在漏洞和安全漏洞的认识和理解。
*   **平台访问和管理控制:**低层代码集中部署，可供整个企业的用户通过浏览器访问。这引入了网络入侵的风险；向未经授权的开发人员提供访问权限，并向远程访问平台时不需要的用户开放更大的权限。
*   **代码库和团队协作:**低代码平台必须确保自动生成的代码能够提交给企业认可的库。这种代码访问不应该被滥用，应该有足够的协议来进行代码控制和升级。

## 代码生成和 DevSecOps 最佳实践

*   **保护定制代码:**低代码工具允许编写定制代码，以扩展和实施平台编码指南和设计模式，从而保护敏感数据免受未经授权的访问。
*   **坚持安全的发布实践:**与现有企业 CI/CD 管道的集成非常重要，这样开发团队可以在投入生产之前将相同的发布治理协议扩展到自动生成的代码。

## 终端用户应用程序访问和数据保护

*   **防止恶意攻击:**如今，web 和移动应用程序正成为安全漏洞的持续目标。自动生成的代码和远程工作的公民开发人员会使低代码应用程序更容易出现漏洞。平台应该生成能够完全抵御钓鱼攻击、SQL 注入、暴力攻击和 DOS 攻击的应用。
*   **保护数据和应用访问:**低代码平台应提供全面的访问控制机制，防止未经授权访问数据和应用功能。随着远程团队随时随地从任何设备访问应用，通过适当的控制可以防止数据泄露。

## 低代码和安全性——发展的未来

随着企业和 ISV 转向更严肃的低代码用例，更大的问题仍然存在。低代码平台能让现代开发团队更快地交付应用程序，同时仍然支持安全和严格治理的环境吗？答案是，是的，他们可以！但是，在考虑低代码平台时，开发团队必须考虑以下安全清单:

1.  选择的低代码平台必须建立在企业安全隔离区或安全私有云内，并且必须毫不费力地通过网络安全检查。
2.  该平台必须为自动生成的代码以及开发人员编写的自定义代码强制实施编程中的最佳实践(编码约定、设计模式和数据加密)，以促进与现有 CI/CD 流程和工具的集成。
3.  该平台必须为网络和移动应用提供针对[10 大 OWASP 漏洞](https://owasp.org/www-project-top-ten/)的全面保护，并拥有第三方认证以保证代码质量和安全性。此外，组织应该确保他们选择的平台的二进制文件以及 CVE 库中列出的所有第三方依赖项(包括开源库)中没有漏洞。
4.  该解决方案必须支持多种身份认证提供者(数据库、LDAP、AD、SSO、SAML、Open-ID、多因子、生物特征)来构建具有强大用户安全性的应用程序。对于用户授权，确保支持粗粒度和细粒度的访问控制策略，以保护基于 RBAC 的应用程序的各个方面。

开发团队可以采用低代码技术，同时确保安全最佳实践到位。低代码已经存在，有了合适的平台，企业和 ISV 可以确保安全性被转移到左边，由开发人员在开发过程的更早阶段解决。结果是高生产力的远程工作人员生产出现代化、可扩展和安全的应用程序。