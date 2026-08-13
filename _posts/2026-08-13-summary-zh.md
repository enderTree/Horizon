---
layout: default
title: "Horizon Summary: 2026-08-13 (ZH)"
date: 2026-08-13
lang: zh
---

> 从 38 条内容中筛选出 10 条重要资讯。

---

1. [Tailscale 将数据库损坏追溯到存在 16 年的 SQLite WAL 重置错误](#item-1) ⭐️ 9.0/10
2. [Qwen 发布 3.8-Max：首次开源 2.4 万亿参数 Max 级模型](#item-2) ⭐️ 9.0/10
3. [DeepSeek V4 Pro 0813 发布：性能强劲且成本低廉](#item-3) ⭐️ 8.0/10
4. [xAI 发布 Grok 4.6，引发基准测试可信度热议](#item-4) ⭐️ 8.0/10
5. [Chrome 中小尺寸 JPEG 显示差异的成因](#item-5) ⭐️ 8.0/10
6. [AI 可能正在淘汰软件工程中的中层阶级](#item-6) ⭐️ 8.0/10
7. [高尔斯：LLM 擅长寻找反例，但还写不出优美证明](#item-7) ⭐️ 8.0/10
8. [Adam 打破旋转不变性，破坏隐式低秩偏置](#item-8) ⭐️ 8.0/10
9. [微信发布 WeLM：以资源效率为核心的大语言模型家族](#item-9) ⭐️ 8.0/10
10. [白宫拟将开源模型纳入 AI 政策，发布前需安全测试](#item-10) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Tailscale 将数据库损坏追溯到存在 16 年的 SQLite WAL 重置错误](https://tailscale.com/blog/sqlite-wal-reset-bug) ⭐️ 9.0/10

Tailscale 发布了一篇详细的事后分析，将反复出现的数据库损坏事件追溯到 SQLite 预写日志（WAL）模式中一个存在了 16 年的竞态条件，即“WAL 重置错误”。该错误已于 2026 年 3 月 3 日由 SQLite 开发者 Dan 修复，Tailscale 还资助了一个开源 VFS shim，用于帮助定位该竞态条件。 这很重要，因为它表明即使经过最广泛测试的数据库库也可能潜藏多年难以发现的并发错误，影响所有以 WAL 模式使用 SQLite 的应用。同时它也展示了公司可以通过资助针对性的调试工具来为开源基础设施做出有意义的贡献。 该错误自 SQLite 3.7.0（2010 年 7 月 21 日发布）首次引入 WAL 模式起就存在，并一直延续到 3.51.2 版本（2026 年 1 月 9 日）。Tailscale 的架构使用单个 Go 进程独占访问数据库，但损坏仍然发生，这说明该竞态条件非常隐蔽。

hackernews · ropbear · 8月12日 14:22 · [社区讨论](https://news.ycombinator.com/item?id=49272832)

**背景**: SQLite 是一种嵌入式数据库引擎，依赖预写日志（WAL）来提升并发性和崩溃恢复能力。在 WAL 模式下，可以在 SQLite 与底层操作系统文件系统之间插入一个 VFS（虚拟文件系统）shim，以添加诸如页面校验和或日志记录等检测功能。这个 shim 在重现和定位竞态条件方面发挥了关键作用，该问题由 WAL 重置操作的罕见交错触发。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://tailscale.com/blog/sqlite-wal-reset-bug">How Tailscale helped find the SQLite WAL-Reset bug</a></li>
<li><a href="https://www.youngju.dev/blog/2026-07-16-sqlite-wal-reset-bug.en">The SQLite WAL-Reset Bug: A Data Corruption Race That Hid for ...</a></li>
<li><a href="https://sqlite.org/vfs.html">The SQLite OS Interface or "VFS"</a></li>

</ul>
</details>

**社区讨论**: 评论者称赞这篇调试故事写得精彩且引人入胜。Simon Willison 强调了 Tailscale 资助特定开源调试工具的价值，其他人则指出一个具有讽刺意味的事实：SQLite 庞大的测试套件（9200 万条测试）仍未能发现这个错误，呼应了 Dijkstra 的观点：测试只能证明错误的存在，而不能证明其不存在。部分用户还赞赏 Tailscale 与 SQLite 签订支持合同的决定。

**标签**: `#SQLite`, `#database`, `#bug`, `#Tailscale`, `#open-source`

---

<a id="item-2"></a>
## [Qwen 发布 3.8-Max：首次开源 2.4 万亿参数 Max 级模型](https://t.me/zaihuapd/43151) ⭐️ 9.0/10

通义千问团队正式发布 Qwen 3.8-Max，参数规模达 2.4 万亿（活跃参数 95B），并宣布模型权重将于下周开源。这是 Qwen 首次对 Max 级别模型开放权重。 这一发布意义重大，因为开源一个 2.4 万亿参数的顶级模型可能让前沿 AI 能力更加普及，并加剧开源模型厂商之间的竞争。DeepSeek、Kimi 等竞品也在推进类似规模的开源模型。 该模型基于 Qwen 3.5 架构，在编码、工作、研究和长周期任务上全面提升；在编码测试中可自主运行超 10 天完成项目构建与自我进化。开放权重版目前仅提供 BF16 和 FP8 格式，且不具备官方 API 版的视觉输入和 1M 上下文长度等特性。

telegram · zaihuapd · 8月12日 16:13

**背景**: Qwen 3.8-Max 采用混合专家（MoE）架构，每个 token 只激活一小部分参数（95B），从而在推理成本接近较小稠密模型的同时拥有巨大的总参数量。在 MoE 模型中，路由器为每个 token 选择使用哪些专家子网络。FP8 是一种低精度格式，可大约减半内存占用并加速推理，同时保持接近 FP16 的精度。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://newsletter.maartengrootendorst.com/p/a-visual-guide-to-mixture-of-experts">A Visual Guide to Mixture of Experts ( MoE )</a></li>
<li><a href="https://nyvoraai.github.io/ai-news/what-is-a-mixture-of-experts-llm.html">What Is a Mixture of Experts LLM? 2026 Guide</a></li>
<li><a href="https://rcrtech.com/semiconductor-news/llms-quantization-fp8-fp4-int8/">LLMs and quantization: FP8, FP4, and INT8 explained</a></li>

</ul>
</details>

**社区讨论**: 评论者对该模型 1-bit 量化后约 397GB、能达到接近 Opus 级性能表示惊叹，但也指出 BF16 原始权重达 4.9TB，发布初期比 Kimi k3 更难部署。还有用户指出开放权重版不支持视觉和 1M 上下文，许可证对年收入超 5000 万美元的商业使用有限制。有用户提到网上对该模型实际性能的评价褒贬不一。

**标签**: `#AI`, `#Qwen`, `#Large Language Model`, `#Open Source`, `#Release`

---

<a id="item-3"></a>
## [DeepSeek V4 Pro 0813 发布：性能强劲且成本低廉](https://openrouter.ai/deepseek/deepseek-v4-pro-0813) ⭐️ 8.0/10

DeepSeek 于 2026 年 8 月发布了旗舰模型 V4 Pro 0813，这是一个 1.6T 参数的混合专家（MoE）模型，激活参数为 49B，配备混合注意力机制、三种推理模式，以及 1,048,576 token 的上下文窗口。该模型可通过 OpenRouter、Together AI 和 DeepSeek 官方 API 访问。 该模型以远低于竞品的价格提供接近前沿的性能：输入每百万 token 收费 0.435 美元，输出每百万 token 0.87 美元，这让更多开发者能够负担起前沿级别的开发与模拟任务。早期用户报告称，在繁重的编程和仿真任务中获得了显著的性能提升，且未引入新的问题。 据 Together AI 的官方描述，该模型支持最多 384,000 token 的输出，并采用混合注意力机制，提供三种推理模式。OpenRouter 还提供了 Artificial Analysis 的独立基准测试结果。

hackernews · explosion-s · 8月12日 16:04 · [社区讨论](https://news.ycombinator.com/item?id=49274600)

**背景**: DeepSeek 是一家总部位于杭州的中国人工智能公司，由对冲基金 High-Flyer 出资成立。其上一代模型 DeepSeek-V3 是一个 671B 参数的 MoE 模型，每 token 激活 37B 参数，采用了多头潜在注意力（MLA）和 DeepSeekMoE 架构。V4 Pro 系列延续了这一 MoE 设计，并将总参数规模大幅提升，但每个 token 只激活一小部分参数，从而保持高效的推理和较低的成本。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openrouter.ai/deepseek/deepseek-v4-pro-0813">DeepSeek V 4 Pro 0813 - API Pricing & Benchmarks | OpenRouter</a></li>
<li><a href="https://www.together.ai/models/deepseek-v4-pro-0813">DeepSeek V 4 Pro 0813 API: Pricing, Benchmarks & Docs | Together AI</a></li>
<li><a href="https://en.wikipedia.org/wiki/DeepSeek">DeepSeek - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上的评论者总体反响积极。一位开发者表示，他全天用该模型运行交通模拟器和物理引擎，约花费 12.50 美元（50% 缓存命中），效果出色。还有人称赞其性价比，称之前的 Flash 更新已经能用很低的成本完成繁重的开发工作；一位用户表示自己大多数时候并不需要 Opus 5 级别的智能，只求以最低成本把活儿干完。也有评论批评这个 OpenRouter 链接信息量太少，建议提供官方文档或基准测试的链接。

**标签**: `#deepseek`, `#llm`, `#ai-model`, `#release`, `#cost-performance`

---

<a id="item-4"></a>
## [xAI 发布 Grok 4.6，引发基准测试可信度热议](https://x.ai/news/grok-4-6) ⭐️ 8.0/10

xAI 发布了新前沿模型 Grok 4.6，该模型基于 1.5 万亿参数的 V9 基础架构，并进行了比 Grok 4.5 更长的补充训练，使用了经过筛选的模型生成数据和高品质工程数据。Artificial Analysis 随即发布了该模型的基准测试结果，引发社区热议。 Grok 4.6 标志着 xAI 全力参与前沿模型竞赛，直接与 OpenAI、Google 和 Anthropic 的模型竞争。社区讨论也凸显了人们日益怀疑快速提升的基准分数究竟代表真正的进步，还是基准测试作弊。 据 xAI 介绍，Grok 4.6 采用了改进的优化器和训练方案，并整合了 AI 编程平台 Cursor 的数据。Elon Musk 还称它是一个 2 万亿参数的模型，目标是挑战 Moonshot AI 的 Kimi K3，不过其他来源则称其基于 1.5 万亿参数的 V9 基础架构。

hackernews · iLuddite · 8月12日 15:32 · [社区讨论](https://news.ycombinator.com/item?id=49274027)

**背景**: 前沿 AI 模型（frontier models）是指在特定时间点上最先进、使用极大规模算力训练、并能在多个领域达到最先进水平的通用 AI 模型。像 Humanity's Last Exam、FrontierMath 和 SWE-bench 等 AI 基准被用来比较这些模型，但社区成员开始质疑，一些实验室是否在人为抬高分数，而非真正提升模型能力。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://x.ai/news/grok-4-6">Introducing Grok 4 . 6 | SpaceXAI</a></li>
<li><a href="https://en.wikipedia.org/wiki/Grok_(chatbot)">Grok (chatbot) - Wikipedia</a></li>
<li><a href="https://www.datacamp.com/blog/frontier-models">Frontier Models Explained: What Defines the Cutting Edge of AI | DataCamp</a></li>

</ul>
</details>

**社区讨论**: 评论区意见不一：有人称赞 Grok 速度快、回答简洁，也有人质疑为什么各大实验室都在两个月内突然达到 Fable 级别的模型性能，并猜测存在基准测试作弊。还有用户指出，xAI API 的默认系统提示可能导致模型拒绝讨论其自身指令。

**标签**: `#AI`, `#Grok`, `#xAI`, `#LLM`, `#Benchmarks`

---

<a id="item-5"></a>
## [Chrome 中小尺寸 JPEG 显示差异的成因](https://guillaumetech.github.io/posts/jpg-scaling-chrome/) ⭐️ 8.0/10

Chrome 在渲染微小 JPEG 时与其他浏览器不同，原因是它采用部分解压并缩小的方式，以速度优先于图像质量。这种优化可能使小图看起来比默认使用更高质量缩放算法的 Firefox 更模糊或更像素化。 这种跨浏览器渲染差异会影响依赖图标和界面元素图像一致性表现的 Web 开发者，甚至可能影响内嵌 Chrome 的 Electron 应用。了解原因有助于开发者选择合适的图像格式和分辨率，避免出现意外的视觉质量下降。 这种差异源自 Chrome 的部分 JPEG 解压实现及其缩放算法，该算法通常比 Firefox 更清晰、基于 Lanczos 的缩放更模糊。此问题不仅限于 JPEG——社区反馈显示 PNG 也可能受影响——而使用尺寸正确的源图像可以缓解该问题。

hackernews · gutechh · 8月12日 14:00 · [社区讨论](https://news.ycombinator.com/item?id=49272549)

**背景**: JPEG 是一种有损图像格式，通常先完整解压后再缩放显示。然而 Chrome 对于小图像可以跳过完整解压，只解码部分数据再进行缩放，从而产生可见的伪影。各浏览器使用不同的重采样算法：Chrome 通常偏向更快、更平滑（更模糊）的滤镜，而 Firefox 使用更清晰但也可能产生轻微振铃的滤镜。CSS 的 image-rendering 属性可以让开发者对缩放算法有一定控制。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://stackoverflow.com/questions/12022675/decode-part-of-jpeg-file">partial - Decode part of JPEG file - Stack Overflow</a></li>
<li><a href="https://entropymine.com/resamplescope/notes/browsers/">How web browsers resize images</a></li>
<li><a href="https://www.codestudy.net/blog/object-fit-cover-gives-pixelated-images-on-chrome/">object-fit: cover Pixelated Images in Chrome: Bug or ...</a></li>

</ul>
</details>

**社区讨论**: 评论者指出 PNG 也会出现同样问题，并提到 Chrome 与 Firefox 使用不同的缩放算法：Chrome 更模糊，Firefox 更清晰但偶尔有振铃。有用户询问 Firefox 是进行部分渲染还是完整渲染后再缩放，另一位用户分享了 Mozilla 关于低分辨率解压工作的 bug 单。大家还一致认为真正解决办法是使用尺寸合适的图像。

**标签**: `#browser-rendering`, `#image-scaling`, `#jpeg`, `#chrome`, `#performance`

---

<a id="item-6"></a>
## [AI 可能正在淘汰软件工程中的中层阶级](https://blog.florianherrengt.com/ai-removing-middle-class-software-engineering.html) ⭐️ 8.0/10

文章认为，AI 编码工具正在自动化常规编程工作，使高级工程师可以直接实现并审查 AI 生成的代码，而无需中层工程师参与。这可能会压缩甚至消除中层的软件工程职位。 这很重要，因为中层软件工程师通常是常见的职业阶梯；减少这些岗位可能重塑整个行业的职业发展路径、团队结构和就业保障。工程师将越来越需要专注于判断、架构和代码审查，而不是日常编码。 文章警告说，‘差劲’的工程师可能会借助 AI 将不良做法在组织内放大十倍，并提醒不要提交巨型 pull request。它建议工程师拆解、质疑并理解 AI 生成的代码，同时指出审查者应拒绝过于庞大的 PR。

hackernews · florianherrengt · 8月12日 13:20 · [社区讨论](https://news.ycombinator.com/item?id=49271994)

**背景**: 在传统的软件团队中，高级工程师负责设计和拆分任务，中层工程师实现代码，初级工程师在实践中学习。如今，GitHub Copilot 和 ChatGPT 等 AI 结对编程工具可以按需生成常规代码，因此高级工程师可以跳过中间环节。人们担心这会移除支撑中层职位的代码编写工作量，尽管监督和判断仍然不可或缺。

**社区讨论**: 评论者大多认同文章的观点。有人指出，‘差劲’的工程师现在可以把不良工程放大十倍；另一个人将 AI 形容为‘Stack Overflow 工程师的自动化’，因为高级工程师可以跳过 Jira 工单交接。还有人强调，工程师绝不能把批判性思维外包给 LLM，也不能停止学习，审查者应拒绝过于庞大的 PR。

**标签**: `#AI`, `#Software Engineering`, `#Career Impact`, `#Productivity`, `#Developer Tools`

---

<a id="item-7"></a>
## [高尔斯：LLM 擅长寻找反例，但还写不出优美证明](https://gowers.wordpress.com/2026/08/12/what-sort-of-maths-are-llms-good-at/) ⭐️ 8.0/10

菲尔兹奖得主蒂莫西·高尔斯在 2026 年 8 月的博文中分析了 LLM 擅长哪些数学任务，认为其优势在于基于采样的反例搜索，同时质疑它们能否产出优美且新颖的证明。 高尔斯作为顶尖数学家的评估有助于校准人们对 LLM 在数学领域能力的预期，并与关于测试时扩展的广泛讨论以及 AI 能否从暴力计算走向真正数学洞见的问题密切相关。 博文区分了 LLM 能胜任的任务（如通过大规模采样寻找反例）与需要新颖、意外且难以偶然发现的方法的任务。高尔斯认为，事后看来优美而自然的证明是顶尖人类数学的标志。

hackernews · ColinWright · 8月12日 10:04 · [社区讨论](https://news.ycombinator.com/item?id=49270022)

**背景**: 寻找反例是数学中的核心方法：要反驳一个全称命题，只需要一个矛盾的具体例子。测试时扩展（test-time scaling）指在推理阶段增加计算量，通常通过采样大量候选解来实现；这正是 LLM 擅长寻找反例的机制。高尔斯借此指出，基于采样的成功并不等于能够构造优美的新证明。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Counterexample">Counterexample - Wikipedia</a></li>
<li><a href="https://arxiv.org/abs/2503.24235">[2503.24235] A Survey on Test-Time Scaling in Large Language ... What, How, Where, and How Well? A Survey on Test-Time Scaling ... What, How, Where, and How Well? A Survey on Test-Time Scaling ... GitHub - testtimescaling/testtimescaling.github.io: "what ... Step-level Verifier-guided Hybrid Test-Time Scaling for Large ... What is test-time compute and how to scale it? - Hugging Face Efficient Test-Time Scaling for Small Vision-Language Models</a></li>

</ul>
</details>

**社区讨论**: 讨论内容充实且总体持赞赏态度。有评论者将高尔斯的文章重述为关于测试时扩展的论证，并引用 AlphaCode 在 2022 年通过采样数百万程序取得的成功。也有人赞同“优美且难以偶然得到的证明”才是检验人类级 AI 的关键标准；还有人指出 AI 数学成就列表往往偏向著名公开问题，并鉴于编程智能体在并发处理上的困难，好奇当前模型在时态逻辑等较冷门领域会表现如何。

**标签**: `#LLMs`, `#mathematics`, `#AI reasoning`, `#test-time scaling`, `#research`

---

<a id="item-8"></a>
## [Adam 打破旋转不变性，破坏隐式低秩偏置](https://www.reddit.com/r/MachineLearning/comments/1vmjb3p/the_loss_does_not_see_the_basis_but_adam_does_r/) ⭐️ 8.0/10

一个 Reddit 分析表明，Adam 的逐坐标二阶矩破坏了因子化矩阵模型中的旋转不变性，导致其失去梯度下降的隐式低秩偏置。对九种更新规则的扫描显示了两组清晰的聚类：GD、共享标量 Adam、Muon 和 Shampoo 保留该偏置，而 Adam、RMSProp、Lion、signum 和 Adafactor 则不能。 该工作指出了一个根本性质，用来区分保留隐式低秩偏置的优化器与不保留的优化器，这对矩阵感知和深度学习中的优化器设计具有直接影响。它还调和了关于 Muon 谱偏置的相互矛盾的结果，表明强简单性偏置和虚假特征拟合在同一条轴上同时存在。 一个将 Adam 的逐坐标分母逐渐转换为单一共享标量的单参数族，使得恢复性能单调提升，从而将损害归因于各向异性而非自适应性本身。该理论仅涵盖无记忆更新规则，因此基于动量的结果是经验性的；声称的 43-44% 留出误差下降依赖于一个仅用训练集调整学习率的规则，该规则对其他方法有利。

reddit · r/MachineLearning · /u/EtherealGlyph · 8月12日 16:39

**背景**: 对于形如 W=UV^T 的因子化模型，损失在旋转 (U,V)→(UQ,VQ) 下保持不变，而梯度下降尊重这种对称性。像 Adam 这样的自适应优化器会计算逐坐标的二阶矩，这依赖于因子写成的基，从而破坏这种不变性。隐式低秩偏置是指基于梯度的优化方法在求解诸如矩阵感知等欠定问题时倾向于收敛到低秩解的性质。Muon（MomentUm Orthogonalized by Newton-Schulz）和 Shampoo 是更先进的预处理优化器，实验显示它们保留了该偏置。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://kellerjordan.github.io/posts/muon/">Muon: An optimizer for hidden layers in neural networks | Keller Jordan blog</a></li>
<li><a href="https://arxiv.org/abs/1802.09568">[1802.09568] Shampoo: Preconditioned Stochastic Tensor ... optimizers/distributed_shampoo/README.md at main ... - GitHub Ashampoo® WinOptimizer Pro 29 - Optimize, clean, and protect ... SOAP: Improving and Stabilizing Shampoo using Adam Shampoo: Preconditioned Stochastic Tensor Optimization GitHub - Daniil-Selikhanovych/Shampoo_optimizer: Our ...</a></li>
<li><a href="https://www.sciencedirect.com/science/article/abs/pii/S1063520323000829">Gradient descent for deep matrix factorization: Dynamics and implicit bias towards low rank - ScienceDirect</a></li>

</ul>
</details>

**标签**: `#optimizer`, `#implicit bias`, `#low-rank`, `#Adam`, `#matrix sensing`

---

<a id="item-9"></a>
## [微信发布 WeLM：以资源效率为核心的大语言模型家族](https://x.com/Weixin_WeChat/status/2087509298310209718) ⭐️ 8.0/10

微信发布了以资源效率为核心的大语言模型家族 WeLM。该家族包含已应用于微信 AI 智能体“小微”的 WeLM-80B（3B 激活）以及采用混合专家（MoE）架构的 WeLM-617B（23B 激活）。 这一发布表明，一家大型科技公司将激活效率作为大语言模型的核心考量，大幅降低推理成本，使模型能够在消费者级规模落地。这可能会推动行业转向稀疏激活和 MoE 架构，而非一味扩展稠密模型。 WeLM-80B 拥有 800 亿参数，但每个 token 仅激活 30 亿参数，实现了极高的稀疏性。研发中的 WeLM-617B 通过 MoE 路由机制激活 230 亿参数，目标是在中等算力下实现更强的通用理解与推理能力；该模型将用于微信生态中的复杂任务，如小程序智能开发与“微信小微”小工具生成。

telegram · zaihuapd · 8月12日 13:58

**背景**: 传统的稠密大语言模型在处理每个 token 时会激活全部参数，计算成本高昂。混合专家（MoE）架构将网络划分为多个专家子网络，并通过一个小型路由器在每次处理时只激活其中部分专家，从而在保持模型容量的同时降低推理成本。WeLM 最初是一个拥有 100 亿参数的中文语言模型；新家族在此基础上扩展出了资源效率更高的稀疏设计。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/2209.10372">WeLM : A Well-Read Pre-trained Language Model for Chinese</a></li>
<li><a href="https://huggingface.co/blog/moe">Mixture of Experts Explained</a></li>

</ul>
</details>

**标签**: `#WeLM`, `#Large Language Models`, `#MoE`, `#WeChat`, `#AI Agent`

---

<a id="item-10"></a>
## [白宫拟将开源模型纳入 AI 政策，发布前需安全测试](https://www.wired.com/story/the-white-house-is-going-to-expand-its-ai-policy/) ⭐️ 8.0/10

白宫计划修订其 AI 政策框架，将开源模型纳入监管范围，一旦达到“前沿”能力便需在发布前接受安全测试。预计未来数月内推出，尽管合规仍是自愿性质。 此举将把政府监管从 Anthropic、OpenAI 等闭源实验室扩展到更广泛的开源生态，影响众多开发者与企业。这标志着达到前沿水平的开放权重模型将与专有模型同等对待，可能重塑开源 AI 的开发与发布方式。 该框架目前仍属自愿，部分原因在于特朗普认为正式监管只会帮助中国追赶美国。部分官员担忧，可能实施的 30 天发布前测试要求会抑制美国企业的创新与竞争力。

telegram · zaihuapd · 8月13日 00:43

**背景**: 目前白宫的 AI 政策框架只覆盖 Anthropic、OpenAI 等闭源模型。前沿 AI 模型是指处于市场可部署能力最前沿的高能力系统；它没有统一的技术定义，但在治理层面需要更强的保障。开放权重模型按约定条款公开权重，但可能不满足完整开源标准——后者通常要求更广泛的自由度和透明度。政府机构已开始对前沿模型进行发布前安全测试，部分第三方评估在保密协议下进行。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://nhimg.org/glossary/frontier-ai-model/">What Is Frontier AI model ? Definition & Examples</a></li>
<li><a href="https://www.pbs.org/newshour/science/whats-the-difference-between-closed-open‑source-and-open-weight-ai-a-researcher-explains">What's the difference between closed, open‑source and open-weight AI? A researcher explains | PBS News</a></li>
<li><a href="https://techcrunch.com/2026/08/09/the-ai-safety-test-is-becoming-a-safety-risk/">The AI safety test is becoming a safety risk | TechCrunch</a></li>

</ul>
</details>

**标签**: `#AI policy`, `#open-source models`, `#safety testing`, `#regulation`, `#White House`

---