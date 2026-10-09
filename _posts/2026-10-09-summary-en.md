---
layout: default
title: "Horizon Summary: 2026-10-09 (EN)"
date: 2026-10-09
lang: en
---

> From 36 items, 5 important content pieces were selected

---

1. [OpenAI Withdraws Three Mathematical Results From Its Proof Repository](#item-1) ⭐️ 8.0/10
2. [SemiAnalysis: China's AI Safety Regime Prioritizes Speed Over Frontier Pacing](#item-2) ⭐️ 8.0/10
3. [OpenAI API adds GPT-6.1 Sol Ultrafast mode at 6x Standard pricing](#item-3) ⭐️ 8.0/10
4. [SpaceX to Acquire Nationwide US Low-Band Spectrum Licenses](#item-4) ⭐️ 8.0/10
5. [Anthropic Launches Free Vulnerability Scanning Service for Open Source](#item-5) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [OpenAI Withdraws Three Mathematical Results From Its Proof Repository](https://twitter.com/danintheory/status/2108065033070789090) ⭐️ 8.0/10

OpenAI's openai/math GitHub repository updated its history.md file to withdraw three previously published mathematical results, as noted in a widely shared social media post. The withdrawal concerns results that were part of a large batch of AI-generated mathematical claims, and it has triggered debate about how such proofs are validated. This is an early public test case for the trustworthiness of AI-generated mathematical research: if results published with fanfare can later be retracted, it casts doubt on how AI outputs are reviewed before being presented as breakthroughs. It affects mathematicians, AI labs, and anyone relying on AI-assisted discovery, and it strengthens the case for requiring machine-checkable proofs rather than natural-language arguments. Discussion around the retraction points out that OpenAI's collection of roughly 372 claimed breakthrough results only partially includes Lean certificates, meaning some proofs exist only in natural-language form and cannot be mechanically verified. Even formally verified proofs are not immune to problems, since a Lean development can compile while formalizing a statement different from what the author actually intended.

hackernews · sashank_1509 · Oct 8, 07:05 · [Discussion](https://news.ycombinator.com/item?id=50002650)

**Background**: Lean is an open-source proof assistant and functional programming language developed since 2013, based on the Calculus of Inductive Constructions and now supported by the Lean Focused Research Organization. It lets mathematicians write proofs that a computer checks line by line, which is a form of formal verification — mathematically proving that a system or statement meets a precise specification. AI systems that generate mathematics typically produce proofs in ordinary prose, which are far harder to verify automatically and can contain subtle logical gaps.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Lean_theorem_prover">Lean theorem prover</a></li>
<li><a href="https://en.wikipedia.org/wiki/Formal_verification">Formal verification</a></li>

</ul>
</details>

**Discussion**: Commenters were broadly skeptical: some questioned why Lean-verified and natural-language-only proofs were mixed together at all, and predicted that many fully AI-generated proofs will eventually fall apart, comparing the slow discovery of errors to the long-running uncertainty around the abc conjecture. Others framed the retraction as mathematics adopting software engineering habits of versioning and retraction, questioned whether a mathematician or another model caught the errors, doubted a separate claimed improvement over O(n log n) integer multiplication, and argued that any such release should be fully formalized.

**Tags**: `#AI-generated proofs`, `#formal verification`, `#Lean`, `#OpenAI`, `#research integrity`

---

<a id="item-2"></a>
## [SemiAnalysis: China's AI Safety Regime Prioritizes Speed Over Frontier Pacing](https://newsletter.semianalysis.com/p/beijing-will-not-pace-the-frontier) ⭐️ 8.0/10

SemiAnalysis published an analysis arguing that China's real approach to AI safety is speed-based rather than safety-based, even though Beijing formally recognizes frontier AI risks. The piece points to China's AI Safety Governance Framework 3.0, whose opening principles declare "promoting AI innovation and development as the first priority." The analysis reframes the global AI safety debate, in which Western labs such as Anthropic, OpenAI and Google have pushed "pacing the frontier" — slowing the development race just enough for evaluation and oversight to keep up. If China explicitly declines to pace, international coordination becomes far harder and other governments may feel pressured to match speed rather than safety. Framework 3.0 reportedly adds an agentic AI annex built around a 33-risk taxonomy covering the full agent lifecycle, from design and deployment through users, model, memory, tools and decommissioning. A caveat worth noting: only the teaser of the SemiAnalysis article is available here, so its full evidence base and methodology could not be verified.

rss · Semianalysis · Oct 8, 17:46

**Background**: "Pacing the frontier" is a concept associated with Anthropic CEO Dario Amodei and endorsed by OpenAI's Sam Altman, meaning safety mechanisms, regulatory capacity and independent evaluation should develop at the same pace as frontier AI capabilities — not halting progress, but slowing the maximum possible race. Frontier AI generally refers to the most capable and most expensive large-scale models at the edge of current capability, often defined through training-compute thresholds. China has periodically signaled interest in AI risk control — for example through Xi Jinping's remarks at the World AI Conference and its September initiative for a UN Global Dialogue on AI Governance — yet its domestic governance framework keeps innovation as the stated first priority.

<details><summary>References</summary>
<ul>
<li><a href="https://newsletter.semianalysis.com/p/beijing-will-not-pace-the-frontier?ref=taaft">Beijing Will Not Pace the Frontier: China ’s Speed-First AI Safety ...</a></li>
<li><a href="https://www.thefrontier.dev/articles/china-ai-safety-governance-framework-3-agentic-annex">China 's AI Safety Governance Framework 3.0 adds a 33-risk agent...</a></li>
<li><a href="https://pwonlyias.com/current-affairs/ai-safety-frontier-ai-regulation-strategic-autonomy/">AI Safety : Pacing Frontier AI , Regulation & Strategic Autonomy</a></li>

</ul>
</details>

**Tags**: `#AI safety`, `#China`, `#AI policy`, `#regulation`, `#geopolitics`

---

<a id="item-3"></a>
## [OpenAI API adds GPT-6.1 Sol Ultrafast mode at 6x Standard pricing](https://developers.openai.com/api/docs/changelog) ⭐️ 8.0/10

OpenAI has added an Ultrafast service tier for the GPT-6.1 Sol model in its Responses API (v1/responses), described as the fastest tier available there, delivering up to roughly 8x the generation speed of Standard. The tier is available to all API users and is priced at 6x Standard: about $12 per million input tokens, $0.60 per million cached input tokens, and $60 per million output tokens for short contexts, per Tibo's day-4 post in a 28-day update streak. Speed-tiered pricing gives developers a direct trade-off between latency and cost, which matters most for real-time and agentic workloads where response time is the bottleneck rather than raw model quality. It also reinforces a broader industry pattern in which frontier labs sell premium "fast lanes" on top of their flagship models, reshaping how teams budget for high-throughput AI infrastructure. The roughly 8x speedup comes at exactly 6x Standard pricing, so the cost-per-second saved only pays off for latency-critical workloads, and the quoted $12/$0.60/$60 per-million-token rates apply specifically to short contexts. Ultrafast is not new to OpenAI — an earlier preview ran GPT-5.6 Sol at up to 14x standard speed on Cerebras hardware — so this announcement extends the tier to the newer GPT-6.1 Sol model rather than introducing the concept.

telegram · zaihuapd · Oct 9, 00:00

**Background**: The Responses API is OpenAI's developer interface, released on March 11, 2025, that combines the simplicity of the older Chat Completions API with built-in tool-calling for building agentic applications. GPT-6.1 is a family of large language models from OpenAI consisting of GPT-6.1 Sol and Astra, with GPT-6.1 Sol released on September 29, 2026. "Ultrafast" is the name OpenAI uses for a premium, low-latency service tier that serves a model much faster than its default Standard tier, at a proportionally higher token price.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/GPT-6.1_Sol">GPT-6.1 Sol</a></li>
<li><a href="https://openai.com/index/previewing-ultrafast/">Previewing Ultrafast mode : GPT-5.6 Sol at up to 14X the... | OpenAI</a></li>
<li><a href="https://grokipedia.com/page/OpenAI_Responses_API">OpenAI Responses API</a></li>

</ul>
</details>

**Tags**: `#OpenAI`, `#API`, `#GPT-6.1`, `#Ultrafast`, `#Pricing`

---

<a id="item-4"></a>
## [SpaceX to Acquire Nationwide US Low-Band Spectrum Licenses](https://x.com/SpaceX/status/2108291133025698301) ⭐️ 8.0/10

SpaceX announced an agreement to acquire a nationwide package of low-band spectrum licenses in the United States, stating that combining this spectrum with its Gen2 constellation would let Starlink Mobile deliver high-speed mobile broadband to Americans no matter where they are. The announcement was made through a short post on X and did not disclose the seller, price, or other deal terms. If completed, the deal would make SpaceX the first major US operator to vertically integrate satellite constellations with terrestrial low-band spectrum, turning Starlink from a partner of carriers into a direct competitor of T-Mobile, AT&T, and Verizon. It signals a broader convergence of satellite and cellular networks, and would put pressure on existing carriers' rural coverage and roaming business models. Low-band spectrum offers wide coverage and good building penetration but limited capacity, so it is typically used for broad coverage rather than high-speed density; any license transfer would still require FCC approval. For comparison, Starlink Mobile today runs on roughly 650 satellites and is available in the US only through T-Mobile's T-Satellite service at roughly 4 Mbps, while the FCC has approved a 15,000-satellite Gen2 mobile constellation that SpaceX says can reach up to 150 Mbps per user.

telegram · zaihuapd · Oct 9, 01:04

**Background**: Low-band spectrum generally refers to frequencies below about 1 GHz, such as the 600 MHz and 700 MHz bands; these airwaves travel far and penetrate walls well, which is why they are prized for nationwide coverage — T-Mobile became the largest bidder in the FCC's 2017 600 MHz incentive auction and used those licenses to build out its 5G network. Starlink is SpaceX's low-Earth-orbit satellite internet service, and 'Gen2' refers to its next-generation constellation, which the FCC has approved at up to 15,000 satellites with direct-to-phone capability. Starlink Mobile (direct-to-cell) currently works only in partnership with a terrestrial carrier's spectrum, so owning its own nationwide low-band licenses would free SpaceX from depending on a partner carrier.

<details><summary>References</summary>
<ul>
<li><a href="https://www.notebookcheck.net/FCC-approves-SpaceX-s-15-000-satellite-Starlink-Mobile-constellation-promising-150Mbps-to-phones.1417902.0.html">FCC approves SpaceX’s 15,000-satellite Starlink Mobile constellation ...</a></li>
<li><a href="https://en.wikipedia.org/wiki/Spectrum_auction">Spectrum auction - Wikipedia</a></li>
<li><a href="https://www.tigerdroppings.com/rant/o-t-lounge/starlink-to-become-a-major-mobile-carrier-in-the-us/125153368/">Starlink to become a major mobile carrier in the US | O-T Lounge</a></li>

</ul>
</details>

**Tags**: `#SpaceX`, `#Starlink`, `#spectrum`, `#telecom`, `#satellite-internet`

---

<a id="item-5"></a>
## [Anthropic Launches Free Vulnerability Scanning Service for Open Source](https://www.anthropic.com/research/launching-opt-in-vuln-finding-service-for-open-source) ⭐️ 8.0/10

Anthropic has launched OSS Scanner, an opt-in service that provides eligible open-source projects with free vulnerability reports generated by Claude and other models, covering reproduction steps, explanations, and patch suggestions where possible. The company says that over the past six months it surfaced more than 29,000 candidate vulnerabilities, of which roughly 6,000 were manually reviewed, and that 85 of 97 high- or critical-severity issues found in early testing met the bar for its disclosure process. Open-source dependencies underpin nearly every commercial software stack, yet most projects have no dedicated security budget or staff, so AI-generated vulnerability hunting at this scale could meaningfully reduce supply-chain risk. It also signals that frontier AI labs are moving from publishing model-safety research toward operating concrete security services embedded in real developer workflows. Anthropic explicitly notes that the reports are generated by models without human review and may therefore contain errors, so findings should be treated as leads rather than confirmed vulnerabilities. Access is gated by eligibility, and core maintainers of qualifying projects must apply by submitting a GitHub pull request.

telegram · zaihuapd · Oct 9, 02:00

**Background**: Open-source software is typically maintained by volunteers, and a single flaw in a widely used library can propagate to thousands of downstream applications — the dynamic behind high-profile incidents such as Log4Shell. Vulnerability scanning traditionally relies on static analysis and human security researchers, both of which are expensive and hard to scale across the millions of public repositories. Large language models can read code in context and reason about logic flaws, making them a promising complement to conventional scanners, though their tendency to produce plausible-but-wrong findings remains a central concern.

<details><summary>References</summary>
<ul>
<li><a href="https://cycode.com/blog/ai-vulnerability-scanner/">What Is an AI Vulnerability Scanner ? | Cycode</a></li>
<li><a href="https://futureagi.com/glossary/vulnerability-scanning-in-ai/">What Is AI Vulnerability Scanning ? FutureAGI Guide (2026)</a></li>

</ul>
</details>

**Tags**: `#Anthropic`, `#开源安全`, `#漏洞扫描`, `#AI for Security`, `#供应链安全`

---