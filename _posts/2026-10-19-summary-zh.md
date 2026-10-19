---
layout: default
title: "Horizon Summary: 2026-10-19 (ZH)"
date: 2026-10-19
lang: zh
---

> 从 36 条内容中筛选出 2 条重要资讯。

---

1. [vLLM v0.32.0 发布：新增结构化决策 API，低精度 KV 缓存全面铺开](#item-1) ⭐️ 8.0/10
2. [美国 AI 基建热潮现裂痕：十万亿美元投资面临回报考验](#item-2) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [vLLM v0.32.0 发布：新增结构化决策 API，低精度 KV 缓存全面铺开](https://github.com/vllm-project/vllm/releases/tag/v0.32.0) ⭐️ 8.0/10

vLLM v0.32.0 正式发布，包含来自 363 位贡献者（其中 121 位是新贡献者）的 814 个提交；核心亮点是新增的 `POST /v1/systemone` 端点，可在结构化状态上回答 `choice`、`noul` 和 `score` 类问题，该端点默认启用，并已支持 `Cloudflare/clef-omni`、`LiquidAI/d1-3B` 和 DiffusionGemma 等模型。本次发布还引入了通用的 `hf` 工具调用解析器与推理内容解析器（`--tool-call-parser hf`、`--reasoning-parser hf`），它们直接读取模型检查点中的 `response_template`，因此自带该模板的模型无需再编写模型专用解析器，Python 与 Rust 两套前端均已支持。 低精度 KV 缓存的支持范围如今已覆盖 SM8x/SM12x 与 SM90 上的 NVFP4、SM100 上 GLM-5.x 默认启用的 FP8，以及 ROCm 上的 4 比特 `ultraquant_4bit`，这直接降低了制约长上下文与高并发推理服务的显存占用。再加上通用 `hf` 解析器免去了为每个模型单独编写适配代码，以及启动与服务性能的优化，本次发布降低了在 NVIDIA 与 AMD 硬件上用 vLLM 部署新模型的工程成本。 升级前需注意若干破坏性变更：不再支持 Python 3.10，默认允许的 CORS 来源被收紧，依赖要求变为 `transformers>=5.16.1,<5.20.0` 与 `tokenizers>=0.23.2`，cascade attention 与 `mamba_cache_mode="all"` 被移除，且 `max_tokens` 不再从上下文窗口中预留。各 PR 中的基准数据均与具体模型和硬件相关——例如 SM100 上 GLM-5.x 的 FP8 KV 缓存将每个 rank 的 KV 显存减半，吞吐提升 2.3-5.5%，但首 token 延迟（TTFT）增加 7-11%；而 SM90 上的 `fp8_ds_mla` 让 GLM-5.3-Flash 的输出吞吐最高提升 31%。

github · khluu · 10月18日 06:50

**背景**: vLLM 是广泛使用的开源大模型推理与服务引擎，以 PagedAttention 式的显存管理著称。它的 KV 缓存保存每个已处理 token 的 key 与 value 向量，使自回归解码无需重复计算，因此 KV 缓存的大小往往决定了可支持的上下文长度、批大小与并发度。以更低精度（FP8、NVFP4、4 比特）存储该缓存可以减少每条序列的显存占用，但会付出一定的精度与延迟代价，且硬件支持取决于 GPU 代际——SM90 指 NVIDIA Hopper 架构的 H100/H200 等型号，SM100 则是 Blackwell 数据中心代际，而 XQA 是 NVIDIA 针对解码阶段优化的专用注意力内核。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.lmsys.org/">LMSYS Org</a></li>
<li><a href="https://arnon.dk/matching-sm-architectures-arch-and-gencode-for-various-nvidia-cards/">Matching CUDA arch and CUDA gencode for various NVIDIA ...</a></li>
<li><a href="https://docs.nvidia.com/cuda/pdf/Blackwell_Compatibility_Guide.pdf">Blackwell Compatibility Guide - NVIDIA Documentation Hub</a></li>

</ul>
</details>

**标签**: `#vLLM`, `#LLM inference`, `#model serving`, `#KV cache`, `#release notes`

---

<a id="item-2"></a>
## [美国 AI 基建热潮现裂痕：十万亿美元投资面临回报考验](https://www.ft.com/content/9ea5a37d-15c9-4d5b-94d6-719048c9cd3c?syn-25a6b1a6=1) ⭐️ 8.0/10

2025 年至 2032 年，美国 AI 基础设施支出预计将超过 10 万亿美元，但自 2026 年初以来，随着融资成本上升、审批受阻和公众反对加剧，已有至少 47 个大型数据中心项目被推迟、撤回或叫停。分析机构估计，美国规划中的数据中心项目仅约 35% 具有较高可行性；英伟达大力支持的云服务商 CoreWeave 周五跌超 11%，费城半导体指数（SOX）则连续第 8 个交易日下跌，追平 2006 年以来最长连跌纪录。 这轮回调表明，支撑芯片需求、超大规模云厂商财报以及美股涨势的 AI 资本开支周期，可能已跑在实际需求与融资能力之前。如果项目取消持续蔓延，将波及数据中心供应链、电力与建筑企业，以及那些已把多年不间断的 AI 增长计入股价的芯片厂商。 融资压力正成为关键瓶颈：数据中心属于资本密集、建设周期长的资产，高度依赖廉价债务，利率上行会直接削弱项目经济性。市场正在重新定价盈利预期，半导体指数连续八个交易日下挫，也呼应了该板块在快速上涨后常出现数月级大幅回撤的历史规律。

telegram · zaihuapd · 10月18日 08:52

**背景**: CoreWeave 是一家以 GPU 为核心的云服务商（IaaS），向 AI 开发者出租英伟达加速算力，凭借英伟达的背书成为 AI 基础设施需求的风向标。费城半导体指数（SOX）追踪美国上市的顶尖半导体公司，涵盖存储芯片厂商与 AI 芯片供应商，是市场广泛关注的行业景气指标。由于 AI 基建大量依赖债务融资和长期产能合约，它对利率变化以及 AI 收入增长跟不上基础设施扩张的任何迹象都格外敏感。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://news.qq.com/rain/a/20251216A076YN00">CoreWeave ： 英 伟 达 “干儿子” 真能子凭父贵？_ 腾讯新闻</a></li>
<li><a href="https://www.laohu8.com/stock/SOX">费 城 半 导 体 指 数 ( SOX )... | 老虎社区</a></li>
<li><a href="https://www.21jingji.com/article/20260714/herald/563e762bc36ac35d8bf5dadc4aca4fe0.html">三问 半 导 体 板块巨震：为何暴跌？ 见顶了吗？ 能买入吗？ - 21经济网</a></li>

</ul>
</details>

**标签**: `#AI infrastructure`, `#data centers`, `#market analysis`, `#financing`, `#semiconductors`

---