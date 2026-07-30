---
layout: default
title: "Horizon Summary: 2026-07-30 (EN)"
date: 2026-07-30
lang: en
---

> From 40 items, 13 important content pieces were selected

---

1. [AI Worm Spreads via Microsoft Copilot in Word](#item-1) ⭐️ 9.0/10
2. [Russia charges Telegram founder Durov with aiding terrorism, issues international warrant](#item-2) ⭐️ 9.0/10
3. [Top AI startups reduce research publications, raising transparency concerns](#item-3) ⭐️ 8.0/10
4. [Vision Pro used for immersive house design walkthroughs](#item-4) ⭐️ 8.0/10
5. [Open-source engine runs Gemma 4 26B in 2GB RAM on M-series Mac](#item-5) ⭐️ 8.0/10
6. [Mitchell Hashimoto launches Superlogical to build terminal apps on libghostty](#item-6) ⭐️ 8.0/10
7. [KOReader: Open-Source Reader for E Ink Devices](#item-7) ⭐️ 8.0/10
8. [Long policy documents fail to govern LLM agents reliably](#item-8) ⭐️ 8.0/10
9. [Matthew Green on AI and Post-Quantum Cryptanalysis](#item-9) ⭐️ 8.0/10
10. [PostSlate uses ncnn Vulkan for vendor-agnostic edge ML inference](#item-10) ⭐️ 8.0/10
11. [Moonshot AI seeks $2B at $30B valuation, third round in six months](#item-11) ⭐️ 8.0/10
12. [OpenAI Offers Free Frontier AI Models to 100,000 Researchers](#item-12) ⭐️ 8.0/10
13. [UK Proposes Easing Apple and Google App Store Payment Rules](#item-13) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [AI Worm Spreads via Microsoft Copilot in Word](https://enklypesalt.com/posts/context-collapse-part3-ai-worming-through-word/) ⭐️ 9.0/10

Researchers demonstrated a document-borne AI worm that self-propagates through Microsoft Copilot for Word, using hidden malicious prompts to trick the AI into altering documents and spreading the attack to new files. This vulnerability allows AI worms to spread through normal document workflows without further attacker involvement, potentially leading to large-scale data breaches and malware propagation in enterprise environments using Copilot. The attack exploits the fundamental lack of separation between instructions and data in current AI models, and hidden prompts can be embedded using techniques like white text or Unicode tricks, making detection difficult.

hackernews · Canopy9560 · Jul 29, 11:44 · [Discussion](https://news.ycombinator.com/item?id=49096188)

**Background**: Prompt injection is a class of attacks where malicious instructions hidden in data (e.g., a document) cause an AI model to behave unexpectedly. An AI worm is a self-replicating prompt injection that spreads from one application to another. In this case, Copilot for Word processes documents and follows embedded instructions, inadvertently propagating the worm.

<details><summary>References</summary>
<ul>
<li><a href="https://www.linkedin.com/pulse/ai-worms-your-word-docs-free-code-review-beats-paid-tools-andy-arnott-61iec">AI Worms in Your Word Docs + Free Code Review That ... - LinkedIn</a></li>
<li><a href="https://zeli.app/en/story/49096188">Document-Borne AI Worms Self-Propagate Through Copilot for ...</a></li>

</ul>
</details>

**Discussion**: Commenters expressed concern that this vulnerability is fundamentally unfixable until AI systems stop mixing instructions with data. Some predicted the situation will worsen before improving, citing examples like hidden prompts in GitHub comments that could steal data or propagate through accounts. Others noted that simple techniques like white text still work to hide prompts.

**Tags**: `#AI security`, `#prompt injection`, `#Copilot vulnerabilities`, `#AI worms`, `#data security`

---

<a id="item-2"></a>
## [Russia charges Telegram founder Durov with aiding terrorism, issues international warrant](https://www.interfax.ru/russia/1106228) ⭐️ 9.0/10

On July 29, Russia's Federal Security Service (FSB) filed criminal charges against Telegram founder Pavel Durov under Article 205.1, Part 1.1 of the Criminal Code (aiding terrorism) and placed him on an international wanted list. This escalation marks a significant legal confrontation between a major platform founder and a state, potentially impacting Telegram's global operations, free speech norms, and the governance of encrypted messaging platforms amid geopolitical tensions. The FSB alleges that Telegram's management refused to remove channels, groups, and bots used by Ukrainian intelligence and terrorist organizations to coordinate sabotage, terrorist attacks, and cyber fraud inside Russia, resulting in casualties and billions of rubles in damage.

telegram · zaihuapd · Jul 29, 05:56

**Background**: Telegram, founded by Pavel Durov in 2013, is a widely used encrypted messaging app, particularly popular in Russia and Ukraine. Durov, a Russian-born entrepreneur, has faced previous legal challenges in France over content moderation. The FSB charges relate to Telegram's stance on removing extremist content, which has been a point of contention between the platform and Russian authorities.

**Tags**: `#Telegram`, `#Pavel Durov`, `#Russia`, `#terrorism charges`, `#international warrant`

---

<a id="item-3"></a>
## [Top AI startups reduce research publications, raising transparency concerns](https://www.science.org/content/article/ai-s-top-startups-are-barely-publishing-their-research) ⭐️ 8.0/10

An article in Science reveals that high-profile AI startups are increasingly choosing not to publish their research, a shift from earlier practices where open publication was common. This trend threatens the open exchange of ideas in AI, potentially slowing collective progress and hindering reproducibility, which are critical for the field's healthy development. The article specifically notes that OpenAI leads in cumulative citations among unicorn startups, followed by companies like MEGVII, Hugging Face, and Anthropic; however, many of these firms now publish less. The study uses citations as a proxy for research significance, acknowledging its imperfection.

hackernews · YeGoblynQueenne · Jul 29, 21:25 · [Discussion](https://news.ycombinator.com/item?id=49103285)

**Background**: In the past, AI research was heavily shared through academic conferences and journals, fostering rapid progress. Startups like DeepMind and OpenAI initially published extensively, but as commercial pressure and competition for talent intensified, many have retreated from open publication to protect intellectual property and maintain competitive advantage.

**Discussion**: Commenters share personal experiences: one notes difficulty publishing in tier-1 journals and eventual shift to preprints, while another explicitly avoids publishing to prevent copying by OpenAI and Anthropic. A third comment criticizes the 'blogification' of AI research, arguing it encourages unverified claims and social-media-like dynamics.

**Tags**: `#AI`, `#startups`, `#research`, `#publications`, `#open science`

---

<a id="item-4"></a>
## [Vision Pro used for immersive house design walkthroughs](https://christianselig.com/2026/07/vision-pro-house/) ⭐️ 8.0/10

Christian Selig showcased a novel use of Apple Vision Pro for real-time immersive walkthroughs of house designs, allowing clients to experience spatial proportions and lighting interactively before construction. This demonstrates a practical, high-value application of Vision Pro beyond entertainment, potentially transforming architectural design workflows by enabling instant spatial validation and reducing costly changes during construction. The walkthrough likely uses Apple's RoomPlan and RealityKit to create a 3D model of the house, streamed to Vision Pro via visionOS; similar workflows already exist with Quest and HTC Vive but Vision Pro offers higher resolution and seamless passthrough.

hackernews · robbiet480 · Jul 29, 20:39 · [Discussion](https://news.ycombinator.com/item?id=49102774)

**Background**: Architectural visualization using VR has been available for years with devices like HTC Vive and Meta Quest, but Apple Vision Pro's high-resolution displays and precise hand/eye tracking enable a more realistic experience. Christian Selig is known for developing Apollo, a popular third-party Reddit client.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Apple_Vision_Pro">Apple Vision Pro</a></li>
<li><a href="https://www.apple.com/apple-vision-pro/">Apple Vision Pro</a></li>
<li><a href="https://plusrender.com/virtual-reality-walkthrough-for-architecture/">Creating the Best Tour for VR Walkthrough Architecture</a></li>

</ul>
</details>

**Discussion**: Professionals in architecture confirmed the value, with one user noting their firm uses a similar 3D-first approach with Quest 3. Others suggested enhancements like sun angle simulation. The community appreciated Christian's contribution, with some calling him a brilliant developer.

**Tags**: `#Vision Pro`, `#architecture`, `#VR/AR`, `#design`, `#3D visualization`

---

<a id="item-5"></a>
## [Open-source engine runs Gemma 4 26B in 2GB RAM on M-series Mac](https://github.com/drumih/turbo-fieldfare) ⭐️ 8.0/10

TurboFieldfare is a new open-source inference engine that runs a 4-bit quantized Gemma 4 26B-A4B-IT model on any M-series Mac with only 2 GB of RAM, by streaming routed experts from SSD during inference. This enables running a 26-billion-parameter model on memory-constrained devices like an 8 GB MacBook Air, making on-device AI more accessible and practical for users with limited RAM. The engine achieves 5–6 tokens/s on an 8 GB M2 MacBook Air and 31–35 tokens/s on an M5 MacBook Pro, using Swift and Metal with a small expert cache and bounded parallel pread. It also includes an experimental OpenAI-compatible local server with streaming and tool calls.

hackernews · gitpusher42 · Jul 29, 15:05 · [Discussion](https://news.ycombinator.com/item?id=49098510)

**Background**: Large language models like Gemma 4 26B require significant memory, often exceeding available RAM on consumer devices. 4-bit quantization reduces weight precision to lower memory footprint, while Mixture of Experts (MoE) models activate only a subset of parameters per token, enabling further efficiency. TurboFieldfare extends this by storing inactive experts on SSD and fetching them on demand, a technique called SSD streaming inference.

<details><summary>References</summary>
<ul>
<li><a href="https://alain-airom.medium.com/run-big-llms-on-small-gpus-a-hands-on-guide-to-4-bit-quantization-and-qlora-40e9e2c95054">Run Big LLMs on Small GPUs: A Hands-On Guide to 4-bit Quantization and QLoRA | by Alain Airom (Ayrom) | Medium</a></li>
<li><a href="https://developer.nvidia.com/blog/applying-mixture-of-experts-in-llm-architectures/">Applying Mixture of Experts in LLM Architectures | NVIDIA Technical...</a></li>
<li><a href="https://www.mindstudio.ai/blog/ssd-streaming-ai-models-ram-dial">SSD Streaming for AI Models: How to Turn RAM from a Wall into a Dial | MindStudio</a></li>

</ul>
</details>

**Discussion**: Community members praised the project for its innovation, with some noting that traditional tools like llama.cpp can also mmap models but lack the tuned synchronization. Users on high-RAM Macs (64 GB) observed even higher speeds (48 tok/s) due to page cache keeping the entire expert set resident. One user provided a compilation workaround for older macOS versions.

**Tags**: `#inference engine`, `#open-source`, `#Gemma`, `#quantization`, `#Mac`

---

<a id="item-6"></a>
## [Mitchell Hashimoto launches Superlogical to build terminal apps on libghostty](https://www.superlogical.com/) ⭐️ 8.0/10

Mitchell Hashimoto announced Superlogical, a new company that will develop terminal applications on top of the open-source libghostty library, following the transfer of Ghostty to a non-profit organization. This represents a novel open-source business model where a company builds proprietary products on top of an open-source library it originally created, ensuring the library remains free and independent. It could inspire similar strategies for other open-source projects seeking sustainable funding. Superlogical will use libghostty as a public building block, consuming the same MIT-licensed components available to anyone, and will contribute upstream to shared terminal work. Ghostty itself is a fast, GPU-accelerated terminal emulator with native UI on macOS and Linux.

hackernews · yan · Jul 29, 15:41 · [Discussion](https://news.ycombinator.com/item?id=49098965)

**Background**: Terminal emulators are essential tools for developers, providing a text-based interface to the operating system. Ghostty, created by Mitchell Hashimoto (also known for Vagrant and Terraform), gained attention for its performance and cross-platform design. libghostty is a library that allows any application to embed a full terminal emulator, enabling new use cases like integrated development environments or remote management tools.

<details><summary>References</summary>
<ul>
<li><a href="https://ghostty.org/">Ghostty</a></li>
<li><a href="https://mitchellh.com/writing/libghostty-is-coming">Libghostty Is Coming – Mitchell Hashimoto</a></li>
<li><a href="https://github.com/ghostty-org/ghostty">GitHub - ghostty -org/ ghostty : Ghostty is a fast, feature-rich, and...</a></li>

</ul>
</details>

**Discussion**: The community response is largely positive, with users praising the strategic transfer of Ghostty to a non-profit before building a company on top of libghostty. Some draw parallels to older technologies like OLE and COM, while others express frustration with minimalist, uninformative announcement titles. There is also interest from developers who see potential for integrating terminal functionality into other tools.

**Tags**: `#terminal`, `#open-source`, `#Ghostty`, `#Superlogical`, `#Mitchell Hashimoto`

---

<a id="item-7"></a>
## [KOReader: Open-Source Reader for E Ink Devices](https://koreader.rocks/) ⭐️ 8.0/10

KOReader is an open-source e-book reader and document viewer for E Ink devices, supporting a wide range of file formats like EPUB, PDF, and MOBI, and offering extensive customization options. It liberates users from proprietary e-reader ecosystems, enabling them to read DRM-free content without conversion, and fosters an active community of developers and readers who value freedom and control over their reading experience. KOReader runs on jailbroken Kindle, Kobo, and other E Ink devices; its features include reflow, text-to-speech, OPDS catalog support, and sync via Calibre or cloud services. However, some users report a non-intuitive UI and occasional lag.

hackernews · Cider9986 · Jul 29, 11:05 · [Discussion](https://news.ycombinator.com/item?id=49095865)

**Background**: E Ink devices are low-power e-readers with reflective displays that mimic paper. Popular models like Amazon Kindle and Kobo have closed operating systems, limiting file format support and customization. KOReader is an open-source alternative that users install after jailbreaking their device, providing support for more formats and advanced features like gesture controls and PDF reflow.

<details><summary>References</summary>
<ul>
<li><a href="https://koreader.rocks/">KOReader</a></li>
<li><a href="https://grokipedia.com/page/KOReader">KOReader</a></li>

</ul>
</details>

**Discussion**: Community comments are largely positive, with users praising KOReader's freedom and format support. However, some note a steep learning curve, unintuitive gestures, and occasional lag. One user adopted KOReader specifically for its ability to sync with iPhone via Readest, but ultimately switched away.

**Tags**: `#open-source`, `#e-reader`, `#kindle`, `#kobo`, `#reading`

---

<a id="item-8"></a>
## [Long policy documents fail to govern LLM agents reliably](https://arxiv.org/abs/2607.25398) ⭐️ 8.0/10

A new study titled 'Handbook.md' demonstrates that LLM agents fail to reliably adhere to long policy documents, revealing fundamental context window limitations. This research challenges the assumption that large context models can effectively govern agent behavior, highlighting a critical gap for deploying AI agents in real-world policy-compliance scenarios. The study highlights that even models claiming support for 1M tokens struggle with context rot, quantization issues, and sampler limitations, making them unreliable for long-policy adherence.

hackernews · spIrr · Jul 29, 13:01 · [Discussion](https://news.ycombinator.com/item?id=49096969)

**Background**: LLM agents are AI systems that use large language models to autonomously perform tasks, often guided by policy documents. Context windows limit the amount of text a model can process at once; longer windows do not guarantee accurate recall or reasoning, especially when models are heavily quantized or use poor sampling methods.

<details><summary>References</summary>
<ul>
<li><a href="https://atlan.com/know/llm-context-window-limitations/">LLM Context Window Limitations in 2026 - atlan.com</a></li>
<li><a href="https://bitfern.com/blog/context-windows/">LLM Context Windows Explained: Limits, Tokens, and Memory</a></li>
<li><a href="https://www.thinkstack.ai/blog/what-are-llm-agents/">What are LLM Agents? A Complete Guide for 2026</a></li>

</ul>
</details>

**Discussion**: Community comments generally agree with the findings, noting that in practice models like Claude quickly ignore long instructions and perform better with short, in-prompt guidance. Some argue that local inference could alleviate the problem, while others point out that even humans struggle with long policy documents.

**Tags**: `#LLM`, `#AI Agents`, `#Context Window`, `#Policy Compliance`, `#Benchmark`

---

<a id="item-9"></a>
## [Matthew Green on AI and Post-Quantum Cryptanalysis](https://simonwillison.net/2026/Jul/29/matthew-green/#atom-everything) ⭐️ 8.0/10

Cryptographer Matthew Green observed that the current transition from traditional public-key algorithms (RSA, ECC) to post-quantum algorithms is an ideal time for AI to advance cryptanalysis, potentially either undermining hard problems or providing robust confidence in new standards. This perspective is timely as industry and standards bodies are actively selecting and deploying post-quantum cryptographic standards; if AI can thoroughly test these algorithms, it could significantly strengthen trust or reveal critical weaknesses before widespread adoption. Green specifically mentions HAWK as an example of a post-quantum standard under NIST evaluation, and references Impagliazzo's Minicrypt world — a scenario where public-key cryptography is impossible but secret-key cryptography exists — as a possible outcome if AI succeeds in undermining all hard problems.

rss · Simon Willison · Jul 29, 18:18

**Background**: Post-quantum cryptography refers to cryptographic algorithms designed to be secure against both classical and quantum computers, as current schemes like RSA and ECC are vulnerable to Shor's algorithm. NIST is leading a standardization process to select and approve these new algorithms. Impagliazzo's Five Worlds is a conceptual framework that classifies possible relationships between computational complexity and cryptography, ranging from Algorithmica (P=NP) to Cryptomania (rich cryptographic primitives).

<details><summary>References</summary>
<ul>
<li><a href="https://hawk-sign.info/">Hawk</a></li>
<li><a href="https://www.nist.gov/pqc">Post-quantum cryptography | NIST</a></li>
<li><a href="https://fanpu.io/blog/2022/impagliazzos-five-worlds/">Impagliazzo ' s Five Worlds, or The Computational... | Fan Pu Zeng</a></li>

</ul>
</details>

**Tags**: `#cryptography`, `#post-quantum`, `#AI`, `#cryptanalysis`, `#standards`

---

<a id="item-10"></a>
## [PostSlate uses ncnn Vulkan for vendor-agnostic edge ML inference](https://www.reddit.com/r/MachineLearning/comments/1v9s4mz/vendoragnostic_ml_inference_on_production_edge/) ⭐️ 8.0/10

PostSlate, a video editing tool, adopted ncnn's Vulkan backend to run ML models like face detection and embedding on diverse GPUs, achieving 10x speedup over ONNX CPU and eliminating vendor-specific runtimes. This approach enables efficient on-device ML inference across NVIDIA, AMD, Intel, and Apple Silicon without forcing users to install CUDA or other proprietary runtimes, lowering deployment barriers for edge AI applications. On an RTX 4070, ncnn Vulkan reduced ArcFace R50 face embedding from 30 ms (ONNX CPU) to 3 ms, and SCRFD face detection from 25 ms to 2.5 ms, with model size halved via fp16 weight storage.

reddit · r/MachineLearning · /u/ppchaos · Jul 29, 10:22

**Background**: ncnn is a high-performance neural network inference framework optimized for mobile and edge platforms, developed by Tencent. Vulkan is a cross-platform GPU API that provides low-level access to graphics and compute hardware. ONNX (Open Neural Network Exchange) is an open standard for representing machine learning models, enabling interoperability between frameworks.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/Tencent/ncnn">GitHub - Tencent/ncnn: ncnn is a high-performance neural ... Treatment by Cancer Type - NCCN Releases · Tencent/ncnn - GitHub home — ncnn documentation About Us - NCNN</a></li>
<li><a href="https://github.khronos.org/Vulkan-Site/tutorial/latest/ML_Inference/Embedded_Applications/01_introduction.html">Embedded Applications: AI at the Edge :: Vulkan Documentation Project</a></li>
<li><a href="https://en.wikipedia.org/wiki/ONNX">ONNX</a></li>

</ul>
</details>

**Tags**: `#machine learning`, `#edge computing`, `#Vulkan`, `#inference`, `#onnx`

---

<a id="item-11"></a>
## [Moonshot AI seeks $2B at $30B valuation, third round in six months](https://t.me/zaihuapd/42845) ⭐️ 8.0/10

Moonshot AI, the Chinese AI startup behind the Kimi chatbot, is seeking up to $2 billion in new funding at a $30 billion valuation, marking its third funding round in six months. The company's annual recurring revenue exceeded $200 million in April, driven by demand for its Kimi chatbot and large language models. This rapid valuation increase from $4 billion to $30 billion in six months reflects strong investor confidence in Chinese AI startups, particularly those with proven product-market fit. Moonshot AI's success signals growing competition in the global LLM space and the importance of consumer-facing AI applications in China. The company is also dismantling its offshore structure to prepare for a Hong Kong IPO, and has launched a general AI agent called Kimi Work. A previous round led by Meituan valued the company at $20 billion post-money, up from just over $4 billion in December 2024.

telegram · zaihuapd · Jul 29, 10:12

**Background**: Moonshot AI was founded in March 2023 by Tsinghua University alumni Yang Zhilin, Zhou Xinyu, and Wu Yuxin, with the goal of advancing general artificial intelligence. Its flagship product, Kimi, is an AI chatbot known for supporting up to 128,000 tokens of context in its initial version. The company has since released open-weights models like Kimi K2 and K3, and is positioning itself as a major player in the Chinese AI ecosystem alongside competitors like Baidu and Alibaba.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Kimi_(chatbot)">Kimi (chatbot)</a></li>
<li><a href="https://en.wikipedia.org/wiki/Moonshot_AI">Moonshot AI - Wikipedia</a></li>
<li><a href="https://www.kimi.com/products/kimi-work">Kimi Work : Next-Gen Desktop AI Agent for Knowledge Workers</a></li>

</ul>
</details>

**Tags**: `#AI`, `#startup`, `#funding`, `#large language model`, `#Chinese tech`

---

<a id="item-12"></a>
## [OpenAI Offers Free Frontier AI Models to 100,000 Researchers](https://openai.com/index/chatgpt-for-academic-researchers/) ⭐️ 8.0/10

On July 29, 2026, OpenAI launched the ChatGPT for Academic Researchers program, offering free access to its frontier GPT-5.6 models to up to 100,000 researchers worldwide by 2027, with applications open immediately for an initial cohort of 10,000. This initiative significantly lowers the barrier for academic researchers to leverage state-of-the-art AI, potentially accelerating discoveries in fields like genomics, protein modeling, and literature review. It also represents OpenAI's commitment to investing over $250 million in external research by 2027. Participants can use GPT-5.6 models (including the frontier Sol tier) and invite up to four institutional collaborators, with data not used for model training by default. The program covers training and technical support for the entire research workflow, including grant writing and genomic analysis.

telegram · zaihuapd · Jul 30, 00:17

**Background**: Frontier AI models, such as OpenAI's GPT-5.6 series, are the most advanced and capable models at a given time, trained on massive datasets to deliver state-of-the-art performance across diverse tasks. These models often have emergent abilities that are both powerful and unpredictable, creating opportunities as well as risks. Prior to this program, access to such models was typically limited to paid API users or enterprise customers, making them less accessible to academic researchers with limited budgets.

<details><summary>References</summary>
<ul>
<li><a href="https://kie.ai/gpt-5-6">OpenAI GPT - 5 . 6 API: Frontier Intelligence with Sol, Terra, and... | Kie.ai</a></li>
<li><a href="https://www.vellum.ai/blog/gpt-5-6-benchmarks-explained">GPT - 5 . 6 Sol vs Terra vs Luna: Which Tier Should You Actually Use?</a></li>
<li><a href="https://www.nvidia.com/en-us/glossary/frontier-models/">What Are Frontier AI Models and How They Work | NVIDIA Glossary</a></li>

</ul>
</details>

**Tags**: `#OpenAI`, `#academic research`, `#AI models`, `#science funding`, `#GPT-5`

---

<a id="item-13"></a>
## [UK Proposes Easing Apple and Google App Store Payment Rules](https://t.me/zaihuapd/42855) ⭐️ 8.0/10

On June 30, 2026, the UK Competition and Markets Authority (CMA) proposed allowing app developers to direct users to alternative payment options outside of Apple and Google's app stores, and also considering requiring Apple to open its NFC technology for contactless payments in iOS apps. This proposal could reduce the commissions Apple and Google charge on in-app purchases, potentially lowering costs for developers and consumers, and increase competition in the mobile app ecosystem. It may also set a precedent for other regions considering similar digital market regulations. The CMA specified that any fees Apple or Google charge for directing users to external payments must be fair, reasonable, and lower than the existing app store commission. The savings should benefit consumers or be used for innovation. The proposal is part of a consultation under the UK's new digital markets regime, following the designation of Apple and Google as having strategic market status in mobile ecosystems last year.

telegram · zaihuapd · Jul 30, 02:10

**Background**: The UK's Digital Markets, Competition and Consumers Act 2024 empowers the CMA to regulate firms designated with 'strategic market status' (SMS) in digital activities. NFC (Near Field Communication) is a technology that enables contactless payments by allowing devices to communicate when close together. The CMA's proposal addresses concerns that Apple and Google's control over app store payments and NFC access stifles competition and innovation.

<details><summary>References</summary>
<ul>
<li><a href="https://www.gov.uk/government/news/cma-consults-on-new-requirements-for-apple-and-googles-mobile-platforms">CMA consults on new requirements for Apple and Google’s ...</a></li>
<li><a href="https://en.wikipedia.org/wiki/Digital_Markets,_Competition_and_Consumers_Act_2024">Digital Markets, Competition and Consumers Act 2024 - Wikipedia</a></li>

</ul>
</details>

**Tags**: `#antitrust`, `#app store`, `#digital regulation`, `#mobile payments`, `#UK CMA`

---