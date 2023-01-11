# DevOpsQA NJ Meetup–ELK Stack

> 原文：<https://devops.com/devopsqa-nj-meetup-elk-stack/>

我们在新泽西州五月会议上的演讲嘉宾是来自 Elastic 的 Peter Kim。Peter 是 Elastic 的解决方案架构师，在使用 Endeca、MarkLogic 和 core Lucene 设计和开发搜索应用程序方面拥有超过 10 年的经验。他给了我们一个关于 ELK Stack 的很好的概述，它由 ElasticSearch，LogStash 和 Kibana 组成。

总之，ELK Stack 是一个端到端的堆栈，能够实时洞察来自几乎任何类型的结构化和非结构化数据源的数据。它旨在解决日志格式不一致、跨服务器的日志分布以及理解日志输出所需的高级专业知识等问题。ELK Stack 提供了与 Chef、Puppet 和 Ansible 等配置管理工具的开源集成，以及一个用于 Hadoop 的连接器。

然后，Peter 详细讨论了 ELK 堆栈的每个组件。Logstash 通过收集、解析和存储数据来管理事件日志。它是完全开源的，拥有 Apache 2.0 许可。Grok 是一个工具，可以用来将非结构化数据解析成结构化和可查询的数据。[![logstash_logo](img/dbeee74129cf730dbcffaeb089c75ab1.png)](https://devops.com/wp-content/uploads/2015/05/logstash_logo.png)

ElasticSearch 是一个无模式的、基于 REST 和 JSON 的文档库。它的每个函数都是通过 REST APIs 公开的。ElasticSearch 是分布式的，可水平扩展的，附带一个用于分析、本地化支持等的插件日志，以及用于各种编程语言的客户端 API。

Kibana 是一个集成了 ElasticSearch 的数据可视化和分析平台。Peter 用 Apache weblog 数据做了一个 Kibana 的现场演示。

会议之后是许多好问题，从安全性、实时数据到模糊搜索和复杂聚合。最后，Peter 向我们介绍了 Elastic Roadmap，包括用于提醒的 Watcher 和作为 ElasticSearch 2.0 一部分的新功能。

如果你有兴趣了解更多关于弹性的知识，你可以在 [【邮件保护】](/cdn-cgi/l/email-protection#6d1d0819081f2d08010c1e19040e430e02) 联系彼得

特别感谢 Ishi systems([http://www.ishisystems.com/](http://www.ishisystems.com/))赞助本次活动。

在[http://www.meetup.com/DevOpsandAutomationNJ/](https://www.meetup.com/DevOpsandAutomationNJ/)报名参加我们的下一次聚会，或者在 Twitter [@DevOpsQA](https://twitter.com/DevOpsQA) 上关注

[![logo-elastic](img/f7f5feec684d828b43a34e35b552e7f8.png)](https://devops.com/wp-content/uploads/2015/05/logo-elastic.png)