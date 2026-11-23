---
layout: default
title: "Horizon Summary: 2026-11-23 (EN)"
date: 2026-11-23
lang: en
---

> From 28 items, 6 important content pieces were selected

---

1. [Baez Analyzes Masullo's Claimed Riemann Hypothesis Proof and Credit Dispute](#item-1) ⭐️ 8.0/10
2. [GL.iNet cloud flaw exploited to infect routers and KVM devices](#item-2) ⭐️ 8.0/10
3. [OpenAI Article Links Perplexity to Model Intelligence, Sparking Debate](#item-3) ⭐️ 8.0/10
4. [Tim O'Reilly argues Silicon Valley optimized for profit, not human flourishing](#item-4) ⭐️ 8.0/10
5. [Lean formalization progress map for Masullo's Riemann hypothesis proof draws scrutiny](#item-5) ⭐️ 8.0/10
6. [Z.ai Releases GLM-5.3-Flash: 320B Multimodal MoE with 18B Active Params at One-Tenth the Price](#item-6) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Baez Analyzes Masullo's Claimed Riemann Hypothesis Proof and Credit Dispute](https://johncarlosbaez.wordpress.com/2026/11/22/masullo-on-the-riemann-hypothesis/) ⭐️ 8.0/10

John Carlos Baez published a postmortem on Alessandro Masullo's proposed proof of the Generalized Riemann Hypothesis, examining the claim and the circumstances around AMS president Ravi Vakil's November 20, 2026 call for mathematicians to review it. Baez explicitly cautions that he is not a number theorist and that his analysis is tentative. A claimed proof of the Riemann Hypothesis or its generalization is one of the highest-stakes events in mathematics, so the case tests how the field handles verification, priority, and public announcement. It also intersects with a growing debate over whether AI-assisted Lean verification can confirm results without producing the conceptual insight that normally drives mathematics. Masullo's manuscript reportedly advances a trace formula in the tradition of Weil, Connes, and Meyer using functional analysis on GL1, and it is described as a human draft that received months of scrutiny from Brian Conrad; a separate Lean/Claude artifact reportedly landed the same day. Baez's caveat and the HN thread highlight that informal review, formal verification, and credit attribution are distinct problems.

hackernews · xiaoyu2006 · Nov 22, 10:59 · [Discussion](https://news.ycombinator.com/item?id=50598441)

**Background**: The Riemann Hypothesis asserts that all non-trivial zeros of the Riemann zeta function have real part 1/2; the Generalized Riemann Hypothesis extends similar zero-location statements to broader classes of L-functions. A proof would resolve a problem more than 150 years old with deep consequences for prime distribution. Lean is an interactive theorem prover whose compiler checks every step, so a Lean-verified proof is mechanically reliable once the statement and axioms are trusted; AI systems increasingly generate such formal proofs, but mathematicians still debate whether they yield understanding.

<details><summary>References</summary>
<ul>
<li><a href="https://www.arpaia.io/files/mathematics/riemann-hypothesis-masullo.pdf">Alessandro Masullo’s Proof of the Riemann Hypothesis</a></li>
<li><a href="https://explainx.ai/blog/alessandro-masullo-grh-human-proof-claimed-vs-verified-november-2026">Masullo GRH Draft: What Vakil Announced (Nov 20) - explainx.ai</a></li>
<li><a href="https://www.science.org/doi/10.1126/science.aej2213">Advancing mathematics research with AI-driven formal proof ...</a></li>

</ul>
</details>

**Discussion**: HN commenters expressed concern that Masullo's 12-year effort could be 'cheapened' by the dispute, while others argued that AI-driven brute-force verification produces little new mathematical insight. A third strand pushed back on the 'scooped' framing, insisting that if Masullo proved the result without AI, both he and Alpöge should receive credit rather than treating priority as a winner-take-all race.

**Tags**: `#mathematics`, `#Riemann-Hypothesis`, `#proof-verification`, `#research-culture`, `#AI-in-math`

---

<a id="item-2"></a>
## [GL.iNet cloud flaw exploited to infect routers and KVM devices](https://www.gl-inet.com/en-us/blogs/blog/glinet-security-notice-2026-11-20) ⭐️ 8.0/10

On November 20, 2026, GL.iNet disclosed a vulnerability in its cloud remote management services that an unauthorized party exploited to access and install malicious software on a subset of its routers and KVM devices. The vendor published a formal security notice on its website and forum, and the disclosure was subsequently reported by BleepingComputer. GL.iNet devices are popular among homelab users, travelers, and small businesses, and because the compromise came through the vendor's own cloud management channel, it exposes the systemic risk of cloud-connected networking gear that phones home by default. Anyone running an affected router or KVM over IP should assume possible compromise and audit their device. The notice states that only a subset of routers and KVM devices were affected via the cloud remote management service, but it does not clearly specify whether devices with cloud management disabled are safe, leaving users to infer that local-only operation avoids the attack path. Affected owners are advised to check GL.iNet's official notice and forum thread for remediation guidance and firmware updates.

hackernews · gregsadetsky · Nov 22, 23:06 · [Discussion](https://news.ycombinator.com/item?id=50604988)

**Background**: GL.iNet makes compact travel routers, home routers, and KVM-over-IP devices that ship with a customized version of OpenWrt firmware and integrate with the company's GoodCloud remote management platform, which lets users reach their devices from anywhere. Many of these devices are also well supported by upstream OpenWrt, so users can replace the vendor firmware entirely. Cloud-based remote management is convenient but expands the attack surface, since a flaw in the vendor's service can be used to push malicious code to every enrolled device.

<details><summary>References</summary>
<ul>
<li><a href="https://www.gl-inet.com/en-us/blogs/blog/glinet-security-notice-2026-11-20">GL.iNet Security Notice 2026-11-20</a></li>
<li><a href="https://forum.gl-inet.com/t/2026-11-20-gl-inet-security-notice-goodcloud-kvm-routers/73056">2026-11-20: GL.iNet Security Notice - GoodCloud / KVM / Routers</a></li>
<li><a href="https://www.bleepingcomputer.com/news/security/hackers-exploit-glinet-cloud-flaw-to-infect-routers-kvm-devices/">Hackers exploit GL.iNet cloud flaw to infect routers, KVM devices</a></li>

</ul>
</details>

**Discussion**: Commenters were sharply critical of cloud-connected appliances, with several urging users to flash OpenWrt or build a DIY router and to always disable cloud/remote access on such devices, drawing parallels to remote-access problems seen with Ubiquiti gear. One commenter linked a GL.iNet forum post suggesting the devices may have been compromised since at least the previous year, while another noted that OpenWrt support covers many GL.iNet routers but not the KVMs, which is particularly worrying.

**Tags**: `#security`, `#networking`, `#routers`, `#GL.iNet`, `#OpenWrt`

---

<a id="item-3"></a>
## [OpenAI Article Links Perplexity to Model Intelligence, Sparking Debate](https://openai.com/index/perplexity-and-intelligence/) ⭐️ 8.0/10

OpenAI published a new article, "Perplexity and Intelligence," examining how perplexity — the measure of how surprised a model is when predicting the next token — tracks with model capability. The piece generated heavy discussion on Hacker News (roughly 550 points and 373 comments), with readers noting an apparently clear trend line between log-perplexity and benchmark performance across recent models. If a single, cheap-to-compute pre-training metric like perplexity reliably predicts downstream capability, it could simplify a benchmark landscape that is increasingly fragmented and expensive to run. It also revives the classic information-theoretic argument that better prediction equals better compression, and better compression equals more intelligence — a claim that shapes how labs think about scaling and evaluation. Perplexity is bounded between 1 (perfect prediction, since it is the exponentiated cross-entropy) and the vocabulary size (a uniform random predictor), and the article reportedly plots log-perplexity against capability across model generations. The discussion highlighted the open question of whether reinforcement-learning-based post-training, which optimizes objectives other than cross-entropy, still leaves the pre-training trend intact.

hackernews · acossta · Nov 22, 17:06 · [Discussion](https://news.ycombinator.com/item?id=50601525)

**Background**: Perplexity is a standard information-theory metric for how well a probability model predicts a sample; in language modeling it is the exponentiated average cross-entropy per token, so lower values mean the model assigns higher probability to real text. It was the dominant yardstick in pre-Transformer and early LLM eras, but has been largely displaced in public reporting by task benchmarks such as MMLU or coding and math evaluations, partly because perplexity depends heavily on the tokenizer and the evaluation corpus. The compression-as-intelligence view traces back to figures like Jürgen Schmidhuber, who has argued that progress in prediction/compression of raw data streams underlies curiosity, creativity, and learning.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Perplexity">Perplexity - Wikipedia</a></li>
<li><a href="https://mbrenndoerfer.com/writing/perplexity-language-model-evaluation-metric">Perplexity : The Standard Language Model Metric - Interactive</a></li>
<li><a href="https://arxiv.org/abs/0812.4360">[0812.4360] Driven by Compression Progress: A Simple Principle...</a></li>

</ul>
</details>

**Discussion**: Commenters were largely enthusiastic but nitpicked the framing: one noted the article never actually defines perplexity and supplied the definition (1 at best, vocabulary size at worst), while another called the cross-entropy trend "shocking" given the shift toward RL-based training and welcomed a simple benchmark over increasingly convoluted ones. Others leaned on the compression argument — one cited a 2008 paper of their own making the same point — and one commenter claimed Microsoft's Mustafa Suleyman had posted that its MAI-2 Base model would be reported on OpenAI's held-out evaluation set, drawing skeptical and amused replies.

**Tags**: `#LLMs`, `#perplexity`, `#AI evaluation`, `#machine learning`, `#compression`

---

<a id="item-4"></a>
## [Tim O'Reilly argues Silicon Valley optimized for profit, not human flourishing](https://www.oreilly.com/radar/what-happened-to-silicon-valley/) ⭐️ 8.0/10

In a new essay on O'Reilly Radar titled "What Happened to Silicon Valley?", Tim O'Reilly argues the tech industry has shifted from a focus on human flourishing to optimizing for shareholder value, and calls for applying mechanism design—described as "reverse game theory"—to reprogram the incentive systems that shape technology. He frames the core question as "What game ought we to be playing?" rather than merely accepting the rules of the current one. The essay comes from one of the industry's most prominent publishing figures and lands as a substantive critique of how venture capital and shareholder-value incentives have shaped the products billions of people use. It resonates especially now, as AI-driven spending and consolidation raise questions about whether market incentives alone steer technology toward socially desirable outcomes. O'Reilly's proposal leans on mechanism design, the economics and game-theory field that asks how to construct rules producing good outcomes even when participants' private preferences are unknown—work recognized with the 2007 Nobel Prize in Economics and already used in ad auctions and internet routing. The key caveat is that the argument is a normative call to action rather than a concrete policy blueprint, and the essay's central idea appears near the end rather than up front.

hackernews · greenyouse · Nov 22, 19:20 · [Discussion](https://news.ycombinator.com/item?id=50602947)

**Background**: Mechanism design is sometimes called "reverse game theory": instead of analyzing the outcome of given rules, it starts from a desired outcome and works backwards to find rules that incentivize participants to produce it. It underpins much of the modern internet economy, from Google's and Facebook's ad auctions to inter-domain routing. O'Reilly's argument is that the tech industry's implicit "mechanism"—maximizing shareholder value and venture returns—was never deliberately chosen for human benefit, so it could be redesigned.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Mechanism_design">Mechanism design - Wikipedia</a></li>
<li><a href="https://www.web.stanford.edu/~jacksonm/mechtheo.pdf">Mechanism Theory - Stanford University</a></li>

</ul>
</details>

**Discussion**: Hacker News commenters largely agreed with O'Reilly, with several praising the buried mechanism-design framing as the essay's most valuable idea. Others pressed on proximate causes: one argued the zero-interest-rate era let companies grow to grotesque proportions and push startups into speculative "green fields," while another lamented that Wall Street types and self-serving "VC influencers" have eroded whatever integrity the Valley once had.

**Tags**: `#silicon-valley`, `#tech-industry`, `#mechanism-design`, `#capitalism`, `#venture-capital`

---

<a id="item-5"></a>
## [Lean formalization progress map for Masullo's Riemann hypothesis proof draws scrutiny](https://claude.ai/artifact/CtQyX8qfYAF822bgHJHHE3) ⭐️ 8.0/10

A public progress map tracking the Lean formalization of Alessandro Masullo's claimed proof of the Generalized Riemann Hypothesis sparked a heavily engaged Hacker News discussion (208 points, 157 comments). The repository, worked on by contributing mathematicians, also carries an errata list with hundreds of open issues, and commenters debated whether the project represents a genuine breakthrough or is chasing a proof with a fatal gap. The episode is a live test case for how formal verification and AI-assisted mathematics handle extraordinary claims: instead of waiting for peer review, the community is simultaneously mechanizing the argument and auditing it in public. It matters to anyone tracking Lean-based proof engineering, automated theorem proving, and how credibility of major results gets established in the open. A high percentage on the progress map does not imply the proof is largely correct, since a single unfilled gap can invalidate everything downstream; contributors explicitly cautioned that it is too early to tell whether the core idea has a big hole. Commenters also cited reporting that Ravi Vakil, who announced the work on Masullo's behalf, said he had not reviewed the document himself, that Brian Conrad called the manuscript in need of "major revision", and that Masullo has no other publications.

hackernews · Qision · Nov 22, 23:12 · [Discussion](https://news.ycombinator.com/item?id=50605045)

**Background**: Lean is an interactive theorem prover and dependently typed programming language in which mathematical statements and their proofs are written in code so a computer can check every step mechanically; it is also the system Google DeepMind used to build its AlphaProof math-reasoning system. The Riemann Hypothesis, and its generalization to the GRH, is one of the most famous open problems in mathematics, and Masullo's draft reportedly runs to roughly 940 pages. "Formalizing" such a proof means translating its arguments into Lean definitions and lemmas so that any gap becomes a compile error rather than a subtle oversight.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Lean_(proof_assistant)">Lean (proof assistant) - Wikipedia</a></li>
<li><a href="https://www.arpaia.io/files/mathematics/riemann-hypothesis-masullo.pdf">Alessandro Masullo's Proof of the Riemann Hypothesis</a></li>
<li><a href="https://xenospectrum.com/en/masullo-riemann-proof-draft-release/">Draft Proof of the Generalized Riemann Hypothesis, 12 Years ...</a></li>

</ul>
</details>

**Discussion**: One of the mathematicians contributing to the repository asked readers not to over-read the hundreds of errata items, saying some are minor and some are not, but that it is far too early to judge whether the core idea has a big hole. Others warned that the progress bar is not evidence of correctness, with one commenter arguing the machinery feels like a smaller step than another recent approach, while another expressed gloom that agentic LLM-based AI makes mathematics a less interesting place for smart, educated people.

**Tags**: `#formal-verification`, `#Lean`, `#mathematics`, `#Riemann-hypothesis`, `#AI-assisted-research`

---

<a id="item-6"></a>
## [Z.ai Releases GLM-5.3-Flash: 320B Multimodal MoE with 18B Active Params at One-Tenth the Price](https://t.me/zaihuapd/45309) ⭐️ 8.0/10

Z.ai released GLM-5.3-Flash, the first native multimodal model in its GLM-5 series, with 320B total parameters but only 18B active per token. The company claims it beats GLM-5.2 on multiple coding and agent benchmarks and comes close to Claude Opus 4.8, while cutting API prices to roughly one-tenth of the previous generation: a promotional $0.075 per million input tokens, $0.015 for cached input, $0.25 for output, and free cache storage for a limited time. The release combines a large sparse model with a steep price cut, which could make a capable multimodal agentic model affordable for high-volume coding and tool-use workloads that were previously priced out of reach. If the benchmark claims hold up under independent testing, it intensifies the price war among Chinese LLM providers and gives developers a cheaper alternative to Western frontier models. The 320B-total/18B-active split implies a Mixture-of-Experts architecture, so per-token compute cost tracks the 18B active path rather than the full model size. The pricing figures quoted are promotional rates with full prices to be restored later, and all performance claims so far come from Z.ai's own announcement with no published methodology or third-party verification.

telegram · zaihuapd · Nov 23, 04:47

**Background**: Mixture-of-Experts models keep a very large pool of parameters but route each token through only a small subset, so a 320B model can run at roughly the cost of an 18B dense one. 'Native multimodal' means the model was trained on text, images and other modalities together from the start in a unified architecture, rather than bolting a separate vision encoder onto an existing language model. Separately, most LLM APIs bill discounted 'cached input' tokens, since repeated prompt prefixes can be reused instead of recomputed, which is why providers list a separate cache-hit price.

<details><summary>References</summary>
<ul>
<li><a href="https://gate.ai/zh/blog/dense-model-vs.-moe-model-what-are-the-differences-in-model-architecture">Dense Model vs MoE Model： 模 型 架构有 什 么 区别？｜Gate.AI</a></li>
<li><a href="https://zhuanlan.zhihu.com/p/2036759233539077945">原生多模态模型技术全景 - 知乎 - 知乎专栏</a></li>
<li><a href="https://juejin.cn/post/7678132532524810240">DeepSeek 涨 价 了，你换了吗？— — 大 模 型 API ...</a></li>

</ul>
</details>

**Tags**: `#LLM`, `#GLM-5.3-Flash`, `#multimodal`, `#model release`, `#API pricing`

---