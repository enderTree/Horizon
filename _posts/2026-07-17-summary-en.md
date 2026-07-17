---
layout: default
title: "Horizon Summary: 2026-07-17 (EN)"
date: 2026-07-17
lang: en
---

> From 43 items, 12 important content pieces were selected

---

1. [Thinking Machines Lab Releases Inkling Open-Weights MoE Model](#item-1) ⭐️ 9.0/10
2. [Japan to Buy 27,500 Nvidia Rubin Chips for Robot AI](#item-2) ⭐️ 9.0/10
3. [Kimi K3: Open Frontier Intelligence Model with High Pricing](#item-3) ⭐️ 8.0/10
4. [LM Studio Launches Bionic: AI Agent for Local Open Models](#item-4) ⭐️ 8.0/10
5. [Decoy Font: Adversarial Typeface Confuses AI OCR](#item-5) ⭐️ 8.0/10
6. [Roc Compiler Rewrite from Rust to Zig Progress Report](#item-6) ⭐️ 8.0/10
7. [LLM Critics Are Right, Yet I Keep Using Them](#item-7) ⭐️ 8.0/10
8. [Codex Bug Can Delete User Files in Full Access Mode](#item-8) ⭐️ 8.0/10
9. [Linus Torvalds Defends AI Use in Linux Kernel](#item-9) ⭐️ 8.0/10
10. [ExTernD: Ternary Decomposition with Expanded Rank for LLM PTQ](#item-10) ⭐️ 8.0/10
11. [1Password Launches Claude Integration for Safe AI Login](#item-11) ⭐️ 8.0/10
12. [Truth Social to Sell Fast Access to Trump's Posts to Wall Street](#item-12) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Thinking Machines Lab Releases Inkling Open-Weights MoE Model](https://simonwillison.net/2026/Jul/16/inkling/#atom-everything) ⭐️ 9.0/10

Thinking Machines Lab, led by Mira Murati, released Inkling, an open-weights Mixture-of-Experts model with 975 billion total parameters and 41 billion active, trained on 45 trillion tokens of multimodal data. They also announced Inkling-Small (276B total, 12B active) for future release. This is a significant contribution to the open-weights AI ecosystem, providing a large, permissively licensed model (Apache-2.0) that can be fine-tuned via the Tinker platform. It strengthens US open-weights efforts against Chinese competitors and enables broader access to multimodal capabilities. The model card and training data documentation are notably sparse, lacking detailed information. Inkling is not a frontier model but is positioned as a strong base for customization via fine-tuning, with efficient inference due to its MoE architecture.

rss · Simon Willison · Jul 16, 15:35

**Background**: A Mixture-of-Experts (MoE) model uses multiple specialized sub-networks activated per input token, which improves efficiency by only using a fraction of parameters per forward pass. Open-weights models release the trained parameters publicly, allowing anyone to download, run, study, and modify the model, unlike fully closed models like GPT-4 or Gemini.

<details><summary>References</summary>
<ul>
<li><a href="https://datanorth.ai/blog/what-is-mixture-of-experts-moe-and-why-does-it-matter">What is mixture of experts (MoE) and why does it matter?</a></li>
<li><a href="https://opensource.org/ai/open-weights">Open Weights: not quite what you’ve been told</a></li>

</ul>
</details>

**Tags**: `#AI`, `#open-source`, `#machine learning`, `#language model`, `#Mixture-of-Experts`

---

<a id="item-2"></a>
## [Japan to Buy 27,500 Nvidia Rubin Chips for Robot AI](https://www.bloomberg.com/news/articles/2026-07-16/japan-to-buy-nvidia-rubin-chips-to-build-sovereign-ai-for-robots) ⭐️ 9.0/10

Japan plans to purchase 27,500 of Nvidia's next-generation Rubin chips to build a sovereign AI for robotics, led by new company Noetra and backed by $24 billion in government funding. This massive investment aims to reduce Japan's dependency on US and Chinese AI technologies, positioning the country as a 'third option' in global AI development and targeting over 30% of the global robotics market by 2040. Noetra will build a large data center and develop a domestic base AI model for robotics, with the first model expected by March 2027 and a robot-specific version in a few years; partners include SoftBank, Toyota-backed Preferred Networks, and NEC.

telegram · zaihuapd · Jul 16, 10:59

**Background**: Sovereign AI refers to a nation's ability to develop and control its own AI infrastructure and capabilities, reducing reliance on foreign providers. Nvidia's Rubin architecture, unveiled at CES 2026, is the successor to Blackwell, offering significant leaps in computational power for AI workloads. Japan's move mirrors a global trend where countries invest in domestic AI to ensure economic and national security.

<details><summary>References</summary>
<ul>
<li><a href="https://www.linkedin.com/posts/theodoreaggelopoulos_nvidia-launches-powerful-new-rubin-chip-architecture-activity-7414286177656119296-o6T0">Nvidia launches powerful new Rubin chip architecture | TechCrunch</a></li>
<li><a href="https://hai.stanford.edu/news/ai-sovereigntys-definitional-dilemma">AI Sovereignty's Definitional Dilemma | Stanford HAI</a></li>
<li><a href="https://www.weforum.org/stories/2024/04/sovereign-ai-what-is-ways-states-building/">Sovereign AI: What it is, and 6 ways states are building it | World Economic Forum</a></li>

</ul>
</details>

**Tags**: `#NVIDIA`, `#Rubin`, `#Japan`, `#sovereign AI`, `#robotics`

---

<a id="item-3"></a>
## [Kimi K3: Open Frontier Intelligence Model with High Pricing](https://www.kimi.com/blog/kimi-k3) ⭐️ 8.0/10

Moonshot AI released Kimi K3, an open-weight frontier AI model with 2.8 trillion parameters, claiming it to be their most capable model yet and competitive with top frontier models. Kimi K3 represents a significant entry from a Chinese AI lab into the frontier intelligence space, potentially pressuring pricing and highlighting the strategic shift toward commoditizing AI capabilities. The model has a 1 million token context window and pricing of $3 per million input tokens and $15 per million output tokens, which is extremely high for an open-weight model but aligned with Anthropic's Sonnet series.

hackernews · vincent_s · Jul 16, 14:46 · [Discussion](https://news.ycombinator.com/item?id=48935342)

**Background**: Open-weight models refer to AI models whose trained parameters are publicly released, allowing developers to use and fine-tune them. Frontier intelligence denotes the most advanced, general-purpose AI models available. The release of Kimi K3 continues the trend of Chinese AI labs producing competitive models, but here the pricing is notably high.

**Discussion**: Comments note that Kimi K3's pricing is extremely high for a Chinese open-weight model, but if truly competitive, the price may be justified. Some discuss the strategic commoditization of AI by Chinese labs, while others highlight the model's 2.8 trillion parameters and strong benchmark performance surpassing Opus 4.8.

**Tags**: `#AI`, `#language models`, `#frontier intelligence`, `#pricing`, `#open-weight`

---

<a id="item-4"></a>
## [LM Studio Launches Bionic: AI Agent for Local Open Models](https://lmstudio.ai/blog/introducing-lm-studio-bionic) ⭐️ 8.0/10

LM Studio introduced Bionic, an AI agent for open-source local LLMs that can handle coding and document creation tasks, initially supporting models like Qwen, Kimi, and GLM. Bionic provides a user-friendly agentic interface for local models, bridging the gap between cloud-based AI agents and privacy-preserving local execution, which could drive broader adoption of local LLMs for practical applications. Bionic offers two project modes: Code for coding and Work for document creation with automatic checkpointing on every change. Users can point it to their existing LM Studio model library, and early feedback indicates smooth integration though some rough edges remain.

hackernews · minimaxir · Jul 16, 20:18 · [Discussion](https://news.ycombinator.com/item?id=48939662)

**Background**: LM Studio is a desktop application that simplifies running local LLMs with a clean chat interface and easy model downloads, requiring no command-line usage. Local LLMs run on personal hardware, offering privacy and cost benefits over cloud APIs. Bionic extends LM Studio into agentic AI, enabling autonomous multi-step tasks.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/lmstudio-ai">LM Studio · GitHub</a></li>
<li><a href="https://lmstudio.ai/">LM Studio - Local AI on your computer</a></li>
<li><a href="https://blog.alexewerlof.com/p/local-llms-for-agentic-coding">Using local LLMs for agentic coding - Alex Ewerlöf Notes</a></li>

</ul>
</details>

**Discussion**: The founder offered free credits for testing with specific models, and users reported positive first impressions, noting similarity to Codex UI but with local models. Some expressed concern about the business model shift toward cloud reliance, while others appreciated the unified local agent solution.

**Tags**: `#LM Studio`, `#AI agent`, `#open models`, `#local LLM`, `#coding`

---

<a id="item-5"></a>
## [Decoy Font: Adversarial Typeface Confuses AI OCR](https://www.mixfont.com/experiments/decoy-font) ⭐️ 8.0/10

A new font called 'Decoy Font' has been published on MixFont that displays different text at high resolution than when blurred, effectively confusing AI and OCR systems while remaining human-readable. This demonstrates a practical adversarial attack on visual AI systems, highlighting vulnerabilities in OCR and AI reading capabilities. It has implications for AI safety, digital forensics, and privacy protection. The font works by embedding a hidden message in the blurry version that becomes visible when the image is scaled down or blurred, while the sharp version shows a different message. Community tests show that large language models like GPT and Gemini can sometimes detect the hidden text when prompted.

hackernews · ray__ · Jul 16, 16:18 · [Discussion](https://news.ycombinator.com/item?id=48936584)

**Background**: Adversarial examples are inputs intentionally designed to cause machine learning models to make mistakes. In text recognition, adversarial fonts can exploit differences in how humans and AI perceive letters, using techniques like subtle distortions or dual-layer designs. OCR (Optical Character Recognition) systems convert images of text into machine-encoded text, and are common in document processing.

<details><summary>References</summary>
<ul>
<li><a href="https://bdtechtalks.com/2020/07/15/machine-learning-adversarial-examples/">What is adversarial machine learning? - TechTalks</a></li>
<li><a href="https://boschko.ca/adversarial-ml/">Breaking Down Adversarial Machine Learning Attacks Through Red...</a></li>

</ul>
</details>

**Discussion**: Comments are mixed: some find it cool but not practically useful, while others show that AI models like GPT-5.6 can partially detect the hidden text when prompted. One user suggests a simple PIL script could fix it for OCR, and another notes that it is just a level-of-detail effect.

**Tags**: `#font`, `#AI`, `#OCR`, `#adversarial`, `#hacking`

---

<a id="item-6"></a>
## [Roc Compiler Rewrite from Rust to Zig Progress Report](https://rtfeldman.com/rust-to-zig) ⭐️ 8.0/10

The author provides a detailed update on rewriting the Roc compiler from Rust to Zig, citing better memory control and incremental compilation as primary motivations. This rewrite highlights practical trade-offs between Rust and Zig for systems programming, especially in compiler engineering, and may influence future language choices for similar projects. The Roc compiler rewrite prioritizes memory safety without runtime overhead and aims for significantly faster incremental builds compared to Rust's current capabilities.

hackernews · jorangreef · Jul 16, 11:39 · [Discussion](https://news.ycombinator.com/item?id=48933149)

**Background**: Roc is a functional programming language (not to be confused with HP's RPL). Rust is a memory-safe systems language with a strong type system, while Zig offers manual memory management with fast compilation. The decision to rewrite from Rust to Zig is notable because many compilers are written in Rust.

<details><summary>References</summary>
<ul>
<li><a href="https://www.roc-lang.org/">The Roc Programming Language</a></li>
<li><a href="https://en.wikipedia.org/wiki/Rust_(programming_language)">Rust (programming language) - Wikipedia</a></li>

</ul>
</details>

**Discussion**: Community comments question the necessity of unsafe code in compilers, the effectiveness of Zig's runtime safety checks, and whether Zig's incremental builds are truly faster than OCaml's Dune. Some express hope that Rust will eventually gain similar features.

**Tags**: `#Rust`, `#Zig`, `#compilers`, `#programming languages`, `#rewrite`

---

<a id="item-7"></a>
## [LLM Critics Are Right, Yet I Keep Using Them](https://www.theocharis.dev/blog/llm-critics-are-right-i-use-llms-anyway/) ⭐️ 8.0/10

A software engineer openly acknowledges valid criticisms of large language models (LLMs), such as skill atrophy and low-quality contributions, but explains why they still find LLMs useful for their work. This article sparks a nuanced debate about the trade-offs of LLM use in software engineering, highlighting concerns about long-term skill development and code quality while recognizing practical productivity gains. The author mentions spending nearly $10,000 on API tokens in a month, and community comments note an influx of low-quality PRs in open source projects due to LLM-generated contributions.

hackernews · JeremyTheo · Jul 16, 11:59 · [Discussion](https://news.ycombinator.com/item?id=48933310)

**Background**: Large language models (LLMs) like GPT-4 are AI systems that generate human-like text. They are increasingly used by developers for code generation, debugging, and documentation, but critics worry they may erode foundational skills and flood projects with shallow contributions.

**Discussion**: Comments express concerns about skill atrophy, drawing parallels to smartphone addiction, and question whether LLM use enriches thinking in the long run. Some developers report blocking LLM-generated PRs from external contributors to maintain quality.

**Tags**: `#LLM`, `#software engineering`, `#AI tools`, `#critical thinking`, `#developer experience`

---

<a id="item-8"></a>
## [Codex Bug Can Delete User Files in Full Access Mode](https://simonwillison.net/2026/Jul/16/bad-codex-bug/#atom-everything) ⭐️ 8.0/10

A bug in GPT-5.6 Codex can cause unintended file deletion when Full Access mode is enabled without sandboxing or auto-review, due to the model mistakenly deleting $HOME instead of overriding a temporary directory. This reveals a concrete safety risk in AI coding agents, emphasizing the need for sandboxing and approval mechanisms. Developers and organizations relying on Codex for automated tasks must adopt proper safeguards to prevent data loss. The bug triggers when the model attempts to set a temporary directory by overriding $HOME, but instead deletes the entire home directory. It occurs most commonly when Full Access mode is enabled without sandboxing or auto-review, removing all human oversight.

rss · Simon Willison · Jul 16, 17:45

**Background**: Codex is an AI coding agent by OpenAI that can perform tasks like file editing and code generation. It operates in different security modes: Read Only, Default/Agent (with approval), and Full Access (no restrictions). Auto-review replaces manual approval with a separate reviewer agent. Full Access mode bypasses sandboxing and approval, making file deletion bugs particularly dangerous.

<details><summary>References</summary>
<ul>
<li><a href="https://developers.openai.com/codex/llms-full.txt">developers.openai.com/ codex /llms- full .txt</a></li>
<li><a href="https://daehnhardt.com/blog/2026/02/06/codex-cli-part-2-security-controls-and-safe-edits/">Codex CLI Part 2 — Security Controls & Safe Editing</a></li>
<li><a href="https://alignment.openai.com/auto-review/">Auto-review of agent actions without synchronous human oversight</a></li>

</ul>
</details>

**Tags**: `#codex`, `#ai-safety`, `#coding-agents`, `#generative-ai`, `#bug`

---

<a id="item-9"></a>
## [Linus Torvalds Defends AI Use in Linux Kernel](https://simonwillison.net/2026/Jul/16/linus-torvalds/#atom-everything) ⭐️ 8.0/10

Linus Torvalds stated on the Linux media mailing list that Linux is not an anti-AI project and that AI is a clearly useful tool, inviting anyone who disagrees to fork the project or leave. As the creator and top maintainer of Linux, Torvalds' stance sets a strong precedent for the entire open-source ecosystem, potentially influencing how AI tools are accepted and integrated into other projects. Torvalds acknowledged that AI's usefulness was questionable a year ago but is no longer in doubt, though he noted other open questions like the economy of AI remain.

rss · Simon Willison · Jul 16, 13:26

**Background**: Linus Torvalds is the creator of the Linux kernel, one of the largest and most influential open-source projects. In recent years, generative AI and large language models have sparked debate in open-source communities about code quality, licensing, and ethics.

**Tags**: `#Linux`, `#AI`, `#Linus Torvalds`, `#open source`

---

<a id="item-10"></a>
## [ExTernD: Ternary Decomposition with Expanded Rank for LLM PTQ](https://www.reddit.com/r/MachineLearning/comments/1uy2zb3/externd_expandedrank_ternary_decomposition/) ⭐️ 8.0/10

Researchers propose ExTernD, a post-training quantization method that decomposes a weight matrix into two ternary matrices and a diagonal scaling matrix, allowing the inner rank to be arbitrarily expanded to achieve accuracy comparable to any quantization level, while requiring only slightly more VRAM than current quantization methods. This approach addresses the fundamental accuracy limitations of ternary quantization in large language models, enabling efficient deployment with much higher accuracy. It could significantly reduce the computational cost and memory footprint of LLMs while maintaining performance, making them more accessible for resource-constrained environments. The core innovation is that rather than fixing the matrix size, ExTernD allows the inner rank to be arbitrarily large, which the authors claim can achieve arbitrarily small accuracy loss. The method reportedly requires only a modest increase in VRAM compared to standard quantization, justified by exploiting ternary arithmetic.

reddit · r/MachineLearning · /u/LMTLS5 · Jul 16, 13:31

**Background**: Large language models (LLMs) are typically stored in high precision (e.g., FP16 or FP32), requiring large amounts of memory and compute. Post-training quantization (PTQ) reduces model size and speeds up inference by converting weights to lower-precision formats like INT8 or ternary values ({-1,0,1}). Ternary LLMs (e.g., 1.58-bit) are extremely efficient but often suffer significant accuracy loss. ExTernD aims to overcome this by allowing an expanded rank decomposition.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/1.58-bit_large_language_model">1.58-bit large language model - Wikipedia</a></li>
<li><a href="https://developer.nvidia.com/blog/optimizing-llms-for-performance-and-accuracy-with-post-training-quantization/">Optimizing LLMs for Performance and Accuracy with Post-Training Quantization | NVIDIA Technical Blog</a></li>

</ul>
</details>

**Tags**: `#LLM`, `#quantization`, `#ternary decomposition`, `#PTQ`, `#model compression`

---

<a id="item-11"></a>
## [1Password Launches Claude Integration for Safe AI Login](https://9to5mac.com/2026/07/16/1password-now-lets-claude-sign-in-to-websites-without-seeing-your-passwords/) ⭐️ 8.0/10

1Password has launched an integration with Anthropic's Claude AI on Mac, allowing users to authorize Claude to log into websites on their behalf without the AI ever seeing the password or two-factor authentication codes. This integration bridges AI-driven convenience with stringent security, potentially setting a new standard for how AI agents handle sensitive credentials, impacting both enterprise and personal security. Credentials are injected directly into the webpage via a secure channel, and each login requires biometric approval for the current session; if auto-fill fails, the filled data is immediately wiped. The feature is available for Mac users with both 1Password and Claude desktop and browser extensions installed.

telegram · zaihuapd · Jul 16, 15:54

**Background**: 1Password is a popular password manager that stores encrypted credentials. Claude is a large language model developed by Anthropic, designed with a focus on safety and ethics. This integration uses a secure API approach so that the AI never gains access to raw secrets, addressing common concerns about AI handling private data.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Claude_(AI)">Claude (AI)</a></li>
<li><a href="https://en.wikipedia.org/wiki/Anthropic">Anthropic</a></li>

</ul>
</details>

**Tags**: `#password management`, `#AI integration`, `#security`, `#Claude`, `#1Password`

---

<a id="item-12"></a>
## [Truth Social to Sell Fast Access to Trump's Posts to Wall Street](https://www.cnn.com/2026/07/16/business/truth-social-data-wall-street) ⭐️ 8.0/10

On August 1, Trump Media & Technology Group will launch Truth API, a real-time data service that provides millisecond-speed access to posts from the top 10 accounts on Truth Social, including former President Trump, to institutional clients for high-frequency trading. This move monetizes the market-moving power of Trump's Truth Social posts, raising serious ethical concerns about the intersection of politics and finance, as traders could gain unfair advantages by reacting to presidential announcements faster than the public. The API specifically targets the top 10 accounts, but Trump's posts are the primary driver of market volatility. Pricing has not been disclosed, and CNN previously reported that Trump has used Truth Social to promote stocks he personally bought.

telegram · zaihuapd · Jul 17, 01:02

**Background**: High-frequency trading (HFT) uses algorithms to execute trades in fractions of a second, relying on speed to capture tiny price differences. Real-time access to influential social media posts can provide a critical edge. Truth Social is a social media platform founded by former President Donald Trump after he was banned from major platforms. It has become his primary channel for policy announcements.

<details><summary>References</summary>
<ul>
<li><a href="https://news.google.com/stories/CAAqNggKIjBDQklTSGpvSmMzUnZjbmt0TXpZd1NoRUtEd2p6eUpQUEVSRzVfanE2YUctQ1BpZ0FQAQ?hl=en-US&gl=US&ceid=US:en">Google News - Trump Media unveils Truth API for real-time post...</a></li>
<li><a href="https://www.investopedia.com/articles/investing/091615/world-high-frequency-algorithmic-trading.asp">investopedia.com/articles/investing/091615/world- high - frequency ...</a></li>

</ul>
</details>

**Tags**: `#Truth Social`, `#financial markets`, `#API`, `#ethics`, `#politics`

---