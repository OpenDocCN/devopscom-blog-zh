# 裂变开源无服务器框架提供了实时重载、金丝雀部署、记录回放等更多特性，以提高 Kubernetes 上无服务器应用程序的质量并简化其发布自动化

> 原文：<https://devops.com/fission-open-source-serverless-framework-offers-live-reload-canary-deployments-record-replay-more-features-to-improve-the-quality-and-simplify-release-automation-of-serverless-applications-on-kuber/>

*实时重新加载、记录回放、自动 Canary 部署、Prometheus 集成等等，让开发人员和运营人员对无服务器应用的生产就绪性充满信心，同时还能轻松排除故障，优化成本/性能*

加利福尼亚州森尼维尔—2018 年 10 月 16 日—SaaS 管理的混合云的领导者 platform 9([https://platform9.com/](http://icm-tracking.meltwater.com/link.php?DynEngagement=true&H=FcQ5do3Mtm%2F2JnP%2FxXFcY%2BL9mOkU%2Fad4G7kfqxVfSdkEEq1vNf2gy8Wq6j0ZhwPi7DcEbUyl6hQ9JmhW1n%2FOQLnigeVvBUfFdeJuP6x%2FULWfFM96URAw5Q%3D%3D&G=0&R=https%3A%2F%2Fplatform9.com%2F&I=20181016124942.0000002ec8ac%40mail6-41-usnbn1&X=MHwxMDQ2NzU4OjViYzUwMTRkYmQ3OTdkYzNiZjc2YjE3MDs%3D&S=dZGEK-ilegp6F9n7zAk1ysDsdr1IxSDzdTAWC9nqTCY))今天宣布了一个新版本的裂变. io——流行的开源 Kubernetes——原生无服务器框架——新功能使开发人员和 IT 运营人员能够提高无服务器应用的质量和可靠性。

 裂变是业内第一个无服务器解决方案，提供内置的实时重新加载和记录回放功能，以简化测试和加速反馈循环。其他新功能包括自动化金丝雀部署以降低失败发布的风险，Prometheus 集成以实现自动化监控和警报，以及细粒度的成本和性能优化功能。在这个最新版本中，裂变提供了最完整的功能集，允许开发和运营团队安全地采用无服务器，并在任何环境中(无论是公共云还是内部部署)受益于这种云原生开发模式的速度、成本节约和可扩展性。

【https://fission.io/】**)了解更多关于裂变、开源、Kubernetes-native 的无服务器框架。**

“创建裂变的目的是为开发人员提供一种更简单、更容易的方式来加速 Kubernetes 的价值实现。我们的目标是帮助开发人员生成高质量的无服务器代码，并为运营团队提供在生产中运行无服务器应用的最大信心，”Platform9 的创建者 Soam Vasani 说。“无服务器允许开发人员更快地行动，提高工作效率。裂变的最新版本专注于加速反馈循环和降低部署风险，以确保团队不仅可以快速移动，而且可以安全地大规模移动。”

**裂变的最新特性集包括:**

**-实时加载:随打随测**

通过 Live-reload，当代码被写入实时 Kubernetes 测试集群时，裂变会自动部署代码，并允许开发人员在他们的开发环境和函数运行时之间切换，以快速迭代他们的编码和测试周期。

这允许在应用程序开发生命周期中更早地发现并修复错误，因为这样做成本更低——在更高的环境中发现错误或导致生产中的任何服务中断之前。此外，通过使用与配置和相关服务(即数据库、API 调用等)一致的实时环境在流程的早期运行集成测试，它简化并提高了集成测试的保真度。)在生产中使用。

**记录回放:简化测试调试**

裂变是首款无服务器解决方案，提供开箱即用的记录回放功能，便于测试和故障排除。Record-replay 自动保存触发无服务器功能的事件，并允许根据需要重放这些事件，提供有关应用程序使用方式、功能输入和输出的详细信息。裂变用户可以配置记录哪些功能和工作流，以及记录的事件保留多长时间。

Record-replay 被开发人员用来重现测试或调试过程中的复杂故障，简化回归测试，并解决问题(即根据过去的输入检查功能的执行)。此外，运营团队通常能够记录部分实时生产流量，以帮助工程师重现问题或验证应用程序更新。

**自动化金丝雀部署:降低失败释放的风险**

Canary 部署是一种行之有效的部署策略，可最大限度地降低应用发布失败的风险，并避免最终用户的服务中断。在这种策略中，应用程序的新版本首先只部署到一小部分实时流量中，然后在版本稳定后逐步推广到生产中。在生产失败的情况下，应用程序可以回滚到以前的稳定版本。

裂变是第一个提供易于配置的全自动 Canary 部署的开源无服务器框架。这使得 DevOps 团队和站点可靠性工程师无需手动管理金丝雀或投资繁琐的脚本和测试来执行这一高级部署策略，从而使其直观、易于使用且无错误。最终，这将最大限度地降低应用程序的停机风险。

通过自动化的 Canary 部署，只要成功，裂变会自动将流量比例增加到新版本的功能，如果新版本失败，则回滚到旧版本。用户可以配置接收新版本功能的流量百分比、构成故障的错误率以及推出新版本的发布率。

**普罗米修斯集成:简易指标收集与提醒**

与 Prometheus 的现成集成支持自动聚合函数指标，包括调用函数的数量、函数执行时间、成功、失败等等。用户还可以为关键事件定义自定义警报，例如当功能失败或执行时间过长时。Prometheus metrics 还可以提供监控仪表板来可视化应用程序指标。

**裂变中的成本优化**

由于裂变是开源的，可以在任何 Kubernetes 集群上工作，它使企业能够在任何基础设施上轻松运行类似 Lambda 的无服务器服务——使用公共云上更便宜的实例，或者利用他们自己的数据中心。为了让 IT 最大限度地提高公共云和内部资源的基础设施利用率，裂变提供了细粒度的成本和性能优化控制。

无服务器功能可以配置特定的 CPU 和内存资源使用限制、最小/最大实例数量和自动缩放参数。这些参数允许使用最适合特定业务用例的执行策略来调整功能。例如，具有严格成本约束的功能可以按需部署到容器中，以性能为代价最小化成本。相反，需要性能高于所有其他要求的功能可以配置为让实例始终运行，确保低延迟，但会增加成本。函数还可以利用裂变的预热容器池，它将大量函数的池化成本加在一起，同时为所有函数提供性能优势。

“我们的全球照片平台通过将数千种定制产品上所有他们喜爱的照片结合起来，帮助数亿忠实用户保存他们的记忆。我们一直在寻找方法来改善我们管理应用规模和质量的方式。Snapfish 技术总监 Kenneth Lam 表示:“这些新的裂变功能将帮助我们的开发人员提供基于无服务器应用程序的新客户体验，而无需依赖管理规模的复杂性。“裂变使我们的公司能够在我们选择的任何环境中受益于云原生开发模式的速度、成本节约和可扩展性，无论是公共云还是本地云。”

**安装最新版本的裂变，访问:**[**(****https://裂变. io**](http://icm-tracking.meltwater.com/link.php?DynEngagement=true&H=FcQ5do3Mtm%2F2JnP%2FxXFcY%2BL9mOkU%2Fad4G7kfqxVfSdkEEq1vNf2gy8Wq6j0ZhwPi7DcEbUyl6hQ9JmhW1n%2FOQLnigeVvBUfFdeJuP6x%2FULWfFM96URAw5Q%3D%3D&G=0&R=https%3A%2F%2Ffission.io%2F&I=20181016124942.0000002ec8ac%40mail6-41-usnbn1&X=MHwxMDQ2NzU4OjViYzUwMTRkYmQ3OTdkYzNiZjc2YjE3MDs%3D&S=1uRXdJKh93VnPacaR-du2M8WEYC1xWooYcPYHhF_OLc) **)。**

**分享一下:**新的@fissionio 特性包括 Live-reload，Record-replay，自动化#Canary 部署，#Prometheus，以及更多提高质量和降低风险的# Kubernetes # FAAS[https://platform9.com/press/<wbr>裂变-开源-<wbr>server less-framework-offers-<wbr>Live-reload-Canary-<wbr>部署-Record-replay-<wbr>more-改善质量-发布- <wbr>自动化-server less-on-<wbr>](http://icm-tracking.meltwater.com/link.php?DynEngagement=true&H=FcQ5do3Mtm%2F2JnP%2FxXFcY%2BL9mOkU%2Fad4G7kfqxVfSdkEEq1vNf2gy8Wq6j0ZhwPi7DcEbUyl6hQ9JmhW1n%2FOQLnigeVvBUfFdeJuP6x%2FULWfFM96URAw5Q%3D%3D&G=0&R=https%3A%2F%2Fplatform9.com%2Fpress%2Ffission-open-source-serverless-framework-offers-live-reload-canary-deployments-record-replay-more-improve-quality-releases-automation-serverless-on-kubernetes%2F&I=20181016124942.0000002ec8ac%40mail6-41-usnbn1&X=MHwxMDQ2NzU4OjViYzUwMTRkYmQ3OTdkYzNiZjc2YjE3MDs%3D&S=s6P-8KI98tDaRwwky8SPqo609_FvGQfn1Y87AyZbnzI)

**关于平台 9**

platform 9([platform9.com](http://icm-tracking.meltwater.com/link.php?DynEngagement=true&H=FcQ5do3Mtm%2F2JnP%2FxXFcY%2BL9mOkU%2Fad4G7kfqxVfSdkEEq1vNf2gy8Wq6j0ZhwPi7DcEbUyl6hQ9JmhW1n%2FOQLnigeVvBUfFdeJuP6x%2FULWfFM96URAw5Q%3D%3D&G=0&R=https%3A%2F%2Fwww.platform9.com%2F&I=20181016124942.0000002ec8ac%40mail6-41-usnbn1&X=MHwxMDQ2NzU4OjViYzUwMTRkYmQ3OTdkYzNiZjc2YjE3MDs%3D&S=ZdlToNLoWev6qNzpeLOaFyr8nNEVVMIrPR_0MeYjUjo))提供了一个 SaaS 管理的混合云解决方案，可以将现有的基础设施立即转变为云。我们帮助企业推动数字化转型，使他们能够管理任何基础设施上的虚拟机、容器和无服务器功能，无论是在内部、公共云中还是在边缘，并提供简单统一的自助式体验。Cadence、Autodesk、Veritas、Nanometrics、EBSCO、Bitly、LogMeIn 和 Aruba 等客户的 IT 效率提高了 300 %,上市时间缩短了 33 %,数据中心利用率和成本降低了 50-80%。该公司总部位于加利福尼亚州森尼韦尔，由红点风险投资公司、门洛风险投资公司、帆布风险投资公司和 HPE 公司提供支持。