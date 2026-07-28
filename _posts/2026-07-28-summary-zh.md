---
layout: default
title: "Horizon Summary: 2026-07-28 (ZH)"
date: 2026-07-28
lang: zh
---

> 从 29 条内容中筛选出 8 条重要资讯。

---

1. [月之暗面发布 2.8 万亿参数 Kimi-K3 权重](#item-1) ⭐️ 9.0/10
2. [Fastjson 1.x 高危 RCE 漏洞，无需 gadget 或 autoType](#item-2) ⭐️ 9.0/10
3. [中芯国际测试中国首台国产 DUV 光刻机](#item-3) ⭐️ 9.0/10
4. [Anthropic 呼吁对强大模型强制安全测试](#item-4) ⭐️ 8.0/10
5. [用户名中缺少下划线导致无辜者被误判 18 个月监禁](#item-5) ⭐️ 8.0/10
6. [Paged Out 第 9 期发布：免费技术杂志](#item-6) ⭐️ 8.0/10
7. [法官驳回谷歌以 DMCA 为由禁止数据抓取的辩护](#item-7) ⭐️ 8.0/10
8. [个人基准测试发现 6 个前沿大模型均表现出左倾政治偏见](#item-8) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [月之暗面发布 2.8 万亿参数 Kimi-K3 权重](https://simonwillison.net/2026/Jul/27/kimi-k3/#atom-everything) ⭐️ 9.0/10

月之暗面（Moonshot AI）已在 Hugging Face 上发布了 Kimi-K3 的权重，这是一个 2.8 万亿参数的开权重模型，采用修改版 MIT 许可，对大型企业增加了额外的商业限制。 作为有史以来发布的最大开权重模型，Kimi-K3 代表了在普及前沿 AI 能力方面的一个重要里程碑，但其限制性许可可能会阻碍大型商业实体的采用。 该模型在 Hugging Face 上大小为 1.56 TB，并已通过 OpenRouter 从 7 家提供商获得，输入 token 价格为每百万个 3 美元，输出 token 价格为每百万个 15 美元；K3 许可要求年收入超过 2000 万美元的“模型即服务”企业签署单独协议。

rss · Simon Willison · 7月27日 23:39

**背景**: Kimi-K3 是一个开权重模型，意味着其训练参数公开可用，但由于许可限制，并非完全开源。拥有 2.8 万亿参数，它超越了之前的大模型，专为长上下文编程、知识工作和复杂推理任务设计，具备工具使用和网页浏览等代理能力。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.kimi.com/es-419/blog/kimi-k3">Kimi K3 Tech Blog: Open Frontier Intelligence</a></li>
<li><a href="https://huggingface.co/blog/ResterChed/kimi-k3-model-overview-mxfp4-quantization-open-wei">Kimi K3 Model Overview: 2.8T Parameters, MXFP4 Quantization, and What the Open Weights Mean for the Community</a></li>
<li><a href="https://www.tomshardware.com/tech-industry/artificial-intelligence/moonshot-releases-2-8-trillion-parameter-kimi-k3">China's 2.8-trillion-parameter Kimi K3 beats Claude Fable 5 in Frontend Code Arena benchmark— Moonshot AI delivers largest open-weight AI model ever, as China works around U.S. compute limits | Tom's Hardware</a></li>

</ul>
</details>

**标签**: `#AI`, `#open-source`, `#large language models`, `#weights release`, `#Moonshot AI`

---

<a id="item-2"></a>
## [Fastjson 1.x 高危 RCE 漏洞，无需 gadget 或 autoType](https://t.me/zaihuapd/42797) ⭐️ 9.0/10

安全研究人员 Kirill Firsov 披露，Fastjson 1.2.68 至 1.2.83 版本存在高危远程代码执行漏洞，该漏洞无需开启 autoType 也无需依赖 classpath gadget。 该漏洞极其危险，因为它影响所有 Fastjson 1.x 用户，可在 JDK 8、17 和 21 上利用。由于 Fastjson 1.x 已停止维护，官方不会发布补丁，唯一的缓解措施是升级到 Fastjson 2。 该漏洞不需要特殊配置（默认 autoType 关闭），也不依赖已有的 gadget 链，因此在多种 Java 版本上均可利用。报告建议升级到 Fastjson 2，或通过禁用 Feature.SupportAutoType 等方式进行临时缓解。

telegram · zaihuapd · 7月27日 10:31

**背景**: Fastjson 是一个流行的 Java JSON 解析和序列化库，广泛应用于各类应用中。autoType 功能允许动态类型解析，但历史上一直是漏洞的来源。Gadget 链是在反序列化过程中可利用的一系列类，用于执行任意代码。这个新漏洞绕过了之前依赖于关闭 autoType 或移除危险 gadget 的缓解措施。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://dev.to/tutorialboy/the-fastjson-auto-type-bypass-leads-to-rce-vulnerability-cve-2022-25845-19m0">The Fastjson “ Auto Type Bypass” leads to RCE... - DEV Community</a></li>
<li><a href="https://snyk.io/blog/serialization-and-deserialization-in-java/">Serialization and deserialization in Java | Snyk Blog | Snyk</a></li>

</ul>
</details>

**标签**: `#security`, `#vulnerability`, `#fastjson`, `#rce`, `#java`

---

<a id="item-3"></a>
## [中芯国际测试中国首台国产 DUV 光刻机](https://t.me/zaihuapd/42800) ⭐️ 9.0/10

中芯国际正在试运行上海初创公司宇量昇研发的中国首台国产深紫外（DUV）光刻机。该设备旨在生产 28 纳米芯片，并可通过多重图形化工艺实现 7 纳米，量产目标定在 2027 年。 这一进展是中国实现半导体自给自足的关键一步，减少了对荷兰 ASML 的依赖。如果成功，它可能通过提供成熟和先进节点光刻的替代来源，重塑全球芯片供应链。 该设备大部分零部件已实现国产化，但仍有部分依赖进口。中芯国际正用它生产 28 纳米芯片，并尝试通过多重图形化实现 7 纳米，甚至低良率下挑战 5 纳米。业内人士估计，实现稳定良率至少需要一至两年，量产最快可能于 2027 年实现。

telegram · zaihuapd · 7月27日 14:10

**背景**: 深紫外（DUV）光刻使用 193 纳米或 248 纳米的光在硅晶圆上刻画电路，单次曝光可实现约 50 纳米的最小特征尺寸。为了达到 7 纳米等更小节点，制造商采用多重图形化技术，将单层图案分割成多次曝光，从而有效缩小印刷特征。目前，中国最先进的芯片依赖进口的 ASML DUV 设备，而使用 13.5 纳米光进行更精细图案的极紫外（EUV）光刻则因美国出口管制而被禁止对华销售。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/DUV_lithography">DUV lithography</a></li>
<li><a href="https://semiengineering.com/knowledge_centers/manufacturing/patterning/multipatterning/">Multiple Patterning - Semiconductor Engineering</a></li>
<li><a href="https://en.wikipedia.org/wiki/Extreme_ultraviolet_lithography">EUV lithography - Wikipedia</a></li>

</ul>
</details>

**标签**: `#semiconductor`, `#lithography`, `#china`, `#duv`, `#smic`

---

<a id="item-4"></a>
## [Anthropic 呼吁对强大模型强制安全测试](https://www.anthropic.com/news/position-open-weights-models) ⭐️ 8.0/10

Anthropic 发布了一项政策声明，主张对所有足够强大的 AI 模型（包括开源权重和封闭模型）进行强制性安全测试。许多社区成员认为，由于测试成本和访问权限等实际障碍，这一立场实际上是在呼吁禁止开源权重模型。 这一立场可能对开源权重 AI 生态系统产生重大影响，如果强制性测试成为法律，可能会限制强大开源模型的发布。它也凸显了 AI 安全倡导者与开源社区在监管和访问权问题上日益加剧的紧张关系。 Anthropic 明确表示从未主张禁止开源权重模型，但要求对所有有能力的模型进行安全测试。然而，批评者指出，实际执行——谁进行测试、成本以及潜在的行政拒绝——可能实际上构成禁令。

hackernews · surprisetalk · 7月27日 22:03 · [社区讨论](https://news.ycombinator.com/item?id=49076057)

**背景**: 开源权重模型是指其训练参数（权重）公开发布的 AI 模型，任何人都可以下载和使用。Anthropic 是一家 AI 安全公司，开发 Claude 模型系列，并制定了包含分级安全等级的负责任扩展政策。争论的焦点在于，政府强制要求的安全测试是否会不成比例地加重开源权重发布的负担，从而实际上限制它们。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://hai.stanford.edu/ai-definitions/what-is-an-open-weight-model">What is an Open-Weight Model? - Stanford HAI</a></li>
<li><a href="https://www.anthropic.com/policy">AI policy \ Anthropic</a></li>
<li><a href="https://www.anthropic.com/responsible-scaling-policy">Anthropic’s Responsible Scaling Policy \ Anthropic</a></li>

</ul>
</details>

**社区讨论**: 社区评论普遍持批评态度，指责 Anthropic 虚伪并试图保护其商业利益。评论者认为，类似的对华芯片销售禁令并未奏效，而测试要求将对开源模型产生不成比例的影响。

**标签**: `#AI safety`, `#open-weights`, `#regulation`, `#Anthropic`, `#policy`

---

<a id="item-5"></a>
## [用户名中缺少下划线导致无辜者被误判 18 个月监禁](https://arstechnica.com/tech-policy/2026/07/police-missed-one-underscore-and-sent-the-wrong-man-to-prison/) ⭐️ 8.0/10

Kik 用户名中缺少一个下划线，导致警方逮捕并定罪了一名无辜男子，使其服刑 18 个月后才发现错误并撤销定罪。 此案凸显了数字证据中的微小技术错误如何造成毁灭性的现实后果，以及调查人员的确认偏差如何阻碍这些错误的纠正。它强调了在司法系统中加强数据完整性检查和人为监督的紧迫性。 这名无辜男子没有任何亲密图像或证据将其与犯罪联系起来，警方甚至无法证明他在相关期间访问过 Kik。尽管如此，他仍被判定犯有引诱未成年人、提供色情材料和持有儿童色情制品罪。

hackernews · quantified · 7月27日 22:10 · [社区讨论](https://news.ycombinator.com/item?id=49076116)

**背景**: Kik 是一款使用用户名的即时通讯应用。在此案中，犯罪者的用户名包含一个下划线，而无辜者的用户名则缺少它。确认偏差——即倾向于接受符合自己先入为主观念的信息——导致调查人员忽视了这一差异及其他无罪证据。此案是一个警示故事，说明了人类在评估数字证据时判断力的易错性。

**社区讨论**: 评论者对系统性失误表示愤慨，许多人质疑为何该男子未因失去收入和名誉损害获得赔偿。有人建议使用 LLM 来检测此类案件中的差异，另一些人则引用经典故事《Computers Don't Argue》来说明过度依赖数据而不加核实的危险。讨论还注意到跨国因素：受害者在美国，被告在加拿大。

**标签**: `#legal-system`, `#data-integrity`, `#wrongful-conviction`, `#confirmation-bias`, `#ethics`

---

<a id="item-6"></a>
## [Paged Out 第 9 期发布：免费技术杂志](https://pagedout.institute/download/PagedOut_009.pdf) ⭐️ 8.0/10

Paged Out 第 9 期已作为免费 PDF 发布，包含深入的技术文章和精美的排版设计。 它延续了 2600 和 Phrack 等黑客杂志的传统，提供高质量、社区驱动的出版物，吸引对技术好奇的读者。 PDF 可免费下载；未来计划推出印刷版。该杂志涵盖 C 语言编程和亚像素渲染等多个主题。

hackernews · laurensr · 7月27日 14:22 · [社区讨论](https://news.ycombinator.com/item?id=49070138)

**背景**: Paged Out 是一本免费的社区驱动技术杂志，专注于深入、黑客好奇的主题。其设计注重视觉吸引力，类似于现代的 2600 或 Phrack，但拥有高质量排版和插图。

**社区讨论**: 评论者赞赏该杂志的幽默（如《C 语言初学步骤》）、技术深度（如《亚像素动物园》）和设计。有人表示有兴趣购买印刷版。还有人将其与 2600 和 Phrack 相提并论。

**标签**: `#programming`, `#hacking`, `#zine`, `#technical`, `#community`

---

<a id="item-7"></a>
## [法官驳回谷歌以 DMCA 为由禁止数据抓取的辩护](https://www.techdirt.com/2026/07/27/judge-rejects-googles-attempt-to-dmca-its-way-out-of-being-scraped/) ⭐️ 8.0/10

一名联邦法官裁定，谷歌不能利用《数字千年版权法》（DMCA）禁止第三方抓取其搜索结果，为网络抓取和版权法确立了重要的法律先例。 这一裁决明确了搜索引擎结果不属于受 DMCA 保护的版权汇编，可能为更多网络抓取行为打开大门，并影响公司保护其在线数据的方式。 法院驳回了谷歌认为其搜索结果符合 DMCA 下受版权保护的数据库的论点。值得注意的是，谷歌此前已弃用其搜索 API，使得第三方别无选择，只能通过抓取获取数据。

hackernews · cdrnsf · 7月27日 18:15 · [社区讨论](https://news.ycombinator.com/item?id=49073513)

**背景**: 《数字千年版权法》（DMCA）是美国一项法律，规定规避保护版权作品的技术措施属于犯罪。网络抓取是指从网站自动提取数据。谷歌的搜索结果是有序的链接列表，该公司辩称其作为数据库受到版权保护。本案（很可能是 SerpAPI 诉谷歌）测试了抓取公开搜索结果是否构成版权侵权。

**社区讨论**: 社区评论者普遍支持这一裁决，指出谷歌在抓取网络内容的同时反对他人抓取其搜索结果的双重标准。有人指出谷歌弃用了搜索 API，迫使第三方依赖抓取。还有人对比了欧盟和美国关于数据库保护法规的差异。少数评论者强调了抓取对于打击广告欺诈的实际重要性。

**标签**: `#scraping`, `#DMCA`, `#Google`, `#legal`, `#copyright`

---

<a id="item-8"></a>
## [个人基准测试发现 6 个前沿大模型均表现出左倾政治偏见](https://www.reddit.com/r/MachineLearning/comments/1v8fnzw/evaluated_6_frontier_llms_gpt54_claude_sonnet_46/) ⭐️ 8.0/10

一项对六个前沿大模型（GPT-5.4、Claude Sonnet 4.6、Claude Opus 4.7、Gemini Pro、Gemini Flash 和 Grok 4.3）的独立评估，涵盖八个偏见基准测试，发现所有模型均表现出左倾政治倾向，包括自称右倾的 Grok。研究还记录了在种族相关问题上显著的拒绝率，GPT-5.4 在 BBQ 种族数据上的拒绝率达到 20.3%。 这一发现意义重大，因为它与 Grok 自称的政治倾向相矛盾，并表明即使是声称中立的模型也可能存在系统性偏见。了解前沿大模型中偏见的方向和程度，对于在内容审核、招聘和政治讨论等敏感应用中部署这些模型至关重要。 评估使用了八个已建立的偏见/公平性数据集，包括 WinoBias、BBQ（种族/民族）、SeeGULL、OpinionsQA、cajcodes 政治偏见、超党派新闻和政治光谱。这是一项独立的、未经同行评审的项目，没有多次运行平均，每个任务仅使用单一提示模板，这可能会限制其普遍性。

reddit · r/MachineLearning · /u/marggggggggg · 7月27日 22:37

**背景**: 像 BBQ（QA 偏见基准）这样的偏见基准测试通过在有歧义和无歧义的上下文中提出问题，来衡量 AI 系统中的社会偏见。SeeGULL 是一个覆盖多个国家身份群体的广覆盖刻板印象数据集。政治光谱测试是一种常见的工具，用于在经济和社会轴上绘制意识形态立场，并已被改编用于评估大模型的政治倾向。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/2110.08193">[2110.08193] BBQ: A Hand-Built Bias Benchmark for Question Answering</a></li>
<li><a href="https://github.com/google-research-datasets/seegull">GitHub - google-research-datasets/seegull: SeeGULL is a broad-coverage stereotype dataset in English containing stereotypes about identity groups spanning 178 countries across 8 different geo-political regions across 6 continents, as well as state-level identities within the US and India. · GitHub</a></li>
<li><a href="https://www.reddit.com/r/dataisbeautiful/comments/1jc7k1u/oc_political_compass_chart_for_all_major_ai_llm/">[OC] Political Compass chart for all major AI LLM models : ChatGPT, Claude, Gemini, Grok, DeepSeek. (Read submission comment for more details) : r/dataisbeautiful - Reddit</a></li>

</ul>
</details>

**标签**: `#LLM bias`, `#fairness`, `#political bias`, `#frontier models`, `#evaluation`

---