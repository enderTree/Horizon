---
layout: default
title: "Horizon Summary: 2026-11-03 (EN)"
date: 2026-11-03
lang: en
---

> From 46 items, 6 important content pieces were selected

---

1. [Astra edits Qwen3.5-0.8B weights directly, lifting MATH-500 from 7.9% to 48.1%](#item-1) ⭐️ 8.0/10
2. [Subvocal unveils RF-sensing smart glasses that decode silent speech into text](#item-2) ⭐️ 8.0/10
3. [Ubuntu LTS kernels still unpatched for critical 0day RCE three weeks after disclosure](#item-3) ⭐️ 8.0/10
4. [Faint aircraft noise in videos can reveal exact recording location via ADS-B](#item-4) ⭐️ 8.0/10
5. [Raspberry Pi 5 Launches With 2.4GHz Cortex-A76 and Dual 4K60 HDMI](#item-5) ⭐️ 8.0/10
6. [Linux kernel IPv4 TCP use-after-free (CVE-2026-98432) allows remote RCE, patch now](#item-6) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Astra edits Qwen3.5-0.8B weights directly, lifting MATH-500 from 7.9% to 48.1%](https://rikiyat.github.io/blog/weight-space-programming/) ⭐️ 8.0/10

A new blog post describes Astra, an LLM-based system that can inspect and directly rewrite the weights of a small Qwen model (Qwen3.5-0.8B) without any external tooling or gradient-based training, reportedly raising its MATH-500 score from 7.9% to 48.1% in author-run tests. The post also claims Astra can identify which simple games small networks were trained on purely by reading their weights. If the result holds up, it points to a form of "weight-space programming" in which a model can repair or upgrade another model's capabilities in a single shot, potentially replacing costly data curation and full fine-tuning loops. That prospect touches model interpretability, safety oversight and the debate over whether LLMs are approaching recursive self-improvement. The numbers come from author-run experiments on a single 0.8B-parameter model and one math benchmark, and independent researchers have not yet verified them; the blog itself notes that some attempted edits failed. Notably, Astra is claimed to do this natively rather than through a conventional weight-editing optimizer or LoRA-style adapter, which is the part most experts are questioning.

hackernews · dbreunig · Nov 2, 18:21 · [Discussion](https://news.ycombinator.com/item?id=50341174)

**Background**: Large language models normally work only on token sequences: their weights are fixed after training, and improving a model usually means collecting more data and running further training or adding low-rank adapters such as LoRA. "Weight-space learning" is a smaller research line that treats a network's parameters themselves as data that can be read, generated or edited, and prior work has shown that weights can be modified for larger models. Qwen is Alibaba's open-weight model family, and its small variants are popular because they can be run and experimented on cheaply.

<details><summary>References</summary>
<ul>
<li><a href="https://explainx.ai/blog/weight-space-programming-gpt-6-astra-edits-qwen3-5-0-8b-weights-math-7-9-to-48-1-mit-csail-2026">GPT-6 Astra Edits Qwen Weights: MATH-500 7.9% to 48.1% ...</a></li>
<li><a href="https://kingy.ai/blog/weight-space-programming-ai-agent-model-weights/">Weight-Space Programming: GPT-6 Astra Edits Qwen</a></li>
<li><a href="https://rikiyat.github.io/blog/weight-space-programming/">Sparks of Weight - Space Programming: LLMs can natively read & write...</a></li>

</ul>
</details>

**Discussion**: Reaction is sharply split: one commenter called the result "insane" and paradigm-shifting, arguing it shows LLMs have a native understanding of their own weights comparable to or better than human intuition about neurons. A researcher working in weight-space learning pushed back, saying the blog and its promotion overstate the results and that editing and generating weights has been possible for a while, while another commenter speculated Astra was deliberately trained on weight data as an attempt at recursive self-improvement rather than showing an emergent ability.

**Tags**: `#weight-space-learning`, `#LLM`, `#model-editing`, `#research`, `#Qwen`

---

<a id="item-2"></a>
## [Subvocal unveils RF-sensing smart glasses that decode silent speech into text](https://news.ycombinator.com/item?id=50340088) ⭐️ 8.0/10

The Subvocal Company, a YC F26 startup founded by Aarush and Arnav — former Georgia Tech CS students — showed off smart glasses whose frames embed antennas that emit low-power radio waves (similar to Bluetooth) through the wearer's face, decoding silently mouthed words into text at speech speed. The team began with an EMG-electrode hack at Stanford's TreeHacks in February, abandoned muscle sensing as impractical, and switched to RF after finding that the signal is modulated by the tongue, lips and soft palate — and that it works even with the lips fully closed, on what they call "internal speech". A silent speech interface would remove the biggest social barrier to voice-driven AI dictation tools like Wispr Flow, letting people type by voice in libraries, open offices and public spaces without being overheard. If the hardware works reliably outside a lab, it also has obvious accessibility value for users with speech or motor impairments and marks one of the first consumer attempts at a non-acoustic, always-available input channel for computers. The product is at pre-order stage with no published accuracy or word-error-rate figures, and the team says the hardest remaining problem is cross-user generalization, since each person's facial anatomy produces very different RF signal patterns and the only lever they found was to scale up data collection. The custom low-noise RF sensing stack and antenna placement (fields must overlap the articulators) were the core engineering challenges, and the founders admit the current "internal speech" mode feels odd to perform even though they have practiced it.

hackernews · aarushyadav · Nov 2, 17:16

**Background**: Silent speech recognition (SSR) is a long-studied alternative to acoustic speech recognition: instead of listening to sound, the system reads the physiological activity of speech production — muscle signals, or in this case, how radio waves are perturbed as they pass through the tongue, lips and soft palate. The best-known precedent is MIT Media Lab's AlterEgo, which the founders cite as inspiration and which used surface EMG electrodes on the face and neck. Subvocalization, the internal "sound" of words when reading or thinking, is a related but distinct phenomenon — Subvocal's system does not read involuntary inner monologue, but rather deliberate, lip-closed mouthing.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Subvocal_recognition">Subvocal recognition - Wikipedia</a></li>
<li><a href="https://pubmed.ncbi.nlm.nih.gov/29855428/">Development of sEMG sensors and algorithms for silent speech ...</a></li>
<li><a href="https://chaof94.github.io/Papers/EarSSR.pdf">EarSSR: Silent Speech Recognition via Earphones</a></li>

</ul>
</details>

**Discussion**: Commenters were enthusiastic — one called it "straight out of a sci-fi novel" and praised the accessibility angle — but pressed hard on practicality: several asked whether whispering quietly would be more natural than mouthing with no sound at all, and whether the signal processing runs on the glasses or through a phone app. Others gave concrete hardware feedback, requesting adjustable metal nose-pad arms for non-standard nose bridges and a clip-on version that attaches to existing prescription glasses, while one raised privacy alarms about always-on sensing and asked whether inference happens on-device and works offline.

**Tags**: `#silent-speech-recognition`, `#smart-glasses`, `#RF-sensing`, `#human-computer-interaction`, `#accessibility`

---

<a id="item-3"></a>
## [Ubuntu LTS kernels still unpatched for critical 0day RCE three weeks after disclosure](https://freenode.net/article/ubuntu-lts-kernels-still-unfixed-for-critical-cve-2026-98432) ⭐️ 8.0/10

Ubuntu LTS kernels remain unfixed for CVE-2026-98432, a critical remote code execution vulnerability in the Linux kernel, nearly three weeks after public disclosure, and Ubuntu has published no mitigation guidance or revised patched kernel packages. The issue drew a high-engagement Hacker News thread (over 800 points and 400+ comments) in which users traded workarounds and questioned the delay. Ubuntu LTS is one of the most widely deployed server and cloud operating systems, so an unpatched remotely exploitable kernel flaw leaves a large population of production hosts exposed for an extended window. The absence of vendor mitigation advice also pushes administrators to improvise their own filtering rules, which can break legitimate traffic if applied incorrectly. Commenters noted that Ubuntu's security tracker rates the flaw "High" rather than "Critical," a designation that would normally trigger an out-of-schedule kernel update, and that Ubuntu has offered no mitigation instructions while Red Hat published one that it says "reduces exposure to this vulnerability but cannot fully prevent it." A community-proposed stopgap uses an iptables/nftables u32 match in the raw PREROUTING table to drop matching TCP packets at the network edge, though this is an unofficial workaround rather than a fix.

hackernews · majorchord · Nov 2, 18:39 · [Discussion](https://news.ycombinator.com/item?id=50341462)

**Background**: A zero-day (0day) is a vulnerability that is publicly known — and potentially already being exploited — before an official fix exists, which is why the window between disclosure and patching is the most dangerous period for defenders. Remote code execution (RCE) is a class of flaw that lets an attacker run arbitrary code on a machine over a network without physical access or user interaction, making it among the most severe vulnerability types. CVE-2026-98432 is the standardized Common Vulnerabilities and Exposures identifier assigned to this specific kernel bug, allowing vendors, scanners and advisories to refer to the same issue. Ubuntu LTS (Long Term Support) releases ship a kernel that receives security maintenance for years, so a gap in that maintenance directly affects long-lived servers and cloud instances.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Zero-day_vulnerability">Zero-day vulnerability - Wikipedia</a></li>
<li><a href="https://www.crowdstrike.com/en-us/cybersecurity-101/cyberattacks/remote-code-execution/">What is Remote Code Execution (RCE)? | CrowdStrike</a></li>
<li><a href="https://en.wikipedia.org/wiki/Common_Vulnerabilities_and_Exposures">Common Vulnerabilities and Exposures - Wikipedia</a></li>

</ul>
</details>

**Discussion**: Sentiment was largely critical of Ubuntu: one commenter flagged that a simple u32 drop rule in raw PREROUTING could block the attack traffic before the kernel is exploitable and complained nobody was publicizing it, while others pressed for an official explanation of the delay and contrasted Ubuntu's silence with Red Hat's advisory. Several commenters questioned why the flaw was rated High rather than Critical, and one widened the concern to consumer routers and wireless access points that run Linux kernels and never receive security updates, especially as LLM-assisted attackers lower the bar for exploitation.

**Tags**: `#linux-kernel`, `#security-vulnerability`, `#ubuntu`, `#cve`, `#rce`

---

<a id="item-4"></a>
## [Faint aircraft noise in videos can reveal exact recording location via ADS-B](https://simonwillison.net/2026/Nov/3/a-sound-that-leaks-your-exact-location/) ⭐️ 8.0/10

Security researcher Colsto published a YouTube demonstration showing that almost imperceptible aircraft background noise in a video's soundtrack can be isolated, converted into Doppler curves, and then cross-referenced against public ADS-B flight data to pinpoint exactly where the video was recorded. The technique uses each passing aircraft's speed, distance and the time gaps between successive flights to constrain the location, and Simon Willison highlighted it as a "genius piece of OSINT." This exposes ambient sound as a geolocation side channel that almost nobody scrubs before publishing, so it can defeat visual anonymization even when a video shows no recognizable landmarks, street signs or skyline. Because the flight data is free and public, the technique lowers the barrier for investigators, journalists and malicious actors alike, and anyone filming from a home or sensitive site should assume aircraft noise is potentially identifying. The method hinges on the precise Doppler frequency shift produced as an aircraft approaches and recedes overhead, with matching based on airspeed, slant distance and the timing gaps between consecutive flights rather than on any single sound. Its accuracy therefore depends on dense ADS-B receiver coverage over the recording site and on the audio containing enough faint aircraft noise, and independent re-implementations such as the doppler-locate project and a Hermes agent plugin already exist.

rss · Simon Willison · Nov 3, 05:32

**Background**: ADS-B (Automatic Dependent Surveillance–Broadcast) is an aviation surveillance technology in which aircraft determine their own position via satellite navigation and periodically broadcast it along with altitude, speed and identity; crowdsourced receiver networks such as Flightradar24 and FlightAware republish these tracks publicly, largely in real time. The Doppler effect is the shift in perceived frequency when a sound source moves relative to a listener — the familiar drop in pitch as a plane passes overhead — and the shape of that curve encodes how close and how fast the aircraft was. A spectrogram makes these faint shifts visible as drifting lines in the audio, which is what allows software to recover the geometry of each flyover.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Automatic_Dependent_Surveillance–Broadcast">Automatic Dependent Surveillance–Broadcast - Wikipedia</a></li>
<li><a href="https://www.flightradar24.com/how-it-works/ads-b">Automatic Dependent Surveillance - Broadcast | Flightradar24</a></li>
<li><a href="https://github.com/digitalis-p/doppler-locate/tree/main">GitHub - digitalis-p/doppler-locate: Geolocate audio ...</a></li>

</ul>
</details>

**Tags**: `#privacy`, `#OSINT`, `#geolocation`, `#signal-processing`, `#ADS-B`

---

<a id="item-5"></a>
## [Raspberry Pi 5 Launches With 2.4GHz Cortex-A76 and Dual 4K60 HDMI](https://t.me/zaihuapd/44854) ⭐️ 8.0/10

The Raspberry Pi 5 has been officially released, priced at $60 for the 4GB model and $80 for the 8GB model (plus local taxes), and it is the first flagship Pi to move to a 2.4GHz quad-core 64-bit Arm Cortex-A76 CPU paired with a VideoCore VII GPU supporting OpenGL ES 3.1 and Vulkan 1.2. The board also adds dual 4K60p HDMI outputs, a 4K60p HEVC decoder, dual-band 802.11ac Wi-Fi, Bluetooth 5.0/BLE, a high-speed microSD interface with SDR104 support, and two USB 3.0 ports capable of 5Gbps simultaneously. The Pi 5 is a generational leap for the most widely used single-board computer, replacing the aging Cortex-A72 platform with a modern out-of-order core and desktop-class graphics, which directly benefits embedded, edge-computing, and hobbyist projects that were previously CPU- and I/O-bound. The addition of dual 4K60 HDMI and USB 3.0 also pushes the board closer to usable general-purpose desktop territory at a price far below most Arm development boards. The GPU is the VideoCore VII inside Broadcom's 16nm BCM2712 SoC, clocked around 800MHz, which is a major step up from the VideoCore VI used in the Pi 4. The SDR104 microSD mode matters because it raises card interface throughput well above the older 50MB/s-class SDR50/DDR50 modes, though reaching those speeds depends on using a compatible UHS-I card and stable 1.8V signaling on the board.

telegram · zaihuapd · Nov 2, 12:00

**Background**: Raspberry Pi is a family of low-cost, credit-card-sized single-board computers that became the de facto standard for hobbyist electronics, education, and many industrial/embedded deployments; earlier models relied on 32-bit or older 64-bit cores such as the Cortex-A72. The Cortex-A76 is a 64-bit Armv8.2 out-of-order microarchitecture originally designed for smartphones and laptops, offering far higher per-clock performance and a much-improved branch predictor compared with the A72, which is why it represents the biggest CPU jump in Pi history. VideoCore is Broadcom's family of mobile GPUs integrated into the SoCs that power the Pi, so each Pi generation's graphics capability is tied to the VideoCore version in its Broadcom chip. SDR104 is the fastest UHS-I bus mode for SD cards, roughly doubling the interface clock rate and read throughput compared with earlier modes.

<details><summary>References</summary>
<ul>
<li><a href="https://www.androidauthority.com/cortex-a76-deep-dive-870896/">Arm Cortex - A 76 CPU microarchitecture deep dive</a></li>
<li><a href="https://community.st.com/stm32-mpus-products-and-hardware-related-39/how-to-enable-sdr104-mode-with-full-speed-on-stm32mp15x-platform-34607">How to enable SDR104 mode with full speed on STM32MP15x ...</a></li>

</ul>
</details>

**Tags**: `#Raspberry Pi`, `#hardware`, `#embedded systems`, `#single-board computer`, `#Arm Cortex-A76`

---

<a id="item-6"></a>
## [Linux kernel IPv4 TCP use-after-free (CVE-2026-98432) allows remote RCE, patch now](https://t.me/zaihuapd/44866) ⭐️ 8.0/10

A security reminder circulating on Telegram warns that the Linux kernel's IPv4 TCP stack contains a high-severity use-after-free vulnerability, tracked as CVE-2026-98432, that can be triggered from the network without authentication or user interaction. A public remote-code-execution (RCE) proof-of-concept targeting MPTCP listen ports has already been published, and the Go security team has issued an advisory stating that Go 1.24+ programs enable MPTCP on listen sockets by default on Linux. Any unpatched Linux server reachable from the internet is potentially at risk, which covers the vast majority of cloud, container and edge infrastructure. The exposure is wider than it first appears because Go 1.24+ services inherit the vulnerable precondition by default, meaning teams that never deliberately adopted MPTCP may still need to patch or reconfigure. The vulnerability is not confined to MPTCP deployments — the Go advisory notes that systems with no MPTCP listeners may still be susceptible to similar attacks, and MPTCP is only enabled for listen sockets while outgoing connections remain plain TCP. The practical mitigation is updating the kernel (or otherwise disabling the default MPTCP listen behaviour) rather than relying on the absence of MPTCP configuration.

telegram · zaihuapd · Nov 3, 02:37

**Background**: A use-after-free bug means a program keeps using a chunk of memory after it has been freed, so an attacker who can shape that memory can often redirect execution and run their own code. Multipath TCP (MPTCP) is an IETF extension to standard TCP, specified in RFC 8684, that lets a single connection span multiple network paths for better throughput and redundancy; on Linux an application normally has to opt in explicitly. Since Go 1.24, however, the Go net package requests MPTCP automatically for listen sockets on Linux, so many Go-based network services became MPTCP-capable without their authors doing anything — which is how a kernel networking bug turns into a default exposure for a large part of the cloud-native ecosystem.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Multipath_TCP">Multipath TCP - Wikipedia</a></li>
<li><a href="https://docs.kernel.org/networking/mptcp.html">Multipath TCP (MPTCP) — The Linux Kernel documentation</a></li>
<li><a href="https://groups.google.com/g/golang-announce/c/PCoQcdxoScw">[security] Protecting against CVE-2026-98432 - Google Groups</a></li>

</ul>
</details>

**Tags**: `#security`, `#linux-kernel`, `#vulnerability`, `#networking`, `#go`

---