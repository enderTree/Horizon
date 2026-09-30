---
layout: default
title: "Horizon Summary: 2026-09-30 (ZH)"
date: 2026-09-30
lang: zh
---

> 从 39 条内容中筛选出 6 条重要资讯。

---

1. [OpenAI 发布 GPT-6.1 Sol，定价仅为 Astra 的五分之一](#item-1) ⭐️ 9.0/10
2. [OpenAI 开发者大会 2026：Dots 智能体、GPT-6.1 Sol、Ultrafast 等 20 余项更新](#item-2) ⭐️ 9.0/10
3. [OpenAI 发布 Dots：拥有云端电脑的常驻在线智能体](#item-3) ⭐️ 8.0/10
4. [Relapse 漏洞利用可越狱 7.00–13.60 固件的 PS5](#item-4) ⭐️ 8.0/10
5. [Anthropic：新模型在二进制漏洞利用基准上跨越能力门槛](#item-5) ⭐️ 8.0/10
6. [DeepSeek 开源华为昇腾基础组件套件](#item-6) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [OpenAI 发布 GPT-6.1 Sol，定价仅为 Astra 的五分之一](https://openai.com/index/introducing-gpt-6-1-sol/) ⭐️ 9.0/10

OpenAI 宣布推出 GPT-6.1 Sol，这是 GPT-6 Sol 的升级版本，官方称其在智能体编程、计算机操作和专业任务上接近 GPT-6 Astra 的水平，而价格仅为 Astra 标准价的五分之一。该模型已通过 OpenAI API 以 gpt-6.1-sol 的名称提供，标准价格为每百万输入 token 2 美元、每百万缓存输入 token 0.10 美元、每百万输出 token 10 美元，并正向 Plus、Pro、Business、Enterprise 和 Edu 用户推送。 此次发布把 AI 价格战推向新低点：缓存输入价格比 GPT-6 Sol 的缓存价格低 50%，比标准输入价格低约 95%，直接降低了运行编程智能体和长上下文工作负载的成本。这也给 Anthropic、DeepSeek 等竞争对手带来压力，使竞争焦点从单纯的能力转向每 token 成本。 早期第三方数据虽有限但表现亮眼：Devin 报告称在低 effort 设置下，GPT-6.1 Sol 以每任务 0.21 美元的成本取得 58.1% 的成绩，高于同设置下 GPT-6 Sol 的 50.5%，是其排行榜上所有单任务成本低于 0.30 美元的模型中的最高分。不过 OpenAI 自家页面指出该模型尚未在 ChatGPT 中上线，因此目前主要通过 API 和合作方工具访问，而非普通聊天界面。

hackernews · crorella · 9月29日 17:06 · [社区讨论](https://news.ycombinator.com/item?id=49896586)

**背景**: OpenAI 的 GPT-6 家族分为三个层级：面向公众发布的 GPT-6 Astra（2026 年 9 月 4 日），以及更便宜的 Sol 与 Luna 变体（2026 年 9 月 22 日）。Astra 被定位为前沿、智能水平最高的模型，并因宣称解决了 10 个长期悬而未决的数学与计算机科学难题而广受关注；Sol 则是更经济的主力模型，被 Codex、Devin 等编程工具采用。所谓“缓存输入”token，指服务商已经处理并存储过的提示词 token，在重复请求时可享受大幅折扣。因此 GPT-6.1 属于一次中途更新，试图在尽量缩小与 Astra 差距的同时大幅压低使用成本。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/GPT-6_Sol">GPT-6 Sol</a></li>
<li><a href="https://openai.com/index/introducing-gpt-6-1-sol/">Introducing GPT - 6 . 1 Sol | OpenAI</a></li>
<li><a href="https://devin.ai/blog/gpt-6-1-sol">GPT - 6 . 1 Sol is now available in Devin | Devin</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上该帖获得 844 分、762 条评论，整体氛围偏怀疑。多位开发者认为 DeepSeek 速度够快、价格够低、质量差距也可忽略，因此每月为 OpenAI 或 Anthropic 花 200 甚至 500 美元很难说得通；也有人表示 GPT-6 Sol 退步严重，已转向 Anthropic 的 Opus 5.5。还有评论者猜测 GPT-6.1 Sol 其实是泄露文件中“Astra-Minor”模型的临时改名，并普遍认同真正的头条是缓存输入降价而非模型本身；有人则评论说，token 价格成为行业主战场“对行业和投资者而言是个不祥信号”。

**标签**: `#OpenAI`, `#GPT-6.1`, `#LLMs`, `#AI pricing`, `#model release`

---

<a id="item-2"></a>
## [OpenAI 开发者大会 2026：Dots 智能体、GPT-6.1 Sol、Ultrafast 等 20 余项更新](https://openai.com/zh-Hant/index/devday-2026-recap/) ⭐️ 9.0/10

在旧金山举行的年度 DevDay 开发者大会上，OpenAI 发布了 20 余项更新，其中最重要的是常驻伴生智能体 Dots——它可以自主操控电脑并从已连接的应用中拉取信息，完成调研、起草文档和开发软件等长线任务；此外还有专注编程与电脑操控的 GPT-6.1 Sol（以约五分之一的价格获得接近 Astra 的智能水平），以及比 Astra Standard 最高快 8 倍（API 端 6 倍）、速度达每秒 300 token 的 Astra Ultrafast 档位。OpenAI 同时推出了 Codex 云端体验、原生支持电脑操控与 AWS Bedrock 托管的 Agents API、用于类型化分类与路由的轻量级 Decisions API、全新 Pro 500 订阅档位，以及可将订阅额度直连 Devin、Notion 等第三方工具的“Sign in with ChatGPT”账号互通功能。 这是 AI 行业影响最大的单日发布之一，因为它标志着 OpenAI 从单纯售卖模型调用，转向售卖“常驻自主智能体 + 面向智能体的开发者平台”，这将重塑第三方应用的构建方式与商业模式。尤其是 Decisions API 把廉价、低延迟的决策能力下沉到基础设施层，而“Sign in with ChatGPT”让订阅额度可以流向外部工具，有可能使 OpenAI 成为整个智能体生态的身份与计费底座。 Ultrafast 的速度伴随着显著溢价：API 调用成本是对应模型标准费率的 6 倍，首发仅支持 GPT-6 Astra，6.1 Sol 版本承诺后续推出；OpenAI 还表示正与微软合作，在 Agent 365 中把专用 Dots 接入企业治理与安全控制体系。据报道，OpenAI 在发布 Dots 之前曾因安全顾虑搁置了一款新模型的推出；而 Decisions API 作为补充，会根据用户预设的选项返回一个带概率的类型化答案，据称比通过标准 API 调用 GPT-6 Luna 快约 10 倍（约 150 毫秒对约 1.6 秒）。

telegram · zaihuapd · 9月29日 17:52

**背景**: OpenAI 每年举办 DevDay 开发者大会来发布面向开发者的新产品，2026 年的主题围绕“智能体”（Agent）展开——也就是能够代替用户执行操作、而不只是回答提示词的 AI 系统。CEO Sam Altman 称 Dots 比 ChatGPT“更具野心”，是一种“与 AI 协作的全新方式”，折射出全行业竞相打造可常驻运行、能直接操作软件的智能体的趋势。Astra、Sol、Luna 这些名字对应 OpenAI GPT-6 系列中面向不同能力与成本定位的模型，而 Agents、Decisions 等 API 则是让外部开发者在自己应用中调用这些能力的接口。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openai.com/index/introducing-dots/">Introducing dots | OpenAI</a></li>
<li><a href="https://venturebeat.com/technology/openais-gpt-6-1-sol-offers-astra-like-performance-at-1-5th-price-a-new-ultrafast-tier-clocks-at-300-tokens-per-second">OpenAI's GPT-6.1 Sol offers Astra-like performance at 1/5th price. A new Ultrafast tier clocks at 300 tokens per second. | VentureBeat</a></li>
<li><a href="https://www.theguardian.com/technology/2026/sep/29/openai-announces-dots-agent-safety-concerns">OpenAI announces ‘dots’ agent after scrapping launch of new AI model over safety concerns | OpenAI | The Guardian</a></li>

</ul>
</details>

**标签**: `#OpenAI`, `#AI Agents`, `#LLM`, `#Developer APIs`, `#Industry Announcement`

---

<a id="item-3"></a>
## [OpenAI 发布 Dots：拥有云端电脑的常驻在线智能体](https://openai.com/index/introducing-dots/) ⭐️ 8.0/10

在旧金山举行的 DevDay 2026 上，OpenAI 发布了 Dots，官方称其为"能力出众的常驻在线智能体"，会持续了解用户在意的事情并主动替用户工作。据相关报道，每个 Dot 由 GPT-6 Astra 驱动，拥有独立的云端计算机，可接入 4000 多个应用，Pro 和 Business Premium 订阅用户可直接获得第一个 Dot。 这是 OpenAI 从对话式助手转向持久、主动型智能体最明确的一步：智能体不再等待提示，而是替用户持续工作，同时也让 OpenAI 与增长迅猛的 Meta 个人智能体 Muse 正面交锋。由于 Dot 会不断积累应用集成和工作历史，它也引发了关于平台锁定，以及 OpenAI 如何区分 Dots 与 Codex 及其他 ChatGPT 产品的切实疑问。 已知的具体信息是：Dots 由 GPT-6 Astra 驱动，每个 Dot 拥有自己的云端计算机，并通过插件接入 4000 多个应用，Pro 与 Business Premium 套餐各包含一个 Dot。锁定效应更多是技术层面的而非合同层面的：更换模型相对容易，但迁移一个承载着你的集成、凭据与工作历史的智能体，实际上等于搬迁整个云端工作环境。

hackernews · alvis · 9月29日 17:07 · [社区讨论](https://news.ycombinator.com/item?id=49896604)

**背景**: "常驻在线智能体"指的是长期在后台运行、拥有独立虚拟机的 AI 系统，它能跨应用执行多步骤操作，而不只是回答一轮对话。OpenAI 在这一方向上已有多款彼此重叠的产品——面向编程的 Codex 和面向通用工作的 ChatGPT——这正是评论者觉得它们与 Dots 之间界限模糊的原因。此次发布也处在智能体平台大战之中：上一周公布的 Meta Muse 被视为面向消费者的产品，可以靠 Meta 的广告业务补贴，并通过其应用家族获得分发。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openai.com/index/introducing-dots/">Introducing dots - OpenAI</a></li>
<li><a href="https://www.wired.com/story/openai-dots-always-on-ai-agents-that-proactively-help/">OpenAI’s Dots Are Always-On AI Agents—and Its Answer to Meta ...</a></li>
<li><a href="https://www.datacamp.com/blog/openai-dots">OpenAI Dots: Always-On Agents in ChatGPT, Explained</a></li>

</ul>
</details>

**社区讨论**: 这条有 378 条评论的 Hacker News 讨论整体偏怀疑：多位用户认为常驻智能体是在刻意加深平台锁定——因为它承载着你的集成与工作历史，"本质上就是你放在云端的电脑"，比换一个模型 API 难脱身得多。也有人抱怨 Dots 与 Codex、ChatGPT Work 之间的界限越来越模糊，担心 OpenAI 正靠推送非必要产品来消耗当初用慷慨的 Codex 额度换来的用户忠诚；还有几位表示更看好面向消费者的 Meta Muse。最后一种观点认为，云端常驻智能体将终结 PC 时代，其目标用户并非今天的开发者，而是非技术人群和下一代 AI 原住民。

**标签**: `#OpenAI`, `#AI agents`, `#always-on agents`, `#platform lock-in`, `#product strategy`

---

<a id="item-4"></a>
## [Relapse 漏洞利用可越狱 7.00–13.60 固件的 PS5](https://github.com/ntfargo/Relapse-Exploit) ⭐️ 8.0/10

开发者 ntfargo 在 GitHub 上公开了一个名为 Relapse 的 PlayStation 5 漏洞利用链，声称可越狱运行 7.00 至 13.60 固件版本的 PS5 主机。用户只需在 PS5 浏览器中打开托管页面，或在本地运行 Python 服务（serve.py）即可触发；据报道，9 月 16 日及之后更新过固件的主机无法使用。 越狱之所以重要，是因为它能在封闭的主机生态中解锁自制软件、备份以及跨区或修改版游戏，而覆盖七个主要固件分支的利用链大幅降低了现役主机用户的入局门槛。这也会给索尼带来快速修补的压力（很可能通过强制固件更新），并再次点燃主机厂商与自制社区之间长期存在的矛盾。 根据对该仓库的报道，Relapse 并非单一漏洞，而是一条将 WebKit 漏洞与内核竞争条件（race condition）结合起来的利用链；项目说明 9 月 16 日更新过固件的主机不兼容，因此该技术仅适用于特定的固件窗口。触发方式只需使用主机自带的网页浏览器，比基于硬件的手段门槛低得多。

hackernews · therepanic · 9月29日 15:44 · [社区讨论](https://news.ycombinator.com/item?id=49895304)

**背景**: 越狱是指利用 PS5（2020 年 11 月发布）等封闭主机中的软件或硬件缺陷，获得运行未签名代码的能力，从而实现自制程序、备份和非官方修改。现代利用链通常从浏览器渲染的网页开始：WebKit 的 JavaScript 引擎 JavaScriptCore 历来是内存破坏漏洞的富矿，很多问题源于切换至更高层 JIT 编译器时缺少检查，这类漏洞提供了最初的立足点，随后再由第二阶段提权至内核。由于这些漏洞往往通过固件更新被悄悄修复，漏洞研究者通常会囤积大量未公开的缺陷，只有在更新固件封堵了其他路径时才放出其中一个。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/ntfargo/Relapse-Exploit">GitHub - ntfargo/Relapse-Exploit: Exploit chain for PS5 7.00 - 13.60 · GitHub</a></li>
<li><a href="https://elsolitario.org/en/2026/09/29/relapse-repo-claims-ps5-exploit-firmware-7-00-to-13-60/">PS5 Jailbreak: What Is Relapse Exploit and Its Scope</a></li>

</ul>
</details>

**社区讨论**: 评论者主要关注实际影响：一位用户询问 Relapse 能否最终实现游戏存档的手动 USB 备份，并抱怨 PS5 将存档锁定在每个用户档案各自订阅的 PS Plus 云服务之后——他的女儿曾因此丢失了一年的 Minecraft 进度。其他人则推测索尼可能会通过关闭 JavaScriptCore 的 JIT 来缩小攻击面，指出越狱社区通常还藏有其他用于突破引导加载程序的零日漏洞，也有人调侃发布时机应与 GTA 6 挂钩，或借此在主机上玩 Steam 的 PC 游戏。

**标签**: `#PS5`, `#security-exploit`, `#WebKit`, `#JavaScriptCore`, `#homebrew`

---

<a id="item-5"></a>
## [Anthropic：新模型在二进制漏洞利用基准上跨越能力门槛](https://simonwillison.net/2026/Sep/29/anthropic-frontier-red-team/) ⭐️ 8.0/10

Anthropic 的 Frontier Red Team 在其内部 Binary Exploitation 基准中随机抽取 100 个任务对多个模型进行评估，结果显示 GLM-5.3 在 4% 的试验中实现了完整的控制流劫持，Claude Mythos Preview 的比例为 6%。而此前的模型，包括 Claude Opus 4.6 和 GLM-5.2，在任何任务上都未能成功，该团队认为这标志着一条门槛已被明确跨越。 这是首次有报道显示前沿语言模型在此类漏洞利用开发基准上取得非零成绩，意味着自动化发现并武器化内存破坏漏洞的能力正从理论走向部分验证。这一进展将影响漏洞研究人员、必须加快修补速度的防御方，也会加剧关于先进网络攻击能力是否正在从少数资源雄厚的实验室向外扩散的争论。 从绝对值看成功率仍然很低（100 个随机任务中分别为 4% 和 6%），而且该基准是 Anthropic 的内部基准而非公开标准，因此这些数字无法在不同实验室之间直接比较。值得注意的是，GLM-5.3 与 GLM-5.2 使用相同的基础模型，所有性能提升都来自后训练，这说明能力跃升来自训练方法而非模型规模。

rss · Simon Willison · 9月29日 22:20

**背景**: Anthropic 的 Frontier Red Team 是一支研究团队，专门对前沿 AI 系统进行压力测试，以摸清其当前能力并预判包括网络攻击在内的新兴风险。二进制漏洞利用是指滥用内存破坏缺陷来攻破已编译程序，使其以有利于攻击者的方式违反信任边界；控制流劫持则是攻击者将程序执行流重定向到自己选定代码的阶段，通常也是完整利用链的最终目标。GLM-5.3 是 Z.ai 的旗舰模型，与 GLM-5.2 共用同一基础模型——一种大型稀疏混合专家（MoE）架构，总参数量约 753B，每个 token 激活约 40B 参数。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.anthropic.com/research/team/frontier-red-team">Frontier Red Team Research \ Anthropic</a></li>
<li><a href="https://huggingface.co/zai-org/GLM-5.3">zai-org/GLM-5.3 · Hugging Face</a></li>
<li><a href="https://trailofbits.github.io/ctf/exploits/binary1.html">Binary Exploits 1 - CTF Field Guide</a></li>

</ul>
</details>

**标签**: `#ai-security-research`, `#cybersecurity`, `#llm-capabilities`, `#red-teaming`, `#anthropic`

---

<a id="item-6"></a>
## [DeepSeek 开源华为昇腾基础组件套件](https://mp.weixin.qq.com/s/X41mKH4Ds-VXUAnK6M8Eww) ⭐️ 8.0/10

据报道，DeepSeek 于 2026 年 9 月 30 日开源了面向华为昇腾平台的一整套基础组件，涵盖 TileLang 高级语言编译工具、计算库和分布式通信库，与其现有的英伟达平台组件一一对应。此次发布的内容据称包括 DeepGEMM Ascend、DeepEP Ascend、TileKernels、FlashMLA 和 DeepSelect。 这将是构建非英伟达 AI 基础设施栈的重要一步，因为 DeepSeek 实际上是把让其模型高效运行的底层训练与推理工具移植到了华为昇腾 NPU 上。如果这些组件在使用体验上能与 CUDA 对应组件相当，就能降低中国实验室和企业在纯国产硬件上训练与部署大模型的门槛。 DeepSeek 称相关组件在多项测试中性能接近硬件上限，并表示正与华为推进昇腾 950 的 128 卡超节点方案。但该消息本身较为简短，来自微信/Telegram 式的转发且几乎没有实质性讨论，且所引日期指向未来，因此仓库地址、许可证、基准测试数据等具体细节目前仍属未经证实。

telegram · zaihuapd · 9月30日 03:09

**背景**: 华为昇腾 NPU 是中国最主要的英伟达 GPU 替代方案，但长期以来编程难度更高，因为绝大多数 AI 训练与推理软件都是为英伟达的 CUDA 生态编写的。DeepSeek 此前已开源过若干组件，例如 DeepGEMM（快速矩阵乘法算子）、DeepEP（面向 MoE 混合专家模型的专家并行通信库）、FlashMLA（高效注意力算子），以及 TileLang——一种基于分块（tile）的编程模型，允许开发者用类 Python 语言编写 GPU/NPU 算子。把这些组件全部移植到昇腾，意味着要在另一种芯片架构上重新实现同样的底层性能优化，这正是此举对更广泛的非英伟达生态意义重大的原因。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://tilelang.com/">TileLang 0.1.14 documentation</a></li>
<li><a href="https://github.com/deepseek-ai/DeepEP-Ascend/tree/main/">GitHub - deepseek-ai/DeepEP-Ascend: A high-performance ...</a></li>
<li><a href="https://github.com/deepseek-ai/DeepGEMM/pull/462">Public release 26/09/30 by LyricZhao · Pull Request #462 · deepseek-ai/DeepGEMM</a></li>

</ul>
</details>

**标签**: `#DeepSeek`, `#Huawei Ascend`, `#Open Source`, `#AI Infrastructure`, `#TileLang`

---