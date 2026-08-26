---
layout: default
title: "Horizon Summary: 2026-08-26 (ZH)"
date: 2026-08-26
lang: zh
---

> 从 42 条内容中筛选出 13 条重要资讯。

---

1. [苹果发布 M6 与 M5 Ultra 芯片，AI 算力大幅跃升](#item-1) ⭐️ 9.0/10
2. [OpenAI 自研芯片 Jalapeño 测试表现据称超越 Nvidia Blackwell](#item-2) ⭐️ 9.0/10
3. [FDA 批准首款可穿戴设备，同时连续监测酮体和血糖](#item-3) ⭐️ 8.0/10
4. [苹果发布搭载 M6 与 M5 Pro 芯片的新款 Mac mini](#item-4) ⭐️ 8.0/10
5. [Nitter 和 XCancel 收到 X 的停止函](#item-5) ⭐️ 8.0/10
6. [Firefox 157 将在所有平台上默认启用 JPEG XL](#item-6) ⭐️ 8.0/10
7. [SpaceX 宣布在路易斯安那州建设 Starbase LA 发射场](#item-7) ⭐️ 8.0/10
8. [EVE Online 启动大规模 Python 3 迁移，使用 Futurize](#item-8) ⭐️ 8.0/10
9. [在开放权重模型上持续学习，为 SovereignAI 提供可行路径](#item-9) ⭐️ 8.0/10
10. [SpaceX 计划于 2027 年将英伟达 Vera Rubin NVL72 送入轨道](#item-10) ⭐️ 8.0/10
11. [Qwen 预告 3.8-Flash-Next 开源，8 月 26 日发布](#item-11) ⭐️ 8.0/10
12. [特斯拉监督版 FSD 正式登陆中国](#item-12) ⭐️ 8.0/10
13. [英伟达 Vera Rubin NVL72 首测：DeepSeek 吞吐提升 30 倍](#item-13) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [苹果发布 M6 与 M5 Ultra 芯片，AI 算力大幅跃升](https://www.apple.com/newsroom/2026/08/apple-introduces-m6-and-m5-ultra-for-a-big-leap-in-performance-and-ai-compute/) ⭐️ 9.0/10

苹果于 2026 年 8 月 25 日发布了 M6 与 M5 Ultra 芯片。M6 是苹果首款 2nm 芯片，配备 12 核 CPU、12 核 GPU 和双 16 核神经引擎，而 M5 Ultra 则是苹果首款四芯片封装（quad-die）架构芯片，也是迄今最强的芯片。 这标志着苹果自研芯片的一次代际飞跃，性能和端侧 AI 算力大幅提升。所有 Mac 用户都将受到影响，也表明苹果正努力在 AI PC 时代保持竞争力；不过定价以及关于 M6 产品线的传闻引发了外界讨论。 M5 Ultra 采用四芯片封装（quad-die）架构，在 Mac Studio 中最高可配置 256GB 内存（512GB 版本稍后推出）和 16TB 存储。M6 基于 2nm 工艺，有报道称这是最后一代 Apple silicon 系统芯片，并猜测苹果可能会跳过 M6 Pro、M6 Max 和 M6 Ultra，专注于 AI 能力更强的 M7。

hackernews · interpol_p · 8月25日 13:01 · [社区讨论](https://news.ycombinator.com/item?id=49433292)

**背景**: Apple silicon 是苹果基于 ARM 架构设计的系统级芯片（SoC），在同一封装内集成 CPU、GPU、神经引擎（Neural Engine）和统一内存。神经引擎用于加速机器学习任务，是端侧 AI 算力的关键。2nm 指晶体管的制造工艺，比前代更小，能带来更高的性能和能效。M5 Ultra 是苹果首款四芯片封装（quad-die）设计，通过组合多个 die 实现更强性能。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.apple.com/newsroom/2026/08/apple-introduces-m6-and-m5-ultra-for-a-big-leap-in-performance-and-ai-compute/">Apple introduces M6 and M5 Ultra for a big leap in ...</a></li>
<li><a href="https://en.wikipedia.org/wiki/Apple_M6">Apple M6 - Wikipedia</a></li>
<li><a href="https://www.pcmag.com/news/apple-m5-ultra-and-m6-silicon-explained">Apple M5 Ultra and M6 Silicon Explained: 2nm Tech ... - PCMag</a></li>

</ul>
</details>

**社区讨论**: 评论区对性能提升普遍感到兴奋，有用户表示在从 M1 Pro 换机后，试用 M5 Pro 时感觉速度提升明显。不过不少人指出定价高昂：一台顶配 M5 Ultra Mac Studio 已要价 18,299 美元，传闻中的 512GB 版本可能超过 24,000 美元。也有用户讨论彭博社关于苹果可能跳过 M6 Pro/Max/Ultra、全力开发 AI 芯片 M7 的报道，观点不一。还有人开玩笑说这让人想起 90 年代末的处理器竞赛。

**标签**: `#Apple Silicon`, `#Hardware`, `#AI compute`, `#Processors`, `#Mac`

---

<a id="item-2"></a>
## [OpenAI 自研芯片 Jalapeño 测试表现据称超越 Nvidia Blackwell](https://newsletter.semianalysis.com/p/openai-jalapeno-better-than-nvidia) ⭐️ 9.0/10

OpenAI 发布了与 Broadcom 联合设计的自研推理 ASIC“Jalapeño”，初步测试据称在性能上超越了 Nvidia 旗舰 Blackwell 处理器。SemiAnalysis 的通讯文章详细对比了总拥有成本（TCO）、每兆瓦吞吐量以及与 Nvidia Rubin 架构的裸片尺寸。 这可能是 AI 硬件领域的范式转变，意味着头部 AI 实验室能够凭借面向推理的专用芯片挑战 Nvidia 近乎垄断的地位。如果 Jalapeño 兑现其宣称的成本与性能优势，将可能重塑大规模 LLM 推理服务的经济性，并降低整个行业对 Nvidia GPU 的依赖。 Jalapeño 是专为 LLM 推理设计的定制 ASIC，而非通用 GPU，据报道它对应 OpenAI 到 2029 年 10 GW 的基础设施承诺。社区评论指出，对比表格省略了裸片尺寸——其尺寸与 Rubin 大致相当，但 NVFP4 PFLOPs 仅为 Nvidia 的约三分之一，并讨论了 FP4 精度的使用。

hackernews · Semianalysis · 8月25日 14:06 · [社区讨论](https://news.ycombinator.com/item?id=49434378)

**背景**: Nvidia 的 Blackwell 架构是 Hopper 和 Ada Lovelace 的继任者，采用台积电 4NP 工艺，集成 2080 亿个晶体管，并为 AI 工作负载带来了显著的能效提升。OpenAI 的 Jalapeño 属于行业向定制芯片迈进的更广泛趋势，这类专用推理 ASIC 旨在降低大模型服务的成本和功耗。2026 年 8 月的彭博社文章首先报道了 OpenAI 的主张，随后 SemiAnalysis 进行了深入的技术分析。这一举动反映了头部 AI 实验室寻求替代通用数据中心 GPU 的日益增长的趋势。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.stork.ai/blog/jalapeo-openais-nvidia-killer">OpenAI 's Jalapeño Chip : A Custom ASIC to Challenge... | Stork.AI</a></li>
<li><a href="https://www.spheron.network/blog/openai-jalapeno-chip-gpu-cloud-inference-2026/">OpenAI Jalapeño Chip Explained: What... | Spheron Blog</a></li>
<li><a href="https://en.wikipedia.org/wiki/Blackwell_(microarchitecture)">Blackwell (microarchitecture) - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 评论者总体上很感兴趣，但看法不一：有人猜测未来可能直接将 LLM 权重烧录进芯片，也有人将方兴未艾的推理芯片格局比作早期 3dfx/Riva 显卡之争。还有多人提出了技术性质的保留意见，质疑 FP4 精度，并指出裸片尺寸的换算看起来并不像头条数字那么亮眼。少数评论还称赞 SemiAnalysis 对这一万亿美元级别的行业做出了非传统而又世界级的分析。

**标签**: `#AI hardware`, `#OpenAI`, `#Nvidia`, `#chip design`, `#inference`

---

<a id="item-3"></a>
## [FDA 批准首款可穿戴设备，同时连续监测酮体和血糖](https://www.fda.gov/news-events/press-announcements/fda-authorizes-first-wearable-device-continuously-monitors-both-ketone-levels-and-blood-sugar) ⭐️ 8.0/10

美国食品和药物管理局（FDA）批准了首款可同时连续监测酮体水平和血糖的可穿戴设备。这一监管里程碑在 FDA 官网公布，标志着代谢健康监测领域的重大突破。 这可能显著改善糖尿病（尤其是 1 型糖尿病）的管理，让患者通过单一设备实时追踪两项关键代谢指标。它还为可穿戴生物传感器在慢病管理和代谢健康领域的更广泛应用铺平了道路。 该设备将连续血糖监测（CGM）与连续酮体监测（CKM）集成在一起，可实时提供两项生物标志物的数据。酮体是脂肪代谢的产物，其水平可提示糖尿病酮症酸中毒（一种危险并发症）或低碳水饮食导致的营养性生酮状态。

hackernews · sunnynagra · 8月25日 19:07 · [社区讨论](https://news.ycombinator.com/item?id=49439017)

**背景**: 传统上，糖尿病患者通过指尖血糖仪测量血糖，并通过尿试纸或血液检测来测量酮体。连续血糖监测仪已经普及，但连续酮体监测是一项较新的技术。此次 FDA 批准将两者整合进一个可穿戴传感器，有望让日常代谢监测更简便、更全面。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Ketone_bodies">Ketone bodies</a></li>
<li><a href="https://beyondtype1.org/ketone-monitoring-timeline/">From Urine Strips to Continuous Monitoring : The Evolution of Ketone ...</a></li>
<li><a href="https://ckmonitors.com/">Wearable Continuous Ketone Monitors | CKMonitors</a></li>

</ul>
</details>

**社区讨论**: 评论者们的情绪既有个人共鸣，也有怀疑。有人分享了朋友因糖尿病酮症酸中毒去世的个人经历，也有人称赞佩戴类似 CGM 设备的便利性。其他人则质疑该设备的准确性、对普通糖尿病患者的实用性，并担心成本和保险报销问题。

**标签**: `#FDA`, `#wearables`, `#diabetes`, `#ketone-monitoring`, `#health-tech`

---

<a id="item-4"></a>
## [苹果发布搭载 M6 与 M5 Pro 芯片的新款 Mac mini](https://www.apple.com/newsroom/2026/08/apple-unveils-a-more-powerful-mac-mini-featuring-the-all-new-m6-and-m5-pro/) ⭐️ 8.0/10

苹果发布了搭载全新 M6 和 M5 Pro 芯片的新一代 Mac mini，起售价有所提高。这一发布标志着其告别此前超性价比的入门定位。 这一点很重要，因为 Mac mini 长期以来都是苹果最平价的 macOS 入门选择，大幅涨价可能会影响预算有限的用户和小型企业。搭载 2nm 的 M6 芯片也表明苹果持续投入端侧 AI 性能。 M6 是苹果首款 2 纳米制程芯片，配备双 16 核神经引擎；M5 Pro 则最高提供 18 核 CPU 和 20 核 GPU，内存带宽达 307GB/s。据社区反馈，基础机型在欧洲的售价已突破 1000 欧元大关。

hackernews · runako · 8月25日 13:13 · [社区讨论](https://news.ycombinator.com/item?id=49433450)

**背景**: Mac mini 自 2005 年以来一直是苹果紧凑、平价的台式机，2020 年起采用 Apple Silicon，首款为 M1 芯片。M 系列芯片是苹果基于 ARM 架构的片上系统，集成了 CPU、GPU 和统一内存。M5 Pro 此前已于 2026 年 3 月随 MacBook Pro 发布，而 M6 则实现了向 2 纳米制程的跃迁。本次发布延续了苹果在整个 Mac 产品线中从 Intel 向自研芯片过渡的策略。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.apple.com/newsroom/2026/08/apple-introduces-m6-and-m5-ultra-for-a-big-leap-in-performance-and-ai-compute/">Apple introduces M6 and M5 Ultra for a big leap in performance and AI compute - Apple</a></li>
<li><a href="https://www.macrumors.com/2026/08/25/apple-reveals-m6/">Apple Reveals M6 as First-Ever 2nm Chip - MacRumors</a></li>
<li><a href="https://en.wikipedia.org/wiki/Apple_M5">Apple M5 - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 评论者对之前 499 美元的 M4 Mac mini 表示怀念，并对欧洲基础款售价超过 1000 欧元感到失望。有人质疑拿 M6 与 M1 比较的基准测试意义，认为应对比 M5 Pro；还有用户对“常驻式智能体计算”的宣传口号感到不安。

**标签**: `#Apple`, `#Mac mini`, `#M6`, `#M5 Pro`, `#Hardware`

---

<a id="item-5"></a>
## [Nitter 和 XCancel 收到 X 的停止函](https://github.com/zedeus/nitter/issues/1442) ⭐️ 8.0/10

X 已向隐私友好的替代前端 Nitter 和 XCancel 发出了停止函。目前所有 Nitter 实例均已下线，预计在可预见的未来将保持关闭，项目方正等待法律建议。 此事威胁到隐私保护型 X 内容浏览工具的存续，影响注重隐私的用户、研究人员以及无法正常访问 X 的人群。同时也标志着开源生态中第三方前端面临的法律压力加大。 在 Nitter 的 GitHub issue 中，项目方仅表示已收到停止函，细节不多，正在等待法律建议，所有已知实例目前均保持离线。Nitter 曾是流行的 Twitter 替代前端，XCancel 也提供类似的可匿名浏览 X 公开主页和帖子的服务。

hackernews · Banditoz · 8月25日 17:08 · [社区讨论](https://news.ycombinator.com/item?id=49437283)

**背景**: Nitter 是一个开源的 Twitter/X 替代前端，让用户无需 JavaScript、广告或 IP 追踪即可浏览推文，深受隐私倡导者欢迎。XCancel 提供类似功能，通过替代界面查看 X 的公开主页和帖子。在 X 限制匿名访问并要求登录后，这些工具变得更加重要。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Nitter">Nitter - Wikipedia</a></li>
<li><a href="https://github.com/zedeus/nitter">GitHub - zedeus/nitter: Alternative Twitter front-end · GitHub</a></li>
<li><a href="https://85ideas.com/blog/what-is-xcancel-complete-guide-explanation/">What Is XCancel? Complete Guide & Explanation - 85ideas.com</a></li>

</ul>
</details>

**社区讨论**: 评论区普遍表示失望，部分用户称宁愿不再阅读 X 内容也不愿登录。也有用户呼吁转移到 Mastodon、Bluesky 等去中心化平台，还有人建议非美司法管辖区为这类项目提供法律保护以对抗美国科技公司。

**标签**: `#open-source`, `#privacy`, `#legal`, `#nitter`, `#twitter`

---

<a id="item-6"></a>
## [Firefox 157 将在所有平台上默认启用 JPEG XL](https://groups.google.com/a/mozilla.org/g/dev-platform/c/3YMV4MS34KA?pli=1) ⭐️ 8.0/10

Mozilla 宣布 Firefox 157 将在所有平台上默认启用 JPEG XL，标志着该格式在跨浏览器采用方面迈出了重要一步。此举使 Firefox 与 Chromium 的相关行动保持一致。 Firefox 和 Chromium 的默认支持可能会加速 JPEG XL 成为网络上下一代标准图像格式。如果苹果也跟进，JPEG XL 可能在几年内取代传统 JPEG 成为常见应用格式。 该公告发布在 Mozilla 的 dev-platform 邮件列表上，Firefox 157 是浏览器的一个未来版本。值得注意的是，社区讨论强调 Firefox 和 Chromium 都在利用基于 Rust 的 jxl-rs 库来支持 JPEG XL。

hackernews · yboris · 8月25日 17:55 · [社区讨论](https://news.ycombinator.com/item?id=49437946)

**背景**: JPEG XL 是由联合图像专家组（JPEG）与 Google 和 Cloudinary 合作开发的下一代图像格式。它支持有损和无损压缩，旨在提供比 PNG、JPEG 和 WebP 等现有格式更高的压缩率和更好的质量。JPEG XL 还能无缝转码传统 JPEG 文件，使其成为实用的替代品。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/JPEG_XL">JPEG XL - Wikipedia</a></li>
<li><a href="https://jpegxl.info/index.html">JPEG XL : Superior Image Compression</a></li>

</ul>
</details>

**社区讨论**: 公告下方的评论对 JPEG XL 的潜力表示兴奋，一些用户希望在几年内所有人都能告别 JPEG。还有人提到 Chrome 也在进行类似的支持，同时一些评论提出了关于处理不支持 JPEG XL 的上传字段的实际问题，并对苹果对 Rust 库的态度表示好奇。

**标签**: `#JPEG XL`, `#Firefox`, `#web standards`, `#image formats`, `#browser`

---

<a id="item-7"></a>
## [SpaceX 宣布在路易斯安那州建设 Starbase LA 发射场](https://www.spacex.com/sites/starbase-la) ⭐️ 8.0/10

SpaceX 在数月的猜测之后，正式宣布将在路易斯安那州新建 Starbase LA 火箭发射场。该发射场旨在支持未来的发射任务，被视为 SpaceX 在得克萨斯州设施之外的重要扩张。 这一公告意义重大，因为它代表着 SpaceX 基础设施的重大扩张，并可能为美国最贫困的沿海地区之一带来可观的经济增长。该地的纬度也可能提供轨道优势，特别是对于太阳同步轨道任务。 社区讨论指出，从路易斯安那州向太阳同步轨道发射时，发射角约为相对于赤道的 98°，大致朝正南方向。观察者还注意到公告页面上的文案问题，其中关于海岸线恢复和沼泽重建的两段文字几乎完全相同，第一句话也一模一样。

hackernews · bilsbie · 8月25日 16:37 · [社区讨论](https://news.ycombinator.com/item?id=49436822)

**背景**: Starbase 是 SpaceX 在得克萨斯州现有的工业园区和火箭发射设施，是 Starship 运载器的主要生产和测试地点，也是公司的总部。发射场纬度是轨道力学中的一个重要因素，因为它影响可达到的轨道倾角以及火箭能借用的地球自转速度。较低纬度的发射场通常更有利于赤道轨道，而较高纬度的发射场可能对某些极地轨道和太阳同步轨道更有利。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/SpaceX_Starbase">SpaceX Starbase - Wikipedia</a></li>
<li><a href="https://builtin.com/articles/starbase-spacex-elon-musk">What Is Starbase? Elon Musk’s Controversial New City | Built In</a></li>
<li><a href="https://www.quora.com/Why-is-the-ideal-orbital-inclination-for-launch-equal-to-the-latitude-of-the-launch-site-I-understand-that-both-the-COM-of-the-Earth-and-the-launch-site-have-to-be-included-in-the-plane-but-the-earth-does-not">Why is the ideal orbital inclination for launch equal to the latitude of the launch site? I understand that both the COM of the Earth and the launch site have to be included in the plane, but the earth does not necessarily rotate at that angle. - Quora</a></li>

</ul>
</details>

**社区讨论**: 评论区总体积极，强调了该经济萧条地区获得长期建设和技工就业机会的潜力，并对美国出现雄心勃勃的现实项目表示兴奋。一些评论者确认当地房地产经纪人在 5 月就预测到了这一公告，Ars Technica 也在早些时候报道过相关传闻；另一些人则批评页面文案重复，并调侃该网站的真实性。

**标签**: `#SpaceX`, `#Starbase`, `#Louisiana`, `#Space Industry`, `#Infrastructure`

---

<a id="item-8"></a>
## [EVE Online 启动大规模 Python 3 迁移，使用 Futurize](https://simonwillison.net/2026/Aug/25/eve-online-move-to-python-3/) ⭐️ 8.0/10

EVE Online 宣布启动期待已久的从 Stackless Python 2.7 到 Python 3 的迁移，利用 futurize 脚本处理 240 万行代码。此次升级需手动审查约 20,000 处 Python 2 与 Python 3 行为差异的地方。 此次迁移意义重大，因为 EVE Online 是生产环境中规模最大、运行时间最长的 Python 代码库之一，为 Python 3 采用提供了宝贵的现实案例。其成功或失败可能影响其他遗留 Stackless Python 项目如何进行现代化改造。 公告未说明如何替换 Stackless，但去年的 EVE Frontier 演示描述了使用开源的 carbonengine/scheduler 库取代 Stackless。迁移使用 futurize，该工具可自动将 Python 2 代码重写为 Python 2/3 兼容，随后手动审查整数除法等语义差异。

rss · Simon Willison · 8月25日 22:59

**背景**: Stackless Python 是 Python 的增强版本，避免依赖 C 调用栈，支持称为 tasklet 的微线程，允许并发运行数十万个任务。EVE Online 自 2003 年上线以来一直运行在 Stackless Python 上，上一次重大升级是 2010 年的 Stackless Python 2.7。Python 2 已于 2020 年停止维护，而 Stackless Python 本身也已正式停止开发，其 GitHub 仓库于 2025 年 2 月归档。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Stackless_Python">Stackless Python</a></li>
<li><a href="https://python-future.org/futurize.html">futurize : Py2 to Py2/3 — Python -Future documentation</a></li>

</ul>
</details>

**标签**: `#Python`, `#EVE Online`, `#Migration`, `#Stackless Python`, `#Futurize`

---

<a id="item-9"></a>
## [在开放权重模型上持续学习，为 SovereignAI 提供可行路径](https://www.reddit.com/r/MachineLearning/comments/1vxvzju/continual_learning_of_frontier_models_for/) ⭐️ 8.0/10

TRI-FAIR 实验室发布的技术报告提出，预算有限的机构可以通过在现有开放权重模型上进行持续学习，达到前沿模型性能。报告还发布了名为 Thomson 的通用前沿开放权重模型，重点面向高风险专业任务，技术报告与权重均已公开。 这一观点挑战了“前沿 AI 只有少数资金雄厚的实验室才能实现”的固有认知，为更广泛的机构提供了实现主权 AI（SovereignAI）的具体技术路径。若经实证验证，可能重塑 AI 治理格局，让更多主体拥有模型、工具、价值观与数据隐私的控制权。 该方法采用现代中段与后段训练（mid- & post-training）技术栈，并通过防护机制在训练各阶段保持可塑性与稳定性，声称可实现相当于跨越多个模型世代的性能提升。Thomson 的评估呈现独特的“π形”模式：在众多能力上广泛提升，同时几乎消除了常见于窄域适配的灾难性遗忘，且计算与人力成本显著更低。

reddit · r/MachineLearning · /u/Forsaken_Scientist · 8月25日 10:30

**背景**: 持续学习（continual learning）是一种 AI 训练范式，让模型在依次学习新任务的同时保留已有知识，避免朴素微调中常见的“灾难性遗忘”。开放权重模型（open-weight model）提供可下载、可微调的已训练权重，但不一定公开全部训练数据，这与真正意义上的开源 AI 有所不同。主权 AI（SovereignAI）指一个组织独立构建、部署并治理自身 AI 系统的能力；此前人们普遍认为只有少数巨头才能做到这一点。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.ibm.com/think/topics/continual-learning">What is continual learning? - IBM</a></li>
<li><a href="https://www.geeksforgeeks.org/machine-learning/continual-learning-in-machine-learning/">Continual Learning in Machine Learning - GeeksforGeeks</a></li>

</ul>
</details>

**标签**: `#continual-learning`, `#open-models`, `#frontier-ai`, `#AI-democratization`, `#technical-report`

---

<a id="item-10"></a>
## [SpaceX 计划于 2027 年将英伟达 Vera Rubin NVL72 送入轨道](https://www.theregister.com/off-prem/2026/08/25/spacex-claims-it-will-put-a-vera-rubin-nvl72-rack-scale-system-into-orbit-next-year/5292067) ⭐️ 8.0/10

SpaceX 宣布计划于 2027 年将一套英伟达 Vera Rubin NVL72 机架级 AI 系统送入轨道，用于测试太空数据中心技术。这将是首次在太空中部署机架级 AI 超级计算机。 如果成功，这项任务将为在太空中处理 AI 任务的轨道数据中心铺平道路，减少对地面基础设施的依赖。它还可能通过在恶劣太空环境中演示高性能计算，对 AI 和航天产业产生深远影响。 NVL72 系统由 72 颗 Rubin GPU 和 36 颗 Vera CPU 组成，功耗超过 100 千瓦，通常需要复杂的液冷和供电设施。SpaceX 尚未公布具体发射时间、轨道高度以及系统在太空中的供电和冷却方案。

telegram · zaihuapd · 8月25日 08:03

**背景**: 英伟达 Vera Rubin NVL72 是一款机架级 AI 超级计算机，集成了 72 颗 Rubin GPU 和 36 颗 Vera CPU，可为智能体式 AI 及超大规模训练和推理提供算力。轨道数据中心被视为在地球之外扩展算力的潜在途径，但面临发射成本、供电和散热、辐射防护以及轨道碎片等多重挑战。布鲁金斯学会指出，太空维护困难、设施体积重量和成本也进一步阻碍了部署。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.nvidia.com/en-us/data-center/vera-rubin-nvl72/">NVIDIA Vera Rubin NVL72 | Co-Designed Infrastructure for Agentic AI</a></li>
<li><a href="https://www.brookings.edu/articles/orbital-data-centers-feasibility-gap-is-a-governance-risk/">Orbital data centers' feasibility gap is a governance risk | Brookings</a></li>
<li><a href="https://en.wikipedia.org/wiki/Space-based_data_center">Space-based data center - Wikipedia</a></li>

</ul>
</details>

**标签**: `#SpaceX`, `#Nvidia`, `#AI computing`, `#orbital data center`, `#space technology`

---

<a id="item-11"></a>
## [Qwen 预告 3.8-Flash-Next 开源，8 月 26 日发布](https://www.modelscope.cn/models/Qwen/Qwen3.8-Flash-Next) ⭐️ 8.0/10

Qwen 宣布即将开源 Qwen3.8-Flash-Next，这是一个基于下一代 Qwen4 架构的多模态混合专家（MoE）模型。该模型将于 2026 年 8 月 26 日 23:00（UTC+8）在 ModelScope 上提供下载，包括标准版和 FP8 版本。 此次发布让开发者提前接触到将驱动未来 Qwen4 系列的架构，使社区能够提前准备和构建。作为一个开源权重多模态 MoE 模型，它可能通过设定对 Qwen4 能力和性能的预期，对 AI 生态产生重大影响。 该模型是多模态的，采用混合专家（MoE）架构，计划于 2026 年 8 月 26 日发布。将提供两个版本：标准版和 FP8 版，以满足不同的部署需求。

telegram · zaihuapd · 8月25日 12:59

**背景**: 混合专家（MoE）是一种机器学习技术，将模型划分为多个专家网络，由路由器根据输入仅激活其中的子集，从而在不按比例增加计算成本的情况下高效扩展模型规模。FP8 是一种低精度浮点格式，可减少内存占用并加速兼容硬件上的推理。Qwen 是阿里巴巴开发的一系列大语言模型，Qwen3.8-Flash-Next 是即将推出的 Qwen4 架构的技术预览版。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Mixture_of_experts">Mixture of experts - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Qwen">Qwen - Wikipedia</a></li>

</ul>
</details>

**标签**: `#Qwen`, `#MoE`, `#open-source`, `#LLM`, `#ModelScope`

---

<a id="item-12"></a>
## [特斯拉监督版 FSD 正式登陆中国](https://t.me/zaihuapd/43397) ⭐️ 8.0/10

特斯拉在 X 平台发文宣布，监督版完全自动驾驶（FSD）现已在中国可用，标志着该功能正式进入中国市场。 此次发布是中国自动驾驶商业化的重要里程碑，可能加速 AI/ML 在汽车领域的应用，并加剧与本土自动驾驶厂商的竞争。 特斯拉的监督版 FSD 仍要求驾驶员全程保持注意力并随时准备接管，并非完全自动驾驶。此次公告未提供太多技术细节，关于中国市场的监管审批和定价信息尚未公布。

telegram · zaihuapd · 8月25日 13:42

**背景**: 监督版完全自动驾驶（FSD）是特斯拉的高级驾驶辅助系统，利用摄像头提供 360 度视野，在驾驶员监督下处理常见驾驶任务。'监督版'这一措辞表明，尽管名为'完全自动驾驶'，当前系统仍属于 L2 级自动驾驶，需要驾驶员持续关注路况。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.tesla.com/fsd">Full Self-Driving (Supervised) - Tesla</a></li>
<li><a href="https://electrek.co/2024/03/28/tesla-supervised-full-self-driving-language/">Tesla starts using ' Supervised Full Self - Driving ' language | Electrek</a></li>
<li><a href="https://en.wikipedia.org/wiki/Tesla_Autopilot">Tesla Autopilot - Wikipedia</a></li>

</ul>
</details>

**标签**: `#Tesla`, `#FSD`, `#autonomous driving`, `#AI`, `#China`

---

<a id="item-13"></a>
## [英伟达 Vera Rubin NVL72 首测：DeepSeek 吞吐提升 30 倍](https://blogs.nvidia.com/blog/vera-rubin-nvl72-efficiency-ai-agents/) ⭐️ 8.0/10

英伟达首次公布了下一代机柜级系统 Vera Rubin NVL72 的片上基准测试结果：在 DeepSeek-V4-Pro 智能体编码任务上，每兆瓦吞吐量较 GB300 最高提升 30 倍，每百万 Token 成本最高下降 35 倍。该公司还宣布推理加速芯片 Groq 3 LPX 进入量产，并发布面向 AI 智能体的 Vera CPU。 这些结果标志着 AI 推理效率和 Token 经济性的重大飞跃，将使大规模智能体工作负载变得更加廉价和节能。数据中心运营商和企业可能看到运营成本大幅下降，同时英伟达在 AI 基础设施领域的竞争优势得到进一步巩固。 基准测试以 Blackwell 上一代产品 GB300 为对比对象，使用 DeepSeek-V4-Pro 执行智能体编码任务，衡量每兆瓦吞吐量和每百万 Token 成本。Groq 3 LPX 运行 Gemma 4 31B 时输出速度达每秒 3400 Token，SpaceXAI 计划在 2028 年前将 Vera CPU 机柜部署到太空。

telegram · zaihuapd · 8月25日 14:48

**背景**: Vera Rubin NVL72 是英伟达下一代机柜级 AI 超级计算机，基于第三代 MGX NVL72 设计，通过第六代 NVLink 将 72 颗 Rubin GPU 与 36 颗 Vera CPU 统一为共享内存池。它被定位为面向大规模训练和推理的交钥匙解决方案，每百万 Token 推理成本较上一代 Blackwell 降低十分之一。Groq 3 LPX 是与 Vera Rubin 平台协同设计的低延迟推理加速器，而 Vera CPU 采用 Olympus 内核，针对智能体工作负载优化单线程性能。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.nvidia.com/en-us/data-center/vera-rubin-nvl72/">Rack-Scale Agentic AI Supercomputer | NVIDIA Vera Rubin NVL72</a></li>
<li><a href="https://developer.nvidia.com/blog/inside-nvidia-groq-3-lpx-the-low-latency-inference-accelerator-for-the-nvidia-vera-rubin-platform/">Inside NVIDIA Groq 3 LPX: The Low-Latency Inference Accelerator for the NVIDIA Vera Rubin Platform | NVIDIA Technical Blog</a></li>
<li><a href="https://www.nvidia.com/en-us/data-center/vera-cpu/">Next Gen Data Center CPU | NVIDIA Vera CPU</a></li>

</ul>
</details>

**标签**: `#NVIDIA`, `#AI hardware`, `#DeepSeek`, `#data center`, `#inference`

---