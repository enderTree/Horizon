---
layout: default
title: "Horizon Summary: 2026-09-27 (ZH)"
date: 2026-09-27
lang: zh
---

> 从 26 条内容中筛选出 3 条重要资讯。

---

1. [DeepSeek 发布 DSec 沙箱平台，单集群可跑 38 万个并发沙箱](#item-1) ⭐️ 8.0/10
2. [SemiAnalysis 发布 Intel Panther Lake 与 18A 工艺免费拆解报告](#item-2) ⭐️ 8.0/10
3. [Excel 首次支持在一个单元格中存放多个值（列表与数组）](#item-3) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [DeepSeek 发布 DSec 沙箱平台，单集群可跑 38 万个并发沙箱](https://arxiv.org/abs/2609.22978) ⭐️ 8.0/10

DeepSeek 发布了一份关于 DeepSeek Elastic Compute（DSec）的技术报告，这是一个生产级沙箱平台，通过统一的 SDK 对外提供 FnCall、容器、microVM 和完整虚拟机四种沙箱后端。根据官方说明以及社区讨论，该系统仅用 160 个基于 Epyc 的服务器节点就支撑起了 38 万个并发沙箱。 一次性运行数十万个隔离环境，是大规模智能体训练与评测的核心瓶颈，因为模型必须执行自己生成的、不可信的代码。DSec 让 DeepSeek 直接与 Google 开源的 AX 智能体运行时以及 Modal 等商业沙箱服务商形成竞争，也说明沙箱基础设施正在成为 AI 技术栈中的一等公民。 该平台的关键设计是用同一套 SDK 抽象出四个隔离层级——从轻量的函数调用一直到完整的虚拟机——让不同负载可以在隔离强度、启动延迟和单节点密度之间做权衡。值得注意的是，这篇论文的作者名单异常之长，社区成员数出共有 131 位作者，这本身也成了讨论话题。

hackernews · shenli3514 · 9月26日 18:22 · [社区讨论](https://news.ycombinator.com/item?id=49859112)

**背景**: 沙箱指的是把代码放在一个隔离、可随时丢弃的环境中运行，使其无法破坏宿主机或泄露数据。随着大语言模型智能体越来越多地编写并执行自己的代码，各家实验室需要快速拉起海量此类环境，通常借助 microVM（轻量级虚拟机）或容器来实现。Google 的 AX（Agent Executor）是一个开源的分布式智能体运行时，可在规模上对智能体任务进行沙箱化；Modal 也公开了其扩展到百万级并发沙箱的设计，因此并发沙箱吞吐量已成为 AI 基础设施的一项竞争性指标。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/2609.22978">[2609.22978] DeepSeek Elastic Compute ( DSec ): A Sandbox...</a></li>
<li><a href="https://www.techzine.eu/news/devops/141577/google-launches-open-source-runtime-for-ai-agents/">Google launches open-source runtime for AI agents - Techzine Global</a></li>
<li><a href="https://modal.com/blog/scaling-to-1-million-concurrent-sandboxes-in-seconds">Scaling to 1 million concurrent sandboxes in seconds - Modal</a></li>

</ul>
</details>

**社区讨论**: 评论区最先被规模数字震撼，有人称在 160 个 Epyc 节点上跑 38 万个并发沙箱是「疯狂之举」，也有人指出该系统与 Google 正在打造的 AX 颇为相似。另一个反复出现的话题是这篇论文有 131 位作者，读者打趣说相比技术内容，这么多作者如何协作沟通反而更有意思，并猜测把每位员工都列上是一种人才保留或「资产保护」策略，以免竞争对手知道该挖谁；还有评论者追问 DSec 是否本质上就是一种「智能体基底（agent substrate）」。

**标签**: `#DeepSeek`, `#distributed systems`, `#cloud infrastructure`, `#sandboxing`, `#AI agents`

---

<a id="item-2"></a>
## [SemiAnalysis 发布 Intel Panther Lake 与 18A 工艺免费拆解报告](https://newsletter.semianalysis.com/p/intel-panther-lake-teardown) ⭐️ 8.0/10

SemiAnalysis 通过其 STEEL 拆解实验室发布了一份关于 Intel Panther Lake 处理器与 Intel 18A 工艺节点的免费拆解报告。该报告深入剖析了 Intel 首款基于 18A 工艺量产客户端芯片的内部结构，对芯片本体与封装进行了细致分析。 Panther Lake 是 Intel 多年来最重要的客户端产品，因为它是首款基于 18A 节点出货的芯片，而 18A 正是 Intel 押注晶圆代工业务的核心工艺。对芯片进行独立的物理分析，能让工程师难得且可信地了解 18A 的 RibbonFET 与背面供电技术在实际硬件中是否兑现了承诺。 Panther Lake 采用分块（tile）设计：CPU 模块基于 Intel 18A 制造，图形模块采用由 Xe2（Battlemage）衍生而来的 Arc Xe3 架构，I/O 模块则由台积电 N6 工艺生产。核心配置因产品线而异，H 系列为 4+8+4 布局，低功耗型号则采用更小的 4+4 模块。

rss · Semianalysis · 9月26日 13:36

**背景**: Intel 18A 是 Intel 最先进的工艺节点，也是首个同时采用 RibbonFET 环绕栅极（GAA）晶体管与 PowerVia 背面供电技术并投入量产的节点。环绕栅极结构从四面包裹晶体管沟道，带来更好的控制能力和更低的漏电；背面供电则把供电线路移到晶体管下方，以缓解布线拥塞并提升能效。SemiAnalysis 运营着专门的拆解实验室（STEEL），通过实际拆解数据中心、AI 与客户端硬件，对真实芯片进行测量与成像，而非依赖厂商公布的规格。以 Core Ultra 系列 3 名义销售的 Panther Lake，是首款大规模量产并采用 18A 的客户端芯片。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Panther_Lake_(microprocessor)">Panther Lake (microprocessor) - Wikipedia</a></li>
<li><a href="https://www.tomshardware.com/pc-components/cpus/intels-pivotal-18a-process-is-making-steady-progress-but-still-lags-behind-yields-only-set-to-reach-industry-standard-levels-in-2027">Intel's pivotal 18A process is making steady progress, but still lags behind — yields only set to reach industry standard levels in 2027 | Tom's Hardware</a></li>
<li><a href="https://www.intel.com/content/www/us/en/foundry/process/18a.html">Intel 18A | See Our Biggest Process Innovation</a></li>

</ul>
</details>

**标签**: `#Intel`, `#semiconductors`, `#process technology`, `#hardware teardown`, `#Panther Lake`

---

<a id="item-3"></a>
## [Excel 首次支持在一个单元格中存放多个值（列表与数组）](https://techcommunity.microsoft.com/blog/microsoft365insiderblog/put-multiple-values-in-one-cell-with-lists-and-arrays-in-excel/4559395) ⭐️ 8.0/10

微软已面向 Windows 和 Mac 的 Beta 通道用户推送列表（Lists）、单元格内数组与嵌套数组功能，这是 Excel 诞生 40 年来首次允许一个单元格存放多个值。与此同时还新增了 FLATTEN、HAS、HASANY、HASALL 四个用于处理数组的新函数。 Excel 是全球使用最广泛的数据工具之一，打破“一个单元格只能有一个值”这一长期限制，可能改变数百万用户构建、筛选和分析表格的方式，减少对辅助列、文本分列和分隔符技巧的依赖。这也表明微软正在对 Excel 的核心数据模型进行现代化改造，而非仅仅增加表面功能。 用户可以通过 Ctrl+J 或「插入 > 列表」在一个单元格中写入以逗号或分号分隔的多个项目，并能按列表中的单项进行筛选和计算。像 =B2 这样引用列表可以将其中的值溢出到其他单元格，FLATTEN 可将区域展平为单列，HAS、HASANY、HASALL 则用于判断值是否存在；但这些都属于预览功能，正式发布前行为可能调整，因此微软建议暂不要用于重要工作簿。

telegram · zaihuapd · 9月26日 16:26

**背景**: 长期以来，Excel 的一个单元格只能承载一个值——一个数字、一个日期或一段文本，因此想在一个单元格里表示多个项目，只能借助分隔符文本配合 TEXTSPLIT 之类的函数或辅助列等变通做法。Excel 中的数组此前只作为公式结果溢出到一片区域，无法直接存放在单个单元格内。新增的 FLATTEN（把多个区域合并为一列）和 HAS 系列（判断列表是否包含某个值）等函数，正是为了让这种新的“列表式”数据模型能真正用于日常分析和筛选。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://techcommunity.microsoft.com/blog/microsoft365insiderblog/put-multiple-values-in-one-cell-with-lists-and-arrays-in-excel/4559395">Put multiple values in one cell with lists and arrays in Excel</a></li>
<li><a href="https://www.xelplus.com/excel-lists-in-cells/">Excel Lists in Cells: Put Multiple Values in One Cell</a></li>
<li><a href="https://www.neowin.net/news/excel-finally-supporting-multiple-values-in-single-cell-microsoft-explains-how/">Excel finally supporting multiple values in single cell... - Neowin</a></li>

</ul>
</details>

**标签**: `#Excel`, `#Microsoft`, `#Spreadsheet`, `#Data Analysis`, `#Feature Update`

---