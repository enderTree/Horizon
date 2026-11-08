---
layout: default
title: "Horizon Summary: 2026-11-08 (EN)"
date: 2026-11-08
lang: en
---

> From 34 items, 9 important content pieces were selected

---

1. [Need for Speed Underground 2 Now Playable Online in the Browser via WebGPU](#item-1) ⭐️ 8.0/10
2. [MaxxBench Tests Whether DeepSWE Scores Survive Task-Spec Variation](#item-2) ⭐️ 8.0/10
3. [Coldframe: A Python Honeypot Posing as a Supermarket Fridge Controller](#item-3) ⭐️ 8.0/10
4. [Researcher finds undocumented macOS daemons building a personal knowledge graph of your relationships](#item-4) ⭐️ 8.0/10
5. [Microsoft Research's AI Frontiers Group Reportedly Dissolved as John Langford Departs](#item-5) ⭐️ 8.0/10
6. [Asahi Linux 7.3 Report: Same-Day Fedora Asahi Remix and Licensing Worries](#item-6) ⭐️ 8.0/10
7. [SemiAnalysis Tours China's Wind-Powered 800MW AI Campus in Inner Mongolia](#item-7) ⭐️ 8.0/10
8. [China Blocks SoftBank's $5.4B Acquisition of ABB Robotics](#item-8) ⭐️ 8.0/10
9. [GitHub's Rubicon architecture handles 7,200 pushes per second](#item-9) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Need for Speed Underground 2 Now Playable Online in the Browser via WebGPU](https://nfsu2.xyz/) ⭐️ 8.0/10

A site at nfsu2.xyz now runs the full 2004 PC racing game Need for Speed Underground 2 directly in a web browser, accelerated by WebGPU, and it includes working online multiplayer so players can race together in shared sessions. The project drew 876 points and 239 comments on Hacker News, where users reported playing it on phones and desktops alike. It demonstrates how far browser-based emulation and GPU access have come: a commercial AAA game from two decades ago runs without installation, and its long-dead online mode has been revived through reverse engineering. That combination of preservation and restored multiplayer hints at how many other abandoned games could be brought back to life. Because the site distributes copyrighted game data without a license, commenters expect a takedown request and note that the game is effectively abandonware that EA no longer sells. Linux users report needing to enable unsafe WebGPU features, for example launching Chromium with the relevant flag, to get rendering working.

hackernews · fluxusars · Nov 7, 09:36 · [Discussion](https://news.ycombinator.com/item?id=50403052)

**Background**: Need for Speed Underground 2 was released by EA in 2004 and its official online services were shut down long ago, leaving retail copies difficult to run on modern hardware. WebGPU is the W3C-standard JavaScript API that supersedes WebGL, giving web pages efficient access to a system's GPU through Vulkan, Metal, or Direct3D 12; by late 2025 it shipped in all major browsers. Running a full PC game in a browser typically relies on WebAssembly-based emulation or engine recreation, which reads the original game's data files with a newly written engine.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/WebGPU">WebGPU</a></li>
<li><a href="https://en.wikipedia.org/wiki/List_of_game_engine_recreations">List of game engine recreations - Wikipedia</a></li>

</ul>
</details>

**Discussion**: Sentiment is overwhelmingly positive and nostalgic, with players recalling college-era PCs and Xbox sessions and delighting in the chaos of hundreds of cars doing burnouts together online. The main caveats raised are legal: some argue it is dubious to accept or solicit donations for copyrighted content, while others hope EA leaves the abandonware project alone. Users also shared practical tips, such as the Chromium flag needed on Linux.

**Tags**: `#browser-emulation`, `#WebGPU`, `#game-preservation`, `#abandonware`, `#reverse-engineering`

---

<a id="item-2"></a>
## [MaxxBench Tests Whether DeepSWE Scores Survive Task-Spec Variation](https://maxxbench.unlap.ai/research/why-maxxbench/) ⭐️ 8.0/10

MaxxBench published a methodological study that re-ran DeepSWE-style tasks with varied task specifications to see whether the reported scores hold up, and concluded that many of the results do not generalize well. The study also surfaced a set of bugs in DeepSWE itself and produced a practical takeaway — roughly, "don't use max mode" — that commenters seized on. Benchmark leaderboards are routinely used to pick coding agents and to justify claims about model capability, so evidence that scores shift under minor changes to the task spec undermines confidence in those rankings. The critique matters most for practitioners choosing models for real repository-level engineering work, where the benchmark's narrow framing may not carry over. The core method is deliberately simple: perturb one parameter or the task specification and measure how much the score moves, rather than treating a single leaderboard number as fixed. The analysis also notes that the collapse is uneven — models with "-flash" in the name and smaller variants fare worst — and that at least some of DeepSWE's tasks carry latent bugs, meaning part of the measured gap may reflect benchmark defects rather than model ability.

hackernews · antiuniverse · Nov 7, 17:19 · [Discussion](https://news.ycombinator.com/item?id=50406222)

**Background**: DeepSWE is a long-horizon software engineering agent benchmark in which an agent must autonomously resolve real repository-level coding issues end to end, typically run through a harness such as mini-swe-agent inside an isolated container with no internet access. Its tasks are written from scratch rather than adapted from existing commits or pull requests, an approach intended to make the benchmark contamination-free. MaxxBench's study asks a different question from "who scores highest": whether a given DeepSWE score is stable enough to mean anything when the task presentation changes.

<details><summary>References</summary>
<ul>
<li><a href="https://deepswe.datacurve.ai/">DeepSWE measures frontier coding agents on original, long-horizon...</a></li>
<li><a href="https://llm-stats.com/benchmarks/deepswe">DeepSWE Leaderboard | LLM Stats</a></li>
<li><a href="https://news.ycombinator.com/item?id=50406222">MaxxBench – "Nice DeepSWE score. But is it true?" | Hacker News</a></li>

</ul>
</details>

**Discussion**: Hacker News commenters largely welcomed the critique, with one arguing that varying a single parameter and watching the score move should be the default first-order robustness test for any benchmark. Others focused on the reported DeepSWE bugs, saying such defects in a widely cited benchmark erode trust, while one commenter identified the pattern that smaller "-flash" models collapse most and another attributed the problem less to training on benchmarks than to labs building sloppy RL environments that fail to vary task complexity.

**Tags**: `#LLM benchmarks`, `#model evaluation`, `#AI/ML`, `#benchmark validity`, `#DeepSWE`

---

<a id="item-3"></a>
## [Coldframe: A Python Honeypot Posing as a Supermarket Fridge Controller](https://github.com/hedgerow-dev/coldframe) ⭐️ 8.0/10

A developer released Coldframe, a single-file, standard-library-only Python honeypot that faithfully impersonates the web interfaces of Danfoss AK-SM 800A and Dixell XWEB supermarket refrigeration controllers, and both personas are currently fingerprinted by Shodan as genuine devices rather than honeypots. Two instances went live and, in their first day, saw only generic internet scanners plus Shodan's crawler, refrigerator.census.shodan.io. Retail refrigeration is a low-visibility but high-impact OT attack surface: recent incidents in Europe reportedly pushed hundreds of stores' units into defrost mode, spoiling food and disrupting operations. A cheap, convincing decoy lets defenders and researchers observe real attacker TTPs against internet-exposed ICS rather than guessing from vulnerability databases alone. To match real units, the author copied header ordering, page titles, certificate fields and TLS versions from Shodan records — the Danfoss persona emits nginx headers in the same order as a real AK-SM 800A, while the Dixell persona sends no Server header and pads its page to exactly 8,202 bytes. The honeypot also recognises CVE-2025-41450 (the Danfoss "code of the day" login bypass) and three other Danfoss CVEs plus XWEB vulnerabilities, and default logins open a fake store dashboard with defrost buttons so second-stage behaviour can be captured.

hackernews · hedgerow-dev · Nov 7, 17:27 · [Discussion](https://news.ycombinator.com/item?id=50406292)

**Background**: Supermarket refrigeration is managed by system managers such as the Danfoss AK-SM 800A and the Copeland/Dixell XWEB series, which expose web and Modbus-based interfaces for monitoring temperatures and alarms and are frequently reachable directly from the internet with default credentials. In recent weeks attackers reportedly compromised such controllers across European supermarkets and triggered defrost mode remotely. CVE-2025-41450 is an improper authentication flaw affecting Danfoss AK-SM 8xxA series before version 4.2, allowing an authentication bypass. A honeypot is a decoy system designed to attract and study attacker activity without exposing production infrastructure.

<details><summary>References</summary>
<ul>
<li><a href="https://www.bleepingcomputer.com/news/security/hackers-disrupt-refrigeration-systems-at-european-supermarkets/">Hackers disrupt refrigeration systems at European supermarkets</a></li>
<li><a href="https://nvd.nist.gov/vuln/detail/CVE-2025-41450">NVD - CVE - 2025 - 41450</a></li>
<li><a href="https://www.danfoss.com/en/products/dcs/electronic-controls/products/system-managers/">System manager components | Easy to use | Danfoss</a></li>

</ul>
</details>

**Discussion**: Commenters were sceptical of using Shodan data as ground truth, warning that many internet-facing devices are themselves honeypots and the rest are often already compromised, so a locally acquired device would be a better baseline. The author added that blood banks may be an even more damaging target and argued supermarkets have no security team, so secure defaults must come from vendors and installers; others questioned whether the reported 'hack' was actually a mass simultaneous software update, noting the effects appeared country by country.

**Tags**: `#security`, `#honeypots`, `#ICS/OT`, `#show-hn`, `#threat-intelligence`

---

<a id="item-4"></a>
## [Researcher finds undocumented macOS daemons building a personal knowledge graph of your relationships](https://8rank.ai/game/apple-intelligence-personal-knowledge-graph) ⭐️ 8.0/10

A security researcher's reverse-engineering write-up reveals that every Mac since macOS 13 (2022) ships two undocumented background daemons — knowledgeconstructiond and intelligenceplatformd — that together build an on-device "personal knowledge graph" linking your contacts, how they relate to each other, how you communicate with them, and where you go. The analysis, based on inspection of the Apple Intelligence bundle in macOS 26, describes a persistent graph-building subsystem that runs on both Intel and Apple silicon Macs and includes inferred classifications such as family relationships. This puts a mainstream consumer OS in the position of silently inferring sensitive social relationships — including who is family — without explicit disclosure, which conflicts with Apple's public privacy-first marketing and with regulatory frameworks like the GDPR's rules on inferred personal data. Because the system runs locally and feeds Apple Intelligence features, it sharpens the debate over whether on-device processing alone is sufficient justification for data collection that users never opted into. The daemons reportedly operate as a persistent graph-building subsystem rather than being confined to a single app's sandbox, quietly linking contacts, behavior and hardware state on both Intel and Apple silicon hardware; the write-up follows earlier independent work by Nic Lydon, who encountered the same database while building his own personal knowledge graph. Apple has not documented the system publicly, and the author has published a follow-up study on the knowledge graph.

hackernews · infwhispers · Nov 7, 09:46 · [Discussion](https://news.ycombinator.com/item?id=50403097)

**Background**: A knowledge graph is a data structure that stores facts as entities and relationships (for example "Alice — sister of — Bob"), letting software reason over connections instead of just matching keywords. On-device AI features such as Apple Intelligence need this kind of contextual memory to answer questions like "when is my sister's flight?", and vendors argue that processing it locally rather than in the cloud protects privacy. The trade-off is that the inference itself — including classifying who counts as family — happens without users being told it exists, which is what the researcher and commenters are questioning.

<details><summary>References</summary>
<ul>
<li><a href="https://8rank.ai/game/apple-intelligence-personal-knowledge-graph">Anatomy of Apple 's Personal Knowledge Graph — Eighth Rank</a></li>
<li><a href="https://techplanet.today/post/apples-hidden-personal-knowledge-graph-understanding-macoss-undocumented-family-classifier">Apple's Hidden Personal Knowledge Graph: Understanding macOS ...</a></li>
<li><a href="https://techbytes.app/posts/every-mac-comes-with-an-undocumented-family-member-classifier/">Every Mac comes with an (undocumented) family member classifier</a></li>

</ul>
</details>

**Discussion**: The Hacker News thread (658 points, 368 comments) was broadly uneasy: one commenter said such data would once have seemed fascinating if opt-in but now feels exhausting, raising the social concern that a record of every conversation removes the natural forgetting that human relationships rely on. Others noted that leaving the Apple ecosystem limits exposure but that Google's equivalent profile would likely be worse, and several quoted Steve Jobs' 2010 statement that privacy means asking users repeatedly in plain English what will be done with their data.

**Tags**: `#privacy`, `#apple`, `#macos`, `#knowledge-graph`, `#on-device-ai`

---

<a id="item-5"></a>
## [Microsoft Research's AI Frontiers Group Reportedly Dissolved as John Langford Departs](https://hunch.net/?p=13764006) ⭐️ 8.0/10

John Langford, a partner researcher manager at Microsoft Research New York, announced on his blog Machine Learning (Theory) that he has left Microsoft and declared the AI Frontiers group over. AI Frontiers was MSR's lab focused on frontier research in efficient language models and agentic systems. The dissolution of a prominent exploratory lab at one of the world's leading industrial research organizations is being read as a signal that big companies are consolidating around transformer scaling and deprioritizing open-ended AI research. For researchers tracking where fundamental AI work will happen, it suggests a shrinking space inside industry labs. According to Langford's post and the discussion around it, the issue is less about abandoning transformers than about organizational friction — office politics, poor management and weak research-to-product transfer. Notably, Microsoft Research's AI Frontiers page now states that as of September the lab became part of Microsoft AI, indicating a reorganization rather than a simple shutdown.

hackernews · srean · Nov 7, 18:02 · [Discussion](https://news.ycombinator.com/item?id=50406563)

**Background**: Microsoft Research (MSR) has long been one of the largest corporate basic-research organizations in computing, and its culture was built on a simple bargain: do good work and good things happen, without pressure to ship products. AI Frontiers was one of its newer labs, aimed at frontier work on efficient language models and agentic systems. The broader AI field has meanwhile converged on transformer architectures, where performance improves predictably by scaling parameters, data and compute — an approach that is expensive but low-risk compared with exploratory alternatives. John Langford is a well-known machine-learning researcher and learning-theory specialist who has written for years on his blog about how ML is shifting from an academic discipline to an industrial tool.

<details><summary>References</summary>
<ul>
<li><a href="https://www.microsoft.com/en-us/research/lab/ai-frontiers/">Microsoft Research AI Frontiers - Microsoft Research</a></li>
<li><a href="https://businessexaminer.ca/victoria-articles/item/microsoft-researcher-john-langford-exits-as-ai-frontiers-group-is-declared/">Microsoft Researcher John Langford Exits as AI ... | Business Examiner</a></li>
<li><a href="https://en.wikipedia.org/wiki/John_Langford_(computer_scientist)">John Langford (computer scientist) - Wikipedia</a></li>

</ul>
</details>

**Discussion**: Commenters largely agree this reflects an industry-wide pattern: transformer scaling is treated as the safe highway, and exploratory research into other AI methods is discouraged, with one noting Meta similarly sidelined its prior research leadership. Several expressed sadness that billions flow into essentially one idea, and that MSR's implicit "do good work and good things happen" contract has been repeatedly broken under current leadership, which they see as culture-destroying. A counterpoint held that Langford did not claim transformer research stopped — he mentioned a specific transformer variant — and that the real story is office politics and poor execution, with labs like Qwen and DeepSeek showing LLM innovation still pays off.

**Tags**: `#AI research`, `#Microsoft Research`, `#industry trends`, `#research culture`, `#transformer models`

---

<a id="item-6"></a>
## [Asahi Linux 7.3 Report: Same-Day Fedora Asahi Remix and Licensing Worries](https://asahilinux.org/2026/11/progress-report-7-3/) ⭐️ 8.0/10

Asahi Linux published its Linux 7.3 progress report, highlighting that Fedora Asahi Remix shipped on the same day as Fedora Linux 45, which was released on 3 November — the first time the remix has ever matched upstream's release date. The report also covers ongoing Apple Silicon enablement work and raises concerns about third parties exploiting the project's permissive licensing to hijack its work and monetize Linux on Apple Silicon. Same-day releases mean Apple Silicon Mac users can adopt the newest Fedora features and fixes without the multi-week lag that previously made Fedora Asahi Remix feel like a second-class downstream. The licensing warning matters for the wider open source ecosystem, since it questions whether permissive licenses leave reverse-engineering-heavy projects vulnerable to rebranding and commercial capture. The report frames same-day shipping as an operational milestone rather than a feature milestone, indicating the downstream build and QA pipeline has matured, while the licensing section notes multiple attempts to exploit the project's permissive terms with the stated goal of replacing the project. Hardware enablement remains incremental, with newer Apple SoC generations and long-standing gaps such as USB-C display output still exercising users.

hackernews · ackyshake · Nov 7, 05:20 · [Discussion](https://news.ycombinator.com/item?id=50401867)

**Background**: Asahi Linux is a volunteer-driven project that ports the Linux kernel and supporting software to Apple Silicon Macs by reverse-engineering Apple's systems-on-chip, which lack public documentation. Fedora Asahi Remix is its flagship distribution, built on Fedora Linux with KDE Plasma as the default desktop. The project has weathered organizational turbulence, including founder Hector Martin stepping down as project lead in February 2025, so release engineering milestones and governance questions carry extra weight for its community.

<details><summary>References</summary>
<ul>
<li><a href="https://asahilinux.org/2026/11/progress-report-7-3/">Progress Report: Linux 7.3 - Asahi Linux</a></li>
<li><a href="https://en.wikipedia.org/wiki/Asahi_Linux">Asahi Linux - Wikipedia</a></li>

</ul>
</details>

**Discussion**: Commenters were broadly positive about the same-day release, with long-time financial backers calling it a welcome sign of maturity, but several said the lack of USB-C external display support remains a hard blocker before they would daily-drive Asahi on a MacBook Air, and some questioned why newer CPU support outranks that feature. Others speculated about which downstream effort the licensing warning refers to and argued the project should have used a copyleft license, while one developer promoted a competing project claiming Vulkan 1.4, M4/M5 support, and suspend-to-RAM.

**Tags**: `#Linux`, `#Apple Silicon`, `#Asahi Linux`, `#Fedora`, `#Open Source`

---

<a id="item-7"></a>
## [SemiAnalysis Tours China's Wind-Powered 800MW AI Campus in Inner Mongolia](https://newsletter.semianalysis.com/p/we-visited-chinas-stargate-in-inner) ⭐️ 8.0/10

SemiAnalysis published an on-site report from Inner Mongolia describing a wind-powered AI data-center campus designed for 800MW total capacity, of which roughly 120MW was built inside a single year. The site also hosts a 5MW pilot using solid-state transformers to deliver 800V DC power natively, plus a cooling design that eliminates central chillers entirely. The buildout pace and power architecture suggest Chinese operators are moving faster than many Western hyperscalers on both construction speed and next-generation DC power delivery, which matters as AI scaling becomes increasingly constrained by energy and grid interconnection rather than chips alone. If the SST-native 800V DC and chiller-less approaches hold up at scale, they could become reference designs for AI campuses globally. The 800V DC pilot is rated at 5MW and is described as SST-native, meaning the solid-state transformer interfaces directly between the medium-voltage AC grid and an 800V DC bus rather than going through conventional AC transformation and rectification stages. Cutting central chillers implies reliance on ambient/free cooling and liquid-cooled servers, an approach that works well in Inner Mongolia's cold climate but has narrower applicability in hotter, humid regions.

rss · Semianalysis · Nov 7, 19:01

**Background**: AI training clusters are pushing rack densities far beyond what traditional alternating-current data-center power distribution handles efficiently, prompting an industry push toward 800V DC architectures that cut conversion stages and copper losses. A solid-state transformer replaces the bulky iron-and-copper transformer with power electronics, providing galvanic isolation from medium-voltage AC while outputting DC directly. Chiller-less cooling, meanwhile, uses outside air or water-side economizers instead of mechanical chillers, and has been used by Google in Belgium and Microsoft in Ireland; Inner Mongolia's cold, windy climate and abundant wind generation make it a natural fit for combining all three ideas at very large scale.

<details><summary>References</summary>
<ul>
<li><a href="https://www.electronicdesign.com/technologies/power/product/55371996/electronic-design-novel-solid-state-transformer-supports-800-v-dc-power-in-ai-data-centers">Novel Solid-State Transformer Supports 800-V DC Power in AI ...</a></li>
<li><a href="https://www.eaton.com/content/dam/eaton/markets/data-center/the-impact-of-ai/whitepapers/eaton-deploying-800vdc-architecture-whitepaper-en-us.pdf">eaton deploying 800vdc architecture whitepaper en us</a></li>
<li><a href="https://www.datacenterknowledge.com/hyperscalers/microsoft-s-chiller-less-data-center">Microsoft's Chiller - less Data Center</a></li>

</ul>
</details>

**Tags**: `#AI infrastructure`, `#data centers`, `#China`, `#energy`, `#cooling`

---

<a id="item-8"></a>
## [China Blocks SoftBank's $5.4B Acquisition of ABB Robotics](https://t.me/zaihuapd/44988) ⭐️ 8.0/10

On November 5, ABB confirmed it had been notified by China's foreign investment security review authority that the deal may not be implemented in China, effectively blocking SoftBank Group's roughly $5.4 billion acquisition of ABB's robotics business. The decision stalls SoftBank's plans to build out a position across AI and robotics. China accounts for roughly 30% of ABB's robotics business, so a prohibition on implementing the deal there is enough to jeopardize the transaction as a whole and shows that Chinese review can veto M&A between two non-Chinese companies. It also signals tightening scrutiny of foreign investment in strategic technology sectors, complicating consolidation in industrial robotics and AI at a time when such deals are accelerating. Chinese regulators were reportedly concerned that industrial data, supply chain information and core technology tied to ABB's robotics business could be transferred overseas and potentially used to train AI models. The case also fits a pattern of heightened review of strategic tech deals, following earlier scrutiny of transactions such as Meta's.

telegram · zaihuapd · Nov 7, 11:24

**Background**: ABB is a Swiss-Swedish industrial giant whose robotics division supplies factory automation arms and software, a business with significant operations, customers and revenue in China. SoftBank is a Japanese investment group that has been assembling assets in AI and robotics. Under China's foreign investment security review regime, transactions involving foreign parties can require approval when they touch domestic operations, data or critical technology — even when neither party is Chinese — so a single jurisdiction's veto can halt a global deal.

**Tags**: `#robotics`, `#SoftBank`, `#ABB`, `#China regulation`, `#AI industry`

---

<a id="item-9"></a>
## [GitHub's Rubicon architecture handles 7,200 pushes per second](https://github.blog/engineering/architecture-optimization/inside-githubs-new-git-storage-architecture/) ⭐️ 8.0/10

GitHub unveiled Rubicon, a redesigned Git storage architecture that stores Git object data in Azure Blob Storage while managing references through Ref-CAS, a quorum-committed compare-and-swap reference store. In internal stress tests, a single repository supported 5,000 concurrent AI agents and up to 7,200 pushes per second while keeping read latency low; the system is now in limited private preview. AI coding agents generate bursts of commits to the same repository, a workload pattern that traditional single-repository Git storage was never designed for, so Rubicon could determine whether GitHub can host fleets of agents without degrading performance for human developers. If it scales beyond private preview, it may also reshape how very large, high-churn repositories are hosted across the ecosystem. Requests pass through a routing layer called Spokes to per-repository groups of virtual replicas that hold only cached state, while background nodes handle pack compaction and each Ref-CAS transaction locks only the references it touches and becomes visible once a majority of log replicas record it. GitHub has not given a public timeline for broader availability beyond the limited private preview.

telegram · zaihuapd · Nov 7, 14:12

**Background**: Git normally stores a repository as a set of immutable objects (commits, trees, blobs) packed into files, plus a small set of mutable references such as branches and tags that point at those objects. On hosted platforms, keeping the references consistent while many writers push at once is the hard part, since conflicting writes to the same branch must be serialized safely. Rubicon separates these concerns by moving bulk object data to cheap, scalable blob storage and centralizing reference coordination in a dedicated compare-and-swap service, then adding cache-only replicas in front for read throughput.

<details><summary>References</summary>
<ul>
<li><a href="https://github.blog/engineering/architecture-optimization/inside-githubs-new-git-storage-architecture/">Inside GitHub's new Git storage architecture - The GitHub Blog</a></li>
<li><a href="https://trashexpert.ru/news/software-news/github-rubicon-git-storage-stress-test">GitHub : до 7200 пушей в секунду в тесте архитектуры Rubicon</a></li>

</ul>
</details>

**Tags**: `#GitHub`, `#Git storage`, `#architecture`, `#AI agents`, `#scalability`

---