---
layout: default
title: "Horizon Summary: 2026-08-12 (EN)"
date: 2026-08-12
lang: en
---

> From 38 items, 12 important content pieces were selected

---

1. [New Attack Recovers Hidden Chain-of-Thought from OpenAI, Anthropic, and Google LLM APIs](#item-1) ⭐️ 9.0/10
2. [Compression Is Prediction: The Deep Link Between Data Compression and Machine Learning](#item-2) ⭐️ 8.0/10
3. [Nvidia Launches Nemotron 3.5 Lightning and NeMo Switchyard](#item-3) ⭐️ 8.0/10
4. [Go Is an Ideal Language for AI-Assisted Engineering, Says Rob Pike](#item-4) ⭐️ 8.0/10
5. [Nvidia's CUDA Moat Faces Demand Doubts and Open-Source Threats](#item-5) ⭐️ 8.0/10
6. [London Underground Expands Face-Scanning Trial](#item-6) ⭐️ 8.0/10
7. [Decoupled Descent: Enforcing Exact Train-Test Error Tracking via AMP Onsager Corrections](#item-7) ⭐️ 8.0/10
8. [Benign Long Context Passively Decouples RLHF Refusal in Small LLMs](#item-8) ⭐️ 8.0/10
9. [Graphene-powered soft lens could enable compact varifocal optics](#item-9) ⭐️ 8.0/10
10. [Cloudflare reports surge in DDoS attacks, over-1-Tbps up 519% QoQ](#item-10) ⭐️ 8.0/10
11. [NVIDIA reportedly developing Nemotron 4 open-source models with 1T+ parameters](#item-11) ⭐️ 8.0/10
12. [LTX Releases Open-Source Video Model LTX-2.5, Runs on Single RTX 5090](#item-12) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [New Attack Recovers Hidden Chain-of-Thought from OpenAI, Anthropic, and Google LLM APIs](https://stolen-thoughts.com/) ⭐️ 9.0/10

Researchers demonstrated a practical attack that recovers hidden chain-of-thought (CoT) reasoning from proprietary LLM APIs such as those of OpenAI, Anthropic, and Google, despite existing safeguards. The attack combines trace replay—feeding encrypted reasoning traces into weaker sibling models—with tool-based attacks to bypass protections. This matters because it undermines the privacy protections that frontier model providers rely on to keep their reasoning processes secret. It could enable model distillation, competitive intelligence gathering, and more effective jailbreaks, affecting security researchers, AI vendors, and enterprises using LLM APIs. The paper characterizes encrypted reasoning traces and shows that a compatible decoder model from the same provider can recover hidden reasoning across a broad range of models, providers, and trace formats. In the first-party attacker scenario, the adversary queries a capable, safeguarded target model to generate encrypted traces, then replays those traces into a weaker sibling model to recover the CoT.

hackernews · quantumgarbage · Aug 11, 13:22 · [Discussion](https://news.ycombinator.com/item?id=49257876)

**Background**: Chain-of-thought prompting improves LLM reasoning by having the model generate intermediate reasoning steps. To protect proprietary reasoning, OpenAI, Anthropic, and Google hide these steps from users, transmitting them as encrypted, base64-encoded envelopes that are passed back on subsequent calls to maintain multi-turn context. This research exploits the fact that encrypted traces must be decodable at some point, making them vulnerable to replay attacks when a compatible decoder exists.

<details><summary>References</summary>
<ul>
<li><a href="https://arxiv.org/pdf/2608.09867">Stealing Reasoning Traces from Proprietary LLM APIs</a></li>
<li><a href="https://cybersecuritynews.com/top-ai-models-apis-flaw-exposes-hidden-reasoning/">OpenAI, Anthropic, and Google LLM APIs vulnerability Exposes...</a></li>
<li><a href="https://www.alphaxiv.org/abs/2608.09867">Stealing Reasoning Traces from Proprietary LLM APIs | alphaXiv</a></li>

</ul>
</details>

**Discussion**: Commenters debated whether this is truly "stealing," arguing that paying users already paid for tokens but were denied access to the reasoning. Several shared related tricks, such as disabling thinking mode and providing a "deep_think" tool, while another noted that a simple developer prompt caused Codex to output encrypted compaction data in plaintext. Some expressed curiosity about cross-model replay and whether it was intentionally allowed.

**Tags**: `#security`, `#LLM`, `#privacy`, `#chain-of-thought`, `#jailbreak`

---

<a id="item-2"></a>
## [Compression Is Prediction: The Deep Link Between Data Compression and Machine Learning](https://ngrok.com/blog/compression-is-prediction) ⭐️ 8.0/10

The blog post 'Compression is prediction' proposes that data compression and prediction are fundamentally the same problem, with each being reducible to the other. This perspective frames LLMs and other AI systems as essentially prediction engines operating on compressed representations of data. This idea bridges information theory and modern machine learning, suggesting that compression benchmarks could serve as a proxy for intelligence and prediction capability. It could reshape how researchers evaluate and design AI models, including large language models, by highlighting compression as a core objective. The argument is grounded in concepts such as Kolmogorov complexity and the minimum description length (MDL) principle, where the shortest program describing data is considered the best model. The community response cites supporting materials, including Grant Sanderson's 'Compression is Intelligence' video and MacKay's textbook, indicating the idea has deep roots in information theory.

hackernews · nikolay · Aug 11, 19:49 · [Discussion](https://news.ycombinator.com/item?id=49263497)

**Background**: Kolmogorov complexity measures the length of the shortest computer program that produces a given object, capturing the object's inherent information content. The minimum description length principle applies this idea to model selection: the best model is the one that compresses the data most effectively. Because a good compressor implicitly captures the statistical regularities of data, it can be used for prediction, and vice versa. This equivalence has been recognized since the early days of cybernetics and remains a guiding principle in fields like algorithmic information theory and compression-based sequence prediction.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Kolmogorov_complexity">Kolmogorov complexity</a></li>
<li><a href="https://en.wikipedia.org/wiki/Minimum_Description_Length_Principle">Minimum Description Length Principle</a></li>
<li><a href="https://www.academia.edu/21919272/Compression_based_methods_for_nonparametric_on_line_prediction_regression_classification_and_density_estimation_of_time_series">(PDF) Compression based methods for nonparametric on-line...</a></li>

</ul>
</details>

**Discussion**: Commenters largely embrace the thesis, pointing to existing work such as Grant Sanderson's video 'Compression is Intelligence' and Cambridge's information theory course. Some share their own projects, like a binary inference dictionary for electoral NLP, demonstrating the idea's practical applications. Overall, the discussion is constructive and expands on the post's central claim rather than disputing it.

**Tags**: `#compression`, `#prediction`, `#information theory`, `#machine learning`, `#LLMs`

---

<a id="item-3"></a>
## [Nvidia Launches Nemotron 3.5 Lightning and NeMo Switchyard](https://blogs.nvidia.com/blog/nemotron-lightning-switchyard-rtx-dgx/) ⭐️ 8.0/10

Nvidia released the Nemotron 3.5 Lightning family, an open 30B Mixture-of-Experts model with 3B active parameters, and open-sourced NeMo Switchyard, a Rust-based library for routing LLM requests across models. The model claims up to 4x faster output speed and 30% faster agentic task completion compared with similar models. This matters because it pushes open, efficient small models and intelligent routing to the center of agentic AI, potentially cutting cost and latency for high-volume agent workloads. Developers deploying on RTX and DGX can now post-train a compact MoE model and route each workflow step to the most suitable model. The Nemotron 3.5 Lightning-30B-A3B-NVFP4 checkpoint is available on Hugging Face and is commercial-ready, released with speculative decoding methods for faster generation. NeMo Switchyard is a Rust proxy/library for LLM traffic that automatically routes prompts to the most capable and efficient model based on task needs.

hackernews · droidjj · Aug 11, 19:35 · [Discussion](https://news.ycombinator.com/item?id=49263340)

**Background**: Mixture-of-Experts models keep total parameter counts large but activate only a small subset of parameters per token, making them fast and efficient for high-volume serving. Model routing, like NeMo Switchyard, addresses the reality that no single model is best for every step of an agent workflow. Agentic AI often chains many LLM calls, so routing and small specialized models can lower infrastructure costs while preserving accuracy.

<details><summary>References</summary>
<ul>
<li><a href="https://blogs.nvidia.com/blog/nemotron-lightning-switchyard-rtx-dgx/">NVIDIA Nemotron 3.5 Lightning and NeMo Switchyard Deliver Faster, Smarter, More Efficient Agentic AI | NVIDIA Blog</a></li>
<li><a href="https://developer.nvidia.com/blog/nvidia-nemotron-3-5-lightning-delivers-fast-accurate-specialized-task-execution-for-long-running-agents/">NVIDIA Nemotron 3.5 Lightning Delivers Fast, Accurate Specialized Task Execution for Long-Running Agents | NVIDIA Technical Blog</a></li>
<li><a href="https://github.com/NVIDIA-NeMo/Switchyard">GitHub - NVIDIA-NeMo/Switchyard · GitHub</a></li>

</ul>
</details>

**Discussion**: Commenters largely welcomed the efficiency push but raised practical concerns: one developer found MoE models like Nemotron 3.5 Lightning and Qwen 35B performed poorly on a coding-agent task, while dense ~30B models did better. Others asked how routers handle prompt caching and session stickiness, and a commenter criticized the included benchmark graphs for omitting Qwen models rather than including an out-of-league variant.

**Tags**: `#NVIDIA`, `#LLM`, `#Mixture-of-Experts`, `#Model Routing`, `#AI Infrastructure`

---

<a id="item-4"></a>
## [Go Is an Ideal Language for AI-Assisted Engineering, Says Rob Pike](https://developers.googleblog.com/why-go-is-an-ideal-language-for-ai-assisted-software-engineering/) ⭐️ 8.0/10

Rob Pike, a creator of Go, published an article on the Google Developers Blog arguing that Go's simplicity, tooling, and static typing make it especially suited to AI-assisted software engineering. The post generated significant discussion, with 324 comments. This argument matters because teams are increasingly choosing languages based on how well AI coding assistants can generate and maintain code in them. The debate it sparked shows that the language community is split, as proponents at Netflix report better Go output while Rust advocates argue a stricter compiler is more LLM-friendly. The article appeared on Google's official developers blog with the title 'Why Go is an ideal language for AI-assisted software engineering.' In the comments, a Netflix Go guild lead confirmed increased reports of AI agents writing better Go code, while other developers countered that Go's weak abstraction and concurrency issues make it risky for LLM-generated code.

hackernews · 0xedb · Aug 11, 16:57 · [Discussion](https://news.ycombinator.com/item?id=49261133)

**Background**: AI-assisted software engineering uses large language models to write or complete source code, and language design can heavily influence how reliable the generated code is. Go is known for its minimal syntax, built-in formatting with gofmt, and strong standard tooling, which may make it easier for both humans and AI to predict and verify. The broader industry is actively debating which languages will be most productive in an AI-driven workflow, with Rust and Go emerging as two common candidates.

**Discussion**: Comment sentiment is sharply divided. A Netflix Go guild lead said the article matches their internal data, while a commenter preferring Rust argued that a fussy compiler surfaces errors at compile time, which suits LLM workflows better. Another skeptic warned that LLMs can produce buggy concurrent Go code faster, making Go a risky choice for teams without enough senior reviewers.

**Tags**: `#Go`, `#AI-assisted software engineering`, `#programming languages`, `#large language models`, `#developer tools`

---

<a id="item-5"></a>
## [Nvidia's CUDA Moat Faces Demand Doubts and Open-Source Threats](https://stratechery.com/2026/nvidias-risky-business/) ⭐️ 8.0/10

The article analyzes Nvidia's strategic vulnerabilities, arguing that its CUDA software ecosystem dominance is fragile and that market demand forecasts for AI compute may be overestimated. It highlights the risk that second-order assumptions about demand growth could fail. Nvidia's stock and market position hinge on sustained AI compute demand and CUDA's lock-in. If open-source alternatives emerge or demand growth slows, the semiconductor giant's valuation and ecosystem advantage could erode significantly, affecting the entire AI supply chain. The analysis is from Stratechery's Ben Thompson and draws attention to CUDA's programming model, which is powerful for optimization but notoriously painful to use. Community discussion also points to potential moves by Google, AMD, or a 'Manhattan Project' style effort to build an open-source CUDA alternative.

hackernews · jonbaer · Aug 11, 10:02 · [Discussion](https://news.ycombinator.com/item?id=49255710)

**Background**: CUDA (Compute Unified Device Architecture) is Nvidia's proprietary platform for general-purpose GPU computing, enabling developers to use C++, Python, and frameworks like PyTorch for AI workloads. It is deeply entrenched in machine learning research and production, creating a powerful moat for Nvidia's hardware sales. However, the platform's complexity and vendor lock-in have long drawn criticism, and industry players are increasingly interested in open alternatives.

<details><summary>References</summary>
<ul>
<li><a href="https://koder.ai/blog/nvidia-accelerated-computing-gpus-cuda-ai-infrastructure">NVIDIA ’s Accelerated Computing Stack: GPUs, CUDA , AI ... | Koder. ai</a></li>
<li><a href="https://www.modular.com/blog/democratizing-ai-compute-part-4-cuda-is-the-incumbent-but-is-it-any-good">CUDA is the incumbent, but is it any good? (Democratizing AI ...)</a></li>

</ul>
</details>

**Discussion**: Commenters largely agree that Nvidia's advantage is software entrenchment rather than raw hardware, but they debate the durability of that moat. Some note CUDA C/C++ is a poor developer experience and predict that a large customer or hyperscaler could fund an open-source alternative. Others caution that first-order demand for compute is real, yet second-order growth expectations are likely exaggerated.

**Tags**: `#nvidia`, `#cuda`, `#ai-chips`, `#semiconductors`, `#market-analysis`

---

<a id="item-6"></a>
## [London Underground Expands Face-Scanning Trial](https://www.btp.police.uk/news/btp/news/england/btp-expands-live-facial-recognition-lfr-trial-into-london-underground-stations/) ⭐️ 8.0/10

The British Transport Police has expanded its Live Facial Recognition (LFR) trial into London Underground stations, with cameras now scanning passengers' faces in real time. The expansion extends an existing police trial that uses real-time face matching against a watchlist. This brings biometric surveillance into one of the world's busiest transit systems, affecting millions of daily commuters. It raises serious privacy and civil-liberty questions and could set a precedent for routine facial monitoring in public spaces across the UK. The trial uses Live Facial Recognition (LFR) technology, which compares live CCTV images against a police watchlist in real time. Critics argue there is no clear failure case for such a pilot, because the surveillance infrastructure is likely to remain once deployed.

hackernews · BlueBerry2001 · Aug 11, 09:40 · [Discussion](https://news.ycombinator.com/item?id=49255496)

**Background**: Live Facial Recognition (LFR) is a biometric surveillance technology that scans faces in crowds and matches them against a database, typically of wanted persons. Police say it helps arrest fugitives, while civil-liberties groups warn it is inaccurate, biased, and invasive. The London Underground is a central part of the city's public transport, carrying millions of people daily, so even a trial deployment is highly consequential.

**Discussion**: Commenters are overwhelmingly critical. One notes that anonymous travel on the Underground was already lost when contactless bank cards became the main entry method; another calls Britain 'the original Orwellian society' and questions what a failed trial would even look like. A third compares the surveillance unfavorably with China, saying London offers surveillance without safety while serious criminals are released after six months.

**Tags**: `#facial-recognition`, `#surveillance`, `#privacy`, `#civil-liberties`, `#London-Underground`

---

<a id="item-7"></a>
## [Decoupled Descent: Enforcing Exact Train-Test Error Tracking via AMP Onsager Corrections](https://www.reddit.com/r/MachineLearning/comments/1vlu1se/decoupled_descent_enforcing_exact_traintest_error/) ⭐️ 8.0/10

The paper introduces Decoupled Descent (DD), a training algorithm that applies approximate message passing (AMP) Onsager corrections to enforce a train-test identity, certifying that training error asymptotically equals test error at every parameter iterate. It frames the generalization gap as a consequence of data reuse bias and demonstrates the method on Gaussian mixture models. This matters because it offers a principled, theory-grounded way to address the long-standing generalization gap in deep learning, where training error drops while test error stagnates or rises. By certifying train-test error tracking, it could enable more reliable model selection, optimal stopping, and hyperparameter tuning. The method is developed on stylized Gaussian mixture models and full-batch gradient descent, using AMP's Onsager correction from high-dimensional statistics to decouple errors. It is a theory paper that does not yet scale to very large models, but the author plans to release a PyTorch-compatible implementation.

reddit · r/MachineLearning · /u/mlovik1 · Aug 11, 21:06

**Background**: In supervised learning, the generalization gap refers to the difference between training error and test error; it often appears when a model memorizes the training data rather than learning patterns that generalize. Approximate message passing (AMP) is an iterative algorithm from compressed sensing and high-dimensional statistics whose Onsager correction subtracts self-interference across iterations, allowing errors to be tracked as if each step were independent. Decoupled Descent borrows this idea to create a training procedure where the train error is provably coupled to test error at each iteration.

<details><summary>References</summary>
<ul>
<li><a href="https://arxiv.org/html/2604.27883v1">Decoupled Descent: Exact Test Error Tracking Via Approximate Message Passing</a></li>
<li><a href="https://arxiv.org/abs/1607.05966">[1607.05966] Onsager-corrected deep learning for sparse linear inverse problems</a></li>
<li><a href="https://krzakala.github.io/cargese.io/AMP_Tutorial_18.pdf">Approximate Message Passing Tutorial</a></li>

</ul>
</details>

**Tags**: `#machine learning`, `#optimization`, `#generalization`, `#approximate message passing`, `#theory`

---

<a id="item-8"></a>
## [Benign Long Context Passively Decouples RLHF Refusal in Small LLMs](https://www.reddit.com/r/MachineLearning/comments/1vm16hs/contextinduced_activation_drift_long_benign/) ⭐️ 8.0/10

Researchers show that feeding a long, benign, semantically coherent prefix (100–3000 tokens) into Google's gemma-3-1b-it causes a large internal activation shift at deep layers, which decouples RLHF refusal behavior without any adversarial prompt or jailbreak. A shuffled-text ablation confirms the effect is semantics-driven, not a positional artifact. This challenges the assumption that RLHF alignment is a robust, invariant property of aligned models, showing that even benign context can passively change safety behavior. It has important implications for LLM safety evaluation, alignment robustness, and the design of safeguards against unintended jailbreak-like states. The study tracks Excess Semantic Attention (ΔA_sem), a latent vector L2 shift (Δh_2 ≈ 3434 at Layer 22, ~85% depth), logit divergence (D_KL ≈ 22.87 nats), and an entropy surge (up to 325×) on the first generated token. The shuffle ablation destroys semantic coherence while keeping length, vocabulary, and token frequency identical, and it fails to reproduce the drift, isolating semantics as the driver.

reddit · r/MachineLearning · /u/PresentSituation8736 · Aug 12, 02:09

**Background**: RLHF (reinforcement learning from human feedback) is the standard method for aligning LLMs with human preferences, typically teaching models to refuse harmful requests. Activation drift refers to gradual or context-induced changes in a model's internal representations. RoPE (rotary position embedding) encodes word order in transformers, which the authors rule out as a cause via the shuffled-text ablation.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Reinforcement_learning_from_human_feedback">Reinforcement learning from human feedback - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Representational_drift">Representational drift - Wikipedia</a></li>
<li><a href="https://1y33.github.io/blog/rope/">1y33.github.io/blog/ rope</a></li>

</ul>
</details>

**Tags**: `#mechanistic interpretability`, `#RLHF alignment`, `#LLM safety`, `#activation drift`, `#language models`

---

<a id="item-9"></a>
## [Graphene-powered soft lens could enable compact varifocal optics](https://www.qmul.ac.uk/news/latest-news/2026/science-and-engineering/se/new-graphene-powered-soft-lens-could-pave-the-way-for-smarter-glasses-cameras-and-medical-devices.html) ⭐️ 8.0/10

Researchers at Queen Mary University of London developed a transparent soft lens using reduced graphene oxide electrodes that changes focal length via an electric field. The prototype was published in the journal Advanced Functional Materials. This technology could replace bulky mechanical components in autofocus cameras, wearable displays, VR/AR headsets, and miniature medical imaging devices. It represents a step toward compact varifocal lenses with broad consumer and medical applications. The prototype integrates ultra-thin transparent graphene electrodes directly onto the actuator layer beneath the lens, overcoming the opacity limitation that previously forced electrodes to the lens edge. Further optimization of electrode transparency and performance is still needed.

telegram · zaihuapd · Aug 11, 12:27

**Background**: The lens is based on dielectric elastomer actuators, a class of electroactive polymers that deform when an electric field is applied, converting electrical energy into mechanical work. These actuators are used in soft robotics and artificial muscle research. Reduced graphene oxide is a commercially accessible form of graphene that can be mass-produced and used as transparent electrodes in such devices.

<details><summary>References</summary>
<ul>
<li><a href="https://techxplore.com/news/2026-08-graphene-powered-soft-lens-pave.html">Graphene-powered soft lens could pave the way for smarter glasses...</a></li>
<li><a href="https://en.wikipedia.org/wiki/Dielectric_elastomer_actuator">Dielectric elastomer actuator</a></li>

</ul>
</details>

**Tags**: `#graphene`, `#optics`, `#adaptive lens`, `#materials science`, `#medical devices`

---

<a id="item-10"></a>
## [Cloudflare reports surge in DDoS attacks, over-1-Tbps up 519% QoQ](https://blog.cloudflare.com/ddos-threat-report-2026-h1/) ⭐️ 8.0/10

Cloudflare's 2026 H1 DDoS Threat Report says it mitigated 935 network-layer DDoS attacks over 1 Tbps in H1 2026, with Q2 up 519% QoQ. DNS floods surged 580% QoQ, becoming the third-largest attack type in Q2. The rapid growth of massive multi-terabit attacks and DNS floods signals escalating infrastructure-level threats, pressuring organizations to strengthen network defense. Media, publishing, and government sectors are increasingly targeted, making this data critical for security planning. In Q2, over-1-Tbps attacks rose to 805, more than six times Q1; DNS floods accounted for 34.3% of network-layer attacks in H1. Media, publishing, and production was the most attacked industry in both quarters, while government jumped from 29th to 9th.

telegram · zaihuapd · Aug 11, 13:20

**Background**: A DNS flood is a DDoS attack that overwhelms DNS servers with massive volumes of queries, disrupting domain resolution. Network-layer (Layer 3) DDoS attacks target network infrastructure by flooding devices like routers and firewalls with packets, while HTTP floods attack applications at Layer 7. These concepts help clarify the report's statistics.

<details><summary>References</summary>
<ul>
<li><a href="https://www.cloudflare.com/learning/ddos/dns-flood-ddos-attack/">DNS flood DDoS attack | Learning Center</a></li>
<li><a href="https://www.fastly.com/learning/security/the-different-types-of-ddos-attacks">The Different Types of DDoS Attacks | Fastly</a></li>
<li><a href="https://en.wikipedia.org/wiki/DNS_Flood">DNS Flood - Wikipedia</a></li>

</ul>
</details>

**Tags**: `#DDoS`, `#Cloudflare`, `#Network Security`, `#Cybersecurity`, `#Attack Trends`

---

<a id="item-11"></a>
## [NVIDIA reportedly developing Nemotron 4 open-source models with 1T+ parameters](https://economictimes.indiatimes.com/tech/artificial-intelligence/nvidia-is-developing-nemotron-4-open-source-models-the-information/articleshow/133157952.cms) ⭐️ 8.0/10

According to The Information, NVIDIA is developing the Nemotron 4 family of open-source models, with the largest version expected to exceed 1 trillion parameters. The report, citing several employees, says training could finish as early as late autumn, though no official release date has been set. If true, this would position NVIDIA as a major contender in open-source large language models, directly competing with top-tier open models. A 1T+ parameter open model could significantly advance reasoning, coding, and agentic AI capabilities, affecting developers and enterprises that rely on open alternatives. The same day, NVIDIA reportedly released Nemotron 3.5 Lightning for code review tasks and NeMo Switchyard, a model routing library for automatic task distribution. The 1T+ parameter figure is based on leaks and has not been officially confirmed by NVIDIA.

telegram · zaihuapd · Aug 12, 01:15

**Background**: Nemotron is a family of AI models developed by Nvidia, including large language models and multimodal models, with open weights, training data, and training methods released for parts of the family. In June 2024, NVIDIA released the Nemotron-4 340B family under a permissive open model license. Open-source models with over 1 trillion parameters are extremely rare today, so a 1T open model would be a significant milestone. NeMo Switchyard is a library that routes AI agent workloads across different models based on task requirements, reducing cost and improving efficiency.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Nemotron">Nemotron</a></li>
<li><a href="https://research.nvidia.com/publication/2024-06_nemotron-4-340b">Nemotron-4 340B | Research</a></li>
<li><a href="https://developer.nvidia.com/blog/route-ai-agent-workloads-across-models-with-nvidia-nemo-switchyard/">Route AI Agents Across Models with NVIDIA NeMo Switchyard</a></li>

</ul>
</details>

**Tags**: `#NVIDIA`, `#LLM`, `#Open Source`, `#AI`, `#Nemotron`

---

<a id="item-12"></a>
## [LTX Releases Open-Source Video Model LTX-2.5, Runs on Single RTX 5090](https://ltx.io/model/ltx-2-5) ⭐️ 8.0/10

LTX released LTX-2.5, an open-source video generation foundation model, making weights, training code, and inference pipeline publicly available. It runs on a single RTX 5090 and supports text-to-video and image-to-video generation. This matters because open-sourcing a competitive video model with full training and inference code lowers the barrier for researchers and small teams. It also demonstrates that high-quality video generation can run on consumer hardware, potentially accelerating innovation in AI video. The model improves multi-shot coherence and prompt adherence, using a new diffusion video decoder and a Gemma 4 12B text encoder. In a 98-prompt flaw evaluation, LTX 2.5 Pro ranked first among ten models; commercial use is free for companies with annual revenue below $10 million.

telegram · zaihuapd · Aug 12, 02:15

**Background**: Video generation models traditionally require powerful cloud infrastructure and are often closed. LTX-2.5 follows a trend of open-weight models that run locally, with the diffusion decoder being a small diffusion model that denoises pixels conditioned on latent representations, and Gemma 4 12B serving as a modern open text encoder.

<details><summary>References</summary>
<ul>
<li><a href="https://ltx.io/model/ltx-2-5">LTX - 2 . 5 : LTX's Latest AI Open-Source Foundation Model | LTX</a></li>
<li><a href="https://github.com/huggingface/diffusers/blob/main/src/diffusers/pipelines/ltx2/pipeline_ltx2_diffusion_decode.py">diffusers/src/diffusers/pipelines/ltx2/pipeline_ltx2_ diffusion _ decode .py...</a></li>
<li><a href="https://blog.google/innovation-and-ai/technology/developers-tools/introducing-gemma-4-12b/">Introducing Gemma 4 12 B</a></li>

</ul>
</details>

**Tags**: `#video-generation`, `#open-source`, `#AI`, `#text-to-video`, `#model-release`

---