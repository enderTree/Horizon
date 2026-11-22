---
layout: default
title: "Horizon Summary: 2026-11-22 (ZH)"
date: 2026-11-22
lang: zh
---

> 从 24 条内容中筛选出 8 条重要资讯。

---

1. [Lean 社区宣布对（广义）黎曼猜想完成形式化验证](#item-1) ⭐️ 9.0/10
2. [浙江大学在超导芯片上首次真机实现量子随机存储器](#item-2) ⭐️ 9.0/10
3. [GnuPG 就 GPGME 双重释放漏洞发布安全公告](#item-3) ⭐️ 8.0/10
4. [微软发布 RDMA over USB4 预览版，多台 PC 可合跑一个本地 AI 模型](#item-4) ⭐️ 8.0/10
5. [OpenRouter 警告 MiniMax 模型提示词疑遭第三方读取](#item-5) ⭐️ 8.0/10
6. [口服 daraxonrasib 联合化疗：一线胰腺癌确认缓解率达 60.7%](#item-6) ⭐️ 8.0/10
7. [特斯拉海外开始推送 FSD v15，带来全新 Reality View](#item-7) ⭐️ 8.0/10
8. [美商务部将定稿新规，封堵中国 AI 公司远程使用境外芯片](#item-8) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Lean 社区宣布对（广义）黎曼猜想完成形式化验证](https://leanprover-community.github.io/blog/posts/riemann-hypothesis/) ⭐️ 9.0/10

Lean 证明器社区发布博客文章，宣布完成了对黎曼猜想的形式化验证——看起来是广义黎曼猜想（GRH）——该工作由 Claude 提供大量 AI 辅助、并由人类专家（据称是一位名为 Levent 的合作者）指导完成。这一声明在 Hacker News 上引发大规模讨论（931 分、791 条评论），聚焦于证明是如何被检验的，以及过程中究竟形式化了多少现代数学。 如果这一结果站得住脚，那么机器检验的 GRH 证明将是解析数论与形式化验证两大领域的里程碑，因为 GRH 蕴含算术级数中素数的强分布界，并支撑了大量现代数论工作。讨论还显示，这项工作可能需要形式化当代数学的一大块内容，因此它对数学基础与 AI 辅助形式化的意义，或许不亚于对猜想本身的意义。 质疑者指出，此前一个针对考拉兹猜想的虚假反证曾骗过某个号称独立的检查器，而且主要内核与一致性检查器（con-leche 与 con-ron）之间的独立性常被夸大。支持者则反驳说，如今一个 bug 必须同时存在于所有内核中、并同时破坏自洽性证明才可能蒙混过关；而且有真正的人类专家参与把关，AI 单凭“钻漏洞”硬闯过去的可能性要低得多。

hackernews · g-b-r · 11月21日 14:36 · [社区讨论](https://news.ycombinator.com/item?id=50589618)

**背景**: Lean 是一个开源证明助手兼函数式编程语言，其中的证明被写成可被一个很小的可信核心（即内核）机械检验的形式，这正是形式化验证的基础。黎曼猜想是数学中最著名的未解难题之一，断言黎曼 zeta 函数的所有非平凡零点都位于临界线上；广义黎曼猜想则把它推广到更广的一类 L 函数，尤其是狄利克雷 L 函数。由于这类证明规模极其庞大，形式化工作通常分散在相互独立的内核与单独验证的检查器上，结果的可信度取决于这些组件是否会彼此独立地出错、而非同时出错。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Generalized_Riemann_hypothesis">Generalized Riemann hypothesis - Wikipedia</a></li>
<li><a href="https://lean-lang.org/learn/">Learn — Lean Lang</a></li>
<li><a href="https://www.anthropic.com/research/formalizing-fermats-last-theorem">Formalizing Fermat's Last Theorem \ Anthropic</a></li>

</ul>
</details>

**社区讨论**: 评论者的态度总体是谨慎乐观：有人认为如今“靠 bug 蒙混过关”的概率已微乎其微，因为需要多个不同语言实现的内核（包括带自洽性证明的 con-leche 与 con-ron）同时出错。也有人提到此前考拉兹猜想虚假反证曾通过某个独立检查器的先例，并高度评价人类合作者 Levent 把 Claude 的潜力发挥到极致；还有人指出，真正的看点或许是为此形式化了多少现代数学。

**标签**: `#formal-verification`, `#lean`, `#riemann-hypothesis`, `#ai-theorem-proving`, `#mathematics`

---

<a id="item-2"></a>
## [浙江大学在超导芯片上首次真机实现量子随机存储器](https://finance.sina.com.cn/stock/2026-11-21/doc-iniznhsk3530826.shtml) ⭐️ 9.0/10

浙江大学团队在自主研制的超导量子芯片“天目 2 号”上，全球首次在真实硬件上实现量子随机存储器（QRAM），4 位和 8 位原型的数据读取准确率分别为 80.9%和 60.4%，成果发表于《自然·物理》。 QRAM 是 Grover 搜索、量子线性代数等量子算法长期寻求的关键组件，此次在真实硬件上实现，使该领域从理论方案向实用量子存储器迈进一步。该工作还为桶旅架构的耐噪声能力提供了实验证据，可能为未来可扩展的 QRAM 设计提供指导。 4 位和 8 位原型分别对应 16 个和 256 个存储单元，团队报告线路深度较未优化方案降低 30% 以上，并首次实验验证了该架构具备局部抗噪特性；不过，8 位数据 60.4% 的读取准确率仍远低于容错应用所需的水平。

telegram · zaihuapd · 11月21日 08:31

**背景**: 量子随机存储器（QRAM）允许量子计算机以处于多个地址叠加态的地址来查询数据，有望以比经典 RAM 少得多的存储资源完成信息读取。大多数方案采用桶旅架构，由地址量子比特通过量子开关树来路由查询，但这类线路深度大且对噪声非常敏感。超导电路是量子计算的主流平台之一，然而受线路深度和保真度限制，在真实硬件上演示 QRAM 一直十分困难。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://news.mydrivers.com/1/1167/1167501.htm">news.mydrivers.com/1/1167/1167501.htm</a></li>
<li><a href="https://github.com/IAI-USTC-Quantum/QRAM-Simulator">GitHub - IAI-USTC-Quantum/ QRAM -Simulator: Efficient quantum...</a></li>

</ul>
</details>

**标签**: `#quantum computing`, `#QRAM`, `#superconducting qubits`, `#quantum memory`, `#research breakthrough`

---

<a id="item-3"></a>
## [GnuPG 就 GPGME 双重释放漏洞发布安全公告](https://lists.gnupg.org/pipermail/gnupg-announce/2026q4/000517.html) ⭐️ 8.0/10

GnuPG 针对 GPGME 发布了一份安全公告，涉及一个双重释放（double-free）漏洞；该漏洞由 Johan Carlsson 发现，并由 GitLab 于 2026-11-12 通知上游。原定于 2026-11-25 进行的协同披露，因 GitLab 需要为无关的 Ruby2Shell 漏洞提前发布更新，而提前至 2026-11-20。 GPGME 是大多数应用程序用来接入 OpenPGP 加密与签名功能的 C 库，因此其中的内存破坏漏洞影响范围远超 GnuPG 命令行工具本身。对支持签名提交的 GitLab 而言尤为敏感——该路径上的代码执行被视为严重后果；社区成员还指出，所有链接 2.3.0 之前版本 GPGME 的软件都受影响，包括邮件客户端、XMPP 客户端、Samba、Flatpak 与 Gpg4win。 评论者强调这只是一个双重释放漏洞，而非现成的远程代码执行链；其中一位指出，常规工具大约五年前就在 Red Hat 的打包中标记过此问题，但上游似乎漏掉了该修复。建议受影响方检查自身捆绑或静态链接的 GPGME 构建；而像 apt 这样不直接使用该库的组件，据报道并不受影响。

hackernews · gdgghhhhh · 11月21日 08:32 · [社区讨论](https://news.ycombinator.com/item?id=50587208)

**背景**: GPGME（GnuPG Made Easy）是一个 C 库，在 GnuPG 之上为应用程序提供加密、解密、签名与密钥管理的高层 API，使开发者无需直接调用 gpg 命令行即可加入 OpenPGP 支持。双重释放是指对同一内存地址两次调用 free()，破坏分配器的内部记录，可能导致崩溃或可被利用的堆破坏。这类缺陷正是业界推动内存安全语言以及对 C/C++ 代码库采用更严格工具链的主要原因之一。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Memory_safety">Memory safety - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: Hacker News 的讨论既有实际排查，也有元层面的争论：有人试图厘清究竟哪些软件真正链接了 GPGME，有人质疑该报告是否通过暗示存在 RCE 链而夸大了严重性，还有人主张在缺乏 Rust 级别工具保障的情况下不应再编写 C/C++。此外，鉴于下游打包似乎比上游早数年发现该漏洞，也有人对披露流程表示怀疑。

**标签**: `#security`, `#GnuPG`, `#GPGME`, `#vulnerability`, `#memory-safety`

---

<a id="item-4"></a>
## [微软发布 RDMA over USB4 预览版，多台 PC 可合跑一个本地 AI 模型](https://videocardz.com/newz/microsoft-brings-rdma-over-usb4-to-windows-allowing-multiple-pcs-to-run-one-local-ai-model) ⭐️ 8.0/10

微软发布了面向 Windows 的 RDMA over USB4 开发者预览版，多台 PC 可以用普通 USB4 线缆互联，共享内存与 GPU 算力，共同运行同一个本地 AI 大模型，而无需专用网卡或交换机。演示中三台搭载 AMD Ryzen AI Max+ 395 的机器以 4-bit 量化联合运行 Qwen3-235B-A22B，速度约为每秒 18.5 个 token，该功能将通过 Windows Insider 推送。 这让普通消费级 PC 借助用户已有的接口和线缆组成小型推理集群，大幅降低了运行远超单机容量的大模型的门槛。对于希望在不依赖云端和数据中心硬件的前提下获得大模型能力的爱好者、小型工作室和隐私敏感团队而言，这可能重塑本地 AI 的工作方式。 该预览版通过标准 USB4 链路通信，因而不需要传统 RDMA 所依赖的专用网卡和交换机，微软将其定位为经由 Windows Insider 推送的开发者预览而非成品功能。演示将三台 Ryzen AI Max+ 395 主机与 4-bit 量化的 Qwen3-235B-A22B 混合专家模型搭配，该模型总参数 2350 亿但每个 token 仅激活约 220 亿参数，使跨设备池化后的计算负担更可控。

telegram · zaihuapd · 11月21日 06:13

**背景**: RDMA（远程直接内存访问）允许一台机器直接读写另一台机器的内存，绕过 CPU 和操作系统网络栈，过去通常需要数据中心里的 InfiniBand 或支持 RoCE 的专用网卡。USB4 是面向消费级市场的高速互连标准（较新版本带宽可达 40 Gbps 以上），可以隧道传输 PCIe 和网络流量，因此成为普通笔记本、迷你主机之间实现 RDMA 的可行载体。Qwen3-235B-A22B 是阿里巴巴的旗舰开源混合专家模型，总参数 2350 亿、激活参数 220 亿；4-bit 量化把权重从 FP16 压缩到 INT4，显存占用可减少约 75%，从而让这种规模的模型得以拆分到多台机器的内存与显存中运行。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.geekfan.net/news/1120313205.html">微软推出 USB4 RDMA 多 Win11 协同 AI 方案，多电脑搭积木式合并内存...</a></li>
<li><a href="https://news.qq.com/rain/a/20261122A05M1M00">不用交换机！微软Windows11上线USB4 RDMA：多机合体做AI推理</a></li>
<li><a href="https://baike.baidu.com/item/Qwen3-235B-A22B/67420648">Qwen3-235B-A22B_百度百科</a></li>

</ul>
</details>

**标签**: `#RDMA`, `#USB4`, `#local-llm-inference`, `#distributed-systems`, `#microsoft-windows`

---

<a id="item-5"></a>
## [OpenRouter 警告 MiniMax 模型提示词疑遭第三方读取](https://news.ycombinator.com/item?id=50585962) ⭐️ 8.0/10

OpenRouter 通过邮件通知用户，发往 MiniMax 模型的提示词内容可能已被第三方读取：一名安全研究者在 2026 年 7 月至 10 月间向这些模型提交了嵌入唯一「金丝雀」URL 的提示词，结果发现第三方在 40 到 130 小时后访问了这些 URL。OpenRouter 将问题归因于 MiniMax 及其转发方 AtlasCloud、Novita 和 StreamLake，已下架受影响端点的「零数据保留」标签，并建议曾暴露敏感凭证的用户更换 API Key 和密码。 这一事件动摇了 API 路由层的核心承诺：即单一网关能够为其背后每一个模型和转发方的数据处理行为背书。通过托管 LLM API 发送敏感提示词的开发者，尤其是那些依赖「零数据保留」标签满足合规要求的团队，今后需要把这类标签当作待验证的声明，而非可靠保证。 证据来自「金丝雀」URL——为每条提示词生成唯一链接，通过访问日志即可判断是否有他人在何时读取了内容；这些访问发生在响应早已返回之后很久，说明数据被留存并在之后被再次处理，而非仅在请求过程中短暂经过。值得注意的是，报道时 OpenRouter 官网尚未发布相关公告，警告主要通过直接邮件传达给受影响用户。

telegram · zaihuapd · 11月21日 06:53

**背景**: OpenRouter 是一个路由与模型市场层，让开发者通过单一 API 和单一计费账户调用多家提供商的众多模型，这也意味着一条提示词在抵达模型前可能经过多个中间环节。「零数据保留」（ZDR）是提供商的一项承诺：提示词仅在生成响应所需的时间内存在于系统中，随后即被清除，这一承诺往往是企业及合规敏感客户所依赖的。MiniMax 是一家中国大模型厂商，其模型同时也通过 AtlasCloud、Novita、StreamLake 等第三方推理转发服务商提供，因此一次请求可能经过多个运营方，而它们的日志记录做法未必与模型方自身的政策一致。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openrouter.ai/blog/insights/zero-data-retention/">Zero Data Retention (ZDR): What It Means for AI APIs</a></li>
<li><a href="https://platform.kimi.com/docs/guide/zero-data-retention">什么是零数据保留（ZDR）？ - Kimi API 开放平台</a></li>
<li><a href="https://www.streamlake.com/">StreamLake 溪流湖 | 行业领先的AI大 模 型 平台与音视频云 服 务 商</a></li>

</ul>
</details>

**标签**: `#security`, `#privacy`, `#LLM APIs`, `#OpenRouter`, `#data retention`

---

<a id="item-6"></a>
## [口服 daraxonrasib 联合化疗：一线胰腺癌确认缓解率达 60.7%](https://event.eortc.org/ena2026/2026/11/20/metastatic-pancreatic-cancer-responds-well-to-initial-treatment/) ⭐️ 8.0/10

11 月 20 日，在巴塞罗那举行的 EORTC-NCI-AACR（ENA 2026）大会上，研究者以 late-breaking 口头报告形式公布了 I/II 期数据：61 例既往未接受治疗的转移性胰腺导管腺癌患者口服 daraxonrasib 200 mg 每日一次，联合吉西他滨/白蛋白紫杉醇，确认客观缓解率达 60.7%，完全缓解率 8.2%（约十二分之一）。该方案还取得 90.2% 的疾病控制率、12.8 个月的中位无进展生存期，以及在中位随访 18.3 个月时 76.6% 的 12 个月总生存率。 转移性胰腺癌是最致命的实体瘤之一，化疗的历史 1 年生存率区间仅为 22%–48%，因此这一口服靶向药联合化疗的一线方案若能获得验证，其缓解与生存信号有可能实质性地改变治疗范式。这也标志着 RAS 靶向治疗从针对单一突变的 KRAS G12C 药物，扩展到在 KRAS 突变几乎普遍存在的瘤种中采用多选择性泛 RAS 抑制策略。 该研究是单臂 I/II 期试验，没有化疗对照组，主要研究者明确表示疗效对比要靠正在进行的 III 期试验来验证；化疗的 1 年生存参照来自 MPACT 试验（白蛋白紫杉醇联合吉西他滨为 35%）和 mFOLFIRINOX（48%），因此不宜简单宣称「远高于化疗」。机制上，daraxonrasib 是一种口服 RAS(ON) 多选择性抑制剂，通过与亲环素 A 结合作用于活跃态（GTP 结合）RAS，覆盖多种 KRAS/NRAS 突变而非仅针对 G12C；该药已于 8 月 26 日获 FDA 批准，商品名 RASONQUE，用于既往治疗后的患者，依据是 III 期 RMC-302 试验（中位总生存 13.2 个月 vs 6.7 个月）。

telegram · zaihuapd · 11月21日 11:24

**背景**: 胰腺导管腺癌以对多数疗法高度耐药著称，约 90% 的病例携带 KRAS 突变，但第一代 KRAS 药物仅针对 G12C 变异，而该变异在胰腺癌中十分罕见。RAS 蛋白是分子开关，与 GTP 结合时处于「开启」状态，daraxonrasib 属于新一代三复合物抑制剂，借助分子伴侣蛋白亲环素 A 关闭多种 RAS 突变体的活性 GTP 结合形态。MPACT 试验确立了白蛋白紫杉醇联合吉西他滨作为转移性胰腺癌一线标准化疗骨架的地位，其中位总生存约 8.5–8.7 个月，这也是评估这一新联合方案时所参照的基准。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.webmd.com/cancer/pancreatic-cancer/pancreatic-cancer-rasonque">What to Know About Rasonque for Pancreatic Cancer</a></li>
<li><a href="https://physicianresources.dana-farber.org/news/ras-on-inhibitor-daraxonrasib-shows-promising-results-in-advanced-pancreatic-cancer-phase-1/2-study">RAS ( ON ) Inhibitor Daraxonrasib Shows Promising Results in...</a></li>
<li><a href="https://www.drugs.com/rasonque.html">Rasonque ( daraxonrasib ): Uses, Dosage, Side Effects</a></li>

</ul>
</details>

**标签**: `#pancreatic cancer`, `#daraxonrasib`, `#RAS inhibitor`, `#oncology`, `#clinical trial`

---

<a id="item-7"></a>
## [特斯拉海外开始推送 FSD v15，带来全新 Reality View](https://x.com/Tesla/status/2124222447855743019) ⭐️ 8.0/10

特斯拉在 X 上宣布，已开始在海外向车主推送 FSD v15，声称其端到端驾驶网络对安全关键场景的处理能力提升到原来的 25 倍。本次更新还带来了全新的“Tesla Reality View”可视化界面，可在车机屏幕叠加实时摄像头画面与 FSD 的行驶规划，并附带一系列驾驶体验优化。 FSD v15 是特斯拉监督式自动驾驶软件的一次重大版本跃升，若 25 倍的安全性提升能够成立，将是该项目迄今单次版本中最大幅度的改进之一，直接影响车主对系统的信任度与使用频率。全新的生成式可视化界面还表明，特斯拉押注于把神经网络感知结果清晰地呈现给乘客，以此赢得用户与监管机构的认可。 根据网络上流传的更新说明，v15 升级了端到端驾驶网络的每一个部分，并改进了对轮胎、树枝、纸箱等路面障碍物的绕行偏移能力，同时优化了无保护转弯以及学校区域和恶劣天气下的速度控制。Reality View 支持全屏、地图和分屏布局以及安静模式，并在可视化画面中叠加导航转向提示，转向灯提示音也变得更轻柔并逐渐减弱；值得注意的是，25 倍这一数字来自特斯拉官方说法，尚未经过独立验证。

telegram · zaihuapd · 11月22日 00:03

**背景**: 特斯拉的 Full Self-Driving（FSD）是一套高级驾驶辅助套件，在驾驶员监督下可以处理城市道路和高速公路上的大部分驾驶任务，但它并非完全自动驾驶，特斯拉官方目前也将该版本标注为“Full Self-Driving (Supervised)”。在转向端到端神经网络方案后，特斯拉不再手工编写驾驶规则，而是用单个大型模型把摄像头输入直接映射为驾驶决策，因此 v15 这样的重大版本意味着整个网络被重新训练。特斯拉此前已为 v15 预热多时，马斯克曾承诺新界面将以“令人脑洞大开的方式渲染现实”。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.tesla.com/fsd">Full Self - Driving (Supervised) | Tesla</a></li>
<li><a href="https://www.notateslaapp.com/news/5057/tesla-fsd-v15-coming-next-month-with-holiday-update-musk">Tesla FSD V 15 Arriving Next Month: Home Garage... - Not a Tesla App</a></li>
<li><a href="https://www.youtube.com/watch?v=ur6qSANo_M4">Tesla FSD V 15 Blew My Mind! (First Drive ) - YouTube</a></li>

</ul>
</details>

**标签**: `#Tesla`, `#FSD`, `#autonomous-driving`, `#AI`, `#release`

---

<a id="item-8"></a>
## [美商务部将定稿新规，封堵中国 AI 公司远程使用境外芯片](https://t.me/zaihuapd/45289) ⭐️ 8.0/10

美国商务部正在敲定一项规则，禁止中国 AI 公司通过境外数据中心远程使用先进 AI 芯片，最早可能于本月公布。该管制将在现有半导体出口限制的基础上扩展至马来西亚、新加坡、泰国等七个国家，以封堵远程访问和芯片走私的漏洞；商务部目前仍在与其他政府机构磋商后定稿。 这标志着美国对华技术限制的一次明显升级——管制对象从实体芯片出货转向算力访问本身，可能切断中国 AI 实验室用于训练前沿模型的一条变通路径。此举将直接影响中国 AI 开发者、东南亚的海外数据中心与云服务运营商，以及其硬件支撑了大部分此类远程算力的英伟达。 该规则在跨机构磋商中起草，此前白宫已要求国会立法，责成商务部制定这一规则。据报道，英伟达曾游说反对封堵这一远程访问缺口，理由是美国的 AI 基础设施需要在全球取胜；七个受管制国家的具体范围及执行机制尚未公开确认。

telegram · zaihuapd · 11月22日 04:34

**背景**: 自 2022 年起，美国逐步限制向中国出口高性能 AI 芯片（例如英伟达最先进的加速卡），目的是延缓中国在前沿 AI 与先进计算方面的发展。这些规定管的是硬件的实体出货，却留下一个缺口：中国企业可以租用部署在中国境外数据中心的芯片算力，远程训练模型。已有报道称，包括月之暗面（Moonshot AI）在内的中国实验室曾寻求使用欧洲等地海外设施中的英伟达芯片，而这项新规正是为了封堵该漏洞。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.cnbc.com/2026/11/05/moonshot-ai-nvidia-chips-europe-china.html">China's Moonshot AI sought Nvidia chip access in Europe amid...</a></li>
<li><a href="https://forklog.com/en/china-accesses-nvidia-chips-via-overseas-data-centers/">China Accesses Nvidia Chips via Overseas Data Centers | ForkLog</a></li>
<li><a href="https://forums.hardwarezone.com.sg/threads/us-to-restrict-chinese-remote-access-to-ai-chips-from-southeast-asian-data-centers-report.7231761/">US to restrict Chinese remote access to AI chips from Southeast...</a></li>

</ul>
</details>

**标签**: `#export-controls`, `#AI-chips`, `#US-China-tech`, `#semiconductors`, `#AI-policy`

---