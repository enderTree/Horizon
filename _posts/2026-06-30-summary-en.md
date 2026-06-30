---
layout: default
title: "Horizon Summary: 2026-06-30 (EN)"
date: 2026-06-30
lang: en
---

> From 39 items, 11 important content pieces were selected

---

1. [Supreme Court rules geofence warrants require constitutional protections](#item-1) ⭐️ 9.0/10
2. [vLLM v0.24.0 Released with Major Optimizations](#item-2) ⭐️ 8.0/10
3. [Rocket Lab acquires Iridium in $8B deal](#item-3) ⭐️ 8.0/10
4. [WATaBoy: JIT-Compiling Game Boy Instructions to WASM Outperforms Native Interpreter](#item-4) ⭐️ 8.0/10
5. [Deep Dive: CUDA Kernel Execution Pipeline from CPU to GPU](#item-5) ⭐️ 8.0/10
6. [Ornith-1.0: Open-Weight LLMs Achieve SOTA in Agentic Coding](#item-6) ⭐️ 8.0/10
7. [Cerebras-OpenAI Deal Pushes Startups to Back of Waitlist](#item-7) ⭐️ 8.0/10
8. [Google's AI Peer-Reviewer Processed ~10K Papers at ICML/STOC](#item-8) ⭐️ 8.0/10
9. [EML Trees Proven as Universal Approximators](#item-9) ⭐️ 8.0/10
10. [CXMT signs nearly $3B DRAM deal with Tencent](#item-10) ⭐️ 8.0/10
11. [Tesla FSD v14 Lite: HW4 Capabilities for HW3](#item-11) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Supreme Court rules geofence warrants require constitutional protections](https://www.theguardian.com/us-news/2026/jun/29/supreme-court-geofence-warrants-case-decision) ⭐️ 9.0/10

The US Supreme Court ruled 6-3 that geofence warrants are subject to Fourth Amendment protections, affirming that individuals have a reasonable expectation of privacy in their cell-phone location data. The decision was authored by Justice Elena Kagan. This landmark decision significantly limits law enforcement's ability to conduct mass location surveillance without a warrant, setting a critical precedent for digital privacy in the era of ubiquitous mobile tracking. It impacts both future investigations and the tech companies that store location data. The case originated from a bank robbery where Google provided location data of devices within 150 meters of the bank. The court held that geofence warrants must be based on probable cause and particularly describe the place to be searched, citing the 2014 Riley v. California decision. The ruling does not ban geofence warrants outright but requires them to comply with traditional warrant requirements.

hackernews · cdrnsf · Jun 29, 15:54 · [Discussion](https://news.ycombinator.com/item?id=48720924)

**Background**: A geofence warrant is a reverse location warrant that allows law enforcement to demand from technology companies a list of all mobile devices within a specific geographic area during a specific time period. The Fourth Amendment protects against unreasonable searches and seizures, and courts have traditionally required warrants to name the person or place to be searched. This ruling extends that protection to digital location data, even when the data is held by third parties and collected in public spaces.

<details><summary>References</summary>
<ul>
<li><a href="https://www.theguardian.com/us-news/2026/jun/29/supreme-court-geofence-warrants-case-decision">US supreme court rules geofence warrants require constitutional privacy protections | US supreme court | The Guardian</a></li>
<li><a href="https://en.wikipedia.org/wiki/Geofence_warrant">Geofence warrant - Wikipedia</a></li>
<li><a href="https://techcrunch.com/2026/06/29/in-major-privacy-win-supreme-court-rules-geofence-warrants-are-protected-by-privacy-rights/">In major privacy win, Supreme Court rules geofence warrants are protected by privacy rights | TechCrunch</a></li>

</ul>
</details>

**Discussion**: Commenters highlighted historical precedents such as the Paula Broadwell case and praised the court for citing sources. Some expressed concern about other surveillance technologies like Flock cameras potentially requiring warrants now. Others debated the balance between effective law enforcement and privacy rights, with overall sentiment supportive of the ruling's privacy protections.

**Tags**: `#privacy`, `#supreme court`, `#geofence warrants`, `#digital rights`, `#fourth amendment`

---

<a id="item-2"></a>
## [vLLM v0.24.0 Released with Major Optimizations](https://github.com/vllm-project/vllm/releases/tag/v0.24.0) ⭐️ 8.0/10

vLLM v0.24.0 adds support for MiniMax-M3 and DeepSeek-V4 models, introduces Model Runner V2 as default for quantized models, and includes 571 commits from 256 contributors with extensive performance optimizations. This release underscores vLLM's rapid development and strong community engagement, solidifying its role as a leading open-source LLM inference engine. The optimizations for DeepSeek-V4 and MiniMax-M3 enable faster and more efficient serving of cutting-edge models, benefiting both developers and end users. Key technical details include a FlashInfer sparse index cache improving time-to-first-token for DeepSeek-V4, MXFP4 quantization support for MiniMax-M3, and Model Runner V2 now default for quantized models. The release also adds a streaming parser engine and DiffusionGemma support.

github · khluu · Jun 29, 19:41

**Background**: vLLM is a high-throughput, memory-efficient inference engine for large language models, widely adopted in production. FlashInfer is a kernel library for LLM serving that optimizes attention computations, while MXFP4 is a 4-bit floating-point format for model quantization, enabling reduced memory usage.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/flashinfer-ai/flashinfer">GitHub - flashinfer-ai/flashinfer: FlashInfer: Kernel Library for LLM Serving · GitHub</a></li>
<li><a href="https://arxiv.org/abs/2501.01005">[2501.01005] FlashInfer: Efficient and Customizable Attention Engine for LLM Inference Serving</a></li>
<li><a href="https://rocm.blogs.amd.com/artificial-intelligence/w4a6-quant-mm/README.html">MXFP6 and MXFP 4 Mixed Precision for Accelerating... — ROCm Blogs</a></li>

</ul>
</details>

**Tags**: `#vllm`, `#LLM serving`, `#open-source`, `#performance`, `#deep learning`

---

<a id="item-3"></a>
## [Rocket Lab acquires Iridium in $8B deal](https://investors.rocketlabcorp.com/news-releases/news-release-details/rocket-lab-acquire-iridium-historic-deal-creating-fully) ⭐️ 8.0/10

Rocket Lab announced on June 29, 2025 that it will acquire Iridium Communications in a cash-and-stock deal valued at approximately $8 billion. The merger is expected to close by mid-2027, pending shareholder and regulatory approvals. The acquisition creates a fully integrated space company combining Rocket Lab's launch and spacecraft manufacturing with Iridium's satellite network and spectrum, enabling entry into satellite IoT, direct-to-device, and PNT markets. It mirrors SpaceX's Starlink model of using satellite services to guarantee launch demand. Rocket Lab has secured a $3.6 billion bridge loan commitment for the transaction. Iridium's L-band spectrum, global constellation of 66 operational satellites, and over 2.55 million active subscribers are key assets.

hackernews · everfrustrated · Jun 29, 14:09 · [Discussion](https://news.ycombinator.com/item?id=48719485)

**Background**: Rocket Lab is a launch service provider and satellite manufacturer known for its Electron small-lift rocket. Iridium operates a low Earth orbit satellite constellation for global voice and data communications. The deal reflects a trend of vertical integration in the space industry.

**Discussion**: Comments highlight concerns about space debris and commercialization of orbit, with one user noting the potential for satellite ads. Another user praises the deal as a smart move to secure launch contracts, similar to SpaceX's Starlink model. A technical user recalls paying $1 per KB for Iridium data in 2014.

**Tags**: `#rocket-lab`, `#iridium`, `#space`, `#acquisition`, `#satellites`

---

<a id="item-4"></a>
## [WATaBoy: JIT-Compiling Game Boy Instructions to WASM Outperforms Native Interpreter](https://humphri.es/blog/WATaBoy/) ⭐️ 8.0/10

A blog post by Will Humphreys demonstrates that just-in-time (JIT) compiling Game Boy emulator instructions to WebAssembly (WASM) can outperform a native interpreter, using a project called WATaBoy. This approach challenges the assumption that native interpretation is always faster, and opens up new possibilities for high-performance emulation on platforms with JIT restrictions, such as iOS, where WASM JIT is permitted via web browsers. The WATaBoy project compiles Game Boy CPU instructions into WebAssembly modules at runtime, achieving speedups over a native interpreter. The author notes that Firefox is about 25% slower than Chrome or Safari in running the compiled WASM.

hackernews · energeticbark · Jun 29, 15:02 · [Discussion](https://news.ycombinator.com/item?id=48720190)

**Background**: Just-in-time (JIT) compilation is a technique that compiles code at runtime to native machine code for faster execution, as opposed to interpretation which processes each instruction individually. WebAssembly (WASM) is a low-level binary format that runs in web browsers with near-native performance, and browsers are allowed to use JIT for WASM even on platforms like iOS that normally restrict JIT compilation.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Tracing_just-in-time_compilation">Tracing just-in-time compilation - Wikipedia</a></li>

</ul>
</details>

**Discussion**: Commenters praised the project as impressive for an undergraduate, and noted that WASM overhead (~20%) is much lower than interpreter overhead (~1000%), explaining the performance win. Discussions also covered related methods like eval-based JIT in JavaScript, static recompilation of NES code, and the clever workaround of iOS JIT restrictions via WASM.

**Tags**: `#JIT`, `#WebAssembly`, `#Game Boy`, `#Emulation`, `#Performance`

---

<a id="item-5"></a>
## [Deep Dive: CUDA Kernel Execution Pipeline from CPU to GPU](https://fergusfinn.com/blog/what-happens-when-you-run-a-gpu-kernel/) ⭐️ 8.0/10

A detailed blog post walks through the entire process of launching a CUDA kernel, covering the CPU driver interaction, command submission, GPU hardware scheduling, and warp execution. This article bridges a critical gap in understanding GPU programming by explaining the often-opaque path from CUDA API calls to actual hardware execution, which is essential for performance optimization and debugging. The post devotes special attention to the doorbell register and queue management descriptor (QMD), which form the bridge between CPU-side CUDA runtime and GPU hardware. It also explains warp eligibility and scheduling in detail.

hackernews · mezark · Jun 29, 13:11 · [Discussion](https://news.ycombinator.com/item?id=48718863)

**Background**: CUDA (Compute Unified Device Architecture) is NVIDIA's parallel computing platform and programming model. A CUDA kernel is a function that runs on the GPU, launched from the CPU via a call to the CUDA runtime API. The GPU processes threads in groups of 32 called warps, which are scheduled by warp schedulers to hide memory latency.

<details><summary>References</summary>
<ul>
<li><a href="https://www.hpcs.cs.tsukuba.ac.jp/icpp2019/data/posters/Poster17-abst.pdf">Understanding the Overheads of Launching CUDA Kernels</a></li>
<li><a href="https://modal.com/gpu-glossary/device-hardware/warp-scheduler">What is a Warp Scheduler? | GPU Glossary</a></li>
<li><a href="https://stevengong.co/notes/Warp-Scheduling">Warp Scheduling (GPU Thread Scheduling)</a></li>

</ul>
</details>

**Discussion**: Commenters praised the article's depth, particularly the explanation of doorbell and QMD. One reader noted that CUDA's automatic command synchronization contrasts with Vulkan's explicit approach. Another speculated about open-source kernel optimization libraries potentially competing with commercial optimization companies.

**Tags**: `#CUDA`, `#GPU programming`, `#kernel execution`, `#NVIDIA`, `#HPC`

---

<a id="item-6"></a>
## [Ornith-1.0: Open-Weight LLMs Achieve SOTA in Agentic Coding](https://simonwillison.net/2026/Jun/29/ornith/#atom-everything) ⭐️ 8.0/10

DeepReinforce has released Ornith-1.0, a family of open-weight large language models (LLMs) under the MIT license, achieving state-of-the-art performance on coding benchmarks among open-source models of comparable size. The models, available in sizes from 9B to 397B parameters, are built on Google's Gemma 4 and Alibaba's Qwen 3.5. Ornith-1.0's open-weight, permissive license and strong coding performance make it a significant addition to the open-source AI ecosystem, potentially accelerating the development of autonomous coding agents. Its self-scaffolding approach could reduce the need for complex external toolkits in agentic workflows. The model family includes a 35B Mixture-of-Experts (MoE) variant and a 397B MoE variant, with the 35B GGUF file (~20GB) tested by Simon Willison using LM Studio and Pi, showing proficiency in multi-tool-call agent harnesses. The underlying models (Gemma 4 and Qwen 3.5) are both Apache 2.0 licensed, ensuring license compatibility.

rss · Simon Willison · Jun 29, 16:17

**Background**: Self-scaffolding LLMs can construct their own reasoning steps or tool calls without external orchestration, improving agentic coding capabilities. Open-weight models like Ornith-1.0 allow researchers and developers to run powerful LLMs locally or on custom infrastructure, reducing dependence on proprietary APIs. GGUF is a file format optimized for running LLMs on consumer hardware using projects like llama.cpp and LM Studio.

<details><summary>References</summary>
<ul>
<li><a href="https://simonwillison.net/2026/Jun/29/ornith/">Ornith-1.0: Self - Scaffolding LLMs for Agentic Coding</a></li>
<li><a href="https://deep-reinforce.com/ornith_1_0.html">Ornith-1.0: Self - Scaffolding LLMs ... | DeepReinforce Blog | Jun. 2026</a></li>

</ul>
</details>

**Tags**: `#LLM`, `#open-source`, `#coding`, `#AI`, `#machine learning`

---

<a id="item-7"></a>
## [Cerebras-OpenAI Deal Pushes Startups to Back of Waitlist](https://www.reddit.com/r/MachineLearning/comments/1uiqhiv/cerebras_openai_deal_capacity_has_effectively/) ⭐️ 8.0/10

A startup founder reports that Cerebras' $20 billion deal with OpenAI has pre-allocated nearly all of Cerebras' near-term inference capacity, making their API waitlist effectively infinite for smaller companies. This concentration of ASIC inference capacity in a single customer threatens to stifle innovation among AI startups that rely on fast, specialized hardware for real-time applications. The startup requires sustained high-throughput inference with 1-2k tokens/second and p95 latency constraints, which Cerebras' wafer-scale ASICs are well-suited to provide, but access is blocked by the deal.

reddit · r/MachineLearning · /u/Kortopi-98 · Jun 29, 12:00

**Background**: Cerebras produces wafer-scale AI chips that excel at inference due to high bandwidth and low latency. ASICs (Application-Specific Integrated Circuits) are more efficient than GPUs for dedicated inference workloads. OpenAI's massive order has consumed most of Cerebras' production capacity, highlighting a growing access inequality in AI hardware.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Cerebras">Cerebras Systems - Wikipedia</a></li>
<li><a href="https://www.cerebras.ai/chip">Product - Chip - Cerebras</a></li>
<li><a href="https://medium.com/@danny_54172/asic-inference-vs-non-inference-ai-chips-a5f1a5f05183">ASIC Inference vs. Non-Inference AI Chips | by Danny H Lee | Medium</a></li>

</ul>
</details>

**Discussion**: Community comments expressed frustration with the deal's impact on smaller players, with some suggesting that such concentration may lead to antitrust concerns, while others debated whether startups should pivot to alternative hardware or self-host.

**Tags**: `#AI Hardware`, `#Inference`, `#Startup Challenges`, `#Cerebras`, `#OpenAI`

---

<a id="item-8"></a>
## [Google's AI Peer-Reviewer Processed ~10K Papers at ICML/STOC](https://www.reddit.com/r/MachineLearning/comments/1uio9rb/googles_agentic_peerreviewer_handled_10k_papers/) ⭐️ 8.0/10

Google deployed an agentic AI system to peer-review approximately 10,000 papers at the ICML and STOC conferences, achieving a 30-minute turnaround per paper and catching 34% more mathematical errors than zero-shot prompting. The formal research paper detailing this system has now been published on arXiv. This demonstrates a significant real-world application of AI for scientific peer review at scale, potentially reducing reviewer burden and improving error detection. It sets a precedent for AI-assisted review in top conferences, which could transform how research is validated and published. The system is agentic, meaning it can autonomously read papers, identify mathematical errors, and provide feedback without human intervention. It achieved a 34% improvement in catching mathematical errors compared to zero-shot prompting, a baseline where the model is given no examples.

reddit · r/MachineLearning · /u/Justgototheeffinmoon · Jun 29, 10:05

**Background**: Agentic AI refers to systems that can perceive, reason, and act autonomously to achieve specific goals, often using large language models. Zero-shot prompting is a technique where a model performs a task without any prior examples. ICML and STOC are premier conferences in machine learning and theoretical computer science, respectively. Peer review is critical for ensuring research quality but is often slow and labor-intensive.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/AI_agent">AI agent - Wikipedia</a></li>
<li><a href="https://mitsloan.mit.edu/ideas-made-to-matter/agentic-ai-explained">Agentic AI, explained | MIT Sloan</a></li>
<li><a href="https://en.wikipedia.org/wiki/Zero-shot_prompting">Zero-shot prompting</a></li>

</ul>
</details>

**Tags**: `#AI`, `#peer review`, `#research automation`, `#machine learning`

---

<a id="item-9"></a>
## [EML Trees Proven as Universal Approximators](https://www.reddit.com/r/MachineLearning/comments/1uipl1t/eml_trees_are_universal_approximators_r/) ⭐️ 8.0/10

A new paper proves that EML trees—a compositional representation of elementary functions—are universal approximators for continuous functions and Sobolev spaces, providing an explicit construction using LEGO-like blocks. This result establishes EML trees as a theoretically grounded framework for function approximation, potentially offering an alternative to neural networks with explicit interpretability and guaranteed approximation capabilities. The proof includes explicit EML-type representations for binary operations, polynomials, hyperbolic tangent, and approximate partitions of unity. The authors also propose a learning algorithm for EML-type trees with fitting parameters and demonstrate its feasibility on practical optimization problems.

reddit · r/MachineLearning · /u/JoeGermany · Jun 29, 11:16

**Background**: Universal approximation theorems (UATs) are foundational results in machine learning, showing that neural networks with sufficient width or depth can approximate any continuous function. EML (Elementary Mathematical Language) trees compose elementary functions (like sin, exp, log) to represent complex functions. This work extends that idea by proving that such compositions can approximate a wide class of functions, not just elementary ones.

<details><summary>References</summary>
<ul>
<li><a href="https://arxiv.org/abs/2606.23179">[2606.23179] EML Trees Are Universal Approximators</a></li>
<li><a href="https://en.wikipedia.org/wiki/Universal_approximation_theorem">Universal approximation theorem</a></li>

</ul>
</details>

**Tags**: `#universal approximation`, `#EML trees`, `#function approximation`, `#machine learning theory`

---

<a id="item-10"></a>
## [CXMT signs nearly $3B DRAM deal with Tencent](https://www.reuters.com/world/china/chinas-cxmt-wins-3-billion-memory-supply-deal-with-tencent-sources-say-2026-06-29/) ⭐️ 8.0/10

CXMT has signed a long-term DRAM supply agreement with Tencent valued at over 200 billion RMB (approximately $2.94 billion), covering server memory for several years. This is one of the largest Chinese memory chip deals, signaling growing domestic substitution in the semiconductor supply chain and strengthening Tencent's server capacity for cloud and AI workloads. The deal duration is reported by sources to be three to five years. CXMT is also rumored to be in talks with other Chinese internet firms including Alibaba Cloud, ByteDance, and Xiaomi.

telegram · zaihuapd · Jun 29, 09:31

**Background**: DRAM (Dynamic Random Access Memory) is a type of volatile memory used in servers, PCs, and consumer electronics. CXMT is a leading Chinese DRAM manufacturer that has recently ramped up production of DDR5 and LPDDR5X chips. This deal helps reduce China's reliance on foreign memory suppliers like Samsung and SK Hynix.

<details><summary>References</summary>
<ul>
<li><a href="https://www.gys.cn/jichengdianluic/5510051897.html">CXMR4E832S6AS-AN1C 长 鑫 （ CXMT ） 存 储 芯片 应用：笔记本电脑</a></li>
<li><a href="https://www.chinaflashmarket.com/Producer/CXMT">长 鑫 存 储 _厂商主页_CFM闪 存 市场</a></li>

</ul>
</details>

**Tags**: `#DRAM`, `#半导体`, `#供应链`, `#长鑫存储`, `#腾讯`

---

<a id="item-11"></a>
## [Tesla FSD v14 Lite: HW4 Capabilities for HW3](https://x.com/Tesla_AI/status/2071592820889260101) ⭐️ 8.0/10

Tesla released FSD v14 Lite on June 29, 2026, for HW3 vehicles, distilling the HW4 neural network to about 15% size and enabling reinforcement learning, improved driving behaviors, and first-time parking functions. This update significantly extends the lifespan of older HW3 vehicles, providing near-HW4 autonomous driving capabilities without hardware upgrades, and sets a precedent for knowledge distillation in automotive AI. The distilled neural network runs on firmware 2026.20.5.1, first rolled out to early-access users. The update includes improved navigation, lane changes, pedestrian interaction, and new curbside parking, backing out, and reversing functions.

telegram · zaihuapd · Jun 30, 02:26

**Background**: HW3 (Hardware 3) is Tesla's first custom Full Self-Driving computer introduced in 2019, using a 14nm chip with limited memory compared to HW4 which debuted in 2023 with higher performance. Knowledge distillation is a technique where a large 'teacher' model (HW4) trains a smaller 'student' model (HW3) to mimic its behavior, enabling advanced capabilities on constrained hardware.

<details><summary>References</summary>
<ul>
<li><a href="https://www.notateslaapp.com/news/4369/tesla-launches-fsd-v14-lite-first-impressions">Tesla Launches FSD V 14 - Lite : First Impressions - Not a Tesla App</a></li>
<li><a href="https://electrek.co/2026/06/29/tesla-fsd-v14-lite-hw3-rollout/">Tesla starts FSD v 14 ' Lite ' rollout to HW3 cars | Electrek</a></li>
<li><a href="https://en.wikipedia.org/wiki/Tesla_Autopilot_hardware">Tesla Autopilot hardware - Wikipedia</a></li>

</ul>
</details>

**Tags**: `#Tesla`, `#FSD`, `#autonomous driving`, `#HW3`, `#HW4`

---