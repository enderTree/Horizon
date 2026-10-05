---
layout: default
title: "Horizon Summary: 2026-10-05 (EN)"
date: 2026-10-05
lang: en
---

> From 24 items, 4 important content pieces were selected

---

1. [Apple CEO John Ternus pushes reforms to accelerate and streamline the company](#item-1) ⭐️ 9.0/10
2. [Strata runs 125B Qwen 3.8 Flash Next on a single RTX 4090 at 100+ tok/s](#item-2) ⭐️ 8.0/10
3. [ARC-AGI-3 Kaggle top score reportedly jumps from 7% to 56% in 30 days](#item-3) ⭐️ 8.0/10
4. [SK Telecom Apologizes for Massive Data Breach, Offers Free USIM Replacements](#item-4) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Apple CEO John Ternus pushes reforms to accelerate and streamline the company](https://t.me/zaihuapd/44211) ⭐️ 9.0/10

Weeks after taking over as Apple CEO, John Ternus has begun pushing internal reforms aimed at speeding up product development, expanding the product lineup, and making the organization leaner and more engineering-focused. According to Bloomberg and Reuters, Apple is considering moving away from its fixed spring/fall launch cadence toward more flexible year-round releases, trimming some middle-management roles to shorten the decision chain between engineering teams and top executives, and hunting for new revenue streams from existing products. This is one of the most consequential leadership transitions in the tech industry: Apple is handing the CEO seat to a hardware engineer at a moment when its rivals are led by software and AI specialists. If Ternus succeeds in loosening the rigid spring/fall launch calendar, it could reshape how Apple's supply chain, developers, and customers plan around new products, and signal a strategic pivot toward hardware execution and engineering-driven decision making. The reforms reportedly include cutting some middle-management positions and shortening the path between engineering teams and senior leadership, while exploring ways to extract more revenue from the existing install base rather than relying solely on new hardware. The shift away from fixed spring/fall launch windows is described as under consideration rather than finalized, so new-product timing for developers and retail partners remains uncertain.

telegram · zaihuapd · Oct 4, 15:03

**Background**: John Ternus joined Apple's product design team in 2001, became vice president of hardware engineering in 2013, and joined Apple's executive team in 2021 as senior vice president of hardware engineering, overseeing products including the iPhone, iPad, Mac and AirPods. He took over the CEO role from Tim Cook, whose long tenure was defined by operational excellence and a highly regularized annual launch cadence. Apple's habit of anchoring major product launches in spring and fall has shaped everything from its supply chain planning to the seasonal rhythm of app and accessory ecosystems, so any change to that calendar has ripple effects across the industry.

<details><summary>References</summary>
<ul>
<li><a href="https://news.qq.com/rain/a/20260901A0ABT600">Tim Cook卸任苹果首席执行官一职， John Ternus ...</a></li>
<li><a href="https://global.hk01.com/数码生活/60343373/apple新ceo-john-ternus是谁-曾为一颗螺丝跟同事吵翻的细节狂魔">Apple 新CEO John Ternus 是谁？ 曾为一颗螺丝跟同事吵翻的细节狂魔</a></li>
<li><a href="https://today.line.me/tw/v3/article/vXOLpp3">Tim Cook交棒！ Apple 硬 體 工 程 資深 副 總 裁 John Ternus 將接任CEO</a></li>

</ul>
</details>

**Tags**: `#Apple`, `#CEO transition`, `#organizational restructuring`, `#product strategy`, `#tech industry`

---

<a id="item-2"></a>
## [Strata runs 125B Qwen 3.8 Flash Next on a single RTX 4090 at 100+ tok/s](https://github.com/Niko1221/Strata) ⭐️ 8.0/10

The open-source project Strata (GitHub: Niko1221/Strata) demonstrates running the 125B-parameter Qwen 3.8 Flash Next model on a single consumer RTX 4090 at over 100 tokens per second. Community members quickly reproduced the result, reporting 124 tok/s on a 4090 with 128GB DDR5 and Ryzen 7950X3D, and roughly 62 tok/s on a single 24GB RTX 5090 plus ~40GB of system RAM using a UD-IQ4_XS (~4-bit) GGUF quant. Running a 100B+ class open-weight model interactively on hardware that costs a few thousand dollars, rather than a rented data-center GPU, meaningfully lowers the barrier to local, private, offline inference. At the same time, the thread shows the community increasingly treating tokens-per-second claims as insufficient, demanding accuracy, energy, and long-context measurements alongside throughput before accepting such optimizations as genuinely useful. The approach relies on low-bit GGUF quantization (around 4-bit and below) combined with substantial system RAM for weight offloading, so its performance is memory-bandwidth bound rather than compute bound. A user's 50-image coordinate-prediction benchmark found Strata produced a median error of 154.8 pixels versus 46.5 pixels for llama.cpp with the same GGUF weights and vision adapter, which is a concrete signal that the speedup may come with a real accuracy cost for vision tasks.

hackernews · snehesht · Oct 4, 12:51 · [Discussion](https://news.ycombinator.com/item?id=49953495)

**Background**: Quantization is a model-compression technique that converts a model's weights (and sometimes activations) from high-precision formats such as FP16 or BF16 into lower-precision representations like 4-bit integers; it can cut hardware requirements by up to roughly 80 percent at the cost of some quality loss. This is what makes very large models fit into the 24GB of VRAM on a consumer card like the RTX 4090, with the remaining weights streamed from system RAM. Qwen 3.8 Flash Next is a 125B-parameter model from Alibaba's Qwen team, and its official Hugging Face release plus local-run guides (e.g. Unsloth's) are what made same-day experimentation possible.

<details><summary>References</summary>
<ul>
<li><a href="https://huggingface.co/Qwen/Qwen3.8-Flash-Next">Qwen / Qwen 3 . 8 - Flash - Next · Hugging Face</a></li>
<li><a href="https://unsloth.ai/docs/models/qwen3.8-next">Qwen 3 . 8 - Flash - Next : How to Run Locally | Unsloth Documentation</a></li>
<li><a href="https://www.datacamp.com/tutorial/quantization-for-large-language-models">Quantization for Large Language Models (LLMs): Reduce... | DataCamp</a></li>

</ul>
</details>

**Discussion**: Sentiment is a mix of genuine excitement and methodological skepticism. Several users reported solid real-world results (124 tok/s on a 4090; ~62 tok/s on a 5090 with ~4-bit quant that "holds up fine" for coding and refactoring), while others questioned whether benchmarking survives a fixed task suite measuring accuracy, energy, long-context behavior and run-to-run variance, and warned that going below 4-bit risks significant quality degradation. The most pointed counterargument was an independent vision benchmark where Strata's error was roughly three times that of llama.cpp on identical weights.

**Tags**: `#LLM inference`, `#quantization`, `#consumer hardware`, `#Qwen`, `#performance optimization`

---

<a id="item-3"></a>
## [ARC-AGI-3 Kaggle top score reportedly jumps from 7% to 56% in 30 days](https://www.reddit.com/r/MachineLearning/comments/1wxcd4k/top_arc%CE%B1gi3_scores_on_kaggle_just_went_from_7_to/) ⭐️ 8.0/10

A Reddit post on r/MachineLearning reports that the top score on the Kaggle leaderboard for ARC-AGI-3, the interactive reasoning benchmark from the ARC Prize Foundation, rose from roughly 7% to about 56% over the past 30 days. The reported gains were achieved by smallish local models running inside a harness, since Kaggle competition rules restrict participants to locally runnable models rather than frontier API systems. ARC-AGI has become one of the most closely watched indicators of progress toward general reasoning ability, and ARC-AGI-3 was specifically designed so that humans outperform machines by requiring agents to explore novel environments and learn goals on the fly. If the reported jump holds up, it suggests that scaffolding plus modest open models can close a gap that was previously treated as a strong marker of human superiority, which would reshape how the community interprets AGI benchmark progress. The claim is based on a single Reddit post whose author admits the attached leaderboard graphic is slightly out of date, and the scores depend heavily on the harness and scaffolding wrapped around the models rather than raw model capability alone. Because it is a leaderboard result rather than a peer-reviewed evaluation, the numbers may shift as the leaderboard updates and should be treated as a community-visible signal rather than a confirmed capability breakthrough.

reddit · r/MachineLearning · /u/we_are_mammals · Oct 4, 10:24 · [Discussion](https://www.reddit.com/r/MachineLearning/comments/1wxcd4k/top_arcαgi3_scores_on_kaggle_just_went_from_7_to/)

**Background**: ARC-AGI (Abstraction and Reasoning Corpus for AGI) is a benchmark series from the ARC Prize Foundation intended to measure fluid intelligence and general reasoning rather than memorized knowledge; earlier versions (ARC-AGI-1 and 2) tested passive puzzle solving, while ARC-AGI-3 turns the task into an interactive one where agents must act, get feedback, build world models, and adapt to unfamiliar game mechanics. A score of 100% on ARC-AGI-3 would mean an agent can beat every game as efficiently as humans. An evaluation harness is the standardized infrastructure that runs a model through a benchmark, applies prompts and tooling, and scores the results, so harness design can substantially change reported scores.

<details><summary>References</summary>
<ul>
<li><a href="https://arcprize.org/arc-agi/3">ARC-AGI-3</a></li>
<li><a href="https://arcprize.org/leaderboard">ARC-AGI-3 Leaderboard - ARC Prize</a></li>
<li><a href="https://arize.com/blog/what-is-an-evaluation-harness/">What is an evaluation harness ? Definition & guide - Arize AI</a></li>

</ul>
</details>

**Tags**: `#ARC-AGI`, `#benchmarks`, `#LLM-reasoning`, `#AGI`, `#Kaggle`

---

<a id="item-4"></a>
## [SK Telecom Apologizes for Massive Data Breach, Offers Free USIM Replacements](https://t.me/zaihuapd/44206) ⭐️ 8.0/10

SK Telecom (SKT), South Korea's largest mobile carrier, confirmed that hackers breached its internal systems and compromised a core HSS server, exposing sensitive data of more than 25 million users — including IMEI, SN, ICCID, PIN2/PUK2, eID, encrypted K values and private keys. Following the incident, the SKT CEO issued a public apology and announced free USIM card replacements for any SKT user who wants one (including MVNO users on its network, with some device exceptions), plus reimbursement for users who recently paid to replace their cards. The leaked K key is the root secret used to authenticate a subscriber on the mobile network, so its exposure could let attackers clone USIM cards, impersonate subscribers, or intercept communications if exploited. As a breach affecting 25+ million people at a national carrier's core infrastructure, it underscores how vulnerable telecom authentication databases are critical targets and is likely to push other operators to harden HSS security and accelerate USIM replacement programs. The exposed dataset includes device identifiers (IMEI, SN), card identifiers (ICCID), card unlock codes (PIN2/PUK2), eID, and the encrypted K values and private keys used in authentication. SKT notes that some device types are excluded from the free replacement program, and it has been urgently scaling up its response; users who recently paid for a USIM swap are eligible for reimbursement.

telegram · zaihuapd · Oct 4, 09:02

**Background**: A Home Subscriber Server (HSS) is the central database in 4G/LTE and 5G networks that stores subscriber profiles and provides the authentication and authorization data used to let devices join the network. Each subscriber's USIM — the upgraded SIM used for 3G and later networks — stores an ICCID and a secret K key that, combined with an operator key, forms the basis of all network cryptography; because the HSS holds a copy of that same K key, a breach there directly threatens card-level security. Replacing a USIM issues a new card with a new K key, which is why a nationwide card swap is the standard mitigation when keys are suspected of leaking.

<details><summary>References</summary>
<ul>
<li><a href="https://www.p1sec.com/blog/home-subscriber-server-hss">Home Subscriber Server (HSS): The Backbone of Modern Telecom ...</a></li>
<li><a href="https://nickvsnetworking.com/hss-usim-authentication-in-lte-nr-4g-5g/">HSS & USIM Authentication in LTE/NR (4G & 5G) | Nick vs ...</a></li>
<li><a href="https://support.huawei.com/enterprise/en/doc/EDOC1000079719/2070a180/what-is-the-difference-between-sim-and-usim-cards">What Is the Difference Between SIM and USIM Cards? - AR ...</a></li>

</ul>
</details>

**Tags**: `#cybersecurity`, `#data-breach`, `#telecom`, `#SKT`, `#USIM`

---