# 互联网的具体细节是如何改变你的编码方式的

> 原文：<https://devops.com/how-the-nuts-and-bolts-of-the-internet-are-evolving-to-change-the-way-you-code/>

2019 年是互联网基础设施、编程语言和平台开发的大年。在过去的 12 个月中，随着[TLS 1.3](https://telemetry.mozilla.org/new-pipeline/evo.html#!aggregates=0%2520bucket%2520percentage&cumulative=0&end_date=2019-10-15&include_spill=0&keys=!__none__!__none__&max_channel_version=beta%252F70&measure=SSL_HANDSHAKE_VERSION&min_channel_version=beta%252F57&processType=*&product=Firefox&sanitize=1&sort_keys=submissions&start_date=2019-09-01&trim=1&use_submission_date=0)和证书透明性的增长，我们看到了类似 [在天空和海洋](https://www.washingtonpost.com/business/why-low-earth-orbit-satellites-are-the-new-space-race/2019/10/31/30c7213e-fbc1-11e9-9e02-1d45cb3dfa8f_story.html) 中的新连接，以及这些连接的更大安全性。但是在我们迈向 2020 年的时候，有三个趋势对开发者产生了最大的影响。

## **Rust 功能提升其受欢迎程度**

Rust 继续受欢迎，因为它连续第四年被选为 Stack Overflow 最受欢迎的语言[](https://insights.stackoverflow.com/survey/2019#technology-_-most-loved-dreaded-and-wanted-languages)，这在很大程度上是因为它具有无与伦比的能力，可以让开发人员在编程语言的安全性和性能之间自由选择。在 Rust 出现之前，开发人员必须在 C 语言和 Haskell 语言之间做出选择，C 语言速度很快，但安全性很高，Haskell 语言安全性更高，但性能明显较差。Rust 提供了开发人员以前无法享受的安全保障，同时仍然提供低水平的原生性能。学习曲线相当陡峭，但你期望从现代语言中获得的电池特性检查了开发者明年需要优先交付的盒子。

## **HTTP/2 为 HTTP/3 铺平了道路，允许开发者构建更高性能的网站，而没有所有的麻烦**

提供和保护更丰富内容的协议在 2019 年也取得了进展，HTTP/2 成为最常见的网络协议[](https://telemetry.mozilla.org/new-pipeline/dist.html#!cumulative=0&end_date=2019-08-26&include_spill=0&keys=__none__!__none__!__none__&max_channel_version=beta%252F69&measure=HTTP_RESPONSE_VERSION&min_channel_version=null&processType=*&product=Firefox&sanitize=1&sort_by_value=0&sort_keys=submissions&start_date=2019-07-07&table=0&trim=1&use_submission_date=0)，HTTP/3 将在 2020 年带来更大的好处。HTTP/2 简化了开发人员为获得使用 HTTP/1.1 的高性能站点而必须做的工作，解决了页面中大量小对象的复杂性，从而使开发人员的生活变得更加轻松。通过减少页面加载时间和提高响应能力，HTTP/2 为 HTTP/3 奠定了坚实的基础，随着新的传输协议[【QUIC】](https://www.fastly.com/blog/why-fastly-loves-quic-http3)接近完成 ，HTTP/3 有可能在 2020 年初得到广泛部署。TCP 的替代产品 QUIC 解决了 HTTP/2 在一些 p90 场景中出现的行首阻塞延迟。此外，QUIC 整合了 TLS 1.3，确保轻松升级到最新版本的互联网标准安全功能。

## **WebAssembly 承诺新的可能性**

最令人兴奋的是，由于其安全、高性能、跨平台和跨设备的运行时得到了认可，开发人员对 WebAssembly (Wasm)的喜爱和支持在 2019 年得到了加强。对 Wasm 未来的一瞥承诺了更大的可移植性，因为它允许开发人员大规模地将他们编写的代码运行在完全不同的平台上。Wasm 是整个行业的巨变，因为程序将不仅能够在不同的浏览器 — 上运行，正如我们在 Wasm — 上发布的 [Google Earth 所看到的那样，而且能够超越浏览器，跨越各种设备和平台。想想手表、电视、汽车和安全系统，它们可以更安全地连接 — ，更不用说功能即服务在边缘加速世界。在 Mozilla、Fastly、Red Hat 和 Intel 之间新成立的合作组织](https://blog.chromium.org/2019/06/webassembly-brings-google-earth-to-more.html) [字节码联盟](https://bytecodealliance.org/) 的支持下，Wasm 成为 2020 年更加安全和可移植的软件开发的主要基础。

随着 2019 年的所有变化，2020 年对[开发人员](https://devops.com/critical-skills-developers-need-to-avoid-getting-left-behind/)来说将是又一个激动人心的一年，为他们的角色和职业机会带来更大的灵活性。持续的互联网基础设施改进不断增强我们的开发人员社区的能力，支持更安全、更高效的编程和计算 — ，同时改善最终用户体验。

泰勒·麦克马伦