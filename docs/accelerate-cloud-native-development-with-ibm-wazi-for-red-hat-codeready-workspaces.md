# 使用 IBM Wazi for Red Hat CodeReady 工作区加速云原生开发

> 原文：<https://devops.com/accelerate-cloud-native-development-with-ibm-wazi-for-red-hat-codeready-workspaces/>

**By Willie Tejada, GM and Chief Developer Advocate, IBM** 
Learning the ecosystem is one of the biggest challenges facing new IBM Z developers. It’s not enough that you’re new to the mainframe. You might also have to learn a new programming language and a new way to interact with a computer. Frequently, you’re forced to abandon your preferred IDE and instead use tooling that’s specific to IBM Z and your organization.
That’s why I’m thrilled to announce the availability of IBM Wazi for Red Hat CodeReady Workspaces (Wazi Workspaces). This environment addresses all of these onboarding challenges and, in the process, makes cloud-native development on IBM Z a reality.

Wazi Workspaces 为您提供了从各种 ide 中选择日常开发任务的能力。您可以使用 Red Hat CodeReady 工作区、浏览器内的 OpenShift-native 开发人员工作区、桌面上的 IDE(如 Microsoft VS Code)或基于 Eclipse 的 IDE(如 IBM Z Open Development)。最重要的是，Wazi Workspaces 提供了一个个性化的专用 z/OS 沙箱——运行在 Red Hat OpenShift 上——以加速开发和测试。

有了 Wazi Workspaces 环境，您可以使用自己选择的 IDE 为 z/OS 编写应用程序。然后，您可以在 x86 硬件上运行的 Red Hat OpenShift 上的个人 z/OS 沙箱中调试、构建和测试代码。沙箱运行真正的 z/OS——带有真正的 CICS、IMS、Db2、编译器等等——提供了一个成熟的开发环境。一旦您准备好了，您就可以将本地测试的更改从您的开发工作区直接签入到 Git，并触发构建和部署到容器化的 z/OS 沙箱中，作为 Jenkins 编排的标准 CI/CD 管道的一部分—在 Artifactory 或 Nexus 等流行的工件存储库中进行。所有这些都不需要直接访问 IBM Z 系统；您可以使用任何本地或基于云的 x86 OpenShift 环境。然后，您可以将这些应用程序部署到运行在 IBM Z 硬件上的本机 z/OS 的生产环境中。有了 Wazi Workspaces，真正的平台无关、企业范围的标准化——使用流行的开源和第三方工具作为 DevOps 工具链的一部分——成为现实。

所有这些是如何工作的？在 OpenShift UI 中，您只需运行 IBM Wazi 沙盒操作符。一旦沙盒启动并运行，您就可以打开首选的 IDE 并连接到沙盒来编辑、调试、构建和测试您的代码。这种灵活的环境赋予您的不仅仅是您自己的工具；您还有一个针对 z/OS 开发的个性化专用沙箱，针对 OpenShift 进行了优化。再一次，我们能够提供一个环境，让开发人员能够构建智能和安全的环境。

Red Hat 的高级工程总监 Adi Sakala 总结道:“随着组织经历数字化转型之旅，使其数据中心和开发团队现代化以采用混合云模型，Z 的原生开发将继续发挥关键作用。在这个过程中，大多数组织面临的挑战是对容器化开发以及 z/OS 相关工具的需求不断增长。当前的世界形势使得许多组织，包括那些有大量 Z 投资的组织，在扩展他们的应用程序的同时，重新思考和重组他们的开发团队。IBM Wazi for Red Hat Code Ready work spaces 为组织提供了为 Red Hat OpenShift 高效地交付 z/OS 应用程序的机会，并使 z/OS 开发团队能够在容器原生应用程序上进行协作。IBM Wazi 建立在 Red Hat Code Ready 工作区之上，并针对 Red Hat OpenShift 进行了优化。

在[IBM Wazi for Red Hat CodeReady work spaces 页面](https://www.ibm.com/products/wazi-for-red-hat-codeready-workspaces) 上了解更多信息，包括如何开始。请访问 IBM 应用平台副总裁 Danny Mace 发布的 [这篇博文](https://www.ibm.com/cloud/blog/announcements/ibm-wazi-for-red-hat-codeready-workspaces) ，从更高的层面了解 IBM Wazi 如何融入 IBM Z 的云原生开发故事