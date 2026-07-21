---
layout: default
title: "Horizon Summary: 2026-07-21 (ZH)"
date: 2026-07-21
lang: zh
---

> 从 39 条内容中筛选出 14 条重要资讯。

---

1. [AI 模型发布：Kimi K3、Qwen 3.8 与 Anthropic 的动荡](#item-1) ⭐️ 9.0/10
2. [Fastjson 1.x 曝无 gadget 高危 RCE 漏洞，无补丁](#item-2) ⭐️ 9.0/10
3. [中国开源 AI 模型威胁西方定价策略](#item-3) ⭐️ 8.0/10
4. [AI 比人类更快找到数学反例](#item-4) ⭐️ 8.0/10
5. [黑客清除罗马尼亚整个土地登记数据库](#item-5) ⭐️ 8.0/10
6. [中国开放权重 AI 模型逐步超越美国专有模型](#item-6) ⭐️ 8.0/10
7. [arXiv 上 AI 写作检测显示高达 39%论文被标记](#item-7) ⭐️ 8.0/10
8. [Altman 2022 年邮件透露 OpenAI 计划开源 GPT-3 模型](#item-8) ⭐️ 8.0/10
9. [Coincidex：无需重放缓冲区的持续学习动态路由方法](#item-9) ⭐️ 8.0/10
10. [Hugging Face 披露 AI 智能体攻击事件](#item-10) ⭐️ 8.0/10
11. [特朗普政府可能限制美国企业使用中国开放权重 AI 模型](#item-11) ⭐️ 8.0/10
12. [美军应用被发现嵌入中俄代码](#item-12) ⭐️ 8.0/10
13. [智谱建成全国产芯片 1 吉瓦数据中心](#item-13) ⭐️ 8.0/10
14. [谷歌开发 Frozen v2 AI 芯片，将 Gemini 嵌入硬件](#item-14) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [AI 模型发布：Kimi K3、Qwen 3.8 与 Anthropic 的动荡](https://www.emergingtrajectories.com/lh/frontier-lab-economics/) ⭐️ 9.0/10

中国实验室 Moonshot AI 和阿里巴巴发布了开源权重模型 Kimi K3 和 Qwen 3.8 Preview，而 Anthropic 因 Claude Design 发布争议面临董事会内部冲突。 这些发布标志着前沿 AI 模型的快速商品化，可能重塑竞争格局，而 Anthropic 的内部动荡引发对其战略方向的质疑。 Kimi K3 拥有 1M token 的上下文窗口，面向智能编码；Qwen 3.8 Preview 是一个 2.4 万亿参数的开源权重模型；Anthropic 的 CPO 在 Claude Design 发布前几天从 Figma 董事会辞职，引发利益冲突猜测。

hackernews · cl42 · 7月20日 15:13 · [社区讨论](https://news.ycombinator.com/item?id=48980019)

**背景**: 开源权重模型允许开发者检查和微调架构，加速了商品化。ASICs（专用集成电路）可以更高效地运行推理，随着模型能力趋同，可能成为关键差异化因素。Figma-Anthropic 事件凸显了产品策略与董事会职责之间的紧张关系。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Kimi_(chatbot)">Kimi (chatbot) - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Qwen3.8-Max">Qwen3.8-Max</a></li>
<li><a href="https://platform.kimi.ai/docs/guide/kimi-k3-quickstart">Kimi K3 - Kimi API Platform</a></li>

</ul>
</details>

**社区讨论**: Hacker News 的评论者讨论了模型商品化是否使 ASICs 成为最终赢家，一些人认为前沿模型已对许多任务'足够好'。其他人关注 Anthropic 的 Figma 董事会辞职，视其为对合作伙伴的背叛。少数评论者注意到炒作周期缩短，暗示可能出现平台期。

**标签**: `#AI`, `#LLM`, `#Anthropic`, `#Open Source`, `#Tech Industry`

---

<a id="item-2"></a>
## [Fastjson 1.x 曝无 gadget 高危 RCE 漏洞，无补丁](https://x.com/k_firsov/status/2078872293745570032) ⭐️ 9.0/10

安全研究员 Kirill Firsov 披露，Fastjson 1.x 版本 1.2.68 至 1.2.83 存在严重远程代码执行漏洞，无需开启 autoType 支持或依赖 classpath gadget，可在 JDK 8/17/21 上利用。Fastjson 1.x 已于 2024 年 10 月停止维护，官方不会发布修复补丁。 该漏洞严重性高，因为无需额外 gadget 即可实现未授权远程代码执行，容易在许多 Java 应用中被利用。Fastjson 1.x 用户必须紧急迁移至 Fastjson2 或开启 SafeMode 以降低风险。 该漏洞不需要开启 autoTypeSupport，也不依赖任何特定的 classpath gadget 链，且能在现代 JDK 版本（8、17、21）上运行。唯一推荐的缓解措施是升级至仍在维护的 Fastjson2，或通过启动参数和配置文件启用 SafeMode。

telegram · zaihuapd · 7月20日 14:32

**背景**: Fastjson 是一个流行的轻量级 Java 库，用于 JSON 字符串与 Java 对象之间的相互转换，广泛应用于阿里及其他生态。安全术语中的 'gadget chain' 是指反序列化时可执行任意代码的一系列类；以往的许多反序列化漏洞需要特定 gadget。此漏洞特别严重，因为它绕过了对 gadget 的需求，使其更具通用性且更易利用。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.baeldung.com/fastjson">A Guide to FastJson | Baeldung</a></li>
<li><a href="https://github.com/alibaba/fastjson">GitHub - alibaba/fastjson: FASTJSON 2.0.x has been released, faster and more secure, recommend you upgrade. · GitHub</a></li>
<li><a href="https://portswigger.net/web-security/deserialization/exploiting">Exploiting insecure deserialization vulnerabilities | Web Security ...</a></li>

</ul>
</details>

**标签**: `#security`, `#java`, `#vulnerability`, `#fastjson`, `#rce`

---

<a id="item-3"></a>
## [中国开源 AI 模型威胁西方定价策略](https://stratechery.com/2026/whos-afraid-of-chinese-models/) ⭐️ 8.0/10

中国实验室正在免费发布高质量的开源 AI 模型，削弱了 Anthropic 和 OpenAI 等西方实验室的高级 API 定价。 这威胁到了西方 AI 实验室的天价估值——这些估值基于对 API 巨额利润的预期——并可能重塑整个 AI 市场和风险投资格局。 Anthropic 估值 1.2 万亿美元，OpenAI 估值 8500 亿美元，但中国开源模型迫使降价和逐底竞争。文章还质疑为什么蒸馏美国模型应该被视为坏事。

hackernews · mfiguiere · 7月20日 11:05 · [社区讨论](https://news.ycombinator.com/item?id=48977128)

**背景**: 大型语言模型（LLM）是训练于海量互联网数据的 AI 系统。OpenAI 和 Anthropic 等前沿实验室对 API 访问收费，而中国实验室免费发布开源模型。蒸馏是利用大型模型训练较小模型的过程，美国公司试图限制这一做法。

**社区讨论**: 评论者指出 AI 工具的切换成本很低，与文章中的粘性说法相矛盾。一位用户观察到其分析网站上有大量中国流量，表明大规模数据中心建设。另一位用户支持文章观点，认为蒸馏美国模型应该被允许，因为 LLM 本身就是从互联网数据蒸馏而来。

**标签**: `#AI`, `#open source`, `#China`, `#venture capital`, `#AI models`

---

<a id="item-4"></a>
## [AI 比人类更快找到数学反例](https://xenaproject.wordpress.com/2026/07/20/human-mathematicians-are-being-outcounterexampled/) ⭐️ 8.0/10

大型语言模型现在能够为数学猜想生成反例，可能在寻找反证方面超越人类数学家。 这一进展可能通过快速否定错误猜想节省数学家的时间，使他们专注于更有前景的问题。还可能将数学家的角色转变为引导 AI，而非进行常规的反例搜索。 来自 Xena Project 博客的文章讨论了 Sol 和 Fable 等 AI 模型如何被用于寻找反例，一些研究生每月支付 200 美元获取访问权限。社区提到一个历史案例：Jacobian 猜想中一个错误的推论影响了张益唐的职业生涯。

hackernews · artninja1988 · 7月20日 19:03 · [社区讨论](https://news.ycombinator.com/item?id=48983382)

**背景**: 数学家经常提出猜想——被认为是真实的陈述——并努力试图证明它们。否定一个猜想通常需要找到一个反例，这可能是一个困难的搜索过程。大型语言模型在大量数学文献上训练，能够探索组合空间并提出人类可能忽略的潜在反例。

**社区讨论**: 评论意见不一：一位用户认为这是好事，可以避免在错误猜想上浪费时间；另一位引用约翰·亨利之歌，质疑人类是否还能胜过机器。第三位评论讲述了个人经历：一个错误推论导致职业困境，暗示 AI 本可帮助。讨论还注意到访问先进模型的成本障碍。

**标签**: `#AI`, `#mathematics`, `#research`, `#large language models`, `#counterexamples`

---

<a id="item-5"></a>
## [黑客清除罗马尼亚整个土地登记数据库](https://news.risky.biz/risky-bulletin-hacker-wipes-romanias-entire-land-registry-database/) ⭐️ 8.0/10

一名黑客入侵了罗马尼亚国家地籍与土地登记局（ANCPI），并清除了整个土地登记数据库，迫使该机构从头重建其网络。 此次攻击威胁到了数百万罗马尼亚人的财产所有权记录，如果备份无法恢复，可能导致大规模社会混乱，凸显了国家关键基础设施的脆弱性。 黑客身份确认为阿尔及利亚的 Zakaria Mahdjoub，声称已删除备份，但官方表示拥有离线副本，并正在将应用程序迁移至政府云。

hackernews · speckx · 7月20日 13:28 · [社区讨论](https://news.ycombinator.com/item?id=48978605)

**背景**: 土地登记是记录财产所有权和交易的关键政府数据库。一旦遭到破坏，可能导致法律纠纷和经济混乱。罗马尼亚的 ANCPI 机构持有全国范围内的记录。

**社区讨论**: 评论者指出，IT 合同授予中的腐败是根本原因，有用户提到任人唯亲导致安全性差。另一位用户推测了引渡的影响，指出阿尔及利亚与罗马尼亚有引渡条约。总体来看，情绪从对社会影响的担忧到对恢复速度的怀疑不等。

**标签**: `#cybersecurity`, `#data breach`, `#critical infrastructure`, `#Romania`, `#land registry`

---

<a id="item-6"></a>
## [中国开放权重 AI 模型逐步超越美国专有模型](https://werd.io/american-ai-is-locked-down-and-proprietary-its-losing/) ⭐️ 8.0/10

文章指出，中国发布开放权重 AI 模型的策略正在取得成功，许多初创公司选择使用这些模型而非美国专有模型，这反映了自由开放技术最终胜出的历史趋势。 这一转变可能重塑全球 AI 格局，使中国在 AI 采用方面获得战略优势，并可能削弱美国科技巨头的统治地位，同时也挑战了只有封闭专有 AI 才能盈利的观念。 文章声称 80%的初创公司使用中国模型，但评论者对此有争议。开放权重模型（如中国发布的）允许用户下载和运行模型权重，但并不一定提供训练数据或代码的完全访问权限，与真正的开源不同。

hackernews · benwerd · 7月20日 14:21 · [社区讨论](https://news.ycombinator.com/item?id=48979269)

**背景**: 开放权重 AI 模型是公开发布的预训练神经网络参数，使开发者能够进行微调和本地部署。这与开源不同，开源需要完全访问训练代码和数据。美国 AI 行业主要专注于专有模型（如 GPT-4、Claude），而中国则积极发布来自阿里巴巴、百度和 DeepSeek 等公司的开放权重模型，以获取广泛采用和生态系统锁定。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://neysa.ai/blog/open-weights-open-source/">Open Weights vs Open Source: What’s the Real Difference?</a></li>
<li><a href="https://opensource.org/ai/open-weights">Open Weights: not quite what you’ve been told – Open Source ...</a></li>

</ul>
</details>

**社区讨论**: 评论者的看法不一。一些人赞同历史类比，认为自由和低端技术（Linux、Windows）击败了专有 Unix。另一些人持怀疑态度，指出许多初创公司仍在使用 Claude 和 Codex 等美国模型，并指出 Meta 的开放权重模型 Llama 并未带来商业成功。还有人怀疑这篇文章可能反映 Palantir CEO 的议程而非客观现实。

**标签**: `#AI`, `#open-source`, `#China`, `#AI strategy`, `#geopolitics`

---

<a id="item-7"></a>
## [arXiv 上 AI 写作检测显示高达 39%论文被标记](https://unslop.run/blog/measuring-ai-writing-on-arxiv) ⭐️ 8.0/10

一项使用自定义调优 AI 检测器的研究发现，截至 2026 年 1 月，大约 39%的 arXiv 论文和 65%的计算机科学论文被标记为 AI 写作，同时在 ChatGPT 之前的论文上保持了低于 0.4%的误报率。 这量化了 LLM 在学术写作中的快速采用，引发了对科学诚信和同行评审可靠性的担忧；同时也凸显了准确检测 AI 的难度，因为 ChatGPT 之前的论文可能被误分类。 检测器经过调优以避免误报，在 ChatGPT 之前的论文上达到 0.4%的检测率；标记阈值设为 42%的机器概率。该研究使用由三个分类器组成的自定义流程分析了 2021 年至 2026 年的论文。

hackernews · dopamine_daddy · 7月20日 16:36 · [社区讨论](https://news.ycombinator.com/item?id=48981206)

**背景**: AI 文本检测器是试图区分人类撰写文本和机器生成文本的工具，但它们常常存在高误报率，并可能被改写技术规避。arXiv 是一个广泛用于物理学、数学、计算机科学及相关领域的预印本仓库。该研究的方法涉及结合多个检测器分数并手动验证子集，但源代码未公开。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/2403.13812">[2403.13812] Quantitative Analysis of AI-Generated Texts in Academic Research: A Study of AI Presence in Arxiv Submissions using AI Detection Tool</a></li>
<li><a href="https://www.pangram.com/blog/all-about-false-positives-in-ai-detectors">All About False Positives in AI Detectors | Pangram Labs</a></li>
<li><a href="https://arxiv.org/abs/2306.15666">[2306.15666] Testing of Detection Tools for AI-Generated Text</a></li>

</ul>
</details>

**社区讨论**: 评论者对检测器的准确性表示怀疑，一些人上传了自己在 LLM 之前的论文并得到高机器分数，质疑检测器是否实际上测量了类似 LLM 的写作风格。另一些人则赞赏在调优以避免误报方面的方法论谨慎，但指出由于源代码不可用，结果无法复现。

**标签**: `#AI detection`, `#arXiv`, `#academic integrity`, `#LLM usage`, `#machine learning`

---

<a id="item-8"></a>
## [Altman 2022 年邮件透露 OpenAI 计划开源 GPT-3 模型](https://simonwillison.net/2026/Jul/20/sam-altman/#atom-everything) ⭐️ 8.0/10

Sam Altman 在 2022 年致 OpenAI 董事会的邮件（于 2026 年 Musk 诉 Altman 案中曝光）中提出，计划发布一个可在消费硬件上本地运行的、能力接近 GPT-3 的语言模型，以阻止 Stability AI 等竞争对手发布类似模型。 这一披露让人罕见地了解到 OpenAI 为抢占先机而开源模型以遏制竞争对手的战略思路，凸显了 AI 行业开源与竞争优势之间的张力。同时，它也反映出业界早期就已认识到本地 LLM 能力的重要性。 邮件日期为 2022 年 10 月 1 日，特别提到要在“Stability 或其他公司之前”发布。该模型将具有“接近 GPT-3 的能力”并可在消费硬件上本地运行，这在 2022 年颇具挑战，但如今通过量化等技术已变得可行。

rss · Simon Willison · 7月20日 03:47

**背景**: 2022 年，GPT-3 是最先进的大语言模型之一，但运行它需要云端访问。OpenAI 考虑发布一个更小、可本地运行的模型，以阻止其他公司开发类似能力。当时 Stability AI 已发布广受欢迎的开源图像生成模型 Stable Diffusion，引发了类似开源 LLM 的担忧。此后，通过量化和强大的 GPU，在消费硬件上本地运行 LLM 已变得实用。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.sitepoint.com/definitive-guide-local-llms-2026-privacy-tools-hardware/">Guide to Local LLMs in 2026: Privacy, Tools & Hardware</a></li>
<li><a href="https://en.wikipedia.org/wiki/Stability_AI">Stability AI</a></li>

</ul>
</details>

**标签**: `#ai-ethics`, `#open-source`, `#openai`, `#gpt-3`, `#sam-altman`

---

<a id="item-9"></a>
## [Coincidex：无需重放缓冲区的持续学习动态路由方法](https://www.reddit.com/r/MachineLearning/comments/1v1rmbb/exploring_continual_learning_without_replay/) ⭐️ 8.0/10

研究人员推出了 Coincidex，这是一个开源的持续学习框架，通过动态任务相似性路由避免使用重放缓冲区，并分享了其成功与失败模式的发现。 这项工作为内存或隐私受限场景下的持续学习提供了一种轻量级替代方案，有望在不存储过去数据的情况下实现更高效、更隐私的顺序学习。 该框架实时计算任务相似性矩阵以路由数据路径，基准测试表明它能够很好地处理清晰的任务边界，但在分布变化剧烈的混乱长尾任务序列中表现欠佳。

reddit · r/MachineLearning · /u/theawkwardbong · 7月20日 17:13

**背景**: 持续学习旨在按顺序训练模型处理多个任务而不遗忘先前任务，这一挑战称为灾难性遗忘。传统方法使用重放缓冲区存储过去样本，但这会带来内存和隐私开销。Coincidex 探索了一种基于路由的方法，根据任务相似性动态引导数据，从而无需存储样本。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://proceedings.mlr.press/v235/wen24f.html">Provable Contrastive Continual Learning</a></li>
<li><a href="https://www.youtube.com/watch?v=vjaq03IYgSk">Continual Learning and Catastrophic Forgetting - YouTube</a></li>

</ul>
</details>

**标签**: `#continual learning`, `#dynamic routing`, `#task-similarity`, `#catastrophic forgetting`, `#open-source`

---

<a id="item-10"></a>
## [Hugging Face 披露 AI 智能体攻击事件](https://huggingface.co/blog/security-incident-july-2026) ⭐️ 8.0/10

Hugging Face 披露了 2026 年 7 月的一起安全事件，攻击者利用数据集处理流程中的两处代码执行漏洞，借助自主 AI 智能体框架入侵内部系统，窃取了部分内部数据集和服务凭证。 该事件凸显了 AI 智能体驱动的攻击风险日益增大，并揭示了一个关键盲点：商业大模型可能因安全护栏而拒绝协助取证分析，从而延缓应急响应。 攻击者在周末期间执行了数万次操作，并在多个内部集群间横向移动。在商业模型 API 被安全护栏拦截后，Hugging Face 改用本地部署的 GLM 5.2 模型完成了超过 1.7 万条攻击记录的取证分析。

telegram · zaihuapd · 7月20日 10:41

**背景**: AI 智能体框架能够自主运行并进行横向移动，正成为高级攻击的日益增长的载体。GLM 5.2 是 Z.ai 开发的大型语言模型，具有 100 万 token 的上下文窗口和强大的推理能力，适用于安全取证等长上下文分析任务。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.sohu.com/a/1005882838_121124365">智能体安全研究：威胁全景、攻击案例、防御技术与治理框架</a></li>
<li><a href="https://www.datalearner.com/ai-models/pretrained-models/glm-5-2">GLM-5.2: Specs, Pricing, Benchmarks & Model Details ...</a></li>
<li><a href="https://gate.ai/zh/blog/glm-5-2-z-ai-specs-pricing-api-use-cases">GLM 5.2：完整规格、定价、API访问与应用场景（2026）</a></li>

</ul>
</details>

**标签**: `#安全`, `#AI智能体`, `#Hugging Face`, `#GLM`, `#供应链安全`

---

<a id="item-11"></a>
## [特朗普政府可能限制美国企业使用中国开放权重 AI 模型](https://www.axios.com/2026/07/20/ai-us-china-open-source-kimi) ⭐️ 8.0/10

据 Axios 报道，特朗普政府正考虑实施新的限制措施，以防止美国企业使用物美价廉的中国开放权重 AI 模型（如 Kimi K3），理由是国家安全担忧。 这一政策转变可能分裂全球 AI 生态系统，增加美国企业的成本，并加剧中美科技紧张局势，可能扼杀开源 AI 创新。 预计限制将是软性的，通过采购规则、实体清单威胁和舆论而非直接禁令实施；白宫 AI 顾问 David Sacks 批评此举是闭源巨头试图消灭开源竞争。

telegram · zaihuapd · 7月20日 11:49

**背景**: 开放权重 AI 模型公开其训练参数，允许任何人下载、运行、研究或修改。由中国初创公司 Moonshot AI 开发的 Kimi K3 自称是全球最大的开放 AI 模型，直接与 Anthropic 和 OpenAI 的领先系统竞争。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://hai.stanford.edu/ai-definitions/what-is-an-open-weight-model">What is an Open-Weight Model? - Stanford HAI</a></li>
<li><a href="https://www.youtube.com/watch?v=6-ccuwX4gCQ">Chinese AI Startup Moonshot Unveils Kimi K 3 Model - YouTube</a></li>

</ul>
</details>

**标签**: `#AI policy`, `#open-source`, `#geopolitics`, `#Kimi K3`, `#US-China`

---

<a id="item-12"></a>
## [美军应用被发现嵌入中俄代码](https://www.wired.com/story/apps-marketed-to-us-troops-are-shipping-chinese-and-russian-code/) ⭐️ 8.0/10

普渡大学等机构的研究人员发现，面向美军推广的 220 多款应用中，近三分之二嵌入了来自中国、俄罗斯等国的第三方代码，其中包括已被美国政府列为国家安全威胁的华为软件开发工具包（SDK）。 这引发了严重的国家安全担忧，因为嵌入的 SDK 可以通过远程更新植入隐藏代码，可能危及敏感的军事数据。它凸显了军事人员软件供应链中的关键漏洞。 这项研究分析了涵盖基地评价、制服指南、银行及约会等类别的 220 多款应用。虽然未观察到数据实际流向华为服务器，但这些 SDK 可随时获取远程更新，存在潜在风险。

telegram · zaihuapd · 7月20日 13:42

**背景**: 第三方 SDK 是开发者嵌入以添加分析或广告等功能的预构建代码库，但如果 SDK 提供商不可信，可能会引入安全风险。供应链安全已成为美国国防部的主要关切，此前国防部曾报告对手利用商业位置数据监视中东美军人员。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.rfi.fr/cn/中国/20260720-美研究-为美军设计的app-有来自中国和俄罗斯软体公司的程式码">美研究：为美军设计的app 有来自中国和俄罗斯软体公司的程式码 - RFI ...</a></li>
<li><a href="https://www.secrss.com/articles/16421">美国国防后勤局《供应链安全战略》浅析 - 安全内参 | 决策者的网络安...</a></li>

</ul>
</details>

**标签**: `#安全`, `#供应链安全`, `#第三方代码`, `#华为SDK`, `#国家安全`

---

<a id="item-13"></a>
## [智谱建成全国产芯片 1 吉瓦数据中心](https://www.bloomberg.com/news/articles/2026-07-20/z-ai-completes-giant-data-center-with-chinese-chips-to-train-ai) ⭐️ 8.0/10

智谱 AI 已完成一座全部采用国产芯片的 1 吉瓦数据中心建设，并已开始部分运营，用于支持其 GLM 平台的训练。 这一里程碑证明了中国利用国产芯片建设大规模 AI 基础设施的能力，减少了对国外供应商的依赖，并推动了国内 AI 生态系统的发展。 该设施功率容量为 1 吉瓦，足以供约 75 万户家庭用电，是中国 AI 实验室建造的最大规模数据中心之一，拥有多个各含上万枚芯片的计算集群。

telegram · zaihuapd · 7月20日 15:43

**背景**: 智谱 AI（即 Z.ai）开发 GLM 系列大语言模型，包括 GLM-4.5 和 GLM-5.2 等开源版本。2025 年 1 月，该公司被列入美国实体清单，从而推动了国产芯片的使用。该数据中心是确保 AI 模型训练独立性的战略举措。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/GLM_(AI)">GLM (AI) - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Zhipu_AI">Zhipu AI</a></li>
<li><a href="https://www.businessinsider.com/what-is-glm-5-2-chinese-ai-coding-model-2026-6">What is GLM-5.2? Another open-source Chinese AI model has Silicon Valley's attention.</a></li>

</ul>
</details>

**标签**: `#AI infrastructure`, `#Chinese chips`, `#data center`, `#large-scale computing`, `#GLM`

---

<a id="item-14"></a>
## [谷歌开发 Frozen v2 AI 芯片，将 Gemini 嵌入硬件](https://www.quiverquant.com/news/Google+Reportedly+Developing+%E2%80%98Frozen+v2%E2%80%99+AI+Chip+to+Boost+Gemini+Efficiency) ⭐️ 8.0/10

据一份报告，谷歌正在开发一款代号为“Frozen v2”的新型 AI 服务器芯片，将 Gemini 模型的部分能力直接写入硬件，旨在实现每瓦特 token 数达到最新 TPU 的 6 到 10 倍，目标 2028 年部署。 该芯片可大幅提升 AI 推理效率，有望降低能源成本并缓解 Google Cloud 的算力短缺，同时标志着将模型架构嵌入硅片的专用 AI 硬件趋势。 Frozen v2 设计为补充而非取代谷歌的 TPU 产品线，是专为 Gemini 工作负载定制的加速器。该芯片通过将 Gemini 架构部分固化到硬件中，减少了计算量和数据移动。

telegram · zaihuapd · 7月21日 01:01

**背景**: 谷歌的张量处理单元（TPU）是用于神经网络工作负载的定制专用集成电路（ASIC）。虽然 TPU 是通用 AI 加速器，但 Frozen v2 是一种更专业的芯片，将模型特定逻辑嵌入硬件，可提高效率但降低灵活性。这种方法与一些公司为特定模型或运算优化芯片的方式类似。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.cnbc.com/2026/07/20/alphabet-googl-stock-ai-chip-report.html">Alphabet stock pops on report it's developing a more efficient AI chip</a></li>
<li><a href="https://qz.com/google-gemini-chip-frozen-tpu-efficiency-072026">Google developing Gemini-specific chip called Frozen v2</a></li>

</ul>
</details>

**标签**: `#AI`, `#hardware`, `#chip`, `#Google`, `#Gemini`

---