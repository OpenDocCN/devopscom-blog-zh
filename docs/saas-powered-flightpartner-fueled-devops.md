# SaaS 动力飞行伙伴由 DevOps 提供燃料

> 原文：<https://devops.com/saas-powered-flightpartner-fueled-devops/>

私人飞机租赁公司 FlightPartner 正从 DevOps 中获益，构建一个强大的软件即服务(SaaS)产品，让其客户毫无延迟地高飞。

“FlightPartner 并不拥有任何飞机，而是通过向包机经纪人(客户的代理人)提供私人飞机包机的全球网络来满足客户的旅行需求，”FlightPartner 的首席执行官兼创始人道格拉斯·施莫尔说。通过充当全球分销网络(GDN)，FlightPartner 能够实时获得私人飞机的供应情况。

施莫尔说，TravelPort 和 FlightPartner 对于航空公司的座位可用性和私人飞机可用性的关系。

FlightPartner 基于云的 SaaS 通过网络浏览器作为基于网络的服务来管理数据交换和交易，不需要为经纪人或运营商安装客户端软件。该服务使用 Angular.js，[“动态 Web 应用的结构框架”](https://docs.angularjs.org/guide/introduction)将数据从浏览器传递到 PHP 后端。Schmohl 说，一个数据库和集成系统后端为可用的私人飞机建立实时报价，而支付机制支持搜索、预订和支付，完成交易。

FlightPartner 使用了一个由[泰勒奥特韦尔](http://taylorotwell.com/)创建的 [Laravel](https://laravel.com/) 开源 PHP 框架，最初的目标是开发遵循[模型-视图-控制器(MVC)架构模式](https://developer.chrome.com/apps/app_frameworks#mvc)的 Web 应用。“这个框架允许快速开发、测试和部署我们的 SaaS 解决方案，”Schmohl 指出。

## SaaS 技术挑战

Schmohl 和他的公司在构建 FlightPartner 软件的过程中遇到了一些技术问题，并努力将其提升到最终可以翱翔的天空。施莫尔致力于遵循埃里克·赖斯的精益创业实践，他是《精益创业》一书的作者，该书重新定义了初创科技公司的路线图。根据这本书，作为一个精益创业公司，处理一项新业务的第一步是尝试推出一个“最小可行产品”，或者仅仅是足够测试市场需求的产品或服务。“由于包机市场的复杂性，这对于我们来说几乎是不可能的，”他说，因此 Schmohl 不得不投资于一个技术更先进的产品，而不是一个简单的解决方案。

在私人飞机租赁行业，变化如此之多，变量如此之多，需要访问的参与者如此之多，FlightPartner 需要访问的系统如此之多，一个最低限度的可行产品仍然需要大量的外部集成和 API。Schmohl 说:“开发协作实现这一目标是非常困难的，开发人员经常将代码推向生产，结果每次部署都会产生更多的问题。”。

第二个技术失误——在缺乏正式开发结构的情况下——sch mohl 的团队编写代码来逐个解决特定的功能问题。然而，团队发现开发一个功能的方法会与创建另一个功能的不同方法相冲突，等等。“前端和后端的不断修补包括任何可行的方法。管理和扩展这些代码变得非常困难，”他说。

Schmohl 说，由于这两个技术挑战，FlightPartner 在最小可行产品和遵循精益创业方法方面的尝试很快就陷入了混乱的代码和难以管理的方法中。

## FlightPartner 开发渠道

今天，FlightPartner 的开发有了很大的改进。SaaS 及其组件从本地构建开始，系统在 [AWS](https://aws.amazon.com/) 中将本地构建推送到开发服务器。FlightPartner 开发者使用 [SourceTree](https://www.sourcetreeapp.com/) 、Git 客户端和 [Git](https://git-scm.com/) 版本管理系统来管理软件版本。FlightPartner 使用质量保证来管理开发和测试代码，开发人员使用 [Elasticbeanstalk](https://aws.amazon.com/elasticbeanstalk/) 修复错误代码并将其部署到 AWS。“这使得快速构建和持续部署成为可能，”Schmohl 说。

使用 DevOps 方法进行开发给高度动态的市场带来了结构。“将 SaaS 解决方案作为一个市场来提供，所面临的挑战不同于典型的市场。我们的库存(飞机)是流动的，因为它经常移动，价格随地点而变化。这种操作上的挑战转化为软件功能变化的大量和持续的开发。

这些是驱动软件需求的操作需求；开发人员的目标越来越多地是满足那些需求，以便软件无缝地支持操作。开发使用优先级状态来识别和升级对持续、平稳的操作活动最关键的构建。

## 结果

FlightPartner 的开发流程创建了一个工作流程，可最大限度地减少实现运营结果所需的资源。Schmohl 说，在很大程度上由于 DevOps 和基于云的 SaaS 系统，FlightPartner 的 GDN 在七大洲的六个洲都有飞机可供租赁，包括 35%位于美国以外的可用飞机。