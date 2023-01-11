# 在 SRE 定义可用性、可维护性和可靠性

> 原文：<https://devops.com/defining-availability-maintainability-and-reliability-in-sre/>

在可靠性工程领域，你会经常遇到三个“能力”词:可用性、可维护性和可靠性。听起来很像，意思也差不多。事实上，这些词可能看起来如此相似，以至于很容易将它们互换使用。

那将是一个错误。可用性、可维护性和可靠性都有不同的(如果相关的话)含义，它们在可靠性操作中扮演不同的角色。

## 可用性、可维护性和可靠性的定义

让我们从简洁地定义每个术语开始。

## 可用性，已定义

可用性是指 IT 资源在被请求时准备好执行任务的程度。

因此，响应请求的应用程序或服务器是可用的(即使响应时间比预期的长，或者运行不佳，在这种情况下，可能有可靠性问题，但没有可用性问题)。

可用性通常以百分比来衡量。例如，可用性为 99%的资源在 99%的时间里都在运行和响应。

## 可维护性，已定义

可维护性是当出现问题时，资源修复的速度和容易程度的度量。

如果一个有问题的应用程序版本可以通过回滚到一个稳定的版本来快速修复，那么这个应用程序将具有高度的可维护性。另一方面，如果您有一个服务器，在它出现故障后需要手动重建，那么它就不太容易维护。

## 可靠性，已定义

可靠性是指资源根据请求发挥作用的程度(相对于简单的可用性)。

例如，如果您的用户需要一个应用程序在一秒钟内处理每一个事务，并且它在 99%的时间里都这样做，同时还保持 99%的可用性级别，那么这将是一个相对可靠的应用程序。相比之下，响应几乎所有请求但遭受高延迟或高错误率的应用程序将不是非常可靠，尽管它可能是高度可用的。

## 可用性、可维护性和可靠性之间的差异

阐明可用性、可维护性和可靠性之间区别的最简单的方法是突出每个概念的独特之处。

### 有效性

与可维护性和可靠性不同，可用性本质上是一个二元[度量](https://devops.com/?s=metrics)，在这个意义上，系统要么可用，要么不可用。尽管可用性状态会随着时间的推移而变化，但是不存在可用性程度的变化。

可用性也很突出，因为它通常是定义[SLA 和](https://rootly.io/blog/practical-guide-to-sre-using-slos-to-increase-reliability)SLOs 的最重要指标。合同通常指定资源将达到一定的可用性级别，以百分比的形式定义。他们有时还可能指定响应时间等指标，这些指标反映了可靠性，但可用性更可能是服务协议中最重要的指标。

### 可维护性

可维护性的独特之处在于它是一个非常主观的概念。一个被一个[](https://rootly.io/blog/what-is-an-sre)认为容易维护的系统对另一个 SRE 来说似乎很难维护。工程师用来优化可维护性的方法也可能不同；例如，来自 [DevOps 背景](https://rootly.io/blog/should-you-be-an-sre-or-a-devops-engineer) 的人可能比受过 [经典站点可靠性工程](https://rootly.io/blog/sre-vs-devops-what-are-the-differences) 培训的人更关注软件交付链中的可维护性优化，后者更关注通过代码实现 IT 操作自动化，而不是软件交付过程。

也就是说，[自动化](https://devops.com/?s=automation)工具帮助几乎每个团队最大化可维护性，不管他们的偏好或背景如何。

### 可靠性

可靠性之所以突出，是因为它反映了系统运行的好坏。同样，这是一个有点主观的指标，因为不同用户的性能需求可能不同。尽管如此，可靠性是衡量系统是否满足其所需性能水平的最有效手段，即使这些要求会随着时间的推移而改变。

## 为什么可用性、可维护性和可靠性很重要？

因为可用性、可维护性和可靠性分别衡量系统状态的不同方面，所以将它们放在一起是深入了解系统整体可靠性的有效方法。

为了可靠，系统需要可用性和可维护性。如果一个系统不可用，它就不可能可靠。如果由于低可维护性而花费很长时间来修复问题，它也不太可能是高度可靠的。

同时，通过分别关注可用性、可维护性和可靠性，您可以深入到您管理的 IT 资源中的特定问题。例如，当系统可用时，您可能拥有高性能的系统，但是由于可用性问题，系统的可靠性很低。在这种情况下，您将知道在提高可用性方面的投资可能会为提高整体可靠性带来最大的回报。

## 底线

底线:虽然可用性、可维护性和可靠性都是 IT 资源质量的反映，但它们以不同的方式衡量质量。单独跟踪每个类别对于确保您了解整个系统性能和运行状况中最薄弱的环节非常重要。

但是，与此同时，比较和关联可用性、可维护性和可靠性数据也很重要，这样您就可以持续了解资源的状态。当您可以单独跟踪每个项目，也可以将它们组合在一起以获得系统的完整视图时，您就处于优化可靠性操作的最佳位置。