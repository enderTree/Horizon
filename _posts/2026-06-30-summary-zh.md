---
layout: default
title: "Horizon Summary: 2026-06-30 (ZH)"
date: 2026-06-30
lang: zh
---

> 从 39 条内容中筛选出 11 条重要资讯。

---

1. [最高法院裁定地理围栏搜查令需宪法保护](#item-1) ⭐️ 9.0/10
2. [vLLM v0.24.0 发布，带来重大优化](#item-2) ⭐️ 8.0/10
3. [火箭实验室以 80 亿美元收购铱星](#item-3) ⭐️ 8.0/10
4. [WATaBoy：将 Game Boy 指令 JIT 编译为 WebAssembly，性能超越原生解释器](#item-4) ⭐️ 8.0/10
5. [深入解析：CUDA 内核从 CPU 到 GPU 的执行流程](#item-5) ⭐️ 8.0/10
6. [Ornith-1.0：开源权重 LLM 在智能编码中达到 SOTA](#item-6) ⭐️ 8.0/10
7. [Cerebras 与 OpenAI 交易将初创公司推至候补名单末尾](#item-7) ⭐️ 8.0/10
8. [谷歌 AI 同行评审在 ICML/STOC 处理约 1 万篇论文](#item-8) ⭐️ 8.0/10
9. [EML 树被证明是通用逼近器](#item-9) ⭐️ 8.0/10
10. [长鑫存储与腾讯签订近 30 亿美元 DRAM 协议](#item-10) ⭐️ 8.0/10
11. [特斯拉 FSD v14 Lite：HW3 车型获得 HW4 级能力](#item-11) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [最高法院裁定地理围栏搜查令需宪法保护](https://www.theguardian.com/us-news/2026/jun/29/supreme-court-geofence-warrants-case-decision) ⭐️ 9.0/10

美国最高法院以 6 比 3 裁定，地理围栏搜查令受第四修正案保护，确认个人对其手机位置数据拥有合理的隐私期待。该判决由埃琳娜·卡根大法官执笔。 这一里程碑式的判决极大地限制了执法部门在没有搜查令的情况下进行大规模位置监控的能力，为无处不在的移动追踪时代的数字隐私设定了关键先例。它将影响未来的调查以及存储位置数据的科技公司。 该案源于一起银行抢劫案，谷歌提供了银行周围 150 米范围内设备的位置数据。法院认为，地理围栏搜查令必须基于可能原因，并具体描述要搜查的地点，引用了 2014 年 Riley 诉加利福尼亚州案的裁决。该裁决并未完全禁止地理围栏搜查令，但要求其符合传统的搜查令要求。

hackernews · cdrnsf · 6月29日 15:54 · [社区讨论](https://news.ycombinator.com/item?id=48720924)

**背景**: 地理围栏搜查令是一种反向定位搜查令，允许执法部门要求科技公司提供特定时间段内特定地理区域内所有移动设备的列表。第四修正案保护公民免受不合理的搜查和扣押，传统上法院要求搜查令指明要搜查的人或地点。该裁决将这一保护扩展到数字位置数据，即使数据由第三方持有且在公共空间收集。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.theguardian.com/us-news/2026/jun/29/supreme-court-geofence-warrants-case-decision">US supreme court rules geofence warrants require constitutional privacy protections | US supreme court | The Guardian</a></li>
<li><a href="https://en.wikipedia.org/wiki/Geofence_warrant">Geofence warrant - Wikipedia</a></li>
<li><a href="https://techcrunch.com/2026/06/29/in-major-privacy-win-supreme-court-rules-geofence-warrants-are-protected-by-privacy-rights/">In major privacy win, Supreme Court rules geofence warrants are protected by privacy rights | TechCrunch</a></li>

</ul>
</details>

**社区讨论**: 评论者强调了诸如 Paula Broadwell 案等历史先例，并赞扬法院引用了来源。一些人担心其他监控技术如 Flock 摄像头现在可能需要搜查令。其他人则讨论了有效执法与隐私权之间的平衡，总体情绪支持该裁决对隐私的保护。

**标签**: `#privacy`, `#supreme court`, `#geofence warrants`, `#digital rights`, `#fourth amendment`

---

<a id="item-2"></a>
## [vLLM v0.24.0 发布，带来重大优化](https://github.com/vllm-project/vllm/releases/tag/v0.24.0) ⭐️ 8.0/10

vLLM v0.24.0 新增了对 MiniMax-M3 和 DeepSeek-V4 模型的支持，默认启用 Model Runner V2 以支持量化模型，并包含来自 256 位贡献者的 571 次提交，进行了广泛的性能优化。 此次发布凸显了 vLLM 的快速开发和强大的社区参与，巩固了其作为领先开源 LLM 推理引擎的地位。对 DeepSeek-V4 和 MiniMax-M3 的优化使得尖端模型的推理更快速高效，惠及开发者和终端用户。 关键技术细节包括：用于 DeepSeek-V4 的 FlashInfer 稀疏索引缓存（提升首 token 延迟）、MiniMax-M3 的 MXFP4 量化支持，以及 Model Runner V2 默认用于量化模型。此版本还新增了流式解析引擎和 DiffusionGemma 支持。

github · khluu · 6月29日 19:41

**背景**: vLLM 是一个高吞吐、内存高效的大语言模型推理引擎，广泛应用于生产环境。FlashInfer 是一个用于 LLM 服务的内核库，优化注意力计算；MXFP4 是一种 4 位浮点格式，用于模型量化，可减少内存占用。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/flashinfer-ai/flashinfer">GitHub - flashinfer-ai/flashinfer: FlashInfer: Kernel Library for LLM Serving · GitHub</a></li>
<li><a href="https://arxiv.org/abs/2501.01005">[2501.01005] FlashInfer: Efficient and Customizable Attention Engine for LLM Inference Serving</a></li>
<li><a href="https://rocm.blogs.amd.com/artificial-intelligence/w4a6-quant-mm/README.html">MXFP6 and MXFP 4 Mixed Precision for Accelerating... — ROCm Blogs</a></li>

</ul>
</details>

**标签**: `#vllm`, `#LLM serving`, `#open-source`, `#performance`, `#deep learning`

---

<a id="item-3"></a>
## [火箭实验室以 80 亿美元收购铱星](https://investors.rocketlabcorp.com/news-releases/news-release-details/rocket-lab-acquire-iridium-historic-deal-creating-fully) ⭐️ 8.0/10

火箭实验室于 2025 年 6 月 29 日宣布，将以现金加股票方式收购铱星通信公司，交易价值约 80 亿美元。合并预计于 2027 年年中完成，尚需铱星股东和监管批准。 这笔收购打造了一家完全整合的航天公司，将火箭实验室的发射和航天器制造能力与铱星的卫星网络和频谱相结合，从而进入卫星物联网、直连设备和定位导航授时市场。这模仿了 SpaceX 利用 Starlink 保障发射需求的模式。 火箭实验室已获得 36 亿美元过桥贷款承诺。铱星的 L 波段频谱、由 66 颗在轨卫星组成的全球星座以及超过 255 万活跃订阅者是关键资产。

hackernews · everfrustrated · 6月29日 14:09 · [社区讨论](https://news.ycombinator.com/item?id=48719485)

**背景**: 火箭实验室是一家发射服务提供商和卫星制造商，以其电子号小型运载火箭闻名。铱星运营着一套低地球轨道卫星星座，提供全球语音和数据通信。这笔交易反映了航天业垂直整合的趋势。

**社区讨论**: 评论中有人担忧太空垃圾和轨道商业化，认为未来可能出现卫星广告。另有人称赞该交易是保障发射合同的明智之举，类似于 SpaceX 的 Starlink 模式。一名技术用户回忆 2014 年使用铱星数据时每 KB 收费 1 美元。

**标签**: `#rocket-lab`, `#iridium`, `#space`, `#acquisition`, `#satellites`

---

<a id="item-4"></a>
## [WATaBoy：将 Game Boy 指令 JIT 编译为 WebAssembly，性能超越原生解释器](https://humphri.es/blog/WATaBoy/) ⭐️ 8.0/10

Will Humphreys 发表博客文章，展示了一个名为 WATaBoy 的项目，它将 Game Boy 模拟器指令即时编译（JIT）为 WebAssembly（WASM），性能甚至超越了原生解释器。 这一方法挑战了原生解释器总是更快的传统假设，并为受 JIT 限制的平台（如 iOS）上的高性能模拟开辟了新可能——因为 WebAssembly JIT 在浏览器中是被允许的。 WATaBoy 项目在运行时将 Game Boy CPU 指令编译为 WebAssembly 模块，相比原生解释器实现了加速。作者指出，在运行编译后的 WASM 时，Firefox 比 Chrome 或 Safari 慢约 25%。

hackernews · energeticbark · 6月29日 15:02 · [社区讨论](https://news.ycombinator.com/item?id=48720190)

**背景**: 即时编译（JIT）是一种在运行时将代码编译为原生机器码以加速执行的技术，而解释器则逐条处理指令。WebAssembly（WASM）是一种低级二进制格式，在浏览器中以接近原生的性能运行，即使在像 iOS 这样通常限制 JIT 编译的平台上，浏览器也被允许对 WASM 使用 JIT。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Tracing_just-in-time_compilation">Tracing just-in-time compilation - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 评论者称赞该项目作为本科生作品令人印象深刻，并指出 WASM 开销（约 20%）远低于解释器开销（约 1000%），从而解释了性能优势。讨论还涉及相关方法，如 JavaScript 中的基于 eval 的 JIT、NES 代码的静态重编译，以及通过 WASM 巧妙绕过 iOS JIT 限制的方法。

**标签**: `#JIT`, `#WebAssembly`, `#Game Boy`, `#Emulation`, `#Performance`

---

<a id="item-5"></a>
## [深入解析：CUDA 内核从 CPU 到 GPU 的执行流程](https://fergusfinn.com/blog/what-happens-when-you-run-a-gpu-kernel/) ⭐️ 8.0/10

一篇详细的博客文章全面介绍了启动 CUDA 内核的完整过程，涵盖 CPU 驱动交互、命令提交、GPU 硬件调度以及线程束执行。 这篇文章解释了从 CUDA API 调用到实际硬件执行这一通常不透明的路径，弥合了理解 GPU 编程的关键空白，对性能优化和调试至关重要。 文章特别关注了门铃寄存器和队列管理描述符（QMD），它们是 CPU 端 CUDA 运行时与 GPU 硬件之间的桥梁。文章还详细解释了线程束资格和调度。

hackernews · mezark · 6月29日 13:11 · [社区讨论](https://news.ycombinator.com/item?id=48718863)

**背景**: CUDA（统一计算设备架构）是 NVIDIA 的并行计算平台和编程模型。CUDA 内核是一个在 GPU 上运行的函数，通过 CPU 调用 CUDA 运行时 API 来启动。GPU 以 32 个线程为一组（称为线程束）进行处理，由线程束调度器调度以隐藏内存延迟。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.hpcs.cs.tsukuba.ac.jp/icpp2019/data/posters/Poster17-abst.pdf">Understanding the Overheads of Launching CUDA Kernels</a></li>
<li><a href="https://modal.com/gpu-glossary/device-hardware/warp-scheduler">What is a Warp Scheduler? | GPU Glossary</a></li>
<li><a href="https://stevengong.co/notes/Warp-Scheduling">Warp Scheduling (GPU Thread Scheduling)</a></li>

</ul>
</details>

**社区讨论**: 评论者称赞了文章的深度，特别是对门铃和 QMD 的解释。一位读者指出 CUDA 的自动命令同步与 Vulkan 的显式方法形成对比。另一位读者猜测开源内核优化库可能会与商业优化公司竞争。

**标签**: `#CUDA`, `#GPU programming`, `#kernel execution`, `#NVIDIA`, `#HPC`

---

<a id="item-6"></a>
## [Ornith-1.0：开源权重 LLM 在智能编码中达到 SOTA](https://simonwillison.net/2026/Jun/29/ornith/#atom-everything) ⭐️ 8.0/10

DeepReinforce 发布了 Ornith-1.0 系列开源权重的大语言模型（LLM），采用 MIT 许可证，在编码基准测试中取得了同规模开源模型的最优性能。这些模型基于 Google 的 Gemma 4 和阿里巴巴的 Qwen 3.5，参数量从 9B 到 397B 不等。 Ornith-1.0 的开源权重、宽松许可证和强大的编码性能使其成为开源 AI 生态系统的重要补充，可能加速自主编码智能体的发展。其自脚手架方法可以减少智能体工作流中复杂外部工具包的需求。 该模型系列包括 35B 混合专家（MoE）变体和 397B MoE 变体，Simon Willison 使用 LM Studio 和 Pi 测试了 35B GGUF 文件（约 20GB），在多工具调用智能体 harness 中表现出色。底层模型（Gemma 4 和 Qwen 3.5）均采用 Apache 2.0 许可证，确保了许可证兼容性。

rss · Simon Willison · 6月29日 16:17

**背景**: 自脚手架 LLM 可以自行构建推理步骤或工具调用，无需外部编排，从而改进智能编码能力。Ornith-1.0 等开源权重模型允许研究者和开发者在本地或自定义基础设施上运行强大的 LLM，减少对专有 API 的依赖。GGUF 是一种文件格式，针对使用 llama.cpp 和 LM Studio 等项目在消费级硬件上运行 LLM 进行了优化。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://simonwillison.net/2026/Jun/29/ornith/">Ornith-1.0: Self - Scaffolding LLMs for Agentic Coding</a></li>
<li><a href="https://deep-reinforce.com/ornith_1_0.html">Ornith-1.0: Self - Scaffolding LLMs ... | DeepReinforce Blog | Jun. 2026</a></li>

</ul>
</details>

**标签**: `#LLM`, `#open-source`, `#coding`, `#AI`, `#machine learning`

---

<a id="item-7"></a>
## [Cerebras 与 OpenAI 交易将初创公司推至候补名单末尾](https://www.reddit.com/r/MachineLearning/comments/1uiqhiv/cerebras_openai_deal_capacity_has_effectively/) ⭐️ 8.0/10

一位初创公司创始人报告称，Cerebras 与 OpenAI 价值 200 亿美元的交易已预分配了 Cerebras 近期几乎全部的推理容量，导致其 API 候补名单对小公司而言实际上无限长。 ASIC 推理容量集中在单一客户手中，可能抑制依赖快速专用硬件进行实时应用的 AI 初创公司的创新。 该初创公司需要持续高吞吐量推理，每秒 1-2k token，且要求 p95 延迟约束，Cerebras 的晶圆级 ASIC 非常适合提供这些性能，但因这笔交易而无法获得访问权限。

reddit · r/MachineLearning · /u/Kortopi-98 · 6月29日 12:00

**背景**: Cerebras 生产晶圆级 AI 芯片，因其高带宽和低延迟而在推理方面表现出色。ASIC（专用集成电路）在专用推理工作负载上比 GPU 更高效。OpenAI 的大规模订单消耗了 Cerebras 大部分产能，凸显了 AI 硬件领域日益增长的可访问性不平等。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Cerebras">Cerebras Systems - Wikipedia</a></li>
<li><a href="https://www.cerebras.ai/chip">Product - Chip - Cerebras</a></li>
<li><a href="https://medium.com/@danny_54172/asic-inference-vs-non-inference-ai-chips-a5f1a5f05183">ASIC Inference vs. Non-Inference AI Chips | by Danny H Lee | Medium</a></li>

</ul>
</details>

**社区讨论**: 社区评论表达了对该交易影响小企业的沮丧，有人提出这种集中可能引发反垄断担忧，另一些人则讨论初创公司是否应转向替代硬件或自建基础设施。

**标签**: `#AI Hardware`, `#Inference`, `#Startup Challenges`, `#Cerebras`, `#OpenAI`

---

<a id="item-8"></a>
## [谷歌 AI 同行评审在 ICML/STOC 处理约 1 万篇论文](https://www.reddit.com/r/MachineLearning/comments/1uio9rb/googles_agentic_peerreviewer_handled_10k_papers/) ⭐️ 8.0/10

谷歌部署了一个代理型 AI 系统，在 ICML 和 STOC 会议上对约 1 万篇论文进行同行评审，每篇论文只需 30 分钟，比零样本提示多发现 34%的数学错误。详细介绍该系统的正式研究论文现已发布在 arXiv 上。 这展示了 AI 在大规模科学同行评审中的重大实际应用，可能减轻评审者负担并提高错误检测能力。它为顶级会议中的 AI 辅助评审树立了先例，可能改变研究验证和发表的方式。 该系统是代理型的，意味着它可以自主阅读论文、识别数学错误并提供反馈，无需人工干预。与零样本提示（模型没有任何示例的基线方法）相比，它在发现数学错误方面提高了 34%。

reddit · r/MachineLearning · /u/Justgototheeffinmoon · 6月29日 10:05

**背景**: 代理型 AI 指的是能够自主感知、推理并采取行动以实现特定目标的系统，通常使用大语言模型。零样本提示是一种技术，模型在没有先前示例的情况下执行任务。ICML 和 STOC 分别是机器学习和理论计算机科学领域的顶级会议。同行评审对于确保研究质量至关重要，但往往耗时且劳动密集。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/AI_agent">AI agent - Wikipedia</a></li>
<li><a href="https://mitsloan.mit.edu/ideas-made-to-matter/agentic-ai-explained">Agentic AI, explained | MIT Sloan</a></li>
<li><a href="https://en.wikipedia.org/wiki/Zero-shot_prompting">Zero-shot prompting</a></li>

</ul>
</details>

**标签**: `#AI`, `#peer review`, `#research automation`, `#machine learning`

---

<a id="item-9"></a>
## [EML 树被证明是通用逼近器](https://www.reddit.com/r/MachineLearning/comments/1uipl1t/eml_trees_are_universal_approximators_r/) ⭐️ 8.0/10

一篇新论文证明了 EML 树（一种初等函数的组合表示）是连续函数和 Sobolev 空间的通用逼近器，并通过类似乐高积木的方式给出了显式构造。 该结果将 EML 树确立为函数逼近的一个有理论基础框架，可能提供一种具有显式可解释性和保证逼近能力的神经网络替代方案。 证明包括二元运算、多项式、双曲正切和近似单位分割的显式 EML 类型表示。作者还提出了一种带拟合参数的 EML 类型树的学习算法，并在实际优化问题上展示了其可行性。

reddit · r/MachineLearning · /u/JoeGermany · 6月29日 11:16

**背景**: 通用逼近定理是机器学习中的基础结果，表明具有足够宽度或深度的神经网络可以逼近任何连续函数。EML（初等数学语言）树通过组合初等函数（如 sin、exp、log）来表示复杂函数。该工作扩展了这一思想，证明了此类组合可以逼近更广泛的函数类别，而不仅仅是初等函数。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/2606.23179">[2606.23179] EML Trees Are Universal Approximators</a></li>
<li><a href="https://en.wikipedia.org/wiki/Universal_approximation_theorem">Universal approximation theorem</a></li>

</ul>
</details>

**标签**: `#universal approximation`, `#EML trees`, `#function approximation`, `#machine learning theory`

---

<a id="item-10"></a>
## [长鑫存储与腾讯签订近 30 亿美元 DRAM 协议](https://www.reuters.com/world/china/chinas-cxmt-wins-3-billion-memory-supply-deal-with-tencent-sources-say-2026-06-29/) ⭐️ 8.0/10

长鑫存储（CXMT）与腾讯签署了一项价值超过 200 亿元人民币（约 29.4 亿美元）的长期 DRAM 内存芯片供应协议，覆盖数年服务器供货。 这是中国内存芯片领域最大规模的交易之一，标志着半导体供应链国产替代的加速，并增强了腾讯在云服务和 AI 工作负载方面的服务器能力。 据消息人士透露，协议期限为三至五年。传闻长鑫存储还在与其他中国互联网公司谈判，包括阿里云、字节跳动和小米。

telegram · zaihuapd · 6月29日 09:31

**背景**: DRAM（动态随机存取存储器）是一种用于服务器、个人电脑和消费电子产品的易失性存储器。长鑫存储是中国领先的 DRAM 制造商，近期已开始大规模生产 DDR5 和 LPDDR5X 芯片。该交易有助于减少中国对外国内存供应商（如三星和 SK 海力士）的依赖。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.gys.cn/jichengdianluic/5510051897.html">CXMR4E832S6AS-AN1C 长 鑫 （ CXMT ） 存 储 芯片 应用：笔记本电脑</a></li>
<li><a href="https://www.chinaflashmarket.com/Producer/CXMT">长 鑫 存 储 _厂商主页_CFM闪 存 市场</a></li>

</ul>
</details>

**标签**: `#DRAM`, `#半导体`, `#供应链`, `#长鑫存储`, `#腾讯`

---

<a id="item-11"></a>
## [特斯拉 FSD v14 Lite：HW3 车型获得 HW4 级能力](https://x.com/Tesla_AI/status/2071592820889260101) ⭐️ 8.0/10

特斯拉于 2026 年 6 月 29 日发布 FSD v14 Lite，通过将 HW4 神经网络压缩至约 15%大小，使 HW3 车型获得强化学习、改进的驾驶行为及首次引入的停车功能。 此次更新大幅延长了旧款 HW3 车型的使用寿命，无需硬件升级即可获得接近 HW4 的自动驾驶能力，并为汽车人工智能中的知识蒸馏开创了先例。 蒸馏后的神经网络运行于固件版本 2026.20.5.1，首先向早期测试用户推送。更新包括改进的导航、并线、行人交互，以及新增的路边停车、出库和倒车功能。

telegram · zaihuapd · 6月30日 02:26

**背景**: HW3（硬件 3）是特斯拉 2019 年推出的首款定制全自动驾驶计算机，采用 14 纳米芯片，内存相比 2023 年推出的 HW4 更小。知识蒸馏是一种技术，其中大型'教师'模型（HW4）训练小型'学生'模型（HW3）模仿其行为，从而在受限硬件上实现高级功能。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.notateslaapp.com/news/4369/tesla-launches-fsd-v14-lite-first-impressions">Tesla Launches FSD V 14 - Lite : First Impressions - Not a Tesla App</a></li>
<li><a href="https://electrek.co/2026/06/29/tesla-fsd-v14-lite-hw3-rollout/">Tesla starts FSD v 14 ' Lite ' rollout to HW3 cars | Electrek</a></li>
<li><a href="https://en.wikipedia.org/wiki/Tesla_Autopilot_hardware">Tesla Autopilot hardware - Wikipedia</a></li>

</ul>
</details>

**标签**: `#Tesla`, `#FSD`, `#autonomous driving`, `#HW3`, `#HW4`

---