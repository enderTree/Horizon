---
layout: default
title: "Horizon Summary: 2026-07-18 (EN)"
date: 2026-07-18
lang: en
---

> From 36 items, 8 important content pieces were selected

---

1. [Meta in Talks to Lease AI Compute to Anthropic for $100B](#item-1) ⭐️ 9.0/10
2. [Moonshot AI Releases Open-Source 2.8T Parameter Model Kimi K3](#item-2) ⭐️ 9.0/10
3. [First Atmosphere Found on Earth-Like Planet in Habitable Zone](#item-3) ⭐️ 8.0/10
4. [Practical SQLite Tips: .expert Index Analysis and .dump Backup with zstd](#item-4) ⭐️ 8.0/10
5. [Open Source AI Models Surge in Usage and Debate](#item-5) ⭐️ 8.0/10
6. [Three Non-Solution Responses to Problems](#item-6) ⭐️ 8.0/10
7. [Huawei Unveils Ascend 950 SuperNode with 6.7x Performance Claim](#item-7) ⭐️ 8.0/10
8. [SpaceX in talks with Pentagon for AI computing power deal worth billions](#item-8) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Meta in Talks to Lease AI Compute to Anthropic for $100B](https://www.nytimes.com/2026/07/17/technology/meta-anthropic-ai-computing-power.html) ⭐️ 9.0/10

Meta is in early talks to lease AI computing power to Anthropic, a deal potentially worth $100 billion over two years. This deal underscores the extreme scarcity of AI compute infrastructure and could reshape how large tech firms monetize their data center investments. Anthropic proposed the deal in June 2026, Meta is evaluating, and the terms include monthly payments and early exit options for both parties.

telegram · zaihuapd · Jul 18, 01:14

**Background**: AI compute refers to the massive processing power needed to train and run large language models. Companies like Meta have invested heavily in data centers; leasing excess capacity allows them to generate revenue and justify spending.

**Tags**: `#AI infrastructure`, `#Meta`, `#Anthropic`, `#AI compute`, `#cloud computing`

---

<a id="item-2"></a>
## [Moonshot AI Releases Open-Source 2.8T Parameter Model Kimi K3](https://t.me/zaihuapd/42637) ⭐️ 9.0/10

Moonshot AI has released Kimi K3, the world's first open-source 2.8 trillion parameter model, achieving the top score in the Frontend Code Arena benchmark and surpassing previous models. It introduces the novel Kimi Delta Attention and Attention Residuals architectures. This release represents a significant leap in open-source AI, demonstrating that a 2.8T model can be openly available and outperform competitors in specialized coding tasks, potentially accelerating AI-assisted frontend development. Kimi K3 features a 1 million token context window, native vision capabilities, and was built using the Kimi Delta Attention (KDA) and Attention Residuals (AttnRes) architectures. In the Frontend Code Arena, it scored 1679, rising from 18th place with the previous Kimi k2.6 model.

telegram · zaihuapd · Jul 18, 02:29

**Background**: Kimi Delta Attention is an efficient linear attention mechanism that reduces memory usage for long contexts, building on Gated DeltaNet. Attention Residuals are a drop-in replacement for standard residual connections, allowing each layer to selectively aggregate previous layers. The Frontend Code Arena evaluates models on agentic frontend coding tasks such as HTML and React application development.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Kimi_(chatbot)">Kimi (chatbot) - Wikipedia</a></li>
<li><a href="https://arxiv.org/abs/2510.26692">[2510.26692] Kimi Linear: An Expressive, Efficient Attention Architecture</a></li>
<li><a href="https://x.com/arena/status/2056803664606679059">Arena.ai on X: "Code Arena: Frontend evaluates models on agentic frontend coding tasks from real users building apps and websites (HTML and React). Agents are an entirely different contest. More from Arena soon. Filter and dive into all the Code Arena: Frontend leaderboard details at:" / X</a></li>

</ul>
</details>

**Tags**: `#AI`, `#open-source`, `#large language model`, `#Moonshot AI`, `#coding benchmark`

---

<a id="item-3"></a>
## [First Atmosphere Found on Earth-Like Planet in Habitable Zone](https://www.bbc.com/news/articles/cy4kdd1e0ejo) ⭐️ 8.0/10

Astronomers have detected an atmosphere on LHS 1140b, a rocky exoplanet in the habitable zone of a red dwarf star, 48 light-years away. This marks the first confirmed atmosphere on an Earth-like planet in a potentially habitable region. This discovery demonstrates that rocky planets around red dwarfs can retain atmospheres despite intense stellar activity, opening new possibilities for finding habitable worlds. It also validates JWST's capability to characterize temperate exoplanet atmospheres and brings us closer to searching for biosignatures. LHS 1140b is larger and cooler than Earth, with a helium-rich atmosphere detected via JWST emission spectroscopy during its secondary eclipse. The planet's atmosphere rules out a mini-Neptune scenario, confirming its rocky nature.

hackernews · neversaydie · Jul 17, 14:06 · [Discussion](https://news.ycombinator.com/item?id=48947560)

**Background**: Red dwarfs are the most common stars in the Milky Way, but their habitable zones are very close, exposing planets to intense stellar flares and stripping. Detecting atmospheres on such planets is challenging; JWST's infrared sensitivity makes it possible. Previous exoplanet atmosphere detections were mostly on hot Jupiters, not rocky worlds.

<details><summary>References</summary>
<ul>
<li><a href="https://www.nytimes.com/2026/07/16/science/astronomy-exoplanet-atmosphere.html">Astronomers Find an Atmosphere on a Nearby Earthlike Planet - The New York Times</a></li>
<li><a href="https://en.wikipedia.org/wiki/Red_dwarf">Red dwarf - Wikipedia</a></li>

</ul>
</details>

**Discussion**: Comments show mixed reactions: some skepticism about whether a rocky planet so close to a red dwarf can hold an atmosphere, but the JWST data rules out a mini-Neptune. Others discuss future telescopes like a solar lens and propulsion methods for reaching the planet within centuries.

**Tags**: `#astronomy`, `#exoplanets`, `#habitable zone`, `#atmosphere`, `#JWST`

---

<a id="item-4"></a>
## [Practical SQLite Tips: .expert Index Analysis and .dump Backup with zstd](https://jvns.ca/blog/2026/07/17/learning-about-running-sqlite/) ⭐️ 8.0/10

Julia Evans shares a collection of practical SQLite tips, highlighting the .expert command for automatic index recommendations and backup strategies using .dump piped to zstd for efficient compression. These tips help database users optimize performance and backup workflows with minimal effort, especially valuable for those managing local databases like Home Assistant or small web applications. .expert mode suggests optimal indexes based on queries, while .dump with zstd offers fast, compressible backups that work alongside WAL mode without blocking writers.

hackernews · surprisetalk · Jul 17, 17:45 · [Discussion](https://news.ycombinator.com/item?id=48950122)

**Background**: SQLite is a popular embedded database engine used in many applications. The sqlite3 CLI provides commands like .expert for index recommendations, and .dump to output the database as SQL text. zstd is a fast lossless compression algorithm that can be used to compress the dump output efficiently.

<details><summary>References</summary>
<ul>
<li><a href="https://sqlite.org/cli.html">Command Line Shell For SQLite</a></li>
<li><a href="https://github.com/facebook/zstd">GitHub - facebook/zstd: Zstandard - Fast real-time compression algorithm · GitHub</a></li>
<li><a href="https://sqlite.org/src/file?name=ext/expert/README.md&ci=tip">SQLite: README.md at tip</a></li>

</ul>
</details>

**Discussion**: Commenters share additional techniques: using WAL mode for non-blocking backups, batching DELETE operations to avoid locks, and leveraging tools like s3-credentials for easy cloud storage access. The community finds .expert particularly useful for less experienced users.

**Tags**: `#SQLite`, `#backup`, `#database`, `#CLI`, `#tools`

---

<a id="item-5"></a>
## [Open Source AI Models Surge in Usage and Debate](https://stateofopensource.ai/) ⭐️ 8.0/10

A new report from Mozilla's CTO details the rapid growth of open-weight AI models, which now handle 63% of tokens on OpenRouter, up from 37% four months ago. This shift threatens the market dominance of closed-source leaders like OpenAI and Anthropic, as open models offer competitive performance without licensing fees, potentially reshaping the AI industry. The report notes open models processed 4.19 trillion tokens on March 19, nearly 5x the 888 billion from four months earlier. However, multiple commenters criticized the report as LLM-generated and lacking genuine analysis.

hackernews · rellem · Jul 17, 14:31 · [Discussion](https://news.ycombinator.com/item?id=48947825)

**Background**: Open-weight AI models, such as Meta's Llama and Mistral, provide trained parameters for download but may not meet full open-source definitions requiring training data and code. The debate over open vs closed AI has intensified as open models rapidly improve.

<details><summary>References</summary>
<ul>
<li><a href="https://www.linkedin.com/pulse/frontier-ai-models-closed-vs-open-weight-source-varadaraj-pandurangan-yrdue">Frontier AI Models : Closed vs Open Weight vs Open Source</a></li>
<li><a href="https://geotoolbox.ai/blog/open-weights-vs-open-source">Open Weights vs Open Source : The Real Difference... | GEO Toolbox</a></li>

</ul>
</details>

**Discussion**: Commenters like babblingfish and GodelNumbering highlight the market shift favoring open models, predicting the decline of closed-source companies. Others criticize the report's quality, with andymatuschak noting it is clearly LLM-generated and hughw calling it painful to read.

**Tags**: `#open source`, `#AI`, `#machine learning`, `#models`, `#community`

---

<a id="item-6"></a>
## [Three Non-Solution Responses to Problems](https://improvesomething.today/responses-to-problems/) ⭐️ 8.0/10

The article categorizes three common non-solution responses to problems: ignoring, preserving, and a third unnamed response, offering a framework for understanding organizational behavior. This framework is relevant for software engineers, managers, and anyone in organizations, as it highlights how incentives and system dynamics often prevent effective problem-solving. The article's community discussion, including comments from didgetmaster and 0wis, provides real-world examples in government and expert roles, showing how preserving problems can serve institutional or personal interests.

hackernews · surprisetalk · Jul 17, 14:00 · [Discussion](https://news.ycombinator.com/item?id=48947490)

**Background**: In organizational behavior, problems often go unsolved not due to incompetence but because incentives reward maintaining the status quo. The article introduces a simple taxonomy of non-solution responses that goes beyond the usual focus on active problem-solving.

**Discussion**: Commenters generally agreed with the framework, with didgetmaster highlighting government's incentive to preserve problems and 0wis noting that even individual experts may avoid solving root causes to protect their positions. Another comment linked the categories to risk management strategies.

**Tags**: `#problem-solving`, `#organizational-behavior`, `#system-dynamics`, `#management`, `#incentives`

---

<a id="item-7"></a>
## [Huawei Unveils Ascend 950 SuperNode with 6.7x Performance Claim](https://www.ithome.com/0/978/019.htm) ⭐️ 8.0/10

Huawei publicly debuted the Ascend 950 SuperNode (Atlas 950 SuperPoD) at the 2026 World AI Conference, claiming it delivers 6.7 times the computing power of NVIDIA's equivalent NVL144 system. This announcement signals a potential paradigm shift in AI hardware, as Huawei challenges NVIDIA's dominance with a massive performance advantage, which could reshape the AI compute landscape especially in China. The Ascend 950 SuperNode supports up to 1024 Ascend processors via the Lingqu interconnection protocol, offering 1 EFLOPS FP8 and 2 EFLOPS FP4 compute with 256 TB unified memory, based on a supernode architecture.

telegram · zaihuapd · Jul 17, 10:27

**Background**: Huawei's supernode architecture uses a high-speed interconnect protocol called Lingqu (now UnifiedBus) to pool AI processors into a single massive compute unit. This approach aims to bypass limitations of traditional clustering and reduce dependence on advanced chip manufacturing, as Huawei faces US export restrictions. The Ascend 384 SuperNode has already been deployed in over 750 commercial systems across industries.

<details><summary>References</summary>
<ul>
<li><a href="https://www.huawei.com/en/news/2025/9/hc-lingqu-ai-superpod">Huawei Unveils World's Most Powerful SuperPoDs and... - Huawei</a></li>
<li><a href="https://www.scmp.com/tech/big-tech/article/3311873/huawei-pushes-ascend-ai-processor-based-supernode-computing-architecture-developers">Huawei pushes Ascend AI processor-based ‘ Supernode ’ computing...</a></li>

</ul>
</details>

**Tags**: `#Huawei`, `#AI Hardware`, `#Ascend`, `#SuperNode`, `#Computing`

---

<a id="item-8"></a>
## [SpaceX in talks with Pentagon for AI computing power deal worth billions](https://www.wsj.com/tech/ai/spacex-in-talks-to-provide-computing-power-for-pentagons-ai-push-15e752e4) ⭐️ 8.0/10

SpaceX is negotiating with the U.S. Pentagon to provide data center computing power for running AI models, with the deal potentially worth tens of billions of dollars. The talks are ongoing and could still collapse, according to people familiar with the matter. This deal would mark SpaceX's largest expansion into cloud computing and deepen its ties with the Pentagon, which is racing to acquire computing capability for national security AI applications. Success could shift the landscape of defense cloud contracts, traditionally dominated by Amazon, Microsoft, and Google. The Pentagon recently approved SpaceX, Amazon, Google, Microsoft, and Oracle to use their AI models in classified environments. SpaceX has also signed similar computing deals with Anthropic and Google in recent months and plans to scale its cloud business dramatically.

telegram · zaihuapd · Jul 18, 01:44

**Background**: SpaceX is primarily known for rockets and satellites (Starlink), but it also operates a growing cloud computing division called SpaceX Cloud, which leverages its data center infrastructure. The Pentagon is seeking to integrate AI into operations, requiring massive computing resources that traditional cloud providers are also competing to supply.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Anthropic_AI_PBC">Anthropic AI PBC</a></li>

</ul>
</details>

**Tags**: `#AI算力`, `#国防`, `#SpaceX`, `#云计算`

---