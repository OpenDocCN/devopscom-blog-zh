# 是 web 性能，姑且不叫它 WebDevPerfOps

> 原文：<https://devops.com/web-performance-lets-call-webdevperfops/>

今年的速度很快。这只是我第二次去圣克拉拉，但据我所知，每一次 Velocity 大会都很棒。很少有会议能提供如此快速的回报。Velocity 在营造正确氛围方面做得很好。这些谈话通常既有趣又有知识性。[Scott Hanselman 的视频](https://www.youtube.com/watch?v=FZYrlKbkLe8)就是一个很好的例子。他巧妙地告诉开源受众，他们也可以在 Azure 云中运行自己的代码。我碰巧知道一些公司正在这么做。很高兴看到微软继续拥抱开源，因为我自己也是在 Linux 上运行 C#的粉丝。

让一屋子热情的专家聚在一起，让他们开怀畅饮，这是一个令人敬畏的合作的开始。当这群人玩得开心时，话题自然会转移到技术话题上。如果你不在会议的走廊上工作，你就错过了。我总是喜欢寻找其他人处理与我目前面临的问题类似的问题，以及由此产生的双向同行评审。有时，有人也有一个银弹，他们解决了组织中的一个问题，解决方案最终变得易于实现和高度可移植。

当 Velocity 结束时，我发现自己乘坐下午 3:30 的航班返回亚特兰大，但这家酒店的退房时间严格限制在中午 12 点。我知道 devOpsDays 即将到来，google.io 正在进行，一位与会的朋友提醒我 webperfdays 也即将到来。Webperfdays 位于谷歌的山景城园区，就在这条街上。当我调查的时候，门票只有 15 美元，所以如果我没有其他地方可去，为什么不花半天时间在谷歌的校园里谈论网络性能呢？

会议棒极了。Webperfdays 是一个比 Velocity 小得多的群体。这一天除了主要会谈和点火会议外，还包括开放空间讨论。我学到了很多东西，实际上，我在午餐时打电话要求乘红眼航班返回亚特兰大，这样我就可以呆一整天了。

午饭后留下来要考虑几件事。首先，我在那里一个人都不认识。我认出了几个人，但都不是我说过话的人。看着 DevOpsDays 的名单，我没有看到太多新的名字，并且在过去的几个月里与大多数主要的主持人交谈过。

这一切足以吸引我进门，但我留下来，因为他们让我大吃一惊。Andrea Giammarchi 关于移动网络性能的演讲进行了实时演示，展示了降低应用速度如何在各种设备上提供更一致的体验，但假设只有最先进的设备才会给大多数观众带来性能问题。[这篇博文](https://webreflection.blogspot.com/2014/06/on-meaningful-performance.html)介绍了整个演讲，并提供了演示过程中使用的基准测试工具的链接。

我也喜欢托尼·帕里西在 webGL 上的演讲。相比之下，他提出了许多关于我们的硬件有多棒以及它能为我们做些什么的好观点。这段视频涵盖了托尼在网络表演日提出的许多相同观点。我不知道我们的浏览器有 3D 功能，也不知道它有多容易获得。

我大吃一惊，意识到自己根本没有真正考虑过 web 性能。我一直非常关注 devOps 的 CAMS 模型，这在很大程度上意味着通过大量的监控和报告，尽可能安全、快速地对生产进行更改。重点是不要弄坏任何东西。如果变化很严重，绩效下降确实可以称之为突破，但确保我们的数字不下滑并不等同于积极努力让它们变得更好。这是一个商店内的文化视角，为了从内部促进这一点，我自己必须成为一个网络表演倡导者。

我不认为我是唯一一个采用 devOps 反模式的人。挑选团队并最终变得有竞争力是人的本性。DevOps 希望我们的组织去孤岛化，但我在我们致力于纠正此类问题的会议上目睹了行业专家的自我隔离。这就是为什么我在 Velocity 的时候没有和任何人说过话:我们都坚持各自的方向。我认识的那些人不是在休假就是回家了。

我和我一起工作的人没有太多的会议重叠，因为他们大部分时间都在关注 web 性能。因为我是 devOps 的工程师，所以我们坚持自己感兴趣的领域是很自然的。我甚至会承认，我对主动转移对一些深层绩效讨论的注意力感到内疚，因为，“这不是我的领域，我需要保持专注”。

我一回到亚特兰大，这种思考过程就停止了，我希望你们也不要如此短视地看待我们的行业。我们有能力同时研究 devOps、web 性能等等。虽然我们可能不总是房间里的专家，但我们可以在其他领域足够流利，以留意我们的影响，并欣赏我们的团队在各自领域每天面临的胜利和失败。我们可以在我们的组织中创造一种分享的文化，但是如果我们不能对收到的信息感同身受，我们就不能做出相应的回应。