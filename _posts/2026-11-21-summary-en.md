---
layout: default
title: "Horizon Summary: 2026-11-21 (EN)"
date: 2026-11-21
lang: en
---

> From 34 items, 11 important content pieces were selected

---

1. [Masullo Rushes Out 12-Year GRH Proof Hours After Anthropic's AI Claim](#item-1) ⭐️ 9.0/10
2. [Levent Alpöge claims proof of the Generalized Riemann Hypothesis, backed by a 15M-line Lean formalization](#item-2) ⭐️ 9.0/10
3. [Terry Tao Links Unforced Navier-Stokes Singularity to the Generalized Riemann Hypothesis](#item-3) ⭐️ 9.0/10
4. [GitHub repo claims finite-time blow-up for unforced Navier–Stokes](#item-4) ⭐️ 9.0/10
5. [Thinking Machines Releases Inkling 2 Mini Open-Weights Looped Transformer](#item-5) ⭐️ 8.0/10
6. [Language Model Rewrites Its Own Weights Without Gradients](#item-6) ⭐️ 8.0/10
7. [Nasdaq Wipes Out 2026 Gains as AI Sell-Off Hits Anthropic's Second Day](#item-7) ⭐️ 8.0/10
8. [CVE-2026-99312: KVM Flaw on AMD Hosts Lets Guest VMs Read Host Memory](#item-8) ⭐️ 8.0/10
9. [OpenAI Reportedly Claims Solution to Navier–Stokes Millennium Prize Problem](#item-9) ⭐️ 8.0/10
10. [Google Reportedly Launches Gemini 4 Neon for Coding, Knowledge Work and Research](#item-10) ⭐️ 8.0/10
11. [Microsoft demos RDMA over USB4 to pool multiple PCs for one local AI model](#item-11) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Masullo Rushes Out 12-Year GRH Proof Hours After Anthropic's AI Claim](https://math216.wordpress.com/2026/11/20/hurried-announcement-alessandro-masullo-grh/) ⭐️ 9.0/10

On November 20, 2026, Alessandro Maria Masullo released an incomplete, roughly 940-page manuscript claiming a proof of the Generalized Riemann Hypothesis (GRH) that he says he has worked on for almost 12 years, with the announcement posted hurriedly by AMS president Ravi Vakil within hours of Anthropic mathematician Levent Alpöge's claim to have proven the Riemann hypothesis with the Claude model. A correct proof of GRH would be one of the biggest results in mathematics, since it would settle the Riemann hypothesis as a special case and unlock vast consequences across number theory; the near-simultaneous human and AI claims have also turned the episode into a test case for how credit, priority and verification work in an era of machine-assisted mathematics. The draft is unverified and visibly unfinished — commenters note that section 1.1.1 of the 940-page manuscript is empty — but Stanford mathematician Brian Conrad, Masullo's doctoral thesis adviser, has reportedly been reviewing it closely for months and considers it to be looking good so far, with his feedback being incorporated.

hackernews · jasondavies · Nov 20, 18:33 · [Discussion](https://news.ycombinator.com/item?id=50579568)

**Background**: The Riemann hypothesis, posed by Bernhard Riemann in 1859, conjectures that all non-trivial zeros of the Riemann zeta function have real part 1/2, and it remains unproven despite being one of mathematics' most famous open problems. The Generalized Riemann Hypothesis extends the same statement from the zeta function to the much broader family of global L-functions, which encode arithmetic and geometric objects; a proof of GRH would therefore be strictly stronger and far-reaching than a proof of RH alone. Claims of this magnitude are normally withheld until peer review, so a rushed public posting is unusual and reflects concerns about establishing priority.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Generalized_Riemann_hypothesis">Generalized Riemann hypothesis - Wikipedia</a></li>
<li><a href="https://www.scientificamerican.com/article/dueling-claims-of-riemann-hypothesis-proofs-emerge/">Dueling claims of Riemann hypothesis proofs ... | Scientific American</a></li>
<li><a href="https://math216.wordpress.com/2026/11/20/hurried-announcement-alessandro-masullo-grh/">Hurried Announcement: Alessandro Masullo GRH</a></li>

</ul>
</details>

**Discussion**: Commenters were sharply divided between alarm and skepticism: some read the episode as evidence that intellectual work now depends on machines controlled by a handful of wealthy actors, others focused on the human cost of 12 years of work nearly being eclipsed by an AI announcement, and several questioned how a 940-page result could be kept private for so long. A few raised unsubstantiated speculation that the proof may have leaked to Anthropic through uploaded material, while others simply noted that neither claim has yet survived scrutiny.

**Tags**: `#mathematics`, `#Riemann Hypothesis`, `#AI`, `#research`, `#academia`

---

<a id="item-2"></a>
## [Levent Alpöge claims proof of the Generalized Riemann Hypothesis, backed by a 15M-line Lean formalization](https://alpo.ge/remark.pdf) ⭐️ 9.0/10

Mathematician Levent Alpöge posted a paper at alpo.ge/remark.pdf claiming a proof of the Generalized Riemann Hypothesis, accompanied by what commenters measured as roughly 1.3 GB and about 15 million lines of Lean code distributed as a 14-part tarball. The claim, reported by outlets such as Scientific American, has not yet been independently verified by the mathematical community. The Riemann Hypothesis is the most famous open problem in mathematics, and its generalization to Dirichlet and Dedekind zeta functions underpins vast swaths of analytic number theory, so a valid proof would restructure the field and instantly rank among the great achievements in mathematics. The fact that the argument arrives with a machine-checkable Lean development also makes this a test case for whether formal verification can settle — or at least sharply accelerate — the review of extraordinary claims. The formalization's sheer size (roughly 1.3 GB, ~15 million lines) is far beyond the scale of typical Lean projects, which makes human review impractical and shifts scrutiny onto whether the Lean statement actually encodes GRH and whether any axioms or unfinished steps remain. Commenters also linked a separate, hurried GRH announcement by Alessandro Masullo, and independent expert validation of Alpöge's argument is still pending.

hackernews · iamronaldo · Nov 20, 14:16 · [Discussion](https://news.ycombinator.com/item?id=50574968)

**Background**: The Riemann Hypothesis conjectures that all non-trivial zeros of the Riemann zeta function lie on the critical line with real part 1/2; the Generalized Riemann Hypothesis extends this to a broader family of L-functions, including Dirichlet L-functions and Dedekind zeta functions, with major consequences for how primes are distributed. Lean is a proof assistant developed principally by Leonardo de Moura, and its community-driven mathematical library mathlib lets mathematicians write proofs in a formal language that a small trusted kernel checks mechanically. A Lean formalization does not make a theorem true by itself — it guarantees that the stated claim follows from the axioms and library used — so the correctness of the formal statement and the absence of hidden assumptions are exactly what reviewers must examine.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Generalized_Riemann_hypothesis">Generalized Riemann hypothesis - Wikipedia</a></li>
<li><a href="https://leanprover-community.github.io/">Lean community</a></li>
<li><a href="https://www.scientificamerican.com/article/anthropic-mathematician-claims-to-prove-riemann-hypothesis-most-famous-problem-in-all-of-math/">Anthropic mathematician claims to prove... | Scientific American</a></li>

</ul>
</details>

**Discussion**: The Hacker News thread (over 2,500 points and 1,700 comments) mixes genuine awe with caution: one commenter reproduced the download and measured the enormous proof size, another resurfaced a 2014 Turkish interview in which a just-graduated Alpöge named solving the Riemann Hypothesis as his life goal. Others joked that breakthroughs are arriving so fast people are becoming numb to them, worried about AI-driven scientific acceleration and even about coordinating a pause, and expressed hope that such theoretical results will eventually translate into tangible benefits like better food, energy and medicine.

**Tags**: `#Riemann Hypothesis`, `#mathematics`, `#Lean theorem proving`, `#formal verification`, `#research breakthrough`

---

<a id="item-3"></a>
## [Terry Tao Links Unforced Navier-Stokes Singularity to the Generalized Riemann Hypothesis](https://terrytao.wordpress.com/2026/11/20/unforced-euler-singularity-unforced-navier-stokes-singularity-and-the-generalized-riemann-hypothesis/) ⭐️ 9.0/10

In a November 20, 2026 blog post, Terence Tao discussed results on unforced Euler singularity formation, unforced Navier-Stokes singularity formation, and their connection to the Generalized Riemann Hypothesis, noting that the first unforced Euler blow-up result had already been proved by OpenAI and announced the same day as a forced Navier-Stokes blow-up. The post sparked a 163-comment Hacker News thread in which commenters reported that the associated proof was accepted by two independent Lean kernels, suggesting no kernel bug was exploited. These are two of the most famous open problems in mathematics — the Navier-Stokes existence and smoothness question tied to a $1 million Millennium Prize, and the Riemann Hypothesis — so progress on either, especially machine-assisted progress, would reshape both fields. The discussion signals a broader shift in which AI systems contribute to frontier mathematical proof, raising urgent questions for researchers about verification, trust, and the future role of human mathematicians. Commenters noted that the argument reportedly draws on the full power of modern developments in the Langlands program and arithmetic geometry, and that independent verification across two Lean kernels is the key evidence that the proof is not an artifact of a kernel bug. Tao's post reportedly stops short of asserting significance, which some readers found frustrating given the magnitude of a Riemann Hypothesis claim.

hackernews · archon1410 · Nov 20, 17:21 · [Discussion](https://news.ycombinator.com/item?id=50578358)

**Background**: The Navier-Stokes existence and smoothness problem asks whether smooth solutions to the three-dimensional Navier-Stokes equations — the standard model of fluid flow — always exist, or whether they can blow up into singularities in finite time; the Euler equations are the inviscid (friction-free) special case, and 'unforced' means no external force term is applied. The Riemann Hypothesis, one of the most important conjectures in mathematics, states that the non-trivial zeros of the Riemann zeta function have real part 1/2, and the Generalized Riemann Hypothesis extends this claim to the broader family of global L-functions. Lean is an interactive theorem prover whose small trusted kernel checks proofs mechanically, which is why independent kernel verification matters so much for machine-generated mathematics.

<details><summary>References</summary>
<ul>
<li><a href="https://terrytao.wordpress.com/2026/11/20/unforced-euler-singularity-unforced-navier-stokes-singularity-and-the-generalized-riemann-hypothesis/">Unforced Euler singularity , unforced Navier - Stokes singularity , and...</a></li>
<li><a href="https://en.wikipedia.org/wiki/Navier–Stokes_existence_and_smoothness">Navier – Stokes existence and smoothness - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Generalized_Riemann_hypothesis">Generalized Riemann hypothesis - Wikipedia</a></li>

</ul>
</details>

**Discussion**: The thread mixes excitement with anxiety: some commenters describe feeling both thrilled and terrified about their careers, with one saying AI now appears to have essentially surpassed human mathematical intelligence and that it is only a matter of time before such capability spreads to other fields. A recurring counterpoint is the question of where genuinely new abstractions and concepts will come from — as one commenter asked, how do we create the next 'Langlands program' rather than exploit existing ones — while others criticized Tao for not commenting on the significance of a Riemann Hypothesis result.

**Tags**: `#mathematics`, `#fluid-dynamics`, `#Riemann-hypothesis`, `#AI-theorem-proving`, `#research`

---

<a id="item-4"></a>
## [GitHub repo claims finite-time blow-up for unforced Navier–Stokes](https://github.com/tristanbuckmaster/navier-stokes/) ⭐️ 9.0/10

A GitHub repository hosted under Tristan Buckmaster's account claims a finite-time blow-up result for the unforced three-dimensional Navier–Stokes equations. The claim drew 273 points and 86 comments on Hacker News, where it was treated as a potential Millennium Prize-level result. If valid, this would settle one of the Clay Mathematics Institute's Navier–Stokes existence and smoothness statements and mark a major breakthrough in partial differential equations. Because it targets the unforced equations, it is closer to the original physical problem than a construction that relies on a carefully designed external force. The claim is specifically for the unforced case; commenters distinguish it from OpenAI's earlier forced construction, which used a carefully designed external force. The repository claim still requires independent verification and peer review, since proofs of three-dimensional singularity formation are notoriously delicate.

hackernews · trotro · Nov 20, 15:34 · [Discussion](https://news.ycombinator.com/item?id=50576232)

**Background**: The Navier–Stokes equations describe the motion of viscous fluids. The existence and smoothness problem asks whether smooth solutions in three-dimensional space remain smooth for all time or can develop singularities; a finite-time blow-up is the latter case. In 2000 the Clay Mathematics Institute named this one of its Millennium Prize Problems, with separate forced and unforced clauses, where “unforced” means no external force is applied.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Navier–Stokes_existence_and_smoothness">Navier–Stokes existence and smoothness - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Navier–Stokes_priority_controversy">Navier–Stokes priority controversy - Wikipedia</a></li>
<li><a href="https://openai.com/index/navier-stokes-solution/">On the Navier–Stokes Millennium Prize Problem | OpenAI</a></li>

</ul>
</details>

**Discussion**: Commenters reacted with excitement and disbelief, with one noting that an unforced Navier–Stokes blow-up plus a claimed generalized Riemann Hypothesis on the same day would set a new standard for mathematics. Several focused on the forced-versus-unforced distinction and called the unforced version more “realistic,” while others discussed OpenAI's earlier forced result, rumors of an Anthropic Millennium Prize result, and the resulting priority drama around Buckmaster and Alpoge. Some asked whether a numerical simulation could show the blow-up in real time and give intuition for where the equations depart from reality.

**Tags**: `#Navier-Stokes`, `#fluid dynamics`, `#PDEs`, `#Millennium Prize`, `#mathematical breakthrough`

---

<a id="item-5"></a>
## [Thinking Machines Releases Inkling 2 Mini Open-Weights Looped Transformer](https://thinkingmachines.ai/news/inkling-2-mini/) ⭐️ 8.0/10

Thinking Machines has released Inkling 2 Mini, an open-weights looped-transformer model trained end-to-end in nvfp4, and early reports say it matches Qwen3-27B-class models while running efficiently on local hardware. This is significant because looped architectures are still rare among openly available models and could point toward more parameter-efficient designs, while also giving local-inference users a new option that works with llama.cpp and GGUF tooling. The model was trained end-to-end in nvfp4 rather than quantized only after training, and early users report about 27 tokens/s on a Ryzen 395 with llama.cpp Vulkan and about 10 tokens/s on a 32 GB M1 Pro with a q4 XL quant. Community notes point to several unmerged llama.cpp PRs and a small patch that yields about a 30% speedup, while a simple CSV-sorting coding test succeeded but a coin-identification test failed after long babbling.

hackernews · jasondavies · Nov 20, 20:12 · [Discussion](https://news.ycombinator.com/item?id=50581260)

**Background**: A looped transformer reuses one transformer block across repeated passes, aiming to simulate greater depth and reasoning ability without growing parameter count as much as a conventional deep stack. NVFP4 is a 4-bit floating-point format that micro-scales groups of weights, often 16 at a time, to compress models while keeping activations at higher precision for numerical stability. Most open-weight releases are trained in higher precision and quantized afterward, so end-to-end nvfp4 training is a notable distinction.

<details><summary>References</summary>
<ul>
<li><a href="https://thinkingmachines.ai/news/inkling-2-mini/">Introducing Inkling 2 Mini - Thinking Machines Lab</a></li>
<li><a href="https://www.emergentmind.com/topics/looped-transformer-architecture">Looped Transformer Architecture</a></li>
<li><a href="https://unsloth.ai/docs/models/qwen3.8">Qwen3.8 - How to Run Locally | Unsloth Documentation</a></li>

</ul>
</details>

**Discussion**: Commenters are largely excited, calling the model 'bonkers good' if its benchmarks hold and predicting that more open models may adopt looped architectures; several share concrete local-inference numbers, including ~27 tok/s on Ryzen 395 with Vulkan and ~10 tok/s on a 32 GB M1 Pro. They also point to specific llama.cpp PRs and a small patch for ~30% speedup, while some voice safety and interpretability concerns about looped architectures becoming widely available. Test reports are mixed: one user's simple CSV-sorting task was solved well, but a coin-identification stress test failed after roughly 12,000 tokens.

**Tags**: `#LLM`, `#open-weights`, `#looped-transformers`, `#local-inference`, `#quantization`

---

<a id="item-6"></a>
## [Language Model Rewrites Its Own Weights Without Gradients](https://arxiv.org/abs/2611.21885) ⭐️ 8.0/10

A new arXiv paper (2611.21885) claims to show for the first time that a language model can rewrite its own weights through its own reasoning, improving accuracy across eight consecutive sessions without gradients or conventional training. If reproducible, self-rewriting would let deployed models repair or improve themselves without costly retraining, but it also blurs the line between inference and training and raises serious AI-safety questions about autonomous self-modification. The model reportedly tests candidate edits on practice problems and keeps only those that work; however, commenters note that the only self-improvement identified was shortening its reasoning traces to avoid token limits, and prior work such as Weight-Space Programming and Google's Sleep framework already explored related weight-editing ideas.

hackernews · lwhsiao · Nov 20, 16:29 · [Discussion](https://news.ycombinator.com/item?id=50577265)

**Background**: Large language models are normally trained once and then frozen; changing their behavior usually requires fine-tuning with gradient-based optimization or adding prompts and inference-time scaffolding. Weight editing is an alternative that directly modifies a model's parameters, and recent research has shown that frontier LLMs can read and write the weights of small neural networks without running a gradient loop. This paper extends that line of work by asking whether a model can edit its own weights through reasoning rather than external training.

<details><summary>References</summary>
<ul>
<li><a href="https://arxiv.org/abs/2611.21885">[2611.21885] Language Models Can Rewrite Their Own Weights</a></li>
<li><a href="https://rikiyat.github.io/blog/weight-space-programming/">Sparks of Weight -Space Programming: LLMs can natively read & write...</a></li>
<li><a href="https://notesbylex.com/weight-space-programming">Weight -Space Programming - NotesByLex.com</a></li>

</ul>
</details>

**Discussion**: The 116-comment discussion is broadly intrigued but skeptical: commenters cite Google's Sleep framework and Weight-Space Programming as prior art, question whether 'no training' is an honest framing since the process still selects working edits, and warn that autonomous weight editing could be used to abliterate safety-relevant activations.

**Tags**: `#ai-safety`, `#self-improving-models`, `#llm-research`, `#weight-editing`, `#machine-learning`

---

<a id="item-7"></a>
## [Nasdaq Wipes Out 2026 Gains as AI Sell-Off Hits Anthropic's Second Day](https://www.theguardian.com/business/2026/nov/20/global-stock-markets-slump-anthropic-ipo-ai-sell-off) ⭐️ 8.0/10

On November 20, 2026, a broad sell-off in AI and semiconductor stocks erased Nasdaq's year-to-date gains and pushed major U.S. indexes into correction territory, while Anthropic shares fell on their second trading day after a record-breaking IPO and at times hovered near the IPO price. The reversal shows how much of the 2026 market rally depended on AI optimism, and Anthropic's reception is being read as a key signal for other cash-hungry AI companies—especially OpenAI, which has postponed its own IPO to 2027—considering whether public markets will keep funding huge valuations. Anthropic shares had closed up 17% on their record-breaking debut but fell almost 5% in after-market trading and remained only about 11% above the IPO price; the sell-off also hit AI and semiconductor names, with the Dow and S&P 500 entering correction territory alongside the Nasdaq plunge.

hackernews · cdrnsf · Nov 20, 13:29 · [Discussion](https://news.ycombinator.com/item?id=50574383)

**Background**: An IPO is the process by which a private company sells shares to the public and lists on a stock exchange, giving it access to large-scale capital and giving early investors a market price. Nasdaq is a U.S. stock exchange heavily weighted toward technology companies, so swings in AI-related stocks can move the index sharply. A correction generally refers to a decline of at least 10% from a recent peak.

<details><summary>References</summary>
<ul>
<li><a href="https://www.theguardian.com/technology/2026/nov/20/anthropic-ipo-historic-stock-market-debut-key-takeaways-what-next-for-ai">Anthropic ’s historic stock market debut: key... | The Guardian</a></li>
<li><a href="https://www.ft.com/content/c7ad2e0c-efd1-40c2-a5a8-819ced8acf5b?syn-25a6b1a6=1">Tech stocks fall after Anthropic IPO</a></li>
<li><a href="https://www.upi.com/Top_News/US/2026/11/20/stocks-dow-jones-nasdaq-correction-territory/1061795214998/">Dow, S&P 500 enter correction as Nasdaq plunges in AI ... - UPI</a></li>

</ul>
</details>

**Discussion**: Commenters debated whether cheap AI automation could shrink measured GDP in high-wage industries, warned that Anthropic and broader tech valuations rest on "hopes and dreams" rather than fundamentals, and questioned whether the weak reception could derail OpenAI's IPO plans. Others framed the moment as a concentration problem—progress that "strip-mines all of human knowledge" for a small group—while one commenter noted the surreal coincidence of a record IPO, a market slump, and a claimed Riemann hypothesis solution.

**Tags**: `#AI industry`, `#stock market`, `#Anthropic`, `#IPO`, `#tech valuations`

---

<a id="item-8"></a>
## [CVE-2026-99312: KVM Flaw on AMD Hosts Lets Guest VMs Read Host Memory](https://thehackernews.com/2026/11/new-linux-kvm-flaw-cve-2026-99312-lets.html) ⭐️ 8.0/10

A Linux kernel KVM vulnerability tracked as CVE-2026-99312 was disclosed on November 18, 2026, after researchers demonstrated reading roughly 127 GB of a DigitalOcean server's memory from inside a guest virtual machine. Upstream fixes shipped in stable kernels including 7.3.5, but distribution kernels such as Debian and Ubuntu had not yet been patched at the time of reporting. The flaw breaks the isolation boundary that multi-tenant cloud providers depend on, so on a shared AMD host the leaked memory can include other customers' virtual machines. Because KVM is the default hypervisor for most Linux-based cloud infrastructure, unpatched AMD hosts with nested virtualization enabled carry real exposure. The bug is described as a stale pointer in KVM that traces back to an earlier security fix, and it only affects hosts with AMD processors where nested virtualization is enabled. Administrators can mitigate by disabling nested virtualization until patched kernels are available, and many cloud providers surveyed were unaffected precisely because they do not enable that feature on AMD hardware.

telegram · zaihuapd · Nov 20, 14:23

**Background**: KVM is the hypervisor built directly into the Linux kernel, letting one physical machine run many isolated virtual machines. Nested virtualization means running a hypervisor inside a guest VM, which on AMD hardware relies on AMD-V/SVM extensions and nested paging so the outer hypervisor can trap and emulate the inner one's instructions. That extra emulation layer adds complexity to the guest-host boundary, and a mistake there can turn a read of virtualized state into a read of host memory. Kernel fixes typically reach users only after each Linux distribution rebases its own kernel, which is why upstream patches and distro availability diverge.

<details><summary>References</summary>
<ul>
<li><a href="https://thehackernews.com/2026/11/new-linux-kvm-flaw-cve-2026-99312-lets.html">Linux KVM Flaw CVE - 2026 - 99312 Lets Guest VMs Access Host...</a></li>
<li><a href="https://www.terra.security/blog/kvm-guest-to-host-escape">KVM Guest-to-Host Escape | Terra Security Research</a></li>
<li><a href="https://www.digitalocean.com/blog/cve-2026-99312-kvm-patch">Virtualization , Responsible Disclosure, and CVE - 2026 - 99312</a></li>

</ul>
</details>

**Tags**: `#KVM`, `#CVE`, `#Linux security`, `#virtualization`, `#AMD`

---

<a id="item-9"></a>
## [OpenAI Reportedly Claims Solution to Navier–Stokes Millennium Prize Problem](https://t.me/zaihuapd/45265) ⭐️ 8.0/10

A Telegram channel reports that OpenAI announced a resolution of the Navier–Stokes existence and smoothness problem — one of the seven Clay Millennium Prize Problems — releasing both a paper and a Lean formal verification. According to the post, the proof was produced by a massive internal system using roughly 10,000 parallel agents, 2.7 million messages, and about 130 billion output tokens, and OpenAI reportedly said it has no intention of claiming the prize. If verified, this would be the first time an AI system produced a resolution to a Millennium Prize Problem, marking a potential turning point for AI-driven mathematics and for formal verification as a credibility standard. It would also reshape a core question in fluid dynamics, and the reported scale of the multi-agent run would be a notable data point for large-scale agentic systems. The reported proof allegedly shows that initially smooth fluid flows can develop a singularity in finite time, which corresponds to the finite-time breakdown side of the Clay problem rather than the global-regularity side. Details such as the agent counts and the claim that OpenAI initially believed Anthropic's Levent Alpöge and NYU's Tristan Buckmaster had also solved it read oddly, and the claim currently rests on a single Telegram channel with no independent corroboration or peer review.

telegram · zaihuapd · Nov 20, 15:29

**Background**: The Navier–Stokes equations describe the motion of viscous fluids, and the Clay Mathematics Institute's Millennium Prize problem asks whether smooth solutions to the three-dimensional incompressible equations always exist for all time, or whether they can break down in finite time — a resolution must establish one of these two outcomes. Lean is a free, open-source proof assistant and functional programming language based on dependent type theory, in which mathematical proofs can be written and machine-checked, so a Lean formalization of a proof would in principle allow anyone to verify it mechanically.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Navier–Stokes_existence_and_smoothness">Navier – Stokes existence and smoothness - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Lean_(proof_assistant)">Lean (proof assistant) - Wikipedia</a></li>
<li><a href="https://navier-stokes.org/navier-stokes-existence-and-smoothness/">Clay Navier - Stokes Problem : Official Statement Explained</a></li>

</ul>
</details>

**Tags**: `#AI research`, `#mathematics`, `#Navier-Stokes`, `#Lean formal verification`, `#LLM agents`

---

<a id="item-10"></a>
## [Google Reportedly Launches Gemini 4 Neon for Coding, Knowledge Work and Research](https://t.me/zaihuapd/45267) ⭐️ 8.0/10

Google has reportedly released a new model called Gemini 4 Neon, positioned for fast end-to-end execution of complex software engineering, knowledge work and research workflows, and made available to developers, enterprises and Google AI Pro/Ultra subscribers. The listed pricing is $3 per million input tokens ($0.15 for cached input) and $15 per million output tokens, with a 1 million token context window. If the benchmark claims hold up, Google would be placing a model at the very top of agentic coding leaderboards while undercutting rivals on price, which directly affects developers choosing which agent or model to build long-running coding and research pipelines on. It also signals that competition in 2026 has shifted from raw chat quality toward reliable execution of multi-step, tool-using tasks. The post claims Gemini 4 Neon tops the Artificial Analysis Coding Agent Index at 58.6 and ranks third overall on the Intelligence Index at its xhigh setting with 61 points, with a Terminal-Bench result that is cut off in the source text. Notably, the item comes from a short Telegram post with no link to an official Google announcement, model card or independent verification, so the specs and scores should be treated as unconfirmed.

telegram · zaihuapd · Nov 21, 01:09

**Background**: The Artificial Analysis Coding Agent Index is a composite benchmark score assembled from FrontierCode-AA 2.0, Terminal-Bench 4.1 and SWE-Atlas-QnA-AA, and the site itself advises reading it alongside the per-evaluation breakdowns rather than as a single verdict. Terminal-Bench measures whether an AI agent can actually operate a computer through a terminal to complete real tasks, which is why it has become a common yardstick for coding agents. Prompt caching, meanwhile, lets an API reuse previously processed context; across tracked LLM APIs a cache hit typically costs 2%–25% of the standard input rate (median around 10%), so the reported $0.15 versus $3 input price works out to roughly a 95% discount.

<details><summary>References</summary>
<ul>
<li><a href="https://artificialanalysis.ai/agents/coding-agents">AI Coding Agent Benchmarks & Leaderboard | Artificial Analysis</a></li>
<li><a href="https://www.tbench.ai/">TERMINAL - BENCH</a></li>
<li><a href="https://llmcostlab.com/articles/llm-prompt-caching-prices-compared-2026/">LLM Prompt Caching Prices Compared (2026) | LLM Cost Lab</a></li>

</ul>
</details>

**Tags**: `#Gemini`, `#Google`, `#LLM`, `#software engineering`, `#AI benchmarks`

---

<a id="item-11"></a>
## [Microsoft demos RDMA over USB4 to pool multiple PCs for one local AI model](https://videocardz.com/newz/microsoft-brings-rdma-over-usb4-to-windows-allowing-multiple-pcs-to-run-one-local-ai-model) ⭐️ 8.0/10

Microsoft released a Windows developer preview of RDMA over USB4, letting multiple PCs share registered memory regions and GPU compute over an ordinary USB4 cable to run a single local AI model without dedicated NICs or switches. In the demo, three AMD Ryzen AI Max+ 395 machines ran Qwen3-235B-A22B at 4-bit quantization at roughly 18.5 tokens per second, with the preview rolling out through Windows Insider. This turns cheap, ubiquitous USB4 ports into an interconnect for distributed local inference, letting enthusiasts and small teams pool hardware they already own instead of buying a single machine with enough VRAM for large models. It signals that Windows is building out a host-to-host fabric layer, which could make consumer-grade distributed AI inference a standard capability rather than a hack. RDMA over USB4 builds on Windows 11's existing host-to-host USB4 networking: each PC forms its own USB4 domain and the Windows connection manager sets up a peer-to-peer tunnel so data moves directly between registered memory regions, bypassing copies through the CPU. The preview is currently limited to specific AMD hardware, and the ~18.5 token/s figure comes from a 4-bit quantized 235B-parameter MoE model split across three machines, so it is a feasibility demo rather than a performance benchmark.

telegram · zaihuapd · Nov 21, 06:13

**Background**: RDMA (Remote Direct Memory Access) lets one machine read and write another machine's memory without involving the remote CPU or operating system, and it has long been the backbone of high-performance clusters, but traditionally over InfiniBand or specialized Ethernet NICs. USB4 (which shares its underpinnings with Thunderbolt 3/4) offers high-bandwidth, low-latency PCIe tunneling over a plain cable, making it a plausible carrier for RDMA on consumer hardware. Large language models are typically limited by how much memory they fit in, so pooling VRAM across machines is a way to run models far bigger than any single GPU or unified-memory APU can hold; quantization to 4-bit shrinks the weights so a 235B-parameter model fits in a few machines, and Qwen3-235B-A22B is a mixture-of-experts model that activates only about 22B parameters per forward pass, which keeps compute per token manageable.

<details><summary>References</summary>
<ul>
<li><a href="https://www.techpowerup.com/355062/microsoft-brings-rdma-over-usb4-to-windows-11-for-daisy-chained-pcs">Microsoft Brings RDMA over USB 4 to Windows 11 for... | TechPowerUp</a></li>
<li><a href="https://www.guru3d.com/story/microsoft-previews-usb4-links-that-let-windows-pcs-pool-memory-and-gpu-resources/">Microsoft previews USB 4 links that let Windows PCs pool memory ...</a></li>
<li><a href="https://writingmate.ai/models/qwen/qwen3-235b-a22b">Qwen: Qwen 3 235 B A 22 B - AI Model Details | Writingmate</a></li>

</ul>
</details>

**Tags**: `#RDMA`, `#USB4`, `#local AI`, `#Windows`, `#distributed inference`

---