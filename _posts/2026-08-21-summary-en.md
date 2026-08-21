---
layout: default
title: "Horizon Summary: 2026-08-21 (EN)"
date: 2026-08-21
lang: en
---

> From 47 items, 11 important content pieces were selected

---

1. [Malicious Rust crate arrayref delivers build-time payload](#item-1) ⭐️ 9.0/10
2. [Linux Kernel 7.2 Released With Notable Improvements](#item-2) ⭐️ 9.0/10
3. [GitHub Outage Post-Mortem: Retry Bug and Soaring Commit Growth](#item-3) ⭐️ 8.0/10
4. [AliExpress silent WebAudio fingerprinting breaks Bluetooth multipoint](#item-4) ⭐️ 8.0/10
5. [125M Transformer Autocompletes Piano Performances in Real Time on iPhone](#item-5) ⭐️ 8.0/10
6. [The Spectral Neuron: A New ML Primitive for Scalable, Interpretable Models](#item-6) ⭐️ 8.0/10
7. [Mini Kimi K3 Replica Trained for Under $250 Beats GPT-2 124M](#item-7) ⭐️ 8.0/10
8. [OpenAI Previews Private Security Processing, Zero-Data Retention for Frontier Models](#item-8) ⭐️ 8.0/10
9. [Stripe Reportedly to Acquire OpenRouter for Over $7 Billion](#item-9) ⭐️ 8.0/10
10. [Terence Tao warns AI could trigger math's biggest crisis since Gödel](#item-10) ⭐️ 8.0/10
11. [Reverse-Lookup Service Breach Exposes Millions of Face Photos](#item-11) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Malicious Rust crate arrayref delivers build-time payload](https://safedep.io/arrayref-proc-macro1-rust-build-time-malware/) ⭐️ 9.0/10

A compromised release of the widely used Rust crate arrayref was published to crates.io and pulled in a typosquatted dependency named proc-macro1, whose build script downloaded and executed a remote binary during compilation. The Rust Project removed the malicious versions of arrayref and two related crates—internment and append-only-vec—after the incident. This supply-chain attack hit a crate with more than 245 million downloads, demonstrating how a compromised maintainer account and malicious build scripts can poison the entire Rust ecosystem. It also exposes gaps in crates.io's incident response, including missing security advisories and yank notifications for removed releases. The attacker chained the arrayref update with new releases of internment and append-only-vec, all depending on the typosquatted proc-macro1 package. The malicious versions were silently removed from crates.io, and the incident is tracked in RustSec advisory-db issue #3161, prompting community calls for Cargo build script sandboxing.

hackernews · abhisek · Aug 20, 13:23 · [Discussion](https://news.ycombinator.com/item?id=49374269)

**Background**: Rust crates are distributed through the crates.io registry, and many crates include build scripts (build.rs) that run arbitrary code at compile time, making them a powerful but risky extension point. Typosquatting is a supply-chain technique where an attacker publishes a package with a name similar to a popular one, hoping it gets used directly or pulled in as a transitive dependency. Compromised maintainer accounts have become an increasingly common vector for injecting malware into open-source ecosystems.

<details><summary>References</summary>
<ul>
<li><a href="https://thehackernews.com/2026/08/rust-supply-chain-attack-puts-build.html">Rust Supply Chain Attack Puts Build-Time Malware in Crates with 245 Million Downloads</a></li>
<li><a href="https://www.stepsecurity.io/blog/arrayref-rust-crate-supply-chain-attack">Rust Supply-Chain Attack: arrayref, internment, and append-only-vec Poisoned by the proc-macro1 Build-Time Dropper - StepSecurity</a></li>

</ul>
</details>

**Discussion**: Commenters criticized crates.io's handling, noting that the malicious version disappeared without a yank indicator or security advisory. Several argued that Rust's heavy reliance on hundreds of transitive dependencies makes such attacks likely, and renewed calls for sandboxing build.rs scripts, referencing previous proposals that stalled.

**Tags**: `#security`, `#supply-chain`, `#rust`, `#malware`, `#open-source`

---

<a id="item-2"></a>
## [Linux Kernel 7.2 Released With Notable Improvements](https://www.igalia.com/2026/08/19/Linux-72-Released.html) ⭐️ 9.0/10

The Linux kernel 7.2 has been released, with the announcement published on Igalia's website on August 19, 2026. The release has generated strong community engagement, including discussions about HDMI 2.1 support in AMD's open-source driver and the kernel's ongoing evolution. As a major kernel release, Linux 7.2 affects the entire open-source ecosystem, from desktop users to embedded systems such as the Raspberry Pi. The community discussion highlights both persistent challenges like HDMI 2.1 support and the kernel's long-term development over 35 years. The announcement received a 9.0/10 score with 192 points and 67 comments. A commenter recalls that HDMI 2.1 support in AMD's open-source driver was previously blocked by the HDMI Forum, and asks what changed to enable it; the available material does not provide an official answer.

hackernews · mariuz · Aug 20, 15:46 · [Discussion](https://news.ycombinator.com/item?id=49376265)

**Background**: The Linux kernel is the core of Linux-based operating systems, first released by Linus Torvalds in 1991 and now developed by thousands of contributors worldwide. New kernel versions are regularly released, each with extensive changelogs covering new hardware support, performance improvements, and bug fixes. Issues like HDMI 2.1 support can involve industry licensing bodies such as the HDMI Forum, which may restrict open-source implementations. Companies like Igalia contribute to the kernel and often publish announcements about major releases.

**Discussion**: Commenters note the contrast between the kernel's seemingly unchanged user experience and its rich, always-growing changelog. One user expresses excitement about updating their Raspberry Pi 4, while another asks what changed to allow HDMI 2.1 support in AMD's open-source driver. A less technical reader questions who the target audience is, and one commenter compares the coverage to LWN's reporting.

**Tags**: `#linux`, `#kernel`, `#open source`, `#release`

---

<a id="item-3"></a>
## [GitHub Outage Post-Mortem: Retry Bug and Soaring Commit Growth](https://github.blog/news-insights/company-news/the-august-17-outage-and-the-work-ahead/) ⭐️ 8.0/10

GitHub published a post-mortem of the August 17 outage, attributing it to a client-side retry loop triggered by service errors and a latent retry bug in VS Code that amplified traffic roughly 10x, delaying recovery of the Copilot Token Service. The report also revealed monthly commits grew from 1.4 billion to 2.9 billion since April. This incident underscores how simple client-side retry logic can cascade into a major outage, especially at GitHub's scale where even small inefficiencies are amplified. It also highlights the operational pressure caused by unprecedented growth in developer activity, raising questions about the sustainability of free-tier services and AI-driven workloads. The retry storm originated from delayed replies to a single internal endpoint, and the VS Code retry bug did not have proper backoff or caps. GitHub noted the difficulty of recovering while handling 10x normal traffic, and the growth in commits reflects industry-wide 'productivity panic' with heavy AI-assisted coding.

hackernews · 0xedb · Aug 20, 19:22 · [Discussion](https://news.ycombinator.com/item?id=49378957)

**Background**: A retry storm occurs when many clients retry failing requests simultaneously, overwhelming the service and delaying recovery. Best practices include exponential backoff, jitter, capping retry attempts, and using circuit breakers to prevent such cascades. GitHub's outage is a real-world example of the Retry Storm antipattern described in Microsoft's Azure Architecture Center.

<details><summary>References</summary>
<ul>
<li><a href="https://learn.microsoft.com/en-us/azure/architecture/antipatterns/retry-storm/">Retry Storm Antipattern - Azure Architecture Center Advanced Client-side Transaction Retries - CockroachDB Advanced Client-side Transaction Retries - CockroachDB Top 9 Retry Policies That Don’t Create Storms - Medium Retry pattern - Azure Architecture Center | Microsoft Learn Which HTTP Error Status Codes Should Not Be Retried? - Baeldung</a></li>
<li><a href="https://jeffbailey.us/blog/2025/12/16/what-is-a-retry-storm/">What Is a Retry Storm? | Jeff Bailey</a></li>
<li><a href="https://keyholesoftware.com/preventing-retry-storms-with-responsible-client-policies/">How to Prevent Retry Storms with Responsible Client-Side ...</a></li>

</ul>
</details>

**Discussion**: Commenters criticized the error-handling philosophy that hides errors behind spinners, and some doubted GitHub can keep up with scale without charging for currently free features. Others noted that Microsoft's AI interests may intentionally subsidize heavy AI-driven usage, making simple fee-based fixes unlikely.

**Tags**: `#github`, `#outage`, `#postmortem`, `#reliability`, `#devops`

---

<a id="item-4"></a>
## [AliExpress silent WebAudio fingerprinting breaks Bluetooth multipoint](https://blog.laserphile.com/2026/08/aliexpress-webpage-keeping-multipoint.html) ⭐️ 8.0/10

A developer found that AliExpress's webpage creates two hidden AudioContext objects to run silent WebAudio fingerprinting, which interrupts Bluetooth multipoint audio playback when the tab is open in Firefox. The silent tab caused connected multipoint headphones to stop playing audio from other sources. This matters because AliExpress is a widely used site, and its privacy-invasive audio API usage produces real device side effects for users with multipoint Bluetooth headphones. It highlights how WebAudio fingerprinting can harm the broader browsing experience and underscores the need for browsers to detect and block silent audio processing. The page is silent but creates two AudioContext objects purely for fingerprinting, according to the finding. This can also keep mobile browsers running in the background, and related comments report similar Bluetooth disruptions with hearing aids and car audio systems.

hackernews · emctech · Aug 20, 10:08 · [Discussion](https://news.ycombinator.com/item?id=49372583)

**Background**: WebAudio fingerprinting uses the Web Audio API to render a silent waveform and hash the resulting audio output, producing a stable browser or device identifier that can survive private mode, cleared cookies, and VPN changes. Bluetooth multipoint is a feature that lets one headset maintain simultaneous connections to two or more source devices, such as a phone and a laptop, so audio can be shared or switched between them.

<details><summary>References</summary>
<ul>
<li><a href="https://elsolitario.org/en/2026/08/20/aliexpress-webaudio-fingerprinting-bluetooth-en/">WebAudio Fingerprinting: The AliExpress Case - elsolitario.org</a></li>
<li><a href="https://fingerprint.com/blog/audio-fingerprinting/">Audio Fingerprinting: What It Is + How It Works with Web API</a></li>
<li><a href="https://www.soundguys.com/bluetooth-multipoint-explained-28601/">What is Bluetooth multipoint? - SoundGuys</a></li>

</ul>
</details>

**Discussion**: Commenters shared related real-world issues, such as hearing aids changing amplification on websites and the AliExpress iOS app triggering car audio commands, and called for browsers to show the speaker icon whenever such audio tricks occur. Some noted that Firefox and other browsers are already working to mitigate WebAudio fingerprinting, while others questioned whether Apple would remove AliExpress from the App Store over similar behavior.

**Tags**: `#web-privacy`, `#fingerprinting`, `#webaudio`, `#browser-security`, `#bluetooth`

---

<a id="item-5"></a>
## [125M Transformer Autocompletes Piano Performances in Real Time on iPhone](https://simedw.com/2026/08/20/midi-autocomplete/) ⭐️ 8.0/10

A developer trained a 125M-parameter transformer to autocomplete MIDI piano pieces and runs it entirely on-device, reaching about 108 notes per second on an iPhone 15. The result is a free app that continues a user's playing after just a few notes, like code autocomplete for piano. This shows that useful generative music models can run in real time on a phone, with no server latency and no data leaving the device. It also points toward a broader shift in creative tools, where "generation" is nearly free and the remaining value lies in human taste and fast exploration of musical ideas. The model is a 125M-parameter transformer trained on MIDI data, and the app uses Apple's Core ML framework to keep inference on-device. The developer says the idea is like GitHub Copilot or Tabnine: the user prompts it by playing notes on a MIDI keyboard, and it continues the performance.

hackernews · simedw · Aug 20, 12:04 · [Discussion](https://news.ycombinator.com/item?id=49373456)

**Background**: MIDI (Musical Instrument Digital Interface) is a standard protocol for connecting and communicating between electronic musical instruments, computers, and audio devices, so it is a natural representation for piano performances. Core ML is Apple's framework for integrating machine learning models into apps, providing a unified model representation and performing predictions on device. Transformer models, originally developed for language, are well suited to sequence tasks like music continuation, and can be compressed and optimized to run on mobile hardware.

<details><summary>References</summary>
<ul>
<li><a href="https://developer.apple.com/machine-learning/">AI & Machine Learning - Apple Developer</a></li>
<li><a href="https://en.wikipedia.org/wiki/MIDI">MIDI - Wikipedia</a></li>
<li><a href="https://github.com/apple/coremltools">GitHub - apple/coremltools: Core ML tools contain supporting tools for Core ML model conversion, editing, and validation. · GitHub</a></li>

</ul>
</details>

**Discussion**: Commenters connected the project to classical music pedagogy, noting that "autocomplete" patterns were fundamental to how composers like Rachmaninoff trained. Others drew parallels to AI-based UX design tools, arguing that when generation costs zero, the remaining skill is taste, and a software designer praised the idea of using such models to find dead ends faster. One listener found the way the model took Für Elise in a different direction "surprisingly disconcerting," and another pointed to a related project that algorithmically generated every possible melody to fight music copyright lawsuits.

**Tags**: `#machine-learning`, `#music-generation`, `#core-ml`, `#transformer`, `#on-device-ai`

---

<a id="item-6"></a>
## [The Spectral Neuron: A New ML Primitive for Scalable, Interpretable Models](https://www.reddit.com/r/MachineLearning/comments/1vtfimo/the_spectral_neuron_an_ml_primitive_for_scalable/) ⭐️ 8.0/10

A new preprint titled "The Spectral Neuron" introduces a machine learning primitive of the form f(x) = λ_k(A0 + Σ x_i A_i), with theoretical analysis, a practical initialization and training recipe, and scaling experiments on synthetic and real data. Open-source code is available on GitHub. This primitive is designed to simultaneously offer simplicity, scalability, interpretability, and controllability—qualities that are often in tension in modern ML. By providing mathematical foundations and training recipes, it could enable engineers and researchers to build models whose behavior can be inspected and constrained directly from learned matrices. The model looks like a simple one-liner, but its expressivity depends on the size of the matrices; the paper analyzes what can be read directly from learned matrices and which shapes can be guaranteed by construction. The author notes that the code was heavily AI-written and reviewed by the author, while the manuscript used AI assistance for literature review.

reddit · r/MachineLearning · /u/alexsht1 · Aug 20, 10:20

**Background**: In machine learning, a primitive is the smallest atomic unit of processing, analogous to a neuron in a neural network. Spectral methods have emerged as a simple yet effective approach for extracting information from massive, noisy and incomplete data, often using eigenvalues and eigenvectors of matrices. The spectral neuron combines these ideas by defining a model as the k-th eigenvalue of a linear matrix combination, which can be scaled and interpreted through the learned matrices.

<details><summary>References</summary>
<ul>
<li><a href="https://arxiv.org/html/2608.08003">The spectral neuron</a></li>
<li><a href="https://congma1028.github.io/Publication/Spectral/SpectralMethods_FnTarticle-nowplain.pdf">Spectral Methods</a></li>
<li><a href="https://en.wikipedia.org/wiki/Language_primitive">Language primitive - Wikipedia</a></li>

</ul>
</details>

**Tags**: `#machine learning`, `#interpretability`, `#spectral methods`, `#scalability`, `#arxiv`

---

<a id="item-7"></a>
## [Mini Kimi K3 Replica Trained for Under $250 Beats GPT-2 124M](https://www.reddit.com/r/LocalLLaMA/comments/1vth1c3/i_just_built_a_mini_kimik3_from_scratch_under_250/) ⭐️ 8.0/10

A hobbyist pretrained a 1.02-billion-parameter mixture-of-experts (MoE) model replicating Kimi K3's architecture for under $250, using only 5 billion tokens. The model scores 33.4% on HellaSwag, outperforming GPT-2 124M's 28%. This shows that frontier architectural innovations like those in Kimi K3 can be validated at tiny scale with a very small budget, making serious pretraining experiments accessible to individuals. It also underscores how far efficient MoE design has come, enabling 1B-class models to punch above their weight. The 1.02B model activates only 145M parameters per token and includes K3's Kimi Delta Attention, Gated MLA, Attention Residuals, and LatentMoE with an aux-loss-free balancer. It also uses K3's unmodified 163,840-token tokenizer and has never been instruction-tuned; a full tutorial is available.

reddit · r/LocalLLaMA · /u/OtherRaisin3426 · Aug 20, 11:38

**Background**: Kimi K3 is a 2.8-trillion-parameter open MoE model built on Kimi Delta Attention and Attention Residuals, with a 1M-token context window. LatentMoE is a hardware-aware MoE variant that routes computation in a lower-dimensional latent space to improve efficiency. MLA (Multi-head Latent Attention), first introduced in DeepSeek-V2, reduces attention memory footprint and is combined with gating in this replica.

<details><summary>References</summary>
<ul>
<li><a href="https://www.kriraai.com/blog/kimi-k3-architecture-explained">Kimi K3 Architecture Explained: Specs, Benchmarks, Costs</a></li>
<li><a href="https://www.kimi.ai/ai-models/kimi-k3">Kimi K3: 2.8T Open Model for Coding & Knowledge Work</a></li>
<li><a href="https://arxiv.org/abs/2601.18089">[2601.18089] LatentMoE: Toward Optimal Accuracy per FLOP and Parameter in Mixture of Experts</a></li>

</ul>
</details>

**Tags**: `#pretraining`, `#MoE`, `#Kimi-K3`, `#LLM`, `#tutorial`

---

<a id="item-8"></a>
## [OpenAI Previews Private Security Processing, Zero-Data Retention for Frontier Models](https://openai.com/index/offering-zero-data-retention-for-frontier-models/) ⭐️ 8.0/10

OpenAI previewed a private security processing mechanism and reaffirmed its zero-data-retention (ZDR) commitment for frontiermodel API customers, ensuring prompts and replies are not stored after processing. The feature is being tested with early customers and is planned to roll out gradually starting in September, alongside a technical whitepaper. This development matters because it directly addresses core trust concerns for enterprise and regulated-industry API customers about data privacy and content visibility. It also signals a push toward stronger privacy guarantees in AI APIs, potentially raising the baseline for competitors. Customer content is encrypted with customer-controlled keys, so even flagged requests cannot be read by OpenAI personnel. The private security processing mechanism identifies potential abuse across related interactions by returning only limited security signals, without exposing raw prompts or replies.

telegram · zaihuapd · Aug 20, 02:33

**Background**: Zero data retention (ZDR) is an operational mode in which an AI API provider does not store, log, or use customer prompts, replies, or associated metadata for purposes such as training or abuse monitoring. Private security processing builds on confidential computing, which uses hardware-based trusted execution environments to protect data while it is in use, and on techniques such as homomorphic encryption, which allow computations to be performed on encrypted data. These approaches close the security gap left by encrypting data only at rest and in transit, enabling abuse detection without exposing raw content.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Confidential_computing">Confidential computing</a></li>
<li><a href="https://en.wikipedia.org/wiki/Homomorphic_encryption">Homomorphic encryption</a></li>
<li><a href="https://decagon.ai/glossary/what-is-zero-data-retention-ai">What is Zero Data Retention AI? Definition & Vendor Guide | Decagon</a></li>

</ul>
</details>

**Tags**: `#OpenAI`, `#Privacy`, `#Security`, `#API`, `#Data Retention`

---

<a id="item-9"></a>
## [Stripe Reportedly to Acquire OpenRouter for Over $7 Billion](https://t.me/zaihuapd/43290) ⭐️ 8.0/10

Stripe has reportedly reached an agreement to acquire OpenRouter, a unified AI model access platform, for more than $7 billion, though the final price could still change. Stripe declined to comment, and OpenRouter has not responded publicly. This deal underscores the growing strategic importance of AI model aggregation and distribution infrastructure. If completed, it would give a fintech giant like Stripe a direct foothold in the AI developer ecosystem, potentially reshaping how developers access, route, and pay for AI models. OpenRouter was founded in 2023 and provides access to more than 400 AI models from multiple providers through a single API. The company said in May that it had served 8 million developers. The reported $7 billion-plus price is not final and could change before closing.

telegram · zaihuapd · Aug 20, 07:00

**Background**: OpenRouter is a unified API platform that lets developers access hundreds of AI models from providers such as OpenAI, Anthropic, Google, and Meta through a single endpoint and API key. Acquiring OpenRouter would allow Stripe to integrate payments with AI model usage and expand its reach into the fast-growing AI infrastructure layer.

<details><summary>References</summary>
<ul>
<li><a href="https://openrouter.ai/">OpenRouter</a></li>
<li><a href="https://www.datacamp.com/tutorial/openrouter">OpenRouter : A Guide With Practical Examples | DataCamp</a></li>
<li><a href="https://www.codecademy.com/article/what-is-openrouter">What is OpenRouter? A Guide with Practical Examples</a></li>

</ul>
</details>

**Tags**: `#acquisition`, `#Stripe`, `#OpenRouter`, `#AI infrastructure`, `#fintech`

---

<a id="item-10"></a>
## [Terence Tao warns AI could trigger math's biggest crisis since Gödel](https://the-decoder.com/terence-tao-says-ai-could-trigger-maths-biggest-crisis-since-godel/) ⭐️ 8.0/10

In an article prepared for the 2026 International Congress of Mathematicians, Terence Tao argues that mathematicians should stop debating what AI can do and instead confront the neglected question of research goals. He cites the First Proof project's second round, where four AI systems were tested on 10 unpublished lemmas and at least one system deemed seven of them acceptable, at a cost of tens to hundreds of dollars per problem. A leading mathematician's warning signals that AI-generated proofs could shift mathematics from proof scarcity to proof surplus, potentially making the discipline incomprehensible to humans. This affects the standards of proof, peer review, and the broader ecosystem of AI evaluation in research mathematics, as exemplified by projects like First Proof. First Proof is an independent evaluation initiative that tests AI systems on difficult research mathematics problems, and its second batch gave four AI systems 10 unpublished lemmas from working researchers. Tao adds that a proof no one can clearly explain should be considered incomplete even if it passes formal verification, because formal verification alone does not guarantee human intelligibility.

telegram · zaihuapd · Aug 20, 13:19

**Background**: First Proof is an independent project launched in February 2026 by organizers including Harvard professor Lauren Williams, created in response to claims of rapid AI progress in mathematics. In such evaluations, a 'lemma' is a theorem proved on the way to a larger proof, and formal verification is a step-by-step logical check of a proof that does not assess whether the proof can be understood or explained by humans. Tao's comparison to Gödel and Russell refers to the foundational crisis of the early 20th century, when paradoxes and incompleteness theorems forced mathematicians to re-examine the assumptions underlying their field.

<details><summary>References</summary>
<ul>
<li><a href="https://1stproof.org/">First Proof Project</a></li>
<li><a href="https://current.fas.harvard.edu/stories/first-proofs-second-batch-math-problems-test-ai">First Proof’s second batch of math problems test AI</a></li>
<li><a href="https://www.scientificamerican.com/article/mathematicians-launch-first-proof-a-first-of-its-kind-math-exam-for-ai/">Mathematicians launch First Proof, a first-of-its-kind math ...</a></li>

</ul>
</details>

**Tags**: `#AI`, `#mathematics`, `#proof verification`, `#Terence Tao`, `#research ethics`

---

<a id="item-11"></a>
## [Reverse-Lookup Service Breach Exposes Millions of Face Photos](https://arstechnica.com/gadgets/2026/08/reverse-lookup-service-exposed-millions-of-photos-of-peoples-faces/) ⭐️ 8.0/10

A reverse image search service suffered a data breach that exposed roughly 450 GB of data, including over nine million photos of people's faces and associated personal information such as email addresses, phone numbers, and IP addresses. The service has restricted access to the database, but the full scope and remediation efforts remain unclear. Because faces are immutable biometric identifiers, this breach raises serious privacy and identity-security concerns. The leaked data could be used for unauthorized identification, personal tracking, or fraud, affecting millions of individuals and underscoring the risks of large-scale biometric data collection. The exposed database is approximately 450 GB in size and contains more than nine million images. Along with facial photos, the data includes email addresses, phone numbers, and IP addresses, amplifying the potential for connecting biometric data to specific individuals.

telegram · zaihuapd · Aug 20, 15:14

**Background**: Reverse image search, also known as content-based image retrieval, allows users to upload an image and find matching or similar images and their sources online. Biometric information such as faces is unique and difficult to change, so once leaked, it cannot be simply replaced like a password, making such breaches particularly damaging.

<details><summary>References</summary>
<ul>
<li><a href="https://zh.wikipedia.org/zh-hans/反向图像搜索">反向图像搜索 - 维基百科，自由的百科全书</a></li>
<li><a href="https://www.cebnet.com.cn/20210304/102733568.html">cebnet.com.cn/20210304/102733568.html</a></li>

</ul>
</details>

**Tags**: `#数据泄露`, `#隐私`, `#生物识别`, `#安全`, `#人脸识别`

---