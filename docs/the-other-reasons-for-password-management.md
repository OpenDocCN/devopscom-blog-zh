# 密码管理的其他原因

> 原文：<https://devops.com/the-other-reasons-for-password-management/>

我尽量不写正在进行的工作——如果它足够重要，可以写在工作产品中，然后写一些别的东西。但是偶尔，需求会压倒我的简单原则。毕竟，热衷于遵守规则并不是我们擅长的事情。

我在为一个客户做[密码管理](https://devops.com/?s=password+management)的时候碰到过几个。我提到了工作产品中的几个重要问题，但是提到其中一个问题时，我警告说它并不深奥，而另一个问题是显而易见和必要的，但是除了密码管理器之外，还有其他解决方案可以处理它。我没有对这两点进行过多的讨论。

然而，更广泛的市场——那些还没有解决密码管理问题的人或者那些刚刚开始将密码管理作为企业解决方案进行研究的人——可能没有意识到这是企业需要的和 DevOps 需要的两个问题。

企业需求越不明显。关于外围环境的变化推动外围安全的变化(如果外围安全有任何意义的话)，外界议论纷纷。但潜在的变化因素不是我们的周边去拥抱更大的互联网上的项目，而是互联网的增长。是的，我们的边界延伸到了云或服务提供商(或多个云或多个服务提供商)，但是使互联网和 web 成为可能的技术也以不太明显的方式延伸了我们的边界。

现在，在您的组织中，您的业务合作伙伴有数百个未确认的帐户。这些账户*应该*被知道，但它们却隐藏在众目睽睽之下。账户存在于那些提供小东西的地方——那种过去用零用现金支付的东西。营销部门购买一次性物品的商店，或者会计部门办公用品用完时的紧急备用账户——诸如此类的账户。密码管理会自动保护这些帐户(假设它正在被使用)。你的组织在保护这些帐户免受服务器端攻击方面无能为力——毕竟那些不是你的服务器——但是密码管理*会*通过实施诸如强度策略和更改频率规则之类的东西来保护它们免受用户端的攻击。

更明显但被低估的一个是秘密管理。如今，大多数密码管理供应商都进行秘密管理，共享核心产品中已经实现的密码保护技术。如果你是一家甚至有点自动化的 DevOps 商店，你*需要*秘密管理。秘密管理可以在其他地方进行(通常是这样)，但是大多数组织使用硬编码的凭证和 API 密匙。

我罕见的有力声明:“如果你正在硬编码凭证、API 密匙、SSL 证书或其他秘密，停止它。*现在就停止*。你是 DevOps，而不是“这是王国的钥匙”——Ops。”密码管理可以为您做到这一点，无需硬编码。其他产品也可以，但是如果你也用密码管理器来管理密码，你就有了两个解决方案。对于 DevOps 来说，一个通过 API 和命令行访问提供秘密管理的密码管理产品是巨大的。要在任何给定的 DevOps 场景中使用该产品，这两者之一将解决该场景。

一如既往，继续踢。你是公司的代言人。无论是销售、营销、公关还是其他什么，当人们与公司互动时(无论是员工、合作伙伴还是客户)，他们几乎总是在与你运行的系统打交道。还有，记得保护好宝宝。密码管理不是以产品为中心的事情，而是通过秘密管理推动集中实施。通过密码管理提高驾驶速度，通过机密管理提高部署效率，同时减少顾虑。我一般不自称，但我会接近它，因为它可能与您相关—如果您感兴趣，在我的名下有更多关于密码管理的内容，包括我对您应该考虑的人的看法。