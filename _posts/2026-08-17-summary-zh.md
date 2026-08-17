---
layout: default
title: "Horizon Summary: 2026-08-17 (ZH)"
date: 2026-08-17
lang: zh
---

> 从 34 条内容中筛选出 8 条重要资讯。

---

1. [Anthropic 公开 Claude 系统提示词，社区用 Git Diff 追踪变更](#item-1) ⭐️ 8.0/10
2. [Cloudflare 在切换域名服务器时静默注入分析脚本](#item-2) ⭐️ 8.0/10
3. [Stripe 以超过 70 亿美元收购 AI 公司 OpenRouter](#item-3) ⭐️ 8.0/10
4. [Qwen 3.8 27B：优秀开源模型但默认过度思考](#item-4) ⭐️ 8.0/10
5. [PJM 建模失误浪费 120 亿美元用户资金](#item-5) ⭐️ 8.0/10
6. [SSOG 注意力：可分离高斯和实现次二次复杂度注意力替代方案](#item-6) ⭐️ 8.0/10
7. [重新审视 ECA：跨通道交互假设受到质疑](#item-7) ⭐️ 8.0/10
8. [Anthropic 第二季营收暴涨 14 倍，超 115 亿美元](#item-8) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Anthropic 公开 Claude 系统提示词，社区用 Git Diff 追踪变更](https://platform.claude.com/docs/en/release-notes/system-prompts) ⭐️ 8.0/10

Anthropic 的 Claude 系统提示词发布说明公开了 Opus 4.8、Fable 5 和 Mythos 5 背后的指令。开发者 Simon Willison 将这些提示词重建为 git 提交历史，方便用户比较各版本之间的改动。 这是外界难得一见的公开视角，展示领先 AI 实验室如何为旗舰模型编写指令，让开发者和研究者更了解提示词设计与模型行为。它也推动了关于透明度、上下文窗口管理以及更长系统提示词是否有助于模型表现的广泛讨论。 系统提示词异常冗长，其中有一条明确告诉 Claude：提示中提到图片并不代表图片一定存在，因此 Claude 需要自行核实。社区对比 diff 后指出，最值得关注的改动涉及 Claude Fable 5 和 Claude Mythos 5 的首次发布；也有评论者质疑连 Fable 5 都带有相似的图片检查指令，以及过长的提示词是否会让模型分心。

hackernews · tosh · 8月16日 12:48 · [社区讨论](https://news.ycombinator.com/item?id=49319556)

**背景**: 系统提示词是在对话开始前添加给大语言模型的一组特殊指令，用于设定角色、规则和上下文。Anthropic 的 Claude 模型家族包括 Opus、Sonnet、Haiku、Fable 和 Mythos 等型号，它们在智能水平、速度和成本上各有差异。基于 diff 的版本对比通过标注新增和删除的行来展示文本变化，是审查代码、现在也用于追踪模型提示词的常用方法。这些背景解释了为何发布说明和 Simon Willison 的 git 历史能引起开发者广泛关注。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://promptengineering.org/system-prompts-in-large-language-models/">System Prompts in Large Language Models - Prompt Engineering</a></li>
<li><a href="https://en.wikipedia.org/wiki/Diff">diff - Wikipedia</a></li>
<li><a href="https://toloka.ai/blog/claude-models-explained/">Claude models explained: Opus, Sonnet, Haiku, and Fable Guide</a></li>

</ul>
</details>

**社区讨论**: 社区对透明度总体持正面态度，Simon Willison 用 git diff 追踪提示词变动的做法被视为实用工具。但也有不少评论者提出质疑：有人指该论坛会悄悄删除对 AI 持负面报道的文章；有人认为让 Opus 4.8 自行核实图片是否存在只是“基本常识”，并不代表智能；还有人觉得系统提示词过长，反而可能分散模型注意力。

**标签**: `#AI`, `#LLM`, `#Claude`, `#system prompts`, `#transparency`

---

<a id="item-2"></a>
## [Cloudflare 在切换域名服务器时静默注入分析脚本](https://news.ycombinator.com/item?id=49322107) ⭐️ 8.0/10

一名 Hacker News 用户报告称，为启用 R2 存储桶服务而将域名服务器切换到 Cloudflare 后，Cloudflare 静默向其纯 HTML、无 JavaScript 的网站注入了 Web Analytics JavaScript 片段。该注入仅能在分析仪表盘中看到，用户必须事后手动关闭，属于“默认启用、事后退出”而非主动选择加入。 这凸显了人们对大型基础设施提供商“黑暗模式”的担忧：用户默认被跟踪，除非自己发现并关闭该功能。任何切换域名服务器或使用 Cloudflare 代理的客户都可能受影响，不仅会污染网站统计数据，还会引发隐私问题。 被注入的脚本托管在 static.cloudflareinsights.com/beacon.min.js，带有 CF beacon token 和版本号（如 2024.11.0）。用户可以在分析仪表盘中添加站点然后关闭该片段来禁用；也可以使用包含 script-src 的 Content-Security-Policy（CSP）在客户端阻止它。

hackernews · stagas · 8月16日 17:49

**背景**: Cloudflare 提供以隐私为导向的 Web Analytics 产品，但在将域名添加到 Cloudflare 时，该脚本似乎是默认启用的。原作者使用的是 Cloudflare R2 对象存储服务，并为了通过自定义子域名提供存储桶内容而切换了域名服务器。由于他的网站本身不含 JavaScript，注入的脚本显得格外意外，只能在仪表盘中看到。在 CDN 架构下，Cloudflare 会终止 HTTPS 连接，并在响应到达浏览器之前修改 HTML，这正是注入能够发生的原因。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://developers.cloudflare.com/r2/buckets/public-buckets/">Public buckets · Cloudflare R2 docs</a></li>
<li><a href="https://notifire.in/infra/cloudflare-may-be-adding-code-to-your-website">Cloudflare Analytics Script Injected Without User Consent</a></li>
<li><a href="https://ideaverse.ai/blog/cloudflare-dns-change-triggered-hidden-analytics-script-injection-mswbamkg">Cloudflare DNS Change Triggered Hidden Analytics Script ...</a></li>

</ul>
</details>

**社区讨论**: 评论区用户反应强烈，有人称 Cloudflare 的黑暗模式“介于 GoDaddy 和 RyanAir 之间”。也有用户提供了技术缓解方案，例如使用 CSP meta 标签限制脚本来源；还有用户指出，注入发生意味着 Cloudflare 正在终止 HTTPS 连接并进行代理，而不仅仅是提供 DNS 解析服务。

**标签**: `#cloudflare`, `#privacy`, `#dark-patterns`, `#web-analytics`, `#security`

---

<a id="item-3"></a>
## [Stripe 以超过 70 亿美元收购 AI 公司 OpenRouter](https://www.bloomberg.com/news/articles/2026-08-16/stripe-nears-deal-to-buy-ai-firm-openrouter-for-over-7-billion) ⭐️ 8.0/10

据 Bloomberg 2026 年 8 月报道，Stripe 已敲定以超过 70 亿美元收购统一 AI 模型路由平台 OpenRouter。此次收购标志着 Stripe 从单纯处理支付，进入拥有 AI 基础设施的领域。 这笔交易使 Stripe 有望成为 LLM API 支付与路由的中介，把其在金融支付抽象层上的专长延伸到 AI“token 轨道”。它可能会重塑 AI 模型的变现方式，并让 Stripe 在 AI 支付量上获得巨大话语权。 据悉，OpenRouter 在几个月前刚以 13 亿美元估值融资，因此 70 亿美元的退出是一次飞速跃升。交易发生之际，OpenAI 刚将支付服务商从 Stripe 换成 Adyen，而 OpenRouter 与 OpenAI 合计代表了约 1000 亿美元的支付量。

hackernews · zacharyozer · 8月16日 20:31 · [社区讨论](https://news.ycombinator.com/item?id=49323381)

**背景**: OpenRouter 是一个统一 API 市场，让开发者通过单一接口访问来自不同提供商的数百个 AI 模型，并处理路由、回退和统一计费。Stripe 是面向互联网企业处理在线支付的大型金融基础设施平台。通过收购 OpenRouter，Stripe 希望成为 AI 模型使用的支付与路由层。这契合“支付轨道”的概念——即在付款方与收款方之间转移资金的网络。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openrouter.ai/">OpenRouter</a></li>
<li><a href="https://www.codecademy.com/article/what-is-openrouter">What is OpenRouter? A Guide with Practical Examples | Codecademy</a></li>
<li><a href="https://en.wikipedia.org/wiki/Payment_rail">Payment rail - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 评论者围绕估值展开讨论，有人指出 70 亿美元超过了 Lyft、Dolby 和 Alaska Airlines 的市值。也有人认为这是 Stripe API 专长的自然延伸，以及 OpenAI 转投 Adyen 后争夺 AI 支付量的防御性举措。还有人称赞 OpenRouter 投资者获得快速回报，并强调切换成本和分发渠道是核心护城河。

**标签**: `#AI`, `#Acquisitions`, `#Fintech`, `#OpenRouter`, `#Stripe`

---

<a id="item-4"></a>
## [Qwen 3.8 27B：优秀开源模型但默认过度思考](https://simonwillison.net/2026/Aug/16/qwen-38-27b/) ⭐️ 8.0/10

Simon Willison 评测了阿里巴巴 Qwen 实验室发布的 Apache-2.0 许可、270 亿参数的视觉语言模型 Qwen 3.8 27B。他报告称，该模型的自我基准测试优于 Qwen 3.6 27B 和闭源的 Qwen 3.7-Plus，但其默认的“xhigh”推理强度会导致极端过度思考，例如生成一个 SVG 图像竟然耗时 21 分钟。 该模型表明开放权重模型在消费级硬件上的能力正在快速提升，可能对闭源模型构成挑战。然而，默认的过度思考行为暴露出实际可用性问题，可能影响普通用户在日常任务中的采用。 该模型默认将 reasoning_effort 设为“xhigh”，并提供“medium”和“low”选项。Willison 在 LM Studio 中遇到了 8,192 token 的默认上下文限制，不得不加载到 262,144 token 的最大值；一个“鹈鹕骑自行车”的 SVG 使用了 22,276 个推理 token 和 3,223 个输出 token，耗时 21 分钟。该模型在 LM Studio 中以 17GB 的 Q4_K_M 量化 GGUF 形式提供。

rss · Simon Willison · 8月16日 22:00

**背景**: Qwen 3.8 27B 来自阿里巴巴的 Qwen 实验室，采用 Apache-2.0 许可证，允许免费使用和修改。它具备视觉能力，可以处理图像，其前代 Qwen 3.6 27B 已经非常适合本地使用。开放权重模型与闭源模型的不同之处在于其权重是公开的，但训练数据和方法可能不公开。过度思考指的是模型在回答之前生成过多的思维链推理，这会消耗上下文并大幅降低响应速度。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://deepmind.google/research/publications/203490/">Towards Structural Understanding of LLM Overthinking</a></li>
<li><a href="https://www.pbs.org/newshour/science/whats-the-difference-between-closed-open‑source-and-open-weight-ai-a-researcher-explains">What's the difference between closed, open‑source and open-weight AI? A researcher explains | PBS News</a></li>

</ul>
</details>

**标签**: `#AI`, `#LLM`, `#Qwen`, `#open-source`, `#model release`

---

<a id="item-5"></a>
## [PJM 建模失误浪费 120 亿美元用户资金](https://newsletter.semianalysis.com/p/12b-of-us-ratepayers-money-wasted) ⭐️ 8.0/10

SemiAnalysis 发布的调查指出，PJM 容量市场中的一个建模失误已浪费了约 120 亿美元美国用户资金，并警告 PJM 可能在下一次拍卖中重蹈覆辙。 这一浪费抬高了 PJM 所覆盖地区数百万用户的电费，也削弱了人们对容量市场设计的信任。它同时说明，看似技术性的建模选择可能对电网产生巨大的财务影响。 问题集中在 PJM 的可靠性定价模型（RPM）拍卖中使用的可变资源需求（VRR）曲线和新建成本净值（Net CONE）参数上。批评者认为，这条有缺陷的曲线购买了超出需求的容量，导致以用户资金向发电商超额支付。

rss · Semianalysis · 8月16日 22:27

**背景**: PJM 运营着美国最大的电网，并通过年度容量市场——可靠性定价模型（RPM）——来确保未来有足够的电力资源满足需求。拍卖使用基于 Net CONE 等假设而管理设计的 VRR 需求曲线。Brattle 等机构每四年会审查这条曲线，但 SemiAnalysis 认为建模失误至今未得到纠正，并且还可能再次发生。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.pjm.com/markets-and-operations/rpm.aspx">PJM - Capacity Market (RPM)</a></li>
<li><a href="https://www.brattle.com/wp-content/uploads/2025/04/Sixth-Review-of-PJMs-Variable-Resource-Requirement-Curve.pdf">Sixth Review of PJM s Variable Resource Requirement Curve</a></li>
<li><a href="https://www.renewableenergyworld.com/power-grid/no-electricity-markets-are-not-broken-heres-why/">No, electricity markets are not broken – here’s why</a></li>

</ul>
</details>

**标签**: `#energy grid`, `#modeling`, `#PJM`, `#infrastructure`, `#economics`

---

<a id="item-6"></a>
## [SSOG 注意力：可分离高斯和实现次二次复杂度注意力替代方案](https://www.reddit.com/r/MachineLearning/comments/1vpt6ay/ssogattention_sum_of_separable_gaussians_as_a/) ⭐️ 8.0/10

SSOG-Attention 用每头少量可学习的高斯原子替代缩放点积注意力（SDPA），根据查询令牌从几何上调整这些原子，而不再计算所有查询-键相似度。它将复杂度降至 O(N·√N·d)，并宣称在 CIFAR-100 和 ImageNet 基准上达到或超过 SDPA 的表现。 它解决了标准注意力 O(N²·d) 的扩展瓶颈，该瓶颈限制了 Transformer 在长序列和高分辨率图像上的效率。如果得到验证，SSOG 可在更大规模上实现更快、更省内存的视觉 Transformer，并提供开源实现供社区检验。 这些高斯原子被分解为可分离的高斯和，从而实现复杂度降低，同时通过有界的小偏移保持基于内容的引导。项目提供了博客文章和 GitHub 仓库，包含实验与消融结果；部分代码和文本使用了 AI 辅助，但作者声明对全部内容负责。

reddit · r/MachineLearning · /u/4rtemi5 · 8月16日 10:06

**背景**: 缩放点积注意力（SDPA）由《Attention Is All You Need》提出，需要计算所有查询与键之间的两两相似度，因此代价为 O(N²·d)，在输入规模增大时难以承受。可分离滤波器或核可分解为低维运算，这正是高斯核分解能减少计算量的原因。SSOG 将这一思想应用于注意力，把每个注意力头的分布建模为可分离高斯之和，而不是显式的查询-键打分。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/4rtemi5/ssog">GitHub - 4rtemi5/ssog: SSOG - Attention : Near-linear Visual-Attention...</a></li>
<li><a href="https://www.openai-hub.com/news/1620/">SSOG - Attention ... - OpenAI Hub</a></li>
<li><a href="https://uxlfoundation.github.io/oneDNN/dev_guide_graph_sdpa.html">Scaled Dot-Product Attention (SDPA) — oneDNN v3.14.0 documentation</a></li>

</ul>
</details>

**标签**: `#attention`, `#efficient transformers`, `#sub-quadratic`, `#machine learning`, `#Gaussian`

---

<a id="item-7"></a>
## [重新审视 ECA：跨通道交互假设受到质疑](https://www.reddit.com/r/MachineLearning/comments/1vptaw9/revisiting_the_efficient_channel_attention_paper/) ⭐️ 8.0/10

一篇 Reddit 分析文章指出，高效通道注意力（ECA）论文的核心主张——跨通道交互是关键——在概念上存在缺陷，且实验结果并不能完全支持这一论点。作者在象棋残局表库数据上证明，核大小为 k=3 的 ECA 与 k=1（无跨通道交互）以及简单的逐通道门控表现相近。 这一批评挑战了被高度引用（约 1.2 万次引用）的注意力机制背后所普遍接受的假设，可能影响未来关于高效注意力设计的研究。它也提醒人们，设计原理是否真正得到受控实验验证很重要，而不仅仅看最终准确率。 作者使用 6 子象棋残局表库而非图像数据集，理由是它可以对完整底层问题进行无偏采样。ECA（k=3）的测试准确率为 96.68%，优于 SE 的 96.17%，但 ECA（k=1）也达到 96.61%，逐通道门控达 96.65%，这削弱了“跨通道交互必不可少”的论断。

reddit · r/MachineLearning · /u/arkuto · 8月16日 10:13

**背景**: Squeeze-and-Excitation（SE）模块通过压缩空间维度并使用瓶颈层建模通道依赖，来重新校准通道特征。ECA-Net（CVPR 2020）避免了降维，直接对通道均值做小核一维卷积，并认为适当的跨通道交互能以更少参数保持性能。然而，该 Reddit 作者指出，在通道维度上做一维卷积假定了通道间存在局部性和顺序性，而这种顺序性可能并不存在，类似于把 CNN 用在表格数据上。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/1910.03151">[1910.03151] ECA-Net: Efficient Channel Attention for Deep Convolutional Neural Networks</a></li>
<li><a href="https://arxiv.org/abs/1709.01507">[1709.01507] Squeeze-and-Excitation Networks</a></li>

</ul>
</details>

**标签**: `#attention`, `#efficient channel attention`, `#deep learning`, `#research critique`, `#machine learning`

---

<a id="item-8"></a>
## [Anthropic 第二季营收暴涨 14 倍，超 115 亿美元](https://www.cnbc.com/2026/08/15/anthropic-revenue-jumps-to-over-11point5-billion-in-q2-report.html) ⭐️ 8.0/10

Anthropic 第二季初步营收超过 115 亿美元，同比增长逾 14 倍，去年同期为 7.87 亿美元。该公司当季调整后营业利润转正，并正筹备可能在今秋启动的 IPO。 这一财务里程碑表明，领先的 AI 实验室不仅能大规模投入，也能实现快速商业化和盈利。这也为今年最受关注的科技 IPO 之一奠定基础，可能影响整个 AI 板块的投资者情绪。 据彭博社援引文件称，这些数字为初步数据，仍可能调整。环比增速同样惊人：2026 年第一季营收为 47.3 亿美元，而第二季营收环比增长了一倍以上。

telegram · zaihuapd · 8月16日 07:26

**背景**: Anthropic 是一家领先的 AI 公司，其财务表现受到 AI 行业的密切关注。「调整后营业利润」通常剔除一次性成本和股权激励费用，以反映持续经营业务的盈利能力；「初步营收」则指数字在最终报告前仍可能调整。据报道，该公司正在筹备可能于今年秋季启动的大型 IPO。

**标签**: `#Anthropic`, `#AI industry`, `#Revenue`, `#IPO`, `#Business news`

---