---
layout: default
title: "Horizon Summary: 2026-11-26 (EN)"
date: 2026-11-26
lang: en
---

> From 34 items, 8 important content pieces were selected

---

1. [Aaronson Flags AI Math Milestone as Matrix Multiplication Exponent Hits 9/4](#item-1) ⭐️ 9.0/10
2. [1Password Discloses November 2026 Backend Code-Push Security Incident](#item-2) ⭐️ 8.0/10
3. [Anthropic's GRH Lean proof compressed from 17M to 76k lines](#item-3) ⭐️ 8.0/10
4. [Google's Cogentic agent posts six AI-written math papers on factoring and discrete logs](#item-4) ⭐️ 8.0/10
5. [OpenAI preprint disproves the polynomial Hirsch conjecture](#item-5) ⭐️ 8.0/10
6. [US Extends AI Chip Export Controls to Remote Cloud Access](#item-6) ⭐️ 8.0/10
7. [Minecraft Java RCE: Malicious Resource Pack Fonts Run Code on Windows](#item-7) ⭐️ 8.0/10
8. [FCC Partially Approves SpaceX's Gen2 Starlink Expansion Toward Gigabit Speeds](#item-8) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Aaronson Flags AI Math Milestone as Matrix Multiplication Exponent Hits 9/4](https://scottaaronson.blog/?p=10379) ⭐️ 9.0/10

Scott Aaronson published a short, expletive-titled blog post reacting to a claimed AI-assisted proof — reportedly from OpenAI — that the matrix multiplication exponent ω is 9/4 (2.25), linking to the paper and a Hacker News thread that drew over 1,300 points and 1,100 comments. If correct, lowering the best known upper bound from roughly 2.37 to 2.25 would be one of the largest theoretical improvements in decades for a core computational primitive, and it would strengthen the case that AI systems can produce genuinely novel axiomatic mathematics rather than merely retrieve known results. It also feeds broader debates about cryptographic assumptions and existential risk, because complexity breakthroughs can reshape what is considered computationally hard. The exponent ω is an asymptotic infimum, so an algorithm achieving 9/4 may carry enormous constant factors and remain impractical for real-world matrix sizes; the result still needs independent verification and peer review. Aaronson's post itself is mostly a pointer to the paper and discussion rather than a detailed technical exposition.

hackernews · Kotlopou · Nov 25, 19:11 · [Discussion](https://news.ycombinator.com/item?id=50646108)

**Background**: Matrix multiplication is a fundamental operation: multiplying two n×n matrices naively takes O(n^3) operations, and Strassen's 1969 algorithm began a long quest to lower the exponent ω in O(n^{ω+ε}). The best known upper bounds have hovered around 2.37 for years, while ω is conjectured to be 2 and cannot be below 2. AI systems have recently been used to discover new algorithms and mathematical identities, and Scott Aaronson is a theoretical computer scientist known for complexity theory and commentary on AI risk.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Computational_complexity_of_matrix_multiplication">Computational complexity of matrix multiplication - Wikipedia</a></li>
<li><a href="https://www.alphaxiv.org/abs/2611.matrix-multiplication-exponent-lower-bound">The Matrix Multiplication Exponent Is Nine Fourths | alphaXiv</a></li>
<li><a href="https://interestingengineering.com/culture/openai-exact-2-25-matrix-multiplication-exponent">OpenAI establishes exact 2.25 exponent for matrix multiplication</a></li>

</ul>
</details>

**Discussion**: Hacker News commenters mixed awe with skepticism: one argued that AI's success at 'analytic a priori' axiomatic math does not imply it will solve other fields or kill us all, while another doubted that labs have secret cryptographic breaks because such breakthroughs would be too large to keep quiet. Others said humans are biologically incapable of registering the appropriate level of alarm, and one invoked Bruno Latour's 'centers of calculation' to frame the moment.

**Tags**: `#AI`, `#mathematics`, `#existential-risk`, `#cryptography`, `#research-breakthrough`

---

<a id="item-2"></a>
## [1Password Discloses November 2026 Backend Code-Push Security Incident](https://1password.com/blog/update-on-nov-2026-security-incident) ⭐️ 8.0/10

1Password disclosed a November 2026 security incident in which malicious code was pushed to its backend services, according to the company's incident update. The disclosure has prompted discussion about how SaaS providers secure code deployment pipelines and what it means for password-manager trust. 1Password is a widely used password manager, so any compromise of its backend deployment path raises concerns for individual users and enterprises that rely on it. The incident highlights SaaS supply-chain risk: if attackers can push code into production services, the deployment pipeline itself becomes a critical security boundary. Community commenters noted that the announcement did not clearly explain whether branch protection rules were missing or bypassed, and some users wanted an explicit statement that encrypted vaults were not downloaded. The notice reportedly said a small number of users were in a particular state and were specifically notified, but the public discussion focused on the lack of clearer technical detail.

hackernews · lxhrstn · Nov 25, 17:18 · [Discussion](https://news.ycombinator.com/item?id=50644817)

**Background**: Supply-chain attacks target software developers and suppliers, often by compromising source code, build processes, or update mechanisms so that malicious code reaches legitimate users. 1Password markets a zero-knowledge architecture in which the service stores encrypted vault data it cannot decrypt without the user's master password. Even so, a backend code-push incident matters because production services and client-delivered code are part of the trust boundary around that encrypted data.

<details><summary>References</summary>
<ul>
<li><a href="https://1password.com/features/zero-knowledge-encryption">1Password Zero-Knowledge Encryption Protects Your Sensitive ...</a></li>
<li><a href="https://learn.microsoft.com/en-us/defender-endpoint/malware/supply-chain-malware">Supply chain attacks - Microsoft Defender for Endpoint</a></li>
<li><a href="https://www.paloaltonetworks.com/blog/sase/saas-supply-chain-security/">SaaS Supply Chain Security: Managing Risky Connected Apps ...</a></li>

</ul>
</details>

**Discussion**: Commenters treated the incident as a serious SaaS supply-chain lesson: tptacek argued that compromised employee laptops leading to code pushed to GitHub and deployed is the standard fact pattern for SaaS breaches. Others pressed 1Password for clearer answers on branch protection and asked for an explicit statement that encrypted vaults were not downloaded, while longtime users described maintaining local-only vaults out of concern for exactly this kind of incident.

**Tags**: `#security`, `#1password`, `#supply-chain`, `#saas`, `#incident-response`

---

<a id="item-3"></a>
## [Anthropic's GRH Lean proof compressed from 17M to 76k lines](https://github.com/lsernau/grh-lean) ⭐️ 8.0/10

A GitHub repository (lsernau/grh-lean) publishes a dramatically compressed Lean formalization of the Generalized Riemann Hypothesis derived from Anthropic's original proof, shrinking roughly 17 million lines down to about 76,000 — a 99.56% reduction. The repo also ships a more readable ~300k-line variant that separates "known math" from "new math" and includes human-readable documentation throughout. The compression suggests that LLM-generated formal proofs can be "golfed" down and annotated into something closer to human-digestible mathematics, which speaks directly to Terence Tao's concern that huge machine proofs may yield no insight. If proof size and readability can be engineered after the fact, AI-assisted formal verification becomes far more useful to working mathematicians rather than just kernel-checkable artifacts. The reduction is purely a refactoring and compression of the same underlying formal argument, so correctness still rests on Lean's kernel checking the final proof term rather than on human reading of the code. Commenters note that even the compressed version remains extremely dense — one linked file in grh-compact is cited as an example of code that is essentially unreadable without deep Lean expertise.

hackernews · nb-t · Nov 25, 21:48 · [Discussion](https://news.ycombinator.com/item?id=50648050)

**Background**: Lean is a proof assistant and functional programming language based on the calculus of constructions with inductive types; it lets mathematicians write proofs that a small trusted kernel mechanically verifies, with the shared Mathlib library supplying most of modern mathematics. The Generalized Riemann Hypothesis extends the Riemann Hypothesis — that all nontrivial zeros of the zeta function lie on the critical line Re(s)=1/2 — to Dirichlet and Dedekind L-functions, and it underpins many results about primes in arithmetic progressions. Recent months have seen a wave of AI systems producing Lean-checked proofs, raising a new question: a proof can be machine-verified while still being far too large for any human to understand.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Generalized_Riemann_hypothesis">Generalized Riemann hypothesis - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Lean_(proof_assistant)">Lean ( proof assistant ) - Wikipedia</a></li>
<li><a href="https://leanprover.github.io/theorem_proving_in_lean/introduction.html">1. Introduction — Theorem Proving in Lean 3 (outdated)...</a></li>

</ul>
</details>

**Discussion**: The Hacker News thread (422 upvotes, 212 comments) is broadly enthusiastic, with commenters highlighting the known-math versus new-math split and inline documentation as a major aid to digestion. Skeptics ask how realistic it is for a human to actually read and "grok" dense Lean code, while others frame the compression as a possible answer to Tao's worry that LLM-produced mega-proofs deliver no insight.

**Tags**: `#Lean`, `#formal-verification`, `#mathematics`, `#AI/ML`, `#proof-compression`

---

<a id="item-4"></a>
## [Google's Cogentic agent posts six AI-written math papers on factoring and discrete logs](https://github.com/google-research/google-research/tree/master/cogentic_research_papers) ⭐️ 8.0/10

Google Research added six papers to its public GitHub repository that were produced by Cogentic, a multi-agent harness for automated proof discovery built on Gemini 4, reportedly from a single prompt. The lead paper claims that every integer can be factored in proven expected time, with companion papers covering discrete logarithms and related topics. Integer factorization and discrete logarithms underpin the hardness assumptions behind RSA and Diffie-Hellman-style public-key cryptography, so any claimed improvement in these problems draws immediate scrutiny. The release also fuels a broader debate about AI systems contributing original results to pure mathematics rather than just assisting human mathematicians. Commenters note the factorization result does not actually beat the general number field sieve (GNFS), which has far better asymptotic complexity but rests on three unproven heuristics; Cogentic reportedly replaced the heuristic-dependent parts of GNFS while paying a significant complexity penalty. The claims are also described as not yet independently verified, and the repository itself offers limited detail beyond the paper links.

hackernews · rgwohlbold · Nov 25, 13:33 · [Discussion](https://news.ycombinator.com/item?id=50642086)

**Background**: Integer factorization is the problem of finding the prime factors of a large composite number, and the presumed difficulty of doing so for large numbers is what makes RSA encryption hard to break. The discrete logarithm problem plays the same role for Diffie-Hellman key exchange and elliptic-curve cryptography: no efficient classical algorithm is known for solving it in general. The general number field sieve is the best known classical factoring algorithm, but its complexity analysis depends on unproven conjectures about the distribution of smooth numbers. Cogentic is Google's multi-agent system in which frontier language models orchestrate the search for proofs of open research problems.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Integer_factorization">Integer factorization - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Discrete_logarithm">Discrete logarithm - Wikipedia</a></li>

</ul>
</details>

**Discussion**: Hacker News discussion (487 points, 349 comments) was largely skeptical about the practical cryptographic significance: one top commenter argued the result merely sidesteps GNFS's unproven heuristics at a large complexity cost, and that the bar for AI-generated proofs has been raised very high. Others saw it as part of a pattern of rapid AI-driven math discoveries, comparing it to AlphaGo's exploration of Go's search space, and one commenter cited rumors from credible people that this is "the tip of something bigger."

**Tags**: `#cryptography`, `#integer-factorization`, `#discrete-logarithms`, `#Google Research`, `#AI for math`

---

<a id="item-5"></a>
## [OpenAI preprint disproves the polynomial Hirsch conjecture](https://github.com/openai/math/blob/main/preprints/Superpolynomial-graph-diameter-of-simple-polytopes-November-24-2026/paper.pdf) ⭐️ 8.0/10

A preprint hosted in OpenAI's GitHub math repository (dated November 24, 2026) constructs simple polytopes whose graph diameter grows superpolynomially in the number of facets, thereby disproving the polynomial Hirsch conjecture. Because the diameter of a polytope lower-bounds the number of edge-pivots any simplex method must take, the result rules out the existence of a polynomial-time simplex algorithm. The Hirsch conjecture and its polynomial version were originally motivated by a practical puzzle: why does the simplex method, despite its exponential worst-case theory, work so well in practice on linear programs such as logistics and scheduling models. Settling the polynomial version closes a central question in polyhedral combinatorics and optimization theory, and redirects attention toward interior-point and smoothed-complexity explanations for simplex's real-world speed. The counterexample is built from simple polytopes — polytopes in which exactly d facets meet at every vertex — which is the most favorable class for the conjecture, so the disproof is as strong as possible. Crucially, the result says nothing about whether linear programs can be solved in polynomial time in general; it only excludes edge-following simplex variants, while interior-point methods remain polynomial-time.

hackernews · acossta · Nov 25, 17:34 · [Discussion](https://news.ycombinator.com/item?id=50644980)

**Background**: The Hirsch conjecture, stated by Warren M. Hirsch in a 1957 letter to George Dantzig, claimed that the edge-vertex graph of any polytope with n facets in d dimensions has diameter at most n − d. It survived for over fifty years until Francisco Santos gave a counterexample in 2010: a 43-dimensional polytope with 86 facets whose diameter exceeds 43. The polynomial Hirsch conjecture is the weaker surviving statement that the diameter is bounded by some fixed polynomial in n and d; Kalai and Kleitman proved a quasipolynomial bound around 1992. Polytopes here are the geometric feasible regions of linear programs, and the simplex algorithm moves between adjacent vertices along edges, so polytope diameter bounds the minimum number of pivots needed.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Polynomial_Hirsch_conjecture">Polynomial Hirsch conjecture</a></li>
<li><a href="https://en.wikipedia.org/wiki/Hirsch_conjecture">Hirsch conjecture - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Simplex_algorithm">Simplex algorithm - Wikipedia</a></li>

</ul>
</details>

**Discussion**: Commenters largely converged on framing the paper as a follow-up rather than a shock: one notes the original Hirsch conjecture was disproved in 2010 after 50+ years, making this "more of a mopping up result," while another stresses it implies no polynomial-time simplex algorithm. Others translated the abstraction into plain terms — linear constraints forming a multi-dimensional shape whose corners are feasible but suboptimal solutions, and polytope diameter as the worst-case number of edges between two cube vertices — with a side thread of speculation that AI will soon clear out most major open math problems, and a joke that breakthroughs now arrive as GitHub patch notes.

**Tags**: `#mathematics`, `#linear-programming`, `#complexity-theory`, `#polytopes`, `#optimization`

---

<a id="item-6"></a>
## [US Extends AI Chip Export Controls to Remote Cloud Access](https://t.me/zaihuapd/45361) ⭐️ 8.0/10

On November 16, the US Commerce Department issued an interim final rule that extends export controls on advanced AI chips and servers to remote access, closing the loophole of reaching controlled hardware through data centers in third countries. The rule additionally requires licenses for reexports of AI chips to Indonesia, Malaysia, Singapore, Thailand and Brazil. Until now, export controls mainly governed physical shipments, so foreign customers could effectively tap restricted compute by renting cloud instances abroad. By covering remote access and adding licensing requirements for five additional countries, the rule substantially widens the extraterritorial reach of US controls and could further narrow channels through which Chinese firms obtain advanced AI compute. The measure takes the form of an interim final rule, meaning it can take effect before the formal comment process is complete, and it was drafted with leadership from the Treasury Department and the National Security Council, signaling a whole-of-government push. As with earlier controls, enforcement will hinge on how cloud providers and server operators verify who is actually using the hardware remotely.

telegram · zaihuapd · Nov 25, 11:35

**Background**: US export controls on semiconductors are administered by the Bureau of Industry and Security (BIS), the agency within the Commerce Department that maintains the Export Administration Regulations and the lists of controlled items and destinations. Historically these rules were written around the physical export, reexport or transfer of hardware, which left a gap as AI workloads increasingly moved to rented cloud capacity in third countries. An interim final rule is a procedural device that lets an agency address an urgent gap immediately while still collecting public comments for possible revision.

**Tags**: `#AI chips`, `#export controls`, `#US policy`, `#data centers`, `#semiconductors`

---

<a id="item-7"></a>
## [Minecraft Java RCE: Malicious Resource Pack Fonts Run Code on Windows](https://github.com/bikini/minecraft2shell) ⭐️ 8.0/10

On November 22, a public proof-of-concept dubbed minecraft2shell showed that a crafted TrueType font delivered inside a server resource pack can trigger a native out-of-bounds write in FreeType 2.14.3 and earlier, allowing arbitrary code execution on a Windows client running Minecraft Java Edition 26.3. All Java Edition versions from 1.20.5 through 1.21.10, plus snapshots 26.1 to 26.4, are affected, while 1.20.4 and older releases and Bedrock Edition are not. Resource packs are downloaded and applied automatically when a player joins a multiplayer server, so any malicious or compromised server can take over a player's PC with essentially no interaction beyond connecting. With Mojang still shipping no patch, a very large installed base of Java Edition players remains exposed unless they manually disable server resource packs or install the community workaround. Mojang still bundles lwjgl-freetype 3.4.3 with no official fix; the community's m2sfix 1.0.0, published November 24, ships as a Java agent or mod and mitigates the flaw by turning off font hinting, the code path that reaches the FreeType out-of-bounds write. Players and server operators are advised to disable server resource pack permissions entirely until an official update lands.

telegram · zaihuapd · Nov 25, 12:46

**Background**: FreeType is an open-source font rasterization library used by nearly every platform to render TrueType and OpenType fonts, and Minecraft reaches it through LWJGL (Lightweight Java Game Library), which binds the native lwjgl-freetype library for text rendering. Font parsers are a classic attack surface because font files are complex, memory-unsafe binary formats that even contain a small bytecode interpreter for hinting, and previous FreeType flaws such as CVE-2025-27363 have been exploited in the wild. Minecraft's resource pack system lets servers push custom textures, sounds and fonts to clients, so a malicious font travels the same trusted path as ordinary gameplay assets.

<details><summary>References</summary>
<ul>
<li><a href="https://minecraft.wiki/w/Tutorial:Update_LWJGL_(Legacy)">Tutorial:Update LWJGL (Legacy) – Minecraft Wiki Tutorials/Update LWJGL (Legacy) – Minecraft Wiki /release/3.3.3/bin/lwjgl-freetype - LWJGL lwjgl3ify - Minecraft Mods - CurseForge Minecraft2Shell RCE in Minecraft Java Still Unpatched</a></li>
<li><a href="https://javadoc.lwjgl.org/org/lwjgl/util/freetype/FreeType.html">FreeType (LWJGL 3.4.2-snapshot)</a></li>
<li><a href="https://www.cybergensecurity.com/threat-watch/cve/CVE-2025-27363">CVE-2025-27363 FreeType Out-of-Bounds Write Vulnerability</a></li>

</ul>
</details>

**Tags**: `#Minecraft`, `#RCE`, `#security-vulnerability`, `#FreeType`, `#Java`

---

<a id="item-8"></a>
## [FCC Partially Approves SpaceX's Gen2 Starlink Expansion Toward Gigabit Speeds](https://t.me/zaihuapd/45375) ⭐️ 8.0/10

The U.S. Federal Communications Commission (FCC) announced on Friday that it partially approved SpaceX's application to expand its second-generation Starlink constellation, clearing the company to launch an additional 7,500 Gen2 satellites. That brings the authorized Gen2 total to 15,000 satellites, which will be allowed to operate in lower orbits to improve performance, with the FCC framing the decision as "a key step toward next-generation service" and attaching deployment milestones. This is one of the largest regulatory green lights yet for Starlink's next-generation network, and it moves satellite broadband closer to gigabit-class speeds that could rival terrestrial fiber and cable in underserved and rural markets. It also strengthens SpaceX's already dominant position in the low Earth orbit broadband market, raising competitive and orbital-debris concerns for rival operators and regulators. The approval is only partial: SpaceX received clearance for 7,500 of the roughly 30,000 Gen2 satellites it originally requested, and the FCC attached deployment deadlines that the company must meet to keep the authorizations. Lowering the satellites' altitude shortens the signal path to users, which is the main lever for cutting latency and raising throughput toward the 1 Gbps target.

telegram · zaihuapd · Nov 26, 04:45

**Background**: Starlink is SpaceX's broadband service delivered from a constellation of satellites in low Earth orbit (LEO), typically a few hundred kilometers up, rather than the much farther geostationary orbit used by traditional satellite internet. Because LEO satellites are so much closer, latency drops from hundreds of milliseconds to roughly 25–60 ms, though still above fiber's 11–14 ms. SpaceX's second-generation "Gen2" satellites, including the V2 and smaller V2 Mini variants, are designed to add far more capacity than the first-generation fleet, and SpaceX has sought permission for a constellation of nearly 30,000 spacecraft in total.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Starlink">Starlink - Wikipedia</a></li>
<li><a href="https://starlink.com/public-files/Gen2StarlinkSatellites.pdf">SECOND GENERATION STARLINK SATELLITES</a></li>
<li><a href="https://en.wikipedia.org/wiki/Low_Earth_orbit">Low Earth orbit - Wikipedia</a></li>

</ul>
</details>

**Tags**: `#Starlink`, `#SpaceX`, `#FCC`, `#satellite internet`, `#telecom regulation`

---