# PagerDuty 宣布为 CloudWatch、GuardDuty、CloudTrail 和个人健康仪表板提供新的 AWS 集成

> 原文：<https://devops.com/pagerduty-announces-new-aws-integrations-for-for-cloudwatch-guardduty-cloudtrail-and-personal-health-dashboard/>

**page duty 为 CLOUDWATCH、GUARDDUTY、CLOUDTRAIL 和个人健康仪表板推出新的 AWS 集成**

安德鲁·马歇尔

正如你可能对亚马逊前员工创办的公司[所期望的那样，多年来，PagerDuty 一直在帮助 AWS 用户自动将任何信号转化为正确的见解和行动。我们的 Amazon CloudWatch 集成使团队能够主动缓解影响客户的问题，这反过来又使组织能够满怀信心地创新和扩展其 AWS 和混合环境。](https://www.pagerduty.com/blog/humble-beginnings/)

今年早些时候，我们宣布 AWS 客户现在可以通过 [AWS Marketplace](https://aws.amazon.com/marketplace/pp/B07HH6FNLP) 和 AWS Marketplace 的企业合同进行 PagerDuty 订阅。本周在拉斯维加斯举行的 AWS re:Invent 上，我们很高兴地宣布 PagerDuty 将推出全新的 AWS 集成，用于 CloudWatch Events、GuardDuty、CloudTrail 和个人健康仪表板。

### Amazon CloudWatch(事件和警报):AWS 服务的门户

AWS 用户依靠 Amazon CloudWatch 来提供性能数据，他们可以使用这些数据来监控他们作为整体 AWS 生态系统的一部分而部署的 AWS 服务的状态。利用公共云资源并不意味着用户可以忽略支撑它们的服务器的状态和性能；事实上，随着公司将关键应用迁移到 AWS，跟踪所使用的各种工具变得越来越重要。

PagerDuty 与我们的共享客户已经使用了一段时间的 CloudWatch 警报的集成，允许用户通过设置自定义的高分辨率警报阈值来监控资源利用率(如内存优化)。当这些警报被触发时，您需要的任何解决方案自动化都可以通过 PagerDuty 启动。这是一个极其强大的组合——如果不是最受欢迎的话，这也不足为奇。

虽然 CloudWatch 警报是一个非常有用的工具，但它只能在指定的时间段内观察单个指标，并根据指标值相对于阈值的变化执行一个或多个指定的操作。换句话说，警报在特定的时间点发生一次。本周在 AWS re:Invent 上，我们很高兴推出 **CloudWatch Events** ，这是一个新的 AWS 集成，补充了我们的亚马逊 CloudWatch Alarms 集成。

**CloudWatch Events** 是描述 AWS 资源变化的系统事件流，它增加了 CloudWatch 收集的指标。您可以将“事件”视为对 AWS 环境以及支撑它的服务的任何更改。

对于现代 ITOps 和 DevOps 团队来说，密切关注变化对于保持生态系统的连续性和性能至关重要。例如，团队需要知道 EC2 实例的状态是否从“挂起”变为“运行”他们还需要知道“自动缩放”实际上发生了多少“缩放”此外，AWS CloudTrail 与 Amazon CloudWatch 相结合，使您能够监视 API 调用之类的事情。

弹性和快速扩展的能力是 AWS、Google Cloud 和 Microsoft Azure 等公共云提供商的关键价值主张。作为一种“按使用付费”的服务，记录 AWS 账单对大多数团队来说也非常重要。通过 CloudWatch 集成，如果您的 AWS 账单超过某个阈值，PagerDuty 可以提醒您，帮助团队避免代价高昂的计划外扩展。

通过在 CloudWatch 警报之上添加 CloudWatch 事件集成，PagerDuty 使团队能够基于一组更强大的 AWS 数据来自动化他们的数字操作。它还允许 PagerDuty 客户利用来自更多 AWS 服务的数据，包括:

*   亚马逊 EC2 实例
*   AWS 函数
*   亚马逊 Kinesis 数据流中的流
*   亚马逊 Kinesis Data Firehose 中的交付流
*   Amazon ECS 任务
*   系统管理器运行命令
*   系统管理器自动化
*   AWS 批处理作业
*   阶跃函数状态机
*   AWS 代码管道中的管道
*   AWS 代码构建项目
*   亚马逊检查员评估模板
*   亚马逊社交网站主题
*   亚马逊 SQS 队列

无论您的公司使用本地服务器、AWS、Azure、Google Cloud 还是混合基础设施的任何组合，PagerDuty 都能够从您的基础设施中收集关键信号，并使用它们来支持实时操作。

### 亚马逊瓜德罗蒂

如今，经常听到“安全是每个人的责任”这句话，这与 AWS 的“[共担责任](https://aws.amazon.com/compliance/shared-responsibility-model/)”模式非常吻合。安全是[每个人的工作](https://www.pagerduty.com/blog/security-training-at-pagerduty/)——pager duty 与 Amazon GuardDuty 的集成通过自动化响应工作流，以及减少升级到安全专家的摩擦，帮助开发人员获得安全所有权。Amazon GuardDuty 允许用户持续监控任何恶意或未经授权的行为，这些行为可能会影响一个组织的 AWS 生态系统和建立在其上的应用程序。例如，虽然意外的 API 调用或潜在的受损实例可能没什么可担心的，但是最好收集这些信息以便进行更深入的分析。

这就是 PagerDuty 和 DevSecOps 的用武之地。在 CloudWatch 中收集面向机器的输出只是第一步——您仍然需要一个工作流来确定威胁的性质、其总体影响以及要采取的正确行动。当 Amazon GuardDuty 检测到威胁时，PagerDuty 会根据您的响应规则，自动将关键安全问题通知给适当的人员。此外，您的团队可以通过使用[页面责任事件智能](https://www.pagerduty.com/features/event-intelligence-and-automation/)将威胁与其他问题进行分组来[消除噪音](https://www.pagerduty.com/blog/suppress-noise-event-intelligence/)，为您提供解决问题的合适环境，而不是淹没在类似的警报中。所有这些都可以通过与您的各种记录系统(例如，吉拉、ServiceNow、Remedy 或 Cherwell)无缝集成来完成。).

### 亚马逊个人健康仪表板

AWS 有很多服务。他们可能会在本周的 re:Invent 上发布更多。虽然这些新服务为 AWS 用户提供了更大的灵活性和能力来构建和支持新软件，但它可以让您更轻松地监视您的组织所关心的 AWS 服务、区域和专区的当前状态。这里有一个仅适用于北美的 AWS 服务健康仪表板的滚动浏览。

AWS 了解这个问题，这就是 AWS 个人健康仪表板的用武之地。整体服务运行状况仪表板为您提供了 AWS 服务的一般状态视图，而个人运行状况仪表板则提供了您的团队日常使用的 AWS 服务的性能和可用性的个性化视图。这些关于您真正关心的服务的警告是有帮助的——但是您仍然需要利用这些知识做一些事情。

新的 PagerDuty AWS 个人健康仪表板集成让您可以接收这些数据，然后自动确定如何、何时以及与谁一起采取措施来解决任何问题。然后，团队可以利用导致问题的精确 AWS 服务来增加支持行动和票证，从而为组织中的每个人提供快速解决 AWS 服务中断所需的信息。

如果您正在参加 re:Invent，并希望了解更多关于个人健康仪表板和 PagerDuty 集成的信息，请查看 AWS 举办的以下会议:

**会议:**使用 AWS 支持工具(ENT316-R)优化性能和降低风险
**日期和时间:**11 月 26 日星期一下午 4 点
**地点:** Bellagio，1 楼，大宴会厅 6

**会议:**使用 AWS 支持工具优化性能和降低风险(R1 ENT316)
**日期和时间:**11 月 27 日星期二上午 11:30:
**地点:**C3 海市蜃楼活动中心

### 亚马逊云迹

AWS 和最终用户之间的另一项共同责任是合规性、治理和运营审计。仅仅因为服务器不在你的数据中心，并不意味着你可以撒手不管这些工作流。AWS CloudTrail 帮助用户实现其 AWS 生态系统的治理、合规性、运营审计和风险审计。

通过使团队能够保存在其 AWS 生态系统中发生的各种事件的日志，Amazon 提供了一个强大的工具来管理合规性，包括通过 AWS 管理控制台、AWS SDKs、命令行工具和其他 AWS 服务采取的行动。你可以想象，根据上面的文字，这只是成功的一半。

通过 PagerDuty 新的 AWS CloudTrail 集成，团队可以收集整个 AWS 事件历史记录，用于 DevSecOps 比赛，根据需要自动执行操作，并与吉拉和斯诺等记录系统无缝集成。PagerDuty 支持关联和分组以及其他正在进行的问题，为 DevOps 和 [DevSecOps 团队](https://www.pagerduty.com/blog/datadog-devsecops-force-awakens/)提供了他们需要的背景，以消除运营噪音。例如，团队可以识别亚马逊 S3 何时发生潜在的数据泄露，或者在亚马逊虚拟私有云的安全组规则发生变化时立即收到警报。在这两个示例中，PagerDuty 都可以用来实时自动做出正确的响应。

### 请到 re:Invent 与我们交流

作为 AWS 合作伙伴网络中具有 DevOps 能力的高级合作伙伴，PagerDuty 很高兴加入 AWS at re:Invent，与我们共同的客户分享这些令人兴奋的新集成。如果你这周在拉斯维加斯，请到 1023 号展位来找我们。不打算重新:发明？PagerDuty 提供 14 天免费试用，可以通过 AWS 市场购买[。此外，你可以](https://aws.amazon.com/marketplace/pp/B07HH6FNLP?qid=1540399468305&sr=0-1&ref_=srh_res_product_title)[在这里](https://www.pagerduty.com/partners/amazon-aws/)阅读更多关于 AWS 集成的信息。

### 开始使用这些 AWS 集成:

[https://support . page duty . com/docs/AWS-cloud watch-integration-guide](https://support.pagerduty.com/docs/aws-cloudwatch-integration-guide)
[https://support . page duty . com/docs/AWS-guard duty-integration-guide](https://support.pagerduty.com/docs/aws-guardduty-integration-guide)
[https://support . page duty . com/docs/AWS/AWS-cloud trail-integration-guide](https://support.pagerduty.com/docs/aws-cloudtrail-integration-guide)
[https://support . page duty . com/docs/AWS-personal-health-dashboard](https://support.pagerduty.com/docs/aws-personal-health-dashboard)