---
layout: default
title: "Horizon Summary: 2026-08-01 (EN)"
date: 2026-08-01
lang: en
---

> From 37 items, 9 important content pieces were selected

---

1. [Elevator Algorithms Explored: SCAN, LOOK, and the Destination Dispatch Debate](#item-1) ⭐️ 8.0/10
2. [YC Releases QM, a Multiplayer Agent Harness for Work](#item-2) ⭐️ 8.0/10
3. [Tailscale Postmortem: Reusable Auth Key Enabled Hugging Face Intrusion](#item-3) ⭐️ 8.0/10
4. [DeepSeek Releases V4-Flash-0731, a 304B-Parameter Agentic Model](#item-4) ⭐️ 8.0/10
5. [Stateless MCP sparks renewed interest and new projects](#item-5) ⭐️ 8.0/10
6. [Trump Administration Weighs $100,000 Fee for Foreign Students' Post-Grad Work](#item-6) ⭐️ 8.0/10
7. [MiniMax to Open-Source H3 Multimodal Video Model on August 3](#item-7) ⭐️ 8.0/10
8. [Supreme Court Declines AI Copyright Case, Upholds Human Authorship](#item-8) ⭐️ 8.0/10
9. [Google Confirms Free and Paid Tiers for Android Developer Verification, Withholds Developer List](#item-9) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Elevator Algorithms Explored: SCAN, LOOK, and the Destination Dispatch Debate](https://john.fun/elevators) ⭐️ 8.0/10

A new analytical article on john.fun examines elevator scheduling algorithms including SCAN, LOOK, and destination dispatch, sparking a Hacker News discussion with 961 points and 238 comments. The piece compares algorithm performance under random versus real-world travel patterns. Elevator scheduling affects billions of rides every day, yet it is rarely analyzed in depth. This discussion bridges computer science concepts like disk scheduling with real-world building behavior, informing how future elevators could be optimized. The article notes that destination dispatch can be worse than LOOK under random destinations, though real buildings often have biased travel patterns, such as large groups heading to the same floor. Commenters connected the SCAN algorithm to hard-drive disk scheduling and recommended the Elevator Saga simulation game.

hackernews · Jrh0203 · Jul 31, 15:17 · [Discussion](https://news.ycombinator.com/item?id=49124218)

**Background**: The elevator algorithm, also known as SCAN, is a disk-scheduling algorithm that moves the read/write head in one direction until no more requests require service, then reverses. LOOK is a variant that only travels as far as the highest or lowest pending request. Destination dispatch uses keypads outside the elevator so passengers select their destination floor before boarding, allowing the system to group passengers in real time. These concepts come from operating systems and building engineering.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Elevator_algorithm">Elevator algorithm - Wikipedia</a></li>
<li><a href="https://dev.to/thesaltree/elevator-scheduling-algorithms-fcfs-sstf-scan-and-look-2pae">Elevator Scheduling Algorithms: FCFS, SSTF, SCAN, and LOOK Elevator Algorithms: SCAN, LOOK, and RSR Explained SCAN (Elevator) Disk Scheduling Algorithms - GeeksforGeeks Difference between SCAN and LOOK Disk scheduling algorithms Elevator algorithm - Wikipedia Elevators - john.fun Elevator algorithm — Grokipedia</a></li>
<li><a href="https://elsolitario.org/en/2026/07/31/elevator-algorithms-scan-look-rsr/">Elevator Algorithms: SCAN, LOOK, and RSR Explained</a></li>

</ul>
</details>

**Discussion**: The Hacker News comments were largely positive and constructive. One user noted that HDDs behave like a 'long elevator' and mentioned SCAN as a disk-scheduling algorithm; another observed that destination dispatch underperforms in random simulations but real buildings often have biased traffic, like lunchtime groups. Several commenters shared the Elevator Saga game and complained that passengers commonly press both up and down buttons, which degrades algorithm performance.

**Tags**: `#elevator-algorithms`, `#scheduling`, `#simulation`, `#hn-discussion`, `#optimization`

---

<a id="item-2"></a>
## [YC Releases QM, a Multiplayer Agent Harness for Work](https://github.com/yc-software/qm) ⭐️ 8.0/10

YC has released qm, an open-source multiplayer agent harness for work that lets several people supervise the same long-running agent work. It supports per-person scopes and shared rooms for company-wide assistant collaboration, with both strict and auto approval modes for tool calls. QM addresses one of the hardest problems in multiplayer agents—scoping—while enabling shared workspaces for teams. It validates a growing trend toward shared AI-agent control planes and gives companies a harness they can run outside the sandbox, keeping credentials and LLM API keys in the loop rather than the environment. The harness runs outside the sandbox so credentials stay out of the agent environment, while the loop holds LLM API keys, user tokens, and database access. Deployment can point the Auto-mode screening classifier at its own proxy, and every harness tool call pauses for human approval in Strict mode.

hackernews · tosh · Jul 31, 18:04 · [Discussion](https://news.ycombinator.com/item?id=49126604)

**Background**: A multi-agent harness is infrastructure that orchestrates one or more AI agents, managing their tools, permissions, and human oversight—crucially, the loop holds credentials and context so agents can safely perform tasks. Multiplayer agents extend this to teams, where several people supervise the same long-running agent work, which requires careful scoping to avoid privilege misuse. Recent tools such as Agent Room and shared workspaces reflect a shift toward practical control layers for multi-agent collaboration.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/yc-software/qm">GitHub - yc-software/qm: Multiplayer agent harness for work · GitHub</a></li>
<li><a href="https://www.mendral.com/blog/multi-player-agents-sandbox">Multi - Player Agents Don't Fit in the Sandbox | Mendral</a></li>
<li><a href="https://insights.reinventing.ai/articles/ai-agents-shared-workspaces-small-teams-2026-06-01">Shared AI Agent Workspaces Become a Practical Control Layer ...</a></li>

</ul>
</details>

**Discussion**: Commenters largely praised qm's approach to scoping, calling it 'a sane answer for a company-wide assistant,' but some questioned how it compares to established tools like Claude Cowork and requested a 'QM vs Cowork' comparison. Others noted adjacent projects (Buzz, AQ, gstack) and raised questions about Hermes or 'openclaw'-style agent systems.

**Tags**: `#AI agents`, `#multiplayer`, `#developer tools`, `#YC`, `#agent harness`

---

<a id="item-3"></a>
## [Tailscale Postmortem: Reusable Auth Key Enabled Hugging Face Intrusion](https://tailscale.com/blog/hugging-face-intrusion) ⭐️ 8.0/10

Tailscale published a postmortem of the Hugging Face intrusion, revealing that no Tailscale vulnerabilities were exploited. Instead, a reusable auth key stored in an environment file allowed an attacker to enroll unauthorized nodes into Hugging Face's tailnet. This incident demonstrates that even with a secure mesh VPN, poor credential management can lead to serious breaches. It underscores the need for robust alerting, ephemeral auth keys, and strict access controls, impacting all organizations relying on Tailscale or similar zero-config VPN solutions. The reusable auth key was used over several days to enroll a total of 181 nodes into Hugging Face's tailnet, each receiving a CI node identity tag. Tailscale highlighted this as an alerting gap, and community experts suggest scoping credentials to specific origins/destinations and using one-off, ephemeral keys to mitigate such risks.

hackernews · bluehatbrit · Jul 31, 19:03 · [Discussion](https://news.ycombinator.com/item?id=49127306)

**Background**: Tailscale is a software-defined mesh VPN that enables secure, zero-configuration connectivity between devices. Auth keys are used to authenticate and provision devices; reusable keys remain valid across multiple enrollments, so if exposed they can be exploited. Best practices include using ephemeral, single-use keys and avoiding storing them in insecure files or shell histories.

<details><summary>References</summary>
<ul>
<li><a href="https://tailscale.com/docs/features/access-control/auth-keys">Auth keys · Tailscale Docs</a></li>
<li><a href="https://tailscale.com/docs/features/access-control/auth-keys/how-to/secure-auth-keys">Securely handle an auth key · Tailscale Docs</a></li>
<li><a href="https://en.wikipedia.org/wiki/Tailscale">Tailscale</a></li>

</ul>
</details>

**Discussion**: Comments generally praise Tailscale for its transparency, though some view the article as clever marketing that highlights Hugging Face's mistake. Others discuss technical improvements such as a security checkup feature and binding auth keys to specific machine properties, while one commenter suggests the incident reveals a need for better alerting on unusual node enrollment patterns.

**Tags**: `#security`, `#tailscale`, `#credentials`, `#postmortem`, `#vpn`

---

<a id="item-4"></a>
## [DeepSeek Releases V4-Flash-0731, a 304B-Parameter Agentic Model](https://simonwillison.net/2026/Jul/31/deepseek-v4-flash-0731/#atom-everything) ⭐️ 8.0/10

DeepSeek released DeepSeek-V4-Flash-0731, a 304-billion-parameter model with substantially enhanced agentic capabilities, available on Hugging Face. It is priced at $0.14 per million input tokens and $0.27 per million output tokens, and ranks ahead of MiniMax M3 on the Artificial Analysis Intelligence Index. This release may currently offer the best value-per-intelligence among major models, combining strong benchmark performance with dramatically lower cost than rivals. It makes high-end agentic reasoning more accessible to developers and could intensify price competition in the LLM market. The 167GB model can be run with configurable reasoning effort; Simon Willison found that raising the reasoning level to 'high' produced much better results than the default. A scatter plot from Artificial Analysis shows it with an intelligence score of about 50 at roughly $0.028 per task, on the far left of the most attractive cost-performance quadrant.

rss · Simon Willison · Jul 31, 23:59

**Background**: DeepSeek is a Chinese AI lab known for open-weight models such as DeepSeek-V3 and R1, which have challenged Western LLM leaders on performance and price. The Artificial Analysis Intelligence Index aggregates multiple benchmarks into a single score for comparing model intelligence, while cost-per-task measures pricing relative to intelligence. Agentic AI refers to models that can autonomously plan and execute multi-step tasks, a frontier capability increasingly emphasized in new releases.

<details><summary>References</summary>
<ul>
<li><a href="https://artificialanalysis.ai/models/">Comparison of AI Models across Intelligence, Performance, and Price</a></li>
<li><a href="https://www.ibm.com/think/topics/agentic-ai">What is Agentic AI? | IBM</a></li>
<li><a href="https://analyticalinsider.ai/blog/top-50-llm-comparison-price-performance-2026">Top 50 LLM Comparison: Price vs Performance 2026 (With Value Scores) | Analytical Insider</a></li>

</ul>
</details>

**Tags**: `#AI`, `#DeepSeek`, `#LLM`, `#model release`, `#agentic`

---

<a id="item-5"></a>
## [Stateless MCP sparks renewed interest and new projects](https://simonwillison.net/2026/Jul/31/stateless-mcp/#atom-everything) ⭐️ 8.0/10

Simon Willison reports that the 2026-07-28 Model Context Protocol specification, which makes MCP stateless, is the protocol's most significant change since its launch. The update reignited his interest and led him to build mcp-explorer, a CLI tool for interactively probing MCP servers, along with datasette-mcp. The stateless design eliminates the need for servers to maintain session state, making MCP far simpler to implement and deploy at scale. This could boost adoption of MCP as a standard for LLM tool integration, especially for smaller models and auditable agent setups. The new stateless flow requires a single HTTP request using the MCP-Protocol-Version and Mcp-Method headers, replacing the legacy two-step initialize-then-call sequence that relied on an Mcp-Session-Id. This simplifies client and server implementations and removes the need to route requests to the same backend instance.

rss · Simon Willison · Jul 31, 23:13

**Background**: The Model Context Protocol, introduced by Anthropic in November 2024, is an open standard for connecting AI applications like LLMs to external tools and data sources. It gained huge popularity in 2025 before being somewhat eclipsed by Anthropic's Skills approach. Stateless protocols generally offer better visibility, reliability, and scalability because the server does not need to store session state between requests.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Stateless_protocol">Stateless protocol</a></li>
<li><a href="https://en.wikipedia.org/wiki/Model_Context_Protocol">Model Context Protocol</a></li>

</ul>
</details>

**Discussion**: In the Hacker News thread about the stateless MCP specification, infrastructure operators voiced strong support, with at least one gateway maintainer noting that a large share of their bugs stemmed from the need to maintain server-side session state.

**Tags**: `#MCP`, `#AI agents`, `#protocol`, `#LLM`, `#developer tools`

---

<a id="item-6"></a>
## [Trump Administration Weighs $100,000 Fee for Foreign Students' Post-Grad Work](https://www.bloomberg.com/news/articles/2026-07-30/trump-weighs-100-000-fee-for-foreign-students-to-work-post-grad) ⭐️ 8.0/10

The Trump administration is considering charging international students a $100,000 fee to work in the U.S. after graduation through Optional Practical Training (OPT). The proposal is under discussion but has not yet been formally announced as policy. If implemented, the fee could severely impact universities that depend on international student tuition and tech and financial firms that hire international graduates. Nearly 300,000 international students held OPT status last fall, making this a major shift in the U.S. talent pipeline. The fee would apply to the OPT program, which allows F-1 students to work for up to 12 months (or 24 months with a STEM extension) in their field of study. The administration also proposed a similar fee for H-1B visas, but a federal judge ruled it unlawful in June; the White House is appealing.

telegram · zaihuapd · Jul 31, 09:00

**Background**: OPT is a temporary employment authorization that allows F-1 international students to gain practical work experience in the U.S. directly related to their major, and often serves as a stepping stone to the H-1B visa. The H-1B visa lets U.S. employers hire foreign professionals in specialty occupations requiring at least a bachelor's degree. Recent administration moves, such as shortening student visa stay limits to four years, reflect a broader tightening of international student policies.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Optional_Practical_Training">Optional Practical Training - Wikipedia</a></li>
<li><a href="https://www.uscis.gov/working-in-the-united-states/students-and-exchange-visitors/optional-practical-training-opt-for-f-1-students">Optional Practical Training (OPT) for F-1 Students - USCIS</a></li>
<li><a href="https://en.wikipedia.org/wiki/H-1B_visa">H-1B visa - Wikipedia</a></li>

</ul>
</details>

**Tags**: `#immigration policy`, `#international students`, `#tech workforce`, `#OPT`, `#H-1B`

---

<a id="item-7"></a>
## [MiniMax to Open-Source H3 Multimodal Video Model on August 3](https://modelscope.cn/models/MiniMax/MiniMax-H3) ⭐️ 8.0/10

MiniMax announced that its next-generation general-purpose multimodal video model, H3, will be open-sourced on the ModelScope community on August 3. The model natively supports understanding and generation across text, image, audio, and video modalities. This release brings a frontier-class open-weight video generation model with native audio and multi-reference support to the open-source AI ecosystem, potentially enabling high-quality, production-ready content creation for film, advertising, e-commerce, and gaming without relying on closed commercial APIs. According to early documentation, MiniMax H3 can generate up to 2K resolution, 15-second videos with native stereo audio. It accepts up to 9 reference images for subject and style, 3 video clips for motion, and 3 audio clips for guidance, and offers multi-dimensional precise editing controls.

telegram · zaihuapd · Jul 31, 12:37

**Background**: Open-sourcing a model means releasing its weights and code for public use, modification, and study, often via platforms like Alibaba's ModelScope community, which provides model hosting, inference, and deployment tools. MiniMax is a Chinese AI company building foundation models across text, image, audio, and video. Multimodal video models like H3 aim to unify understanding and generation across multiple input and output types, enabling tasks such as generating a coherent video from an image, a style reference, audio clips, and a text prompt.

<details><summary>References</summary>
<ul>
<li><a href="https://fal.ai/minimax-h3">MiniMax H3 - Open-Weights General-Purpose Multimodal Video Model | fal</a></li>
<li><a href="https://www.minimax.io/blog/minimax-h3">MiniMax H3: An Open Model Breaking the Boundaries Between Tasks and Modalities - MiniMax Research | MiniMax</a></li>
<li><a href="https://modelscope.ai/home">Home Page · ModelScope</a></li>

</ul>
</details>

**Tags**: `#AI`, `#multimodal`, `#video generation`, `#open-source`, `#MiniMax`

---

<a id="item-8"></a>
## [Supreme Court Declines AI Copyright Case, Upholds Human Authorship](https://t.me/zaihuapd/42900) ⭐️ 8.0/10

On March 2, the U.S. Supreme Court declined to hear Stephen Thaler's appeal, letting stand lower court rulings that AI-generated works are not copyrightable because copyright law requires human authorship. This decision clarifies, for now, that purely AI-created works cannot claim copyright protection in the U.S., affecting artists, technologists, and businesses relying on generative AI. It reinforces a legal barrier that could shape how AI outputs are used and commercialized as AI tools become more common. The case involved Thaler's AI system DABUS, which autonomously created a visual artwork, but the Copyright Office and lower courts rejected the application for lack of a human author. The Supreme Court's refusal to hear the appeal is a procedural action, not a ruling on the merits, though it leaves the human-author requirement intact for now.

telegram · zaihuapd · Jul 31, 13:11

**Background**: DABUS (Device for the Autonomous Bootstrapping of Unified Sentience) is an AI system developed by Stephen Thaler that reportedly conceived novel products and artwork autonomously. Thaler has also pursued patent protection for DABUS-generated inventions in multiple countries, sparking global debates over whether AI can be named an inventor. Under U.S. copyright law, protection generally requires human authorship, a principle derived from the Constitution’s goal of promoting creative progress by granting rights to authors.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/DABUS">DABUS - Wikipedia</a></li>
<li><a href="https://www.linkedin.com/pulse/can-ai-inventor-global-dabus-rulings-future-patent-law-devak-bhardwaj-0cuif">Can an AI Be an "Inventor"? The Global DABUS Rulings and the...</a></li>
<li><a href="https://www.linklaters.com/en/insights/blogs/digilinks/2023/december/ai-systems-cannot-be-patent-inventors">AI systems cannot be patent inventors</a></li>

</ul>
</details>

**Tags**: `#AI`, `#copyright`, `#legal`, `#intellectual property`, `#generative AI`

---

<a id="item-9"></a>
## [Google Confirms Free and Paid Tiers for Android Developer Verification, Withholds Developer List](https://t.me/zaihuapd/42911) ⭐️ 8.0/10

Google has confirmed that Android 16 will introduce a developer verification system requiring developers of sideloaded apps to register their package name and signing key. Verification will have a $25 paid tier matching the Google Play registration fee and a free email-based tier with installation limits. This is a major platform policy change because it extends Google's oversight to apps installed outside the Play Store, affecting open-source stores like F-Droid and user privacy. The decision to collect developer personal data without publishing a developer list may create new censorship and autonomy concerns for the Android ecosystem. The verification uses cloud-based checks, which may require a network connection and could disrupt offline sideloading workflows. Google's documentation states that, starting in September 2026, apps from participating stores in select regions must be registered by a verified developer to install on certified Android devices.

telegram · zaihuapd · Aug 1, 03:08

**Background**: Sideloading is the practice of installing Android apps from outside Google Play, commonly used by users of open-source repositories such as F-Droid. App signing keys are cryptographic credentials that identify the developer of an app, and Google's new system requires these to be pre-registered. Google says the verification is intended to deter malware and scams, but critics worry it centralizes control over independently distributed software.

<details><summary>References</summary>
<ul>
<li><a href="https://developer.android.com/developer-verification">Android developer verification | Android Developers</a></li>
<li><a href="https://support.google.com/android-developer-console/answer/16561738?hl=en">Understanding Android developer verification - Google Help</a></li>
<li><a href="https://en.wikipedia.org/wiki/F-Droid">F-Droid</a></li>

</ul>
</details>

**Discussion**: Reddit discussions show concern that the new verification could effectively end F-Droid and other free app sources, with users questioning whose safety the policy really serves. Some posts ask directly whether F-Droid is now in danger, reflecting anxiety about the future of open-source distribution.

**Tags**: `#Android`, `#sideloading`, `#privacy`, `#developer verification`, `#open-source`

---