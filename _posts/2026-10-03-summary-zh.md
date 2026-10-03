---
layout: default
title: "Horizon Summary: 2026-10-03 (ZH)"
date: 2026-10-03
lang: zh
---

> 从 31 条内容中筛选出 6 条重要资讯。

---

1. [Google 通过 Fairwind 计划发布前沿模型 Gemini 4 Argon](#item-1) ⭐️ 9.0/10
2. [2025 年诺贝尔生理学或医学奖授予外周免疫耐受发现者](#item-2) ⭐️ 9.0/10
3. [AI 终于攻克《Stratego》，以更低成本击败史上最强人类玩家](#item-3) ⭐️ 8.0/10
4. [Redis 之父 antirez 发布本地 LLM 推理引擎 ds4](#item-4) ⭐️ 8.0/10
5. [arXiv 对未核查 LLM 生成内容的投稿实施一年禁投处罚](#item-5) ⭐️ 8.0/10
6. [Google Research 推出 Cogentic，多智能体协作发现数学证明](#item-6) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Google 通过 Fairwind 计划发布前沿模型 Gemini 4 Argon](https://t.me/zaihuapd/44165) ⭐️ 9.0/10

2026 年 9 月 30 日，Google 发布了面向软件工程、企业知识工作和网络安全的前沿模型 Gemini 4 Argon，首批通过 Fairwind 计划仅向一批受信任的网络防御者开放。该模型支持最多 100 万输出 token，起售价为每百万输入 token 2 美元、每百万输出 token 10 美元，Google 还宣称它能够自主发现、验证并修复关键软件漏洞。 此次发布延续了前沿网络安全能力通过受信任准入计划而非公开上线的方式发布的趋势，这决定了谁能使用最强的安全类 AI 以及防御方能多快用上它。如果其自主发现、验证和修复漏洞的能力属实，可能会显著改变安全团队和软件工程师排查与修复缺陷的方式；而 2 美元/10 美元的定价和 100 万 token 的输出窗口，也会给竞争对手的前沿模型带来压力。 最引人注目的数字是 100 万 token 的输出上限，这一规模相当罕见，更适合长代码生成和智能体式工作流，而非短对话回复。Google 表示初期仅面向 Fairwind 受信任防御者，待扩大测试并完善安全措施后才会向付费 API 客户和 Google AI Ultra 订阅用户开放；由于信源只是一条简短的 Telegram 帖子，其自主能力宣称和定价目前均来自 Google 官方，尚未经过独立验证。

telegram · zaihuapd · 10月2日 04:59

**背景**: Fairwind 是 Google 的一项受控准入计划，向受信任的政府机构、Google Cloud 客户和网络安全合作伙伴开放网络专用 Gemini 模型；此前的版本将 Gemini 3.8 Flash Cyber 与名为 CodeMender 的工具配合，用于发现、验证并生成漏洞修复方案，因此 Gemini 4 Argon 可视为该系列之后更通用、更前沿的一步。所谓“前沿模型”，通常指厂商能力最强、成本最高的一类模型，其定价一般按每百万 token 计费。Google AI Ultra 是 Google 最高档的消费者订阅服务，提供最高用量上限并可使用其最强模型，因此被列为 Argon 后续的分发渠道之一。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://blog.google/innovation-and-ai/models-and-research/gemini-models/3-8-flash-and-3-8-flash-cyber/">Introducing Gemini 3.8 Flash and 3.8 Flash Cyber</a></li>
<li><a href="https://siften.com/read/technology/google-s-fairwind-turns-frontier-cyber-ai-into-gated-defensive-infrastructure-1788657503816">Google’s Fairwind packages frontier cyber AI as gated... | Siften</a></li>
<li><a href="https://blog.google/products-and-platforms/products/google-one/google-ai-ultra/">Google announces AI Ultra subscription plan</a></li>

</ul>
</details>

**标签**: `#Google Gemini`, `#LLM Release`, `#AI Security`, `#Frontier Models`, `#Software Engineering`

---

<a id="item-2"></a>
## [2025 年诺贝尔生理学或医学奖授予外周免疫耐受发现者](https://t.me/zaihuapd/44174) ⭐️ 9.0/10

2025 年诺贝尔生理学或医学奖联合授予 Mary E. Brunkow、Fred Ramsdell 和 Shimon Sakaguchi，以表彰他们在外周免疫耐受方面的开创性发现。他们的研究鉴定并阐明了对调节性 T 细胞（Treg）以及 FOXP3 基因作为免疫系统“不攻击自身组织”这一能力核心调控者的作用。 该奖项表彰的是解释免疫系统如何被约束而不攻击自身的奠基性机制，这一发现支撑着当代针对自身免疫病、癌症免疫治疗和器官移植的研究。它有望加速开发既能增强 Treg 活性以治疗自身免疫病、又能抑制 Treg 以帮助免疫系统对抗肿瘤的疗法。 Treg 表达 CD4、FOXP3 和 CD25 等生物标志物，而效应 T 细胞同样带有 CD4 和 CD25，因此长期以来在技术上很难区分这两类细胞群。值得注意的是，肿瘤微环境中 Treg 数量偏高往往与预后不良相关，因为 Treg 会抑制抗肿瘤免疫——这对癌症治疗而言是一把双刃剑。

telegram · zaihuapd · 10月2日 14:15

**背景**: 免疫系统具有两层耐受机制：中枢耐受在胸腺和骨髓中清除自身反应性 T 细胞和 B 细胞；外周耐受则在淋巴细胞离开初级淋巴器官后，在淋巴结及其他组织中发挥作用。胸腺对自身反应性 T 细胞的清除效率只有约 60%–70%，因此必须依靠外周耐受机制——包括调节性 T 细胞、克隆清除、无能（anergy）以及向 Treg 转化——来防止自身免疫病的发生。FOXP3 是 Treg 发育与功能的“主控开关”，一旦其缺失，自身耐受就会崩溃并导致自身免疫病。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Peripheral_immune_tolerance">Peripheral immune tolerance</a></li>
<li><a href="https://en.wikipedia.org/wiki/Regulatory_T_cell">Regulatory T cell</a></li>
<li><a href="https://en.wikipedia.org/wiki/FOXP3_(gene)">FOXP3 (gene)</a></li>

</ul>
</details>

**标签**: `#Nobel Prize`, `#Immunology`, `#Peripheral Immune Tolerance`, `#Medicine`, `#Science News`

---

<a id="item-3"></a>
## [AI 终于攻克《Stratego》，以更低成本击败史上最强人类玩家](https://arstechnica.com/science/2026/10/ai-finally-beat-the-best-stratego-player-in-history-and-did-it-on-a-budget/) ⭐️ 8.0/10

一套新的 AI 系统成为首个击败史上最强《Stratego》人类玩家的系统，而且其训练所用对局数量比 DeepMind 的 DeepNash 少了约 34 倍。该成果发表于《Nature》论文，并配有对应的 arXiv 预印本（2511.07312）。 《Stratego》属于非完全信息博弈，这类游戏历来难以被 AI 攻克，因为传统的前瞻搜索假设玩家已知局面状态。此次以远低得多的算力击败顶尖人类，是一个堪比 AlphaGo 与 DeepStack 的里程碑，也意味着在谈判、安全、拍卖等现实不确定决策场景中可能获得更高效的方法。 作为对比，DeepMind 在 2022 年的 DeepNash 通过四个月约 55 亿局自我对弈从头学会《Stratego》，因此新系统训练对局数减少约 34 倍是其核心的效率主张。讨论中也指出一个重要的限定：DeepNash 在 2022 年宣称的“掌握”并未明显超越顶尖人类玩家，因此这次才是首个令人信服的达到或超越人类水平的成果。

hackernews · PaulHoule · 10月2日 14:11 · [社区讨论](https://news.ycombinator.com/item?id=49933740)

**背景**: 《Stratego》是一款类似国际象棋的双人棋盘战棋游戏，在 10×10 的棋盘上进行，每方拥有 40 枚按数字编号的棋子，另有炸弹（地雷）、工兵（排雷者）和间谍，目标是夺取对方的军旗。与象棋或围棋不同，玩家看不到对方棋子的身份，因此它属于非完全信息博弈：最优走法取决于你不知道的信息，经典的“我这样走、对方就会那样走”式前瞻搜索因此失效。AI 此前已在扑克这类游戏中攻克过该问题，Libratus 和 Pluribus 曾击败顶尖人类；而在《Stratego》上，DeepMind 于 2022 年推出了无模型多智能体强化学习系统 DeepNash。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Stratego">Stratego - Wikipedia</a></li>
<li><a href="https://www.axios.com/2022/12/01/ai-beats-humans-complex-games">Two new AI systems beat humans at complex games of Stratego and...</a></li>
<li><a href="https://siliconangle.com/2022/12/02/deepmind-debuts-new-ai-system-capable-playing-stratego/">DeepMind debuts new AI system capable of playing... - SiliconANGLE</a></li>

</ul>
</details>

**社区讨论**: Hacker News 的评论者主要聚焦于隐藏信息为何是关键：janalsncm 认为在非完全信息下，一步棋的好坏取决于你无从知晓的事实，因此前瞻搜索根本无法进行，而 34 倍的训练效率提升才是该方法得以奏效的核心。其他人则分享了童年玩《Stratego》的回忆，有人提到当年的对手偷偷在棋子上做记号以“揭示”隐藏信息，也有人指出 DeepNash 在 2022 年宣称的“掌握”在四年后看来其实为时过早。

**标签**: `#AI`, `#reinforcement-learning`, `#game-playing`, `#imperfect-information`, `#research-breakthrough`

---

<a id="item-4"></a>
## [Redis 之父 antirez 发布本地 LLM 推理引擎 ds4](https://dwarfstar.sh/) ⭐️ 8.0/10

Redis 的作者 Salvatore Sanfilippo（即 antirez）发布了 ds4（DwarfStar 4），这是一个用 C 语言编写的、专门面向 DeepSeek V4 Flash 模型的本地推理引擎，在 macOS 上使用 Metal 加速，在 Linux 上使用 CUDA。该仓库上线四天内 GitHub 星标数就突破 7000，之后又加入了对 Qwen 系列模型的支持。 一位知名系统程序员进入本地 LLM 领域，说明轻量、面向特定模型的推理引擎有能力与大型通用框架竞争，也为 Apple Silicon 和 CUDA 用户提供了又一个完全在自己的硬件上运行模型的高性能轻量选择。社区迅速涌现出分支、语言绑定和衍生引擎，表明本地推理生态正围绕个人开发者项目快速扩张。 与必须兼容众多模型架构的通用引擎不同，ds4 刻意做成面向特定模型：最初只针对 DeepSeek V4 Flash，随后扩展到 Qwen；它用纯 C 实现，因此可以被嵌入并绑定到其他语言。社区分支已将其封装为共享库并提供 FFI 绑定，从而催生了基于 Go 的 ds4go 等项目。

hackernews · fibo · 10月2日 18:01 · [社区讨论](https://news.ycombinator.com/item?id=49936575)

**背景**: 在本地运行大语言模型需要使用推理引擎，例如 llama.cpp、Ollama、LM Studio 或 vLLM 这类软件，它们负责加载模型权重并在本机的 GPU 或 CPU 上执行生成文本所需的计算，而无需调用云端 API。主流引擎大多是通用的，通过分支代码路径支持数十种模型架构；ds4 则反其道而行，针对一个或少数几个模型做极致优化。FFI（外部函数接口）是一种让某种语言编写的程序调用由另一种语言编译的函数的机制，ds4 的 C 内核正是借此被 Go、Python 或 Rust 复用。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.youtube.com/watch?v=7_pXlTiJ240">ds 4 : antirez's New Inference Engine — 7.1k Stars in 4 Days - YouTube</a></li>
<li><a href="https://www.linkedin.com/posts/aarontrelstad_github-aarontrelstadllm-serving-platform-activity-7456689028055179264-hL1j">LLM Inference is a Systems Problem, Not a Model Problem | LinkedIn</a></li>
<li><a href="https://bizon-tech.com/blog/best-llm-inference-engines">vLLM, Ollama, LM Studio, llama.cpp: Choosing the best LLM ...</a></li>

</ul>
</details>

**社区讨论**: 评论整体非常积极：一位维护者称他把 ds4 分支封装成共享库并提供 FFI 绑定，开发了基于 Go 的 ds4go，并随上游同步加入了 Vision 和 Qwen 支持；另一位开发者表示自己为 Intel Xe-LP 笔记本写了一个类似引擎（xenolith）。反复出现的疑问是：编写面向特定模型的推理引擎需要多少领域知识，以及主流引擎究竟是真正通用，还是只是一大堆 switch 分支。用户也报告了大量实际使用经验，有人在一台 M5 Max 128GB 机器上连续使用 Qwen 3.8 Flash 超过一周，称赞其速度和超长上下文窗口，但偶尔会出现记不住早前内容的状况。

**标签**: `#LLM inference`, `#local LLM`, `#open source`, `#Redis`, `#ds4`

---

<a id="item-5"></a>
## [arXiv 对未核查 LLM 生成内容的投稿实施一年禁投处罚](https://t.me/zaihuapd/44166) ⭐️ 8.0/10

arXiv 正式明确了针对含有未核查 LLM 生成内容稿件的处罚措施：若稿件中出现足以证明作者未检查生成结果的内容，作者将被禁止投稿一年。禁投期结束后，其后续投稿还须先被可信的同行评审 venue 接收，才能提交到 arXiv。 这是主流预印本平台首次针对 AI 生成的“灌水”内容出台明确且可执行的处罚，表明平台将要求作者对机器生成的内容负责。这直接影响把 LLM 当作写作辅助工具的研究者，也提高了整个学术出版界对科研诚信的要求。 处罚针对的是那些明显的“露馅”迹象，例如幻觉引用、LLM 遗留的元注释，以及“表格数据仅为示例、请替换为真实实验数据”这类占位文本。arXiv 的行为准则要求，作者署名即代表对论文全部内容负责，不论内容由何种方式生成。

telegram · zaihuapd · 10月2日 06:21

**背景**: arXiv 是一个免费、开放获取的预印本服务器，收录近 240 万篇学术论文，主要集中在物理学、数学和计算机科学领域，许多研究者在正式同行评审之前会先在此发布成果。大语言模型会编造看起来很像真实文献、实则不存在的参考文献，这种现象被称为“幻觉引用”。由于预印本通常未经同行评审即可发布，未核查的 LLM 输出可能迅速扩散，因此 arXiv 在推出这一处罚政策之外，还增加了首次投稿者需获得现有作者背书等措施。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/">arXiv .org e- Print archive</a></li>
<li><a href="https://www.linkedin.com/posts/frommholz_arxiv-preprint-server-clamps-down-on-ai-slop-activity-7422368432240676864-Z6el">ArXiv preprint server clamps down on AI slop | Ingo Frommholz</a></li>
<li><a href="https://www.emergentmind.com/topics/llm-induced-hallucinated-citations">LLM -Induced Hallucinated Citations</a></li>

</ul>
</details>

**标签**: `#arXiv`, `#LLM-generated content`, `#research integrity`, `#academic publishing`, `#AI policy`

---

<a id="item-6"></a>
## [Google Research 推出 Cogentic，多智能体协作发现数学证明](https://arxiv.org/abs/2609.40324v1) ⭐️ 8.0/10

Google Research 提出了 Cogentic，一套用于自动证明发现的多智能体系统，它让多个基于 Gemini 的独立证明器分别探索不同方向，并由专门的对抗式验证组件进行核查，把已确认的结果存入可持续复用的验证账本。该系统在在线学习、拍卖理论和机制设计领域的 5 个开放问题上给出了新结果，这些结果均由领域专家独立验证，并写在配套论文中。 这项工作有力地说明，基于 LLM 的多智能体系统不仅能重复证明已知定理，还能对开放数学问题给出真正新颖且经专家验证的结果，标志着 AI for Mathematics 正从刷基准转向真正参与研究。若该方法可以推广，将有望缩短理论计算机科学与经济学研究者在探索证明思路上的时间。 论文称该系统效率相当高：大多数问题只需约 100 次 Gemini 调用，较难的问题约需 1000 次调用；已验证的结果会被沉淀在持久化账本中，因此每次运行无需从零重建信任。需要注意的地方是：目前流传的消息只是简短的二手摘要，缺乏技术细节，而且新闻中引用的 arXiv 编号与该论文的实际登记条目相比似乎异常。

telegram · zaihuapd · 10月2日 12:04

**背景**: 自动定理证明传统上依赖形式化系统和专用求解器，但近期研究越来越多地用大语言模型生成证明思路与推理步骤，并常配合自动验证器逐步检查。一个反复出现的难题是 LLM 可能给出看似合理却错误的论证，因此“验证器在环”（verifier-in-the-loop）和对抗式验证成为热门研究方向。Cogentic 属于这一脉络，也延续了 Google 此前基于 Gemini 的多智能体项目（如把“生成—评估—改进”循环用于生物医学假设发现的 AI Co-Scientist）的思路。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/html/2609.40324">Cogentic : Multi - Agent Orchestration for Automated Proof Discovery</a></li>
<li><a href="https://udit.co/blog/google-ai-co-scientist-gemini-biomedical-discovery">Google 's AI Co-Scientist uses multi - agent Gemini to acceler</a></li>
<li><a href="https://arxiv.org/abs/2507.23726">[2507.23726] Seed-Prover: Deep and Broad Reasoning for Automated ...</a></li>

</ul>
</details>

**标签**: `#multi-agent systems`, `#automated theorem proving`, `#LLM agents`, `#AI for mathematics`, `#Google Research`

---