---
layout: default
title: "Horizon Summary: 2026-09-27 (EN)"
date: 2026-09-27
lang: en
---

> From 26 items, 3 important content pieces were selected

---

1. [DeepSeek unveils DSec sandbox platform running 380,000 concurrent sandboxes](#item-1) ⭐️ 8.0/10
2. [SemiAnalysis Publishes Free Teardown of Intel Panther Lake and 18A](#item-2) ⭐️ 8.0/10
3. [Excel now stores multiple values in a single cell with lists and arrays](#item-3) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [DeepSeek unveils DSec sandbox platform running 380,000 concurrent sandboxes](https://arxiv.org/abs/2609.22978) ⭐️ 8.0/10

DeepSeek published a technical report on DeepSeek Elastic Compute (DSec), a production sandbox platform that exposes FnCall, container, microVM, and full-VM backends through a unified SDK. According to the announcement and community discussion, the system sustains 380,000 concurrent sandboxes across only 160 Epyc-based server nodes. Running hundreds of thousands of isolated environments at once is the core bottleneck for large-scale agentic training and evaluation, where models must execute untrusted generated code. DSec puts DeepSeek in direct competition with Google's open-source AX agent runtime and commercial sandbox providers such as Modal, signalling that sandbox infrastructure is becoming a first-class layer of the AI stack. The platform's key design choice is a single SDK that abstracts four isolation levels — from lightweight function calls up to full virtual machines — letting workloads trade isolation strength against startup latency and per-node density. Notably, the paper carries an unusually long author list, with community members counting 131 names, which itself became a talking point.

hackernews · shenli3514 · Sep 26, 18:22 · [Discussion](https://news.ycombinator.com/item?id=49859112)

**Background**: Sandboxing means running code inside an isolated, disposable environment so it cannot damage the host or leak data. As LLM agents increasingly write and execute their own code, labs need to spin up enormous numbers of such environments quickly, typically using microVMs (lightweight virtual machines) or containers. Google's AX (Agent Executor) is an open-source distributed agent runtime that sandboxes agent tasks at scale, and Modal has published its own design for scaling to a million concurrent sandboxes, so concurrent-sandbox throughput has become a competitive benchmark for AI infrastructure.

<details><summary>References</summary>
<ul>
<li><a href="https://arxiv.org/abs/2609.22978">[2609.22978] DeepSeek Elastic Compute ( DSec ): A Sandbox...</a></li>
<li><a href="https://www.techzine.eu/news/devops/141577/google-launches-open-source-runtime-for-ai-agents/">Google launches open-source runtime for AI agents - Techzine Global</a></li>
<li><a href="https://modal.com/blog/scaling-to-1-million-concurrent-sandboxes-in-seconds">Scaling to 1 million concurrent sandboxes in seconds - Modal</a></li>

</ul>
</details>

**Discussion**: Commenters were most struck by the raw numbers, with one calling 380,000 concurrent sandboxes on 160 Epyc nodes "crazy stuff," and another noting the system looks similar to what Google is building with AX. A recurring theme was the 131-author paper, with readers joking that the topic is less interesting than how so many authors coordinated, and speculating that listing every employee is a talent-retention or "asset protection" strategy to keep competitors from identifying who to poach; one commenter also asked whether DSec is essentially an "agent substrate."

**Tags**: `#DeepSeek`, `#distributed systems`, `#cloud infrastructure`, `#sandboxing`, `#AI agents`

---

<a id="item-2"></a>
## [SemiAnalysis Publishes Free Teardown of Intel Panther Lake and 18A](https://newsletter.semianalysis.com/p/intel-panther-lake-teardown) ⭐️ 8.0/10

SemiAnalysis has published a free teardown of Intel's Panther Lake processor and the Intel 18A process node, produced by its STEEL teardown lab. The report looks inside Intel's first high-volume client chip built on 18A, examining the silicon and packaging in detail. Panther Lake is Intel's most important client product in years because it is the first to ship on the 18A node, the process Intel is betting its foundry business on. Independent physical analysis of the silicon gives engineers a rare, credible look at whether 18A's RibbonFET and backside-power claims hold up in real hardware. Panther Lake is a tiled design: the CPU tile is built on Intel 18A, the graphics tile uses the Arc Xe3 architecture derived from Xe2 (Battlemage), and the I/O tile is manufactured on TSMC's N6 process. Core configurations vary by segment, with a 4+8+4 layout for the H series and a smaller 4+4 tile for low-power parts.

rss · Semianalysis · Sep 26, 13:36

**Background**: Intel 18A is Intel's most advanced process node and the first to enter production using both RibbonFET gate-all-around (GAA) transistors and PowerVia backside power delivery. Gate-all-around wraps the transistor channel on all sides for better control and lower leakage, while backside power delivery moves the power wiring beneath the transistors to reduce congestion and improve efficiency. SemiAnalysis runs a dedicated teardown lab (STEEL) that physically disassembles datacenter, AI and client hardware to measure and image the actual silicon rather than relying on vendor specifications. Panther Lake, marketed as the Core Ultra series 3, is the first high-volume client chip to use 18A.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Panther_Lake_(microprocessor)">Panther Lake (microprocessor) - Wikipedia</a></li>
<li><a href="https://www.tomshardware.com/pc-components/cpus/intels-pivotal-18a-process-is-making-steady-progress-but-still-lags-behind-yields-only-set-to-reach-industry-standard-levels-in-2027">Intel's pivotal 18A process is making steady progress, but still lags behind — yields only set to reach industry standard levels in 2027 | Tom's Hardware</a></li>
<li><a href="https://www.intel.com/content/www/us/en/foundry/process/18a.html">Intel 18A | See Our Biggest Process Innovation</a></li>

</ul>
</details>

**Tags**: `#Intel`, `#semiconductors`, `#process technology`, `#hardware teardown`, `#Panther Lake`

---

<a id="item-3"></a>
## [Excel now stores multiple values in a single cell with lists and arrays](https://techcommunity.microsoft.com/blog/microsoft365insiderblog/put-multiple-values-in-one-cell-with-lists-and-arrays-in-excel/4559395) ⭐️ 8.0/10

Microsoft has begun rolling out lists, in-cell arrays, and nested arrays to Excel Beta users on Windows and Mac, letting a single cell hold multiple values for the first time in the product's 40-year history. Alongside this, four new array functions — FLATTEN, HAS, HASANY, and HASALL — were introduced to work with that data. Because Excel is one of the most widely used data tools in the world, removing the long-standing "one value per cell" constraint could reshape how millions of users build, filter, and analyze spreadsheets, potentially reducing reliance on helper columns, text splitting, and delimiter hacks. It also signals that Microsoft is modernizing Excel's core data model rather than just adding cosmetic features. Users can enter multiple items in a cell via Ctrl+J or Insert > List, with entries separated by commas or semicolons, and can then filter and calculate on individual items within the list. Referencing a list such as =B2 can spill its values into separate cells, while FLATTEN converts ranges into a single column and HAS, HASANY, and HASALL test whether values are present — but all of these are preview features whose behavior may change before general release, so Microsoft advises against using them in important workbooks.

telegram · zaihuapd · Sep 26, 16:26

**Background**: Historically, an Excel cell has held exactly one value — a number, a date, or a piece of text — so representing multiple items in one cell required workarounds such as delimiter-separated text plus functions like TEXTSPLIT or helper columns. Arrays in Excel existed as formula results that spilled across a range, but they could not be stored directly inside a single cell. New functions like FLATTEN (which merges multiple ranges into one column) and the HAS family (which check list membership) are designed to make this new list-based data model practical for everyday analysis and filtering.

<details><summary>References</summary>
<ul>
<li><a href="https://techcommunity.microsoft.com/blog/microsoft365insiderblog/put-multiple-values-in-one-cell-with-lists-and-arrays-in-excel/4559395">Put multiple values in one cell with lists and arrays in Excel</a></li>
<li><a href="https://www.xelplus.com/excel-lists-in-cells/">Excel Lists in Cells: Put Multiple Values in One Cell</a></li>
<li><a href="https://www.neowin.net/news/excel-finally-supporting-multiple-values-in-single-cell-microsoft-explains-how/">Excel finally supporting multiple values in single cell... - Neowin</a></li>

</ul>
</details>

**Tags**: `#Excel`, `#Microsoft`, `#Spreadsheet`, `#Data Analysis`, `#Feature Update`

---