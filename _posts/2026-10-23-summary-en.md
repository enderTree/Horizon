---
layout: default
title: "Horizon Summary: 2026-10-23 (EN)"
date: 2026-10-23
lang: en
---

> From 44 items, 12 important content pieces were selected

---

1. [Anthropic argues LLM agents make formal verification practical at scale](#item-1) ⭐️ 8.0/10
2. [Quad9 to Exit France After Court Holds DNS Resolver Liable for Piracy](#item-2) ⭐️ 8.0/10
3. [iOS 16.5 XNU kernel booted on Android phones and QEMU](#item-3) ⭐️ 8.0/10
4. [eMudhra Exits Global SSL/TLS CA Business After Weak Private Key Incident](#item-4) ⭐️ 8.0/10
5. [Triangulating 3.7M map polygons in 489 ms, faster than Earcut](#item-5) ⭐️ 8.0/10
6. [Switch 2 Jailbroken: ns2jb Software Exploit Built With an LLM-Driven KVM Rig](#item-6) ⭐️ 8.0/10
7. [Carbon-X: an open 14.8B model trained jointly on DNA and text](#item-7) ⭐️ 8.0/10
8. [Tesla begins North American production of steering-wheel-less Cybercab robotaxi](#item-8) ⭐️ 8.0/10
9. [Oracle Issues Critical Security Alert for High-Severity Java SE Flaw](#item-9) ⭐️ 8.0/10
10. [333 Backdoored Tor Exit Relays Taken Offline After Ebury Infection](#item-10) ⭐️ 8.0/10
11. [Export-banned Nvidia B300 chips surface in Chinese state-backed deployment](#item-11) ⭐️ 8.0/10
12. [SpaceX in Talks to Lease 80,000 Cell Sites for U.S. Wireless Carrier](#item-12) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Anthropic argues LLM agents make formal verification practical at scale](https://www.anthropic.com/research/formal-verification) ⭐️ 8.0/10

Anthropic published a research post arguing that LLM agents can make formal software verification practical at much larger scales than before, and described initial explorations applying the approach to tasks such as assessing the security of the zlib compression algorithm, proving behavioral equivalence for a Python interpreter written in Rust, and rooting out long-standing bugs in critical software. The post prompted a substantial Hacker News discussion with roughly 193 upvotes and over 100 comments. Formal verification has long been bottlenecked by the enormous human effort required to write proofs, so automating proof generation could bring mathematical correctness guarantees to ordinary production code and security-critical components rather than just small hand-verified kernels. If the approach scales, it would affect systems programmers, security engineers, and anyone relying on low-level software such as compression libraries and language runtimes. The post's own appendix acknowledges a key limitation: agent-written proofs are only as good as any proof of the same theorem, but it remains unclear whether agents can scale their verbose proof style to more complex programs, and experience from projects such as MachCSL suggests agents hit a complexity wall that requires restructuring the proofs. In other words, verification proves code matches a specification — it does not establish that the specification itself is correct.

hackernews · johnbender · Oct 22, 22:54 · [Discussion](https://news.ycombinator.com/item?id=50202217)

**Background**: Formal verification is the act of proving or disproving the correctness of a system against a formal specification using mathematical methods, rather than relying on testing and code review. It has historically been reserved for high-stakes domains like hardware design, compilers, and cryptographic primitives, because writing machine-checkable proofs in tools such as Lean or Coq is slow and demands specialized expertise. LLM agents that can write and iterate on such proofs shift the economics of the practice, which is what the Anthropic post is arguing about.

<details><summary>References</summary>
<ul>
<li><a href="https://www.anthropic.com/research/formal-verification">LLMs are making formal software verification feasible at a ...</a></li>
<li><a href="https://en.wikipedia.org/wiki/Formal_verification">Formal verification - Wikipedia</a></li>
<li><a href="https://lubis-eda.com/proof-complexity-in-formal-verification/">Proof complexity in formal verification: why proofs fail</a></li>

</ul>
</details>

**Discussion**: Reaction was mixed rather than uniformly enthusiastic: one commenter predicted LLMs will never formally verify LLM-written imperative code and argued the industry will instead migrate toward deterministic declarative languages, while another cited the paper's appendix warning about a complexity wall seen in earlier agent-based verification projects. On the practical side, a developer reported moderate success applying LLM-assisted verification to a Rust rewrite of Postgres — translating both Rust and C into Lean and having an LLM prove behavioral equivalence — covering about 12% of the code (roughly 70k lines of C) and surfacing subtle differences such as floating-point behavior. Another commenter offered the analogy that verification perfects the "inspection" step against the blueprint, but cannot check whether the blueprint matches the original intent.

**Tags**: `#formal-verification`, `#LLMs`, `#software-engineering`, `#AI-agents`, `#programming-languages`

---

<a id="item-2"></a>
## [Quad9 to Exit France After Court Holds DNS Resolver Liable for Piracy](https://quad9.net/news/blog/au-revoir-france/) ⭐️ 8.0/10

Quad9, the Swiss non-profit public DNS resolver, announced it is pulling out of France after French courts held it responsible for failing to block copyright-infringing domains, and fined it for contempt of court when plaintiff Sony Music Entertainment circumvented Quad9's geoIP blocks by using a VPN from Germany. Quad9 says it will likely apply geoIP filters to stop serving French users after November 24. This is a precedent-setting moment for internet infrastructure: it establishes that a public recursive resolver can be held liable and fined for the traffic it resolves, even when the rights holder itself defeated the geoblocking measure. It also shrinks privacy- and security-focused DNS options for French users and adds pressure on other resolvers, several of which have already been forced to implement French blocking orders or leave the market. Quad9 argues the ruling creates an impossible technical bind: geoIP blocking is too coarse to selectively deny resolution for specific domain names, yet the court treated geoIP filtering as noncompliance once a VPN defeated it. Quad9 is a malware/phishing-blocking resolver with DNSSEC validation on all addresses, operated by a Swiss public-benefit foundation under Swiss privacy law, so its exit removes a security-filtering option rather than a purely neutral one.

hackernews · farrokhi · Oct 22, 14:32 · [Discussion](https://news.ycombinator.com/item?id=50195959)

**Background**: A recursive DNS resolver is the service that translates human-readable domain names into IP addresses, effectively acting as a directory lookup for every connection a device makes. French courts have for years issued "web-blocking" injunctions against piracy sites at the request of rights holders such as Sony Music and Canal+, and because DNS is a convenient chokepoint, those orders have increasingly been aimed at public resolvers like Google, Cloudflare, Cisco's OpenDNS and Quad9. Cisco's OpenDNS previously exited France over a similar sports-piracy blocking order, while Google and Cloudflare unsuccessfully opposed the orders and now implement them.

<details><summary>References</summary>
<ul>
<li><a href="https://quad9.net/news/blog/au-revoir-france/">A public and free DNS service for a better security and privacy | Quad9</a></li>
<li><a href="https://en.wikipedia.org/wiki/Quad9">Quad9 - Wikipedia</a></li>
<li><a href="https://news.ycombinator.com/item?id=50195959">Quad9 ( DNS Resolver ) to Exit France | Hacker News</a></li>

</ul>
</details>

**Discussion**: The Hacker News thread (over 1,000 points and 376 comments) was largely sympathetic to Quad9, with Quad9 CTO John Todd joining to acknowledge the apparent contradiction between opposing geoblocking and using geoIP filters to cut off France, while arguing that energy is better spent elsewhere. Commenters were incredulous that a resolver could be fined after the plaintiff itself used a VPN to circumvent the block, drew analogies to punishing a phone book for listing a criminal's number, noted Cisco's earlier exit, and some argued resolvers forced into blocking should stop resolving the plaintiffs' own domains.

**Tags**: `#DNS`, `#internet-policy`, `#censorship`, `#copyright-law`, `#privacy`

---

<a id="item-3"></a>
## [iOS 16.5 XNU kernel booted on Android phones and QEMU](https://github.com/oosexgang/hackios-xnu-kernel) ⭐️ 8.0/10

A research project called hackios-xnu-kernel has published patches, an EFI loader, a UEFI port and QEMU scripts that let Apple's iOS 16.5 XNU kernel and firmware boot on Android hardware — including the POCO X5 Pro 5G and some Xiaomi devices — as well as in the QEMU emulator. Rather than a flashable ROM, it runs as a time-limited research bench: a session lasts a fixed number of seconds, after which the kernel hands its log back to the loader. Booting Apple's closed-source iOS kernel image on non-Apple hardware is a striking reverse-engineering and emulation milestone, and the project's QEMU path makes the work reproducible for other researchers. It also raises practical concerns, since convincing iOS-on-Android demos could be abused to fake used iPhones or counterfeit devices. The repository ships XNU kernel patches, the EFI loader, the UEFI port, Wi-Fi support and prebuilt kernel/loader/UEFI binaries, but the session is deliberately bounded in time and ends by dumping a log rather than offering a usable system. Booting only the kernel and firmware means there is no usable iOS userland, so this is a diagnostic bench rather than a phone you can operate.

hackernews · aghuang · Oct 22, 15:26 · [Discussion](https://news.ycombinator.com/item?id=50196718)

**Background**: XNU ("X is Not Unix") is the hybrid kernel Apple has developed since 1996 (originating at NeXT), combining a Mach-based core with BSD-derived components; it underpins macOS, iOS, iPadOS, watchOS and tvOS, and its source is released as part of the open-source Darwin project. QEMU is a general-purpose machine emulator and virtualizer that can run a full system image for a foreign architecture on a host machine. Getting XNU to boot therefore requires recreating the low-level boot chain — here a custom EFI loader and UEFI port — that iOS normally relies on Apple's own hardware and bootloader to provide.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/XNU_kernel">XNU kernel</a></li>
<li><a href="https://github.com/oosexgang/hackios-xnu-kernel">GitHub - oosexgang/hackios- xnu - kernel · GitHub</a></li>
<li><a href="https://en.wikipedia.org/wiki/Mach_(kernel)">Mach ( kernel ) - Wikipedia</a></li>

</ul>
</details>

**Discussion**: Hacker News commenters were impressed that it works across QEMU, the POCO X5 Pro and Xiaomi devices, though several read it as a research bench rather than a usable ROM, with one speculating that the time-limited design might exist so an AI assistant would agree to help with the project at all. Others raised fraud worries — used-iPhone buyers should double-check before purchasing — and drifted into wishful side topics such as running Android or LineageOS on an iPad and porting Garmin firmware to cheaper models.

**Tags**: `#reverse-engineering`, `#iOS`, `#Android`, `#kernel-emulation`, `#QEMU`

---

<a id="item-4"></a>
## [eMudhra Exits Global SSL/TLS CA Business After Weak Private Key Incident](https://emudhra.com/en/press-release/emudhra-to-exit-global-ssl-tls-certificate-business) ⭐️ 8.0/10

Indian certificate authority eMudhra announced it is exiting the global SSL/TLS certificate business following an incident in which eight of its intermediate CA private keys were found to have catastrophically weak randomness — reportedly only about 256 possible values, with one key literally being the number 4. eMudhra says it revoked the affected CAs within 14 hours of discovery and disclosed promptly, while Mozilla pushed a block to all Firefox users within roughly 3 hours of receiving the report on October 17 and Google blocked the affected public keys the same day. This is a rare case of a publicly trusted CA abandoning an entire business line because of a cryptographic failure, and it puts the browser root-store accountability process on full display: misissuance risk is now handled in hours, not weeks. Any organization relying on eMudhra-issued TLS or code-signing certificates — and anyone who depends on the WebPKI's assumption that a CA's key generation is sound — is affected. Of the eight compromised intermediate CAs, six could issue TLS server certificates and two could issue code-signing certificates; security researcher Scott Helme's analysis found one private key was simply the number 4. eMudhra's chairman V. Srinivasan argued the social-media scrutiny was "out of proportion to SSL/TLS's place in our business" and stressed that the global SSL/TLS infrastructure runs separately from its other operations, though critics note the company never explained how the flaw arose.

hackernews · bo0tzz · Oct 22, 13:33 · [Discussion](https://news.ycombinator.com/item?id=50195110)

**Background**: Publicly trusted CAs are the linchpins of HTTPS: browsers ship a root store of trusted roots, and any certificate chaining up to one of them is treated as valid for encrypting traffic and proving a site's identity. Intermediate CAs are delegated signing authorities that sit between a root and the end-entity certificates handed to websites, so anyone who can reconstruct an intermediate's private key can mint trusted HTTPS certificates for any domain. Because browsers — not governments or auditors — ultimately decide what is trusted, they can and do remove or distrust CAs through their root store programs, which are coordinated in the CA/Browser Forum.

<details><summary>References</summary>
<ul>
<li><a href="https://emudhra.com/en/press-release/emudhra-to-exit-global-ssl-tls-certificate-business">eMudhra to Exit global SSL / TLS Certificate Business</a></li>
<li><a href="https://unit42.paloaltonetworks.com/emudhra-certificate-compromise/">EMudhra Intermediate CA Certificates Compromised</a></li>
<li><a href="https://www.theregister.com/security/2026/10/20/indian-certification-authority-emudhras-private-keys-compromised-one-of-them-was-the-number-4/5304312">Indian certification authority eMudhra ’s private keys compromised...</a></li>

</ul>
</details>

**Discussion**: Commenters were scathing, mocking the weak key generation (one joked the key was a four-byte RSA private key) and arguing that eMudhra's refusal to explain the root cause makes the company look worse than the defect itself. Others highlighted the Chrome team's publicly filed, brutally detailed question list on Mozilla's Bugzilla (bug 2083449) and pushed back on eMudhra's claim that "no end entity certificates were issued" from the affected CAs, since in principle anyone could have issued them.

**Tags**: `#SSL/TLS`, `#PKI`, `#certificate authorities`, `#security incident`, `#browser trust`

---

<a id="item-5"></a>
## [Triangulating 3.7M map polygons in 489 ms, faster than Earcut](https://globus.software/blog/2026/10/16/cutting-map-polygons/) ⭐️ 8.0/10

A Globus Software blog post presents a triangulation implementation that processes a 3.7-million-polygon map corpus in 489 ms, claiming faster performance than Mapbox's Earcut on that dataset. Triangulation is a core step for rendering maps and geometry in the browser, so faster triangulation can reduce load times and make larger datasets practical. The discussion also highlights the real trade-offs among raw speed, bundle size, and mesh quality that geometry library authors must balance. The benchmark uses a published 3.7-million-polygon corpus, and the Earcut author notes that Earcut is about 4.1 KB min+gzip and deliberately rejects some optimizations to keep bundle size small. Commenters also point out that the fast output contains many long, thin triangles, which can be problematic for GPU rasterization.

hackernews · molind · Oct 22, 09:31 · [Discussion](https://news.ycombinator.com/item?id=50193170)

**Background**: Polygon triangulation breaks a polygon into triangles so GPUs can render it; for a simple polygon with n vertices, a triangulation contains n−2 triangles. Earcut is Mapbox's widely used JavaScript triangulation library, designed to be small (about 4 KB gzipped) and fast enough for real-time browser use, favoring speed and simplicity over mesh quality. Ear clipping is a common family of algorithms that repeatedly clips convex 'ears' from a polygon, while alternatives such as Seidel's trapezoidal method and Delaunay triangulation offer different complexity and quality trade-offs. WebAssembly lets computationally heavy geometry code run at near-native speed in browsers, making WASM triangulators a natural comparison point for pure-JS libraries.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/mapbox/earcut">GitHub - mapbox/earcut: The fastest and smallest JavaScript ...</a></li>
<li><a href="https://en.wikipedia.org/wiki/Polygon_triangulation">Polygon triangulation - Wikipedia</a></li>
<li><a href="https://dev.to/tianyaschool/combining-webassembly-with-webgl-high-performance-graphics-processing-322">Combining WebAssembly with WebGL High-Performance Graphics ...</a></li>

</ul>
</details>

**Discussion**: Earcut author mourner praised the work, explained that he deliberately rejected some optimizations to keep Earcut's bundle small, and asked about the size of the WebAssembly build; Delaunay32 author morishuz asked how the divide-and-conquer constrained Delaunay approach would compare with the baseline. Commenters also debated why ear clipping has won in practice over Seidel's trapezoidal method and raised concerns about long, thin triangles affecting GPU rasterization.

**Tags**: `#computational-geometry`, `#triangulation`, `#performance-optimization`, `#webassembly`, `#gis-mapping`

---

<a id="item-6"></a>
## [Switch 2 Jailbroken: ns2jb Software Exploit Built With an LLM-Driven KVM Rig](https://pepsipu.com/blog/2026-10-switch2-jailbreak-ns2jb/) ⭐️ 8.0/10

Security researcher pepsipu published ns2jb, described as the first software-only, tethered userland jailbreak for the Nintendo Switch 2, reportedly working on the latest 23.0.1 firmware. The exploit chains a SmileBASIC 4 integer overflow with a buffer overflow in the `fs` sysmodule to reach native code execution, enabling homebrew, game mods and save backups. The Switch 2 shipping with a working software exploit so early in its life is a worst-case scenario for Nintendo, since decrypted filesystem access could quickly lead to game dumps and the recomps/decomps that let console exclusives run on arbitrary hardware. It also demonstrates a reusable pattern — LLM agents given "eyes and arms" through KVM and USB/HDMI — that could speed up exploit research on other closed devices. The jailbreak is tethered rather than a permanent custom firmware: it must be re-applied after every reboot, which limits casual use and keeps a console restart as the main recovery path. The write-up also details the automation stack, in which JetKVM units send controller inputs over USB and capture HDMI video while a Bluetooth switch-flicker bot (identified by commenters as a SwitchBot Bot) physically presses the power button when the console crashes.

hackernews · ledoge · Oct 22, 08:01 · [Discussion](https://news.ycombinator.com/item?id=50192536)

**Background**: Jailbreaking a console means exploiting bugs in its software to run code Nintendo did not authorize, typically to enable homebrew applications, mods and save management. A "userland" exploit gains control inside an unprivileged application process, and chaining it with a kernel or system-module flaw (here a buffer overflow in `fs`, the filesystem module) is what allows broader access such as reading decrypted files. KVM here means keyboard-video-mouse-over-IP hardware that lets a remote machine control a physical computer, which is why an AI coding agent like OpenAI Codex could drive real Switch consoles automatically and iterate on exploits without human hands.

<details><summary>References</summary>
<ul>
<li><a href="https://gbatemp.net/news/switch-2-jailbreak-ns2jb-released-software-only-exploit-tethered.685698/">Switch 2 jailbreak "ns2jb" released. Software-only exploit ...</a></li>
<li><a href="https://www.techspot.com/news/114303-nintendo-switch-2-jailbreaking-here-homebrew-modding-reverse.html">Nintendo Switch 2 jailbreaking is here, with homebrew ...</a></li>
<li><a href="https://www.aipulse.it/en/news/nintendo-switch-2-jailbreak-ns2jb-exploit-504293">Switch 2 Jailbroken: First Software Exploit Runs Homebrew and ...</a></li>

</ul>
</details>

**Discussion**: Commenters were impressed on both fronts: several predicted that if decrypted read/write `fs` access is real, Switch 2 game dumps could surface within hours, feeding the recomps/decomps scene that already runs Tears of the Kingdom at 60fps on an iPhone. Others focused on the hardware plumbing — the JetKVMs, USB controller support and the Bluetooth "Switch SwitchBot Bot" that presses the power button — as a neat template for automation, while one user questioned how much the LLM actually contributed, noting that Codex often refuses security research tasks and that the blog reads like the work of an experienced security expert.

**Tags**: `#switch2`, `#jailbreak`, `#security`, `#llm-agents`, `#hardware-hacking`

---

<a id="item-7"></a>
## [Carbon-X: an open 14.8B model trained jointly on DNA and text](https://www.reddit.com/r/MachineLearning/comments/1xchayq/carbonx_is_an_open_148b_model_trained_jointly_on/) ⭐️ 8.0/10

HuggingFaceBio released Carbon-X, an Apache-2.0, 14.8B-parameter decoder-only model that accepts raw DNA inside an ordinary chat and answers in English, using a single shared token stream in which DNA is encoded as 6-mer tokens alongside normal text. After mid-training on 302B tokens, the model card reports a 66.7% average across five DNA benchmarks with thinking disabled, compared with 67.5% for GPT-6.1 Sol. Because the weights fit on a single 80GB GPU and are openly licensed, genomics teams can run sequence analysis entirely on their own hardware, which matters a lot for sensitive or private patient data that cannot be sent to a proprietary API and for reproducible research. A near-parity open model on DNA benchmarks also signals that general-purpose LLM architectures with unified DNA/text tokenization are becoming a viable alternative to specialized genomics models. The bf16 weights consume roughly 30GB, so the model comfortably fits on one 80GB GPU, though the authors do not claim clinical validity and the model card explicitly says exact sequence operations should still be handled by code rather than by the model itself. The headline benchmark number is an average over five DNA tasks with thinking disabled, and the comparison target is a frontier proprietary model whose own variant-level performance on private data remains unverified.

reddit · r/MachineLearning · /u/jatingargiitk · Oct 22, 12:32

**Background**: DNA language models apply the same next-token prediction objective used by text LLMs to genomic sequence, but first the raw nucleotide string must be split into tokens; a common approach is k-mer tokenization, which groups k consecutive bases (here 6) into one token, an idea popularized by models such as DNABERT. Carbon-X differs by funneling those 6-mer tokens and ordinary text tokens through a single shared vocabulary and token stream, rather than training a separate DNA-only encoder. Benchmarks for this space, such as BEND-style task suites, typically test whether a model captures biologically meaningful signals like regulatory element activity or splice sites.

<details><summary>References</summary>
<ul>
<li><a href="https://xqiu625.github.io/ai4bio-concepts/foundation-models-deep-learning/tokenization-strategies.html">Tokenization Strategies - AI4Bio Learning Hub</a></li>
<li><a href="https://indepth.dev/posts/2025/en/floats-and-model-memory">Floats, bfloat, and how bits shape model memory - indepth.dev</a></li>
<li><a href="https://openreview.net/pdf?id=5NM4guc90N">L2G: Repurposing Language Models for Genomics Tasks</a></li>

</ul>
</details>

**Tags**: `#genomics`, `#large-language-models`, `#open-source-models`, `#foundation-models`, `#bioinformatics`

---

<a id="item-8"></a>
## [Tesla begins North American production of steering-wheel-less Cybercab robotaxi](https://t.me/zaihuapd/44614) ⭐️ 8.0/10

Tesla has reportedly started mass production of the Cybercab in North America, a purpose-built two-seat autonomous EV that deletes the steering wheel, pedals and side mirrors entirely. The vehicle's architecture and human-machine interface are designed around a camera-only Full Self-Driving system that takes direct control of driving. A mass-produced car built with no manual controls is a symbolic milestone for the Robotaxi industry, moving autonomous ride-hailing from retrofitted test vehicles toward dedicated hardware. If Tesla can scale it, it would pressure rivals such as Waymo and Baidu's Apollo Go and reshape how urban fleets are designed and regulated. The Cybercab is a two-passenger battery-electric robotaxi using a camera-only sensor setup with no lidar, and it also omits the rear window and side mirrors. Notably, a vehicle without a steering wheel currently cannot be sold to consumers or legally driven in most markets, so its deployment depends on regulatory exemptions and Tesla's own Robotaxi network operations.

telegram · zaihuapd · Oct 22, 07:54

**Background**: Robotaxi refers to driverless ride-hailing services, where a fleet of autonomous cars picks up passengers without a human safety driver. Tesla unveiled the Cybercab concept in October 2024 as the centerpiece of its Robotaxi business, betting that its camera-based Full Self-Driving software can reach unsupervised operation at far lower hardware cost than lidar-based rivals. Until now, Tesla's paid robotaxi service has relied on modified Model Y vehicles with safety monitors in a handful of US cities.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Tesla_Cybercab">Tesla Cybercab - Wikipedia</a></li>
<li><a href="https://electrek.co/2026/07/06/tesla-cybercab-production-before-autonomy/">Tesla Cybercab: mass-producing a car it can't sell or drive... | Electrek</a></li>
<li><a href="https://www.tesla.com/robotaxi">Robotaxi | Tesla</a></li>

</ul>
</details>

**Tags**: `#Tesla`, `#Cybercab`, `#autonomous driving`, `#Robotaxi`, `#EV`

---

<a id="item-9"></a>
## [Oracle Issues Critical Security Alert for High-Severity Java SE Flaw](https://www.oracle.com/security-alerts/alert-cve-2026-91403.html) ⭐️ 8.0/10

Oracle released Security Alert CVE-2026-91403, a CVSS 9.1 flaw in the JSSE component of Java SE that can be exploited remotely without authentication, with patches published for affected Java SE and GraalVM releases including 8u511, 11.0.33, 17.0.21, 21.0.13, 25.0.5, 27.0.1 and multiple GraalVM versions. Because JSSE is the standard TLS/SSL layer shipped inside every JDK, the flaw touches a vast installed base of enterprise servers, middleware and client applications across several long-term-support lines at once, making this an urgent patch-now item rather than a routine update. Oracle notes that the vulnerability is exploitable via APIs in the affected component — for example through a web service that supplies data to those APIs — and that it also affects deployments such as sandboxed Java Web Start applications or applets that load untrusted code; no workaround is listed in the CVE record, so applying the Oracle patches (or restricting network exposure to Java/GraalVM services in the interim) is the recommended path.

telegram · zaihuapd · Oct 22, 12:30

**Background**: JSSE (Java Secure Socket Extension) is the Java API and provider implementation that gives the Java runtime its TLS/SSL capabilities, enabling secure internet communications; it ships as a standard component of the JDK and follows the same provider-based design as the Java Cryptography Architecture. CVSS scores run from 0 to 10, and 9.1 falls in the "critical" band, signalling a remotely reachable flaw with serious impact on confidentiality and integrity. GraalVM is Oracle's standalone JDK distribution built on the Java SE runtime, which is why it inherits the same defect and needs its own patched releases.

<details><summary>References</summary>
<ul>
<li><a href="https://www.oracle.com/security-alerts/alert-cve-2026-91403.html">Oracle Security Alert Advisory - CVE-2026-91403</a></li>
<li><a href="https://blogs.oracle.com/security/security-alert-cve-2026-91403-released">Security Alert CVE-2026-91403 Released - Oracle Blogs</a></li>
<li><a href="https://en.wikipedia.org/wiki/Java_Secure_Socket_Extension">Java Secure Socket Extension - Wikipedia</a></li>

</ul>
</details>

**Tags**: `#security`, `#java`, `#vulnerability`, `#cve`, `#oracle`

---

<a id="item-10"></a>
## [333 Backdoored Tor Exit Relays Taken Offline After Ebury Infection](https://kaba.cx/posts/20261020_Tor/) ⭐️ 8.0/10

A Tor operator scanned roughly 3,000 exit relays with a script and found 333 of them — about 10% — infected with the Ebury backdoor, which hijacked SSH connections on port 22 to 12 interception servers to steal credentials. The relays were flagged as BadExit on October 4 and all went offline the following day. Tor exit relays are the final hop where traffic leaves the anonymity network, so a compromise at this scale directly threatens the credentials of anyone using those exits for SSH or other plaintext protocols. The incident also shows how a long-lived SSH-dwelling backdoor can quietly spread through hosting infrastructure and turn privacy infrastructure into a credential-harvesting pipeline. The attackers appear to have compromised the servers in August 2026 and blocked certain ports so the relays would mainly collect unencrypted mail traffic; how they initially gained access is still undetermined. The response relied on the Tor directory authorities' BadExit flag, which removes a relay from exit duty without necessarily removing it from the network entirely.

telegram · zaihuapd · Oct 22, 14:52

**Background**: Tor routes traffic through three relays, and the exit relay is the last one, where traffic reaches the open internet — meaning the exit operator can observe or tamper with anything not end-to-end encrypted. Ebury is a Linux malware family that lives inside SSH servers, steals credentials and spreads to other hosts, and has been tracked infecting large numbers of servers over many years. When directory authorities assign the BadExit flag to a relay, Tor clients stop using it for exit traffic, effectively demoting it to a non-exit relay.

<details><summary>References</summary>
<ul>
<li><a href="https://arstechnica.com/security/2024/05/ssh-backdoor-has-infected-400000-linux-servers-over-15-years-and-keeps-on-spreading/">Linux maintainers were infected for 2 years by SSH-dwelling backdoor ...</a></li>
<li><a href="https://www.eff.org/pages/what-tor-relay">What is a Tor Relay ? | Electronic Frontier Foundation</a></li>
<li><a href="https://support-torran-614d1f0af8d705a14a8e1cd6f9898bed23485e1842c2493e.pages.torproject.net/relay-operators/what-is-the-bad-exit-flag/">What is the BadExit flag? | Tor Project | Support</a></li>

</ul>
</details>

**Tags**: `#Tor`, `#security`, `#malware`, `#privacy`, `#network-security`

---

<a id="item-11"></a>
## [Export-banned Nvidia B300 chips surface in Chinese state-backed deployment](https://theinference.org/article/china-s-state-money-bought-banned-nvidia-b300-servers-then-redacted-the-receipts) ⭐️ 8.0/10

A Chinese state-controlled semiconductor leasing group reportedly financed the purchase of 32 ASUS servers equipped with export-banned Nvidia B300 GPUs as part of a larger 700-plus server deal worth over ¥3 billion, intended for China Mobile's Ningxia hub; after the filing drew regulatory attention, the group resubmitted documents with the hardware descriptions removed. Both Nvidia and ASUS said they are investigating the matter and complying with export controls. The B300 sits in the most restrictive US export-control tier and is effectively banned for sale to China, so if the reporting holds, it would be a concrete case of top-tier AI compute reaching a state-linked Chinese deployment despite controls. It puts fresh scrutiny on the grey-market supply chain and on intermediaries such as leasing firms, distributors and OEMs that export rules rely on to actually bite. The GPU in question is the B300 (B300 SXM6), a Blackwell-generation part with 288 GB of HBM3e memory on an 8192-bit bus, making it the highest-memory accelerator commonly listed among available Nvidia parts. The deal is reported at over ¥3 billion for 700-plus servers and targets China Mobile's Ningxia (Zhongwei) computing campus, and the redaction of hardware details from refiled documents is itself a notable element of the story.

telegram · zaihuapd · Oct 22, 15:22

**Background**: Washington restricts advanced AI chip exports through a tiered system, and the AI Diffusion Rule framework places top-tier destinations like Japan and South Korea under far lighter restrictions than China, which is cut off from B300-class hardware entirely. China Mobile's Ningxia Zhongwei data center is one of the country's flagship AI computing campuses, with hundreds of megawatts of commissioned IT capacity and heavy renewable-energy integration, making it a natural destination for large GPU clusters. Export controls bind chipmakers and OEMs like Nvidia and ASUS, but financing intermediaries and leasing arrangements can obscure where end hardware actually lands.

<details><summary>References</summary>
<ul>
<li><a href="https://www.techpowerup.com/gpu-specs/b300-sxm6-ac.c4375">NVIDIA B 300 SXM6 AC Specs | TechPowerUp GPU Database</a></li>
<li><a href="https://www.trendforce.com/news/2025/03/27/news-u-s-ai-chip-controls-are-coming-a-breakdown-of-the-tiered-restrictions/">[News] U . S . AI Chip Controls Are Coming— A Breakdown of the...</a></li>
<li><a href="https://www.datacenters.com/china-mobile-international-ltd-ningxia-zhongwei">China Mobile International Ltd: Ningxia Zhongwei Data Center</a></li>

</ul>
</details>

**Tags**: `#Nvidia`, `#export-controls`, `#semiconductors`, `#AI-infrastructure`, `#China`

---

<a id="item-12"></a>
## [SpaceX in Talks to Lease 80,000 Cell Sites for U.S. Wireless Carrier](https://www.bloomberg.com/news/articles/2026-10-22/spacex-in-talks-to-access-80-000-cell-sites-for-wireless-network) ⭐️ 8.0/10

SpaceX is reportedly negotiating to lease at least 80,000 cellular tower sites from Crown Castle and at least one other infrastructure company as it advances plans for a fourth U.S. nationwide wireless carrier. People familiar with the matter said the deal could be worth several billion dollars. If SpaceX combines a leased terrestrial footprint with its own spectrum and direct-to-cell satellites, it could become a genuine fourth U.S. wireless carrier and intensify pressure on AT&T, Verizon and T-Mobile. The market reaction—Crown Castle up about 10% after hours while the three incumbents fell roughly 5%—shows investors view the move as a serious competitive threat. The report says SpaceX acquired low-band spectrum this month and has been cleared to launch 15,000 direct-to-cell satellites, but leasing 80,000 sites is only one piece of building a nationwide network. Low-band spectrum supports broad coverage and indoor penetration, while direct-to-cell service is best suited to filling gaps and providing basic connectivity outside terrestrial coverage.

telegram · zaihuapd · Oct 23, 03:30

**Background**: Crown Castle is a U.S. communications infrastructure real estate investment trust (REIT) that owns and leases tower and small-cell sites to wireless carriers, so a lease deal would give SpaceX immediate access to thousands of physical locations without building towers from scratch. Low-band spectrum refers to lower radio frequencies that travel farther and penetrate buildings better than higher bands, making it valuable for wide-area coverage even though it carries less capacity. Direct-to-cell technology lets ordinary smartphones connect to satellites, which can extend coverage to areas without terrestrial service; SpaceX's Starlink constellation is central to that effort.

<details><summary>References</summary>
<ul>
<li><a href="https://www.gsm.pku.edu.cn/123456789.pdf">REITsReal Estate Investment Trusts 是以发行权益投</a></li>
<li><a href="https://www.telecomsci.com/rc-pub/front/front-article/download/145774237/lowqualitypdf/手机直连卫星系统及其星载相控阵天线分析与建议.pdf">手 机 直 连 卫 星 系统及其 星 载相控阵天线分析与建议</a></li>

</ul>
</details>

**Tags**: `#SpaceX`, `#telecom`, `#wireless networks`, `#satellite connectivity`, `#spectrum`

---