---
layout: default
title: "Horizon Summary: 2026-07-12 (EN)"
date: 2026-07-12
lang: en
---

> From 26 items, 8 important content pieces were selected

---

1. [vLLM v0.25.0 Makes Model Runner V2 Default, Removes PagedAttention](#item-1) ⭐️ 9.0/10
2. [OpenAI Releases GPT-5.6 Series with Sol, Terra, Luna Models](#item-2) ⭐️ 9.0/10
3. [Circular Financing in the GPU Boom: Nvidia, CoreWeave, Nebius](#item-3) ⭐️ 8.0/10
4. [ClickHouse scales PgBouncer throughput 4x with peering](#item-4) ⭐️ 8.0/10
5. [Prefer strict tables in SQLite](#item-5) ⭐️ 8.0/10
6. [VultronRetriever Models Top MTEB with Efficiency Gains](#item-6) ⭐️ 8.0/10
7. [Six U-Boot flaws enable pre-boot code execution](#item-7) ⭐️ 8.0/10
8. [Shanghai aims for high-quality brain control by 2027](#item-8) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [vLLM v0.25.0 Makes Model Runner V2 Default, Removes PagedAttention](https://github.com/vllm-project/vllm/releases/tag/v0.25.0) ⭐️ 9.0/10

vLLM v0.25.0 sets Model Runner V2 as the default execution path for all dense models and removes the legacy PagedAttention implementation, while adding support for new models like LLaVA-OneVision-2 and introducing a Streaming Parser Engine. This release represents a major architectural overhaul for vLLM, improving inference performance and modularity, and sets the stage for future optimizations in LLM serving. Model Runner V2 (MRv2) replaces the Python-based model runner with GPU-native Triton kernels, achieving up to 56% higher throughput. The removal of PagedAttention means all attention now goes through the V1/MRv2 backends.

github · khluu · Jul 11, 20:06

**Background**: vLLM is a high-performance inference engine for large language models, originally introduced with PagedAttention for efficient memory management. PagedAttention, inspired by OS virtual memory paging, reduces KV cache waste. Model Runner V2 is a redesigned execution core that separates CPU scheduling from GPU execution for better efficiency.

<details><summary>References</summary>
<ul>
<li><a href="https://vllm.ai/blog/2026-03-24-mrv2">Model Runner V2: A Modular and Faster Core for vLLM | vLLM Blog</a></li>
<li><a href="https://docs.vllm.ai/en/v0.22.1/design/model_runner_v2/">Model Runner V2 Design Document - vLLM</a></li>
<li><a href="https://en.wikipedia.org/wiki/PagedAttention">PagedAttention - Wikipedia</a></li>

</ul>
</details>

**Tags**: `#vLLM`, `#LLM inference`, `#model optimization`, `#release notes`, `#GPU`

---

<a id="item-2"></a>
## [OpenAI Releases GPT-5.6 Series with Sol, Terra, Luna Models](https://t.me/zaihuapd/42497) ⭐️ 9.0/10

OpenAI officially released the GPT-5.6 series, comprising three models: Sol (flagship with highest capabilities), Terra (balanced performance and cost), and Luna (high-concurrency, low-cost). The series features improvements in code, knowledge work, design, research, and cybersecurity, and introduces max/ultra reasoning, multi-agent collaboration, and programmatic tool calling. This release provides a tiered pricing and capability structure, allowing users to choose the optimal model for their budget and task complexity. The improved performance-cost ratio and new reasoning modes enable more efficient complex task execution, benefiting developers, enterprises, and AI researchers. Pricing per 1M tokens: Sol $5/$30 (input/output), Terra $2.50/$15, Luna $1/$6. Max reasoning allocates more compute per invocation while Ultra uses subagents for parallelism. Programmatic tool calling allows dynamic code generation for tool use. By default, GPT-5.6 will point to Sol.

telegram · zaihuapd · Jul 11, 13:34

**Background**: OpenAI's GPT series has evolved from single models to a family of variants tailored for different use cases. Reasoning modes like max and ultra increase answer quality for complex tasks by allowing more inference time or parallel sub-agent execution. Programmatic tool calling enhances the model's ability to interact with external tools through code generation, improving accuracy and reducing token usage.

<details><summary>References</summary>
<ul>
<li><a href="https://openai.com/index/previewing-gpt-5-6-sol/">Previewing GPT-5.6 Sol: a next-generation model | OpenAI</a></li>
<li><a href="https://www.mindstudio.ai/blog/what-is-gpt-5-6-soul-terra-luna-explained">What Is GPT-5.6? OpenAI's Soul, Terra, and Luna Model Tiers Explained | MindStudio</a></li>
<li><a href="https://www.datacamp.com/blog/gpt-5-6-sol-luna-terra">GPT-5.6 Sol, Terra, and Luna: OpenAI's Next-Gen Model Family | DataCamp</a></li>

</ul>
</details>

**Tags**: `#OpenAI`, `#GPT-5.6`, `#AI`, `#large language models`, `#machine learning`

---

<a id="item-3"></a>
## [Circular Financing in the GPU Boom: Nvidia, CoreWeave, Nebius](https://io-fund.com/ai-stocks/nvidia-coreweave-nebius-circular-financing-gpu-boom) ⭐️ 8.0/10

An analysis by io-fund.com examines the investments by Nvidia in GPU cloud providers CoreWeave and Nebius, arguing that the so-called circular financing narrative is overstated, while raising questions about the economic viability of massive GPU builds. This matters because it challenges a popular criticism of the AI infrastructure boom, and redirects attention to whether these massive GPU deployments can generate sufficient returns, which is critical for investors and the broader AI ecosystem. Nvidia's $2 billion investment in CoreWeave represented only about 5.7% of CoreWeave's single-year CapEx for 2026, suggesting the circularity is limited. The analysis also notes that Nvidia invests in neoclouds as a hedge against hyperscalers gaining too much power.

hackernews · adletbalzhanov · Jul 11, 17:21 · [Discussion](https://news.ycombinator.com/item?id=48873836)

**Background**: CoreWeave and Nebius are GPU cloud providers that offer access to Nvidia's high-performance GPUs like H100, B200, and Blackwell for AI workloads. Circular financing refers to a scenario where Nvidia invests money into companies that then spend that money back on Nvidia's GPUs, potentially inflating demand artificially.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/CoreWeave">CoreWeave - Wikipedia</a></li>
<li><a href="https://nebius.com/about">About Nebius</a></li>

</ul>
</details>

**Discussion**: Commenters largely agree that the circular financing narrative is overblown, with one noting that Nvidia's investment is only a small fraction of CoreWeave's CapEx. Others shift focus to whether these builds can be economically profitable, suggesting metrics like ROI per token and enterprise token budgets.

**Tags**: `#AI infrastructure`, `#GPU cloud`, `#financing`, `#Nvidia`, `#CoreWeave`

---

<a id="item-4"></a>
## [ClickHouse scales PgBouncer throughput 4x with peering](https://clickhouse.com/blog/pgbouncer-clickhouse-managed-postgres) ⭐️ 8.0/10

ClickHouse detailed how they scaled PgBouncer throughput by 4x using a peering mechanism that forwards query cancellation requests to the correct process, enabling multi-process deployment without breaking cancellation behavior. This improvement allows PgBouncer to handle higher concurrency and throughput, benefiting PostgreSQL users who rely on connection pooling. It also addresses a longstanding limitation of PgBouncer's single-process architecture, making it more scalable for modern cloud environments. The peering mechanism ensures that cancellation requests reaching the wrong process are forwarded to the session owner. This was a key challenge because PostgreSQL cancellation requests are session-specific, and without peering they would fail if they landed on a different process.

hackernews · saisrirampur · Jul 11, 15:28 · [Discussion](https://news.ycombinator.com/item?id=48872874)

**Background**: PgBouncer is a widely used lightweight connection pooler for PostgreSQL that helps manage database connections efficiently. Traditionally, PgBouncer runs as a single process, limiting its scalability. The peering mechanism allows multiple PgBouncer processes to share state and handle query cancellations correctly, enabling horizontal scaling.

<details><summary>References</summary>
<ul>
<li><a href="https://www.pgbouncer.org/">PgBouncer - lightweight connection pooler for PostgreSQL</a></li>
<li><a href="https://www.tipranks.com/news/private-companies/architecture-enhancements-highlight-performance-focus-in-clickhouse-managed-postgres">Architecture Enhancements Highlight Performance Focus in ClickHouse ...</a></li>

</ul>
</details>

**Discussion**: Community members suggested alternative tools like Odyssey and pgdog. Some asked about Kubernetes compatibility and whether peering works across pods. Others shared their experiences running PgBouncer on Kubernetes and appreciated the approach.

**Tags**: `#PostgreSQL`, `#PgBouncer`, `#connection pooling`, `#performance scaling`, `#ClickHouse`

---

<a id="item-5"></a>
## [Prefer strict tables in SQLite](https://evanhahn.com/prefer-strict-tables-in-sqlite/) ⭐️ 8.0/10

The article advocates for using SQLite's strict tables to enforce type constraints on columns, improving data integrity. This matters because strict tables prevent accidental type mismatches that can cause silent data corruption, especially in multi-application or long-lived databases. Strict tables were introduced in SQLite version 3.37.0 (2021-11-27) and cannot be created by altering an existing table; you must copy data to a new strict table. Tools like simonw's sqlite-utils can automate this conversion.

hackernews · ingve · Jul 11, 17:33 · [Discussion](https://news.ycombinator.com/item?id=48873940)

**Background**: SQLite by default uses dynamic typing, where column types are hints rather than enforced rules. Strict tables, enabled per table with the STRICT keyword, enforce that inserted values match the declared type, rejecting mismatches at insert time.

<details><summary>References</summary>
<ul>
<li><a href="https://www.sqlite.org/stricttables.html">STRICT Tables</a></li>
<li><a href="https://antonz.org/sqlite-strict-tables/">STRICT tables in SQLite</a></li>
<li><a href="https://www.sqlitetutorial.net/sqlite-strict-tables/">SQLite Strict Tables</a></li>

</ul>
</details>

**Discussion**: Community comments show mixed opinions: simonw built a tool (sqlite-utils) to convert non-strict tables to strict; dfabulich links to SQLite's 'flextypegood' rationale against making strict the default; others argue strict should be default for better type safety.

**Tags**: `#SQLite`, `#databases`, `#type safety`, `#best practices`, `#data integrity`

---

<a id="item-6"></a>
## [VultronRetriever Models Top MTEB with Efficiency Gains](https://www.reddit.com/r/MachineLearning/comments/1utmxq8/vultronretriever_family_of_models_released_on/) ⭐️ 8.0/10

The VultronRetriever family of embedding models, including Prime-8B, Core-4.5B, and Flash-0.8B, was released on HuggingFace and claims the top positions on the MTEB leaderboard across size classes. These models demonstrate significant efficiency improvements—such as 12x higher throughput and 16x smaller index storage for Prime-8B—which could enable high-quality retrieval on edge devices like smartphones. All models use the Hydra architecture for late interaction retrieval, are trained on datasets with zero cross-dataset duplication and zero evaluation contamination, and can run fully offline on an iPhone.

reddit · r/MachineLearning · /u/madkimchi · Jul 11, 15:22

**Background**: MTEB (Massive Text Embedding Benchmark) is a widely used leaderboard for evaluating embedding models across retrieval, clustering, and classification tasks. Late interaction retrieval, as used in ColBERT, allows fine-grained query-document matching by comparing token-level embeddings after separate encoding, offering a balance between efficiency and precision.

<details><summary>References</summary>
<ul>
<li><a href="https://huggingface.co/spaces/mteb/leaderboard">MTEB Leaderboard - a Hugging Face Space by mteb</a></li>
<li><a href="https://leaderboard.mteb.org/models">Models · MTEB Leaderboard</a></li>
<li><a href="https://arxiv.org/html/2603.28554v2">Hydra : Unifying Document Retrieval and Generation in a Single...</a></li>

</ul>
</details>

**Tags**: `#embedding models`, `#retrieval`, `#MTEB`, `#ML models`, `#efficiency`

---

<a id="item-7"></a>
## [Six U-Boot flaws enable pre-boot code execution](https://www.bleepingcomputer.com/news/security/new-u-boot-flaws-could-enable-stealthy-firmware-attacks/) ⭐️ 8.0/10

Six vulnerabilities have been discovered in U-Boot's FIT image signature verification code, two of which can lead to arbitrary code execution and four cause denial of service, affecting all versions since U-Boot 2013.07. These flaws allow attackers to execute malicious code before the operating system and security software start, potentially disabling firmware security, modifying boot flow, or installing persistent firmware malware, affecting countless embedded devices. The vulnerabilities are in the FIT signature verification phase, and for systems like BMCs that support remote firmware updates, exploitation can be done without physical access. Patches have been accepted by U-Boot maintainers but require downstream vendor integration.

telegram · zaihuapd · Jul 11, 08:32

**Background**: U-Boot is a widely used open-source bootloader for embedded systems, supporting multiple architectures. FIT (Flattened Image Tree) is a format for bundling kernel, device tree, and other images with signatures, and U-Boot verifies those signatures during boot. The vulnerabilities bypass this verification, enabling malicious code execution before the OS loads.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Das_U-Boot">Das U - Boot - Wikipedia</a></li>
<li><a href="https://u-boot.org/">Das U - Boot : The Universal Boot Loader</a></li>
<li><a href="https://www.sentinelone.com/vulnerability-database/cve-2021-27138/">CVE-2021-27138: Denx U-Boot FIT Unit Address Vulnerability</a></li>

</ul>
</details>

**Tags**: `#security`, `#bootloader`, `#vulnerabilities`, `#firmware`, `#U-Boot`

---

<a id="item-8"></a>
## [Shanghai aims for high-quality brain control by 2027](https://t.me/zaihuapd/42501) ⭐️ 8.0/10

The Shanghai Municipal Science and Technology Commission issued the Shanghai Brain-Computer Interface Future Industry Cultivation Action Plan (2025-2030), setting targets for high-quality brain control, clinical application of semi-invasive BCI products, and breakthroughs in invasive BCI research by 2027. This policy signals China's strategic push to lead in BCI technology, potentially accelerating clinical adoption and stimulating investment. It could benefit patients with neurological disorders and position Shanghai as a global BCI hub. The plan targets 5 or more invasive and semi-invasive BCI products to complete medical device type testing and clinical trials, aiming to restore partial language and motor functions for patients with aphasia or paralysis.

telegram · zaihuapd · Jul 11, 15:49

**Background**: Brain-computer interfaces (BCIs) enable direct communication between the brain and external devices. They are generally classified as invasive (surgically implanted), semi-invasive (attached to the dura mater), or non-invasive (external sensors). Shanghai's plan focuses on the first two types, which offer higher signal fidelity but require medical procedures.

<details><summary>References</summary>
<ul>
<li><a href="https://manasikkm.medium.com/it-doesnt-take-a-brainiac-to-learn-about-brain-computer-interfaces-24be96645df8">It Doesn’t Take A Brainiac to Learn About Brain - Computer Interfaces</a></li>
<li><a href="https://www.linkedin.com/pulse/minds-interface-bridging-thought-technology-bci-neuranet-ai-otbae">The Mind's Interface : Bridging Thought and Technology with BCI</a></li>
<li><a href="https://www.business-standard.com/technology/tech-news/what-makes-brain-implants-more-than-just-a-sci-fi-fantasy-as-ai-era-unfolds-126051100098_1.html">What makes brain implants more than just a sci-fi... - Business Standard</a></li>

</ul>
</details>

**Tags**: `#brain-computer interface`, `#neurotechnology`, `#policy`, `#China`, `#medical devices`

---