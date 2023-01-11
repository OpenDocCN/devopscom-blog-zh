# Vivint 利用 DevOps 应对智能家居物联网挑战

> 原文：<https://devops.com/use-case-vivint-meets-smart-home-iot-challenges-using-devops/>

智能家居技术供应商 [Vivint](http://www.vivint.com/) 为超过 100 万美国和加拿大消费者提供服务，包括宽带互联网、云存储、家庭自动化产品、家庭安全服务和能源自动化控制。

Vivint 平台架构总监尼克·布朗(Nick Brown)表示，这家公司以家庭安全起家，利用门窗传感器、运动探测器和玻璃破碎传感器，以及检测家中洪水、热量、冰冻、烟雾和一氧化碳的传感器。“我们有一系列室内和室外摄像机，如门铃摄像机和 ping 摄像机，这是一种支持双向音频的室内摄像机。”对于智能家居，Vivint 将自动化设备、智能恒温器和亚马逊 Echo 扩展到家庭中。

Vivint 使用 DevOps 在一年内建立并运行了这些传感器和智能家居设备背后的软件平台。Vivint 继续使用 DevOps 来满足其不断增长的平台需求。

## 构建智能家居的软件平台

Vivint 开始了从家庭安全公司到最大的智能家居提供商的扩张，面临的挑战是发展一个可以服务一百万客户的平台。这对于将 70 万家庭安全客户和 20 万新的智能家居客户纳入进来是必要的，因为其领导层知道这 20 万新客户将在几个月内到来。

“我们完全是从零开始建设这个新的基础设施，在运营的头几个月，我们需要支持 20 万个新的安装，”布朗说。Vivint 现有的家庭安全客户使用第三方公司支持的传统平台；那家公司有整整 10 年的时间来建设它的基础设施。Vivint 有一年的时间将这 70 万现有客户纳入一个新系统，而准备新客户涌入的时间则更少。

Vivint 实现了其目标，在最初的 12 个月里为超过 900，000 个家庭提供了服务。

## DevOps 现在为 Vivint 实现了什么

布朗说，DevOps 使 Vivint 能够大规模管理状态和历史数据，这使该公司能够为世界上最大的智能家居平台提供动力。通过一个 7 英寸的控制显示屏，顾客可以看到房子里发生的一切，包括当前和 45 天内发生的事情。

他指出，Vivint 平台提供的真正价值在于集成的室内体验，该公司将这种体验虚拟化，并在世界各地随时随地提供，让客户可以实时查看他们的家庭数据。

为了构建、使用和进化这个平台，Vivint 使用了 [MongoDB](https://www.mongodb.com/) 、 [RabbitMQ](https://www.rabbitmq.com/) 、 [Nginx](https://www.nginx.com) 、ELK(曾经的 ELK 栈，现在的[弹性栈](https://www.elastic.co/webinars/introduction-elk-stack))、 [Salt](https://saltstack.com/) 和自制工具。Vivint 将其自主开发的代码应用于指导通信协议的任务，使智能家居和 Vivint 云能够相互通信。

该公司使用 RabbitMQ，这是一种基于 Erlang 语言的开源消息代理工具，支持 T2 高级消息队列协议(AMQP)，将这些消息分散到其软件平台内外，驱动它们在内部基础设施中进出 Vivint 的服务。Vivint 使用多功能网络服务器/反向代理服务器 Nginx 来提供网络应用和服务。

Vivint 运行一个 ELK 堆栈，由 [Elasticsearch](https://www.elastic.co/products/elasticsearch) 、 [Logstash](https://www.elastic.co/products/logstash) 和 [Kibana](https://www.elastic.co/products/kibana) 组成，用于监控。它的运营团队使用 Salt，一个基于 Python 的配置管理器来管理一切。“我们期待添加 Kubernetes 作为新的基础设施解决方案，使其更加模块化，”Brown 说。

## DevOps 模块化之路

Vivint 需要其软件平台尽可能模块化。“基础设施的每一部分都必须支持模块化范例。因为我们正在遵循一个高风险、紧急的时间表，我们需要确保我们在这个过程中犯的任何错误都很容易被删除和替换，”布朗指出。Vivint 在推出每周软件发布的同时，几乎使用了无数的服务来实现这一点。

“从 DevOps 的角度来看，我们这里有很多事情要管理，”他说。Vivint 使用 AWS 来支持其云中的基础设施，该公司也有自己的私有云。Vivint 需要安全快速地移动，同时保持其灵活性并协调所有这些不同的元素。

为了将所有智能家居技术引入新系统，Vivint 选择了 MongoDB，因为它的数据模型和代码往往会自然地与数据库中的数据模型相结合。“我们利用了灵活的模式，Mongo 面向文档的架构确实允许我们编写非常少的数据访问代码，”Brown 说。这大大缩短了实施时间。