---
layout: default
title: "Horizon Summary: 2026-11-17 (EN)"
date: 2026-11-17
lang: en
---

> From 43 items, 4 important content pieces were selected

---

1. [Burnt Sushi Releases Jiff 1.0, an Opinionated Datetime Library for Rust](#item-1) ⭐️ 9.0/10
2. [vLLM v0.34.0: Extensible KV Cache by Default, Model Runner V1 Removed](#item-2) ⭐️ 8.0/10
3. [Optimizely supply-chain attack served malware to 178 sites including Zoom and GitLab](#item-3) ⭐️ 8.0/10
4. [Ablation Meta-Analysis of 127k ML Papers Finds 26% of Changes Didn't Help](#item-4) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Burnt Sushi Releases Jiff 1.0, an Opinionated Datetime Library for Rust](https://burntsushi.net/jiff/) ⭐️ 9.0/10

Andrew Gallant (BurntSushi), the author of ripgrep and the regex crate, has published Jiff 1.0, a new datetime library for Rust. The release pairs a deliberately opinionated API design — one that puts time zone handling and daylight saving time correctness front and center — with a detailed written comparison against the existing chrono and time crates. Datetime handling is one of the most error-prone areas in software, and Rust's ecosystem has long leaned on chrono, which is stable but widely considered dated in its API. A mature, well-documented alternative from a maintainer with an exceptional track record gives Rust developers a credible migration path and raises the bar for API design across the ecosystem. Jiff focuses on high-level datetime primitives that are hard to misuse while keeping reasonable performance, and unlike chrono and time it ships with out-of-the-box support for reading the system's copy of the Time Zone Database. The documentation is explicitly opinionated and states plainly that Jiff is not the right tool for every use case; Jiff is pronounced like "gif" with a soft "g".

hackernews · burntsushi · Nov 16, 16:53 · [Discussion](https://news.ycombinator.com/item?id=50519744)

**Background**: A datetime library handles representing instants in time, calendar dates, durations, and conversions between time zones — including daylight saving time, where clocks skip or repeat hours and naive arithmetic silently produces wrong results. chrono has been Rust's default choice for years, with the time crate as the main alternative; both leave time zone database loading to third-party crates such as chrono-tz and time-tz. Jiff's thesis is that time zone handling should be built into the core API rather than bolted on, so that the common mistakes become hard to express.

<details><summary>References</summary>
<ul>
<li><a href="https://burntsushi.net/jiff/">A datetime library for Rust - Andrew Gallant's Blog</a></li>
<li><a href="https://docs.rs/jiff/latest/jiff/">jiff - Rust - Docs.rs</a></li>
<li><a href="https://docs.rs/jiff/latest/jiff/_documentation/comparison/index.html">Comparison with other Rust datetime crates</a></li>

</ul>
</details>

**Discussion**: The discussion is largely enthusiastic: commenters praise Jiff's quality, hope the wider ecosystem adopts it over chrono, and single out the honest scoping ("Jiff isn't always the right thing to use") as exemplary engineering. A former chrono maintainer explained that they took over maintenance hoping to fix the API, but met resistance to any change and eventually burned out, expressing gratitude to BurntSushi for writing the datetime library they had wanted. Others pushed on deeper technical questions, asking how Jiff handles time scales such as TAI and UT1 for very long-range or high-precision simulations.

**Tags**: `#rust`, `#datetime`, `#libraries`, `#open-source`, `#api-design`

---

<a id="item-2"></a>
## [vLLM v0.34.0: Extensible KV Cache by Default, Model Runner V1 Removed](https://github.com/vllm-project/vllm/releases/tag/v0.34.0) ⭐️ 8.0/10

vLLM released v0.34.0, a massive release built from 1,061 commits by 412 contributors that adds 10 new model architectures (including Mistral Large 4, MiniMax-M3.1-Flash and Nemotron-3.5-Transcribe) and turns extensible KV cache sizing on by default. Model Runner V1 is now removed entirely, making Model Runner V2 the only GPU runner, and the release brings speedups of up to 1.95× decode on Blackwell and 1.6× throughput on MI355X-class hardware. vLLM is one of the most widely deployed open-source LLM serving engines, so a default-on KV cache change that enlarges cache capacity (for example MiniMax-M3 on H200 growing from 433k to 672k tokens) directly affects throughput and TTFT for anyone running inference in production. The breaking changes — default block size moving from 16 to 64, dropped ROCm 7.2 artifacts and a hard requirement on huggingface_hub >= 2.0.0 — mean operators must plan an upgrade rather than pull the new image blindly. The new sizing logic measures memory actually free after CUDA graph capture and warmup rather than relying on an estimate, which raises per-token decode latency on some models (TPOT up 6–18% on some H200 models at concurrency 128); users can opt out with --gpu-memory-utilization 0.9 or --no-enable-extensible-kv-cache. Upgraders must also remove VLLM_USE_V2_MODEL_RUNNER=0 (it now fails at startup), port V1 logits processors to vllm.v1.worker.gpu.sample.logits_processor, and note that QuTLASS/fp_quant checkpoints no longer load.

github · khluu · Nov 16, 23:22

**Background**: vLLM is an open-source inference and serving engine for large language models, best known for PagedAttention, which manages the KV cache — the stored key/value tensors that let a model reuse context instead of recomputing it — in fixed-size blocks similar to virtual memory pages. Historically vLLM estimated how much KV cache would fit using a gpu_memory_utilization fraction (default 0.92); the new extensible design reserves address space and commits blocks on demand, keeping fixed offsets so captured CUDA graphs remain valid. The Model Runner is the component that executes the actual forward pass each step, and Model Runner V2 was introduced as a ground-up, more modular rewrite before V1 was retired in this release. The release also targets newer accelerators such as NVIDIA Blackwell (GB200) and AMD's CDNA 4-based MI355X, which offer very large HBM capacity for open-weight model serving.

<details><summary>References</summary>
<ul>
<li><a href="https://docs.vllm.ai/en/latest/api/vllm/v1/worker/extensible_kv_cache/">extensible_kv_cache - vLLM</a></li>
<li><a href="https://vllm.ai/blog/2026-03-24-mrv2">Model Runner V2: A Modular and Faster Core for vLLM</a></li>
<li><a href="https://www.developersdigest.tech/blog/amd-mi355x-vs-nvidia-b200-b300-open-weights-serving-2026">AMD MI 355 X vs NVIDIA B200 vs B300 for... - Developers Digest</a></li>

</ul>
</details>

**Tags**: `#vllm`, `#llm-inference`, `#kv-cache`, `#release-notes`, `#gpu-optimization`

---

<a id="item-3"></a>
## [Optimizely supply-chain attack served malware to 178 sites including Zoom and GitLab](https://blog.report-uri.com/worlds-largest-brands-infected-with-malware-via-optimizely/) ⭐️ 8.0/10

Attackers planted malicious JavaScript inside Optimizely Web, the widely used experimentation and A/B testing platform, and that code was served to visitors of 178 organizations on 16 November, including Zoom, GitLab, CNN, the BBC, Salesforce, IKEA, HSBC and Ledger. Report URI, which documented the incident, stressed that Optimizely's CDN delivered exactly what it was handed — this was not CDN cache poisoning but malicious content pushed through Optimizely's own delivery pipeline. This is a textbook third-party script supply-chain failure: any site that embedded the Optimizely snippet — including some of the highest-traffic properties on the internet — silently became a malware distributor without changing a single line of its own code. It sharpens the long-running argument that marketing-driven tag injection (Optimizely, Google Tag Manager and similar tools) creates a trust path into production that most organizations do not monitor or control. According to Report URI's analysis, the injected code swapped cryptocurrency wallet addresses and skimmed card details typed into some affected sites, and Optimizely's own properties (www.optimizely.com and login.optimizely.com) also carried the payload. It remains unexplained how the attacker obtained write access across so many unrelated customer projects — whether via a compromised Optimizely system, a credential with cross-customer privileges, or something else.

hackernews · kristjansson · Nov 16, 23:00 · [Discussion](https://news.ycombinator.com/item?id=50524767)

**Background**: Optimizely Web is a SaaS experimentation platform whose JavaScript snippet is embedded in customer pages so marketers can run A/B tests and feature flags without shipping code. Because that snippet is loaded at runtime from Optimizely's CDN, it executes with full privileges on the host page — the same trust model behind tag managers such as Google Tag Manager — so a compromise upstream reaches every embedding site at once. Security guidance on third-party JavaScript has long identified server-side compromise of the vendor as the single greatest risk, since the host site has no way to inspect or version-pin what it receives.

<details><summary>References</summary>
<ul>
<li><a href="https://www.bleepingcomputer.com/news/security/optimizely-supply-chain-attack-delivers-malware-to-cnn-fox-news-bbc-salesforce-sites/">Optimizely hack infected CNN, Fox News, BBC, Salesforce sites ...</a></li>
<li><a href="https://shiftdelete.net/en/optimizely-malware">Optimizely Malware Hit 178 Sites: What It Stole and What to Do</a></li>
<li><a href="https://pentest.y-security.de/OWASP+Cheat+Sheet+Series/Third_Party_Javascript_Management_Cheat_Sheet/">Y- Security performs Attack Simulations, Penetration Tests, and...</a></li>

</ul>
</details>

**Discussion**: Commenters largely agreed the root cause is structural: one noted that Google Tag Manager existed precisely to let marketing add tags without engineering involvement, which is how pages ended up shipping megabytes of untrusted JavaScript, and hoped teams are now re-evaluating that. Others demanded accountability — arguing Optimizely lacked release safeguards like staged rollouts and automated security checks, and that huge sites such as CNN and the BBC have no excuse for not applying the same controls or serving first-party code. A few pushed back or asked clarifying questions, noting that compromise of a vendor should not be enough to steal card data unless sites are also doing something careless, and suggesting tools like NoScript to reduce exposure.

**Tags**: `#security`, `#supply-chain`, `#third-party-scripts`, `#web-security`, `#malware`

---

<a id="item-4"></a>
## [Ablation Meta-Analysis of 127k ML Papers Finds 26% of Changes Didn't Help](https://www.reddit.com/r/MachineLearning/comments/1xybvju/we_logged_621k_changes_from_127k_papers_ablations/) ⭐️ 8.0/10

Latentic Labs extracted 621,064 reported ablation changes from the full text of 126,758 machine-learning papers published between 2016 and 2026 across venues including ICML, NeurIPS, ICLR, CVPR, AAAI, ICCV, ECCV, TPAMI, IJCV and JMLR. By the papers’ own reported numbers, 69% of changes helped, 10% had no clear effect, 16% were worse and 5% were mixed, meaning 26% did not help. This is a large-scale empirical audit of what ML papers actually report in ablations, rather than another benchmark of model accuracy, and it finds that 66% of papers include at least one change that did not help by their own numbers. That could push authors and reviewers to treat null and negative ablation results as publishable evidence, and it gives concrete priors about which common tweaks—such as raising sampling temperature or LoRA rank—often fail. The analysis reports venue-level differences: ML venues report a null or negative result for 31% of changes, versus 22% for vision venues, and among common changes, higher sampling temperature was unhelpful in 52% of 122 papers, larger LoRA rank in 46%, and larger learning rate in 46%, while adding a contrastive loss was unhelpful in only 4% of 1,317 cases. Caveats include the automated full-text extraction method and the authors’ disclosure that they built the atlas, though they say they will share the method and accept corrections.

reddit · r/MachineLearning · /u/latenticlabs · Nov 17, 05:11

**Background**: An ablation study in machine learning is an experiment that removes, disables or alters a component of a system—such as a layer, loss term, dataset size or hyperparameter—to measure that component’s effect on performance. LoRA is a parameter-efficient fine-tuning method that adds small low-rank trainable matrices to a frozen model; its rank controls adapter capacity, and a larger rank is not automatically better. Contrastive loss trains embeddings so that similar items are closer and dissimilar items are farther apart, and is often used in representation learning.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Ablation_(artificial_intelligence)">Ablation (artificial intelligence) - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/LoRA_(machine_learning)">LoRA (machine learning) - Wikipedia</a></li>
<li><a href="https://www.geeksforgeeks.org/deep-learning/loss-functions-in-deep-learning/">Loss Functions in Deep Learning - GeeksforGeeks</a></li>

</ul>
</details>

**Tags**: `#machine-learning`, `#ablation-studies`, `#meta-research`, `#empirical-analysis`, `#research-practice`

---