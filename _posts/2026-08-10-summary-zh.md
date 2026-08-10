---
layout: default
title: "Horizon Summary: 2026-08-10 (ZH)"
date: 2026-08-10
lang: zh
---

> 从 34 条内容中筛选出 4 条重要资讯。

---

1. [利用基因组语言模型生成设计可行噬菌体基因组](#item-1) ⭐️ 9.0/10
2. [1998 年 W3C 经典文章重现，再引链接腐坏讨论](#item-2) ⭐️ 8.0/10
3. [AI 可穿戴设备记录一切，隐私反制引发热议](#item-3) ⭐️ 8.0/10
4. [全球最大 AI 算力设施在乌兰察布投产](#item-4) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [利用基因组语言模型生成设计可行噬菌体基因组](https://www.reddit.com/r/MachineLearning/comments/1vjj4pr/r_generative_design_of_novel_bacteriophages_with/) ⭐️ 9.0/10

研究人员使用基因组语言模型 Evo 1 和 Evo 2，以 ΦX174 为模板生成噬菌体全基因组序列，并通过实验验证了其中 16 个设计的噬菌体具有生存能力。这是首次实现对可行噬菌体基因组的生成式设计。 这项工作证明了基因组语言模型能够生成全基因组规模的功能序列，是迈向 AI 驱动合成生物学的重要一步。它可能加速定制噬菌体的设计，应用于噬菌体疗法和微生物组工程等领域。 生成的完整基因组具有真实的遗传架构和预期的宿主趋向性，16 个可行噬菌体显示出显著的进化新颖性。较新的模型 Evo 2 是一个开源的基因组基础模型，以单核苷酸分辨率在原核和真核 DNA 上训练。

reddit · r/MachineLearning · /u/moschles · 8月9日 07:11

**背景**: 基因组语言模型（gLMs）将 DNA 和 RNA 序列视为生物文本，利用 transformer 架构从原始序列中学习基因组语法和调控模式。Evo 1 和 Evo 2 是由 Arc Institute 和加州大学开发的开源基础模型，直接基于原始 DNA 序列而非自然语言进行训练。噬菌体是感染细菌的病毒；设计新型噬菌体对噬菌体疗法和理解病毒进化都很有价值。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Evo_(AI)">Evo (AI) - Wikipedia</a></li>
<li><a href="https://www.nature.com/articles/s41586-026-10176-5">Genome modelling and design across all domains of life with Evo 2 | Nature</a></li>
<li><a href="https://academic.oup.com/bib/article/27/1/bbaf724/8426124">comprehensive survey of genome language models in bioinformatics | Briefings in Bioinformatics | Oxford Academic</a></li>

</ul>
</details>

**标签**: `#generative AI`, `#genome language models`, `#synthetic biology`, `#bacteriophage`, `#Evo 2`

---

<a id="item-2"></a>
## [1998 年 W3C 经典文章重现，再引链接腐坏讨论](https://www.w3.org/Provider/Style/URI) ⭐️ 8.0/10

1998 年 W3C 的经典文章《Cool URIs Don't Change》在 Hacker News 上重新引发关注，引发 43 条评论讨论其现实意义。讨论中列举了链接腐坏的现代案例，包括 NSF.gov 的失效链接和微软失效的支持页面链接。 该讨论表明，在 Berners-Lee 提出这一建议几十年后，链接腐坏仍是普遍存在的问题，甚至影响到大型机构。它重新引发了关于持久标识符、重定向以及 SEO 实践如何影响 URL 管理的讨论。 W3C 的该页面已在同一 URI 上存在超过 26 年，印证了其关于稳定性的主张。评论者指出，这篇文章早于 301/302 重定向的普及，而 WordPress 等现代 CMS 在修改 slug 时会自动重定向，部分缓解但仍未解决该问题。

hackernews · Klaster_1 · 8月9日 14:32 · [社区讨论](https://news.ycombinator.com/item?id=49231809)

**背景**: 链接腐坏（link rot）指的是超链接因目标页面迁移或消失而逐渐失效的现象。蒂姆·伯纳斯-李（Tim Berners-Lee）于 1998 年撰写《Cool URIs Don't Change》，敦促网站管理员设计保持稳定的 URL，并警告“URI 不会变，是人把它们改掉了”。这篇文章已成为 Web 架构领域的经典建议。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.w3.org/Provider/Style/URI">Hypertext Style: Cool URIs don't change.</a></li>
<li><a href="https://en.wikipedia.org/wiki/Link_rot">Link rot</a></li>
<li><a href="https://news.ycombinator.com/item?id=23865484">Cool URIs Don't Change (1998) | Hacker News</a></li>

</ul>
</details>

**社区讨论**: 评论者大体认同这篇文章的建议具有永恒价值，但也指出了持续存在的失败案例：NSF.gov 的出版链接失效、微软将用户导向通用落地页，以及 W3C 自身的无障碍实践页面并未遵循该原则。有用户指出，这篇文章已在同一 URI 上存在 28 年，进一步增强了其信息可信度。

**标签**: `#web architecture`, `#URLs`, `#W3C`, `#web standards`, `#link rot`

---

<a id="item-3"></a>
## [AI 可穿戴设备记录一切，隐私反制引发热议](https://www.theatlantic.com/technology/2026/05/ai-wearable-surveillance-countermeasures/687203/) ⭐️ 8.0/10

《大西洋月刊》发表文章，探讨 AI 驱动的可穿戴设备如何持续记录人们的一切言行，并总结了反监控妆容、对抗性贴片等潜在反制手段。该文迅速引发广泛关注，在 Hacker News 上获得 171 条评论和大量讨论。 这一话题之所以重要，是因为它凸显了无处不在的 AI 监控与个人隐私之间日益加剧的冲突。这场讨论影响消费者、科技公司和政策制定者，并提出了关于企业权力以及采取反监控措施必要性的紧迫问题。 该文章通过 archive.is 的存档链接访问，评论者还贴出了芝加哥大学 Sandlab 实验室的 Jammer 研究项目，称其是早期灵感来源。讨论中还提到了避开验证码和地域限制的 archive.is 替代方案。

hackernews · ike_usawa · 8月9日 11:30 · [社区讨论](https://news.ycombinator.com/item?id=49230477)

**背景**: 智能眼镜和摄像头等 AI 可穿戴设备可以持续录制，从而实现被动监控。多年来人们开发了多种反制手段：CV Dazzle 通过化妆和发型干扰人脸检测，Stealth Wear 采用金属化织物屏蔽热成像，对抗性贴片则是能欺骗计算机视觉模型的实体物体。这些技术体现了监控与隐私保护之间持续的军备竞赛。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Computer_vision_dazzle">Computer vision dazzle - Wikipedia</a></li>
<li><a href="https://www.zdnet.com/article/stealth-wear-the-latest-in-anti-surveillance-clothing/">Stealth Wear : The latest in anti - surveillance clothing | ZDNET</a></li>
<li><a href="https://analyticsindiamag.com/deep-tech/what-are-adversarial-patches-why-should-we-worry/">What Are Adversarial Patches & Why Should We Worry</a></li>

</ul>
</details>

**社区讨论**: 评论者普遍对隐私和企业权力表示担忧，有人甚至呼吁像政教分离那样实现'企业与国家分离'。还有人提供了实用资源，包括文章赠阅链接、Jammer 原始研究项目页面，以及无需 JavaScript 的 archive.is 文本命令替代方案。

**标签**: `#surveillance`, `#privacy`, `#AI`, `#wearables`, `#ethics`

---

<a id="item-4"></a>
## [全球最大 AI 算力设施在乌兰察布投产](https://www.globaltimes.cn/page/202608/1367666.shtml) ⭐️ 8.0/10

2026 年 8 月 6 日，远景科技集团宣布“远景乌兰察布星河基地”正式投产。该基地是全球最大的单体 AI 算力设施，建筑面积达 12 万平方米，规划总容量 2GW，支持百万 GPU 并行计算，绿电占比超过 80%。 这一基础设施里程碑大幅增强了中国的 AI 算力供给，该基地是全球 Token 产出能力最强的单体 AI 数据中心。同时，它也验证了大规模绿色算力集群的可行性，并为“东数西算”战略提供了重要示范。 基地位于国家“东数西算”八大节点之一的乌兰察布，距北京约 240 公里，数据传输延迟仅 4.2 毫秒，电价较京津冀地区低约 50%。该项目是远景“戈壁使命”计划的首个旗舰项目，旨在为国产算力集群提供可复制的建设方案。

telegram · zaihuapd · 8月9日 05:06

**背景**: “东数西算”是中国自 2022 年起实施的一项工程，将东部产生的海量数据送往西部资源丰富地区进行存储和计算，以优化资源配置。乌兰察布是该工程的重要节点，此前华为、阿里巴巴、苹果、快手等企业已在此布局算力设施。新投产的星河基地专门面向 AI 负载，利用超过 80%的绿电来降低大规模 AI 训练和推理的碳排放。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://zh.wikipedia.org/zh-hans/东数西算">东数西算 - 维基百科，自由的百科全书</a></li>
<li><a href="https://baike.baidu.com/item/东数西算/57984771">东数西算_百度百科</a></li>
<li><a href="https://www.iii.tsinghua.edu.cn/info/1121/3154.htm">“东数西算”工程解读-清华大学互联网产业研究院</a></li>

</ul>
</details>

**标签**: `#AI infrastructure`, `#data center`, `#green energy`, `#China`, `#East-Data-West-Computing`

---