---
layout: default
title: "Horizon Summary: 2026-11-15 (ZH)"
date: 2026-11-15
lang: zh
---

> 从 35 条内容中筛选出 3 条重要资讯。

---

1. [SpaceX 在第十五次试飞结束时用发射塔机械臂捕获星舰助推器](#item-1) ⭐️ 9.0/10
2. [Lovable 生成的应用泄露护照信息和超 20 万条私密消息](#item-2) ⭐️ 8.0/10
3. [谷歌 Project Zero 将漏洞披露窗口逐步缩短至 30 天](#item-3) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [SpaceX 在第十五次试飞结束时用发射塔机械臂捕获星舰助推器](https://www.spacex.com/launches/starship-flight-15) ⭐️ 9.0/10

SpaceX 在第十五次飞行测试结束时，用发射塔的机械臂成功捕获了星舰（Starship）的超重型助推器（Super Heavy），这一动作已成为其试飞流程中反复验证的关键环节。此次飞行以助推器返回发射场、在半空中被机械臂夹住而非用着陆腿降落而告终。 每一次成功捕获都让 SpaceX 更接近完全且快速可重复使用的发射系统，而这正是星舰的核心经济逻辑：两级全复用有望把每公斤入轨成本压到远低于一次性火箭、甚至低于猎鹰 9 号这类部分复用运载器的水平。这不仅关系到星链（Starlink）和商业载荷，也关系到 NASA 的阿尔忒弥斯（Artemis）登月着陆器计划以及未来重型运载和火星探索的雄心。 捕获由发射塔上被昵称为“筷子”的巨大机械臂完成，它在助推器返回发射台下降时将其夹住，从而省去了着陆腿及其带来的结构重量。仍然悬而未决的是工程层面的问题：飞行器的隔热罩能否在再入中完好到支持快速复用，以及星舰最终的入轨质量分数究竟是多少——因为该飞行器只能以部分推进剂入轨，深空任务还需依赖在轨加注。

hackernews · ls612 · 11月14日 21:22 · [社区讨论](https://news.ycombinator.com/item?id=50500963)

**背景**: 星舰是 SpaceX 的两级完全可重复使用超重型运载火箭：高约 232 英尺的“超重型”助推器负责把整个组合体推离发射台，星舰上面级则继续飞向轨道。与猎鹰 9 号用着陆腿降落不同，超重型助推器会返回发射场，由发射塔上的机械臂在半空中夹住，这种设计旨在节省结构重量并实现快速周转。该项目自 2023 年以来通过一系列日益大胆的试飞逐步推进，SpaceX 将完全复用视为借助规模效应降低发射成本的关键。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/List_of_Starship_launches">List of Starship launches - Wikipedia</a></li>
<li><a href="https://www.bbc.com/news/live/cq0k683l3dz3t">SpaceX successfully catches part of Starship rocket on... - BBC News</a></li>
<li><a href="https://en.wikipedia.org/wiki/List_of_Super_Heavy_boosters">List of Super Heavy boosters - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 评论者几乎一致表示赞叹，把星舰形容为“做对了的航天飞机”——完全复用的助推器没有固体助推器，上面级堆叠在顶部而非侧面，从而规避了挑战者号与哥伦比亚号事故背后的失效模式。多位评论者指出，接下来的里程碑是验证隔热罩、实现两级同时捕获以及重复使用同一批飞行器；也有人指出，即便入轨质量分数尚不确定，100% 可复用的系统在成本上仍优于猎鹰 9 号这样的部分复用系统。

**标签**: `#SpaceX`, `#Starship`, `#reusable rockets`, `#spaceflight`, `#aerospace engineering`

---

<a id="item-2"></a>
## [Lovable 生成的应用泄露护照信息和超 20 万条私密消息](https://www.crissyfield.de/research/lovable-en/) ⭐️ 8.0/10

Crissy Field 的一位安全研究人员发布了一份事件报告，记录了多款由 AI 应用构建工具 Lovable 生成的应用因 Supabase 行级安全（RLS）策略不充分，而泄露包括护照信息和超过 20 万条私密消息在内的敏感数据。该披露最初在 Hacker News 上反响平平，重新提交后获得约 734 分和近 295 条评论。 这是“氛围编程”（vibe coding）式 AI 生成应用安全风险的一个具体真实案例：没有安全背景的用户也能上线背后连着真实数据库、承载真实用户数据的应用。它把讨论从对 AI 代码生成的抽象警告，转向了整个 AI 应用栈中究竟该由谁负责——构建平台、数据库提供商还是终端用户——的尖锐问题。 根本原因是 Supabase 中行级安全策略缺失或配置不当，导致被打包进前端代码的公开 anon API 密钥可以读取本不该访问的数据表——这意味着攻击者只需在浏览器中查看网络请求即可。评论者还指出 Supabase 长期以来的默认行为是 RLS 不启用就不生效，据称已在 10 月 30 日的一项变更中修复，但对已有项目可能仍然适用。

hackernews · armcat · 11月14日 17:43 · [社区讨论](https://news.ycombinator.com/item?id=50499017)

**背景**: Lovable 是一款 AI 应用构建工具，可以根据自然语言提示生成完整应用，包括界面、数据库结构和业务逻辑，并且通常连接 Supabase——一个基于 Postgres 的后端即服务。在 Supabase 中，行级安全（RLS）决定每个用户能读写哪些数据行，需要按表启用，并分别为 SELECT、INSERT、UPDATE 和 DELETE 编写独立策略。如果暴露 schema 中的表未启用 RLS，那么每个客户端都会携带的公开 API 密钥实际上就成了该表的万能钥匙。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://supabase.com/docs/guides/database/postgres/row-level-security">Row Level Security | Supabase Docs</a></li>
<li><a href="https://lovable.dev/">App & Website Builder | Build Software in Minutes | Lovable</a></li>
<li><a href="https://zyntari.com/guides/security-holes-in-ai-generated-apps">Lovable App Security Risks : What We Keep Finding — Zyntari</a></li>

</ul>
</details>

**社区讨论**: 讨论明显呈现多方观点：Lovable 的安全负责人亲自回应称，根本原因是 RLS 不足，而他们发布前的自动扫描和可选的 SAST 深度扫描正是为了捕捉这类问题，且对所有用户免费，发现问题后可一键修复、后台自动修复或阻止发布。另一些评论者把矛头指向 Supabase，认为其当年为降低上手门槛而让 RLS 默认关闭才是真正的祸根；还有人指出 AI 生成应用数量庞大、易于攻击，其用户根本无从判断风险，呼吁应采用默认拒绝的数据库和最小权限 API。

**标签**: `#security`, `#AI-generated apps`, `#Supabase`, `#Row-Level Security`, `#data breach`

---

<a id="item-3"></a>
## [谷歌 Project Zero 将漏洞披露窗口逐步缩短至 30 天](https://projectzero.google/2026/11/disclosure-policy.html) ⭐️ 8.0/10

谷歌 Project Zero 宣布分阶段收紧其漏洞披露政策：即日起实行“Full 90”，即在向厂商报告漏洞 90 天后公开；2027 年 2 月 2 日转为“Full 60”，2028 年 1 月 3 日再转为“Full 30”。走完最后一步后，Project Zero 将在通知受影响厂商仅 30 天后就公开漏洞细节。 Project Zero 的时限历来会重塑行业惯例——其最初的 90 天政策后来被众多厂商和安全团队当作事实标准——因此把窗口压缩到 30 天可能迫使商业软件和开源项目的补丁流程与发布节奏发生全面改变。无法快速交付修复的厂商将面临未修补漏洞被公开的局面，实际风险会转嫁到最终用户身上。 该时间表为厂商留出了大约 14 个月的缓冲期，之后 30 天规则才生效，而已披露的政策文本并未说明针对复杂修复或多方协作修复是否设有例外或延期机制。这一变化恰逢谷歌越来越多地使用自动化与基于大模型的漏洞发现工具（如 BigSleep），这类工具发现漏洞的速度往往快于人工修复周期所能承受的节奏。

hackernews · hacb · 11月14日 11:13 · [社区讨论](https://news.ycombinator.com/item?id=50496051)

**背景**: Project Zero 是谷歌聘用的一支安全分析团队，于 2014 年 7 月对外公布，专门在广泛使用的软件中寻找零日漏洞并推动厂商修复。漏洞披露通常遵循所谓“协同漏洞披露”（CVD）流程：研究人员私下通知厂商、留出修复时间，之后公开细节，以便用户和防御方评估自身受影响程度。Project Zero 于 2015 年首创的 90 天期限后来成为行业非正式基准，而许多漏洞赏金计划则通过付费鼓励研究者私下上报漏洞，而不是卖给漏洞掮客。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Project_Zero">Project Zero - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Coordinated_vulnerability_disclosure">Coordinated vulnerability disclosure</a></li>
<li><a href="https://en.wikipedia.org/wiki/Bug_bounty_program">Bug bounty program</a></li>

</ul>
</details>

**社区讨论**: 评论者普遍怀疑这一收紧后的时限是否现实，有人直言 Ubuntu 尤其“需要比这长得多的时间”。也有人主张应当立即披露，因为谷歌的漏洞赏金已经消除了隐瞒漏洞的经济动机；还有评论提出更微妙的担忧：披露压力可能被用作杠杆，推动厂商采用报告方自家的基于大模型的工具。

**标签**: `#vulnerability disclosure`, `#Project Zero`, `#cybersecurity`, `#open source security`, `#bug bounty`

---