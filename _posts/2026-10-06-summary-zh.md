---
layout: default
title: "Horizon Summary: 2026-10-06 (ZH)"
date: 2026-10-06
lang: zh
---

> 从 33 条内容中筛选出 2 条重要资讯。

---

1. [Reflection 发布 Beam：501B 参数开源稀疏 MoE 模型](#item-1) ⭐️ 8.0/10
2. [Sona：单个 Transformer 在 A/B 测试中取代 Yandex Music 的 15+ 组件推荐系统](#item-2) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Reflection 发布 Beam：501B 参数开源稀疏 MoE 模型](https://reflection.ai/blog/introducing-beam) ⭐️ 8.0/10

Reflection 发布了 Beam，这是一个开放权重的稀疏混合专家（MoE）模型，总参数量 5010 亿、激活参数 230 亿，专门面向编程、推理和智能体（agentic）任务。该模型在 23.8 万亿条经过筛选的网页与授权数据 token 上完成预训练，并投入大规模强化学习进行后训练，Reflection 称其表现可匹敌甚至超过同规模的开源基础模型。 5010 亿总参数、230 亿激活参数的开放权重模型，加上在预训练和强化学习上的重金投入，意味着又一款接近前沿水平的模型进入可下载生态，让研究者和企业可以在编程与智能体流程中自托管，而不必完全依赖闭源 API。这也让各大实验室围绕大规模稀疏 MoE 权重开放的开源与闭源之争进一步升温。 Beam 的 230 亿激活参数意味着其推理成本远低于 5010 亿总参数量所暗示的水平，这正是稀疏 MoE 架构的典型特征。值得注意的是，社区对比指出 Beam 不含任何 n-gram/PLE 参数，而同量级的另一款模型 DeepSeek V4.1 Flash 据称使用了 1960 亿这类参数；此外 Beam 主打的泛化能力证据是在一个“病毒式传播的 X 拼图”网格任务上取得 95.5% 覆盖率，位于 Opus 5（92.5%）与另一模型之间。

hackernews · Philpax · 10月5日 19:16 · [社区讨论](https://news.ycombinator.com/item?id=49969183)

**背景**: 混合专家（MoE）模型用多个独立的“专家”子网络取代部分稠密前馈层，并由路由器为每个 token 只激活其中一小部分，因此模型可以拥有庞大的总参数量，而单次推理只用到其中一小部分。所谓“开放权重”指训练好的参数被公开发布，任何人都能下载、检查、运行或微调，但训练数据和代码未必开源。强化学习后训练如今已成为前沿实验室在大规模语料预训练之后，用来打磨推理与智能体能力的主流手段。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.analyticsvidhya.com/blog/2025/04/open-weight-models/">What are Open Source and Open Weight Models ? | Analytics Vidhya</a></li>
<li><a href="https://mbrenndoerfer.com/writing/mixtral-8x7b-sparse-mixture-of-experts-architecture">Mixtral 8x7B: Sparse Mixture of Experts Architecture - Interactive</a></li>
<li><a href="https://magazine.sebastianraschka.com/p/the-state-of-llm-reasoning-model-training">The State of Reinforcement Learning for LLM Reasoning</a></li>

</ul>
</details>

**社区讨论**: 社区总体欢迎又一款开放权重模型，但对基准宣传持怀疑态度：有评论者特别指出“病毒式 X 拼图”演示图注，质疑 95.5% 的网格覆盖率究竟能证明多少泛化能力。也有人讨论架构路线，追问为何较新的开放权重模型似乎放弃了 n-gram/SSD 检索方案，而这类方案曾被视为利用存储低成本扩充知识的途径；还有评论者贴出与 DeepSeek V4.1 Flash 的参数量对照，显示 Beam 激活参数更多但完全没有 n-gram/PLE 参数。

**标签**: `#open-weight-models`, `#mixture-of-experts`, `#llm-release`, `#reinforcement-learning`, `#ai-research`

---

<a id="item-2"></a>
## [Sona：单个 Transformer 在 A/B 测试中取代 Yandex Music 的 15+ 组件推荐系统](https://www.reddit.com/r/MachineLearning/comments/1wy4qxm/sona_one_transformer_replaced_our_15_candidate/) ⭐️ 8.0/10

Yandex Music 推出了 Sona，用一个单一的 Transformer 在一次 A/B 测试中替代了其整个生产推荐流水线——包括 15 个以上的候选生成器、预排序模型和排序模型。在智能音箱场景下，为期 7 天、每组 15% 用户的 A/B 测试中，Sona 相比生产对照组取得 +4.53% 活跃用户和 +6.30% 总收听时长，两者均在 p < 0.01 水平上显著。 它提供了生产规模的证据，证明单个端到端生成式模型可以吞并多年来主导工业级推荐系统的“候选生成 / 预排序 / 排序”多阶段架构，与基于大语言模型的系统所呈现的整合趋势相呼应。如果这一结论可推广，推荐团队有望大幅削减流水线复杂度、特征工程和线上服务基础设施。 Sona 最多读取 8,192 个事件，但由于该长度下的全注意力开销过高，它采用了所谓“历史压缩”：将历史切分为较早的 6,144 个事件和最近的 2,048 个事件，两个块通过交叉注意力以及一层全历史自注意力交换信息，随后仅对最近的 2,048 个事件运行一个 7 层堆叠，从而将推理成本大约减半，同时保留了全注意力的大部分质量。候选项由束搜索以语义 ID 的形式产出并立即打分，编码器的输出同时供解码器和排序模块使用，因此编码器每次请求只运行一次；其目录覆盖率低于生产流水线，模型尚未全量上线，长期 A/B 测试正在进行中。

reddit · r/MachineLearning · /u/SettingAccording8986 · 10月5日 10:07

**背景**: 工业级推荐系统通常被组织成漏斗结构：多个候选生成器（每个都是如双塔网络这样的专用召回模型）先从海量目录中低成本地筛出成千上万个可能相关的物品，再由预排序模型缩小范围，最后由更重的排序模型利用数百个特征对幸存项打分。Transformer 最初为序列建模而提出，如今是大语言模型的骨干，它通过注意力机制让序列中每个位置都能关注其他所有位置，效果强大但随序列长度增长开销急剧上升。近年来的生成式推荐器借鉴大语言模型的思路，直接由解码器输出物品标识符（通常是“语义 ID”），而 Sona 要验证的正是这种单模型方案能否在音乐推荐中取代整个漏斗。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.linkedin.com/pulse/candidate-generators-recommender-systems-mikhail-shakhray-9f3tf">Candidate generators / recommender systems</a></li>
<li><a href="https://aman.ai/recsys/ranking/">Aman's AI Journal • Recommendation Systems • Ranking/Scoring</a></li>
<li><a href="https://en.wikipedia.org/wiki/Transformer_(deep_learning)">Transformer (deep learning) - Wikipedia</a></li>

</ul>
</details>

**标签**: `#recommender systems`, `#transformers`, `#production ML`, `#ranking`, `#A/B testing`

---