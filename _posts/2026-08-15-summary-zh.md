---
layout: default
title: "Horizon Summary: 2026-08-15 (ZH)"
date: 2026-08-15
lang: zh
---

> 从 33 条内容中筛选出 12 条重要资讯。

---

1. [GLM-5.3：具备涌现网络能力的前沿编程模型](#item-1) ⭐️ 9.0/10
2. [PostgreSQL 修复高危 to_char 漏洞，可致任意代码执行](#item-2) ⭐️ 9.0/10
3. [Qwen 3.8 27B 发布：开源权重本地大模型表现抢眼](#item-3) ⭐️ 8.0/10
4. [“Going Dark”时代终结：执法部门从漏洞转向后门](#item-4) ⭐️ 8.0/10
5. [批评：Opus 5 的省略式、面向智能体的语言让人类体验更差](#item-5) ⭐️ 8.0/10
6. [Firefox 成为最后仍支持 uBlock Origin 的主流浏览器](#item-6) ⭐️ 8.0/10
7. [开发者将 Doom 渲染器编译为 210 亿参数 Transformer，无需训练](#item-7) ⭐️ 8.0/10
8. [AI 机器人实验室年测 300 万人体样本，有望取代动物试验](#item-8) ⭐️ 8.0/10
9. [小红书开源 dots3-note：280B MoE 仅 16B 激活参数](#item-9) ⭐️ 8.0/10
10. [美国法官限期谷歌一周内移除第三方应用商店安装障碍](#item-10) ⭐️ 8.0/10
11. [苹果 CEO 库克 2026 年卸任，特努斯接任](#item-11) ⭐️ 8.0/10
12. [苹果自研中国专属 AI 大模型，联手阿里或成首个获批外企](#item-12) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [GLM-5.3：具备涌现网络能力的前沿编程模型](https://z.ai/blog/glm-5.3) ⭐️ 9.0/10

Z.ai（智谱 AI）发布了最新旗舰模型 GLM-5.3。该模型基于 GLM-5.2 的底座，通过后训练显著提升了复杂软件工程与长周期智能体任务能力，并在社区测试和 CVE 协调披露中展现出自主发现与利用漏洞的涌现性网络能力。 前沿编程模型出现涌现性网络能力，意味着智能体可以比人类防御者更快、更大规模地发现并利用漏洞，这是一个重要转折。这可能从根本上影响软件安全、CVE 处理流程以及安全研究的方式。 GLM-5.3 与 GLM-5.2 使用相同底座，所有改进都来自后训练，并提供三档思考强度与 1M 上下文窗口。Z.ai 还通过 cvd.z.ai 披露其在流行开源及商业软件中发现的漏洞，其中许多处于保密期的 CVE 被评定为严重或高危。

hackernews · pella · 8月14日 05:19 · [社区讨论](https://news.ycombinator.com/item?id=49294997)

**背景**: 前沿编程模型是专注于软件工程和智能体任务的大型语言模型，例如编写代码、修复缺陷以及编排多步骤工作。所谓“涌现能力”，是指只有在模型规模达到一定程度时才会出现的、并非被显式训练出来的全新技能。后训练（post-training）指在基础模型预训练之后进行的额外微调或对齐。协调漏洞披露（CVD）是研究者先私下向厂商报告漏洞、再公开披露的流程，通常以 CVE 编号跟踪。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://docs.z.ai/guides/llm/glm-5.3">GLM - 5 . 3 - Overview - Z. AI DEVELOPER DOCUMENT</a></li>
<li><a href="https://models.dev/models/zhipuai/glm-5.3/">GLM - 5 . 3 pricing, providers, and specs | Models .dev</a></li>
<li><a href="https://www.emergentmind.com/topics/emergent-capabilities">Emergent Capabilities in AI</a></li>

</ul>
</details>

**社区讨论**: 有评论者分享了令人印象深刻的实测结果，包括模型主动接受红队安全测试、利用 WordPress 插件中的 0-day、适配 6.8 内核漏洞利用，甚至与另一个 GLM 智能体进行攻防对抗。也有人认为该模型与 Sol、Fable 等竞品仍略有差距，并质疑相比 OpenAI 在经济学上是否足够有吸引力；同时有人赞赏 Z.ai 的写作风格更像研究者而非营销炒作。此外，评论中也有对大规模漏洞扫描成本不断下降的担忧。

**标签**: `#AI`, `#ML`, `#Cybersecurity`, `#GLM`, `#Coding`

---

<a id="item-2"></a>
## [PostgreSQL 修复高危 to_char 漏洞，可致任意代码执行](https://www.postgresql.org/support/security/CVE-2026-14669/) ⭐️ 9.0/10

PostgreSQL 披露了高危漏洞 CVE-2026-14669，这是 to_char(timestamptz) 函数中的堆缓冲区溢出，可让已认证的低权限用户执行任意代码。修复版本为 18.6、17.11、16.15、15.19 和 14.24。 该漏洞非常严重，因为它允许低权限的已认证用户获得数据库服务器上的操作系统级代码执行能力，影响所有受支持的 PostgreSQL 版本。数据库管理员应立即修复以防止被利用。 该漏洞在 to_char 处理超长 POSIX 时区缩写时触发堆缓冲区溢出。CVSS 评分为 8.8，但利用需要低权限数据库账户；此小版本更新不需要转储/重载或 pg_upgrade，只需替换程序文件并重启服务。

telegram · zaihuapd · 8月14日 14:35

**背景**: 堆缓冲区溢出是指程序向堆分配的内存缓冲区写入超过其容量的数据，从而破坏内存并可能导致代码执行。to_char 函数用于将时间戳转换为格式化的字符串，而 POSIX 时区规范定义了时区缩写和偏移量；攻击者可利用超长的缩写引发缓冲区溢出，最终以 PostgreSQL 服务进程的权限执行任意代码。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://hackerdna.com/blog/buffer-overflow">Buffer Overflow Explained: How the Attack Works (2026) | HackerDNA</a></li>
<li><a href="https://orbisappsec.com/blog/heap-buffer-overflow-in-darktables-color-chart-how">Heap Buffer Overflow in darktable's Color | Orbis AppSec</a></li>
<li><a href="https://postgrespro.com/docs/postgrespro/9.6/datetime-posix-timezone-specs">Postgres Pro Standard : Documentation: 9.6: B.5. POSIX Time Zone ...</a></li>

</ul>
</details>

**标签**: `#PostgreSQL`, `#security`, `#CVE`, `#vulnerability`, `#database`

---

<a id="item-3"></a>
## [Qwen 3.8 27B 发布：开源权重本地大模型表现抢眼](https://huggingface.co/Qwen/Qwen3.8-27B-FP8) ⭐️ 8.0/10

Qwen 3.8 27B 是阿里 Qwen 系列新发布的开源权重本地大模型，这次 FP8 版本一经推出便受到关注。用户反馈其推理能力表现出色，并且思考痕迹的书写风格与 Qwen 3.6 等旧版本明显不同，呈现独特的笔记式表达。 这一发布进一步证明，具备较强推理能力的大语言模型可以在消费级硬件上本地运行，降低对云端 API 的依赖。同时它也显示，美国之外的研究团队正在推出能与顶级闭源模型竞争的开源权重模型，这可能会重塑本地模型生态。 社区测试显示，在某个私有基准上，它成为继 Gemma 4 之后第二个正确通过的本地模型，但为此花费了约 5 倍的 token 数量，并在开启 MTP 时耗时 12 分 30 秒。有用户在 RTX 5090 上通过 ninfer 引擎获得约 138 tokens/s 的速度，约为朴素 llama.cpp 配置的两倍；不过它的 VRAM 使用效率似乎低于 Gemma 4 或 Glimmer。

hackernews · erdaltoprak · 8月14日 15:00 · [社区讨论](https://news.ycombinator.com/item?id=49299605)

**背景**: Qwen 是阿里云打造的大语言模型家族，许多版本以 Apache 2.0 等开源或开放许可发布，支持本地部署和商用。'开放权重'意味着模型的权重参数公开，但训练数据、完整代码和完整训练方法不一定公开，因此不等同于完全开源。具备推理能力的大模型会先生成逐步的链式思考内容再给出答案，这种 'thinking trace' 是社区讨论 Qwen 3.8 27B 时的焦点。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Qwen">Qwen - Wikipedia</a></li>
<li><a href="https://huggingface.co/Qwen">Org profile for Qwen on Hugging Face, the AI community building the...</a></li>
<li><a href="https://research.google/blog/thinking-to-recall-how-reasoning-unlocks-parametric-knowledge-in-llms/">Thinking to recall: How reasoning unlocks parametric knowledge in...</a></li>

</ul>
</details>

**社区讨论**: 评论总体非常正面，许多用户认为这是目前最适合本地运行的模型之一，并称赞它在私有测试中的表现超过了 Laguna 和 Muse Glimmer。也有用户提到其'原始人般'的思考痕迹风格、VRAM 占用较高，以及 MTP 预测可能被这种痕迹拖累等问题；还有人由此看到非美国大厂模型快速崛起的趋势。

**标签**: `#LLM`, `#Qwen`, `#Local Models`, `#AI`, `#Open Source`

---

<a id="item-4"></a>
## [“Going Dark”时代终结：执法部门从漏洞转向后门](https://blog.cryptographyengineering.com/2026/08/14/everything-is-about-to-go-dark/) ⭐️ 8.0/10

一位密码学专家认为，执法部门正从利用软件漏洞转向施压企业安插后门，开启大规模监控黑客的时代。 这一观点重新定义了“Going Dark”的争论：执法部门可能不再接受加密带来的限制，而是要求削弱系统安全性。这将影响所有软件用户的隐私与安全，而不仅仅是罪犯。 文章认为，可利用的软件漏洞终将枯竭，从而推动政府通过法律强制要求植入后门。评论者还指出，“Going Dark”具有误导性，因为监控摄像头、元数据和公司数据共享之下，真正“黑暗”的空间已所剩无几。

hackernews · vslira · 8月14日 20:52 · [社区讨论](https://news.ycombinator.com/item?id=49304447)

**背景**: “Going Dark”是联邦调查局等执法机构使用的说法，指即使持有法院令状，也无法读取加密通信。为此，执法部门越来越多地采用黑客工具，通过利用软件漏洞未经授权访问设备。这种做法引发了法律与隐私方面的担忧，尤其是在政府讨论是否要求企业预留后门的背景下。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://archives.fbi.gov/archives/news/testimony/going-dark-lawful-electronic-surveillance-in-the-face-of-new-technologies">FBI — Going Dark : Lawful Electronic Surveillance in the Face of New...</a></li>
<li><a href="https://www.newamerica.org/insights/brief-history-law-enforcement-hacking-united-states/">A Brief History of Law Enforcement Hacking in the... - New America</a></li>
<li><a href="https://www.techdirt.com/2020/01/06/there-is-no-going-dark-always-on-surveillance-posing-risks-to-us-covert-operations/">There Is No ' Going Dark :' Always-On Surveillance Posing... | Techdirt</a></li>

</ul>
</details>

**社区讨论**: 评论者对“漏洞枯竭”的说法表示怀疑，认为 AI 生成的代码可能带来更多漏洞，而不是更少。也有人预测，如果漏洞用尽，政府将迫使企业植入后门，尽管量子系统最终可能让窃听变得可被察觉。还有评论嘲讽“Going Dark”的说法，指出摄像头无处不在、元数据被收集、平台数据被共享，真正“黑暗”的部分其实很少。

**标签**: `#security`, `#cryptography`, `#surveillance`, `#law-enforcement`, `#encryption`

---

<a id="item-5"></a>
## [批评：Opus 5 的省略式、面向智能体的语言让人类体验更差](https://mun-logadan.github.io/why-does-opus-5-feel-worse/) ⭐️ 8.0/10

一篇批评性博客文章指出，Anthropic 的 Opus 5 模型以过度抽象、省略式的风格进行交流，这种风格似乎是为 AI 智能体而非人类读者优化的，在 Hacker News 上引发了广泛讨论。 这一批评之所以引人共鸣，是因为 Opus 5 是面向高难度推理和智能体工作的旗舰模型；如果它的输出让人感觉陌生，可能损害用户信任和采用率。它也凸显了行业向智能体间通信转变的大趋势，在这种趋势下，人类可读性可能变成次要考虑。 该文章重点关注过度抽象的措辞、绕圈子的省略句，以及滥用无生命名词作主语以制造“惊喜”结尾。评论者补充说，Opus 5 经常“坦白”错误并长篇大论，令一些人感到疲惫。

hackernews · numeri · 8月14日 10:12 · [社区讨论](https://news.ycombinator.com/item?id=49296740)

**背景**: Claude Opus 5 是 Anthropic 的旗舰大语言模型，约于 2026 年 7 月发布，输入每百万 token 5 美元、输出每百万 token 25 美元，上下文窗口为 100 万 token。省略式语言会省略词语或在要点间跳跃，对机器可能高效，但对人类却令人困惑。这一讨论反映出一种日益增长的担忧：随着 LLM 越来越为智能体间协作而进行后训练，面向人类的行文可能被降低优先级。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openrouter.ai/anthropic/claude-opus-5">Claude Opus 5 - API Pricing & Benchmarks | OpenRouter</a></li>
<li><a href="https://www.wam.ae/en/article/17c8lgc-anthropic-rolls-out-opus-model-efficiency-upgrade">Anthropic rolls out Opus 5 AI model in efficiency upgrade</a></li>
<li><a href="https://www.masterclass.com/articles/how-to-write-an-elliptical-sentence">How to Write an Elliptical Sentence: Improve Your... - MasterClass</a></li>

</ul>
</details>

**社区讨论**: 评论区大多同意这一批评：barrkel 称省略式写作是最大烦恼；D13Fd 在发现 Opus 5 的交流令人疲惫后转用 OpenAI；zmmmmm 推测人类已不再是后训练的目标受众。MyFirstSass 则退回到 4.8，认为第 5 版已退化且在没有严格指令时会跑偏。

**标签**: `#AI`, `#LLM`, `#UX`, `#Opus 5`, `#human-AI interaction`

---

<a id="item-6"></a>
## [Firefox 成为最后仍支持 uBlock Origin 的主流浏览器](https://www.pcworld.com/article/3212428/firefox-is-now-the-last-major-browser-that-still-supports-ublock-origin.html) ⭐️ 8.0/10

Firefox 现在是唯一一个仍完全支持 uBlock Origin（一款领先的开源广告拦截器）的主流浏览器。Chrome 和 Edge 因谷歌 Manifest V3 的变更而逐步停止了对该扩展完整功能支持。 这一变化意义重大，因为它使 Firefox 成为依赖 uBlock Origin 强大广告和跟踪器拦截功能的用户的最后主流选择。同时，这也凸显了人们对谷歌掌控扩展生态系统以及开放网络上广告拦截未来的日益担忧。 uBlock Origin 依赖 webRequestBlocking API，而该 API 在 Manifest V3 下受到极大限制，仅适用于企业侧载的扩展。目前有一个非官方移植版本 uBlock-mv3，但由于完整版本无法在新 API 下运行而面临挑战；Firefox 还会定期审查诸如 uBlock Origin 等热门扩展以确保安全。

hackernews · DemiGuru · 8月14日 19:03 · [社区讨论](https://news.ycombinator.com/item?id=49303202)

**背景**: uBlock Origin 是一款广泛使用的免费开源内容拦截器，能以较低的 CPU 和内存占用拦截广告、跟踪器和不需要的脚本。Manifest V3 是 Chrome 的新扩展平台，旨在改善隐私、安全和性能，但它移除了实时请求检查并限制规则数量，从而削弱了广告拦截扩展的效果。Firefox 虽然也支持 WebExtensions，但保留了更强大的 API，使 uBlock Origin 仍能完整运行。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/UBlock_Origin">uBlock Origin - Wikipedia</a></li>
<li><a href="https://developer.chrome.com/docs/extensions/develop/migrate/what-is-mv3">Extensions / Manifest V 3 | Chrome for Developers</a></li>
<li><a href="https://thelibre.news/manifest-v3-how-google-is-killing-ad-blocking-on-chromium/">Manifest V 3 : How Google is killing ad-blocking on Chromium</a></li>

</ul>
</details>

**社区讨论**: 评论者大多称赞 Firefox 在每次更新时都审查 uBlock Origin，并批评谷歌通过 Manifest V3 限制了扩展的自由。有人提到已存在非官方的 MV3 移植版 uBlock Origin，但仍有局限；还有用户对普遍充斥着广告的浏览体验表达了不满。

**标签**: `#Firefox`, `#uBlock Origin`, `#ad-blocking`, `#Chrome`, `#browser extensions`

---

<a id="item-7"></a>
## [开发者将 Doom 渲染器编译为 210 亿参数 Transformer，无需训练](https://www.reddit.com/r/MachineLearning/comments/1voazhm/i_compiled_dooms_renderer_into_a_21bparameter/) ⭐️ 8.0/10

一位开发者使用自定义编译器将 Doom 的渲染算法移植到了一个 210 亿参数的 Transformer 检查点中，整个过程没有任何训练。该模型会生成包含像素绘制命令的 token 序列，机械地执行这些命令即可渲染出著名的 E1M1 帧。 这展示了在神经网络中进行算法计算的一种新颖方法，证明复杂的软件可以在不经过基于梯度的训练的情况下被编译进 Transformer 权重中。它为将确定性算法嵌入语言模型开辟了可能性，尽管其当前的实际影响仍局限于一个小众的概念验证。 负责加载检查点并渲染一帧的主机程序只有 43 行 Python 代码，而定义计算图的代码则长得多，并被编译进 Transformer 自身。每一帧需要一个 3,614 token 的提示词，并生成 53,747 个 token，在 NVIDIA B200 上需约 40 分钟（相当于每天约 35 帧，而原版 Doom 在 486 上每秒可跑 35 帧）。

reddit · r/MachineLearning · /u/notforrob · 8月14日 15:50

**背景**: Transformer 是一种基于注意力机制处理序列的神经网络架构，通常需要在大型数据集上训练以学习规律。计算图将机器学习模型表示为有向无环图（DAG）中的一系列操作，PyTorch 和 TensorFlow 等框架都依赖这种表示。“神经编译”是一个新兴研究方向，目标是通过记忆或构造而非学习的方式将算法直接编码到神经网络权重中；本项目就是该思路的一个具体实例。Hugging Face 的 trust_remote_code 设置用于控制加载远程模型仓库时是否允许执行自定义代码，而这个生成的检查点只使用标准 transformers 格式，因此无需开启该设置。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.researchgate.net/publication/382080356_Algorithmic_Language_Models_with_Neurally_Compiled_Libraries">(PDF) Algorithmic Language Models with Neurally Compiled Libraries</a></li>
<li><a href="https://pooya.io/ai/computational_graph_machine_learning/">Computational Graph in Machine Learning · pooya.io</a></li>
<li><a href="https://www.geeksforgeeks.org/deep-learning/dynamic-vs-static-computational-graphs-pytorch-and-tensorflow/">Dynamic vs Static Computational Graphs - PyTorch... - GeeksforGeeks</a></li>

</ul>
</details>

**标签**: `#transformer`, `#compiler`, `#deep learning`, `#rendering`, `#algorithmic compilation`

---

<a id="item-8"></a>
## [AI 机器人实验室年测 300 万人体样本，有望取代动物试验](https://www.fastcompany.com/91589344/the-worlds-largest-biological-datacenter-could-help-make-animal-testing-obsolete) ⭐️ 8.0/10

生物技术公司 Vivodyne 在旧金山南部建立了 12 个'蜂巢'机器人实验室，每年可对 300 多万个人体组织开展受控实验。这些由 AI 设计的实验旨在比现有方法更好地预测药物的疗效和安全性。 如此规模的人体组织测试有望大幅减少对动物试验的依赖，目前约 90% 通过动物试验的候选药物在后续人体临床试验中仍告失败。若取得成功，可能使动物试验被淘汰，并加速药物研发进程。 该系统的测试容量大约是美国所有在研临床试验总容量的两倍。Vivodyne 使用衣柜大小的机器人实验室培养人体组织，并用 AI 设计实验。

telegram · zaihuapd · 8月14日 01:48

**背景**: 器官芯片（organ-on-a-chip）技术利用含有人体细胞的微流控芯片来模拟人体器官的结构和功能，比传统细胞培养更接近人体真实状态。尽管前景广阔，这类系统仍处于早期发展阶段，而将其规模扩大到数百万个样本是一大进步。Vivodyne 的方法将这一技术与自动化和 AI 相结合，以前所未有的规模生成与人体相关的数据，有望解决临床前结果向人体转化这一长期瓶颈。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.vivodyne.com/">Vivodyne | Make biology computable</a></li>
<li><a href="https://en.wikipedia.org/wiki/Microphysiological_systems">Microphysiological systems</a></li>
<li><a href="https://medium.com/@ieee.wiemuj/tiny-devices-big-impact-the-promise-of-organ-on-a-chip-technology-in-healthcare-5349fe47c7e8">Tiny Devices, Big Impact: The Promise of Organ - on -a- Chip ... | Medium</a></li>

</ul>
</details>

**标签**: `#AI`, `#Biotechnology`, `#DrugTesting`, `#LabAutomation`, `#ClinicalTrials`

---

<a id="item-9"></a>
## [小红书开源 dots3-note：280B MoE 仅 16B 激活参数](https://x.com/dotsstudioai/status/2088083314855018521) ⭐️ 8.0/10

小红书 dots 实验室开源了 dots3-note preview，这是 dots3 系列首个开放权重模型，总参数 280B，每次仅激活 16B 参数。该模型支持 512K 上下文、多模态输入（文字、图片、视频、音频），并引入了 TEMPO 强化学习方法及两个新基准。 这是来自中国头部互联网公司的重要发布，将大规模稀疏 MoE 模型以开放权重形式公开，兼具高推理效率和长上下文能力。这可能推动长上下文多模态智能体研究，并为主动式、长周期任务设立新的评测标准。 该模型采用 MoE 架构，总参数 280B，但每次推理仅激活 16B 参数，并支持 512K 上下文窗口和多模态理解。TEMPO 通过自批判和测试时价值估计来训练长程智能体，发布还包括 VibeSearchBench 和 VibeLifeBench 两个真实场景智能体基准。

telegram · zaihuapd · 8月14日 08:27

**背景**: MoE（混合专家）模型保留大量总参数，但每个 token 只激活其中一小部分，从而以较低算力成本实现高模型容量。小红书是中国主流社交平台，正越来越多地参与开源 AI。新发布的基准聚焦主动式和长周期智能体任务：VibeSearchBench 评测模糊多轮主动搜索，VibeLifeBench 则覆盖基于模拟服务后端的多周日常生活任务。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://vibebench.github.io/VibeSearchBench.github.io/">VibeSearchBench — Benchmarking Long-horizon Proactive Search...</a></li>
<li><a href="https://vibebench.github.io/VibeLifeBench_homepage/">VibeLifeBench — Can Your Life Agent Be Proactive and Persistent in...</a></li>
<li><a href="https://arxiv.org/html/2605.27882">VibeSearchBench : Benchmarking Long-horizon Proactive Search in...</a></li>

</ul>
</details>

**标签**: `#MoE`, `#open-source`, `#reinforcement-learning`, `#multimodal`, `#LLM`

---

<a id="item-10"></a>
## [美国法官限期谷歌一周内移除第三方应用商店安装障碍](https://www.androidauthority.com/google-play-store-remove-third-party-app-store-friction-3698697/) ⭐️ 8.0/10

这项反垄断裁决可能重塑安卓应用分发格局，让用户更容易安装第三方应用商店，从而增强与 Google Play 的竞争。它也为平台利用警告和额外步骤阻碍竞争对手的做法确立了重要的法律先例。 该命令是 Epic 诉谷歌案补救阶段的一部分，此前陪审团裁定谷歌在安卓应用分发上构成非法垄断。谷歌必须让安装第三方商店像安装普通安卓应用一样直接，取消多余的确认和警告界面。

telegram · zaihuapd · 8月14日 09:55

**背景**: 安卓系统本身允许用户通过 Google Play 之外的渠道“侧载”应用，但谷歌长期以来在用户尝试安装竞品应用商店时显示警告并增加额外点击步骤。Epic 的诉讼正是挑战这些做法，认为它们会吓退普通用户并巩固谷歌的垄断地位。法官 Donato 的命令就是为了纠正这种行为的补救措施之一。

**标签**: `#antitrust`, `#Android`, `#Google`, `#app stores`, `#legal`

---

<a id="item-11"></a>
## [苹果 CEO 库克 2026 年卸任，特努斯接任](https://t.me/zaihuapd/43191) ⭐️ 8.0/10

苹果宣布管理层交接：现任 CEO 蒂姆·库克将卸任并出任董事会执行董事长，硬件工程高级副总裁约翰·特努斯将从 2026 年 9 月 1 日起担任新任 CEO。 这是苹果这家全球最具影响力的科技公司之一的一次重大领导层更迭。这一变动影响投资者、员工和整个科技行业，外界将关注特努斯上任后苹果的产品与服务战略是否会发生变化。 董事会已一致批准这项安排，库克将在整个夏天继续担任 CEO，以完成过渡。现任董事长 Arthur Levinson 将于 9 月 1 日转任首席独立董事，特努斯同日加入董事会。特努斯 2001 年加入苹果，2013 年升任硬件工程副总裁，2021 年进入高管团队。

telegram · zaihuapd · 8月14日 11:00

**背景**: 苹果是全球最大、最具影响力的科技公司之一，CEO 负责公司的整体战略与运营。此次交接中，库克并未完全离开公司：出任执行董事长后，他将专注于董事会领导与对管理层的建议，而特努斯负责日常运营。特努斯 2001 年加入苹果，长期负责 iPhone、Mac、iPad、AirPods 等核心产品的硬件工程，此次任命体现了苹果从内部核心产品体系选拔接班人的思路。

**标签**: `#Apple`, `#Leadership`, `#CEO transition`, `#Tim Cook`, `#Tech industry`

---

<a id="item-12"></a>
## [苹果自研中国专属 AI 大模型，联手阿里或成首个获批外企](https://www.reuters.com/business/retail-consumer/apple-trains-its-own-ai-model-china-market-with-alibabas-support-sources-say-2026-08-14/) ⭐️ 8.0/10

苹果已专门为中国市场训练一款大语言模型，并得到阿里巴巴支持，改变了此前依赖第三方模型的策略。Apple Intelligence 预计未来数月内随 iOS 更新在中国上线。 若落地，苹果可能成为首家获得北京批准在中国提供自有 AI 模型的外国公司，从而更好地掌控中国市场的 AI 体验。这可能为其他跨国科技公司应对中国 AI 监管树立先例。 中国国家互联网信息办公室已于上月对苹果的生成式 AI 服务进行备案。自研模型标志着从第三方供应商的策略转变，苹果可能需要满足中国生成式 AI 服务备案要求。

telegram · zaihuapd · 8月14日 14:47

**背景**: Apple Intelligence 是苹果于 2024 年 6 月发布的 AI 功能套件，结合端侧与服务器处理，包含写作辅助、图像生成及 ChatGPT 集成等功能。在中国，政府要求面向公众的生成式 AI 服务依据《生成式人工智能服务管理暂行办法》进行备案，因此外国公司通常与本地企业合作以获得批准。阿里巴巴的支持可能帮助苹果满足监管要求并实现面向中国用户的本地化。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Apple_Intelligence">Apple Intelligence</a></li>
<li><a href="https://www.apple.com/apple-intelligence/">Apple Intelligence and Siri - Apple</a></li>

</ul>
</details>

**标签**: `#Apple`, `#AI`, `#China`, `#Alibaba`, `#LLM`

---