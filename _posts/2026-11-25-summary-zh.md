---
layout: default
title: "Horizon Summary: 2026-11-25 (ZH)"
date: 2026-11-25
lang: zh
---

> 从 27 条内容中筛选出 11 条重要资讯。

---

1. [Anthropic 称内部 Claude 模型证明 VP ≠ VNP 并给出 Lean 4 形式化证明](#item-1) ⭐️ 9.0/10
2. [预印本声称矩阵乘法指数恰为 9/4](#item-2) ⭐️ 8.0/10
3. [PrismML 推出 Ternary Bonsai 2.5 27B：三元量化模型让本地也能跑智能体编程](#item-3) ⭐️ 8.0/10
4. [OpenAI 称 GPT-6.2 能通过写代码设计蛋白迷你结合子](#item-4) ⭐️ 8.0/10
5. [创始人被要求 24 小时内自证未蒸馏 Anthropic 模型](#item-5) ⭐️ 8.0/10
6. [社区项目让泄露的 GTA 6 Xbox 版本在 Windows 上运行](#item-6) ⭐️ 8.0/10
7. [Simon Willison 梳理十二个月内 LLM 的三个拐点](#item-7) ⭐️ 8.0/10
8. [GPT-6.2 Astra 自主破解 1808 年匿名速写本的作者身份](#item-8) ⭐️ 8.0/10
9. [华为与高通达成多年期广泛专利交叉许可，涵盖 5G 与人工智能](#item-9) ⭐️ 8.0/10
10. [VMware vCenter 再曝 9.8 分鉴权绕过漏洞，已被作为零日利用](#item-10) ⭐️ 8.0/10
11. [SpaceX 与特斯拉董事会设立特别委员会审议潜在合并](#item-11) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Anthropic 称内部 Claude 模型证明 VP ≠ VNP 并给出 Lean 4 形式化证明](https://t.me/zaihuapd/45345) ⭐️ 9.0/10

11 月 24 日，Anthropic 公开了论文《VP ≠ VNP over every field》以及配套的 Lean 4 形式化证明，仓库声明该结果由内部研究用 Claude 模型发现，论文与代码均由 AI 撰写。论文声称给出了哈密顿圈多项式的超多项式算术电路下界，并据此推出 VP 是 VNP 的真子类。 如果该结论成立，就等于解决了 Valiant 于 1979 年提出的代数复杂度猜想——一个常被称为 P 与 NP 问题代数版本的长期未解难题，这将成为 AI 系统参与前沿数学研究的最引人注目的案例之一。配套的可机器检验的 Lean 4 证明，也让该结果相比纯文字论证更容易被独立验证。 该结果只针对算术电路，明确不涉及布尔意义上的 P 与 NP 问题，因为代数电路必须对域中所有元素及其扩域都成立，而不只是对 0 和 1 成立。仓库称已通过三条标准公理审计与独立内核校验，但该消息目前源自一条 Telegram 帖子，仍需复杂度理论领域的独立审查。

telegram · zaihuapd · 11月24日 12:18

**背景**: 在代数复杂度理论中，VP 是由多项式规模的算术电路可计算的多项式集合（P 的代数类比），VNP 则是其非确定性对应物（NP 的类比）；Valiant 在 1979 年证明了在特征不为 2 的域上永久式（permanent）是 VNP 完全的。VP 是否等于 VNP 是 P 与 NP 问题的代数版本，证明二者分离已悬而未决数十年。Lean 4 是一个基于依赖类型论的开源证明助手兼函数式编程语言，其证明由一个小型可信内核机械校验，因此一个完整的 Lean 形式化能大幅降低出现细微逻辑错误的可能性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Arithmetic_circuit_complexity">Arithmetic circuit complexity - Wikipedia</a></li>
<li><a href="https://hexagonmath.org/2611.00954v1">VP ||#92;neq$ VNP over every field · Hexagon</a></li>
<li><a href="https://en.wikipedia.org/wiki/Lean_(proof_assistant)">Lean (proof assistant) - Wikipedia</a></li>

</ul>
</details>

**标签**: `#complexity theory`, `#VP vs VNP`, `#Lean 4`, `#AI for mathematics`, `#formal verification`

---

<a id="item-2"></a>
## [预印本声称矩阵乘法指数恰为 9/4](https://github.com/openai/math/blob/main/preprints/The-matrix-multiplication-exponent-is-nine-fourths-November-24-2026/paper.pdf) ⭐️ 8.0/10

一篇发布在 openai/math GitHub 仓库中的 OpenAI 相关预印本声称，矩阵乘法指数在所有域上都恰好是 9/4，即 Θ(n^2.25)；评论者将此描述为证明了与近期公布的某个上界算法相匹配的下界 Ω(n^2.25)。该论文是四篇与 OpenAI 相关的论文之一，据称这些论文解决了由大语言模型排名的 Top-500 开放问题清单中的八个问题。 如果得到验证，9/4 的精确指数将通过反驳“矩阵乘法指数等于 2”这一长期猜想，解决代数复杂性理论中的一个核心问题，并对线性代数、优化和圖算法产生 downstream 影响。这也加剧了关于 AI 实验室能否产生基础数学突破、以及此类声明应如何验证的争论。 该声明是一篇 GitHub 仓库中的预印本，而非显然经过同行评审的出版物，且所提供材料并未展示独立验证；评论者还称，该工作据报来自一个未公开配方的未发布模型。标题已从 O(n^2.25) 更正为 Θ(n^2.25)，一位评论者指出，一个实际的 O(n^2.25) 算法虽然具有渐近重要性，但远不实用。

hackernews · E-Reverance · 11月25日 01:19 · [社区讨论](https://news.ycombinator.com/item?id=50637220)

**背景**: 朴素地相乘两个 n×n 矩阵需要 Θ(n^3) 次域运算，而矩阵乘法指数 ω 是任何算法所能达到的指数下确界。Strassen 算法首次打破了 n^3，此后数十年的工作将上界逐步降低到接近 2，但证明高于 2 的非平凡下界一直很困难，这使得 ω=2 的猜想成为一个重大开放问题。Top-500 清单是由大语言模型排名的开放数学问题目录，并非专家共识，因此其排名提供的是背景而非重要性的证明。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Computational_complexity_of_matrix_multiplication">Computational complexity of matrix multiplication - Wikipedia</a></li>
<li><a href="https://www.proofatlas.ai/open-problems/">Top 500 Open Math Problems: LLM-assessed Importance — ProofAtlas</a></li>
<li><a href="https://www.effortlessmath.com/blog/can-we-trust-ai-math-proofs/">Can We Trust AI Math Proofs? How Lean Verifies Them</a></li>

</ul>
</details>

**社区讨论**: Hacker News 评论者既印象深刻又持怀疑态度：一些人将这批成果形容为 AI 实验室类似于贝尔实验室式的突破潮，另一些人则质疑 OpenAI 和 Anthropic 的动机、未发布模型与未公开配方，以及缺乏独立验证。还有几位评论者将标题中的 O(n^2.25) 更正为 Θ，并澄清新的贡献是下界。

**标签**: `#matrix-multiplication`, `#complexity-theory`, `#algorithms`, `#openai`, `#llm-research`

---

<a id="item-3"></a>
## [PrismML 推出 Ternary Bonsai 2.5 27B：三元量化模型让本地也能跑智能体编程](https://prismml.com/news/bonsai-2-5-27b) ⭐️ 8.0/10

PrismML 发布了 Ternary Bonsai 2.5 27B，这是一个 270 亿参数、采用三元量化的模型，能够在消费级硬件上本地运行智能体编程任务，支持 128k 上下文，生成速度约为每秒 22–30 个 token。PrismML 声称其在 SWE-bench Verified 上的表现接近约六个月前的前沿模型水平。 如果这一说法成立，一个能轻松装进 24GB 统一内存、性能又接近上一代前沿水平的 270 亿参数模型，意味着开发者可以完全离线运行能力不错的编程智能体，既不用按 token 付费，也不必把源代码交给第三方。这也进一步印证了小尺寸、激进量化模型只落后前沿约半年的趋势。 三元量化把每个权重限制在 {-1, 0, +1} 三个取值，约合每个权重 1.58 bit，模型以 Q2 GGUF 格式分发；一位社区测试者在配备 24GB 内存的 Mac Mini M5 Pro 上测得生成速度 22.3 tok/s、首 token 延迟 2.12 秒、提示处理速度 222.9 tok/s。有评论者指出，在官方公布的基准表格中该模型的原始分数看起来不如 Qwen，说明其真正优势在于内存占用和吞吐而非绝对准确率。

hackernews · b0m · 11月24日 20:08 · [社区讨论](https://news.ycombinator.com/item?id=50633922)

**背景**: 量化通过以更低精度存储权重来压缩模型，而三元量化是其中最极端的一种：每个权重只能取三个值之一，因此一个 270 亿参数的模型只需几 GB 而非几十 GB 内存，代价是损失一定精度。SWE-bench Verified 是一个广泛使用的基准，要求模型解决 Python 仓库中真实的 GitHub issue，通常被当作智能体编程能力的代理指标。这类模型之所以能在本地跑起来，主要得益于 Apple Silicon 等消费级芯片让 CPU 与 GPU 共享高速统一内存。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://prismml.com/news/prismml-introduces-ternary-bonsai-model-family">PrismML — PrismML Introduces Ternary Bonsai Model Family</a></li>
<li><a href="https://en.wikipedia.org/wiki/1.58-bit_large_language_model">1.58-bit large language model - Wikipedia</a></li>
<li><a href="https://www.swebench.com/">SWE-bench Leaderboards</a></li>

</ul>
</details>

**社区讨论**: Hacker News 的讨论以具体实测数据为主：测试者在 Mac Mini M5 Pro 上报告 22–25 tok/s，在 MacBook 上通过 Unsloth 得到约 300 tok/s 的预填充和 30 tok/s 的生成速度，其中一人称其在智能体调用上优于 inkling 2 mini Q4。一项长周期本地基准显示，它与 Bonsai 2 同样是 8 项通过 5 项，但步数减少 17%、实际耗时减少 29%；也有评论者在争论这一提升有多少是真实的小模型进步，多少是基准刷分或基准本身漂移所致。

**标签**: `#local-llm`, `#quantization`, `#small-language-models`, `#swe-bench`, `#agentic-coding`

---

<a id="item-4"></a>
## [OpenAI 称 GPT-6.2 能通过写代码设计蛋白迷你结合子](https://openai.com/index/gpt-6-models-demonstrate-intrinsic-protein-design-capabilities/) ⭐️ 8.0/10

OpenAI 称，GPT-6.2 在获得五个靶蛋白的三维结构及指定结合位点后，通过编写代码自行生成迷你结合子的三维设计，且实验室测试在五个靶点上均发现结合证据。 如果结果成立，这表明通用大模型可以把蛋白质设计转化为代码编写与工具编排任务，可能降低治疗性结合子早期发现的准入门槛并加快设计迭代。实际影响取决于 GPT-6.2 是在替代专用蛋白质模型，还是主要充当围绕这些模型的自动化层。 OpenAI 的流程仍依赖专用工具：SolubleMPNN 为 GPT-6.2 的三维设计建议氨基酸序列，其他专用蛋白质模型则帮助筛选那些被预测能按设计折叠并在预期位点结合的候选。评论者还指出，证据偏重计算探索，实验室对照相对有限。

hackernews · acossta · 11月24日 21:02 · [社区讨论](https://news.ycombinator.com/item?id=50634658)

**背景**: 蛋白质是由氨基酸组成并折叠成三维形状的链，而迷你结合子（minibinder）是被设计用来结合特定靶标的小型蛋白质。计算蛋白质设计通常把骨架生成、序列设计以及折叠或结合预测分开，由专用模型处理各个环节。像 GPT-6.2 这样的通用大语言模型能够编写代码，因此核心问题是它能否协调甚至替代这些专用工具。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openai.com/index/gpt-6-models-demonstrate-intrinsic-protein-design-capabilities/">GPT-6 models demonstrate intrinsic protein-design ... - OpenAI</a></li>
<li><a href="https://pmc.ncbi.nlm.nih.gov/articles/PMC11042314/">De novo design of protein minibinder agonists of TLR3 - PMC</a></li>
<li><a href="https://www.nature.com/articles/s41587-024-02123-4">Designing proteins with language models - Nature Biotechnology</a></li>

</ul>
</details>

**社区讨论**: Hacker News 评论者普遍认为结果有趣，但对“超越专用模型”的说法提出质疑：fabian2k 追问在 SolubleMPNN 提供序列的情况下 GPT-6.2 究竟设计了什么，plaidfuji 则认为 GPT 更像连接各专用工具且有前景的“胶水层”，并可能在部分子任务上表现更好。joe-esquibel 指出证据在实验室对照方面偏少、在计算探索方面偏多，gopalv 则强调写代码是这些模型的核心超能力。

**标签**: `#AI for science`, `#protein design`, `#LLM capabilities`, `#biotech`, `#AI agents`

---

<a id="item-5"></a>
## [创始人被要求 24 小时内自证未蒸馏 Anthropic 模型](https://news.ycombinator.com/item?id=50630809) ⭐️ 8.0/10

一位创始人在 Hacker News 上发帖称，Anthropic 指控其公司利用 Claude API 进行模型蒸馏，并给出 24 小时自证清白的期限。该创始人否认这一指控——公司并不训练自己的模型——并怀疑唯一可能触发标记的行为，是每次调整 AI 设置时运行的自动化回归基准测试。 这一事件暴露出：不透明的服务条款执行方式加上举证责任不清，会让依赖闭源大模型 API 的公司面临生死攸关的风险，因为一次封禁就可能在一夜之间切断其核心依赖。由于重复性的自动化基准测试是标准工程实践，许多 API 客户都可能陷入同样的误判模式。 真正的难点在于举证：创始人无法在不暴露用户数据的前提下交出原始流量日志或提示词/回复对，而 Anthropic 并未公开说明什么样的证据算合格。评论者建议提交生成基准测试的代码及其 git 提交历史，并先把材料交给 Claude 评估，看它在自动审核者眼中是否足以说明问题。

hackernews · weli · 11月24日 16:45

**背景**: 模型蒸馏（知识蒸馏）是指用更强的“教师”模型生成的输出去训练一个更小的“学生”模型，使竞争者能以较低成本逼近前沿模型的能力。正因如此，商业大模型供应商的条款通常禁止利用 API 输出去训练或改进竞争性模型，Anthropic 也表示其对 API 流量运行分类器和行为指纹识别，以检测蒸馏式使用模式。问题在于，蒸馏流量与合法的自动化评测流量具有相似特征——高调用量、系统性重复提示词、以及广泛覆盖模型行为——这恰恰是误报难以排除的原因。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/tashfeenahmed/freellmapi">tashfeenahmed/freellmapi: 10.1 billion tokens per month. 87 free LLM ...</a></li>
<li><a href="https://docs.litellm.ai/docs/">Getting Started | liteLLM</a></li>

</ul>
</details>

**社区讨论**: 评论者普遍同情这位创始人，并对执法流程持怀疑态度，建议他先把证据材料交给 Claude 自己审核一遍，因为 Anthropic 的审核人员很可能也会用 Claude。也有人建议改走 AWS Bedrock 接入 Claude，以获得可对接的人类客户经理；有人质疑为何还要继续付钱给这样对待客户的供应商；还有人指出，如果账号会因为提示词内容被封，那么故意在网页上植入蒸馏式指令就可能演变成一种提示词注入攻击向量。

**标签**: `#AI policy`, `#Anthropic`, `#model distillation`, `#API terms of service`, `#LLM providers`

---

<a id="item-6"></a>
## [社区项目让泄露的 GTA 6 Xbox 版本在 Windows 上运行](https://twitter.com/raul_bs3/status/2125213756238291075) ⭐️ 8.0/10

一个社区逆向工程项目借助类似 Wine 的兼容层与重编译方案，成功让泄露的 GTA 6 Xbox 版本在 Windows PC 上运行起来。推进此事的主力是 xcl 和 Victory 两个项目（以及相关的静态重编译框架 Leonida），据称他们基于泄露者 Cyberleek 放出的可执行文件开展工作。 这说明现代 Xbox 主机与 Windows PC 之间的技术鸿沟已经非常小，使得爱好者主导的“移植”在官方 PC 版发布之前很久就成为可能。此事也把游戏保存与逆向工程的合法性和伦理边界推到聚光灯下，并让人关注发行商是否会以更强的防篡改或始终在线保护来回应。 据社区成员介绍，该 Xbox 版本没有任何特殊的 DRM 或混淆保护，而现代 Xbox 硬件本质上就是一台带有额外主机专用组件的 Windows PC，因此真正的难题在于兼容层与图形翻译，而非破解保护。讨论中一个值得注意的细节是，相关项目 Leonida 此前曾在主要开发者还在上学时被 GitHub 封禁。

hackernews · andrem · 11月24日 13:19 · [社区讨论](https://news.ycombinator.com/item?id=50627783)

**背景**: 静态重编译是一种把主机二进制文件的机器码（例如 Xbox 360 游戏的 PowerPC 指令）翻译成 C 等高级语言，再编译为可在 x86-64 或 ARM64 上原生运行的代码的技术，介于模拟与真正的原生移植之间。Wine 的原理则不同：它是一个兼容层，拦截 Windows API 调用并将其翻译成宿主操作系统的对应实现，例如把 DirectX 映射到 OpenGL 或 Vulkan，从而无需完整虚拟机即可运行 Windows 可执行文件。由于当前 Xbox 在类 PC 的 AMD 硬件上运行衍生于 Windows 的操作系统，类似 Wine 的兼容层原则上只需相对有限的适配就能承载主机游戏代码。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://gta6recomp.com/leonida">Leonida — GTA 6 PC Static Recompilation Project Tracker & Source</a></li>
<li><a href="https://github.com/ivall/xcl">ivall/xcl: Xbox Series compatibility layer for Windows - runs console ...</a></li>
<li><a href="https://heldgames.com/guides/retro-decompilation-recompilation-explained">What Decompiled and Recompiled Games Actually Are... | Held Games</a></li>

</ul>
</details>

**社区讨论**: 评论者深入讨论了二进制兼容性、图形翻译、DRM 与防篡改等技术细节，也有人就合法性与行业影响展开争论；一种颇具共识的看法是，此事不会对游戏制作构成实质威胁，因为 GTA 6 利润极为丰厚，还能通过 DLC 和官方 PC 版再赚一轮。另一个反复出现的担忧是，这类社区成果可能促使发行商转向依赖云端的组件或始终在线的设计，使游戏无法被反编译或保存。

**标签**: `#game-reverse-engineering`, `#binary-compatibility`, `#wine`, `#game-preservation`, `#drm`

---

<a id="item-7"></a>
## [Simon Willison 梳理十二个月内 LLM 的三个拐点](https://simonwillison.net/2026/Nov/24/llm-inflection-points/) ⭐️ 8.0/10

Simon Willison 发布了一篇基于其在 AI Engineer Code Summit 主题演讲的回顾文章，提出过去十二个月里 LLM 与编程智能体的能力跨过了三个明显的拐点，并以 Claude Opus 4.5 发布一周年（2025 年 11 月 24 日）作为时间锚点。文章可见部分详细展开了其中两个：2025 年 11 月 Claude Opus 4.5 与 OpenAI 的 GPT-5.1 / GPT-5.1-Codex 让编程智能体默认就能可靠可用，以及 2026 年 6 至 7 月他所称的“Fable 级模型”登场。 这篇文章为这个高速演进的领域提供了一线从业者的历史分期视角，指出真正的分水岭是智能体的“可靠性”而非跑分——决定它是加速工程工作，还是只增加审阅负担。对于正在决定何时以及如何采用编程智能体的团队而言，Willison 的时间线说明能力跃迁往往以突然、离散的台阶形式出现，而非平缓爬升。 Willison 将“Fable 级模型”定义为：只要你能说清目标并提供必要工具，它们就能以蛮力方式把问题解决——例证是 Claude Fable 为了排查一个 Safari 显示故障，自行搭建了基于 pyobjc-framework-Quartz 的截图机制和一个启用 CORS 的本地日志服务器。他还提到 Claude Fable 5 在 2026 年 6 月曾因美国出口管制被短暂下架，直到 7 月 1 日才恢复，而公开文本在揭晓第三个拐点之前就已被截断。

rss · Simon Willison · 11月24日 23:02

**背景**: Claude Opus 4.5 由 Anthropic 于 2025 年 11 月 24 日发布，属于其 Haiku/Sonnet/Opus 命名体系中的最高一档，在编程与智能体任务上表现突出而广受关注。Claude Code 是 Anthropic 的终端编程智能体，最初于 2025 年 2 月随 Claude 3.7 Sonnet 一同推出；这类智能体可以代表开发者检视代码仓库、修改文件、执行终端命令并运行测试。2026 年 Anthropic 还研发出能力更强的 Claude Mythos，因网络安全方面的担忧而未向公众发布，随后推出了名为 Claude Fable 的限制版，禁止将其用于安全相关用途。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Claude_Opus_4.5">Claude Opus 4.5</a></li>
<li><a href="https://en.wikipedia.org/wiki/Claude_(AI)">Claude (AI) - Wikipedia</a></li>
<li><a href="https://cursor.com/learn/working-with-agents">Working with Agents | Cursor Learn</a></li>

</ul>
</details>

**标签**: `#LLMs`, `#coding agents`, `#AI engineering`, `#Claude Opus`, `#software development`

---

<a id="item-8"></a>
## [GPT-6.2 Astra 自主破解 1808 年匿名速写本的作者身份](https://simonwillison.net/2026/Nov/24/astra-historical-mystery/) ⭐️ 8.0/10

历史学家 Mark Humphries 记录了一次实验：在仅给出极少提示的情况下，GPT-6.2 Astra 仅用 22 分钟便自主利用公开的一手与二手资料，确认了耶鲁大学拜内克图书馆所藏一本 1808 年匿名速写本的作者身份。在此过程中，该模型还在一个纸质档案中找到了一份鲜为人知的文献，预测它能够验证自己的假设，而最终结果证明其判断正确。 这是一个具体案例，说明大语言模型可以作为自主研究代理运作，并产出真正新颖的学术成果，而不只是概括已有知识。它暗示 AI 代理可能很快重塑开放式档案研究与人文研究工作流，同时也引出这样一个问题：当机器能完成人类难以完成的工作时，各学科该如何应对。 关键线索是一则日记记载：沙博子爵（vicomte de Chabot）曾在速写本所记某条河流附近某日期之前五天到访，Astra 据此提出，沙博的旅行日记（只能向克利夫兰州立大学订购获取）可以确认作者身份。Humphries 指出这只是单一的轶事性案例，而非基准测试，不过新发现的这份档案本身对加拿大史与毛皮贸易史研究者而言就是一项重要收获。

rss · Simon Willison · 11月24日 16:53

**背景**: GPT-6.2 Astra 是 OpenAI GPT-6.2 模型家族的一员，于 2026 年 11 月 17 日与 GPT-6.2 Sol 一同发布，仅向付费用户开放，早期重度用户的评价褒贬不一。所谓自主代理（autonomous agent），是指能够独立规划并执行浏览、检索、对资料进行推理等多步骤任务的 AI 系统。拜内克图书馆是耶鲁大学的珍本与手稿图书馆，已将部分馆藏（包括这本速写本）数字化并公开在线访问。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/GPT-6.2_Astra">GPT-6.2 Astra</a></li>
<li><a href="https://simonwillison.net/2026/Nov/17/gpt62-astra-and-sol/">GPT ‑ 6 . 2 Astra and GPT ‑ 6 . 2 Sol | Simon Willison’s Weblog</a></li>
<li><a href="https://en.wikipedia.org/wiki/Autonomous_agent">Autonomous agent</a></li>

</ul>
</details>

**社区讨论**: Humphries 本人预测历史学界会经历一场“温和的”信心危机，并将其类比为数学界面对能解决难题的 AI 系统时的反应；但他认为历史学受到的冲击会更小，因为历史学家是在不断变化的当下重新解释过去，而非追求唯一的普世真理，并且历史写作更接近哲学与文学，其中“人”仍是必要条件。Simon Willison 则把这一结果视为 AI 辅助检索与代理式研究的一个值得注意的数据点。

**标签**: `#AI research agents`, `#LLMs`, `#digital humanities`, `#autonomous agents`, `#historical research`

---

<a id="item-9"></a>
## [华为与高通达成多年期广泛专利交叉许可，涵盖 5G 与人工智能](https://t.me/zaihuapd/45344) ⭐️ 8.0/10

华为官方宣布与高通达成一项为期多年、范围广泛的专利许可协议，双方在 5G、计算、人工智能和网络等多个领域的专利组合进行交叉许可，同时高通将购买华为部分美国专利。据彭博社援引华为发言人的说法，高通还同意获得华为“逻辑折叠”芯片制造技术相关专利的许可；华为称交易在获得必要监管批准并完成后，其专利许可协议的累计预期合同价值预计超过 69 亿美元（约合 463.02 亿元人民币）。 该协议把电信与移动芯片领域两家最大的参与者联系在一起，超过 69 亿美元的累计预期合同价值使其成为业界规模最大的专利安排之一，实际上化解了华为与高通多年的摩擦。据报道其中还包含华为逻辑折叠技术的授权，这一点尤为关键，因为它意味着华为可能把一项为绕开美国出口管制下先进制程限制而自研的技术路线变现。 该协议是专利组合的双向交叉许可，而非单向授权，并且仍需获得监管批准才能完成交割。华为表示其知识产权授权业务自 2021 年起已实现正向收入，而向高通转让的专利仅限华为部分美国专利，并非其全部专利组合。

telegram · zaihuapd · 11月24日 11:38

**背景**: 专利交叉许可能让企业互相开放大规模专利组合，从而避免诉讼；在 5G 领域这是通行做法，因为没有哪一家厂商掌握全部标准必要专利。华为的“逻辑折叠”技术由半导体业务部总裁何庭波在 2026 年 5 月的一场电路研讨会上发布，属于三维集成电路（3D IC）与先进封装范畴：通过混合键合把完整的逻辑电路面对面堆叠，使信号传播距离更短，从而提升晶体管密度与能效，而不是依赖更小的晶体管。华为将其视为绕开摩尔定律极限与美国制造限制的一条路径，并预计会应用于 2026 年的麒麟处理器。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://baike.baidu.com/item/逻辑折叠技术/67870423">逻辑折叠技术 - 百度百科</a></li>
<li><a href="https://insightsintegration.com/logic-folding-explained-huaweis-chip-packaging-breakthrough-that-could-redefine-the-ai-race/">Logic Folding Explained: Huawei's Chip Packaging Breakthrough ...</a></li>
<li><a href="https://www.huaweicentral.com/huawei-logicfolding-architecture-everything-you-need-to-know/">Huawei LogicFolding Architecture: Everything you need to know</a></li>

</ul>
</details>

**标签**: `#Huawei`, `#Qualcomm`, `#patent-licensing`, `#5G`, `#semiconductors`

---

<a id="item-10"></a>
## [VMware vCenter 再曝 9.8 分鉴权绕过漏洞，已被作为零日利用](https://thehackernews.com/2026/11/vmware-vcenter-hit-by-another-critical.html) ⭐️ 8.0/10

Broadcom 为 VMware 产品线的 23 个漏洞发布补丁，其中最核心的是 vCenter 目录服务（vmdir）中的鉴权绕过漏洞 CVE-2026-123903，CVSS 评分 9.8：只要网络可达 vCenter，攻击者无需任何凭据即可直接进入系统。该漏洞在补丁发布前几天就已经被作为零日漏洞在野利用。 vCenter 是企业 vSphere 的控制中枢，这里的免鉴权绕过实际上等于把整个环境中所有受管 ESXi 主机和虚拟机的管理员权限交给攻击者。而就在几天前，另一个同样 9.8 分的 vmdir 鉴权绕过漏洞刚刚曝光，这说明攻击者正在有针对性地挖掘这一组件并已取得成功，因此几乎所有大型虚拟化环境都应把立即打补丁列为最高优先级。 该漏洞仅要求攻击者能够网络访问 vCenter 部署，不需要任何有效凭据，也不需要用户交互；Broadcom 未提供任何临时缓解措施，因此打补丁是唯一的修复手段。由于漏洞在补丁可用之前就已被利用，防守方应把所有曾对外暴露的 vCenter 实例都视为可能已失陷，在打补丁之外还要主动排查入侵痕迹。

telegram · zaihuapd · 11月24日 14:50

**背景**: VMware vCenter 是 Broadcom 旗下用于管理 vSphere 的集中管理平台，负责管理 ESXi 虚拟化主机集群及其上运行的虚拟机。VMware 目录服务 vmdir（在 vCenter Server Appliance 上以 vmdird 进程运行）是一个多主复制的 LDAP 目录服务，存储平台的认证、证书、查询和许可信息，正因如此，其中的鉴权绕过漏洞危害极大。CVSS 9.8 属于“严重”级别中的最高档，通常保留给可远程利用、且不需要任何权限或用户交互的漏洞。本次事件紧随 2026 年 11 月 19 日发布的 VMSA-2026-0009 公告之后，该公告修复的是另一个同样 9.8 分、编号为 CVE-2026-123890 的 vmdir 鉴权绕过漏洞。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://thehackernews.com/2026/11/critical-vmware-vcenter-flaw-cvss-98.html">Critical VMware vCenter Zero-Day Flaw Lets Network Attackers ...</a></li>
<li><a href="https://www.rapid7.com/blog/post/etr-cve-2026-123890-critical-authentication-bypass-vmware-vcenter/">CVE-2026-123890: Critical Authentication Bypass in VMware vCenter</a></li>
<li><a href="https://nhimg.org/glossary/vmdir/">What Is vmdir ? Definition & Examples</a></li>

</ul>
</details>

**标签**: `#security`, `#vmware`, `#vulnerability`, `#cve`, `#enterprise-infrastructure`

---

<a id="item-11"></a>
## [SpaceX 与特斯拉董事会设立特别委员会审议潜在合并](https://t.me/zaihuapd/45351) ⭐️ 8.0/10

SpaceX 与特斯拉的董事会各自成立了由独立董事组成的特别委员会，负责审议两家公司可能进行的合并。马斯克表示，委员会是应股东要求设立的，他因存在利益冲突将不参与相关讨论，并称双方尚未就交易条款达成一致。 把全球领先的私营航天发射公司与最大的纯电动汽车制造商合并，将把马斯克控制的多项资产集中到一个实体中，从而重塑航天与汽车两大行业格局。由于马斯克同时担任两家公司的 CEO 和大股东，特别委员会这一安排表明，治理与利益冲突问题将是交易能否推进的核心。 马斯克支持这一构想，但强调交易远未确定，最终仍需股东支持；SpaceX 方面获得股东投票通过相对容易，而特斯拉则需要获得全体股东中 50%的赞成票。特别委员会由独立董事组成，目前双方尚未就任何交易条款进行谈判。

telegram · zaihuapd · 11月25日 00:41

**背景**: SpaceX 是马斯克旗下的私营火箭与卫星公司，特斯拉则是上市的电动汽车与能源企业，两者不仅同由马斯克担任首席执行官，还在卫星宽带、先进制造等领域存在交集。由独立董事组成的特别委员会是常见的公司治理机制，通常在交易对管理层或控股股东构成利益冲突时启用。由于 SpaceX 并未上市，任何合并都将涉及复杂的估值与换股问题，并需通过监管审查。

**标签**: `#SpaceX`, `#Tesla`, `#merger`, `#Elon Musk`, `#corporate governance`

---