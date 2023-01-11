# 实现 metal devops 的两条途径:云类 API 驱动和集群构建

> 原文：<https://devops.com/two-paths-metal-devops-cloud-like-api-driven-cluster-building/>

我看到人们对 [metal DevOps](https://devops.com/2015/03/06/vms-vs-containers-vms-becoming-el-caminos/) 越来越感兴趣，这是由运行在金属层的容器和横向扩展数据中心平台(如 Hadoop、Ceph & OpenStack)推动的。虽然我看到这是一个越来越大的趋势([包](https://packet.net)、[内纳普](http://www.internap.com/bare-metal/bare-metal-cloud/) [、](https://wiki.openstack.org/wiki/Ironic) [RackSpace](http://www.rackspace.com/en-us/cloud/servers/onmetal) 、 [OpenStack 讽刺](https://wiki.openstack.org/wiki/Ironic)、 [MaaS](https://maas.ubuntu.com/) )，但我将坚定地留在[我的车轮罩](http://rackn.com)内，并在这里使用 [OpenCrowbar](https://github.com/opencrowbar/core) 作为我的参考。

基于 OpenCrowbar 的 API 驱动的 metal 特性，这已经转化为工作负载在 metal 上运行的两种途径:

1) **、使用来自[厨师供应](https://github.com/chef/chef-provisioning)、[盐堆 Libcloud](https://docs.saltstack.com/en/latest/topics/cloud/install/index.html) 、[码头机](https://github.com/docker/machine)、[云铸造炉腹](https://github.com/cloudfoundry/bosh)等工具的 API**将金属“云化”。这些工具拥有面向云 API 的客户端，如 OpenStack 和 Amazon。这些针对云的客户端可以很容易地移植到 Crowbar 的 API 上。五年前，传统观点认为我们需要一个通用的云 API 然而，实践表明，以一种不会将每个云减少到最小公分母的方式包装 API 并不困难。

2) **DevOps 使用移交给 Chef、Saltstack、Puppet 或 Ansible 等工具来部署工作负载**。这种方法利用工作负载的社区脚本(指南、模块、行动手册),具有创建调优环境并将所需参数直接注入脚本的关键能力。我们从 Crowbar v1 到 v2 学到的一个重要教训是，我们的脚本应该有清晰的属性输入/输出边界，以避免将环境知识嵌入到代码中。

虽然我是用撬棍术语来描述这一点，但我认为这种金属方法是出于对金属上的容器和金属上的开发的渴望，通过强制燃料进入市场的。

## 让我们看看每种方法的一些独特和共享的使用案例:

| **金属 API** | **双双** | **金属簇** |
| 

*   Migration to Yi Yun metals
*   Jijian tool custom made

 | 

*   Portability of devps script
*   With power cycle
*   Enable continuous refresh cycle

 | 

*   Use hardware features
*   Advanced network topology

 |

无论是哪种情况，您都必须在配置流程中处理专门针对您的运营需求的定制步骤。我们的经验是每个站点(甚至每个服务器！)在某种程度上是独特的。例如，一个站点可能需要带 VLANs 的团队网络，而另一个站点需要带 SDN 层的平面网络。

**这些差异不是错误或失误**:物理操作和个人操作选择的现实意味着存在大量有效的配置。我们没有尝试强制一致的西西弗式的任务，而是努力抽象出差异，这样当它们不重要时就可以忽略。

最终，选择是**而不是**互斥的。金属 API 通常更快，但更难优化。您可以使用它们快速入门，然后投入时间来优化集群以实现长期运营。**底层的物理编排可以支持这两者。**

你是否打算向金属靠拢？您认为以上哪个选项最有意义？我很想听听您的使用案例、架构和配置需求。