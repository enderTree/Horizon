---
layout: default
title: "Horizon Summary: 2026-08-21 (ZH)"
date: 2026-08-21
lang: zh
---

> 从 47 条内容中筛选出 11 条重要资讯。

---

1. [恶意 Rust crate arrayref 在构建时执行恶意负载](#item-1) ⭐️ 9.0/10
2. [Linux 内核 7.2 发布，带来显著改进](#item-2) ⭐️ 9.0/10
3. [GitHub 停机事故复盘：重试缺陷与提交量激增](#item-3) ⭐️ 8.0/10
4. [速卖通无声 WebAudio 指纹识别破坏蓝牙多点连接](#item-4) ⭐️ 8.0/10
5. [iPhone 上用 1.25 亿参数 Transformer 实时自动续写钢琴演奏](#item-5) ⭐️ 8.0/10
6. [谱神经元：一种可扩展且可解释的机器学习原语](#item-6) ⭐️ 8.0/10
7. [迷你 Kimi K3 复刻版：不到 250 美元训练，超越 GPT-2 124M](#item-7) ⭐️ 8.0/10
8. [OpenAI 预览私密安全处理，前沿模型承诺零数据留存](#item-8) ⭐️ 8.0/10
9. [Stripe 据报以超 70 亿美元收购 OpenRouter](#item-9) ⭐️ 8.0/10
10. [陶哲轩警告：AI 或引发数学界自哥德尔以来最大危机](#item-10) ⭐️ 8.0/10
11. [反向查询服务泄露数百万张人脸照片](#item-11) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [恶意 Rust crate arrayref 在构建时执行恶意负载](https://safedep.io/arrayref-proc-macro1-rust-build-time-malware/) ⭐️ 9.0/10

广受欢迎的 Rust crate arrayref 的一个被攻破的版本被发布到 crates.io，并引入了名为 proc-macro1 的仿冒依赖，其构建脚本在编译期间下载并执行远程二进制文件。事件发生后，Rust 项目移除了 arrayref 以及另外两个相关 crate（internment 和 append-only-vec）的恶意版本。 这次供应链攻击波及一个下载量超过 2.45 亿次的 crate，说明被攻破的维护者账号和恶意构建脚本可能污染整个 Rust 生态系统。它也暴露出 crates.io 在应急响应方面的不足，例如被移除的版本没有安全公告和 yank 提示。 攻击者将 arrayref 的更新与 internment 和 append-only-vec 的新版本串联起来，这些版本都依赖仿冒的 proc-macro1 包。恶意版本已从 crates.io 被悄悄移除，该事件在 RustSec advisory-db issue #3161 中跟踪，社区因此呼吁对 Cargo 构建脚本进行沙箱化。

hackernews · abhisek · 8月20日 13:23 · [社区讨论](https://news.ycombinator.com/item?id=49374269)

**背景**: Rust crate 通过 crates.io 注册表分发，许多 crate 包含构建脚本（build.rs），这些脚本会在编译时运行任意代码，因此是一个强大但危险的扩展点。仿冒（typosquatting）是一种供应链攻击手法，攻击者发布名称与流行包相似的包，希望它被直接使用或作为传递依赖被引入。被攻破的维护者账号正日益成为向开源生态注入恶意软件的常见途径。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://thehackernews.com/2026/08/rust-supply-chain-attack-puts-build.html">Rust Supply Chain Attack Puts Build-Time Malware in Crates with 245 Million Downloads</a></li>
<li><a href="https://www.stepsecurity.io/blog/arrayref-rust-crate-supply-chain-attack">Rust Supply-Chain Attack: arrayref, internment, and append-only-vec Poisoned by the proc-macro1 Build-Time Dropper - StepSecurity</a></li>

</ul>
</details>

**社区讨论**: 评论者批评 crates.io 的处理方式，指出恶意版本消失时没有 yank 标记或安全公告。不少人认为 Rust 对大量传递依赖的依赖使得此类攻击很容易发生，并再次呼吁对 build.rs 脚本进行沙箱化，还提到了此前停滞的相关提案。

**标签**: `#security`, `#supply-chain`, `#rust`, `#malware`, `#open-source`

---

<a id="item-2"></a>
## [Linux 内核 7.2 发布，带来显著改进](https://www.igalia.com/2026/08/19/Linux-72-Released.html) ⭐️ 9.0/10

Linux 内核 7.2 已正式发布，公告于 2026 年 8 月 19 日在 Igalia 网站上公布。此次发布引发了社区的热烈讨论，涉及 AMD 开源驱动中的 HDMI 2.1 支持问题以及内核的持续演进。 作为一次重要的内核发布，Linux 7.2 影响了整个开源生态系统，从桌面用户到树莓派等嵌入式系统。社区讨论既突出了诸如 HDMI 2.1 支持这类持续存在的挑战，也体现了内核 35 年来的长期发展。 该公告获得了 9.0/10 的评分，共 192 分和 67 条评论。有评论者回忆称，AMD 开源驱动中的 HDMI 2.1 支持此前受到 HDMI 论坛的阻碍，并询问是什么变化使其得以实现；现有资料中并未提供官方解释。

hackernews · mariuz · 8月20日 15:46 · [社区讨论](https://news.ycombinator.com/item?id=49376265)

**背景**: Linux 内核是基于 Linux 的操作系统的核心，由 Linus Torvalds 于 1991 年首次发布，现由全球数千名贡献者维护。新内核版本定期发布，每个版本都带有详尽的变更日志，涵盖新硬件支持、性能改进和错误修复。类似 HDMI 2.1 支持这类问题可能涉及 HDMI 论坛等行业授权机构，这些机构有时会限制开源实现。Igalia 等公司为内核做出贡献，并经常发布关于重大版本的公告。

**社区讨论**: 评论者指出，内核的用户体验表面上几乎未变，但其变更日志却丰富且不断增长。一位用户对更新树莓派 4 的内核表示兴奋，另一位则询问 AMD 开源驱动为何如今能够支持 HDMI 2.1。一位不太懂技术的读者质疑此类内容的受众是谁，还有评论者将其与 LWN 的报道进行比较。

**标签**: `#linux`, `#kernel`, `#open source`, `#release`

---

<a id="item-3"></a>
## [GitHub 停机事故复盘：重试缺陷与提交量激增](https://github.blog/news-insights/company-news/the-august-17-outage-and-the-work-ahead/) ⭐️ 8.0/10

GitHub 发布了 8 月 17 日停机事故的事后分析，将其归因于服务错误触发的客户端重试循环，以及 VS Code 中一个潜在的重试缺陷，该缺陷将流量放大了约 10 倍，导致 Copilot 令牌服务恢复延迟。报告还披露，自 4 月以来，每月提交量从 14 亿次增长到 29 亿次。 这起事件凸显了简单的客户端重试逻辑如何在 GitHub 这种规模下升级为重大故障，即使很小的低效也会被放大。它还揭示了开发者活动前所未有的增长带来的运维压力，引发了对免费服务和 AI 驱动工作负载可持续性的质疑。 重试风暴源于单个内部端点的延迟响应，而 VS Code 的重试缺陷缺乏适当的退避或次数上限。GitHub 指出，在处理相当于正常水平 10 倍的流量时恢复服务非常困难；提交量增长也反映了全行业在 AI 辅助编程下的“生产力焦虑”。

hackernews · 0xedb · 8月20日 19:22 · [社区讨论](https://news.ycombinator.com/item?id=49378957)

**背景**: 重试风暴是指大量客户端同时重试失败的请求，导致服务过载并延缓恢复。最佳实践包括使用指数退避、抖动、限制重试次数以及熔断器来防止此类级联故障。GitHub 的这次故障是微软 Azure 架构中心所描述的“重试风暴反模式”的一个现实案例。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://learn.microsoft.com/en-us/azure/architecture/antipatterns/retry-storm/">Retry Storm Antipattern - Azure Architecture Center Advanced Client-side Transaction Retries - CockroachDB Advanced Client-side Transaction Retries - CockroachDB Top 9 Retry Policies That Don’t Create Storms - Medium Retry pattern - Azure Architecture Center | Microsoft Learn Which HTTP Error Status Codes Should Not Be Retried? - Baeldung</a></li>
<li><a href="https://jeffbailey.us/blog/2025/12/16/what-is-a-retry-storm/">What Is a Retry Storm? | Jeff Bailey</a></li>
<li><a href="https://keyholesoftware.com/preventing-retry-storms-with-responsible-client-policies/">How to Prevent Retry Storms with Responsible Client-Side ...</a></li>

</ul>
</details>

**社区讨论**: 评论者批评了这种将错误隐藏在加载图标背后的错误处理理念，也有人怀疑 GitHub 若不将当前免费功能收费，将难以应对规模压力。另有人指出，微软的 AI 战略可能会故意补贴大量的 AI 驱动使用量，因此简单的收费方案不太可能出现。

**标签**: `#github`, `#outage`, `#postmortem`, `#reliability`, `#devops`

---

<a id="item-4"></a>
## [速卖通无声 WebAudio 指纹识别破坏蓝牙多点连接](https://blog.laserphile.com/2026/08/aliexpress-webpage-keeping-multipoint.html) ⭐️ 8.0/10

一名开发者发现，速卖通网页会创建两个隐藏的 AudioContext 对象，进行无声的 WebAudio 指纹识别；当该标签页在 Firefox 中打开时，会中断蓝牙多点连接的音频播放。即使标签页完全无声，也会导致已连接的多点蓝牙耳机停止播放来自其他设备的音频。 此事意义重大，因为速卖通是广泛使用的网站，其对音频 API 的隐私侵犯式使用会给使用多点蓝牙耳机的用户带来真实的设备副作用。这也说明 WebAudio 指纹识别可能损害整体浏览体验，并凸显了浏览器检测和阻止无声音频处理的必要性。 该网页本身无声，但会根据调查结果创建两个 AudioContext 对象，仅用于指纹识别。这也可能导致网站在移动浏览器后台继续运行；相关评论还报告了助听器和车载音频系统出现类似的蓝牙中断问题。

hackernews · emctech · 8月20日 10:08 · [社区讨论](https://news.ycombinator.com/item?id=49372583)

**背景**: WebAudio 指纹识别利用 Web Audio API 渲染一段无声波形，并对生成的音频输出进行哈希计算，从而产生稳定的浏览器或设备标识符；这种标识符在隐私模式、清除 Cookie 或切换 VPN 后仍然有效。蓝牙多点连接是一项允许一副耳机同时连接两台或更多源设备（如手机和笔记本电脑）的功能，以便在设备之间共享或切换音频。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://elsolitario.org/en/2026/08/20/aliexpress-webaudio-fingerprinting-bluetooth-en/">WebAudio Fingerprinting: The AliExpress Case - elsolitario.org</a></li>
<li><a href="https://fingerprint.com/blog/audio-fingerprinting/">Audio Fingerprinting: What It Is + How It Works with Web API</a></li>
<li><a href="https://www.soundguys.com/bluetooth-multipoint-explained-28601/">What is Bluetooth multipoint? - SoundGuys</a></li>

</ul>
</details>

**社区讨论**: 评论者分享了相关的真实问题，例如访问网站时助听器改变环境音放大效果，以及速卖通 iOS 应用触发车载音频命令；他们呼吁浏览器在此类音频手段发生时显示扬声器图标。还有人指出 Firefox 等浏览器已在努力缓解 WebAudio 指纹识别，另一些人则质疑苹果是否会因类似行为将速卖通从 App Store 下架。

**标签**: `#web-privacy`, `#fingerprinting`, `#webaudio`, `#browser-security`, `#bluetooth`

---

<a id="item-5"></a>
## [iPhone 上用 1.25 亿参数 Transformer 实时自动续写钢琴演奏](https://simedw.com/2026/08/20/midi-autocomplete/) ⭐️ 8.0/10

一位开发者训练了一个 1.25 亿参数的 Transformer 模型，用于自动续写 MIDI 钢琴演奏，并完全在设备端运行，在 iPhone 15 上每秒约处理 108 个音符。该成果以免费 App 形式发布：用户弹几个音符，模型就会继续演奏，就像钢琴版的代码自动补全。 这表明实用的生成式音乐模型可以在手机上实时运行，无需服务器延迟，也无需将数据传出设备。它也预示着创意工具领域的一个更广泛转变：当“生成”几乎零成本时，剩余的价值主要在于人的品味和对音乐想法的快速探索。 该模型是一个在 MIDI 数据上训练的 1.25 亿参数 Transformer，App 使用 Apple 的 Core ML 框架在设备端完成推理。开发者表示，这个想法类似 GitHub Copilot 或 Tabnine：用户通过 MIDI 键盘弹几个音符作为提示，模型接着续写演奏。

hackernews · simedw · 8月20日 12:04 · [社区讨论](https://news.ycombinator.com/item?id=49373456)

**背景**: MIDI（乐器数字接口）是一种用于电子乐器、计算机和音频设备之间连接与通信的标准协议，因此它很适合表示钢琴演奏。Core ML 是 Apple 提供的框架，用于将机器学习模型集成到 App 中，提供统一的模型表示并在设备端执行预测。Transformer 模型最初为语言任务而开发，但也非常适合音乐续写这类序列任务，并且可以被压缩和优化以在移动硬件上运行。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://developer.apple.com/machine-learning/">AI & Machine Learning - Apple Developer</a></li>
<li><a href="https://en.wikipedia.org/wiki/MIDI">MIDI - Wikipedia</a></li>
<li><a href="https://github.com/apple/coremltools">GitHub - apple/coremltools: Core ML tools contain supporting tools for Core ML model conversion, editing, and validation. · GitHub</a></li>

</ul>
</details>

**社区讨论**: 评论者将该项目与古典音乐教学法联系起来，指出“自动续写”式的模式其实是拉赫玛尼诺夫等作曲家训练方式的基础。也有人将其类比为基于 AI 的 UX 设计工具，认为当生成成本趋近于零时，剩下的核心能力就是品味；一位软件设计师称赞这类模型能帮助更快地排除死胡同。还有听众觉得模型把《致爱丽丝》带向完全不同的方向“出人意料地令人不安”，另有人提到了一个用算法穷举所有旋律以对抗音乐版权诉讼的相关项目。

**标签**: `#machine-learning`, `#music-generation`, `#core-ml`, `#transformer`, `#on-device-ai`

---

<a id="item-6"></a>
## [谱神经元：一种可扩展且可解释的机器学习原语](https://www.reddit.com/r/MachineLearning/comments/1vtfimo/the_spectral_neuron_an_ml_primitive_for_scalable/) ⭐️ 8.0/10

一篇题为《The Spectral Neuron》的新预印本提出了一种机器学习原语，其形式为 f(x) = λ_k(A0 + Σ x_i A_i)，并给出了理论分析、实用的初始化和训练方法，以及在合成和真实数据上的扩展性实验。开源代码已在 GitHub 上提供。 这种原语旨在同时提供简单性、可扩展性、可解释性和可控性，而这些特性在现代机器学习中往往难以兼顾。通过提供数学基础和训练方法，它可以帮助工程师和研究人员构建能够直接从学习到的矩阵中检查和约束行为的模型。 该模型看起来像一个简单的单行表达式，但其表达能力取决于矩阵的大小；论文分析了可以直接从学习到的矩阵中读取什么，以及哪些形状可以通过构造保证。作者指出，代码大部分由 AI 编写并由作者审查，而手稿在文献综述时使用了 AI 辅助。

reddit · r/MachineLearning · /u/alexsht1 · 8月20日 10:20

**背景**: 在机器学习中，原语（primitive）是最小的原子处理单元，类似于神经网络中的神经元。谱方法已被证明是一种从海量、含噪声且不完整的数据中提取信息的简单而有效的方法，通常使用矩阵的特征值和特征向量。谱神经元（spectral neuron）将这两者结合，将模型定义为矩阵线性组合的第 k 个特征值，从而可以通过学习到的矩阵进行扩展和解释。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/html/2608.08003">The spectral neuron</a></li>
<li><a href="https://congma1028.github.io/Publication/Spectral/SpectralMethods_FnTarticle-nowplain.pdf">Spectral Methods</a></li>
<li><a href="https://en.wikipedia.org/wiki/Language_primitive">Language primitive - Wikipedia</a></li>

</ul>
</details>

**标签**: `#machine learning`, `#interpretability`, `#spectral methods`, `#scalability`, `#arxiv`

---

<a id="item-7"></a>
## [迷你 Kimi K3 复刻版：不到 250 美元训练，超越 GPT-2 124M](https://www.reddit.com/r/LocalLLaMA/comments/1vth1c3/i_just_built_a_mini_kimik3_from_scratch_under_250/) ⭐️ 8.0/10

一名爱好者以不到 250 美元的成本，预训练了一个复刻 Kimi K3 架构的 10.2 亿参数混合专家（MoE）模型，仅使用了 50 亿个 token。该模型在 HellaSwag 上取得 33.4%的成绩，超过了 GPT-2 124M 的 28%。 这表明，像 Kimi K3 这样的前沿架构创新可以以极小的预算在小规模上得到验证，使严肃的预训练实验对个人变得可行。它也凸显了高效 MoE 设计的进步，使得 10 亿参数级别的模型能够超越其规模的表现。 这个 10.2 亿参数的模型每个 token 只激活 1.45 亿参数，并包含 K3 的 Kimi Delta Attention、Gated MLA、Attention Residuals，以及带无辅助损失平衡器的 LatentMoE。它还使用了 K3 未修改的 163,840 词表分词器，且从未经过指令微调；完整的教程已经发布。

reddit · r/LocalLLaMA · /u/OtherRaisin3426 · 8月20日 11:38

**背景**: Kimi K3 是一个 2.8 万亿参数的开源 MoE 模型，基于 Kimi Delta Attention 和 Attention Residuals 构建，支持 100 万 token 的上下文窗口。LatentMoE 是一种硬件感知的 MoE 变体，在低维潜空间中路由计算以提高效率。MLA（多头潜在注意力）首次在 DeepSeek-V2 中提出，可降低注意力计算的内存占用，在这个复刻版中与门控机制结合。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.kriraai.com/blog/kimi-k3-architecture-explained">Kimi K3 Architecture Explained: Specs, Benchmarks, Costs</a></li>
<li><a href="https://www.kimi.ai/ai-models/kimi-k3">Kimi K3: 2.8T Open Model for Coding & Knowledge Work</a></li>
<li><a href="https://arxiv.org/abs/2601.18089">[2601.18089] LatentMoE: Toward Optimal Accuracy per FLOP and Parameter in Mixture of Experts</a></li>

</ul>
</details>

**标签**: `#pretraining`, `#MoE`, `#Kimi-K3`, `#LLM`, `#tutorial`

---

<a id="item-8"></a>
## [OpenAI 预览私密安全处理，前沿模型承诺零数据留存](https://openai.com/index/offering-zero-data-retention-for-frontier-models/) ⭐️ 8.0/10

OpenAI 预览了面向前沿模型 API 客户的私密安全处理机制，并重申零数据留存（ZDR）承诺：请求处理完毕后，提示词与回复不会被保留。该功能正与早期客户测试，计划于 9 月起逐步上线，并同步发布技术白皮书。 这项进展对企业和受监管行业的 API 客户意义重大，因为它直接回应了关于数据隐私和内容可见性的核心信任问题。它也表明 AI API 服务正在向更强的隐私保障方向推进，可能提高整个行业的默认安全基线。 客户内容使用客户控制的密钥加密存储，因此即使请求被标记，OpenAI 人员也无法读取原文。私密安全处理机制通过仅回传有限的安全信号，在跨相关交互中识别潜在滥用，而不会暴露原始提示词或回复内容。

telegram · zaihuapd · 8月20日 02:33

**背景**: 零数据留存（ZDR）是 AI API 提供商的一种运行模式，指客户的提示词、回复及相关元数据不会被存储、记录，也不会用于模型训练或滥用监控等目的。私密安全处理依托机密计算（confidential computing）和同态加密等隐私增强技术：前者利用硬件可信执行环境保护使用中的数据，后者允许直接在加密数据上执行计算。这些方法弥补了仅对静态数据和传输中数据进行加密所留下的安全空白，使服务商无需查看原始内容也能完成滥用检测。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Confidential_computing">Confidential computing</a></li>
<li><a href="https://en.wikipedia.org/wiki/Homomorphic_encryption">Homomorphic encryption</a></li>
<li><a href="https://decagon.ai/glossary/what-is-zero-data-retention-ai">What is Zero Data Retention AI? Definition & Vendor Guide | Decagon</a></li>

</ul>
</details>

**标签**: `#OpenAI`, `#Privacy`, `#Security`, `#API`, `#Data Retention`

---

<a id="item-9"></a>
## [Stripe 据报以超 70 亿美元收购 OpenRouter](https://t.me/zaihuapd/43290) ⭐️ 8.0/10

知情人士称，Stripe 已与 OpenRouter 达成收购协议，金额超过 70 亿美元，但最终价格仍可能变动。Stripe 发言人称不予评论，OpenRouter 也未公开回应。 这笔交易凸显了 AI 模型聚合与分发基础设施日益增长的战略价值。如果完成，将让 Stripe 这样的金融科技巨头在 AI 开发者生态中直接占据一席之地，并可能重塑开发者访问、路由和支付 AI 模型的方式。 OpenRouter 成立于 2023 年，通过统一 API 提供来自多个提供商的 400 多个 AI 模型的访问。该公司今年 5 月称已服务 800 万名开发者。据报道的 70 多亿美元价格并非最终数字，在交易完成前仍可能变动。

telegram · zaihuapd · 8月20日 07:00

**背景**: OpenRouter 是一个统一 API 平台，让开发者通过单一端点和 API 密钥即可访问 OpenAI、Anthropic、Google、Meta 等数百个 AI 模型，而无需为不同提供商分别管理密钥。收购 OpenRouter 将使 Stripe 能够将支付服务与 AI 模型调用深度整合，并扩展其在高增长的 AI 基础设施层的影响力。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openrouter.ai/">OpenRouter</a></li>
<li><a href="https://www.datacamp.com/tutorial/openrouter">OpenRouter : A Guide With Practical Examples | DataCamp</a></li>
<li><a href="https://www.codecademy.com/article/what-is-openrouter">What is OpenRouter? A Guide with Practical Examples</a></li>

</ul>
</details>

**标签**: `#acquisition`, `#Stripe`, `#OpenRouter`, `#AI infrastructure`, `#fintech`

---

<a id="item-10"></a>
## [陶哲轩警告：AI 或引发数学界自哥德尔以来最大危机](https://the-decoder.com/terence-tao-says-ai-could-trigger-maths-biggest-crisis-since-godel/) ⭐️ 8.0/10

在为 2026 年国际数学家大会撰写的文章中，陶哲轩提出数学家应停止争论 AI 能做什么，转而正视被忽视的研究目标问题。他援引 First Proof 项目第二轮的结果：4 个 AI 系统接受了 10 道未发表引理的测试，至少有一个系统判定其中 7 道合格，每道题成本仅为数十至数百美元。 这位顶尖数学家的警告表明，AI 生成的证明可能使数学从“证明稀缺”转向“证明过剩”，从而让这门学科变得人类无法理解。这会影响证明标准、同行评审，以及 First Proof 等项目所代表的 AI 研究数学评估生态。 First Proof 是一个独立评估 AI 系统解决困难研究数学问题能力的项目，其第二轮测试让 4 个 AI 系统处理研究者提供的 10 道未发表引理。陶哲轩还表示，即使证明通过了形式验证，如果无人能清晰讲解，也应视为不完整，因为形式验证本身并不能保证人类可理解性。

telegram · zaihuapd · 8月20日 13:19

**背景**: First Proof 是由包括哈佛大学教授 Lauren Williams 在内的组织者于 2026 年 2 月发起的独立项目，旨在回应关于 AI 数学能力快速进步的种种说法。在这类评估中，“引理”是为了证明更大定理而中途证明的定理；形式验证则是逐步骤的纯逻辑检查，但并不评判证明能否被人类理解或讲解。陶哲轩将当下比作哥德尔和罗素的时代，指的是 20 世纪初的基础危机，当时悖论和不完备定理迫使数学家重新审视本学科的基本假设。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://1stproof.org/">First Proof Project</a></li>
<li><a href="https://current.fas.harvard.edu/stories/first-proofs-second-batch-math-problems-test-ai">First Proof’s second batch of math problems test AI</a></li>
<li><a href="https://www.scientificamerican.com/article/mathematicians-launch-first-proof-a-first-of-its-kind-math-exam-for-ai/">Mathematicians launch First Proof, a first-of-its-kind math ...</a></li>

</ul>
</details>

**标签**: `#AI`, `#mathematics`, `#proof verification`, `#Terence Tao`, `#research ethics`

---

<a id="item-11"></a>
## [反向查询服务泄露数百万张人脸照片](https://arstechnica.com/gadgets/2026/08/reverse-lookup-service-exposed-millions-of-photos-of-peoples-faces/) ⭐️ 8.0/10

一家反向图像搜索服务发生数据泄露，暴露了约 450 GB 的数据，其中包括超过 900 万张人物面部照片以及与之关联的邮箱、电话和 IP 地址等个人信息。该服务已限制数据库访问，但事件的全部影响范围和补救措施仍未明确。 由于人脸是不可变更的生物识别标识，此次泄露引发了严重的隐私和身份安全担忧。泄露的数据可能被用于未经授权的身份识别、个人追踪或诈骗，影响数百万用户，并凸显了大规模生物识别数据收集的潜在风险。 被暴露的数据库大小约为 450 GB，包含超过 900 万张图像。除面部照片外，数据中还包含邮箱地址、电话号码和 IP 地址，这加大了将生物识别数据关联到具体个人的风险。

telegram · zaihuapd · 8月20日 15:14

**背景**: 反向图像搜索（又称基于内容的图像检索）允许用户上传一张图片，在互联网上查找相似图像及其来源。人脸等生物识别信息具有唯一性和不可变更性，一旦泄露便无法像密码一样简单更换，因此此类泄露事件的危害尤其严重。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://zh.wikipedia.org/zh-hans/反向图像搜索">反向图像搜索 - 维基百科，自由的百科全书</a></li>
<li><a href="https://www.cebnet.com.cn/20210304/102733568.html">cebnet.com.cn/20210304/102733568.html</a></li>

</ul>
</details>

**标签**: `#数据泄露`, `#隐私`, `#生物识别`, `#安全`, `#人脸识别`

---