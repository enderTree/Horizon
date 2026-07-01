---
layout: default
title: "Horizon Summary: 2026-07-01 (ZH)"
date: 2026-07-01
lang: zh
---

> 从 41 条内容中筛选出 14 条重要资讯。

---

1. [Claude Code 在请求中秘密嵌入隐写标记](#item-1) ⭐️ 9.0/10
2. [美国解除对 Claude Fable 5 和 Mythos 5 的出口管制](#item-2) ⭐️ 9.0/10
3. [Claude Sonnet 5 发布：代理能力最强，接近 Opus 性能](#item-3) ⭐️ 9.0/10
4. [Anthropic 推出面向数据科学的 Claude Science](#item-4) ⭐️ 8.0/10
5. [通过 WebAssembly 将 Kubernetes 移植到浏览器](#item-5) ⭐️ 8.0/10
6. [DIY 毫米波雷达实现材料分类助力石棉检测](#item-6) ⭐️ 8.0/10
7. [TokenBudgeting：重新思考企业 AI Token 支出](#item-7) ⭐️ 8.0/10
8. [REAP：自动策展编程智能体基准测试](#item-8) ⭐️ 8.0/10
9. [Claude Code 2.1.91 隐蔽遥测探测中国用户](#item-9) ⭐️ 8.0/10
10. [小红书前员工举报合规风险](#item-10) ⭐️ 8.0/10
11. [谷歌向开发者推出 Nano Banana 2 Lite 和 Gemini Omni Flash](#item-11) ⭐️ 8.0/10
12. [Anthropic 发布 Claude Sonnet 4.6，性能大幅提升](#item-12) ⭐️ 8.0/10
13. [特斯拉宣布监督版 FSD 在中国可用](#item-13) ⭐️ 8.0/10
14. [Vercel 现支持通过 Dockerfile 部署容器](#item-14) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Claude Code 在请求中秘密嵌入隐写标记](https://thereallo.dev/blog/claude-code-prompt-steganography) ⭐️ 9.0/10

Anthropic 的 Claude Code 工具被发现会在请求中嵌入隐写水印，很可能是为了检测竞争对手进行的未授权模型蒸馏。这一做法通过逆向工程被揭露，并引发了关于透明度和信任的争论。 这一发现削弱了用户对 Anthropic 透明度的信任，因为用户并未被告知存在隐藏的数据外泄行为。它还引发了关于在开发工具中未经披露使用隐写技术的伦理和安全问题。 隐写标记嵌入在发送给 Claude API 的提示中，该技术据称较为粗糙，增加了被检测到的风险。其意图似乎是识别从事模型蒸馏的中国公司的使用情况，但未披露的做法可能违反用户信任和隐私期望。

hackernews · kirushik · 6月30日 15:44 · [社区讨论](https://news.ycombinator.com/item?id=48734373)

**背景**: 隐写术是将数据隐藏在其他数据中的做法，例如在图像或文本中嵌入秘密信息。模型蒸馏是一种让较小模型从较大模型中学习的技术，常用于创建强大的 AI 模型的低成本本地版本。像 Anthropic 这样的公司投入大量资源训练大型模型，可能希望防止竞争对手未经许可蒸馏其模型的能力。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Model_distillation">Model distillation</a></li>

</ul>
</details>

**社区讨论**: 社区意见存在分歧：一些人批评缺乏透明度，认为这是对信任的背叛；另一些人则认为意图明确，并且不会伤害普通开发者。少数评论者指出实现方式草率，并且有更隐蔽的方法可以达到相同目的。还有人将 Codex CLI 的开源性质与此对比，认为其更值得信赖。

**标签**: `#steganography`, `#Anthropic`, `#AI ethics`, `#security`, `#transparency`

---

<a id="item-2"></a>
## [美国解除对 Claude Fable 5 和 Mythos 5 的出口管制](https://twitter.com/AnthropicAI/status/2072106151890809341) ⭐️ 9.0/10

美国商务部已解除对 Anthropic 的 Claude Fable 5 和 Claude Mythos 5 模型的出口管制，允许更广泛的国际部署。 这一政策转变标志着 AI 监管的重大举措，可能影响全球对先进 AI 模型的访问，并引发关于商业关键应用监管和可靠性的辩论。 值得注意的是，由于针对网络安全任务的分类器，Claude Fable 5 最初将限制编码能力，日常编码和调试将回退到 Opus 4.8。

hackernews · Pragmata · 6月30日 23:55 · [社区讨论](https://news.ycombinator.com/item?id=48740771)

**背景**: Claude Fable 5 是 Anthropic 最强大的广泛发布模型，用于高要求推理和长周期任务，而 Claude Mythos 5 旨在发现软件漏洞，仅通过 Project Glasswing 有限发布。最初实施出口管制是因为类似核技术的双重用途担忧。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Claude_Fable_5">Claude Fable 5</a></li>
<li><a href="https://www.anthropic.com/claude/fable">Claude Fable \ Anthropic</a></li>
<li><a href="https://platform.claude.com/docs/en/about-claude/models/introducing-claude-fable-5-and-claude-mythos-5">Introducing Claude Fable 5 and Claude Mythos 5 - Claude Platform Docs</a></li>

</ul>
</details>

**社区讨论**: 社区情绪复杂：有人认为缺乏可预测性破坏了美国前沿模型的信任，而另一些人质疑 AI 是否应像核技术一样受监管。有用户指出解除管制同时限制编码能力的讽刺，还有人强调过程中缺乏国会批准。

**标签**: `#AI regulation`, `#export controls`, `#Anthropic`, `#government policy`

---

<a id="item-3"></a>
## [Claude Sonnet 5 发布：代理能力最强，接近 Opus 性能](https://t.me/zaihuapd/42280) ⭐️ 9.0/10

Anthropic 发布了 Claude Sonnet 5，称其为迄今代理能力最强的 Sonnet 模型，能够规划、使用浏览器和终端等工具并自主运行。它在推理、工具使用、编码和知识工作上优于 Sonnet 4.6，性能接近 Opus 4.8，但价格更低。 此次发布大幅降低了获取接近旗舰级别代理能力的成本，可能加速自主 AI 智能体在开发和企业工作流中的采用。它以更低的价格提供强劲性能，挑战了竞争对手，重塑了 LLM 市场的性价比格局。 Claude Sonnet 5 即日起面向所有套餐开放，并成为 Free 和 Pro 用户的默认模型。在 Claude Platform 上，限时价格截至 2026 年 8 月 31 日，每百万输入 token 为 2 美元，输出 token 价格未公布。

telegram · zaihuapd · 7月1日 01:12

**背景**: Anthropic 的 Claude 模型通常按三个层级发布：Haiku（最快/最便宜）、Sonnet（均衡）和 Opus（能力最强）。代理推理指 LLM 能够自主规划、使用工具和执行任务，无需持续人工监督。Sonnet 5 旨在弥合成本与代理能力之间的差距。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Claude_(language_model)">Claude (language model)</a></li>
<li><a href="https://platform.claude.com/docs/en/about-claude/models/overview">Models overview - Claude Platform Docs</a></li>
<li><a href="https://towardsdev.com/the-rise-of-agentic-reasoning-how-llms-are-evolving-from-thinkers-to-doers-3eaf896bf097">The Rise of Agentic Reasoning: How LLMs Are Evolving... | Towards Dev</a></li>

</ul>
</details>

**社区讨论**: 一些评论者指出，对于需要超过中等努力水平的任务，Opus 通常提供更好的每美元性能，建议用户切换模型而非增加努力级别。其他人指出 Sonnet 5 在漏洞发现和琐事方面表现不佳，其性价比与 GLM-5.2 相当但成本翻倍。

**标签**: `#AI`, `#大语言模型`, `#Claude`, `#Anthropic`, `#模型发布`

---

<a id="item-4"></a>
## [Anthropic 推出面向数据科学的 Claude Science](https://claude.com/product/claude-science) ⭐️ 8.0/10

Anthropic 发布了 Claude Science，这是一款数据科学工具，通过本地服务器和基于 Web 的 UI 与高性能计算（HPC）系统和数据库集成。 该产品对科学计算意义重大，尤其是在制药和生物技术等受到严格监管的行业，它能够在安全的机构基础设施上实现 AI 辅助数据分析。 Claude Science 运行一个本地服务器，连接到用户的浏览器，提供与机构 HPC 集群和各种数据库的集成。它生成可审计的工件，并支持计算设计任务，例如 RNAi 生物农药设计。

hackernews · lebovic · 6月30日 17:07 · [社区讨论](https://news.ycombinator.com/item?id=48735770)

**背景**: 高性能计算（HPC）用于复杂的科学模拟和数据分析，通常处于安全环境中，外部云连接受限。数据科学工具如 Jupyter Notebooks 很常见，但可能无法很好地与机构集群集成。Claude Science 通过提供连接现有 HPC 和数据库资源的本地服务器架构来解决这一问题。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.anthropic.com/news/claude-science-ai-workbench">Claude Science, an AI workbench for scientists \ Anthropic</a></li>
<li><a href="https://www.technologyreview.com/2026/06/30/1139987/claude-science-is-anthropics-newest-flagship-product/">Claude Science is Anthropic’s newest flagship product</a></li>
<li><a href="https://en.wikipedia.org/wiki/High-performance_computing">High-performance computing - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 社区评论强调，Claude Science 的架构（本地服务器 + Web UI）非常适合受严格监管的制药环境。一位为 Biomni 构建了集成 HPC 工具的贡献者指出，它的价值远不止于绘图。用户报告称，在 RNAi 生物农药工作中成功进行了单次设计，但也指出了方法幼稚和脱靶筛选有限等注意事项。

**标签**: `#AI`, `#data science`, `#HPC`, `#Anthropic`, `#scientific computing`

---

<a id="item-5"></a>
## [通过 WebAssembly 将 Kubernetes 移植到浏览器](https://ngrok.com/blog/i-ported-kubernetes-to-the-browser) ⭐️ 8.0/10

ngrok 的一位开发者使用 WebAssembly 将 Kubernetes 的子集移植到浏览器中，创建了名为 Webernetes 的项目，无需任何后端服务器组件即可启动完整的 Kubernetes 集群。 这使得 Kubernetes 概念可以在无需云资源的情况下用于教育目的，并展示了 WebAssembly 在浏览器中运行复杂基础设施软件的能力日益增强。 该项目重新实现了 Kubernetes 核心组件（如 API 服务器、调度器和控制器管理器），使用 TypeScript 编写并编译为 WebAssembly，而不是移植原始的 Go 代码，以保持包体积可控。

hackernews · peterdemin · 6月30日 20:48 · [社区讨论](https://news.ycombinator.com/item?id=48738985)

**背景**: Kubernetes 是一个用于自动化容器化应用程序的部署、扩展和管理的开源平台。WebAssembly（Wasm）是一种二进制指令格式，能够在 Web 浏览器中实现高性能执行，最初设计用于客户端应用，但现在越来越多地用于服务器端和可移植工作负载。将 Kubernetes 移植到 Wasm 需要重新实现原始 Go 代码所依赖的操作系统级抽象。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/ngrok/webernetes">GitHub - ngrok/webernetes: Kubernetes in the browser.</a></li>

</ul>
</details>

**社区讨论**: 评论者称赞了其教育价值，并指出它可以改善概念学习，类似于之前的 Katacoda 等平台。一些人担心由于复制 Kubernetes 源代码而导致的维护问题，而另一些人则认为开发工作流——使用 LLM 编写代码并针对真实 Kubernetes 行为进行测试——比项目本身更有趣。

**标签**: `#Kubernetes`, `#WebAssembly`, `#education`, `#browser`, `#LLM`

---

<a id="item-6"></a>
## [DIY 毫米波雷达实现材料分类助力石棉检测](https://gauthier-lechevalier.com/radar) ⭐️ 8.0/10

一位开发者使用德州仪器 IWRL6432 和 ESP32 开发板构建了一款毫米波材料分类雷达，其概念验证能够区分常见材料，并有望用于非侵入式石棉检测。该项目以详细的文章形式分享，包括经验教训。 该项目展示了低成本、开源硬件的材料分类方法，有望解决建筑中普遍存在的石棉检测问题（当前检测需要侵入式取样）。同时，它为毫米波雷达和硬件黑客社区提供了宝贵的工程经验。 该雷达使用 FMCW（调频连续波）信号和基于频谱图的机器学习来分类材料。作者指出，当前原型尚未证明能一致地区分含石棉材料与其对应物，也未解决浓度敏感性问题。

hackernews · GL26 · 6月30日 17:29 · [社区讨论](https://news.ycombinator.com/item?id=48736137)

**背景**: 毫米波雷达工作在 30-300 GHz 频段，能够穿透非金属材料，因此适用于感知隐藏物体或材料特性。FMCW 雷达是一种常见类型，可测量距离，并通过分析反射信号用于材料分类。DIY 雷达项目常使用低成本评估模块，如 TI IWRL6432 Boost 板。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://gauthier-lechevalier.com/radar">How I built a mmWave material classification radar</a></li>
<li><a href="https://aicrier.com/post/tpq50o2kiwtxvzoa6ac2">Student builds mmWave radar for asbestos detection — AICrier</a></li>
<li><a href="https://sesamedisk.com/mmwave-radar-material-classification-industrial/">Millimeter-Wave Radar for Material - Sesame Disk</a></li>

</ul>
</details>

**社区讨论**: 评论者称赞该项目分享了失败教训，有人认为这种学习是无价的。一位用户提出关键点：核心的石棉检测功能未经验证，因为概念验证只分类了常见材料。另一位用户建议其他应用，如检测材料中的不连续性用于皮肤癌检测。

**标签**: `#mmWave`, `#radar`, `#material classification`, `#hardware`, `#DIY`

---

<a id="item-7"></a>
## [TokenBudgeting：重新思考企业 AI Token 支出](https://newsletter.semianalysis.com/p/tokenbudgeting-our-conversations) ⭐️ 8.0/10

文章《TokenBudgeting》质疑了 AI 使用中 Token 最大化（TokenMaxxing）的普遍性，指出许多企业实际上更注重 Token 预算管理和高效消费。 这一分析挑战了 TokenMaxxing 作为生产力指标的热点，可能改变企业的成本管理策略和 AI 部署实践。 该文章来自信誉良好的 SemiAnalysis，报道了与企业对话的结果，显示企业实际关注 Token 预算而非最大化消费，这与流行叙事相反。

rss · Semianalysis · 6月30日 18:32

**背景**: TokenMaxxing 是一种通过最大化 AI Token 消耗来显得高产的做法，通常在内部排行榜上追踪。Token 是大语言模型（LLM）使用的计算单位。相比之下，TokenBudgeting 强调成本控制和 AI 资源的高效使用。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Token_maxxing">Token maxxing - Wikipedia</a></li>
<li><a href="https://www.inc.com/ben-sherry/what-is-tokenmaxxing-ai-productivity-hack/91328999">What Is ‘Tokenmaxxing’? The Controversial AI Productivity Metric</a></li>

</ul>
</details>

**标签**: `#AI`, `#token economy`, `#enterprise`, `#LLM`, `#cost management`

---

<a id="item-8"></a>
## [REAP：自动策展编程智能体基准测试](https://www.reddit.com/r/MachineLearning/comments/1uk713d/reap_automatic_curation_of_coding_agent/) ⭐️ 8.0/10

REAP 是一个自动化管道，无需人工标注即可从真实生产编码助手会话中策展基于执行的基准测试。 它解决了静态基准测试的局限性，为 AI 编程智能体提供更相关、更多样的评估，影响 AI/ML 和编码工具生态系统。 REAP 用于策展 Harvest 基准测试，其中的任务提供真实开发者提示，并根据从生产中获取的失效到通过测试验证代码更改，涵盖超过四种编程语言。

reddit · r/MachineLearning · /u/julian88888888 · 7月1日 00:50

**背景**: 编程智能体基准测试通常是静态且手动创建的，限制了其相关性。REAP 自动从真实生产使用日志中提取任务，使用失效到通过测试验证正确性，从而提高了基准测试质量。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/2604.01527">[2604.01527] REAP: Automatic Curation of Coding Agent ...</a></li>
<li><a href="https://arxiv.org/html/2604.01527v3">REAP: Automatic Curation of Coding Agent Benchmarks from ...</a></li>
<li><a href="https://www.semanticscholar.org/paper/REAP:-Automatic-Curation-of-Coding-Agent-Benchmarks-Jha-Paltenghi/b106bab30b9fdbf890b1fcf1a0dae725f00904a4">REAP: Automatic Curation of Coding Agent Benchmarks from ...</a></li>

</ul>
</details>

**标签**: `#coding agents`, `#benchmarks`, `#machine learning`, `#AI evaluation`

---

<a id="item-9"></a>
## [Claude Code 2.1.91 隐蔽遥测探测中国用户](https://www.reddit.com/r/ClaudeAI/comments/1ujila1/anthropic_embedded_spyware_in_claude_code_and/) ⭐️ 8.0/10

这引发了严重的透明度和隐私担忧，因为遥测功能被混淆且未在更新日志中披露，专门针对中国用户检测未经授权的转售或滥用行为，而用户对此毫不知情。 该遥测使用 XOR 密钥 91 混淆逻辑，检查时区如 Asia/Shanghai 以及指向中国 AI 实验室的代理 URL，然后修改系统提示中日期字段的 Unicode 撇号来编码结果，实际上将提示词变成了隐蔽的数据通道。

telegram · zaihuapd · 6月30日 10:34

**背景**: XOR 混淆是一种常见于恶意软件的技术，通过与密钥进行按位异或操作来隐藏恶意逻辑。LLM 中的隐写术涉及在提示词或输出中嵌入隐藏信息而不改变其表面含义。此事件与一些远程访问木马（RAT）使用的策略类似，这些木马通过 XOR 和 Base64 编码隐藏配置。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://gbhackers.com/millenium-rat-uses-base64-and-xor/">Millenium RAT Uses Base64 and XOR Configuration to Hide ...</a></li>
<li><a href="https://www.threatdown.com/blog/nowhere-to-hide-three-methods-of-xor-obfuscation/">Nowhere to Hide: Three methods of XOR obfuscation</a></li>
<li><a href="https://www.emergentmind.com/topics/steganographic-capabilities-in-llms">Steganography in LLMs: Techniques & Security</a></li>

</ul>
</details>

**标签**: `#Claude Code`, `#telemetry`, `#privacy`, `#AI ethics`, `#reverse engineering`

---

<a id="item-10"></a>
## [小红书前员工举报合规风险](https://www.163.com/dy/article/L0M7BHUT0511ADM5.html) ⭐️ 8.0/10

前小红书员工陈浩于 6 月 29 日向港交所和香港证监会提交实名合规投诉，指控公司在境外期权、用工合规和信息披露方面存在隐患。小红书计划于 2026 年 6 月底递交港股 IPO 材料，估值约 310 亿美元。 合规举报正值小红书筹备高调 IPO 的关键时刻，可能影响监管审批和投资者信心。该事件凸显了中国科技公司中持续的劳动法和期权争议，强调了寻求海外上市的公司遵守 ESG 合规的重要性。 陈浩此前已获得违法解除劳动合同赔偿金 190624 元及期权损失调解赔付 661545 元。他声称近 50 名离职员工有类似情况，要求小红书澄清境内外主体关系的信披矛盾、披露用工诉讼及 ESG 劳工缺陷。

telegram · zaihuapd · 6月30日 13:33

**背景**: 小红书是中国知名的社交电商平台，以用户生成的美妆、时尚和生活内容闻名。多年来一直传闻计划在香港 IPO。期权是初创公司吸引人才的常见手段，但关于归属和离职的争议可能引发法律纠纷。ESG（环境、社会和治理）标准对在香港上市的公司越来越重要。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.163.com/dy/article/L0N3JJ7H0519A26B.html">遭“内部人”实名举报！小红书的红与黑|期权|电商|ipo|知名企业_网易订...</a></li>
<li><a href="https://www.sohu.com/a/1043825752_120321309">小红书关键时刻，前员工向港交所实名举报_期权_上市_陈浩</a></li>
<li><a href="https://www.topnews.cn/news/145CD7E447B84E75">独家丨期权临期被解约，小红书前员工维权获法院判赔85万</a></li>

</ul>
</details>

**标签**: `#IPO`, `#compliance`, `#labor law`, `#Xiaohongshu`, `#tech regulation`

---

<a id="item-11"></a>
## [谷歌向开发者推出 Nano Banana 2 Lite 和 Gemini Omni Flash](https://blog.google/innovation-and-ai/models-and-research/gemini-models/gemini-omni-flash-nano-banana-2-lite/) ⭐️ 8.0/10

谷歌发布了 Nano Banana 2 Lite（其最快、成本效益最高的图像生成模型，延迟 4 秒，每千张图片成本 0.034 美元）和 Gemini Omni Flash（首度向开发者开放的视频生成模型，输出视频每秒 0.10 美元）。 这些发布大幅降低了生成式媒体的成本和延迟，使设计、广告和社交应用中的快速迭代成为可能，并通过 API 让开发者能获取高质量视频生成能力。 Nano Banana 2 Lite 现已在 Google AI Studio、Gemini API 和 Gemini Enterprise Agent Platform 中正式可用，并即将进入搜索 AI Mode 和 Gemini app 等消费端产品。Gemini Omni Flash 目前支持文本、图像和视频输入生成 10 秒视频，但在 API 中暂不支持音频参考和场景延展，跨场景角色一致性仍有限。

telegram · zaihuapd · 6月30日 16:14

**背景**: 这类生成式 AI 模型能让计算机根据文字描述创建图像或视频，常用于原型设计、内容创作和市场营销。Nano Banana 2 Lite 属于谷歌 Gemini 图像模型系列，针对速度和成本效率进行了优化；而 Gemini Omni Flash 是一种原生多模态视频生成模型，使用谷歌的张量处理单元（TPU）训练，最早在 Google I/O 2026 上宣布。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://blog.google/innovation-and-ai/models-and-research/gemini-models/gemini-omni-flash-nano-banana-2-lite/">Start building with Nano Banana 2 Lite and Gemini Omni Flash</a></li>
<li><a href="https://deepmind.google/models/gemini-image/flash-lite/">Gemini 3.1 Flash- Lite Image – Nano Banana ... — Google DeepMind</a></li>
<li><a href="https://cloud.google.com/blog/products/ai-machine-learning/nano-banana-2-lite-and-gemini-omni-flash-available/">Nano Banana 2 Lite and Gemini Omni Flash available | Google ...</a></li>

</ul>
</details>

**标签**: `#Google AI`, `#generative models`, `#image generation`, `#video generation`, `#cost efficiency`

---

<a id="item-12"></a>
## [Anthropic 发布 Claude Sonnet 4.6，性能大幅提升](https://t.me/zaihuapd/42277) ⭐️ 8.0/10

Anthropic 发布了 Claude Sonnet 4.6 模型，在编程、计算机操作和长文本推理方面有了显著改进。该模型现已成为 Free 和 Pro 用户的默认版本，并支持 100 万 token 的上下文窗口。 此次发布标志着领先 AI 助手的一次重大升级，增强了开发者和高级用户的实用性。特别是改进的计算机使用能力，扩展了 Claude 在自动化复杂桌面任务方面的实际价值。 该模型的计算机使用能力在 OSWorld 基准测试中取得了显著进步，该基准评估代理在真实操作系统上的任务表现。Claude Sonnet 4.6 已通过 API 和主流云平台上线，定价保持不变。

telegram · zaihuapd · 6月30日 17:58

**背景**: Anthropic 的 Claude Sonnet 是一款中端模型，在性能和成本之间取得平衡，定位介于轻量级 Haiku 和旗舰 Opus 之间。计算机使用是一项功能，允许 Claude 直接导航和控制计算机界面，从而跨应用实现工作流程自动化。OSWorld 基准测试评估 AI 代理在 Ubuntu 环境中执行真实计算机任务的能力。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.anthropic.com/news/3-5-models-and-computer-use">Introducing computer use, a new Claude 3.5 Sonnet, and Claude ...</a></li>
<li><a href="https://os-world.github.io/">OSWorld : Benchmarking Multimodal Agents for Open-Ended Tasks in...</a></li>

</ul>
</details>

**标签**: `#Anthropic`, `#Claude`, `#AI`, `#LLM`, `#Machine Learning`

---

<a id="item-13"></a>
## [特斯拉宣布监督版 FSD 在中国可用](https://t.me/zaihuapd/42281) ⭐️ 8.0/10

特斯拉今早在社交媒体 X 上宣布，其监督版完全自动驾驶（FSD）软件现已在中国可用。 这标志着特斯拉的自动驾驶技术正式进入全球最大的汽车市场，可能加剧与本土厂商如小鹏和华为的竞争。 监督版 FSD 系统要求驾驶员持续监督，并不能使车辆完全自动驾驶，特斯拉的支持文档已明确说明。

telegram · zaihuapd · 7月1日 01:22

**背景**: 特斯拉的完全自动驾驶（FSD）是一种高级驾驶辅助系统，可以在高速公路和城市道路上导航、变道并遵循路线。然而，尽管名称如此，它并非完全自动驾驶，需要一名警惕的驾驶员随时准备接管。最近采用的'监督版'一词正是为了强调这一限制。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.tesla.com/fsd">Full Self-Driving (Supervised) - Tesla</a></li>
<li><a href="https://www.tesla.com/support/fsd">Full Self-Driving (Supervised) | Tesla Support</a></li>
<li><a href="https://insideevs.com/news/714524/tesla-fsd-beta-supervised-name/">Tesla Full Self-Driving Comes Out Of Beta, But Must Be Supervised</a></li>

</ul>
</details>

**标签**: `#Tesla`, `#FSD`, `#autonomous driving`, `#China`

---

<a id="item-14"></a>
## [Vercel 现支持通过 Dockerfile 部署容器](https://vercel.com/blog/dockerfile-on-vercel) ⭐️ 8.0/10

Vercel 宣布支持通过 Dockerfile.vercel 文件部署 Docker 容器，让开发者可以在 Vercel 的 Fluid compute 平台上运行任何 HTTP 容器，并具有自动缩放和基于 CPU 的计费功能。 这扩展了 Vercel 平台的范围，从无服务器函数到容器化应用，使开发者能够无缝运行 Rails、Spring Boot 和 FastAPI 等框架，并采用按使用付费的定价模式。 Dockerfile.vercel 文件必须放在项目根目录；Vercel 会构建、存储和部署镜像，服务必须监听 $PORT（默认 80）并提供 HTTP 服务。每次 git push 都会触发重建并生成预览 URL。

telegram · zaihuapd · 7月1日 03:58

**背景**: Vercel 是一个面向前端开发者的云平台，最初专注于无服务器函数。Fluid compute 是 Vercel 的执行模型，可以在单个容器实例上并发处理多个请求，减少空闲时间。Dockerfile 支持允许开发者使用任何可以在容器中运行的语言或框架。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://vercel.com/docs/functions/container-images">Deploy OCI container images with a Dockerfile or Containerfile on...</a></li>
<li><a href="https://vercel.com/fluid">Fluid compute</a></li>

</ul>
</details>

**标签**: `#Vercel`, `#Docker`, `#container deployment`, `#serverless`, `#cloud computing`

---