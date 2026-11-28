---
layout: default
title: "Horizon Summary: 2026-11-28 (ZH)"
date: 2026-11-28
lang: zh
---

> 从 29 条内容中筛选出 8 条重要资讯。

---

1. [Linux 内核 NFS 服务器曝 9.8 分漏洞，可免登录获取 root](#item-1) ⭐️ 9.0/10
2. [Unkernel 将真实 Linux 内核编译为 WebAssembly，直接在浏览器中运行](#item-2) ⭐️ 8.0/10
3. [多州总检察长起诉 SpaceX，要求阻止 Grok 生成儿童性虐待材料与报复性色情内容](#item-3) ⭐️ 8.0/10
4. [虚假的计算机验证证明](#item-4) ⭐️ 8.0/10
5. [SemiAnalysis 解析 AWS Trainium3 推理、微架构及对比 GB300 的 TCO](#item-5) ⭐️ 8.0/10
6. [中情局等多家美国情报机构遭 Artex AI 辅助黑客攻击](#item-6) ⭐️ 8.0/10
7. [Minecraft Java 版曝未修复 minecraft2shell 远程代码执行漏洞，可通过恶意字体触发](#item-7) ⭐️ 8.0/10
8. [澳大利亚联邦法院裁定苹果须于 2027 年前向第三方应用商店开放 iPhone](#item-8) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Linux 内核 NFS 服务器曝 9.8 分漏洞，可免登录获取 root](https://opensec.in/blog/nfs2root-cve-2026-99362) ⭐️ 9.0/10

OpenSec 披露了 CVE-2026-99362，这是 Linux 内核 NFS 服务器（nfsd）中的一个 CVSS 9.8 分预认证堆溢出漏洞，未认证攻击者只需向 tcp/2049 发送一条连接即可越界写入内核堆并获得 root。该漏洞自 2014 年的 Linux 3.16 起存在，影响运行 NFSv4.1 或 4.2 的主机，修复已在 6.12.117、6.18.61、7.3.2 和 7.4-rc1 内核中发布，CVE 于 2026 年 11 月 20 日公开。 该漏洞攻击面极易触达且无需任何凭据，因此任何对外或对内网暴露的 NFS 文件服务器、NAS 设备和集群存储节点都面临风险，而漏洞长达十余年的存在时间意味着受影响的已部署内核数量极其庞大。这种级别的预认证远程内核沦陷属于最严重的 Linux 安全事件类别，会迫使存储基础设施进行紧急的升级与重启。 利用该漏洞仅需向启用了 NFSv4.1 或 4.2 的主机的 tcp/2049 发起一条连接，修复必须升级内核并重启，没有运行时热修复方案。无法立即打补丁的组织应作为临时缓解措施在防火墙上封禁 tcp/2049，或将 NFS 访问限制在可信网络内。

telegram · zaihuapd · 11月27日 12:57

**背景**: NFS（网络文件系统）是 Unix/Linux 世界长期使用的网络文件共享协议，在 Linux 上服务端由名为 nfsd 的内核组件实现，直接在核心地址空间内处理 NFS 请求。NFSv4.1 和 4.2 是协议的较新版本，引入了会话（session）与并行访问等特性，其会话处理代码路径在任何用户认证发生之前即可被触达。由于 nfsd 以内核权限运行，其中的内存破坏漏洞可绕过所有用户态沙箱，通常会导致攻击者完全掌控主机的 root 权限。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://opensec.in/blog/nfs2root-cve-2026-99362">NFS2ROOT (CVE-2026-99362): pre-auth root in Linux nfsd | OpenSec</a></li>
<li><a href="https://man7.org/linux/man-pages/man8/nfsd.8.html">nfsd (8) - Linux manual page</a></li>
<li><a href="https://datazone.de/en/aktuelles/nfs-ganesha-vs-kernel-nfsd-truenas/">NFS Ganesha vs. Kernel NFSd : What Makes Sense in... | DATAZONE</a></li>

</ul>
</details>

**标签**: `#security`, `#linux-kernel`, `#nfs`, `#vulnerability-disclosure`, `#remote-exploit`

---

<a id="item-2"></a>
## [Unkernel 将真实 Linux 内核编译为 WebAssembly，直接在浏览器中运行](https://unkernel.dev/) ⭐️ 8.0/10

Unkernel 是一个开源项目（pithings/unkernel），它把一个真正的 Linux 7.x 内核编译成单个 WebAssembly 模块，可在浏览器中不到一秒就启动到 shell。其系统调用层、调度器、内存管理、ext4 文件系统和 TCP/IP 协议栈都是被编译出来的代码而非模拟实现，项目同时提供 npx 运行方式和 JavaScript SDK。 如果一个完整的 Linux 内核可以被编译成 Wasm 并在浏览器标签页里运行，浏览器就成为一个无需启动虚拟机或容器即可承载遗留 Linux 二进制的可信沙箱。这对客户端沙箱隔离、长尾软件的可移植执行以及轻量级边缘/无服务器运行时都有直接影响。 据项目文档说明，Unkernel 只模拟用户态程序，内核本身以编译后的 Wasm 形式运行并带有真实的 MMU，这正是它与 QEMU 式全系统模拟器的区别所在。在 Hacker News 讨论中，有用户报告同时运行 4 个 md5sum 的挂钟时间与单进程相同，但在 Unkernel 里安装 Chromium 并尝试嵌套运行另一个 Unkernel 则未能成功。

hackernews · nreece · 11月28日 03:19 · [社区讨论](https://news.ycombinator.com/item?id=50674218)

**背景**: WebAssembly（Wasm）是一种可移植的底层字节码格式，最初是为了让代码能在浏览器中安全地以接近原生的速度运行，如今也越来越多地被用作浏览器之外的沙箱执行目标。Linux 内核是操作系统的核心，负责系统调用、调度、内存、文件系统和网络，通常通过 MMU（内存管理单元）直接与硬件交互。传统的浏览器中运行 Linux 的演示依赖 QEMU 之类的模拟器，需要解释或翻译内核与用户程序的每一条指令；Unkernel 则把内核预先编译成 Wasm，只模拟用户进程，用通用性换取速度和更小的体积。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/pithings/unkernel">GitHub - pithings/unkernel: A real Linux kernel, compiled to ...</a></li>
<li><a href="https://jamilxt.com/blog/linux-compiled-to-webassembly-unkernel-explained">Linux Compiled to WebAssembly: How unkernel Works and How to ...</a></li>
<li><a href="https://unkernel.dev/">unkernel</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上的反响热烈且充满动手探索：评论者互相引出了 tabc、tabernetes、sidebyside 等相关浏览器原生项目，还有人指出 Gary Bernhardt 在 2014 年的演讲《The Birth and Death of JavaScript》基本上已经预言了这一天的到来。另一些人贡献了实测结果，包括四路 md5sum 并发测试、在 Chromium 中嵌套运行 Unkernel 的失败尝试，以及“无需开虚拟机即可跑小型后端脚本”的具体用例。

**标签**: `#webassembly`, `#linux-kernel`, `#virtualization`, `#browser-runtime`, `#systems-research`

---

<a id="item-3"></a>
## [多州总检察长起诉 SpaceX，要求阻止 Grok 生成儿童性虐待材料与报复性色情内容](https://www.oag.state.va.us/media-center/news-releases/jay-jones/3162-attorneys-general-jones-and-rayfield-file-suit-against-spacex-parent-company-of-x-xai-and-grok-over-creation-and-promotion-of-child-exploitation-and-non-consensual-images-on-platform) ⭐️ 8.0/10

包括弗吉尼亚州总检察长 Jay Jones 与 Rayfield 在内的多州总检察长联盟对 SpaceX 提起诉讼，指控其旗下 X、xAI 与 Grok 的聊天机器人 Grok 生成并传播儿童性虐待材料（CSAM）以及未经同意的私密影像。诉讼要求该公司停止产生此类内容，这也是首批直接针对生成式模型输出、而非仅针对提出请求的用户的重要法律行动之一。 这是人工智能安全与监管领域的重要里程碑，因为它检验了模型提供方（而不仅仅是单个用户）是否要为有害生成内容承担法律责任。裁决结果可能影响美国所有面向消费者的聊天机器人厂商如何设计内容过滤与审核机制，并引发更广泛的宪法争论：AI 生成的性相关图像是否属于受保护的言论。 该诉讼专门针对 Grok——这款模型以相对宽松、带有“叛逆”风格的定位作为卖点；起诉书同时涉及儿童性虐待材料与未经同意的私密影像，而后者在法律上性质不同，因为它必然涉及真实人物。与多数内容护栏系统一样，过滤机制可能通过提示词操控被绕过，因此核心事实争点在于：Grok 的安全防护是根本缺失，还是仅被用户“越狱”绕过。

hackernews · DeepLogin · 11月27日 19:42 · [社区讨论](https://news.ycombinator.com/item?id=50670855)

**背景**: Grok 是埃隆·马斯克的 xAI 于 2023 年 11 月推出的一系列大语言模型，已与 X 社交平台整合，并提供 iOS 与 Android 应用。它从一开始就被定位为比竞争对手过滤更少的替代品，xAI 称其具有“叛逆气质”，可以给出直接、不加过滤的回答。“护栏”（guardrails）是位于用户与模型之间的校验与控制层，用于筛查提示词与输出是否符合政策；与训练阶段内嵌进模型的“对齐”不同，护栏运行在应用层，可以被配置，理论上也可以被绕过。州总检察长是本州最高执法官员，经常就跨州消费者保护与公共安全诉讼开展协作。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Grok_(chatbot)">Grok (chatbot) - Wikipedia</a></li>
<li><a href="https://www.coursera.org/articles/what-is-grok">What is Grok? Understanding the AI Chatbot from xAI - Coursera</a></li>
<li><a href="https://fastrouter.ai/feeds/blog/guardrails-generative-ai">What Are AI Guardrails ? A Complete Guide</a></li>

</ul>
</details>

**社区讨论**: 评论者意见分歧：一方要求追究提出生成请求的用户责任，另一方则质疑 Grok 的过滤为何失效得如此彻底——有读者追问该模型是对所有人都如此宽松，还是需要刻意“诱导”才能生成。最具实质性的讨论涉及美国宪法第一修正案，有评论者认为最高法院已有判例，只要不涉及真实儿童，为个人使用而用 AI 生成 CSAM 属于受保护言论；同时指出报复性色情在法律上不同，因为它必然指向真实人物。

**标签**: `#ai-safety`, `#regulation`, `#legal`, `#generative-ai`, `#content-moderation`

---

<a id="item-4"></a>
## [虚假的计算机验证证明](https://cr.yp.to/proofs/falseccp.html) ⭐️ 8.0/10

Dan Bernstein 在其页面中论证：由于证明检验器存在可靠性（soundness）缺陷，经计算机验证的证明也可能是假的。这引发了 Hacker News 上专家的讨论，话题涉及多重验证器架构，以及现实风险与理论差距之间的对比。

hackernews · _tk_ · 11月27日 15:26 · [社区讨论](https://news.ycombinator.com/item?id=50667989)

**标签**: `#formal-verification`, `#proof-assistants`, `#Lean`, `#Metamath`, `#software-security`

---

<a id="item-5"></a>
## [SemiAnalysis 解析 AWS Trainium3 推理、微架构及对比 GB300 的 TCO](https://newsletter.semianalysis.com/p/trainium3-inferencex) ⭐️ 8.0/10

SemiAnalysis 发布了对 AWS Trainium3 推理性能和微架构的深度分析，称其相较 NVIDIA GB300 具有更优的性能 TCO，并在 UBenchX 基准中展示了高 MFU、高 MBU 和低延迟表现。该分析还给出了基于第一性原理的物理架构评估。 若这些 TCO 结论成立，Trainium3 可能改变云上 AI 推理的经济性，并加剧 AWS 自研芯片与 NVIDIA 加速器之间的竞争。这将影响选择推理平台的云客户以及研究 AI 加速器架构的学者。 这些结论基于 SemiAnalysis 的 UBenchX 基准和第一性原理架构分析，因此性能 TCO 结果会受具体负载、软件栈成熟度和部署可用性影响。读者应将其视为特定工作负载下的比较，而非普适结论。

rss · Semianalysis · 11月27日 15:54

**背景**: AWS Trainium 是亚马逊的自研 AI 加速器系列，Trainium3 在 re:Invent 2025 上发布，Trn3 UltraServer 可扩展至 144 个设备，提供约 360+ PF8 算力和超过 20 TB 的 HBM3e。NVIDIA GB300 NVL72 是机架级液冷系统，集成 72 个 Blackwell Ultra GPU 和 36 个 Grace CPU。UBenchX 是 SemiAnalysis 推出的持续开源 AI 加速器系统基准，用于跨平台对比。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.linkedin.com/posts/faikconference_awsreinvent2025-trainium3-trn3ultraservers-activity-7453021991508398080-AM92">AWS Trainium 3 UltraServers for Large Scale AI Training and Inference</a></li>
<li><a href="https://www.nvidia.com/en-us/data-center/gb300-nvl72/">Designed for AI Reasoning Performance & Efficiency - NVIDIA</a></li>
<li><a href="https://inferencex.semianalysis.com/">AI Accelerator System Benchmark | AcceleratorX by SemiAnalysis</a></li>

</ul>
</details>

**标签**: `#AWS Trainium3`, `#AI accelerators`, `#inference`, `#microarchitecture`, `#performance TCO`

---

<a id="item-6"></a>
## [中情局等多家美国情报机构遭 Artex AI 辅助黑客攻击](https://www.forbes.com/sites/the-wiretap/2026/11/25/us-government-under-ai-cyberattack) ⭐️ 8.0/10

据《纽约时报》报道（福布斯转述），黑客借助一款名为 Artex 的开源 AI 工具攻击了多家美国情报机构，包括中央情报局（CIA）、国家地理空间情报局（NGA）和国家情报总监办公室（ODNI）。此次攻击看起来严重程度有限，受影响的只是非机密的侦察数据，而非机密系统。 这是首批被公开报道的、针对美国情报目标使用自主式进攻性 AI 框架的案例之一，说明自主 AI 攻击工具已从理论演示走向针对高价值政府网络的真实行动。由于这类框架可以免费下载并搭配低成本模型使用，它们大幅降低了网络间谍活动的技术与资源门槛，从根本上改变了网络攻击的经济学。 Artex 是一个开源框架，可调度多个开源 AI 模型来探测网络与计算机防御，实质上把侦察和渗透测试流程自动化。一名中国开发者今年早些时候发布了它，在它被关联到多起攻击（包括针对欧盟的一起）之后，该开发者已将其从自己的 GitHub 账号删除；而 FBI 今年早些时候就已警告称，网络罪犯和间谍正在广泛使用 Artex。

telegram · zaihuapd · 11月27日 10:42

**背景**: Artex 属于研究者所称的“自主式进攻框架”（AOF）：它不再由人手动操作扫描与利用工具，而是由大语言模型自行规划步骤并调用现成的安全工具。该项目自称是面向授权安全测试的“自主渗透测试控制台”，但一旦被滥用，同样的能力可以作用于任何目标。受影响的三家机构——CIA、负责从卫星影像生成地理空间情报的 NGA，以及协调 18 个情报机构的情报总监办公室 ODNI——都是美国情报体系的核心部门，因此即便是一次局限于非机密数据的入侵也格外引人关注。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.microsoft.com/en-us/security/blog/2026/11/25/what-defenders-need-to-know-artex-agentic-ai-framework-threat-actors-abuse/">What defenders need to know about ARTEX, the agentic AI ...</a></li>
<li><a href="https://cloudsecurityalliance.org/artifacts/aof">The Third Wave: ARTEX and Agentic Offensive Frameworks | CSA</a></li>
<li><a href="https://www.wiz.io/blog/agentic-attacks-artex-offensive-ai-frameworks">Agentic Attacks in the Wild: ARTEX & Offensive AI Frameworks ...</a></li>

</ul>
</details>

**标签**: `#AI security`, `#cybersecurity`, `#nation-state hacking`, `#offensive AI`, `#government intelligence`

---

<a id="item-7"></a>
## [Minecraft Java 版曝未修复 minecraft2shell 远程代码执行漏洞，可通过恶意字体触发](https://t.me/zaihuapd/45413) ⭐️ 8.0/10

11 月 22 日公开的名为 minecraft2shell 的漏洞显示，服务器资源包中特制的 TrueType 字体可以触发 FreeType 2.14.3 及更早版本中的原生越界写，从而在 Windows 平台的 Minecraft Java 版客户端上执行任意代码。1.20.5 至 1.21.10 的所有版本以及 26.1 至 26.4 快照均受影响，而 1.20.4 及更早版本与基岩版不受影响。 这是全球装机量最大的游戏客户端之一中存在的高危且目前尚无补丁的远程代码执行漏洞，利用方式仅仅是加入一个不受信任的多人服务器。由于资源包会被自动下载并应用，玩家可能在毫无明显警示的情况下被入侵，这对服务器管理员和 Mojang 都构成了紧迫压力。 Mojang 目前仍在使用 LWJGL 的 FreeType 绑定 3.4.3 版本，其中打包了存在漏洞的原生 FreeType 代码，官方补丁尚未发布。该利用链专门针对 Windows 客户端，且受影响版本范围异常广泛，因为这条存在漏洞的字体加载路径自 1.20.5 起就一直存在。

telegram · zaihuapd · 11月27日 18:04

**背景**: Minecraft 服务器可以向任何连接的客户端推送资源包，而资源包中可以包含 TrueType 格式的自定义字体。为了渲染这些字体，Minecraft 通过 LWJGL 的 Java 绑定调用 FreeType 库，而 FreeType 在 Java 沙箱之外以原生代码解析字体文件的二进制结构。解析过程中出现的越界写可以让攻击者破坏游戏进程的内存并劫持执行流，其思路与 2021 年 Log4Shell 把日志库缺陷变成 Minecraft 远程代码执行的情况类似。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.lwjgl.org/browse/release/3.4.3/bin/lwjgl-freetype">/release/3.4.3/bin/lwjgl-freetype - LWJGL</a></li>
<li><a href="https://mvnrepository.com/artifact/org.lwjgl/lwjgl-freetype/3.4.3">LWJGL FreeType Bindings » 3.4.3 - Maven Repository: org.lwjgl</a></li>

</ul>
</details>

**标签**: `#security`, `#vulnerability`, `#remote-code-execution`, `#minecraft`, `#freetype`

---

<a id="item-8"></a>
## [澳大利亚联邦法院裁定苹果须于 2027 年前向第三方应用商店开放 iPhone](https://t.me/zaihuapd/45419) ⭐️ 8.0/10

澳大利亚联邦法院裁定，苹果须自 2027 年 3 月 1 日起允许澳区 iPhone 用户通过第三方应用商店以及直接从网站安装应用，同时须开放替代支付方式和应用内外部支付链接。Fortnite 将立即重返澳区 App Store，苹果则表示将提起上诉并申请暂缓执行。 这使澳大利亚成为继欧盟依据《数字市场法》之后，第二个强制苹果拆解其高度受控的 iOS 应用分发与应用内支付垄断的主要司法辖区。该裁决可能成为先例，推动其他国家的监管机构和法院提出类似要求，直接影响苹果利润丰厚的服务业务收入，并为开发者提供新的分发与变现渠道。 法院认定苹果在 iOS 应用分发与支付市场拥有实质性市场力量，其限制行为实质性削弱了竞争，违反了澳大利亚竞争法，该裁决源于 Epic Games 提起的反垄断诉讼。值得注意的是，相关义务要到 2027 年 3 月 1 日才生效，而苹果计划的上诉与暂缓执行申请可能推迟或改变最终结果。

telegram · zaihuapd · 11月28日 07:00

**背景**: 长期以来，苹果要求所有 iOS 应用必须通过其自家的 App Store 分发，数字商品必须使用其应用内支付系统购买，并从中抽取最高 30% 的佣金。欧盟《数字市场法》迫使苹果从 2024 年起在欧盟允许替代应用市场和替代支付方式，由此催生了 AltStore PAL 等第三方商店。自 2020 年因 Fortnite 被下架而与苹果产生争端以来，Epic Games 已在多个国家对苹果的 App Store 做法提起诉讼。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.theverge.com/24100464/altstore-pal-dma-eu-launch-delta-nintendo-emulator-clip-clipboard-manager">Third - party iPhone app store AltStore PAL is now live in... | The Verge</a></li>
<li><a href="https://developer.apple.com/support/payment-options-on-the-app-store-in-the-eu/">Payment options on the App Store in the EU... - Apple Developer</a></li>
<li><a href="https://en.wikipedia.org/wiki/App_Store_(Apple)">App Store (Apple) - Wikipedia</a></li>

</ul>
</details>

**标签**: `#Apple`, `#antitrust`, `#app stores`, `#regulation`, `#Epic Games`

---