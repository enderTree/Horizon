---
layout: default
title: "Horizon Summary: 2026-11-14 (EN)"
date: 2026-11-14
lang: en
---

> From 40 items, 4 important content pieces were selected

---

1. [Science: Unregulated Base-Editing Trial at Shanghai Xinhua Hospital Led to Girl's Death](#item-1) ⭐️ 9.0/10
2. [Hobbyist fine-tunes tiny transformer to predict personal blood sugar](#item-2) ⭐️ 8.0/10
3. [TorchTitan scales a 1T-parameter MoE to 1,300 tokens/s per GPU on JUPITER](#item-3) ⭐️ 8.0/10
4. [DeepSeek Opens Full-Stack Application API: Search, OCR, ASR, TTS and Tool Calling](#item-4) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Science: Unregulated Base-Editing Trial at Shanghai Xinhua Hospital Led to Girl's Death](https://t.me/zaihuapd/45103) ⭐️ 9.0/10

Science published an exclusive investigation on July 23, 2026 reporting that a 6-year-old girl with a rare single-base-mutation genetic disease died in late March 2025 after receiving an experimental base-editing therapy at Shanghai Jiao Tong University-affiliated Xinhua Hospital. The therapy was delivered by injecting trillions of AAV viral vectors into her spinal fluid to reach brain neurons, and she died seven days later from a severe immune reaction; the case was never publicly disclosed and allegedly bypassed regulatory oversight. The case raises fundamental questions about how experimental gene-editing therapies are reviewed and disclosed in China, and it echoes the 2018 He Jiankui affair that first brought global scrutiny to unregulated human genome editing. It could trigger tighter oversight of clinical trials, mandatory adverse-event reporting, and greater scrutiny of how unproven editing therapies are offered to desperate families. The treatment involved intrathecal injection of trillions of AAV vectors intended to reach brain neurons, and the child died seven days later from what was described as a severe immune response. Her parents reportedly paid more than $800,000 out of pocket, and the trial's ClinicalTrials.gov record had not been updated for over a year.

telegram · zaihuapd · Nov 13, 09:24

**Background**: Base editing is a CRISPR-derived technique that chemically converts one DNA letter into another without cutting both strands of the double helix, making it attractive for diseases caused by single-base mutations. Adeno-associated virus (AAV) is the most widely used delivery vehicle for gene therapy because it infects cells efficiently and generally causes limited immune response, but high doses and delivery directly into the central nervous system are known to carry risks of severe immune activation and neurotoxicity.

<details><summary>References</summary>
<ul>
<li><a href="https://www.synthego.com/crispr-base-editing-guide/">CRISPR Base Editing Explained | ABE & CBE in Gene Therapy</a></li>
<li><a href="https://www.addgene.org/guides/aav/">Addgene: Adeno-associated virus ( AAV ) Guide</a></li>
<li><a href="https://pmc.ncbi.nlm.nih.gov/articles/PMC11386282/">Immune responses to central nervous system directed...</a></li>

</ul>
</details>

**Tags**: `#gene-editing`, `#bioethics`, `#clinical-trials`, `#regulation`, `#investigative-journalism`

---

<a id="item-2"></a>
## [Hobbyist fine-tunes tiny transformer to predict personal blood sugar](https://www.reddit.com/r/MachineLearning/comments/1xvja5n/i_have_trained_a_model_to_predict_my_blood_sugar_p/) ⭐️ 8.0/10

A hobbyist trained a 31,253-parameter encoder-only transformer on roughly 19,200 CGM-years of synthetic type 1 diabetes data, then LoRA-finetuned it on 115 days of personal CGM data (80 days for adapter training, 35 for testing). The model can forecast blood glucose two hours ahead, infill missing CGM traces, and perform backcasts, and the author reports it is competitive with published models. This project shows that a very small, personally adapted model can be trained with synthetic pretraining plus LoRA personalization, potentially lowering the data and compute barriers for CGM forecasting. It also hints at counterfactual reasoning over insulin and carbohydrate inputs, which is important for practical diabetes decision support and edge-device AI. The model uses a variable context window of 3.5 to 7 days, predicts time-of-day from past glucose once context reaches at least 48 hours, and is trained in Kovatchev risk-space with DILATE/MSE and pinball loss combined via learned Kendall-Gal weights. Caveats include the lack of a downstream benchmark for counterfactual insulin/carb reasoning, and the author notes the model is still worse than they are at predicting hypoglycemia in the next ~30 minutes.

reddit · r/MachineLearning · /u/0xdeadf1sh · Nov 13, 20:48

**Background**: Continuous glucose monitors (CGMs) measure interstitial glucose frequently and are widely used in type 1 diabetes management, producing rich time-series data suitable for machine learning. LoRA (Low-Rank Adaptation) is a parameter-efficient fine-tuning technique that adapts a pretrained model by adding small low-rank weights instead of retraining the whole network. Transformers are neural sequence models that use attention over a context window, and here the author uses a synthetic simulator to pretrain on many simulated patients before personalizing to one real patient.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/LoRA_(machine_learning)">LoRA (machine learning) - Wikipedia</a></li>
<li><a href="https://www.nature.com/articles/s41586-025-09925-9">A foundation model for continuous glucose monitoring data</a></li>

</ul>
</details>

**Tags**: `#machine-learning`, `#healthcare-ai`, `#time-series`, `#lora`, `#synthetic-data`

---

<a id="item-3"></a>
## [TorchTitan scales a 1T-parameter MoE to 1,300 tokens/s per GPU on JUPITER](https://www.reddit.com/r/MachineLearning/comments/1xvce5h/scaling_to_1t_moe_on_torchtitan_p/) ⭐️ 8.0/10

An engineering team working with TorchTitan and PyTorch maintainers reported pushing GH200 GPUs on the JUPITER supercomputer to train a roughly 1-trillion-parameter Mixture-of-Experts model at about 1,300 tokens/s per GPU across 384 GPUs — a 14X improvement over their starting point, whose baseline step took 84 seconds with 68 of those seconds spent waiting on the network. It shows that a PyTorch-native stack (TorchTitan) can drive trillion-parameter MoE training at high throughput on hardware that is fast at compute but comparatively slow at inter-node networking, giving ML systems engineers a concrete, reproducible recipe instead of a vendor benchmark. The configuration is 384-way FSDP combined with 4-way expert parallelism kept strictly inside a node (pipeline parallelism was deliberately skipped to avoid long steps and slow debugging), and the wins came from full activation checkpointing (~4X), offloading checkpoint activations to Grace over the 900 GB/s C2C link with layer-ahead prefetch, switching from Adam to Muon to halve optimizer state and reach 64k-token sequences, and using FlexShard to shard experts as whole experts so Newton-Schulz orthogonalization runs locally with zero communication.

reddit · r/MachineLearning · /u/f14-bertolotti · Nov 13, 16:28

**Background**: TorchTitan is a clean-room, PyTorch-native platform for large-scale LLM pre-training, and a Mixture-of-Experts (MoE) model activates only a subset of its expert subnetworks per token, so total parameters can grow far beyond per-token compute. Training such a model requires sharding: Fully Sharded Data Parallel (FSDP) slices every weight across ranks and gathers them just in time, while Expert Parallelism (EP) gives each GPU a subset of experts and routes tokens to them over the network. GH200 is NVIDIA's Grace Hopper Superchip pairing an HBM3e GPU with a Grace CPU over a 900 GB/s chip-to-chip link, and JUPITER is the supercomputer built from them; on JUPITER, InfiniBand delivers only ~25 GB/s per GPU, roughly 6X slower than NVLink.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/pytorch/torchtitan">GitHub - pytorch/ torchtitan : A PyTorch native platform for training...</a></li>
<li><a href="https://arxiv.org/abs/2410.06511">[2410.06511] TorchTitan : One-stop PyTorch native solution for...</a></li>
<li><a href="https://en.wikipedia.org/wiki/Mixture_of_experts">Mixture of experts - Wikipedia</a></li>

</ul>
</details>

**Tags**: `#distributed-training`, `#MoE`, `#PyTorch`, `#HPC`, `#GPU-scaling`

---

<a id="item-4"></a>
## [DeepSeek Opens Full-Stack Application API: Search, OCR, ASR, TTS and Tool Calling](https://mp.weixin.qq.com/s/78KBHc4-4N5b2vfL9SkutQ) ⭐️ 8.0/10

DeepSeek has opened up its "full-stack" application API, letting developers toggle parameters in the existing API to gain deep-thinking search, file input, link reading and voice conversation capabilities, with the server automatically handling tool invocation and context stitching. The V4.1-Flash model is supported across three endpoints, while Search, Fetch, OCR, ASR and TTS can also be called individually, and the company open-sourced a frontend chat demo (deepseek-ai/chat-demo) that can import existing conversation history. This turns DeepSeek's API from a plain text-completion endpoint into an application-level platform where retrieval, vision, speech and agent-style tool orchestration are handled server-side, lowering the engineering cost for anyone building a ChatGPT-style assistant. It also intensifies competition with other model providers that charge separately for search, OCR and speech services. The demo client supports streaming replies, deep thinking, smart search, link reading with source citations, attachment upload/paste/drag-and-drop, voice input and read-aloud replies, and it lets users import chat history exported from DeepSeek Chat so they can continue existing conversations locally with their own API key. The underlying V4.1-Flash is a multimodal Mixture-of-Experts model with a 552B backbone and up to 1M-token context, activating only 8B parameters during prefill and 16B during decode.

telegram · zaihuapd · Nov 13, 14:27

**Background**: DeepSeek-V4.1-Flash is the smallest model in DeepSeek's new architecture family, designed for faster inference and higher throughput while natively understanding images as well as text. Tool calling (also called function calling) is the mechanism by which a model decides which external capability — a web search, a page fetch, an OCR pass or a text-to-speech conversion — to invoke for a given user request; normally developers must wire these tools up themselves. OCR, ASR and TTS refer to optical character recognition (text from images/PDFs), automatic speech recognition (speech to text) and text-to-speech synthesis respectively.

<details><summary>References</summary>
<ul>
<li><a href="https://www.deepseek.com/en/news/deepseek-v4-1-flash/">DeepSeek | Introducing DeepSeek-V4.1-Flash: smarter, faster ...</a></li>
<li><a href="https://huggingface.co/deepseek-ai/DeepSeek-V4.1-Flash">deepseek-ai/DeepSeek-V4.1-Flash · Hugging Face</a></li>
<li><a href="https://github.com/deepseek-ai/chat-demo">GitHub - deepseek -ai/ chat - demo : Chat Demo · GitHub</a></li>

</ul>
</details>

**Tags**: `#DeepSeek`, `#API`, `#LLM`, `#multimodal`, `#open-source`

---