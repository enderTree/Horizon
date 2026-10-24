---
layout: default
title: "Horizon Summary: 2026-10-24 (ZH)"
date: 2026-10-24
lang: zh
---

> 从 33 条内容中筛选出 4 条重要资讯。

---

1. [PHP 紧急发布补丁修复两个 CVSS 9.2 的严重远程代码执行漏洞](#item-1) ⭐️ 9.0/10
2. [月之暗面发布 Kimi K3.1 Pro：3T 级开放权重模型](#item-2) ⭐️ 8.0/10
3. [研究者公开可用的 iPhone 漏洞利用链演示](#item-3) ⭐️ 8.0/10
4. [Telegram 爆料称 iPhone 18 Pro 实现自 iOS 9 以来首个不完美越狱之外的完整不完美越狱](#item-4) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [PHP 紧急发布补丁修复两个 CVSS 9.2 的严重远程代码执行漏洞](https://t.me/zaihuapd/44647) ⭐️ 9.0/10

PHP 团队发布紧急的非计划安全更新，修复两个允许攻击者在无需登录的情况下远程执行任意代码的漏洞，两项漏洞在 CVSS 4.0 标准下均被评为 9.2 分。官方敦促用户立即升级至 PHP 8.5.12、8.4.27、8.3.36 或 8.2.35。 这些漏洞几乎影响所有处理网页请求的 PHP 部署，从小型站点到大型生产集群均在其列，因此几乎所有运行 PHP 的后端与基础设施团队都处在影响范围内。由于利用漏洞无需任何凭据，任何暴露在外、尚未打补丁的服务器在完成升级前都应被视为存在风险。 所有处理网页请求的 SAPI 均受影响，包括 PHP-FPM、Apache 的 mod_php、php-cgi、FrankenPHP 和 LiteSpeed；其中 mod_php 风险最高，因为已有验证表明攻击可在网站业务代码运行之前就被触发。补丁同时在 8.2 至 8.5 四个受支持分支上发布，这种非例行做法本身就说明漏洞的严重程度非同寻常。

telegram · zaihuapd · 10月23日 13:46

**背景**: PHP 是驱动互联网的最广泛部署的服务端脚本语言之一，但它并不直接与 Web 服务器通信：SAPI（服务器应用编程接口）是连接 Web 服务器或应用服务器（如 Apache、PHP-FPM、FrankenPHP）与 PHP 解释器的那一层。正因为这一层位于每个请求的最前端，其中的缺陷可能在任何框架或业务代码执行之前就被触达，这也是此类未授权漏洞格外危险的原因。由 FIRST 于 2023 年 11 月发布的 CVSS 4.0 沿用人们熟悉的 0–10 分严重级别区间，其中 9.0 至 10.0 分被归为“严重（Critical）”。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.php.net/downloads.php">PHP : Downloads</a></li>
<li><a href="https://frankenphp.dev/">FrankenPHP : the modern PHP app server</a></li>
<li><a href="https://secportal.io/blog/cvss-4-0-vs-3-1-explained">CVSS 4 . 0 vs CVSS 3.1: Differences, Migration, Audit Impact</a></li>

</ul>
</details>

**标签**: `#security`, `#php`, `#vulnerability`, `#remote-code-execution`, `#patching`

---

<a id="item-2"></a>
## [月之暗面发布 Kimi K3.1 Pro：3T 级开放权重模型](https://www.kimi.ai/blog/kimi-k3-1-pro) ⭐️ 8.0/10

2026 年 10 月 24 日，月之暗面（Moonshot AI）发布了全新 K3.1 系列的首款模型 Kimi K3.1 Pro，并同步推出速度更快的 Kimi K3.1 Pro Highspeed 版本。官方称 K3.1 Pro 是其迄今最强的 3T 级开放权重模型，拥有 100 万 token 上下文窗口，并在编程、3D 创作、金融研究和智能体任务上取得显著提升。 一个拥有百万级上下文窗口的 3 万亿参数级开放权重模型，使月之暗面直接站到了西方前沿实验室的竞争行列中；社区测试显示，它在部分智能体任务上追平 Claude Sonnet 5.5，而成本不到后者的一半。官方承诺在 11 月 4 日前放出完整模型权重，这对需要自行部署或微调前沿级模型的团队意义重大，而不必只能通过 API 租用。 K3.1 Pro 是在 Kimi K3 基础上经过后训练的版本，后训练算力大幅增加；目前已上线 Kimi.ai、Kimi Work、Kimi Code 和 Kimi API，完整模型权重计划于 11 月 4 日前发布。在评论者引用的一项独立 Pac-Man 智能体基准测试中，K3.1 Pro 与 Claude Sonnet 5.5 同为 93 分，但成本仅 0.68 美元、耗时 11 分钟，而 Sonnet 为 1.61 美元和 14 分钟。

hackernews · Jowsey · 10月23日 16:59 · [社区讨论](https://news.ycombinator.com/item?id=50212065)

**背景**: 总部位于中国的月之暗面（Moonshot AI）开发 Kimi 系列大语言模型，并通过网页应用、API 和 Kimi Code 命令行智能体以开放权重的方式对外提供，模型支持图像和视频等多模态输入。开放权重发布之所以重要，是因为任何人都可以下载模型并在自有硬件上运行或微调，这与 Anthropic 的 Claude 等闭源模型形成对比——后者只能通过付费 API 使用。由于厂商自报的分数往往经过挑选，业界常用 Artificial Analysis 以及社区自发的基准测试（如 Pac-Man bakeoff）来比较模型的能力与价格。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://platform.kimi.ai/docs/guide/kimi-k3-1-pro-quickstart">Kimi K3.1 Pro - Kimi API Platform</a></li>
<li><a href="https://www.unite.ai/moonshot-ai-releases-kimi-k3-1-pro-first-model-in-new-k3-1-series/">Moonshot AI Releases Kimi K3.1 Pro , First Model in New K3.1 ...</a></li>
<li><a href="https://en.wikipedia.org/wiki/Moonshot_AI">Moonshot AI - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: Hacker News 的评论者主要围绕性价比展开讨论：有人报告 K3.1 Pro 在 Pac-Man 智能体基准上以更低的费用和更短的时间追平 Claude Sonnet 5.5；也有人指出模型在推理过程中出现奇怪的身份混乱，有时自称 ChatGPT 或提到“评估者”。多位用户质疑月之暗面移除网络安全训练数据的做法，追问他是否连同普通软件知识一并删除；还有一位长期订阅用户警告说，五小时的使用限额让付费套餐几乎无法使用。

**标签**: `#AI models`, `#LLM`, `#Kimi`, `#benchmarks`, `#model release`

---

<a id="item-3"></a>
## [研究者公开可用的 iPhone 漏洞利用链演示](https://blog.calif.io/p/iphone) ⭐️ 8.0/10

一篇发布在 blog.calif.io 的博客文章《Today, we hacked what we'd set out to hack: the iPhone》展示了针对 iOS 的可运行漏洞利用演示，据读者反馈其中至少有一个演示可以让攻击者获得设备的 root 权限。该文在 Hacker News 上获得 779 分和 526 条评论，读者对各个演示及其背后的攻击向量进行了深入讨论。 公开且完整的 iOS 漏洞利用链非常罕见，每一条都为攻防双方提供了这个世界最封闭消费级平台攻击面的具体地图。围绕该文的讨论也凸显出，这类研究很快就会被追问缓解措施、补丁修复以及实际防御价值等问题。 该文章被定位为带有演示的定向漏洞利用研究，而非通用越狱工具；评论者指出，其中某些演示步骤似乎把解析阶段与提权阶段串联了起来。讨论中提出的关键未解问题是：这种访问权限能否在苹果系统更新后继续保留，以及锁定模式（Lockdown mode）能否有效阻断演示中的任何攻击向量。

hackernews · pavel_lishin · 10月23日 16:21 · [社区讨论](https://news.ycombinator.com/item?id=50211474)

**背景**: iOS 越狱是指利用内核或用户态漏洞移除苹果施加的软件限制，通常是为了获得 root 级别的文件系统访问权限并安装未经授权的软件。苹果的锁定模式（Lockdown mode）是一个可选的极端安全设置，通过禁用或限制许多消息附件类型和复杂网页技术等特性来缩小攻击面。此前备受关注的利用链，例如 Google Project Zero 分析的 NSO Pegasus “ForcedEntry” 漏洞，就是通过 iMessage 投递畸形的 PDF 类内容，这也是 PDF 处理环节在这些讨论中反复出现的原因。再比如 checkm8 这类 BootROM 漏洞属于“不完美越狱”（tethered），每次开机都必须重新运行，说明持久化往往是最困难的一环。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/IOS_jailbreaking">iOS jailbreaking - Wikipedia</a></li>
<li><a href="https://arstechnica.com/information-technology/2019/09/developer-of-checkm8-explains-why-idevice-jailbreak-exploit-is-a-game-changer/">Developer of Checkm8 explains why iDevice jailbreak exploit is...</a></li>

</ul>
</details>

**社区讨论**: 评论者大多对演示表示赞赏，但同时追问防御层面的问题：开启锁定模式是否真的有用、该技术能否在苹果更新后继续存在或反过来阻止更新，以及为什么 PDF 解析始终是 iOS 上如此可靠的攻击面，并将其与 Pegasus 的 ForcedEntry 相提并论。也有人询问该利用链是否依赖攻陷某个内核模块或 iMessage 附件读取组件来实现提权，还有评论者调侃说这些被攻破的 iPhone 能做的事情比苹果官方允许的设备更酷。

**标签**: `#iOS security`, `#jailbreak`, `#exploit research`, `#mobile security`, `#vulnerability analysis`

---

<a id="item-4"></a>
## [Telegram 爆料称 iPhone 18 Pro 实现自 iOS 9 以来首个不完美越狱之外的完整不完美越狱](https://t.me/zaihuapd/44644) ⭐️ 8.0/10

Telegram 频道「科技圈·茶馆」发布消息称，iPhone 18 Pro 已被成功越狱，且属于重启后越狱状态依然保留、无需连接电脑的 untethered（不完美/完全）越狱，演示者署名为 @calif_io。该消息称攻击链由 cryptex 子系统、TSS 票签欺骗和 PAC（指针认证码）绕过三层组成，并称这是自 iOS 9 以来首个公开的完整越狱。 如果得到证实，这将是约十年来首个公开演示的完整 untethered 越狱，说明 Apple 的代码签名、cryptex 封装的系统内容以及指针认证等多层防御，在新款硬件上仍可能被组合攻破。其意义远不止于玩机爱好者的折腾，因为这些原语同样是安全研究人员和攻击者在 iOS 上实现持久化与后渗透时所依赖的能力。 目前该说法仅来自一条简短的社交媒体帖子，没有技术细节、概念验证代码，也未说明受影响的 iOS 版本，因此应视为未经证实；值得注意的是，消息称该攻击链在 Apple 于 9 月 14 日修复 273 个漏洞之后依然有效。所谓 untethered 越狱，特指每次重启后漏洞利用都能自行重新建立、无需借助电脑，这比 tethered 或 semi-tethered 方案的门槛高得多。

telegram · zaihuapd · 10月23日 11:43

**背景**: 越狱是指利用漏洞链解除 iOS 的软件限制，从而运行未签名的代码；其中 untethered（完全越狱）意味着越狱状态在重启后依然保持，而 tethered 和 semi-tethered 越狱则需要借助电脑或特定 App 重新触发漏洞。PAC（Pointer Authentication Code，指针认证码）是 Apple 在 ARM 硬件上启用的机制，用密码学方式对指针签名，使被篡改或伪造的指针直接导致进程崩溃，因此绕过 PAC 是现代 iOS 内核利用的核心环节。cryptex 子系统随 iOS 16 引入（macOS 中也有使用），它把系统内容封装在经过密码学签名的磁盘镜像中，由 iOS 在启动时挂载，从而让篡改系统文件变得更加困难。TSS（Ticket Signing Service）是 Apple 的服务器端签名服务，负责签发授权固件恢复的 SHSH 票签；所谓 TSS「票签欺骗」，就是指诱使设备接受未经授权的恢复或签名状态。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://eclecticlight.co/2022/11/16/cryptex-how-a-custom-iphone-is-changing-macos-updates/">Cryptex : how a custom iPhone is changing macOS updates</a></li>
<li><a href="https://keith.github.io/xcode-man-pages/cryptex.5.html">cryptex (5)</a></li>

</ul>
</details>

**标签**: `#iOS jailbreak`, `#security`, `#exploit chain`, `#Apple`, `#PAC bypass`

---