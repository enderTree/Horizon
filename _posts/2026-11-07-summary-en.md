---
layout: default
title: "Horizon Summary: 2026-11-07 (EN)"
date: 2026-11-07
lang: en
---

> From 37 items, 4 important content pieces were selected

---

1. [libghostty 1.0 released with a stable C ABI for embeddable terminal emulation](#item-1) ⭐️ 8.0/10
2. [PwnEscape Part 2: A Practical Firecracker microVM Escape Walkthrough](#item-2) ⭐️ 8.0/10
3. [Sodium-ion batteries near cost parity with LFP as 70 GWh contracted](#item-3) ⭐️ 8.0/10
4. [Taobao's MNN Team Open-Sources a 0.3B On-Device Model for Phones](#item-4) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [libghostty 1.0 released with a stable C ABI for embeddable terminal emulation](https://mitchellh.com/writing/libghostty-1-0) ⭐️ 8.0/10

Mitchell Hashimoto announced the 1.0 release of libghostty-vt, a portable, high-performance C library for terminal emulation extracted directly from the core of the Ghostty terminal. The 1.0 milestone means both the library itself and its C ABI are now stable, roughly a year after the project was first described as a coming Zig module with no C API at all. Because terminal emulation logic is now a reusable, stable-ABI library rather than something each application reinvents, a whole wave of new terminals and "agentic" coding tools such as herdr and cmux have been built on it instead of writing yet another emulator. That reduces ecosystem fragmentation: a bug fixed for one embedder, or a feature added once, benefits every downstream terminal and IDE. libghostty-vt is MIT licensed and written in C and Zig with zero external dependencies, making it embeddable across platforms and UI toolkits. It handles advanced terminal capabilities that embedders previously had to implement themselves, including the Kitty graphics protocol for inline images, OSC-8 hyperlinks, and fast viewport scrolling.

hackernews · mfiguiere · Nov 6, 23:30 · [Discussion](https://news.ycombinator.com/item?id=50399933)

**Background**: A terminal emulator is the program that interprets the escape sequences a shell or TUI application emits and renders them as text, colors, and cursor movement; Ghostty is a fast, cross-platform terminal that uses platform-native UI and GPU acceleration. libghostty is the extraction of that emulation engine into a standalone library, so an app can embed a terminal surface without building a whole emulator. The closest existing precedent is libvte, which provides a terminal widget for GTK+ and underpins GNOME Terminal, XFCE Terminal, sakura and others, but it is tightly bound to GTK and therefore much narrower in scope.

<details><summary>References</summary>
<ul>
<li><a href="https://mitchellh.com/writing/libghostty-1-0">Libghostty 1.0 – Mitchell Hashimoto</a></li>
<li><a href="https://lib.ghostty.org/vt/">libghostty-vt: libghostty-vt</a></li>
<li><a href="https://wiki.gnome.org/Apps/Terminal/VTE">Apps/Terminal/VTE – GNOME Wiki Archive</a></li>

</ul>
</details>

**Discussion**: Hacker News reaction was enthusiastic, with developers reporting real experience embedding libghostty in an Android project and saying it "just works" and saves them tremendous amounts of work. Commenters praised its handling of fancy TUIs, inline images via the Kitty graphics protocol and OSC-8 hyperlinks, and one user noted that Hashimoto resisted plugging his own competing project Rex in the announcement. A recurring thread compared libghostty-vt with libvte, acknowledging the shared spirit while pointing out that libvte's GTK dependency limits its reach.

**Tags**: `#terminals`, `#libghostty`, `#open-source`, `#systems-programming`, `#developer-tools`

---

<a id="item-2"></a>
## [PwnEscape Part 2: A Practical Firecracker microVM Escape Walkthrough](https://pwn.ai/blog/firecracker-escape) ⭐️ 8.0/10

The second part of the PwnEscape write-up, published on pwn.ai, walks through a practical, end-to-end escape from a Firecracker microVM, showing how the previously disclosed PwnEscape vulnerability can be turned into a working exploit chain in practice. Rather than announcing a new bug, it documents the concrete steps an attacker who has already compromised the guest VM would follow to break out to the host. Firecracker is the isolation layer underneath AWS Lambda and FaaS platforms and is widely used by container and sandbox providers, so a working escape path is directly relevant to anyone whose threat model assumes microVM hardware isolation is a strong boundary. The write-up gives defenders and platform operators a concrete case study for evaluating how much of their security depends on the jailer rather than the hypervisor itself. The most important caveat is that the demonstrated configuration ran Firecracker without the jailer, meaning no seccomp filter, namespaces, cgroups, or privilege dropping were in place — the write-up itself states that a deployment using those production controls needs a separate assessment of what privileges and resources remain reachable after a VMM compromise. It is also an exploitation walkthrough of an already-disclosed issue rather than a new CVE.

hackernews · SerCe · Nov 6, 19:33 · [Discussion](https://news.ycombinator.com/item?id=50397219)

**Background**: Firecracker is an open-source virtualization technology from AWS that runs workloads in lightweight virtual machines called microVMs, using KVM in user space with a minimal device model to combine hardware-virtualization isolation with container-like startup speed and memory overhead. Because the VMM itself is still a userspace process, Firecracker ships a companion 'jailer' that chroots the process, places it in namespaces and cgroups, drops privileges, and applies a seccomp filter before exec'ing the Firecracker binary. A VM escape means an attacker who controls code inside the guest kernel or a compromised workload manages to execute code in that VMM process on the host.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/firecracker-microvm/firecracker">GitHub - firecracker-microvm/firecracker: Secure and fast ...</a></li>
<li><a href="https://www.pandastack.ai/blog/firecracker-jailer-explained/">The Firecracker Jailer Explained · PandaStack</a></li>
<li><a href="https://hypervisor.org/">NOVA Microhypervisor</a></li>

</ul>
</details>

**Discussion**: Commenters focused on the jailer caveat, with one wishing the article had expanded on how a properly jailed Firecracker instance changes the picture, while another argued the incident strengthens the case for microhypervisor designs like the formally verified NOVA microkernel running under complex guest kernels. Others offered a live ClickBench playground hosting hundreds of database engines as a place to reproduce the escape, and several noted this is a write-up of an already-disclosed issue rather than a new vulnerability — including one pointing out the submission is a duplicate of an earlier HN thread.

**Tags**: `#security`, `#virtualization`, `#firecracker`, `#exploitation`, `#microvm`

---

<a id="item-3"></a>
## [Sodium-ion batteries near cost parity with LFP as 70 GWh contracted](https://www.pv-magazine.com/2026/11/06/sodium-ion-batteries-approach-cost-parity-with-lfp-with-70-gwh-covered-by-supply-agreements/) ⭐️ 8.0/10

Sodium-ion batteries are approaching cost parity with LFP lithium iron phosphate chemistry, with roughly 70 GWh of supply already covered by agreements, according to pv magazine. The milestone comes as CATL is still ramping production of its Naxtra sodium-ion cells, making it an early validation of sodium-ion cost-curve projections. If sodium-ion can match LFP on cost, it offers grid and stationary storage a lithium-free alternative that can absorb demand without competing for scarce lithium, potentially easing pressure on lithium prices and diversifying battery supply chains. The 70 GWh of agreements shows buyers are beginning to treat sodium-ion as bankable rather than experimental. The headline is cost parity, not a cost advantage: sodium-ion still generally trails LFP on energy density, so near-term deployments are expected to concentrate in stationary storage where size and weight matter less. Sodium-ion's ability to operate at lower temperatures and its comparatively safer chemistry are cited as additional advantages, while the volume covered by supply agreements remains modest relative to the overall grid-storage pipeline.

hackernews · doener · Nov 6, 23:00 · [Discussion](https://news.ycombinator.com/item?id=50399657)

**Background**: Sodium-ion batteries use sodium ions as charge carriers instead of lithium, and sodium is far more abundant and geographically widespread than lithium. Many sodium-ion designs avoid cobalt, copper, and nickel, and can use iron-based cathode materials, which is why the chemistry has long been promoted as a lower-cost alternative. LFP, or lithium iron phosphate, is a mature lithium-ion chemistry widely used in grid storage and lower-cost electric vehicles, and it is the cost benchmark sodium-ion must beat or match. The larger sodium ion leads to slower intercalation kinetics and generally lower energy density than lithium-ion, so early commercialization has focused on stationary storage and small vehicles.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Sodium-ion_battery">Sodium-ion battery</a></li>
<li><a href="https://www.batterydesign.net/chemistry/sodium-ion-battery/">Sodium-Ion Battery - Battery Design</a></li>
<li><a href="https://bslbatt.com/blogs/lfp-vs-nmc-lithium-battery-comparison/">LFP Vs NMC Battery : A Technical Comparison Of Cycle... - BSLBATT</a></li>

</ul>
</details>

**Discussion**: Commenters on Hacker News were split: some were eager for sodium-based home batteries because of safety and low-temperature operation, while others were disappointed that the milestone is only cost parity rather than a clear price advantage over LFP. A prominent view held that CATL's Naxtra ramp is still early and that each GWh of sodium capacity displaces lithium demand, which could pressure prices for higher-value battery chemistries.

**Tags**: `#batteries`, `#energy-storage`, `#sodium-ion`, `#hardware`, `#cleantech`

---

<a id="item-4"></a>
## [Taobao's MNN Team Open-Sources a 0.3B On-Device Model for Phones](https://www.ithome.com/1/023/212.htm) ⭐️ 8.0/10

On November 6, Taobao's MNN team open-sourced MNN-Pocket-0.3B, a roughly 300-million-parameter on-device model that runs fully offline on an iPhone 18 Pro at an average decoding speed of about 350 tokens/s, with an INT4 deployment file of only 173 MB. The team released multiple versions covering the pre-training, post-training, and on-device deployment stages. A 0.3B model that fits in a 173 MB INT4 file and decodes at several hundred tokens per second makes fully offline LLM features practical on ordinary phones, without network latency, server costs, or user data leaving the device. Coming from a major e-commerce company's inference team, it is also a concrete reference point for how small on-device models are being shrunk and tuned for mass-market apps. To hit its goals of under 300 MB peak memory and more than 200 tokens/s decoding, the team used a 28-layer architecture and shrank the vocabulary from 151K to 64K tokens, both of which directly reduce embedding size and per-step computation. The reported ~350 tokens/s figure comes from an iPhone 18 Pro, so performance on mid-range Android hardware will likely be lower.

telegram · zaihuapd · Nov 6, 15:13

**Background**: MNN (Mobile Neural Network) is Alibaba's open-source lightweight deep learning inference engine, designed for running models on phones and IoT devices; it has been used in Taobao, Youku, Fliggy, and dozens of other apps for tasks like search, image retrieval, and risk control. On-device LLMs are typically built by taking a small model and applying INT4 quantization, which stores weights as 4-bit numbers and shrinks the model file by roughly 7x versus FP32. The tokens/s metric measures how many text tokens the model generates per second during decoding, and on phones anything above roughly 20–30 tokens/s starts to feel close to reading speed.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/alibaba/MNN">GitHub - alibaba/MNN: MNN: A blazing-fast, lightweight ...</a></li>
<li><a href="https://developer.volcengine.com/articles/7382995327139184691">淘宝开源深度学习端侧推理引擎 MNN - 文章 - 开发者社区 - 火山引擎</a></li>
<li><a href="https://www.tinyash.com/blog/ai-memory-crisis-rammageddon-6-tips/">AI 内存危机来了：开发者如何应对 RAMmageddon...</a></li>

</ul>
</details>

**Tags**: `#on-device AI`, `#LLM`, `#MNN`, `#model compression`, `#edge computing`

---