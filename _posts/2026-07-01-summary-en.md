---
layout: default
title: "Horizon Summary: 2026-07-01 (EN)"
date: 2026-07-01
lang: en
---

> From 41 items, 14 important content pieces were selected

---

1. [Claude Code secretly embeds steganographic marks in requests](#item-1) ⭐️ 9.0/10
2. [US Lifts Export Controls on Claude Fable 5 and Mythos 5](#item-2) ⭐️ 9.0/10
3. [Claude Sonnet 5: Most Agentic Sonnet Yet, Near Opus Performance](#item-3) ⭐️ 9.0/10
4. [Anthropic Launches Claude Science for Data Science](#item-4) ⭐️ 8.0/10
5. [Kubernetes ported to browser via WebAssembly](#item-5) ⭐️ 8.0/10
6. [DIY mmWave Radar Classifies Materials for Asbestos Detection](#item-6) ⭐️ 8.0/10
7. [TokenBudgeting: Rethinking Enterprise AI Token Spend](#item-7) ⭐️ 8.0/10
8. [REAP: Automatic Curation of Coding Agent Benchmarks](#item-8) ⭐️ 8.0/10
9. [Claude Code 2.1.91 Hides Telemetry to Detect Chinese Users](#item-9) ⭐️ 8.0/10
10. [Xiaohongshu Former Employee Reports Compliance Risks Before IPO](#item-10) ⭐️ 8.0/10
11. [Google unveils Nano Banana 2 Lite and Gemini Omni Flash for developers](#item-11) ⭐️ 8.0/10
12. [Anthropic releases Claude Sonnet 4.6 with major upgrades](#item-12) ⭐️ 8.0/10
13. [Tesla Announces Supervised FSD in China](#item-13) ⭐️ 8.0/10
14. [Vercel Now Supports Dockerfile Container Deployment](#item-14) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Claude Code secretly embeds steganographic marks in requests](https://thereallo.dev/blog/claude-code-prompt-steganography) ⭐️ 9.0/10

Anthropic's Claude Code tool has been discovered to embed steganographic watermarks in its requests, likely as a measure to detect unauthorized model distillation by competitors. This practice was revealed through reverse engineering and has sparked debate over transparency and trust. This discovery undermines trust in Anthropic's transparency, as users were not informed about hidden data exfiltration. It also raises ethical and security concerns about steganographic techniques being used without disclosure in developer tools. The steganographic marks are embedded in the prompts sent to Claude's API, and the technique is reportedly crude, increasing the risk of detection. The intent appears to be identifying usage by Chinese firms engaged in model distillation, but the lack of disclosure may violate user trust and privacy expectations.

hackernews · kirushik · Jun 30, 15:44 · [Discussion](https://news.ycombinator.com/item?id=48734373)

**Background**: Steganography is the practice of hiding data within other data, such as embedding a secret message in an image or text. Model distillation is a technique where a smaller model learns from a larger one, often used to create cheaper, local versions of powerful AI models. Companies like Anthropic invest heavily in training large models and may want to prevent competitors from distilling their model's capabilities without permission.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Model_distillation">Model distillation</a></li>

</ul>
</details>

**Discussion**: Community sentiment is divided: some criticize the lack of transparency, calling it a betrayal of trust, while others argue that the intent is clear and that it does not harm normal developers. A few commenters note that the implementation is sloppy and that there are more underhanded ways to achieve the same goal. There is also a comparison to Codex CLI being open-source and thus more trustworthy.

**Tags**: `#steganography`, `#Anthropic`, `#AI ethics`, `#security`, `#transparency`

---

<a id="item-2"></a>
## [US Lifts Export Controls on Claude Fable 5 and Mythos 5](https://twitter.com/AnthropicAI/status/2072106151890809341) ⭐️ 9.0/10

The US Department of Commerce has lifted export controls on Anthropic's Claude Fable 5 and Claude Mythos 5 models, allowing broader international deployment. This policy shift marks a significant move in AI regulation, potentially impacting global access to advanced AI models and sparking debate on oversight and reliability for business-critical applications. Notably, Claude Fable 5 will initially have limited coding capabilities due to classifiers targeting cybersecurity tasks, falling back to Opus 4.8 for routine coding and debugging.

hackernews · Pragmata · Jun 30, 23:55 · [Discussion](https://news.ycombinator.com/item?id=48740771)

**Background**: Claude Fable 5 is Anthropic's most capable widely released model for demanding reasoning and long-horizon tasks, while Claude Mythos 5 is designed for finding software vulnerabilities and is available only in limited release through Project Glasswing. Export controls were initially imposed due to dual-use concerns similar to nuclear technology.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Claude_Fable_5">Claude Fable 5</a></li>
<li><a href="https://www.anthropic.com/claude/fable">Claude Fable \ Anthropic</a></li>
<li><a href="https://platform.claude.com/docs/en/about-claude/models/introducing-claude-fable-5-and-claude-mythos-5">Introducing Claude Fable 5 and Claude Mythos 5 - Claude Platform Docs</a></li>

</ul>
</details>

**Discussion**: Community sentiment is mixed: some argue that the lack of predictability undermines trust in US frontier models, while others question whether AI should be regulated like nuclear tech. A user noted the irony of lifting controls while limiting coding capabilities, and another highlighted the absence of Congressional approval in the process.

**Tags**: `#AI regulation`, `#export controls`, `#Anthropic`, `#government policy`

---

<a id="item-3"></a>
## [Claude Sonnet 5: Most Agentic Sonnet Yet, Near Opus Performance](https://t.me/zaihuapd/42280) ⭐️ 9.0/10

Anthropic released Claude Sonnet 5, which it calls the most agentic Sonnet model yet, capable of planning, using tools like browsers and terminals, and running autonomously. It outperforms Sonnet 4.6 in reasoning, tool use, coding, and knowledge work, and its performance approaches that of Opus 4.8 at a lower price. This release significantly lowers the cost of accessing near-flagship level agentic AI capabilities, potentially accelerating adoption of autonomous AI agents in development and enterprise workflows. It challenges competitors by offering strong performance at a lower price point, reshaping the LLM market's cost-performance trade-off. Claude Sonnet 5 is available immediately to all plans and becomes the default model for Free and Pro users. On the Claude Platform, a limited-time price of $2 per million input tokens and an undisclosed output token price is effective until August 31, 2026.

telegram · zaihuapd · Jul 1, 01:12

**Background**: Anthropic's Claude models are typically released in three tiers: Haiku (fastest/cheapest), Sonnet (balanced), and Opus (most capable). Agentic reasoning refers to an LLM's ability to plan, use tools, and execute tasks autonomously without constant human oversight. Sonnet 5 aims to bridge the gap between cost and agentic capability.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Claude_(language_model)">Claude (language model)</a></li>
<li><a href="https://platform.claude.com/docs/en/about-claude/models/overview">Models overview - Claude Platform Docs</a></li>
<li><a href="https://towardsdev.com/the-rise-of-agentic-reasoning-how-llms-are-evolving-from-thinkers-to-doers-3eaf896bf097">The Rise of Agentic Reasoning: How LLMs Are Evolving... | Towards Dev</a></li>

</ul>
</details>

**Discussion**: Some commenters note that for tasks requiring more than medium effort, Opus often provides better performance per cost, suggesting users should switch models rather than increasing effort levels. Others point out that Sonnet 5 underperforms in vulnerability discovery and trivia, and its cost-performance is comparable to GLM-5.2 but at twice the cost.

**Tags**: `#AI`, `#大语言模型`, `#Claude`, `#Anthropic`, `#模型发布`

---

<a id="item-4"></a>
## [Anthropic Launches Claude Science for Data Science](https://claude.com/product/claude-science) ⭐️ 8.0/10

Anthropic has launched Claude Science, a data science tool that integrates with high-performance computing (HPC) systems and databases via a local server and web-based UI. This product is significant for scientific computing, particularly in tightly regulated industries like pharma and biotech, where it enables AI-assisted data analysis on secure, institutional infrastructure. Claude Science runs a local server that connects to the user's browser, offering integrations with institutional HPC clusters and various databases. It produces auditable artifacts and supports computational design tasks, such as RNAi biopesticide design.

hackernews · lebovic · Jun 30, 17:07 · [Discussion](https://news.ycombinator.com/item?id=48735770)

**Background**: High-performance computing (HPC) is used for complex scientific simulations and data analysis, often in secure environments where external cloud connections are restricted. Data science tools like Jupyter Notebooks are common but may not integrate well with institutional clusters. Claude Science addresses this by providing a local server architecture that connects to existing HPC and database resources.

<details><summary>References</summary>
<ul>
<li><a href="https://www.anthropic.com/news/claude-science-ai-workbench">Claude Science, an AI workbench for scientists \ Anthropic</a></li>
<li><a href="https://www.technologyreview.com/2026/06/30/1139987/claude-science-is-anthropics-newest-flagship-product/">Claude Science is Anthropic’s newest flagship product</a></li>
<li><a href="https://en.wikipedia.org/wiki/High-performance_computing">High-performance computing - Wikipedia</a></li>

</ul>
</details>

**Discussion**: Community comments highlight that Claude Science's architecture (local server + web UI) is well-suited for locked-down pharma environments. A contributor who built an integrated HPC tool for Biomni noted its value beyond plotting. Users reported successful one-shot designs in RNAi biopesticide work, though with caveats about naive approaches and limited off-target screening.

**Tags**: `#AI`, `#data science`, `#HPC`, `#Anthropic`, `#scientific computing`

---

<a id="item-5"></a>
## [Kubernetes ported to browser via WebAssembly](https://ngrok.com/blog/i-ported-kubernetes-to-the-browser) ⭐️ 8.0/10

A developer at ngrok has ported a subset of Kubernetes to run entirely in the browser using WebAssembly, creating a project called Webernetes that boots a full Kubernetes cluster without any backend server components. This makes Kubernetes concepts accessible for educational purposes without requiring cloud resources, and demonstrates the growing capability of WebAssembly to run complex infrastructure software in the browser. The project reimplements core Kubernetes components like API server, scheduler, and controller manager in TypeScript compiled to WebAssembly, rather than porting the original Go code, to keep the bundle size manageable.

hackernews · peterdemin · Jun 30, 20:48 · [Discussion](https://news.ycombinator.com/item?id=48738985)

**Background**: Kubernetes is an open-source platform for automating deployment, scaling, and management of containerized applications. WebAssembly (Wasm) is a binary instruction format that enables high-performance execution in web browsers, originally designed for client-side applications but increasingly used for server-side and portable workloads. Porting Kubernetes to Wasm requires reimplementing operating system-level abstractions that the original Go code relies on.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/ngrok/webernetes">GitHub - ngrok/webernetes: Kubernetes in the browser.</a></li>

</ul>
</details>

**Discussion**: Commenters praised the educational value and noted it could improve conceptual learning, similar to previous platforms like Katacoda. Some raised concerns about maintainability due to duplicating Kubernetes source code, while others found the development workflow—using LLMs to write code and testing against real Kubernetes behavior—more interesting than the project itself.

**Tags**: `#Kubernetes`, `#WebAssembly`, `#education`, `#browser`, `#LLM`

---

<a id="item-6"></a>
## [DIY mmWave Radar Classifies Materials for Asbestos Detection](https://gauthier-lechevalier.com/radar) ⭐️ 8.0/10

A developer built a millimeter-wave (mmWave) material classification radar using Texas Instruments IWRL6432 and ESP32 boards, with a proof-of-concept that can distinguish common materials and potential application for non-intrusive asbestos detection. The project was shared as a detailed write-up including lessons learned. This project demonstrates a low-cost, open-hardware approach to material classification that could help address the widespread problem of asbestos in buildings, where current detection requires invasive sampling. It also contributes valuable engineering insights for the mmWave radar and hardware hacking community. The radar uses FMCW (Frequency-Modulated Continuous Wave) signals and machine learning on spectrograms to classify materials. The author notes that the current prototype has not yet demonstrated consistent differentiation between asbestos-containing materials and their counterparts, nor did it address concentration sensitivity.

hackernews · GL26 · Jun 30, 17:29 · [Discussion](https://news.ycombinator.com/item?id=48736137)

**Background**: Millimeter-wave radar operates in the 30-300 GHz band and can penetrate non-metallic materials, making it suitable for sensing hidden objects or material properties. FMCW radar is a common type that measures range and can be used for material classification by analyzing reflected signals. DIY radar projects often use low-cost Evaluation Modules (EVMs) like the TI IWRL6432 Boost board.

<details><summary>References</summary>
<ul>
<li><a href="https://gauthier-lechevalier.com/radar">How I built a mmWave material classification radar</a></li>
<li><a href="https://aicrier.com/post/tpq50o2kiwtxvzoa6ac2">Student builds mmWave radar for asbestos detection — AICrier</a></li>
<li><a href="https://sesamedisk.com/mmwave-radar-material-classification-industrial/">Millimeter-Wave Radar for Material - Sesame Disk</a></li>

</ul>
</details>

**Discussion**: Commenters praised the project for sharing failures and lessons learned, with one noting that such learning is invaluable. A user raised a critical point that the core feature of asbestos detection was not validated, as the POC only classified common materials. Another user suggested alternative applications like detecting discontinuities in materials for skin cancer detection.

**Tags**: `#mmWave`, `#radar`, `#material classification`, `#hardware`, `#DIY`

---

<a id="item-7"></a>
## [TokenBudgeting: Rethinking Enterprise AI Token Spend](https://newsletter.semianalysis.com/p/tokenbudgeting-our-conversations) ⭐️ 8.0/10

The article 'TokenBudgeting' questions the prevalence of token maximization (TokenMaxxing) in enterprise AI usage, suggesting that many enterprises are instead focusing on budgeting and efficient token consumption. This analysis challenges the hype around TokenMaxxing as a productivity metric, which could shift enterprise cost management strategies and AI deployment practices. The article is from SemiAnalysis, a reputable source, and reports on conversations with enterprises that indicate a focus on token budgeting rather than maximizing consumption, contrary to popular narratives.

rss · Semianalysis · Jun 30, 18:32

**Background**: TokenMaxxing is a practice where employees maximize AI token consumption to appear productive, often tracked on internal leaderboards. Tokens are units of computation used by large language models (LLMs). In contrast, TokenBudgeting emphasizes cost control and efficient use of AI resources.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Token_maxxing">Token maxxing - Wikipedia</a></li>
<li><a href="https://www.inc.com/ben-sherry/what-is-tokenmaxxing-ai-productivity-hack/91328999">What Is ‘Tokenmaxxing’? The Controversial AI Productivity Metric</a></li>

</ul>
</details>

**Tags**: `#AI`, `#token economy`, `#enterprise`, `#LLM`, `#cost management`

---

<a id="item-8"></a>
## [REAP: Automatic Curation of Coding Agent Benchmarks](https://www.reddit.com/r/MachineLearning/comments/1uk713d/reap_automatic_curation_of_coding_agent/) ⭐️ 8.0/10

REAP is an automated pipeline that curates execution-based benchmarks from real production coding assistant sessions without manual labeling. It addresses the limitations of static benchmarks by providing more relevant and diverse evaluations for AI coding agents, impacting the AI/ML and coding tools ecosystem. REAP was used to curate Harvest, a benchmark where tasks feed real developer prompts and verify code changes against fail-to-pass tests from production, spanning over four programming languages.

reddit · r/MachineLearning · /u/julian88888888 · Jul 1, 00:50

**Background**: Coding agent benchmarks are typically static and manually created, limiting their relevance. REAP automatically extracts tasks from real production usage logs, using fail-to-pass tests to verify correctness, thus improving benchmark quality.

<details><summary>References</summary>
<ul>
<li><a href="https://arxiv.org/abs/2604.01527">[2604.01527] REAP: Automatic Curation of Coding Agent ...</a></li>
<li><a href="https://arxiv.org/html/2604.01527v3">REAP: Automatic Curation of Coding Agent Benchmarks from ...</a></li>
<li><a href="https://www.semanticscholar.org/paper/REAP:-Automatic-Curation-of-Coding-Agent-Benchmarks-Jha-Paltenghi/b106bab30b9fdbf890b1fcf1a0dae725f00904a4">REAP: Automatic Curation of Coding Agent Benchmarks from ...</a></li>

</ul>
</details>

**Tags**: `#coding agents`, `#benchmarks`, `#machine learning`, `#AI evaluation`

---

<a id="item-9"></a>
## [Claude Code 2.1.91 Hides Telemetry to Detect Chinese Users](https://www.reddit.com/r/ClaudeAI/comments/1ujila1/anthropic_embedded_spyware_in_claude_code_and/) ⭐️ 8.0/10

A reverse engineer discovered that Claude Code version 2.1.91, released in April 2026, includes hidden telemetry that checks for Chinese timezones and proxy connections, then encodes the results into system prompts sent to Anthropic's API using XOR obfuscation and Unicode steganography. This raises serious transparency and privacy concerns, as the telemetry is obfuscated and undisclosed in changelogs, targeting users in China to detect unauthorized reselling or abuse without their knowledge. The telemetry uses an XOR key of 91 to obfuscate logic that checks timezones like Asia/Shanghai and proxy URLs pointing to Chinese AI labs, then alters the Unicode apostrophe in the system prompt's date field to encode the result, effectively turning the prompt into a covert data channel.

telegram · zaihuapd · Jun 30, 10:34

**Background**: XOR obfuscation is a common technique used in malware to hide malicious logic by applying a bitwise XOR operation with a key. Steganography in LLMs involves embedding hidden information in prompts or outputs without altering their apparent meaning. This incident mirrors tactics used by some RATs and malware, where configuration is hidden via XOR and Base64 encoding.

<details><summary>References</summary>
<ul>
<li><a href="https://gbhackers.com/millenium-rat-uses-base64-and-xor/">Millenium RAT Uses Base64 and XOR Configuration to Hide ...</a></li>
<li><a href="https://www.threatdown.com/blog/nowhere-to-hide-three-methods-of-xor-obfuscation/">Nowhere to Hide: Three methods of XOR obfuscation</a></li>
<li><a href="https://www.emergentmind.com/topics/steganographic-capabilities-in-llms">Steganography in LLMs: Techniques & Security</a></li>

</ul>
</details>

**Tags**: `#Claude Code`, `#telemetry`, `#privacy`, `#AI ethics`, `#reverse engineering`

---

<a id="item-10"></a>
## [Xiaohongshu Former Employee Reports Compliance Risks Before IPO](https://www.163.com/dy/article/L0M7BHUT0511ADM5.html) ⭐️ 8.0/10

Former Xiaohongshu employee Chen Hao submitted a real-name compliance complaint to the Hong Kong Stock Exchange and SFC on June 29, alleging irregularities in overseas stock options, labor compliance, and information disclosure. Xiaohongshu plans to file for a Hong Kong IPO by June 2026 at a valuation of about $31 billion. The compliance allegations come at a critical moment as Xiaohongshu prepares for a high-profile IPO, potentially affecting regulatory approval and investor confidence. The case highlights ongoing labor and stock option disputes in Chinese tech firms, underscoring the importance of ESG compliance for companies seeking overseas listings. Chen Hao previously won a court ruling for wrongful termination (190,624 RMB) and a mediation award for stock option losses (661,545 RMB). He claims nearly 50 former employees have similar grievances and demands that Xiaohongshu clarify inconsistencies in its disclosure of domestic and overseas entities, labor lawsuits, and ESG labor deficiencies.

telegram · zaihuapd · Jun 30, 13:33

**Background**: Xiaohongshu (Little Red Book) is a Chinese social commerce platform popular for user-generated content on fashion, beauty, and lifestyle. It has been rumored to plan a Hong Kong IPO for years. Stock options are often used by startups to attract talent, but disputes over vesting and termination can lead to legal conflicts. ESG (Environmental, Social, and Governance) criteria are increasingly important for companies listing in Hong Kong.

<details><summary>References</summary>
<ul>
<li><a href="https://www.163.com/dy/article/L0N3JJ7H0519A26B.html">遭“内部人”实名举报！小红书的红与黑|期权|电商|ipo|知名企业_网易订...</a></li>
<li><a href="https://www.sohu.com/a/1043825752_120321309">小红书关键时刻，前员工向港交所实名举报_期权_上市_陈浩</a></li>
<li><a href="https://www.topnews.cn/news/145CD7E447B84E75">独家丨期权临期被解约，小红书前员工维权获法院判赔85万</a></li>

</ul>
</details>

**Tags**: `#IPO`, `#compliance`, `#labor law`, `#Xiaohongshu`, `#tech regulation`

---

<a id="item-11"></a>
## [Google unveils Nano Banana 2 Lite and Gemini Omni Flash for developers](https://blog.google/innovation-and-ai/models-and-research/gemini-models/gemini-omni-flash-nano-banana-2-lite/) ⭐️ 8.0/10

Google has released Nano Banana 2 Lite, its fastest and most cost-efficient image generation model, achieving 4-second latency and costing $0.034 per 1,000 images, and Gemini Omni Flash, a video generation model available for the first time to developers at $0.10 per second of video output. These releases significantly lower the cost and latency for generative media, enabling rapid iteration in design, advertising, and social apps, and making high-quality video generation accessible to developers through an API. Nano Banana 2 Lite is now generally available in Google AI Studio, Gemini API, and the Gemini Enterprise Agent Platform, and will soon appear in consumer products like Search AI Mode and the Gemini app. Gemini Omni Flash currently supports text, image, and video inputs to generate 10-second videos, but lacks audio reference and scene extension in the API, with limited cross-scene character consistency.

telegram · zaihuapd · Jun 30, 16:14

**Background**: Generative AI models like these allow computers to create images or videos from text descriptions, often used for prototyping, content creation, and marketing. Nano Banana 2 Lite is part of Google's Gemini image model family, optimized for speed and cost efficiency, while Gemini Omni Flash is a native multimodal video generation model, trained on Google's Tensor Processing Units (TPUs), and was first announced at Google I/O 2026.

<details><summary>References</summary>
<ul>
<li><a href="https://blog.google/innovation-and-ai/models-and-research/gemini-models/gemini-omni-flash-nano-banana-2-lite/">Start building with Nano Banana 2 Lite and Gemini Omni Flash</a></li>
<li><a href="https://deepmind.google/models/gemini-image/flash-lite/">Gemini 3.1 Flash- Lite Image – Nano Banana ... — Google DeepMind</a></li>
<li><a href="https://cloud.google.com/blog/products/ai-machine-learning/nano-banana-2-lite-and-gemini-omni-flash-available/">Nano Banana 2 Lite and Gemini Omni Flash available | Google ...</a></li>

</ul>
</details>

**Tags**: `#Google AI`, `#generative models`, `#image generation`, `#video generation`, `#cost efficiency`

---

<a id="item-12"></a>
## [Anthropic releases Claude Sonnet 4.6 with major upgrades](https://t.me/zaihuapd/42277) ⭐️ 8.0/10

Anthropic released Claude Sonnet 4.6, featuring significant improvements in coding, computer use, and long-context reasoning. The model now serves as the default for Free and Pro users with a 1M token context window. This release marks a substantial upgrade to one of the leading AI assistants, enhancing its utility for developers and power users. The improved computer use capability in particular expands Claude's practical value for automating complex desktop tasks. The model's computer use ability achieved notable gains on the OSWorld benchmark, which evaluates agents on real operating system tasks. Claude Sonnet 4.6 is available via API and major cloud platforms, with pricing unchanged.

telegram · zaihuapd · Jun 30, 17:58

**Background**: Anthropic's Claude Sonnet is a mid-tier model balancing performance and cost, positioned between the lightweight Haiku and the flagship Opus. Computer use is a feature that allows Claude to navigate and control a computer interface directly, enabling automation of workflows across applications. The OSWorld benchmark tests an AI agent's ability to perform real-world computer tasks in an Ubuntu environment.

<details><summary>References</summary>
<ul>
<li><a href="https://www.anthropic.com/news/3-5-models-and-computer-use">Introducing computer use, a new Claude 3.5 Sonnet, and Claude ...</a></li>
<li><a href="https://os-world.github.io/">OSWorld : Benchmarking Multimodal Agents for Open-Ended Tasks in...</a></li>

</ul>
</details>

**Tags**: `#Anthropic`, `#Claude`, `#AI`, `#LLM`, `#Machine Learning`

---

<a id="item-13"></a>
## [Tesla Announces Supervised FSD in China](https://t.me/zaihuapd/42281) ⭐️ 8.0/10

Tesla announced on social media X that its supervised Full Self-Driving (FSD) software is now available for use in China. This marks a significant expansion of Tesla's autonomous driving technology into the world's largest auto market, potentially increasing competition with local players like Xpeng and Huawei. The supervised FSD system requires constant driver supervision and does not make the vehicle fully autonomous, as clarified in Tesla's support documentation.

telegram · zaihuapd · Jul 1, 01:22

**Background**: Tesla's Full Self-Driving (FSD) is an advanced driver-assistance system that can navigate highways and city streets, make lane changes, and follow routes. However, despite the name, it is not fully autonomous and requires a vigilant driver ready to take control at any time. The term 'Supervised' was recently adopted to emphasize this limitation.

<details><summary>References</summary>
<ul>
<li><a href="https://www.tesla.com/fsd">Full Self-Driving (Supervised) - Tesla</a></li>
<li><a href="https://www.tesla.com/support/fsd">Full Self-Driving (Supervised) | Tesla Support</a></li>
<li><a href="https://insideevs.com/news/714524/tesla-fsd-beta-supervised-name/">Tesla Full Self-Driving Comes Out Of Beta, But Must Be Supervised</a></li>

</ul>
</details>

**Tags**: `#Tesla`, `#FSD`, `#autonomous driving`, `#China`

---

<a id="item-14"></a>
## [Vercel Now Supports Dockerfile Container Deployment](https://vercel.com/blog/dockerfile-on-vercel) ⭐️ 8.0/10

Vercel has announced support for deploying Docker containers via a Dockerfile.vercel file, allowing developers to run any HTTP container on Vercel's Fluid compute platform with automatic scaling and CPU-based billing. This expands Vercel's platform beyond serverless functions to containerized applications, enabling developers to run frameworks like Rails, Spring Boot, and FastAPI seamlessly with pay-per-use pricing. The Dockerfile.vercel file must be placed at the project root; Vercel builds, stores, and deploys the image, and the service must listen on $PORT (default 80) and serve HTTP. Each git push triggers a rebuild and generates a preview URL.

telegram · zaihuapd · Jul 1, 03:58

**Background**: Vercel is a cloud platform for frontend developers, originally focused on serverless functions. Fluid compute is Vercel's execution model that handles multiple requests concurrently on a single container instance, reducing idle time. Dockerfile support allows developers to use any language or framework that can run in a container.

<details><summary>References</summary>
<ul>
<li><a href="https://vercel.com/docs/functions/container-images">Deploy OCI container images with a Dockerfile or Containerfile on...</a></li>
<li><a href="https://vercel.com/fluid">Fluid compute</a></li>

</ul>
</details>

**Tags**: `#Vercel`, `#Docker`, `#container deployment`, `#serverless`, `#cloud computing`

---