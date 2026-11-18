---
layout: default
title: "Horizon Summary: 2026-11-18 (ZH)"
date: 2026-11-18
lang: zh
---

> 从 41 条内容中筛选出 8 条重要资讯。

---

1. [OpenAI 发布 GPT-6.2 Astra 与 Sol，大幅降低成本](#item-1) ⭐️ 9.0/10
2. [Java4Shell：OpenJDK 处理 Base64 数据时触发远程代码执行漏洞](#item-2) ⭐️ 8.0/10
3. [Cloudflare 称 Quad9 退出法国是 DNS 监管的警示信号](#item-3) ⭐️ 8.0/10
4. [英伟达新加坡子公司营收达 1040 亿美元，公司停止单独披露当地销售数据](#item-4) ⭐️ 8.0/10
5. [微软发布 MAI Code 2 与 Code 2 Flash 编程模型，已接入 GitHub Copilot](#item-5) ⭐️ 8.0/10
6. [SolidJS 2.0 发布：新增服务端原语与 Rust 编译器](#item-6) ⭐️ 8.0/10
7. [Datasette Lite 使用 Service Worker 与 Pyodide 重写](#item-7) ⭐️ 8.0/10
8. [美国将 AI 芯片出口管制延伸至远程访问](#item-8) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [OpenAI 发布 GPT-6.2 Astra 与 Sol，大幅降低成本](https://openai.com/index/introducing-gpt-6-2-astra-sol/) ⭐️ 9.0/10

OpenAI 推出了面向高难度专业项目的前沿模型 GPT-6.2 Astra，以及面向日常工作的轻量高效模型 GPT-6.2 Sol，二者均宣称能用更少的输出 token 取得更好结果。OpenAI 表示，在 Cognition 的 FrontierCode 2.0 上，Sol 与 Astra 的差距仅 0.5 分，成本约为后者的五分之一。 此次发布之所以重要，是因为更便宜、更快速的前沿级模型降低了运行多步骤智能体的成本，使先进 AI 在大规模企业应用中更具可行性；与此同时，办公任务表现参差不齐也说明能力短板仍然存在。这还会加剧领先模型厂商之间在性价比上的竞争。 社区测试发现，在一次数据分析考试中，Astra 的成本从 V6 的约 20 美元降至 V6.2 的约 4 美元，Sol 从 2.6 美元降至 1.2 美元，准确率相近，部分原因是 token 减少了 20% 且工具调用次数更少；不过模型有时会“提前完成”而没找到答案。早期展示的幻灯片、工作簿和备忘录等办公任务示例则因质量不佳受到尖锐批评。

hackernews · jasondavies · 11月17日 17:46 · [社区讨论](https://news.ycombinator.com/item?id=50535230)

**背景**: OpenAI 的 GPT-6.2 系列延续了一种常见做法：推出面向高难度编程、工具使用和文档生成工作的旗舰模型“Astra”，同时提供面向日常任务的更便宜模型“Sol”。这类发布通常会通过 FrontierCode 等测试编程能力的基准，以及模拟 Word、Excel、PDF、电子邮件和日历等真实办公流程的智能体基准来评估。此次宣传重点与其说在原始能力上，不如说在成本和速度上，反映出业界越来越关注让 AI 智能体能够以可负担的成本大规模运行。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openai.com/index/introducing-gpt-6-2-astra-sol/">Introducing GPT - 6 . 2 Astra and Sol | OpenAI</a></li>
<li><a href="https://openrouter.ai/openai/gpt-6.2-sol">GPT - 6 . 2 Sol - API Pricing & Benchmarks | OpenRouter</a></li>
<li><a href="https://artificialanalysis.ai/models/gpt-6-2-sol">GPT - 6 . 2 Sol Models - Intelligence, Performance... | Artificial Analysis</a></li>

</ul>
</details>

**社区讨论**: 评论者看法分化：许多人称赞成本和速度大幅改善，有人报告在准确率相近的情况下成本约降至五分之一；但也有人批评 OpenAI 展示的办公任务示例质量不佳，甚至不如前代模型。还有读者抱怨早期评论多在评价旧版 GPT 模型而非测试新模型，并有人提到系统卡中关于模型表现出“评测意识”迹象的说明。

**标签**: `#OpenAI`, `#GPT-6.2`, `#LLMs`, `#AI benchmarks`, `#cost efficiency`

---

<a id="item-2"></a>
## [Java4Shell：OpenJDK 处理 Base64 数据时触发远程代码执行漏洞](https://calif.io/java4shell/) ⭐️ 8.0/10

安全研究团队 Calif 公开了名为 Java4Shell 的漏洞细节：OpenJDK 在解析 Base64 数据的过程中可被触发远程代码执行（RCE）。该利用滥用了 HotSpot 虚拟机在运行时生成的 stub 代码，并且需要通过网络远程完成精细的堆布局塑造，作者将其称为“远程堆风水”（Remote Heap Feng Shui）。 由于 OpenJDK 是 Java SE 的官方参考实现、也是部署最广泛的 JDK，任何基于 HotSpot 的运行时（包括 Oracle JDK 与 GraalVM）只要会解码攻击者可控的 Base64 输入，就可能暴露在风险之中，涉及面覆盖大量服务端 Java 基础设施。该研究还展示了一种颇为新颖的远程堆布局控制手法，很可能影响后续的 Java 漏洞利用研究。 作者指出该攻击对 RTT、抖动等网络条件较为敏感，并且他们是通过公网 IP 在互联网上验证的，而非假设理想的实验室环境。讨论区中，Semgrep 发布了涵盖五个条件的免费检测脚本（基于 HotSpot 的 JDK 受影响，OpenJ9 与 Azul Prime/Zing 不受影响），另有评论者转述了一条未经证实的说法：该漏洞与 AVX512 版 Base64 解码实现有关，可用 -XX:UseAVX=2 参数规避。

hackernews · werrett · 11月17日 21:11 · [社区讨论](https://news.ycombinator.com/item?id=50538240)

**背景**: OpenJDK 是 Java SE 的自由开源参考实现，最初由 Sun Microsystems 启动，如今是最主流的 JDK 发行版；HotSpot 则是其中默认的虚拟机与即时编译器（JIT），会在运行时生成 stub 代码。堆风水（heap feng shui，也称 heap grooming）是漏洞利用中的经典预备步骤：攻击者以精心选择的大小进行内存分配与释放，使堆布局变得可预测，从而让后续的内存安全缺陷落在有用的目标上而不是随机崩溃。本次的新意在于，这种布局塑造完全通过针对远程目标的网络流量来完成。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/OpenJDK">OpenJDK</a></li>
<li><a href="https://en.wikipedia.org/wiki/Heap_feng_shui">Heap feng shui - Wikipedia</a></li>
<li><a href="https://stackoverflow.com/questions/16568253/difference-between-jvm-and-hotspot">java - Difference between JVM and HotSpot ? - Stack Overflow</a></li>

</ul>
</details>

**社区讨论**: 讨论整体评价非常正面：Semgrep 的 ievans 称这项工作“极其出色”，并分享了可区分 HotSpot 系 JDK 与其他实现的免费检测脚本；AgentME 则转述了推上未经证实的说法，认为漏洞与 AVX512 Base64 解码有关、或可用 -XX:UseAVX=2 规避。另有评论者转向悲观论调，警告关键基础设施可能在数月内被严重攻破，并认为积极的一面是这会迫使老旧机构加速现代化。

**标签**: `#security`, `#vulnerability`, `#OpenJDK`, `#exploitation`, `#Java`

---

<a id="item-3"></a>
## [Cloudflare 称 Quad9 退出法国是 DNS 监管的警示信号](https://blog.cloudflare.com/quad9-withdrawal-from-france/) ⭐️ 8.0/10

Cloudflare 发布分析文章，将 Quad9 因法国版权方发起的 DNS 封锁诉讼而撤出法国公共 DNS 解析服务一事，称为欧洲互联网自由的“煤矿里的金丝雀”。文章认为，法院强制中立的递归解析器执行域名封锁，开创了可能迫使包括 Cloudflare 在内的其他公共 DNS 服务商退出整个国家的先例。 如果法院可以要求中立的公共解析器执行全国性封锁名单，像 Quad9 这样的小型非营利运营者就只能在合规与退出市场之间二选一，从而压缩欧洲用户可选的注重隐私的 DNS 服务商范围。该案被普遍视为版权执法从 ISP 延伸至 DNS 层的模板，影响所有依赖第三方解析器获取隐私保护或规避审查的用户。 Quad9 选择撤走其在法国的任播节点，而不是执行被裁定的封锁名单，这意味着法国用户完全失去了一个注重隐私的解析器选项，而不仅仅是被封锁了某些域名。Cloudflare 表示自身也面临类似诉讼并正在上诉，但文章并未承诺若败诉将采取何种具体行动（例如退出法国），这一空白立刻被评论者抓住。

hackernews · subset · 11月17日 22:13 · [社区讨论](https://news.ycombinator.com/item?id=50538994)

**背景**: 公共 DNS 解析器是代表用户把域名翻译成 IP 地址的第三方服务，人们常因速度、隐私或过滤需求而弃用 ISP 的解析器，主要运营者包括 Google Public DNS、Cloudflare 以及瑞士非营利机构 Quad9。DNS 封锁名单是指解析器拒绝为其作答的域名列表，这项技术长期用于反垃圾邮件和恶意软件，如今越来越多地被用于版权执法。由于现代解析器支持 DNS over HTTPS（DoH）等加密传输，针对解析器的封锁命令成为监管者触及那些 ISP 已难以窥探的流量的手段。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://quad9.net/">Quad 9 | A public and free DNS service for a better security and privacy</a></li>
<li><a href="https://en.wikipedia.org/wiki/Public_DNS_resolver">Public DNS resolver</a></li>
<li><a href="https://en.wikipedia.org/wiki/DNS_Blacklist">DNS Blacklist</a></li>

</ul>
</details>

**社区讨论**: Quad9 首席技术官 John Todd 在 IETF 127 现场表示，目前各方对 Quad9 立场一致支持，DNS 社区对此案及类似案件普遍感到“忧虑不安”。其他评论者感叹欧洲 2000 年代互联网自由的消退，认为这种过度监管短视；也有批评者要求 Cloudflare 不要再含糊其辞，明确承诺若自身上诉失败也会退出受影响的国家。

**标签**: `#dns`, `#internet-regulation`, `#privacy`, `#france`, `#internet-freedom`

---

<a id="item-4"></a>
## [英伟达新加坡子公司营收达 1040 亿美元，公司停止单独披露当地销售数据](https://www.ft.com/content/dbde7a30-548c-4f9d-a4be-7898a0c24dcf) ⭐️ 8.0/10

据《金融时报》报道，英伟达（Nvidia）在其新加坡子公司 2025 年外部营收达到 1040 亿美元后，已停止单独披露新加坡地区的销售数据。这一披露方式的变化，加上新加坡记账金额之庞大，引发了外界关于先进 AI 芯片是否经由当地转运至中国等受出口管制市场的讨论。 新加坡已成为英伟达最大的收入记账地之一，因此失去国别层面的透明度，会让投资者、监管机构和研究者更难判断需求真正来自何处、芯片最终流向哪里。这一争议正处在 AI 硬件供应链与美国出口管制的交叉点上——在这里，会计意义上的地理归属与芯片实际所在的地点可能大相径庭。 1040 亿美元这一数字指的是英伟达新加坡子公司的外部营收，其中包含只是通过新加坡实体开票或走单的 GPU 订单，而非实际交付到新加坡或在当地使用的芯片。由于多数终端客户是通过 OEM、ODM 和经销商间接采购英伟达 GPU，单看记账地点并不能说明硬件的最终去向。

hackernews · louiereederson · 11月17日 17:12 · [社区讨论](https://news.ycombinator.com/item?id=50534631)

**背景**: 与许多跨国公司一样，英伟达出于税务、物流和客户管理的需要，通过区域子公司确认销售，其历史上按开票实体或客户总部所在地披露收入，而不是按 GPU 实际安装的数据中心所在地。美国出口管制限制向中国销售先进 AI 加速卡，并自 2022 年 10 月起不断收紧，这使得任何记账规模异常快速增长的第三国都会受到审视。新加坡是亚洲重要的贸易与物流枢纽，在有关芯片转运的调查中常被提及为中转地，包括近期台湾查处的一起涉英伟达芯片流向中国的案件。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.csis.org/analysis/clues-us-dutch-japanese-semiconductor-export-controls-deal-are-hiding-plain-sight">Clues to the U.S.-Dutch-Japanese Semiconductor Export Controls ...</a></li>
<li><a href="https://www.mlxio.com/technology/nvidia-chip-smuggling-china-japan">$15M Nvidia Chip Haul Exposes China Smuggling Route | MLXIO</a></li>

</ul>
</details>

**社区讨论**: Hacker News 的评论者强烈反驳了“走私”叙事：多人认为 1040 亿美元纯粹是“由哪个实体记账”的会计归属问题，并不能说明收入产生地或芯片最终去向。也有人持怀疑态度，将经新加坡走单视为规避制裁的证据，并类比俄罗斯石油如何通过中间商流入西方市场；还有一派观点认为，这条新闻之所以有话题性，仅仅是因为英伟达此前披露过该数字、如今又不再披露。

**标签**: `#Nvidia`, `#Singapore`, `#export controls`, `#semiconductors`, `#AI hardware`

---

<a id="item-5"></a>
## [微软发布 MAI Code 2 与 Code 2 Flash 编程模型，已接入 GitHub Copilot](https://microsoft.ai/news/introducing-mai-code-2-and-mai-code-2-flash/) ⭐️ 8.0/10

微软发布了 MAI Code 2 和 MAI Code 2 Flash，这是其自研 MAI 编程模型家族的新一代产品，目前两款模型均已上线 GitHub Copilot。微软称 Code 2 达到 GPT-6.1 Sol 性能的 98%、成本仅为其 40%，并达到 Claude Opus 5.5 性能的 96%、成本约为其 5%；更便宜的 Flash 版本在三个面向日常高频编程任务的基准上比肩 GPT-6 Luna 和 Claude Haiku 5.5，成本分别只有后两者的 65% 和 20%。 这是微软迄今为止最明确的一次发力，意在让自研模型而非 OpenAI 的模型成为其开发者产品与生产力工具的默认引擎，这将在编程这一细分市场上直接对 OpenAI 和 Anthropic 的性价比形成压力。由于 Code 2 还被进一步优化为 MAI Work Flash 以服务 M365 和 Fabric IQ，此次发布表明微软正推行覆盖 Copilot 与企业软件的完整模型栈自有化战略。 除通用基准外，微软还表示将 Code 2 Flash 在其自有 MISRA 修复历史上微调后，对于生产环境中前沿模型需要人工返工的问题，有 44% 能给出可直接合并的修复，而成本不到前者的十分之一；此外该模型在关键的 Excel 内部客户场景基准上的准确率和 token 效率与 GPT-6 Luna 相当。这些成本数字来自微软自己对选定竞品的比较，因此应视为厂商自述数据，而非独立验证的结论。

hackernews · lemonish97 · 11月17日 18:25 · [社区讨论](https://news.ycombinator.com/item?id=50535885)

**背景**: GitHub Copilot 是微软的 AI 编程助手，此前其模型能力很大一部分来自 OpenAI 和 Anthropic，而非微软自研的 MAI 系列，后者过去主要聚焦轻量级编程辅助。MAI Code 2 被定位为向复杂、智能体式（agentic）软件工程的升级，即模型能够规划并执行多步骤改动，而不只是补全代码行。SWE-bench、LiveCodeBench 等编程基准是业界比较模型在真实软件任务上表现的标准方式，但由于榜单成绩并不总能转化为日常开发体验，这类基准一直存在争议。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://microsoft.ai/news/introducing-mai-code-2-and-mai-code-2-flash/">MAI Code 2 and Code 2 Flash: Everyday coding at scalable ...</a></li>
<li><a href="https://microsoft.ai/models/mai-code-2/">MAI Code 2 - Microsoft AI</a></li>
<li><a href="https://github.blog/changelog/2026-11-17-mai-code-2-and-mai-code-2-flash-in-github-copilot/">MAI Code 2 and MAI Code 2 Flash in GitHub Copilot</a></li>

</ul>
</details>

**社区讨论**: 社区对其实用性的反馈总体正面：一位把 Copilot 切换到 MAI Code 2 的开发者表示，它解决了 WSL/Ubuntu 中棘手的 Python 构建问题、生成了全部通过的测试用例，还修复了 Azure Bicep 部署问题，感觉与 Claude Opus 没有差别。怀疑者则质疑微软为何能如此迅速地追赶上来，猜测其通过蒸馏 OpenAI 模型实现，并追问成本对比是否存在挑选数据的嫌疑；也有人认为这次发布恰恰说明 OpenAI 和 Anthropic 的领先优势其实很薄弱。另有部分用户把矛头指向 GitHub Copilot 的订阅价值，其中一个团队称在几天内耗尽额度后，连 19 美元的档位也取消了。

**标签**: `#AI models`, `#code generation`, `#Microsoft`, `#LLM benchmarks`, `#AI competition`

---

<a id="item-6"></a>
## [SolidJS 2.0 发布：新增服务端原语与 Rust 编译器](https://www.solidjs.com/blog/solid-2-0-the-long-hold/) ⭐️ 8.0/10

SolidJS 正式发布 2.0 版本，这是这个细粒度响应式 JavaScript UI 框架的一次重大更新，新增了服务端 RPC、"live" 与 "broadcast" 等原语，并重建了基于 Oxc、用 Rust 编写的编译器工具链，@solidjs/vite-plugin 默认启用该原生工具链。此次发布还带来了改进后的诊断信息，并以"Built to Be Written by Agents"为宣传点，目标是让报错更易追踪。 这些服务端原语填补了前后端之间长期存在的鸿沟——这正是 Remix 等框架曾大力宣传却未必真正兑现的能力，使 Solid 拥有了连贯的全栈叙事。与此同时，这次发布也是对现有用户升级路径的一次压力测试，因为响应式框架的大版本升级通常会牵动响应式语义、编译产物和包体积预算。 包体积是最引人注目的隐忧：有社区基准测试显示，一个极简的计数器组件在 Solid v1.9.18 中经 brotli 压缩后为 4.8 KiB，而在 v2.0.0 中升至 20.3 KiB。早期采用者也发布了从 1.0 升级到 2.0 候选版本的详细迁移记录，说明这并非可直接替换的升级，而是涉及不小的 API 与行为变化。

hackernews · pier25 · 11月17日 18:56 · [社区讨论](https://news.ycombinator.com/item?id=50536387)

**背景**: SolidJS 是由 Ryan Carniato 创建的声明式 JavaScript UI 库，最早于 2018 年 4 月开源。它以细粒度响应式著称：不重新渲染整个组件，而是在 signal 层面追踪依赖，只更新那些依赖了变化值的具体 DOM 节点——这一模型后来也影响了其他框架中基于 signals 的响应式设计。Solid 同时体积小巧、完全支持 tree-shaking，并支持服务端渲染。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.solidjs.com/blog/solid-2-0-rc-the-big-reveal/">Solid 2.0 RC: The Big - solidjs.com</a></li>
<li><a href="https://grokipedia.com/page/SolidJS">SolidJS</a></li>
<li><a href="https://github.com/solidjs/solid">GitHub - solidjs / solid : A declarative, efficient, and flexible JavaScript...</a></li>

</ul>
</details>

**社区讨论**: 评论整体偏向正面：有人称赞服务端 RPC 以及 live、broadcast 原语比 LiveView 或 htmx/datastar 更无缝、更自然，还有人认为 Solid 对前后端"中间层"的解法非常漂亮，而 Remix 在这方面并未真正做到。主要质疑集中在包体积，有基准测试显示体积增长约四倍；也有人指出所谓"对 Agent 友好"的诊断本质上只是更好的调试体验，同样有益于人类开发者，另有一位读者分享了自己从 1.0 迁移到 2.0 的详细记录。

**标签**: `#SolidJS`, `#JavaScript`, `#frontend frameworks`, `#reactive UI`, `#web development`

---

<a id="item-7"></a>
## [Datasette Lite 使用 Service Worker 与 Pyodide 重写](https://simonwillison.net/2026/Nov/17/datasette-lite/) ⭐️ 8.0/10

Simon Willison 发布了 Datasette Lite 的完整重写版，使用 Service Worker 和 Pyodide 让完整的 Datasette Python 应用直接在浏览器中运行。新版本允许用户从 PyPI 加载指定版本的 Datasette、从 GitHub 加载特定提交/标签/分支、选择 100 多个 SQLite 版本之一，并从 PyPI 或 wheel 文件 URL 安装额外的 Datasette 插件。 这使得只需一个 URL 就能分享可复现的 Datasette 演示、开发中的功能和 bug 复现，而无需启动服务器。它也表明通过 WebAssembly 在浏览器中运行 Python 已相当成熟，因为一个真正的服务器端应用现在几乎可以在客户端上表现得一模一样。 URL 支持 ?install= 等参数来添加 datasette-maplibre 等插件，&url= 可加载 SQLite、JSON、CSV 或 SQL 文件，&metadata= 用于元数据，插件安装参数可重复以加载多个包。文章提到会有一个短暂的加载界面，并将该工具定位为链接演示的理想选择，而非替代生产服务器部署。

rss · Simon Willison · 11月17日 16:48

**背景**: Datasette 是一个用于探索和发布数据的开源 Python 工具，通常以 SQLite 数据库为后端。Pyodide 是 CPython 到 WebAssembly/Emscripten 的移植版本，能让 Python 包在浏览器中运行；而 Service Worker 则充当 Web 应用与网络之间的事件驱动代理。通过结合这两者，Datasette Lite 可以拦截浏览器请求，并在客户端提供完整的 Datasette 应用，而不是依赖 Python Web 服务器。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://pyodide.org/en/stable/index.html">Pyodide — Version 314.0.7</a></li>
<li><a href="https://github.com/simonw/datasette">GitHub - simonw/ datasette : An open source multi- tool for exploring...</a></li>
<li><a href="https://www.linkedin.com/pulse/every-background-task-belongs-service-worker-claudio-cirino-2ccbf">Not Every Background Task Belongs in a Service Worker</a></li>

</ul>
</details>

**标签**: `#Datasette`, `#Pyodide`, `#WebAssembly`, `#service workers`, `#SQLite`

---

<a id="item-8"></a>
## [美国将 AI 芯片出口管制延伸至远程访问](https://t.me/zaihuapd/45204) ⭐️ 8.0/10

2026 年 11 月中旬，美国商务部工业与安全局（BIS）发布临时最终规则，把针对先进 AI 芯片和服务器的出口许可要求扩展到“远程访问”，即境外实体不能再在无许可证的情况下合法调用托管在第三国数据中心、受美方管制的先进算力。该规则同时要求向印度尼西亚、马来西亚、新加坡、泰国和巴西再出口 AI 芯片须申请许可，并正式撤销此前的“AI 扩散规则”。 这堵上了美方眼中最大的一个漏洞——不进口芯片、而是到海外租算力，此前中国 AI 企业正是通过东南亚等地数据中心继续使用美国顶级硬件训练模型。新规可能重塑跨境云服务与 AI 基础设施合作，进一步压缩中国实验室获取前沿算力的渠道，同时给全球云厂商和数据中心运营商带来更高的合规负担。 针对新纳入管制的目的地和远程访问安排的许可证将采取“逐案审查”方式，而非一刀切地批准或拒绝；规则以“临时最终规则”形式发布，意味着它很快生效，同时 BIS 仍会收集意见并可能据此修订。有报道称，英伟达也面临相关压力，被要求说明其与中国相关的收入并未通过此类远程访问安排获得。

telegram · zaihuapd · 11月18日 05:11

**背景**: 自 2022 年起，美国通过《出口管理条例》（EAR）限制先进 AI 加速器对华出口，BIS 将顶级芯片和服务器列入 3A090、4A090 等出口管制分类编号。此后推出的“AI 扩散规则”试图管理美国 AI 技术在全球的扩散范围，但因盟友和业界反对而饱受批评，如今被正式撤销。由于此前的规则主要针对实物出货，企业仍可以租用部署在第三国数据中心里的美国设计芯片——这正是新规要封堵的缺口。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.wilmerhale.com/en/insights/client-alerts/20261117-us-government-restricts-remote-access-to-advanced-ai-chips-and-formally-rescinds-the-ai-diffusion-rule">US Government Restricts Remote Access to Advanced AI Chips ...</a></li>
<li><a href="https://www.bbc.com/news/articles/cwq6e2qgvmlgo">How Trump's chip restrictions on South East Asia will hit China</a></li>
<li><a href="https://www.cnbc.com/2026/11/17/nvidia-china-cloud-ai-chip-access.html">Nvidia warns chip buyers of legal risks tied to China access : sources</a></li>

</ul>
</details>

**标签**: `#AI chips`, `#export controls`, `#US policy`, `#semiconductors`, `#remote computing`

---