---
layout: default
title: "Horizon Summary: 2026-11-08 (ZH)"
date: 2026-11-08
lang: zh
---

> 从 34 条内容中筛选出 9 条重要资讯。

---

1. [《极品飞车：地下狂飙 2》借助 WebGPU 实现浏览器在线联机游玩](#item-1) ⭐️ 8.0/10
2. [MaxxBench 检验 DeepSWE 分数在任务规格变动下是否依然成立](#item-2) ⭐️ 8.0/10
3. [Coldframe：伪装成超市冷柜控制器的 Python 蜜罐](#item-3) ⭐️ 8.0/10
4. [研究员发现 macOS 内置未公开守护进程，悄悄构建你的个人关系知识图谱](#item-4) ⭐️ 8.0/10
5. [微软研究院 AI Frontiers 团队据传被解散，John Langford 离职](#item-5) ⭐️ 8.0/10
6. [Asahi Linux 7.3 进展报告：Fedora Asahi Remix 实现同步发布，并表达授权担忧](#item-6) ⭐️ 8.0/10
7. [SemiAnalysis 实地探访内蒙古 800MW 风电 AI 数据中心园区](#item-7) ⭐️ 8.0/10
8. [中国叫停软银 54 亿美元收购 ABB 机器人业务](#item-8) ⭐️ 8.0/10
9. [GitHub 新架构 Rubicon 实现每秒 7200 次推送](#item-9) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [《极品飞车：地下狂飙 2》借助 WebGPU 实现浏览器在线联机游玩](https://nfsu2.xyz/) ⭐️ 8.0/10

nfsu2.xyz 这个网站现在可以直接在网页浏览器中运行 2004 年的完整 PC 赛车游戏《极品飞车：地下狂飙 2》，并借助 WebGPU 进行加速，同时还支持可用的在线多人联机，玩家能够在同一局中一起竞速。该项目在 Hacker News 上获得了 876 分和 239 条评论，用户反馈称在手机和桌面端都能正常游玩。 它展示了浏览器端模拟与 GPU 访问能力已经发展到何种程度：一款二十年前的商业 3A 游戏无需安装即可运行，而且早已停服的联机模式通过逆向工程被重新复活。这种游戏保存与联机复活的结合，暗示着还有许多被抛弃的老游戏有可能重获新生。 由于该网站在未获授权的情况下分发受版权保护的游戏数据，评论者预计会收到下架请求，并指出这款游戏实际上已成为 EA 不再销售的“弃置软件”（abandonware）。Linux 用户反馈需要启用不安全的 WebGPU 特性，例如用相关命令行参数启动 Chromium，才能让渲染正常工作。

hackernews · fluxusars · 11月7日 09:36 · [社区讨论](https://news.ycombinator.com/item?id=50403052)

**背景**: 《极品飞车：地下狂飙 2》由 EA 于 2004 年发行，其官方在线服务早已关闭，零售版在现代硬件上也难以运行。WebGPU 是由 W3C 标准化的 JavaScript API，用于取代 WebGL，通过 Vulkan、Metal 或 Direct3D 12 让网页高效访问系统 GPU，到 2025 年底已登陆所有主流浏览器。在浏览器中运行完整的 PC 游戏通常依赖基于 WebAssembly 的模拟或引擎重制，即用新编写的引擎读取原版游戏的数据文件。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/WebGPU">WebGPU</a></li>
<li><a href="https://en.wikipedia.org/wiki/List_of_game_engine_recreations">List of game engine recreations - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 社区情绪以怀旧和赞赏为主，玩家们回忆起大学时代的电脑和 Xbox 上的游戏时光，并为数百辆车在线上同时烧胎的混乱场面感到兴奋。主要顾虑集中在法律层面：有人认为为此类受版权保护的内容接受或募集捐款颇具争议，也有人希望 EA 对这个弃置软件项目睁一只眼闭一只眼。用户还分享了实用技巧，例如 Linux 上需要使用的 Chromium 启动参数。

**标签**: `#browser-emulation`, `#WebGPU`, `#game-preservation`, `#abandonware`, `#reverse-engineering`

---

<a id="item-2"></a>
## [MaxxBench 检验 DeepSWE 分数在任务规格变动下是否依然成立](https://maxxbench.unlap.ai/research/why-maxxbench/) ⭐️ 8.0/10

MaxxBench 发布了一项方法论研究，通过改变任务规格重新运行 DeepSWE 类型任务，检验已公布的分数是否依然成立，结论是许多结果并不具备良好的泛化性。该研究还暴露出 DeepSWE 自身存在若干 bug，并给出了一条实用建议——大意是“不要使用 max 模式”——这成为评论区讨论的焦点。 基准排行榜经常被用来挑选编程智能体，也常被用来论证模型能力，因此“仅小幅改动任务规格分数就会变化”的证据会削弱人们对这些排名的信心。对于要在真实仓库级工程任务中选型的实践者而言，这一批评尤为重要，因为基准的狭窄设定未必能迁移到实际场景。 其核心方法刻意保持简单：扰动某一个参数或任务规格，然后测量分数变化幅度，而不是把单一的排行榜数字当作固定事实。分析还指出这种崩塌并不均匀——名称中带“-flash”的模型以及更小的变体表现最差——并且 DeepSWE 至少部分任务存在潜在 bug，这意味着测得的差距中有一部分可能来自基准缺陷而非模型能力。

hackernews · antiuniverse · 11月7日 17:19 · [社区讨论](https://news.ycombinator.com/item?id=50406222)

**背景**: DeepSWE 是一个长周期软件工程智能体基准，要求智能体端到端自主解决真实的仓库级编程问题，通常通过 mini-swe-agent 之类的执行框架在无网络的隔离容器中运行。其任务是从零编写而非改编自既有 commit 或 PR，目的是让基准免受数据污染。MaxxBench 的研究问的不是“谁得分最高”，而是当任务呈现方式发生变化时，某个 DeepSWE 分数是否稳定到具有参考意义。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://deepswe.datacurve.ai/">DeepSWE measures frontier coding agents on original, long-horizon...</a></li>
<li><a href="https://llm-stats.com/benchmarks/deepswe">DeepSWE Leaderboard | LLM Stats</a></li>
<li><a href="https://news.ycombinator.com/item?id=50406222">MaxxBench – "Nice DeepSWE score. But is it true?" | Hacker News</a></li>

</ul>
</details>

**社区讨论**: Hacker News 的评论者普遍欢迎这一批评，有人主张“改变一个参数、观察分数如何变化”应当成为任何基准的默认一阶鲁棒性检验。也有人聚焦于被披露的 DeepSWE bug，认为一个被广泛引用的基准出现这类缺陷会侵蚀信任；还有评论者指出较小的“-flash”模型崩塌最严重的规律，另有观点认为问题与其说在于直接在基准上训练，不如说在于实验室构建的强化学习环境过于粗糙，未能对任务复杂度做足够变化。

**标签**: `#LLM benchmarks`, `#model evaluation`, `#AI/ML`, `#benchmark validity`, `#DeepSWE`

---

<a id="item-3"></a>
## [Coldframe：伪装成超市冷柜控制器的 Python 蜜罐](https://github.com/hedgerow-dev/coldframe) ⭐️ 8.0/10

一位开发者发布了 Coldframe，这是一个仅使用 Python 标准库、单文件实现的蜜罐，可高度还原 Danfoss AK-SM 800A 与 Dixell XWEB 超市制冷控制器的 Web 界面，并且这两套“人设”目前在 Shodan 上都被识别为真实设备而非蜜罐。两个实例上线一天后，只观测到通用互联网扫描器和 Shodan 的爬虫 refrigerator.census.shodan.io 的访问。 零售制冷是一个曝光度低但影响巨大的 OT 攻击面：近期欧洲发生的事件据称将数百家门店的制冷设备切换到除霜模式，导致食品变质与运营中断。一个低成本且高度逼真的诱饵，可以让防御方和研究者观察针对暴露在互联网上的 ICS 的真实攻击手法，而不只是依靠漏洞库去推测。 为了与真实设备一致，作者依据 Shodan 记录复制了响应头顺序、页面标题、证书字段和 TLS 版本——Danfoss 人设按照真实 AK-SM 800A 的顺序发送 nginx 头，而 Dixell 人设不发送 Server 头，并把页面填充到恰好 8,202 字节。该蜜罐还能识别 CVE-2025-41450（Danfoss 的“当日代码”登录绕过）以及另外三个 Danfoss CVE 和多个 XWEB 漏洞；使用默认口令登录后会进入一个带除霜按钮的虚假门店仪表盘，从而捕获攻击者的第二阶段行为。

hackernews · hedgerow-dev · 11月7日 17:27 · [社区讨论](https://news.ycombinator.com/item?id=50406292)

**背景**: 超市制冷系统由 Danfoss AK-SM 800A、Copeland/Dixell XWEB 系列等系统管理器管理，这些设备提供基于 Web 和 Modbus 的接口用于监控温度和告警，并且常常使用默认口令就能直接从互联网访问。近期据称有攻击者攻陷了欧洲多家超市的此类控制器并远程触发除霜模式。CVE-2025-41450 是一个不当身份认证漏洞，影响 4.2 版本之前的 Danfoss AK-SM 8xxA 系列，可导致认证绕过。蜜罐是一种诱饵系统，用于在不暴露生产设施的前提下吸引并研究攻击者活动。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.bleepingcomputer.com/news/security/hackers-disrupt-refrigeration-systems-at-european-supermarkets/">Hackers disrupt refrigeration systems at European supermarkets</a></li>
<li><a href="https://nvd.nist.gov/vuln/detail/CVE-2025-41450">NVD - CVE - 2025 - 41450</a></li>
<li><a href="https://www.danfoss.com/en/products/dcs/electronic-controls/products/system-managers/">System manager components | Easy to use | Danfoss</a></li>

</ul>
</details>

**社区讨论**: 评论者对以 Shodan 数据作为真实基线表示怀疑，指出许多暴露在互联网上的设备本身就是蜜罐，其余往往也已被攻陷，因此购买一台真实设备进行本地探测会是更好的基准。作者补充说，血库可能是更具伤害性的目标，并认为超市根本没有安全团队，因此安全默认配置必须由厂商和安装商提供；也有人质疑所谓“黑客攻击”实际上可能是一次大规模的同步软件更新，并指出影响似乎是按国家逐一出现的。

**标签**: `#security`, `#honeypots`, `#ICS/OT`, `#show-hn`, `#threat-intelligence`

---

<a id="item-4"></a>
## [研究员发现 macOS 内置未公开守护进程，悄悄构建你的个人关系知识图谱](https://8rank.ai/game/apple-intelligence-personal-knowledge-graph) ⭐️ 8.0/10

一位安全研究人员的逆向分析文章指出，自 2022 年 macOS 13 起，每台 Mac 都内置了两个未公开的后台守护进程——knowledgeconstructiond 与 intelligenceplatformd，它们会协同在设备本地构建一个“个人知识图谱”，把你的联系人、这些人彼此之间的关系、你与他们的沟通方式以及你的行踪关联起来。该分析基于对 macOS 26 中 Apple Intelligence 组件的检查，描述了一个在 Intel 与 Apple 芯片 Mac 上都会运行的持久化图谱构建子系统，其中还包含对家庭关系等推断出的分类。 这让一个主流消费级操作系统在未明确披露的情况下，悄悄推断敏感的社会关系（包括谁是你的家人），这与苹果一贯宣称的“隐私优先”形象相矛盾，也与 GDPR 等针对推断性个人数据的规定存在张力。由于该系统在本地运行并为 Apple Intelligence 功能提供数据，它也加剧了一个争论：仅仅因为在设备端处理，是否就足以正当化用户从未主动选择加入的数据收集。 据报道，这些守护进程并非局限在单一应用的沙盒内，而是作为一个持久化的图谱构建子系统运行，在 Intel 和 Apple 芯片硬件上都会把联系人、行为与硬件状态悄悄关联起来；此次披露也呼应了 Nic Lydon 早前的独立工作，他在构建自己的个人知识图谱时发现了同一个数据库。苹果并未公开记录该系统，作者还发布了关于该知识图谱的后续研究。

hackernews · infwhispers · 11月7日 09:46 · [社区讨论](https://news.ycombinator.com/item?id=50403097)

**背景**: 知识图谱是一种以实体和关系来存储事实的数据结构（例如“Alice——是——Bob 的姐妹”），使软件能够基于关联进行推理，而不仅仅是匹配关键词。Apple Intelligence 这类设备端 AI 功能需要这种上下文记忆，才能回答“我妹妹的航班是几点”之类的问题，厂商也主张在本地而非云端处理可以保护隐私。问题在于，这种推断本身——包括判断谁算作家人——是在用户完全不知情的情况下进行的，这正是研究者和评论者所质疑的地方。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://8rank.ai/game/apple-intelligence-personal-knowledge-graph">Anatomy of Apple 's Personal Knowledge Graph — Eighth Rank</a></li>
<li><a href="https://techplanet.today/post/apples-hidden-personal-knowledge-graph-understanding-macoss-undocumented-family-classifier">Apple's Hidden Personal Knowledge Graph: Understanding macOS ...</a></li>
<li><a href="https://techbytes.app/posts/every-mac-comes-with-an-undocumented-family-member-classifier/">Every Mac comes with an (undocumented) family member classifier</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上的讨论（658 分、368 条评论）整体情绪不安：一位评论者表示，这类数据如果可以选择加入，过去会觉得很有趣，但现在只感到疲惫，并提出社会层面的担忧——每一段对话都被记录，会剥夺人际关系所依赖的“自然遗忘”。其他人指出，离开苹果生态可以减少暴露，但谷歌对应的画像恐怕会更糟；还有多人引用史蒂夫·乔布斯 2010 年的说法：隐私意味着用平实的语言、反复地告诉用户数据将被如何使用。

**标签**: `#privacy`, `#apple`, `#macos`, `#knowledge-graph`, `#on-device-ai`

---

<a id="item-5"></a>
## [微软研究院 AI Frontiers 团队据传被解散，John Langford 离职](https://hunch.net/?p=13764006) ⭐️ 8.0/10

微软研究院纽约实验室的合伙人级研究员经理 John Langford 在其博客《Machine Learning (Theory)》上宣布已离开微软，并宣告 AI Frontiers 团队终结。AI Frontiers 是微软研究院旗下专注于高效语言模型与智能体系统前沿研究的实验室。 一家全球顶尖工业研究机构中颇具代表性的探索型实验室被解散，被外界解读为大公司正围绕 Transformer 规模化路线收敛，并降低开放式 AI 研究的优先级。对于关注基础 AI 研究何去何从的研究者而言，这意味着工业界实验室内的自由探索空间正在收窄。 根据 Langford 的文章及围绕它的讨论，问题与其说是放弃 Transformer，不如说是组织层面的摩擦——办公室政治、管理不善，以及研究成果向产品转化不力。值得注意的是，微软研究院 AI Frontiers 的页面如今显示该实验室已于 9 月并入 Microsoft AI，说明这更像是一次重组而非单纯的关停。

hackernews · srean · 11月7日 18:02 · [社区讨论](https://news.ycombinator.com/item?id=50406563)

**背景**: 微软研究院（MSR）长期以来是计算领域规模最大的企业基础研究机构之一，其文化建立在一个简单的默契之上：做好研究，好事自然会发生，而不必背负交付产品的压力。AI Frontiers 是其较新的实验室之一，瞄准高效语言模型与智能体系统的前沿工作。与此同时，整个 AI 领域已收敛到 Transformer 架构上——通过扩大参数、数据和算力，性能可以可预期地提升，相比探索性替代方案，这条路昂贵但风险更低。John Langford 是知名机器学习研究者与学习理论专家，多年来在其博客上撰文讨论机器学习如何从一门学科转变为一种工业工具。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.microsoft.com/en-us/research/lab/ai-frontiers/">Microsoft Research AI Frontiers - Microsoft Research</a></li>
<li><a href="https://businessexaminer.ca/victoria-articles/item/microsoft-researcher-john-langford-exits-as-ai-frontiers-group-is-declared/">Microsoft Researcher John Langford Exits as AI ... | Business Examiner</a></li>
<li><a href="https://en.wikipedia.org/wiki/John_Langford_(computer_scientist)">John Langford (computer scientist) - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 评论者大体认同这反映了一种行业普遍现象：Transformer 规模化被视为一条安全的高速公路，而对其他 AI 方法的探索性研究则受到抑制，有人指出 Meta 同样让其此前的研究负责人边缘化。不少人对数百亿美元几乎押注在同一个想法上感到惋惜，并认为微软研究院那条"做好研究，好事自然会发生"的隐性契约在现任领导层下被反复打破，正在摧毁研究文化。也有反对意见指出，Langford 并未说他们停止了 Transformer 研究——他还提到了一种具体的 Transformer 变体——真正的问题在于办公室政治与执行不力，而 Qwen、DeepSeek 等实验室证明在大模型上创新依然能带来惊人成果。

**标签**: `#AI research`, `#Microsoft Research`, `#industry trends`, `#research culture`, `#transformer models`

---

<a id="item-6"></a>
## [Asahi Linux 7.3 进展报告：Fedora Asahi Remix 实现同步发布，并表达授权担忧](https://asahilinux.org/2026/11/progress-report-7-3/) ⭐️ 8.0/10

Asahi Linux 发布了 Linux 7.3 进展报告，其中重点提到 Fedora Asahi Remix 在 11 月 3 日 Fedora Linux 45 发布当天同步推出，这是该项目首次做到与上游同日发布。报告还介绍了 Apple Silicon 平台支持的持续开发工作，并对有第三方利用项目宽松的开源许可证来“劫持”其成果、把 Apple Silicon 上的 Linux 用于激进商业变现表示担忧。 同步发布意味着 Apple Silicon Mac 用户能够直接获得 Fedora 的最新特性和修复，而不必像过去那样等待数周，使 Fedora Asahi Remix 不再像是“二等下游”发行版。授权方面的警告对整个开源生态同样重要，因为它提出了一个问题：宽松许可证是否会让这类重度依赖逆向工程的项目容易被他人改头换面并商业收割。 报告的定位是把“同日发布”视为一项工程与流程上的里程碑，而非功能里程碑，说明其下游构建与质量验证流水线已经成熟；授权部分则提到存在多起利用项目宽松条款的尝试，其明确目标是取代这个项目。硬件支持方面仍是渐进推进，较新的 Apple SoC 世代以及 USB-C 外接显示输出等长期缺口依然困扰用户。

hackernews · ackyshake · 11月7日 05:20 · [社区讨论](https://news.ycombinator.com/item?id=50401867)

**背景**: Asahi Linux 是一个由志愿者推动的项目，通过逆向工程苹果未公开文档的系统级芯片（SoC），把 Linux 内核及相关软件移植到 Apple Silicon Mac 上。Fedora Asahi Remix 是其旗舰发行版，基于 Fedora Linux 构建，并以 KDE Plasma 作为默认桌面环境。该项目经历过组织层面的动荡，包括创始人 Hector Martin 于 2025 年 2 月辞去项目负责人一职，因此发布工程方面的里程碑与治理问题对其社区而言格外重要。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://asahilinux.org/2026/11/progress-report-7-3/">Progress Report: Linux 7.3 - Asahi Linux</a></li>
<li><a href="https://en.wikipedia.org/wiki/Asahi_Linux">Asahi Linux - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 评论者普遍对同日发布给予正面评价，一些长期资助者称这是项目走向成熟的积极信号；但多位用户表示，缺少 USB-C 外接显示支持仍是他们在 MacBook Air 上日常使用 Asahi 的硬性障碍，也有人质疑为何新 CPU 支持会排在这一功能之前。还有人猜测授权警告具体指向哪个下游项目，并认为项目当初就应采用 copyleft 许可证；同时有开发者借机宣传自己的竞争项目，声称已支持 Vulkan 1.4、M4/M5，并实现了休眠到内存（suspend to RAM）。

**标签**: `#Linux`, `#Apple Silicon`, `#Asahi Linux`, `#Fedora`, `#Open Source`

---

<a id="item-7"></a>
## [SemiAnalysis 实地探访内蒙古 800MW 风电 AI 数据中心园区](https://newsletter.semianalysis.com/p/we-visited-chinas-stargate-in-inner) ⭐️ 8.0/10

SemiAnalysis 发布了一篇来自内蒙古的实地考察报告，介绍了一个规划总容量达 800MW 的风电驱动 AI 数据中心园区，其中约 120MW 在一年之内建成。该园区还部署了一个 5MW 的试点项目，采用固态变压器直接输出 800V 直流电，并采用了完全取消中央冷水机组的制冷设计。 这样的建设速度和供电架构表明，中国运营商在施工进度和下一代直流供电方面可能比许多西方超大规模厂商走得更快；在 AI 扩张越来越受制于能源和电网接入而非单纯芯片供应的背景下，这一点尤为关键。如果固态变压器原生 800V 直流与无冷水机组方案能在大规模下经受验证，它们有可能成为全球 AI 园区的参考设计。 该 800V 直流试点功率为 5MW，被称为“固态变压器原生”，即固态变压器直接在中压交流电网与 800V 直流母线之间完成隔离变换，而不经过传统的交流变压与整流环节。取消中央冷水机组意味着依赖自然冷却/免费冷却和液冷服务器，这一方案在内蒙古寒冷气候下效果很好，但在更炎热潮湿的地区适用性较窄。

rss · Semianalysis · 11月7日 19:01

**背景**: AI 训练集群的机架功率密度已远超传统交流供配电方式所能高效承载的范围，推动业界转向 800V 直流架构，以减少变换级数和铜损。固态变压器用电力电子器件取代笨重的铁芯铜绕组变压器，在实现中压交流侧电气隔离的同时直接输出直流电。无冷水机组制冷则利用室外空气或水侧经济器替代机械冷水机组，谷歌在比利时、微软在爱尔兰都曾采用；内蒙古寒冷多风且风电资源丰富，非常适合把这三项思路在超大规模下组合起来。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.electronicdesign.com/technologies/power/product/55371996/electronic-design-novel-solid-state-transformer-supports-800-v-dc-power-in-ai-data-centers">Novel Solid-State Transformer Supports 800-V DC Power in AI ...</a></li>
<li><a href="https://www.eaton.com/content/dam/eaton/markets/data-center/the-impact-of-ai/whitepapers/eaton-deploying-800vdc-architecture-whitepaper-en-us.pdf">eaton deploying 800vdc architecture whitepaper en us</a></li>
<li><a href="https://www.datacenterknowledge.com/hyperscalers/microsoft-s-chiller-less-data-center">Microsoft's Chiller - less Data Center</a></li>

</ul>
</details>

**标签**: `#AI infrastructure`, `#data centers`, `#China`, `#energy`, `#cooling`

---

<a id="item-8"></a>
## [中国叫停软银 54 亿美元收购 ABB 机器人业务](https://t.me/zaihuapd/44988) ⭐️ 8.0/10

11 月 5 日，ABB 确认已收到中国外商投资安全审查机构的通知，禁止该交易在中国实施，实际上叫停了软银集团以约 54 亿美元收购 ABB 机器人业务的计划。此举使软银布局人工智能与机器人产业的步伐受挫。 中国约占 ABB 机器人业务 30%的份额，因此禁止该交易在华实施足以危及整笔交易，也表明中国监管审查可以否决两家非中国企业之间的并购。这同时释放出对战略科技领域外资并购审查趋严的信号，在工业机器人与人工智能整合加速的当下加大了此类交易的难度。 据报道，中国监管机构担忧 ABB 机器人业务所涉及的工业数据、供应链信息及核心技术可能被转移至海外，并可能被用于训练人工智能模型。此案也延续了对战略科技交易加强审查的趋势，此前 Meta 的相关交易也曾受到类似审视。

telegram · zaihuapd · 11月7日 11:24

**背景**: ABB 是一家瑞士-瑞典工业巨头，其机器人部门提供工厂自动化机械臂与软件，在中国拥有可观的业务、客户与营收。软银则是日本投资集团，近年持续在人工智能与机器人领域布局。根据中国的外商投资安全审查制度，涉及外方的交易在触及境内运营、数据或关键技术时可能需要审批——即使交易双方都不是中国企业——因此单一司法辖区的否决即可让一笔全球交易停摆。

**标签**: `#robotics`, `#SoftBank`, `#ABB`, `#China regulation`, `#AI industry`

---

<a id="item-9"></a>
## [GitHub 新架构 Rubicon 实现每秒 7200 次推送](https://github.blog/engineering/architecture-optimization/inside-githubs-new-git-storage-architecture/) ⭐️ 8.0/10

GitHub 公布了代号 Rubicon 的全新 Git 存储架构：Git 对象数据存入 Azure Blob Storage，引用则由 Ref-CAS 管理，它是一种基于多数派提交的 compare-and-swap 引用存储。在内部压力测试中，单个仓库可支撑 5000 个 AI 智能体同时操作、每秒最高 7200 次推送，同时读取延迟保持较低水平；该架构目前处于有限私有预览阶段。 AI 编程智能体会对同一个仓库产生突发式提交，这是传统单仓库 Git 存储从未针对设计过的负载模式，因此 Rubicon 能否成功，将决定 GitHub 是否能承载成群的智能体而不拖慢人类开发者的体验。如果该架构能够从私有预览走向大规模推广，也可能改变整个生态中高写入频率超大型仓库的托管方式。 请求先经过名为 Spokes 的路由层，再分发到每个仓库对应的虚拟副本组，这些副本只持有缓存状态；后台节点负责数据包（pack）压缩，而每次 Ref-CAS 事务只锁定它所涉及的引用，并在日志副本多数派记录后即可见。除有限私有预览外，GitHub 尚未公布更大范围开放的时间表。

telegram · zaihuapd · 11月7日 14:12

**背景**: Git 通常把一个仓库存储为一组不可变对象（提交、树对象、文件内容对象）打包成的文件，外加少量可变引用（如分支和标签）指向这些对象。在托管平台上，难点在于许多写入者同时推送时如何保持引用一致，因为对同一分支的并发写入必须被安全地串行化。Rubicon 的做法是把这两件事拆开：把海量对象数据放到廉价且可弹性扩展的 Blob 存储中，把引用协调集中到一个专用的 compare-and-swap 服务里，再在前端增加只做缓存、不持久化的副本来提升读取吞吐。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.blog/engineering/architecture-optimization/inside-githubs-new-git-storage-architecture/">Inside GitHub's new Git storage architecture - The GitHub Blog</a></li>
<li><a href="https://trashexpert.ru/news/software-news/github-rubicon-git-storage-stress-test">GitHub : до 7200 пушей в секунду в тесте архитектуры Rubicon</a></li>

</ul>
</details>

**标签**: `#GitHub`, `#Git storage`, `#architecture`, `#AI agents`, `#scalability`

---