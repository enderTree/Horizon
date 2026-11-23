---
layout: default
title: "Horizon Summary: 2026-11-23 (ZH)"
date: 2026-11-23
lang: zh
---

> 从 28 条内容中筛选出 6 条重要资讯。

---

1. [Baez 分析 Masullo 的黎曼猜想证明主张与署名争议](#item-1) ⭐️ 8.0/10
2. [GL.iNet 云服务漏洞被利用，路由器与 KVM 设备遭恶意软件感染](#item-2) ⭐️ 8.0/10
3. [OpenAI 发文探讨困惑度与模型智能的关系，引发热议](#item-3) ⭐️ 8.0/10
4. [Tim O'Reilly 称硅谷已偏离人类福祉，只优化企业利润](#item-4) ⭐️ 8.0/10
5. [Masullo 黎曼猜想证明的 Lean 形式化进度图引发争议](#item-5) ⭐️ 8.0/10
6. [Z.ai 发布 GLM-5.3-Flash：320B 参数原生多模态模型，激活仅 18B，价格降至上代十分之一](#item-6) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Baez 分析 Masullo 的黎曼猜想证明主张与署名争议](https://johncarlosbaez.wordpress.com/2026/11/22/masullo-on-the-riemann-hypothesis/) ⭐️ 8.0/10

John Carlos Baez 发表了一篇复盘文章，审视 Alessandro Masullo 提出的广义黎曼猜想证明及其来龙去脉，包括美国数学会主席 Ravi Vakil 于 2026 年 11 月 20 日匆忙发出、呼吁数学家审阅该证明的公告。Baez 明确提醒自己并非数论专家，其分析只是初步判断。 黎曼猜想或其推广的证明主张是数学界风险最高的事件之一，因此这一案例检验了数学界如何处理验证、优先权和公开宣布。它还牵涉到一场日益激烈的争论：AI 辅助的 Lean 形式化验证能否在不产生通常推动数学发展的概念性洞见的情况下确认结果。 据一份配套综述介绍，Masullo 的文稿在 Weil、Connes 和 Meyer 的传统中，借助 GL1 上的泛函分析给出一个迹公式；另一篇说明则称这是经过 Brian Conrad 数月审查的人工草稿，而同一天还出现了另一个由 Claude 辅助的 Lean 工件。Baez 的保留意见和 HN 讨论都表明，非正式审阅、形式化验证与功劳归属是三个不同的问题。

hackernews · xiaoyu2006 · 11月22日 10:59 · [社区讨论](https://news.ycombinator.com/item?id=50598441)

**背景**: 黎曼猜想断言黎曼 ζ 函数的所有非平凡零点实部都为 1/2；广义黎曼猜想则把类似的零点位置陈述推广到更广泛的一类 L 函数。若得证，将解决一个已有一百五十多年历史、对素数分布有深远影响的问题。Lean 是一种交互式定理证明器，其编译器会逐步检查证明，因此一旦陈述和公理可信，经 Lean 验证的证明在机械意义上是可靠的；AI 系统正越来越多地生成此类形式化证明，但数学家仍在争论它们是否带来真正的理解。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.arpaia.io/files/mathematics/riemann-hypothesis-masullo.pdf">Alessandro Masullo’s Proof of the Riemann Hypothesis</a></li>
<li><a href="https://explainx.ai/blog/alessandro-masullo-grh-human-proof-claimed-vs-verified-november-2026">Masullo GRH Draft: What Vakil Announced (Nov 20) - explainx.ai</a></li>
<li><a href="https://www.science.org/doi/10.1126/science.aej2213">Advancing mathematics research with AI-driven formal proof ...</a></li>

</ul>
</details>

**社区讨论**: HN 评论者担心，Masullo 十二年的努力可能因这场争议而被“贬值”；也有人认为，AI 驱动的暴力验证几乎产生不了新的数学洞见。还有一派反对“被抢发”的叙事，坚持认为如果 Masullo 在没有 AI 辅助的情况下证明了结果，他和 Alpöge 都应获得功劳，而不应把优先权当成赢家通吃的竞赛。

**标签**: `#mathematics`, `#Riemann-Hypothesis`, `#proof-verification`, `#research-culture`, `#AI-in-math`

---

<a id="item-2"></a>
## [GL.iNet 云服务漏洞被利用，路由器与 KVM 设备遭恶意软件感染](https://www.gl-inet.com/en-us/blogs/blog/glinet-security-notice-2026-11-20) ⭐️ 8.0/10

2026 年 11 月 20 日，GL.iNet 披露其云远程管理服务中存在一个安全漏洞，未经授权的攻击者利用该漏洞访问了部分 GL.iNet 路由器与 KVM 设备并在其上安装了恶意软件。厂商已在官网和论坛发布正式安全公告，BleepingComputer 随后对此进行了报道。 GL.iNet 设备在家庭实验室用户、差旅人士和小型企业中颇受欢迎，而此次入侵是通过厂商自有的云管理通道实现的，这暴露出默认回连云端的网络设备所面临的系统性风险。任何使用受影响路由器或 KVM over IP 设备的用户都应假定设备可能已被攻陷并进行排查。 公告称仅有一部分路由器和 KVM 设备通过云远程管理服务受到影响，但并未明确说明禁用云管理功能的设备是否安全，用户只能推断仅本地运行可避开该攻击路径。受影响的用户被建议查阅 GL.iNet 官方公告和论坛帖子以获取修复指引和固件更新。

hackernews · gregsadetsky · 11月22日 23:06 · [社区讨论](https://news.ycombinator.com/item?id=50604988)

**背景**: GL.iNet 生产便携旅行路由器、家用路由器和 KVM-over-IP 设备，出厂搭载基于 OpenWrt 定制的固件，并与公司的 GoodCloud 远程管理平台集成，使用户可以随时随地访问自己的设备。这些设备中有很多也获得上游 OpenWrt 的良好支持，因此用户可以完全替换厂商固件。云端远程管理虽然方便，但扩大了攻击面——厂商服务中的一个漏洞就可能被用来向所有已注册设备推送恶意代码。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.gl-inet.com/en-us/blogs/blog/glinet-security-notice-2026-11-20">GL.iNet Security Notice 2026-11-20</a></li>
<li><a href="https://forum.gl-inet.com/t/2026-11-20-gl-inet-security-notice-goodcloud-kvm-routers/73056">2026-11-20: GL.iNet Security Notice - GoodCloud / KVM / Routers</a></li>
<li><a href="https://www.bleepingcomputer.com/news/security/hackers-exploit-glinet-cloud-flaw-to-infect-routers-kvm-devices/">Hackers exploit GL.iNet cloud flaw to infect routers, KVM devices</a></li>

</ul>
</details>

**社区讨论**: 评论者对联网云设备持强烈批评态度，多人呼吁用户刷入 OpenWrt 或自建 DIY 路由器，并始终关闭此类设备的云/远程访问功能，还将其与 Ubiquiti 设备出现的远程访问问题相提并论。一位评论者贴出 GL.iNet 论坛帖子，暗示这些设备可能至少从去年起就已被攻陷；另一位评论者指出 OpenWrt 支持覆盖了许多 GL.iNet 路由器，但不包括 KVM 设备，这尤其令人担忧。

**标签**: `#security`, `#networking`, `#routers`, `#GL.iNet`, `#OpenWrt`

---

<a id="item-3"></a>
## [OpenAI 发文探讨困惑度与模型智能的关系，引发热议](https://openai.com/index/perplexity-and-intelligence/) ⭐️ 8.0/10

OpenAI 发布了一篇题为《Perplexity and Intelligence》的新文章，探讨困惑度（即模型预测下一个 token 时的"惊讶程度"）与模型能力之间的关联。该文在 Hacker News 上引发大量讨论（约 550 分、373 条评论），有读者指出，从近期模型来看，对数困惑度与基准测试表现之间呈现出相当清晰的趋势线。 如果像困惑度这样一个计算成本低廉的预训练指标能够可靠地预测下游能力，那么日益碎片化、运行成本高昂的基准测试体系就可能被大大简化。这也让"更好的预测等于更好的压缩、更好的压缩等于更高的智能"这一经典信息论观点重新回到台面，而这一观点深刻影响着各家实验室对扩展规律与评估方式的思考。 困惑度的取值范围介于 1（完美预测，因为它是指数化的交叉熵）与词表大小（均匀随机预测器）之间，据称文章将各代模型的对数困惑度与能力水平作了对照绘制。讨论中还提出了一个悬而未决的问题：以交叉熵之外的目标进行优化的强化学习后训练，是否仍会让预训练阶段呈现的这一趋势保持不变。

hackernews · acossta · 11月22日 17:06 · [社区讨论](https://news.ycombinator.com/item?id=50601525)

**背景**: 困惑度是信息论中衡量概率模型预测样本好坏的标准指标；在语言建模中，它是每个 token 平均交叉熵的指数化结果，数值越低意味着模型给真实文本分配的概率越高。在 Transformer 出现之前以及早期大模型时代，它是最主要的衡量标准，但在对外发布中已基本被 MMLU、编程与数学评测等任务型基准所取代，部分原因是困惑度高度依赖于分词器和评测语料。"压缩即智能"的观点可追溯到 Jürgen Schmidhuber 等人，他们主张对原始数据流进行预测/压缩的进步，正是好奇心、创造力与学习能力的根基。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Perplexity">Perplexity - Wikipedia</a></li>
<li><a href="https://mbrenndoerfer.com/writing/perplexity-language-model-evaluation-metric">Perplexity : The Standard Language Model Metric - Interactive</a></li>
<li><a href="https://arxiv.org/abs/0812.4360">[0812.4360] Driven by Compression Progress: A Simple Principle...</a></li>

</ul>
</details>

**社区讨论**: 评论者总体热情颇高，但也对文章的表述提出了挑剔：有人指出文章通篇并未真正定义困惑度，并自行给出定义（最好情况为 1，最坏情况为词表大小）；另有人表示，在训练重心转向强化学习的背景下，交叉熵趋势依然如此清晰令人"震惊"，并乐见这样一个简单基准取代日益复杂的评测。还有人援引压缩理论支持该观点——其中一位提到自己 2008 年的论文早已提出同样论点——另有一位评论者称微软的 Mustafa Suleyman 发帖表示其 MAI-2 Base 模型将在 OpenAI 的留出评测集上报告结果，引来不少质疑与调侃。

**标签**: `#LLMs`, `#perplexity`, `#AI evaluation`, `#machine learning`, `#compression`

---

<a id="item-4"></a>
## [Tim O'Reilly 称硅谷已偏离人类福祉，只优化企业利润](https://www.oreilly.com/radar/what-happened-to-silicon-valley/) ⭐️ 8.0/10

在 O'Reilly Radar 发表的新文章《What Happened to Silicon Valley?》中，Tim O'Reilly 指出科技行业已从关注人类福祉转向优化股东价值，并呼吁运用“机制设计”（他称之为“逆向博弈论”）来重新设计塑造技术的激励体系。他把核心问题表述为“我们本应玩的是哪一场游戏？”，而不是被动接受当下游戏的规则。 这篇文章出自业内最具影响力的出版人之一，对风险投资与股东价值激励如何塑造数十亿人使用的产品提出了实质性批评。在 AI 驱动的巨额投入与行业整合引发“仅靠市场激励能否让技术走向社会期望方向”质疑的当下，这一观点尤其引发共鸣。 O'Reilly 的提议依托于机制设计——这一经济学与博弈论分支研究如何在参与者私人偏好未知的情况下构造出能产生良好结果的规则，该领域曾获 2007 年诺贝尔经济学奖，并已被用于广告拍卖与互联网路由。需要注意的是，这更像是一种规范性的行动呼吁而非具体政策蓝图，而且文章的核心观点被放在结尾而非开头。

hackernews · greenyouse · 11月22日 19:20 · [社区讨论](https://news.ycombinator.com/item?id=50602947)

**背景**: 机制设计常被称为“逆向博弈论”：它不是分析既定规则会产生什么结果，而是从期望的结果出发，反向寻找能激励参与者达成该结果的规则。它支撑着现代互联网经济的诸多部分，从 Google 和 Facebook 的广告拍卖到互联网域间路由。O'Reilly 的论点在于，科技行业隐含的“机制”——最大化股东价值与风险投资回报——从来不是为人类福祉而刻意选择的，因此它可以被重新设计。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Mechanism_design">Mechanism design - Wikipedia</a></li>
<li><a href="https://www.web.stanford.edu/~jacksonm/mechtheo.pdf">Mechanism Theory - Stanford University</a></li>

</ul>
</details>

**社区讨论**: Hacker News 的评论者大多认同 O'Reilly 的观点，不少人称赞文章结尾处关于机制设计的论述是最有价值的洞见。也有人聚焦于近因：一位评论者认为零利率时代让企业膨胀到畸形规模，并促使初创公司投向投机性的“新大陆”；还有人感叹华尔街式人物与自我推销的“VC 网红”侵蚀了硅谷仅存的操守。

**标签**: `#silicon-valley`, `#tech-industry`, `#mechanism-design`, `#capitalism`, `#venture-capital`

---

<a id="item-5"></a>
## [Masullo 黎曼猜想证明的 Lean 形式化进度图引发争议](https://claude.ai/artifact/CtQyX8qfYAF822bgHJHHE3) ⭐️ 8.0/10

一份追踪 Alessandro Masullo 所声称的广义黎曼猜想证明在 Lean 中形式化进度的公开进度图，在 Hacker News 上引发了热烈讨论（208 分、157 条评论）。该仓库由多位数学研究者共同参与，还附有一份包含数百个未决问题的勘误列表；评论者就这一工作究竟是真正的突破，还是在追查一个存在致命漏洞的证明展开了争论。 这一事件是检验形式化验证与 AI 辅助数学如何应对“惊人主张”的实时案例：社区不再被动等待同行评审，而是同时把论证机械化并在公开场合对其进行审计。对于关注基于 Lean 的证明工程、自动定理证明，以及重大成果的可信度如何在公开环境中被确立的人来说，这件事意义重大。 进度图上的高百分比并不意味着证明大体正确，因为一个未填补的漏洞就可能让后续所有环节失效；贡献者明确提醒，目前判断核心思路是否存在大洞还为时过早。评论者还援引报道称：代表 Masullo 发布该工作的 Ravi Vakil 表示自己并未审阅过这份文稿，Brian Conrad 认为手稿需要“重大修订”，而 Masullo 除此之外没有任何其他发表记录。

hackernews · Qision · 11月22日 23:12 · [社区讨论](https://news.ycombinator.com/item?id=50605045)

**背景**: Lean 是一款交互式定理证明器，同时也是依值类型（dependent type）编程语言；数学命题及其证明以代码形式书写，由计算机逐步机械地检查，Google DeepMind 构建数学推理系统 AlphaProof 时也使用了 Lean。黎曼猜想及其推广形式广义黎曼猜想（GRH）是数学中最著名的未解难题之一，据报道 Masullo 的草稿长达约 940 页。所谓“形式化”这样的证明，就是把其中的论证转写为 Lean 的定义与引理，使任何漏洞都变成编译错误，而不是隐蔽的疏漏。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Lean_(proof_assistant)">Lean (proof assistant) - Wikipedia</a></li>
<li><a href="https://www.arpaia.io/files/mathematics/riemann-hypothesis-masullo.pdf">Alessandro Masullo's Proof of the Riemann Hypothesis</a></li>
<li><a href="https://xenospectrum.com/en/masullo-riemann-proof-draft-release/">Draft Proof of the Generalized Riemann Hypothesis, 12 Years ...</a></li>

</ul>
</details>

**社区讨论**: 一位参与该仓库的数学家在评论中请读者不要过度解读那数百条勘误，称其中有轻有重，但判断核心思路是否存在大洞仍为时过早。其他人则警告进度条不能作为正确性的证据，有评论者认为所用机器比另一条近期路线更像是一小步而非重大飞跃；也有评论者对基于智能体的大语言模型 AI 表达了沮丧，认为它让数学对聪明、受过教育的人而言变成了一个不那么有趣的地方。

**标签**: `#formal-verification`, `#Lean`, `#mathematics`, `#Riemann-hypothesis`, `#AI-assisted-research`

---

<a id="item-6"></a>
## [Z.ai 发布 GLM-5.3-Flash：320B 参数原生多模态模型，激活仅 18B，价格降至上代十分之一](https://t.me/zaihuapd/45309) ⭐️ 8.0/10

Z.ai 发布了 GLM-5 系列首个原生多模态模型 GLM-5.3-Flash，总参数 320B，但每次推理仅激活 18B 参数。官方称其在多项编程与智能体基准上超过 GLM-5.2、接近 Claude Opus 4.8，同时把 API 价格降到约上代的十分之一：限时优惠期间每百万 Tokens 输入 0.075 美元、缓存输入 0.015 美元、输出 0.25 美元，缓存存储暂时免费。 这次发布把大参数稀疏模型与大幅降价结合在一起，有望让具备多模态能力的智能体模型进入此前因成本过高而无法承担的高频编程与工具调用场景。如果基准成绩能经得起独立测试验证，将进一步加剧中国大模型厂商之间的价格战，并为开发者提供比西方前沿模型更便宜的替代方案。 320B 总参数、18B 激活参数的组合意味着它采用混合专家（MoE）架构，因此单 Token 的计算成本取决于 18B 的激活路径而非完整模型规模。文中价格属于限时优惠价，之后会恢复原价；同时所有性能说法目前均来自 Z.ai 自己的发布声明，尚未公布评测方法，也没有第三方验证。

telegram · zaihuapd · 11月23日 04:47

**背景**: 混合专家（MoE）模型保留规模很大的参数池，但每个 Token 只经过其中一小部分专家，因此 320B 的模型可以按接近 18B 稠密模型的成本运行。“原生多模态”指的是模型从预训练阶段就在统一架构下同时学习文本、图像等模态，而不是在已有语言模型上外挂一个视觉编码器。此外，主流大模型 API 通常对命中缓存的输入 Token 打折计费，因为重复的提示前缀可以复用而不必重新计算，所以厂商会单独列出缓存命中价格。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://gate.ai/zh/blog/dense-model-vs.-moe-model-what-are-the-differences-in-model-architecture">Dense Model vs MoE Model： 模 型 架构有 什 么 区别？｜Gate.AI</a></li>
<li><a href="https://zhuanlan.zhihu.com/p/2036759233539077945">原生多模态模型技术全景 - 知乎 - 知乎专栏</a></li>
<li><a href="https://juejin.cn/post/7678132532524810240">DeepSeek 涨 价 了，你换了吗？— — 大 模 型 API ...</a></li>

</ul>
</details>

**标签**: `#LLM`, `#GLM-5.3-Flash`, `#multimodal`, `#model release`, `#API pricing`

---