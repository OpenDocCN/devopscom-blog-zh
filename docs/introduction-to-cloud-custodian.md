# 云托管简介

> 原文：<https://devops.com/introduction-to-cloud-custodian/>

组织继续增加他们在云中的足迹。然而，跨[多个云环境](https://accelerationeconomy.com/cybersecurity/hybrid-multi-cloud-is-the-new-normal/)大规模应用治理和实施策略是一项具有挑战性的工作。组织通常有用英语编写的治理策略，但是将它们转换成可执行的代码在历史上需要一些定制的变通方法。与基础设施即代码(IaC)一样，DevOps 工程师现在也在寻求一种类似的 GitOps 方法来跨基于云的工作负载实施共享策略。

[云托管者](https://cloudcustodian.io/)就是这样一个工具集，它能够以标准化的格式管理和执行云策略。使用云托管，云卓越中心就拥有了创建安全治理、开发护栏和云成本优化策略的构建模块。这个免费的开源项目多年来一直在稳步发展，最近[获得了云计算原生计算基金会(CNCF)的孵化资格](https://www.cncf.io/blog/2022/09/14/cloud-custodian-becomes-a-cncf-incubating-project/)，迄今为止在 [GitHub](https://github.com/cloud-custodian/cloud-custodian) 上已经有超过 350 名贡献者。

我会见了云托管的创建者和维护者、Stacklet 的 with Kapil Thangavelu，以了解更多关于云托管的信息，以及在不久的将来我们应该从该项目中获得哪些功能。下面，我们将全面介绍云托管，探索它的历史，如何使用它及其核心优势。我们还将分析几个样本策略，展示云托管在实践中是如何运作的。

## 什么是云托管？

Thangavelu 解释说,“云托管”是 2015 年底在 Capitol One 内部开发的内部工具。当时，工程师们正在努力应对新发现的大规模管理云的现实，并意识到跨团队的一次性特别策略正在引起摩擦。Thangavelu 说:“大规模地管理和执行政策真的很难。因此，工程师们考虑创建一种更 GitOps 的治理和安全策略方法，可以作为内部 SaaS 解决方案运行。

于是，云护法诞生了。YAML DSL 工具允许您轻松定义管理云基础设施的规则。它可以提供实时执行并产生基于事件的响应。例如，您可以创建要求对资源进行标记的策略，或者在非工作时间关闭实例的策略。或者，策略可以防止没有适当权限的开发人员不小心打开负载平衡器。云托管支持 AWS、Azure 和 GCP，并且策略被指定给资源类型，无论是 EC2、ASG、红移、CosmosDB 还是 PubSub 主题。

Thangavelu 将云管理员描述为一堆乐高积木，开发者可以用任意方式捡起来建造护栏。他说，“云监管者让定制本身成为一等公民”，而不是与固定的规则集一起运输。Capital One 开源了该项目，并于 2020 年 8 月向 CNCF 提供了云托管服务。

## 示例策略

云保管人附带了一个动作和过滤器库。让我们看一下三个主要云提供商的一些示例策略。但是首先，要从 [PyPI](https://pypi.org/project/c7n/) 安装云托管器，您可以启动以下命令:

```
$ python3 -m venv custodian
$ source custodian/bin/activate
(custodian) $ pip install c7n 
```

让我们考虑一个可以提高 AWS 安全性的示例策略。下面是一个这样的策略，它创建了一个 CloudWatch 事件，当用户从一个无效的 IP 地址登录时就会触发该事件。这可用于 ping 安全管理员进行调查。根据这一规则，还可以打开自动修复功能。

```
policies:

  - name: invalid-ip-address-login-detected
    resource: account
    description: |
      Notifies on invalid external IP console logins
    mode:
       type: cloudtrail
       events:
          - ConsoleLogin
    filters:
      - not:
          - type: event
            key: 'detail.sourceIPAddress'
            value: |
               '^((158\.103\.|142\.179\.|187\.39\.)([01]?[0-9]?[0-9]|2[0-4][0-9]|25[0-5])
               \.([01]?[0-9]?[0-9]|2[0-4][0-9]|25[0-5]))|(12\.([01]?[0-9]?[0-9]|2[0-4][0-9]|25[0-5])
               \.([01]?[0-9]?[0-9]|2[0-4][0-9]|25[0-5])\.([01]?[0-9]?[0-9]|2[0-4][0-9]|25[0-5]))$'
            op: regex
    actions:
      - type: notify
        template: default.html
        priority_header: 1
        subject: "Login From Invalid IP Detected - [custodian {{ account }} - {{ region }}]"
        violation_desc: "A User Has Logged In Externally From A Invalid IP Address Outside The Company's Range:"
        action_desc: |
            "Please investigate and revoke the invalid session along
            with any other restrictive actions if appropriate"
        to:
          - [[email protected]](/cdn-cgi/l/email-protection)
          - [[email protected]](/cdn-cgi/l/email-protection)
        transport:
          type: sqs
          queue: https://sqs.us-east-1.amazonaws.com/12345678900/cloud-custodian-mailer
          region: us-east-1 
```

接下来，让我们考虑一个策略，它将为在 Azure 上工作的开发人员增加某种程度的治理。一个简单但受欢迎的策略是给单个资源标记所有权细节。因此，该策略将使用创建者的电子邮件地址标记所有资源组:

```
policies:
  - name: azure-auto-tag-creator-resource-groups
    resource: azure.resourcegroup
    description: |
      Tag all existing resource groups with the 'CreatorEmail' tag; looking up to 10 days prior.
    actions:
     - type: auto-tag-user
       tag: CreatorEmail
       days: 10 
```

最后，让我们考虑一项有助于 GCP 成本优化的政策。下面是一个在 GCP 上对自动缩放器强制实施[最小 CPU 利用率的策略示例。实施这样的政策有助于避免利用不足，以应对](https://cloudcustodian.io/docs/gcp/examples/gce-autoscaler.html)[不断上升的云成本](https://devops.com/how-to-respond-to-rising-cloud-costs/)。

```
vars:
  min-utilization-target: &min-utilization-target 0.8
policies:
  - name: gcp-autoscalers-enforced
    resource: gcp.autoscaler
    mode:
      type: gcp-audit
      methods:
        - v1.compute.autoscalers.insert
    filters:
      - type: value
        key: autoscalingPolicy.cpuUtilization.utilizationTarget
        op: less-than
        value: *min-utilization-target
    actions:
      - type: set
        cpuUtilization:
          utilizationTarget: 0.8 
```

## 云托管的优势

通过自动化大量繁琐的策略管理，云托管可以通过更加简化的云治理来降低风险和事故。Thangavelu 说:“当每个人都有基础设施时，它就解决了自然问题。”。通过聚合临时脚本和统一整个组织的策略，您可以立即启动新规则，而无需手动提醒组织的所有成员，这可能需要数年时间。

对于那些熟悉[开放策略代理(OPA)](https://containerjournal.com/features/introduction-to-open-policy-agent-opa/) 的人来说，您可能会注意到一些目标上的重叠，因为两者都是制定云原生策略的引擎。与 OPA 相比，云托管有一些开发者体验津贴。首先，您不必使用减压阀，因为策略是用 YAML 语言编写的，这是 DevOps 工程师熟悉的配置语言。云托管人对每个云提供商的事件运行时进行抽象。此外，Thangavelu 说，与 OPA 相比，你不需要为特定的问题领域绑定引擎，因为云托管专门绑定到云治理和管理。

云托管也是久经考验的。许多大公司都在生产中使用它，包括 Capital One、HBO Max、Intuit Inc、JP 摩根大通、西门子和 Zapier。在整个采用过程中，该工具往往要么被卓越云中心、安全团队用来进行报告或揭示实时事件，要么被首席财务官用来指导成本优化。

## 云托管的未来

云托管维护者将该项目描述为一个一致的消防站。由于该项目实时跟踪所有云提供商资源的变化，所以它是一个相当动态的工具集。除了每月更新，用户还可以期待许多其他更新，包括对腾讯云的支持以及其他 Kubernetes 支持。Thangavelu 说，正在围绕左移功能做额外的工作，以满足开发人员的需求。

要了解更多信息，请查看云托管的[快速入门指南，或者在此](https://cloudcustodian.io/docs/quickstart/index.html)查看项目[路线图。](https://github.com/orgs/cloud-custodian/projects/1/views/1)