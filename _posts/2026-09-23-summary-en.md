---
layout: default
title: "Horizon Summary: 2026-09-23 (EN)"
date: 2026-09-23
lang: en
---

> From 43 items, 11 important content pieces were selected

---

1. [OpenAI Launches GPT-6 Sol and Luna Frontier Models](#item-1) ⭐️ 10.0/10
2. [Anthropic Ships Claude Opus 5.5 With Cheaper API Pricing](#item-2) ⭐️ 9.0/10
3. [Pentagon: AI Overreliance Contributed to Iran School Missile Strike](#item-3) ⭐️ 9.0/10
4. [vLLM v0.30.0 ships 762 commits, new models and a persistent weight cache](#item-4) ⭐️ 8.0/10
5. [Hackers claim they stole data on all FBI employees](#item-5) ⭐️ 8.0/10
6. [Trail of Bits Calls SAML 'a Fractal of Bad Design'](#item-6) ⭐️ 8.0/10
7. [WordPress patches unauthenticated path traversal enabling conditional RCE](#item-7) ⭐️ 8.0/10
8. [Claude Opus 5.5 and GPT-6 Sol/Luna land as frontier model price war heats up](#item-8) ⭐️ 8.0/10
9. [DeepSeek and Tsinghua release DSec sandbox platform serving 3M sandboxes daily](#item-9) ⭐️ 8.0/10
10. [China Probes DeepSeek and Moonshot Over Alleged Claude Data Leaks](#item-10) ⭐️ 8.0/10
11. [OpenAI Begins Limited Preview of GPT-5.6 Family: Sol, Terra, Luna](#item-11) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [OpenAI Launches GPT-6 Sol and Luna Frontier Models](https://openai.com/index/introducing-gpt-6-sol-and-luna/) ⭐️ 10.0/10

OpenAI announced GPT-6 Sol and Luna, two new models trained with similar methods to GPT-6 Astra, with Sol aimed at complex tasks such as coding and Luna positioned for high-volume, clearly scoped work like summarizing documents, extracting information, and answering quick questions. OpenAI says the pair brings Astra's advances in professional work, factuality, coding, computer use, and alignment to faster, more affordable models. By pushing near-frontier capability into cheaper, faster tiers, OpenAI lowers the cost of running agentic and high-volume workloads, which directly affects how developers and companies choose between competing AI platforms. The release also intensifies price and plan-limit competition with rivals such as Anthropic's Claude, an issue the Hacker News thread debated at length. TechCrunch reports OpenAI is claiming both lower cost and fewer mistakes, and community testing notes that GPT-6 Luna is priced at roughly half the cost of GPT-5.6 Luna, making the price cut one of the headline changes. The two models continue the tiered naming scheme OpenAI introduced with GPT-5.6, where developers route different task types to different capability-and-cost tiers.

hackernews · OfficialTurkey · Sep 22, 18:00 · [Discussion](https://news.ycombinator.com/item?id=49805509)

**Background**: Frontier models are the most advanced AI models available at any given moment, trained on massive datasets to deliver state-of-the-art performance in reasoning, generation, and agentic workflows; they are what defines the leading edge of AI capability. GPT-6 Astra was OpenAI's previous generation of frontier intelligence, and Sol and Luna are built with the same training methods to distribute that intelligence more cheaply. Since the GPT-5.6 generation, OpenAI has used a tiered naming convention (Sol, Terra, Luna) so that applications can route simple classification to a cheap tier and complex analysis to a stronger one within the same system.

<details><summary>References</summary>
<ul>
<li><a href="https://techcrunch.com/2026/09/22/openai-launches-gpt-6-sol-and-luna/">OpenAI launches GPT-6 Sol and Luna, boasting lower cost and fewer mistakes | TechCrunch</a></li>
<li><a href="https://openai.com/index/introducing-gpt-6-sol-and-luna/">Introducing GPT-6 Sol and Luna | OpenAI</a></li>
<li><a href="https://www.mindstudio.ai/blog/what-is-gpt-5-6-sol-terra-luna-explained">What Is GPT-5.6? OpenAI's Sol, Terra, and Luna Model Tiers Explained | MindStudio</a></li>

</ul>
</details>

**Discussion**: The Hacker News thread (1294 points, 646 comments) is broadly enthusiastic but focused on economics and workflow fit: Simon Willison calls Luna costing half as much as GPT-5.6 Luna a really big deal, while m_fayer describes an unusual emotional attachment to 5.6 Sol and worries a technically better successor may feel less natural to work with. Others compare plan value directly, with jeffnash favoring Codex Pro 20x over Claude Code 20x on usage limits, and leokennis arguing that for average users ChatGPT Plus has felt effectively limitless since 5.6.

**Tags**: `#OpenAI`, `#GPT-6`, `#LLM release`, `#AI models`, `#Hacker News`

---

<a id="item-2"></a>
## [Anthropic Ships Claude Opus 5.5 With Cheaper API Pricing](https://www.anthropic.com/claude-opus-5-5) ⭐️ 9.0/10

Anthropic released Claude Opus 5.5, described as its strongest Opus model yet, with a stated focus on more natural communication and better support for long-running agentic and coding work. Alongside the launch, API prices dropped across the board: input tokens fell from $5 to $4 per million and output tokens from $25 to $20, with cache reads dropping from $0.50 to $0.20 and cache writes from $6.25 to $5. Pricing is a central competitive battleground for frontier labs, and a cut of this size on Anthropic's flagship-tier model directly pressures rivals and makes agentic, long-session workloads cheaper to run. The release also lands right after Anthropic publicly called for 'pacing the frontier,' so shipping a new flagship immediately afterward has reignited debate about how serious that commitment is. Anthropic says early testers found Opus 5.5's writing clearer and easier to follow, putting the most important information up front, which it frames as both a usability and a safety benefit for checking long agentic runs. The price reductions apply to all four billing categories (cache reads, input, output, cache writes) rather than just headline input/output rates.

hackernews · km144 · Sep 22, 16:29 · [Discussion](https://news.ycombinator.com/item?id=49803892)

**Background**: A 'frontier model' is a large language model at or near the leading edge of general-purpose capability for its release window — typically the largest and most expensive models from the handful of labs that can afford to train them. Anthropic's Claude family is tiered by capability and cost: Opus is the top tier, Sonnet the mid tier, and Haiku the fastest and cheapest tier. API pricing for these models is quoted per million tokens, and prompt caching — which lets repeated context be stored and reused — is billed separately for cache writes and cache reads.

<details><summary>References</summary>
<ul>
<li><a href="https://www.anthropic.com/claude/opus">Claude Opus \ Anthropic</a></li>
<li><a href="https://claude.com/blog/claude-models-explained-choosing-the-best-model-for-your-use-case">Claude models explained: choosing the best model for your use ...</a></li>
<li><a href="https://www.levellers.ai/what-is/frontier-model">What is a frontier model ? Clear business guide | Levellers. ai</a></li>

</ul>
</details>

**Discussion**: Hacker News reaction was large and mixed: many celebrated the price cut as long overdue, noting the OpenRouter data point that Opus 5 was the highest-spend model there, while others mocked the release's opening line about pacing the frontier as a reminder that Anthropic was plainly not pacing anything. Some developers said they were content with cheaper alternatives such as DeepSeek, citing its aggressive tool use and low cost, and others highlighted the described improvements in communication quality.

**Tags**: `#AI/ML`, `#Anthropic`, `#Claude`, `#LLM Release`, `#Pricing`

---

<a id="item-3"></a>
## [Pentagon: AI Overreliance Contributed to Iran School Missile Strike](https://www.bloomberg.com/graphics/2026-iran-school-attack/) ⭐️ 9.0/10

The Pentagon concluded that overreliance on an AI targeting system contributed to a deadly missile strike on a school in Minab, Iran, according to a Bloomberg investigation. Its report found the U.S. "failed in its obligation to do everything feasible to verify" that the school was a military objective and that the failure "went beyond mere negligence." This is one of the first public acknowledgments by a major military power that an AI-assisted targeting pipeline contributed to civilian deaths, setting a precedent for accountability debates under international humanitarian law. It is likely to intensify scrutiny of military AI procurement, kill-chain automation, and the legal responsibility for machine-recommended targets. The Minab site had been cataloged as an Islamic Revolutionary Guard Corps facility due to outdated data, was fed into the Maven system alongside other candidates, and emerged as a recommended day-one target, compressing target-list work that once took hours into minutes. A related incident saw the U.S. nearly board a Chinese vessel that AI incorrectly flagged as carrying nuclear-weapons material.

hackernews · devonnull · Sep 22, 19:03 · [Discussion](https://news.ycombinator.com/item?id=49806430)

**Background**: Project Maven is a U.S. Department of Defense program that applies machine learning to drone imagery and intelligence data to help generate and rank targets. Such automated recommendation systems can speed up the "kill chain," but their output is only as reliable as the underlying data and the human review layered on top. Under international humanitarian law, militaries must verify that a target is a legitimate military objective and take feasible precautions to protect civilians, obligations that become harder to satisfy when recommendations are produced at machine speed.

**Discussion**: Commenters largely pushed back on framing AI itself as the culprit, with one noting the report describes human command recklessness that "went beyond mere negligence," and another arguing the real problem is that the pipeline "optimizes the wrong metric." Others drew parallels to Israel's reported use of AI to target Hamas operatives, questioned why any state would deploy such tools, and cited the near-boarding of a Chinese vessel flagged by faulty AI as further evidence of systemic risk.

**Tags**: `#AI ethics`, `#military AI`, `#automated targeting`, `#accountability`, `#Pentagon`

---

<a id="item-4"></a>
## [vLLM v0.30.0 ships 762 commits, new models and a persistent weight cache](https://github.com/vllm-project/vllm/releases/tag/v0.30.0) ⭐️ 8.0/10

The vLLM project released v0.30.0, a major version built from 762 commits by 315 contributors (104 of them first-timers), adding support for models such as DeepSeek-V4.1-Flash, DeepSeek-V4-Flash-Vision-Exp, GLM-5.3-Flash, K2-Horizon, Cohere Compass, Bailing V3 VL and Nanbeige4.2. The release also introduces a "Fast Start" feature, a persistent per-GPU weight-cache daemon that keeps post-quantized, tensor-parallel-sharded weights in GPU memory so restarted engines map them over CUDA IPC with `--load-format ipc_cache` instead of reloading from disk. vLLM is one of the most widely used open-source LLM inference and serving engines, so its releases directly shape how organizations deploy and scale models in production. Fast Start in particular targets one of the most painful operational costs of large-scale serving — the minutes-long engine restart and re-quantization cycle — and the breadth of new model integrations means operators can adopt newer architectures without waiting for third-party forks. Fast Start now covers FP4 checkpoints and multi-node tensor parallelism, and other highlights include Gumbel-max watermarking with per-request opt-out and dual-key support for speculative decoding, a HiSparse host-resident tier that spills sparse-MLA KV pages to pinned host memory under GPU pressure, "Model Runner V2" with dual-batch overlap, MTP/EAGLE3 speculative decoding under pipeline parallelism and a graph-capture optimization that cut engine init on H200 from 28.9s to 8.2s. The release also adds targeted online quantization via `quantization_config.targets`, W4A16 DSA with an `nvfp4_fp8_ds_mla` KV cache, and makes FlashInfer CuTeDSL NVFP4 W4A16 the default over Marlin on SM100/103.

github · khluu · Sep 22, 05:20

**Background**: vLLM is an open-source library for high-throughput serving and inference of large language models; it has become a de facto standard component in AI infrastructure stacks, used both for online API serving and for offline batch and reinforcement-learning rollouts. The release notes reference low-precision numeric formats such as MXFP8 and NVFP4 (block-scaled float formats that shrink memory footprint and speed up matrix multiplication on modern GPUs), DeepSeek's FlashMLA attention kernels and DeepGEMM tensor-core kernel library, tensor parallelism (TP, splitting a model across GPUs) and speculative decoding (using a small draft model to propose tokens that a larger model verifies). Because these layers change quickly, a single release coordinating new models, kernels and serving features is the main channel through which practitioners adopt them.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/deepseek-ai/FlashMLA">GitHub - deepseek-ai/ FlashMLA : FlashMLA : Efficient Multi-head...</a></li>
<li><a href="https://github.com/deepseek-ai/DeepGEMM">GitHub - deepseek-ai/DeepGEMM: DeepGEMM: clean and efficient BLAS kernel library on GPU · GitHub</a></li>
<li><a href="https://en.wikipedia.org/wiki/MXFP8">MXFP8</a></li>

</ul>
</details>

**Tags**: `#vLLM`, `#LLM inference`, `#release`, `#model serving`, `#AI infrastructure`

---

<a id="item-5"></a>
## [Hackers claim they stole data on all FBI employees](https://www.404media.co/we-hacked-the-fbi-hackers-say-they-have-data-on-all-fbi-employees/) ⭐️ 8.0/10

A hacking group behind the message "We hacked the FBI" claims to have exfiltrated data covering all FBI employees, a claim reported by 404 Media and not yet independently verified. A representative for the group told the outlet that what they plan is "not something I'd call extortion, maybe coercion," adding that the operation is "not financially motivated." If the claim holds up, it would mean the personal and contact details of an entire national law-enforcement workforce are in the hands of criminals or possibly a state actor, creating serious counterintelligence and harassment risks for agents and staff. It also reinforces a growing industry assumption that even well-resourced government agencies cannot fully prevent large-scale data theft, shifting focus from prevention alone to detection, containment and victim protection. The report offers no technical evidence of the breach and, in the excerpt available, no confirmation from the FBI or independently verified sample data, so the claim should be treated as unconfirmed. The scale implied is significant — one commenter notes that exfiltrating multiple terabytes would normally take days to weeks and should trigger sysadmin alarms — yet no timeline, data volume or intrusion vector is specified in the material provided.

hackernews · spenvo · Sep 22, 17:46 · [Discussion](https://news.ycombinator.com/item?id=49805278)

**Background**: 404 Media is an independent technology-journalism outlet that frequently reports on hacking groups and the cybercrime economy. The discussion references ShinyHunters, the name of a well-known data-theft and extortion crew that has previously leaked databases from major companies, though the news item itself does not confirm the group's identity. "Exfiltration" means copying data out of a network rather than just breaking in, and modern extortion groups often skip traditional ransomware encryption in favor of threatening to publish or sell stolen records. Commenters also point to the 2015 breach of the U.S. Office of Personnel Management, which exposed records on roughly 22 million current and former federal employees, as precedent for how damaging such leaks can be.

**Discussion**: Sentiment on Hacker News was a mix of technical concern, skepticism and dark humor. Several commenters questioned how terabytes of data could leave a network unnoticed and asked why sysadmins wouldn't be alerted, while others took a cynical view that no large database is safe anymore and cited the OPM breach as proof. Others greeted the news with jokes — a Battlestar Galactica reference about unnetworked ships, and a satire of the group's non-financial "coercion" framing.

**Tags**: `#cybersecurity`, `#data breach`, `#FBI`, `#hacking`, `#privacy`

---

<a id="item-6"></a>
## [Trail of Bits Calls SAML 'a Fractal of Bad Design'](https://blog.trailofbits.com/2026/09/21/saml-a-fractal-of-bad-design/) ⭐️ 8.0/10

Trail of Bits published a blog post on September 21, 2026 titled "SAML: A fractal of bad design," arguing that the SAML authentication protocol suffers from deep, structural design flaws rather than isolated bugs. The post drew a substantial Hacker News discussion with 184 points and 106 comments dissecting canonicalization failures, XML signature vulnerabilities, and alternatives. SAML remains the backbone of enterprise single sign-on, so a rigorous critique from a well-known security firm reinforces the long-running argument that the industry should migrate toward OIDC and other modern authentication protocols. For defenders, it highlights that vulnerabilities in SAML deployments often stem from the protocol's inherent complexity rather than sloppy implementation alone. The critique centers on XML canonicalization — the fragile process of producing a byte-exact representation of XML before signing or verifying it — and on classes of attacks such as XML signature wrapping, where an attacker exploits XML's structural flexibility to have a valid signature validate while the application processes a different, unauthenticated element. Community members also recalled that the main C implementation of XML signature once defaulted to also accepting HMAC signatures from attacker-controlled documents or signatures chained to Web PKI, making forged assertions trivially valid.

hackernews · aray07 · Sep 22, 18:57 · [Discussion](https://news.ycombinator.com/item?id=49806335)

**Background**: SAML 2.0 (Security Assertion Markup Language) is an XML-based standard for exchanging authentication and authorization data between an identity provider (IdP) and a service provider (SP), and it is how most enterprise single sign-on works today. Because SAML messages are XML, their integrity is protected with XML Signature, a specification that first canonicalizes the element, hashes it, and then signs it — a chain with many implementation-sensitive steps. XML can represent the same information in many equivalent serializations, so canonicalization was introduced to make signatures reproducible, but it also created a large attack surface that XML signature wrapping attacks exploit by moving the signed element elsewhere in the document.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/SAML">SAML - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/SAML_2.0">SAML 2.0 - Wikipedia</a></li>
<li><a href="https://www.ibm.com/think/topics/xml-signature-wrapping">What is XML Signature Wrapping? | IBM</a></li>

</ul>
</details>

**Discussion**: Commenters largely agreed with the critique but split on remedies: one argued that protocols should be designed so canonicalization is unnecessary — validate the signature over the exact received blob, then decode — while another shared horror stories of the C XML signature library accepting HMAC passwords and Web PKI keys from attacker-controlled documents. A few pushed back on the OIDC triumphalism, noting SAML still uniquely supports IdP-initiated flows and has a more stable commonly-implemented subset, so vendors selling to enterprises should support both.

**Tags**: `#SAML`, `#security`, `#authentication`, `#XML`, `#protocol-design`

---

<a id="item-7"></a>
## [WordPress patches unauthenticated path traversal enabling conditional RCE](https://github.com/WordPress/wordpress-develop/security/advisories/GHSA-7hp8-65ch-5whp) ⭐️ 8.0/10

WordPress released version 7.1.2, fixing an unauthenticated path traversal flaw (tracked as CVE-2026-87902) in which get_page_template() page-template resolution could be made to include a chosen readable local .php file located outside the active theme directories, potentially leading to remote code execution. As a courtesy to users on older releases, the fix was backported to every branch back to WordPress 4.7. WordPress powers an enormous share of the web, and an unauthenticated bug that can escalate into remote code execution is the most dangerous class of vulnerability, since no login or user interaction is required. The fact that the patch reaches back to branches from roughly nine years ago shows how many deployments still run legacy versions that now need emergency updates. Exploitation is conditional rather than guaranteed: the advisory notes that relevant pre-conditions must be met in both the server environment and the active theme before the file inclusion escalates to RCE. The vulnerable code path traces back to locate_template(), whose own documentation warned years ago that it does not prevent directory traversal when passed a user-supplied template name.

hackernews · vntok · Sep 22, 16:33 · [Discussion](https://news.ycombinator.com/item?id=49803959)

**Background**: Path traversal is a web vulnerability in which user input is used to build a file path without proper validation, letting an attacker reach files outside the intended directory. Remote code execution (RCE) means an attacker can run their own code on the target server, typically the most severe outcome of any security flaw. WordPress is a PHP-based content management system that renders pages by including template files from the active theme, and functions such as get_page_template() decide which template file gets loaded. If that resolution can be steered toward a .php file outside the theme directories, the attacker may get that file executed by the server.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/WordPress/wordpress-develop/security/advisories/GHSA-7hp8-65ch-5whp">Unauthenticated path traversal in page-template resolution leading to conditional RCE · Advisory · WordPress/wordpress-develop · GitHub</a></li>
<li><a href="https://securityonline.info/wordpress-rce-vulnerability-cve-2026-87902/">CVE-2026-87902: Critical WordPress RCE Flaw Fixed in Version 7.1.2</a></li>
<li><a href="https://en.wikipedia.org/wiki/Arbitrary_code_execution">Arbitrary code execution - Wikipedia</a></li>

</ul>
</details>

**Discussion**: Commenters were largely unsurprised, describing WordPress as one of the most-exploited pieces of software in web history and noting that roughly a third of installs still are not on the recent 7.x branch. Several shared migration stories, including one reader who moved to statically hosted Hugo templates to escape WordPress entirely, while another pointed out that a nine-year-old documentation comment on the affected function had already described both the nature of the flaw and its remediation.

**Tags**: `#WordPress`, `#security`, `#vulnerability`, `#RCE`, `#path-traversal`

---

<a id="item-8"></a>
## [Claude Opus 5.5 and GPT-6 Sol/Luna land as frontier model price war heats up](https://simonwillison.net/2026/Sep/22/opus-and-sol-and-luna/) ⭐️ 8.0/10

On the same day, Anthropic released Claude Opus 5.5 and, roughly an hour later, OpenAI released GPT-6 Sol and GPT-6 Luna, following Grok 4.7 and Xiaomi's MiMo v2.6 Flash/Pro the previous day. Simon Willison reports that GPT-6 Luna costs half of GPT-5.6 Luna ($0.10 per million input tokens and $0.50 per million output tokens), and GPT-6 Sol saw a similar reduction versus GPT-5.6 Sol. Halving the price of frontier-class models dramatically lowers the cost of building AI applications and squeezes competitors, with Grok 4.7's earlier $2/$6 pricing advantage now largely erased against GPT-6 Sol. The shift also obsoletes older tiers almost overnight: with GPT-5.6 Terra priced identically to GPT-6 Sol but with a higher output rate, Willison says any remaining reason to use Terra has evaporated. At $0.10/$0.50 per million tokens, GPT-6 Luna is one of the cheapest models OpenAI has ever released, beaten only by the far weaker GPT-4.1 Nano ($0.10/$0.40, April 2025) and GPT-5 Nano ($0.05/$0.40, August 2025). Claude Opus 5.5 sits at $4 input/$20 output with $0.20 cached input, while GPT-5.6 is scheduled for a 25% price increase in November, meaning GPT-6 is half the promotional price of those models, not just the list price.

rss · Simon Willison · Sep 22, 23:46

**Background**: These are "frontier" large language models, the most capable general-purpose models each lab offers, sold through APIs priced per million tokens of input and output; cached input pricing gives a discount when the same context is reused. Willison, a well-known developer and analyst, is also the creator of the informal "pelican on a bicycle" benchmark, in which models are asked to generate an SVG of a pelican riding a bicycle — he used it here to compare the visual output of the GPT-6 and GPT-5.6 families. Model releases are increasingly accompanied by steep price cuts, part of a broader trend in which frontier token prices have fallen far below their 2023 levels.

<details><summary>References</summary>
<ul>
<li><a href="https://ai.miraheze.org/wiki/Pelican_Bicycle_Benchmark">Pelican Bicycle Benchmark - Learn AI</a></li>
<li><a href="https://benchlm.ai/llm-pricing-trends">LLM API Pricing Trends & Updates (September 2026) | BenchLM.ai</a></li>
<li><a href="https://siliconangle.com/2026/09/22/xiaomi-introduces-mimo-v2-6-series-open-source-ai-model-family/">Xiaomi introduces Mimo-V2.6 series open-source AI model family - SiliconANGLE</a></li>

</ul>
</details>

**Tags**: `#LLMs`, `#AI industry`, `#model releases`, `#pricing`, `#OpenAI/Anthropic`

---

<a id="item-9"></a>
## [DeepSeek and Tsinghua release DSec sandbox platform serving 3M sandboxes daily](https://arxiv.org/abs/2609.22978) ⭐️ 8.0/10

DeepSeek-AI and Tsinghua University jointly published a technical report on DSec (DeepSeek Elastic Compute), a sandbox infrastructure built to support large-scale agent training and evaluation. The platform exposes four backends through a unified SDK — FnCall, containers, Firecracker microVMs, and full VMs — covering workloads such as online-judge grading, software engineering, security penetration testing, and computer-use tasks. Sandbox capacity and startup latency are widely considered a core bottleneck for reinforcement-learning-based agent training, so a production-scale account of how to serve millions of isolated environments per day is valuable to anyone building agent systems. The report also shows how stateful rollout execution can be decoupled from preemptible GPU training, a design pattern likely to influence how other labs architect their agent RL pipelines. A single production unit spans roughly 160 nodes and serves about 3 million sandbox instances per day, with peak concurrency above 380,000 and creation rates exceeding 5,000 per second; each node can densely host up to 3,200 containers or 800 microVMs. DSec loads EROFS images on demand over the 3FS distributed file system, which the report claims yields 1.7× faster task completion and 57% less disk write compared with traditional full Docker pulls, while memory sharing and reclamation cut peak memory usage by about 40%.

telegram · zaihuapd · Sep 22, 04:45

**Background**: Agent training typically requires the model to interact with real software — running code, browsing files, or operating an OS — inside an isolated environment that can be reset, which is what a sandbox provides. Firecracker is AWS's open-source virtualization technology that creates lightweight microVMs combining hardware-level isolation with sub-second startup and low memory overhead, making it popular for multi-tenant workloads. EROFS is a lightweight read-only Linux file system optimized for runtime performance and storage savings, while 3FS (Fire-Flyer File System) is DeepSeek's own high-performance distributed file system designed for AI workloads over SSDs and RDMA networks.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/firecracker-microvm/firecracker">GitHub - firecracker-microvm/firecracker: Secure and fast ... GitHub - firecracker-microvm/firecracker: Secure and fast ... firecracker-microvm/firecracker | DeepWiki Run Your First Firecracker microVM - labs.iximiuz.com I tried Firecracker microVMs for self-hosted services, and it ... What Is a Firecracker VM? · Learn</a></li>
<li><a href="https://zh.wikipedia.org/wiki/EROFS">EROFS - 维基百科，自由的百科全书</a></li>
<li><a href="https://blog.csdn.net/qq_45453266/article/details/145924103">DeepSeek开源周Day5压轴登场： 3 FS 与Smallpond，能否终结AI...</a></li>

</ul>
</details>

**Tags**: `#AI agents`, `#sandbox infrastructure`, `#DeepSeek`, `#RL training`, `#systems`

---

<a id="item-10"></a>
## [China Probes DeepSeek and Moonshot Over Alleged Claude Data Leaks](https://www.theinformation.com/articles/china-probes-deepseek-moonshot-potential-data-leaks-anthropic) ⭐️ 8.0/10

China's internet regulator is investigating DeepSeek and Moonshot AI after Anthropic's 154-page report, published on September 10, accused seven Chinese AI companies of improperly routing user data to its Claude models — including a DeepSeek request reportedly tied to engineers building a police surveillance system. The Information reported the probe, citing people familiar with the matter. The investigation marks a rare case of Chinese regulators scrutinizing their own flagship AI startups over cross-border model usage, turning a vendor's abuse report into a domestic data-governance case. It could reshape how Chinese AI firms handle data routing and API access, and it escalates the already tense geopolitics between Chinese model developers and U.S. AI labs such as Anthropic. Anthropic's report alleges industrial-scale misuse of Claude through networks of fraudulent accounts — one earlier disclosure cited roughly 24,000 fake accounts and more than 16 million interactions, with operations attributed to Alibaba alone reportedly sending over 151 million interactions to Claude in three months. DeepSeek and Moonshot have not publicly confirmed the investigation, and the specific data-handling rules allegedly violated remain unclear.

telegram · zaihuapd · Sep 22, 14:37

**Background**: Anthropic is a U.S. AI company that makes the Claude family of models, and it has published several threat-intelligence reports this year accusing Chinese labs of "distillation" — training their own models on another model's outputs to cheaply replicate its capabilities. DeepSeek is a Hangzhou-based AI lab known for low-cost frontier models, while Moonshot AI (月之暗面) is a Beijing-based company behind the Kimi assistant. Both are among China's most prominent AI startups, which makes an official probe into their data practices especially notable.

<details><summary>References</summary>
<ul>
<li><a href="https://www.voachinese.com/a/anthropic-alleges-chinese-ai-firms-distilled-claude-s-capabilities-as-china-linked-accounts-used-it-for-overseas-surveillance-20260911/8196927.html">Anthropic 指 中 国 AI 公 司 大 规 模蒸馏 Claude ... | 美 国 之音</a></li>
<li><a href="https://zh.wikipedia.org/wiki/月之暗面_(公司)">月 之 暗 面 ( 公 司 ) - 维基百科，自由的百科全书</a></li>
<li><a href="https://finance.sina.cn/tech/2026-02-24/detail-inhnxaes3088094.d.html?fromtech=1&vt=4">中国公司“偷走” Claude 模 型 ？Anthropic气炸，却被马斯克一句话怼到无语</a></li>

</ul>
</details>

**Tags**: `#AI regulation`, `#DeepSeek`, `#Anthropic Claude`, `#data privacy`, `#China tech policy`

---

<a id="item-11"></a>
## [OpenAI Begins Limited Preview of GPT-5.6 Family: Sol, Terra, Luna](https://t.me/zaihuapd/43990) ⭐️ 8.0/10

OpenAI has reportedly begun a limited preview of its GPT-5.6 model family, consisting of the flagship Sol, the balanced Terra, and the low-cost Luna. The preview is initially limited to a small set of trusted partners and is delivered through the API and Codex, with OpenAI describing it as a short-term measure requested by the US government before a broader rollout to ChatGPT and Codex in the coming weeks. A new flagship model family from OpenAI would be one of the most consequential events in the LLM landscape, directly affecting developers building on the API, competitors' positioning, and enterprise model-selection decisions. The reported government involvement in gating the preview also signals that frontier-model access is increasingly being shaped by policy and national-security considerations rather than purely commercial timelines. Sol is said to emphasize stronger coding, biological, and cybersecurity capabilities, and adds a new "max" reasoning intensity plus an "ultra" mode; Terra reportedly delivers performance close to GPT-5.5 at roughly half the cost, while Luna is positioned as the cheapest option. These claims come from a single Telegram aggregator with no independent verification, so specifics such as pricing, context limits, and benchmark numbers remain unconfirmed.

telegram · zaihuapd · Sep 22, 18:04

**Background**: OpenAI has been naming its frontier models in numbered generations (GPT-4, GPT-5 and successors), with higher reasoning settings and specialized modes used to trade off latency against answer quality, and the "x.5" style designations typically denoting intermediate refreshes rather than full generational jumps. Codex is OpenAI's suite of AI coding agents that lets developers delegate software-engineering tasks such as writing features and fixing bugs to a model-driven agent, which is why it appears alongside the API as an early distribution channel for a preview model. Limited previews to vetted partners are a common practice before general availability, letting OpenAI gather safety and reliability data under controlled conditions.

<details><summary>References</summary>
<ul>
<li><a href="https://grokipedia.com/page/OpenAI_Codex">OpenAI Codex</a></li>

</ul>
</details>

**Tags**: `#OpenAI`, `#GPT-5.6`, `#LLM`, `#model-release`, `#AI`

---