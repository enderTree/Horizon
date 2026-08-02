---
layout: default
title: "Horizon Summary: 2026-08-02 (EN)"
date: 2026-08-02
lang: en
---

> From 35 items, 6 important content pieces were selected

---

1. [OpenAI's Astra Model Claims Advances on Ten Long-Standing Math Problems](#item-1) ⭐️ 9.0/10
2. [NetBSD 11.0 Released with Firewall Enhancements and MicroVM Kernel](#item-2) ⭐️ 8.0/10
3. [KataGo Author Studies Symmetry in Go Network Internals](#item-3) ⭐️ 8.0/10
4. [VLMs pass radiology benchmarks while erasing clinical terms and adding bias](#item-4) ⭐️ 8.0/10
5. [Microsoft Confirms Plan to Launch Copilot 'Super App' This Year](#item-5) ⭐️ 8.0/10
6. [AI Chip Count Doubling Every 9 Months to Reach 200 Million by 2028](#item-6) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [OpenAI's Astra Model Claims Advances on Ten Long-Standing Math Problems](https://simonwillison.net/2026/Aug/1/ten-advances-in-mathematics/#atom-everything) ⭐️ 9.0/10

OpenAI announced that an internal version of its upcoming Astra model made progress on ten mathematics and theoretical computer science problems that had seen no major advance for at least a decade. The company says each solution cost less than $2,000 in tokens at GPT-5.6 Sol pricing, and it released Lean 4 formalizations plus a paper describing the results. This is a striking demonstration that frontier AI models can produce genuinely hard mathematical research at modest token costs, potentially accelerating discovery in fields that have been stuck for decades. It also intensifies the competitive race between OpenAI and Anthropic, and raises profound questions about the future role of humans in mathematics. OpenAI's post does not disclose how many problems were attempted without success, nor the prompts used. The results include Lean 4 formalizations in the openai/ten-proofs repository, a paper, and an LLM-generated walkthrough PDF; the tackled problems reportedly span high-dimensional sphere packing, non-Sofic groups, Connes rigidity, arithmetic circuit lower bounds, quantum parallel repetition, the closest vector problem, and multicolor Ramsey numbers.

rss · Simon Willison · Aug 1, 20:34

**Background**: The announcement follows Anthropic's recent claim that its Claude Mythos Preview model discovered cryptographic weaknesses, with token costs around $100,000 per finding. Lean 4 is an interactive theorem prover that can mechanically verify mathematical proofs, making OpenAI's release of formalizations a notable transparency measure. Terence Tao has described the shift toward 'big mathematics' — large-scale human-machine collaboration where AI handles much of the technical work. The news has sparked what some call a 'Deep Blue' moment among mathematicians, with essays like Kirwin Hampshire's 'The Dark Night of Mathematics' expressing anxiety about AI's implications.

<details><summary>References</summary>
<ul>
<li><a href="https://the-decoder.com/openai-announces-its-next-major-model-astra-by-dropping-ten-previously-unsolved-math-solutions/">OpenAI announces its "next major model" Astra by dropping ten previously unsolved math solutions</a></li>
<li><a href="https://openrouter.ai/openai/gpt-5.6-sol">GPT-5.6 Sol - API Pricing & Benchmarks | OpenRouter</a></li>
<li><a href="https://en.wikipedia.org/wiki/Claude_Mythos">Claude Mythos - Wikipedia</a></li>

</ul>
</details>

**Discussion**: Simon Willison praises the transparency but asks for the prompts, noting failures were not disclosed. The broader reaction online, per the post, is a mix of awe and existential anxiety among mathematicians — a 'Deep Blue' moment — with essays like Kirwin Hampshire's 'The Dark Night of Mathematics' highlighting the psychological impact.

**Tags**: `#AI`, `#mathematics`, `#theoretical computer science`, `#OpenAI`, `#research`

---

<a id="item-2"></a>
## [NetBSD 11.0 Released with Firewall Enhancements and MicroVM Kernel](https://blog.netbsd.org/tnf/entry/netbsd_11_0_released) ⭐️ 8.0/10

NetBSD 11.0 has been released, introducing major improvements to the npf firewall, a new fast-booting MICROVM kernel for x86, and various hardware enhancements. This major release demonstrates that the long-standing open-source NetBSD project remains actively developed and relevant. The new microVM kernel could enable new use cases in virtualization and edge computing. The release announcement notes that while there are open issues, the release resolves many more than it creates. NPF firewall improvements include layer 2 filtering and user/group filtering, and the MICROVM kernel for x86 can boot in about 10 milliseconds.

hackernews · jaypatelani · Aug 1, 17:56 · [Discussion](https://news.ycombinator.com/item?id=49136736)

**Background**: NetBSD is a free, open-source Unix-like operating system and part of the BSD family, known for its portability and clean design. NPF is NetBSD's packet filter, providing stateful inspection, NAT, and IP sets. A microVM is a lightweight virtual machine designed for fast boot and minimal overhead, commonly used in serverless and edge computing. The new MICROVM kernel takes advantage of this concept to boot in roughly 10 ms.

<details><summary>References</summary>
<ul>
<li><a href="https://www.koyeb.com/blog/what-is-a-microvm">What is a microVM ? - Koyeb</a></li>
<li><a href="https://northflank.com/blog/what-is-a-microvm">What is a microVM ? | Blog — Northflank</a></li>
<li><a href="https://rmind.github.io/npf/configuration.html">NPF : packet filter with stateful inspection, NAT, IP sets, etc.</a></li>

</ul>
</details>

**Discussion**: Commenters discuss the current status and relevance of the BSDs compared to Linux, with some praising the npf layer 2 and user/group filtering and the 10 ms boot time. One commenter notes the release announcement's candid tone about open issues, observing that the release likely closes more issues than it opens. Another shares a nostalgic story about using NetBSD for molecular dynamics simulations.

**Tags**: `#NetBSD`, `#BSD`, `#Operating System`, `#Release`, `#Open Source`

---

<a id="item-3"></a>
## [KataGo Author Studies Symmetry in Go Network Internals](https://www.reddit.com/r/MachineLearning/comments/1vcrki2/how_symmetric_are_the_insides_of_a_go_network_r/) ⭐️ 8.0/10

The author of KataGo published a new interpretability study examining whether superhuman Go-playing neural networks learn orientation-independent internal concepts or memorize information separately for each rotation and reflection. The study found unexpected results about how symmetry is handled in these networks. This work contributes to neural network interpretability, an area where the internal representations of deep models remain poorly understood. Insights could help researchers design better inductive biases for domains with known symmetries, such as vision, physics, and molecular modeling. The study analyzed KataGo, a strong open-source Go engine, whose networks are trained with stochastic 8-fold data augmentation rather than explicit symmetry constraints. Notably, the study and its writeup were heavily assisted by AI, though with detailed human direction and feedback, and the code is publicly linked from the article.

reddit · r/MachineLearning · /u/icosaplex · Aug 1, 16:18

**Background**: Go is a board game whose rules are completely invariant under rotation and reflection, but KataGo's neural networks do not enforce this symmetry architecturally; instead, training uses stochastic 8-fold data augmentation to randomly orient each training batch. This study explores how much a superhuman-strength network learns orientation-independent concepts from this indirect signal. KataGo is a top-tier open-source AI Go engine known for surpassing professional players.

<details><summary>References</summary>
<ul>
<li><a href="https://katagotraining.org/">KataGo Distributed Training</a></li>
<li><a href="https://geekpython.in/data-augmentation-in-deep-learning">An Intuitive Guide On Data Augmentation In Deep Learning ...</a></li>

</ul>
</details>

**Tags**: `#ML interpretability`, `#neural networks`, `#Go`, `#symmetry`, `#KataGo`

---

<a id="item-4"></a>
## [VLMs pass radiology benchmarks while erasing clinical terms and adding bias](https://www.reddit.com/r/MachineLearning/comments/1vcipzz/vlms_can_score_well_on_benchmarks_while_silently/) ⭐️ 8.0/10

This paper reveals that vision-language models (VLMs) for chest X-ray report generation can score well on benchmarks while silently erasing clinically meaningful rare terms and introducing biased terms. The authors propose a framework to measure these failures, called Clinical Association Displacement (CAD) and Weighted Association Erasure (WAE). Existing evaluation metrics for medical AI are flawed, so models that appear highly accurate may produce clinically useless or biased radiology reports. This has serious implications for the safe deployment of automated report generation in healthcare. The proposed framework, Clinical Association Displacement (CAD), is a vocabulary-level method that quantifies shifts in demographic-based word associations in generated reports, while Weighted Association Erasure (WAE) aggregates these shifts to measure clinical signal loss across demographics. The authors also note that benchmark metrics rewarded repetitive templates and “normal” reports that lacked clinical terminology.

reddit · r/MachineLearning · /u/ade17_in · Aug 1, 09:27

**Background**: A vision-language model (VLM) is a type of AI system that can jointly interpret images and text, enabling tasks such as generating radiology reports from chest X-rays. Radiology report generation (RRG) aims to reduce clinician workload, but evaluation is challenging because medical reports contain rare yet clinically critical terms. This paper highlights that standard benchmark metrics can be fooled by repetitive, vague language, hiding the loss of meaningful clinical information.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Vision-language_model_(VLM)">Vision-language model (VLM)</a></li>
<li><a href="https://pmc.ncbi.nlm.nih.gov/articles/PMC12292164/">Advancements in Radiology Report Generation : A Comprehensive...</a></li>
<li><a href="https://arxiv.org/html/2603.01625">Measuring What VLMs Don’t Say: Validation Metrics Hide Clinical ...</a></li>

</ul>
</details>

**Tags**: `#VLM`, `#Radiology Report Generation`, `#Evaluation Metrics`, `#Medical AI`, `#Bias`

---

<a id="item-5"></a>
## [Microsoft Confirms Plan to Launch Copilot 'Super App' This Year](https://www.theverge.com/tech/972927/microsoft-copilot-super-app-confirmed) ⭐️ 8.0/10

Microsoft CEO Satya Nadella confirmed on the company's earnings call that Microsoft will release an AI super app this year, combining Copilot chat, coding features, and agentic capabilities for both consumers and enterprises. The app will merge experiences including Copilot, GitHub Copilot, Copilot Cowork, and Autopilot systems. This confirms a major product direction for Microsoft, marking a shift from standalone AI assistants to a unified super-app strategy that could reshape how users access AI tools. It also intensifies competition with OpenAI, which recently launched a similar integrated app called ChatGPT Work. Nadella said Copilot is evolving from a chat tool to 'cowork' and 'autopilots,' with the company merging these experiences, including code features, into one app this quarter. Microsoft's last-quarter revenue grew to $90 billion, driven mainly by AI and cloud businesses.

telegram · zaihuapd · Aug 1, 13:18

**Background**: Copilot is Microsoft's family of AI assistants embedded across its products, while GitHub Copilot assists developers with code. Copilot Cowork is a newer capability that executes tasks on the user's behalf, such as sending emails, scheduling meetings, and managing the calendar, with enterprise-grade security. Autopilot refers to autonomous modes where AI agents complete multi-step tasks with limited supervision. These concepts reflect the broader industry trend toward agentic AI, where systems perceive, reason, and act on their own.

<details><summary>References</summary>
<ul>
<li><a href="https://learn.microsoft.com/en-us/microsoft-365/copilot/cowork/">Copilot Cowork overview | Microsoft Learn</a></li>
<li><a href="https://www.microsoft.com/en-us/microsoft-365/blog/2026/03/09/copilot-cowork-a-new-way-of-getting-work-done/">Copilot Cowork: A new way of getting work done | Microsoft 365 Blog</a></li>
<li><a href="https://mitsloan.mit.edu/ideas-made-to-matter/agentic-ai-explained">Agentic AI, explained | MIT Sloan</a></li>

</ul>
</details>

**Tags**: `#Microsoft`, `#Copilot`, `#AI`, `#Super App`, `#Agents`

---

<a id="item-6"></a>
## [AI Chip Count Doubling Every 9 Months to Reach 200 Million by 2028](https://www.nytimes.com/interactive/2026/07/29/technology/ai-chips-data-center-boom.html) ⭐️ 8.0/10

According to Epoch AI, the global AI chip count is roughly 20 million and is doubling every nine months, projecting about 200 million chips by the end of 2028. IDC forecasts global AI infrastructure investment will exceed $1 trillion by 2029, up from $318 billion last year. This explosive growth in AI compute underscores the dominant role of 'scaling laws' in AI progress and intensifies geopolitical competition, as the US controls roughly 80% of global AI compute. It also raises economic and environmental concerns about whether the massive investment can be sustained without leading to a bubble. The trend is driven by 'scaling laws'—the idea that more compute yields more capable AI. Google alone is believed to have four times as many AI chips as all Chinese companies combined, while China is aggressively pursuing self-developed semiconductors and AI infrastructure to close the gap.

telegram · zaihuapd · Aug 2, 01:01

**Background**: Neural scaling laws are empirical rules describing how AI performance improves as model parameters, training data, and compute increase. Epoch AI is a research institute that tracks AI development trends through comprehensive databases on training compute, model parameters, and hardware capabilities, and its forecasts are widely cited in debates about AI progress and infrastructure spending.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Neural_scaling_law">Neural scaling law - Wikipedia</a></li>
<li><a href="https://blogs.nvidia.com/blog/ai-scaling-laws/">How Scaling Laws Drive Smarter, More Powerful AI - NVIDIA Blog</a></li>
<li><a href="https://epoch.ai/about">About Us | Epoch AI</a></li>

</ul>
</details>

**Tags**: `#AI chips`, `#AI infrastructure`, `#scaling laws`, `#data centers`, `#investment trends`

---