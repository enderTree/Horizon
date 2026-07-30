---
layout: default
title: "Horizon Summary: 2026-07-30 (ZH)"
date: 2026-07-30
lang: zh
---

> 从 40 条内容中筛选出 13 条重要资讯。

---

1. [AI 蠕虫通过 Word 中的 Copilot 传播](#item-1) ⭐️ 9.0/10
2. [俄罗斯指控 Telegram 创始人杜罗夫协助恐怖活动，发出国际通缉](#item-2) ⭐️ 9.0/10
3. [顶级 AI 初创公司减少研究发表，引发透明度担忧](#item-3) ⭐️ 8.0/10
4. [Vision Pro 用于沉浸式房屋设计漫游](#item-4) ⭐️ 8.0/10
5. [开源引擎在 M 系列 Mac 上用 2GB 内存运行 Gemma 4 26B](#item-5) ⭐️ 8.0/10
6. [Mitchell Hashimoto 创立 Superlogical，基于 libghostty 构建终端应用](#item-6) ⭐️ 8.0/10
7. [KOReader：为电子墨水屏设备打造的开源阅读器](#item-7) ⭐️ 8.0/10
8. [长政策文件无法可靠约束 LLM 代理](#item-8) ⭐️ 8.0/10
9. [Matthew Green 谈人工智能与后量子密码分析](#item-9) ⭐️ 8.0/10
10. [PostSlate 使用 ncnn Vulkan 实现跨厂商的边缘机器学习推理](#item-10) ⭐️ 8.0/10
11. [月之暗面新一轮融资估值达 300 亿美元](#item-11) ⭐️ 8.0/10
12. [OpenAI 向 10 万学者免费提供前沿 AI 模型](#item-12) ⭐️ 8.0/10
13. [英国提议放宽苹果和谷歌应用商店支付规则](#item-13) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [AI 蠕虫通过 Word 中的 Copilot 传播](https://enklypesalt.com/posts/context-collapse-part3-ai-worming-through-word/) ⭐️ 9.0/10

研究人员展示了一种通过 Microsoft Word 的 Copilot 自我传播的文档型 AI 蠕虫，它利用隐藏的恶意提示欺骗 AI 修改文档并将攻击传播到新文件中。 此漏洞使 AI 蠕虫能够在无需攻击者进一步干预的情况下通过常规文档工作流程传播，可能导致使用 Copilot 的企业环境中发生大规模数据泄露和恶意软件传播。 该攻击利用了当前 AI 模型中指令与数据之间根本缺乏分离的缺陷，并且可以通过白色文本或 Unicode 技巧等手法嵌入隐藏提示，使得检测变得困难。

hackernews · Canopy9560 · 7月29日 11:44 · [社区讨论](https://news.ycombinator.com/item?id=49096188)

**背景**: 提示注入是一类攻击，将恶意指令隐藏在数据（如文档）中，诱使 AI 模型做出意外行为。AI 蠕虫是一种自我复制的提示注入，能从一款应用传播到另一款。在此例中，Word 的 Copilot 处理文档并遵循嵌入的指令，无意中传播了蠕虫。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.linkedin.com/pulse/ai-worms-your-word-docs-free-code-review-beats-paid-tools-andy-arnott-61iec">AI Worms in Your Word Docs + Free Code Review That ... - LinkedIn</a></li>
<li><a href="https://zeli.app/en/story/49096188">Document-Borne AI Worms Self-Propagate Through Copilot for ...</a></li>

</ul>
</details>

**社区讨论**: 评论者担忧，在 AI 系统停止混合指令与数据之前，这一漏洞根本不可修复。一些人预测情况在改善前会变得更糟，并举出例子如 GitHub 评论中的隐藏提示可能窃取数据或通过账户传播。其他人指出，诸如白色文本之类的简单技术仍然可以用来隐藏提示。

**标签**: `#AI security`, `#prompt injection`, `#Copilot vulnerabilities`, `#AI worms`, `#data security`

---

<a id="item-2"></a>
## [俄罗斯指控 Telegram 创始人杜罗夫协助恐怖活动，发出国际通缉](https://www.interfax.ru/russia/1106228) ⭐️ 9.0/10

7 月 29 日，俄罗斯联邦安全局对 Telegram 创始人帕维尔·杜罗夫提起刑事指控，依据《刑法》第 205.1 条第 1.1 款（协助恐怖活动），并将其列入国际通缉名单。 这一升级标志着主要平台创始人与国家之间重大的法律对抗，可能影响 Telegram 的全球运营、言论自由规范以及在地缘政治紧张局势下对加密通信平台的治理。 FSB 指控 Telegram 管理层拒绝删除被乌克兰情报机构及恐怖组织用于在俄罗斯境内协调破坏活动、恐怖袭击和网络诈骗的频道、群组和机器人，造成人员伤亡和数十亿卢布损失。

telegram · zaihuapd · 7月29日 05:56

**背景**: Telegram 由帕维尔·杜罗夫于 2013 年创立，是一款广泛使用的加密通讯应用，尤其在俄罗斯和乌克兰受欢迎。杜罗夫是俄罗斯出生的企业家，此前曾在法国因内容审核问题面临法律挑战。FSB 的指控涉及 Telegram 在删除极端主义内容方面的立场，这一直是该平台与俄罗斯当局之间的争议点。

**标签**: `#Telegram`, `#Pavel Durov`, `#Russia`, `#terrorism charges`, `#international warrant`

---

<a id="item-3"></a>
## [顶级 AI 初创公司减少研究发表，引发透明度担忧](https://www.science.org/content/article/ai-s-top-startups-are-barely-publishing-their-research) ⭐️ 8.0/10

《科学》杂志的一篇文章揭示，知名 AI 初创公司正越来越多地选择不发表其研究成果，这与早期普遍公开出版的做法形成对比。 这一趋势威胁到 AI 领域的开放思想交流，可能减缓集体进步并阻碍可重复性，而这对于该领域的健康发展至关重要。 文章特别指出，在独角兽初创公司中，OpenAI 在累计引用量上领先，紧随其后的是 MEGVII、Hugging Face 和 Anthropic 等公司；然而，其中许多公司现在的发表量减少了。该研究使用引用量作为研究重要性的代理指标，并承认其不完美。

hackernews · YeGoblynQueenne · 7月29日 21:25 · [社区讨论](https://news.ycombinator.com/item?id=49103285)

**背景**: 过去，AI 研究主要通过学术会议和期刊广泛分享，促进了快速发展。像 DeepMind 和 OpenAI 这样的初创公司最初大量发表成果，但随着商业压力和人才竞争加剧，许多公司为了保护知识产权和保持竞争优势，退出了公开出版。

**社区讨论**: 评论者分享了个人经历：一位指出在顶级期刊发表困难，最终转向预印本；另一位明确避免发表以防止被 OpenAI 和 Anthropic 复制；还有一位批评 AI 研究的“博客化”，认为这鼓励了未经证实的说法和类似社交媒体的动态。

**标签**: `#AI`, `#startups`, `#research`, `#publications`, `#open science`

---

<a id="item-4"></a>
## [Vision Pro 用于沉浸式房屋设计漫游](https://christianselig.com/2026/07/vision-pro-house/) ⭐️ 8.0/10

Christian Selig 展示了 Apple Vision Pro 的新用途，用于实时沉浸式漫游房屋设计，让客户在施工前交互式体验空间比例和光照。 这展示了 Vision Pro 在娱乐之外的实用高价值应用，可能通过实现即时空间验证并减少施工期间的高成本变更，从而改变建筑设计工作流程。 该漫游可能使用 Apple 的 RoomPlan 和 RealityKit 创建房屋 3D 模型，并通过 visionOS 流式传输到 Vision Pro；类似工作流已在 Quest 和 HTC Vive 上存在，但 Vision Pro 提供更高分辨率和无缝透视功能。

hackernews · robbiet480 · 7月29日 20:39 · [社区讨论](https://news.ycombinator.com/item?id=49102774)

**背景**: 使用 VR 的建筑可视化已存在多年，设备如 HTC Vive 和 Meta Quest，但 Apple Vision Pro 的高分辨率显示屏和精确的手眼追踪可实现更逼真的体验。Christian Selig 以开发流行的第三方 Reddit 客户端 Apollo 而闻名。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Apple_Vision_Pro">Apple Vision Pro</a></li>
<li><a href="https://www.apple.com/apple-vision-pro/">Apple Vision Pro</a></li>
<li><a href="https://plusrender.com/virtual-reality-walkthrough-for-architecture/">Creating the Best Tour for VR Walkthrough Architecture</a></li>

</ul>
</details>

**社区讨论**: 建筑专业人士证实了其价值，一位用户指出其公司使用类似的三维优先方法搭配 Quest 3。其他人建议增加太阳角度模拟等增强功能。社区赞赏 Christian 的贡献，有人称他为杰出的开发者。

**标签**: `#Vision Pro`, `#architecture`, `#VR/AR`, `#design`, `#3D visualization`

---

<a id="item-5"></a>
## [开源引擎在 M 系列 Mac 上用 2GB 内存运行 Gemma 4 26B](https://github.com/drumih/turbo-fieldfare) ⭐️ 8.0/10

TurboFieldfare 是一个新的开源推理引擎，通过在推理过程中从 SSD 流式传输路由专家，在任何 M 系列 Mac 上仅用 2 GB 内存即可运行 4 位量化的 Gemma 4 26B-A4B-IT 模型。 这使得在内存受限的设备（如 8 GB MacBook Air）上运行 260 亿参数模型成为可能，让内存有限的用户更容易使用设备端 AI。 该引擎在 8 GB M2 MacBook Air 上达到 5-6 token/s，在 M5 MacBook Pro 上达到 31-35 token/s，使用 Swift 和 Metal，结合小型专家缓存和有界并行 pread。它还包含一个实验性的 OpenAI 兼容本地服务器，支持流式传输和工具调用。

hackernews · gitpusher42 · 7月29日 15:05 · [社区讨论](https://news.ycombinator.com/item?id=49098510)

**背景**: 像 Gemma 4 26B 这样的大语言模型需要大量内存，通常超出消费级设备的可用 RAM。4 位量化通过降低权重精度来减少内存占用，而混合专家（MoE）模型每个 token 仅激活部分参数，进一步提升效率。TurboFieldfare 通过将非活跃专家存储在 SSD 上并按需获取来扩展这一概念，这种技术称为 SSD 流式推理。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://alain-airom.medium.com/run-big-llms-on-small-gpus-a-hands-on-guide-to-4-bit-quantization-and-qlora-40e9e2c95054">Run Big LLMs on Small GPUs: A Hands-On Guide to 4-bit Quantization and QLoRA | by Alain Airom (Ayrom) | Medium</a></li>
<li><a href="https://developer.nvidia.com/blog/applying-mixture-of-experts-in-llm-architectures/">Applying Mixture of Experts in LLM Architectures | NVIDIA Technical...</a></li>
<li><a href="https://www.mindstudio.ai/blog/ssd-streaming-ai-models-ram-dial">SSD Streaming for AI Models: How to Turn RAM from a Wall into a Dial | MindStudio</a></li>

</ul>
</details>

**社区讨论**: 社区成员称赞该项目的创新，有人指出传统工具如 llama.cpp 也可以 mmap 模型，但缺乏调优的同步。高 RAM Mac（64 GB）用户观察到更高速度（48 tok/s），因为页面缓存使整个专家集常驻内存。一位用户为较旧 macOS 版本提供了编译解决方法。

**标签**: `#inference engine`, `#open-source`, `#Gemma`, `#quantization`, `#Mac`

---

<a id="item-6"></a>
## [Mitchell Hashimoto 创立 Superlogical，基于 libghostty 构建终端应用](https://www.superlogical.com/) ⭐️ 8.0/10

Mitchell Hashimoto 宣布成立新公司 Superlogical，将在开源库 libghostty 之上开发终端应用，此前他已将 Ghostty 项目移交给了非营利组织。 这代表了一种新颖的开源商业模式：公司在自身创建的开源库之上构建专有产品，同时确保该库保持免费和独立。这可能会激励其他寻求可持续资金的开源项目采用类似策略。 Superlogical 将把 libghostty 作为公共基础组件，使用与任何人相同的 MIT 许可组件，并将向上游贡献共享终端工作。Ghostty 本身是一个快速、GPU 加速的终端模拟器，在 macOS 和 Linux 上具有原生 UI。

hackernews · yan · 7月29日 15:41 · [社区讨论](https://news.ycombinator.com/item?id=49098965)

**背景**: 终端模拟器是开发者必不可少的工具，提供基于文本的操作系统界面。Ghostty 由 Mitchell Hashimoto（还因 Vagrant 和 Terraform 而闻名）创建，因其性能和跨平台设计而备受关注。libghostty 是一个库，允许任何应用程序嵌入完整的终端模拟器，从而支持集成开发环境或远程管理工具等新用例。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://ghostty.org/">Ghostty</a></li>
<li><a href="https://mitchellh.com/writing/libghostty-is-coming">Libghostty Is Coming – Mitchell Hashimoto</a></li>
<li><a href="https://github.com/ghostty-org/ghostty">GitHub - ghostty -org/ ghostty : Ghostty is a fast, feature-rich, and...</a></li>

</ul>
</details>

**社区讨论**: 社区反应整体积极，用户赞扬了将 Ghostty 移交非营利组织、再在 libghostty 之上建立公司的战略举措。一些人将其与 OLE 和 COM 等老技术进行对比，另一些人则对过于简约、信息不足的公告标题表示不满。此外，还有开发者看到了将终端功能集成到其他工具中的潜力。

**标签**: `#terminal`, `#open-source`, `#Ghostty`, `#Superlogical`, `#Mitchell Hashimoto`

---

<a id="item-7"></a>
## [KOReader：为电子墨水屏设备打造的开源阅读器](https://koreader.rocks/) ⭐️ 8.0/10

KOReader 是一款面向 E Ink 设备的开源电子书阅读器和文档浏览器，支持 EPUB、PDF、MOBI 等多种文件格式，并提供丰富的自定义选项。 它使用户摆脱了专有电子阅读器生态系统的束缚，无需格式转换即可阅读无 DRM 内容，并培养了一个重视阅读自由和控制的活跃开发者与读者社区。 KOReader 可在已破解的 Kindle、Kobo 和其他 E Ink 设备上运行；其功能包括重排、文本转语音、OPDS 目录支持以及通过 Calibre 或云服务同步。但部分用户反映界面不直观且偶尔有卡顿。

hackernews · Cider9986 · 7月29日 11:05 · [社区讨论](https://news.ycombinator.com/item?id=49095865)

**背景**: E Ink 设备是采用反射式显示屏的低功耗电子阅读器，类似纸张。亚马逊 Kindle 和 Kobo 等流行型号操作系统封闭，限制文件格式支持和自定义。KOReader 是一种开源替代方案，用户在对设备越狱后安装，支持更多格式和高级功能，如手势控制和 PDF 重排。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://koreader.rocks/">KOReader</a></li>
<li><a href="https://grokipedia.com/page/KOReader">KOReader</a></li>

</ul>
</details>

**社区讨论**: 社区评论总体正面，用户赞赏 KOReader 的自由度和格式支持。但部分人指出学习曲线陡峭、手势不直观以及偶有卡顿。有用户为了通过 Readest 与 iPhone 同步而采用 KOReader，但最终放弃。

**标签**: `#open-source`, `#e-reader`, `#kindle`, `#kobo`, `#reading`

---

<a id="item-8"></a>
## [长政策文件无法可靠约束 LLM 代理](https://arxiv.org/abs/2607.25398) ⭐️ 8.0/10

一项名为'Handbook.md'的新研究表明，LLM 代理无法可靠遵守长政策文件，揭示了上下文窗口的根本限制。 这项研究挑战了大上下文模型能有效约束代理行为的假设，指出了在现实世界政策合规场景中部署 AI 代理的关键缺陷。 该研究强调，即使声称支持 100 万 token 的模型也面临上下文退化、量化问题和采样器限制，使其在长政策遵循方面不可靠。

hackernews · spIrr · 7月29日 13:01 · [社区讨论](https://news.ycombinator.com/item?id=49096969)

**背景**: LLM 代理是使用大型语言模型自主执行任务的 AI 系统，通常由政策文件指导。上下文窗口限制了模型一次能处理的文本量；更长的窗口并不能保证准确的回忆或推理，尤其是在模型被严重量化或使用不良采样方法时。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://atlan.com/know/llm-context-window-limitations/">LLM Context Window Limitations in 2026 - atlan.com</a></li>
<li><a href="https://bitfern.com/blog/context-windows/">LLM Context Windows Explained: Limits, Tokens, and Memory</a></li>
<li><a href="https://www.thinkstack.ai/blog/what-are-llm-agents/">What are LLM Agents? A Complete Guide for 2026</a></li>

</ul>
</details>

**社区讨论**: 社区评论普遍同意这一发现，指出在实践中像 Claude 这样的模型会很快忽略长指令，而短提示指导效果更好。一些人认为本地推理可以缓解这个问题，另一些人指出即使是人类也难以遵循长政策文件。

**标签**: `#LLM`, `#AI Agents`, `#Context Window`, `#Policy Compliance`, `#Benchmark`

---

<a id="item-9"></a>
## [Matthew Green 谈人工智能与后量子密码分析](https://simonwillison.net/2026/Jul/29/matthew-green/#atom-everything) ⭐️ 8.0/10

密码学家 Matthew Green 指出，当前从传统公钥算法（RSA、ECC）向抗量子算法过渡的时期，正是人工智能推动密码分析进步的绝佳时机，AI 可能要么破解所有难题，要么为新标准提供可靠信心。 这一观点非常及时，因为业界和标准机构正在积极选择和部署后量子密码标准；如果 AI 能对这些算法进行彻底测试，将极大增强信任度，或在广泛采用前揭示关键弱点。 Green 特别提到 HAWK 是 NIST 正在评估的后量子标准之一，并引用了 Impagliazzo 的 Minicrypt 世界——即公钥密码不可能但私钥密码存在的场景——作为 AI 成功破解所有难题后可能出现的情形。

rss · Simon Willison · 7月29日 18:18

**背景**: 后量子密码学是指能够抵抗经典计算机和量子计算机攻击的密码算法，因为 RSA 和 ECC 等现行方案易受 Shor 算法攻击。NIST 正在主导标准化流程以筛选和批准这些新算法。Impagliazzo 的五世界是一个概念框架，用于分类计算复杂性与密码学之间可能的关系，从 Algorithmica（P=NP）到 Cryptomania（丰富的密码原语）。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://hawk-sign.info/">Hawk</a></li>
<li><a href="https://www.nist.gov/pqc">Post-quantum cryptography | NIST</a></li>
<li><a href="https://fanpu.io/blog/2022/impagliazzos-five-worlds/">Impagliazzo ' s Five Worlds, or The Computational... | Fan Pu Zeng</a></li>

</ul>
</details>

**标签**: `#cryptography`, `#post-quantum`, `#AI`, `#cryptanalysis`, `#standards`

---

<a id="item-10"></a>
## [PostSlate 使用 ncnn Vulkan 实现跨厂商的边缘机器学习推理](https://www.reddit.com/r/MachineLearning/comments/1v9s4mz/vendoragnostic_ml_inference_on_production_edge/) ⭐️ 8.0/10

视频编辑工具 PostSlate 采用 ncnn 的 Vulkan 后端，在多种 GPU 上运行人脸检测和嵌入等机器学习模型，相比 ONNX CPU 实现了 10 倍加速，并消除了对特定厂商运行时的依赖。 这种方法使得在 NVIDIA、AMD、Intel 和 Apple Silicon 上实现高效的设备端机器学习推理成为可能，而无需用户安装 CUDA 或其他专有运行时，从而降低了边缘 AI 应用的部署门槛。 在 RTX 4070 上，ncnn Vulkan 将 ArcFace R50 人脸嵌入从 30 毫秒（ONNX CPU）降至 3 毫秒，SCRFD 人脸检测从 25 毫秒降至 2.5 毫秒，通过 fp16 权重存储使模型大小减半。

reddit · r/MachineLearning · /u/ppchaos · 7月29日 10:22

**背景**: ncnn 是由腾讯开发的高性能神经网络推理框架，针对移动和边缘平台进行了极致优化。Vulkan 是一种跨平台 GPU API，提供对图形和计算硬件的底层访问。ONNX（开放神经网络交换格式）是一种用于表示机器学习模型的开放标准，实现了不同框架之间的互操作性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/Tencent/ncnn">GitHub - Tencent/ncnn: ncnn is a high-performance neural ... Treatment by Cancer Type - NCCN Releases · Tencent/ncnn - GitHub home — ncnn documentation About Us - NCNN</a></li>
<li><a href="https://github.khronos.org/Vulkan-Site/tutorial/latest/ML_Inference/Embedded_Applications/01_introduction.html">Embedded Applications: AI at the Edge :: Vulkan Documentation Project</a></li>
<li><a href="https://en.wikipedia.org/wiki/ONNX">ONNX</a></li>

</ul>
</details>

**标签**: `#machine learning`, `#edge computing`, `#Vulkan`, `#inference`, `#onnx`

---

<a id="item-11"></a>
## [月之暗面新一轮融资估值达 300 亿美元](https://t.me/zaihuapd/42845) ⭐️ 8.0/10

中国 AI 初创公司月之暗面（Moonshot AI）正寻求至多 20 亿美元的新融资，目标估值 300 亿美元，这已是其六个月内的第三轮融资。受 Kimi 聊天机器人和大模型需求推动，该公司 4 月年度经常性收入突破 2 亿美元。 估值在六个月内从 40 亿升至 300 亿美元，反映出投资者对中国 AI 初创公司的强烈信心，尤其是那些已证明产品市场契合度的公司。月之暗面的成功标志着全球大模型领域竞争加剧，以及面向消费者的 AI 应用在中国的重要性。 该公司还在拆除境外架构以筹备香港上市，并推出了通用 AI 代理 Kimi Work。此前由美团领投的一轮融资完成后估值 200 亿美元，相比 2024 年 12 月刚过 40 亿美元的估值大幅攀升。

telegram · zaihuapd · 7月29日 10:12

**背景**: 月之暗面于 2023 年 3 月由清华大学校友杨植麟、周昕宇和吴宇欣创立，致力于推动通用人工智能发展。其旗舰产品 Kimi 是一款 AI 聊天机器人，初始版本支持高达 12.8 万 token 的上下文。该公司随后发布了开源权重的 Kimi K2 和 K3 模型，并与百度、阿里巴巴等竞争对手共同成为中国 AI 生态系统的重要参与者。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Kimi_(chatbot)">Kimi (chatbot)</a></li>
<li><a href="https://en.wikipedia.org/wiki/Moonshot_AI">Moonshot AI - Wikipedia</a></li>
<li><a href="https://www.kimi.com/products/kimi-work">Kimi Work : Next-Gen Desktop AI Agent for Knowledge Workers</a></li>

</ul>
</details>

**标签**: `#AI`, `#startup`, `#funding`, `#large language model`, `#Chinese tech`

---

<a id="item-12"></a>
## [OpenAI 向 10 万学者免费提供前沿 AI 模型](https://openai.com/index/chatgpt-for-academic-researchers/) ⭐️ 8.0/10

2026 年 7 月 29 日，OpenAI 启动了“面向学术研究者的 ChatGPT”项目，计划到 2027 年向全球多达 10 万名研究人员免费提供其前沿 GPT-5.6 系列模型，首批 1 万人现已开放申请。 该计划大幅降低了学术研究人员使用最先进 AI 的门槛，可能加速基因组学、蛋白质建模和文献综述等领域的发现。这也是 OpenAI 到 2027 年投资超过 2.5 亿美元支持外部科研承诺的一部分。 参与者可使用 GPT-5.6 模型（包括前沿的 Sol 版本）并邀请最多 4 位机构合作者，默认情况下工作区数据不用于模型训练。该项目还提供从经费申请到基因组分析等科研全流程的培训和技术支持。

telegram · zaihuapd · 7月30日 00:17

**背景**: 前沿 AI 模型（如 OpenAI 的 GPT-5.6 系列）是特定时期内最先进、能力最强的模型，它们在大量数据集上训练，能够在多种任务中提供顶尖性能。这些模型往往具有强大且不可预见的涌现能力，既带来机遇也伴随风险。在此项目之前，这类模型通常只对付费 API 用户或企业客户开放，资金有限的学术研究人员难以获得。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://kie.ai/gpt-5-6">OpenAI GPT - 5 . 6 API: Frontier Intelligence with Sol, Terra, and... | Kie.ai</a></li>
<li><a href="https://www.vellum.ai/blog/gpt-5-6-benchmarks-explained">GPT - 5 . 6 Sol vs Terra vs Luna: Which Tier Should You Actually Use?</a></li>
<li><a href="https://www.nvidia.com/en-us/glossary/frontier-models/">What Are Frontier AI Models and How They Work | NVIDIA Glossary</a></li>

</ul>
</details>

**标签**: `#OpenAI`, `#academic research`, `#AI models`, `#science funding`, `#GPT-5`

---

<a id="item-13"></a>
## [英国提议放宽苹果和谷歌应用商店支付规则](https://t.me/zaihuapd/42855) ⭐️ 8.0/10

2026 年 6 月 30 日，英国竞争与市场管理局提议允许应用开发者将用户引导至苹果和谷歌应用商店之外的替代支付选项，并考虑要求苹果开放其 NFC 技术，以便在 iOS 应用中实现非接触式支付。 该提案可能降低苹果和谷歌对应用内购买收取的佣金，从而为开发者和消费者节省成本，并促进移动应用生态系统的竞争。它也可能为其他考虑类似数字市场法规的地区树立先例。 CMA 规定，苹果或谷歌对引导用户使用外部支付所收取的任何费用必须公平合理，且低于现有的应用商店佣金。节省的费用应让消费者受益或用于创新。该提案是英国新数字市场制度下的咨询的一部分，此前苹果和谷歌去年被认定在移动生态系统中具有战略市场地位。

telegram · zaihuapd · 7月30日 02:10

**背景**: 英国的《2024 年数字市场、竞争与消费者法案》授权 CMA 对在数字活动中被认定为具有“战略市场地位”的企业进行监管。NFC（近场通信）是一种技术，允许设备在靠近时进行通信，从而实现非接触式支付。CMA 的提案旨在解决苹果和谷歌对应用商店支付和 NFC 访问的控制阻碍竞争和创新的担忧。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.gov.uk/government/news/cma-consults-on-new-requirements-for-apple-and-googles-mobile-platforms">CMA consults on new requirements for Apple and Google’s ...</a></li>
<li><a href="https://en.wikipedia.org/wiki/Digital_Markets,_Competition_and_Consumers_Act_2024">Digital Markets, Competition and Consumers Act 2024 - Wikipedia</a></li>

</ul>
</details>

**标签**: `#antitrust`, `#app store`, `#digital regulation`, `#mobile payments`, `#UK CMA`

---