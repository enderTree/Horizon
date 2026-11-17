---
layout: default
title: "Horizon Summary: 2026-11-17 (ZH)"
date: 2026-11-17
lang: zh
---

> 从 43 条内容中筛选出 4 条重要资讯。

---

1. [Burnt Sushi 发布 Rust 日期时间库 Jiff 1.0，设计立场鲜明](#item-1) ⭐️ 9.0/10
2. [vLLM v0.34.0 发布：默认启用可扩展 KV 缓存，Model Runner V1 被移除](#item-2) ⭐️ 8.0/10
3. [Optimizely 供应链攻击向 Zoom、GitLab 等 178 个网站投放恶意代码](#item-3) ⭐️ 8.0/10
4. [12.7 万篇论文消融分析：26%的改动未带来提升](#item-4) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Burnt Sushi 发布 Rust 日期时间库 Jiff 1.0，设计立场鲜明](https://burntsushi.net/jiff/) ⭐️ 9.0/10

ripgrep 和 regex 库的作者 Andrew Gallant（BurntSushi）发布了 Rust 的新日期时间库 Jiff 1.0。此次发布不仅带来了立场鲜明的 API 设计——把时区处理和夏令时正确性放在核心位置——还附上了与现有 chrono、time 两个库的详细对比文档。 日期时间处理是软件开发中最容易出错的领域之一，而 Rust 生态长期依赖 chrono——它虽然稳定，但 API 被普遍认为已经过时。如今一位有着出色履历的维护者带来了成熟且文档完备的替代方案，这为 Rust 开发者提供了可信的迁移路径，也抬高了整个生态在 API 设计上的门槛。 Jiff 专注于提供难以被误用的高层日期时间原语，同时保持合理的性能，并且与 chrono、time 不同，它开箱即支持读取系统自带的时区数据库（Time Zone Database）。其文档明确带有立场，并直言 Jiff 并非适用于所有场景的万能工具；另外，Jiff 的读音类似 "gif"，但 g 发软音。

hackernews · burntsushi · 11月16日 16:53 · [社区讨论](https://news.ycombinator.com/item?id=50519744)

**背景**: 日期时间库负责表示时间点、日历日期、时间间隔以及时区之间的转换——其中还包括夏令时问题：在夏令时切换时，时钟会跳过或重复某些小时，简单的算术会在不知不觉中得出错误结果。多年来 chrono 一直是 Rust 的默认选择，time 库则是主要替代品，而这两者都把时区数据库的加载交给 chrono-tz、time-tz 等第三方库处理。Jiff 的核心理念是：时区处理应当内建于核心 API，而不是事后外挂，从而让常见错误难以被写出来。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://burntsushi.net/jiff/">A datetime library for Rust - Andrew Gallant's Blog</a></li>
<li><a href="https://docs.rs/jiff/latest/jiff/">jiff - Rust - Docs.rs</a></li>
<li><a href="https://docs.rs/jiff/latest/jiff/_documentation/comparison/index.html">Comparison with other Rust datetime crates</a></li>

</ul>
</details>

**社区讨论**: 社区讨论整体非常热情：评论者称赞 Jiff 的质量，希望更广泛的生态能采用它取代 chrono，并特别指出文档坦诚地划定适用范围（"Jiff 并不总是合适的选择"）堪称工程实践的典范。一位前 chrono 维护者解释说，自己当初接手维护正是想改进其 API，但任何改动都遭遇阻力，最终因心力交瘁而放弃，并对 BurntSushi 写出了自己一直想要的那个日期时间库表示感谢。也有人提出了更深层的技术问题，询问 Jiff 如何处理 TAI、UT1 等时间尺度，以满足超长时间跨度或高精度模拟的需求。

**标签**: `#rust`, `#datetime`, `#libraries`, `#open-source`, `#api-design`

---

<a id="item-2"></a>
## [vLLM v0.34.0 发布：默认启用可扩展 KV 缓存，Model Runner V1 被移除](https://github.com/vllm-project/vllm/releases/tag/v0.34.0) ⭐️ 8.0/10

vLLM 发布了 v0.34.0，这是一个由 412 位贡献者提交 1,061 个 commit 的大型版本，新增 10 个模型架构（包括 Mistral Large 4、MiniMax-M3.1-Flash 和 Nemotron-3.5-Transcribe），并默认启用可扩展的 KV 缓存容量测算。Model Runner V1 已被彻底移除，Model Runner V2 成为唯一的 GPU 运行器；该版本在 Blackwell 上带来最高 1.95 倍的解码加速，在 MI355X 级别硬件上带来 1.6 倍的吞吐提升。 vLLM 是部署最广泛的开源大模型推理引擎之一，因此默认开启的 KV 缓存改动会直接扩大缓存容量（例如 MiniMax-M3 在 H200 上从 433k 增至 672k token），从而影响所有生产环境推理的吞吐和首 token 延迟。同时，默认块大小从 16 改为 64、ROCm 7.2 构建产物被弃用、强制要求 huggingface_hub >= 2.0.0 等破坏性变更意味着运维人员必须提前规划升级，而不能直接拉取新镜像。 新的容量测算逻辑基于 CUDA graph 捕获与预热之后实际空闲的显存，而非依赖估算值，这会使部分模型的单 token 解码延迟上升（在某些 H200 模型、并发 128 时 TPOT 增加 6–18%）；用户可通过 --gpu-memory-utilization 0.9 或 --no-enable-extensible-kv-cache 关闭该特性。升级者还需移除 VLLM_USE_V2_MODEL_RUNNER=0（现在会在启动时直接报错），将 V1 的 logits processor 迁移到 vllm.v1.worker.gpu.sample.logits_processor，并注意 QuTLASS/fp_quant 检查点已无法加载。

github · khluu · 11月16日 23:22

**背景**: vLLM 是一个开源的大语言模型推理与服务引擎，最知名的是 PagedAttention 技术：它把 KV 缓存（模型保存的 key/value 张量，用于复用上下文而非重复计算）像虚拟内存分页一样按固定大小的块来管理。过去 vLLM 依靠 gpu_memory_utilization 比例（默认 0.92）来估算能容纳多少 KV 缓存；新的可扩展设计则预先保留地址空间并按需提交块，块保持固定偏移，从而让已捕获的 CUDA graph 始终有效。Model Runner 是每步执行实际前向计算的组件，Model Runner V2 是先从头重写、更模块化的版本，本次发布中 V1 正式退役。该版本还针对 NVIDIA Blackwell（GB200）和基于 CDNA 4 架构的 AMD MI355X 等新加速器做了优化，这些硬件拥有非常大的 HBM 容量，适合开放权重模型的服务部署。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://docs.vllm.ai/en/latest/api/vllm/v1/worker/extensible_kv_cache/">extensible_kv_cache - vLLM</a></li>
<li><a href="https://vllm.ai/blog/2026-03-24-mrv2">Model Runner V2: A Modular and Faster Core for vLLM</a></li>
<li><a href="https://www.developersdigest.tech/blog/amd-mi355x-vs-nvidia-b200-b300-open-weights-serving-2026">AMD MI 355 X vs NVIDIA B200 vs B300 for... - Developers Digest</a></li>

</ul>
</details>

**标签**: `#vllm`, `#llm-inference`, `#kv-cache`, `#release-notes`, `#gpu-optimization`

---

<a id="item-3"></a>
## [Optimizely 供应链攻击向 Zoom、GitLab 等 178 个网站投放恶意代码](https://blog.report-uri.com/worlds-largest-brands-infected-with-malware-via-optimizely/) ⭐️ 8.0/10

攻击者在广泛使用的实验与 A/B 测试平台 Optimizely Web 中植入了恶意 JavaScript，这些代码于 11 月 16 日被投递给 178 家机构的网站访客，包括 Zoom、GitLab、CNN、BBC、Salesforce、宜家、汇丰和 Ledger。最先披露此事的 Report URI 强调，Optimizely 的 CDN 只是原样分发了它收到的内容——这不是 CDN 缓存投毒，而是恶意内容经由 Optimizely 自身的分发流程流出。 这是一次典型的第三方脚本供应链失效：任何嵌入了 Optimizely 代码片段的网站——包括互联网上流量最大的一批站点——在自己代码一行未改的情况下就悄然变成了恶意软件分发渠道。这也让长期存在的争论更加尖锐：由市场部门驱动的标签注入（Optimizely、Google Tag Manager 等工具）在生产环境中打开了一条大多数组织既不监控也无法控制的信任通道。 根据 Report URI 的分析，注入的代码会替换加密货币钱包地址，并在部分受影响网站中窃取用户输入的银行卡信息，连 Optimizely 自家站点（www.optimizely.com 和 login.optimizely.com）的代码片段也带有该载荷。攻击者究竟如何获得横跨如此多互不相关客户项目的写入权限，目前仍无解释——可能是 Optimizely 内部系统被攻破，也可能是某个具备跨客户权限的凭证泄露。

hackernews · kristjansson · 11月16日 23:00 · [社区讨论](https://news.ycombinator.com/item?id=50524767)

**背景**: Optimizely Web 是一个 SaaS 实验平台，客户页面中嵌入它的 JavaScript 代码片段，市场人员无需发版就能运行 A/B 测试和功能开关。由于该片段是在运行时从 Optimizely 的 CDN 加载并在宿主页面上以完全权限执行——Google Tag Manager 等标签管理器采用同样的信任模型——因此上游一旦被攻破，所有嵌入该脚本的站点会同时中招。关于第三方 JavaScript 的安全指南早已指出，供应商服务端被攻陷是最大的单一风险，因为宿主网站根本无法检查或对收到的内容做版本锁定。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.bleepingcomputer.com/news/security/optimizely-supply-chain-attack-delivers-malware-to-cnn-fox-news-bbc-salesforce-sites/">Optimizely hack infected CNN, Fox News, BBC, Salesforce sites ...</a></li>
<li><a href="https://shiftdelete.net/en/optimizely-malware">Optimizely Malware Hit 178 Sites: What It Stole and What to Do</a></li>
<li><a href="https://pentest.y-security.de/OWASP+Cheat+Sheet+Series/Third_Party_Javascript_Management_Cheat_Sheet/">Y- Security performs Attack Simulations, Penetration Tests, and...</a></li>

</ul>
</details>

**社区讨论**: 评论者普遍认为问题出在结构层面：有人指出 Google Tag Manager 的初衷正是让市场部门无需工程介入即可添加标签，页面因此塞进了数 MB 的不可信 JavaScript，并希望团队现在能重新审视这一做法。也有人要求追责，认为 Optimizely 缺少分阶段发布、自动化安全检查等发布防护机制，而 CNN、BBC 这类超大站点更没有理由不采取同样的管控、或改为由自己一方提供脚本。还有少数人提出质疑或追问：除非站点自身也有疏忽，否则单纯供应商被攻破不应足以窃取银行卡数据，并建议用 NoScript 之类的工具降低暴露面。

**标签**: `#security`, `#supply-chain`, `#third-party-scripts`, `#web-security`, `#malware`

---

<a id="item-4"></a>
## [12.7 万篇论文消融分析：26%的改动未带来提升](https://www.reddit.com/r/MachineLearning/comments/1xybvju/we_logged_621k_changes_from_127k_papers_ablations/) ⭐️ 8.0/10

Latentic Labs 从 2016 至 2026 年间 ICML、NeurIPS、ICLR、CVPR、AAAI、ICCV、ECCV、TPAMI、IJCV、JMLR 等场所发表的 126,758 篇机器学习论文全文中，抽取了 621,064 项消融改动。按论文自身报告的数字，69% 的改动有帮助，10% 无明显效果，16% 更差，5% 结果混杂，即 26% 的改动未带来帮助。 这是一次对机器学习论文消融实验实际报告内容的大规模实证审计，而非又一个模型准确率基准；它发现 66% 的论文至少包含一项按自身数字未带来帮助的改动。这可能推动作者和审稿人把零结果和负结果也视为可发表证据，并为哪些常见调整——例如提高采样温度或 LoRA 秩——经常无效提供具体先验。 分析报告了场所差异：机器学习场所有 31% 的改动报告为零结果或负结果，而视觉场所为 22%；在常见改动中，提高采样温度在 122 篇论文里有 52% 未带来帮助，增大 LoRA 秩为 46%，增大学习率为 46%，而添加对比损失在 1,317 个案例中仅 4% 未带来帮助。注意事项包括其自动化全文抽取方法，以及作者披露他们构建了该图谱，不过他们表示会公开方法并接受更正。

reddit · r/MachineLearning · /u/latenticlabs · 11月17日 05:11

**背景**: 机器学习中的消融研究，是通过移除、禁用或改变系统的一个组成部分——例如某一层、损失项、数据规模或超参数——来衡量该部分对性能影响的实验。LoRA 是一种参数高效微调方法，它在冻结的模型上加入小型低秩可训练矩阵；其秩控制适配器容量，增大秩并不自动带来更好效果。对比损失则训练嵌入表示，使相似样本更接近、不相似样本更远离，常用于表示学习。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Ablation_(artificial_intelligence)">Ablation (artificial intelligence) - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/LoRA_(machine_learning)">LoRA (machine learning) - Wikipedia</a></li>
<li><a href="https://www.geeksforgeeks.org/deep-learning/loss-functions-in-deep-learning/">Loss Functions in Deep Learning - GeeksforGeeks</a></li>

</ul>
</details>

**标签**: `#machine-learning`, `#ablation-studies`, `#meta-research`, `#empirical-analysis`, `#research-practice`

---