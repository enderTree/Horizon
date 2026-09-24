---
layout: default
title: "Horizon Summary: 2026-09-24 (ZH)"
date: 2026-09-24
lang: zh
---

> 从 33 条内容中筛选出 3 条重要资讯。

---

1. [Anthropic 称 Claude 发现具类 CRISPR 重复序列的新型酶系统](#item-1) ⭐️ 8.0/10
2. [文章预测：LLM token 或将便宜到不如一次 grep](#item-2) ⭐️ 8.0/10
3. [ClusterMAX 3.0 发布：SemiAnalysis 更新 GPU 云评级体系](#item-3) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Anthropic 称 Claude 发现具类 CRISPR 重复序列的新型酶系统](https://www.anthropic.com/news/claude-discovers-novel-enzyme-system) ⭐️ 8.0/10

Anthropic 在其官方博客中宣布，其模型 Claude 以自主智能体的方式分析原始 DNA 序列时，识别出此前未被描述过的基因组排列：一个具有类 CRISPR 结构的串联重复序列阵列，紧邻一个已知的 retron 样逆转录酶。该发现在 Anthropic 的新闻稿中发布后，迅速成为本周讨论度最高的 AI for Science 话题之一。 这是 LLM 智能体参与真实生物学发现的一个高关注度案例，既为“AI 驱动科学发现”增添了有力例证，也再次点燃了关于是否应让这类模型涉足基因组工程的生物安全争论。如果智能体真能从原始数据中找出新的序列结构，那么生物学研究的瓶颈将进一步转向实验验证与结果解读。 评论者指出，该系统的核心是一个已知的 retron 样逆转录酶，而当前基因编辑的实际瓶颈主要在于递送，而非核酸酶本身是否够多够好，因此“突破”的表述可能被夸大。此外，独立的 CRISPR 阵列以及类 CRISPR 重复的 RNA 调控元件在文献中已有多年的记载，这也在一定程度上削弱了该重复序列排列本身的新颖性。

hackernews · raahelb · 9月23日 18:06 · [社区讨论](https://news.ycombinator.com/item?id=49820134)

**背景**: CRISPR 全称是“成簇规律间隔短回文重复序列”，是细菌和古菌的适应性免疫系统，由短重复序列与间隔序列交替排列构成，通常紧邻 cas 基因，科学家将其改造成了 Cas9 等基因编辑工具。Retron 则是细菌中的逆转录元件，通过逆转录酶生成 msDNA，近年来同样被工程化改造为基因组编辑工具。大语言模型智能体能够读取超长的 DNA 序列并在其中标注出模式，这正是此类“发现”得以声称的技术机制。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/CRISPR">CRISPR - Wikipedia</a></li>
<li><a href="https://pmc.ncbi.nlm.nih.gov/articles/PMC7757702/">CRISPR Arrays Away from cas Genes - PMC - NIH</a></li>
<li><a href="https://www.nature.com/articles/s41586-023-06221-2">Scientific discovery in the age of artificial intelligence | Nature</a></li>

</ul>
</details>

**社区讨论**: 整体情绪是兴奋中带着冷静：一条高赞评论认为该发现实际上只是围绕已知逆转录酶的一个此前未被描述的排列，并强调基因编辑疗法受限于递送；也有人很享受通过智能体的对话记录“重历”发现过程。多位评论者调侃 Anthropic 一边明令禁止将 Claude 用于生物工程、一边又宣传它与基因组编辑相关的发现存在矛盾，还有人直接提问：LLM 究竟是如何对生化问题进行推理的。

**标签**: `#AI for Science`, `#CRISPR`, `#Genomics`, `#Anthropic`, `#Biotechnology`

---

<a id="item-2"></a>
## [文章预测：LLM token 或将便宜到不如一次 grep](https://jyn.dev/tokens-too-cheap-to-meter/) ⭐️ 8.0/10

一篇题为《Tokens too cheap to meter》的博客文章指出，调用 GPT-5.6 Luna 这类模型的成本目前仅比运行一次 grep 高出约 4–5 个数量级，并据此预测：按当前的进步速度，调用 LLM 很快就会比调用 grep 这类本地工具更便宜。该文在 Hacker News 上引发热议，获得 254 分和 186 条评论。 如果推理真的便宜到这种程度，智能体（agent）软件的经济学将被根本改写：模型可以被用来做那些目前只交给本地工具处理的琐碎校验、重试和并行扇出工作，“把 LLM 当子程序调用”可能成为默认做法。与此同时，这也迫使外界审视：支撑这些廉价 token 的巨额基础设施投入究竟能否收回。 该预测所需跨越的差距仍有 4–5 个数量级，意味着必须再有多年持续的复利式效率提升才能成立。文章聚焦单次调用成本，却基本没有讨论商业模式的可行性，也回避了高质量、已编译能力（compiled capabilities）的单次成本可能见顶而非无限下降的问题；评论者还对该文关于“可塑软件（malleable software）”的相关论断提出质疑。

hackernews · teoruiz · 9月23日 09:21 · [社区讨论](https://news.ycombinator.com/item?id=49813482)

**背景**: LLM 推理 token 是模型读取和生成的文本单位，服务商按每百万输入/输出 token 计费；推理是指模型在训练完成后回答提示词的过程。工具调用（tool call）则指模型调用外部函数或程序（例如 grep）来获取数据或作用于环境，目前相比一次模型调用几乎免费。文章标题借用了 Lewis Strauss 于 1954 年提出的核能“便宜到无需计量”（too cheap to meter）承诺——这一预言从未实现，多位评论者也提出了这一类比。从历史看，固定能力水平下的推理成本下降极快：Stanford HAI《2025 AI Index》报告显示，GPT-3.5 级别的系统在 2022 年 11 月至 2024 年 10 月间成本下降超过 280 倍。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://valueaddvc.com/blog/how-ai-inference-costs-have-dropped-95-in-two-years-and-what-happens-next">AI Inference: 95% Cost Cut in Two Years, $0.50/M</a></li>
<li><a href="https://www.mirantis.com/blog/inference-costs/">Optimizing Inference Costs: The Complete Guide | Mirantis</a></li>
<li><a href="https://huggingface.co/blog/Kseniase/inference">Topic 23: What is LLM Inference , it's challenges and solutions for it</a></li>

</ul>
</details>

**社区讨论**: 讨论整体持赞赏态度，但对这种外推普遍存疑：jetrink 引用斯坦因定律（Stein's Law），认为如果某件事不可能永远持续下去，它终将停止，因此这些效率提升不会无限延续。cs702 称赞文章有洞见，但指出它对商业模式可行性的分析很薄弱——所有主要玩家都在押注未来利润足以证明当前的巨额基础设施投入是合理的。abirch 把这一论断与 Lewis Strauss 1954 年从未兑现的核能“便宜到无需计量”承诺相提并论，rtpg 则对文中“可塑软件”的说法表示怀疑。

**标签**: `#AI/ML`, `#LLM economics`, `#inference cost`, `#business models`, `#technology forecasting`

---

<a id="item-3"></a>
## [ClusterMAX 3.0 发布：SemiAnalysis 更新 GPU 云评级体系](https://newsletter.semianalysis.com/p/clustermax-30-the-industry-standard) ⭐️ 8.0/10

SemiAnalysis 发布了 ClusterMAX 3.0，这是其 GPU 云评级与排名体系的第三个主要版本，从可靠性、性能、支持、定价和安全等维度对全球 GPU 云服务商进行评估。官方称这是迄今为止对全球 GPU 云服务商最详尽的一次分析。 在 GPU 供应依然紧张的背景下，选择 GPU 云已成为 AI 团队重大的资本与运营决策，而一份独立、以数据驱动的评分表能帮助采购方分辨真正可靠的算力与宣传话术。由于 ClusterMAX 已成为事实上的行业基准，其评级会影响服务商声誉、企业采购决策乃至定价能力。 ClusterMAX 框架对 80 多家 GPU 云服务商进行打分，评估维度包括性能、网络、存储、安全、支持和定价，而不只是简单的基准测试或价格对比。它属于行业分析而非技术突破，完整细节发布在 SemiAnalysis 的 newsletter 及专门的 clustermax.ai 网站上。

rss · Semianalysis · 9月23日 21:20

**背景**: SemiAnalysis 是一家由 Dylan Patel 领导的半导体与 AI 基础设施研究机构，其关于数据中心电力、加速器和供应链的分析广受关注。其 ClusterMAX 体系（2.0 版本于 2025 年 11 月发布）被设计为一个独立框架，不局限于原始基准测试，而是评判 GPU 云的整个服务生态。GPU 云以按小时租用的方式提供 NVIDIA 等加速器用于 AI 训练与推理，而它们在互连带宽、存储吞吐和支持响应速度等方面的实际质量差异巨大，这正是 ClusterMAX 试图量化的内容。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.clustermax.ai/">GPU Cloud ClusterMAX™ Rating & Ranking System | SemiAnalysis</a></li>
<li><a href="https://www.clustermax.ai/overview">ClusterMAX Overview — GPU Cloud Rating Methodology ...</a></li>
<li><a href="https://newsletter.semianalysis.com/p/clustermax-20-the-industry-standard">ClusterMAX™ 2.0: The Industry Standard GPU Cloud Rating System</a></li>

</ul>
</details>

**标签**: `#GPU cloud`, `#AI infrastructure`, `#cloud benchmarking`, `#systems research`, `#SemiAnalysis`

---