---
layout: default
title: "Horizon Summary: 2026-09-23 (ZH)"
date: 2026-09-23
lang: zh
---

> 从 43 条内容中筛选出 11 条重要资讯。

---

1. [OpenAI 发布 GPT-6 Sol 与 Luna 前沿模型](#item-1) ⭐️ 10.0/10
2. [Anthropic 发布 Claude Opus 5.5，API 价格同步下调](#item-2) ⭐️ 9.0/10
3. [五角大楼：过度依赖 AI 导致伊朗学校遭导弹袭击](#item-3) ⭐️ 9.0/10
4. [vLLM v0.30.0 发布：762 次提交、新增多款模型与持久化权重缓存](#item-4) ⭐️ 8.0/10
5. [黑客声称窃取了全体 FBI 员工的数据](#item-5) ⭐️ 8.0/10
6. [Trail of Bits 称 SAML 是“糟糕设计的分形”](#item-6) ⭐️ 8.0/10
7. [WordPress 修复可致条件性 RCE 的未授权路径穿越漏洞](#item-7) ⭐️ 8.0/10
8. [Claude Opus 5.5 与 GPT-6 Sol/Luna 发布，前沿模型价格战升温](#item-8) ⭐️ 8.0/10
9. [DeepSeek 与清华发布 DSec 沙箱平台技术报告，日服务 300 万个沙箱](#item-9) ⭐️ 8.0/10
10. [中国监管机构调查 DeepSeek 与月之暗面涉嫌数据外泄](#item-10) ⭐️ 8.0/10
11. [OpenAI 有限预览 GPT-5.6 系列：Sol、Terra、Luna 三款模型](#item-11) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [OpenAI 发布 GPT-6 Sol 与 Luna 前沿模型](https://openai.com/index/introducing-gpt-6-sol-and-luna/) ⭐️ 10.0/10

OpenAI 发布了 GPT-6 Sol 与 Luna 两款新模型，它们采用了与 GPT-6 Astra 相似的训练方法：Sol 面向编程等复杂任务，Luna 则定位于文档摘要、信息抽取、快速问答这类目标明确的高并发任务。OpenAI 表示，这两款模型把 Astra 在专业工作、事实准确性、编程、计算机操作和对齐方面的进展，带到了速度更快、价格更低的模型上。 把接近前沿的能力下放到更便宜、更快的模型层级，会显著降低智能体和高并发工作负载的运行成本，从而直接影响开发者和企业在各家 AI 平台之间的选择。这次发布也加剧了与 Anthropic 的 Claude 等对手在价格和套餐额度上的竞争，而这正是 Hacker News 讨论中争论最多的话题之一。 TechCrunch 报道称，OpenAI 同时宣称成本更低、错误更少；社区实测还指出，GPT-6 Luna 的价格大约只有 GPT-5.6 Luna 的一半，价格下调因此成为本次发布最受关注的亮点之一。两款模型延续了 OpenAI 自 GPT-5.6 起采用的层级命名方式，开发者可以把不同类型的任务分派给不同能力与成本的层级。

hackernews · OfficialTurkey · 9月22日 18:00 · [社区讨论](https://news.ycombinator.com/item?id=49805509)

**背景**: 前沿模型是指在某一时刻最先进的 AI 模型，它们基于海量数据训练，在推理、内容生成和智能体工作流上具备顶尖表现，代表着一个时代 AI 能力的上限。GPT-6 Astra 是 OpenAI 上一代的前沿智能模型，而 Sol 与 Luna 采用相同的训练方法，目的是以更低的成本把这种智能普及开来。自 GPT-5.6 一代起，OpenAI 开始使用分层命名体系（Sol、Terra、Luna），让应用可以在同一套系统内把简单分类任务交给廉价层级，把复杂分析交给更强的层级。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://techcrunch.com/2026/09/22/openai-launches-gpt-6-sol-and-luna/">OpenAI launches GPT-6 Sol and Luna, boasting lower cost and fewer mistakes | TechCrunch</a></li>
<li><a href="https://openai.com/index/introducing-gpt-6-sol-and-luna/">Introducing GPT-6 Sol and Luna | OpenAI</a></li>
<li><a href="https://www.mindstudio.ai/blog/what-is-gpt-5-6-sol-terra-luna-explained">What Is GPT-5.6? OpenAI's Sol, Terra, and Luna Model Tiers Explained | MindStudio</a></li>

</ul>
</details>

**社区讨论**: Hacker News 的讨论（1294 分、646 条评论）总体热情很高，但焦点集中在价格与工作流契合度上：Simon Willison 认为 Luna 只要 GPT-5.6 Luna 一半的价格是件大事；m_fayer 则罕见地表示自己对 5.6 Sol 产生了情感依赖，担心技术上更强的新模型反而不如它顺手。也有人直接比较套餐价值，jeffnash 基于用量限制更看好 Codex Pro 20x 而非 Claude Code 20x，leokennis 则认为对普通用户来说，ChatGPT Plus 自 5.6 起几乎已经“无限量”。

**标签**: `#OpenAI`, `#GPT-6`, `#LLM release`, `#AI models`, `#Hacker News`

---

<a id="item-2"></a>
## [Anthropic 发布 Claude Opus 5.5，API 价格同步下调](https://www.anthropic.com/claude-opus-5-5) ⭐️ 9.0/10

Anthropic 发布了 Claude Opus 5.5，官方称其为迄今最强的 Opus 模型，主打更自然的沟通表达，以及对长时间运行的智能体（agent）和编程任务的更好支持。与此同时 API 价格全面下调：每百万 token 的输入价格从 5 美元降至 4 美元，输出价格从 25 美元降至 20 美元，缓存读取从 0.50 美元降至 0.20 美元，缓存写入从 6.25 美元降至 5 美元。 价格已成为前沿模型实验室的核心竞争战场，Anthropic 在其旗舰级模型上做出这一幅度的降价，会直接对竞争对手形成压力，并显著降低智能体类、长会话类任务的运行成本。此次发布恰好紧随 Anthropic 公开呼吁“为前沿发展设定节奏（pacing the frontier）”之后，因此“话音刚落就发布新旗舰”的做法重新点燃了外界对其承诺严肃性的争论。 Anthropic 表示，早期测试者认为 Opus 5.5 的写作更清晰、更易读，会把最重要的信息放在开头，官方将此既视为易用性提升，也视为便于审查长时间智能体运行的安全收益。此次降价覆盖全部四类计费项（缓存读取、输入、输出、缓存写入），而不只是表面的输入/输出价格。

hackernews · km144 · 9月22日 16:29 · [社区讨论](https://news.ycombinator.com/item?id=49803892)

**背景**: 所谓“前沿模型（frontier model）”，是指在发布时可以代表通用能力最前沿或接近最前沿的大语言模型，通常出自少数几个有能力承担训练成本的实验室，且规模最大、价格最贵。Anthropic 的 Claude 系列按能力与成本分层：Opus 为最高端，Sonnet 居中，Haiku 最快最便宜。这些模型的 API 价格按每百万 token 计价，而提示缓存（prompt caching）——即把重复出现的上下文存下来复用——则对缓存写入和缓存读取分别计费。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.anthropic.com/claude/opus">Claude Opus \ Anthropic</a></li>
<li><a href="https://claude.com/blog/claude-models-explained-choosing-the-best-model-for-your-use-case">Claude models explained: choosing the best model for your use ...</a></li>
<li><a href="https://www.levellers.ai/what-is/frontier-model">What is a frontier model ? Clear business guide | Levellers. ai</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上的讨论规模庞大且观点分化：不少人认为这次降价早该到来，并援引 OpenRouter 的数据指出 Opus 5 曾是该平台上支出最高的模型；也有人嘲讽发布文首句提到“为前沿设定节奏”，认为这恰恰说明 Anthropic 根本没有在放慢脚步。一些开发者表示自己更满足于 DeepSeek 这类更便宜的替代方案，称其工具调用极为积极且成本低廉，另一些人则肯定了官方所描述的沟通质量提升。

**标签**: `#AI/ML`, `#Anthropic`, `#Claude`, `#LLM Release`, `#Pricing`

---

<a id="item-3"></a>
## [五角大楼：过度依赖 AI 导致伊朗学校遭导弹袭击](https://www.bloomberg.com/graphics/2026-iran-school-attack/) ⭐️ 9.0/10

据彭博社调查报道，五角大楼得出结论称，过度依赖一套 AI 目标定位系统是导致伊朗米纳布一所学校遭到致命导弹袭击的原因之一。报告认定美国“未能尽到一切可行努力去核实”该学校是军事目标这一义务，并称这一失职“已超出单纯的疏忽”。 这是主要军事强国首次公开承认 AI 辅助目标定位流程与平民死亡相关，为国际人道法下的问责争论树立了先例。此事很可能加剧外界对军用 AI 采购、杀伤链自动化以及机器推荐目标法律责任的审视。 米纳布这处地点因数据过时而一直被登记为伊斯兰革命卫队设施，它与其他候选目标一起被输入 Maven 系统，最终被列为推荐的“首日打击目标”，把过去需要数小时的目标清单工作压缩到几分钟。另有一件相关事件：美方曾差点登临一艘被 AI 误判为载有核武器材料的中国船只。

hackernews · devonnull · 9月22日 19:03 · [社区讨论](https://news.ycombinator.com/item?id=49806430)

**背景**: Project Maven（马文计划）是美国国防部的一个项目，利用机器学习分析无人机影像和情报数据，以帮助生成和排序打击目标。这类自动推荐系统能够加速“杀伤链”，但其输出结果的可靠性完全取决于底层数据质量以及叠加其上的人工审核。根据国际人道法，军队必须核实目标确属合法的军事目标，并采取可行预防措施保护平民；而当推荐以机器速度生成时，这些义务就更难履行。

**社区讨论**: 评论者大多反对把 AI 本身当作罪魁祸首：有人指出报告描述的是人类指挥层的鲁莽行为，“已超出单纯的疏忽”；也有人认为真正的问题在于这套流程“优化了错误的指标”。还有人将其与以色列据称使用 AI 打击哈马斯成员的做法相提并论，质疑为何任何国家会部署此类工具，并以 AI 误判中国船只一事作为系统性风险的又一佐证。

**标签**: `#AI ethics`, `#military AI`, `#automated targeting`, `#accountability`, `#Pentagon`

---

<a id="item-4"></a>
## [vLLM v0.30.0 发布：762 次提交、新增多款模型与持久化权重缓存](https://github.com/vllm-project/vllm/releases/tag/v0.30.0) ⭐️ 8.0/10

vLLM 项目发布了 v0.30.0，这一重要版本由 315 位贡献者（其中 104 位是新贡献者）提交的 762 个 commit 构成，新增支持 DeepSeek-V4.1-Flash、DeepSeek-V4-Flash-Vision-Exp、GLM-5.3-Flash、K2-Horizon、Cohere Compass、Bailing V3 VL、Nanbeige4.2 等模型。该版本还引入了 "Fast Start" 功能：一个常驻的每 GPU 权重缓存守护进程，将量化后、按张量并行切分的权重保留在 GPU 显存中，使重启的引擎可以通过 `--load-format ipc_cache` 经 CUDA IPC 直接映射这些权重，而无需从磁盘重新加载。 vLLM 是目前使用最广泛的开源大模型推理与服务引擎之一，因此它的版本发布直接影响企业如何在生产环境中部署和扩展模型。Fast Start 尤其针对大规模服务中最痛苦的一项运维成本——长达数分钟的引擎重启与重新量化过程；而大量新增模型支持也意味着运维方无需等待第三方分支即可采用更新的模型架构。 Fast Start 目前已经覆盖 FP4 检查点和多节点张量并行；其他亮点还包括支持按请求退出的 Gumbel-max 水印生成与检测（双密钥模式可兼容投机解码）、在 GPU 显存紧张时把稀疏 MLA 的 KV 页溢写到固定主机内存的 HiSparse 主机侧分层、具备双批次重叠的 "Model Runner V2"、流水线并行下的 MTP/EAGLE3 投机解码，以及将 H200 上引擎初始化从 28.9 秒缩短到 8.2 秒的图捕获优化。该版本还新增了通过 `quantization_config.targets` 实现的目标化在线量化、配合 `nvfp4_fp8_ds_mla` KV 缓存的 W4A16 DSA，并在 SM100/103 上将 FlashInfer CuTeDSL NVFP4 W4A16 设为优于 Marlin 的默认实现。

github · khluu · 9月22日 05:20

**背景**: vLLM 是一个用于大语言模型高吞吐服务与推理的开源库，已经成为 AI 基础设施栈中事实上的标准组件，既用于在线 API 服务，也用于离线批处理和强化学习的采样生成。本次发布说明中提到的 MXFP8、NVFP4 属于低精度数值格式（块缩放浮点格式，可压缩显存占用并加速现代 GPU 上的矩阵乘法），此外还涉及 DeepSeek 的 FlashMLA 注意力算子、DeepGEMM 张量核心算子库、张量并行（TP，把模型切分到多张 GPU 上）以及投机解码（用小草稿模型提议 token、由大模型验证）。由于这些底层组件更新极快，一次同时整合新模型、新算子和新服务能力的版本发布，正是从业者采纳这些技术的主要渠道。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/deepseek-ai/FlashMLA">GitHub - deepseek-ai/ FlashMLA : FlashMLA : Efficient Multi-head...</a></li>
<li><a href="https://github.com/deepseek-ai/DeepGEMM">GitHub - deepseek-ai/DeepGEMM: DeepGEMM: clean and efficient BLAS kernel library on GPU · GitHub</a></li>
<li><a href="https://en.wikipedia.org/wiki/MXFP8">MXFP8</a></li>

</ul>
</details>

**标签**: `#vLLM`, `#LLM inference`, `#release`, `#model serving`, `#AI infrastructure`

---

<a id="item-5"></a>
## [黑客声称窃取了全体 FBI 员工的数据](https://www.404media.co/we-hacked-the-fbi-hackers-say-they-have-data-on-all-fbi-employees/) ⭐️ 8.0/10

一个打出“我们入侵了 FBI”旗号的黑客组织声称已窃取覆盖全体 FBI 员工的数据，这一说法由 404 Media 报道，目前尚未得到独立证实。该组织的一名代表对媒体表示，他们计划做的事情“不能算勒索，或许算胁迫”，并补充说这次行动“并非出于金钱动机”。 如果该说法属实，意味着整个国家执法机构的员工个人与联系方式数据落入犯罪分子乃至潜在国家行为体之手，会给探员和工作人员带来严重的反情报与骚扰风险。这也进一步印证了业内日益普遍的看法：即便是资源充足的政府机构也无法完全阻止大规模数据窃取，从而把重心从单纯预防转向检测、止损与受害者保护。 该报道没有提供入侵的技术证据，在可获取的摘要中也没有 FBI 的确认或经独立核实的样本数据，因此这一说法应被视为未经证实。其暗示的数据规模相当可观——有评论者指出，窃取数 TB 数据通常需要数天到数周，理应触发系统管理员的警报——但现有材料并未给出时间线、数据量或入侵途径。

hackernews · spenvo · 9月22日 17:46 · [社区讨论](https://news.ycombinator.com/item?id=49805278)

**背景**: 404 Media 是一家独立科技新闻媒体，经常报道黑客组织与网络犯罪产业。讨论中提到了 ShinyHunters，这是一个知名的数据窃取与勒索团伙，此前曾泄露多家大型企业的数据库，不过该新闻本身并未确认该组织的身份。“数据外泄”（exfiltration）指的是把数据从网络中复制带走，而不只是入侵系统；现代勒索团伙常常放弃传统的勒索软件加密手段，转而威胁公开或出售窃取的数据。评论者还提到 2015 年美国人事管理局（OPM）数据泄露事件，那次事件曝光了约 2200 万名现任及前任联邦雇员的记录，可作为此类泄露危害程度的先例。

**社区讨论**: Hacker News 上的反应混杂着技术担忧、质疑与黑色幽默。一些评论者质疑数 TB 数据如何能在不被察觉的情况下流出网络，并追问为何系统管理员没有收到警报；另一些人则持愤世嫉俗的看法，认为如今没有任何大型数据库是安全的，并以 OPM 泄露事件作为佐证。还有人用玩笑来回应这条新闻——引用《太空堡垒卡拉狄加》中不联网飞船的桥段，以及对该组织所谓非金钱“胁迫”说法的讽刺。

**标签**: `#cybersecurity`, `#data breach`, `#FBI`, `#hacking`, `#privacy`

---

<a id="item-6"></a>
## [Trail of Bits 称 SAML 是“糟糕设计的分形”](https://blog.trailofbits.com/2026/09/21/saml-a-fractal-of-bad-design/) ⭐️ 8.0/10

Trail of Bits 于 2026 年 9 月 21 日发表了一篇题为《SAML：糟糕设计的分形》的博客文章，认为 SAML 认证协议的问题并非个别 bug，而是深层的结构性设计缺陷。该文在 Hacker News 上引发了热烈讨论，获得 184 分和 106 条评论，内容涉及规范化失败、XML 签名漏洞以及替代方案。 SAML 至今仍是企业单点登录的支柱，因此来自知名安全公司 Trail of Bits 的严厉批评进一步强化了行业应迁移到 OIDC 等现代认证协议的长期主张。对防御方而言，这也说明 SAML 部署中的漏洞往往源于协议本身的复杂性，而不只是实现者的粗心。 批评的核心在于 XML 规范化（canonicalization）——即为签名或验签而生成字节级精确 XML 表示的脆弱过程——以及像 XML 签名包装（signature wrapping）这类攻击：攻击者利用 XML 结构的灵活性，让一个有效签名通过校验，而应用程序实际处理的却是另一个未经认证的元素。社区成员还回忆称，XML 签名的主流 C 语言实现曾经默认还会接受由攻击者控制文档中指定的 HMAC 签名，或依据 Web PKI 链的签名，从而使伪造的断言轻易通过验证。

hackernews · aray07 · 9月22日 18:57 · [社区讨论](https://news.ycombinator.com/item?id=49806335)

**背景**: SAML 2.0（安全断言标记语言）是一种基于 XML 的标准，用于在身份提供者（IdP）与服务提供者（SP）之间交换认证和授权数据，也是当今大多数企业单点登录的实现方式。由于 SAML 消息是 XML，其完整性由 XML Signature 规范保护，而该规范需要先对元素进行规范化、计算哈希，然后再签名——这条链条上有许多对实现细节高度敏感的步骤。同一份 XML 信息可以有多种等价的序列化形式，因此引入了规范化以保证签名可复现，但这也制造了巨大的攻击面，XML 签名包装攻击正是通过把被签名元素移动到文档其他位置来加以利用。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/SAML">SAML - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/SAML_2.0">SAML 2.0 - Wikipedia</a></li>
<li><a href="https://www.ibm.com/think/topics/xml-signature-wrapping">What is XML Signature Wrapping? | IBM</a></li>

</ul>
</details>

**社区讨论**: 评论者总体认同这一批评，但在解决思路上存在分歧：有人主张协议设计应彻底避免规范化——即先对收到的原始数据块验证签名，再进行解码；也有人分享了 C 语言 XML 签名库会接受攻击者文档中的 HMAC 密码和 Web PKI 密钥的骇人经历。还有人对“OIDC 必胜论”提出了反驳，指出 SAML 仍独有 IdP 发起的流程，且其被广泛实现的子集更为稳定，因此面向企业销售的产品应当同时支持两者。

**标签**: `#SAML`, `#security`, `#authentication`, `#XML`, `#protocol-design`

---

<a id="item-7"></a>
## [WordPress 修复可致条件性 RCE 的未授权路径穿越漏洞](https://github.com/WordPress/wordpress-develop/security/advisories/GHSA-7hp8-65ch-5whp) ⭐️ 8.0/10

WordPress 发布了 7.1.2 版本，修复了一个未授权的路径穿越漏洞（编号 CVE-2026-87902）：攻击者可诱导 get_page_template() 的页面模板解析过程包含活动主题目录之外任意可读的本地 .php 文件，从而可能造成远程代码执行。出于对旧版本用户的照顾，该修复被向后移植到 WordPress 4.7 以来的所有分支。 WordPress 占据了互联网上极大的份额，而一个无需认证、又可升级为远程代码执行的漏洞属于最危险的一类缺陷，因为攻击者既不需要登录也不需要用户交互。补丁一直向后移植到约九年前的分支，说明仍有大量部署运行在旧版本上，如今需要紧急更新。 该漏洞的利用是有条件的，而非必然成功：公告指出必须先满足服务器环境与当前活动主题这两方面的相关前提，文件包含才可能升级为 RCE。相关代码路径可追溯到 locate_template()，其官方文档多年前就警告过：当传入用户提供的模板名时，该函数无法阻止目录穿越。

hackernews · vntok · 9月22日 16:33 · [社区讨论](https://news.ycombinator.com/item?id=49803959)

**背景**: 路径穿越是一种 Web 漏洞：应用在拼接文件路径时未做充分校验，使攻击者能够访问预期目录之外的文件。远程代码执行（RCE）指攻击者可以在目标服务器上运行自己的代码，通常是安全缺陷中最严重的后果。WordPress 是基于 PHP 的内容管理系统，通过包含当前主题中的模板文件来渲染页面，get_page_template() 之类的函数负责决定加载哪个模板文件。如果这一解析过程可以被引导到主题目录之外的 .php 文件，攻击者就可能让服务器执行该文件。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/WordPress/wordpress-develop/security/advisories/GHSA-7hp8-65ch-5whp">Unauthenticated path traversal in page-template resolution leading to conditional RCE · Advisory · WordPress/wordpress-develop · GitHub</a></li>
<li><a href="https://securityonline.info/wordpress-rce-vulnerability-cve-2026-87902/">CVE-2026-87902: Critical WordPress RCE Flaw Fixed in Version 7.1.2</a></li>
<li><a href="https://en.wikipedia.org/wiki/Arbitrary_code_execution">Arbitrary code execution - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 评论者普遍并不意外，认为 WordPress 堪称 Web 历史上被利用最多的软件之一，并指出约三分之一的安装仍未使用较新的 7.x 分支。有人分享了迁移经历，其中一位读者改用静态托管的 Hugo 模板以彻底摆脱 WordPress；还有人指出，九年前该受影响函数下的一条文档评论就已经同时描述了这个缺陷的性质及其修复方法。

**标签**: `#WordPress`, `#security`, `#vulnerability`, `#RCE`, `#path-traversal`

---

<a id="item-8"></a>
## [Claude Opus 5.5 与 GPT-6 Sol/Luna 发布，前沿模型价格战升温](https://simonwillison.net/2026/Sep/22/opus-and-sol-and-luna/) ⭐️ 8.0/10

同一天，Anthropic 发布了 Claude Opus 5.5，约一小时后 OpenAI 发布了 GPT-6 Sol 和 GPT-6 Luna；此前一天还有 Grok 4.7 和小米的 MiMo v2.6 Flash/Pro 亮相。Simon Willison 指出，GPT-6 Luna 的价格只有 GPT-5.6 Luna 的一半（输入每百万 token 0.10 美元、输出每百万 token 0.50 美元），GPT-6 Sol 相比 GPT-5.6 Sol 也有类似的降价幅度。 把前沿级模型的价格砍半，会大幅降低开发者构建 AI 应用的成本，同时挤压竞争对手——Grok 4.7 此前每百万 token 2 美元输入/6 美元输出的价格优势，如今在 GPT-6 Sol 面前已基本被抹平。这种变化还会在一夜之间让旧型号过时：GPT-5.6 Terra 与 GPT-6 Sol 定价相同但输出价格更高，Willison 认为继续使用 Terra 的理由已经不复存在。 GPT-6 Luna 每百万 token 输入 0.10 美元、输出 0.50 美元，是 OpenAI 有史以来最便宜的模型之一，仅落后于能力弱得多的 GPT-4.1 Nano（0.10/0.40 美元，2025 年 4 月）和 GPT-5 Nano（0.05/0.40 美元，2025 年 8 月）。Claude Opus 5.5 的定价为输入 4 美元、输出 20 美元，缓存输入 0.20 美元；而 GPT-5.6 计划在 11 月涨价 25%，这意味着 GPT-6 只有这些模型促销价的一半，而非仅仅是标价的一半。

rss · Simon Willison · 9月22日 23:46

**背景**: 这些模型属于“前沿”大语言模型，即各家实验室能力最强的通用模型，通过 API 按每百万输入与输出 token 计价；缓存输入价格则是在重复使用同一段上下文时提供的折扣。Willison 是知名开发者和分析师，同时也是非正式“骑自行车的鹈鹕”基准的创造者——该基准要求模型生成一张鹈鹕骑自行车的 SVG 图，他在这里用它来比较 GPT-6 与 GPT-5.6 系列的可视化输出。如今模型发布往往伴随着大幅降价，这是前沿 token 价格远低于 2023 年水平的整体趋势的一部分。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://ai.miraheze.org/wiki/Pelican_Bicycle_Benchmark">Pelican Bicycle Benchmark - Learn AI</a></li>
<li><a href="https://benchlm.ai/llm-pricing-trends">LLM API Pricing Trends & Updates (September 2026) | BenchLM.ai</a></li>
<li><a href="https://siliconangle.com/2026/09/22/xiaomi-introduces-mimo-v2-6-series-open-source-ai-model-family/">Xiaomi introduces Mimo-V2.6 series open-source AI model family - SiliconANGLE</a></li>

</ul>
</details>

**标签**: `#LLMs`, `#AI industry`, `#model releases`, `#pricing`, `#OpenAI/Anthropic`

---

<a id="item-9"></a>
## [DeepSeek 与清华发布 DSec 沙箱平台技术报告，日服务 300 万个沙箱](https://arxiv.org/abs/2609.22978) ⭐️ 8.0/10

DeepSeek-AI 与清华大学联合发布技术报告，公开了自研沙箱基础设施 DSec（DeepSeek Elastic Compute），用于支撑大规模智能体（Agent）训练与评测。该平台通过统一 SDK 提供 FnCall、容器、Firecracker microVM 和完整 VM 四种后端，覆盖 OJ 判题、软件工程、安全渗透、电脑操作等多种负载。 沙箱的并发规模与启动延迟被普遍视为强化学习智能体训练的核心瓶颈，因此一份关于如何每天支撑数百万个隔离环境的量产级实践报告，对任何构建智能体系统的人都很有价值。报告还展示了如何将有状态的 rollout 执行与可抢占的 GPU 训练解耦，这一设计思路很可能影响其他团队构建智能体强化学习流水线的方式。 单个生产单元约 160 个节点，每天服务约 300 万个沙箱实例，峰值并发超过 38 万，创建速度超过每秒 5000 个；单节点可高密度承载 3200 个容器或 800 个 microVM。DSec 基于 3FS 分布式文件系统按需加载 EROFS 镜像，报告称相比传统 Docker 全量拉取任务完成时间快 1.7 倍、磁盘写入减少 57%，同时内存共享与回收机制使峰值内存占用下降约 40%。

telegram · zaihuapd · 9月22日 04:45

**背景**: 智能体训练通常需要模型在可重置的隔离环境中与真实软件交互，例如执行代码、浏览文件或操作操作系统，这正是沙箱的作用。Firecracker 是 AWS 开源的虚拟化技术，能创建轻量级 microVM，兼具硬件级隔离、亚秒级启动和低内存开销，因此广泛用于多租户场景。EROFS 是面向运行时性能和存储节省优化的轻量级 Linux 只读文件系统，而 3FS（Fire-Flyer File System）是 DeepSeek 自研的高性能分布式文件系统，基于 SSD 与 RDMA 网络为 AI 工作负载设计。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/firecracker-microvm/firecracker">GitHub - firecracker-microvm/firecracker: Secure and fast ... GitHub - firecracker-microvm/firecracker: Secure and fast ... firecracker-microvm/firecracker | DeepWiki Run Your First Firecracker microVM - labs.iximiuz.com I tried Firecracker microVMs for self-hosted services, and it ... What Is a Firecracker VM? · Learn</a></li>
<li><a href="https://zh.wikipedia.org/wiki/EROFS">EROFS - 维基百科，自由的百科全书</a></li>
<li><a href="https://blog.csdn.net/qq_45453266/article/details/145924103">DeepSeek开源周Day5压轴登场： 3 FS 与Smallpond，能否终结AI...</a></li>

</ul>
</details>

**标签**: `#AI agents`, `#sandbox infrastructure`, `#DeepSeek`, `#RL training`, `#systems`

---

<a id="item-10"></a>
## [中国监管机构调查 DeepSeek 与月之暗面涉嫌数据外泄](https://www.theinformation.com/articles/china-probes-deepseek-moonshot-potential-data-leaks-anthropic) ⭐️ 8.0/10

中国互联网监管机构正在调查 DeepSeek 与月之暗面（Moonshot AI），起因是 Anthropic 于 9 月 10 日发布的 154 页报告指控 7 家中国 AI 公司违规将用户数据转发给其 Claude 模型，其中举例称 DeepSeek 曾把警方监控系统开发工程师的请求转发给 Claude。The Information 援引知情人士报道了此次调查。 此次调查是中国监管机构少见地针对本国头部 AI 初创企业跨境使用模型的行为展开审查，把一家海外厂商的违规报告升级为国内数据治理案件。这可能改变中国 AI 公司处理数据流向和 API 访问的方式，同时也加剧了中国模型开发者与美国 AI 实验室（如 Anthropic）之间本已紧张的地缘政治博弈。 Anthropic 的报告指控有组织地通过大量虚假账户“工业化规模”地滥用 Claude——此前披露提到约 2.4 万个虚假账户、超过 1600 万次交互，而仅归因于阿里巴巴的操作者据称在三个月内向 Claude 发起了超过 1.51 亿次交互。DeepSeek 和月之暗面目前均未公开确认此事，涉嫌违反的具体数据处理规定也尚不明确。

telegram · zaihuapd · 9月22日 14:37

**背景**: Anthropic 是一家美国 AI 公司，开发 Claude 系列模型，今年以来已多次发布威胁情报报告，指控中国实验室进行“蒸馏”——即用另一个模型的输出训练自家模型，以低成本复制其能力。DeepSeek 是一家总部位于杭州的 AI 实验室，以低成本前沿模型著称；月之暗面（Moonshot AI）是北京的一家公司，旗下有 Kimi 助手。两者都是中国最受关注的 AI 初创企业，因此官方对其数据处理行为展开调查格外引人注目。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.voachinese.com/a/anthropic-alleges-chinese-ai-firms-distilled-claude-s-capabilities-as-china-linked-accounts-used-it-for-overseas-surveillance-20260911/8196927.html">Anthropic 指 中 国 AI 公 司 大 规 模蒸馏 Claude ... | 美 国 之音</a></li>
<li><a href="https://zh.wikipedia.org/wiki/月之暗面_(公司)">月 之 暗 面 ( 公 司 ) - 维基百科，自由的百科全书</a></li>
<li><a href="https://finance.sina.cn/tech/2026-02-24/detail-inhnxaes3088094.d.html?fromtech=1&vt=4">中国公司“偷走” Claude 模 型 ？Anthropic气炸，却被马斯克一句话怼到无语</a></li>

</ul>
</details>

**标签**: `#AI regulation`, `#DeepSeek`, `#Anthropic Claude`, `#data privacy`, `#China tech policy`

---

<a id="item-11"></a>
## [OpenAI 有限预览 GPT-5.6 系列：Sol、Terra、Luna 三款模型](https://t.me/zaihuapd/43990) ⭐️ 8.0/10

据报 OpenAI 已开始对 GPT-5.6 系列模型进行有限预览，该系列包括旗舰模型 Sol、均衡型 Terra 和低成本模型 Luna。此次预览最初只面向少数可信合作伙伴，通过 API 和 Codex 提供；OpenAI 称这是应美国政府要求采取的短期措施，目标是在未来几周内扩展到 ChatGPT、Codex 等产品。 OpenAI 推出新的旗舰模型系列将是 LLM 领域最具影响力的事件之一，会直接影响基于 API 开发的开发者、竞争对手的定位以及企业选型决策。报道中提到的政府介入预览环节，也表明前沿模型的开放节奏正越来越多地受到政策与国家安全因素的左右，而非单纯由商业时间表决定。 据称 Sol 主打更强的编码、生物和网络安全能力，并新增“max”推理强度以及“ultra”模式；Terra 的性能接近 GPT-5.5 而成本大约只有其一半；Luna 则定位为最低成本的选择。这些说法来自单一 Telegram 聚合频道，尚无独立来源验证，因此定价、上下文长度和基准测试成绩等具体细节仍无法确认。

telegram · zaihuapd · 9月22日 18:04

**背景**: OpenAI 一直以带编号的世代来命名其前沿模型（GPT-4、GPT-5 及其后续版本），并通过更高的推理强度档位和专门模式在延迟与回答质量之间做取舍，而“x.5”这类编号通常表示中间版本的小幅更新，而非完整的代际跃升。Codex 是 OpenAI 的一套 AI 编程智能体，允许开发者把编写功能、修复缺陷等软件工程任务交给由模型驱动的智能体完成，这正是它与 API 一同成为预览模型早期分发渠道的原因。在正式开放前先面向经过审核的合作伙伴进行有限预览，是行业常见做法，便于 OpenAI 在受控条件下收集安全性与可靠性数据。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://grokipedia.com/page/OpenAI_Codex">OpenAI Codex</a></li>

</ul>
</details>

**标签**: `#OpenAI`, `#GPT-5.6`, `#LLM`, `#model-release`, `#AI`

---