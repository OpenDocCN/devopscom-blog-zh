# 只有 30%的组织完全实施了 DevSecOps

> 原文：<https://devops.com/only-30-of-orgs-fully-implement-devsecops/>

随着更快发布的压力，在大多数组织中，安全性在[持续开发管道](https://devops.com/how-to-scale-microservices-ci-cd-pipelines/)中向左移动。随着网络攻击的增加，这种必要性越来越大。然而，最近的一项 CSA 研究发现，缺乏培训和低能见度阻碍了许多 DevSecOps 的推出。

DevSecOps 仍然是一个相对较新的实践，在大多数组织中尚未成熟。尽管几乎所有公司都在努力，但只有 30%的安全专业人员表示他们在实践中完全实施了 DevSecOps。这使得大多数组织处于某种发展合作构想和规划的状态。

CSA 最近发布了趋势科技委托的[安全开发和误配置 2021 报告](https://cloudsecurityalliance.org/artifacts/secure-devops-and-misconfigurations-survey-report/)。该报告发现，错误配置通常源于默认的安全设置。缺乏内部指导和安全资源的可访问性通常也会阻碍 DevSecOps 的成熟。

下面，我将回顾报告中的其他主要内容，看看它们如何在组织开始实施 DevSecOps 时为组织提供信息。

## DevSecOps 的采用情况

[DevSecOps](https://devops.com/6-traits-that-define-devsecops/) 旨在提高快速部署的安全性。它通过将[安全自动化](https://containerjournal.com/topics/container-security/the-last-cloud-native-puzzle-piece-security-automation/)转移到左边并将开发运维团队和 It 安全团队之间的[边界分离，将安全放入开发运维团队。](https://devops.com/bridging-the-appsec-and-devops-disconnect/)

虽然大多数工程师都意识到了 DevSecOps 的好处，但每个组织的 DevSecOps 之旅的*状态*却大不相同。虽然令人印象深刻的是，90%的组织都处于 DevSecOps 之旅的某个阶段，但只有 30%的组织正在实施 DevSecOps，24%的组织处于规划阶段，18%的组织正在设计，18%的组织仍在完善其 DevSecOps 战略。超过十分之一的安全专家表示，他们的团队根本没有投资 DevSecOps 的计划。

展望未来，42%的受访者表示他们将在未来 12 个月内实施完整的 DevSecOps。但是由于它目前的新生状态，错误的配置仍然存在。这些错误配置的主要原因是有缺陷或缺乏内部指导(33%)。

许多专业人士表示，关于漏洞和错误配置，根本没有足够的培训、支持或内部知识。错误配置的其他主要原因包括不安全的默认设置(18%)和疏忽(16%)。

除了错误配置之外，组织还报告了身份、授权和访问方面的挑战。确保正确的权限对于避免升级攻击至关重要，升级攻击是一个普遍存在的问题。在 2019 年至 2020 年期间， [80%的公司](https://www.businesswire.com/news/home/20200603005175/en/Ermetic-Reports-Nearly-80-of-Companies-Experienced-a-Cloud-Data-Breach-in-Past-18-Months)经历了某种形式的数据泄露，其中许多是由于错误配置的访问控制。 [OWASP](https://owasp.org/www-project-api-security/) 还报告称，破坏授权是高流量 web API 端点的一大漏洞。

## 常见威胁缓解实践

为了减轻这些威胁，开发和安全团队必须保持最佳实践，然而某些问题阻止了 DevSecOps 的出现。例如，60%的安全专业人员表示，他们面临的最大挑战是对安全或法规遵从性差距的可见性不足，这是目前最常见的挑战，11%的人还提到了不一致的云客户入职。最后，10%的人说耗时、缓慢和/或不足的架构阻碍了他们的发展。

减轻威胁的一种方法是更频繁地引入常规安全审查。然而，这里很难设定一个明确的基准，因为组织审查其云基础架构的漏洞或错误配置的频率差异很大。根据调查，目前有 22%的公司每天、22%的公司每月、18%的公司每周和 23%的公司每季度进行这样的安全检查。随着 DevSecOps 在开发生命周期中变得越来越普遍和自动化，这个比率可能会增加。

与现代安全框架保持同步是影响 DevSecOps 采用的另一个方面；组织倾向于遵循多种框架来制定他们的安全策略。超过四分之三(78%)遵循国家标准与技术研究所(NIST)的指导方针，67%遵循互联网安全中心(CIS)的基准，66%遵循云安全联盟(CSA)，54%遵循国际标准化组织(ISO)，44%表示遵循亚马逊网络服务(AWS)的安全建议。

例如，政府运营的标准制定机构 NIST 最近制定了网络安全指导方针，建议跨部门使用零信任和服务网络。这些安全指南可以被认为是架构基准，特别是对于大型的、[高度管制的行业](https://containerjournal.com/features/going-cloud-native-in-highly-regulated-industries/)。

## DevSecOps 培训类型

最后，投资社区资源和培训是提高 DevSecOps 意识的另一种方式。只有一半的调查受访者报告说他们的 DevSecOps 最佳实践资源是可访问的，因此，领导者有责任在他们的组织内使这些知识民主化。

大多数(81%)受访者认为在线文章和培训是他们了解云安全工具和供应商的主要形式。研讨会、会议和网络研讨会紧随其后。组织还采用许多内部知识共享方法来应对突发事件。整整 85%的受访者表示，他们会进行认知培训，然后是桌面练习(52%)、攻击模拟(45%)和协议或响应框架培训(37%)。

## 云中的未来发展合作

看起来大多数团队仍然在制定他们的 DevSecOps 策略。但是展望未来，42%的人表示他们将在未来 12 个月内实施完整的 DevSecOps。与此同时，整个行业预计会受到更多云的推动。

目前，40%的组织有 41%到 99%的工作负载在公共云中。55%的组织在未来一年将有 41%到 99%的工作负载位于公共云中。随着越来越多的组织转向[容器平台](https://containerjournal.com/features/when-using-kubernetes-does-and-doesnt-make-sense/)、功能即服务和其他无服务器功能，工作负载的类型也可能在未来一年发生变化。为了充分获得这些新技术带来的好处，组织无疑必须应对一类新的[云原生漏洞](https://containerjournal.com/topics/container-security/insecure-defaults-remain-a-threat-for-kubernetes/)。

### 关于报告

云安全联盟(CSA)是一个非营利组织，其使命是广泛推广确保云计算和 it 技术网络安全的最佳实践。安全开发和错误配置调查于 2021 年 7 月至 2021 年 9 月进行，收集了来自不同行业和组织规模的全球 IT 安全专业人员的 900 多份回复。要获得报告的完整副本，您可以在此用一些个人信息换取 PDF 下载。