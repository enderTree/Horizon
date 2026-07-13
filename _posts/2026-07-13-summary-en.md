---
layout: default
title: "Horizon Summary: 2026-07-13 (EN)"
date: 2026-07-13
lang: en
---

> From 34 items, 8 important content pieces were selected

---

1. [GPT-5.6 Proves 50-Year-Old Graph Conjecture in One Hour](#item-1) ⭐️ 10.0/10
2. [Terry Tao explores AI coding agents for app creation](#item-2) ⭐️ 9.0/10
3. [xAI Grok CLI Uploads Entire Codebase and Secret Files by Default](#item-3) ⭐️ 9.0/10
4. [OpenAI Launches GPT-5.6 Series: Sol, Terra, Luna with Enhanced Capabilities](#item-4) ⭐️ 9.0/10
5. [World's First Invasive BCI Medical Device Approved in China](#item-5) ⭐️ 9.0/10
6. [Chromium 148 Math.tanh Enables OS Fingerprinting](#item-6) ⭐️ 8.0/10
7. [George Hotz: LLMs Create Value, But Hype Misleads Valuation](#item-7) ⭐️ 8.0/10
8. [Beijing Official Builds AI-Powered Flood App with Claude Code](#item-8) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [GPT-5.6 Proves 50-Year-Old Graph Conjecture in One Hour](https://www.qbitai.com/2026/07/447873.html) ⭐️ 10.0/10

OpenAI's GPT-5.6 Sol Ultra proved the cycle double cover conjecture, a 50-year-old open problem in graph theory, in under an hour using 64 sub-agents and a detailed 700-character prompt. The model generated a 3-page PDF of the proof. This achievement demonstrates AI's ability to perform original mathematical research autonomously, potentially revolutionizing the pace of mathematical discovery. It signals a paradigm shift in how complex theoretical problems could be approached using large language models with parallel reasoning architectures. The model used 64 parallel sub-agents to decompose the problem into edge labeling over finite fields and systems of linear equations. OpenAI also released the full prompt, which specified acceptance criteria, definitions, boundary conditions, and failure cases without prescribing fixed solution steps.

telegram · zaihuapd · Jul 12, 03:49

**Background**: The cycle double cover conjecture, posed by Szekeres and Seymour independently in the 1970s, asks whether every bridgeless undirected graph has a set of cycles that covers each edge exactly twice. Sub-agents are specialized AI components that work in parallel on different aspects of a task, orchestrated by a main agent. This approach allows large-scale reasoning with efficient resource usage.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Cycle_double_cover_conjecture">Cycle double cover conjecture</a></li>
<li><a href="https://ai-sdk.dev/docs/agents/subagents">Subagents - Agents</a></li>

</ul>
</details>

**Tags**: `#AI`, `#mathematics`, `#graph theory`, `#GPT-5.6`, `#breakthrough`

---

<a id="item-2"></a>
## [Terry Tao explores AI coding agents for app creation](https://terrytao.wordpress.com/2026/07/11/old-and-new-apps-via-modern-coding-agents/) ⭐️ 9.0/10

Terry Tao, a renowned mathematician, published a blog post on July 11, 2026, describing how modern AI coding agents like those from Cursor and Zencoder can facilitate the creation of both old-style and new applications, highlighting a vast latent demand for software. This is significant because it demonstrates how LLM-based coding agents are democratizing software creation, enabling experts from non-programming fields to build tools that were previously out of reach, potentially accelerating innovation across disciplines. Tao notes that while LLM-coded supplements are not mission-critical, the downside risk of using guided interaction with LLM agents for generating visualizations is acceptable, reflecting a balanced view of AI tools.

hackernews · subset · Jul 12, 11:09 · [Discussion](https://news.ycombinator.com/item?id=48880170)

**Background**: AI coding agents are tools that use large language models (LLMs) to assist in writing code, often through natural language prompts. Examples include Cursor, an AI-powered code editor, and Zencoder, a platform for AI code generation. These agents lower the barrier to software development, allowing users with minimal coding experience to create functional applications.

<details><summary>References</summary>
<ul>
<li><a href="https://zencoder.ai/">Zencoder | The AI Coding Agent</a></li>
<li><a href="https://cursor.com/">Cursor: AI coding agent</a></li>

</ul>
</details>

**Discussion**: The community comments express enthusiasm and humor about Tao's exploration. For instance, 'recursivedoubts' shares how LLMs boosted his CS classes, while 'luciana1u' jokes about a Fields Medalist using coding agents. 'semiquaver' emphasizes the infinite latent demand for software beyond traditional spaces, and 'wffurr' appreciates Tao's balanced perspective on the acceptable risk of using LLM agents.

**Tags**: `#AI coding agents`, `#LLMs`, `#software development`, `#education`, `#Terry Tao`

---

<a id="item-3"></a>
## [xAI Grok CLI Uploads Entire Codebase and Secret Files by Default](https://gist.github.com/cereblab/dc9a40bc26120f4540e4e09b75ffb547) ⭐️ 9.0/10

Security researchers discovered that xAI's Grok Build CLI tool (v0.2.93) uploads the entire code repository and sensitive files like .env to xAI servers by default, even with the 'improve model' setting disabled. This security flaw exposes developers' proprietary code and secrets, potentially leading to data breaches and compromising software security across projects using the tool. The tool uploads code via two channels: file contents are embedded in model conversation requests and also uploaded as a git bundle to Google Cloud Storage, with a 12 GB repository resulting in over 5 GiB uploaded.

telegram · zaihuapd · Jul 12, 04:19

**Background**: Grok Build is a terminal-based coding agent powered by xAI's Grok models, released in May 2026. It is designed to execute commands and assist with development directly from the command line. The git-bundle command packages Git objects into a single file for offline transfer, which the CLI used to send the entire repository to xAI's servers.

<details><summary>References</summary>
<ul>
<li><a href="https://x.ai/news/grok-build-cli">Introducing Grok Build | SpaceXAI</a></li>
<li><a href="https://x.ai/cli">Grok Build | SpaceXAI</a></li>
<li><a href="https://git-scm.com/docs/git-bundle">Git - git - bundle Documentation</a></li>

</ul>
</details>

**Tags**: `#安全`, `#隐私`, `#xAI`, `#CLI工具`, `#代码泄露`

---

<a id="item-4"></a>
## [OpenAI Launches GPT-5.6 Series: Sol, Terra, Luna with Enhanced Capabilities](https://t.me/zaihuapd/42512) ⭐️ 9.0/10

OpenAI has officially released the GPT-5.6 series, introducing three distinct models—Sol (flagship), Terra (balanced), and Luna (low-cost)—each optimized for different performance and cost trade-offs. The series brings significant improvements in coding, knowledge work, design, scientific research, and cybersecurity, along with new features like max/ultra reasoning, multi-agent collaboration, and Programmatic Tool Calling. This release expands OpenAI's model lineup to better serve diverse use cases, from high-performance tasks to cost-sensitive deployments, making advanced AI more accessible. The introduction of multi-agent collaboration and programmatic tool calling signals a shift toward more autonomous and efficient AI workflows, potentially transforming how developers build complex applications. Pricing per 1M tokens is $5/$30 for Sol, $2.50/$15 for Terra, and $1/$6 for Luna (input/output). The bare gpt-5.6 API alias defaults to Sol, but explicit model IDs are gpt-5.6-sol, gpt-5.6-terra, and gpt-5.6-luna. Programmatic Tool Calling allows models to write code that calls tools within a sandbox environment, reducing API round-trips.

telegram · zaihuapd · Jul 12, 11:19

**Background**: OpenAI's GPT-5.6 series is a family of large language models that build on previous GPT generations. The three tiers—Sol, Terra, Luna—let users choose the best balance of intelligence, speed, and cost for their applications. Multi-agent collaboration involves multiple AI agents coordinating to solve complex tasks, while Programmatic Tool Calling enables models to programmatically invoke external tools via code, improving efficiency and reliability.

<details><summary>References</summary>
<ul>
<li><a href="https://openai.com/index/previewing-gpt-5-6-sol/">Previewing GPT-5.6 Sol: a next-generation model | OpenAI</a></li>
<li><a href="https://www.mindstudio.ai/blog/what-is-gpt-5-6-soul-terra-luna-explained">What Is GPT-5.6? OpenAI's Soul, Terra, and Luna Model Tiers Explained | MindStudio</a></li>
<li><a href="https://www.vellum.ai/blog/gpt-5-6-benchmarks-explained">GPT-5.6 Sol vs Terra vs Luna: Which Tier Should You Actually Use?</a></li>

</ul>
</details>

**Tags**: `#GPT`, `#OpenAI`, `#AI models`, `#machine learning`, `#natural language processing`

---

<a id="item-5"></a>
## [World's First Invasive BCI Medical Device Approved in China](https://t.me/zaihuapd/42515) ⭐️ 9.0/10

China's National Medical Products Administration (NMPA) has approved the world's first invasive brain-computer interface (BCI) medical device, the 'Implantable BCI Hand Motor Function Compensation System' developed by Broturn Medical Technology (Shanghai) Co., Ltd., for clinical use in quadriplegic patients with cervical spinal cord injury. This approval marks a paradigm shift in neurotechnology, moving invasive BCIs from research labs to approved clinical devices, potentially restoring hand function and improving quality of life for paralyzed patients worldwide. The device uses minimally invasive epidural implantation and wireless power and communication technology, connected to a pneumatic glove that helps patients aged 18-60 with quadriplegia perform hand grasping movements. Clinical trials showed significant improvement in hand grasping ability.

telegram · zaihuapd · Jul 12, 14:39

**Background**: Invasive brain-computer interfaces (BCIs) are surgically implanted devices that establish a direct communication pathway between the brain and an external device. Traditional invasive BCIs require opening the skull and implanting electrodes into brain tissue, but this new device uses a minimally invasive epidural approach—placing electrodes on the dura mater without penetrating the brain. Wireless power and data communication eliminate the need for transcutaneous wires, reducing infection risk.

<details><summary>References</summary>
<ul>
<li><a href="https://flcube.com/?p=59388">China NMPA Approves World's First Invasive BCI Medical Device...</a></li>
<li><a href="https://en.wikipedia.org/wiki/Brain–computer_interface">Brain–computer interface - Wikipedia</a></li>

</ul>
</details>

**Tags**: `#brain-computer interface`, `#medical device`, `#neurotechnology`, `#spinal cord injury`, `#China`

---

<a id="item-6"></a>
## [Chromium 148 Math.tanh Enables OS Fingerprinting](https://scrapfly.dev/posts/browser-math-os-fingerprint/) ⭐️ 8.0/10

Since Chromium 148, the Math.tanh function in V8 now uses the host operating system's libm implementation instead of a bundled routine, making it possible to fingerprint the underlying OS by measuring differences in floating-point computation results. This opens a new, hard-to-spoof browser fingerprinting vector that can silently detect a user's OS even if they change user-agent strings, raising significant privacy concerns for users and complicating anti-fingerprinting efforts. Only Math.tanh among JavaScript math functions leaks OS information because Chrome 148 replaced its implementation with platform-specific std::tanh; other functions like Math.cos remain consistent across platforms. Additionally, CSS trigonometric functions and Web Audio API exhibit similar platform-dependent behavior.

hackernews · joahnn_s · Jul 12, 21:12 · [Discussion](https://news.ycombinator.com/item?id=48884853)

**Background**: Browser fingerprinting collects device and software attributes to identify users without cookies. Traditionally, techniques rely on screen resolution, fonts, or User-Agent strings. Math.tanh fingerprinting exploits subtle differences in how operating systems compute transcendental functions due to varying math libraries and CPU architectures, creating a consistent signature for each platform.

<details><summary>References</summary>
<ul>
<li><a href="https://scrapfly.dev/posts/browser-math-os-fingerprint/">Your Browser Does Math Differently on Every OS , and Anti-Bot...</a></li>
<li><a href="https://news.ycombinator.com/item?id=48884853">Since Chromium 148, Math.tanh is now fingerprintable to link underlying OS | Hacker News</a></li>
<li><a href="https://asibiont.com/en/blog/since-chromium-148-math-tanh-teper-mozhno-ispolzovat-dlya-privyazki-k-os-chto-eto-znachit-dlya-veb-razrabotchikov">Chromium 148 : How Math . tanh Became... — ASI Biont Blog</a></li>

</ul>
</details>

**Discussion**: Community comments note that this fingerprinting vector may also reveal browser version range, not just OS. Some question the motives behind the write-up, suspecting anti-bot companies may benefit from getting these techniques fixed. Others suggest this underscores the need for correctly rounded transcendental functions across platforms.

**Tags**: `#browser fingerprinting`, `#privacy`, `#Chromium`, `#Math.tanh`, `#web security`

---

<a id="item-7"></a>
## [George Hotz: LLMs Create Value, But Hype Misleads Valuation](https://geohot.github.io//blog/jekyll/update/2026/07/12/i-love-llms.html) ⭐️ 8.0/10

George Hotz published a blog post arguing that while large language models generate enormous value, frontier AI labs may fail to capture that value, and that LLMs are shifting open source dynamics toward private forks rather than upstream contributions. This perspective challenges the high valuations of frontier labs like OpenAI and Anthropic, suggesting that value creation does not guarantee value capture, which has implications for investors and the AI industry. It also highlights a nuanced impact on open source software, where LLMs make forking so easy that it may reduce collaborative upstreaming. The post emphasizes that LLMs are being used to build one-off, stripped-down software for specific personal use cases, leading to a 'have it your way' era where forking is preferred over contributing upstream. Hotz also notes that frontier model subscription prices ($100–$200/month) are still cost-effective, but the value flows to users, not necessarily to the model providers.

hackernews · therepanic · Jul 12, 18:31 · [Discussion](https://news.ycombinator.com/item?id=48883343)

**Discussion**: Commenters broadly agree with Hotz's value capture argument, noting that productivity gains from LLMs lead to private tools rather than public contributions. Some express concern about the future of open source, while others mention that newer models like Sonnet 4 and Opus 4.5 feel like step changes, accelerating progress and making timelines uncertain.

**Tags**: `#LLM`, `#open source`, `#hype`, `#valuation`, `#productivity`

---

<a id="item-8"></a>
## [Beijing Official Builds AI-Powered Flood App with Claude Code](https://www.xieyunshi.com/blog/?id=11) ⭐️ 8.0/10

Xie Yunshi, deputy director of the Beijing Miyun branch of the Municipal Planning and Natural Resources Commission, purchased 10 billion tokens and spent a month developing a flood prevention app called 'Jiaoying' using Claude Code. This demonstrates a novel real-world application of AI coding tools in the public sector for public safety, potentially inspiring other government officials to leverage AI for local disaster response. The app integrates geological hazard points, threatened households, and support personnel information, with real-time updates on mountain warnings, rain changes, and evacuation status, and supports one-click navigation to hazard points.

telegram · zaihuapd · Jul 12, 15:16

**Background**: Claude Code is an AI coding agent developed by Anthropic that can understand codebases, edit files, and run commands. In AI, tokens are the smallest units of text processed by language models; 10 billion tokens represent a substantial amount of computation for a personal project.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Claude_Code">Claude Code</a></li>
<li><a href="https://blogs.nvidia.com/blog/ai-tokens-explained/">What Are AI Tokens ? The Language and Currency... | NVIDIA Blog</a></li>
<li><a href="https://claude.com/product/claude-code">Claude Code by Anthropic | AI Coding Agent, Terminal, IDE</a></li>

</ul>
</details>

**Tags**: `#AI coding`, `#disaster response`, `#Claude Code`, `#public sector`, `#innovation`

---