---
layout: default
title: "Horizon Summary: 2026-07-05 (ZH)"
date: 2026-07-05
lang: zh
---

> 从 37 条内容中筛选出 12 条重要资讯。

---

1. [安娜的档案馆悬赏 20 万美元获取谷歌图书扫描件](#item-1) ⭐️ 9.0/10
2. [提示注入攻击泄露 YouTube 创作者的私密视频](#item-2) ⭐️ 9.0/10
3. [新的稀疏微调方法 USAF：在消费级 GPU 上微调 MoE 模型](#item-3) ⭐️ 9.0/10
4. [GPT-5.5 Codex 推理标记聚类导致性能下降](#item-4) ⭐️ 8.0/10
5. [Zig 将包管理从编译器移至构建系统](#item-5) ⭐️ 8.0/10
6. [LLM 会话/缓存泄漏风险跨用户账号](#item-6) ⭐️ 8.0/10
7. [sqlite-utils 4.0rc2：AI 代码审查用 Claude Fable 发现关键漏洞](#item-7) ⭐️ 8.0/10
8. [模型越好，工具越差：新 Claude 模型在工具架构上表现不佳](#item-8) ⭐️ 8.0/10
9. [BaryGraph 将关系作为知识图谱中的一等文档](#item-9) ⭐️ 8.0/10
10. [华为发表“韬定律”：以时间缩微延续半导体演进](#item-10) ⭐️ 8.0/10
11. [谷歌 Chrome 网上应用商店禁止 AI 越狱及预测市场扩展](#item-11) ⭐️ 8.0/10
12. [iOS 27 将加入 Trust Insights 反欺诈功能](#item-12) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [安娜的档案馆悬赏 20 万美元获取谷歌图书扫描件](https://software.annas-archive.gl/AnnaArchivist/annas-archive/-/work_items/234) ⭐️ 9.0/10

安娜的档案馆宣布悬赏 20 万美元，以获取谷歌图书的所有扫描件，旨在大幅扩展其数字图书馆馆藏。 这项悬赏可能大幅增加全球范围内数字化图书的可获取性，尤其对书籍资源匮乏国家的用户意义重大，同时也挑战了数字存档领域的版权和法律规范。 悬赏针对谷歌图书的“所有扫描件”，可能需要大规模数据提取。安娜的档案馆是一个非营利项目，聚合了 Library Genesis、Sci-Hub 和 Z-Library 的内容。

hackernews · Cider9986 · 7月4日 16:51 · [社区讨论](https://news.ycombinator.com/item?id=48786838)

**背景**: 安娜的档案馆是一个非营利项目，致力于通过备份数字图书馆来保存人类的所有知识和文化。谷歌图书已扫描了数百万册图书，但访问常受版权限制。此类悬赏激励个人释放受限数据以造福公众。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Anna's_Archive">Anna ' s Archive - Wikipedia</a></li>
<li><a href="https://annas-archive.gl/">Anna ’ s Archive : LibGen (Library Genesis), Sci-Hub, Z-Library in one...</a></li>

</ul>
</details>

**社区讨论**: 评论者表达了对安娜的档案馆的感激，因为它提供了他们原本无法获得的书籍，尤其是在书籍资源有限的地区。还有人讨论了 SourceLibrary.org 等相关项目，并提出了对互联网爬取和隐私的担忧。

**标签**: `#digital archives`, `#bounty`, `#books`, `#Google Books`, `#Anna's Archive`

---

<a id="item-2"></a>
## [提示注入攻击泄露 YouTube 创作者的私密视频](https://javoriuski.com/post/youtube) ⭐️ 9.0/10

YouTube Studio 的 AI 评论提示功能存在提示注入漏洞，攻击者通过在评论中嵌入恶意指令，可以泄露创作者的私密或未公开视频。 该漏洞影响数百万依赖 YouTube Studio 的创作者，可能泄露敏感内容，并削弱用户对 AI 辅助审核工具的信任。 攻击原理是创作者点击评论区的建议 AI 提示后，被注入的评论操控 AI 泄露视频标题。攻击者使用看似官方支持的评论来欺骗系统。

hackernews · javxfps · 7月4日 16:45 · [社区讨论](https://news.ycombinator.com/item?id=48786781)

**背景**: 提示注入是一种安全攻击，攻击者制作特定输入，使大语言模型（LLM）忽略开发者指令并产生意外行为。YouTube Studio 最近推出了 Ask Studio 功能，这是一个利用 LLM 帮助创作者分析评论和频道数据的 AI 助手。如果攻击者留下精心构造的评论，AI 可能将其解读为指令并泄露隐私数据。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Prompt_injection_attack">Prompt injection attack</a></li>
<li><a href="https://support.google.com/youtube/answer/16291691?hl=en">Learn about Ask Studio in YouTube Studio - YouTube Help</a></li>

</ul>
</details>

**社区讨论**: 讨论中有一位前 Google 员工解释了内部处理流程，有用户测试该漏洞并部分成功，多数人认为 YouTube 应将提示注入视为严重漏洞。文章本身因清晰简洁的风格受到赞扬。

**标签**: `#security`, `#prompt-injection`, `#youtube`, `#vulnerability`, `#xss`

---

<a id="item-3"></a>
## [新的稀疏微调方法 USAF：在消费级 GPU 上微调 MoE 模型](https://www.reddit.com/r/MachineLearning/comments/1unl62q/if_your_gpu_can_run_inference_it_should_be_able/) ⭐️ 9.0/10

一种名为 USAF 的新型稀疏微调方法已发布，可以在消费级 GPU 上以与推理相同的显存需求微调混合专家（MoE）模型。作者演示了在 12GB 显存的 AMD RX 6750 XT 上微调 Qwen3-30B-A3B。 这使大型 MoE 模型的微调变得普及，此前需要高端 GPU。它能让研究人员和爱好者用可负担的硬件适配顶尖的 MoE 模型。 USAF 通过仅训练稀疏专家权重和路由器工作，而非像 LoRA 那样添加适配器。它完全开源，采用 Apache 2.0 许可证，且无需任何自定义 CUDA 内核。

reddit · r/MachineLearning · /u/tsuyu122 · 7月4日 21:56

**背景**: 混合专家（MoE）模型是一种神经网络，它使用多个‘专家’子网络，并由一个路由器为每个输入选择激活哪些专家。这可以在不按比例增加计算成本的情况下扩展模型规模。然而，微调 MoE 模型通常需要比推理更多的显存，因为梯度更新会影响所有参数。USAF 通过仅更新稀疏专家权重和路由器来解决这个问题，使显存使用与推理相近。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://medium.com/@apoorvajain1111/inside-the-sparse-brain-how-mixture-of-experts-moe-makes-llms-smarter-faster-and-greener-205b0fea1416">Inside the Sparse Brain: How Mixture - of - Experts ( MoE )... | Medium</a></li>
<li><a href="https://sumitdotgh.github.io/ai-examples/tiny-moe-based-model/">Tiny MoE model - AI Examples</a></li>

</ul>
</details>

**标签**: `#machine learning`, `#fine-tuning`, `#MoE`, `#open source`, `#GPU`

---

<a id="item-4"></a>
## [GPT-5.5 Codex 推理标记聚类导致性能下降](https://github.com/openai/codex/issues/30364) ⭐️ 8.0/10

用户报告称，GPT-5.5 Codex 的推理标记聚类导致模型输出错误结果，标记以固定间隔（如 516 和 518 个标记）聚类，造成性能下降。 这一性能回退影响了依赖 Codex 进行复杂推理任务的开发者，削弱了对模型的信任，并促使用户转向 Claude 或本地模型等替代方案。它凸显了在 AI 编程助手中保持质量一致性的持续挑战。 该问题可通过 Codex CLI 使用谜题提示复现；当模型恰好使用 516 个思考标记时，常返回错误结果，而使用 6000-8000 个标记时则给出正确答案。还观察到标记数以 518 为间隔聚类的现象。

hackernews · maille · 7月4日 21:51 · [社区讨论](https://news.ycombinator.com/item?id=48789428)

**背景**: 推理标记是大型语言模型在思维链推理过程中生成的额外标记，旨在提升性能。标记聚类指模型输出标记数集中在特定值附近的现象，可能表明内部优化问题。GPT-5.5 模型于 2026 年 4 月发布，声称改进了标记效率，但此缺陷表明存在实现问题。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openai.com/index/introducing-gpt-5-5/">Introducing GPT-5.5 | OpenAI</a></li>
<li><a href="https://news.ycombinator.com/item?id=48789428">GPT-5.5 Codex reasoning - token clustering may be... | Hacker News</a></li>
<li><a href="https://arxiv.org/pdf/2506.22638">Layer Importance for Mathematical Reasoning is Forged in...</a></li>

</ul>
</details>

**社区讨论**: 社区表达了沮丧和担忧，用户确认了这一性能回退，并将其与 Claude Code 的类似事件相比较。有人建议切换到本地模型或 GLM 5.2 等替代方案。对于 OpenAI 的响应速度存在怀疑，因为该问题已持续数月。

**标签**: `#GPT-5.5`, `#Codex`, `#AI performance regression`, `#reasoning tokens`, `#OpenAI`

---

<a id="item-5"></a>
## [Zig 将包管理从编译器移至构建系统](https://ziglang.org/devlog/2026/#2026-06-30) ⭐️ 8.0/10

Zig 于 2026 年 6 月 30 日宣布，将所有包管理功能从编译器移至构建系统。这标志着该语言的一次重大架构转变。 这一变更将包管理与编译器解耦，可能提升编译器性能并实现更灵活的构建过程。它反映了 Zig 持续向模块化、可维护工具链演进的设计方向。 此次迁移将依赖解析、获取和整合从编译器的职责中移除，构建系统现在负责这些任务。这与长期目标——在 WebAssembly 虚拟机中运行构建系统——相一致。

hackernews · tosh · 7月4日 16:30 · [社区讨论](https://news.ycombinator.com/item?id=48786638)

**背景**: Zig 是一种注重鲁棒性和最优性的通用系统编程语言，其构建系统是管理项目编译和依赖的核心组件。此前，包管理直接集成在编译器中，使编译器代码复杂化。此次迁移简化了编译器，并让构建系统能够独立演进。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://ziglang.org/learn/build-system/">Zig Build System ⚡ Zig Programming Language</a></li>
<li><a href="https://ziglang.org/">Home Zig Programming Language</a></li>

</ul>
</details>

**社区讨论**: 评论中反应不一。一些开发者质疑为何包管理曾被放在编译器中，其他人则对未来计划（如基于 WebAssembly 的构建系统）表示兴奋。总体情绪积极，对 Zig 的开发方向表示赞赏。

**标签**: `#Zig`, `#package management`, `#build system`, `#language design`

---

<a id="item-6"></a>
## [LLM 会话/缓存泄漏风险跨用户账号](https://github.com/anthropics/claude-code/issues/74066) ⭐️ 8.0/10

多名用户报告称，来自不同提供商（包括 Claude 和 GPT 模型）的 LLM 服务可能会在账户间泄漏会话上下文或缓存响应，可能导致敏感数据暴露。 这一安全漏洞可能危及广泛使用的 AI 助手中的用户隐私和数据机密性，影响依赖这些服务处理敏感任务的个人用户和企业。 具体报告的事例包括 API 网关处理 HTTP 100 状态码时出现 off-by-one 错误，以及缓存冲突导致返回其他用户会话的响应。Claude Code 团队正在调查，但目前认为这些报告属于幻觉。

hackernews · chatmasta · 7月4日 14:03 · [社区讨论](https://news.ycombinator.com/item?id=48785485)

**背景**: 会话和缓存隔离是多租户 AI 平台中的关键安全属性：每个用户的上下文、对话历史和临时数据必须严格分离。当隔离失败时，可能发生跨会话泄漏，暴露隐私信息。该问题类似于传统 Web 应用程序漏洞，但由于 LLM 输出的非确定性，更难以检测。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.giskard.ai/knowledge/cross-session-leak-when-your-ai-assistant-becomes-a-data-breach">Cross Session Leak: LLM security vulnerability & detection guide</a></li>
<li><a href="https://news.ycombinator.com/item?id=48785485">Potential session/cache leakage between workspace instances or consumer accounts | Hacker News</a></li>
<li><a href="https://eucloudservers.com/security-encryption/potential-session-cache-leakage-between-workspace-instances-or-consumer-accounts/">Potential session/cache leakage between workspace instances or...</a></li>

</ul>
</details>

**社区讨论**: 社区意见不一：一些用户提供了潜在泄露的详细技术描述，而另一些人则认为这些报告是幻觉或由长上下文窗口引起。一名 Claude Code 团队成员确认收到了报告，并表示他们确信这是幻觉，但正在进一步调查。

**标签**: `#AI`, `#security`, `#cache leakage`, `#LLM`, `#privacy`

---

<a id="item-7"></a>
## [sqlite-utils 4.0rc2：AI 代码审查用 Claude Fable 发现关键漏洞](https://simonwillison.net/2026/Jul/5/sqlite-utils-fable/#atom-everything) ⭐️ 8.0/10

Simon Willison 发布 sqlite-utils 4.0rc2，此前使用了 Claude Fable 对 4.0rc1 进行代码审查，花费约 149.25 美元。AI 发现了五个发布阻塞漏洞，包括 delete_where()中的数据丢失漏洞，导致 34 次提交和 1,321 行代码更改。 这展示了 AI 辅助代码审查对开源项目的实际价值，能够捕获可能需要 5.0 版本才能修复的严重漏洞。这表明大型语言模型能够以相对较低的成本显著提高软件质量。 Claude Fable 将五个问题分类为‘发布阻塞’，最严重的是 delete_where()从不提交且毒化数据库连接，导致静默数据丢失。审查过程涉及 37 次提示，跨越多个会话，作者在 AI 工作时参加了游行。

rss · Simon Willison · 7月5日 01:00

**背景**: sqlite-utils 是一个用于操作 SQLite 数据库的 Python CLI 工具和库，由 Simon Willison 创建。Claude Fable 是 Anthropic 的大型语言模型，以其编程和分析能力著称。语义化版本控制（SemVer）意味着破坏性变更需要主版本号升级，因此在稳定版发布前发现漏洞至关重要。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/simonw/sqlite-utils">GitHub - simonw/sqlite-utils: Python CLI utility and library for manipulating SQLite databases · GitHub</a></li>
<li><a href="https://en.wikipedia.org/wiki/Claude_Fable">Claude Fable</a></li>
<li><a href="https://sqlite-utils.datasette.io/">sqlite-utils</a></li>

</ul>
</details>

**标签**: `#AI-assisted development`, `#sqlite-utils`, `#code review`, `#open source`, `#Claude`

---

<a id="item-8"></a>
## [模型越好，工具越差：新 Claude 模型在工具架构上表现不佳](https://simonwillison.net/2026/Jul/4/better-models-worse-tools/#atom-everything) ⭐️ 8.0/10

Armin Ronacher 报告称，较新的 Claude 模型（Opus 4.8、Sonnet 5）在工具调用架构中比旧模型更频繁地发明额外字段，导致被 Pi 等第三方编码工具拒绝。尽管这些模型整体能力更强，但出现了这种退化。 此问题揭示了一个反直觉的趋势：模型改进可能会降低特定结构化输出任务的可靠性，给依赖严格架构遵循的 AI 工具开发者带来实际挑战。可能迫使第三方工具制作者针对不同模型调整实现。 问题特别出现在 Pi 编辑工具调用的嵌套`edits[]`数组中，新模型会插入虚构的键。Armin 推测这是因为 Anthropic 针对 Claude Code 自有编辑工具的强化学习训练，导致模型过度拟合内部架构。

rss · Simon Willison · 7月4日 22:53

**背景**: 像 Claude 这样的大型语言模型可以获取工具定义，并期望其调用参数符合 JSON 架构。工具调用是编码代理的关键能力。然而，不同模型在精确遵循架构方面可能有所不同，第三方工具（如个人 AI 助手 Pi）定义了自己的工具。帖子对比了 Anthropic 的搜索替换编辑工具与 OpenAI 的 apply_patch 机制。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://devtk.ai/en/blog/ai-structured-output-guide-2026/">AI Structured JSON Output: Model Support & Code... - DevTk.AI</a></li>
<li><a href="https://aiskillcerts.com/blog/claude-picasso-structured-output-prompt-patterns">Claude Picasso: Sculpting Strict Structured Output · AI Skill Certs</a></li>
<li><a href="https://llm-stats.com/leaderboards/best-ai-for-tool-calling">Best AI for Tool Calling 2026 - Top Function Calling Models</a></li>

</ul>
</details>

**标签**: `#LLMs`, `#tool-calling`, `#JSON schema`, `#Claude`, `#AI reliability`

---

<a id="item-9"></a>
## [BaryGraph 将关系作为知识图谱中的一等文档](https://www.reddit.com/r/MachineLearning/comments/1un3lsf/barygraph_knowledge_graph_where_every/) ⭐️ 8.0/10

BaryGraph 引入了一种新颖的知识图谱架构，其中每个关系都被嵌入为称为 BaryEdge 的独立文档，并且可以递归组合成 MetaBary 三元组，从而揭示平面向量搜索无法发现的概念桥梁。该系统基于完整的英文维基词典（660 万文档）构建，使用本地工具：MongoDB Community、mongot 和 nomic-embed-text。 该方法直接解决了标准 RAG 和向量搜索的一个关键局限性——它们将关系视为点邻近性的副产品——通过使关系语义可显式检索。这使得跨领域桥接成为可能，例如，将章鱼神经科学与分布式传感器网络联系起来，这可能显著改善 AI 系统的推理和知识发现能力。 BaryGraph 使用公式 bary_vector = normalize(q·v(CM1) + q·v(CM2) + (1−q)·v(type)) 对关系进行编码，其中 q 是连接质量，v(type) 是上下文嵌入，并且它无需额外嵌入调用即可构建层次结构。在 SimLex-999 上，结构指标（共享 BaryEdge、邻域重叠）与人类判断的相关性 ρ ≈ 0.32–0.53，而原始余弦相似度则无相关性（ρ ≈ −0.04）。

reddit · r/MachineLearning · /u/adseipsum · 7月4日 08:24

**背景**: 传统知识图谱将关系表示为节点之间的边，这些边本身不可检索。在 RAG 中，向量搜索通常通过嵌入相似性检索文档，但关系只能从邻近性中推断。BaryGraph 将每个关系视为具有自身嵌入的一等可检索文档。它使用 BaryEdge 作为嵌入的关系文档，并递归堆叠形成 MetaBary 三元组，创建一种森林结构，支持高效遍历。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://thysrael.github.io/Horizon/2026/07/04/summary-zh.html">Horizon Summary: 2026-07-04 (ZH) | Horizon Daily</a></li>
<li><a href="https://www.sourcetrail.com/software/mongodb-mongot-source-code-and-the-future-of-search-and-rag/">MongoDB mongot source code: search and vector explained</a></li>

</ul>
</details>

**标签**: `#knowledge graph`, `#RAG`, `#embeddings`, `#vector search`, `#machine learning`

---

<a id="item-10"></a>
## [华为发表“韬定律”：以时间缩微延续半导体演进](https://t.me/zaihuapd/42346) ⭐️ 8.0/10

在 2026 年于上海举办的 IEEE 国际电路与系统研讨会（ISCAS 2026）上，华为正式提出“韬定律”（τ定律），主张以“时间缩微”替代传统的“几何缩微”。华为宣称过去六年已据此设计并量产 381 款芯片，今年秋季将推出采用“逻辑折叠”技术的新麒麟手机芯片。 随着摩尔定律逼近物理极限，“韬定律”通过系统级优化为半导体性能持续提升提供了潜在新范式，可能重塑行业方向并降低对极紫外光刻的依赖。若得到验证，这将是华为乃至全球芯片产业的重大突破，尤其在地缘政治限制下意义深远。 “韬定律”致力于降低从器件、电路到芯片和系统的时间常数（τ），目标是在 2031 年实现等效 1.4 纳米制程的晶体管密度。其核心“逻辑折叠”技术是在单颗晶圆片内部进行三维堆叠，不同于传统先进封装，通过重新规划电路逻辑路径的三维结构来缩短信号传输距离。

telegram · zaihuapd · 7月4日 04:56

**背景**: 摩尔定律预测晶体管密度约每两年翻一番，但由于几何缩微面临物理和经济极限而放缓。传统缩微通过缩小特征尺寸来提升密度和性能，但在 3 纳米以下愈发困难。华为的路径则转而优化时间延迟和系统架构，借助多年在美国制裁下进行芯片设计的经验，寻找替代方案。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://news.qq.com/rain/a/20260525A041XU00">华为正式发表「韬（τ）定律」：用「时间缩微」替代「几何缩微」</a></li>
<li><a href="https://www.zaobao.com.sg/news/china/story20260525-9105489">【早知】“ 韬 定 律 ”是什么？ | 联合早报</a></li>

</ul>
</details>

**标签**: `#semiconductor`, `#Moore's Law`, `#Huawei`, `#chip design`, `#innovation`

---

<a id="item-11"></a>
## [谷歌 Chrome 网上应用商店禁止 AI 越狱及预测市场扩展](https://developer.chrome.com/blog/cws-policy-updates-2026) ⭐️ 8.0/10

2026 年 7 月 1 日，谷歌宣布更新 Chrome 网上应用商店政策，明确禁止用于 AI 越狱（绕过 AI 安全护栏）和预测市场（对事件结果进行真实货币交易）的扩展，新规于 2026 年 8 月 1 日生效。同时，政策收紧数据收集规则，要求扩展仅收集严格必要的数据，并显著披露数据收集行为。 此次更新对 Chrome 扩展生态系统产生重大影响，可能导致许多热门 AI 工具和预测市场应用被下架，并为平台治理 AI 安全及金融投机树立先例。开发者现在必须审计其扩展以确保合规，用户可能会失去某些功能。 新规追溯适用于所有现有扩展；违规可能导致从 Chrome 网上应用商店下架。如果安装后数据处理方式发生变化，开发者必须主动告知用户。

telegram · zaihuapd · 7月4日 06:30

**背景**: AI 越狱指通过提示注入等技术诱使大语言模型绕过安全过滤器，可能生成有害内容。预测市场允许用户对未来事件（如选举、体育赛事）的结果进行真钱投注，在许多司法管辖区被视为赌博。谷歌此举符合对 AI 安全及未受监管金融产品日益增长的监管关注。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/AI_jailbreak">AI jailbreak</a></li>
<li><a href="https://en.wikipedia.org/wiki/Prediction_market">Prediction market</a></li>

</ul>
</details>

**标签**: `#Chrome`, `#extensions`, `#policy`, `#AI`, `#data-privacy`

---

<a id="item-12"></a>
## [iOS 27 将加入 Trust Insights 反欺诈功能](https://www.cultofmac.com/news/ios-27-trust-insights-feature) ⭐️ 8.0/10

Apple 在 iOS 27 中引入了 Trust Insights，这是一个全新的设备端行为分析框架，用于检测用户在电话诈骗中被胁迫转账或修改账户的行为。 该功能通过设备端处理增强了用户对社会工程诈骗的防范，同时保护隐私，但其效果取决于开发者的广泛接入。 Trust Insights 分析用户的操作模式、时机、上下文和传感器数据，不会读取信息、邮件或照片内容，原始数据会立即删除，只向服务器发送单一输出值。

telegram · zaihuapd · 7月4日 14:30

**背景**: 电话诈骗通常涉及诈骗者在电话中指导受害者完成转账或修改账户等步骤。传统的欺诈检测依赖服务器端对交易的分析，可能错过行为线索。Trust Insights 利用保护隐私的设备端机器学习实时检测异常行为。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://news.google.com/stories/CAAqNggKIjBDQklTSGpvSmMzUnZjbmt0TXpZd1NoRUtEd2pSbDRmQ0VSRjR5NFFzQy1Tb1d5Z0FQAQ?hl=en-US&gl=US&ceid=US:en">Google News - Apple introduces Trust Insights to detect scams in...</a></li>
<li><a href="https://www.ithinkdiff.com/ios-27-trust-insights-scam-detection-framework/">iOS 27 Adds Trust Insights to Detect Scams Before They Happen</a></li>

</ul>
</details>

**标签**: `#iOS`, `#anti-fraud`, `#privacy`, `#machine learning`, `#security`

---