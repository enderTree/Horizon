---
layout: default
title: "Horizon Summary: 2026-10-05 (ZH)"
date: 2026-10-05
lang: zh
---

> 从 24 条内容中筛选出 4 条重要资讯。

---

1. [苹果新 CEO 特努斯推动提速与精简组织改革](#item-1) ⭐️ 9.0/10
2. [Strata 在单张 RTX 4090 上以 100+ tokens/s 运行 125B 的 Qwen 3.8 Flash Next](#item-2) ⭐️ 8.0/10
3. [ARC-AGI-3 的 Kaggle 最高分据称在 30 天内从 7% 跃升至 56%](#item-3) ⭐️ 8.0/10
4. [SK 电信就大规模数据泄露致歉，为全体用户免费更换 USIM 卡](#item-4) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [苹果新 CEO 特努斯推动提速与精简组织改革](https://t.me/zaihuapd/44211) ⭐️ 9.0/10

上任数周后，苹果新任 CEO 约翰·特努斯已开始推动公司改革，目标是加快产品开发、扩大产品线，并让组织更精简、更加聚焦工程。据彭博社和路透社报道，苹果正考虑减少对春季、秋季固定发布节奏的依赖，让新品在全年更灵活地推出；同时精简部分中层管理岗位，缩短工程团队与高层之间的决策链条，并在寻找新的收入来源、探索如何从现有产品中获取更多收入。 这是科技行业最重大的领导层更替之一：在竞争对手纷纷由软件和 AI 专家掌舵之时，苹果却把 CEO 之位交给了一位硬件工程师。如果特努斯成功打破春季、秋季固定发布的刚性节奏，将重塑苹果供应链、开发者和消费者的产品规划方式，并释放出向硬件执行力和工程驱动决策倾斜的战略信号。 据报道，改革内容包括削减部分中层管理岗位、缩短工程团队与高层之间的沟通路径，并探索从既有用户群中获得更多收入，而不是单纯依赖新硬件。放弃固定春秋发布窗口目前仍处于“考虑”阶段而非最终定案，因此新品时间表对开发者和零售伙伴而言仍存在不确定性。

telegram · zaihuapd · 10月4日 15:03

**背景**: 约翰·特努斯于 2001 年加入苹果产品设计团队，2013 年成为硬件工程副总裁，2021 年进入高管团队并担任硬件工程高级副总裁，负责 iPhone、iPad、Mac、AirPods 等产品线。他从蒂姆·库克手中接任 CEO，而库克时代以卓越的运营能力和高度规律的年度发布节奏著称。苹果习惯把重要产品发布锚定在春季和秋季，这一节奏影响了从供应链规划到应用与外设生态的季节性规律，因此任何改动都会在整个行业产生连锁反应。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://news.qq.com/rain/a/20260901A0ABT600">Tim Cook卸任苹果首席执行官一职， John Ternus ...</a></li>
<li><a href="https://global.hk01.com/数码生活/60343373/apple新ceo-john-ternus是谁-曾为一颗螺丝跟同事吵翻的细节狂魔">Apple 新CEO John Ternus 是谁？ 曾为一颗螺丝跟同事吵翻的细节狂魔</a></li>
<li><a href="https://today.line.me/tw/v3/article/vXOLpp3">Tim Cook交棒！ Apple 硬 體 工 程 資深 副 總 裁 John Ternus 將接任CEO</a></li>

</ul>
</details>

**标签**: `#Apple`, `#CEO transition`, `#organizational restructuring`, `#product strategy`, `#tech industry`

---

<a id="item-2"></a>
## [Strata 在单张 RTX 4090 上以 100+ tokens/s 运行 125B 的 Qwen 3.8 Flash Next](https://github.com/Niko1221/Strata) ⭐️ 8.0/10

开源项目 Strata（GitHub：Niko1221/Strata）展示了如何在单张消费级 RTX 4090 上以超过 100 tokens/s 的速度运行 125B 参数的 Qwen 3.8 Flash Next 模型。社区成员很快复现了该结果：在配备 128GB DDR5 和 Ryzen 7950X3D 的 4090 机器上达到 124 tokens/s，而在单张 24GB RTX 5090 加约 40GB 系统内存、使用 UD-IQ4_XS（约 4-bit）GGUF 量化时约为 62 tokens/s。 在一块仅需几千美元的消费级显卡上交互式运行 100B 级别的开源权重模型，而非租用数据中心 GPU，显著降低了本地、私密、离线推理的门槛。与此同时，这次讨论也表明社区越来越不满足于单纯的 tokens/s 数字，而是要求在认可这类优化之前同时给出准确率、能耗和长上下文等方面的测量结果。 该方法依赖低位宽 GGUF 量化（约 4-bit 及更低）并配合大容量系统内存进行权重卸载，因此性能瓶颈在内存带宽而非算力。一位用户做的 50 张图像坐标预测基准显示，Strata 的中位误差为 154.8 像素，而相同 GGUF 权重与视觉适配器在 llama.cpp 上的中位误差仅为 46.5 像素，这是速度提升可能以视觉任务精度下降为代价的具体证据。

hackernews · snehesht · 10月4日 12:51 · [社区讨论](https://news.ycombinator.com/item?id=49953495)

**背景**: 量化是一种模型压缩技术，它把模型的权重（有时还包括激活值）从 FP16、BF16 等高精度格式转换为 4-bit 整数等低精度表示，可将硬件需求降低最多约 80%，代价是损失一部分质量。正是量化让超大模型能够塞进 RTX 4090 这类消费级显卡的 24GB 显存，其余权重则从系统内存流式加载。Qwen 3.8 Flash Next 是阿里 Qwen 团队发布的 125B 参数模型，其官方 Hugging Face 发布页以及本地运行指南（例如 Unsloth 的文档）让人们能够在发布当天就展开实验。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/Qwen/Qwen3.8-Flash-Next">Qwen / Qwen 3 . 8 - Flash - Next · Hugging Face</a></li>
<li><a href="https://unsloth.ai/docs/models/qwen3.8-next">Qwen 3 . 8 - Flash - Next : How to Run Locally | Unsloth Documentation</a></li>
<li><a href="https://www.datacamp.com/tutorial/quantization-for-large-language-models">Quantization for Large Language Models (LLMs): Reduce... | DataCamp</a></li>

</ul>
</details>

**社区讨论**: 讨论情绪是真实的兴奋与方法论上的怀疑并存。多位用户报告了不错的实际表现（4090 上 124 tokens/s；5090 上约 62 tokens/s，且约 4-bit 量化在编码和代码重构任务上“完全够用”），但也有人质疑这种性能能否在固定任务套件下经受住准确率、能耗、长上下文行为和多次运行波动的检验，并警告低于 4-bit 会带来明显的质量退化。最有力的反证是一项独立视觉基准，在相同权重下 Strata 的误差约为 llama.cpp 的三倍。

**标签**: `#LLM inference`, `#quantization`, `#consumer hardware`, `#Qwen`, `#performance optimization`

---

<a id="item-3"></a>
## [ARC-AGI-3 的 Kaggle 最高分据称在 30 天内从 7% 跃升至 56%](https://www.reddit.com/r/MachineLearning/comments/1wxcd4k/top_arc%CE%B1gi3_scores_on_kaggle_just_went_from_7_to/) ⭐️ 8.0/10

r/MachineLearning 上的一篇帖子称，ARC Prize 基金会推出的交互式推理基准 ARC-AGI-3 的 Kaggle 排行榜最高分在过去 30 天内从约 7% 上升到约 56%。据称这些提升是由运行在 harness（评测框架）中的小型本地模型实现的，因为 Kaggle 比赛规则只允许参赛者使用可在本地运行的模型，而非前沿的 API 系统。 ARC-AGI 已成为衡量通用推理能力进展最受关注的指标之一，而 ARC-AGI-3 的设计初衷正是让人类表现优于机器——它要求智能体自主探索陌生环境并即时学习目标。如果这一跃升经得起检验，就意味着「工程脚手架 + 中等规模开源模型」能够弥合此前被视为人类优越性标志的差距，从而改变社区对 AGI 基准进展的解读方式。 该说法仅基于一篇 Reddit 帖子，发帖者本人也承认所附的排行榜截图略有滞后，而且这些分数在很大程度上取决于模型外层的 harness 与脚手架，而非模型本身的原始能力。由于这只是排行榜结果而非经过同行评审的评测，随着榜单更新数字可能变化，应将其视为社区可见的信号，而非已被确认的能力突破。

reddit · r/MachineLearning · /u/we_are_mammals · 10月4日 10:24 · [社区讨论](https://www.reddit.com/r/MachineLearning/comments/1wxcd4k/top_arcαgi3_scores_on_kaggle_just_went_from_7_to/)

**背景**: ARC-AGI（Abstraction and Reasoning Corpus for AGI）是 ARC Prize 基金会推出的一系列基准，旨在衡量流动智力与通用推理能力，而非记忆性知识；早期版本（ARC-AGI-1 与 ARC-AGI-2）测试的是被动的谜题求解，而 ARC-AGI-3 将任务变为交互式的：智能体必须执行动作、获得反馈、构建世界模型，并适应陌生的游戏机制。在 ARC-AGI-3 上取得 100% 意味着智能体能像人类一样高效通关所有游戏。评测 harness（评测框架）是让模型跑完基准、施加提示与工具调用并给出评分的标准化基础设施，因此 harness 的设计会显著影响所报告的分数。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arcprize.org/arc-agi/3">ARC-AGI-3</a></li>
<li><a href="https://arcprize.org/leaderboard">ARC-AGI-3 Leaderboard - ARC Prize</a></li>
<li><a href="https://arize.com/blog/what-is-an-evaluation-harness/">What is an evaluation harness ? Definition & guide - Arize AI</a></li>

</ul>
</details>

**标签**: `#ARC-AGI`, `#benchmarks`, `#LLM-reasoning`, `#AGI`, `#Kaggle`

---

<a id="item-4"></a>
## [SK 电信就大规模数据泄露致歉，为全体用户免费更换 USIM 卡](https://t.me/zaihuapd/44206) ⭐️ 8.0/10

韩国最大移动运营商 SK 电信（SKT）确认其内部系统遭黑客攻击，核心 HSS 服务器被攻破，超过 2500 万用户的敏感数据外泄，涉及 IMEI、SN、ICCID、PIN2/PUK2、eID、加密 K 值和私钥等信息。事件发生后，SKT CEO 已公开致歉，并宣布为所有希望更换的 SKT 用户（含其网络下的 MVNO 用户，部分设备除外）免费更换 USIM 卡，同时为近期已付费更换的用户报销费用。 泄露的加密 K 值是用户在移动网络上进行身份认证的根密钥，一旦被利用，攻击者可能克隆 USIM 卡、冒充用户身份或截获通信内容。作为影响超过 2500 万人的国家级运营商核心基础设施泄露事件，它凸显了电信鉴权数据库是高价值攻击目标，也可能促使其他运营商加固 HSS 安全并加快 USIM 换卡计划。 此次外泄的数据集包括设备标识（IMEI、SN）、卡片标识（ICCID）、卡片解锁码（PIN2/PUK2）、eID，以及用于鉴权的加密 K 值和私钥。SKT 表示部分设备类型不在此次免费换卡范围内，并已紧急扩大响应规模；近期已自费更换 USIM 卡的用户可申请报销。

telegram · zaihuapd · 10月4日 09:02

**背景**: HSS（归属用户服务器）是 4G/LTE 与 5G 网络中的核心数据库，存储用户签约信息，并提供设备接入网络所需的鉴权与授权数据。每张 USIM 卡——即用于 3G 及之后网络的升级版 SIM 卡——都存有 ICCID 和一个保密的 K 值，K 值与运营商密钥共同构成整个网络加密体系的基础；由于 HSS 中保存着同样的 K 值副本，HSS 被攻破就直接威胁到卡片层面的安全。更换 USIM 卡会下发带有新 K 值的新卡片，这也是密钥疑似泄露时采取全国范围换卡这一标准补救措施的原因。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.p1sec.com/blog/home-subscriber-server-hss">Home Subscriber Server (HSS): The Backbone of Modern Telecom ...</a></li>
<li><a href="https://nickvsnetworking.com/hss-usim-authentication-in-lte-nr-4g-5g/">HSS & USIM Authentication in LTE/NR (4G & 5G) | Nick vs ...</a></li>
<li><a href="https://support.huawei.com/enterprise/en/doc/EDOC1000079719/2070a180/what-is-the-difference-between-sim-and-usim-cards">What Is the Difference Between SIM and USIM Cards? - AR ...</a></li>

</ul>
</details>

**标签**: `#cybersecurity`, `#data-breach`, `#telecom`, `#SKT`, `#USIM`

---