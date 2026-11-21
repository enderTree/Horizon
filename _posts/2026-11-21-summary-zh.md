---
layout: default
title: "Horizon Summary: 2026-11-21 (ZH)"
date: 2026-11-21
lang: zh
---

> 从 34 条内容中筛选出 11 条重要资讯。

---

1. [马苏洛抢在 Anthropic 人工智能声明后数小时仓促公布耗时 12 年的 GRH 证明](#item-1) ⭐️ 9.0/10
2. [Levent Alpöge 宣称证明广义黎曼猜想，并附约 1500 万行 Lean 形式化代码](#item-2) ⭐️ 9.0/10
3. [陶哲轩将无外力纳维-斯托克斯奇点与广义黎曼猜想联系起来](#item-3) ⭐️ 9.0/10
4. [GitHub 仓库声称无外力纳维-斯托克斯方程有限时间爆破](#item-4) ⭐️ 9.0/10
5. [Thinking Machines 发布 Inkling 2 Mini 开放权重循环 Transformer 模型](#item-5) ⭐️ 8.0/10
6. [语言模型无需梯度即可重写自身权重](#item-6) ⭐️ 8.0/10
7. [AI 抛售抹去纳斯达克 2026 年涨幅，Anthropic 上市次日承压](#item-7) ⭐️ 8.0/10
8. [CVE-2026-99312：KVM 漏洞使 AMD 主机内存可被虚拟机读取](#item-8) ⭐️ 8.0/10
9. [OpenAI 据称宣布解决纳维–斯托克斯千禧年难题](#item-9) ⭐️ 8.0/10
10. [谷歌据称发布 Gemini 4 Neon，主打编程、知识工作与科研](#item-10) ⭐️ 8.0/10
11. [微软演示 RDMA over USB4：多台 PC 合力运行一个本地 AI 模型](#item-11) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [马苏洛抢在 Anthropic 人工智能声明后数小时仓促公布耗时 12 年的 GRH 证明](https://math216.wordpress.com/2026/11/20/hurried-announcement-alessandro-masullo-grh/) ⭐️ 9.0/10

2026 年 11 月 20 日，亚历山德罗·玛丽亚·马苏洛（Alessandro Maria Masullo）公布了一份约 940 页、尚不完整的手稿，声称证明了广义黎曼猜想（GRH），并表示自己为此已钻研近 12 年；这一消息由美国数学会主席拉维·瓦基尔（Ravi Vakil）仓促发布，距离 Anthropic 数学家莱文特·阿尔珀格（Levent Alpöge）宣称借助 Claude 模型证明黎曼猜想仅过去数小时。 若 GRH 得到正确证明，将是数学史上最重大的成果之一——它将作为特例解决黎曼猜想，并在数论领域产生大量推论；而人类与人工智能几乎同时宣称证明，也使这一事件成为检验机器辅助数学时代如何认定优先权、归属与验证的典型案例。 该手稿尚未经过验证且明显未完成——有评论者指出，这份 940 页文稿的第 1.1.1 节竟是空的——但马苏洛的博士论文导师、斯坦福大学的布莱恩·康拉德（Brian Conrad）据称已仔细审阅数月，目前认为它看起来不错，其反馈意见正被纳入修订。

hackernews · jasondavies · 11月20日 18:33 · [社区讨论](https://news.ycombinator.com/item?id=50579568)

**背景**: 黎曼猜想由伯恩哈德·黎曼于 1859 年提出，猜测黎曼ζ函数的所有非平凡零点实部均为 1/2，至今仍未获证明，是数学中最著名的未解难题之一。广义黎曼猜想则把同一断言从ζ函数推广到范围更广的一类全局 L 函数——这类函数刻画了多种算术与几何对象，因此证明 GRH 比只证明 RH 更强、影响也更深远。如此量级的成果通常会等到同行评审后才公开，因此这次仓促发布颇为罕见，反映出作者对确立优先权的焦虑。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Generalized_Riemann_hypothesis">Generalized Riemann hypothesis - Wikipedia</a></li>
<li><a href="https://www.scientificamerican.com/article/dueling-claims-of-riemann-hypothesis-proofs-emerge/">Dueling claims of Riemann hypothesis proofs ... | Scientific American</a></li>
<li><a href="https://math216.wordpress.com/2026/11/20/hurried-announcement-alessandro-masullo-grh/">Hurried Announcement: Alessandro Masullo GRH</a></li>

</ul>
</details>

**社区讨论**: 评论者的态度在忧虑与怀疑之间明显分化：有人认为这起事件表明智力劳动如今要依赖少数富豪掌控的机器，有人则关注 12 年心血几乎被一则人工智能公告盖过的人性代价，还有人质疑一份 940 页的成果如何能被隐藏如此之久。少数人提出缺乏依据的猜测，认为证明可能通过上传的材料泄露给了 Anthropic；也有人只是提醒，两项声明目前都尚未经受住检验。

**标签**: `#mathematics`, `#Riemann Hypothesis`, `#AI`, `#research`, `#academia`

---

<a id="item-2"></a>
## [Levent Alpöge 宣称证明广义黎曼猜想，并附约 1500 万行 Lean 形式化代码](https://alpo.ge/remark.pdf) ⭐️ 9.0/10

数学家 Levent Alpöge 在 alpo.ge/remark.pdf 发布论文，宣称证明了广义黎曼猜想（GRH），并附上一份被网友测出约 1.3 GB、约 1500 万行的 Lean 形式化代码，以 14 个分卷压缩包的形式提供下载。据《科学美国人》等媒体报道，这一声明尚未获得数学界的独立验证。 黎曼猜想是数学中最著名的未解难题，而其推广形式（涉及 Dirichlet 与 Dedekind zeta 函数）是解析数论大量结论的基础，因此一旦证明成立，将重塑整个领域，并立即跻身数学史上最伟大的成就之列。由于该论证同时附带可由机器检查的 Lean 形式化代码，这也成为一次检验：形式化验证能否裁决——或至少大幅加快——对这类惊人声明的审稿过程。 这份形式化的规模（约 1.3 GB、约 1500 万行）远超一般 Lean 项目的量级，使人工审阅几乎不可行，审查重点因此转向：Lean 中形式化的命题是否确实是 GRH，以及是否残留额外公理或未完成的证明步骤。评论区还提到 Alessandro Masullo 另一份仓促发布的 GRH 声明，而 Alpöge 论证的独立专家验证目前仍在等待之中。

hackernews · iamronaldo · 11月20日 14:16 · [社区讨论](https://news.ycombinator.com/item?id=50574968)

**背景**: 黎曼猜想断言黎曼 zeta 函数的所有非平凡零点都位于实部为 1/2 的临界线上；广义黎曼猜想把这一断言推广到包括 Dirichlet L 函数与 Dedekind zeta 函数在内的更广泛的一类 L 函数，对素数分布等问题有重大推论。Lean 是由 Leonardo de Moura 主导开发的证明助手，其社区维护的数学库 mathlib 让数学家可以用形式化语言书写证明，并由一个很小的可信内核机械地检查。Lean 形式化本身并不能使定理为真——它只保证所述命题在所采用的公理与库之下成立——因此形式化命题是否写对、是否存在隐藏假设，正是审稿人必须核查的关键。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Generalized_Riemann_hypothesis">Generalized Riemann hypothesis - Wikipedia</a></li>
<li><a href="https://leanprover-community.github.io/">Lean community</a></li>
<li><a href="https://www.scientificamerican.com/article/anthropic-mathematician-claims-to-prove-riemann-hypothesis-most-famous-problem-in-all-of-math/">Anthropic mathematician claims to prove... | Scientific American</a></li>

</ul>
</details>

**社区讨论**: Hacker News 讨论帖（超过 2500 分、1700 条评论）交织着真切的惊叹与审慎：有人复现了下载流程并测出这份证明的庞大体量，也有人翻出 2014 年的一段土耳其语采访，当时刚毕业的 Alpöge 把解决黎曼猜想称为自己的人生目标。还有人调侃突破来得太快、人们已经开始麻木，并对 AI 推动的科学加速乃至“协调暂停”表示担忧；同时也希望这类理论成果最终能转化为粮食、能源与医疗等方面的切实收益。

**标签**: `#Riemann Hypothesis`, `#mathematics`, `#Lean theorem proving`, `#formal verification`, `#research breakthrough`

---

<a id="item-3"></a>
## [陶哲轩将无外力纳维-斯托克斯奇点与广义黎曼猜想联系起来](https://terrytao.wordpress.com/2026/11/20/unforced-euler-singularity-unforced-navier-stokes-singularity-and-the-generalized-riemann-hypothesis/) ⭐️ 9.0/10

在 2026 年 11 月 20 日的一篇博客文章中，陶哲轩（Terence Tao）讨论了无外力欧拉方程奇点形成、无外力纳维-斯托克斯方程奇点形成及其与广义黎曼猜想的联系，并指出首个无外力欧拉方程爆破结果已由 OpenAI 证明，且与受外力纳维-斯托克斯爆破在同一天公布。该文引发了 Hacker News 上多达 163 条评论的讨论，有评论者称相关证明已被两个独立的 Lean 内核接受，表明并未利用内核漏洞。 这两个问题都是数学中最著名的未解难题——与 100 万美元千禧年大奖挂钩的纳维-斯托克斯存在性与光滑性问题，以及黎曼猜想——因此其中任何一项的进展（尤其是机器辅助的进展）都会重塑这两个领域。这场讨论也标志着一种更广泛的转变：AI 系统开始参与前沿数学证明，并就验证、可信度以及人类数学家的未来角色向研究者提出了紧迫问题。 评论者指出，该论证据称用到了朗兰兹纲领（Langlands program）和算术几何的现代发展成果，而两个独立 Lean 内核的交叉验证是证明并非内核漏洞产物的关键证据。据报道，陶哲轩的文章并未直接断言其重要性，考虑到黎曼猜想命题的分量，一些读者对此感到不满。

hackernews · archon1410 · 11月20日 17:21 · [社区讨论](https://news.ycombinator.com/item?id=50578358)

**背景**: 纳维-斯托克斯存在性与光滑性问题问的是：三维纳维-斯托克斯方程（流体运动的标准模型）的光滑解是否总是存在，还是可能在有限时间内爆破形成奇点；欧拉方程是其无粘性（无摩擦）的特例，而“无外力”意味着方程中没有外加力项。黎曼猜想是数学中最重要的猜想之一，它断言黎曼 ζ 函数的非平凡零点实部均为 1/2，而广义黎曼猜想把这一断言推广到更广泛的一类全局 L 函数。Lean 是一种交互式定理证明器，其体积很小的可信内核会机械地检查证明，这正是独立内核验证对机器生成的数学如此重要的原因。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://terrytao.wordpress.com/2026/11/20/unforced-euler-singularity-unforced-navier-stokes-singularity-and-the-generalized-riemann-hypothesis/">Unforced Euler singularity , unforced Navier - Stokes singularity , and...</a></li>
<li><a href="https://en.wikipedia.org/wiki/Navier–Stokes_existence_and_smoothness">Navier – Stokes existence and smoothness - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Generalized_Riemann_hypothesis">Generalized Riemann hypothesis - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 讨论中既有兴奋也有焦虑：一些评论者形容自己对职业前景既激动又恐惧，其中一人称 AI 目前似乎已在本质上超越人类数学智能，而这种能力扩散到其他领域只是时间问题。一个反复出现的反驳意见是：真正全新的抽象与概念将从何而来——正如一位评论者所问，我们如何创造出下一个“朗兰兹纲领”，而不是只利用现有的；另一些人则批评陶哲轩没有评论这一黎曼猜想结果的重要性。

**标签**: `#mathematics`, `#fluid-dynamics`, `#Riemann-hypothesis`, `#AI-theorem-proving`, `#research`

---

<a id="item-4"></a>
## [GitHub 仓库声称无外力纳维-斯托克斯方程有限时间爆破](https://github.com/tristanbuckmaster/navier-stokes/) ⭐️ 9.0/10

一个托管在 Tristan Buckmaster 名下的 GitHub 仓库声称，对无外力的三维纳维-斯托克斯方程给出了有限时间爆破结果。相关讨论在 Hacker News 上获得 273 分和 86 条评论，并被当作可能达到千禧年大奖难题级别的重要结果。 如果该结果成立，它将解决 Clay 数学研究所提出的纳维-斯托克斯存在性与光滑性难题中的一个陈述，并成为偏微分方程领域的重大突破。由于它针对无外力方程，比依赖精心设计外力构造的反例更接近原始物理问题。 该结果专门针对无外力情形；评论者将其与 OpenAI 此前使用精心设计外力构造的结果区分开来。仓库中的声称仍需独立验证和同行评审，因为三维奇点形成的证明以技术上的精细和脆弱著称。

hackernews · trotro · 11月20日 15:34 · [社区讨论](https://news.ycombinator.com/item?id=50576232)

**背景**: 纳维-斯托克斯方程描述黏性流体的运动。存在性与光滑性问题问的是：三维空间中的光滑解是否永远保持光滑，还是会在有限时间内产生奇点；有限时间爆破就是后一种情形。2000 年 Clay 数学研究所将其列为千禧年大奖难题，并区分有外力与无外力等不同条款，其中“无外力”指没有外部作用力。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Navier–Stokes_existence_and_smoothness">Navier–Stokes existence and smoothness - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Navier–Stokes_priority_controversy">Navier–Stokes priority controversy - Wikipedia</a></li>
<li><a href="https://openai.com/index/navier-stokes-solution/">On the Navier–Stokes Millennium Prize Problem | OpenAI</a></li>

</ul>
</details>

**社区讨论**: 评论者既兴奋又惊讶，有人指出若同一天还出现广义黎曼猜想的声称，那将刷新数学史上的重大事件标准。不少人聚焦于有外力与无外力的区别，认为无外力版本更“真实”，也有人谈论 OpenAI 此前的外力结果、关于 Anthropic 千禧年难题的传闻，以及 Buckmaster 和 Alpoge 之间由此产生的优先权戏剧。还有人询问能否用数值模拟实时展示爆破，以帮助直观理解方程在何处偏离现实。

**标签**: `#Navier-Stokes`, `#fluid dynamics`, `#PDEs`, `#Millennium Prize`, `#mathematical breakthrough`

---

<a id="item-5"></a>
## [Thinking Machines 发布 Inkling 2 Mini 开放权重循环 Transformer 模型](https://thinkingmachines.ai/news/inkling-2-mini/) ⭐️ 8.0/10

Thinking Machines 发布了 Inkling 2 Mini，这是一个以 nvfp4 端到端训练的开放权重循环 Transformer 模型；早期反馈称其性能可媲美 Qwen3-27B 级别模型，同时能在本地硬件上高效运行。 这很重要，因为循环架构在开放模型中仍然少见，可能指向更参数高效的设计方向；同时它也为本地推理用户提供了一个可配合 llama.cpp 和 GGUF 工具使用的新选择。 该模型在训练全程使用 nvfp4，而不是仅在训练后量化；早期用户报告在 Ryzen 395 上通过 llama.cpp Vulkan 约为 27 tokens/s，在 32GB M1 Pro 上使用 q4 XL 量化约为 10 tokens/s。社区指出若干尚未合并的 llama.cpp PR 和一个小补丁可带来约 30% 加速，同时一个简单的 CSV 排序编程测试成功，但硬币识别测试在长时间胡言乱语后失败。

hackernews · jasondavies · 11月20日 20:12 · [社区讨论](https://news.ycombinator.com/item?id=50581260)

**背景**: 循环 Transformer 会重复使用同一个 Transformer 块进行多轮传递，目标是在不让参数量像传统深层堆叠那样增长的情况下，模拟更深的网络和更强的推理能力。NVFP4 是一种 4 位浮点格式，通常以 16 个权重为一组进行微缩放，从而压缩模型，同时让激活值保持较高精度以维持数值稳定性。大多数开放权重模型先用较高精度训练、之后再量化，因此端到端 nvfp4 训练是一个值得注意的区别。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://thinkingmachines.ai/news/inkling-2-mini/">Introducing Inkling 2 Mini - Thinking Machines Lab</a></li>
<li><a href="https://www.emergentmind.com/topics/looped-transformer-architecture">Looped Transformer Architecture</a></li>
<li><a href="https://unsloth.ai/docs/models/qwen3.8">Qwen3.8 - How to Run Locally | Unsloth Documentation</a></li>

</ul>
</details>

**社区讨论**: 评论者总体上非常兴奋，认为如果基准测试经得起检验，这款模型“好得离谱”，并预测更多开放模型可能转向循环架构；多人分享了具体的本地推理数据，包括 Ryzen 395 搭配 Vulkan 约 27 tokens/s、32GB M1 Pro 约 10 tokens/s。他们还指出了具体的 llama.cpp PR 和一个可带来约 30% 加速的小补丁，同时有人对循环架构广泛可用后的安全性和可解释性表示担忧。测试结果喜忧参半：一位用户的简单 CSV 排序任务完成得很好，但硬币识别压力测试在约 12,000 个 token 后失败。

**标签**: `#LLM`, `#open-weights`, `#looped-transformers`, `#local-inference`, `#quantization`

---

<a id="item-6"></a>
## [语言模型无需梯度即可重写自身权重](https://arxiv.org/abs/2611.21885) ⭐️ 8.0/10

一篇新的 arXiv 论文（2611.21885）声称首次证明，语言模型可以通过自身推理重写自己的权重，在连续八次会话中提升准确率，且无需梯度或传统训练。 如果结果可复现，自我重写将使已部署模型无需昂贵的重新训练即可自我修复或改进，但它也模糊了推理与训练的界限，并引发关于自主自我修改的严重 AI 安全担忧。 据报道，该模型在练习题上测试候选编辑，只保留有效的修改；但评论者指出，所发现的唯一自我改进是缩短推理轨迹以避免 token 限制，而 Weight-Space Programming 和 Google 的 Sleep 框架等先前工作已经探索过相关的权重编辑思路。

hackernews · lwhsiao · 11月20日 16:29 · [社区讨论](https://news.ycombinator.com/item?id=50577265)

**背景**: 大型语言模型通常只训练一次然后被冻结；要改变其行为，通常需要用基于梯度的优化进行微调，或添加提示词和推理时脚手架。权重编辑是一种直接修改模型参数的替代方法，近期研究已表明前沿 LLM 可以在不运行梯度循环的情况下读写小型神经网络的权重。这篇论文延续了这一方向，探讨模型能否通过推理而非外部训练来编辑自己的权重。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/2611.21885">[2611.21885] Language Models Can Rewrite Their Own Weights</a></li>
<li><a href="https://rikiyat.github.io/blog/weight-space-programming/">Sparks of Weight -Space Programming: LLMs can natively read & write...</a></li>
<li><a href="https://notesbylex.com/weight-space-programming">Weight -Space Programming - NotesByLex.com</a></li>

</ul>
</details>

**社区讨论**: 这场有 116 条评论的讨论总体既感兴趣又持怀疑态度：评论者引用 Google 的 Sleep 框架和 Weight-Space Programming 作为先前工作，质疑“无训练”的说法是否诚实，因为该过程仍在筛选有效修改，并警告自主权重编辑可能被用于消除与安全相关的激活。

**标签**: `#ai-safety`, `#self-improving-models`, `#llm-research`, `#weight-editing`, `#machine-learning`

---

<a id="item-7"></a>
## [AI 抛售抹去纳斯达克 2026 年涨幅，Anthropic 上市次日承压](https://www.theguardian.com/business/2026/nov/20/global-stock-markets-slump-anthropic-ipo-ai-sell-off) ⭐️ 8.0/10

2026 年 11 月 20 日，AI 与半导体股票遭遇广泛抛售，抹去了纳斯达克指数今年以来的全部涨幅，并推动美国主要股指进入回调区间；Anthropic 在创纪录 IPO 后的第二个交易日股价下跌，一度逼近发行价。 这轮反转表明 2026 年市场上涨在多大程度上依赖 AI 乐观情绪，而 Anthropic 的上市表现被视为其他急需资金的 AI 公司——尤其是已把 IPO 推迟到 2027 年的 OpenAI——能否继续从公开市场获得高估值融资的重要信号。 Anthropic 在创纪录上市首日收涨 17%，但随后在盘后交易中下跌近 5%，股价仅比发行价高约 11%；此次抛售也冲击了 AI 与半导体板块，道指和标普 500 指数与纳指一同进入回调区间。

hackernews · cdrnsf · 11月20日 13:29 · [社区讨论](https://news.ycombinator.com/item?id=50574383)

**背景**: IPO 即首次公开募股，是私营公司向公众发行股票并在证券交易所上市的过程，使公司获得大规模资本，也让早期投资者有了市场价格。纳斯达克是科技公司权重很高的美国交易所，因此 AI 相关股票的波动会显著影响该指数。所谓“回调”通常指股指较近期高点下跌至少 10%。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.theguardian.com/technology/2026/nov/20/anthropic-ipo-historic-stock-market-debut-key-takeaways-what-next-for-ai">Anthropic ’s historic stock market debut: key... | The Guardian</a></li>
<li><a href="https://www.ft.com/content/c7ad2e0c-efd1-40c2-a5a8-819ced8acf5b?syn-25a6b1a6=1">Tech stocks fall after Anthropic IPO</a></li>
<li><a href="https://www.upi.com/Top_News/US/2026/11/20/stocks-dow-jones-nasdaq-correction-territory/1061795214998/">Dow, S&P 500 enter correction as Nasdaq plunges in AI ... - UPI</a></li>

</ul>
</details>

**社区讨论**: 评论者讨论了廉价 AI 自动化是否会缩小高薪行业的 GDP 统计口径，警告 Anthropic 及更广泛科技板块的高估值建立在“希望和梦想”而非基本面之上，并质疑疲软的上市表现是否会打乱 OpenAI 的 IPO 计划。也有人把这视为利益集中问题——技术进步在“剥离全人类知识”为少数人服务——还有评论者感叹创纪录 IPO、市场暴跌与黎曼猜想被宣布解决同时出现，令人感到诡异。

**标签**: `#AI industry`, `#stock market`, `#Anthropic`, `#IPO`, `#tech valuations`

---

<a id="item-8"></a>
## [CVE-2026-99312：KVM 漏洞使 AMD 主机内存可被虚拟机读取](https://thehackernews.com/2026/11/new-linux-kvm-flaw-cve-2026-99312-lets.html) ⭐️ 8.0/10

Linux 内核 KVM 漏洞 CVE-2026-99312 于 2026 年 11 月 18 日公开披露，研究人员此前已演示从一台客户虚拟机内部读取到 DigitalOcean 服务器约 127 GB 的内存。上游修复已随 7.3.5 等稳定内核发布，但报道发布时 Debian、Ubuntu 等发行版内核尚未修复。 该漏洞打破了多租户云服务商赖以生存的隔离边界，因此在共享的 AMD 主机上，被泄露的内存可能包含其他客户的虚拟机数据。由于 KVM 是大多数基于 Linux 的云基础设施的默认虚拟化层，尚未修复且启用了嵌套虚拟化的 AMD 主机面临真实风险。 该漏洞被描述为 KVM 中的一处失效指针（stale pointer），可追溯到此前的某次安全修复，且仅影响启用了嵌套虚拟化的 AMD 处理器主机。管理员可在补丁内核可用之前关闭嵌套虚拟化作为缓解措施，而被调查的许多云服务商之所以不受影响，正是因为它们未在 AMD 硬件上启用该功能。

telegram · zaihuapd · 11月20日 14:23

**背景**: KVM 是直接内建于 Linux 内核的虚拟化管理程序，可让一台物理机运行多个相互隔离的虚拟机。嵌套虚拟化指的是在客户虚拟机内部再运行一个虚拟化管理程序，在 AMD 硬件上这依赖 AMD-V/SVM 扩展与嵌套分页，使外层虚拟化层能够捕获并模拟内层的指令。这层额外的模拟增加了客户机与主机边界的复杂度，此处一旦出错，读取虚拟化状态的操作为就可能变成对主机内存的读取。内核修复通常要等到各 Linux 发行版重新基线自己的内核后才到达用户，这也是上游补丁与发行版可用性出现时间差的原因。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://thehackernews.com/2026/11/new-linux-kvm-flaw-cve-2026-99312-lets.html">Linux KVM Flaw CVE - 2026 - 99312 Lets Guest VMs Access Host...</a></li>
<li><a href="https://www.terra.security/blog/kvm-guest-to-host-escape">KVM Guest-to-Host Escape | Terra Security Research</a></li>
<li><a href="https://www.digitalocean.com/blog/cve-2026-99312-kvm-patch">Virtualization , Responsible Disclosure, and CVE - 2026 - 99312</a></li>

</ul>
</details>

**标签**: `#KVM`, `#CVE`, `#Linux security`, `#virtualization`, `#AMD`

---

<a id="item-9"></a>
## [OpenAI 据称宣布解决纳维–斯托克斯千禧年难题](https://t.me/zaihuapd/45265) ⭐️ 8.0/10

据一个 Telegram 频道消息，OpenAI 宣布解决了纳维–斯托克斯存在性与光滑性问题（七大克雷千禧年大奖难题之一），并同时公开了论文与 Lean 形式化验证。该帖称，证明由一个大规模内部系统生成，动用约 1 万个并行智能体、270 万条消息和约 1300 亿输出 token，OpenAI 还表示无意申领该奖项。 若经证实，这将是 AI 系统首次给出千禧年大奖难题的解答，可能成为 AI 驱动数学研究的转折点，也让形式化验证成为新的可信度标准。它还会重塑流体力学中的一个核心问题，而据报道的多智能体运行规模，也将成为大规模智能体系统的重要参考数据。 据称该证明显示，初始光滑的流体流动可在有限时间内产生奇点，这对应克雷问题中“有限时间爆破”的一侧，而非“全局正则性”的一侧。不过，诸如智能体数量之类的细节，以及 OpenAI 起初以为 Anthropic 的 Levent Alpöge 与纽约大学的 Tristan Buckmaster 也解出该题的说法，都显得颇为蹊跷；目前该消息仅来自单一 Telegram 频道，既无独立佐证，也未经过同行评审。

telegram · zaihuapd · 11月20日 15:29

**背景**: 纳维–斯托克斯方程描述黏性流体的运动，克雷数学研究所的千禧年大奖难题所要问的是：三维不可压缩方程的光滑解是否始终存在，还是会在有限时间内失效——任何解答都必须在这两种结论中确立一个。Lean 是一个免费开源的证明助手与函数式编程语言，基于依赖类型论，可用于书写并机器检验数学证明，因此若证明真的完成了 Lean 形式化，原则上任何人都能通过机器对其进行验证。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Navier–Stokes_existence_and_smoothness">Navier – Stokes existence and smoothness - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Lean_(proof_assistant)">Lean (proof assistant) - Wikipedia</a></li>
<li><a href="https://navier-stokes.org/navier-stokes-existence-and-smoothness/">Clay Navier - Stokes Problem : Official Statement Explained</a></li>

</ul>
</details>

**标签**: `#AI research`, `#mathematics`, `#Navier-Stokes`, `#Lean formal verification`, `#LLM agents`

---

<a id="item-10"></a>
## [谷歌据称发布 Gemini 4 Neon，主打编程、知识工作与科研](https://t.me/zaihuapd/45267) ⭐️ 8.0/10

据传谷歌发布了名为 Gemini 4 Neon 的新模型，主打复杂软件工程、知识工作与科研工作流的快速端到端执行，并已向开发者、企业以及 Google AI Pro/Ultra 订阅用户开放。其公布的价格为每百万输入 token 3 美元（缓存输入 0.15 美元）、每百万输出 token 15 美元，并支持 100 万 token 的上下文窗口。 如果这些基准测试成绩属实，谷歌将把一个模型推到智能体编程排行榜的最顶端，同时在价格上低于竞争对手，这会直接影响开发者选择哪种智能体或模型来构建长时间运行的编程与科研流水线。这也说明 2026 年的竞争已从单纯的对话质量转向多步骤、调用工具任务的可靠执行能力。 该帖称 Gemini 4 Neon 以 58.6 分登顶 Artificial Analysis 编程智能体指数，并在智能指数 xhigh 档以 61 分位列总榜第三，Terminal-Bench 的成绩在原文中被截断。值得注意的是，这条消息仅来自一则简短的 Telegram 帖子，没有提供谷歌官方公告、模型卡或独立验证的链接，因此这些规格与分数应视为未经证实。

telegram · zaihuapd · 11月21日 01:09

**背景**: Artificial Analysis 编程智能体指数是一个综合基准分数，由 FrontierCode-AA 2.0、Terminal-Bench 4.1 和 SWE-Atlas-QnA-AA 三项评测组合而成，该网站本身也建议将其与各项分项成绩对照阅读，而不是当作唯一结论。Terminal-Bench 衡量的是 AI 智能体能否真正通过终端操作计算机来完成真实任务，因此它已成为评测编程智能体的常用标尺。提示缓存则允许 API 复用此前处理过的上下文；在已追踪的 LLM API 中，缓存命中的价格通常是标准输入价格的 2%–25%（中位数约 10%），因此报道中的 0.15 美元对 3 美元输入价格约相当于 95% 的折扣。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://artificialanalysis.ai/agents/coding-agents">AI Coding Agent Benchmarks & Leaderboard | Artificial Analysis</a></li>
<li><a href="https://www.tbench.ai/">TERMINAL - BENCH</a></li>
<li><a href="https://llmcostlab.com/articles/llm-prompt-caching-prices-compared-2026/">LLM Prompt Caching Prices Compared (2026) | LLM Cost Lab</a></li>

</ul>
</details>

**标签**: `#Gemini`, `#Google`, `#LLM`, `#software engineering`, `#AI benchmarks`

---

<a id="item-11"></a>
## [微软演示 RDMA over USB4：多台 PC 合力运行一个本地 AI 模型](https://videocardz.com/newz/microsoft-brings-rdma-over-usb4-to-windows-allowing-multiple-pcs-to-run-one-local-ai-model) ⭐️ 8.0/10

微软发布了 Windows 平台的 RDMA over USB4 开发者预览，多台 PC 可通过普通的 USB4 线缆共享已注册的内存区域与 GPU 算力，从而合力运行同一个本地 AI 模型，无需专用网卡或交换机。在演示中，三台搭载 AMD Ryzen AI Max+ 395 的机器以 4-bit 量化运行 Qwen3-235B-A22B，速度约为 18.5 token/s，该预览版将通过 Windows Insider 通道推送。 这让廉价且普及的 USB4 接口变成了分布式本地推理的互联通道，发烧友和小团队可以把手头已有的机器拼起来，而不必去购买一台显存足以装下大模型的单机。它也表明 Windows 正在构建主机到主机的互联（fabric）层，有望让消费级的分布式 AI 推理从“折腾玩法”变成系统级的标准能力。 RDMA over USB4 建立在 Windows 11 已有的 USB4 主机到主机网络之上：每台 PC 构成独立的 USB4 域，由 Windows 连接管理器在两者之间建立点对点隧道，数据得以在已注册的内存区域之间直接搬运，省去经 CPU 的多次拷贝。该预览目前仅支持特定的 AMD 硬件，约 18.5 token/s 的成绩来自把 4-bit 量化的 235B 参数 MoE 模型拆分到三台机器上运行，因此更像可行性演示而非性能基准。

telegram · zaihuapd · 11月21日 06:13

**背景**: RDMA（远程直接内存访问）允许一台机器直接读写另一台机器的内存，无需远端 CPU 或操作系统参与，长期是高性​​能集群的核心技术，但过去通常运行在 InfiniBand 或专用以太网卡之上。USB4（与雷电 3/4 同源）能通过普通线缆提供高带宽、低延迟的 PCIe 隧道，使其成为消费级硬件上承载 RDMA 的可行载体。大语言模型通常受限于能否装进显存，因此把多台机器的显存池化，就能运行远超任何单块 GPU 或统一内存 APU 容量的大模型；4-bit 量化压缩了权重，使 235B 参数的模型能分布到几台机器上，而 Qwen3-235B-A22B 是混合专家（MoE）模型，每次前向只激活约 22B 参数，从而把单 token 的计算量控制在可接受范围。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.techpowerup.com/355062/microsoft-brings-rdma-over-usb4-to-windows-11-for-daisy-chained-pcs">Microsoft Brings RDMA over USB 4 to Windows 11 for... | TechPowerUp</a></li>
<li><a href="https://www.guru3d.com/story/microsoft-previews-usb4-links-that-let-windows-pcs-pool-memory-and-gpu-resources/">Microsoft previews USB 4 links that let Windows PCs pool memory ...</a></li>
<li><a href="https://writingmate.ai/models/qwen/qwen3-235b-a22b">Qwen: Qwen 3 235 B A 22 B - AI Model Details | Writingmate</a></li>

</ul>
</details>

**标签**: `#RDMA`, `#USB4`, `#local AI`, `#Windows`, `#distributed inference`

---