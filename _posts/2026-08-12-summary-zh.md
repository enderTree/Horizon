---
layout: default
title: "Horizon Summary: 2026-08-12 (ZH)"
date: 2026-08-12
lang: zh
---

> 从 38 条内容中筛选出 12 条重要资讯。

---

1. [新研究展示从专有 LLM API 窃取隐藏思维链的攻击](#item-1) ⭐️ 9.0/10
2. [压缩即预测：数据压缩与机器学习的内在联系](#item-2) ⭐️ 8.0/10
3. [英伟达发布 Nemotron 3.5 Lightning 与 NeMo Switchyard](#item-3) ⭐️ 8.0/10
4. [Rob Pike：Go 是 AI 辅助软件工程的理想语言](#item-4) ⭐️ 8.0/10
5. [英伟达 CUDA 护城河面临需求疑虑与开源挑战](#item-5) ⭐️ 8.0/10
6. [伦敦地铁扩大人脸扫描试点](#item-6) ⭐️ 8.0/10
7. [解耦下降：通过 AMP Onsager 修正实现训练-测试误差的精确追踪](#item-7) ⭐️ 8.0/10
8. [良性长上下文可被动解除小型 LLM 的 RLHF 拒答对齐](#item-8) ⭐️ 8.0/10
9. [石墨烯软镜片有望实现紧凑型变焦光学](#item-9) ⭐️ 8.0/10
10. [Cloudflare 报告 DDoS 攻击激增，超 1 Tbps 攻击环比增 519%](#item-10) ⭐️ 8.0/10
11. [英伟达被曝研发 Nemotron 4 开源模型，最大版本超 1 万亿参数](#item-11) ⭐️ 8.0/10
12. [LTX 发布开源视频模型 LTX-2.5，单张 RTX 5090 即可运行](#item-12) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [新研究展示从专有 LLM API 窃取隐藏思维链的攻击](https://stolen-thoughts.com/) ⭐️ 9.0/10

研究人员展示了一种实用攻击方法，可从 OpenAI、Anthropic 和 Google 等专有 LLM API 中恢复隐藏的思维链推理，尽管这些 API 设有防护。该攻击结合了轨迹重放（将加密的推理轨迹输入较弱的同系列模型）与基于工具的攻击来绕过保护措施。 这一发现意义重大，因为它破坏了前沿模型提供商赖以保密的推理过程隐私防护。它可能助长模型蒸馏、商业情报收集和更有效的越狱攻击，影响安全研究人员、AI 供应商以及使用 LLM API 的企业。 该论文对加密推理轨迹进行了表征，并表明来自同一提供商的兼容解码器模型可以跨多种模型、提供商和轨迹格式恢复隐藏推理。在第一方攻击者场景中，攻击者查询一个有能力且受保护的目标模型以生成加密轨迹，然后将这些轨迹重放到一个较弱的同系列模型中，从而恢复思维链。

hackernews · quantumgarbage · 8月11日 13:22 · [社区讨论](https://news.ycombinator.com/item?id=49257876)

**背景**: 思维链提示通过让模型生成中间推理步骤来提升大语言模型的推理能力。为了保护专有推理过程，OpenAI、Anthropic 和 Google 等公司向用户隐藏这些步骤，并以加密的 base64 编码信封形式传输，在后续调用中传回以维持多轮上下文。这项研究利用了一个事实：加密轨迹必须在某个时刻能够被解码，因此一旦存在兼容的解码器，就容易受到重放攻击。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/pdf/2608.09867">Stealing Reasoning Traces from Proprietary LLM APIs</a></li>
<li><a href="https://cybersecuritynews.com/top-ai-models-apis-flaw-exposes-hidden-reasoning/">OpenAI, Anthropic, and Google LLM APIs vulnerability Exposes...</a></li>
<li><a href="https://www.alphaxiv.org/abs/2608.09867">Stealing Reasoning Traces from Proprietary LLM APIs | alphaXiv</a></li>

</ul>
</details>

**社区讨论**: 评论者争论这是否真的算“窃取”，认为付费用户已经为 token 付费，却被拒绝访问推理过程。一些人分享了相关技巧，例如禁用思考模式并提供一个“deep_think”工具，还有人指出，一个简单的开发者提示词就让 Codex 以明文形式输出了加密的压缩数据。还有人表示对跨模型重放感到好奇，并猜测这可能是被故意允许的。

**标签**: `#security`, `#LLM`, `#privacy`, `#chain-of-thought`, `#jailbreak`

---

<a id="item-2"></a>
## [压缩即预测：数据压缩与机器学习的内在联系](https://ngrok.com/blog/compression-is-prediction) ⭐️ 8.0/10

博客文章《压缩即预测》提出，数据压缩与预测在本质上是同一个问题，二者可以相互转化。这一观点将大型语言模型等人工智能系统视为对数据压缩表示进行预测的引擎。 这一观点将信息论与现代机器学习联系起来，表明压缩基准可以成为衡量智能和预测能力的替代指标。它可能改变研究人员评估和设计 AI 模型（包括大型语言模型）的方式，使压缩成为核心目标。 该论点基于柯尔莫哥洛夫复杂性和最小描述长度（MDL）原则等概念，即生成数据的最短程序被视为最佳模型。社区评论引用了支持的资料，包括 Grant Sanderson 的《压缩即智能》视频和 MacKay 的教科书，表明这一思想在信息论中有深厚根基。

hackernews · nikolay · 8月11日 19:49 · [社区讨论](https://news.ycombinator.com/item?id=49263497)

**背景**: 柯尔莫哥洛夫复杂度衡量生成给定对象所需的最短计算机程序的长度，反映对象固有的信息内容。最小描述长度原则将此思想应用于模型选择：最有效的压缩模型即为最佳模型。由于好的压缩器隐式捕获数据的统计规律，因此可用于预测，反之亦然。这种等价性自控制论早期就已被认识，至今仍是算法信息论和基于压缩的序列预测等领域的指导原则。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Kolmogorov_complexity">Kolmogorov complexity</a></li>
<li><a href="https://en.wikipedia.org/wiki/Minimum_Description_Length_Principle">Minimum Description Length Principle</a></li>
<li><a href="https://www.academia.edu/21919272/Compression_based_methods_for_nonparametric_on_line_prediction_regression_classification_and_density_estimation_of_time_series">(PDF) Compression based methods for nonparametric on-line...</a></li>

</ul>
</details>

**社区讨论**: 评论者大多认同这一论点，并指出已有的相关工作，如 Grant Sanderson 的视频《压缩即智能》和剑桥大学的信息论课程。还有人分享自己的项目，如用于选举 NLP 的二元推理词典，展示了该思想的实际应用。总体而言，讨论建设性强，围绕文章核心主张展开延伸而非质疑。

**标签**: `#compression`, `#prediction`, `#information theory`, `#machine learning`, `#LLMs`

---

<a id="item-3"></a>
## [英伟达发布 Nemotron 3.5 Lightning 与 NeMo Switchyard](https://blogs.nvidia.com/blog/nemotron-lightning-switchyard-rtx-dgx/) ⭐️ 8.0/10

英伟达发布了 Nemotron 3.5 Lightning 系列，这是一个开放的 30B Mixture-of-Experts 模型，仅有 3B 活跃参数；同时开源了 NeMo Switchyard，一个基于 Rust 的 LLM 请求路由库。该模型声称相比同类模型，输出速度提升最高 4 倍，Agent 任务完成速度提升 30%。 这件事的意义在于，它把开放、高效的小型模型和智能路由推向 Agentic AI 的核心，有望降低高并发 Agent 工作负载的成本和延迟。部署在 RTX 和 DGX 上的开发者现在可以对紧凑的 MoE 模型进行后训练，并将工作流中的每一步路由到最合适的模型。 Nemotron 3.5 Lightning-30B-A3B-NVFP4 检查点已在 Hugging Face 上发布，可商用，并随附多种投机解码方法以加速生成。NeMo Switchyard 是一个用于 LLM 流量的 Rust 代理/库，可根据任务需求自动将提示词路由到最强大且最高效的模型。

hackernews · droidjj · 8月11日 19:35 · [社区讨论](https://news.ycombinator.com/item?id=49263340)

**背景**: Mixture-of-Experts 模型虽然总参数量很大，但每个 token 只激活其中一小部分参数，因此在高并发服务中速度快且效率高。NeMo Switchyard 这类模型路由技术针对的现实是：没有单一模型适合 Agent 工作流的每一步。Agentic AI 通常需要串联多次 LLM 调用，因此路由和小型专用模型可以在保持准确率的同时降低基础设施成本。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://blogs.nvidia.com/blog/nemotron-lightning-switchyard-rtx-dgx/">NVIDIA Nemotron 3.5 Lightning and NeMo Switchyard Deliver Faster, Smarter, More Efficient Agentic AI | NVIDIA Blog</a></li>
<li><a href="https://developer.nvidia.com/blog/nvidia-nemotron-3-5-lightning-delivers-fast-accurate-specialized-task-execution-for-long-running-agents/">NVIDIA Nemotron 3.5 Lightning Delivers Fast, Accurate Specialized Task Execution for Long-Running Agents | NVIDIA Technical Blog</a></li>
<li><a href="https://github.com/NVIDIA-NeMo/Switchyard">GitHub - NVIDIA-NeMo/Switchyard · GitHub</a></li>

</ul>
</details>

**社区讨论**: 评论者总体上欢迎这种效率导向的进展，但也提出了实际担忧：一位开发者发现 Nemotron 3.5 Lightning 和 Qwen 35B 等 MoE 模型在编码 Agent 任务上表现不佳，而同等规模的稠密模型表现更好。还有人询问路由如何处理提示词缓存和会话固定问题，也有评论批评所附基准图中省略了 Qwen 模型，只包含一个跨量级的变体。

**标签**: `#NVIDIA`, `#LLM`, `#Mixture-of-Experts`, `#Model Routing`, `#AI Infrastructure`

---

<a id="item-4"></a>
## [Rob Pike：Go 是 AI 辅助软件工程的理想语言](https://developers.googleblog.com/why-go-is-an-ideal-language-for-ai-assisted-software-engineering/) ⭐️ 8.0/10

Go 语言创造者之一 Rob Pike 在 Google Developers Blog 发文，认为 Go 的简洁性、工具链和静态类型使其特别适合 AI 辅助软件工程。这篇文章引发了大量讨论，共收到 324 条评论。 这一论点很重要，因为团队在选择语言时越来越看重 AI 编程助手在该语言中生成和维护代码的能力。该文引发的争论表明语言社区存在分歧：Netflix 的支持者报告 AI 能生成更好的 Go 代码，而 Rust 拥护者则认为更严格的编译器更有利于大语言模型（LLM）。 这篇文章发布在 Google 官方开发者博客上，标题为《Why Go is an ideal language for AI-assisted software engineering》。评论中，Netflix 的 Go 语言团队负责人证实越来越多人报告 AI 代理能写出更好的 Go 代码；但也有开发者反驳称，Go 缺乏抽象能力且并发问题较多，让 LLM 生成的代码存在风险。

hackernews · 0xedb · 8月11日 16:57 · [社区讨论](https://news.ycombinator.com/item?id=49261133)

**背景**: AI 辅助软件工程是指利用大语言模型来编写或补全源代码，语言的设计会显著影响生成代码的可靠性。Go 以语法简洁、内置 gofmt 格式化工具和强大的标准工具链著称，这可能让人类和 AI 都更容易预测和验证代码。整个行业正在积极讨论在 AI 驱动的工作流中哪种语言最具生产力，Rust 和 Go 是两种常见的候选。

**社区讨论**: 评论观点分歧明显。Netflix 的 Go 语言团队负责人表示文章与他们的内部数据一致；一位偏爱 Rust 的评论者则认为，严格挑剔的编译器能在编译期暴露错误，更适合 LLM 工作流。另一位质疑者警告说，LLM 可能更快地生成有 bug 的并发 Go 代码，对于缺乏资深审查者的团队来说风险很高。

**标签**: `#Go`, `#AI-assisted software engineering`, `#programming languages`, `#large language models`, `#developer tools`

---

<a id="item-5"></a>
## [英伟达 CUDA 护城河面临需求疑虑与开源挑战](https://stratechery.com/2026/nvidias-risky-business/) ⭐️ 8.0/10

该文深入分析英伟达的战略弱点，认为其 CUDA 软件生态的统治地位脆弱，市场对 AI 计算需求的预测可能被高估。文章指出，关于需求增长的第二层假设有可能落空，这是英伟达面临的主要风险。 英伟达的股价和市场地位取决于 AI 计算需求的持续增长以及 CUDA 生态的锁定效应。若开源替代方案出现或需求增长放缓，这家半导体巨头的估值和生态优势可能大幅缩水，并影响整个 AI 供应链。 该分析来自 Stratechery 的 Ben Thompson，聚焦 CUDA 编程模型——虽然优化能力强大，但使用体验被指极为痛苦。社区讨论还提到谷歌、AMD 可能推动开源 CUDA 替代方案，或通过“曼哈顿计划”式的集中攻关来打破英伟达的垄断。

hackernews · jonbaer · 8月11日 10:02 · [社区讨论](https://news.ycombinator.com/item?id=49255710)

**背景**: CUDA（统一计算设备架构）是英伟达专有的通用 GPU 计算平台，开发者可借其使用 C++、Python 及 PyTorch 等框架进行 AI 计算。CUDA 已深度嵌入机器学习研究与生产流程，为英伟达硬件销售构筑了强大护城河。但该平台复杂度高、厂商锁定严重，长期受到批评，业内对开源替代方案的兴趣正日益增加。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://koder.ai/blog/nvidia-accelerated-computing-gpus-cuda-ai-infrastructure">NVIDIA ’s Accelerated Computing Stack: GPUs, CUDA , AI ... | Koder. ai</a></li>
<li><a href="https://www.modular.com/blog/democratizing-ai-compute-part-4-cuda-is-the-incumbent-but-is-it-any-good">CUDA is the incumbent, but is it any good? (Democratizing AI ...)</a></li>

</ul>
</details>

**社区讨论**: 评论者大多认同英伟达的优势在于软件生态的根深蒂固，而非单纯硬件性能，但对其护城河的持久性存在分歧。有人指出 CUDA C/C++开发者体验糟糕，并预测大客户或云巨头可能资助开源替代方案。也有人提醒，算力的一阶需求确实存在，但二阶增长预期很可能被夸大。

**标签**: `#nvidia`, `#cuda`, `#ai-chips`, `#semiconductors`, `#market-analysis`

---

<a id="item-6"></a>
## [伦敦地铁扩大人脸扫描试点](https://www.btp.police.uk/news/btp/news/england/btp-expands-live-facial-recognition-lfr-trial-into-london-underground-stations/) ⭐️ 8.0/10

英国交通警察局已将实时人脸识别（LFR）试点扩展到伦敦地铁车站，摄像头现在会实时扫描乘客面部。此次扩展延续了警方此前利用实时面部比对观察名单的试点。 这将生物识别监控引入全球最繁忙的交通系统之一，影响每天数百万通勤者。它引发了严重的隐私和公民自由问题，并可能为英国公共场所的日常面部监控开创先例。 该试点采用实时人脸识别（LFR）技术，将实时闭路电视画面与警方观察名单进行比对。批评者认为，此类试点没有明确的失败条件，因为监控基础设施一旦部署就可能长期存在。

hackernews · BlueBerry2001 · 8月11日 09:40 · [社区讨论](https://news.ycombinator.com/item?id=49255496)

**背景**: 实时人脸识别（LFR）是一种生物识别监控技术，可扫描人群中的面部并与数据库（通常是通缉犯数据库）进行比对。警方称它有助于逮捕逃犯，而公民自由组织则警告该技术不准确、有偏见且侵犯隐私。伦敦地铁是城市公共交通的核心，每天运送数百万人，因此即使是试点部署也具有重大影响。

**社区讨论**: 评论几乎全部持批评态度。有人指出，非接触式银行卡成为主要进站方式后，地铁上的匿名出行早已名存实亡；有人称英国是“原始奥威尔式社会”，并质疑什么样的结果才算是试点失败。还有人将这种监控与中国情况进行不利对比，表示伦敦只有监控没有安全，而重罪犯入狱六个月就被释放。

**标签**: `#facial-recognition`, `#surveillance`, `#privacy`, `#civil-liberties`, `#London-Underground`

---

<a id="item-7"></a>
## [解耦下降：通过 AMP Onsager 修正实现训练-测试误差的精确追踪](https://www.reddit.com/r/MachineLearning/comments/1vlu1se/decoupled_descent_enforcing_exact_traintest_error/) ⭐️ 8.0/10

该论文提出了一种名为“解耦下降”（Decoupled Descent, DD）的训练算法，通过应用近似消息传递（AMP）的 Onsager 修正来强制执行训练-测试一致性，确保训练误差在每个参数迭代处渐近等于测试误差。论文将泛化差距视为数据复用偏差的后果，并在高斯混合模型上演示了该方法。 这一工作意义重大，因为它为深度学习中长期存在的泛化差距问题提供了一种有理论依据的解决思路——即训练误差下降而测试误差停滞甚至上升的问题。通过验证训练-测试误差的追踪，它有望让模型选择、最优停止和超参数调优更加可靠。 该方法是在简化高斯混合模型和全批量梯度下降设定下提出的，利用高维统计中 AMP 的 Onsager 修正来解耦误差。这是一篇理论论文，尚未扩展到非常大的模型，但作者计划发布一个兼容 PyTorch 的实现。

reddit · r/MachineLearning · /u/mlovik1 · 8月11日 21:06

**背景**: 在监督学习中，泛化差距指的是训练误差与测试误差之间的差异；当模型记住训练数据而非学习可泛化的模式时，这种差距往往会出现。近似消息传递（AMP）是一种来自压缩感知和高维统计的迭代算法，其 Onsager 修正会在迭代间减去自干扰项，使得误差可以像每一步独立一样被追踪。解耦下降借鉴了这一思想，构造出一种训练过程，使训练误差在每一步都能被证明地与测试误差相关联。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/html/2604.27883v1">Decoupled Descent: Exact Test Error Tracking Via Approximate Message Passing</a></li>
<li><a href="https://arxiv.org/abs/1607.05966">[1607.05966] Onsager-corrected deep learning for sparse linear inverse problems</a></li>
<li><a href="https://krzakala.github.io/cargese.io/AMP_Tutorial_18.pdf">Approximate Message Passing Tutorial</a></li>

</ul>
</details>

**标签**: `#machine learning`, `#optimization`, `#generalization`, `#approximate message passing`, `#theory`

---

<a id="item-8"></a>
## [良性长上下文可被动解除小型 LLM 的 RLHF 拒答对齐](https://www.reddit.com/r/MachineLearning/comments/1vm16hs/contextinduced_activation_drift_long_benign/) ⭐️ 8.0/10

研究人员发现，向谷歌的 gemma-3-1b-it 输入一段较长、良性且语义连贯的前缀（100–3000 个 token），会在深层网络引发显著的激活漂移，从而在没有任何对抗性提示或越狱指令的情况下解除 RLHF 拒答行为。打乱文本顺序的消融实验证实，该效应由语义驱动，而非序列长度或 RoPE 位置噪声所致。 该发现挑战了“RLHF 对齐是模型稳健且不变属性”的普遍假设，表明即使是良性上下文也能被动地改变安全行为。这对大模型安全评估、对齐鲁棒性以及针对非预期类越狱状态的安全防护设计具有重要意义。 研究追踪了“额外语义注意力”（ΔA_sem）、潜向量 L2 偏移（在第 22 层（约 85%网络深度）Δh_2≈3434）、logit 散度（D_KL≈22.87 nats）以及首个生成 token 的熵激增（最高达 325 倍）。打乱顺序的消融在保持序列长度、词汇和 token 频率不变的前提下破坏了语义连贯性，并未重现该漂移，从而将语义确定为驱动因素。

reddit · r/MachineLearning · /u/PresentSituation8736 · 8月12日 02:09

**背景**: RLHF（基于人类反馈的强化学习）是将大语言模型与人类偏好对齐的标准方法，通常让模型学会拒绝有害请求。激活漂移指模型内部表征发生的渐进式或由上下文引起的改变。RoPE（旋转位置编码）用于在 Transformer 中编码词序，而作者通过打乱文本的消融实验排除了这一解释。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Reinforcement_learning_from_human_feedback">Reinforcement learning from human feedback - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Representational_drift">Representational drift - Wikipedia</a></li>
<li><a href="https://1y33.github.io/blog/rope/">1y33.github.io/blog/ rope</a></li>

</ul>
</details>

**标签**: `#mechanistic interpretability`, `#RLHF alignment`, `#LLM safety`, `#activation drift`, `#language models`

---

<a id="item-9"></a>
## [石墨烯软镜片有望实现紧凑型变焦光学](https://www.qmul.ac.uk/news/latest-news/2026/science-and-engineering/se/new-graphene-powered-soft-lens-could-pave-the-way-for-smarter-glasses-cameras-and-medical-devices.html) ⭐️ 8.0/10

伦敦玛丽女王大学的研究人员开发出一种基于还原氧化石墨烯电极的透明软性镜片，可通过电场改变焦距。该原型研究成果已发表在《Advanced Functional Materials》期刊上。 该技术有望取代自动对焦相机、可穿戴显示器、VR/AR 头显及微型医疗成像设备中笨重的机械部件。它代表着向具有广泛消费和医疗应用的紧凑型变焦透镜迈进了一步。 该原型将超薄透明石墨烯电极直接集成到镜片下方的驱动层上，解决了传统电极因不透明而只能置于镜片边缘的设计瓶颈。目前仍需进一步优化电极的透明度与性能。

telegram · zaihuapd · 8月11日 12:27

**背景**: 该镜片基于介电弹性体致动器，这是一类在施加电场时发生形变的电活性聚合物，可将电能转化为机械功。这类致动器常用于软体机器人和人工肌肉研究。还原氧化石墨烯是石墨烯的一种商业化形态，可大规模生产，并可用作此类器件中的透明电极。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://techxplore.com/news/2026-08-graphene-powered-soft-lens-pave.html">Graphene-powered soft lens could pave the way for smarter glasses...</a></li>
<li><a href="https://en.wikipedia.org/wiki/Dielectric_elastomer_actuator">Dielectric elastomer actuator</a></li>

</ul>
</details>

**标签**: `#graphene`, `#optics`, `#adaptive lens`, `#materials science`, `#medical devices`

---

<a id="item-10"></a>
## [Cloudflare 报告 DDoS 攻击激增，超 1 Tbps 攻击环比增 519%](https://blog.cloudflare.com/ddos-threat-report-2026-h1/) ⭐️ 8.0/10

Cloudflare 的 2026 上半年 DDoS 威胁报告显示，其缓解了 935 起超过 1 Tbps 的网络层攻击，第二季度环比增长 519%。DNS Flood 攻击环比激增 580%，成为当季第三大攻击类型。 超大规模攻击和 DNS Flood 的快速增长表明基础设施层面的威胁正在升级，迫使各机构加强网络防御。媒体、出版和政府等行业越来越成为攻击目标，这些数据对安全规划至关重要。 第二季度超过 1 Tbps 的攻击增至 805 起，是第一季度的六倍多；上半年 DNS 类攻击占网络层攻击的 34.3%。媒体、出版与制作行业两个季度均为受攻击最多行业，政府行业从第 29 位升至第 9 位。

telegram · zaihuapd · 8月11日 13:20

**背景**: DNS Flood 是一种利用海量查询请求淹没 DNS 服务器、扰乱域名解析的 DDoS 攻击。网络层（第 3 层）DDoS 攻击通过向路由器、防火墙等设备发送大量数据包来耗尽网络基础设施资源，而 HTTP Flood 则针对应用层（第 7 层）发起攻击。理解这些概念有助于解读报告中统计数据的具体含义。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.cloudflare.com/learning/ddos/dns-flood-ddos-attack/">DNS flood DDoS attack | Learning Center</a></li>
<li><a href="https://www.fastly.com/learning/security/the-different-types-of-ddos-attacks">The Different Types of DDoS Attacks | Fastly</a></li>
<li><a href="https://en.wikipedia.org/wiki/DNS_Flood">DNS Flood - Wikipedia</a></li>

</ul>
</details>

**标签**: `#DDoS`, `#Cloudflare`, `#Network Security`, `#Cybersecurity`, `#Attack Trends`

---

<a id="item-11"></a>
## [英伟达被曝研发 Nemotron 4 开源模型，最大版本超 1 万亿参数](https://economictimes.indiatimes.com/tech/artificial-intelligence/nvidia-is-developing-nemotron-4-open-source-models-the-information/articleshow/133157952.cms) ⭐️ 8.0/10

据 The Information 报道，英伟达正在开发 Nemotron 4 开源模型家族，最大版本预计将有超过 1 万亿参数。报道援引多名员工称，训练最早可能在深秋完成，但目前尚未确定发布日期。 如果属实，英伟达将在开源大语言模型领域成为重要竞争者，直接对标顶级开源模型。超过 1 万亿参数的开源模型可能大幅提升推理、编程和智能体 AI 的能力，影响依赖开源替代方案的开发者和企业。 同日，英伟达还发布了面向代码审查等任务的 Nemotron 3.5 Lightning，以及用于自动分配任务的模型路由库 NeMo Switchyard。关于 1 万亿参数的消息来自泄露信息，尚未得到英伟达官方证实。

telegram · zaihuapd · 8月12日 01:15

**背景**: Nemotron 是英伟达开发的一系列 AI 模型，包括大语言模型和多模态模型，英伟达已开源了部分模型的权重、训练数据和训练方法。2024 年 6 月，英伟达发布了 Nemotron-4 340B 模型家族，并提供宽松的开源许可。目前开源社区中参数超过 1 万亿的模型非常少见，一旦推出将成为一个重要里程碑。NeMo Switchyard 是一个模型路由库，可根据任务需求在不同模型间分配 AI 智能体工作负载，降低成本并提升效率。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Nemotron">Nemotron</a></li>
<li><a href="https://research.nvidia.com/publication/2024-06_nemotron-4-340b">Nemotron-4 340B | Research</a></li>
<li><a href="https://developer.nvidia.com/blog/route-ai-agent-workloads-across-models-with-nvidia-nemo-switchyard/">Route AI Agents Across Models with NVIDIA NeMo Switchyard</a></li>

</ul>
</details>

**标签**: `#NVIDIA`, `#LLM`, `#Open Source`, `#AI`, `#Nemotron`

---

<a id="item-12"></a>
## [LTX 发布开源视频模型 LTX-2.5，单张 RTX 5090 即可运行](https://ltx.io/model/ltx-2-5) ⭐️ 8.0/10

LTX 发布了开源视频生成基础模型 LTX-2.5，公开了全部权重、训练代码和推理管线。该模型可在单张 RTX 5090 上本地运行，支持文生视频与图生视频。 此举意义重大，因为将具有竞争力的视频模型完整开源，大幅降低了研究人员和小型团队的使用门槛。同时表明高质量视频生成可在消费级硬件上运行，有望加速 AI 视频领域的创新。 该模型改进了多镜头连贯性和提示词遵循，采用新的扩散视频解码器和 Gemma 4 12B 文本编码器。在 98 个提示词的文生视频瑕疵评测中，LTX 2.5 Pro 在十款模型中排名第一；年收入低于 1000 万美元的公司可免费商用。

telegram · zaihuapd · 8月12日 02:15

**背景**: 视频生成模型通常需要强大的云端算力且常常闭源。LTX-2.5 顺应了开源权重、可本地运行的模型趋势，其扩散解码器本身是一个小型扩散模型，在潜变量条件下对像素进行去噪，而 Gemma 4 12B 则是现代开源文本编码器。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://ltx.io/model/ltx-2-5">LTX - 2 . 5 : LTX's Latest AI Open-Source Foundation Model | LTX</a></li>
<li><a href="https://github.com/huggingface/diffusers/blob/main/src/diffusers/pipelines/ltx2/pipeline_ltx2_diffusion_decode.py">diffusers/src/diffusers/pipelines/ltx2/pipeline_ltx2_ diffusion _ decode .py...</a></li>
<li><a href="https://blog.google/innovation-and-ai/technology/developers-tools/introducing-gemma-4-12b/">Introducing Gemma 4 12 B</a></li>

</ul>
</details>

**标签**: `#video-generation`, `#open-source`, `#AI`, `#text-to-video`, `#model-release`

---