---
layout: default
title: "Horizon Summary: 2026-10-16 (EN)"
date: 2026-10-16
lang: en
---

> From 39 items, 8 important content pieces were selected

---

1. [Citizen Lab: Targeted Ads Turned Into Zero-Click Spyware Pipeline](#item-1) ⭐️ 9.0/10
2. [Meta Releases Muse Spark Open, an 816B Open-Weight Model for Mac Studio](#item-2) ⭐️ 8.0/10
3. [Libreboot 26.10 'Ominous Olive' adds UEFI/EDK2 and Chromebook support](#item-3) ⭐️ 8.0/10
4. [Tesla Unveils New Roadster With Optional Rocket Thrusters](#item-4) ⭐️ 8.0/10
5. [Anthropic Tells Investors Q3 Revenue Hit $16.8B Ahead of IPO](#item-5) ⭐️ 8.0/10
6. [ASML Reportedly Developing a Hybrid Bonding Tool](#item-6) ⭐️ 8.0/10
7. [MIT/PNAS: Random Neuron Units Self-Assemble Learning Circuits Rivaling Backprop](#item-7) ⭐️ 8.0/10
8. [Apple's Foldable iPhone Duo Named to Time's 2026 Best Inventions](#item-8) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Citizen Lab: Targeted Ads Turned Into Zero-Click Spyware Pipeline](https://citizenlab.ca/research/how-discover-tech-turned-targeted-ads-into-a-pipeline-for-spyware/) ⭐️ 9.0/10

The Citizen Lab at the University of Toronto published research on an operation it calls "AdFection," in which a mercenary spyware vendor — reported by The Guardian and The Verge as the Israeli firm Discover Tech — abused global targeted-advertising infrastructure to hack specific individuals simply by serving them ads, with dozens of devices reportedly infected across multiple countries. The findings, covered the same day by WIRED, the Financial Times and TechCrunch, are the first publicly documented technical evidence of commercial spyware being distributed at scale through ad networks. This turns the adtech supply chain — an ecosystem almost every internet user passes through daily — into an indiscriminate attack surface, meaning victims no longer need to click, install, or visit anything suspicious to be compromised. It also raises hard accountability questions for ad exchanges, publishers and platforms that unknowingly carried the malicious impressions, and could accelerate regulatory scrutiny of both surveillance vendors and programmatic advertising. Community and press coverage note that the report details the distribution and command-and-control aspects thoroughly but stays vague on the core technical question of what actually triggered the malware execution in a "zero-click" fashion. The team behind it, Citizen Lab, is an interdisciplinary research lab at the Munk School of Global Affairs & Public Policy, University of Toronto, best known for exposing commercial spyware such as Pegasus.

hackernews · jcomp · Oct 15, 10:43 · [Discussion](https://news.ycombinator.com/item?id=50101813)

**Background**: Zero-click spyware infects a device without any action by the user — no link to tap and no attachment to open — which makes it far harder to detect or defend against and is typically reserved for high-value targets. "Mercenary spyware" refers to commercial surveillance tools built by private firms and sold to governments, and Apple even runs a threat-notification system to warn users individually targeted by such attacks. The exploitation here hinges on programmatic advertising, where ad calls are routed through a maze of brokers, exchanges and real-time bidding systems before reaching a user, giving attackers many places to inject a malicious payload.

<details><summary>References</summary>
<ul>
<li><a href="https://www.wired.com/story/nightmare-scenario-zero-click-spyware-is-infecting-phones-via-targeted-ads/">‘Nightmare Scenario’: Zero-Click Spyware Is Infecting Phones ...</a></li>
<li><a href="https://techcrunch.com/2026/10/15/citizen-lab-says-governments-are-abusing-online-ads-to-hack-people-with-zero-click-spyware/">Governments are hacking people with 'zero-click' spyware by ...</a></li>
<li><a href="https://en.wikipedia.org/wiki/Citizen_Lab">Citizen Lab</a></li>

</ul>
</details>

**Discussion**: An adtech engineer with 13 years in the industry pushed back, calling the report sensationalist and vague about the actual zero-click activation mechanism, and arguing there is no single "ad provider" to hold responsible in such a sprawling ecosystem. Other commenters focused on Israel's outsized role in the cyber-surveillance industry — one calling it a top-tier cyber power, another citing the historic Download Valley cluster — with several arguing such firms should be treated as extensions of state interests, while others simply linked to the original Citizen Lab report.

**Tags**: `#cybersecurity`, `#spyware`, `#adtech`, `#privacy`, `#zero-click-exploits`

---

<a id="item-2"></a>
## [Meta Releases Muse Spark Open, an 816B Open-Weight Model for Mac Studio](https://research.meta.ai/blog/muse-spark-open) ⭐️ 8.0/10

Meta released Muse Spark Open, an 816B-parameter open-weight model (listed on Hugging Face as Muse-Spark-Open-816B-A42B) that is explicitly optimized to run locally on Apple's Mac Studio. The release, announced in a Meta research blog post, quickly climbed to 673 points and 364 comments on the aggregator, making it one of the most discussed model drops of the week. The release extends Meta's strategy of publishing downloadable weights rather than gating capability behind an API, putting pressure on other open-weight players such as Qwen and GLM while trying to make Meta's model family the default local stack. It also matters because a model of this size running on consumer Apple hardware would lower the barrier for teams that want frontier-scale capability without datacenter GPUs or per-token API fees. The license permits broad use but contains a "Model as a Service" clause: if the licensee and its affiliates collectively earn more than twenty million dollars in aggregate gross revenue, they may not offer third-party access to the model's outputs via an API or similar interface. Meta has also invested heavily in runner support, with deployment documentation covering everything from Unsloth to MLX.

hackernews · bigwheels · Oct 15, 17:47 · [Discussion](https://news.ycombinator.com/item?id=50107379)

**Background**: Open-weight models are AI models whose trained parameters are published for anyone to download and run themselves, as opposed to closed models that are only reachable through a vendor's API; Meta popularized this approach with its Llama family. The "816B-A42B" naming follows the convention used for mixture-of-experts models, where a large total parameter count is paired with a much smaller number of parameters activated per token, which keeps inference cost manageable. Running a model this large locally is only realistic on machines with very large unified memory pools, which is why the Mac Studio — configurable with up to 512GB of unified memory and roughly 1.2TB/s of memory bandwidth in its latest M-series revisions — has become a popular target for local LLM work.

<details><summary>References</summary>
<ul>
<li><a href="https://www.aimodelwaddle.com/muse-spark">Muse Spark : Meta's Model Versions, Pricing, and Open -Weight Status</a></li>
<li><a href="https://openrouter.ai/meta/muse-spark-1.3">Muse Spark 1.3 - API Pricing & Benchmarks | OpenRouter</a></li>
<li><a href="https://toolhalla.ai/blog/best-local-llms-mac-studio-2026">Best Local LLMs for Mac Studio in 2026 | ToolHalla</a></li>

</ul>
</details>

**Discussion**: Sentiment was mixed: one commenter cited Artificial Analysis data showing the model underperforming Qwen3.8 Flash Next and GLM 5.3 Flash (both runnable on a single B300) and argued Meta has catching up to do in open weights, while also criticizing benchmarking that only compares models at the highest reasoning level. Others focused on licensing, with one user reading the terms and concluding commercial use is broadly permitted except for the Model-as-a-Service clause above $20M revenue, and another arguing Meta is repeating the Llama playbook to build a sticky ecosystem moat as the "rent market on intelligence" fails to materialize. Praise was also given for the breadth of runner support, and one commenter noted they could only test the model through OpenRouter.

**Tags**: `#AI`, `#LLM`, `#open-weight models`, `#Meta`, `#model release`

---

<a id="item-3"></a>
## [Libreboot 26.10 'Ominous Olive' adds UEFI/EDK2 and Chromebook support](https://libreboot.org/news/libreboot2610.html) ⭐️ 8.0/10

Libreboot 26.10, codenamed "Ominous Olive", has been released with integrated UEFI/EDK2 support and newly added Chromebook support, substantially widening the range of hardware the project can target. The release also formalizes a strict policy against LLM-assisted contributions, which became a major talking point in the community response. By adopting UEFI/EDK2 and Chromebook support, Libreboot multiplies the number of devices it can serve and makes adding future machines far easier, a change commenters describe as "huge" for the open-source firmware niche. It also strengthens the connection with related efforts such as the Heads project's ChromeOS ports, which build on similar upstream code. The UEFI support is built on EDK2, TianoCore's open-source reference implementation of UEFI, while the Chromebook work follows the approach used by MrChromebox's custom coreboot firmware for ChromeOS devices. The anti-LLM stance is documented in an AGENTS file in the project's lbmk repository on Codeberg, and community members note that a first ChromeOS port has already landed in the Heads project with more in progress.

hackernews · iamnothere · Oct 15, 12:52 · [Discussion](https://news.ycombinator.com/item?id=50102923)

**Background**: Libreboot is a free and open-source firmware project distributed as a coreboot distribution, in the same way Debian is a Linux distribution; it aims to replace proprietary BIOS or UEFI firmware on supported computers. coreboot is a lightweight open-source firmware that performs only the minimal hardware initialization needed before handing off to an operating system, and many Chromebooks already ship with Google's coreboot-based firmware. EDK2 (EFI Development Kit II) is the TianoCore community's open-source development environment and reference implementation of the UEFI specification, originally led by Intel, HP and Microsoft. Because Chromebooks and UEFI-based machines are so widespread, supporting both technologies is what allows a project like Libreboot to reach far more hardware.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Libreboot">Libreboot - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Coreboot">coreboot - Wikipedia</a></li>
<li><a href="https://tuxownia.pl/en/blog/hello-world-with-edk-ii-first-steps-with-uefi/">Hello World with EDK II - First Steps with UEFI - Tuxownia</a></li>

</ul>
</details>

**Discussion**: Commenters broadly agree the UEFI/EDK integration and Chromebook support are the real headline, with one calling it "huge" because it multiplies available devices and eases future ports. Views on the anti-LLM policy are split: one user finds it refreshing and argues LLM-assisted programming is unappealing, while another simply notes the project "doesn't seem to like AI". A Heads contributor confirms related ChromeOS porting work using MrChromebox's code, and an owner of Acer "Edgar" Chromebooks says he plans to test the release.

**Tags**: `#libreboot`, `#coreboot`, `#UEFI`, `#open-source-firmware`, `#chromebook`

---

<a id="item-4"></a>
## [Tesla Unveils New Roadster With Optional Rocket Thrusters](https://www.tesla.com/roadster) ⭐️ 8.0/10

Tesla unveiled a new-generation Roadster that offers an optional SpaceX rocket-thruster package and extreme performance claims, with the thrusters sold in two modes: a cold-gas (non-combusting) version for extra forward acceleration, and a combustion-rocket version shown in the demo video that is available by invitation only. The reveal sparked a 280-point, 311-comment Hacker News thread debating its engineering novelty and production plausibility. The announcement pushes a mainstream consumer vehicle toward spacecraft-grade propulsion, making it the clearest signal yet of how tightly Tesla's product roadmap is intertwining with SpaceX hardware and engineering culture. It also matters as a test of Tesla's credibility claims, since the company is promising revolutionary capabilities while still struggling with Cybertruck production and quality issues. The cold-gas thrusters reportedly fire directly against the chassis rather than routing force through the wheels, sidestepping the limits of tire-road grip, and SpaceX-style composite overwrapped pressure vessels (COPVs) would be the natural way to store the high-pressure gas. The combustion-rocket variant, being invite-only and shown only in a video, has no announced regulatory path, price, or delivery date.

hackernews · shekhar101 · Oct 16, 01:32 · [Discussion](https://news.ycombinator.com/item?id=50112657)

**Background**: The Roadster was Tesla's original 2008 sports car; a second-generation Roadster was announced in 2017 with promises of sub-2-second 0-60 mph acceleration and a 600-plus-mile range, but it has been repeatedly delayed. Cold gas thrusters are the simplest form of rocket engine, generating thrust by expelling pressurized inert gas through a nozzle with no combustion, and they are widely used on spacecraft such as SpaceX's Dragon capsule for attitude control and maneuvering. The community discussion implicitly assumes familiarity with Tesla's Cybertruck production troubles and with long-running speculation that Tesla and SpaceX could eventually merge.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Cold_gas_thruster">Cold gas thruster - Wikipedia</a></li>
<li><a href="https://www.techtimes.com/articles/327773/20260920/tesla-roadster-lands-oct-1-reveal-spacex-thrusters-bypass-tire-grip-physics.htm">Tesla Roadster Lands Oct 1 Reveal: SpaceX Thrusters Bypass...</a></li>

</ul>
</details>

**Discussion**: Hacker News commenters were genuinely impressed that the car "actually flies" and praised the cleaner aesthetic as what the Cybertruck should have looked like, but the dominant sentiment was skepticism about execution: one top comment warned that Cybertruck production problems mean reserving one would be foolish, arguing Tesla has "torched their engineering reputation" with a page full of revolutionary promises. Another commenter read the whole reveal as a precursor to Tesla being absorbed into SpaceX.

**Tags**: `#Tesla`, `#Roadster`, `#Electric Vehicles`, `#SpaceX`, `#Product Announcement`

---

<a id="item-5"></a>
## [Anthropic Tells Investors Q3 Revenue Hit $16.8B Ahead of IPO](https://simonwillison.net/2026/Oct/15/anthropic-tells-investors/) ⭐️ 8.0/10

Anthropic hosted investors on Wednesday and told them its quarterly revenue rose nearly 50% to $16.8bn in Q3 (July–September), up from $11.5bn in Q2 and about $4.8bn in Q1, as it prepares for an IPO. The company also disclosed that "distillation" accounted for 5% to 7% of its revenue but that it had cut that activity back "materially" in Q3. The disclosure offers a rare look at the economics of a frontier AI lab at IPO scale, showing steep quarter-over-quarter growth and a positive margin on compute spending. It also reveals that rival labs were paying Anthropic hundreds of millions of dollars to train on its model outputs — a revenue stream Anthropic is now deliberately shrinking, which will affect competitors who relied on it. Anthropic reported $1.70 in revenue for every $1 spent on computing power in Q3, with adjusted operating margins of 11% excluding stock-based compensation. Simon Willison's rough calculation suggests that if distillation was 5% of Q2 revenue, unnamed rival labs spent over half a billion dollars distilling Anthropic's models in that quarter; notably, Anthropic no longer appears to lean on "annualized run-rate revenue" in investor communications.

rss · Simon Willison · Oct 15, 13:04

**Background**: Anthropic is the AI lab behind the Claude family of models, and an IPO (initial public offering) would mean listing its shares on a public stock exchange. "Distillation" normally refers to model compression, where a smaller "student" model is trained to imitate the outputs of a larger "teacher" model, but here it means rival labs calling Anthropic's API at scale and training their own models on Claude's outputs. "Adjusted operating margin" is a profitability measure that strips out certain non-cash costs such as stock-based compensation, and "annualized run-rate revenue" is a common startup metric that multiplies a recent period's revenue to project a yearly figure.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Knowledge_distillation">Knowledge distillation - Wikipedia</a></li>
<li><a href="https://www.geeksforgeeks.org/nlp/what-is-llm-distillation/">What is LLM Distillation? - GeeksforGeeks</a></li>

</ul>
</details>

**Tags**: `#Anthropic`, `#AI industry`, `#IPO`, `#revenue`, `#distillation`

---

<a id="item-6"></a>
## [ASML Reportedly Developing a Hybrid Bonding Tool](https://newsletter.semianalysis.com/p/asml-is-building-a-hybrid-bonding) ⭐️ 8.0/10

SemiAnalysis reports that ASML is developing a hybrid bonding tool, based on the company's patent filings, a news report, and its own technology roadmap, even though ASML has made no official announcement. The disclosure points to a possible new product line for the Dutch lithography giant beyond its core scanners. Hybrid bonding is a cornerstone of advanced packaging and 3D chip stacking, an area where players like TSMC, Intel, and HBM memory makers are investing heavily as transistor scaling slows. If ASML enters this equipment market, it could reshape competition in advanced packaging tooling and tighten its already central role in the semiconductor supply chain. The evidence is indirect — patents, a news report, and ASML's roadmap — and the product has not been officially confirmed, so timing, specifications, and target customers remain unknown. Hybrid bonding is a demanding process in which alignment accuracy between bonded pads and vias directly affects performance and yield, making it a natural adjacency for a company with ASML's precision-lithography expertise.

rss · Semianalysis · Oct 15, 19:27

**Background**: Hybrid bonding is a technique that directly bonds two wafers or dies using both metal electrodes (typically copper pads) and an insulating dielectric, creating dense vertical electrical connections without solder bumps. It is a key enabler of advanced packaging, the set of fabrication-grade processes — such as 2.5D interposers, 3D ICs, chiplet integration, and wafer stacking — that combine multiple dies into one package to boost performance while sidestepping the rising cost and yield problems of ever-smaller monolithic nodes. ASML is best known for the extreme ultraviolet (EUV) lithography systems used to pattern the most advanced logic chips, and it has been expanding its portfolio into metrology and inspection.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Advanced_packaging_(semiconductors)">Advanced packaging (semiconductors)</a></li>
<li><a href="https://www.evgroup.com/">EV Group | Semiconductor Manufacturing Equipment and Process...</a></li>
<li><a href="https://aei.dempa.net/archives/25028">Toray Develops New Insulating Resin for Hybrid Bonding | AEI</a></li>

</ul>
</details>

**Tags**: `#ASML`, `#hybrid bonding`, `#semiconductor manufacturing`, `#advanced packaging`, `#lithography`

---

<a id="item-7"></a>
## [MIT/PNAS: Random Neuron Units Self-Assemble Learning Circuits Rivaling Backprop](https://www.reddit.com/r/MachineLearning/comments/1x6hmyg/how_artificial_neural_networks_build_their_own/) ⭐️ 8.0/10

An MIT report published on 13 October 2026 describes a PNAS paper (9 October 2026), "How Biological Synapses Self-Assemble Gradient Learning," showing that randomly interconnected neuron-like units governed by shared local plasticity rules can self-assemble into learning motifs capable of pattern recognition and image classification. The reported benchmarks find performance similar to the backpropagation-trained networks used in the comparison. The result reframes the debate over whether learning machinery must be explicitly designed versus emerging from simple local rules, and it offers a step toward biologically plausible alternatives to backpropagation. If replicated and extended, such self-assembling learning circuits could influence how researchers think about both neuroscience and the architectures used in AI. The authors explicitly caution that self-organisation does not establish that the brain uses this mechanism, and open questions remain about the stability of the motifs under different initial connectivity and about extending the approach beyond the demonstrated classification tasks. The motivation is biological plausibility rather than a claim to replace backpropagation in large-scale models.

reddit · r/MachineLearning · /u/Dorian182 · Oct 15, 10:01

**Background**: Backpropagation, the core algorithm behind most deep learning, is widely considered biologically implausible because it requires weight symmetry, a globally computed error signal, and separate forward and backward training phases. Local plasticity rules instead update synapses using only signals available at the synapse itself, which is closer to how biological neurons are thought to operate. Self-assembling neural networks are architectures that build their own computation graphs, in contrast to hand-designed fixed topologies — this paper combines the two ideas by letting local rules organize the learning circuitry itself.

<details><summary>References</summary>
<ul>
<li><a href="https://arxiv.org/pdf/2406.16062">Towards Biologically Plausible Computing</a></li>
<li><a href="https://arxiv.org/abs/2010.08262">[2010.08262] Local plasticity rules can learn deep ...</a></li>
<li><a href="https://arxiv.org/pdf/2406.09787">Evolving Self - Assembling Neural Networks : From Spontaneous...</a></li>

</ul>
</details>

**Tags**: `#neural-networks`, `#self-organization`, `#learning-rules`, `#biological-plausibility`, `#backpropagation`

---

<a id="item-8"></a>
## [Apple's Foldable iPhone Duo Named to Time's 2026 Best Inventions](https://time.com/collection/best-inventions/2026/apple-iphone-duo/) ⭐️ 8.0/10

Time magazine named Apple's first foldable iPhone, the Duo, to its 2026 Best Inventions list; the device starts at $1,999 and unfolds into a large-screen tablet, making it the biggest design change to the iPhone since 2007. The Duo marks Apple's long-awaited entry into the foldable market, a segment where rivals such as Samsung and Huawei have competed for years, and Time's recognition signals mainstream validation of the form factor at the high end of the market. The $1,999 starting price positions the Duo above most existing foldables and the current iPhone Pro lineup, and the launch event was presented by new CEO John Ternus, who took over from Tim Cook on September 1 and attributed a visible hand tremor during an on-stage interaction with streamer IShowSpeed to lack of sleep and excitement.

telegram · zaihuapd · Oct 16, 03:00

**Background**: Foldable phones use a hinged flexible display so a device can work as a normal phone when closed and as a larger tablet when opened; Samsung, Huawei and others have shipped such devices for years, but Apple had until now stayed out of the category. Time's Best Inventions list is an annual editorial selection of notable products and ideas, so inclusion is a marketing and prestige signal rather than an independent technical benchmark. Apple's CEO transition matters here too: Tim Cook led the company since 2011 and was the public face of every iPhone launch, so Ternus debuting the Duo marks the start of a new era for Apple's product presentations.

**Tags**: `#Apple`, `#foldable phone`, `#iPhone Duo`, `#Time Best Inventions`, `#consumer tech`

---