# DevSecOps 与敏捷开发:将安全性置于程序开发的核心

> 原文：<https://devops.com/devsecops-vs-agile-development-putting-security-at-the-heart-of-program-development/>

尽管大多数开发人员和管理人员都很清楚 DevSecOps 的概念，但它仍然经常与许多相关的过程和概念相混淆。对于国防部(DoD)的承包商来说尤其如此，因为他们长期以来一直被鼓励使用一种被称为敏捷开发的相关过程。

由于敏捷开发已经存在了十多年，组织倾向于将 DevSecOps 视为它的扩展，甚至是同义词。但实际上，这两种方法是截然不同的。这两种方法的目标是相似的:[](https://devops.com/the-best-approach-to-help-developers-build-security-into-the-pipeline/)[早期检测风险](https://devops.com/5-ways-to-detect-application-security-vulnerabilities-sooner-to-reduce-costs-and-risk/) 并且都关注 [云-本机安全性和性能](https://devops.com/cloud-native-security-and-performance-two-sides-of-the-same-coin/) 。

然而，尽管 DevSecOps 确实建立在一些敏捷开发原则之上，例如软件系统的持续集成和循环交付，但它从过程开始就强调集成安全特性，而敏捷只关注软件的交付。

在这篇文章中，我们将看看敏捷开发和真正的 DevSecOps 过程之间的主要区别，以及它们是如何相互补充的。

## **开发团队与敏捷开发**

DevSecOps 和敏捷开发方法之间的区别可以参考软件开发的一个方面来理解:安全性。在这两种方法中，何时、何地以及由谁在软件开发中实现安全性是不同的。

敏捷开发方法关注迭代开发周期，在迭代开发周期中，反馈被不断地整合到正在进行的软件开发中。然而，即使在成熟的敏捷开发过程中，安全性仍然经常作为事后的想法添加到软件中。这不应该被解读为指责软件开发商经常低估恶意软件[](https://surfshark.com/blog/what-is-malware)的潜在危害，或者忽视网络安全的重要性。

相反，在许多公司中，考虑代码的安全含义根本不是开发人员的责任，因为软件在发布前会被交给安全团队。

DevSecOps 将安全性放在与持续集成和交付同等的高度。DevSecOps 方法在开发的最初阶段就强调安全性，并使安全性成为整个软件质量的重要部分。

从本质上来说，这些方法将项目经理的视角从确保软件符合规范或满足规范或审计转移到确保代码编写正确、安全，并以可重复的方式部署。

## **国防部文化的变化**

采用 DevSecOps 方法对国防部承包商至关重要，因为这些方法反映了国防部自己的现代化战略。继在所有类型的系统中发现 [高调漏洞](https://www.military.com/daily-news/2020/02/25/dod-agency-suffers-data-breach-potentially-compromising-ssns.html) 之后，国防部似乎已经发布了网络安全弱点不仅是对关键国防数据的潜在威胁，而且还对功能的持续交付造成了重大的运营瓶颈。

目前，即使那些拥有成熟的敏捷开发框架的公司也会发现，在交付之前，必须对软件执行的多重安全检查和遵从过程会对他们交付迭代软件改进的能力产生不利影响。这就是 [过渡到 DevSecOps](https://hub.packtpub.com/why-do-it-teams-need-to-transition-from-devops-to-devsecops/) 试图克服的问题，试图将组织的网络安全方法从合规性转向真正的安全意识。

与此同时， [分析家们意识到](https://www.afcea.org/content/devsecops-puts-security-heart-program-development-sponsored) 对于许多国防部承包商来说，将网络安全的责任转移到开发人员身上将是不舒服的，而且可能是危险的。从事军用软件基础代码工作的开发人员没有——也不希望有——对其将被部署的所有环境以及他们的软件将被要求与哪些系统接口有详尽的了解。

## **自动化和新模式**

为了应对这些问题，国防部承包商正在重新评估 DevSecOps 模型，并认真考虑如何在连续服务交付至关重要的环境中部署该模型。这种情况有三种主要方式。

首先是自动化的兴起。大多数当代国防部项目所依赖的大规模、多云基础设施的类型可能经常需要在开发和安全团队之间进行重复、持续的维护和安全评估。DevSecOps 用自动化系统取代了这些人工检查:这不是要求一个人检查数百个控制的清单，而是作为软件开发和供应过程管道的一部分自动完成的。

过渡到 DevSecOps 的第二个关键因素是终端安全性。国防部承包商传统使用的整体开发过程类型不适合许多国防部项目的当代部署环境。在这些传统的方法中，系统被构建为离散的洞，不期望数据在组件之间移动时会被暴露。

这现在是一种过时的方法:在 DevSecOps 流程中，虚拟专用网络用于 [提供安全性，并在数据在网络中移动时对数据](https://privacyaustralia.net/#what_is_a_vpn_and_how_does_it_work) 进行加密，而 [最低权限原则](https://www.twilio.com/blog/principle-of-least-privilege-details-best-practices) 减少了员工对一小部分 it 环境的访问。

第三，国防部新一代年轻的军事和文职人员，他们中的许多人是在商业部门接受培训，而不是从大学直接进入军队，他们正在将公司方法引入军用软件的开发。这体现在国防部应用中云服务的使用呈指数级增长，以及在整个组织中分配安全责任的更加动态和分布式的管理框架，而不是将此作为专门安全团队的唯一职责。

## **获得支持**

对于许多承包商来说，转向真正的 DevSecOps 方法可能是一个挑战。然而，正如在过去的十年中，许多公司不得不重新设计他们的开发生命周期以保持敏捷，现在他们需要实现 [安全的开发生命周期](https://devops.com/the-secure-software-development-life-cycle-syncing-development-and-security/) 以保持竞争力。

如果你正在寻求这种转变，你也应该认识到你并不孤单。国防部正与其合作伙伴积极合作，以促进 DevSecOps 流程的推广，并使商业工具和技术对军事承包商可用和有用，因为国防部认识到这种方法对他们委托的软件的价值。

这一点在微软 Azure Government 的最近更新 [中看得最清楚，尽管你也应该知道国防后勤局最近发布的许多资源](https://www.microsoft.com/en-us/us-partner-blog/2019/05/28/microsoft-azure-government-security-capabilities-for-partners/)[](https://www.dla.mil/HQ/InformationOperations/Offers/Services/FIC/ContractorCyberResources/)也集中在向 DevSecOps 的过渡上。

简而言之，虽然向 DevSecOps 的过渡可能具有挑战性，但它不会比早期向敏捷开发的过渡更具挑战性。然而，为了实现这种转变，公司应该利用他们可用的资源，认识到将安全性集成到他们的开发工作流中的价值，并建立在现有的敏捷框架上。