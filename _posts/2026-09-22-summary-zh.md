---
layout: default
title: "Horizon Summary: 2026-09-22 (ZH)"
date: 2026-09-22
lang: zh
---

> 从 37 条内容中筛选出 5 条重要资讯。

---

1. [小米发布 MiMo v2.6 开源 MoE 模型，并公开实时 RL 看板](#item-1) ⭐️ 8.0/10
2. [Bryan Cantrill 回顾 Sun Microsystems 究竟错在哪里](#item-2) ⭐️ 8.0/10
3. [SemiAnalysis 分析 MoE 推理中的计算与数据搬运](#item-3) ⭐️ 8.0/10
4. [苹果发布首款 2 纳米芯片 M6 与首款四芯片 M5 Ultra](#item-4) ⭐️ 8.0/10
5. [25 位菲尔兹奖得主警告：AI 或与数学研究目标错位](#item-5) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [小米发布 MiMo v2.6 开源 MoE 模型，并公开实时 RL 看板](https://mimo.xiaomi.com/mimo-v2-6) ⭐️ 8.0/10

9 月 22 日，小米 MiMo 团队发布并开源 MiMo-V2.6 系列，包含两个混合专家（MoE）变体：Flash 为 309B 总参数 / 15B 激活参数，Pro 为 1.02T 总参数 / 42B 激活参数。两款模型的 RL 版本权重已在 Hugging Face 上线（XiaomiMiMo/MiMo-V2.6-Flash-RL 与 MiMo-V2.6-Pro-RL），同时附带一份详细技术报告和一个公开的实时 RL 训练看板。 一家大型消费硬件公司放出约 1 万亿参数级别的开放权重模型，说明超大规模 MoE 训练不再局限于少数西方 AI 实验室，也会加大其他厂商公开模型后训练细节的压力。其异常开放的训练方法——包括直播式的强化学习看板——让研究者和工程实践者得以一窥大规模 RL 后训练在真实环境中的运行情况。 由于采用 MoE 架构，每个 token 只激活网络中的一小部分，因此 1.02T/42B 的 Pro 在推理时的实际计算量接近于一个小得多的稠密模型，但仍需存储完整的参数集合。训练看板还披露了出于安全考虑的具体决策，例如在 rollout 日志中观察到不良模式后，从接下来的 Pro 训练中移除了“cyber 数据集”；其对齐 RL 阶段采用冷启动方式，让模型反思并重写自身出现偏差的对话轮次。

hackernews · volf_ · 9月21日 20:12 · [社区讨论](https://news.ycombinator.com/item?id=49792730)

**背景**: 混合专家（MoE）是一种架构：由许多独立的子网络（即“专家”）分别擅长输入空间的不同部分，再由一个门控网络决定每个 token 交给哪些专家处理；这样模型可以拥有极多的参数，但每个 token 只用到其中一小部分计算。RLHF 类后训练（基于人类反馈的强化学习，如今常扩展为基于可验证奖励或 AI 生成奖励的强化学习）先训练一个奖励模型，再用它优化语言模型，使输出更符合指令与安全规范。“开放权重”指训练好的参数可被任何人下载和运行，但并不必然意味着训练数据和训练代码也一并公开——这正是社区经常争论的区分点。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/blog/moe">Mixture of Experts Explained</a></li>
<li><a href="https://en.wikipedia.org/wiki/Reinforcement_learning_from_human_feedback">Reinforcement learning from human feedback - Wikipedia</a></li>
<li><a href="https://cursor.com/blog/real-time-rl-for-composer">Improving Composer through real-time RL · Cursor</a></li>

</ul>
</details>

**社区讨论**: 评论者普遍赞赏小米的透明度，有人称实时 RL 看板是“极佳的学习与教学工具”，并认为技术报告异常详尽。也有人特别提到看板中“因 rollout 出现不良模式而从 Pro 训练中移除 cyber 数据集”的说明；还有评论者列出确切的参数规模并附上 Hugging Face 链接。讨论还延伸到地缘政治层面，争论美国在电力与电网上的瓶颈是否会让中国最终赢下 AI 竞赛，此外还有人对两款模型做了轻松的“鹈鹕”渲染测试。

**标签**: `#LLM`, `#open-weights`, `#Mixture-of-Experts`, `#RLHF`, `#Xiaomi`

---

<a id="item-2"></a>
## [Bryan Cantrill 回顾 Sun Microsystems 究竟错在哪里](https://bcantrill.dtrace.org/2026/09/20/what-sun-got-wrong/) ⭐️ 8.0/10

前 Sun Microsystems 工程师、DTrace 主要作者之一 Bryan Cantrill 在其博客上发表了一篇题为《What Sun got wrong》（Sun 错在哪里）的新文章，剖析了导致这家公司衰落的一系列战略与技术失误。文章以亲历者视角把工程史与商业分析结合起来，很快在社区引发大规模讨论（531 分、311 条评论）。 Sun 的衰落至今仍是计算机史上最具教育意义的失败案例之一：一家拥有世界级工程能力的公司，最终仍然败给了更廉价的标准硬件和市场环境的变化。对今天的工程师和创业者——尤其是身处当前 AI 基础设施热潮中的人——这篇文章是一堂关于“仅有技术卓越并不足以保证商业生存”的案例课。 这篇文章并非第三方史书，而是由亲历 Sun 衰落的内部人士撰写，因此在工程与组织两个层面都具备少见的可信度。围绕该文的讨论还点出了若干具体决策，例如 Sun 在 2002 年一度取消 Solaris 的 x86 版本，以及同年未能与 Google 达成交易，评论者普遍把这些视为命运的转折点。

hackernews · chmaynard · 9月21日 14:03 · [社区讨论](https://news.ycombinator.com/item?id=49787436)

**背景**: Sun Microsystems 是 20 世纪 80 至 90 年代计算机行业的中坚力量，销售基于自研 SPARC 处理器和 Solaris 操作系统的高端 Unix 工作站与服务器，并创造了 Java。它那种垂直整合、价格高昂的专有硬件模式，被运行 Linux 的廉价 x86 服务器所冲击，互联网泡沫破裂后公司营收急剧下滑。2010 年 Oracle 收购了 Sun，该公司作为独立企业的历史就此终结。

**社区讨论**: 评论者大体认同文章的判断，同时补充了各自的亲身经历并进一步深化了论点。有人回忆 Sun 冗长痛苦的采购流程，与 Dell 次日送达的标准服务器形成鲜明对比；有人列举具体失误，如取消 Solaris 的 x86 版本、未能与 Google 达成交易；还有评论者认为 Sun 从来就没有真正对“经营企业”感兴趣——它首先是打造出色的技术，做销售只是为了给技术输血。

**标签**: `#Sun Microsystems`, `#tech history`, `#business strategy`, `#software engineering`, `#retrospective`

---

<a id="item-3"></a>
## [SemiAnalysis 分析 MoE 推理中的计算与数据搬运](https://newsletter.semianalysis.com/p/computation-and-data-movement-for) ⭐️ 8.0/10

SemiAnalysis 发布了题为《Computation and Data Movement for Inference》的技术分析，探讨如何将混合专家（MoE）模型的结构与数据流映射到推理硬件上以实现高效服务。文章围绕模型结构、数据流动方式，以及这对构建高效推理系统的意义展开论述。 MoE 已成为当前大多数前沿大模型的主流架构，因此这类稀疏模型如何映射到加速器上，直接决定了部署方或采购方的服务成本、延迟与吞吐。随着行业瓶颈从单纯的算力（FLOPs）转向内存带宽和互连，这类系统层面的分析会影响硬件路线图与数据中心设计。 由于每个 token 只激活一小部分专家，MoE 推理的瓶颈通常在于内存容量、内存带宽，以及把 token 分发到对应专家所需的 all-to-all 通信，而非单纯的矩阵乘吞吐。完整分析对结构、数据流与服务效率有更深入的讨论，但受限于简短的摘录，这里无法逐一核实其中的实测细节。

rss · Semianalysis · 9月21日 18:14

**背景**: 混合专家（MoE）用多个并行的“专家”网络取代了稠密 Transformer 中单一的 前馈网络，并加入一个路由器，将每个 token 只分发给得分最高的少数几个专家，因此模型可以拥有极大的总参数量，而每个 token 只激活其中一小部分。这种稀疏性降低了单 token 的计算量，却把服务变成了一个分布式系统问题：专家通常分散在多块 GPU 上（专家并行），token 需要在它们之间路由，于是数据搬运成为首要考量。SemiAnalysis 是半导体与 AI 基础设施领域广受关注的研究媒体，NVIDIA 也持类似观点，认为当今大多数前沿模型都建立在 MoE 之上。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://developer.nvidia.com/blog/mastering-llm-techniques-inference-optimization/">Mastering LLM Techniques: Inference Optimization</a></li>
<li><a href="https://arxiv.org/pdf/2404.14294">A Survey on Efficient Inference for Large</a></li>
<li><a href="https://hal.science/hal-05113196v1/document">A Survey of Mixture of Experts Models : Architectures and...</a></li>

</ul>
</details>

**标签**: `#MoE`, `#Inference`, `#AI Hardware`, `#Systems Engineering`, `#LLM Serving`

---

<a id="item-4"></a>
## [苹果发布首款 2 纳米芯片 M6 与首款四芯片 M5 Ultra](https://t.me/zaihuapd/43965) ⭐️ 8.0/10

苹果正式发布 M6 芯片，这是其首款采用 2 纳米制程的芯片，首发于新款 Mac mini，配备 12 核 CPU、12 核 GPU、双 16 核神经网络引擎，统一内存带宽最高达 170GB/s。同时苹果在新款 Mac Studio 中推出 M5 Ultra，这是 M 系列首款四芯片（quad-die）架构芯片，最高 36 核 CPU、80 核 GPU、512GB 统一内存，内存带宽高达 1.2TB/s。 这是一次双重代际跨越：转向 2 纳米节点有望为日常 Mac 带来明显更好的每瓦性能，而四芯片的 M5 Ultra 则把 Apple Silicon 推向工作站级别——其内存容量与带宽此前只有高端独立 GPU 和服务器 CPU 才具备。直接受益者是需要本地运行 AI 模型、视频与 3D 渲染管线以及超大数据集内存驻留的开发者；同时，2 纳米芯片的首发也说明最先进制程产能已进入大规模量产产品。 苹果称 M5 Ultra 的 1.2TB/s 统一内存带宽比 M3 Ultra 高出 50%，四芯片布局依靠升级版 UltraFusion 互连技术，将两颗双芯片的 M5 Max 连接而成。需要注意的是，该消息来源只是一段简短摘要，没有跑分、价格、上市时间或第三方性能验证；而“2 纳米”是工艺节点的营销名称，并不对应任何单一物理尺寸。

telegram · zaihuapd · 9月21日 16:32

**背景**: 在芯片制造中，“2 纳米”这类工艺节点（继 3 纳米之后的一代）只是一个制程代际的名称，节点越小通常意味着晶体管密度越高，从而在更低功耗下获得更强性能。苹果的 Ultra 芯片是通过 UltraFusion 互连把两颗 Max 级芯片封装在一起，因此“四芯片”M5 Ultra 实际上是两个 M5 Max 封装拼合而成的单颗 SoC。所谓“统一内存”是指 CPU、GPU 与神经网络引擎共享同一块封装内 LPDDR5X 内存，而不再区分系统内存与显存，因此文中给出的带宽数字决定了这些计算单元读取数据的理论上限。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/2_nm_process">2 nm process - Wikipedia</a></li>
<li><a href="https://applescoop.org/story/m5-ultra-quad-die-architecture-explained">M5 Ultra Explained: How Apple’s First Quad - Die Chip Actually Works</a></li>
<li><a href="https://www.macobserver.com/news/apple-unveils-m6-and-m5-ultra-chips-with-huge-cpu-gpu-and-ai-upgrades/">Apple Unveils M6 and M5 Ultra Chips With Huge CPU, GPU and AI...</a></li>

</ul>
</details>

**标签**: `#apple-silicon`, `#hardware`, `#chips`, `#semiconductor`, `#2nm-process`

---

<a id="item-5"></a>
## [25 位菲尔兹奖得主警告：AI 或与数学研究目标错位](https://t.me/zaihuapd/43973) ⭐️ 8.0/10

由陶哲轩、邓煜等 25 位数学家（报道称签名者为菲尔兹奖得主）联署发表的一份声明警告称，将 AI 快速用于解决数学问题，可能导致 AI 的发展目标与数学研究的目标出现“严重错位”。签名者认为，把“解数学题”当作衡量 AI 能力的基准，可能损害数学研究本身以及整个学术生态。 这是数学界一批最具声望的学者罕见地联合发声，而时机恰逢各大 AI 实验室越来越频繁地以数学基准分数来证明模型推理能力的进步。这意味着数学研究共同体可能会对“如何衡量、奖励和发表 AI 在数学上的成果”提出异议，从而影响 AI 开发者、期刊、高校与资助机构。 声明强调，数学研究的核心在于形成概念性理解与新的洞见，而不仅仅是得到答案；并警告 AI 批量生成成果可能压缩用于验证、交流以及引用前人成果的时间，同时引发署名与抄袭等问题。声明同时也承认，AI 确实有望提升数学研究效率，最终影响取决于人们如何使用这项技术。

telegram · zaihuapd · 9月22日 03:00

**背景**: 菲尔兹奖由国际数学联盟每四年颁发一次，授予不超过四位 40 岁及以下的数学家，被普遍视为数学领域的最高荣誉；声明署名人之一陶哲轩于 2006 年获奖。近年来，大型语言模型在解决数学问题上的能力显著提升，使得数学竞赛题和公开难题成为衡量 AI 推理能力的热门标尺。但在数学中，一项结果只有在其他研究者完成验证、展开讨论并正确标注其依据的前人工作之后，才会真正成为被学界接受的知识，而这些环节既缓慢又高度依赖人力。

**标签**: `#AI`, `#mathematics`, `#research ethics`, `#large language models`, `#academic publishing`

---