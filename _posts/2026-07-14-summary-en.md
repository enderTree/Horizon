---
layout: default
title: "Horizon Summary: 2026-07-14 (EN)"
date: 2026-07-14
lang: en
---

> From 15 items, 4 important content pieces were selected

---

1. [Sega CD Silpheed's Simulated 3D Graphics Deep Dive](#item-1) ⭐️ 8.0/10
2. [Telegram's t.me domain suspended](#item-2) ⭐️ 8.0/10
3. [Chain of Thought as a scaling trap; latent reasoning rises](#item-3) ⭐️ 8.0/10
4. [GPUHedge reduces serverless GPU cold start p95 latency from 117s to 30s](#item-4) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Sega CD Silpheed's Simulated 3D Graphics Deep Dive](https://fabiensanglard.net/silpheed/index.html) ⭐️ 8.0/10

Fabien Sanglard published a detailed technical analysis explaining how the Sega CD game Silpheed simulated 3D graphics by overlaying polygon-rendered sprites on pre-recorded full-motion video (FMV) backgrounds. This analysis reveals the ingenious engineering behind achieving 3D-like visuals on hardware with no 3D capabilities, offering valuable lessons for retro game developers and enthusiasts interested in software optimization. The article details custom video compression, color palette manipulation, and sprite rendering techniques that maximized the Sega CD's limited bandwidth and memory, enabling smooth, cinematic gameplay.

hackernews · ibobev · Jul 13, 14:52 · [Discussion](https://news.ycombinator.com/item?id=48893639)

**Background**: The Sega CD, an add-on for the Sega Genesis, lacked dedicated 3D graphics hardware. To create the illusion of 3D, many games used FMV backgrounds with interactive sprites. Silpheed used this approach, pre-rendering detailed 3D backgrounds on powerful computers and combining them with real-time polygon ships in-game.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Silpheed">Silpheed - Wikipedia</a></li>
<li><a href="https://fabiensanglard.net/silpheed/index.html">The art and engineering of Sega CD Silpheed</a></li>
<li><a href="https://theideamagazine.com/media-entertainment/the-art-and-engineering-of-sega-cd-silpheed/">The Art And Engineering Of Sega CD Silpheed</a></li>

</ul>
</details>

**Discussion**: Commenters expressed nostalgia for the Sega CD era and praised the technical depth of the article. Some noted that while the visuals were impressive, the gameplay was lacking. Others shared links to impressive demos on similar hardware, highlighting the ingenuity of developers of that time.

**Tags**: `#retro gaming`, `#game development`, `#Sega CD`, `#technical deep-dive`, `#graphics programming`

---

<a id="item-2"></a>
## [Telegram's t.me domain suspended](https://www.whois.com/whois/t.me) ⭐️ 8.0/10

Telegram's t.me domain, widely used for short links, has been suspended with ICANN status codes clientRenewProhibited and serverDeleteProhibited, indicating a legal or regulatory dispute. This disruption affects millions of users who rely on t.me links for sharing Telegram content and raises concerns about domain stability under geopolitical pressure. ICANN explains that clientRenewProhibited is uncommon and typically enacted during legal disputes, while serverDeleteProhibited prevents deletion. Telegram uses GoDaddy as its registrar, a company criticized for lack of transparency.

hackernews · Tiberium · Jul 13, 19:52 · [Discussion](https://news.ycombinator.com/item?id=48897878)

**Background**: Domain suspension occurs when a registrar disables a domain, preventing it from resolving to any server. t.me is Telegram's official URL shortener service. Telegram is currently under legal scrutiny in Russia, France, and India for various alleged violations.

<details><summary>References</summary>
<ul>
<li><a href="https://news.ycombinator.com/item?id=48897878">Telegram's t . me domain has been suspended | Hacker News</a></li>
<li><a href="https://meduza.io/en/news/2022/10/30/roskomnadzor-blocks-telegram-domain-t-me">Roskomnadzor briefly blocks Telegram domain t . me — Meduza</a></li>

</ul>
</details>

**Discussion**: Community comments express surprise that Telegram relies on GoDaddy, noting its poor track record. Some users had already started migrating away from Telegram to platforms like Zulip, and this event reinforces that decision. The discussion highlights geopolitical and legal pressures.

**Tags**: `#telegram`, `#domain suspension`, `#internet governance`, `#censorship`, `#godaddy`

---

<a id="item-3"></a>
## [Chain of Thought as a scaling trap; latent reasoning rises](https://www.reddit.com/r/MachineLearning/comments/1uviru5/chain_of_thought_is_a_scaling_trap_the_next_wave/) ⭐️ 8.0/10

A Reddit post argues that Chain of Thought (CoT) reasoning in LLMs is a scaling trap due to faithfulness and cost issues, and advocates for latent reasoning methods such as Coconut (continuous latent thought), HRM (hierarchical reasoning model), and BDH (Dragon Hatchling). The post introduces the concept of "language as interface vs language as compute substrate" and highlights the need for outer-loop governance to address the black-box nature of latent reasoning. This discussion challenges the prevailing use of CoT in LLMs and points to a paradigm shift toward latent reasoning, which could reduce inference cost and improve efficiency. However, it also raises governance concerns for high-stakes applications, making it relevant for researchers and practitioners in AI safety and deployment. Coconut uses the last hidden state as continuous thought without decoding to text, while HRM separates slow planning from fast execution. BDH achieves 97.4% accuracy on Sudoku Extreme without CoT, and aims to combine latent iteration with principled state management over time. The post emphasizes that latent reasoning creates a "black box wall" requiring outer-loop verification via DAGs, unit tests, or formal specs.

reddit · r/MachineLearning · /u/meowsterpieces · Jul 13, 17:50

**Background**: Chain of Thought (CoT) is a prompting method that encourages LLMs to generate intermediate reasoning steps as text, improving performance on complex tasks. However, it increases token usage and latency, and the text trace may not faithfully reflect the model's actual reasoning. Latent reasoning methods instead perform computation in the model's internal representation space, only outputting language at the end, which can reduce cost but raises interpretability challenges.

<details><summary>References</summary>
<ul>
<li><a href="https://arxiv.org/abs/2412.06769">[2412.06769] Training Large Language Models to Reason in a Continuous Latent Space</a></li>
<li><a href="https://arxiv.org/abs/2506.21734">[2506.21734] Hierarchical Reasoning Model</a></li>
<li><a href="https://github.com/pathwaycom/bdh/">GitHub - pathwaycom/bdh: BDH (Dragon Hatchling ...</a></li>

</ul>
</details>

**Tags**: `#chain-of-thought`, `#latent reasoning`, `#LLM reasoning`, `#scaling`, `#faithfulness`

---

<a id="item-4"></a>
## [GPUHedge reduces serverless GPU cold start p95 latency from 117s to 30s](https://www.reddit.com/r/MachineLearning/comments/1uvlb6h/gpuhedge_hedging_serverless_gpu_providers/) ⭐️ 8.0/10

GPUHedge, an open-source tool, uses speculative execution across multiple serverless GPU providers to reduce cold start p95 latency from 116.6 seconds to 29.4 seconds in a benchmark using RunPod as primary and Cerebrium as backup. Cold start latency is a critical problem for serverless GPU inference, often exceeding tens of seconds. GPUHedge's approach demonstrates a practical method to significantly reduce long-tail latency, making serverless GPU more viable for latency-sensitive AI workloads. The tool is licensed under Apache-2.0 and currently in alpha. In the benchmark, hedging launched after 10 seconds, reducing requests over 60 seconds from 11/36 to 0/36, and modeled active-compute cost decreased from $0.0114 to $0.0083 per request.

reddit · r/MachineLearning · /u/Putrid_Construction3 · Jul 13, 19:20

**Background**: Serverless GPU providers offer on-demand access to GPUs but suffer from cold starts when no idle instance is available. Cold starts can take minutes to load models and dependencies. GPUHedge addresses this by hedging: sending requests to a primary provider and conditionally launching a backup on another provider, canceling the losing job.

<details><summary>References</summary>
<ul>
<li><a href="https://www.runpod.io/product/serverless">Serverless GPU Platform for AI Inference | Runpod</a></li>
<li><a href="https://cerebrium.ai/">Serverless GPU Infrastructure for Real-Time AI | Cerebrium</a></li>
<li><a href="https://modal.com/blog/serverless-gpu-article">Learn about the most popular serverless GPU providers in 2025</a></li>

</ul>
</details>

**Tags**: `#GPU`, `#serverless`, `#cold start`, `#hedging`, `#latency`

---