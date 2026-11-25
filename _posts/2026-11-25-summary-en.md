---
layout: default
title: "Horizon Summary: 2026-11-25 (EN)"
date: 2026-11-25
lang: en
---

> From 27 items, 11 important content pieces were selected

---

1. [Anthropic says internal Claude model proved VP ≠ VNP with a Lean 4 proof](#item-1) ⭐️ 9.0/10
2. [Preprint Claims Matrix Multiplication Exponent Is Exactly 9/4](#item-2) ⭐️ 8.0/10
3. [PrismML's Ternary Bonsai 2.5 27B Brings Frontier-Style Agentic Coding to Local Hardware](#item-3) ⭐️ 8.0/10
4. [OpenAI says GPT-6.2 can design protein minibinders by writing code](#item-4) ⭐️ 8.0/10
5. [Founder Given 24 Hours to Prove They Aren't Distilling Anthropic Models](#item-5) ⭐️ 8.0/10
6. [Community Project Runs Leaked GTA 6 Xbox Build on Windows](#item-6) ⭐️ 8.0/10
7. [Simon Willison Maps Three LLM Inflection Points in Twelve Months](#item-7) ⭐️ 8.0/10
8. [GPT-6.2 Astra Autonomously Identifies Author of Anonymous 1808 Sketchbook](#item-8) ⭐️ 8.0/10
9. [Huawei and Qualcomm sign broad multi-year patent cross-license covering 5G, AI](#item-9) ⭐️ 8.0/10
10. [VMware vCenter Hit by Another 9.8 Auth Bypass, Exploited as Zero-Day](#item-10) ⭐️ 8.0/10
11. [SpaceX and Tesla Boards Form Special Committees to Review Possible Merger](#item-11) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Anthropic says internal Claude model proved VP ≠ VNP with a Lean 4 proof](https://t.me/zaihuapd/45345) ⭐️ 9.0/10

On November 24, Anthropic published a paper titled "VP ≠ VNP over every field" alongside a Lean 4 formalization, with the repository stating that the result was discovered by an internal research Claude model and that both the paper and the code were written by AI. The paper claims a superpolynomial arithmetic-circuit lower bound for the Hamiltonian cycle polynomial, from which it derives that VP is a strict subclass of VNP. If the claim holds up, it settles Valiant's 1979 algebraic complexity conjecture — a longstanding open problem often described as the algebraic analogue of P vs NP — and would be one of the most striking demonstrations yet of AI systems contributing to frontier mathematical research. The accompanying machine-checkable Lean 4 proof also makes the result unusually amenable to independent verification compared with a purely prose argument. The result concerns arithmetic circuits only and explicitly does not settle the Boolean P vs NP question, since algebraic circuits must be correct for all field elements and their extensions rather than just 0 and 1. The repository reports auditing against three standard axioms and an independent kernel check, but the claim currently traces back to a Telegram post and still requires independent scrutiny by complexity theorists.

telegram · zaihuapd · Nov 24, 12:18

**Background**: In algebraic complexity theory, VP is the class of polynomials of polynomial degree computable by polynomial-size arithmetic circuits (an algebraic analogue of P), while VNP is its nondeterministic counterpart (analogue of NP); Valiant showed in 1979 that the permanent is VNP-complete over fields of characteristic other than two. Whether VP equals VNP is the algebraic counterpart of the P vs NP problem, and proving a separation has been open for decades. Lean 4 is an open-source proof assistant and functional programming language based on dependent type theory, in which proofs are checked mechanically by a small trusted kernel, so a complete Lean formalization greatly reduces the risk of subtle logical errors.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Arithmetic_circuit_complexity">Arithmetic circuit complexity - Wikipedia</a></li>
<li><a href="https://hexagonmath.org/2611.00954v1">VP ||#92;neq$ VNP over every field · Hexagon</a></li>
<li><a href="https://en.wikipedia.org/wiki/Lean_(proof_assistant)">Lean (proof assistant) - Wikipedia</a></li>

</ul>
</details>

**Tags**: `#complexity theory`, `#VP vs VNP`, `#Lean 4`, `#AI for mathematics`, `#formal verification`

---

<a id="item-2"></a>
## [Preprint Claims Matrix Multiplication Exponent Is Exactly 9/4](https://github.com/openai/math/blob/main/preprints/The-matrix-multiplication-exponent-is-nine-fourths-November-24-2026/paper.pdf) ⭐️ 8.0/10

An OpenAI-affiliated preprint posted in the openai/math GitHub repository claims that the matrix multiplication exponent is exactly 9/4, or Θ(n^2.25), over every field; commenters describe this as proving a matching lower bound Ω(n^2.25) to a recently published upper-bound algorithm. The paper is one of four OpenAI-linked papers said to resolve eight problems on an LLM-ranked Top-500 open-problems list. If verified, an exact exponent of 9/4 would settle a central question in algebraic complexity by refuting the long-standing conjecture that the matrix multiplication exponent equals 2, with downstream implications for linear algebra, optimization, and graph algorithms. It also intensifies debate over whether AI labs can produce fundamental mathematical breakthroughs and how such claims should be verified. The claim is a preprint in a GitHub repository rather than an evidently peer-reviewed publication, and the provided material does not demonstrate independent verification; commenters also say it reportedly came from an unreleased model whose recipe is undisclosed. The headline was corrected from O(n^2.25) to Θ(n^2.25), and one commenter notes that an actual O(n^2.25) algorithm, while asymptotically important, is far from practical.

hackernews · E-Reverance · Nov 25, 01:19 · [Discussion](https://news.ycombinator.com/item?id=50637220)

**Background**: Multiplying two n×n matrices naively takes Θ(n^3) field operations, and the matrix multiplication exponent ω is the infimum exponent achievable by any algorithm. Strassen's algorithm first beat n^3, and decades of work lowered upper bounds toward 2, but proving a nontrivial lower bound above 2 has remained difficult, making the conjecture ω=2 a major open problem. The Top-500 list is an LLM-ranked catalog of open math problems, not an expert consensus, so its rankings provide context rather than proof of significance.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Computational_complexity_of_matrix_multiplication">Computational complexity of matrix multiplication - Wikipedia</a></li>
<li><a href="https://www.proofatlas.ai/open-problems/">Top 500 Open Math Problems: LLM-assessed Importance — ProofAtlas</a></li>
<li><a href="https://www.effortlessmath.com/blog/can-we-trust-ai-math-proofs/">Can We Trust AI Math Proofs? How Lean Verifies Them</a></li>

</ul>
</details>

**Discussion**: Hacker News commenters were impressed but skeptical: some framed the batch as a Bell Labs-style run of AI-lab breakthroughs, while others questioned OpenAI and Anthropic incentives, the unreleased model and undisclosed recipe, and the lack of independent verification. Several commenters also corrected the headline's O(n^2.25) to Θ and clarified that the new contribution is the lower bound.

**Tags**: `#matrix-multiplication`, `#complexity-theory`, `#algorithms`, `#openai`, `#llm-research`

---

<a id="item-3"></a>
## [PrismML's Ternary Bonsai 2.5 27B Brings Frontier-Style Agentic Coding to Local Hardware](https://prismml.com/news/bonsai-2-5-27b) ⭐️ 8.0/10

PrismML released Ternary Bonsai 2.5 27B, a 27B-parameter model whose weights are ternary-quantized so it can run agentic coding workloads locally on consumer hardware with 128k context at roughly 22–30 tokens per second. PrismML claims its SWE-bench Verified performance approaches that of frontier models released about six months earlier. If the claim holds up, a 27B model that fits comfortably in 24GB of unified memory and still scores near last cycle's frontier means developers can run capable coding agents entirely offline, without per-token API costs or sending source code to a third party. It also reinforces the trend of small, aggressively quantized models trailing the frontier by only about six months. Ternary quantization restricts each weight to {-1, 0, +1}, about 1.58 bits per weight, and the model ships in a Q2 GGUF format; a community tester measured 22.3 tok/s generation, a 2.12s first token and 222.9 tok/s prompt processing on a Mac Mini M5 Pro with 24GB RAM. One commenter noted that in the published benchmark table the model's raw scores look worse than Qwen, implying the real advantages are memory footprint and throughput rather than outright accuracy.

hackernews · b0m · Nov 24, 20:08 · [Discussion](https://news.ycombinator.com/item?id=50633922)

**Background**: Quantization shrinks a model by storing weights at lower precision, and ternary quantization is the extreme case: every weight collapses to one of three values, so a 27B model needs only a few gigabytes instead of tens of gigabytes, at the cost of some accuracy. SWE-bench Verified is a widely used benchmark that asks a model to resolve real GitHub issues in Python repositories, and it is commonly used as a proxy for agentic coding ability. Running such models locally has become practical mainly because consumer chips like Apple Silicon share fast unified memory between CPU and GPU.

<details><summary>References</summary>
<ul>
<li><a href="https://prismml.com/news/prismml-introduces-ternary-bonsai-model-family">PrismML — PrismML Introduces Ternary Bonsai Model Family</a></li>
<li><a href="https://en.wikipedia.org/wiki/1.58-bit_large_language_model">1.58-bit large language model - Wikipedia</a></li>
<li><a href="https://www.swebench.com/">SWE-bench Leaderboards</a></li>

</ul>
</details>

**Discussion**: The Hacker News thread is heavy on concrete measurements: testers report 22–25 tok/s on a Mac Mini M5 Pro and roughly 300 tok/s prefill with 30 tok/s generation via Unsloth on a MacBook, with one saying it beats inkling 2 mini Q4 at agentic calls. A long-horizon local benchmark shows the same 5-of-8 pass rate as Bonsai 2 but 17% fewer steps and 29% less wall-clock time, while other commenters debate how much of the gain is genuine small-model progress versus benchmark gaming or benchmark drift.

**Tags**: `#local-llm`, `#quantization`, `#small-language-models`, `#swe-bench`, `#agentic-coding`

---

<a id="item-4"></a>
## [OpenAI says GPT-6.2 can design protein minibinders by writing code](https://openai.com/index/gpt-6-models-demonstrate-intrinsic-protein-design-capabilities/) ⭐️ 8.0/10

OpenAI reports that GPT-6.2 was given the 3D structures of five target proteins and marked attachment sites, then wrote code to generate 3D minibinder designs without using specialized protein AI models for the design step; lab tests found evidence of binding across all five targets. If the results hold up, they suggest general-purpose LLMs can turn protein design into a code-writing and tool-orchestration task, potentially lowering the barrier to early-stage therapeutic binder discovery and speeding up design cycles. The real impact depends on whether GPT-6.2 is replacing specialized protein models or mainly acting as an automation layer around them. OpenAI’s workflow still relied on specialized tools: SolubleMPNN suggested amino acid sequences for GPT-6.2’s 3D designs, and other specialized protein models helped select candidates predicted to fold as designed and bind at the intended site. Commenters also noted that the evidence is heavy on computational exploration and comparatively light on laboratory controls.

hackernews · acossta · Nov 24, 21:02 · [Discussion](https://news.ycombinator.com/item?id=50634658)

**Background**: Proteins are chains of amino acids that fold into 3D shapes, and a minibinder is a small protein engineered to bind a specific target. Computational protein design typically separates backbone generation, sequence design, and folding or binding prediction, with specialized models handling each step. General-purpose LLMs such as GPT-6.2 can write code, so a central question is whether they can coordinate or even replace those specialized tools.

<details><summary>References</summary>
<ul>
<li><a href="https://openai.com/index/gpt-6-models-demonstrate-intrinsic-protein-design-capabilities/">GPT-6 models demonstrate intrinsic protein-design ... - OpenAI</a></li>
<li><a href="https://pmc.ncbi.nlm.nih.gov/articles/PMC11042314/">De novo design of protein minibinder agonists of TLR3 - PMC</a></li>
<li><a href="https://www.nature.com/articles/s41587-024-02123-4">Designing proteins with language models - Nature Biotechnology</a></li>

</ul>
</details>

**Discussion**: Hacker News commenters broadly found the result interesting but pushed back on the “beyond specialized models” framing: fabian2k asked what GPT-6.2 actually designed when SolubleMPNN supplied the sequences, while plaidfuji described GPT as a promising “glue layer” between specialized tools that may outperform them on some subtasks. joe-esquibel said the evidence looks light on lab controls and heavy on computational exploration, and gopalv highlighted code-writing as the models’ core superpower.

**Tags**: `#AI for science`, `#protein design`, `#LLM capabilities`, `#biotech`, `#AI agents`

---

<a id="item-5"></a>
## [Founder Given 24 Hours to Prove They Aren't Distilling Anthropic Models](https://news.ycombinator.com/item?id=50630809) ⭐️ 8.0/10

A founder posted on Hacker News that Anthropic accused them and their company of using the Claude API for model distillation and gave them 24 hours to prove otherwise. The founder denies the claim — the company does not train its own models — and suspects the only usage that could have triggered the flag is automated regression benchmarking run whenever they change AI settings. The case exposes how opaque terms-of-service enforcement and an unclear burden of proof can put companies built on closed LLM APIs at existential risk, since a ban can cut off a core dependency overnight. Because repetitive automated benchmarking is standard engineering practice, many API customers could plausibly be caught by the same false-positive pattern. The hard part is evidentiary: the founder cannot hand over raw traffic logs or prompt/response pairs without exposing user data, and Anthropic has not publicly specified what constitutes acceptable proof. Commenters suggest submitting the benchmark-generating code with its git history, and pre-checking the submission by asking Claude whether it would look convincing to an automated reviewer.

hackernews · weli · Nov 24, 16:45

**Background**: Model distillation (knowledge distillation) is the practice of training a smaller "student" model on outputs produced by a stronger "teacher" model, which lets a competitor cheaply approximate a frontier model's capabilities. For that reason, commercial LLM providers' terms generally forbid using API outputs to train or improve competing models, and Anthropic has said it runs classifiers and behavioral fingerprinting over API traffic to detect distillation-style patterns. The trouble is that distillation traffic and legitimate automated evaluation traffic share characteristics — high volume, systematic and repetitive prompts, and broad coverage of model behavior — which is exactly why false positives are hard to rule out.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/tashfeenahmed/freellmapi">tashfeenahmed/freellmapi: 10.1 billion tokens per month. 87 free LLM ...</a></li>
<li><a href="https://docs.litellm.ai/docs/">Getting Started | liteLLM</a></li>

</ul>
</details>

**Discussion**: Commenters were largely sympathetic and skeptical of the enforcement process, recommending that the founder first validate the evidence packet by submitting it to Claude itself, since Anthropic's reviewers will likely use Claude too. Others advised migrating to Claude via Amazon Bedrock to get a human account representative, questioned why anyone should keep paying a provider that treats customers this way, and noted that if accounts can be dropped over prompt content, deliberately planted distillation-style instructions could become a prompt-injection attack vector.

**Tags**: `#AI policy`, `#Anthropic`, `#model distillation`, `#API terms of service`, `#LLM providers`

---

<a id="item-6"></a>
## [Community Project Runs Leaked GTA 6 Xbox Build on Windows](https://twitter.com/raul_bs3/status/2125213756238291075) ⭐️ 8.0/10

A community reverse-engineering effort has gotten the leaked Xbox build of GTA 6 to run on Windows PCs using a Wine-like compatibility/recompilation approach. Two projects, xcl and Victory (with the related static-recompilation framework Leonida), are the main efforts driving this, reportedly working from an executable leaked by the group Cyberleek. It demonstrates how thin the technical gap between modern Xbox consoles and Windows PCs has become, making fan-driven "ports" of console exclusives plausible long before official PC releases. The case also puts a spotlight on the legal and ethical limits of game preservation and reverse engineering, and on how publishers might respond with stronger anti-tamper or always-online protections. According to community members, the Xbox build lacks any special DRM or obfuscation and modern Xbox hardware is essentially a Windows PC with extra console-specific components, so the hard problems are compatibility shims and graphics translation rather than cracking protection. One notable data point from the discussion is that a related project, Leonida, was previously banned from GitHub while its lead developer was still in school.

hackernews · andrem · Nov 24, 13:19 · [Discussion](https://news.ycombinator.com/item?id=50627783)

**Background**: Static recompilation is a technique that translates a console binary's machine code (for example, PowerPC instructions from an Xbox 360 game) into C or another high-level language, which is then compiled to run natively on x86-64 or ARM64 — something between emulation and a true native port. Wine works differently: it is a compatibility layer that intercepts Windows API calls and translates them into the host operating system's equivalents, for instance mapping DirectX to OpenGL or Vulkan, so Windows executables run without a full virtual machine. Because the current Xbox runs a Windows-derived OS on PC-like AMD hardware, a Wine-style layer can, in principle, host console game code with relatively modest adaptation.

<details><summary>References</summary>
<ul>
<li><a href="https://gta6recomp.com/leonida">Leonida — GTA 6 PC Static Recompilation Project Tracker & Source</a></li>
<li><a href="https://github.com/ivall/xcl">ivall/xcl: Xbox Series compatibility layer for Windows - runs console ...</a></li>
<li><a href="https://heldgames.com/guides/retro-decompilation-recompilation-explained">What Decompiled and Recompiled Games Actually Are... | Held Games</a></li>

</ul>
</details>

**Discussion**: Commenters dug into the technical specifics — binary compatibility, graphics translation, DRM/anti-tamper — while others debated legality and industry impact; one widely shared view is that this will not seriously threaten game production, since GTA 6 is enormously profitable and will sell again as DLC and an official PC port. A recurring concern was that the scene's success could push publishers toward cloud-dependent components or always-online designs that make games impossible to decompile or preserve.

**Tags**: `#game-reverse-engineering`, `#binary-compatibility`, `#wine`, `#game-preservation`, `#drm`

---

<a id="item-7"></a>
## [Simon Willison Maps Three LLM Inflection Points in Twelve Months](https://simonwillison.net/2026/Nov/24/llm-inflection-points/) ⭐️ 8.0/10

Simon Willison published a retrospective post built from his AI Engineer Code Summit keynote, arguing that LLM and coding-agent capabilities crossed three distinct inflection points in the past twelve months, and used the one-year anniversary of Claude Opus 4.5 (released November 24, 2025) as his anchor. The visible portion of the post details two of them: the November 2025 shift where Claude Opus 4.5 and OpenAI's GPT-5.1 / GPT-5.1-Codex models made coding agents reliably useful by default, and the June/July 2026 arrival of what he calls "Fable class models." The post offers a practitioner's historical framing for a fast-moving field, arguing that agent reliability — not benchmark scores — is the real dividing line between tools that accelerate engineering work and tools that merely add review overhead. For teams deciding when and how to adopt coding agents, Willison's timeline suggests capability jumps arrive in sudden, discrete steps rather than gradual improvement. Willison defines "Fable class models" as systems where, if you can state a goal and supply the necessary tools, they can brute-force their way to solving the problem — illustrated by Claude Fable spinning up its own pyobjc-framework-Quartz screenshot mechanism and a CORS-enabled localhost logging server to debug a Safari display glitch. He also notes that Claude Fable 5 was briefly pulled under US export controls in June 2026 before returning on July 1st, and that the published text is truncated before the third inflection point is revealed.

rss · Simon Willison · Nov 24, 23:02

**Background**: Claude Opus 4.5, released by Anthropic on November 24, 2025, sits in the top tier of Anthropic's Haiku/Sonnet/Opus naming scheme and was widely noted for strong performance on coding and agentic tasks. Claude Code is Anthropic's terminal-based coding agent, first introduced alongside Claude 3.7 Sonnet in February 2025; such agents inspect repositories, edit files, run terminal commands and execute tests on the developer's behalf. In 2026 Anthropic also produced a more capable model, Claude Mythos, which it withheld from general release over cybersecurity concerns, then shipped a restricted version called Claude Fable that blocks security-related use.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Claude_Opus_4.5">Claude Opus 4.5</a></li>
<li><a href="https://en.wikipedia.org/wiki/Claude_(AI)">Claude (AI) - Wikipedia</a></li>
<li><a href="https://cursor.com/learn/working-with-agents">Working with Agents | Cursor Learn</a></li>

</ul>
</details>

**Tags**: `#LLMs`, `#coding agents`, `#AI engineering`, `#Claude Opus`, `#software development`

---

<a id="item-8"></a>
## [GPT-6.2 Astra Autonomously Identifies Author of Anonymous 1808 Sketchbook](https://simonwillison.net/2026/Nov/24/astra-historical-mystery/) ⭐️ 8.0/10

Historian Mark Humphries documented that GPT-6.2 Astra, given only minimal prompting, autonomously identified the creator of an anonymous 1808 sketchbook held at Yale's Beinecke Library in just 22 minutes using publicly available primary and secondary sources. In the process, the model located a little-known document in a paper archive, predicted it would confirm its hypothesis, and was proven correct. This is a concrete case study of an LLM functioning as an autonomous research agent that produced a genuinely novel scholarly result, rather than merely summarizing existing knowledge. It suggests AI agents may soon reshape open-ended archival and humanities research workflows, and it raises the question of how disciplines respond when machines can do work humans could not easily do. The key clue was a diary reference to a visit by the vicomte de Chabot dated five days before a date noted in the sketchbook near a river, leading Astra to propose that Chabot's travel journal — obtainable only by order from Cleveland State University — would confirm authorship. Humphries notes this is a single anecdotal case rather than a benchmark, though the newly surfaced archival source is itself a significant find for Canadian and fur trade historians.

rss · Simon Willison · Nov 24, 16:53

**Background**: GPT-6.2 Astra is part of OpenAI's GPT-6.2 model family, released on November 17, 2026 alongside GPT-6.2 Sol and available only to paid users; early reviews from power users were mixed. An autonomous agent is an AI system that can independently plan and carry out multi-step tasks such as browsing, searching and reasoning over sources. The Beinecke Library is Yale University's rare book and manuscript library, which has digitized part of its collection — including the sketchbook in question — for public access online.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/GPT-6.2_Astra">GPT-6.2 Astra</a></li>
<li><a href="https://simonwillison.net/2026/Nov/17/gpt62-astra-and-sol/">GPT ‑ 6 . 2 Astra and GPT ‑ 6 . 2 Sol | Simon Willison’s Weblog</a></li>
<li><a href="https://en.wikipedia.org/wiki/Autonomous_agent">Autonomous agent</a></li>

</ul>
</details>

**Discussion**: Humphries himself predicts a "mild" crisis of confidence for historians, comparing it to how mathematics has reacted to AI systems that solve hard problems — but argues history will be less shaken because historians reinterpret the past rather than chase a single universal truth, and because historical writing is closer to philosophy and literature, where humanity remains a requirement. Simon Willison frames the result as a notable data point for AI-assisted search and agentic research.

**Tags**: `#AI research agents`, `#LLMs`, `#digital humanities`, `#autonomous agents`, `#historical research`

---

<a id="item-9"></a>
## [Huawei and Qualcomm sign broad multi-year patent cross-license covering 5G, AI](https://t.me/zaihuapd/45344) ⭐️ 8.0/10

Huawei officially announced a multi-year, broad patent cross-licensing agreement with Qualcomm covering 5G, computing, AI and networking portfolios, under which Qualcomm will also purchase some of Huawei's US patents. According to Bloomberg, citing a Huawei spokesperson, Qualcomm has additionally agreed to license patents related to Huawei's "logic folding" chip manufacturing technology, and Huawei expects the cumulative contract value of its patent licensing deals to exceed $6.9 billion (about 46.3 billion RMB) once the transaction closes after required regulatory approvals. The deal links two of the largest players in telecom and mobile chips and, at over $6.9 billion in expected cumulative value, represents one of the biggest patent arrangements in the industry, effectively settling years of friction between Huawei and Qualcomm. The reported inclusion of Huawei's logic-folding technology is especially significant because it suggests the company may monetize a homegrown workaround for advanced-node manufacturing constraints imposed by US export controls. The agreement covers cross-licensing of patent portfolios rather than a one-way license, and it still requires regulatory approval before closing. Huawei notes that its IP licensing business has generated positive revenue since 2021, and the patent transfers to Qualcomm are limited to a subset of Huawei's US patents rather than its entire portfolio.

telegram · zaihuapd · Nov 24, 11:38

**Background**: Patent cross-licensing lets companies avoid litigation by granting each other access to large portfolios of inventions, and in 5G it is standard practice because no single vendor holds all the essential patents. Huawei's "logic folding" technology, presented by semiconductor chief Teresa He at a May 2026 circuits conference, is a 3D IC and advanced-packaging approach that stacks complete logic circuits face-to-face using hybrid bonding so signals travel shorter distances, improving density and energy efficiency instead of relying on smaller transistors. Huawei positions this as a path around Moore's Law limits and US manufacturing restrictions, and it is expected to appear in 2026 Kirin processors.

<details><summary>References</summary>
<ul>
<li><a href="https://baike.baidu.com/item/逻辑折叠技术/67870423">逻辑折叠技术 - 百度百科</a></li>
<li><a href="https://insightsintegration.com/logic-folding-explained-huaweis-chip-packaging-breakthrough-that-could-redefine-the-ai-race/">Logic Folding Explained: Huawei's Chip Packaging Breakthrough ...</a></li>
<li><a href="https://www.huaweicentral.com/huawei-logicfolding-architecture-everything-you-need-to-know/">Huawei LogicFolding Architecture: Everything you need to know</a></li>

</ul>
</details>

**Tags**: `#Huawei`, `#Qualcomm`, `#patent-licensing`, `#5G`, `#semiconductors`

---

<a id="item-10"></a>
## [VMware vCenter Hit by Another 9.8 Auth Bypass, Exploited as Zero-Day](https://thehackernews.com/2026/11/vmware-vcenter-hit-by-another-critical.html) ⭐️ 8.0/10

Broadcom published fixes for 23 vulnerabilities across its VMware product line, headlined by CVE-2026-123903, a 9.8-rated authentication bypass in the vCenter Directory Service (vmdir) that lets anyone with network access to vCenter walk straight into the system without credentials. The flaw had already been exploited in the wild as a zero-day in the days before the patch shipped. vCenter is the control plane for enterprise vSphere, so an unauthenticated bypass there effectively hands an attacker administrative control over every managed ESXi host and virtual machine in the estate. Coming only days after a separate 9.8-severity vmdir authentication bypass, it signals that attackers are actively and successfully mining this specific component, making immediate patching a priority for virtually every large virtualization environment. The vulnerability requires only network reachability to the vCenter deployment — no valid credentials and no user interaction — and Broadcom has listed no workarounds, leaving patching as the only remediation. Because exploitation occurred before the fix was available, defenders should treat any exposed vCenter instance as potentially compromised and hunt for indicators of compromise rather than simply applying the update.

telegram · zaihuapd · Nov 24, 14:50

**Background**: VMware vCenter is Broadcom's centralized management platform for vSphere, used to administer clusters of ESXi hypervisors and the virtual machines running on them. VMware Directory Service, or vmdir (running as the vmdird process on the vCenter Server Appliance), is a multi-master LDAP directory that stores authentication, certificate, lookup and licensing data for the platform — which is why an authentication bypass in it is so severe. CVSS 9.8 is the top end of the "Critical" band, generally reserved for remotely exploitable flaws that require no privileges or user action. This incident follows advisory VMSA-2026-0009, published on November 19, 2026, which addressed a separate 9.8-rated vmdir authentication bypass tracked as CVE-2026-123890.

<details><summary>References</summary>
<ul>
<li><a href="https://thehackernews.com/2026/11/critical-vmware-vcenter-flaw-cvss-98.html">Critical VMware vCenter Zero-Day Flaw Lets Network Attackers ...</a></li>
<li><a href="https://www.rapid7.com/blog/post/etr-cve-2026-123890-critical-authentication-bypass-vmware-vcenter/">CVE-2026-123890: Critical Authentication Bypass in VMware vCenter</a></li>
<li><a href="https://nhimg.org/glossary/vmdir/">What Is vmdir ? Definition & Examples</a></li>

</ul>
</details>

**Tags**: `#security`, `#vmware`, `#vulnerability`, `#cve`, `#enterprise-infrastructure`

---

<a id="item-11"></a>
## [SpaceX and Tesla Boards Form Special Committees to Review Possible Merger](https://t.me/zaihuapd/45351) ⭐️ 8.0/10

The boards of SpaceX and Tesla have each formed special committees made up of independent directors to evaluate a potential merger between the two companies. Elon Musk said the committees were created at shareholders' request and that he will recuse himself from the discussions due to a conflict of interest, adding that no deal terms have been agreed. A combination of the world's leading private launch provider and the largest pure-play electric vehicle maker would concentrate Musk-controlled assets into a single entity, reshaping both the space and automotive industries. Because Musk is CEO and a major shareholder of both companies, the special-committee structure signals that governance and conflict-of-interest concerns will be central to whether any deal advances. Musk supports the idea but stressed the deal is far from certain and will ultimately require shareholder backing; a vote among SpaceX shareholders would be relatively easy to secure, whereas Tesla would need approval from 50% of all shareholders. The special committees consist of independent directors, and no transaction terms have yet been negotiated.

telegram · zaihuapd · Nov 25, 00:41

**Background**: SpaceX is Musk's privately held rocket and satellite company, while Tesla is a publicly traded electric vehicle and energy firm; the two share Musk as chief executive and overlap in areas such as satellite broadband and advanced manufacturing. Special committees of independent directors are a standard corporate-governance mechanism used when a transaction poses conflicts of interest for management or controlling shareholders. Because SpaceX is not publicly listed, any merger would involve complex valuation and share-exchange questions alongside regulatory review.

**Tags**: `#SpaceX`, `#Tesla`, `#merger`, `#Elon Musk`, `#corporate governance`

---