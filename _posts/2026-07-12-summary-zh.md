---
layout: default
title: "Horizon Summary: 2026-07-12 (ZH)"
date: 2026-07-12
lang: zh
---

> 从 26 条内容中筛选出 8 条重要资讯。

---

1. [vLLM v0.25.0 将 Model Runner V2 设为默认并移除 PagedAttention](#item-1) ⭐️ 9.0/10
2. [OpenAI 发布 GPT-5.6 系列：Sol、Terra、Luna 三款模型](#item-2) ⭐️ 9.0/10
3. [GPU 热潮中的循环融资：英伟达、CoreWeave 与 Nebius](#item-3) ⭐️ 8.0/10
4. [ClickHouse 通过 Peering 机制将 PgBouncer 吞吐量提升 4 倍](#item-4) ⭐️ 8.0/10
5. [提倡在 SQLite 中使用严格表](#item-5) ⭐️ 8.0/10
6. [VultronRetriever 模型登顶 MTEB 排行榜并大幅提升效率](#item-6) ⭐️ 8.0/10
7. [U-Boot 六个漏洞可导致启动前代码执行](#item-7) ⭐️ 8.0/10
8. [上海计划 2027 年前实现高质量脑控](#item-8) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [vLLM v0.25.0 将 Model Runner V2 设为默认并移除 PagedAttention](https://github.com/vllm-project/vllm/releases/tag/v0.25.0) ⭐️ 9.0/10

vLLM v0.25.0 将 Model Runner V2 作为所有稠密模型的默认执行路径，移除了旧版 PagedAttention 实现，并新增了对 LLaVA-OneVision-2 等模型的支持以及 Streaming Parser Engine。 此次发布代表了 vLLM 的重大架构改革，提升了推理性能和模块化程度，为未来 LLM 服务的优化奠定了基础。 Model Runner V2 (MRv2) 用基于 GPU 的 Triton 内核替换了基于 Python 的模型执行器，吞吐量最高提升 56%。PagedAttention 的移除意味着所有注意力现在都通过 V1/MRv2 后端处理。

github · khluu · 7月11日 20:06

**背景**: vLLM 是一个高性能的大语言模型推理引擎，最初引入 PagedAttention 以实现高效内存管理。PagedAttention 受操作系统虚拟内存分页启发，减少了 KV 缓存浪费。Model Runner V2 是一个重新设计的执行核心，将 CPU 调度与 GPU 执行分离以提高效率。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://vllm.ai/blog/2026-03-24-mrv2">Model Runner V2: A Modular and Faster Core for vLLM | vLLM Blog</a></li>
<li><a href="https://docs.vllm.ai/en/v0.22.1/design/model_runner_v2/">Model Runner V2 Design Document - vLLM</a></li>
<li><a href="https://en.wikipedia.org/wiki/PagedAttention">PagedAttention - Wikipedia</a></li>

</ul>
</details>

**标签**: `#vLLM`, `#LLM inference`, `#model optimization`, `#release notes`, `#GPU`

---

<a id="item-2"></a>
## [OpenAI 发布 GPT-5.6 系列：Sol、Terra、Luna 三款模型](https://t.me/zaihuapd/42497) ⭐️ 9.0/10

OpenAI 正式发布 GPT-5.6 系列，包含三款模型：Sol（旗舰级，能力最强）、Terra（平衡性能与成本）和 Luna（面向高并发低成本场景）。该系列在代码、知识工作、设计、科研和网络安全方面有所提升，并引入了 max/ultra 推理、多智能体协作和 Programmatic Tool Calling。 此次发布提供了分层定价和能力结构，使用户能够根据预算和任务复杂度选择最优模型。改进的性能成本比以及新的推理模式使得复杂任务执行更高效，使开发者、企业和 AI 研究者受益。 每 1M token 定价：Sol 输入 $5 / 输出 $30，Terra 输入 $2.50 / 输出 $15，Luna 输入 $1 / 输出 $6。Max 推理为单次调用分配更多计算，Ultra 使用子智能体进行并行处理。Programmatic Tool Calling 支持通过动态代码生成来调用工具。默认情况下，GPT-5.6 将指向 Sol。

telegram · zaihuapd · 7月11日 13:34

**背景**: OpenAI 的 GPT 系列已从单一模型演变为针对不同用例量身定制的模型家族。max 和 ultra 等推理模式通过允许更多的推理时间或并行子智能体执行，提高了复杂任务的答案质量。Programmatic Tool Calling 通过代码生成增强模型与外部工具交互的能力，从而提高准确性并减少 token 使用量。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openai.com/index/previewing-gpt-5-6-sol/">Previewing GPT-5.6 Sol: a next-generation model | OpenAI</a></li>
<li><a href="https://www.mindstudio.ai/blog/what-is-gpt-5-6-soul-terra-luna-explained">What Is GPT-5.6? OpenAI's Soul, Terra, and Luna Model Tiers Explained | MindStudio</a></li>
<li><a href="https://www.datacamp.com/blog/gpt-5-6-sol-luna-terra">GPT-5.6 Sol, Terra, and Luna: OpenAI's Next-Gen Model Family | DataCamp</a></li>

</ul>
</details>

**标签**: `#OpenAI`, `#GPT-5.6`, `#AI`, `#large language models`, `#machine learning`

---

<a id="item-3"></a>
## [GPU 热潮中的循环融资：英伟达、CoreWeave 与 Nebius](https://io-fund.com/ai-stocks/nvidia-coreweave-nebius-circular-financing-gpu-boom) ⭐️ 8.0/10

io-fund.com 发布的分析报告审视了英伟达对 GPU 云服务商 CoreWeave 和 Nebius 的投资，认为所谓的循环融资说法被夸大了，同时质疑大规模 GPU 建设的经济可行性。 这之所以重要，是因为它挑战了对 AI 基础设施热潮的一种普遍批评，并将注意力重新引向这些大规模 GPU 部署能否产生足够回报的问题，这对投资者和更广泛的 AI 生态系统至关重要。 英伟达对 CoreWeave 的 20 亿美元投资仅占 CoreWeave 2026 年单年资本支出的约 5.7%，表明循环性有限。分析还指出，英伟达投资新兴云服务商是对冲超大规模云厂商权力过大的策略。

hackernews · adletbalzhanov · 7月11日 17:21 · [社区讨论](https://news.ycombinator.com/item?id=48873836)

**背景**: CoreWeave 和 Nebius 是 GPU 云服务商，为 AI 工作负载提供英伟达高性能 GPU（如 H100、B200、Blackwell）的访问。循环融资指的是一种场景：英伟达将资金投资于公司，这些公司又将资金用于购买英伟达的 GPU，从而可能人为地夸大需求。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/CoreWeave">CoreWeave - Wikipedia</a></li>
<li><a href="https://nebius.com/about">About Nebius</a></li>

</ul>
</details>

**社区讨论**: 评论者基本同意循环融资的说法被夸大，有人指出英伟达的投资仅占 CoreWeave 资本支出的一小部分。其他人则将焦点转向这些建设是否能实现经济盈利，建议关注每 token ROI 和企业 token 预算等指标。

**标签**: `#AI infrastructure`, `#GPU cloud`, `#financing`, `#Nvidia`, `#CoreWeave`

---

<a id="item-4"></a>
## [ClickHouse 通过 Peering 机制将 PgBouncer 吞吐量提升 4 倍](https://clickhouse.com/blog/pgbouncer-clickhouse-managed-postgres) ⭐️ 8.0/10

ClickHouse 详细介绍了如何通过 peering 机制将 PgBouncer 的吞吐量提升 4 倍，该机制将查询取消请求转发到正确的进程，从而在不破坏取消行为的情况下实现多进程部署。 这一改进使 PgBouncer 能够处理更高的并发和吞吐量，惠及依赖连接池的 PostgreSQL 用户。它还解决了 PgBouncer 单进程架构的长期限制，使其更适用于现代云环境。 Peering 机制确保到达错误进程的取消请求被转发给会话所有者。这是一个关键挑战，因为 PostgreSQL 的取消请求是特定于会话的，如果没有 peering，它们到达不同进程时会失败。

hackernews · saisrirampur · 7月11日 15:28 · [社区讨论](https://news.ycombinator.com/item?id=48872874)

**背景**: PgBouncer 是一个广泛使用的 PostgreSQL 轻量级连接池，有助于高效管理数据库连接。传统上，PgBouncer 作为单进程运行，限制了其可扩展性。Peering 机制允许多个 PgBouncer 进程共享状态并正确处理查询取消，从而实现水平扩展。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.pgbouncer.org/">PgBouncer - lightweight connection pooler for PostgreSQL</a></li>
<li><a href="https://www.tipranks.com/news/private-companies/architecture-enhancements-highlight-performance-focus-in-clickhouse-managed-postgres">Architecture Enhancements Highlight Performance Focus in ClickHouse ...</a></li>

</ul>
</details>

**社区讨论**: 社区成员建议了替代工具如 Odyssey 和 pgdog。一些人询问了 Kubernetes 兼容性以及 peering 是否在跨 Pod 时生效。其他人分享了他们在 Kubernetes 上运行 PgBouncer 的经验，并对这种方法表示赞赏。

**标签**: `#PostgreSQL`, `#PgBouncer`, `#connection pooling`, `#performance scaling`, `#ClickHouse`

---

<a id="item-5"></a>
## [提倡在 SQLite 中使用严格表](https://evanhahn.com/prefer-strict-tables-in-sqlite/) ⭐️ 8.0/10

文章提倡使用 SQLite 的严格表来对列实施类型约束，从而提高数据完整性。 这很重要，因为严格表可以防止意外的类型不匹配，从而避免静默数据损坏，尤其在多应用或长期运行的数据库中。 严格表是在 SQLite 3.37.0 版本（2021-11-27）中引入的，不能通过修改现有表来创建；必须将数据复制到新的严格表中。诸如 simonw 的 sqlite-utils 等工具可以自动完成这种转换。

hackernews · ingve · 7月11日 17:33 · [社区讨论](https://news.ycombinator.com/item?id=48873940)

**背景**: SQLite 默认使用动态类型，列类型只是提示而非强制规则。严格表通过在每个表后加上 STRICT 关键字启用，强制插入的值与声明的类型匹配，并在插入时拒绝不匹配的数据。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.sqlite.org/stricttables.html">STRICT Tables</a></li>
<li><a href="https://antonz.org/sqlite-strict-tables/">STRICT tables in SQLite</a></li>
<li><a href="https://www.sqlitetutorial.net/sqlite-strict-tables/">SQLite Strict Tables</a></li>

</ul>
</details>

**社区讨论**: 社区评论观点不一：simonw 构建了一个工具（sqlite-utils）将非严格表转换为严格表；dfabulich 引用了 SQLite 关于反对将严格设为默认的“flextypegood”理由；其他人则认为严格应成为默认以提升类型安全性。

**标签**: `#SQLite`, `#databases`, `#type safety`, `#best practices`, `#data integrity`

---

<a id="item-6"></a>
## [VultronRetriever 模型登顶 MTEB 排行榜并大幅提升效率](https://www.reddit.com/r/MachineLearning/comments/1utmxq8/vultronretriever_family_of_models_released_on/) ⭐️ 8.0/10

VultronRetriever 系列嵌入模型（包括 Prime-8B、Core-4.5B 和 Flash-0.8B）已在 HuggingFace 上发布，并宣称在不同规模类别中均占据 MTEB 排行榜首位。 这些模型展现了显著的效率提升——例如 Prime-8B 的吞吐量提高 12 倍，索引存储缩小 16 倍——这可以在智能手机等边缘设备上实现高质量的检索。 所有模型均采用 Hydra 架构实现后期交互检索，训练数据集无跨数据集重复和无评估污染，并且可以在 iPhone 上完全离线运行。

reddit · r/MachineLearning · /u/madkimchi · 7月11日 15:22

**背景**: MTEB（大规模文本嵌入基准）是一个广泛使用的排行榜，用于评估嵌入模型在检索、聚类和分类任务上的表现。后期交互检索（如 ColBERT 中使用）通过分别编码后比较 token 级别的嵌入，实现细粒度的查询-文档匹配，在效率和精度之间取得平衡。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/spaces/mteb/leaderboard">MTEB Leaderboard - a Hugging Face Space by mteb</a></li>
<li><a href="https://leaderboard.mteb.org/models">Models · MTEB Leaderboard</a></li>
<li><a href="https://arxiv.org/html/2603.28554v2">Hydra : Unifying Document Retrieval and Generation in a Single...</a></li>

</ul>
</details>

**标签**: `#embedding models`, `#retrieval`, `#MTEB`, `#ML models`, `#efficiency`

---

<a id="item-7"></a>
## [U-Boot 六个漏洞可导致启动前代码执行](https://www.bleepingcomputer.com/news/security/new-u-boot-flaws-could-enable-stealthy-firmware-attacks/) ⭐️ 8.0/10

U-Boot 的 FIT 镜像签名验证代码中被发现存在 6 个漏洞，其中两个可导致任意代码执行，四个可造成拒绝服务，影响自 U-Boot 2013.07 以来的所有版本。 这些漏洞允许攻击者在操作系统和安全软件启动前执行恶意代码，可能禁用固件安全功能、修改启动流程或植入持久性固件恶意软件，影响大量嵌入式设备。 漏洞位于 FIT 签名验证阶段，对于支持远程固件更新的 BMC 等系统，无需物理接触即可利用。补丁已被 U-Boot 维护者接受，但需要下游厂商集成。

telegram · zaihuapd · 7月11日 08:32

**背景**: U-Boot 是一个广泛使用的嵌入式系统开源引导程序，支持多种架构。FIT（Flattened Image Tree）是一种将内核、设备树和其他镜像与签名打包的格式，U-Boot 在启动时验证这些签名。这些漏洞绕过了此验证，使得恶意代码在操作系统加载前得以执行。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Das_U-Boot">Das U - Boot - Wikipedia</a></li>
<li><a href="https://u-boot.org/">Das U - Boot : The Universal Boot Loader</a></li>
<li><a href="https://www.sentinelone.com/vulnerability-database/cve-2021-27138/">CVE-2021-27138: Denx U-Boot FIT Unit Address Vulnerability</a></li>

</ul>
</details>

**标签**: `#security`, `#bootloader`, `#vulnerabilities`, `#firmware`, `#U-Boot`

---

<a id="item-8"></a>
## [上海计划 2027 年前实现高质量脑控](https://t.me/zaihuapd/42501) ⭐️ 8.0/10

上海市科学技术委员会印发了《上海市脑机接口未来产业培育行动方案（2025-2030 年）》，设定目标到 2027 年实现高质量脑控、半侵入式脑机接口产品率先临床应用、侵入式脑机接口研发取得突破。 这项政策表明中国在脑机接口技术领域的战略推进，可能加速临床应用并刺激投资。它有望惠及神经系统疾病患者，并将上海定位为全球脑机接口中心。 该方案计划推动 5 款以上侵入式、半侵入式脑机接口产品完成医疗器械型式检验和临床试验，旨在帮助失语、瘫痪等患者恢复部分语言和运动功能。

telegram · zaihuapd · 7月11日 15:49

**背景**: 脑机接口（BCI）使大脑与外部设备直接通信，通常分为侵入式（手术植入）、半侵入式（附着在硬脑膜上）和非侵入式（外部传感器）。上海方案聚焦前两类，它们提供更高信号保真度但需医疗手术。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://manasikkm.medium.com/it-doesnt-take-a-brainiac-to-learn-about-brain-computer-interfaces-24be96645df8">It Doesn’t Take A Brainiac to Learn About Brain - Computer Interfaces</a></li>
<li><a href="https://www.linkedin.com/pulse/minds-interface-bridging-thought-technology-bci-neuranet-ai-otbae">The Mind's Interface : Bridging Thought and Technology with BCI</a></li>
<li><a href="https://www.business-standard.com/technology/tech-news/what-makes-brain-implants-more-than-just-a-sci-fi-fantasy-as-ai-era-unfolds-126051100098_1.html">What makes brain implants more than just a sci-fi... - Business Standard</a></li>

</ul>
</details>

**标签**: `#brain-computer interface`, `#neurotechnology`, `#policy`, `#China`, `#medical devices`

---