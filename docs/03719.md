# Chef InSpec 2.0 以 Velocity 实现合规性，从而加快开发进度

> 原文：<https://devops.com/chef-inspec-2-0-delivers-compliance-velocity-accelerate-devsecops/>

*与手动流程相比，开源合规自动化将评估和补救时间减少了 95%*

**S****EATTLE—2018 年 2 月 20 日—** [Chef](https://www.chef.io/) ，持续自动化领域的领导者，今天宣布推出 InSpec 2.0，这是一款合规自动化解决方案，通过允许跨职能应用、基础设施和安全团队评估和修复从开发到整个软件交付生命周期的合规性问题，加快开发进度。InSpec 2.0 提供了云配置测试(包括微软 Azure 和 AWS)，30 多种新的一致性能力(包括 Docker、IIS、NGINX 和 PostgreSQL)，增强了与第三方工具的集成，提高了易用性和可定制性。

InSpec 是 Chef“检测、纠正、自动化”云迁移和持续自动化方法的第一步。它有助于组织维护生产中合规性状态的最新视图，在安全问题进入生产之前及早检测到它们，并在降低风险的同时更快地交付应用程序。InSpec 是一个开源框架，用于描述可在软件工程师、运营和安全工程师之间共享的安全性和合规性规则，能够在软件交付流程的所有阶段(从开发人员的工作站一直到生产)快速实现合规性，不会对性能产生影响或产生副作用。InSpec 的可读性意味着它易于所有团队成员使用和理解，包括那些其角色涉及最少编码的成员。

**新功能**

*   **云配置合规:** InSpec 2.0 让用户能够针对云资源编写合规规则，包括 AWS 和 Microsoft Azure，以及用户定义的自定义合规策略。
*   **改进的用户体验:** InSpec 2.0 包含 30 多种新资源，允许用户为许多常见应用程序和配置文件编写合规性规则，而无需任何编程知识。这些包括 Docker、安全密钥(RSA/DSA/x509)、webserver (IIS/nginx/Apache)配置、包(既有 system 也有 Perl/R/等。)、PostgreSQL 和 MySQL 数据库配置、XML 配置文件中的 XPath 匹配、ZFS 存储池配置等等。
*   **新集成:** InSpec 结果现在可以以 JUnit 格式导出，以便集成到 Jenkins 等持续交付工具中，并且可以从 Chef Automate 中提取合规性配置文件。之前宣布的与亚马逊系统管理器(SSM)的集成为云中的 InSpec 提供了一个无摩擦的入口。
*   **性能提升:** 在 Windows 上，InSpec 2.0 的运行速度比 InSpec 1.0 快 90%，在 Linux 上快 30%。

**支持报价**

*   Niu Solutions 首席技术官 Jon Williams 表示:“InSpec 帮助我们统一了合规、安全和开发团队，简化了审计工作，将通常需要的数千个工时减少了 95%，并消除了整个流程中的重复劳动和数据。 “它让这些团队能够更好地控制合规性政策，让业务部门能够更积极地维护自己的环境。最重要的是，它使我们能够持续监控审计合规性，确保所需的状态并消除节点之间的变化漂移。”
*   Chef 营销副总裁 Marc Holmes 表示:“InSpec 2.0 建立在我们的承诺之上，即构建现代应用团队真正实现 DevSecOps 承诺所需的基本工具和服务，将安全性与传统和云原生软件交付的开发和部署完全集成。InSpec 提供了一种简单易学的开源方法，可将安全性和法规遵从性要求作为代码直接纳入交付流程，从而确保应用程序和基础架构在交付过程的每一步都符合要求，而不仅仅是在流程的最后阶段

**支持数据**

*   行业和政府法规的数量、复杂性和影响都在增加。从零售业的 PCI，到医疗保健行业的 HIPAA，再到欧盟的个人数据 GDPR，我们付出了巨大的努力，他们的影响范围很广，不遵从法规的代价也很高。与 PCI 相关的罚款从每个事件每月 5000 美元到 100000 美元不等1；违反 HIPAA 最高可被罚款 150 万美元 2 ，与 GDPR 相关的罚款最高可达 2000 万欧元，或公司年收入的 4%，以较高者为准 3 。然而，在大多数情况下，评估和遵守的过程和程序仍然是临时的、任意的和人工的。
*   正如 Gartner 4 最近的一份报告所指出的，“手动流程既复杂又繁琐……人为错误不仅威胁到法规遵从性义务，还威胁到业务成果。审计员喜欢具有强大日志记录功能和透明可审计控制的自动化系统的一致性和可追溯性…随着自动化程度的提高，管理监督(包括检测和事件响应)变得更简单、更快速，并且可以根据需要由审计员进行测试，对 I&o .的压力更小
*   Chef 最近对 1，500 多名用户进行的 [调查](https://blog.chef.io/2018/01/30/2018-compliance-survey-compliance-lays-path-to-agility-for-software-delivery-with-detect-correct-automate-approach/) 发现，74%的跨职能应用程序、基础架构和安全团队在生产前手动评估软件的合规性。一旦发现违规和漏洞，一半是手动补救，而不是自动化流程。手动流程导致团队在数天(31%)或数周(19%)内检测和补救安全问题，而不是数小时(18%)。
*   正如 SANS Institute 最近的一篇论文 5 指出的，“要在大型混合云或公共云中扩展，安全将需要采用自动化，这是许多安全从业者一直不愿采用的概念。要让真正的 DevSecOps 站稳脚跟，安全团队需要将自动化测试和控制验证嵌入到部署周期中，并在生产中持续监控应用程序，触发响应，将控制回滚到已知的良好状态，以及其他结果。”

*1*[*http://www . focusonpci . com/site/index . PHP/PCI-101/PCI-non compliant-results . html*](http://www.focusonpci.com/site/index.php/pci-101/pci-noncompliant-consequences.html)

*2*[*https://www . ama-assn . org/practice-management/hipaa-violations-enforce*](https://www.ama-assn.org/practice-management/hipaa-violations-enforcement)

*3*[*https://www.eugdpr.org/key-changes.html*](https://www.eugdpr.org/key-changes.html)

*4**Gartner，* *如何**【H1】**在使用 DevOps* *时避免合规和审计顾虑发布时间:2017 年 11 月 17 日 ID: G00337518*

5[*https://www . sans . org/reading-room/whites/analyst/devsecops-playbook-36792*](https://www.sans.org/reading-room/whitepapers/analyst/devsecops-playbook-36792)

**关于 Chef**Chef 是持续自动化软件的领导者，云原生运营的创新者，DevOps 运动的创始人之一。Chef 与全球一千多家最具创新性的公司合作，以实现他们的数字化转型愿景，提供快速交付软件的实践和平台。[Chef Automate](https://www.chef.io/automate/)是 Chef 的持续自动化平台，由一个令人敬畏的社区和开源软件引擎提供支持:[Chef](https://www.chef.io/chef/)用于基础设施，[Habitat](https://www.habitat.sh/)用于云原生操作，[InSpec](https://www.inspec.io/)用于合规性。更多详情请访问[http://www . chef . io](http://www.chef.io)