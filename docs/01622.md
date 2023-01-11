# xMatters 看到了持续测试的价值

> 原文：<https://devops.com/use-case-xmatters-applies-continuous-testing-intelligent-communications-platform/>

[xMatters](https://www.xmatters.com/) 构建了一个智能通信平台，用于提醒和连接公司利益相关方，以进行 IT 事故响应以及生产线工作流支持和 DevOps 系统场景。依赖 xMatters 的客户也依赖于供应商的持续测试机制的有效性:在 xMatters 早期的持续测试失败可能会对客户的危机响应产生放大的影响，导致代价高昂的后果。

XMatters 使用持续测试来促进其智能通信平台的持续交付，以加速的方式交付对有限数量的特性的更改。xMatters 的 QA 架构师 Deepa Guna 说:“这降低了我们失败的风险，并使解决缺陷变得更加容易。

对于 xMatters，在 DevOps 管道中正确使用和放置连续测试对于确保智能通信解决方案在客户危机期间不会引入错误至关重要。

## xMatters 软件、语言和工具

xMatters 平台由一个服务栈架构组成，该架构具有可通过 web 访问的前端技术和支持它的后端技术。根据古纳的说法，该平台利用了 [Java](https://java.com/) 、 [RESTful JSON](http://bitworking.org/news/restful_json) 、 [Node.js](https://nodejs.org/en/) 和 [Postgres](https://hub.docker.com/_/postgres/) ，它们运行在地理上分散在北美、欧洲和亚太地区的数据中心上。

古纳说:“我们的数据中心建立在基础设施即服务的基础上，其中包括诸如 [OpenStack](https://www.openstack.org/) 、[木偶](https://puppet.com/)、 [Fabric](https://get.fabric.io/) 和[consult](https://www.consul.io/)等技术。作为其通信服务的一部分，XMatters 也有一个针对 iOS 平台的移动应用程序。

## 开发前后的 xMatters 测试方法

Guna 说，在连续交付管道出现之前，该公司的测试包括在每月发布一大组功能和部署客户报告的缺陷的缓慢过程中人工执行回归测试。

今天，xMatters 使用自动和手动回归测试以及单元测试代码覆盖监控，每周发布一小组特性和解决缺陷，同时使客户能够在特性开发过程的早期提供反馈。

在 DevOps 管道的开发、测试和发布阶段，以及向客户交付平台时，XMatters 会使用几个测试。开发阶段包括以下测试工具及其相关测试类型:

*   [sonar cube](https://www.sonarqube.org/)分析代码质量。
*   Jacoco 测量开发人员单元/集成测试的代码覆盖率。
*   在 xMatters 提交更改之前，Git + [Jenkins](https://jenkins.io/) 运行单元和集成测试。

古纳说，测试阶段进行如下测试:

*   Jenkins 在测试环境中部署工件并运行自动化测试。
*   一个包括 [Jmeter](https://jmeter.apache.org/) 、 [Gradle](https://gradle.org/) 、Java、 [TestNG](http://testng.org/doc/index.html) 和 [Selenium](http://www.seleniumhq.org/) 的自动化框架运行它的测试。

发布阶段以这种方式测试软件:

*   Jenkins 在测试环境中部署工件并运行自动化测试。
*   一个包含 Jmeter、Gradle、Java、TestNG 和 Selenium 的自动化框架运行它的测试。
*   [Splunk](http://www.splunk.com/) 和 [Takipi](https://www.takipi.com/) 做异常监控。

Guna 说，当 xMatters 将平台交付给客户时，它会执行以下测试:

*   Runscope 监控系统的健康状况，以确保关键服务正在运行。
*   [Pingdom](https://www.pingdom.com/) 监控客户网站的状态。

## 深入到发布测试

“在发布测试阶段，我们对应用程序进行了 1，000 次全自动和手动启动的测试，我们在每个发布周期都会执行这些测试。我们还有工具可以在发布测试期间监控异常情况，”Guna 说。成功通过这一阶段后，新的软件平台版本就可以投入生产环境了。

Guna 说，XMatters 使用连续交付管道将新的平台版本首先部署到客户阶段环境，然后部署到其生产环境。“所有生产环境都有持续的冒烟测试，我们根据客户层每 5、10 或 15 分钟执行一次，以监控服务的运行状况。”

## 结果指标

xMatters 的持续测试方法似乎对供应商有效。Guna 指出:“与去年相比，我们今年将因应用程序缺陷导致的重大生产事故数量减少了 40%。