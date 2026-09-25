---
layout: default
title: "Horizon Summary: 2026-09-25 (ZH)"
date: 2026-09-25
lang: zh
---

> 从 33 条内容中筛选出 2 条重要资讯。

---

1. [F-Droid 2.0 发布，迎来十年来最大规模改版](#item-1) ⭐️ 8.0/10
2. [Apple 在英国撤下高级数据保护，iCloud 加密形成"双轨制"](#item-2) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [F-Droid 2.0 发布，迎来十年来最大规模改版](https://f-droid.org/2026/09/24/f-droid-2.0-a-new-chapter-for-android-freedom.html) ⭐️ 8.0/10

F-Droid 于 2026 年 9 月 24 日发布 2.0 版本，这是其约十年来最大的一次更新，重新设计了界面并重写了大量底层代码，整体简化为“发现、搜索、我的应用”三大板块。该版本在此前经过 14 次测试发布后推出，并将在未来数周内向用户陆续推送。 F-Droid 是 Android 平台上最具代表性的自由开源应用商店，因此这次大规模改版会直接影响大量注重隐私与开源的、用它替代 Google Play 的用户群体。此次发布恰逢 Google 收紧对第三方来源安装应用的限制，使独立 Android 分发渠道能否持续生存成为现实议题。 新客户端改进了应用发现、分类、搜索与筛选功能，支持在应用描述、分类及翻译内容中进行搜索，并增强了对中文、日文、韩文文本的搜索能力，同时带来更顺畅的安装更新流程与后台检查更新。值得注意的是，此版本暂不支持 F-Droid Privileged Extension，并且已放弃对 Android 6 的支持。

hackernews · daveoc64 · 9月24日 15:26 · [社区讨论](https://news.ycombinator.com/item?id=49831968)

**背景**: F-Droid 是一个面向 Android 的自由开源应用商店与软件仓库，功能与 Google Play 类似，但只收录自由开源软件，无需注册账号，并会标注广告、用户追踪或依赖非自由软件等“反特性”。其网站与服务器软件本身也是开源的，任何人都可以自建仓库。F-Droid Privileged Extension 是一个可选组件，用于实现无人值守的后台安装与更新应用，此前在 LineageOS 等第三方 ROM 上往往需要额外配置才能正常工作。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/F-Droid">F-Droid</a></li>

</ul>
</details>

**社区讨论**: 评论者普遍欢迎这次大改版以及逐步淘汰 Privileged Extension，一位长期使用 GrapheneOS 的用户表示旧版 F-Droid 界面太差，以至于转用了替代客户端 Droid-ify。也有人批评新设计理念，指出首张截图中就能看到的文字换行错误，以及界面缺乏视觉分隔、可点击提示和滚动区域提示。还有用户对 F-Droid 仓库中的二进制包与开发者官方发布版本之间的信任差异表示担忧，并忧虑一旦 Google 明年封锁第三方安装，F-Droid 的未来将走向何方。

**标签**: `#F-Droid`, `#Android`, `#open-source`, `#app-store`, `#privacy`

---

<a id="item-2"></a>
## [Apple 在英国撤下高级数据保护，iCloud 加密形成"双轨制"](https://macanorak.com/two-tier-encryption-in-the-uk/) ⭐️ 8.0/10

Apple 已在英国撤下 iCloud 的"高级数据保护"（ADP）功能，原因是收到一项法律命令，该命令若被执行将要求其削弱 ADP 所依赖的安全架构。Apple 没有选择构建后门，而是直接取消了该选项，使受影响的英国 iCloud 数据回退到"标准数据保护"——原文作者称之为"双轨制"加密：在功能被撤下前已开启 ADP 的英国用户仍保留端到端加密，其余用户则不再享有。 这是一起具有里程碑意义的隐私与政策事件：它显示政府的一纸命令可以迫使一个全球性平台悄悄为整个国家的用户群体提供更弱的加密，而无需公开强制要求后门。这一先例可能被其他政府效仿，也动摇了人们长期以来的假设——大型厂商会在法庭上对抗加密要求，而不是默默降低服务水平。 根据社区分析，原本已有 14 类 iCloud 数据默认采用端到端加密，包括 iCloud 钥匙串和健康数据，而 ADP 会把这一数字提升到 23 类；对未启用 ADP 的英国用户而言，回退的数据类别包括 iCloud 备份、照片、备忘录和 iCloud 云盘等，它们降级为"标准数据保护"，此时密钥由 Apple 掌握，可依法响应合法的法律程序。有评论者反驳"这 14 类基线数据未受影响"的说法，认为英国用户的端到端加密机密在某些常见使用场景下仍可能被暴露。

hackernews · ReturnoftheHack · 9月24日 10:39 · [社区讨论](https://news.ycombinator.com/item?id=49828731)

**背景**: iCloud 数据通常使用由 Apple 存储在其数据中心的密钥进行加密，这使 Apple 能帮助用户恢复数据，但也意味着 Apple 可能被强制交出数据。"高级数据保护"是一项可选设置，它把包括备份、照片和备忘录在内的大多数数据类别切换为端到端加密，密钥仅保存在用户自己的设备上。Apple 于 2022 年底推出 ADP，而据报道，英国的相关命令依据的是《调查权力法》（Investigatory Powers Act），该法可强制企业协助合法监听，并禁止它们对外披露该要求。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://support.apple.com/en-us/108756">How to turn on Advanced Data Protection for iCloud - Apple Support</a></li>
<li><a href="https://support.apple.com/en-us/102651">iCloud data security overview - Apple Support</a></li>
<li><a href="https://macanorak.com/two-tier-encryption-in-the-uk/">Two-Tier Encryption in the UK</a></li>

</ul>
</details>

**社区讨论**: 评论者普遍持批评态度：有人指出 Apple 在 2015 年有胆量抵抗，如今却没有，并以 iPhone 设置过程中强制出现的年龄确认/KYC 界面作为"滑坡效应"的证据；另有人表示此事动摇了他们当初购买 Apple 封闭生态产品的理由，并希望 Apple 退出英国市场或切断对英国政府用户的服务。一个反复出现的担忧是，政府如今既能要求开后门，又能依法禁止厂商披露，等于变相逐步取缔端到端加密。

**标签**: `#encryption`, `#privacy`, `#apple`, `#uk-policy`, `#security`

---