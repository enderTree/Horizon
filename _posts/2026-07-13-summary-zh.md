---
layout: default
title: "Horizon Summary: 2026-07-13 (ZH)"
date: 2026-07-13
lang: zh
---

> 从 34 条内容中筛选出 8 条重要资讯。

---

1. [GPT-5.6 证 50 年图论猜想](#item-1) ⭐️ 10.0/10
2. [陶哲轩探索 AI 编程代理构建应用](#item-2) ⭐️ 9.0/10
3. [xAI Grok CLI 默认上传整个代码库及密钥文件](#item-3) ⭐️ 9.0/10
4. [OpenAI 发布 GPT-5.6 系列：Sol、Terra、Luna 三款模型](#item-4) ⭐️ 9.0/10
5. [全球首款侵入式脑机接口医疗器械中国获批](#item-5) ⭐️ 9.0/10
6. [Chromium 148 中 Math.tanh 可实现操作系统指纹识别](#item-6) ⭐️ 8.0/10
7. [George Hotz：LLM 创造价值，但炒作误导估值](#item-7) ⭐️ 8.0/10
8. [北京官员用 Claude Code 打造 AI 防洪 App](#item-8) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [GPT-5.6 证 50 年图论猜想](https://www.qbitai.com/2026/07/447873.html) ⭐️ 10.0/10

OpenAI 的 GPT-5.6 Sol Ultra 使用 64 个子代理和一份约 700 个字符的详细提示，在一小时内证明了图论中已存在 50 年的循环双覆盖猜想。该模型生成了一个 3 页 PDF 的证明。 这一成就表明人工智能能够自主进行原创数学研究，可能彻底改变数学发现的步伐。它标志着在使用具有并行推理架构的大型语言模型处理复杂理论问题方面的范式转变。 该模型使用了 64 个并行子代理，将问题分解为有限域上的边标号和线性方程组。OpenAI 还发布了完整的提示，其中指定了验收标准、定义、边界条件和失败情形，而没有规定固定的解题步骤。

telegram · zaihuapd · 7月12日 03:49

**背景**: 循环双覆盖猜想由 Szekeres 和 Seymour 在 1970 年代独立提出，询问每个无桥无向图是否都有一个循环集合，使得每条边恰好被覆盖两次。子代理是专门的 AI 组件，它们在主代理的协调下并行处理任务的不同方面。这种方法允许大规模推理并高效利用资源。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Cycle_double_cover_conjecture">Cycle double cover conjecture</a></li>
<li><a href="https://ai-sdk.dev/docs/agents/subagents">Subagents - Agents</a></li>

</ul>
</details>

**标签**: `#AI`, `#mathematics`, `#graph theory`, `#GPT-5.6`, `#breakthrough`

---

<a id="item-2"></a>
## [陶哲轩探索 AI 编程代理构建应用](https://terrytao.wordpress.com/2026/07/11/old-and-new-apps-via-modern-coding-agents/) ⭐️ 9.0/10

知名数学家陶哲轩于 2026 年 7 月 11 日发表博客，描述现代 AI 编程代理（如 Cursor 和 Zencoder）如何促进新旧应用的创建，突显了软件巨大的潜在需求。 这很重要，因为它展示了基于大语言模型的编程代理正在使软件创作民主化，使非编程领域的专家也能构建以前无法实现的工具，有望加速跨学科创新。 陶哲轩指出，虽然 LLM 编写的补充内容并非关键任务，但使用 LLM 代理引导交互来生成可视化效果的下行风险是可以接受的，这反映了对 AI 工具平衡的看法。

hackernews · subset · 7月12日 11:09 · [社区讨论](https://news.ycombinator.com/item?id=48880170)

**背景**: AI 编程代理是利用大语言模型辅助编写代码的工具，通常通过自然语言提示实现。例如，Cursor 是一款 AI 驱动的代码编辑器，Zencoder 是一个 AI 代码生成平台。这些代理降低了软件开发的门槛，使编码经验有限的用户也能创建功能性应用。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://zencoder.ai/">Zencoder | The AI Coding Agent</a></li>
<li><a href="https://cursor.com/">Cursor: AI coding agent</a></li>

</ul>
</details>

**社区讨论**: 社区评论对陶哲轩的探索表达了热情和幽默。例如，“recursivedoubts”分享了 LLMs 如何提升他的计算机科学课程，“luciana1u”开玩笑说菲尔兹奖得主也开始使用编程代理。“semiquaver”强调软件在传统领域之外有无限潜在需求，“wffurr”则赞赏陶哲轩对使用 LLM 代理可接受风险的平衡观点。

**标签**: `#AI coding agents`, `#LLMs`, `#software development`, `#education`, `#Terry Tao`

---

<a id="item-3"></a>
## [xAI Grok CLI 默认上传整个代码库及密钥文件](https://gist.github.com/cereblab/dc9a40bc26120f4540e4e09b75ffb547) ⭐️ 9.0/10

安全研究人员发现，xAI 的 Grok Build CLI 工具（版本 0.2.93）默认将整个代码仓库及 .env 等敏感文件上传到 xAI 服务器，即使关闭“改进模型”设置也无法阻止。 这一安全漏洞会暴露开发者的专有代码和机密信息，可能导致数据泄露，危及使用该工具的所有项目的软件安全。 该工具通过两个渠道上传代码：文件内容嵌入模型对话请求，同时以 git bundle 形式上传至 Google Cloud Storage，实验中一个 12 GB 的仓库上传了超过 5 GiB 的数据。

telegram · zaihuapd · 7月12日 04:19

**背景**: Grok Build 是一个基于终端的编码智能体，由 xAI 的 Grok 模型驱动，于 2026 年 5 月发布。它旨在直接从命令行执行命令并辅助开发。git-bundle 命令可将 Git 对象打包为单个文件用于离线传输，CLI 工具利用此功能将整个仓库发送至 xAI 服务器。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://x.ai/news/grok-build-cli">Introducing Grok Build | SpaceXAI</a></li>
<li><a href="https://x.ai/cli">Grok Build | SpaceXAI</a></li>
<li><a href="https://git-scm.com/docs/git-bundle">Git - git - bundle Documentation</a></li>

</ul>
</details>

**标签**: `#安全`, `#隐私`, `#xAI`, `#CLI工具`, `#代码泄露`

---

<a id="item-4"></a>
## [OpenAI 发布 GPT-5.6 系列：Sol、Terra、Luna 三款模型](https://t.me/zaihuapd/42512) ⭐️ 9.0/10

OpenAI 正式发布 GPT-5.6 系列，推出三款不同定位的模型：旗舰级 Sol、平衡型 Terra 和低成本 Luna，各自针对性能与成本进行了优化。该系列在代码、知识工作、设计、科研和网络安全方面大幅提升，并引入了 max/ultra 推理、多智能体协作和 Programmatic Tool Calling 等新功能。 此次发布扩展了 OpenAI 的模型阵容，更好地满足从高性能任务到成本敏感部署的不同场景，使先进 AI 更加易用。多智能体协作和程序化工具调用的引入标志着向更自主、更高效的 AI 工作流转变，可能改变开发者构建复杂应用的方式。 每百万 token 定价为：Sol 输入 $5 / 输出 $30，Terra 输入 $2.50 / 输出 $15，Luna 输入 $1 / 输出 $6。裸 gpt-5.6 API 别名默认指向 Sol，显式模型 ID 为 gpt-5.6-sol、gpt-5.6-terra 和 gpt-5.6-luna。Programmatic Tool Calling 允许模型在沙箱环境中编写代码调用工具，减少 API 往返次数。

telegram · zaihuapd · 7月12日 11:19

**背景**: OpenAI 的 GPT-5.6 系列是基于前几代 GPT 模型的大语言模型家族。三种档次——Sol、Terra、Luna——让用户根据应用选择最佳的性能、速度和成本平衡。多智能体协作是指多个 AI 智能体协调解决复杂任务；Programmatic Tool Calling 使模型能够通过代码以编程方式调用外部工具，提高效率和可靠性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openai.com/index/previewing-gpt-5-6-sol/">Previewing GPT-5.6 Sol: a next-generation model | OpenAI</a></li>
<li><a href="https://www.mindstudio.ai/blog/what-is-gpt-5-6-soul-terra-luna-explained">What Is GPT-5.6? OpenAI's Soul, Terra, and Luna Model Tiers Explained | MindStudio</a></li>
<li><a href="https://www.vellum.ai/blog/gpt-5-6-benchmarks-explained">GPT-5.6 Sol vs Terra vs Luna: Which Tier Should You Actually Use?</a></li>

</ul>
</details>

**标签**: `#GPT`, `#OpenAI`, `#AI models`, `#machine learning`, `#natural language processing`

---

<a id="item-5"></a>
## [全球首款侵入式脑机接口医疗器械中国获批](https://t.me/zaihuapd/42515) ⭐️ 9.0/10

国家药监局批准了全球首款侵入式脑机接口医疗器械——博睿康医疗科技（上海）有限公司开发的“植入式脑机接口手部运动功能代偿系统”，用于颈段脊髓损伤所致四肢瘫患者的临床治疗。 这一批准标志着神经技术领域范式转变，将侵入式脑机接口从实验室推向获批临床设备，有望恢复瘫痪患者的手部功能并改善其生活质量。 该设备采用硬脑膜外微创植入与无线供能通信技术，连接气动手套，帮助 18-60 岁四肢瘫患者实现手部抓握动作。临床试验显示患者手部抓握能力显著提升。

telegram · zaihuapd · 7月12日 14:39

**背景**: 侵入式脑机接口是通过外科手术植入、在大脑与外部设备之间建立直接通信路径的装置。传统侵入式 BCI 需开颅并将电极植入脑组织，而该新设备采用微创硬脑膜外植入方式——将电极放置在硬脑膜上而不穿透大脑。无线供能与数据传输消除了经皮导线的需求，降低了感染风险。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://flcube.com/?p=59388">China NMPA Approves World's First Invasive BCI Medical Device...</a></li>
<li><a href="https://en.wikipedia.org/wiki/Brain–computer_interface">Brain–computer interface - Wikipedia</a></li>

</ul>
</details>

**标签**: `#brain-computer interface`, `#medical device`, `#neurotechnology`, `#spinal cord injury`, `#China`

---

<a id="item-6"></a>
## [Chromium 148 中 Math.tanh 可实现操作系统指纹识别](https://scrapfly.dev/posts/browser-math-os-fingerprint/) ⭐️ 8.0/10

自 Chromium 148 起，V8 中的 Math.tanh 函数不再使用内置数学库，而是调用宿主操作系统的 libm 实现，因此可以通过测量浮点运算结果的差异来识别底层操作系统。 这打开了一个难以伪造的浏览器指纹识别新途径，即便用户修改了用户代理字符串，也能静默检测其操作系统，这引发了严重的隐私担忧，并使反指纹识别工作变得更加复杂。 在 JavaScript 数学函数中，只有 Math.tanh 会泄露操作系统信息，因为 Chrome 148 将其实现替换为平台特定的 std::tanh；其他函数如 Math.cos 在不同平台上保持一致。此外，CSS 三角函数和 Web Audio API 也表现出类似的平台依赖行为。

hackernews · joahnn_s · 7月12日 21:12 · [社区讨论](https://news.ycombinator.com/item?id=48884853)

**背景**: 浏览器指纹识别通过收集设备和软件属性来识别用户，无需使用 Cookie。传统上，该技术依赖于屏幕分辨率、字体或用户代理字符串。Math.tanh 指纹识别利用了不同操作系统因数学库和 CPU 架构差异而在计算超越函数时产生的细微差别，从而为每个平台创建一致的签名。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://scrapfly.dev/posts/browser-math-os-fingerprint/">Your Browser Does Math Differently on Every OS , and Anti-Bot...</a></li>
<li><a href="https://news.ycombinator.com/item?id=48884853">Since Chromium 148, Math.tanh is now fingerprintable to link underlying OS | Hacker News</a></li>
<li><a href="https://asibiont.com/en/blog/since-chromium-148-math-tanh-teper-mozhno-ispolzovat-dlya-privyazki-k-os-chto-eto-znachit-dlya-veb-razrabotchikov">Chromium 148 : How Math . tanh Became... — ASI Biont Blog</a></li>

</ul>
</details>

**社区讨论**: 社区评论指出，该指纹识别向量可能不仅揭示操作系统，还能揭示浏览器版本范围。一些人质疑这篇报道背后的动机，怀疑反爬虫公司可能从修复这些技术中获益。另一些人则认为，这凸显了跨平台正确舍入超越函数的必要性。

**标签**: `#browser fingerprinting`, `#privacy`, `#Chromium`, `#Math.tanh`, `#web security`

---

<a id="item-7"></a>
## [George Hotz：LLM 创造价值，但炒作误导估值](https://geohot.github.io//blog/jekyll/update/2026/07/12/i-love-llms.html) ⭐️ 8.0/10

George Hotz 发表博文，指出虽然大型语言模型创造巨大价值，但前沿 AI 实验室可能无法捕获这些价值，并且 LLM 正在将开源动态转向私有分支而非向上游贡献。 这一观点挑战了 OpenAI 和 Anthropic 等前沿实验室的高估值，表明价值创造并不保证价值捕获，这对投资者和 AI 行业具有启示意义。它还突显了对开源软件的微妙影响：LLM 使分支如此容易，可能会减少协作上游贡献。 该文章强调，LLM 正被用于构建针对特定个人用例的一次性简化软件，导致了一个'随心所欲'的时代，分支比向上游贡献更受青睐。Hotz 还指出，前沿模型订阅价格（100-200 美元/月）仍然具有成本效益，但价值流向用户，而不一定流向模型提供商。

hackernews · therepanic · 7月12日 18:31 · [社区讨论](https://news.ycombinator.com/item?id=48883343)

**社区讨论**: 评论者普遍同意 Hotz 关于价值捕获的论点，指出 LLM 带来的生产力提升导致私有工具而非公共贡献。一些人对开源未来表示担忧，而另一些人则提到像 Sonnet 4 和 Opus 4.5 这样的新模型感觉像是阶段性变化，加速了进展并使时间线变得不确定。

**标签**: `#LLM`, `#open source`, `#hype`, `#valuation`, `#productivity`

---

<a id="item-8"></a>
## [北京官员用 Claude Code 打造 AI 防洪 App](https://www.xieyunshi.com/blog/?id=11) ⭐️ 8.0/10

北京市规划和自然资源委员会密云分局副局长谢陨石自购 100 亿个 token，耗时近一个月，使用 Claude Code 自主开发了名为'叫应'的防洪 App。 这展示了 AI 编码工具在公共安全领域的创新应用，可能激励其他政府官员利用 AI 进行本地灾害响应。 该 App 整合了地质灾害隐患点、受威胁险户及包保人员信息，实时更新山体预警、雨情变化和群众转移状态，并支持一键导航至隐患点。

telegram · zaihuapd · 7月12日 15:16

**背景**: Claude Code 是 Anthropic 开发的 AI 编码代理，能理解代码库、编辑文件并运行命令。在 AI 中，token 是语言模型处理的最小文本单位；100 亿个 token 对于个人项目而言是相当可观的算力消耗。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Claude_Code">Claude Code</a></li>
<li><a href="https://blogs.nvidia.com/blog/ai-tokens-explained/">What Are AI Tokens ? The Language and Currency... | NVIDIA Blog</a></li>
<li><a href="https://claude.com/product/claude-code">Claude Code by Anthropic | AI Coding Agent, Terminal, IDE</a></li>

</ul>
</details>

**标签**: `#AI coding`, `#disaster response`, `#Claude Code`, `#public sector`, `#innovation`

---