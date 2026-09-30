---
layout: default
title: "Horizon Summary: 2026-09-30 (EN)"
date: 2026-09-30
lang: en
---

> From 39 items, 6 important content pieces were selected

---

1. [OpenAI launches GPT-6.1 Sol at one-fifth of Astra's price](#item-1) ⭐️ 9.0/10
2. [OpenAI DevDay 2026: Dots agent, GPT-6.1 Sol, Ultrafast and 20+ updates](#item-2) ⭐️ 9.0/10
3. [OpenAI Launches Dots, Always-On Agents With Their Own Cloud Computers](#item-3) ⭐️ 8.0/10
4. [Relapse Exploit Jailbreaks PS5 Firmware 7.00–13.60](#item-4) ⭐️ 8.0/10
5. [Anthropic: New Models Cross Threshold on Binary Exploitation Benchmark](#item-5) ⭐️ 8.0/10
6. [DeepSeek Open-Sources Huawei Ascend Foundation Components](#item-6) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [OpenAI launches GPT-6.1 Sol at one-fifth of Astra's price](https://openai.com/index/introducing-gpt-6-1-sol/) ⭐️ 9.0/10

OpenAI has announced GPT-6.1 Sol, an upgrade to GPT-6 Sol that the company says delivers near-GPT-6 Astra intelligence on agentic coding, computer use, and professional tasks while costing only one-fifth of Astra's standard price. It is available through the OpenAI API as gpt-6.1-sol at $2 per million input tokens, $0.10 per million cached input tokens, and $10 per million output tokens, and is being rolled out to Plus, Pro, Business, Enterprise, and Edu users. The release pushes the AI price war to a new low, with cached input priced 50% below GPT-6 Sol's cached rate and roughly 95% below standard input pricing, which directly cuts the cost of running coding agents and long-context workloads. It also raises pressure on rivals such as Anthropic and DeepSeek, and shifts the competitive battleground from raw capability toward cost per token. Early third-party numbers are promising but limited: Devin reports that at low effort GPT-6.1 Sol scores 58.1% for $0.21 per task, up from 50.5% for GPT-6 Sol at the same setting, the highest score of any model under $0.30 per task on its leaderboard. OpenAI's own page notes the model is not yet available in ChatGPT, so access for now is mainly via the API and partner tools rather than the consumer chat interface.

hackernews · crorella · Sep 29, 17:06 · [Discussion](https://news.ycombinator.com/item?id=49896586)

**Background**: OpenAI's GPT-6 family includes three tiers: GPT-6 Astra, released to the general public on September 4, 2026, and the cheaper Sol and Luna variants, released on September 22, 2026. Astra was positioned as the frontier, highest-intelligence model and was widely discussed after reportedly solving 10 long-standing open problems in mathematics and computer science, while Sol was the more affordable workhorse used in coding tools such as Codex and Devin. "Cached input" tokens are prompt tokens the provider has already processed and stored, so they can be re-billed at a steep discount on repeated requests. GPT-6.1 is thus a mid-cycle refresh that tries to close most of the gap to Astra while slashing the cost of using it.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/GPT-6_Sol">GPT-6 Sol</a></li>
<li><a href="https://openai.com/index/introducing-gpt-6-1-sol/">Introducing GPT - 6 . 1 Sol | OpenAI</a></li>
<li><a href="https://devin.ai/blog/gpt-6-1-sol">GPT - 6 . 1 Sol is now available in Devin | Devin</a></li>

</ul>
</details>

**Discussion**: The Hacker News thread (844 points, 762 comments) is largely skeptical. Several developers argue that DeepSeek is fast enough, cheap enough, and close enough in quality that paying $200 or $500 per month for OpenAI or Anthropic tiers is hard to justify, and others report that GPT-6 Sol regressed so badly they switched to Anthropic's Opus 5.5. Commenters also speculate that GPT-6.1 Sol is a last-minute rename of an "Astra-Minor" model found in leaked files, and several agree with the view that the cached-input price cut, not the model itself, is the real headline — while one notes it is "ominous" that token price has become the industry's main battleground.

**Tags**: `#OpenAI`, `#GPT-6.1`, `#LLMs`, `#AI pricing`, `#model release`

---

<a id="item-2"></a>
## [OpenAI DevDay 2026: Dots agent, GPT-6.1 Sol, Ultrafast and 20+ updates](https://openai.com/zh-Hant/index/devday-2026-recap/) ⭐️ 9.0/10

At its annual DevDay showcase in San Francisco, OpenAI announced more than 20 updates, headlined by Dots — an always-on companion agent that can operate a computer and pull data from connected apps to do research, draft documents and build software — plus GPT-6.1 Sol, a coding- and computer-use-focused model that delivers near-Astra intelligence at roughly one-fifth the price, and an Astra Ultrafast tier that runs up to 8x faster than Astra Standard (6x in the API) at 300 tokens per second. OpenAI also launched a Codex cloud experience, an Agents API with native computer use and AWS Bedrock hosting, a lightweight Decisions API for typed classification and routing, a new Pro 500 subscription tier, and 'Sign in with ChatGPT' account linking for third-party tools like Devin and Notion. This is one of the most consequential single-day releases in the AI industry, because it moves OpenAI from selling model access toward selling persistent autonomous agents plus an agent-oriented developer platform — a shift that reshapes how third-party apps are built and monetized. The Decisions API in particular pushes cheap, low-latency decision-making into the stack, while 'Sign in with ChatGPT' lets subscription credits flow into outside tools, potentially making OpenAI an identity and billing layer for the broader agent ecosystem. Ultrafast speed comes at a substantial premium: API usage costs 6x the corresponding model's standard rate, it is initially available only for GPT-6 Astra with a version for 6.1 Sol promised later, and OpenAI says it is working with Microsoft to integrate specialist Dots with enterprise governance and security controls in Agent 365. OpenAI also reportedly scrapped the launch of a new AI model over safety concerns before unveiling Dots, which the Decisions API complements by returning one typed answer from user-defined options with a probability for each option, reportedly about 10x faster than GPT-6 Luna through the standard API (roughly 150 ms versus about 1.6 seconds).

telegram · zaihuapd · Sep 29, 17:52

**Background**: OpenAI holds an annual DevDay event to showcase new products for developers, and its 2026 edition centered on 'agents' — AI systems that act on a user's behalf rather than only answering prompts. Dots is described by CEO Sam Altman as 'more ambitious' than ChatGPT and a 'whole new way to work with AI', reflecting the industry-wide race toward always-on agents that can use software directly. The names Astra, Sol and Luna refer to OpenAI's GPT-6 family of models positioned at different capability and cost points, while APIs like Agents and Decisions are interfaces that let outside developers call these capabilities from their own apps.

<details><summary>References</summary>
<ul>
<li><a href="https://openai.com/index/introducing-dots/">Introducing dots | OpenAI</a></li>
<li><a href="https://venturebeat.com/technology/openais-gpt-6-1-sol-offers-astra-like-performance-at-1-5th-price-a-new-ultrafast-tier-clocks-at-300-tokens-per-second">OpenAI's GPT-6.1 Sol offers Astra-like performance at 1/5th price. A new Ultrafast tier clocks at 300 tokens per second. | VentureBeat</a></li>
<li><a href="https://www.theguardian.com/technology/2026/sep/29/openai-announces-dots-agent-safety-concerns">OpenAI announces ‘dots’ agent after scrapping launch of new AI model over safety concerns | OpenAI | The Guardian</a></li>

</ul>
</details>

**Tags**: `#OpenAI`, `#AI Agents`, `#LLM`, `#Developer APIs`, `#Industry Announcement`

---

<a id="item-3"></a>
## [OpenAI Launches Dots, Always-On Agents With Their Own Cloud Computers](https://openai.com/index/introducing-dots/) ⭐️ 8.0/10

At its DevDay 2026 event in San Francisco, OpenAI introduced Dots, described as "remarkably capable, always-on agents" that get to know what matters to a user and work on their behalf continuously. According to coverage of the launch, each Dot is powered by GPT-6 Astra, runs on its own cloud computer, can plug into more than 4,000 apps, and the first Dot is included with Pro and Business Premium plans. This is OpenAI's clearest move from a chat-based assistant toward persistent, proactive agents that act on a user's behalf rather than waiting for prompts, and it puts OpenAI directly against Meta's fast-growing personal agent Muse. Because a Dot accumulates integrations and work history, it also raises real questions about platform lock-in and about how OpenAI differentiates Dots from Codex and the rest of ChatGPT. The reported specifics are that Dots run on GPT-6 Astra, each with its own cloud computer and plugin access to over 4,000 apps, with one Dot bundled into Pro and Business Premium tiers. The lock-in argument is technical rather than contractual: swapping models is relatively easy, but migrating an agent that holds your integrations, credentials and work history effectively means moving your entire cloud-based working environment.

hackernews · alvis · Sep 29, 17:07 · [Discussion](https://news.ycombinator.com/item?id=49896604)

**Background**: An "always-on agent" is an AI system that runs persistently in the background on its own virtual machine, taking multi-step actions across apps on the user's behalf instead of only answering a single chat turn. OpenAI already ships overlapping products in this direction — Codex for coding and ChatGPT for general work — which is why commenters find the boundary between them and Dots blurry. The launch also lands in the middle of an agent platform war: Meta's Muse, announced the previous week, is framed as a consumer play that can be subsidized by Meta's ad business and distributed through its family of apps.

<details><summary>References</summary>
<ul>
<li><a href="https://openai.com/index/introducing-dots/">Introducing dots - OpenAI</a></li>
<li><a href="https://www.wired.com/story/openai-dots-always-on-ai-agents-that-proactively-help/">OpenAI’s Dots Are Always-On AI Agents—and Its Answer to Meta ...</a></li>
<li><a href="https://www.datacamp.com/blog/openai-dots">OpenAI Dots: Always-On Agents in ChatGPT, Explained</a></li>

</ul>
</details>

**Discussion**: The 378-comment Hacker News thread is largely skeptical: several users argue that always-on agents deliberately deepen platform lock-in, since an agent hosting your integrations and work history is "essentially your computer on the cloud" and far harder to leave than a model API. Others complain that Dots blurs into Codex and ChatGPT Work, worry that OpenAI is now testing the loyalty it earned with generous Codex limits by pushing unnecessary products, and several say they are more bullish on Meta's Muse as a consumer play; a final thread of opinion holds that cloud-resident agents will finally end the PC era and are aimed at non-technical users rather than today's developers.

**Tags**: `#OpenAI`, `#AI agents`, `#always-on agents`, `#platform lock-in`, `#product strategy`

---

<a id="item-4"></a>
## [Relapse Exploit Jailbreaks PS5 Firmware 7.00–13.60](https://github.com/ntfargo/Relapse-Exploit) ⭐️ 8.0/10

A public PlayStation 5 exploit chain called Relapse has been released on GitHub by developer ntfargo, claiming to jailbreak consoles running firmware versions 7.00 through 13.60. Users trigger it by opening a hosted web page or running a local Python server (serve.py) from the PS5's browser, and consoles updated on or after September 16 are reported as incompatible. Jailbreaks are significant because they unlock homebrew, backups, and region-free or modified software on a closed console ecosystem, and a chain spanning seven major firmware branches lowers the barrier for a large portion of the existing install base. It also puts pressure on Sony to patch quickly, likely through a mandatory firmware update, and reignites the long-running tension between console makers and the homebrew community. According to coverage of the repository, Relapse is an exploit chain that combines WebKit flaws with a kernel race condition rather than a single bug, and the project notes that consoles updated on September 16 are not compatible, so the technique only works on a specific firmware window. Triggering it requires only the console's web browser, making it far more accessible than hardware-based approaches.

hackernews · therepanic · Sep 29, 15:44 · [Discussion](https://news.ycombinator.com/item?id=49895304)

**Background**: A jailbreak is the process of exploiting software or hardware flaws in a locked-down console such as the PS5 (released in November 2020) to gain the ability to run unsigned code, which enables homebrew applications, backups, and unofficial modifications. Modern chains typically start from a browser-rendered web page: WebKit's JavaScript engine, JavaScriptCore, has historically been a rich source of memory-corruption bugs, often arising from missing checks when switching to higher-tier JIT compilers, and such a flaw gives the first foothold before a second stage escalates privileges to the kernel. Because these bugs are patched quietly through firmware updates, exploit developers often sit on a stockpile of unpublished flaws and release one only when a newer firmware closes off other paths.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/ntfargo/Relapse-Exploit">GitHub - ntfargo/Relapse-Exploit: Exploit chain for PS5 7.00 - 13.60 · GitHub</a></li>
<li><a href="https://elsolitario.org/en/2026/09/29/relapse-repo-claims-ps5-exploit-firmware-7-00-to-13-60/">PS5 Jailbreak: What Is Relapse Exploit and Its Scope</a></li>

</ul>
</details>

**Discussion**: Commenters focused on practical consequences: one user asked whether Relapse could finally allow manual USB backups of game saves, complaining that the PS5 locks saves behind per-profile PS Plus cloud subscriptions after their daughter lost a year of Minecraft progress. Others speculated that Sony might respond by disabling the JavaScriptCore JIT to shrink the attack surface, noted that jailbreak communities typically hold back additional zero-days for bootloader breakouts, and joked about timing the release around GTA 6 or gaining the ability to play Steam PC games on the console.

**Tags**: `#PS5`, `#security-exploit`, `#WebKit`, `#JavaScriptCore`, `#homebrew`

---

<a id="item-5"></a>
## [Anthropic: New Models Cross Threshold on Binary Exploitation Benchmark](https://simonwillison.net/2026/Sep/29/anthropic-frontier-red-team/) ⭐️ 8.0/10

Anthropic's Frontier Red Team evaluated several models on 100 randomly selected tasks from its internal Binary Exploitation benchmark and reported that GLM-5.3 achieved full control flow hijacks in 4% of trials and Claude Mythos Preview in 6%. Earlier models, including Claude Opus 4.6 and GLM-5.2, did not succeed on any of the tasks, which the team describes as a clearly crossed threshold. This is the first reported case of frontier language models scoring above zero on this kind of exploit-development benchmark, suggesting that automated discovery and weaponization of memory-corruption vulnerabilities is moving from theoretical to partially demonstrated capability. Such progress would affect vulnerability researchers, defenders who must patch faster, and the broader debate over whether advanced cyber capabilities are spreading beyond a small set of well-resourced labs. The success rates are low in absolute terms (4% and 6% of 100 random tasks), and the benchmark is Anthropic's internal one rather than a public standard, so the numbers are not directly comparable across labs. Notably, GLM-5.3 uses the same base model as GLM-5.2, with all reported gains coming from post-training, which suggests the capability jump came from training rather than scale.

rss · Simon Willison · Sep 29, 22:20

**Background**: Anthropic's Frontier Red Team is a research group that stress-tests frontier AI systems to map out their current capabilities and anticipate emerging risks, including cyber offense. Binary exploitation is the practice of subverting a compiled program by abusing memory-corruption bugs so that it violates a trust boundary in the attacker's favor; a control flow hijack is the stage where the attacker redirects the program's execution to code of their choosing, typically the goal of a full exploit chain. GLM-5.3 is Z.ai's flagship model, sharing the same base as GLM-5.2 — a large sparse Mixture-of-Experts (MoE) architecture with roughly 753B total parameters and about 40B activated per token.

<details><summary>References</summary>
<ul>
<li><a href="https://www.anthropic.com/research/team/frontier-red-team">Frontier Red Team Research \ Anthropic</a></li>
<li><a href="https://huggingface.co/zai-org/GLM-5.3">zai-org/GLM-5.3 · Hugging Face</a></li>
<li><a href="https://trailofbits.github.io/ctf/exploits/binary1.html">Binary Exploits 1 - CTF Field Guide</a></li>

</ul>
</details>

**Tags**: `#ai-security-research`, `#cybersecurity`, `#llm-capabilities`, `#red-teaming`, `#anthropic`

---

<a id="item-6"></a>
## [DeepSeek Open-Sources Huawei Ascend Foundation Components](https://mp.weixin.qq.com/s/X41mKH4Ds-VXUAnK6M8Eww) ⭐️ 8.0/10

DeepSeek reportedly open-sourced a suite of foundational software components for Huawei's Ascend platform on September 30, 2026, covering the TileLang high-level compilation tool, core compute libraries, and distributed communication libraries that mirror its existing Nvidia-platform stack. The release is said to include DeepGEMM Ascend, DeepEP Ascend, TileKernels, FlashMLA, and DeepSelect. This would be a major step toward building a non-Nvidia AI infrastructure stack, since DeepSeek is essentially porting the low-level training and inference tooling that made its models efficient onto Huawei's Ascend NPUs. If the components match their CUDA equivalents in usability, they could lower the barrier for Chinese labs and enterprises to train and serve large models entirely on domestic hardware. DeepSeek claims the components approach hardware performance ceilings in multiple benchmarks and says it is working with Huawei on a 128-card supernode design for the Ascend 950. The announcement itself is brief, circulated via a WeChat/Telegram-style repost with little substantive discussion, and cites a future-dated release, so specifics such as repositories, licenses, and benchmark numbers should be treated as unverified.

telegram · zaihuapd · Sep 30, 03:09

**Background**: Huawei's Ascend NPUs are China's leading alternative to Nvidia GPUs, but they have historically been harder to program because most AI training and inference software is written for Nvidia's CUDA ecosystem. DeepSeek previously released open-source components such as DeepGEMM (fast matrix multiplication kernels), DeepEP (expert-parallel communication for Mixture-of-Experts models), FlashMLA (efficient attention kernels), and TileLang, a tile-based programming model that lets developers write GPU/NPU kernels in a Python-like language. Porting all of these to Ascend means rebuilding the same low-level performance tricks for a different chip architecture, which is why the move is significant for the broader non-Nvidia ecosystem.

<details><summary>References</summary>
<ul>
<li><a href="https://tilelang.com/">TileLang 0.1.14 documentation</a></li>
<li><a href="https://github.com/deepseek-ai/DeepEP-Ascend/tree/main/">GitHub - deepseek-ai/DeepEP-Ascend: A high-performance ...</a></li>
<li><a href="https://github.com/deepseek-ai/DeepGEMM/pull/462">Public release 26/09/30 by LyricZhao · Pull Request #462 · deepseek-ai/DeepGEMM</a></li>

</ul>
</details>

**Tags**: `#DeepSeek`, `#Huawei Ascend`, `#Open Source`, `#AI Infrastructure`, `#TileLang`

---