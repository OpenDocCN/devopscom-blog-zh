# DevOps 世界中的安全性:与 Gartner 的 Ben Tomhave 的问答

> 原文：<https://devops.com/security-devops-world-qa-gartners-ben-tomhave/>

随着 infosec 社区赶上了 DevOps 运动的精神，许多 CISOs 和 it 安全领导仍然需要关于如何进行模式转变的指导。这些安全人员不仅绞尽脑汁想弄清楚持续交付带来的额外风险，而且他们还了解到 DevOps 实际上如何帮助他们提高效率以及在他们的 IT 生态系统中提高效率。

[![ben tomhave](img/211544d77c7d680cc7b99bab00a1376f.png) ](https://devops.com/wp-content/uploads/2014/06/ben-tomhave.jpg) Gartner 最近在一份名为[“devo PS 世界中的安全性”](https://www.gartner.com/doc/2725217/security-devops-world)的报告中深入探讨了这个话题。DevOps.com 采访了该报告的主要作者之一、Gartner 的研究总监 Ben Tomhave，讨论了他的一些发现，并详细了解了他认为安全人员需要如何调整理念和实践才能与 DevOps 和平共处。

**DevOps.com:** 您认为安全人员需要如何改变他们的理念才能从 DevOps 实践中获得最大价值？

摆脱这种敌对的“拒绝党”的态度是非常关键的。我们必须摆脱“来找我们，我们会给你东西”的想法，开始考虑合作、协作和指导。在开发方面，安全性需要在过程的早期引入，在代码提交后提供更快的反馈。然后，它需要与运营部门合作，以提供安全的基础，真正内在安全的环境，这些环境在默认情况下是安全的，因此在编写代码后不会发生任何变化。

因为那也是个大问题，对吧？开发人员在谁知道是什么环境的地方编写代码，然后它传播到 QA，QA 看起来更近一点，然后将其发送到生产。然后，它发射了，突然有所有这些惊喜，事情打破左，右，没有沟通的方式。每个人都在不同的平台上工作，而运营部可能甚至没有管理或维护开发平台。我们必须摆脱这种情况，安全性也不例外，它应该是流程的一部分。所有的监控工具，所有的加固工具，所有的东西都需要从开发到质量保证再到生产应用。

**DevOps.com:** 您认为 DevOps 环境中出现的最大安全问题或风险是什么？如果安全团队没有嵌入到 DevOps 模式中，会出现什么样的问题？

我认为这是老一套，推出的代码可能功能上是正确的，但非常不安全，以及所有其他问题，无论是糟糕的加密、糟糕的身份管理处理还是不安全的数据管理。DevOps 商店也不能幸免于这些问题。人们只需看看 Spotify 披露的信息，就知道他们因为一次违规而重置了密码。那是一家很大的 DevOps 商店，显然出了一些差错。

好消息是，进行大量代码推送的 DevOps 商店应该能够相对快速地解决问题。但这意味着他们必须紧密合作，以便在出现问题时，能够快速进行分类和补救，并在事件响应者(无论是安全事件响应者还是运营事件响应者)和开发人员之间进行清晰的沟通，及时向开发人员反馈信息。

**DevOps.com:** 从您的报告中可以清楚地看出，您认为监控比以往任何时候都更重要，以支持 DevOps 周期的快速发展。这是为什么呢？

你知道，我们扩展了 DevOps“快速失败，快速学习”咒语，在里面也加入了“快速恢复”。如果你想快速失败，那很酷。如果你想学得快，那也很酷。但是，您还需要快速恢复，因为您越早检测到违规或某种事件或安全事件，您就能越早开始阻止和补救，并采取积极的措施来清理。

如果您在开发过程中有很多操作透明度，但是您没有足够的透明度来了解项目对所涉及的数据和整体安全监控能力做了什么，您可能会有很多问题。突然间，我们将快速迭代扩展功能的特性和代码推送，然后我们永远不知道环境是否受到攻击，是否得到充分保护，或者是否崩溃。因此，这种透明性也需要扩展到安全监控领域，以便您拥有安全运营透明性和流程透明性。

**DevOps.com:** 我对您倡导的安全架构师帮助安全融入 DevOps 非常感兴趣。一个组织需要从这个角色中得到什么？找到合适的人来做这项工作有什么挑战？

这里的挑战是，你真正需要的是一个真正胜任开发工作的人，并且最好有一些实际经验，可以让他们在开发团队中建立信誉。

但他们也必须是真正强大的安全人员。所以他们理解静态分析，动态分析，他们理解工具在做什么，寻找什么。他们还必须从安全角度理解设计原则，比如为什么不开发自己的加密系统，为什么要与现有的联合身份系统集成，为什么要进行传输加密，以及给定系统的适当保护级别。

在一个人身上找到这两种品质真的很有挑战性。真的很难找到他们，更重要的是，一旦你找到那个人，他们往往是非常昂贵的，尤其是对较小的商店。举例来说，你会想到所有这些移动初创企业。他们的脚被放在火上；它们正受到监管机构的监管。我们已经看到联邦贸易委员会追究一些手机应用公司违反隐私政策之类的事情。那么，当你可能雇不起人的时候，你如何让那些安全机构进入那里呢？

替代的人员配备模式确实说明了这一点。他们可能需要通过专业商店或类似的渠道找到顾问，让他们加入进来，或者通过增加员工的方式参与进来，或者只是基于每个项目。

我认为最关键的是能够在设计评审之前就这样做，并尽早发现这些问题。因为无论你在工具上投资多少，扫描代码库多少次——无论是静态的、动态的还是其他方式——都只能检查 40%的代码。许多这些功能上的弱点，你无法用工具检测出来。你必须让某人看着设计，然后说，‘哦，你完全忘记加密了’，或者‘哦，我看到你在散列，但是你没有给你的散列加盐，所以你的密码怎么安全？’或者‘你为什么在这里处理信用卡数据，这不应该这样做，你应该在那里连接到我们的支付系统。不要重新发明轮子。'

这些类型的事情需要由架构师在早期捕捉，而不是试图使用代码中的工具来捕捉。

**DevOps.com:** 谈到工具，您在报告中专门花时间讨论了工具链和自动化的重要性。自动化对于安全性来说一直很重要，但是现在 DevOps 有什么变化呢？

嗯，我认为最重要的是几乎所有的测试都必须提前自动化。静态代码分析应该尽可能地在每晚的签入库中自动触发。动态分析也是如此。动态 app sec 测试应该自动完成，反馈应该直接反馈到问题管理系统中。除了监控、处理和解决这些工具中的误报之外，根本不应该有太多的人工干预。并且可能添加一些定制的检查，寻找应该在适当的位置或应该在工具中使用的特定库或框架。

我认为我们唯一希望有任何形式的手动中断的时候是第一次预先快速风险分析。决定这是一个处理敏感数据的高风险项目，还是有非常高的正常运行时间要求的高风险项目，还是一个风险较低的项目，我们并不真正担心这里的损失？我认为，以及一些设计审查的考虑将需要一些手动和眼睛参与。

然后一切都应该自动化，直到你说，“好吧，这是一个高风险的项目，我们需要对它进行额外的测试，所以现在我们要开始笔测试，我们需要一些手动验证。”这种验证不仅处理误报，而且真正深入应用程序。所以你模糊了界面，看起来好像破坏了一些东西，你说‘是的，我们验证并证明了它，这就是漏洞。这就是它是如何破裂的。然后以可信的方式反馈给开发人员，以显示代码中有错误的地方，或者这是导致任何情况的逻辑错误。