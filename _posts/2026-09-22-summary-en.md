---
layout: default
title: "Horizon Summary: 2026-09-22 (EN)"
date: 2026-09-22
lang: en
---

> From 37 items, 5 important content pieces were selected

---

1. [Xiaomi releases MiMo v2.6 open-weights MoE models with live RL dashboard](#item-1) ⭐️ 8.0/10
2. [Bryan Cantrill's Retrospective on What Sun Microsystems Got Wrong](#item-2) ⭐️ 8.0/10
3. [SemiAnalysis Analyzes Compute and Data Movement for MoE Inference](#item-3) ⭐️ 8.0/10
4. [Apple unveils 2nm M6 and first quad-die M5 Ultra chips](#item-4) ⭐️ 8.0/10
5. [25 Fields Medalists Warn AI May Be Misaligned With Math Research Goals](#item-5) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Xiaomi releases MiMo v2.6 open-weights MoE models with live RL dashboard](https://mimo.xiaomi.com/mimo-v2-6) ⭐️ 8.0/10

On September 22, Xiaomi's MiMo team released and open-sourced the MiMo-V2.6 family, consisting of two Mixture-of-Experts variants: Flash with 309B total / 15B activated parameters and Pro with 1.02T total / 42B activated parameters. Both are published as RL checkpoints on Hugging Face (XiaomiMiMo/MiMo-V2.6-Flash-RL and MiMo-V2.6-Pro-RL), accompanied by a detailed technical report and a public real-time RL training dashboard. A roughly 1-trillion-parameter open-weights release from a major consumer-hardware company signals that frontier-scale MoE training is no longer limited to a handful of Western AI labs, and it intensifies pressure on other vendors to disclose how their models are post-trained. The unusually open training methodology — including a livestreamed reinforcement-learning dashboard — gives researchers and practitioners a rare look at how large-scale RL post-training actually behaves in practice. Because these are MoE models, each token only activates a small slice of the network, so the 1.02T/42B Pro effectively runs like a far smaller dense model at inference time while still requiring storage for the full parameter set. The training dashboard also disclosed concrete safety-motivated choices, such as removing the "cyber dataset" from the upcoming Pro run after observing bad patterns in rollout logs, and the aligned RL stage uses a cold start in which the model reflects on and rewrites its own misaligned turns.

hackernews · volf_ · Sep 21, 20:12 · [Discussion](https://news.ycombinator.com/item?id=49792730)

**Background**: Mixture-of-Experts (MoE) is an architecture in which many separate sub-networks, or "experts", each specialize in different parts of the input space, and a gating network decides which experts handle each token; this lets a model hold a huge number of parameters while only computing with a fraction of them per token. RLHF-style post-training (reinforcement learning from human feedback, now often generalized to reinforcement learning from verifiable or AI-generated rewards) trains a reward model and then optimizes the language model against it to better follow instructions and safety norms. "Open weights" means the trained parameters are downloadable and runnable by anyone, but it does not necessarily imply that the training data or training code are also released — a distinction the community debates frequently.

<details><summary>References</summary>
<ul>
<li><a href="https://huggingface.co/blog/moe">Mixture of Experts Explained</a></li>
<li><a href="https://en.wikipedia.org/wiki/Reinforcement_learning_from_human_feedback">Reinforcement learning from human feedback - Wikipedia</a></li>
<li><a href="https://cursor.com/blog/real-time-rl-for-composer">Improving Composer through real-time RL · Cursor</a></li>

</ul>
</details>

**Discussion**: Commenters broadly praised Xiaomi's transparency, with one saying the live RL dashboard was "an incredible learning and teaching tool" and that the technical report was unusually comprehensive. Others highlighted the dashboard's note that the cyber dataset was removed from the Pro run after bad rollout patterns appeared, and one commenter cited the exact parameter counts with Hugging Face links; the thread also drifted into a geopolitical debate about whether US energy and grid constraints could let China win the AI race, plus a light-hearted "pelican" rendering test of both models.

**Tags**: `#LLM`, `#open-weights`, `#Mixture-of-Experts`, `#RLHF`, `#Xiaomi`

---

<a id="item-2"></a>
## [Bryan Cantrill's Retrospective on What Sun Microsystems Got Wrong](https://bcantrill.dtrace.org/2026/09/20/what-sun-got-wrong/) ⭐️ 8.0/10

Bryan Cantrill, a former Sun Microsystems engineer best known as a co-creator of DTrace, published a new essay on his blog titled "What Sun got wrong," examining the strategic and technical missteps that led to the company's decline. The post is a first-person retrospective that blends engineering history with business analysis, and it quickly drew a large discussion (531 points, 311 comments) on aggregator sites. Sun's collapse remains one of the most instructive failures in computing history, because it was a company with world-class engineering that still lost to cheaper commodity hardware and a changing market. For today's engineers and founders — especially those riding the current AI infrastructure boom — the essay is a case study in how technical excellence alone does not guarantee commercial survival. The piece is an insider account from someone who lived through Sun's decline rather than a third-party history, which gives it unusual credibility on both the engineering and organizational dimensions. Discussion threads around the essay highlight specific decisions such as Sun's brief cancellation of Solaris on x86 in 2002 and its failed attempt to strike a deal with Google in the same year, both of which commentators treat as turning points.

hackernews · chmaynard · Sep 21, 14:03 · [Discussion](https://news.ycombinator.com/item?id=49787436)

**Background**: Sun Microsystems was a pillar of 1980s and 1990s computing, selling high-end Unix workstations and servers built around its own SPARC processors and Solaris operating system, and it created Java. Its model of vertically integrated, expensive proprietary hardware was undermined by the rise of cheap x86 servers running Linux, and the company's revenue collapsed after the dot-com bubble burst. Oracle acquired Sun in 2010, ending its existence as an independent company.

**Discussion**: Commenters largely agree with the critique while adding their own anecdotes and sharpening the argument. Several recall Sun's painful sales process compared with Dell's next-day commodity servers, others list specific blunders such as cancelling Solaris on x86 and failing to close a Google deal, and one commenter argues Sun was never really interested in running a business at all — it built impressive technology first and tolerated sales only to fund it.

**Tags**: `#Sun Microsystems`, `#tech history`, `#business strategy`, `#software engineering`, `#retrospective`

---

<a id="item-3"></a>
## [SemiAnalysis Analyzes Compute and Data Movement for MoE Inference](https://newsletter.semianalysis.com/p/computation-and-data-movement-for) ⭐️ 8.0/10

SemiAnalysis published a technical analysis titled "Computation and Data Movement for Inference" that maps Mixture-of-Experts (MoE) model structure and data flow onto inference hardware for efficient serving. The piece walks through the model's structure, how data moves through it, and what that implies for building efficient inference systems. MoE has become the dominant architecture behind most frontier LLMs, so how these sparse models map onto accelerators directly determines serving cost, latency, and throughput for anyone deploying or buying inference infrastructure. As the industry shifts from raw FLOPs toward memory bandwidth and interconnect as the binding constraint, this kind of systems-level analysis shapes hardware roadmaps and data-center design. Because only a small subset of experts is activated per token, MoE inference tends to be bound by memory capacity, memory bandwidth, and the all-to-all communication needed to shuffle tokens to their assigned experts, rather than by raw matrix-multiply throughput. The full analysis goes deeper into structure, flow, and serving efficiency, though the short excerpt limits how much of the measured detail can be verified here.

rss · Semianalysis · Sep 21, 18:14

**Background**: Mixture-of-Experts replaces a dense transformer's single feed-forward network with many parallel "expert" networks plus a router that sends each token to only the top few experts, so a model can hold a huge total number of parameters while activating only a fraction of them per token. This sparsity cuts compute per token, but it turns serving into a distributed systems problem: experts are typically spread across multiple GPUs (expert parallelism), and tokens must be routed between them, making data movement a first-order concern. SemiAnalysis is a widely read semiconductor and AI infrastructure research publication, and NVIDIA has likewise argued that MoE underpins most frontier models today.

<details><summary>References</summary>
<ul>
<li><a href="https://developer.nvidia.com/blog/mastering-llm-techniques-inference-optimization/">Mastering LLM Techniques: Inference Optimization</a></li>
<li><a href="https://arxiv.org/pdf/2404.14294">A Survey on Efficient Inference for Large</a></li>
<li><a href="https://hal.science/hal-05113196v1/document">A Survey of Mixture of Experts Models : Architectures and...</a></li>

</ul>
</details>

**Tags**: `#MoE`, `#Inference`, `#AI Hardware`, `#Systems Engineering`, `#LLM Serving`

---

<a id="item-4"></a>
## [Apple unveils 2nm M6 and first quad-die M5 Ultra chips](https://t.me/zaihuapd/43965) ⭐️ 8.0/10

Apple announced the M6, its first chip built on a 2-nanometer process, debuting in a new Mac mini with a 12-core CPU, 12-core GPU, dual 16-core Neural Engines, and unified memory bandwidth of up to 170GB/s. Alongside it, the company introduced the M5 Ultra in a new Mac Studio — its first quad-die M-series chip — offering up to 36 CPU cores, 80 GPU cores, 512GB of unified memory, and 1.2TB/s of memory bandwidth. This is a double generational leap: the move to a 2nm node should deliver meaningfully better performance-per-watt for everyday Macs, while the quad-die M5 Ultra pushes Apple silicon into workstation-class territory with memory capacity and bandwidth that were previously the domain of high-end discrete GPUs and server CPUs. Developers running local AI models, video/3D pipelines, and large in-memory datasets are the most directly affected, and the 2nm debut also signals that leading-edge foundry capacity is now shipping in volume products. Apple claims the M5 Ultra's 1.2TB/s unified memory bandwidth is 50% higher than the M3 Ultra, and it achieves the quad-die layout through an updated UltraFusion interconnect that links two dual-die M5 Max chips. Note that the source is a brief summary with no benchmarks, pricing, availability dates, or independent performance validation, and the term "2nm" refers to a marketing node name rather than any single physical feature size.

telegram · zaihuapd · Sep 21, 16:32

**Background**: In chip manufacturing, a process node such as "2nm" (the step after 3nm) is a name for a generation of fabrication technology; smaller nodes generally allow higher transistor density, which translates into more performance at lower power. Apple's Ultra chips are built by packaging two Max-tier dies together via its UltraFusion interconnect, so a "quad-die" M5 Ultra means two M5 Max packages joined into a single system-on-chip. "Unified memory" means the CPU, GPU, and Neural Engine share one pool of on-package LPDDR5X memory instead of separate RAM and VRAM, so the quoted bandwidth figure sets an upper bound on how fast all those engines can pull data.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/2_nm_process">2 nm process - Wikipedia</a></li>
<li><a href="https://applescoop.org/story/m5-ultra-quad-die-architecture-explained">M5 Ultra Explained: How Apple’s First Quad - Die Chip Actually Works</a></li>
<li><a href="https://www.macobserver.com/news/apple-unveils-m6-and-m5-ultra-chips-with-huge-cpu-gpu-and-ai-upgrades/">Apple Unveils M6 and M5 Ultra Chips With Huge CPU, GPU and AI...</a></li>

</ul>
</details>

**Tags**: `#apple-silicon`, `#hardware`, `#chips`, `#semiconductor`, `#2nm-process`

---

<a id="item-5"></a>
## [25 Fields Medalists Warn AI May Be Misaligned With Math Research Goals](https://t.me/zaihuapd/43973) ⭐️ 8.0/10

A joint statement signed by 25 mathematicians including Terence Tao (陶哲轩) and Deng Yu (邓煜) — described in reports as Fields medalists — warns that the rapid deployment of AI to solve mathematical problems may cause the goals of AI development to become "severely misaligned" with the goals of mathematical research. The signatories argue that treating mathematical problem-solving as a benchmark for AI capability risks damaging both mathematics research and the broader academic ecosystem. This is a rare collective intervention by some of the most decorated figures in mathematics, and it arrives just as AI labs increasingly cite math benchmarks as evidence of reasoning progress. It signals that the research community may push back on how AI capabilities in mathematics are measured, rewarded, and published, affecting AI developers, journals, universities, and funders. The statement stresses that the core of mathematical research is forming conceptual understanding and new insights rather than merely obtaining answers, and warns that AI-generated output at scale could squeeze the time available for verification, communication, and citing prior work while raising problems of authorship and plagiarism. It also concedes that AI has real potential to raise research efficiency, and that the outcome depends on how people choose to use the technology.

telegram · zaihuapd · Sep 22, 03:00

**Background**: The Fields Medal is awarded by the International Mathematical Union every four years to up to four mathematicians aged 40 or under, and is widely regarded as the highest honor in mathematics; Terence Tao, one of the named signatories, received it in 2006. Large language models have improved markedly in recent years at solving mathematical problems, which has made math contests and open problems popular yardsticks for measuring AI reasoning ability. In mathematics, however, a claimed result only becomes knowledge after other researchers verify it, discuss it, and correctly attribute the prior work it builds on — steps that are slow and human-intensive.

**Tags**: `#AI`, `#mathematics`, `#research ethics`, `#large language models`, `#academic publishing`

---