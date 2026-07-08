---
layout: default
title: "Horizon Summary: 2026-07-08 (EN)"
date: 2026-07-08
lang: en
---

> From 40 items, 11 important content pieces were selected

---

1. [16-Year-Old KVM Flaw Allows VM Escape on Intel and AMD](#item-1) ⭐️ 10.0/10
2. [MIRA: 5B Parameter Multiplayer World Model for Rocket League](#item-2) ⭐️ 9.0/10
3. [China mulls export curbs on top AI models](#item-3) ⭐️ 9.0/10
4. [EU Chat Control: Mass Scanning of Private Messages Threatens Encryption](#item-4) ⭐️ 8.0/10
5. [EU mandates driver monitoring cameras in all new cars](#item-5) ⭐️ 8.0/10
6. [sqlite-utils 4.0 Introduces Schema Migrations](#item-6) ⭐️ 8.0/10
7. [New-API Fixes Billing Integer Overflow Vulnerability](#item-7) ⭐️ 8.0/10
8. [Anthropic Releases Claude Sonnet 5 with Enhanced Agentic Abilities](#item-8) ⭐️ 8.0/10
9. [NVIDIA Blackwell wafers made in US, shipped to Taiwan for packaging](#item-9) ⭐️ 8.0/10
10. [DeepSeek Develops Own AI Chip to Reduce Reliance on Nvidia and Huawei](#item-10) ⭐️ 8.0/10
11. [Google Voice Launches Paid Plans for Individuals with Call Recording and Gemini](#item-11) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [16-Year-Old KVM Flaw Allows VM Escape on Intel and AMD](https://github.com/V4bel/Januscape) ⭐️ 10.0/10

Researchers disclosed Januscape (CVE-2026-53359), the first KVM/x86 VM escape vulnerability exploitable on both Intel and AMD platforms, with a proof-of-concept (PoC) publicly released. This vulnerability breaks the isolation boundary between guest VMs and the host kernel in KVM-based multi-tenant clouds, posing severe risks to public cloud providers and any environment using KVM virtualization. The flaw is a use-after-free in the shadow MMU code path (specifically kvm_mmu_get_child_sp()), present since 2010 and affecting Linux kernels up to June 2026; a local unprivileged user can also escalate to root on some distributions like RHEL.

telegram · zaihuapd · Jul 7, 10:14

**Background**: KVM (Kernel-based Virtual Machine) is a Linux kernel module that turns it into a hypervisor, allowing multiple virtual machines to run. The shadow MMU is used to virtualize the guest's page tables when hardware-assisted virtualization (EPT/NPT) is not available. A VM escape is an attack where code running inside a virtual machine breaks out to interact with the host operating system, compromising the isolation.

<details><summary>References</summary>
<ul>
<li><a href="https://thehackernews.com/2026/07/16-year-old-linux-kvm-flaw-lets-guest.html">16-Year-Old Linux KVM Flaw Lets Guest VMs Escape to Host on ...</a></li>
<li><a href="https://cyberpress.org/16-year-old-linux-kvm-vulnerability/">16-Year-Old Linux KVM Vulnerability Allows Malicious Guests ...</a></li>
<li><a href="https://docs.kernel.org/virt/kvm/x86/mmu.html">The x86 kvm shadow mmu — The Linux Kernel documentation</a></li>

</ul>
</details>

**Tags**: `#KVM`, `#virtualization`, `#security`, `#vulnerability`, `#CVE`

---

<a id="item-2"></a>
## [MIRA: 5B Parameter Multiplayer World Model for Rocket League](https://www.reddit.com/r/MachineLearning/comments/1upofuw/mira_multiplayer_interactive_world_models_trained/) ⭐️ 9.0/10

Researchers from General Intuition, Kyutai, and Epic Games have released MIRA, a 5-billion-parameter interactive world model for 4-player Rocket League, trained on 10,000 hours of synthetic data, along with a playable demo, technical report, and a curated dataset. MIRA represents a breakthrough in large-scale world models for multiplayer interactive environments, demonstrating real-time 20 fps simulation on a single B200 GPU, which could advance reinforcement learning, interactive AI, and game simulation. The model has 5 billion parameters and runs at 20 fps for four players on a single NVIDIA B200 GPU, which is based on the Blackwell architecture. A playable online demo and a technical report are available at mira-wm.com, and the dataset includes 1,000 hours of 4-player gameplay.

reddit · r/MachineLearning · /u/MasterScrat · Jul 7, 07:59

**Background**: A world model is a neural network that learns to simulate an environment's dynamics, enabling agents to plan and make decisions without direct interaction. Large-scale world models like MIRA are trained on massive amounts of gameplay data to predict future states and rewards. Reinforcement learning often uses such models for training agents in simulated environments. MIRA specifically tackles the challenge of multiplayer interactions, which require modeling complex agent behaviors.

<details><summary>References</summary>
<ul>
<li><a href="https://worldmodels.github.io/">World Models</a></li>
<li><a href="https://www.nvidia.com/en-us/data-center/dgx-b200/">DGX B200: The Foundation for Your AI Factory | NVIDIA</a></li>

</ul>
</details>

**Tags**: `#world models`, `#reinforcement learning`, `#multiplayer AI`, `#Rocket League`, `#interactive simulation`

---

<a id="item-3"></a>
## [China mulls export curbs on top AI models](https://www.reuters.com/world/beijing-is-looking-curbing-overseas-access-chinas-top-ai-models-sources-say-2026-07-07/) ⭐️ 9.0/10

China's Ministry of Commerce has held meetings with Alibaba, ByteDance, and Zhipu AI to discuss restricting overseas access to the country's most advanced AI models, including unreleased ones. This policy, if enacted, could significantly alter the global AI landscape by limiting the flow of Chinese AI technology abroad, affecting international collaborations and competition. The restrictions may apply only to future model releases, and the scope is still under discussion. The proposal also includes criminalizing AI technology leaks under national security law and restricting foreign investment in Chinese AI startups.

telegram · zaihuapd · Jul 7, 11:42

**Background**: China has developed several competitive AI models, such as those from Zhipu AI (e.g., GLM-130B and ChatGLM), which compete with Western counterparts like GPT-4. The Chinese government has been increasingly concerned about technology security and data sovereignty, leading to tighter controls on AI exports.

<details><summary>References</summary>
<ul>
<li><a href="https://zh.wikipedia.org/wiki/智谱">智谱 - 维基百科，自由的百科全书</a></li>

</ul>
</details>

**Tags**: `#AI regulation`, `#China`, `#export control`, `#technology policy`

---

<a id="item-4"></a>
## [EU Chat Control: Mass Scanning of Private Messages Threatens Encryption](https://fightchatcontrol.eu/chat-control-overview) ⭐️ 8.0/10

The European Union's Chat Control proposal, formally the Child Sexual Abuse Regulation (CSAR), would mandate client-side scanning of all private messages before encryption, effectively breaking end-to-end encryption. Two versions (Chat Control 1.0 and 2.0) have been debated, with the latest updates in 2026 showing partial legislative blockage but ongoing risk. If enacted, this legislation would undermine the fundamental privacy and security of billions of encrypted messages across platforms like WhatsApp, Signal, and Telegram, setting a dangerous global precedent for mass surveillance. It affects every EU citizen and threatens the broader adoption of secure communication. The proposal requires client-side scanning (CSS), where messages are scanned on the user's device before encryption against a database of known illegal content. Critics argue CSS creates backdoors that could be exploited, is prone to false positives, and cannot be audited by users.

hackernews · gasull · Jul 7, 14:23 · [Discussion](https://news.ycombinator.com/item?id=48818311)

**Background**: End-to-end encryption ensures only the sender and recipient can read messages, with no third party access. Client-side scanning circumvents encryption by analyzing content before it is encrypted. The EU Chat Control proposal, first introduced in May 2022, aims to combat child sexual abuse material but has drawn widespread criticism from privacy advocates and tech companies.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Chat_Control">Chat Control - Wikipedia</a></li>
<li><a href="https://www.eff.org/deeplinks/2026/04/eu-parliament-blocks-mass-scanning-our-chats-whats-next">EU Parliament Blocks Mass-Scanning of Our Chats—What's Next? | Electronic Frontier Foundation</a></li>
<li><a href="https://fightchatcontrol.eu/">Fight Chat Control - Protect Digital Privacy in the EU</a></li>

</ul>
</details>

**Discussion**: Community comments express strong opposition, with users arguing it's a 'dictatorial power grab' and that targeted measures would be more effective than mass surveillance. Some question how it affects encrypted messages, noting the Apple-style on-device scanning approach, while others ask how Signal is responding.

**Tags**: `#privacy`, `#encryption`, `#surveillance`, `#policy`, `#EU`

---

<a id="item-5"></a>
## [EU mandates driver monitoring cameras in all new cars](https://allaboutcookies.org/eu-mandatory-distracted-driver-system) ⭐️ 8.0/10

Starting from July 2026, the EU's General Safety Regulation requires every new car sold in the European Union to include a driver monitoring system (DMS) that uses cameras to detect distraction or drowsiness and issue warnings. This regulation aims to reduce accidents caused by driver inattention, potentially saving thousands of lives annually, but it also raises significant privacy and user experience concerns as drivers may feel surveilled by always-on cameras. The mandate applies to all vehicle categories (M and N, i.e., cars, vans, trucks, and buses) and requires Driver Drowsiness and Attention Warning (DDAW) systems, which typically use infrared cameras to track gaze direction and head movement.

hackernews · nickslaughter02 · Jul 7, 20:50 · [Discussion](https://news.ycombinator.com/item?id=48823557)

**Background**: Driver monitoring systems (DMS) have been used in some vehicles since Toyota introduced them in 2006. The technology uses in-car cameras and computer vision to assess alertness. The EU's General Safety Regulation, established in 2019, gradually phases in such mandates to improve road safety.

<details><summary>References</summary>
<ul>
<li><a href="https://smarteye.se/blog/the-general-safety-regulations-gsr-and-driver-monitoring-systems-dms/">How Driver Monitoring Systems (DMS) Are Being Made Mandatory in 18 Million European Cars - Smart Eye</a></li>
<li><a href="https://en.wikipedia.org/wiki/Driver_monitoring_system">Driver monitoring system - Wikipedia</a></li>
<li><a href="https://medium.com/@shahadilh18/your-car-will-soon-watch-your-eyes-b8e78dcfb114">Your Car Will Soon Watch Your Eyes. Here Is the Real Story Behind the EU’s Driver Monitoring Mandate | by Shahadilh | Medium</a></li>

</ul>
</details>

**Discussion**: Comments show mixed reactions: some users note that existing systems (e.g., Ford's BlueCruise) are accurate and can catch distractions like eating or talking, potentially saving lives. Others complain about poor UX in newer cars, such as annoying beeps and lane assist that can't be turned off, drawing parallels to Boeing's alarm issues.

**Tags**: `#EU regulation`, `#driver monitoring`, `#automotive safety`, `#privacy`, `#UX`

---

<a id="item-6"></a>
## [sqlite-utils 4.0 Introduces Schema Migrations](https://simonwillison.net/2026/Jul/7/sqlite-utils/#atom-everything) ⭐️ 8.0/10

sqlite-utils 4.0 has been released, adding official support for database schema migrations, a feature long requested by the community. This update significantly enhances the utility's ability to manage SQLite database schemas over time, making it a more robust tool for Python developers and data scientists who rely on SQLite. The migrations support includes a command-line interface and Python API for applying incremental schema changes, with features like nested transactions first introduced in the release candidate.

rss · Simon Willison · Jul 7, 15:42

**Background**: sqlite-utils is a Python library and CLI tool from Datasette creator Simon Willison, designed to simplify creating and manipulating SQLite databases. Previously, users had to manually handle schema evolution or use external tools; version 4.0 fills this gap.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/simonw/sqlite-utils">GitHub - simonw/sqlite-utils: Python CLI utility and library for manipulating SQLite databases · GitHub</a></li>
<li><a href="https://sqlite-utils.datasette.io/">sqlite-utils</a></li>

</ul>
</details>

**Discussion**: The community has reacted positively, with many expressing excitement about the long-awaited migration feature. Some users noted the addition of nested transactions as a welcome improvement for data integrity.

**Tags**: `#sqlite-utils`, `#SQLite`, `#Python`, `#database`, `#migrations`

---

<a id="item-7"></a>
## [New-API Fixes Billing Integer Overflow Vulnerability](https://github.com/QuantumNous/new-api/commit/d0bd8aa) ⭐️ 8.0/10

The QuantumNous/new-api project has patched an integer overflow vulnerability in its billing system, where oversized parameters could trigger negative fee deductions, effectively reversing charges. This fix prevents attackers from exploiting the vulnerability to gain unauthorized credits or cause financial loss, protecting the integrity of the billing system in a widely-used AI API gateway. The fix adds upper-bound validation and saturation logic to prevent integer overflow when converting quota calculations, and further reinforces boundary checks in other billing entry points.

telegram · zaihuapd · Jul 7, 07:26

**Background**: Integer overflow occurs when an arithmetic operation exceeds the maximum value a data type can hold, causing unexpected wraparound to a minimum or negative value. In billing systems, this can be exploited to deduct negative amounts. QuantumNous/new-api is an open-source unified AI model hub offering API gateway, quota management, and billing features.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/QuantumNous/new-api">GitHub - QuantumNous/new-api: A unified AI model hub for ...</a></li>
<li><a href="https://www.numberanalytics.com/blog/integer-overflow-silent-threat-software-development">Integer Overflow: A Silent Threat - numberanalytics.com</a></li>

</ul>
</details>

**Tags**: `#security`, `#billing`, `#integer overflow`, `#open source`, `#bug fix`

---

<a id="item-8"></a>
## [Anthropic Releases Claude Sonnet 5 with Enhanced Agentic Abilities](https://t.me/zaihuapd/42404) ⭐️ 8.0/10

Anthropic has released Claude Sonnet 5, claiming it is their most capable Sonnet model yet in terms of agentic abilities, able to plan and use tools like browsers and terminals autonomously. The model is available immediately for all plans and becomes the default model for Free and Pro users, with a limited-time API pricing of $2 per million input tokens through August 31, 2026. Claude Sonnet 5's improved agentic capabilities and near-Opus-level performance at a lower price point make advanced AI agents more accessible and cost-effective, potentially accelerating the adoption of autonomous AI systems in enterprise and developer workflows. Claude Sonnet 5 outperforms Sonnet 4.6 in reasoning, tool use, coding, and knowledge work, with performance approaching that of Opus 4.8. The limited-time API pricing is set at $2 per million input tokens and $X per million output tokens (exact output price not specified in content).

telegram · zaihuapd · Jul 7, 09:02

**Background**: Agentic AI refers to AI systems that can perceive, reason, and act autonomously to achieve specific goals with limited supervision. Anthropic's Claude model lineup includes tiers: Haiku for speed, Sonnet for balanced performance, Opus for top-tier capability, and Fable for specialized tasks. Sonnet models are designed to offer a strong balance of performance and cost, making them suitable for a wide range of applications.

<details><summary>References</summary>
<ul>
<li><a href="https://mitsloan.mit.edu/ideas-made-to-matter/agentic-ai-explained">Agentic AI, explained - MIT Sloan</a></li>
<li><a href="https://www.aipricing.guru/">AI API Pricing 2026: Compare GPT, Claude, Gemini Token Costs</a></li>
<li><a href="https://emergent.sh/learn/claude-sonnet-vs-opus">Claude Sonnet vs Opus (2026): Which Claude Model Is Actually ...</a></li>

</ul>
</details>

**Tags**: `#Anthropic`, `#Claude`, `#AI model`, `#agentic capabilities`, `#natural language processing`

---

<a id="item-9"></a>
## [NVIDIA Blackwell wafers made in US, shipped to Taiwan for packaging](https://www.tomshardware.com/tech-industry/nvidia-and-intel-tout-chips-built-in-america-but-every-arizona-made-blackwell-die-is-still-packaged-in-taiwan) ⭐️ 8.0/10

TSMC's Fab 21 in Arizona has begun mass production of NVIDIA Blackwell wafers using the custom 4NP process, but these wafers must be shipped to Taiwan for advanced CoWoS-L packaging and HBM integration because the US lacks such facilities. This highlights a critical dependency in the semiconductor supply chain: even as the US gains advanced logic fabrication, the complete chip production still relies on Taiwan for packaging, posing a bottleneck for AI hardware supply and national security. The Blackwell wafers are fabricated using TSMC's 4NP node, a refinement of the 4N node used for Hopper and Ada Lovelace architectures. The wafers travel about 7,000 miles to Taiwan for dicing, die stacking, and CoWoS-L packaging, a process that integrates logic and HBM memory.

telegram · zaihuapd · Jul 7, 09:47

**Background**: Advanced packaging, such as CoWoS (Chip-on-Wafer-on-Substrate), is crucial for high-performance AI chips because it allows multiple dies (e.g., GPU and HBM memory) to be integrated in a single package with high bandwidth. HBM (High-Bandwidth Memory) is a 3D-stacked memory standard that provides massive data throughput for AI workloads. Currently, TSMC's CoWoS capacity and HBM production are concentrated in Taiwan, and building equivalent facilities in the US will take years.

<details><summary>References</summary>
<ul>
<li><a href="https://3dfabric.tsmc.com/english/dedicatedFoundry/technology/cowos.htm">CoWoS® - Taiwan Semiconductor Manufacturing Company Limited</a></li>
<li><a href="https://en.wikipedia.org/wiki/High_Bandwidth_Memory">High Bandwidth Memory - Wikipedia</a></li>
<li><a href="https://www.trendforce.com/news/2024/03/19/news-tsmcs-4nm-process-powers-nvidias-blackwell-architecture-gpu-ai-performance-surpasses-previous-generations-by-multiples/">[News] TSMC’s 4nm Process Powers NVIDIA’s Blackwell ...</a></li>

</ul>
</details>

**Tags**: `#semiconductor`, `#NVIDIA`, `#supply chain`, `#TSMC`, `#Blackwell`

---

<a id="item-10"></a>
## [DeepSeek Develops Own AI Chip to Reduce Reliance on Nvidia and Huawei](https://www.reuters.com/world/china/chinas-deepseek-developing-its-own-ai-chip-sources-say-2026-07-07/) ⭐️ 8.0/10

DeepSeek is developing its own AI inference chip to reduce dependence on Nvidia and Huawei, according to three sources. The effort started about a year ago and is still in early stages, with DeepSeek recruiting chip designers and engaging with chip design, foundry, and memory companies. This move could reshape the AI chip landscape by reducing DeepSeek's vulnerability to US export controls and decreasing reliance on Nvidia and Huawei. It signals a broader trend of AI companies verticalizing their hardware supply chains to maintain strategic autonomy. The chip focuses on inference (generating answers from trained models) rather than training. DeepSeek previously relied on Nvidia H800 and Huawei Ascend chips, which are subject to US export restrictions.

telegram · zaihuapd · Jul 7, 11:08

**Background**: AI inference chips are specialized processors designed to run trained models efficiently. DeepSeek is a Chinese AI company known for cost-effective models, and founder Liang Wenfeng previously cited chip restrictions as a challenge. US export controls have limited access to advanced Nvidia chips for Chinese firms, prompting many to develop alternatives.

<details><summary>References</summary>
<ul>
<li><a href="https://www.forbes.com/sites/karlfreund/2025/04/02/ai-inference-is-king-do-you-know-which-chip-is-best/">AI Inference Is King; Do You Know Which Chip is Best? - Forbes</a></li>
<li><a href="https://www.huaweicentral.com/huawei-reveals-3-year-ascend-ai-chip-roadmap-950-coming-in-2026/">Huawei reveals 3-year Ascend AI chip roadmap, 950 coming in 2026</a></li>

</ul>
</details>

**Tags**: `#AI chip`, `#DeepSeek`, `#China`, `#semiconductor`, `#inference`

---

<a id="item-11"></a>
## [Google Voice Launches Paid Plans for Individuals with Call Recording and Gemini](http://g.co/voice/upgrade) ⭐️ 8.0/10

Google Voice has introduced two paid plans for individual users, the Starter at $10/month and the Standard at $20/month, which include call recording and Gemini AI integration for call transcription and summarization. This move opens up professional-grade communication features to freelancers and small business owners without requiring a Google Workspace subscription, potentially increasing Google Voice's competitiveness in the VoIP market. The Standard plan includes Gemini-powered call transcription, summarization, and action item generation, with automated Google Docs sent via email after calls. The Starter plan offers three-way calling, call forwarding, and desktop phone support.

telegram · zaihuapd · Jul 8, 01:00

**Background**: Google Voice has historically offered free personal numbers with limited features, while advanced capabilities like call recording and auto attendants required a Google Workspace subscription. This announcement marks the first time individual users can purchase these features directly, making them accessible to a broader audience.

**Tags**: `#Google Voice`, `#Gemini`, `#call recording`, `#paid plans`, `#small business`

---