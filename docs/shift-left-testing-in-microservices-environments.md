# 微服务环境中的左移测试

> 原文：<https://devops.com/shift-left-testing-in-microservices-environments/>

到目前为止，众所周知，在[软件开发生命周期](https://devops.com/?s=SDLC) (SDLC)中检测到的错误越晚，修复该错误所需的时间就越长，成本就越高。

2017 年， [Ponemon Institute](https://www.ibm.com/account/reg/us-en/signup?formid=urx-46992) 发现，修复一个在 SDLC 早期检测到的缺陷平均需要花费约 80 美元，如果在生产阶段检测到同样的缺陷，则需要花费约 7600 美元。

### [基于开发阶段修复缺陷的相对成本](https://www.researchgate.net/figure/IBM-System-Science-Institute-Relative-Cost-of-Fixing-Defects_fig1_255965523)

|  | **设计** | **实施** | **测试** | **维护** |
| **修复缺陷的成本** | 1x | 6.5 倍 | 15 倍 | 100 倍 |

虽然这些数字是有争议的，但是很明显，缺陷的早期检测可以为组织节省大量的时间和金钱，同时使那些组织能够更快地交付更高质量的软件。由于这些原因，许多组织正在实施左移测试实践，包括在微服务环境中。

Shift left 是一组实践，旨在软件交付过程的早期发现并防止缺陷，而不是在测试和维护阶段。左移测试背后的思想是通过在 SDLC 中尽可能早地提供可操作的测试信号和反馈来提高软件质量。

在这里，我们将强调左移位测试，结合测试自动化，如何更好地支持创新和高质量软件的快速交付。我们还将解决在微服务环境中实施左移测试所面临的一些挑战，并介绍成功实施微服务的重要策略。

### 左移测试的好处

开发的瀑布模型包括高度专业化的设计、开发、QA 和发布团队之间的明确责任传递。它还涉及冗长的反馈循环。

Scrum 和敏捷方法通过引入 sprints 和允许更频繁的迭代开发和交付，使得整个 SDLC 更加灵活和敏捷。此外，DevOps 和 DevSecOps 致力于通过工具化和自动化消除开发、运营和安全之间的孤岛。因此，上市时间和质量都大大提高了。将左移测试添加到混合测试中可以更好地定位团队，以尽可能有效地处理从设计阶段到维护阶段的广泛职责。

左移测试侧重于预防而不是检测。向左移动的好处包括:

*   通过尽早消除 SDLC 中的错误来提高效率。
*   减少人为错误和相关成本。
*   提高交付速度，减少发布之间的时间间隔。
*   提高软件质量。
*   获得竞争优势。

像这样思考左移测试可能是有帮助的:在开发的早期并行测试，而不是传统的开发瀑布模型，接着是 QA 测试。

### 微服务环境中的左移测试挑战

通过将应用程序构建为松散耦合、可独立部署的服务的集合，微服务架构支持大型复杂应用程序的频繁交付。

虽然左移测试实践带来了许多好处，但左移测试也带来了三个挑战，当组织在分散的、基于微服务的堆栈上实施它时，必须解决这三个挑战:

1.  分别构建和管理每个微服务可以减少开发时间。然而，在微服务级别实现左移测试意味着左移实践必须应用于每个单独的微服务。
2.  微服务开发者可以选择最适合他们开发需求的编程语言和服务依赖。然而，结果是，左移测试实践需要跨不同的编程语言和依赖性来实现和管理。
3.  为了确保微服务按预期运行，团队通常运行集成测试、端到端测试和性能测试，以评估更大堆栈环境中的功能。由于测试堆栈的复杂性，左移测试在微服务环境中尤其具有挑战性。

![](img/eae4fdd1cd62398e8b15ed90bd82a39b.png)

*微服务，每个都有自己的 SDLC 管道*

### 管道缩放考虑因素

几类自动化左移测试可以集成到 DevOps 管道中，包括单元测试、集成测试、性能测试和安全测试。不同的微服务会有不同的测试需求。

关键是将左移测试实践应用于每个微服务，同时保持这些微服务的灵活性和分散性。理想的工作流系统和 DevOps 管道实现必须简化管道创建，同时使开发团队能够管理管道，并需要 DevOps 和平台团队的最少输入。换句话说，左移实践必须适合所讨论的微服务的特定需求，以使测试过程可扩展，并且易于开发团队持续管理。

仅举一个例子，GitHub Actions 和类似的 CI/CD 管道工具使开发团队能够使用基于 GitOps 的实践来配置、管理他们的微服务的整个管道，同时将基础设施测试和依赖或影响系统其他部分的测试留给 DevOps 团队。

### 测试环境注意事项

在测试环境中，单元测试、集成测试、性能测试和安全测试可以在一组隔离的微服务和配置上运行。这些测试环境的性质和质量与左移测试的有效性直接相关。

当微服务数量较少且总体复杂性相对较低时，可以使用克隆的生产或试运行环境进行测试。然而，一旦组织达到微服务的阈值数量或复杂性的阈值水平，失控的基础架构成本和运营负担就会使这种环境难以为继。

作为回应，一些组织在 SDLC 早期依赖冒烟测试(最小可行稳定性测试)和基于模拟的集成测试。虽然这种测试在短期内很有用，但是将基本测试推迟到 SDLC 的后期阶段通常会在试运行环境中引入测试信号和有效性问题，并且会导致交付延迟和严重的软件质量问题。

那么如何在微服务环境中成功使用左移位测试呢？该解决方案包括使用可伸缩的、短暂的测试环境。

### 短暂的左移测试环境

高质量测试环境的可用性是寻求扩展左移测试实践的组织的常见瓶颈。使用一些高保真暂存环境进行信号测试可能会减缓发布过程。更重要的是，随着时间的推移，它会降低整个 SDLC 的速度，并增加堆栈的不稳定性。

短暂的测试环境提供了一种完全不同的方法。这些沙盒环境使用隔离的环境，使用户能够独立测试，而不会影响其他用户。特别是，它们支持隔离，同时使用应用程序级多租户而不是传统环境中的资源复制方法来共享资源(例如，外部云依赖项和托管数据库)。

这个想法是微服务测试环境可以用来测试更大的服务栈的变化。因为可以同时进行多个测试，所以测试覆盖率和资源效率会大大提高。

高质量的沙盒环境可以在几秒钟内启动，并扩展到数万个微服务。事实上，每个拉请求、分支或提交都可以有自己的测试环境，而不会显著增加基础设施和运营成本。任何变化，无论多小，都可以单独测试，以确保整个堆栈的性能和稳定性。

![](img/ea8f988d58faa89f21b39a69e5846c28.png)

### 微服务的左移测试解决方案

一个基于微服务的组织想要在整个组织范围内扩展左移测试，必须首先解决几个挑战。需要考虑的因素包括:需要对不同的微服务应用测试实践，需要适应不同的编程语言和服务依赖性，以及需要针对堆栈进行测试。

在将左移测试实践扩展到整个组织之前，需要正确的工具和自动化。此外，为了帮助开发人员理解左移测试可以加速和改进他们正在开发的核心功能的方式，可能需要文化上的转变。

为了在微服务环境中应用有价值的左移测试实践，组织应该考虑使用短暂的沙盒环境。在沙盒环境中使用正确的工具集可以让开发团队在整个 SDLC 中测试微服务。通过这样做，组织可以确保这些服务遵循安全最佳实践并完全按照预期执行，无论是独立执行还是针对堆栈执行，同时降低成本、加快上市时间并提高软件质量和用户满意度。