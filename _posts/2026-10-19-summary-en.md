---
layout: default
title: "Horizon Summary: 2026-10-19 (EN)"
date: 2026-10-19
lang: en
---

> From 36 items, 2 important content pieces were selected

---

1. [vLLM v0.32.0 Ships Structured Decision API and Broad Low-Precision KV Cache Support](#item-1) ⭐️ 8.0/10
2. [Cracks Emerge in US AI Infrastructure Boom as $10T Buildout Faces Return Test](#item-2) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [vLLM v0.32.0 Ships Structured Decision API and Broad Low-Precision KV Cache Support](https://github.com/vllm-project/vllm/releases/tag/v0.32.0) ⭐️ 8.0/10

vLLM v0.32.0 landed with 814 commits from 363 contributors (121 of them new), headlined by a new `POST /v1/systemone` endpoint that answers `choice`, `noul` and `score` questions over a structured state, is served by default, and also runs on models such as `Cloudflare/clef-omni`, `LiquidAI/d1-3B` and DiffusionGemma. The release also adds generic `hf` tool-call and reasoning parsers (`--tool-call-parser hf`, `--reasoning-parser hf`) that read a checkpoint's `response_template`, so models shipping that template need no model-specific parser, in both the Python and Rust frontends. Low-precision KV cache support now spans NVFP4 on SM8x/SM12x and SM90, FP8 defaults for GLM-5.x on SM100 and 4-bit `ultraquant_4bit` on ROCm, which directly cuts the GPU memory that limits long-context and high-concurrency serving. Combined with the generic `hf` parsers removing per-model glue code and startup/serving speedups, this release lowers the engineering cost of deploying new models on vLLM across NVIDIA and AMD hardware. There are notable breaking changes to plan for: Python 3.10 is dropped, default CORS origins are restricted, `transformers>=5.16.1,<5.20.0` and `tokenizers>=0.23.2` are now required, cascade attention and `mamba_cache_mode="all"` are removed, and `max_tokens` is no longer reserved from the context window. Benchmarks in the PRs are model- and hardware-specific — for example GLM-5.x FP8 KV cache on SM100 halves KV memory per rank with 2.3-5.5% more throughput but a 7-11% TTFT cost, while `fp8_ds_mla` on SM90 gives GLM-5.3-Flash up to 31% more output throughput.

github · khluu · Oct 18, 06:50

**Background**: vLLM is a widely used open-source inference and serving engine for large language models, best known for PagedAttention-style memory management. Its KV cache stores the key and value vectors of every processed token so that autoregressive decoding does not have to recompute them, which means KV cache size is often what limits context length, batch size and concurrency. Storing that cache in lower precision (FP8, NVFP4, 4-bit) shrinks memory per sequence at some accuracy and latency cost, and hardware support depends on the GPU generation — SM90 refers to NVIDIA Hopper parts like the H100/H200, while SM100 is the Blackwell data-center generation, and XQA is NVIDIA's specialized attention kernel for the decode phase.

<details><summary>References</summary>
<ul>
<li><a href="https://www.lmsys.org/">LMSYS Org</a></li>
<li><a href="https://arnon.dk/matching-sm-architectures-arch-and-gencode-for-various-nvidia-cards/">Matching CUDA arch and CUDA gencode for various NVIDIA ...</a></li>
<li><a href="https://docs.nvidia.com/cuda/pdf/Blackwell_Compatibility_Guide.pdf">Blackwell Compatibility Guide - NVIDIA Documentation Hub</a></li>

</ul>
</details>

**Tags**: `#vLLM`, `#LLM inference`, `#model serving`, `#KV cache`, `#release notes`

---

<a id="item-2"></a>
## [Cracks Emerge in US AI Infrastructure Boom as $10T Buildout Faces Return Test](https://www.ft.com/content/9ea5a37d-15c9-4d5b-94d6-719048c9cd3c?syn-25a6b1a6=1) ⭐️ 8.0/10

US AI infrastructure spending is projected to exceed $10 trillion between 2025 and 2032, but at least 47 large data-center projects have been delayed, withdrawn or cancelled since the start of 2026 as financing costs rise, permitting stalls and public opposition mounts. Analysts estimate only about 35% of planned US data-center projects are highly feasible, and shares of Nvidia-backed cloud provider CoreWeave fell more than 11% on Friday while the Philadelphia Semiconductor Index (SOX) posted its eighth straight decline, matching its longest losing streak since 2006. The pullback signals that the AI capex cycle — which has underpinned chip demand, hyperscaler earnings and much of the US equity rally — may be running ahead of actual demand and financing capacity. If project cancellations continue, it would hit data-center suppliers, power and construction firms, and chipmakers that have priced in years of uninterrupted AI-driven growth. Financing pressure is emerging as the key bottleneck: data centers are capital-intensive, long-lead-time assets that depend on cheap debt, so higher interest rates directly erode project economics. The market is now repricing profitability expectations, with the semiconductor index's eight-session slide echoing the sector's history of sharp multi-month drawdowns after rapid run-ups.

telegram · zaihuapd · Oct 18, 08:52

**Background**: CoreWeave is a GPU-focused cloud provider (IaaS) that rents out Nvidia-accelerated computing capacity to AI developers, and Nvidia's backing has made it a bellwether for AI infrastructure demand. The Philadelphia Semiconductor Index (SOX) tracks the largest US-listed semiconductor companies, including memory makers and AI chip suppliers, making it a widely followed gauge of the sector's health. Because the AI buildout has been financed heavily with debt and long-term capacity contracts, it is unusually sensitive to interest rates and to any sign that AI revenue is not scaling as fast as the infrastructure behind it.

<details><summary>References</summary>
<ul>
<li><a href="https://news.qq.com/rain/a/20251216A076YN00">CoreWeave ： 英 伟 达 “干儿子” 真能子凭父贵？_ 腾讯新闻</a></li>
<li><a href="https://www.laohu8.com/stock/SOX">费 城 半 导 体 指 数 ( SOX )... | 老虎社区</a></li>
<li><a href="https://www.21jingji.com/article/20260714/herald/563e762bc36ac35d8bf5dadc4aca4fe0.html">三问 半 导 体 板块巨震：为何暴跌？ 见顶了吗？ 能买入吗？ - 21经济网</a></li>

</ul>
</details>

**Tags**: `#AI infrastructure`, `#data centers`, `#market analysis`, `#financing`, `#semiconductors`

---