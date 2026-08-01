---
layout: default
title: "Horizon Summary: 2026-08-01 (ZH)"
date: 2026-08-01
lang: zh
---

> 从 37 条内容中筛选出 9 条重要资讯。

---

1. [电梯算法解析：SCAN、LOOK 与目的地派梯之辩](#item-1) ⭐️ 8.0/10
2. [YC 发布 QM：面向工作的多人智能体指挥框架](#item-2) ⭐️ 8.0/10
3. [Tailscale 事后分析：可重用认证密钥导致 Hugging Face 入侵](#item-3) ⭐️ 8.0/10
4. [DeepSeek 发布 V4-Flash-0731：304B 参数的智能体模型](#item-4) ⭐️ 8.0/10
5. [无状态 MCP 重新引发兴趣并催生新项目](#item-5) ⭐️ 8.0/10
6. [特朗普政府拟向留学生收 10 万美元毕业后工作费](#item-6) ⭐️ 8.0/10
7. [MiniMax 将于 8 月 3 日开源 H3 多模态视频模型](#item-7) ⭐️ 8.0/10
8. [最高法院拒审 AI 版权案，维持人类创作原则](#item-8) ⭐️ 8.0/10
9. [谷歌确认 Android 开发者验证分免费和付费两档，不公开开发者名单](#item-9) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [电梯算法解析：SCAN、LOOK 与目的地派梯之辩](https://john.fun/elevators) ⭐️ 8.0/10

john.fun 上的一篇新分析文章探讨了包括 SCAN、LOOK 和目的地派梯在内的电梯调度算法，在 Hacker News 上引发了获得 961 分和 238 条评论的讨论。文章比较了随机与真实出行模式下的算法表现。 电梯调度每天影响数十亿次乘梯，却很少被深入分析。这一讨论将磁盘调度等计算机科学概念与真实楼宇行为联系起来，为未来电梯优化提供了启示。 文章指出，在随机目的地场景下，目的地派梯可能不如 LOOK；但真实楼宇中出行模式往往有偏，例如大群人去往同一楼层。评论者将 SCAN 算法与硬盘磁盘调度联系起来，并推荐了 Elevator Saga 模拟游戏。

hackernews · Jrh0203 · 7月31日 15:17 · [社区讨论](https://news.ycombinator.com/item?id=49124218)

**背景**: 电梯算法又称 SCAN，是一种磁盘调度算法，磁头沿一个方向移动，直到没有请求需要服务再反向。LOOK 是变体，只移动到最高或最低待处理请求的位置。目的地派梯在轿厢外设置按键，让乘客在乘坐前选择目标楼层，从而实时分组派梯。这些概念源自操作系统和楼宇工程。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Elevator_algorithm">Elevator algorithm - Wikipedia</a></li>
<li><a href="https://dev.to/thesaltree/elevator-scheduling-algorithms-fcfs-sstf-scan-and-look-2pae">Elevator Scheduling Algorithms: FCFS, SSTF, SCAN, and LOOK Elevator Algorithms: SCAN, LOOK, and RSR Explained SCAN (Elevator) Disk Scheduling Algorithms - GeeksforGeeks Difference between SCAN and LOOK Disk scheduling algorithms Elevator algorithm - Wikipedia Elevators - john.fun Elevator algorithm — Grokipedia</a></li>
<li><a href="https://elsolitario.org/en/2026/07/31/elevator-algorithms-scan-look-rsr/">Elevator Algorithms: SCAN, LOOK, and RSR Explained</a></li>

</ul>
</details>

**社区讨论**: Hacker News 的评论总体积极且富有建设性。有用户指出 HDD 就像一个‘长长的电梯’，并提到 SCAN 是磁盘调度算法；另一位用户观察到，目的地派梯在随机模拟中表现不佳，但真实楼宇中的交通往往有偏，例如午餐时的人群。几位评论者分享了 Elevator Saga 游戏，并抱怨乘客经常同时按上、下按钮，从而降低了算法性能。

**标签**: `#elevator-algorithms`, `#scheduling`, `#simulation`, `#hn-discussion`, `#optimization`

---

<a id="item-2"></a>
## [YC 发布 QM：面向工作的多人智能体指挥框架](https://github.com/yc-software/qm) ⭐️ 8.0/10

YC 发布了 qm，一个开源的“多人智能体指挥框架”（multiplayer agent harness），允许多人共同监督同一个长期运行的智能体任务。它支持按人划分的权限范围（per-person scopes）和共享房间（shared rooms），以便在公司范围内协作使用助手，并提供严格与自动两种工具调用审批模式。 QM 解决了多人智能体中最棘手的问题之一——权限范围（scoping），同时为团队提供了共享工作空间。它验证了共享 AI 智能体控制面这一日益增长的趋势，并让企业能够在沙箱之外运行这种指挥框架，把凭证和 LLM API 密钥保留在循环中，而不是放在沙箱环境里。 该指挥框架在沙箱之外运行，因此凭证不会进入智能体环境，而循环中持有 LLM API 密钥、用户令牌和数据库访问权限。在自动模式下，部署方可以将筛选分类器指向自己的代理；在严格模式下，每个工具调用都会暂停等待人工审批。

hackernews · tosh · 7月31日 18:04 · [社区讨论](https://news.ycombinator.com/item?id=49126604)

**背景**: 多人智能体指挥框架（multi-agent harness）是编排一个或多个 AI 智能体的基础设施，负责管理它们的工具、权限和人工监督；关键在于循环中保存了凭证和上下文，使智能体可以安全地执行任务。多人智能体（multiplayer agents）则将其扩展到团队场景，由多人共同监督同一个长期运行的智能体任务，这就需要对权限范围进行精细设计，以避免特权滥用。最近出现的 Agent Room、共享工作空间等工具，反映了多智能体协作正在向实用控制层转变。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/yc-software/qm">GitHub - yc-software/qm: Multiplayer agent harness for work · GitHub</a></li>
<li><a href="https://www.mendral.com/blog/multi-player-agents-sandbox">Multi - Player Agents Don't Fit in the Sandbox | Mendral</a></li>
<li><a href="https://insights.reinventing.ai/articles/ai-agents-shared-workspaces-small-teams-2026-06-01">Shared AI Agent Workspaces Become a Practical Control Layer ...</a></li>

</ul>
</details>

**社区讨论**: 评论者大多称赞 qm 在权限范围上的设计，认为它为“公司级助手提供了一个合理的答案”；但也有一些人质疑它与 Claude Cowork 等成熟工具的差异，并要求给出“QM 与 Cowork 的对比”。还有人提到了相邻项目（Buzz、AQ、gstack），并提出了关于 Hermes 或“openclaw”式智能体系统的问题。

**标签**: `#AI agents`, `#multiplayer`, `#developer tools`, `#YC`, `#agent harness`

---

<a id="item-3"></a>
## [Tailscale 事后分析：可重用认证密钥导致 Hugging Face 入侵](https://tailscale.com/blog/hugging-face-intrusion) ⭐️ 8.0/10

Tailscale 发布了对 Hugging Face 入侵事件的事后分析，指出没有 Tailscale 漏洞被利用。相反，存储在环境文件中的可重用认证密钥使攻击者能够将未经授权的节点注册到 Hugging Face 的 tailnet 中。 这一事件表明，即使使用安全的网状 VPN，糟糕的凭据管理也可能导致严重入侵。它强调了强大告警、临时认证密钥和严格访问控制的必要性，影响了所有依赖 Tailscale 或类似零配置 VPN 解决方案的组织。 该可重用认证密钥在数天内被用来向 Hugging Face 的 tailnet 注册了总共 181 个节点，每个节点都获得了 CI 节点身份标签。Tailscale 将这一事件视为告警缺失，社区专家建议将凭据限定到特定来源/目标，并使用一次性、临时密钥来降低此类风险。

hackernews · bluehatbrit · 7月31日 19:03 · [社区讨论](https://news.ycombinator.com/item?id=49127306)

**背景**: Tailscale 是一种软件定义的网状 VPN，可在设备之间实现安全、零配置的连接。认证密钥用于验证和配置设备；可重用密钥在多次注册后仍然有效，因此一旦泄露就可能被利用。最佳实践包括使用临时的一次性密钥，并避免将其存储在不安全的文件或 shell 历史中。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://tailscale.com/docs/features/access-control/auth-keys">Auth keys · Tailscale Docs</a></li>
<li><a href="https://tailscale.com/docs/features/access-control/auth-keys/how-to/secure-auth-keys">Securely handle an auth key · Tailscale Docs</a></li>
<li><a href="https://en.wikipedia.org/wiki/Tailscale">Tailscale</a></li>

</ul>
</details>

**社区讨论**: 评论普遍称赞 Tailscale 的透明度，尽管有些人认为这篇文章是巧妙地展示 Hugging Face 失误的营销。其他人讨论了技术改进，例如安全检查功能和将认证密钥绑定到特定机器属性，一位评论者认为此次事件表明需要对异常节点注册模式进行更好的告警。

**标签**: `#security`, `#tailscale`, `#credentials`, `#postmortem`, `#vpn`

---

<a id="item-4"></a>
## [DeepSeek 发布 V4-Flash-0731：304B 参数的智能体模型](https://simonwillison.net/2026/Jul/31/deepseek-v4-flash-0731/#atom-everything) ⭐️ 8.0/10

DeepSeek 发布了 DeepSeek-V4-Flash-0731，这是一个拥有 3040 亿参数、具备显著增强智能体能力的新模型，已在 Hugging Face 上提供。其定价为每百万输入 token 0.14 美元、每百万输出 token 0.27 美元，在 Artificial Analysis 智能指数上排名超过 MiniMax M3。 该模型可能在当前主流模型中提供最佳的单位智能价值，将强劲的基准测试表现与远低于竞争对手的成本相结合。它使高端智能体推理能力对开发者更易获得，并可能加剧 LLM 市场的价格竞争。 这个 167GB 的模型支持可配置的推理强度；Simon Willison 发现将推理等级调至'high'后，生成结果远优于默认设置。Artificial Analysis 的散点图显示，其智能得分约为 50，每任务成本约 0.028 美元，位于性价比最佳象限的最左侧。

rss · Simon Willison · 7月31日 23:59

**背景**: DeepSeek 是一家以开源权重模型（如 DeepSeek-V3 和 R1）著称的中国 AI 实验室，这些模型在性能与价格上对西方 LLM 领头羊形成了挑战。Artificial Analysis 智能指数将多项基准测试整合为一个分数，用于比较模型智能，而每任务成本则衡量与智能相对应的定价。智能体 AI 指能够自主规划并执行多步骤任务的模型，这是新版本中日益强调的前沿能力。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://artificialanalysis.ai/models/">Comparison of AI Models across Intelligence, Performance, and Price</a></li>
<li><a href="https://www.ibm.com/think/topics/agentic-ai">What is Agentic AI? | IBM</a></li>
<li><a href="https://analyticalinsider.ai/blog/top-50-llm-comparison-price-performance-2026">Top 50 LLM Comparison: Price vs Performance 2026 (With Value Scores) | Analytical Insider</a></li>

</ul>
</details>

**标签**: `#AI`, `#DeepSeek`, `#LLM`, `#model release`, `#agentic`

---

<a id="item-5"></a>
## [无状态 MCP 重新引发兴趣并催生新项目](https://simonwillison.net/2026/Jul/31/stateless-mcp/#atom-everything) ⭐️ 8.0/10

Simon Willison 撰文表示，2026-07-28 发布的 Model Context Protocol 规范引入了无状态（stateless）MCP，这是该协议自发布以来最重要的变更。这一更新重新燃起了他对协议的兴趣，并促使他构建了 mcp-explorer（用于交互式探索 MCP 服务器的 CLI 工具）以及 datasette-mcp。 无状态设计省去了服务器维护会话状态的需求，使 MCP 的实现和大规模部署变得简单得多。这有望推动 MCP 作为 LLM 工具集成标准的普及，尤其有利于较小模型和更易审计的智能体（agent）架构。 新的无状态流程只需一个 HTTP 请求，使用 MCP-Protocol-Version 和 Mcp-Method 等请求头，取代了依赖 Mcp-Session-Id 的“先 initialize 再调用”两步流程。这简化了客户端和服务端实现，也无需再将同一会话的请求路由到同一后端实例。

rss · Simon Willison · 7月31日 23:13

**背景**: Model Context Protocol 由 Anthropic 于 2024 年 11 月推出，是一种将 AI 应用（如 LLM）连接到外部工具和数据源的开源标准。它在 2025 年获得了巨大关注，但后来在一定程度上被 Anthropic 的 Skills 方法所掩盖。无状态协议通常能带来更好的可观察性、可靠性和可扩展性，因为服务器无需在请求之间保存会话状态。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Stateless_protocol">Stateless protocol</a></li>
<li><a href="https://en.wikipedia.org/wiki/Model_Context_Protocol">Model Context Protocol</a></li>

</ul>
</details>

**社区讨论**: 在 Hacker News 上关于无状态 MCP 规范的讨论中，基础设施运营者表达了强烈支持，一位网关维护者提到他们相当一部分 bug 都源于需要维护服务端会话状态。

**标签**: `#MCP`, `#AI agents`, `#protocol`, `#LLM`, `#developer tools`

---

<a id="item-6"></a>
## [特朗普政府拟向留学生收 10 万美元毕业后工作费](https://www.bloomberg.com/news/articles/2026-07-30/trump-weighs-100-000-fee-for-foreign-students-to-work-post-grad) ⭐️ 8.0/10

特朗普政府正考虑向国际学生收取 10 万美元费用，以允许他们通过选择性实践培训（OPT）在毕业后留美工作。该提议仍在讨论中，尚未正式公布为政策。 若实施，该费用将严重冲击依赖国际学生学费的高校，以及聘用国际毕业生的科技和金融企业。去年秋季近 30 万国际学生持 OPT 留美，这将是美国人才输送渠道的重大变化。 该费用将适用于 OPT 项目，该项目允许 F-1 学生在其专业领域工作最多 12 个月（STEM 专业可延长至 24 个月）。政府还曾对 H-1B 签证提出类似费用，但 6 月被联邦法官裁定违法，白宫正在上诉。

telegram · zaihuapd · 7月31日 09:00

**背景**: OPT 是一种临时工作许可，允许 F-1 国际学生在美国获得与专业直接相关的实际工作经验，通常也是通往 H-1B 签证的跳板。H-1B 签证允许美国雇主聘用需要至少本科学历的专业职业的外国人才。政府近期还缩短了学生签证居留期限至四年，反映出对国际学生政策的整体收紧。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Optional_Practical_Training">Optional Practical Training - Wikipedia</a></li>
<li><a href="https://www.uscis.gov/working-in-the-united-states/students-and-exchange-visitors/optional-practical-training-opt-for-f-1-students">Optional Practical Training (OPT) for F-1 Students - USCIS</a></li>
<li><a href="https://en.wikipedia.org/wiki/H-1B_visa">H-1B visa - Wikipedia</a></li>

</ul>
</details>

**标签**: `#immigration policy`, `#international students`, `#tech workforce`, `#OPT`, `#H-1B`

---

<a id="item-7"></a>
## [MiniMax 将于 8 月 3 日开源 H3 多模态视频模型](https://modelscope.cn/models/MiniMax/MiniMax-H3) ⭐️ 8.0/10

MiniMax 宣布其新一代通用多模态视频模型 H3 将于 8 月 3 日在魔搭社区（ModelScope）开源。该模型原生支持文本、图像、音频和视频的理解与生成。 此次发布将一个前沿的开源权重视频生成模型带入开源 AI 生态，该模型支持原生音频与多参考素材，有望让影视、广告、电商和游戏等领域在不依赖商业闭源 API 的情况下进行高质量、可投入生产的内容创作。 根据早期文档，MiniMax H3 可生成最高 2K 分辨率、时长 15 秒、带原生立体声的视频。它最多可输入 9 张参考图像以控制主体和风格、3 段视频片段提供动作参考、3 段音频片段进行引导，并支持多维度的精准编辑控制。

telegram · zaihuapd · 7月31日 12:37

**背景**: 开源模型意味着将其权重和代码公开发布，供用户使用、修改和研究，通常通过阿里巴巴的魔搭社区（ModelScope）等平台提供模型托管、推理和部署工具。MiniMax 是一家中国 AI 公司，致力于构建覆盖文本、图像、音频和视频的基础模型。像 H3 这样的多模态视频模型旨在统一多种输入输出类型的理解与生成，例如根据一张图片、风格参考、音频片段和文本提示生成连贯的视频。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://fal.ai/minimax-h3">MiniMax H3 - Open-Weights General-Purpose Multimodal Video Model | fal</a></li>
<li><a href="https://www.minimax.io/blog/minimax-h3">MiniMax H3: An Open Model Breaking the Boundaries Between Tasks and Modalities - MiniMax Research | MiniMax</a></li>
<li><a href="https://modelscope.ai/home">Home Page · ModelScope</a></li>

</ul>
</details>

**标签**: `#AI`, `#multimodal`, `#video generation`, `#open-source`, `#MiniMax`

---

<a id="item-8"></a>
## [最高法院拒审 AI 版权案，维持人类创作原则](https://t.me/zaihuapd/42900) ⭐️ 8.0/10

3 月 2 日，美国最高法院拒绝受理 Stephen Thaler 的上诉，维持了下级法院的裁定，即根据版权法要求人类作者身份，AI 生成作品不受版权保护。 这一决定暂时明确了在美国纯粹由 AI 创作的作品不能获得版权保护，影响到依赖生成式 AI 的艺术家、技术专家和企业。随着 AI 工具日益普及，它强化了法律障碍，可能影响 AI 产出的使用和商业化方式。 该案涉及 Thaler 的 AI 系统 DABUS 自主创作的一件视觉艺术品，但美国版权局和下级法院以缺乏人类作者为由驳回了申请。最高法院拒绝受理上诉是一种程序性行为，而非实体裁决，但暂时维持了人类作者要求。

telegram · zaihuapd · 7月31日 13:11

**背景**: DABUS（统一感觉自主引导装置）是 Stephen Thaler 开发的 AI 系统，据称能自主构思新颖产品和艺术作品。Thaler 还在多个国家为 DABUS 生成的发明寻求专利保护，引发了关于 AI 能否被列为发明人的全球争议。根据美国版权法，保护通常要求人类作者身份，这一原则源于宪法通过赋予作者权利来促进创造性进步的目标。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/DABUS">DABUS - Wikipedia</a></li>
<li><a href="https://www.linkedin.com/pulse/can-ai-inventor-global-dabus-rulings-future-patent-law-devak-bhardwaj-0cuif">Can an AI Be an "Inventor"? The Global DABUS Rulings and the...</a></li>
<li><a href="https://www.linklaters.com/en/insights/blogs/digilinks/2023/december/ai-systems-cannot-be-patent-inventors">AI systems cannot be patent inventors</a></li>

</ul>
</details>

**标签**: `#AI`, `#copyright`, `#legal`, `#intellectual property`, `#generative AI`

---

<a id="item-9"></a>
## [谷歌确认 Android 开发者验证分免费和付费两档，不公开开发者名单](https://t.me/zaihuapd/42911) ⭐️ 8.0/10

谷歌已确认，Android 16 将推出新的开发者验证系统，要求侧载应用开发者注册包名和签名密钥。验证分为付费和免费两档，付费档需支付 25 美元，与 Google Play 注册费一致；免费档仅需邮箱注册，但安装次数有限。 这是一项重大的平台政策变化，因为谷歌的监管范围将扩大到 Play 商店之外安装的应用，影响 F-Droid 等开源应用商店和用户隐私。收集开发者个人信息却不公开开发者名单的做法，可能引发对 Android 生态审查与自主性的担忧。 该验证通过云端检查完成，可能要求设备联网，并可能干扰离线侧载流程。谷歌文档显示，从 2026 年 9 月起，在部分地区通过参与合作的商店下载的应用，必须由经过验证的开发者注册，才能安装到经认证的 Android 设备上。

telegram · zaihuapd · 8月1日 03:08

**背景**: 侧载（sideloading）是指从 Google Play 之外安装 Android 应用的用法，F-Droid 等开源应用商店用户经常采用这种方式。应用签名密钥是一种加密凭据，用于标识应用开发者，谷歌的新系统要求预先注册这些密钥。谷歌表示该验证旨在阻止恶意软件和诈骗，但批评者担心这会加大对独立分发软件的控制。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://developer.android.com/developer-verification">Android developer verification | Android Developers</a></li>
<li><a href="https://support.google.com/android-developer-console/answer/16561738?hl=en">Understanding Android developer verification - Google Help</a></li>
<li><a href="https://en.wikipedia.org/wiki/F-Droid">F-Droid</a></li>

</ul>
</details>

**社区讨论**: Reddit 上的讨论显示，用户担心新的验证体系可能实质上终结 F-Droid 等免费应用来源，并质疑该政策到底为谁的安全服务。有帖子直接发问 F-Droid 是否正面临危险，反映出对开源分发前景的忧虑。

**标签**: `#Android`, `#sideloading`, `#privacy`, `#developer verification`, `#open-source`

---