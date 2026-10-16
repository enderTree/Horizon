---
layout: default
title: "Horizon Summary: 2026-10-16 (ZH)"
date: 2026-10-16
lang: zh
---

> 从 39 条内容中筛选出 8 条重要资讯。

---

1. [Citizen Lab：定向广告被改造成零点击间谍软件投放管道](#item-1) ⭐️ 9.0/10
2. [Meta 发布 Muse Spark Open：可在 Mac Studio 本地运行的 816B 开放权重模型](#item-2) ⭐️ 8.0/10
3. [Libreboot 26.10「Ominous Olive」发布：新增 UEFI 与 Chromebook 支持](#item-3) ⭐️ 8.0/10
4. [特斯拉发布新款 Roadster，可选装火箭推进器](#item-4) ⭐️ 8.0/10
5. [Anthropic 向投资者披露第三季度营收达 168 亿美元，筹备 IPO](#item-5) ⭐️ 8.0/10
6. [ASML 被曝正在开发混合键合设备](#item-6) ⭐️ 8.0/10
7. [MIT/PNAS：随机神经元单元可自组织出媲美反向传播的学习回路](#item-7) ⭐️ 8.0/10
8. [苹果首款折叠屏手机 Duo 入选《时代》2026 年度最佳发明](#item-8) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Citizen Lab：定向广告被改造成零点击间谍软件投放管道](https://citizenlab.ca/research/how-discover-tech-turned-targeted-ads-into-a-pipeline-for-spyware/) ⭐️ 9.0/10

多伦多大学 Citizen Lab 发布了一项名为“AdFection”的行动研究报告：据《卫报》和 The Verge 报道，以色列公司 Discover Tech 这类雇佣间谍软件供应商滥用全球定向广告投放基础设施，只需向特定目标展示广告即可入侵其设备，据称已在多个国家感染数十台设备。WIRED、《金融时报》和 TechCrunch 当天均作了报道，这是首次公开有技术证据表明商业间谍软件可借助广告网络大规模分发。 这使几乎每个上网者每天都要经过的广告技术供应链变成了无差别的攻击面，受害者无需点击、安装或访问任何可疑内容就可能被入侵。这也让那些在不知情的情况下投放了恶意广告的广告交易平台、发布方和平台面临严重的责任追问，并可能加速针对监控供应商和程序化广告的监管审查。 社区与媒体评论指出，该报告对投放分发和命令控制（C&C）环节描述得相当详细，但对最核心的技术问题——究竟以何种机制实现“零点击”触发恶意代码执行——依然语焉不详。报告背后团队 Citizen Lab 是多伦多大学蒙克全球事务与公共政策学院下属的跨学科研究实验室，以揭露 Pegasus 等商业间谍软件而闻名。

hackernews · jcomp · 10月15日 10:43 · [社区讨论](https://news.ycombinator.com/item?id=50101813)

**背景**: 零点击间谍软件无需用户任何操作即可感染设备——不必点击链接，也无需打开附件——因此更难被发现和防御，通常只用于高价值目标。“雇佣间谍软件”指私营公司开发并出售给政府的商业监控工具，苹果甚至设有威胁通知系统来提醒被此类攻击单独针对的用户。此次利用的关键在于程序化广告：广告请求要经过广告主、中介、交易平台和实时竞价系统等重重环节才到达用户，这为攻击者提供了许多注入恶意载荷的切入点。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.wired.com/story/nightmare-scenario-zero-click-spyware-is-infecting-phones-via-targeted-ads/">‘Nightmare Scenario’: Zero-Click Spyware Is Infecting Phones ...</a></li>
<li><a href="https://techcrunch.com/2026/10/15/citizen-lab-says-governments-are-abusing-online-ads-to-hack-people-with-zero-click-spyware/">Governments are hacking people with 'zero-click' spyware by ...</a></li>
<li><a href="https://en.wikipedia.org/wiki/Citizen_Lab">Citizen Lab</a></li>

</ul>
</details>

**社区讨论**: 一位有 13 年从业经验的广告技术工程师提出反驳，认为该报道有哗众取宠之嫌，且对真正的零点击激活机制语焉不详，并指出在如此庞杂的生态中根本不存在可以单独追责的“广告提供商”。其他评论者则聚焦以色列在网络监控产业中的突出地位——有人称其为顶级网络强国，有人援引历史上“Download Valley”产业集群——其中数人主张这类公司应被视为国家利益的延伸，也有人只是贴出了 Citizen Lab 的原始报告链接。

**标签**: `#cybersecurity`, `#spyware`, `#adtech`, `#privacy`, `#zero-click-exploits`

---

<a id="item-2"></a>
## [Meta 发布 Muse Spark Open：可在 Mac Studio 本地运行的 816B 开放权重模型](https://research.meta.ai/blog/muse-spark-open) ⭐️ 8.0/10

Meta 发布了 Muse Spark Open，这是一个参数量达 816B 的开放权重模型（在 Hugging Face 上以 Muse-Spark-Open-816B-A42B 为名），并明确针对 Apple Mac Studio 的本地运行做了优化。该模型通过 Meta 研究博客公布后，迅速在社区获得 673 分、364 条评论，成为当周讨论度最高的模型发布之一。 这次发布延续了 Meta 公开可下载权重、而非把能力锁在 API 后面的策略，对 Qwen、GLM 等其他开放权重玩家形成压力，同时试图让 Meta 的模型家族成为默认的本地技术栈。其意义还在于，如此规模的模型若能跑在消费级的 Apple 硬件上，将让那些既想要前沿级能力、又不愿购置数据中心 GPU 或按 token 付费的团队大幅降低门槛。 许可证允许广泛使用，但包含一条“模型即服务”（Model as a Service）条款：如果被许可方及其关联方的合计总收入超过两千万美元，就不得通过 API 或类似接口向第三方提供该模型输出的访问。Meta 在推理运行器支持上也投入甚多，其部署文档覆盖了从 Unsloth 到 MLX 的多种方案。

hackernews · bigwheels · 10月15日 17:47 · [社区讨论](https://news.ycombinator.com/item?id=50107379)

**背景**: 开放权重模型是指训练好的参数被公开发布、任何人都可以下载并自行运行的 AI 模型，与之相对的是只能通过厂商 API 访问的闭源模型；Meta 通过 Llama 系列让这一路线广为人知。命名中的“816B-A42B”沿用了混合专家（MoE）模型的惯例，即用较大的总参数量搭配每 token 只激活的少量参数，从而把推理成本控制在可接受范围。如此规模的模型要在本地运行，只有具备超大统一内存池的机器才现实，这也是 Mac Studio 成为本地大模型热门平台的原因——其最新 M 系列版本可配置高达 512GB 统一内存和约 1.2TB/s 的内存带宽。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.aimodelwaddle.com/muse-spark">Muse Spark : Meta's Model Versions, Pricing, and Open -Weight Status</a></li>
<li><a href="https://openrouter.ai/meta/muse-spark-1.3">Muse Spark 1.3 - API Pricing & Benchmarks | OpenRouter</a></li>
<li><a href="https://toolhalla.ai/blog/best-local-llms-mac-studio-2026">Best Local LLMs for Mac Studio in 2026 | ToolHalla</a></li>

</ul>
</details>

**社区讨论**: 社区情绪褒贬不一：有评论者引用 Artificial Analysis 的数据指出该模型表现不及 Qwen3.8 Flash Next 和 GLM 5.3 Flash（后两者都能在单张 B300 上运行），认为 Meta 在开放权重领域还需追赶，同时批评现有评测只在最高推理档位做对比。也有人聚焦许可证，其中一位用户读完后认为除收入超过两千万美元时的“模型即服务”条款外，商业使用基本被允许；另一位则认为 Meta 是在重演 Llama 的打法，在“智能租赁市场”未能成形之际构建具有黏性的生态护城河。此外有人赞赏其对各类推理运行器的广泛支持，还有评论者表示自己只能通过 OpenRouter 来测试该模型。

**标签**: `#AI`, `#LLM`, `#open-weight models`, `#Meta`, `#model release`

---

<a id="item-3"></a>
## [Libreboot 26.10「Ominous Olive」发布：新增 UEFI 与 Chromebook 支持](https://libreboot.org/news/libreboot2610.html) ⭐️ 8.0/10

Libreboot 26.10 版本以代号「Ominous Olive」发布，集成了 UEFI/EDK2 支持，并新增对 Chromebook 的支持，大幅拓宽了该项目可覆盖的硬件范围。此版本还正式确立了一项严格拒绝 LLM 辅助代码贡献的政策，这一点在社区讨论中成为焦点话题。 通过引入 UEFI/EDK2 与 Chromebook 支持，Libreboot 可服务的设备数量成倍增加，未来移植新机型的难度也大幅降低——社区评论者称这对开源固件这一小众领域而言是「巨大的」进展。这也加强了它与 Heads 等项目在 ChromeOS 移植工作上的联动，后者依赖类似的上游代码。 其 UEFI 支持基于 EDK2，即 TianoCore 提供的 UEFI 开源参考实现；而 Chromebook 相关工作则沿用了 MrChromebox 为 ChromeOS 设备定制 coreboot 固件的思路。反 LLM 的立场记录在该项目 Codeberg 上 lbmk 仓库的 AGENTS 文件中，社区成员还提到 Heads 项目已经合并了首个 ChromeOS 移植，并有多项移植正在进行。

hackernews · iamnothere · 10月15日 12:52 · [社区讨论](https://news.ycombinator.com/item?id=50102923)

**背景**: Libreboot 是一个自由开源固件项目，以 coreboot 发行版的形式提供，就像 Debian 是 Linux 发行版一样，其目标是替换受支持电脑上专有的 BIOS 或 UEFI 固件。coreboot 是一种轻量级开源固件，只完成启动操作系统所需的最基本硬件初始化，而许多 Chromebook 出厂时本就搭载基于 coreboot 的 Google 固件。EDK2（EFI Development Kit II）是 TianoCore 社区的开源开发环境，也是 UEFI 规范的参考实现，最初由 Intel、HP 和 Microsoft 主导。由于 Chromebook 和 UEFI 设备极为普及，同时支持这两种技术，正是 Libreboot 这类项目能够覆盖更多硬件的原因。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Libreboot">Libreboot - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Coreboot">coreboot - Wikipedia</a></li>
<li><a href="https://tuxownia.pl/en/blog/hello-world-with-edk-ii-first-steps-with-uefi/">Hello World with EDK II - First Steps with UEFI - Tuxownia</a></li>

</ul>
</details>

**社区讨论**: 评论者普遍认为 UEFI/EDK 集成与 Chromebook 支持才是真正的亮点，有人称其为「巨大的」进步，因为这让可用设备成倍增加、未来移植更轻松。对反 LLM 政策的看法则存在分歧：一位用户觉得这种做法令人耳目一新，并认为 LLM 辅助编程毫无乐趣；另一位则只是指出该项目「似乎不喜欢 AI」。一位 Heads 项目贡献者确认了基于 MrChromebox 代码的相关 ChromeOS 移植工作，还有一位拥有 Acer「Edgar」系列 Chromebook 的用户表示打算测试这一版本。

**标签**: `#libreboot`, `#coreboot`, `#UEFI`, `#open-source-firmware`, `#chromebook`

---

<a id="item-4"></a>
## [特斯拉发布新款 Roadster，可选装火箭推进器](https://www.tesla.com/roadster) ⭐️ 8.0/10

特斯拉发布了新一代 Roadster，可选装 SpaceX 火箭推进器套件，并宣称具备极端性能；推进器分为两种模式：一种是仅用于额外向前加速的冷气（无燃烧）版本，另一种是在演示视频中出现、仅限受邀用户购买的燃烧式火箭发动机版本。此次发布在 Hacker News 上引发热议，帖子获得 280 分、311 条评论，讨论集中在工程创新性与量产可行性上。 这次发布把一款主流消费级车型推向航天器级别的推进技术，是特斯拉产品路线与 SpaceX 硬件及工程文化深度捆绑的最明确信号。同时它也是对特斯拉承诺可信度的一次检验：公司一边许诺革命性能力，一边仍在为 Cybertruck 的量产与质量问题上挣扎。 据报道，冷气推进器直接作用于车身而非通过车轮传递推力，从而绕开了轮胎抓地力的物理限制，而储存高压气体最自然的方案是 SpaceX 常用的复合材料缠绕压力容器（COPV）。燃烧式火箭版本仅限受邀用户、且只在视频中亮相，目前没有公布任何监管路径、价格或交付时间。

hackernews · shekhar101 · 10月16日 01:32 · [社区讨论](https://news.ycombinator.com/item?id=50112657)

**背景**: Roadster 是特斯拉 2008 年推出的首款跑车；第二代 Roadster 于 2017 年发布，宣称 0-60 英里加速不到 2 秒、续航超过 600 英里，但此后一再跳票。冷气推进器是最简单的火箭发动机形式，通过喷管排出加压惰性气体来产生推力，全程不发生燃烧，广泛用于 SpaceX 的 Dragon 飞船等航天器上执行姿态控制与机动。相关讨论还默认读者了解特斯拉 Cybertruck 的量产困境，以及外界长期关于特斯拉与 SpaceX 最终可能合并的猜测。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Cold_gas_thruster">Cold gas thruster - Wikipedia</a></li>
<li><a href="https://www.techtimes.com/articles/327773/20260920/tesla-roadster-lands-oct-1-reveal-spacex-thrusters-bypass-tire-grip-physics.htm">Tesla Roadster Lands Oct 1 Reveal: SpaceX Thrusters Bypass...</a></li>

</ul>
</details>

**社区讨论**: Hacker News 的评论者对这辆车"真的能飞"表示由衷惊叹，并称赞其更利落的外观才是 Cybertruck 应有的样子；但主流情绪是对执行力的怀疑：一条高赞评论警告说，鉴于 Cybertruck 的量产问题，现在预订就是犯傻，认为特斯拉用一页满是革命性承诺的宣传"烧掉了自己的工程信誉"。还有评论者把整场发布解读为特斯拉将被 SpaceX 吸收的前奏。

**标签**: `#Tesla`, `#Roadster`, `#Electric Vehicles`, `#SpaceX`, `#Product Announcement`

---

<a id="item-5"></a>
## [Anthropic 向投资者披露第三季度营收达 168 亿美元，筹备 IPO](https://simonwillison.net/2026/Oct/15/anthropic-tells-investors/) ⭐️ 8.0/10

Anthropic 周三接待了投资者，并告知其第三季度（7 月至 9 月）营收环比增长近 50%至 168 亿美元，高于第二季度的 115 亿美元和第一季度的约 48 亿美元，公司正在筹备 IPO。同时，Anthropic 还披露“蒸馏”行为贡献了其 5%至 7%的营收，但在第三季度已“大幅”削减了这部分业务。 这一披露罕见地展示了一家前沿 AI 实验室在 IPO 规模下的经济状况，显示出营收环比高速增长以及在算力支出上的正向回报。它还揭示出，竞争对手曾向 Anthropic 支付数亿美元以利用其模型输出进行训练，而 Anthropic 如今正有意压缩这一收入来源，这将影响依赖它的竞争厂商。 Anthropic 称第三季度每在算力上花费 1 美元可带来 1.70 美元营收，剔除股权激励后的调整后营业利润率为 11%。Simon Willison 的粗略估算指出，若蒸馏占第二季度营收的 5%，那么未具名的竞争对手当季为蒸馏 Anthropic 的模型花费了超过 5 亿美元；值得注意的是，Anthropic 在投资者沟通中似乎已不再使用“年化运行率营收”这一指标。

rss · Simon Willison · 10月15日 13:04

**背景**: Anthropic 是 Claude 系列模型背后的 AI 实验室，IPO（首次公开募股）意味着其股票将在公开交易所上市。通常所说的“蒸馏”指模型压缩，即训练一个较小的“学生”模型去模仿较大“教师”模型的输出；但在此处，它指的是竞争对手大规模调用 Anthropic 的 API，并用 Claude 的输出来训练自家模型。“调整后营业利润率”是一种盈利能力的衡量口径，会剔除股权激励等非现金成本；而“年化运行率营收”是创业公司常用的指标，通过将近期营收乘以年化系数来推算全年数字。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Knowledge_distillation">Knowledge distillation - Wikipedia</a></li>
<li><a href="https://www.geeksforgeeks.org/nlp/what-is-llm-distillation/">What is LLM Distillation? - GeeksforGeeks</a></li>

</ul>
</details>

**标签**: `#Anthropic`, `#AI industry`, `#IPO`, `#revenue`, `#distillation`

---

<a id="item-6"></a>
## [ASML 被曝正在开发混合键合设备](https://newsletter.semianalysis.com/p/asml-is-building-a-hybrid-bonding) ⭐️ 8.0/10

SemiAnalysis 报道称，ASML 正在开发一款混合键合（hybrid bonding）设备，依据来自该公司的专利申请文件、一则新闻报道以及其自身的技术路线图，尽管 ASML 尚未发布任何官方公告。这一披露意味着这家荷兰光刻机巨头可能在其核心扫描机业务之外开辟新的产品线。 混合键合是先进封装和 3D 芯片堆叠的关键技术，在晶体管微缩放缓的背景下，台积电、英特尔以及 HBM 存储厂商都在该领域大举投入。若 ASML 真的进入这一设备市场，可能重塑先进封装设备的竞争格局，并进一步强化其在半导体供应链中本已核心的地位。 目前证据均为间接来源——专利、新闻报道和 ASML 的路线图——该产品尚未获得官方确认，因此时间表、规格参数和目标客户都还是未知数。混合键合工艺难度很高，键合后焊盘与通孔之间的对准误差会直接影响性能和良率，这对拥有精密光刻专长的 ASML 而言是一个自然的业务延伸。

rss · Semianalysis · 10月15日 19:27

**背景**: 混合键合是一种直接将两片晶圆或芯片键合在一起的技术，它同时利用金属电极（通常是铜焊盘）和绝缘介质层，无需焊球即可形成高密度的垂直电连接。它是先进封装的关键使能技术；先进封装指的是一系列达到晶圆厂级别的工艺——例如 2.5D 中介层、3D IC、chiplet（小芯片）集成和晶圆堆叠——通过把多个芯片封装在一起提升性能，同时规避单体芯片制程不断微缩所带来的成本上升与良率下降问题。ASML 最为人熟知的是用于最先进逻辑芯片图形化的极紫外（EUV）光刻系统，近年来也在向量测与检测领域扩展业务。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Advanced_packaging_(semiconductors)">Advanced packaging (semiconductors)</a></li>
<li><a href="https://www.evgroup.com/">EV Group | Semiconductor Manufacturing Equipment and Process...</a></li>
<li><a href="https://aei.dempa.net/archives/25028">Toray Develops New Insulating Resin for Hybrid Bonding | AEI</a></li>

</ul>
</details>

**标签**: `#ASML`, `#hybrid bonding`, `#semiconductor manufacturing`, `#advanced packaging`, `#lithography`

---

<a id="item-7"></a>
## [MIT/PNAS：随机神经元单元可自组织出媲美反向传播的学习回路](https://www.reddit.com/r/MachineLearning/comments/1x6hmyg/how_artificial_neural_networks_build_their_own/) ⭐️ 8.0/10

MIT 于 2026 年 10 月 13 日发布报道，介绍 10 月 9 日刊登于 PNAS 的论文《How Biological Synapses Self-Assemble Gradient Learning》。该研究表明，由共享局部可塑性规则驱动的随机互联类神经元单元，能够自组织形成具备模式识别与图像分类能力的学习回路，其报告的性能与用于对比的反向传播训练网络相近。 这一结果重新定义了争论焦点：学习机制究竟必须被显式设计，还是可以从简单的局部规则中自发涌现；同时它也为反向传播提供了一条更具生物合理性的替代路径。若该结果能够被复现并进一步扩展，可能会同时影响神经科学与人工智能架构的研究思路。 作者明确提醒：自组织现象并不能证明大脑真的采用这一机制。此外仍存在开放问题，包括学习基元在不同初始连接条件下的稳定性，以及该方法能否从已展示的分类任务扩展到更广泛的任务。其研究动机是探索生物合理性，而非宣称可在大规模模型中取代反向传播。

reddit · r/MachineLearning · /u/Dorian182 · 10月15日 10:01

**背景**: 反向传播是大多数深度学习的核心算法，但人们普遍认为它缺乏生物合理性：它需要权重对称、全局计算的误差信号，以及分离的前向与后向训练阶段。相比之下，局部可塑性规则仅利用突触本身可获得的信号来更新连接强度，这更接近生物神经元的工作方式。自组装神经网络则是指能够自行构建计算图的架构，而非依赖人工设计的固定拓扑；这篇论文把两种思路结合起来，让局部规则去组织学习回路本身。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/pdf/2406.16062">Towards Biologically Plausible Computing</a></li>
<li><a href="https://arxiv.org/abs/2010.08262">[2010.08262] Local plasticity rules can learn deep ...</a></li>
<li><a href="https://arxiv.org/pdf/2406.09787">Evolving Self - Assembling Neural Networks : From Spontaneous...</a></li>

</ul>
</details>

**标签**: `#neural-networks`, `#self-organization`, `#learning-rules`, `#biological-plausibility`, `#backpropagation`

---

<a id="item-8"></a>
## [苹果首款折叠屏手机 Duo 入选《时代》2026 年度最佳发明](https://time.com/collection/best-inventions/2026/apple-iphone-duo/) ⭐️ 8.0/10

《时代》周刊将苹果首款折叠屏手机 Duo 列入 2026 年度最佳发明榜单。该机起售价 1999 美元，展开后可当作大屏平板使用，被认为是 iPhone 自 2007 年问世以来最大的一次设计变革。 Duo 意味着苹果终于进入已由三星、华为等厂商耕耘多年的折叠屏赛道，而《时代》的认可也说明这一形态在高端市场获得了主流背书。对供应链、开发者和消费者换机周期都会产生影响。 1999 美元的起售价使 Duo 高于市面上大多数折叠屏机型，也高于现有 iPhone Pro 系列。发布会上，9 月 1 日刚接替 Tim Cook 的新任 CEO John Ternus 负责展示该机，他在与网红 IShowSpeed 互动时手抖，事后解释是熬夜和过于兴奋所致。

telegram · zaihuapd · 10月16日 03:00

**背景**: 折叠屏手机通过铰链连接柔性屏幕，合上时可当普通手机使用，展开后则变成更大的平板；三星、华为等厂商已推出此类产品多年，而苹果此前一直未涉足该品类。《时代》年度最佳发明是一份由编辑部评选的产品与创意榜单，入选更多意味着曝光度和声誉，并非独立的技术评测。CEO 交接同样值得关注：Tim Cook 自 2011 年起执掌苹果，是历次 iPhone 发布的标志性人物，由 Ternus 发布 Duo 意味着苹果产品发布会进入新阶段。

**标签**: `#Apple`, `#foldable phone`, `#iPhone Duo`, `#Time Best Inventions`, `#consumer tech`

---