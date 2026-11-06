---
layout: default
title: "Horizon Summary: 2026-11-06 (EN)"
date: 2026-11-06
lang: en
---

> From 42 items, 7 important content pieces were selected

---

1. [OpenSSH password auth bypass on Alpine traced to musl crypt() sentinel hashes](#item-1) ⭐️ 9.0/10
2. [SemiAnalysis: Google TPU Becomes a Viable Inference Alternative to NVIDIA's CUDA](#item-2) ⭐️ 8.0/10
3. [Hugging Face Releases a Practical Handbook for Training MoE Models with Megatron-LM](#item-3) ⭐️ 8.0/10
4. [US Approves NVIDIA H200 Sales to About 10 Chinese Firms](#item-4) ⭐️ 8.0/10
5. [Google opens Nano Banana 2 Lite and Gemini Omni Flash to developers](#item-5) ⭐️ 8.0/10
6. [OpenAI begins testing ads in ChatGPT for free and Go users](#item-6) ⭐️ 8.0/10
7. [Baidu releases ERNIE 5.0, a 2.4-trillion-parameter omni-modal model](#item-7) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [OpenSSH password auth bypass on Alpine traced to musl crypt() sentinel hashes](https://sshhole.com/) ⭐️ 9.0/10

A password-authentication bypass in OpenSSH, tracked as CVE-2026-123158 and nicknamed "sshole," allows logins without knowing the password when sshd runs against musl libc (as on Alpine Linux). musl's crypt() returns the sentinel string "*" when it fails — for example on an oversized password — and sshd compares that return value against the account's stored password field in /etc/shadow, which for locked or password-less accounts is itself "*" or "!", so the comparison spuriously succeeds. OpenSSH is one of the most widely deployed pieces of security infrastructure in existence, so an authentication bypass in sshd is a paradigm-level event that potentially exposes any musl-based host — including large swaths of container images, embedded devices, and Alpine-based cloud deployments — to unauthenticated remote access. The incident also casts a harsh light on the practice of overloading magic strings like "*" to mean "no password" and "hashing failed" simultaneously. glibc systems are largely shielded because they use libxcrypt, which returns "*0" on failure so the comparison fails and the login is refused; the vulnerable path is specific to musl. The Alpine advisory notes that affected configurations are those where no account carries a $-style password hash (for instance cloud-init images that commonly set PasswordAuthentication no), and the fix is to update openssh to 10.6p2 and restart sshd, with setting PasswordAuthentication no as a stopgap.

hackernews · josemrb · Nov 5, 12:19 · [Discussion](https://news.ycombinator.com/item?id=50378228)

**Background**: On Unix systems, /etc/shadow stores each account's password as a hash string whose prefix encodes the algorithm (for example $6$ for SHA-512), and sshd verifies a login by calling crypt() with the supplied password and the stored hash as parameters and checking that the result equals the stored value. Accounts that should never be able to log in with a password typically have "*" or "!" in that field instead of a hash. musl libc, the C standard library used by Alpine Linux, deliberately returns an unmatchable hash string rather than NULL when crypt() fails, a design choice that turns a hashing error into a value that can accidentally match a locked account's field.

<details><summary>References</summary>
<ul>
<li><a href="https://www.ox.security/blog/openssh-authentication-bypass-cve-2026-123158/">OpenSSH Bypass : CVE-2026-123158 | OX Security</a></li>
<li><a href="https://alpinelinux.org/posts/2026-11-05-openssh-password-authentication-bypass/">Security advisory: openssh -server password authentication bypass</a></li>
<li><a href="https://git.musl-libc.org/cgit/musl/commit/?id=b3c4cc121f70faea45389fe7ddc1127ed5cbd8bb">musl - musl - an implementation of the standard library for...</a></li>

</ul>
</details>

**Discussion**: The Hacker News thread (roughly 2,500 points and 600+ comments) largely root-caused the bug rather than panicking: one commenter walked through the crypt()/hash comparison to explain why a locked account authenticates, others condemned the use of in-band signaling with "*" as a sentinel value, and one noted that musl had already patched this failure mode in crypt_des but forgot the crypt_sha path (and that the existing workaround itself breaks if the salt is "x"). A further sentiment was disappointment that musl made convenient changes to core crypto code without the auditing that would have caught the flaw.

**Tags**: `#security`, `#openssh`, `#vulnerability`, `#authentication`, `#cryptography`

---

<a id="item-2"></a>
## [SemiAnalysis: Google TPU Becomes a Viable Inference Alternative to NVIDIA's CUDA](https://newsletter.semianalysis.com/p/tpu-strikes-the-king) ⭐️ 8.0/10

SemiAnalysis published a deep-dive analysis arguing that Google's TPU has matured into a viable alternative to NVIDIA's CUDA moat specifically for AI inference workloads, and that NVIDIA is now responding aggressively to the threat. The piece surveys the surrounding software ecosystem — including TorchTPU, vLLM, SGLang, llm-d and Ray — alongside a wave of new models such as Kimi K3, Qwen and GLM5.3. For years CUDA's software lock-in has kept NVIDIA's margins and market share largely unchallenged, so any credible inference alternative on TPUs directly threatens that position and gives large-scale AI deployments a second sourcing option. Because inference (rather than training) is where the bulk of long-run compute spending is expected to sit, even partial TPU adoption could shift pricing power and hardware choices across the AI infrastructure stack. The analysis frames the battle as a software-stack contest rather than a pure chip comparison: TPUs were historically programmed through XLA/JAX, so new bridges such as the Google–Meta open-source TorchTPU PyTorch backend and support for serving engines like vLLM, SGLang and Kubernetes-native llm-d are what make TPUs practical for mainstream inference. Notably, the publicly available version of the article is a teaser, so the specific benchmark numbers and the claimed details of NVIDIA's counter-moves are only visible to paying subscribers.

rss · Semianalysis · Nov 5, 19:03

**Background**: TPU (Tensor Processing Unit) is Google's custom AI accelerator, designed in-house and offered through Google Cloud, in contrast to NVIDIA's general-purpose GPUs. NVIDIA's real advantage has been CUDA, the proprietary programming model and library ecosystem that most AI software is written against, which makes switching hardware costly. vLLM and SGLang are open-source LLM serving engines that maximize throughput via techniques such as paged attention and prefix caching, while llm-d turns them into distributed, Kubernetes-native serving stacks; TorchTPU, announced at PyTorch Conference 2026, adds a native PyTorch backend so models can run on TPUs without a rewrite.

<details><summary>References</summary>
<ul>
<li><a href="https://pytorch.org/blog/introducing-torchtpu/">Introducing TorchTPU - PyTorch</a></li>
<li><a href="https://cloud.google.com/blog/topics/ai-infrastructure/torchtpu-is-now-open-source-run-native-pytorch-on-tpus">TorchTPU is now open source: Run native PyTorch on TPUs</a></li>
<li><a href="https://llm-d.ai/">llm-d</a></li>

</ul>
</details>

**Tags**: `#Google TPU`, `#NVIDIA CUDA`, `#AI inference`, `#AI infrastructure`, `#LLM serving`

---

<a id="item-3"></a>
## [Hugging Face Releases a Practical Handbook for Training MoE Models with Megatron-LM](https://www.reddit.com/r/MachineLearning/comments/1xorgq0/the_ultimate_moe_training_handbook_training/) ⭐️ 8.0/10

Hugging Face engineer Nouamane, previously involved in the Ultra-Scale and Smol Training Playbooks, published a detailed handbook on training Mixture-of-Experts (MoE) models with NVIDIA's Megatron-LM. The handbook includes a Megatron-LM runbook (hardware testing, image building, dense baseline, and a first single-node MoE), a deep dive into MoE layer internals (router, routing, load balancing, experts, block layout), and follow-through to serving and RL, alongside 55 figures and ready-to-use scripts. Most public training guides assume dense transformer models, so practitioners moving to MoE—now the dominant architecture for frontier open models—have had little code-level guidance on routing, load balancing, and expert parallelism. A grounded, end-to-end playbook lowers the barrier for teams with modest GPU budgets to adopt MoE training and helps them avoid expensive misconfigurations. The recommendations are derived from roughly 800k GH200 GPU-hours of MoE training on the Alps cluster at CSCS, and the author explicitly labels which results come from his own runs, which come from cited papers/configs/code of frontier models, and which are toy simulations. Chapters 3 and 4 require no GPU to follow, and every recommended Megatron-LM flag is consolidated into a single configuration block.

reddit · r/MachineLearning · /u/Norlax_42 · Nov 5, 19:13

**Background**: Mixture-of-Experts is an architecture in which each transformer block contains many separate "expert" feed-forward networks, and a learned router sends each token to only a few of them, so total parameter count grows while per-token compute stays roughly constant. Megatron-LM is NVIDIA's open-source PyTorch library for training very large transformer models, providing tensor, pipeline, and expert parallelism. GH200 is NVIDIA's Grace Hopper Superchip, which pairs a Hopper GPU with a Grace CPU and a large unified memory pool, and is widely used for large-scale training clusters.

<details><summary>References</summary>
<ul>
<li><a href="https://huggingface.co/blog/moe">Mixture of Experts Explained</a></li>
<li><a href="https://grokipedia.com/page/Megatron-LM">Megatron-LM</a></li>
<li><a href="https://www.nvidia.com/en-us/data-center/grace-hopper-superchip/">NVIDIA Grace Hopper Superchip | NVIDIA</a></li>

</ul>
</details>

**Tags**: `#MoE`, `#Megatron-LM`, `#LLM training`, `#Hugging Face`, `#systems`

---

<a id="item-4"></a>
## [US Approves NVIDIA H200 Sales to About 10 Chinese Firms](https://t.me/zaihuapd/44945) ⭐️ 8.0/10

Reuters reports that the US Commerce Department has granted export licenses allowing roughly 10 Chinese companies — including Alibaba, Tencent, ByteDance and JD — to buy NVIDIA's H200 chips, with distributors such as Lenovo and Foxconn also licensed and a cap of up to 75,000 units per customer. No deliveries have taken place yet, and Jensen Huang's visit to China is seen as an effort to push the deals through as some Chinese buyers grow cautious under Beijing's guidance. This is one of the largest openings in US export controls on advanced AI chips to China in recent years, potentially restoring a multi-billion-dollar revenue stream for NVIDIA and easing compute shortages for China's biggest AI labs. At the same time, Beijing's cautious stance shows the decision is now shaped by China's own push to substitute domestic AI accelerators, making the H200 as much a geopolitical bargaining chip as a product. The licenses cap each customer at roughly 75,000 H200 units and extend to distributors like Lenovo and Foxconn, but approvals are not deliveries — no shipments have been completed and Chinese firms reportedly remain hesitant pending clearer government signals. The H200 is NVIDIA's Hopper-generation data-center GPU with substantially more high-bandwidth memory than the H100, which is what makes it attractive for large-model training and inference.

telegram · zaihuapd · Nov 5, 14:42

**Background**: Since 2022 the US has progressively tightened export controls on advanced semiconductors to China, and NVIDIA responded by creating China-specific downgraded parts such as the H20, which was itself later blocked. The H200 sits a tier below the newest Blackwell-generation parts but is far more capable than anything previously allowed for Chinese buyers, so its approval marks a notable policy shift. China, meanwhile, has been pushing domestic alternatives from Huawei and others while still depending on NVIDIA hardware for frontier AI work.

<details><summary>References</summary>
<ul>
<li><a href="https://www.nvidia.com/en-us/data-center/h200/">H 200 GPU | NVIDIA</a></li>
<li><a href="https://www.aquanode.io/gpu/nvidia-h200">NVIDIA H 200 GPU : Specs , VRAM, Price & Benchmarks (2026)</a></li>
<li><a href="https://www.worldjournal.com/wj/story/121477/8685685">不只 H 20 晶片被禁 傳 Nvidia 中 國 特 供 版 旗艦顯卡也暫停 供 應 | 世界新聞網</a></li>

</ul>
</details>

**Tags**: `#AI chips`, `#export controls`, `#NVIDIA H200`, `#US-China tech policy`, `#semiconductor industry`

---

<a id="item-5"></a>
## [Google opens Nano Banana 2 Lite and Gemini Omni Flash to developers](https://t.me/zaihuapd/44952) ⭐️ 8.0/10

Google released two generative media models: Nano Banana 2 Lite, which generates 1K images from text with roughly 4-second latency at $0.034 per image, and Gemini Omni Flash, a fast model for video generation that the announcement describes as producing 10-second clips. Both are available through Google AI Studio, the Gemini API, and the Gemini Enterprise Agent Platform, with Nano Banana 2 Lite also heading to consumer surfaces like Search AI Mode and the Gemini app. The pricing and latency figures push high-volume image generation into commodity territory, making it practical for developers to run thousands of generations per workflow rather than a handful of premium calls. Broad availability across the developer API and consumer products simultaneously means the same model family now spans prototyping, production pipelines, and end-user features. Nano Banana 2 Lite is built on Google DeepMind's Gemini 3.1 Flash-Lite Image, described as the fastest and cheapest model in the Gemini 3.1 image family and optimized for both image understanding and generation. Gemini Omni Flash is positioned as a step toward models that can create and edit anything from any input — starting with video — and is documented as producing 720p clips with synchronized native audio from a text prompt or a still image.

telegram · zaihuapd · Nov 6, 00:21

**Background**: Nano Banana is the nickname Google's image models picked up from their early codename and has stuck as a product line name, with the "Lite" variant trading peak quality for speed and cost. Gemini Omni Flash belongs to a newer class of "omni" models intended to handle multiple media types in one model rather than separate image and video systems. Flash-Lite naming follows Google's existing Flash tier convention, which denotes lower-latency, lower-cost versions of its flagship Gemini models.

<details><summary>References</summary>
<ul>
<li><a href="https://deepmind.google/models/gemini-image/flash-lite/">Gemini 3.1 Flash-Lite Image – Nano Banana 2 Lite — Google ...</a></li>
<li><a href="https://ai.google.dev/gemini-api/docs/models/gemini-omni-flash">Learn about the Gemini Omni Flash video generation and editing model</a></li>
<li><a href="https://deepmind.google/models/model-cards/gemini-omni-flash/">Gemini Omni Flash - Model Card — Google DeepMind</a></li>

</ul>
</details>

**Tags**: `#Google`, `#generative-ai`, `#image-generation`, `#video-generation`, `#Gemini API`

---

<a id="item-6"></a>
## [OpenAI begins testing ads in ChatGPT for free and Go users](https://t.me/zaihuapd/44955) ⭐️ 8.0/10

On February 9, OpenAI began testing clearly labeled ads in ChatGPT, placing them in a separate area below the chat box for free and Go subscribers. CEO Sam Altman said OpenAI expects advertising to eventually account for under 50% of long-term revenue. This marks a major monetization shift for the world's most widely used AI assistant, moving beyond subscriptions toward an ad-supported model that could reshape how AI products are priced and how they fund expensive model training and inference. It also puts OpenAI on a collision course with Google's ad-based search business while raising user-experience and trust questions for hundreds of millions of free-tier users. OpenAI says the ads will be optimized based on user needs, will not access private conversations, and advertisers cannot influence ChatGPT's answers. The company also disclosed that ChatGPT's monthly growth rate has climbed back above 10% and plans to release an updated chat model this week.

telegram · zaihuapd · Nov 6, 03:15

**Background**: ChatGPT Go is a low-cost subscription tier that OpenAI first launched in India in August 2025 and later expanded worldwide, designed to bring more users onto paid features at a price closer to free. Until now OpenAI's consumer business has relied mainly on Plus, Pro and Business subscriptions; ads would add a second revenue stream similar to how Google funds free search. Large language models are costly to train and serve, so monetizing the free tier has become a central challenge for AI companies.

<details><summary>References</summary>
<ul>
<li><a href="https://openai.com/index/introducing-chatgpt-go/">Introducing ChatGPT Go, now available worldwide - OpenAI</a></li>
<li><a href="https://chatgpt.com/pricing/">Plans and Pricing | ChatGPT</a></li>

</ul>
</details>

**Tags**: `#OpenAI`, `#ChatGPT`, `#advertising`, `#AI business model`, `#monetization`

---

<a id="item-7"></a>
## [Baidu releases ERNIE 5.0, a 2.4-trillion-parameter omni-modal model](https://t.me/zaihuapd/44959) ⭐️ 8.0/10

Baidu officially released ERNIE 5.0, an omni-modal large model with 2.4 trillion total parameters that uses unified modeling to handle text, images, audio and video. Baidu claims the model surpasses international frontier models such as Gemini-2.5-Pro and GPT-5-High on more than 40 authoritative benchmarks, and says 835 experts from technology, finance, culture and education took part in guiding and calibrating it. At 2.4 trillion parameters this is one of the largest models announced to date, and Baidu is positioning it as a direct challenger to top US frontier systems on benchmark performance. If the claims hold up, it strengthens the case that Chinese labs are closing the gap on multimodal capability, which matters for enterprises and developers choosing a model stack. ERNIE 5.0 uses a Mixture-of-Experts architecture in which fewer than 3% of parameters are activated per inference, which Baidu says preserves capability while improving inference efficiency. The benchmark claims are stated without published per-task numbers or independent verification, and the announcement only notes that individual users can currently access the model through the ERNIE platform.

telegram · zaihuapd · Nov 6, 05:41

**Background**: Mixture-of-Experts (MoE) is an architecture in which a model contains many specialized sub-networks called experts plus a learned routing network that sends each input token to only a small subset of them, so only a fraction of total parameters activate during each inference step. This lets labs scale total parameter counts far beyond what a dense model could afford at the same compute budget, which is why frontier models increasingly report huge totals alongside much smaller activated-parameter figures. "Omni-modal" refers to a single model handling text, image, audio and video natively rather than stitching together separate specialized models, a direction also pursued by research systems such as Ola.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Mixture_of_experts">Mixture of experts - Wikipedia</a></li>
<li><a href="https://arxiv.org/abs/2507.11181">[2507.11181] Mixture of Experts in Large Language Models Mixture of Experts in Large Language Models - arXiv.org Mixture of experts - Wikipedia Mixture of Experts Explained - Hugging Face Applying Mixture of Experts in LLM Architectures | NVIDIA ... A Survey on Mixture of Experts in Large Language Models A Closer Look into Mixture-of-Experts in Large Language Models</a></li>
<li><a href="https://arxiv.org/abs/2502.04328">Ola: Pushing the Frontiers of Omni-Modal Language Model</a></li>

</ul>
</details>

**Tags**: `#Baidu`, `#ERNIE 5.0`, `#large language models`, `#multimodal AI`, `#Mixture-of-Experts`

---