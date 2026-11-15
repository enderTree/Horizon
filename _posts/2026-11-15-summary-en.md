---
layout: default
title: "Horizon Summary: 2026-11-15 (EN)"
date: 2026-11-15
lang: en
---

> From 35 items, 3 important content pieces were selected

---

1. [SpaceX catches Starship booster with tower arms to close out Flight 15](#item-1) ⭐️ 9.0/10
2. [Lovable-built apps leaked passports and 200K+ private messages](#item-2) ⭐️ 8.0/10
3. [Google Project Zero to Shrink Vulnerability Disclosure Windows to 30 Days](#item-3) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [SpaceX catches Starship booster with tower arms to close out Flight 15](https://www.spacex.com/launches/starship-flight-15) ⭐️ 9.0/10

SpaceX successfully caught the Super Heavy booster of its Starship rocket with the launch tower's mechanical arms at the end of Flight 15, a maneuver the company has now demonstrated repeatedly as part of its test campaign. The flight concluded with the booster returning to the launch site and being secured in mid-air rather than landing on legs. Each successful catch moves SpaceX closer to a fully and rapidly reusable launch system, which is the core economic bet behind Starship: reusing both stages could cut the cost per kilogram to orbit far below expendable rockets and even below partially reusable vehicles like Falcon 9. That matters not only for Starlink and commercial payloads but for NASA's Artemis lunar lander plans and any future heavy-lift or Mars ambitions. The catch is performed by the tower's giant mechanical arms, nicknamed "chopsticks", which grab the booster as it descends back to the pad, eliminating landing legs and the associated mass. The remaining open questions are engineering ones: whether the vehicle's heat shield survives reentry well enough to allow rapid reuse, and what final mass fraction to orbit Starship will actually achieve, since the vehicle only reaches orbit with a partial propellant load and relies on orbital refueling for deep-space missions.

hackernews · ls612 · Nov 14, 21:22 · [Discussion](https://news.ycombinator.com/item?id=50500963)

**Background**: Starship is SpaceX's two-stage, fully reusable super-heavy launch vehicle: a 232-foot-tall booster called Super Heavy that lifts the stack off the pad, and a Starship upper stage that continues to orbit. Instead of landing on legs like Falcon 9, Super Heavy returns to the launch site and is caught in mid-air by arms on the launch tower, a design meant to save mass and enable fast turnaround. The program has progressed through a series of increasingly ambitious test flights since 2023, and SpaceX frames full reusability as the key to lowering launch costs through economies of scale.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/List_of_Starship_launches">List of Starship launches - Wikipedia</a></li>
<li><a href="https://www.bbc.com/news/live/cq0k683l3dz3t">SpaceX successfully catches part of Starship rocket on... - BBC News</a></li>
<li><a href="https://en.wikipedia.org/wiki/List_of_Super_Heavy_boosters">List of Super Heavy boosters - Wikipedia</a></li>

</ul>
</details>

**Discussion**: Commenters were overwhelmingly enthusiastic, framing Starship as "the Space Shuttle done right" — a fully reusable booster without solid rocket boosters and with the upper stage stacked on top rather than beside it, avoiding the failure modes behind Challenger and Columbia. Several noted the next milestones are proving the heat shield, catching both stages, and re-flying the same vehicles, while one commenter pointed out that a 100% reusable system beats a partially reusable one like Falcon 9 on cost even if the mass fraction to orbit is uncertain.

**Tags**: `#SpaceX`, `#Starship`, `#reusable rockets`, `#spaceflight`, `#aerospace engineering`

---

<a id="item-2"></a>
## [Lovable-built apps leaked passports and 200K+ private messages](https://www.crissyfield.de/research/lovable-en/) ⭐️ 8.0/10

A security researcher at Crissy Field published an incident report documenting how apps built with the AI app builder Lovable exposed sensitive data — including passport details and more than 200,000 private messages — because their Supabase Row-Level Security policies were insufficient. The disclosure, resubmitted to Hacker News after an initial quiet run, drew roughly 734 points and about 295 comments. This is a concrete, real-world example of the security risks of "vibe-coded" AI-generated applications, where users with no security background ship apps backed by real databases and real user data. It shifts the debate from abstract warnings about AI code generation toward hard questions about who is accountable — the app builder, the database provider, or the end user — across the whole AI app stack. The root cause was missing or misconfigured Row-Level Security in Supabase, so the public anon API key bundled into client-side code could read tables it should never have touched — meaning the attack required only inspecting network calls in a browser. Commenters also pointed to a longstanding Supabase default where RLS is not enforced until explicitly enabled, reportedly addressed in a change dated October 30 but possibly still applying to existing projects.

hackernews · armcat · Nov 14, 17:43 · [Discussion](https://news.ycombinator.com/item?id=50499017)

**Background**: Lovable is an AI app builder that generates full applications — interface, database schema, and logic — from natural-language prompts, and it commonly connects to Supabase, a Postgres-based backend-as-a-service. In Supabase, Row-Level Security (RLS) is the mechanism that decides which rows each user can read or write, and it must be enabled per table with separate policies for SELECT, INSERT, UPDATE and DELETE. When RLS is left off on a table in an exposed schema, the public API key shipped in every client becomes effectively a master key to that table.

<details><summary>References</summary>
<ul>
<li><a href="https://supabase.com/docs/guides/database/postgres/row-level-security">Row Level Security | Supabase Docs</a></li>
<li><a href="https://lovable.dev/">App & Website Builder | Build Software in Minutes | Lovable</a></li>
<li><a href="https://zyntari.com/guides/security-holes-in-ai-generated-apps">Lovable App Security Risks : What We Keep Finding — Zyntari</a></li>

</ul>
</details>

**Discussion**: The discussion was notably multi-sided: Lovable's Head of Security joined to say the root cause was insufficient RLS, that their pre-publish scanning and optional SAST scan are designed to catch exactly this and are free for all users, and that findings can be auto-fixed or block publishing. Other commenters shifted blame toward Supabase, arguing its historical choice to leave RLS off by default to ease onboarding is the real culprit, while others noted AI-generated apps are easy targets created in huge numbers whose users cannot judge the risk and called for deny-by-default databases and least-privilege APIs.

**Tags**: `#security`, `#AI-generated apps`, `#Supabase`, `#Row-Level Security`, `#data breach`

---

<a id="item-3"></a>
## [Google Project Zero to Shrink Vulnerability Disclosure Windows to 30 Days](https://projectzero.google/2026/11/disclosure-policy.html) ⭐️ 8.0/10

Google Project Zero announced a phased tightening of its disclosure policy, starting with a "Full 90" rule under which vulnerabilities are published 90 days after being reported to the vendor, moving to "Full 60" on February 2, 2027, and finally to "Full 30" on January 3, 2028. After that final step, Project Zero will publicly disclose flaws just 30 days after notifying the affected vendor. Project Zero's deadlines have historically reset industry norms — its original 90-day policy became a de facto standard adopted by many vendors and security teams — so compressing the window to 30 days could force sweeping changes to patch pipelines and release cadences across commercial software and open-source projects. Vendors that cannot ship fixes quickly will face public disclosure of unpatched flaws, shifting real risk onto end users. The schedule gives vendors roughly 14 months of lead time before the 30-day regime takes effect, and the quoted policy text does not spell out exceptions or extension mechanisms for complex or multi-party fixes. The change comes as Google increasingly uses automated and LLM-based bug-finding tools such as BigSleep, which can surface vulnerabilities faster than human patch cycles typically accommodate.

hackernews · hacb · Nov 14, 11:13 · [Discussion](https://news.ycombinator.com/item?id=50496051)

**Background**: Project Zero is a team of security analysts employed by Google, announced in July 2014, that hunts for zero-day vulnerabilities in widely used software and presses vendors to fix them. Vulnerability disclosure is governed by what is known as coordinated vulnerability disclosure (CVD), a process in which a researcher privately notifies the vendor, allows time for a patch, and then publishes details so users and defenders can assess their exposure. Project Zero's original 90-day deadline, introduced in 2015, became the informal industry benchmark, and many bug bounty programs pay researchers for reporting flaws privately rather than selling them to brokers.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Project_Zero">Project Zero - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Coordinated_vulnerability_disclosure">Coordinated vulnerability disclosure</a></li>
<li><a href="https://en.wikipedia.org/wiki/Bug_bounty_program">Bug bounty program</a></li>

</ul>
</details>

**Discussion**: Commenters were broadly skeptical that the tightened timeline is realistic, with one predicting that Ubuntu in particular "will need a LOT more time than that." Others argued disclosure should be immediate since Google's bug bounty already removes any financial incentive to sit on a flaw, while one commenter raised a subtler concern that disclosure pressure could be leveraged to push vendors toward adopting the reporting companies' own LLM-based tooling.

**Tags**: `#vulnerability disclosure`, `#Project Zero`, `#cybersecurity`, `#open source security`, `#bug bounty`

---