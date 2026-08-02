---
layout: default
title: "Horizon Summary: 2026-08-02 (ZH)"
date: 2026-08-02
lang: zh
---

> 从 35 条内容中筛选出 6 条重要资讯。

---

1. [OpenAI 称 Astra 模型在十个长期数学难题上取得突破](#item-1) ⭐️ 9.0/10
2. [NetBSD 11.0 发布，带来防火墙增强与 MicroVM 内核](#item-2) ⭐️ 8.0/10
3. [KataGo 作者研究围棋网络内部对称性](#item-3) ⭐️ 8.0/10
4. [VLM 在基准测试中得分高，却删除临床术语并引入偏见](#item-4) ⭐️ 8.0/10
5. [微软确认今年推出 Copilot「超级应用」](#item-5) ⭐️ 8.0/10
6. [AI 芯片每 9 个月翻番，2028 年将达 2 亿颗](#item-6) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [OpenAI 称 Astra 模型在十个长期数学难题上取得突破](https://simonwillison.net/2026/Aug/1/ten-advances-in-mathematics/#atom-everything) ⭐️ 9.0/10

OpenAI 宣布，其下一代模型 Astra 的内部版本在十个至少十年未获重大进展的数学与理论计算机科学问题上取得了进展。该公司表示，按 GPT-5.6 Sol 的 token 价格计算，每个问题的成本不到 2000 美元，并发布了 Lean 4 形式化证明及相关论文。 这是前沿 AI 模型能够以较低 token 成本完成真正困难数学研究的显著例证，可能加速数学等领域数十年来停滞不前的问题取得突破。事件也加剧了 OpenAI 与 Anthropic 之间的竞争，并引发关于人类在数学研究中角色的深刻思考。 OpenAI 的公告没有披露未成功尝试的问题数量，也没有公开所用的提示词。成果包括 openai/ten-proofs 仓库中的 Lean 4 形式化证明、一篇论文，以及模型根据推理轨迹生成的复盘 PDF；所涉及的问题据报道涵盖高维球体堆积、非索菲克群、Connes 刚性猜想、算术电路下界、量子并行重复、最近向量问题及多色 Ramsey 数等。

rss · Simon Willison · 8月1日 20:34

**背景**: 该公告紧随 Anthropic 的宣称——其未发布的 Claude Mythos Preview 模型以约 10 万美元的 token 成本发现了密码学弱点，显示出前沿实验室正将 AI 用于开放性研究。Lean 4 是一种交互式定理证明器，可机械验证数学证明，因此 OpenAI 发布形式化证明被视为重要的透明度举措。陶哲轩曾描述向‘大数学’的转变——人类与机器大规模协作，由 AI 承担大部分技术工作。这一消息在数学界引发了类似‘Deep Blue’时刻的情绪，如 Kirwin Hampshire 的文章《数学的暗夜》表达了对 AI 影响的忧虑。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://the-decoder.com/openai-announces-its-next-major-model-astra-by-dropping-ten-previously-unsolved-math-solutions/">OpenAI announces its "next major model" Astra by dropping ten previously unsolved math solutions</a></li>
<li><a href="https://openrouter.ai/openai/gpt-5.6-sol">GPT-5.6 Sol - API Pricing & Benchmarks | OpenRouter</a></li>
<li><a href="https://en.wikipedia.org/wiki/Claude_Mythos">Claude Mythos - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: Simon Willison 称赞了透明度，但要求公开提示词，并指出未披露失败情况。据文章所述，网上数学家的普遍反应是敬畏与存在性焦虑交织的‘Deep Blue’时刻，Kirwin Hampshire 的《数学的暗夜》等文章突显了这种心理冲击。

**标签**: `#AI`, `#mathematics`, `#theoretical computer science`, `#OpenAI`, `#research`

---

<a id="item-2"></a>
## [NetBSD 11.0 发布，带来防火墙增强与 MicroVM 内核](https://blog.netbsd.org/tnf/entry/netbsd_11_0_released) ⭐️ 8.0/10

NetBSD 11.0 已发布，带来了 npf 防火墙的重大改进、面向 x86 的全新快速启动 MICROVM 内核，以及多项硬件增强。 这一重大版本表明历史悠久的开源 NetBSD 项目仍在积极开发且保持相关。全新的 microVM 内核可能为虚拟化和边缘计算带来新的应用场景。 发布公告指出，虽然仍存在未解决的问题，但本版本解决的问题远多于其引入的问题。NPF 防火墙的改进包括二层过滤和用户/组过滤，面向 x86 的 MICROVM 内核可在约 10 毫秒内启动。

hackernews · jaypatelani · 8月1日 17:56 · [社区讨论](https://news.ycombinator.com/item?id=49136736)

**背景**: NetBSD 是一款免费开源、类 Unix 的操作系统，属于 BSD 家族，以其可移植性和简洁设计著称。NPF 是 NetBSD 的包过滤防火墙，提供状态检测、NAT 和 IP 集合等功能。microVM 是一种专为快速启动和低开销设计的轻量级虚拟机，常用于无服务器和边缘计算。新的 MICROVM 内核利用了这一概念，可在约 10 毫秒内完成启动。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.koyeb.com/blog/what-is-a-microvm">What is a microVM ? - Koyeb</a></li>
<li><a href="https://northflank.com/blog/what-is-a-microvm">What is a microVM ? | Blog — Northflank</a></li>
<li><a href="https://rmind.github.io/npf/configuration.html">NPF : packet filter with stateful inspection, NAT, IP sets, etc.</a></li>

</ul>
</details>

**社区讨论**: 评论者讨论了 BSD 与 Linux 相比的现状和相关性，一些人称赞 npf 的二层和用户/组过滤功能以及 10 毫秒的启动时间。一位评论者指出发布公告对已知问题态度坦诚，并认为该版本关闭的问题可能比引入的更多。还有一位评论者分享了使用 NetBSD 进行分子动力学模拟的怀旧故事。

**标签**: `#NetBSD`, `#BSD`, `#Operating System`, `#Release`, `#Open Source`

---

<a id="item-3"></a>
## [KataGo 作者研究围棋网络内部对称性](https://www.reddit.com/r/MachineLearning/comments/1vcrki2/how_symmetric_are_the_insides_of_a_go_network_r/) ⭐️ 8.0/10

KataGo 作者发布了一项新的可解释性研究，探讨超人类水平的围棋神经网络是学到与方向无关的内部概念，还是对每种旋转和镜像分别记忆信息。研究发现，这些网络处理对称性的方式出乎意料。 这项工作为神经网络可解释性做出了贡献，目前人们对深度模型内部表示的理解仍然不足。研究结果或可帮助研究人员在视觉、物理和分子建模等具有已知对称性的领域中设计更好的归纳偏置。 该研究分析了开源围棋引擎 KataGo，其网络训练时使用随机 8 倍数据增强，而非显式的对称性约束。值得注意的是，这项研究及其文章撰写大量借助了 AI 辅助，但有人类进行详细指导和反馈，代码也已在文章中公开链接。

reddit · r/MachineLearning · /u/icosaplex · 8月1日 16:18

**背景**: 围棋是一种规则在旋转和镜像下完全不变的棋类游戏，但 KataGo 的神经网络没有在架构上强制这种对称性，而是在训练时使用随机 8 倍数据增强来随机调整每个训练批次的朝向。这项研究探讨了超人类水平的围棋网络从这种间接信号中学到了多少与方向无关的概念。KataGo 是著名的开源围棋 AI 引擎，水平已超越职业棋手。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://katagotraining.org/">KataGo Distributed Training</a></li>
<li><a href="https://geekpython.in/data-augmentation-in-deep-learning">An Intuitive Guide On Data Augmentation In Deep Learning ...</a></li>

</ul>
</details>

**标签**: `#ML interpretability`, `#neural networks`, `#Go`, `#symmetry`, `#KataGo`

---

<a id="item-4"></a>
## [VLM 在基准测试中得分高，却删除临床术语并引入偏见](https://www.reddit.com/r/MachineLearning/comments/1vcipzz/vlms_can_score_well_on_benchmarks_while_silently/) ⭐️ 8.0/10

该论文揭示，用于胸部 X 光报告生成的视觉语言模型（VLM）可能在基准测试中得高分，同时悄然删除有临床意义的罕见术语并引入有偏见的术语。作者提出了一个衡量这些问题的框架，称为临床关联位移（CAD）和加权关联擦除（WAE）。 当前医学 AI 的评估指标存在缺陷，因此看似高准确率的模型可能生成无临床价值甚至有偏见的放射学报告。这对自动化报告生成在医疗领域的安全部署具有严重影响。 该框架中的临床关联位移（CAD）是一种词汇级方法，用于量化生成报告中基于人口统计的词关联变化，而加权关联擦除（WAE）则汇总这些变化，以衡量跨人群的临床信号损失。作者还指出，基准指标会奖励重复性模板和缺乏临床术语的“正常”报告。

reddit · r/MachineLearning · /u/ade17_in · 8月1日 09:27

**背景**: 视觉语言模型（VLM）是一类能同时理解图像和文本的 AI 系统，可用于从胸部 X 光片生成放射学报告。放射学报告生成（RRG）旨在减轻医生工作负担，但由于医学报告包含罕见却关键的临床术语，评估难度很大。该论文指出，标准基准指标可能被重复、模糊的语言所欺骗，从而掩盖有意义临床信息的丢失。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Vision-language_model_(VLM)">Vision-language model (VLM)</a></li>
<li><a href="https://pmc.ncbi.nlm.nih.gov/articles/PMC12292164/">Advancements in Radiology Report Generation : A Comprehensive...</a></li>
<li><a href="https://arxiv.org/html/2603.01625">Measuring What VLMs Don’t Say: Validation Metrics Hide Clinical ...</a></li>

</ul>
</details>

**标签**: `#VLM`, `#Radiology Report Generation`, `#Evaluation Metrics`, `#Medical AI`, `#Bias`

---

<a id="item-5"></a>
## [微软确认今年推出 Copilot「超级应用」](https://www.theverge.com/tech/972927/microsoft-copilot-super-app-confirmed) ⭐️ 8.0/10

微软 CEO 萨蒂亚·纳德拉在财报电话会议上确认，公司将于今年推出一款 AI「超级应用」，把 Copilot 聊天、代码功能和智能体能力整合在一起，同时面向消费者和企业。该应用将合并 Copilot、GitHub Copilot、Copilot Cowork 和 Autopilot 等系统。 这证实了微软一个重要的产品方向，标志着其从独立的 AI 助手转向统一的「超级应用」战略，可能改变用户使用 AI 工具的方式。这也加剧了与 OpenAI 的竞争——后者最近也推出了类似的整合型应用 ChatGPT Work。 纳德拉表示，Copilot 正从聊天工具演进到「Cowork」和「Autopilot」，公司本季度将把这些体验（包括代码功能）合并进一款应用。微软上季度营收增至 900 亿美元，主要由 AI 和云业务推动。

telegram · zaihuapd · 8月1日 13:18

**背景**: Copilot 是微软嵌入到其产品中的 AI 助手系列，GitHub Copilot 则帮助开发者编写代码。Copilot Cowork 是较新的功能，能代表用户执行任务，如发送邮件、安排会议、管理日历，并具有企业级安全合规保护。Autopilot 指的是 AI 智能体在有限监督下自主完成多步骤任务的模式。这些概念反映了行业向 agentic AI（智能体 AI）发展的趋势，即系统能自主感知、推理和行动。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://learn.microsoft.com/en-us/microsoft-365/copilot/cowork/">Copilot Cowork overview | Microsoft Learn</a></li>
<li><a href="https://www.microsoft.com/en-us/microsoft-365/blog/2026/03/09/copilot-cowork-a-new-way-of-getting-work-done/">Copilot Cowork: A new way of getting work done | Microsoft 365 Blog</a></li>
<li><a href="https://mitsloan.mit.edu/ideas-made-to-matter/agentic-ai-explained">Agentic AI, explained | MIT Sloan</a></li>

</ul>
</details>

**标签**: `#Microsoft`, `#Copilot`, `#AI`, `#Super App`, `#Agents`

---

<a id="item-6"></a>
## [AI 芯片每 9 个月翻番，2028 年将达 2 亿颗](https://www.nytimes.com/interactive/2026/07/29/technology/ai-chips-data-center-boom.html) ⭐️ 8.0/10

据 Epoch AI 估算，全球 AI 芯片目前约 2000 万颗，每 9 个月翻一番，预计到 2028 年底将达到约 2 亿颗。IDC 预测，到 2029 年全球 AI 基础设施投资将突破 1 万亿美元，而去年为 3180 亿美元。 AI 算力的爆发式增长凸显了“规模定律”在 AI 进步中的主导作用，并加剧了地缘政治竞争，因为美国控制着全球约 80%的 AI 算力。这也引发了经济与环境方面的担忧，即大规模投资能否持续而不导致泡沫。 这一趋势由“规模定律”驱动——即算力越大，AI 能力越强。据信仅 Google 一家的 AI 芯片数量就是中国所有公司总和的四倍，而中国正通过自研半导体和 AI 基础设施建设加速追赶。

telegram · zaihuapd · 8月2日 01:01

**背景**: 神经网络的规模定律是经验性规律，描述 AI 性能如何随模型参数、训练数据和算力的增加而提升。Epoch AI 是一家研究机构，通过关于训练算力、模型参数和硬件能力的综合数据库追踪 AI 发展趋势，其预测在关于 AI 进展和基础设施投资的讨论中被广泛引用。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Neural_scaling_law">Neural scaling law - Wikipedia</a></li>
<li><a href="https://blogs.nvidia.com/blog/ai-scaling-laws/">How Scaling Laws Drive Smarter, More Powerful AI - NVIDIA Blog</a></li>
<li><a href="https://epoch.ai/about">About Us | Epoch AI</a></li>

</ul>
</details>

**标签**: `#AI chips`, `#AI infrastructure`, `#scaling laws`, `#data centers`, `#investment trends`

---