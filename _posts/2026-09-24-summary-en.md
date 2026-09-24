---
layout: default
title: "Horizon Summary: 2026-09-24 (EN)"
date: 2026-09-24
lang: en
---

> From 33 items, 3 important content pieces were selected

---

1. [Anthropic says Claude discovered a novel enzyme system with CRISPR-like repeats](#item-1) ⭐️ 8.0/10
2. [Essay: LLM Tokens Could Soon Cost Less Than a grep](#item-2) ⭐️ 8.0/10
3. [ClusterMAX 3.0: SemiAnalysis Updates Its GPU Cloud Rating System](#item-3) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Anthropic says Claude discovered a novel enzyme system with CRISPR-like repeats](https://www.anthropic.com/news/claude-discovers-novel-enzyme-system) ⭐️ 8.0/10

Anthropic reports that its Claude model, acting as an autonomous agent, identified a previously undescribed genomic arrangement while scanning raw DNA sequence data: a tandem repeat array with CRISPR-like structure sitting next to a known retron-like reverse transcriptase. The finding was published in an Anthropic news post and quickly became one of the most discussed AI-for-science items of the week. It is a high-profile example of an LLM agent contributing to genuine biological discovery, which strengthens the case for AI-driven science while simultaneously re-igniting biosecurity debates about whether such models should be pointed at genome engineering. If agents can surface novel sequence architectures from raw data, the bottleneck in biology shifts further toward experimental validation and interpretation. Commenters note that the system centers on an already known retron-like reverse transcriptase, and that the practical limits of genome editing today come mainly from delivery rather than from the availability of nucleases, so the 'breakthrough' framing may be overstated. Standalone CRISPR arrays and CRISPR repeat-like RNA regulatory elements have also been documented in the literature for years, which tempers how novel the repeat arrangement itself is.

hackernews · raahelb · Sep 23, 18:06 · [Discussion](https://news.ycombinator.com/item?id=49820134)

**Background**: CRISPR stands for clustered regularly interspaced short palindromic repeats: bacterial and archaeal adaptive immune systems built from short repeats separated by spacer sequences, usually sitting next to cas genes, which scientists repurposed into tools such as Cas9 for gene editing. Retrons are bacterial retroelements that use a reverse transcriptase to produce msDNA and have more recently been engineered into genome-editing tools as well. Large language model agents can ingest very long DNA sequences and flag patterns within them, which is the mechanism behind claims of this kind of discovery.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/CRISPR">CRISPR - Wikipedia</a></li>
<li><a href="https://pmc.ncbi.nlm.nih.gov/articles/PMC7757702/">CRISPR Arrays Away from cas Genes - PMC - NIH</a></li>
<li><a href="https://www.nature.com/articles/s41586-023-06221-2">Scientific discovery in the age of artificial intelligence | Nature</a></li>

</ul>
</details>

**Discussion**: The overall sentiment is excitement tempered by skepticism: one highly upvoted comment argues the finding is really just a previously undescribed arrangement around a known reverse transcriptase and that gene-editing therapy is limited by delivery, while others enjoy being able to 'relive' the discovery through the agent's transcript. Several commenters joked about the tension between Anthropic's stated prohibition on using Claude for bio-engineering and its promotion of a genome-editing-related discovery, and one asked how an LLM can reason about biochemistry at all.

**Tags**: `#AI for Science`, `#CRISPR`, `#Genomics`, `#Anthropic`, `#Biotechnology`

---

<a id="item-2"></a>
## [Essay: LLM Tokens Could Soon Cost Less Than a grep](https://jyn.dev/tokens-too-cheap-to-meter/) ⭐️ 8.0/10

In a blog post titled "Tokens too cheap to meter", the author observes that a call to a model such as GPT-5.6 Luna is currently only about 4-5 orders of magnitude more expensive than running grep, and predicts that at current rates of progress, calling an LLM will soon be cheaper than a routine local tool call. The essay drew a large Hacker News discussion of 254 points and 186 comments. If inference really becomes that cheap, the economics of agentic software change fundamentally: models could be invoked for trivial checks, retries and fan-out work that is currently reserved for local tools, making "LLM as a subroutine" the default design pattern. At the same time, it forces scrutiny of whether the enormous infrastructure spending behind those cheap tokens can ever be recouped. The gap being extrapolated is still 4-5 orders of magnitude, so the prediction requires many more years of compounding efficiency gains before it holds. The piece focuses on per-call cost and largely glosses over business-model viability and the possibility that per-call cost for high-quality, compiled capabilities may plateau rather than fall forever; commenters also disputed its related claim about "malleable software".

hackernews · teoruiz · Sep 23, 09:21 · [Discussion](https://news.ycombinator.com/item?id=49813482)

**Background**: LLM inference tokens are the units of text a model reads and generates; providers bill per million input and output tokens, and inference is the step where a trained model answers a prompt rather than being trained. A tool call is when a model invokes an external function or program — such as grep — to fetch data or act on its environment, which today is essentially free compared with a model call. The essay's title echoes Lewis Strauss's 1954 promise of nuclear electricity "too cheap to meter", a forecast that never materialized, a parallel several commenters raised. Historically inference costs at a fixed capability level have fallen dramatically: the Stanford HAI 2025 AI Index reports a more than 280-fold drop for GPT-3.5-level systems between November 2022 and October 2024.

<details><summary>References</summary>
<ul>
<li><a href="https://valueaddvc.com/blog/how-ai-inference-costs-have-dropped-95-in-two-years-and-what-happens-next">AI Inference: 95% Cost Cut in Two Years, $0.50/M</a></li>
<li><a href="https://www.mirantis.com/blog/inference-costs/">Optimizing Inference Costs: The Complete Guide | Mirantis</a></li>
<li><a href="https://huggingface.co/blog/Kseniase/inference">Topic 23: What is LLM Inference , it's challenges and solutions for it</a></li>

</ul>
</details>

**Discussion**: The thread is broadly appreciative but skeptical of the extrapolation: jetrink invokes Stein's Law, arguing that if something cannot go on forever it will stop, so these efficiency gains will not continue indefinitely. cs702 praises the essay but says it poorly analyzes business-model viability, since all the major players are betting that future profits will justify insane amounts of infrastructure investment. abirch compares the claim to Lewis Strauss's 1954 "too cheap to meter" nuclear promise that never came true, and rtpg questions the essay's claim about malleable software.

**Tags**: `#AI/ML`, `#LLM economics`, `#inference cost`, `#business models`, `#technology forecasting`

---

<a id="item-3"></a>
## [ClusterMAX 3.0: SemiAnalysis Updates Its GPU Cloud Rating System](https://newsletter.semianalysis.com/p/clustermax-30-the-industry-standard) ⭐️ 8.0/10

SemiAnalysis has released ClusterMAX 3.0, the third major iteration of its GPU cloud rating and ranking system, which evaluates GPU cloud providers worldwide across reliability, performance, support, pricing, and security. The update is described as the firm's most thorough global analysis of GPU cloud providers to date. Choosing a GPU cloud is now a major capital and operational decision for AI teams, and an independent, data-driven scorecard helps buyers distinguish genuinely reliable capacity from marketing claims as GPU supply remains tight. Because ClusterMAX has become a de facto industry benchmark, its ratings can influence provider reputations, enterprise procurement, and even pricing power. The ClusterMAX framework scores over 80 GPU clouds across dimensions including performance, networking, storage, security, support, and pricing, rather than relying on simple benchmark or cost comparisons alone. It is an industry analysis rather than a technical breakthrough, and the full detail sits behind SemiAnalysis's newsletter and the dedicated clustermax.ai site.

rss · Semianalysis · Sep 23, 21:20

**Background**: SemiAnalysis is a semiconductor and AI infrastructure research firm led by Dylan Patel, widely followed for its analysis of datacenter power, accelerators, and supply chains. Its ClusterMAX system, whose 2.0 edition appeared in November 2025, is designed as an independent framework that goes beyond raw benchmarks to judge the whole service ecosystem of a GPU cloud. GPU clouds rent out accelerators such as NVIDIA GPUs by the hour for AI training and inference, and their real-world quality varies widely in areas like interconnect bandwidth, storage throughput, and support responsiveness — which is exactly what ClusterMAX tries to quantify.

<details><summary>References</summary>
<ul>
<li><a href="https://www.clustermax.ai/">GPU Cloud ClusterMAX™ Rating & Ranking System | SemiAnalysis</a></li>
<li><a href="https://www.clustermax.ai/overview">ClusterMAX Overview — GPU Cloud Rating Methodology ...</a></li>
<li><a href="https://newsletter.semianalysis.com/p/clustermax-20-the-industry-standard">ClusterMAX™ 2.0: The Industry Standard GPU Cloud Rating System</a></li>

</ul>
</details>

**Tags**: `#GPU cloud`, `#AI infrastructure`, `#cloud benchmarking`, `#systems research`, `#SemiAnalysis`

---