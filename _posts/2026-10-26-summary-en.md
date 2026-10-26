---
layout: default
title: "Horizon Summary: 2026-10-26 (EN)"
date: 2026-10-26
lang: en
---

> From 31 items, 1 important content pieces were selected

---

1. [OpenAI and Anthropic Slash LLM Prices by Up to 80% as Competition Intensifies](#item-1) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [OpenAI and Anthropic Slash LLM Prices by Up to 80% as Competition Intensifies](https://minimaxir.com/2026/10/cheap-llms/) ⭐️ 8.0/10

Over the past few months, OpenAI and Anthropic have cut the prices of their large language model APIs by as much as 80%, a rapid sequence of reductions documented in a widely discussed blog post. The cuts affect the per-token prices developers pay to call flagship models, directly lowering the cost of building applications on top of these APIs. Price is the single biggest lever on how widely AI gets adopted, so an 80% cut can turn previously uneconomical use cases — high-volume agents, batch document processing, always-on assistants — into viable products. It also signals that frontier labs no longer treat pricing power as guaranteed, which pressures the entire market, including cloud providers and smaller model vendors, to compete on cost rather than capability alone. The cuts are widely attributed to three forces: falling unit inference costs from better hardware utilization and serving optimizations, competitive pressure from cheap open-weight models such as DeepSeek, Kimi and GLM, and a desire to lock in developers before they migrate. Caveats matter here — list prices are not effective prices, since caching, batch discounts and volume contracts already lowered real costs, and both companies are reportedly still losing billions, so margins remain unclear.

hackernews · minimaxir · Oct 25, 21:11 · [Discussion](https://news.ycombinator.com/item?id=50236102)

**Background**: Inference cost is what a provider pays every time a trained model generates an output — a chatbot reply, a code completion, an image — and it is dominated by GPU compute time, so throughput and utilization matter as much as the sticker price of hardware. Open-weight models publish their trained parameters so anyone can download and self-host them, which puts a hard ceiling on what closed API providers can charge, since a customer can always substitute a locally run model. The combination of falling inference costs and credible open-weight alternatives is what makes steep API price cuts a rational defensive move rather than pure generosity.

<details><summary>References</summary>
<ul>
<li><a href="https://amnic.com/blogs/what-is-inference-cost">What Is Inference Cost ? AI 's Biggest Ongoing Bill - Amnic</a></li>
<li><a href="https://www.n-ix.com/open-weight-ai-models/">Open - weight AI models : What, why, and how to deploy them... - N-iX</a></li>
<li><a href="https://claw-ai.co/en/learn/what-are-open-weight-models">What are open - weight models ? | ClawAI</a></li>

</ul>
</details>

**Discussion**: Commenters largely agree that competition, especially from Chinese open-weight models, is the main driver, with several reporting that they switched to Kimi or GLM after hitting refusals or blocks on OpenAI and Anthropic. A recurring, more cynical thread argues the labs are building moats through enterprise contracts, consumer agents and regulatory capture, with some claiming that pushing regulation is partly aimed at shutting out Chinese open models. Others dispute the narrative that losses stem from R&D and scaling, arguing instead that the underlying LLM business model simply is not yet viable, while one commenter cites DeepSeek's disclosed figures of roughly $38 revenue per GPU-hour to argue incumbents still have significant pricing room.

**Tags**: `#LLM pricing`, `#OpenAI`, `#Anthropic`, `#AI competition`, `#inference costs`

---