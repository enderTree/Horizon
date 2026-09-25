---
layout: default
title: "Horizon Summary: 2026-09-25 (EN)"
date: 2026-09-25
lang: en
---

> From 33 items, 2 important content pieces were selected

---

1. [F-Droid 2.0 launches as its biggest redesign in a decade](#item-1) ⭐️ 8.0/10
2. [Apple Pulls Advanced Data Protection in the UK, Creating Two-Tier iCloud Encryption](#item-2) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [F-Droid 2.0 launches as its biggest redesign in a decade](https://f-droid.org/2026/09/24/f-droid-2.0-a-new-chapter-for-android-freedom.html) ⭐️ 8.0/10

F-Droid released version 2.0 on September 24, 2026, its largest update in roughly ten years, rebuilding both the interface and much of the underlying code around three main areas: Discover, Search, and My Apps. The release follows 14 test builds and will roll out to users over the coming weeks. F-Droid is the flagship free-and-open-source app store for Android, so a major redesign affects a large privacy- and FOSS-focused user base that relies on it instead of Google Play. The release lands as Google moves to tighten restrictions on installing apps from third-party sources, making the sustainability of independent Android distribution a live question. The new client improves app discovery, categories, search and filtering, adds searching across app descriptions, categories and translated content, and strengthens search for Chinese, Japanese and Korean text, plus smoother install/update flows and background update checks. Notably, the F-Droid Privileged Extension is not yet supported in this release, and Android 6 support has been dropped.

hackernews · daveoc64 · Sep 24, 15:26 · [Discussion](https://news.ycombinator.com/item?id=49831968)

**Background**: F-Droid is a free and open-source app store and software repository for Android that functions much like Google Play, but it hosts only FOSS apps, requires no account, and flags "anti-features" such as advertising, user tracking or dependence on non-free software. Its website and server software are themselves open source, letting anyone run a private repository. The F-Droid Privileged Extension is an optional component that allows unattended, background installation and updates of apps, which historically required extra setup on custom ROMs like LineageOS.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/F-Droid">F-Droid</a></li>

</ul>
</details>

**Discussion**: Commenters welcomed the overhaul and the phase-out of the Privileged Extension, with one long-time GrapheneOS user saying the old F-Droid UI was so bad they switched to the alternative client Droid-ify. Others were critical of the new design ethos, pointing to a text-wrapping bug visible in the first screenshot and to a lack of visual dividers, tap affordances and scroll cues. Several users raised trust concerns about binaries from the F-Droid repository versus developers' official releases, and worried about what happens to F-Droid once Google locks down third-party installs next year.

**Tags**: `#F-Droid`, `#Android`, `#open-source`, `#app-store`, `#privacy`

---

<a id="item-2"></a>
## [Apple Pulls Advanced Data Protection in the UK, Creating Two-Tier iCloud Encryption](https://macanorak.com/two-tier-encryption-in-the-uk/) ⭐️ 8.0/10

Apple has withdrawn its Advanced Data Protection (ADP) feature for iCloud users in the United Kingdom, after receiving a legal order that would have required it to weaken the security architecture ADP depends on. Rather than build a backdoor, Apple removed the option entirely, reverting affected UK iCloud data to Standard Data Protection — a state the author of the linked post calls a "two-tier" encryption regime, since UK users who enabled ADP before it was pulled keep end-to-end encryption while everyone else does not. This is a landmark privacy and policy event: it shows how a government order can effectively force a global platform to offer weaker encryption to an entire national user base without ever publicly mandating a backdoor. It sets a precedent that other governments could follow, and it puts pressure on the long-standing assumption that major vendors will fight encryption demands in court rather than quietly degrade service. Per community analysis, 14 iCloud categories were already end-to-end encrypted by default, including iCloud Keychain and Health, and ADP raises the total to 23 categories; the categories that revert for UK users without ADP include iCloud Backup, Photos, Notes and iCloud Drive, which fall back to Standard Data Protection where Apple holds the keys and can respond to lawful legal process. One commenter disputes the framing that the 14 baseline categories were unaffected, arguing UK users' end-to-end-encrypted secrets can still be exposed under common-use circumstances.

hackernews · ReturnoftheHack · Sep 24, 10:39 · [Discussion](https://news.ycombinator.com/item?id=49828731)

**Background**: iCloud data is normally encrypted with keys that Apple stores in its data centers, which lets Apple help users recover data but also means Apple can be compelled to hand it over. Advanced Data Protection is an optional setting that switches most categories — including backups, photos and notes — to end-to-end encryption, so only the user's devices hold the keys. Apple introduced ADP in late 2022, and the UK order reportedly came under the Investigatory Powers Act, which can compel companies to assist with lawful interception and prohibits them from disclosing the demand.

<details><summary>References</summary>
<ul>
<li><a href="https://support.apple.com/en-us/108756">How to turn on Advanced Data Protection for iCloud - Apple Support</a></li>
<li><a href="https://support.apple.com/en-us/102651">iCloud data security overview - Apple Support</a></li>
<li><a href="https://macanorak.com/two-tier-encryption-in-the-uk/">Two-Tier Encryption in the UK</a></li>

</ul>
</details>

**Discussion**: Commenters are largely critical: one argues Apple had the courage to resist in 2015 but not today, pointing to mandatory age-confirmation/KYC screens at iPhone setup as evidence of a slippery slope, while another says the affair undermines the very reason they bought into Apple's closed ecosystem and hopes Apple will pull out of the UK market or cut off UK government users. A recurring concern is that governments can now demand backdoors while legally gagging the vendor, effectively outlawing end-to-end encryption by attrition.

**Tags**: `#encryption`, `#privacy`, `#apple`, `#uk-policy`, `#security`

---