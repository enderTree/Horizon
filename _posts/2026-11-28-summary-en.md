---
layout: default
title: "Horizon Summary: 2026-11-28 (EN)"
date: 2026-11-28
lang: en
---

> From 29 items, 8 important content pieces were selected

---

1. [Critical 9.8 NFS Server Flaw Allows Pre-Auth Root](#item-1) ⭐️ 9.0/10
2. [Unkernel compiles a real Linux kernel to WebAssembly for the browser](#item-2) ⭐️ 8.0/10
3. [State AGs sue SpaceX to stop Grok generating CSAM and revenge porn](#item-3) ⭐️ 8.0/10
4. [False computer-checked proofs](#item-4) ⭐️ 8.0/10
5. [SemiAnalysis Analyzes AWS Trainium3 Inference, Microarchitecture, and TCO vs NVIDIA GB300](#item-5) ⭐️ 8.0/10
6. [CIA and Other US Intelligence Agencies Breached in AI-Assisted Artex Hack](#item-6) ⭐️ 8.0/10
7. [Minecraft Java Edition hit by unpatched 'minecraft2shell' RCE via malicious fonts](#item-7) ⭐️ 8.0/10
8. [Australian Federal Court Orders Apple to Open iPhone to Third-Party App Stores by 2027](#item-8) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Critical 9.8 NFS Server Flaw Allows Pre-Auth Root](https://opensec.in/blog/nfs2root-cve-2026-99362) ⭐️ 9.0/10

OpenSec disclosed CVE-2026-99362, a CVSS 9.8 pre-authentication heap overflow in the Linux kernel NFS server (nfsd) that lets an unauthenticated attacker gain root with a single connection to tcp/2049. The flaw has existed since Linux 3.16 in 2014 and affects hosts running NFSv4.1 or 4.2; fixes shipped in kernels 6.12.117, 6.18.61, 7.3.2 and 7.4-rc1, with the CVE published on November 20, 2026. The attack surface is trivially reachable and requires no credentials, so any internet- or network-exposed NFS file server, NAS appliance or cluster storage node is at risk, and the bug's decade-long lifetime means an enormous installed base of kernels is affected. A pre-auth remote kernel compromise of this severity is among the most serious class of Linux security events, forcing urgent patch-and-reboot cycles across storage infrastructure. Exploitation requires only a single connection to tcp/2049 against a host with NFSv4.1 or 4.2 enabled, and remediation requires upgrading the kernel and rebooting since there is no runtime fix. Organizations that cannot patch immediately should block tcp/2049 at the firewall or restrict NFS access to trusted networks as a stopgap mitigation.

telegram · zaihuapd · Nov 27, 12:57

**Background**: NFS (Network File System) is the long-standing Unix/Linux protocol for sharing files over a network, and on Linux the server side is implemented in-kernel by a component called nfsd, which handles NFS requests directly inside kernel address space. NFSv4.1 and 4.2 are later revisions of the protocol that add features such as sessions and parallel access, and their session-handling code paths are reachable before any user authentication occurs. Because nfsd runs with kernel privileges, a memory-corruption bug there escapes all userspace sandboxing and typically yields full root control of the host.

<details><summary>References</summary>
<ul>
<li><a href="https://opensec.in/blog/nfs2root-cve-2026-99362">NFS2ROOT (CVE-2026-99362): pre-auth root in Linux nfsd | OpenSec</a></li>
<li><a href="https://man7.org/linux/man-pages/man8/nfsd.8.html">nfsd (8) - Linux manual page</a></li>
<li><a href="https://datazone.de/en/aktuelles/nfs-ganesha-vs-kernel-nfsd-truenas/">NFS Ganesha vs. Kernel NFSd : What Makes Sense in... | DATAZONE</a></li>

</ul>
</details>

**Tags**: `#security`, `#linux-kernel`, `#nfs`, `#vulnerability-disclosure`, `#remote-exploit`

---

<a id="item-2"></a>
## [Unkernel compiles a real Linux kernel to WebAssembly for the browser](https://unkernel.dev/) ⭐️ 8.0/10

Unkernel is an open-source project (pithings/unkernel) that compiles a genuine Linux 7.x kernel into a single WebAssembly module which boots to a shell in under a second inside a web browser. Its syscall layer, scheduler, memory management, ext4 filesystem and TCP/IP stack are compiled rather than emulated, and the project also ships an npx runner and a JavaScript SDK. If a full Linux kernel can be compiled to Wasm and run in a tab, the browser becomes a credible sandbox for legacy Linux binaries without spinning up a VM or container. That has direct implications for client-side sandboxing, portable execution of long-tail software, and lightweight edge/serverless runtimes. According to the project docs, only user-space programs are emulated, while the kernel itself runs as compiled Wasm with a real MMU, which is what differentiates it from QEMU-style full-system emulators. In the Hacker News thread a user reported running four concurrent md5sums in the same wall-clock time as a single process, but attempting to install Chromium inside Unkernel and run a nested Unkernel within it did not work.

hackernews · nreece · Nov 28, 03:19 · [Discussion](https://news.ycombinator.com/item?id=50674218)

**Background**: WebAssembly (Wasm) is a portable low-level bytecode format originally designed to run near-native-speed code safely inside web browsers, and it is increasingly used outside the browser as a sandboxed execution target. The Linux kernel is the core of the operating system that handles syscalls, scheduling, memory, filesystems and networking, and it normally talks directly to hardware through an MMU (memory management unit). Traditional browser-based Linux demos rely on emulators like QEMU, which interpret or translate every instruction of both the kernel and user programs; Unkernel instead compiles the kernel ahead of time to Wasm and emulates only user processes, trading generality for speed and a smaller footprint.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/pithings/unkernel">GitHub - pithings/unkernel: A real Linux kernel, compiled to ...</a></li>
<li><a href="https://jamilxt.com/blog/linux-compiled-to-webassembly-unkernel-explained">Linux Compiled to WebAssembly: How unkernel Works and How to ...</a></li>
<li><a href="https://unkernel.dev/">unkernel</a></li>

</ul>
</details>

**Discussion**: The Hacker News reaction was enthusiastic and exploratory: commenters cross-referenced related browser-native projects such as tabc, tabernetes and sidebyside, and several noted that Gary Bernhardt's 2014 talk "The Birth and Death of JavaScript" had essentially predicted this. Others contributed hands-on results, including the four-way md5sum concurrency test, the failed nested-Unkernel-in-Chromium attempt, and a concrete use case of running small backend scripts without provisioning a VM.

**Tags**: `#webassembly`, `#linux-kernel`, `#virtualization`, `#browser-runtime`, `#systems-research`

---

<a id="item-3"></a>
## [State AGs sue SpaceX to stop Grok generating CSAM and revenge porn](https://www.oag.state.va.us/media-center/news-releases/jay-jones/3162-attorneys-general-jones-and-rayfield-file-suit-against-spacex-parent-company-of-x-xai-and-grok-over-creation-and-promotion-of-child-exploitation-and-non-consensual-images-on-platform) ⭐️ 8.0/10

A coalition of state attorneys general, including Virginia's Jay Jones and Rayfield, filed suit against SpaceX — the parent company of X, xAI and Grok — alleging that the Grok chatbot created and promoted child sexual abuse material (CSAM) and non-consensual intimate imagery. The suit seeks to force the company to stop these outputs, making it one of the first major legal actions aimed directly at the outputs of a generative model rather than at the users who request them. This is a significant AI-safety and regulatory milestone because it tests whether model providers, rather than only individual users, bear legal liability for harmful generations. The outcome could shape how every consumer-facing chatbot vendor in the US designs content filters and moderation, and it opens a wider constitutional debate over whether AI-generated sexual imagery counts as protected expression. The action targets Grok specifically, a model marketed for its comparatively permissive, 'rebellious' tone, and the complaint covers both CSAM and non-consensual intimate images, which raise different legal issues since the latter by definition implicates real people. As with most guardrail systems, filtering can be bypassed through prompt manipulation, so a central factual question will be whether Grok's safeguards were fundamentally missing or merely jailbroken by users.

hackernews · DeepLogin · Nov 27, 19:42 · [Discussion](https://news.ycombinator.com/item?id=50670855)

**Background**: Grok is a family of large language models launched by Elon Musk's xAI in November 2023, integrated with the X social network and available on iOS and Android. From the start it was pitched as a less filtered alternative to rivals, with what xAI called a 'rebellious streak' that allows direct, unfiltered answers. 'Guardrails' are the validation and control layers that sit between the user and the model, screening prompts and outputs for policy compliance; unlike alignment baked into the model during training, they operate at the application layer and can be configured or, in principle, bypassed. State attorneys general are the top law-enforcement officers of their states and frequently coordinate on multi-state consumer-protection and public-safety suits.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Grok_(chatbot)">Grok (chatbot) - Wikipedia</a></li>
<li><a href="https://www.coursera.org/articles/what-is-grok">What is Grok? Understanding the AI Chatbot from xAI - Coursera</a></li>
<li><a href="https://fastrouter.ai/feeds/blog/guardrails-generative-ai">What Are AI Guardrails ? A Complete Guide</a></li>

</ul>
</details>

**Discussion**: Commenters were split between demanding accountability for the users who requested the images and questioning how Grok's filters failed so badly — one reader asked whether the model was simply permissive for everyone or had to be deliberately tricked. The most substantive thread raised First Amendment questions, with one commenter arguing that a Supreme Court precedent protects AI-generated CSAM made for personal use as long as no real children are depicted, while noting that revenge porn is legally distinct because it inherently references real people.

**Tags**: `#ai-safety`, `#regulation`, `#legal`, `#generative-ai`, `#content-moderation`

---

<a id="item-4"></a>
## [False computer-checked proofs](https://cr.yp.to/proofs/falseccp.html) ⭐️ 8.0/10

Dan Bernstein's page argues that computer-checked proofs can be false due to soundness bugs in proof checkers, sparking an expert HN discussion about multi-verifier architectures and the real-world risk versus the theoretical gap.

hackernews · _tk_ · Nov 27, 15:26 · [Discussion](https://news.ycombinator.com/item?id=50667989)

**Tags**: `#formal-verification`, `#proof-assistants`, `#Lean`, `#Metamath`, `#software-security`

---

<a id="item-5"></a>
## [SemiAnalysis Analyzes AWS Trainium3 Inference, Microarchitecture, and TCO vs NVIDIA GB300](https://newsletter.semianalysis.com/p/trainium3-inferencex) ⭐️ 8.0/10

SemiAnalysis published a deep dive into AWS Trainium3 inference performance and microarchitecture, reporting better performance TCO versus NVIDIA GB300 along with high MFU, high MBU, and low-latency results in its UBenchX benchmark. The analysis also presents a first-principles, physics-based architecture review. If the TCO claims hold, Trainium3 could shift the economics of cloud AI inference and intensify competition between AWS custom silicon and NVIDIA accelerators. This affects cloud customers choosing inference platforms as well as researchers studying AI accelerator architectures. The findings rely on SemiAnalysis's UBenchX benchmark and a first-principles architecture analysis, so the performance TCO conclusions depend on workload characteristics, software stack maturity, and deployment availability. Readers should treat the comparison as workload-specific rather than a universal verdict.

rss · Semianalysis · Nov 27, 15:54

**Background**: AWS Trainium is Amazon's custom AI accelerator family; Trainium3 was announced at re:Invent 2025, and Trn3 UltraServers can scale to 144 devices with around 360+ PF8 of compute and more than 20 TB of HBM3e. NVIDIA GB300 NVL72 is a rack-scale liquid-cooled system integrating 72 Blackwell Ultra GPUs and 36 Grace CPUs. UBenchX is SemiAnalysis's continuous open-source AI accelerator system benchmark used for cross-platform comparison.

<details><summary>References</summary>
<ul>
<li><a href="https://www.linkedin.com/posts/faikconference_awsreinvent2025-trainium3-trn3ultraservers-activity-7453021991508398080-AM92">AWS Trainium 3 UltraServers for Large Scale AI Training and Inference</a></li>
<li><a href="https://www.nvidia.com/en-us/data-center/gb300-nvl72/">Designed for AI Reasoning Performance & Efficiency - NVIDIA</a></li>
<li><a href="https://inferencex.semianalysis.com/">AI Accelerator System Benchmark | AcceleratorX by SemiAnalysis</a></li>

</ul>
</details>

**Tags**: `#AWS Trainium3`, `#AI accelerators`, `#inference`, `#microarchitecture`, `#performance TCO`

---

<a id="item-6"></a>
## [CIA and Other US Intelligence Agencies Breached in AI-Assisted Artex Hack](https://www.forbes.com/sites/the-wiretap/2026/11/25/us-government-under-ai-cyberattack) ⭐️ 8.0/10

According to a New York Times report cited by Forbes, hackers breached several US intelligence agencies — including the CIA, the National Geospatial-Intelligence Agency (NGA), and the Office of the Director of National Intelligence (ODNI) — with the help of an open-source AI tool called Artex. The intrusion appears relatively limited in severity, affecting only non-classified reconnaissance data rather than classified systems. This is one of the first publicly reported cases in which an agentic offensive AI framework was used against US intelligence targets, showing that autonomous AI attack tooling has moved from theoretical demos into real operations against high-value government networks. Because such frameworks are freely downloadable and can be paired with low-cost models, they lower the skill and resource barrier for espionage, fundamentally changing the economics of cyberattacks. Artex is an open-source framework that orchestrates multiple open-source AI models to probe network and computer defenses, effectively automating reconnaissance and penetration-testing workflows. A Chinese developer released it earlier this year and later deleted it from his GitHub account after it was linked to multiple attacks, including one against the European Union; the FBI had already warned earlier this year that cybercriminals and spies were widely adopting Artex.

telegram · zaihuapd · Nov 27, 10:42

**Background**: Artex belongs to a category researchers call agentic offensive frameworks (AOFs): instead of a human manually driving scanning and exploitation tools, a large language model plans the steps and invokes off-the-shelf security utilities on its own. The project presents itself as an "autonomous pentesting console" for authorized security testing, but the same capabilities work against any target once the tool is misused. The affected agencies — the CIA, NGA (which produces geospatial intelligence from satellite imagery) and ODNI (which coordinates the 18-agency intelligence community) — are core parts of the US intelligence apparatus, which is why even a limited, non-classified compromise draws attention.

<details><summary>References</summary>
<ul>
<li><a href="https://www.microsoft.com/en-us/security/blog/2026/11/25/what-defenders-need-to-know-artex-agentic-ai-framework-threat-actors-abuse/">What defenders need to know about ARTEX, the agentic AI ...</a></li>
<li><a href="https://cloudsecurityalliance.org/artifacts/aof">The Third Wave: ARTEX and Agentic Offensive Frameworks | CSA</a></li>
<li><a href="https://www.wiz.io/blog/agentic-attacks-artex-offensive-ai-frameworks">Agentic Attacks in the Wild: ARTEX & Offensive AI Frameworks ...</a></li>

</ul>
</details>

**Tags**: `#AI security`, `#cybersecurity`, `#nation-state hacking`, `#offensive AI`, `#government intelligence`

---

<a id="item-7"></a>
## [Minecraft Java Edition hit by unpatched 'minecraft2shell' RCE via malicious fonts](https://t.me/zaihuapd/45413) ⭐️ 8.0/10

A vulnerability disclosed on November 22 under the name 'minecraft2shell' shows that a specially crafted TrueType font inside a server resource pack can trigger a native out-of-bounds write in FreeType 2.14.3 and earlier, leading to arbitrary code execution on Windows clients of Minecraft Java Edition. All versions from 1.20.5 through 1.21.10, plus snapshots 26.1 to 26.4, are affected, while 1.20.4 and earlier and Bedrock Edition are not. This is a high-severity, currently unpatched remote code execution flaw in one of the most widely installed game clients in the world, and exploitation requires nothing more than joining an untrusted multiplayer server. Because resource packs are downloaded and applied automatically, players may be compromised without any obvious warning, putting pressure on server operators and Mojang alike. Mojang still ships LWJGL's FreeType bindings at version 3.4.3, which bundles the vulnerable native FreeType code, and no official fix is available yet. The exploit chain specifically targets Windows clients, and the affected version range is unusually broad because the vulnerable font-loading path has been present since 1.20.5.

telegram · zaihuapd · Nov 27, 18:04

**Background**: Minecraft servers can push a resource pack to any client that connects, and resource packs may include custom fonts in the TrueType format. To render those fonts, Minecraft uses the FreeType library through LWJGL's Java bindings; FreeType parses the font file's binary structures natively, outside the Java sandbox. An out-of-bounds write during that parsing lets an attacker corrupt memory in the game process and hijack execution, similar in spirit to how Log4Shell turned a logging library flaw into remote code execution in Minecraft in 2021.

<details><summary>References</summary>
<ul>
<li><a href="https://www.lwjgl.org/browse/release/3.4.3/bin/lwjgl-freetype">/release/3.4.3/bin/lwjgl-freetype - LWJGL</a></li>
<li><a href="https://mvnrepository.com/artifact/org.lwjgl/lwjgl-freetype/3.4.3">LWJGL FreeType Bindings » 3.4.3 - Maven Repository: org.lwjgl</a></li>

</ul>
</details>

**Tags**: `#security`, `#vulnerability`, `#remote-code-execution`, `#minecraft`, `#freetype`

---

<a id="item-8"></a>
## [Australian Federal Court Orders Apple to Open iPhone to Third-Party App Stores by 2027](https://t.me/zaihuapd/45419) ⭐️ 8.0/10

The Australian Federal Court has ruled that Apple must, from March 1, 2027, allow Australian iPhone users to install apps through third-party app stores and directly from websites, and must also permit alternative payment methods and external payment links inside apps. Fortnite will return to the Australian App Store immediately, and Apple has said it will appeal the decision and seek a stay of enforcement. This makes Australia the second major jurisdiction, after the European Union under the Digital Markets Act, to force Apple to dismantle its tightly controlled iOS app distribution and in-app payment monopoly. The ruling could set a precedent that encourages regulators and courts in other countries to impose similar requirements, directly affecting Apple's lucrative services revenue and giving developers new distribution and monetization options. The court found that Apple holds substantial market power in iOS app distribution and payments and that its restrictions substantially lessened competition in violation of Australian competition law, with the ruling stemming from Epic Games' antitrust lawsuit. Notably, the obligations do not take effect until March 1, 2027, and Apple's planned appeal and stay request could delay or alter the outcome.

telegram · zaihuapd · Nov 28, 07:00

**Background**: Apple has long required that all iOS apps be distributed through its own App Store and that digital goods be purchased via its in-app payment system, from which it takes a commission of up to 30%. The European Union's Digital Markets Act forced Apple to permit alternative app marketplaces and payment options in the EU starting in 2024, which led to the launch of stores such as AltStore PAL. Epic Games has been litigating against Apple's App Store practices in multiple countries since its 2020 dispute over Fortnite's removal from the store.

<details><summary>References</summary>
<ul>
<li><a href="https://www.theverge.com/24100464/altstore-pal-dma-eu-launch-delta-nintendo-emulator-clip-clipboard-manager">Third - party iPhone app store AltStore PAL is now live in... | The Verge</a></li>
<li><a href="https://developer.apple.com/support/payment-options-on-the-app-store-in-the-eu/">Payment options on the App Store in the EU... - Apple Developer</a></li>
<li><a href="https://en.wikipedia.org/wiki/App_Store_(Apple)">App Store (Apple) - Wikipedia</a></li>

</ul>
</details>

**Tags**: `#Apple`, `#antitrust`, `#app stores`, `#regulation`, `#Epic Games`

---