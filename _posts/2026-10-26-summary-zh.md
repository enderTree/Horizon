---
layout: default
title: "Horizon Summary: 2026-10-26 (ZH)"
date: 2026-10-26
lang: zh
---

> 从 31 条内容中筛选出 1 条重要资讯。

---

1. [OpenAI 与 Anthropic 数月内将大模型价格最高下调 80%，竞争白热化](#item-1) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [OpenAI 与 Anthropic 数月内将大模型价格最高下调 80%，竞争白热化](https://minimaxir.com/2026/10/cheap-llms/) ⭐️ 8.0/10

过去几个月里，OpenAI 与 Anthropic 将其大语言模型 API 的价格最高下调了 80%，这一系列快速降价被一篇广受讨论的博客文章记录下来。降价直接影响开发者调用旗舰模型时按 token 支付的费用，从而显著降低了在其之上构建应用的成本。 价格是决定 AI 普及程度的最关键因素，80% 的降幅可以让此前不划算的用例——高频调用的智能体、批量文档处理、常驻助手——变成可行的产品。这也说明前沿实验室不再认为定价权是理所当然的，从而迫使整个市场（包括云厂商和中小模型供应商）不得不在成本而非仅仅能力上展开竞争。 业内普遍将降价归因于三股力量：更好的硬件利用率和推理服务优化带来的单位推理成本下降、来自 DeepSeek、Kimi、GLM 等低价开源权重模型的竞争压力，以及在开发者流失前将其锁定的意图。但也要注意几点：标价并不等于实际价格，缓存、批处理折扣和批量合同早已压低了真实成本；而且据报道两家公司仍处于数十亿美元亏损状态，因此利润率依然不明朗。

hackernews · minimaxir · 10月25日 21:11 · [社区讨论](https://news.ycombinator.com/item?id=50236102)

**背景**: 推理成本是指模型在训练完成后每次生成输出（如聊天回复、代码补全、图像）时供应商所需支付的费用，其主体是 GPU 计算时间，因此吞吐量和利用率与硬件的标价同样重要。开放权重模型会公开发布训练好的参数，任何人都可以下载并自行部署，这就为闭源 API 供应商的定价设下了硬性上限，因为客户随时可以换成本地运行的模型。推理成本下降与可用的开放权重替代品两者叠加，使得大幅降价成为一种理性的防御举措，而非单纯的慷慨。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://amnic.com/blogs/what-is-inference-cost">What Is Inference Cost ? AI 's Biggest Ongoing Bill - Amnic</a></li>
<li><a href="https://www.n-ix.com/open-weight-ai-models/">Open - weight AI models : What, why, and how to deploy them... - N-iX</a></li>
<li><a href="https://claw-ai.co/en/learn/what-are-open-weight-models">What are open - weight models ? | ClawAI</a></li>

</ul>
</details>

**社区讨论**: 评论者普遍认同竞争——尤其是来自中国开放权重模型的竞争——是主要推手，不少人表示在遭遇 OpenAI 与 Anthropic 的拒绝或封锁后转向了 Kimi 或 GLM。另一种更悲观的看法反复出现：这些实验室正通过企业合同、消费级智能体和监管俘获来构筑护城河，有人甚至认为推动监管的部分目的就是排挤中国的开放模型。也有人反驳“亏损源于研发与规模化投入”的说法，认为根本问题在于大模型商业模式本身尚不成立；还有评论者引用 DeepSeek 披露的每 GPU 每小时约 38 美元收入数据，认为现有厂商仍有相当大的降价空间。

**标签**: `#LLM pricing`, `#OpenAI`, `#Anthropic`, `#AI competition`, `#inference costs`

---