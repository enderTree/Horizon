---
layout: default
title: "Horizon Summary: 2026-11-16 (EN)"
date: 2026-11-16
lang: en
---

> From 38 items, 3 important content pieces were selected

---

1. [Universal XSS in uBlock Origin via website-driven element picker](#item-1) ⭐️ 8.0/10
2. [Qwen4-Max Launches as Alibaba's New Flagship Multimodal Model](#item-2) ⭐️ 8.0/10
3. [Meta FAIR and NYU: Vision Encoder Pretraining Optional, Vision-Only Weights Required](#item-3) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Universal XSS in uBlock Origin via website-driven element picker](https://iter.ca/post/ubo-uxss/) ⭐️ 8.0/10

A security researcher disclosed a universal XSS (UXSS) vulnerability in uBlock Origin that arises when a malicious website manipulates the extension's interactive element picker. The flaw has been patched, with community members noting that users should upgrade to uBlock Origin 1.75.4 or uBO Lite 2026.1110.1816 and above. uBlock Origin is one of the most widely deployed browser extensions, so a UXSS bug in it can let a malicious page run script with the extension's elevated privileges on any site, crossing the same-origin boundary that normally protects users. Because the exploit is driven by ordinary web content rather than a special attacker setup, the blast radius covers a very large installed base across Firefox and Chromium. The root cause is architectural: the element picker's user interface is injected into the page's own DOM so it can highlight and select page elements, which means hostile page script shares the same DOM context as the picker UI. Mitigations include upgrading to the fixed builds and, for hardened Firefox users, rebuilding profiles so no stale vulnerable extension state persists.

hackernews · zaik · Nov 16, 02:04 · [Discussion](https://news.ycombinator.com/item?id=50513160)

**Background**: Universal XSS (UXSS) differs from ordinary XSS: instead of exploiting a single website's flawed input handling, it exploits the browser or an extension so script can run on any site, effectively defeating the same-origin policy. uBlock Origin's element picker is a feature that lets a user click a page element to generate a cosmetic or network filter that permanently hides it; to do this interactively it overlays its own UI on the page being viewed. Extensions like uBO run with far more privileges than page scripts, so any path where a page can influence that injected UI is a serious trust boundary violation.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Universal_XSS">Universal XSS</a></li>
<li><a href="https://aszx87410.github.io/beyond-xss/en/ch2/universal-xss/">The Most Powerful XSS : Universal XSS | Beyond XSS</a></li>
<li><a href="https://github.com/gorhill/uBlock/wiki/Element-picker">Element picker · gorhill/uBlock Wiki · GitHub</a></li>

</ul>
</details>

**Discussion**: Commenters focused on the architectural root cause, asking why the picker UI cannot simply live in browser chrome instead of the page DOM. Others noted the same pattern affects password manager autofill dropdowns, which can leak a user's account list to a page that watches for new DOM nodes, and several readers shared concrete remediation advice such as verifying version numbers and creating fresh Firefox profiles.

**Tags**: `#security`, `#xss`, `#browser-extensions`, `#uBlock-Origin`, `#web-security`

---

<a id="item-2"></a>
## [Qwen4-Max Launches as Alibaba's New Flagship Multimodal Model](https://qwen.ai/blog?id=qwen4-max) ⭐️ 8.0/10

Alibaba released Qwen4-Max, the flagship model of its Qwen 4 series, which accepts text, image and video input, returns text, and ships with a roughly 1M-token context window and reasoning enabled by default. The model exposes four selectable reasoning-effort levels — none, low, high and xhigh — and the release was discussed extensively on Hacker News. Qwen is one of the most widely used model families, so a new flagship release directly affects developers building coding assistants, frontend-design tools and agentic workflows on top of it. The discussion highlights a tougher competitive question: not just raw benchmark scores, but cost-per-task and serving speed versus closed frontier models from OpenAI and Anthropic. Artificial Analysis measures Qwen4-Max's intelligence score at 43 with an average cost of about $3.27, while a commenter cites GPT-6.1 Sol at medium effort scoring 46 for roughly $0.36 — a large efficiency gap. Community members also flag serving throughput (one reports Qwen 3.8 running near 30 tokens/sec versus roughly 80 for Opus), and note that OpenRouter lists variants such as qwen3.8-max-prime and qwen3.8-max-0902 with different pricing and speed tradeoffs.

hackernews · ilreb · Nov 16, 02:14 · [Discussion](https://news.ycombinator.com/item?id=50513215)

**Background**: Qwen is Alibaba's family of large language models, released in successive generations (Qwen 3, 3.8, and now Qwen 4) with a flagship "Max" tier plus smaller and faster "Flash" variants. "Reasoning effort" is a control that lets callers trade extra inference cost and latency for more deliberation before answering, a pattern popularized by reasoning models trained with reinforcement learning on verifiable rewards. Artificial Analysis is an independent benchmarking service that pairs quality scores with price data, which is why commenters use it to compare models on cost-effectiveness rather than raw capability alone.

<details><summary>References</summary>
<ul>
<li><a href="https://artificialanalysis.ai/models/qwen4-max">Qwen 4 Max - Intelligence, Performance & Price... | Artificial Analysis</a></li>
<li><a href="https://openrouter.ai/qwen/qwen4-max">Qwen 4 Max - API Pricing & Providers | OpenRouter</a></li>
<li><a href="https://www.qwencloud.com/models/qwen4-max?region=ap-southeast-1">Qwen 4 - Max - QwenCloud</a></li>

</ul>
</details>

**Discussion**: Hacker News commenters were split between enthusiasm and skepticism: some welcomed the continued emphasis on efficiency and looked forward to the Flash and 27B versions, while others questioned whether inference speed is now a binding constraint — one developer said Qwen's low scores in their agent arena stem mainly from being "slooooow." A recurring concern was whether the open-weights ecosystem is falling further behind Anthropic and OpenAI with each release.

**Tags**: `#Qwen`, `#LLM`, `#AI models`, `#benchmarking`, `#inference cost`

---

<a id="item-3"></a>
## [Meta FAIR and NYU: Vision Encoder Pretraining Optional, Vision-Only Weights Required](https://www.reddit.com/r/MachineLearning/comments/1xx1k2o/meta_fair_nyu_unbundling_multimodal_vision/) ⭐️ 8.0/10

Meta FAIR and NYU trained more than 200 multimodal LLMs entirely from scratch on identical data with encoder pretraining charged against the same lifetime compute budget, in order to test three usually conflated design choices separately. They report that separate vision encoder pretraining is optional (four pretrained encoders at best tie a from-scratch encoder at matched compute), that vision-only parameters are required (encoder-free models trail at every size from 0.6B to 6.4B and need roughly 3x compute to catch up), and that placing vision capacity before the LLM is optional thanks to an "in-fusion" variant that matches the encoder from 1.7B to 6.4B. Frontier labs currently disagree sharply on vision encoders — Gemma 4 12B dropped the encoder, Kimi K3 trains its encoder from scratch, and Inkling 2 Small brought one back — but published models differ in data and compute, so comparisons cannot isolate any single choice. This controlled ablation gives model builders evidence that the expensive encoder pretraining stage and the separate encoder module can potentially be dropped without losing VQA quality, which could simplify MLLM recipes and reduce training cost. The main comparisons use Qwen3-1.7B and 4B backbones with 0.4B parameters of vision capacity across a scaling ladder from 0.6B to 6.4B, evaluated on 16 Cambrian VQA benchmarks at 448 px and 12 language benchmarks. Notably, pretraining MetaCLIP 6.5x longer raised ImageNet linear-probe accuracy from 80.4% to 84.4% without improving VQA, and at 1.7B the in-fusion vision-only branches in layers 1–8 reached 45.0 VQA versus 44.4 for an encoder, 42.3 when text shares those parameters, and 35.1 when placed in the last 8 layers, while cutting time to first token by about 13%.

reddit · r/MachineLearning · /u/trungh98 · Nov 15, 17:38

**Background**: A typical multimodal LLM stacks three parts: a vision encoder (usually a ViT pretrained with a contrastive objective such as CLIP or MetaCLIP) that turns an image into patch embeddings, a connector that projects those embeddings into the language model's space, and the LLM backbone itself. This design bundles three separate decisions — whether the encoder gets its own upstream pretraining, whether vision tokens get dedicated parameters, and whether that capacity sits before the LLM — and prior work rarely separated them. VQA (visual question answering) benchmarks measure whether a model can answer questions about an image, while linear-probe accuracy on ImageNet measures how linearly separable a frozen encoder's features are; time to first token (TTFT) is an inference-latency metric.

<details><summary>References</summary>
<ul>
<li><a href="https://huggingface.co/papers/date/2026-11-13">Daily Papers - Hugging Face</a></li>
<li><a href="https://github.com/gokayfem/awesome-vlm-architectures">GitHub - gokayfem/awesome-vlm- architectures : Curated visual...</a></li>
<li><a href="https://www.emergentmind.com/topics/mllm">MLLM : Architecture , Adaptation, & Applications</a></li>

</ul>
</details>

**Tags**: `#multimodal-learning`, `#vision-encoders`, `#MLLM`, `#pretraining`, `#scaling-laws`

---