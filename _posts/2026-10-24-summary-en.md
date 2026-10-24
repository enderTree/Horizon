---
layout: default
title: "Horizon Summary: 2026-10-24 (EN)"
date: 2026-10-24
lang: en
---

> From 33 items, 4 important content pieces were selected

---

1. [PHP Ships Emergency Patches for Two Critical RCE Flaws Scored CVSS 9.2](#item-1) ⭐️ 9.0/10
2. [Moonshot Releases Kimi K3.1 Pro, a 3T-Class Open-Weight Model](#item-2) ⭐️ 8.0/10
3. [Researcher Publishes Working iPhone Exploit Chain Demo](#item-3) ⭐️ 8.0/10
4. [Telegram Post Claims First Untethered iPhone 18 Pro Jailbreak Since iOS 9](#item-4) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [PHP Ships Emergency Patches for Two Critical RCE Flaws Scored CVSS 9.2](https://t.me/zaihuapd/44647) ⭐️ 9.0/10

The PHP team has released emergency out-of-band security updates fixing two vulnerabilities that allow attackers to execute arbitrary code remotely without authentication, both rated 9.2 under CVSS 4.0. Users are urged to upgrade immediately to PHP 8.5.12, 8.4.27, 8.3.36, or 8.2.35. The flaws affect essentially every PHP deployment that handles web requests, from small sites to large production fleets, so the blast radius covers nearly all backend and infrastructure teams running PHP. Because exploitation requires no credentials, any exposed server running an unpatched version should be treated as at risk until it is updated. All web request-handling SAPIs are affected, including PHP-FPM, Apache's mod_php, php-cgi, FrankenPHP, and LiteSpeed, with mod_php considered the highest risk because exploitation has been demonstrated to trigger before application code even runs. Patches were issued simultaneously across four supported branches (8.2 through 8.5), an unusual step that signals exceptional severity.

telegram · zaihuapd · Oct 23, 13:46

**Background**: PHP is one of the most widely deployed server-side scripting languages powering the web, and it does not talk to web servers directly: a SAPI (Server Application Programming Interface) is the layer that connects the web server or application server, such as Apache, PHP-FPM, or FrankenPHP, to the PHP interpreter. Because that layer sits in front of every request, a bug there can be reached before any framework or application code executes, which is what makes unauthenticated flaws in it so dangerous. CVSS 4.0, released in November 2023 by FIRST, keeps the familiar 0–10 severity bands in which scores from 9.0 to 10.0 are classified as Critical.

<details><summary>References</summary>
<ul>
<li><a href="https://www.php.net/downloads.php">PHP : Downloads</a></li>
<li><a href="https://frankenphp.dev/">FrankenPHP : the modern PHP app server</a></li>
<li><a href="https://secportal.io/blog/cvss-4-0-vs-3-1-explained">CVSS 4 . 0 vs CVSS 3.1: Differences, Migration, Audit Impact</a></li>

</ul>
</details>

**Tags**: `#security`, `#php`, `#vulnerability`, `#remote-code-execution`, `#patching`

---

<a id="item-2"></a>
## [Moonshot Releases Kimi K3.1 Pro, a 3T-Class Open-Weight Model](https://www.kimi.ai/blog/kimi-k3-1-pro) ⭐️ 8.0/10

Moonshot AI released Kimi K3.1 Pro on October 24, 2026, the first model in its new K3.1 series, together with a faster companion variant called Kimi K3.1 Pro Highspeed. The company describes K3.1 Pro as its most capable 3T-class open-weight model to date, featuring a 1-million-token context window and substantial gains in coding, 3D creation, financial research, and agentic tasks. A 3-trillion-parameter-class open-weight model with a million-token context puts Moonshot in direct competition with Western frontier labs, and community benchmarks suggest it matches Claude Sonnet 5.5 on some agentic tasks at less than half the cost. The promised weight release by November 4 makes it significant for teams that need to self-host or fine-tune frontier-class models rather than rent them via API. K3.1 Pro is a post-trained version of Kimi K3 trained with substantially larger post-training compute, and it is available today on Kimi.ai, Kimi Work, Kimi Code, and the Kimi API, with full model weights slated for release by November 4. In an independent Pac-Man agent benchmark cited by commenters, K3.1 Pro tied Claude Sonnet 5.5 at a score of 93 while costing $0.68 and 11 minutes versus Sonnet's $1.61 and 14 minutes.

hackernews · Jowsey · Oct 23, 16:59 · [Discussion](https://news.ycombinator.com/item?id=50212065)

**Background**: Moonshot AI, based in China, develops the Kimi series of large language models, which it distributes as open weights through a web app, an API, and the Kimi Code command-line agent; the models support multimodal image and video input. Open-weight releases matter because anyone can download and run or fine-tune the model on their own hardware, in contrast to closed models such as Anthropic's Claude, which are only accessible through a paid API. Artificial Analysis and community-run benchmarks like the Pac-Man bakeoff are commonly used to compare these models on capability and price, since vendor-reported scores are often selective.

<details><summary>References</summary>
<ul>
<li><a href="https://platform.kimi.ai/docs/guide/kimi-k3-1-pro-quickstart">Kimi K3.1 Pro - Kimi API Platform</a></li>
<li><a href="https://www.unite.ai/moonshot-ai-releases-kimi-k3-1-pro-first-model-in-new-k3-1-series/">Moonshot AI Releases Kimi K3.1 Pro , First Model in New K3.1 ...</a></li>
<li><a href="https://en.wikipedia.org/wiki/Moonshot_AI">Moonshot AI - Wikipedia</a></li>

</ul>
</details>

**Discussion**: Hacker News commenters focused on cost-effectiveness, with one reporting that K3.1 Pro ties Claude Sonnet 5.5 on a Pac-Man agent benchmark for less money and time, while others flagged odd self-identification in the reasoning traces where the model sometimes calls itself ChatGPT or references "the evaluator." Several users questioned Moonshot's removal of cybersecurity training data, asking whether ordinary software knowledge was also stripped out, and one long-term subscriber warned that the five-hour usage limit makes the paid plan nearly unusable.

**Tags**: `#AI models`, `#LLM`, `#Kimi`, `#benchmarks`, `#model release`

---

<a id="item-3"></a>
## [Researcher Publishes Working iPhone Exploit Chain Demo](https://blog.calif.io/p/iphone) ⭐️ 8.0/10

A blog post at blog.calif.io titled "Today, we hacked what we'd set out to hack: the iPhone" walks through working exploit demos against iOS, reportedly including one that yields root access to the device. The post drew 779 points and 526 comments on Hacker News, with readers digging into the individual demos and the attack vectors behind them. Publicly documented, end-to-end iOS exploit chains are rare, and each one gives both defenders and attackers a concrete map of the attack surface on the world's most locked-down consumer platform. The discussion highlights how quickly such research turns into questions about mitigation, patching, and real-world defensive value. The write-up is framed as targeted exploitation research with demos rather than a general-purpose jailbreak tool, and commenters note that specific demo steps appear to chain a parsing stage with a privilege-escalation stage. Key open questions raised are whether the access persists across Apple software updates and whether Lockdown mode meaningfully blocks any of the demonstrated vectors.

hackernews · pavel_lishin · Oct 23, 16:21 · [Discussion](https://news.ycombinator.com/item?id=50211474)

**Background**: iOS jailbreaking means using kernel or userland exploits to strip away the software restrictions Apple imposes, typically to gain root-level file system access and install unauthorized software. Apple's Lockdown Mode is an optional extreme-security setting that shrinks the attack surface by disabling or restricting features such as many message attachment types and complex web technologies. Prior high-profile chains, such as NSO's Pegasus "ForcedEntry" exploit analyzed by Google's Project Zero, used malformed PDF-style content delivered through iMessage, which is why PDF handling keeps coming up in these discussions. Some exploits, like the checkm8 bootrom bug, are tethered and must be re-run on every boot, showing that persistence is often the hardest part.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/IOS_jailbreaking">iOS jailbreaking - Wikipedia</a></li>
<li><a href="https://arstechnica.com/information-technology/2019/09/developer-of-checkm8-explains-why-idevice-jailbreak-exploit-is-a-game-changer/">Developer of Checkm8 explains why iDevice jailbreak exploit is...</a></li>

</ul>
</details>

**Discussion**: Commenters largely reacted with admiration for the demos while pushing on defensive questions: whether enabling Lockdown mode actually helps, whether the technique can survive or block Apple updates, and why PDF parsing remains such a reliable iOS attack surface, with comparisons drawn to Pegasus ForcedEntry. Others asked whether the chain depends on compromising a kernel module or an iMessage attachment reader to escalate privileges, and one commenter joked that these hacked iPhones do cooler things than an Apple-approved device.

**Tags**: `#iOS security`, `#jailbreak`, `#exploit research`, `#mobile security`, `#vulnerability analysis`

---

<a id="item-4"></a>
## [Telegram Post Claims First Untethered iPhone 18 Pro Jailbreak Since iOS 9](https://t.me/zaihuapd/44644) ⭐️ 8.0/10

A Telegram post from the channel zaihuapd claims that an iPhone 18 Pro has been jailbroken with an untethered exploit that survives a reboot without needing a computer, attributed to a demonstration by @calif_io. The post describes a three-layer attack chain combining the cryptex subsystem, TSS ticket spoofing, and a PAC (Pointer Authentication Code) bypass, and calls it the first public full jailbreak since iOS 9. If verified, this would be the first publicly demonstrated full untethered jailbreak in roughly a decade, showing that Apple's layered defenses — code signing, cryptex-sealed system content, and pointer authentication — can still be defeated together on its newest hardware. That has implications well beyond hobbyist modding, since the same primitives are what security researchers and attackers use for persistence and post-exploitation on iOS. The claim is currently a single brief social-media post with no technical write-up, proof-of-concept code, or affected iOS version listed, so it should be treated as unverified; notably, it says the chain works despite Apple having shipped fixes for 273 vulnerabilities on September 14. An untethered jailbreak specifically means the exploit re-establishes itself on every boot with no host computer, which is a much higher bar than a tethered or semi-tethered approach.

telegram · zaihuapd · Oct 23, 11:43

**Background**: A jailbreak is an exploit chain that removes iOS's software restrictions so users can run unsigned code; "untethered" means it persists across reboots, whereas tethered and semi-tethered jailbreaks need a computer or app to re-trigger the exploit. PAC, or Pointer Authentication Codes, is an ARM hardware feature Apple uses to cryptographically sign pointers so that corrupted or forged pointers crash the process instead of being usable — bypassing it is a core requirement for modern iOS kernel exploits. The cryptex subsystem, introduced with iOS 16 and also used in macOS, packages and seals system content in cryptographically signed disk images that iOS mounts at boot, which complicates tampering with system files. TSS (Ticket Signing Service) is Apple's server-side signing system that issues SHSH tickets authorizing firmware restores; TSS "spoofing" would mean tricking the device into accepting an unauthorized restore or signature state.

<details><summary>References</summary>
<ul>
<li><a href="https://eclecticlight.co/2022/11/16/cryptex-how-a-custom-iphone-is-changing-macos-updates/">Cryptex : how a custom iPhone is changing macOS updates</a></li>
<li><a href="https://keith.github.io/xcode-man-pages/cryptex.5.html">cryptex (5)</a></li>

</ul>
</details>

**Tags**: `#iOS jailbreak`, `#security`, `#exploit chain`, `#Apple`, `#PAC bypass`

---