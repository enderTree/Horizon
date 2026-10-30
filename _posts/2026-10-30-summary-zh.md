---
layout: default
title: "Horizon Summary: 2026-10-30 (ZH)"
date: 2026-10-30
lang: zh
---

> 从 37 条内容中筛选出 4 条重要资讯。

---

1. [Arkham 标注的“币安黑客”实体关联 56 亿美元资金，24 亿美元已被冻结](#item-1) ⭐️ 9.0/10
2. [Mistral 开放 Mistral Large 4 权重，API 价格近乎减半](#item-2) ⭐️ 9.0/10
3. [微型世界模型在 Raspberry Pi Pico 2 W 上运行游戏](#item-3) ⭐️ 8.0/10
4. [DoorDash 宣布收购 Instacart，将缔造美国配送巨头](#item-4) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Arkham 标注的“币安黑客”实体关联 56 亿美元资金，24 亿美元已被冻结](https://arkm.com/explorer/entity/21a94755-f604-45e5-9501-6542e23005e8) ⭐️ 9.0/10

如果得到证实，这将成为史上规模最大的加密货币盗窃案，远超 Mt. Gox 级别的损失，并重塑交易所、发行方与监管机构应对链上犯罪的方式。这也是一次范式级的示范：稳定币发行方能够单方面冻结数十亿美元的“去中心化”资产，这直接冲击了支撑加密货币行业的去中心化叙事。 56 亿美元这一数字来自 Arkham 的实体标签——即基于链上聚类启发式方法构建的归属集群——而非币安的公开声明或法院文件，因此确切损失金额及其与单次事件的关联仍未获确认。所报告的冻结金额（简单相加约 22.8 亿美元）依据的是公开区块浏览器交易记录，其机制是合约层面的黑名单：Tether 的 USDT 合约提供 addBlackList 函数，Circle 对 USDC 地址也行使类似的控制权。

hackernews · Tiberium · 10月29日 21:38 · [社区讨论](https://news.ycombinator.com/item?id=50296470)

**背景**: Arkham Intelligence 是一个区块链情报平台和多链浏览器，它通过去匿名化地址并将其归入带标签的“实体”，因此“Binance hacker 1029”这类标签属于分析师式的归属判断，而非官方认定。USDT、USDC 等稳定币由中心化公司发行，这些公司在智能合约中保留了特权函数，可以在执法机构要求或自身合规需要时冻结特定地址。这种冻结权此前已被大规模使用——Tether 曾将数千个持有数十亿美元 USDT 的地址列入黑名单——因此本次事件再次点燃了关于稳定币资金究竟有多“去中心化”的长期争论。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://info.arkm.com/arkham-blockchain-explorer">Blockchain Explorer | Arkham</a></li>
<li><a href="https://karcrypto.com/en/blog/how-tether-freezes-usdt-blacklist-mechanism.html">How Tether Freezes USDT : The Blacklist Mechanism... | KarCrypto</a></li>
<li><a href="https://fswap.io/blog/stablecoin-controversies">Stablecoin Controversies: Can Tether or Circle “Disable”... | Fswap</a></li>

</ul>
</details>

**社区讨论**: Hacker News 的评论者大多认为该事件可信，并引用 Molly White 的确认以及 Circle 和 Tether 在交易层面的冻结证据。有人将其与 Mt. Gox 时代的旧帖相提并论，视作历史的押韵；也有人把此事看作数字货币领域因“害怕损失”而开启的“向感知质量迁移”的开端。讨论的主流情绪是对中心化发行方能够冻结数十亿美元、而这类资产却以去中心化为卖点感到不安。

**标签**: `#cryptocurrency`, `#security`, `#blockchain`, `#hacking`, `#stablecoins`

---

<a id="item-2"></a>
## [Mistral 开放 Mistral Large 4 权重，API 价格近乎减半](https://mistral.ai/news/mistral-large-4-oss/) ⭐️ 9.0/10

Mistral 公开了 Mistral Large 4 的模型权重，这是一个总参数量 1 万亿、激活参数量 520 亿的混合专家（MoE）模型，并在 Hugging Face 上发布了 Mistral-Large-4-1T-A52B 等检查点。与此同时，Mistral 将 API 价格相比预览版近乎减半，降至每百万输入 token 0.70 美元、每百万输出 token 2.10 美元（此前分别为 1.36 美元和 4.18 美元）。 开放一个万亿参数、接近前沿水平的模型权重，对开放模型生态来说是重大事件，因为这让任何有能力部署该模型的人都能直接使用，而不再只能通过 API 调用。同步进行的降价可能同样关键：在新价格下，该模型在真实评测中的性价比变得有竞争力，而此前预览版在同等评测中被认为不具备竞争力。 Mistral 强调该模型在恶意网络安全请求上的平均拒绝率达到 96.6%，并称这是开放模型中所测得的最高水平，但公告并未给出在良性请求上的误拒率数据作为对照。有评论者指出，实际的权重下载链接被放在公告接近末尾的位置，Hugging Face 上同时发布了标准检查点和一个“NVF”变体。

hackernews · kuberwastaken · 10月29日 14:13 · [社区讨论](https://news.ycombinator.com/item?id=50289418)

**背景**: 混合专家（MoE）是一种模型架构：模型内部包含许多独立的“专家”子网络，并由一个路由网络为每个 token 只激活其中一小部分，因此总参数量可以做得非常大，而每个 token 的计算开销却低得多。这也是为什么一个模型可以被称为“总量 1 万亿、激活 520 亿”——在任意一个 token 上只有约 5% 的参数真正参与计算。“开放权重”指的是训练好的参数可以被任何人下载、运行或微调，它与完全开源不同，因为训练数据和训练代码通常并不公开。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/blog/moe">Mixture of Experts Explained - Hugging Face</a></li>
<li><a href="https://promptengineering.org/llm-open-source-vs-open-weights-vs-restricted-weights/">Openness in Language Models : Open Source vs Open Weights vs ...</a></li>
<li><a href="https://arxiv.org/abs/2507.11181">[2507.11181] Mixture of Experts in Large Language Models Mixture of Experts Explained - Hugging Face Applying Mixture of Experts in LLM Architectures | NVIDIA ... What Is Mixture of Experts (MoE) and How It Works? The Mixture-of-Experts ML Approach - Baeldung Mixture of experts (MoE) | Sebastian Raschka, PhD</a></li>

</ul>
</details>

**社区讨论**: Hacker News 的评论集中在两点：一是约 50% 的降价，最高票评论称由于预览版在旧价格下缺乏竞争力，这次正式发布值得重新全面评估；二是对 96.6% 网络安全拒绝率指标的尖锐批评，认为该基准没有公布误拒数据，有评论者调侃说按 96.7% 的概率随机拒绝也能得到同样的分数。也有人为 Mistral 的发布叫好，认为这对少数几家主导的 AI 供应商而言是有价值的竞争；还有人询问另一个“Mistral Vibe CLI”编程工具在连简单请求都触发限流后是否仍在积极维护。

**标签**: `#open-weights`, `#llm`, `#mistral`, `#model-release`, `#ai-pricing`

---

<a id="item-3"></a>
## [微型世界模型在 Raspberry Pi Pico 2 W 上运行游戏](https://github.com/SheepSeb/tinyworldformer) ⭐️ 8.0/10

开发者 SheepSeb 发布了名为 "tinyworldformer" 的项目，把针对简单游戏的微型 transformer 世界模型直接跑在 Raspberry Pi Pico 2 W 微控制器上。README 指出，要建模像 mini-Doom 这样更复杂的游戏必须使用循环（权重共享、反复应用）的 transformer，而更简单的游戏则无需循环即可运行。 这表明通常与大型 GPU 和重量级训练联系在一起的神经网络世界模型，可以被压缩到几美元的微控制器上，为廉价的嵌入式智能体和面向机器人、游戏的学习型模拟器指明方向。它同时提供了一个具体且可复现的例证：循环 transformer 架构能以很低的参数代价换取额外的建模能力。 该演示面向基于 RP2350 的 Pico 2 W，通过学到的动力学逐帧重建游戏画面，而不是运行原始游戏代码，因此保真度取决于模型对游戏规则的学习程度。项目在如此受限的硬件上展现出的确定性值得注意，但这也引出一个悬而未决的问题：模型是否实际上只是记住了训练轨迹。

hackernews · airinei · 10月29日 20:32 · [社区讨论](https://news.ycombinator.com/item?id=50295450)

**背景**: 所谓"世界模型"，是一种被训练用来预测环境如何演化的神经网络：给定当前游戏画面和一个动作，它预测下一帧，之后便可作为替身模拟器来训练智能体或生成游戏过程。Transformer 是现代大语言模型背后的注意力神经网络架构；"循环"transformer 则在多次重复迭代中复用同一套权重，在不增加参数的情况下模拟更深的网络。Raspberry Pi Pico 2 W 是基于 RP2350 芯片的小型微控制器开发板，于 2024 年底发布，在早期 Pico 2 的基础上增加了 Wi-Fi 和蓝牙。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.emergentmind.com/topics/looped-transformer-architecture">Looped Transformer Architecture - emergentmind.com</a></li>
<li><a href="https://www.raspberrypi.com/products/raspberry-pi-pico-2/">Buy a Raspberry Pi Pico 2 – Raspberry Pi</a></li>
<li><a href="https://arxiv.org/html/2409.15647v2">Looped Transformers for Length Generalization - arXiv.org</a></li>

</ul>
</details>

**社区讨论**: 评论者反响热烈，询问训练使用了什么硬件，以及这个演示能否移植到 WebGPU。不少人关注两个发现：循环 transformer 对 mini-Doom 是必需的，而对更简单的游戏则不然；以及神经网络竟能如此确定，由此引出这是否属于某种过拟合、以及是否所有游戏共用一个模型的疑问。有评论者提出了对抗性视角：如果 actor 也在世界模型的错误上训练，它可能学会诱发幻觉，从而把自己推入更容易的状态。

**标签**: `#world-models`, `#transformers`, `#edge-ai`, `#raspberry-pi-pico`, `#game-emulation`

---

<a id="item-4"></a>
## [DoorDash 宣布收购 Instacart，将缔造美国配送巨头](https://about.doordash.com/en-us/news/doordash-to-acquire-instacart) ⭐️ 8.0/10

DoorDash 宣布计划收购 Instacart，这笔交易将把美国领先的餐饮外卖平台与占据主导地位的杂货配送服务合并在一起。评论者指出，这将是迄今为止两家 Y Combinator 系公司之间规模最大的一次合并——DoorDash（YC S13）与 Instacart（YC S12）。 这笔交易将重塑美国的餐饮与杂货配送市场，把该行业两个最大的消费品牌收归同一所有者，并在线上杂货领域形成对抗沃尔玛和亚马逊的更强力量。它同时也立即引发反垄断方面的疑问，并可能影响依赖这两个平台的商家、配送员和消费者。 社区分析认为，两家公司的业务重叠程度低于标题给人的印象：DoorDash 在杂货配送领域几乎没有什么存在感，而 Instacart 的非杂货配送据称是由 Uber Eats 提供的。DoorDash 给出的说法是此次收购将帮助本地商店增强竞争力，但讨论中引述的商家称该公司是它们不得不忍受却又并不喜欢的“必要之恶”。

hackernews · WalterSobchak · 10月29日 12:33 · [社区讨论](https://news.ycombinator.com/item?id=50287919)

**背景**: DoorDash 是美国最大的餐饮外卖平台，而 Instacart 则是从本地超市代购杂货并提供当日达服务的最知名平台。两家公司都曾入驻 Y Combinator——这家成立于 2005 年的硅谷创业孵化器已资助数千家公司，被普遍视为同类项目中最具声望的一个。随着各家企业寻求规模以对抗亚马逊、沃尔玛和 Uber，零工经济配送行业的整合正在加速。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Y_Combinator">Y Combinator - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 整体情绪偏向怀疑：多位评论者认为美国的配送市场已经处于垄断或寡头状态，一位站在商家立场的用户称 DoorDash 抽走大比例销售额，其配送员对店员态度粗鲁。也有人反驳这种反垄断直觉，认为两家业务重叠很小，这笔交易可能主要是帮助 Instacart 和 DoorDash 与沃尔玛、亚马逊竞争——不过仍有人乐于看到美国司法部出面阻止。

**标签**: `#mergers-acquisitions`, `#doordash`, `#instacart`, `#gig-economy`, `#antitrust`

---