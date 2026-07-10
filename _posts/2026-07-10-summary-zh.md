---
layout: default
title: "Horizon Summary: 2026-07-10 (ZH)"
date: 2026-07-10
lang: zh
---

> 从 38 条内容中筛选出 12 条重要资讯。

---

1. [欧盟议会通过程序手段延长聊天控制 1.0](#item-1) ⭐️ 9.0/10
2. [OpenAI 发布 GPT-5.6，三个尺寸版本，ARC-AGI-3 取得 SOTA](#item-2) ⭐️ 9.0/10
3. [蚂蚁灵波开源全球首个 MoE 具身视频基模 LingBot-Video](#item-3) ⭐️ 9.0/10
4. [Mitchell Hashimoto 谈用 Zig 构建 Ghostty 终端](#item-4) ⭐️ 8.0/10
5. [用 Rust 重写的 PostgreSQL 通过全部回归测试](#item-5) ⭐️ 8.0/10
6. [Meta 发布 Muse Spark 1.1，首个付费 AI 模型](#item-6) ⭐️ 8.0/10
7. [Talos-XII：用 Rust 手写的自动微分加强化学习栈处理抽卡概率](#item-7) ⭐️ 8.0/10
8. [IMGNet：用符号模式替代余弦相似度的人脸验证模型](#item-8) ⭐️ 8.0/10
9. [大疆 EV50 垂直起降无人机飞越珠峰 8861 米](#item-9) ⭐️ 8.0/10
10. [国家超算互联网核心节点在郑州上线](#item-10) ⭐️ 8.0/10
11. [OpenAI 与美国国防部禁止 AI 监控公民](#item-11) ⭐️ 8.0/10
12. [中国法院判定游戏账号可继承，平台禁令无效](#item-12) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [欧盟议会通过程序手段延长聊天控制 1.0](https://www.patrick-breyer.de/en/eu-parliament-greenlights-chat-control-1-0-breyer-our-children-lose-out/) ⭐️ 9.0/10

欧盟议会于 2026 年 7 月 9 日批准延长聊天控制 1.0，允许美国科技公司在无授权情况下自愿扫描私人消息以查找儿童性虐待材料，直至 2028 年。尽管投票议员多数反对，该法案仍通过。 这一决定为欧盟的大规模监控和数字隐私开创了令人担忧的先例，可能削弱端到端加密，并允许在 Instagram、Discord 和 Gmail 等平台上进行无授权检查私人通信。 该延期得以通过是因为否决动议未能获得所需的 361 票绝对多数；314 名议员投票反对，276 人赞成，17 人弃权，113 人缺席。程序操作包括在暑假前举行投票，并且要求绝对多数才能阻止默认通过。

hackernews · rapnie · 7月9日 11:03 · [社区讨论](https://news.ycombinator.com/item?id=48843923)

**背景**: 聊天控制（正式名称为《预防和打击儿童性虐待条例》）由欧盟委员伊尔瓦·约翰松于 2022 年 5 月首次提出。聊天控制 1.0 是 2021 年引入的临时措施，允许自愿扫描私人消息以查找已知儿童色情内容。批评者认为它强制实施大规模监控，侵犯隐私权，并且无法可靠检测未知虐待材料。本次延期复活了已失效的措施，直至 2028 年。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Chat_Control_1.0">Chat Control 1.0</a></li>
<li><a href="https://www.techtimes.com/articles/320010/20260709/eu-parliament-passes-chat-control-default-314-meps-couldnt-block-scanning-law.htm">EU Parliament Passes Chat Control by Default: 314 MEPs Couldn't Block ...</a></li>
<li><a href="https://www.wired.com/story/a-majority-of-european-lawmakers-voted-against-letting-big-tech-read-our-messages-theyre-going-to-anyway/">A Majority of European Lawmakers Voted Against Letting Big ...</a></li>

</ul>
</details>

**社区讨论**: 评论者表达了强烈愤怒，称议会程序操作反民主且威胁隐私。多人指出，在暑假前举行投票并要求绝对多数反对才能阻止，实际上迫使法案通过，尽管多数议员反对。一位评论者警告欧盟正在走向极权。

**标签**: `#privacy`, `#surveillance`, `#EU law`, `#chat control`, `#digital rights`

---

<a id="item-2"></a>
## [OpenAI 发布 GPT-5.6，三个尺寸版本，ARC-AGI-3 取得 SOTA](https://openai.com/index/gpt-5-6/) ⭐️ 9.0/10

OpenAI 发布了其最新旗舰模型 GPT-5.6，包含三个尺寸（Luna、Terra、Sol），其中最大的 Sol 版本在 ARC-AGI-3 交互推理基准测试中以 7.8%的得分取得新的最先进成绩。 这标志着 AI 智能体推理领域的重要里程碑，GPT-5.6 Sol 是首个在 ARC-AGI-3 游戏中取得胜利的已验证前沿模型，展示了向通用流体智能的进步。此外，模型增强的意图理解和图像细节保留能力也提升了用户交互质量。 该模型分为三个层级：Luna（最小）、Terra（中等）和 Sol（最大）。Sol 在最大推理努力下在 ARC-AGI-3 上获得 7.8%的得分，该结果已由 ARC Prize Foundation 验证。GPT-5.6 还保留了原始图像尺寸，并能更好推断用户意图，无需显式的逐步指令。

hackernews · logickkk1 · 7月9日 17:04 · [社区讨论](https://news.ycombinator.com/item?id=48849066)

**背景**: ARC-AGI-3 是一个用于评估智能体智能的交互式基准测试，通过新颖的抽象回合制环境要求智能体自主探索、推断目标并进行规划，且没有显式指令。它基于之前的 ARC 基准测试，但引入了部分可观测性和动态反馈，使其成为 AI 模型面临的严峻挑战。此前的前沿模型在 ARC-AGI-3 上的得分低于 1%，因此 GPT-5.6 的 7.8%代表了有意义的进步。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arcprize.org/arc-agi/3">ARC-AGI-3</a></li>
<li><a href="https://arxiv.org/abs/2603.24621">ARC-AGI-3: A New Challenge for Frontier Agentic Intelligence ARC-AGI-3: A New Challenge for Frontier Agentic Intelligence ARC-AGI-3 Quickstart - ARC-AGI-3 Docs ARC-AGI-3: The New Interactive Reasoning Benchmark - DataCamp GPT 5.6 Sol Tops ARC-AGI 3 With 7.8%, Becomes First Model To ... ARC-AGI-3: Interactive AGI Benchmark - emergentmind.com</a></li>

</ul>
</details>

**社区讨论**: 社区评论既兴奋又质疑。用户指出 GPT-5.6 Sol 在 ARC-AGI-3 上取得了新的 SOTA，但也提到 OpenAI 在生物学基准测试中省略了与 Fable 5 的对比，因为 Fable 5 拒绝回答大多数问题。一些用户比较了编码性能，发现 GPT-5.6 与 GPT-5.5 相似，并在某项测试中落后于 Sonnet 5。总体而言，讨论反映了对技术对比和基准含义的高度参与。

**标签**: `#AI`, `#OpenAI`, `#GPT-5.6`, `#Language Models`, `#ARC-AGI`

---

<a id="item-3"></a>
## [蚂蚁灵波开源全球首个 MoE 具身视频基模 LingBot-Video](https://www.qbitai.com/2026/07/446458.html) ⭐️ 9.0/10

蚂蚁灵波开源了全球首个基于 MoE 架构的具身智能视频生成基础模型 LingBot-Video。该模型在机器人视频评测基准 RBench 上获得 0.620 分，超越了 Wan2.6、Seedance1.5 Pro 和 Cosmos3 Super 等现有模型。 这标志着具身 AI 领域的重大突破，将 MoE 效率与视频生成相结合，可实现更快、更可扩展的机器人技能学习。在 Apache 2.0 许可下开源将加速机器人仿真、动作预测和世界模型等方向的研究。 LingBot-Video 总参数为 300 亿，但每次推理仅激活约 30 亿参数，推理效率约为同等规模稠密架构的三倍。它采用 DiT+MoE 设计，在 7 万小时具身数据上训练，并引入多维强化学习奖励，重点关注物理合理性和任务完成度。

telegram · zaihuapd · 7月9日 04:30

**背景**: MoE（混合专家）架构将神经网络划分为多个专用子网络（专家），每次只激活部分专家以提高效率。Diffusion Transformer（DiT）用 Transformer 主干替代传统扩散模型中的 U-Net，实现可扩展的视频生成。RBench 是专门评估面向机器人视频生成的新基准，涵盖操作、移动等任务。LingBot-Video 结合这些技术，生成物理一致且任务感知的视频，连接仿真与现实机器人学习。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Mixture_of_experts">Mixture of experts - Wikipedia</a></li>
<li><a href="https://encord.com/blog/diffusion-models-with-transformers/">Diffusion Transformer (DiT) Models: A Beginner’s Guide</a></li>
<li><a href="https://arxiv.org/html/2601.15282v1">Rethinking Video Generation Model for the Embodied World - arXiv</a></li>

</ul>
</details>

**标签**: `#MoE`, `#具身智能`, `#视频生成`, `#开源`, `#机器人`

---

<a id="item-4"></a>
## [Mitchell Hashimoto 谈用 Zig 构建 Ghostty 终端](https://alexalejandre.com/programming/interview-with-mitchell-hashimoto/) ⭐️ 8.0/10

Vagrant 创始人 Mitchell Hashimoto 在一场深度访谈中分享了使用 Zig 语言构建 Ghostty 终端模拟器的经历，涉及技术决策、文化氛围和权衡取舍。 此次访谈罕见地揭示了一个知名项目在语言选择上的考量，引发了对 Zig 与 Rust 在系统编程中比较的讨论。Hashimoto 的务实观点会影响开发者在性能关键型应用中的语言选型。 Ghostty 是一个快速、跨平台的终端模拟器，使用原生界面和 GPU 加速。Hashimoto 讨论了为何偏爱 Zig 而非 Rust，指出了文化差异以及功能缺失与简洁性之间的权衡。

hackernews · veqq · 7月9日 17:17 · [社区讨论](https://news.ycombinator.com/item?id=48849292)

**背景**: Ghostty 是一款以高性能和原生外观著称的终端模拟器，于 2024 年底发布。Zig 是一种底层系统编程语言，旨在成为 C 语言的现代替代品，具备编译时元编程和手动内存管理。访谈将 Zig 的极简主义与 Rust 的安全性进行了对比，反映了系统编程社区中持续的争论。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://ghostty.org/">Ghostty</a></li>
<li><a href="https://en.wikipedia.org/wiki/Zig_(programming_language)">Zig (programming language)</a></li>

</ul>
</details>

**社区讨论**: 访谈评论呈现不同观点：有人赞同 Hashimoto 对 Rust 文化的批评，也有人为 Rust 辩护并指出 Zig 功能缺失。有用户注意到语言偏好争论的讽刺性，强调根据项目需求做出务实选择的重要性。

**标签**: `#Zig`, `#Ghostty`, `#Rust`, `#terminal emulator`, `#software engineering`

---

<a id="item-5"></a>
## [用 Rust 重写的 PostgreSQL 通过全部回归测试](https://github.com/malisper/pgrust) ⭐️ 8.0/10

一个名为 pgrust 的项目使用大语言模型（LLMs）将 PostgreSQL 用 Rust 重写，现已通过所有标准 Postgres 回归测试。作者 malisper 正在尝试用 LLMs 打造一个更优版本的三十岁数据库。 该项目展示了 LLMs 辅助大规模软件重写的潜力，可能加速遗留系统的现代化。同时，它也引发了关于单人作者、AI 生成代码库的可行性和可维护性的讨论。 该仓库在一个月内产生了 7101 次提交，全部由 LLMs 生成，使得传统代码审查变得不切实际。该项目目前缺少明确的许可证变更通知，可能引发法律问题。

hackernews · SweetSoftPillow · 7月9日 06:18 · [社区讨论](https://news.ycombinator.com/item?id=48841676)

**背景**: PostgreSQL 是一个成熟的开源关系型数据库，拥有庞大的代码库和数十年的优化经验。用 Rust 重写可能提供更好的内存安全性和并发性，但需要保留数十年的错误修复和边缘情况处理。使用 LLMs 完成此类任务具有新颖性，但也引发了对代码正确性和长期维护的疑问。

**社区讨论**: 社区评论对单人作者 AI 生成的项目表示怀疑，担心可持续性、缺乏开发纪律以及贡献所需的 token 成本。一些人建议采用如镜像查询等实际测试方法来比较性能，另一些人则质疑审查如此庞大自动生成代码库的可行性。

**标签**: `#PostgreSQL`, `#Rust`, `#database`, `#LLM`, `#rewrite`

---

<a id="item-6"></a>
## [Meta 发布 Muse Spark 1.1，首个付费 AI 模型](https://ai.meta.com/blog/introducing-muse-spark-meta-model-api/) ⭐️ 8.0/10

Meta 宣布推出 Muse Spark 1.1，这是其首个商业化 agentic AI 模型，并公布了 API 定价，该模型专为编码和自主任务完成而设计。 这标志着 Meta 开始将 AI 模型商业化，直接与 OpenAI 和 Anthropic 竞争，可能使 agentic 编码对开发者更易获取且成本更低。 定价为每百万输入 token $1.25，每百万输出 token $4.5，缓存输入为$0.15；然而，评估方法因在 Terminal-Bench 2.1 测试中覆盖资源上限而受到批评。

hackernews · ot · 7月9日 14:10 · [社区讨论](https://news.ycombinator.com/item?id=48846184)

**背景**: Agentic AI 是一类使用工具和循环自主完成任务的 AI 系统，与仅生成内容的生成式 AI 不同。Muse Spark 是 Meta Muse 系列的原生多模态推理模型，支持工具使用、视觉思维链和多智能体编排。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://techcrunch.com/2026/07/09/meta-enters-the-crowded-ai-coding-battle-with-muse-spark-1-1/">Meta enters the crowded AI coding battle with Muse Spark 1 ...</a></li>
<li><a href="https://www.hostinger.com/tutorials/agentic-ai-vs-generative-ai/">Generative AI creates content, while agentic AI completes tasks.</a></li>

</ul>
</details>

**社区讨论**: 社区评论关注定价过低、因资源上限覆盖导致的评估缺陷，以及 Meta 应扮演开源搅局者还是正面竞争的战略辩论。一些用户认为该模型实用且便宜，而另一些则质疑其有效性。

**标签**: `#AI`, `#Meta`, `#Muse Spark`, `#model release`, `#agentic`

---

<a id="item-7"></a>
## [Talos-XII：用 Rust 手写的自动微分加强化学习栈处理抽卡概率](https://www.reddit.com/r/MachineLearning/comments/1urvxgb/talosxii_handwritten_autograd_small_rlmlp_stack/) ⭐️ 8.0/10

Talos-XII 是一个命令行模拟器，它完全用 Rust 手写了自动微分引擎、Dueling DQN、PPO 以及带有潜层注意力（MLA）的 Transformer 来建模《明日方舟：终末地》的抽卡系统，无需 PyTorch 或 NumPy 等外部 ML 框架。 该项目表明，Rust 中紧凑且自包含的 ML 栈可以处理特定领域的概率建模（抽卡）并具有竞争力的性能，其跨硬件基准测试的公开请求可为未来 CPU/GPU 优化的 ML 部署提供参考。 该栈包括带有梯度检查的自定义自动微分、运行时 SIMD 调度（标量/AVX2/AVX-512/NEON）、Rayon 并行化模拟、BF16 推理缓存以及用于 Python 脚本的 PyO3 桥接，所有内容通过 142 个测试和单一静态二进制文件整合在一起。

reddit · r/MachineLearning · /u/zay0kami · 7月9日 16:52

**背景**: 自动微分是一种在反向传播中自动计算梯度的技术，是神经网络训练的核心组件。Dueling DQN 是一种将状态价值和动作优势流分离的架构，提高了 Q-learning 的效率。PPO（近端策略优化）是一种流行的演员-评论家强化学习算法，通过约束策略更新来实现稳定训练。多头潜层注意力（MLA）通过低秩投影压缩键值缓存，减少内存并加速 Transformer 推理。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://medium.com/@sainijagjit/understanding-dueling-dqn-a-deep-dive-into-reinforcement-learning-575f6fe4328c">Understanding Dueling DQN: A Deep Dive into Reinforcement ...</a></li>
<li><a href="https://machinelearningmastery.com/a-gentle-introduction-to-multi-head-latent-attention-mla/">A Gentle Introduction to Multi-Head Latent Attention (MLA)</a></li>
<li><a href="https://arxiv.org/abs/2502.07864">TransMLA: Multi-Head Latent Attention Is All You Need TransMLA: Multi-head Latent Attention Is All You Need Towards Economical Inference: Enabling DeepSeek’s Multi-Head ... MHA vs MQA vs GQA vs MLA - Medium Multi-Latent Attention Transformer - emergentmind.com Multi-head Latent Attention (MLA): Making Transformers More ...</a></li>

</ul>
</details>

**标签**: `#Rust`, `#autograd`, `#reinforcement learning`, `#gacha`, `#MLP`

---

<a id="item-8"></a>
## [IMGNet：用符号模式替代余弦相似度的人脸验证模型](https://www.reddit.com/r/MachineLearning/comments/1urxvxh/i_built_imgnet_a_face_verification_model_that/) ⭐️ 8.0/10

IMGNet 提出了一种人脸验证模型，用滑动窗口符号模式匹配替代余弦相似度，在 LFW 上达到 96.27%，模型仅 10.58 MB。 这种新颖的相似度度量方法挑战了传统的人脸验证范式，有助于实现更高效、更鲁棒的轻量级模型，在保持竞争力的同时可能降低计算成本。 该模型在 CASIA-WebFace（49 万张图像）上训练，包含一个 SW Block（在质数窗口大小下计算像素差异）、一个仅依赖于符号一致性的 IMG Sign MSE 损失函数，以及一个投票系统（2/3 或 3/3 通过判定为匹配）。当直接应用于 ArcFace 嵌入而无需重新训练时，IMG Sign Score 在 LFW 上达到 99.58%，仅比 ArcFace+余弦相似度低 0.24%。

reddit · r/MachineLearning · /u/img-_- · 7月9日 18:00

**背景**: 人脸验证通常将人脸图像编码为嵌入向量，并使用余弦相似度进行比较。IMGNet 的 SW Block 用多尺度关系运算替代标准卷积，在质数窗口大小（3、5、7）下计算每个像素与其邻居的差异，然后通过一个小型 MLP 映射这些差异。损失函数纯粹基于符号模式一致性定义，消除了幅值依赖性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openaccess.thecvf.com/content_ECCV_2018/papers/Lior_Talker_Efficient_Sliding_Window_ECCV_2018_paper.pdf">Eﬃcient Sliding Window Computation for NN-Based Template Matching</a></li>
<li><a href="https://regulaforensics.com/blog/face-matching/">Face Matching in Identity Verification</a></li>
<li><a href="https://www.mdpi.com/2076-3417/15/15/8161">A Multicomponent Face Verification and Identification System</a></li>

</ul>
</details>

**社区讨论**: 在 Reddit 讨论中，作者积极参与，解释了符号模式方法背后的动机，并回答了关于训练稳定性和泛化性的问题。许多人对文化灵感以及度量-损失共同设计的潜力表示兴趣，但也有人对该方法在大规模数据集上的可扩展性以及需要更广泛验证提出了担忧。

**标签**: `#face verification`, `#representation learning`, `#similarity metrics`, `#machine learning`

---

<a id="item-9"></a>
## [大疆 EV50 垂直起降无人机飞越珠峰 8861 米](https://www.163.com/dy/article/L1CUCV940514R9OJ.html) ⭐️ 8.0/10

大疆尚未发布的 EV50 垂直起降运载无人机在“巅峰使命”珠峰科考中，于珠峰北坡飞越 8861 米高度，创下同类公开测试中的最高飞行升限纪录。 这一成就展示了 EV50 先进的垂直起降能力，凸显了其在高原物流、科学考察以及百公里级低空货物运输等场景的潜力。 在为期 12 天的任务中，EV50 累计完成 32 架次起降，连续爬升 3730 米，返程时仍剩 30%电量。该无人机采用混合 VTOL 固定翼设计，可原地垂直起降后切换为固定翼巡航。

telegram · zaihuapd · 7月9日 06:00

**背景**: VTOL（垂直起降）无人机结合了多旋翼的垂直起降能力和固定翼飞机的续航与速度优势，无需跑道即可运行，适合山地等复杂地形。在海拔 8000 米以上收集的大气剖面数据有助于科学家了解平流层状况和气候模式。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://uavcoach.com/vtol-drones/">VTOL Drones: An In-Depth Guide [New for 2026]</a></li>
<li><a href="https://zh.wikipedia.org/zh-hans/平流层">平流层 - 维基百科，自由的百科全书</a></li>

</ul>
</details>

**标签**: `#drone`, `#VTOL`, `#DJI`, `#record`, `#high-altitude`

---

<a id="item-10"></a>
## [国家超算互联网核心节点在郑州上线](https://36kr.com/newsflashes/3887797387344387) ⭐️ 8.0/10

2026 年 7 月 9 日，国家超算互联网核心节点在郑州正式上线，提供超过 10 万张国产人工智能算力卡。这是国家超算互联网平台接入的最大单体国产 AI 算力资源池。 这一里程碑显著扩大了中国的国产 AI 算力基础设施，减少对外国芯片的依赖，并支持大规模 AI 模型训练。它还推进了全国一体化算力网络的国家战略，惠及科研、产业和政府应用。 该核心节点旨在管理并调度全国计算资源，整合供需对接和产业孵化等服务。项目于 2024 年 10 月启动建设，2026 年 2 月进入试运行，随后正式上线。

telegram · zaihuapd · 7月9日 07:00

**背景**: 国家超算互联网是一个连接全国多个超算中心的平台，提供统一的高性能计算和 AI 服务。国产 AI 算力卡是由华为、寒武纪等中国企业开发的处理器，正越来越多地用于大模型训练。郑州核心节点是该网络的关键组成部分，旨在协调全国计算资源。

<details><summary>参考链接</summary>
<ul>
<li><a href="http://paper.people.com.cn/rmrb/images/2024-05/06/19/rmrb2024050619.pdf">KJZKRMRB19B20240506C</a></li>
<li><a href="https://baike.baidu.com/item/国家超算互联网核心节点/63648019">国家超算互联网核心节点_百度百科</a></li>
<li><a href="https://news.qq.com/rain/a/20260709A03VDU00">刚刚，国家超算互联网核心节点正式上线_腾讯新闻</a></li>

</ul>
</details>

**标签**: `#supercomputing`, `#AI infrastructure`, `#domestic computing`, `#China`

---

<a id="item-11"></a>
## [OpenAI 与美国国防部禁止 AI 监控公民](https://t.me/zaihuapd/42459) ⭐️ 8.0/10

OpenAI 与美国国防部（原战争部）已同意修订其 AI 合作协议，增加明确禁止使用 AI 对美国公民进行大规模监控的条款，此举由 OpenAI 首席执行官 Sam Altman 主动提出。 这为政府使用 AI 树立了重要的道德先例，回应了公众对监控和隐私的担忧。它可能影响未来 AI 公司与政府机构之间的合同，尤其是在 Anthropic 合作协议因类似争议中止之后。 修订后的条款明确禁止针对美国公民的蓄意监控，以及利用商业获取的个人身份信息进行追踪或监测。该修正合同尚未正式签署。

telegram · zaihuapd · 7月9日 13:22

**背景**: 该新闻涉及 AI 研究机构 OpenAI 与美国国防部。原合同允许将 AI 用于国防目的，但人们担心可能被滥用于国内监控。类似之前的协议，如 Anthropic 与国防部的协议，因这类道德问题而中止。

**标签**: `#AI ethics`, `#government`, `#surveillance`, `#policy`

---

<a id="item-12"></a>
## [中国法院判定游戏账号可继承，平台禁令无效](https://www.tomshardware.com/tech-industry/big-tech/chinese-courts-allow-heirs-to-inherent-accounts-of-deceased-gamers-multiple-cases-spanning-years-establish-precedent-for-digital-ownership-of-games-in-game-items-and-microtransactions) ⭐️ 8.0/10

中国法院在多起跨越数年的案件中裁定，游戏账号、装备道具、加密货币及社交媒体账号等虚拟资产属于可继承的财产，平台禁止继承的条款被认定无效。 这些判例为中国数字资产继承确立了重要的法律先例，可能影响全球平台政策和数字财产权，尤其对数以百万计的游戏玩家和数字服务用户意义重大。 法院认定用户协议中的‘禁止继承’条款因违反法定权利而无效；平台须配合继承人办理资产转移，并可收取合理费用，但聊天记录等纯个人隐私内容不在继承范围内。

telegram · zaihuapd · 7月10日 02:56

**背景**: 数字继承是指个人去世后数字资产所有权的转移。在许多国家，游戏账号等虚拟财产的法律地位尚不明确，平台条款通常禁止转让。这些中国判例明确了虚拟资产具有财产属性并且可以继承，为科技法律树立了先例。

**标签**: `#digital inheritance`, `#virtual property`, `#Chinese law`, `#gaming`, `#legal precedent`

---