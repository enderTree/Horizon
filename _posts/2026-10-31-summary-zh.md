---
layout: default
title: "Horizon Summary: 2026-10-31 (ZH)"
date: 2026-10-31
lang: zh
---

> 从 37 条内容中筛选出 8 条重要资讯。

---

1. [被植入后门的 Claude Code 扩展经由 Cursor 市场写入 SSH 密钥](#item-1) ⭐️ 8.0/10
2. [Northflank 遭遇安全入侵，成为最新一家受攻击的多租户 PaaS 厂商](#item-2) ⭐️ 8.0/10
3. [Show HN：约 1GB 的 Qwen 权重中实现可运行的 NES 模拟器](#item-3) ⭐️ 8.0/10
4. [Tangled 正式发布：基于 AT Protocol 的联邦式代码托管平台](#item-4) ⭐️ 8.0/10
5. [研究者披露 Azure 中五个可完全跨租户入侵的漏洞链](#item-5) ⭐️ 8.0/10
6. [有观点认为：AI 不是在取代 SRE，而是在让其“技能退化”](#item-6) ⭐️ 8.0/10
7. [Soft-MTP：一行梯度修改让多 Token 预测真正发挥作用](#item-7) ⭐️ 8.0/10
8. [DeepSeek 二轮融资约 1055 亿元，估值突破 6155 亿元](#item-8) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [被植入后门的 Claude Code 扩展经由 Cursor 市场写入 SSH 密钥](https://phorion.io/blog/offical-claude-code-vsx-compromise/) ⭐️ 8.0/10

一名恶意行为者将篡改过的 Anthropic Claude Code VS Code 扩展发布到了 Cursor 市场（该市场从 Open VSX 注册表获取扩展），该版本存活了约 11 个小时——从太平洋时间 10 月 29 日周四凌晨 2:27 到下午 1:35——随后被下架并替换。被篡改的版本会向用户的 ~/.ssh/authorized_keys 文件追加一个标记为 "svc-telemetry" 的攻击者 SSH 公钥，Cursor 估计最多有 5000 名用户受到影响。 这是一起针对 AI 编码工具的典型供应链攻击：由于 IDE 扩展以开发者本人的权限运行，一个被投毒的市场条目就能立即获取本地源代码、凭据和开发者机器的访问权。它还凸显了 Cursor 与 Open VSX 等替代市场的结构性风险——这些市场在大多数用户默认可信的微软官方市场之外镜像或重新发布扩展。 该后门属于持久化手法而非漏洞利用：authorized_keys 中的一行内容即可让攻击者获得永久免密 SSH 登录权限，且改密码也无法清除。受影响用户可在 macOS 上运行 `grep -qs svc-telemetry ~/.ssh/authorized_keys && echo "svc-telemetry key found" || echo "No key found; machine not impacted"` 进行自查（Windows 和 Linux 有对应命令），被投毒的版本最终被 2.1.314 版本取代。

hackernews · _chall · 10月30日 07:09 · [社区讨论](https://news.ycombinator.com/item?id=50300683)

**背景**: Claude Code 是 Anthropic 的智能体式编码工具，同时提供终端 CLI 和 VS Code 扩展两种形态；该扩展官方通过微软 Visual Studio Marketplace 和 Anthropic 自有渠道分发。Cursor 是一款基于 VS Code 的流行 AI 优先 IDE，其自有市场主要从 Open VSX 注册表而非微软市场拉取扩展。~/.ssh/authorized_keys 文件列出了允许通过 SSH 登录某账户的公钥，因此在其中添加一条记录是攻击者在初次入侵后维持机器访问权最简单、最持久的方式之一。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://phorion.io/blog/offical-claude-code-vsx-compromise/">Official Claude Code Extension Compromise: Security ... | Phorion</a></li>
<li><a href="https://thehackernews.com/2026/10/official-claude-code-vs-code-extension.html">Official Claude Code VS Code Extension Compromised to Install...</a></li>
<li><a href="https://nhimg.org/glossary/ssh-authorized-keys-backdoor/">What Is SSH Authorized Keys Backdoor? Definition & Examples</a></li>

</ul>
</details>

**社区讨论**: Anthropic 工程师 Felix Rieseberg 在讨论中确认，此次事件并非 Anthropic 系统或员工电脑被攻破，而是恶意行为者利用对 Cursor 市场的访问权限发布了并非 Anthropic 构建的版本，仅 Cursor 用户受影响。评论者分享了检测命令和路透社报道的时间线，同时也追问责任归属与影响范围，有人指出目前尚不确定微软官方市场上的版本是否受影响（现有报道明确指向 Cursor 市场和 Open VSX）。

**标签**: `#security`, `#supply-chain-attack`, `#ai-coding-tools`, `#vs-code-extensions`, `#backdoor`

---

<a id="item-2"></a>
## [Northflank 遭遇安全入侵，成为最新一家受攻击的多租户 PaaS 厂商](https://status.northflank.com/) ⭐️ 8.0/10

Northflank 是一家提供托管 Kubernetes 与 AI 运行时 PaaS 的服务商，为多个区域的多租户托管工作负载，此次通过其状态页面披露了一起安全入侵事件。这使其成为自 9 月以来据称遭遇高速攻击的第六家多租户 as-a-service 厂商，此前已有 PingCAP/TiDB、Fireworks AI、Zeabur、OpenCode Console 和 Railway 等。 这起入侵强化了一个模式：规模较小的托管基础设施厂商正接连遭遇快速、反复的攻击，这也促使开发者质疑平台便利性是否值得承担风险集中的代价。评论者预测企业可能重新回流到超大规模云厂商，因为在企业采购决策中，安全口碑正日益压过开发者体验。 Northflank 对外宣传其具备多层防护，包括加密密钥、沙箱化工作负载执行、网络隔离以及面向多租户环境的基于身份的访问控制，但厂商并未公布此次入侵的影响范围，也未说明客户密钥是否泄露。有评论者称客户代码与二进制文件似乎未被访问，不过厂商并未明确证实这一点。

hackernews · js4ever · 10月30日 15:10 · [社区讨论](https://news.ycombinator.com/item?id=50305025)

**背景**: 像 Northflank 这样的 PaaS 厂商在共享基础设施上运行众多客户的容器、数据库和密钥，这种多租户架构在数据隔离、配置错误和跨租户越权访问方面带来了固有风险。由于此类平台通常掌握部署凭据和环境变量（其中往往包含 API 密钥与数据库密码），控制面一旦失陷，就可能同时波及每一个客户的工作负载。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://northflank.com/features/platform">Platform — Features — Northflank</a></li>
<li><a href="https://www.datacenters.com/providers/northflank">Northflank | Managed Kubernetes PaaS & AI Cloud Runtime</a></li>
<li><a href="https://www.datamation.com/big-data/what-is-multi-tenant-architecture/">Exploring Multi - Tenant Architecture: A Comprehensive... | Datamation</a></li>

</ul>
</details>

**社区讨论**: 评论者将这起事件视为更广泛的信息安全紧急状况的一部分，有人统计出自 9 月以来针对多租户 as-a-service 厂商的至少六起高速攻击。其他人分享了防御技巧，例如加密环境变量并将解密密钥硬编码在应用代码中；还有人预测客户会回流到超大规模云厂商，并担忧面对 LLM 速度的攻击，技术层面的安全防护可能已难以为继。

**标签**: `#security`, `#saas`, `#cloud-infrastructure`, `#breach`, `#multi-tenancy`

---

<a id="item-3"></a>
## [Show HN：约 1GB 的 Qwen 权重中实现可运行的 NES 模拟器](https://github.com/dbreunig/nesformer) ⭐️ 8.0/10

开发者 dbreunig 发布了名为“nesformer”的项目，它并非用普通代码、而是用约 1GB 的 Qwen 模型权重来模拟任天堂娱乐系统（NES）的芯片与内存行为，让主机通过 Transformer 内部的矩阵乘法运行起来。据作者称，这套可用的权重和代码只用了两个提示词就让 Claude 模型生成，起点是此前关于在 Qwen 中构建计算机（qwenputer）的文章。 该项目具体证明了小型虚拟机可以被“编译”进大模型的参数中，由此引发了关于直接在权重内部运行解释器、shell 和命令行工具、而非通过缓慢的外部工具调用完成的设想。同时它也直观展示了神经计算与确定性程序之间巨大的效率鸿沟——这个模拟器比真实硬件慢 150–290 倍。 作者称 nesformer 的运行速度比真实主机慢 150–290 倍，讨论的焦点之一是能否用更小、更快的模型达到实时性能。评论者指出，这种方法消耗的算力比用普通代码编写的传统模拟器高出数千倍；还有读者批评该项目的 README 明显是 AI 写的、难以阅读。

hackernews · dbreunig · 10月30日 16:40 · [社区讨论](https://news.ycombinator.com/item?id=50306442)

**背景**: NES 模拟器通常用确定性软件重新实现主机的 CPU、图形与声音芯片以及内存，每条指令都被精确而廉价地执行。而 Qwen 这类大语言模型则是通过数十亿参数以及注意力、矩阵乘法等运算隐式地完成计算，这些运算本用于预测文本 token。该项目要问的是：能否调整这些权重矩阵，使一次前向传播就能复现主机芯片的状态转换，从而把一台虚拟机“嵌入”模型之中。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Qwen">Qwen - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/NES_emulator">NES emulator</a></li>
<li><a href="https://en.wikipedia.org/wiki/Transformer_(deep_learning)">Transformer (deep learning) - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 社区反应热情但对效率持怀疑态度：一位评论者设想把小型虚拟机编译进权重，用来承载 Python 解释器、shell 以及 sed、grep 等工具，全部通过批量化矩阵运算执行；其他人则欣赏这一创客式玩法，但从汇编级编程的角度看觉得它“令人恐惧”。多位评论者以此说明确定性程序仍然高效得多，还有人直接因 README 是 AI 生成而拒绝阅读。

**标签**: `#LLM`, `#emulation`, `#Qwen`, `#neural-computation`, `#Show HN`

---

<a id="item-4"></a>
## [Tangled 正式发布：基于 AT Protocol 的联邦式代码托管平台](https://tangled.org/blog/forge/) ⭐️ 8.0/10

基于 AT Protocol 构建的联邦式代码托管平台 Tangled 正式公开发布，此次发布稳定了其 lexicon 数据模式、全面重构了架构与界面，并新增了对组织（organizations）的支持。团队表示现在自托管整栈或其中部分组件（Git 托管、CI runner、API 服务器、前端界面）都非常容易，私有仓库也将在接下来的一两周内上线。 代码托管是开发者基础设施中少数仍由单一中心化平台主导的领域之一，而一个允许任何人自建服务器、又能跨实例协作的 forge，为 GitHub 提供了真正意义上的替代方案。Tangled 背后的芬兰初创公司已融资 380 万欧元，加上其他 forge 项目主动寻求互通，说明去中心化代码协作正在从理念走向有资金支持的生态。 Tangled 的互操作性依赖 AT Protocol 的 lexicon——即定义仓库、issue、pull request 和评论等记录类型的 JSON 模式，团队现已宣布其稳定。一位正在开发竞品 forge 的开发者追问，issue、PR 和评论记录是否已从用户作用域迁移到仓库作用域，这一细节决定了其他服务器能否真正充当与 Tangled 兼容的 “knot” 服务器。

hackernews · zlliang · 10月30日 15:44 · [社区讨论](https://news.ycombinator.com/item?id=50305573)

**背景**: AT Protocol（认证传输协议，简称 atproto）是 Bluesky 背后的开放去中心化协议，它使用 DID 实现可迁移身份、个人数据仓库、lexicon 定义数据结构，并通过独立运营的服务器之间联邦互通。Tangled 将这一架构用于源代码托管：仓库保留在所有者自己控制的服务器上，而社交与协作层（issue、pull request、评论）则在网络间交换。这与 ActivityPub 服务的联邦模式在概念上相似，但 AT Protocol 更强调身份与数据的可迁移性以及全网可发现性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://tangled.org/blog/forge/">The federated code forge · The Tangled Blog</a></li>
<li><a href="https://atproto.com/guides/overview">Protocol Overview - AT Protocol</a></li>
<li><a href="https://atproto.com/guides/lexicon">Lexicons - AT Protocol</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上的讨论整体热情高涨：Tangled 联合创始人亲自答疑，一位用户表示打算把副业项目从自建 Gitea 迁到 Tangled、仅保留 GitHub 用于曝光，另有一位 juju.bi 开发者称希望自家 forge 与 Tangled 互通。也有人提出具体界面批评，认为首页时间线内容过于杂乱，并建议个人主页的活动图表改用 GitHub/GitLab 那种用户熟悉的方格热力图。

**标签**: `#federated-code-forge`, `#at-protocol`, `#git`, `#decentralization`, `#code-collaboration`

---

<a id="item-5"></a>
## [研究者披露 Azure 中五个可完全跨租户入侵的漏洞链](https://www.binarysecurity.no/posts/2026/10/one-root-case) ⭐️ 8.0/10

一位安全研究者在 binarysecurity.no 上发表文章，记录了五个不同的漏洞链，每一条都能在微软 Azure 中实现完整的跨租户入侵。这篇题为《Azure's Weakest Link – Five Full Cross-Tenant Compromises》的文章指出，这些攻击链由 Azure 共享多租户服务中长期存在的缺陷类型构成，例如路径遍历（path traversal）和不安全的直接对象引用（IDOR）。 跨租户入侵打破了企业在将工作负载迁移到公有云时所默认的隔离保证，这意味着无论某个客户如何谨慎地配置自己的租户，都可能被牵连暴露。此次披露延续了 Azure 租户隔离问题频发的模式，可能促使微软与企业客户重新审视他们对多租户边界的信任程度。 根据社区评论，这些漏洞的底层类型——路径遍历与 IDOR——很可能自相关功能上线之初就已存在，而研究者建议在资源名称中加入随机性，说明这些标识符可能是可猜测的。提供的材料中未列出 CVE 编号或修复时间表，因此每条攻击链目前的修复状态尚不明确。

hackernews · swq115 · 10月30日 10:06 · [社区讨论](https://news.ycombinator.com/item?id=50301854)

**背景**: Azure 是微软的公有云平台，众多不同组织的工作负载运行在共享基础设施之上；每个组织占据一个“租户”，即相互隔离的目录与账户边界。多租户隔离依靠访问控制检查来实现，这些检查会把每个请求限定到某个租户 ID，因此一旦这类检查存在缺陷——例如 IDOR 或路径遍历漏洞——某个租户就可能触及其他租户的数据或密钥。此类漏洞之所以被视为严重，是因为利用它无需受害者做任何操作，并且可以绕过客户侧的安全防护。此外，Azure AD（Entra ID）的 OAuth 授权同意流程也一直是攻击者反复瞄准的目标，常被用来诱骗用户授权访问其组织的数据。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://news.ycombinator.com/item?id=50301854">Azure 's Weakest Link – Five Full Cross - Tenant Compromises</a></li>
<li><a href="https://cloudsecurityalliance.org/blog/2024/03/15/defend-against-azure-cross-tenant-synchronization-attacks">Defend from Azure Cross - Tenant Synchronization Attacks | CSA</a></li>

</ul>
</details>

**社区讨论**: Hacker News 的评论者既表示钦佩，也提出了尖锐批评：有人称这位研究者是“Azure 开发者的噩梦”，也有人认为 Azure 在跨租户泄露的数量上“远超竞争对手”，并质疑企业为何仍纷纷迁往该平台。一位评论者还指出 login.microsoftonline.com 的 adminconsent 回调中存在一个疑似未修复的相关问题——当攻击者知道另一客户的租户 ID 时该回调可被伪造；其他人则把根本原因归结为路径遍历与 IDOR，认为它们很可能随功能一同发布就已存在。

**标签**: `#cloud-security`, `#azure`, `#vulnerability-research`, `#multi-tenancy`, `#access-control`

---

<a id="item-6"></a>
## [有观点认为：AI 不是在取代 SRE，而是在让其“技能退化”](https://newsletter.signoz.io/p/ai-isnt-replacing-sres-its-deskilling) ⭐️ 8.0/10

SigNoz 通讯的一篇文章提出，AI 智能体并没有取代站点可靠性工程师（SRE），而是在逐步让他们“技能退化”；文章建议 SRE 团队借鉴航空业的做法，把某些事故（即便是 AI 也能处理的）专门保留为人类练习的机会。该文在 Hacker News 上引发热议，获得约 538 分和 404 条评论，讨论围绕自动化、理解能力与可靠性文化展开。 “技能退化”这一视角把讨论从老生常谈的“AI 会不会抢走 SRE 的工作”转向一个更隐蔽的风险：当自动化在从未见过的新型故障中失效时，团队恰恰可能失去那种动手排查的能力。事故响应本身就是复杂分布式系统组织知识的形成与传承过程，因此当下人类与智能体之间的分工方式，将影响未来数年的系统可靠性。 文章的核心类比是美国联邦航空管理局（FAA）要求飞行员即使自动驾驶完全可靠也必须累积手动飞行时间，并据此建议 SRE 团队同样把某些事故指定为人类练习机会。该论述更像是一种规范性的文化主张，并未给出 SRE 团队技能退化的实测数据，也没有说明在不增加风险与值班负担的前提下，这些“练习性事故”该如何挑选。

hackernews · dorianniemiec · 10月30日 15:52 · [社区讨论](https://news.ycombinator.com/item?id=50305693)

**背景**: 站点可靠性工程（SRE）是用软件工程方法来运维生产系统的实践：把运维工作自动化，并通过服务水平指标与目标（SLI/SLO）以及错误预算来衡量可靠性。“技能退化”则是一个早于 AI 数十年的概念，在自动驾驶仪普及后的航空业和 GPS 普及后的导航领域都有记录：当系统代替人完成任务时，原本熟练的技能会可测量地衰退。这场讨论还涉及可观测性（observability），即通过系统的外部输出来推断其内部状态的能力，它比针对已知故障模式盯仪表盘的监控更为宽泛。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Site_reliability_engineering">Site reliability engineering - Wikipedia</a></li>
<li><a href="https://www.sciencedirect.com/topics/social-sciences/deskilling">Deskilling - an overview | ScienceDirect Topics</a></li>
<li><a href="https://terencekok.com/glossary/deskilling/">Deskilling | AI Glossary - Terence Kok</a></li>

</ul>
</details>

**社区讨论**: 评论者普遍认同航空业类比很贴切，但对“技能退化”是否构成真正问题存在分歧。一位在初创公司工作的工程师表示，AI 智能体现在在“使用计算机”方面已超越人类，排查 AWS 问题的速度约是手动翻日志、查路由表的十倍；另一位则坚持认为 SRE 的本质在于理解数据流、瓶颈以及如何缓解故障，而 AI 生成的应用根本提供不了这种理解。还有人反驳说，Terraform 早已让基础设施配置“技能退化”，更好的应对方式是持续改进工具，并推动所有人把可靠性做到五个 9。

**标签**: `#SRE`, `#AI automation`, `#deskilling`, `#observability`, `#software engineering`

---

<a id="item-7"></a>
## [Soft-MTP：一行梯度修改让多 Token 预测真正发挥作用](https://www.reddit.com/r/MachineLearning/comments/1xjnz40/multitoken_prediction_done_right_r/) ⭐️ 8.0/10

一篇新论文提出了 Soft-MTP，只需对训练梯度做一行修改（h_ntp += h_mtp.detach() - h_mtp），就能把标准多 Token 预测（MTP）梯度中隐藏的 KL 自蒸馏信号单独提取出来，同时剔除其中的噪声残差项。作者称这一“免费午餐”式改动在多项任务上改善了 MTP，效果覆盖从 1.67 亿到 120 亿参数规模，并已开源代码、arXiv 论文和 HuggingFace 模型集合。 多 Token 预测已成为前沿大模型预训练流程中的标准配置，很大原因是额外的预测头可以复用为投机解码的草稿头。这样一个几乎零成本的改动既能提升下一 Token 预测质量，又能让这些草稿头更有用，因此对任何从事大模型预训练或推理服务的人都直接相关。 该方法不引入新参数，也不产生额外 logits，作者表示它仍兼容融合算子（fused kernel），因此几乎可以零成本地嵌入现有 MTP 训练代码。论文分析认为，标准 MTP 表现不稳定甚至有害，原因在于一个信噪比很低的残差梯度分量掩盖了有用的 KL 信号，而且这一问题会随着模型规模增大而加剧。

reddit · r/MachineLearning · /u/jayden_teoh_ · 10月30日 18:53

**背景**: 多 Token 预测（MTP）是一种辅助预训练目标，让模型一次预测未来若干个 Token，而不仅仅是紧邻的下一个 Token，从而在一定程度上放松了标准下一 Token 预测中严格的教师强制（teacher forcing）。由于 MTP 会产生额外的预测头来提出候选 Token，它也被用来为投机解码提供草稿头；投机解码是一种推理加速技术，由小模型或草稿模型预先提出若干 Token，再由更大的目标模型并行验证，通常能在不改变输出质量的前提下把生成速度提升 20% 至 50%。Soft-MTP 的核心思想来自自蒸馏：KL 项会把每个 MTP 头的分布拉向模型自身的下一 Token 预测分布，而所提出的技巧通过共享的线性输出头进行梯度路由，从而精确地恢复出这一 KL 梯度。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://aitop.news/item/51133">Soft-MTP Fixes Multi-Token Prediction Training via KL ...</a></li>
<li><a href="https://www.aimodeling.com/en/news/slug/soft-mtp-kl-gradient-recovery">MIT Fixes MTP: One Line Filters Out Its Noisy 80% Gradient</a></li>
<li><a href="https://aiweekly.co/alerts/soft-mtp-one-line-fix-outperforms-standard-mtp-from-167m-to-12b">Soft-MTP: one-line fix outperforms standard MTP from 167M to ...</a></li>

</ul>
</details>

**标签**: `#Multi-Token Prediction`, `#Speculative Decoding`, `#Self-Distillation`, `#LLM Pretraining`, `#Machine Learning`

---

<a id="item-8"></a>
## [DeepSeek 二轮融资约 1055 亿元，估值突破 6155 亿元](https://www.theinformation.com/articles/behind-deepseeks-16-billion-funding-chinese-tech-titans-state-players) ⭐️ 8.0/10

据 The Information 披露，DeepSeek 已完成第二轮融资，规模约 1055 亿元人民币（约合 150 亿美元），估值突破 6155 亿元人民币，参与投资方接近 30 家。其中腾讯出资 100 亿元，宁德时代及董事长曾毓群合计出资 100 亿元，投资名单还包括长鑫存储、中芯国际、美团、vivo 和小红书。 本轮融资是中国大模型公司迄今规模最大的私募融资之一，进一步巩固了 DeepSeek 作为前沿厂商的地位；而国资背景资金占比从约 2% 跃升至约 27%，说明政府相关资本正大举押注本土基础模型龙头。长鑫存储（DRAM 厂商）与中芯国际（晶圆代工）作为战略投资方入局，也把 DeepSeek 的算力与存储供应同国产半导体产业链直接绑定。 首轮融资于今年 6 月完成，规模约 510 亿元，国资背景投资者仅占 2%，因此本轮规模约为上一轮的两倍，且资金来源明显向政府支持资本倾斜。披露的投资方多为产业战略投资者——互联网平台、电池厂商、存储厂商与晶圆代工厂——而非传统财务型风投；6155 亿元估值来自媒体报道，尚未得到公司方面的独立确认。

telegram · zaihuapd · 10月30日 12:37

**背景**: DeepSeek 是一家总部位于杭州的基础模型公司，成立于 2023 年，因陆续发布 DeepSeek-V3、DeepSeek-R1 等开放权重模型而广为人知，官方称其训练与推理成本远低于同级别的美国系统。训练和运行大模型需要海量 GPU 算力以及高带宽内存，这正是长鑫存储这类存储厂商和中芯国际这类代工厂具有战略意义的原因。长鑫存储是中国领先的国产 DRAM 制造商，中芯国际则是中国大陆规模最大、技术最先进的晶圆代工企业，工艺覆盖从 0.35 微米到 14 纳米及更先进节点。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://bianews.com/news/details?id=204884">关于 DeepSeek ，你需要知道的8件事</a></li>
<li><a href="https://zh.wikipedia.org/wiki/中芯国际">中芯国际 - 维基百科，自由的百科全书</a></li>
<li><a href="https://m.163.com/dy/article/L3M01FQ105118AEL.html">长 鑫 存 储 对苹果说“不”：谁稀缺，谁有话语权？| dram ...</a></li>

</ul>
</details>

**标签**: `#DeepSeek`, `#AI funding`, `#China tech`, `#LLM industry`, `#venture capital`

---