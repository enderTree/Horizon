---
layout: default
title: "Horizon Summary: 2026-11-22 (EN)"
date: 2026-11-22
lang: en
---

> From 24 items, 8 important content pieces were selected

---

1. [Lean community reports formal verification of the (Generalized) Riemann Hypothesis](#item-1) ⭐️ 9.0/10
2. [Zhejiang University Demonstrates First Real-Hardware QRAM on Superconducting Chip](#item-2) ⭐️ 9.0/10
3. [GnuPG Issues Security Advisory for GPGME Double-Free Bug](#item-3) ⭐️ 8.0/10
4. [Microsoft ships RDMA over USB4 preview, letting several PCs run one local AI model](#item-4) ⭐️ 8.0/10
5. [OpenRouter warns MiniMax prompts may have been read by third parties](#item-5) ⭐️ 8.0/10
6. [Oral daraxonrasib plus chemo hits 60.7% response in first-line pancreatic cancer](#item-6) ⭐️ 8.0/10
7. [Tesla begins rolling out FSD v15 overseas with new Reality View](#item-7) ⭐️ 8.0/10
8. [US Commerce to finalize rule closing Chinese AI firms' remote chip access](#item-8) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Lean community reports formal verification of the (Generalized) Riemann Hypothesis](https://leanprover-community.github.io/blog/posts/riemann-hypothesis/) ⭐️ 9.0/10

The Lean prover community published a blog post announcing a formal verification of the Riemann Hypothesis — apparently in its Generalized form (GRH) — carried out with substantial AI assistance from Claude plus human expert guidance, reportedly from a collaborator named Levent. The claim triggered a large Hacker News thread (931 points, 791 comments) that scrutinized how the proof was checked and how much of modern mathematics had to be formalized along the way. If it holds up, a machine-checked proof of GRH would be a landmark for both analytic number theory and formal verification, since GRH implies strong bounds on primes in arithmetic progressions and underpins a great deal of modern number theory. The discussion also suggests the effort required formalizing a huge chunk of contemporary mathematics, which would make it as much a milestone for math foundations and AI-assisted formalization as for the conjecture itself. Skeptics point out that a fake refutation of the Collatz conjecture previously slipped past one supposedly independent checker, and that the independence of the major kernels and consistency checkers (con-leche and con-ron) is often overstated. Defenders counter that a bug would now have to exist simultaneously in every kernel and also corrupt the self-consistency proofs, and that having a human expert in the loop makes an AI simply hacking its way through far less likely.

hackernews · g-b-r · Nov 21, 14:36 · [Discussion](https://news.ycombinator.com/item?id=50589618)

**Background**: Lean is an open-source proof assistant and functional programming language in which proofs are written so that a small trusted core — the kernel — can check them mechanically, which is the basis of formal verification. The Riemann Hypothesis, one of mathematics' most famous open problems, states that all non-trivial zeros of the Riemann zeta function lie on the critical line; the Generalized Riemann Hypothesis extends this to a broader family of L-functions, notably Dirichlet L-functions. Because such proofs are enormous, formalization is usually split across independent kernels and separately verified checkers, and the trustworthiness of the result depends on those components failing independently rather than together.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Generalized_Riemann_hypothesis">Generalized Riemann hypothesis - Wikipedia</a></li>
<li><a href="https://lean-lang.org/learn/">Learn — Lean Lang</a></li>
<li><a href="https://www.anthropic.com/research/formalizing-fermats-last-theorem">Formalizing Fermat's Last Theorem \ Anthropic</a></li>

</ul>
</details>

**Discussion**: Commenters converge on cautious optimism: one argues the chance of a proof exploiting a bug is now vanishingly small because multiple kernels in different languages, including con-leche and con-ron with self-consistency proofs, would all have to be wrong at once. Others raise the precedent of the fake Collatz refutation passing an independent checker, credit the human collaborator Levent for drawing so much out of Claude, and note that the real headline may be how much of modern mathematics had to be formalized to get there.

**Tags**: `#formal-verification`, `#lean`, `#riemann-hypothesis`, `#ai-theorem-proving`, `#mathematics`

---

<a id="item-2"></a>
## [Zhejiang University Demonstrates First Real-Hardware QRAM on Superconducting Chip](https://finance.sina.com.cn/stock/2026-11-21/doc-iniznhsk3530826.shtml) ⭐️ 9.0/10

Zhejiang University researchers reported the first real-machine demonstration of a quantum random access memory (QRAM), running 4-bit and 8-bit prototypes on their self-fabricated superconducting 'Tianmu 2' chip with readout accuracies of 80.9% and 60.4%, respectively; the work was published in Nature Physics. QRAM is a long-sought building block for quantum algorithms such as Grover search and quantum linear algebra, and a real-hardware demonstration moves the field beyond theoretical proposals toward practical quantum memory. It also gives experimental support for the noise-resilience claims of the bucket-brigade architecture, which could guide future scalable QRAM designs. The 4-bit and 8-bit prototypes correspond to 16 and 256 memory cells, and the team reports more than 30% lower circuit depth than unoptimized schemes plus the first experimental validation of local noise resilience in this architecture; however, 60.4% readout accuracy for 8-bit data is still far below what fault-tolerant applications require.

telegram · zaihuapd · Nov 21, 08:31

**Background**: A quantum random access memory (QRAM) lets a quantum computer look up data at an address that can be in a superposition of many addresses, potentially retrieving information with exponentially fewer memory resources than classical RAM. Most proposed implementations use a bucket-brigade architecture, in which address qubits route a query through a tree of quantum switches; this requires deep circuits and is highly sensitive to noise. Superconducting circuits are one of the leading platforms for quantum computing, but demonstrating QRAM on real hardware has remained difficult because of these depth and fidelity constraints.

<details><summary>References</summary>
<ul>
<li><a href="https://news.mydrivers.com/1/1167/1167501.htm">news.mydrivers.com/1/1167/1167501.htm</a></li>
<li><a href="https://github.com/IAI-USTC-Quantum/QRAM-Simulator">GitHub - IAI-USTC-Quantum/ QRAM -Simulator: Efficient quantum...</a></li>

</ul>
</details>

**Tags**: `#quantum computing`, `#QRAM`, `#superconducting qubits`, `#quantum memory`, `#research breakthrough`

---

<a id="item-3"></a>
## [GnuPG Issues Security Advisory for GPGME Double-Free Bug](https://lists.gnupg.org/pipermail/gnupg-announce/2026q4/000517.html) ⭐️ 8.0/10

GnuPG published a security advisory for GPGME covering a double-free vulnerability that was reported to the project after being discovered by Johan Carlsson and flagged by GitLab on 2026-11-12. A coordinated disclosure initially planned for 2026-11-25 was moved up to 2026-11-20 because GitLab had to ship updates early for the unrelated Ruby2Shell bug. GPGME is the C library that most applications use to add OpenPGP encryption and signature support, so a memory-corruption flaw there reaches far beyond the GnuPG command-line tools. It is especially sensitive for GitLab, which supports signed commits and would treat code execution along that path as severe, and community members note that everything linking GPGME before version 2.3.0 — mail clients, XMPP clients, Samba, Flatpak, Gpg4win — is in scope. Commenters stress that this is a double-free rather than a ready-made remote code execution chain, and one notes that conventional tooling had already flagged the issue in Red Hat's packaging roughly five years ago, though upstream apparently missed the fix. Affected parties are advised to check their bundled or statically linked GPGME builds, since distributions that do not use the library directly — such as apt — are reportedly not affected.

hackernews · gdgghhhhh · Nov 21, 08:32 · [Discussion](https://news.ycombinator.com/item?id=50587208)

**Background**: GPGME (GnuPG Made Easy) is a C library that gives applications a high-level API for encryption, decryption, signing and key management on top of GnuPG, so developers can add OpenPGP support without shelling out to the gpg binary. A double-free occurs when free() is called twice on the same memory address, corrupting the allocator's bookkeeping and potentially leading to crashes or exploitable heap corruption. Bugs of this class are a major reason the industry is pushing memory-safe languages and stricter tooling for C and C++ codebases.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Memory_safety">Memory safety - Wikipedia</a></li>

</ul>
</details>

**Discussion**: The Hacker News thread mixes practical triage with meta-debate: posters try to scope which software actually links GPGME, question whether the report overstates severity by implying an RCE chain, and argue that C/C++ should not be written without Rust-level tooling to catch such defects. There is also skepticism toward the disclosure process, given that downstream packaging had apparently caught the bug years before upstream did.

**Tags**: `#security`, `#GnuPG`, `#GPGME`, `#vulnerability`, `#memory-safety`

---

<a id="item-4"></a>
## [Microsoft ships RDMA over USB4 preview, letting several PCs run one local AI model](https://videocardz.com/newz/microsoft-brings-rdma-over-usb4-to-windows-allowing-multiple-pcs-to-run-one-local-ai-model) ⭐️ 8.0/10

Microsoft released a developer preview of RDMA over USB4 for Windows, which lets multiple PCs pool their memory and GPU compute over ordinary USB4 cables and run a single large local AI model without dedicated network cards or switches. In the demo, three AMD Ryzen AI Max+ 395 machines jointly ran the 4-bit quantized Qwen3-235B-A22B model at roughly 18.5 tokens per second, and the feature will roll out through Windows Insider. This turns commodity consumer PCs into a small inference cluster using ports and cables people already own, lowering the barrier for running models that are far too large for any single machine. It could reshape local-AI workflows for hobbyists, small studios and privacy-sensitive teams that want large-model capability without cloud dependency or datacenter hardware. The preview communicates over standard USB4 links, so it avoids the specialized RDMA-capable NICs and switches normally required, and Microsoft positions it as a developer preview delivered via Windows Insider rather than a finished consumer feature. The demo pairs three Ryzen AI Max+ 395 systems with a 4-bit quantized Qwen3-235B-A22B mixture-of-experts model, where only about 22B of the 235B total parameters are activated per token, keeping the compute burden manageable across pooled devices.

telegram · zaihuapd · Nov 21, 06:13

**Background**: RDMA (remote direct memory access) lets one machine read and write another machine's memory directly, bypassing the CPU and OS network stack; it has traditionally required InfiniBand or RoCE-capable network cards in datacenters. USB4 is a high-speed consumer interconnect (up to 40 Gbps and beyond in newer revisions) that can tunnel PCIe and networking traffic, making it a plausible transport for RDMA between ordinary laptops and mini-PCs. Qwen3-235B-A22B is Alibaba's flagship open mixture-of-experts model with 235B total and 22B active parameters, and 4-bit quantization compresses weights from FP16 to INT4, cutting memory footprint by roughly 75% so a model of this size can be split across several machines' combined RAM and VRAM.

<details><summary>References</summary>
<ul>
<li><a href="https://www.geekfan.net/news/1120313205.html">微软推出 USB4 RDMA 多 Win11 协同 AI 方案，多电脑搭积木式合并内存...</a></li>
<li><a href="https://news.qq.com/rain/a/20261122A05M1M00">不用交换机！微软Windows11上线USB4 RDMA：多机合体做AI推理</a></li>
<li><a href="https://baike.baidu.com/item/Qwen3-235B-A22B/67420648">Qwen3-235B-A22B_百度百科</a></li>

</ul>
</details>

**Tags**: `#RDMA`, `#USB4`, `#local-llm-inference`, `#distributed-systems`, `#microsoft-windows`

---

<a id="item-5"></a>
## [OpenRouter warns MiniMax prompts may have been read by third parties](https://news.ycombinator.com/item?id=50585962) ⭐️ 8.0/10

OpenRouter notified users by email that prompts sent to MiniMax models may have been read by third parties, after a security researcher embedded unique canary URLs in prompts submitted to those models between July and October 2026 and observed outsiders fetching those URLs 40 to 130 hours later. OpenRouter attributed the problem to MiniMax and its forwarding partners AtlasCloud, Novita and StreamLake, stripped the "zero data retention" label from the affected endpoints, and advised users who had exposed sensitive credentials to rotate API keys and passwords. The incident undermines a core promise of API routing layers: that a single gateway can vouch for the data-handling behavior of every model and reseller behind it. Developers who route sensitive prompts through hosted LLM APIs — and especially those who relied on the zero data retention label for compliance — must now treat such labels as claims to verify rather than guarantees. The evidence came from canary URLs — unique, per-prompt links whose access logs reveal when and whether someone else read the payload — with fetches occurring well after the response had been returned, which points to storage and later reprocessing rather than transient in-flight handling. Notably, OpenRouter's own website had not published an advisory at the time of the report, so the warning circulated mainly through direct email to affected users.

telegram · zaihuapd · Nov 21, 06:53

**Background**: OpenRouter is a routing and marketplace layer that lets developers call many different models from many providers through one API and one billing account, which means a prompt may pass through several intermediaries before reaching the model. "Zero data retention" (ZDR) is a provider commitment that a prompt exists in the system only long enough to generate a response and is then discarded, a promise enterprise and compliance-sensitive customers often depend on. MiniMax is a Chinese model developer whose models are also served through third-party inference resellers such as AtlasCloud, Novita and StreamLake, so a request can traverse multiple operators whose logging practices may differ from the model owner's own policy.

<details><summary>References</summary>
<ul>
<li><a href="https://openrouter.ai/blog/insights/zero-data-retention/">Zero Data Retention (ZDR): What It Means for AI APIs</a></li>
<li><a href="https://platform.kimi.com/docs/guide/zero-data-retention">什么是零数据保留（ZDR）？ - Kimi API 开放平台</a></li>
<li><a href="https://www.streamlake.com/">StreamLake 溪流湖 | 行业领先的AI大 模 型 平台与音视频云 服 务 商</a></li>

</ul>
</details>

**Tags**: `#security`, `#privacy`, `#LLM APIs`, `#OpenRouter`, `#data retention`

---

<a id="item-6"></a>
## [Oral daraxonrasib plus chemo hits 60.7% response in first-line pancreatic cancer](https://event.eortc.org/ena2026/2026/11/20/metastatic-pancreatic-cancer-responds-well-to-initial-treatment/) ⭐️ 8.0/10

At the EORTC-NCI-AACR (ENA 2026) meeting in Barcelona on November 20, investigators presented late-breaking Phase I/II data showing that oral daraxonrasib 200 mg once daily plus gemcitabine/nab-paclitaxel produced a confirmed objective response rate of 60.7% and a complete response rate of 8.2% (roughly 1 in 12) in 61 previously untreated patients with metastatic pancreatic ductal adenocarcinoma. The regimen also achieved a 90.2% disease control rate, a median progression-free survival of 12.8 months, and a 12-month overall survival rate of 76.6% at a median follow-up of 18.3 months. Metastatic pancreatic cancer is one of the deadliest solid tumors, with historical 1-year survival on chemotherapy in the 22%–48% range, so a first-line oral targeted-plus-chemo combination showing this level of response and survival signals could meaningfully shift the treatment paradigm if confirmed. It also marks a broadening of RAS-targeted therapy beyond single-mutation KRAS G12C drugs toward multi-selective pan-RAS inhibition in a tumor type where KRAS mutations are near-universal. The study is a single-arm Phase I/II trial with no chemotherapy control arm, and the principal investigator explicitly said efficacy comparisons must await the ongoing Phase III trial; the 1-year survival benchmark for chemotherapy comes from MPACT (35% for nab-paclitaxel plus gemcitabine) and mFOLFIRINOX (48%), so claims that results are 'far above chemotherapy' are not appropriate. Mechanistically, daraxonrasib is an oral RAS(ON) multi-selective inhibitor that binds the active GTP-bound state of RAS via cyclophilin A and covers multiple KRAS/NRAS mutations rather than only G12C, and it was approved by the FDA on August 26 under the brand name RASONQUE for previously treated patients based on the Phase III RMC-302 trial (median overall survival 13.2 vs 6.7 months).

telegram · zaihuapd · Nov 21, 11:24

**Background**: Pancreatic ductal adenocarcinoma is notoriously resistant to most therapies, and roughly 90% of cases carry a KRAS mutation, but the first generation of KRAS drugs only targeted the G12C variant, which is rare in pancreatic cancer. RAS proteins act as molecular switches that are 'on' when bound to GTP, and daraxonrasib belongs to a newer class of tri-complex inhibitors that use the chaperone protein cyclophilin A to shut down the active, GTP-bound form of multiple RAS mutants. The MPACT trial established nab-paclitaxel plus gemcitabine as a standard first-line chemotherapy backbone in metastatic disease, with median overall survival around 8.5–8.7 months, which is the benchmark against which this new combination is being judged.

<details><summary>References</summary>
<ul>
<li><a href="https://www.webmd.com/cancer/pancreatic-cancer/pancreatic-cancer-rasonque">What to Know About Rasonque for Pancreatic Cancer</a></li>
<li><a href="https://physicianresources.dana-farber.org/news/ras-on-inhibitor-daraxonrasib-shows-promising-results-in-advanced-pancreatic-cancer-phase-1/2-study">RAS ( ON ) Inhibitor Daraxonrasib Shows Promising Results in...</a></li>
<li><a href="https://www.drugs.com/rasonque.html">Rasonque ( daraxonrasib ): Uses, Dosage, Side Effects</a></li>

</ul>
</details>

**Tags**: `#pancreatic cancer`, `#daraxonrasib`, `#RAS inhibitor`, `#oncology`, `#clinical trial`

---

<a id="item-7"></a>
## [Tesla begins rolling out FSD v15 overseas with new Reality View](https://x.com/Tesla/status/2124222447855743019) ⭐️ 8.0/10

Tesla announced on X that it has started pushing FSD v15 to vehicles overseas, claiming that its end-to-end driving network now handles safety-critical cases 25 times better than before. The release also introduces a new "Tesla Reality View" visualization that overlays live camera imagery and FSD's driving plan on the in-car screen, plus a long list of driving refinements. FSD v15 is a major version jump for Tesla's supervised autonomous-driving software, and the claimed 25x safety improvement — if it holds up — would be one of the largest single-release gains the program has reported, directly affecting how much drivers trust and use the system. The new generative visualization also signals Tesla's broader bet that rendering a clear picture of what the neural network perceives is key to winning over passengers and regulators. According to the release notes circulating online, v15 upgrades every part of the end-to-end driving network and improves road-debris offsetting for tires, tree branches and boxes, along with unprotected turns and speed control in school zones and bad weather. Reality View supports full-screen, map and split-screen layouts with a quiet mode, and adds turn-by-turn style overlays on the visualization, while the turn-signal chime is now softer and fades out gradually; notably, the 25x figure is Tesla's own claim and has not been independently verified.

telegram · zaihuapd · Nov 22, 00:03

**Background**: Tesla's Full Self-Driving (FSD) is an advanced driver-assistance package that, under the driver's supervision, can handle most driving tasks on city streets and highways — it is not a fully autonomous system, and Tesla officially labels the current version "Full Self-Driving (Supervised)". Since shifting to an end-to-end neural-network approach, Tesla no longer hand-codes driving rules; instead a single large model maps camera input directly to driving decisions, so each major version like v15 reflects a wholesale retraining of that network. Tesla has been teasing v15 for some time, with Elon Musk promising the new interface would "render reality in a mind-bending way".

<details><summary>References</summary>
<ul>
<li><a href="https://www.tesla.com/fsd">Full Self - Driving (Supervised) | Tesla</a></li>
<li><a href="https://www.notateslaapp.com/news/5057/tesla-fsd-v15-coming-next-month-with-holiday-update-musk">Tesla FSD V 15 Arriving Next Month: Home Garage... - Not a Tesla App</a></li>
<li><a href="https://www.youtube.com/watch?v=ur6qSANo_M4">Tesla FSD V 15 Blew My Mind! (First Drive ) - YouTube</a></li>

</ul>
</details>

**Tags**: `#Tesla`, `#FSD`, `#autonomous-driving`, `#AI`, `#release`

---

<a id="item-8"></a>
## [US Commerce to finalize rule closing Chinese AI firms' remote chip access](https://t.me/zaihuapd/45289) ⭐️ 8.0/10

The US Commerce Department is finalizing a rule that would block Chinese AI companies from remotely accessing advanced AI chips hosted in overseas data centers, with publication possible as soon as this month. The controls would extend beyond existing semiconductor export restrictions to seven additional countries — reportedly including Malaysia, Singapore, and Thailand — in an effort to close remote-access and chip-smuggling loopholes, and the department is still consulting other government agencies before issuing the final text. This marks a significant escalation in US-China tech restrictions by targeting compute access rather than just physical chip shipments, potentially cutting off a workaround that Chinese AI labs have relied on to train frontier models. It would directly affect Chinese AI developers, overseas data center and cloud operators in Southeast Asia, and NVIDIA, whose hardware underpins most of that remote compute. The rule is being drafted with inter-agency consultation and follows a White House request that Congress legislate to require Commerce to write it. NVIDIA has reportedly lobbied against closing the remote-access gap, arguing that US AI infrastructure needs to win globally, and the exact scope of the seven covered countries and enforcement mechanisms has not been publicly confirmed.

telegram · zaihuapd · Nov 22, 04:34

**Background**: Since 2022, the US has progressively restricted exports of high-performance AI chips such as NVIDIA's most advanced accelerators to China, aiming to slow Chinese development of frontier AI and advanced computing. Those rules govern the physical shipment of hardware, but they left a gap: a Chinese company could rent time on chips installed in a data center outside China and use that compute remotely to train models. Reports have described Chinese labs, including Moonshot AI, exploring access to NVIDIA chips hosted in overseas facilities such as those in Europe, which is the loophole this rule is meant to close.

<details><summary>References</summary>
<ul>
<li><a href="https://www.cnbc.com/2026/11/05/moonshot-ai-nvidia-chips-europe-china.html">China's Moonshot AI sought Nvidia chip access in Europe amid...</a></li>
<li><a href="https://forklog.com/en/china-accesses-nvidia-chips-via-overseas-data-centers/">China Accesses Nvidia Chips via Overseas Data Centers | ForkLog</a></li>
<li><a href="https://forums.hardwarezone.com.sg/threads/us-to-restrict-chinese-remote-access-to-ai-chips-from-southeast-asian-data-centers-report.7231761/">US to restrict Chinese remote access to AI chips from Southeast...</a></li>

</ul>
</details>

**Tags**: `#export-controls`, `#AI-chips`, `#US-China-tech`, `#semiconductors`, `#AI-policy`

---