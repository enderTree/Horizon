---
layout: default
title: "Horizon Summary: 2026-08-17 (EN)"
date: 2026-08-17
lang: en
---

> From 34 items, 8 important content pieces were selected

---

1. [Anthropic Reveals Claude System Prompts; Community Tracks Changes via Git Diffs](#item-1) ⭐️ 8.0/10
2. [Cloudflare Silently Injects Analytics Snippet Upon Nameserver Switch](#item-2) ⭐️ 8.0/10
3. [Stripe Buys AI Firm OpenRouter in Over $7B Deal](#item-3) ⭐️ 8.0/10
4. [Qwen 3.8 27B Impresses but Defaults to Wild Overthinking](#item-4) ⭐️ 8.0/10
5. [PJM's Modeling Mistake Wasted $12B of Ratepayer Money](#item-5) ⭐️ 8.0/10
6. [SSOG-Attention: Sum of Separable Gaussians Offers Sub-Quadratic Attention Alternative](#item-6) ⭐️ 8.0/10
7. [Revisiting ECA: Cross-Channel Interaction Hypothesis Questioned](#item-7) ⭐️ 8.0/10
8. [Anthropic Q2 Revenue Surges 14-Fold to Over $11.5 Billion](#item-8) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Anthropic Reveals Claude System Prompts; Community Tracks Changes via Git Diffs](https://platform.claude.com/docs/en/release-notes/system-prompts) ⭐️ 8.0/10

Anthropic's release notes for Claude system prompts expose the underlying instructions for Opus 4.8, Fable 5, and Mythos 5. Developer Simon Willison has republished these prompts as a git commit history, making it easier to spot changes between model versions. This is a rare public look at how a leading AI lab instructs its flagship models, giving developers and researchers visibility into prompt design and model behavior. It also fuels the broader conversation about transparency, context-window management, and whether longer system prompts help or hurt model performance. The system prompts are notably long, and one addition explicitly tells Claude that a prompt mentioning an image does not guarantee one exists, so Claude should verify. According to the community's diff, the most interesting addition relates to the first release of Claude Fable 5 and Claude Mythos 5; commenters also question why even Fable 5 carries a similar image-checking instruction.

hackernews · tosh · Aug 16, 12:48 · [Discussion](https://news.ycombinator.com/item?id=49319556)

**Background**: System prompts are special instructions prepended to a conversation that define an LLM's persona, rules, and context before user input. Anthropic's Claude family includes models such as Opus, Sonnet, Haiku, Fable, and Mythos, which differ in intelligence, speed, and cost. Diff-based tracking compares versions of text by highlighting added and removed lines, a standard technique for reviewing code and now model prompts. This context helps explain why the release notes and Simon Willison's git history attracted broad developer attention.

<details><summary>References</summary>
<ul>
<li><a href="https://promptengineering.org/system-prompts-in-large-language-models/">System Prompts in Large Language Models - Prompt Engineering</a></li>
<li><a href="https://en.wikipedia.org/wiki/Diff">diff - Wikipedia</a></li>
<li><a href="https://toloka.ai/blog/claude-models-explained/">Claude models explained: Opus, Sonnet, Haiku, and Fable Guide</a></li>

</ul>
</details>

**Discussion**: Community sentiment is largely positive about the transparency, with Simon Willison's git-based diffs praised as a practical tool for tracking prompt changes. However, several commenters express concerns: one alleges that the forum silently removes stories with negative AI implications, another argues that instructing Opus 4.8 to check whether an image actually exists is 'generic common sense' rather than a sign of intelligence, and another says the system prompts are far longer than warranted and may distract the model.

**Tags**: `#AI`, `#LLM`, `#Claude`, `#system prompts`, `#transparency`

---

<a id="item-2"></a>
## [Cloudflare Silently Injects Analytics Snippet Upon Nameserver Switch](https://news.ycombinator.com/item?id=49322107) ⭐️ 8.0/10

A Hacker News user reported that switching nameservers to Cloudflare to enable R2 bucket serving caused Cloudflare to silently inject its Web Analytics JavaScript snippet into their HTML-only, JS-free site. The injection only appeared in the analytics dashboard, where the user had to manually disable it after the fact, making it opt-out rather than opt-in. This highlights a growing concern over dark patterns by major infrastructure providers, where users are tracked by default unless they discover and disable the feature. It affects any Cloudflare customer who switches nameservers or uses Cloudflare's proxy, potentially skewing site analytics and raising privacy issues. The injected script is hosted at static.cloudflareinsights.com/beacon.min.js and includes a CF beacon token and a version number (e.g., 2024.11.0). Users can disable it by navigating to the Analytics dashboard, adding the site, and turning off the snippet; a Content-Security-Policy with script-src can also block it client-side.

hackernews · stagas · Aug 16, 17:49

**Background**: Cloudflare offers Web Analytics as a privacy-focused analytics product, but it appears the snippet is enabled by default when domains are added to Cloudflare. The original poster was using Cloudflare R2, an object storage service, and switched nameservers to serve a bucket from a custom subdomain. Because the site had no JavaScript, the injected script was unexpected and visible only by inspecting the dashboard. In a CDN setup, Cloudflare terminates HTTPS and can modify HTML responses before they reach the browser, which is how the injection occurs.

<details><summary>References</summary>
<ul>
<li><a href="https://developers.cloudflare.com/r2/buckets/public-buckets/">Public buckets · Cloudflare R2 docs</a></li>
<li><a href="https://notifire.in/infra/cloudflare-may-be-adding-code-to-your-website">Cloudflare Analytics Script Injected Without User Consent</a></li>
<li><a href="https://ideaverse.ai/blog/cloudflare-dns-change-triggered-hidden-analytics-script-injection-mswbamkg">Cloudflare DNS Change Triggered Hidden Analytics Script ...</a></li>

</ul>
</details>

**Discussion**: Commenters reacted with frustration, with one calling Cloudflare's behavior 'between GoDaddy and RyanAir in dark pattern usage.' Others offered technical mitigations, such as a CSP meta tag restricting script sources, while one user noted that the injection implies Cloudflare is terminating HTTPS connections and proxying traffic rather than merely providing DNS.

**Tags**: `#cloudflare`, `#privacy`, `#dark-patterns`, `#web-analytics`, `#security`

---

<a id="item-3"></a>
## [Stripe Buys AI Firm OpenRouter in Over $7B Deal](https://www.bloomberg.com/news/articles/2026-08-16/stripe-nears-deal-to-buy-ai-firm-openrouter-for-over-7-billion) ⭐️ 8.0/10

Stripe has clinched a deal to acquire OpenRouter, a unified AI model routing platform, for over $7 billion, as reported by Bloomberg in August 2026. The acquisition marks Stripe's entry into owning AI infrastructure rather than just processing payments. This deal positions Stripe to become the middleman for LLM API payments and routing, extending its expertise in abstracting financial rails to AI 'token rails.' It could reshape monetization of AI models and give Stripe significant control over AI payment volume. OpenRouter reportedly raised at a $1.3 billion valuation just months earlier, making the $7 billion exit a rapid jump. The deal comes as OpenAI switched its payment provider from Stripe to Adyen, with OpenRouter and OpenAI together representing roughly $100 billion in payment volume.

hackernews · zacharyozer · Aug 16, 20:31 · [Discussion](https://news.ycombinator.com/item?id=49323381)

**Background**: OpenRouter is a unified API marketplace that lets developers access hundreds of AI models from different providers through a single interface, handling routing, fallbacks, and unified billing. Stripe is a major financial infrastructure platform that processes online payments for internet businesses. By acquiring OpenRouter, Stripe aims to become the payment and routing layer for AI model usage. This fits the concept of 'payment rails' — the networks that move money between payers and payees.

<details><summary>References</summary>
<ul>
<li><a href="https://openrouter.ai/">OpenRouter</a></li>
<li><a href="https://www.codecademy.com/article/what-is-openrouter">What is OpenRouter? A Guide with Practical Examples | Codecademy</a></li>
<li><a href="https://en.wikipedia.org/wiki/Payment_rail">Payment rail - Wikipedia</a></li>

</ul>
</details>

**Discussion**: Commenters debated the valuation, with one noting $7B exceeds the market caps of Lyft, Dolby, and Alaska Airlines. Others saw it as a natural extension of Stripe's API expertise and a defensive move to capture AI payment volume after OpenAI moved to Adyen. Some praised OpenRouter's investors for the rapid return and emphasized switching costs and distribution as key moats.

**Tags**: `#AI`, `#Acquisitions`, `#Fintech`, `#OpenRouter`, `#Stripe`

---

<a id="item-4"></a>
## [Qwen 3.8 27B Impresses but Defaults to Wild Overthinking](https://simonwillison.net/2026/Aug/16/qwen-38-27b/) ⭐️ 8.0/10

Simon Willison reviewed Qwen 3.8 27B, an Apache-2.0-licensed 27B-parameter vision-capable LLM released by Alibaba's Qwen lab. He reports its self-benchmarks beat Qwen 3.6 27B and the closed-weight Qwen 3.7-Plus, but its default 'xhigh' reasoning effort causes extreme overthinking, such as taking 21 minutes to generate an SVG image. This release highlights rapid progress in open-weight models that run on consumer hardware, potentially challenging closed-weight rivals. Still, the default overthinking behavior raises usability concerns that could affect adoption for everyday tasks. The model defaults to a reasoning_effort of 'xhigh', with 'medium' and 'low' alternatives. Willison hit LM Studio's 8,192-token default context limit and had to load the 262,144-token maximum; a pelican-on-a-bicycle SVG used 22,276 reasoning tokens and 3,223 output tokens, taking 21 minutes. It is available as a 17GB Q4_K_M quantized GGUF in LM Studio.

rss · Simon Willison · Aug 16, 22:00

**Background**: Qwen 3.8 27B is from Alibaba's Qwen lab and licensed under Apache-2.0, allowing free use and modification. It is vision-capable, meaning it can process images, and its predecessor Qwen 3.6 27B was already strong for local use. Open-weight models differ from closed ones in that their weights are public, though training data and methods may remain undisclosed. Overthinking refers to models generating excessive chain-of-thought reasoning before answering, which can consume context and greatly slow responses.

<details><summary>References</summary>
<ul>
<li><a href="https://deepmind.google/research/publications/203490/">Towards Structural Understanding of LLM Overthinking</a></li>
<li><a href="https://www.pbs.org/newshour/science/whats-the-difference-between-closed-open‑source-and-open-weight-ai-a-researcher-explains">What's the difference between closed, open‑source and open-weight AI? A researcher explains | PBS News</a></li>

</ul>
</details>

**Tags**: `#AI`, `#LLM`, `#Qwen`, `#open-source`, `#model release`

---

<a id="item-5"></a>
## [PJM's Modeling Mistake Wasted $12B of Ratepayer Money](https://newsletter.semianalysis.com/p/12b-of-us-ratepayers-money-wasted) ⭐️ 8.0/10

SemiAnalysis reveals that a modeling error in PJM's capacity market has wasted roughly $12 billion of US ratepayer money, and warns PJM is at risk of repeating the same mistake in upcoming auctions. The waste raises electricity bills for millions of ratepayers across the PJM footprint and undermines trust in capacity-market design. It also highlights how seemingly technical modeling choices can have enormous financial consequences for the grid. The issue centers on the Variable Resource Requirement (VRR) curve and Net Cost of New Entry (Net CONE) parameters used in PJM's Reliability Pricing Model (RPM) auctions. Critics argue the flawed curve procures more capacity than needed, overpaying generators at ratepayer expense.

rss · Semianalysis · Aug 16, 22:27

**Background**: PJM operates the largest electricity grid in the US and runs an annual capacity market, the Reliability Pricing Model (RPM), to ensure enough power resources exist for future demand. Auctions use an administratively designed demand curve (the VRR curve) built on assumptions such as Net CONE. Periodic reviews by firms like Brattle have evaluated this curve, but SemiAnalysis argues the modeling mistake persists and is about to be repeated.

<details><summary>References</summary>
<ul>
<li><a href="https://www.pjm.com/markets-and-operations/rpm.aspx">PJM - Capacity Market (RPM)</a></li>
<li><a href="https://www.brattle.com/wp-content/uploads/2025/04/Sixth-Review-of-PJMs-Variable-Resource-Requirement-Curve.pdf">Sixth Review of PJM s Variable Resource Requirement Curve</a></li>
<li><a href="https://www.renewableenergyworld.com/power-grid/no-electricity-markets-are-not-broken-heres-why/">No, electricity markets are not broken – here’s why</a></li>

</ul>
</details>

**Tags**: `#energy grid`, `#modeling`, `#PJM`, `#infrastructure`, `#economics`

---

<a id="item-6"></a>
## [SSOG-Attention: Sum of Separable Gaussians Offers Sub-Quadratic Attention Alternative](https://www.reddit.com/r/MachineLearning/comments/1vpt6ay/ssogattention_sum_of_separable_gaussians_as_a/) ⭐️ 8.0/10

SSOG-Attention replaces scaled dot-product attention (SDPA) with a small number of learnable Gaussian atoms per head, steering them geometrically by the query token instead of computing all query-key similarities. This achieves O(N·√N·d) complexity and reportedly matches or outperforms SDPA on CIFAR-100 and ImageNet benchmarks. It addresses the O(N²·d) scaling bottleneck of standard attention, which limits transformer efficiency on long sequences and high-resolution images. If validated, SSOG could enable faster and more memory-efficient vision transformers at scale, with an open-source implementation available for community testing. The Gaussian atoms are factorized into a separable sum of Gaussians, enabling the reduced complexity while keeping content-based steering via small bounded nudges. The project provides a blog post and GitHub repository with experiments and ablations; it uses AI assistance for some code and text but remains author-endorsed.

reddit · r/MachineLearning · /u/4rtemi5 · Aug 16, 10:06

**Background**: Scaled dot-product attention (SDPA), introduced in 'Attention Is All You Need', computes pairwise similarities between all queries and keys, giving an O(N²·d) cost that becomes prohibitive for large inputs. A separable filter or kernel can be decomposed into lower-dimensional operations, which is why factorizing Gaussians reduces computation. SSOG applies this idea to attention by modeling each head's attention distribution as a sum of separable Gaussians rather than explicit query-key scoring.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/4rtemi5/ssog">GitHub - 4rtemi5/ssog: SSOG - Attention : Near-linear Visual-Attention...</a></li>
<li><a href="https://www.openai-hub.com/news/1620/">SSOG - Attention ... - OpenAI Hub</a></li>
<li><a href="https://uxlfoundation.github.io/oneDNN/dev_guide_graph_sdpa.html">Scaled Dot-Product Attention (SDPA) — oneDNN v3.14.0 documentation</a></li>

</ul>
</details>

**Tags**: `#attention`, `#efficient transformers`, `#sub-quadratic`, `#machine learning`, `#Gaussian`

---

<a id="item-7"></a>
## [Revisiting ECA: Cross-Channel Interaction Hypothesis Questioned](https://www.reddit.com/r/MachineLearning/comments/1vptaw9/revisiting_the_efficient_channel_attention_paper/) ⭐️ 8.0/10

A Reddit analysis argues that the central claim of the Efficient Channel Attention (ECA) paper, that cross-channel interaction is key, is conceptually flawed and not fully supported by experiments. The author demonstrates on chess tablebase data that ECA with kernel size k=3 performs similarly to k=1 (no cross-channel interaction) and to simple per-channel gating. This critique challenges a widely held assumption behind a highly cited (12k citations) attention mechanism, which could influence future research on efficient attention designs. It also highlights the importance of probing whether design rationales are actually validated by controlled experiments, rather than just final accuracy. The author used 6-piece chess endgame tablebases instead of image datasets, arguing that this provides an unbiased sample of the full underlying problem. ECA (k=3) achieved 96.68% test accuracy vs. SE's 96.17%, but ECA (k=1) reached 96.61% and a per-channel gate 96.65%, undermining the claim that cross-channel interaction is essential.

reddit · r/MachineLearning · /u/arkuto · Aug 16, 10:13

**Background**: The Squeeze-and-Excitation (SE) block recalibrates channel-wise features by squeezing the spatial dimensions and using a bottleneck to model channel dependencies. ECA-Net (CVPR 2020) avoids dimensionality reduction by applying a 1D convolution directly to the channel means with a small kernel, arguing that appropriate cross-channel interaction preserves performance with fewer parameters. However, the reddit author points out that 1D convolution over channels assumes a locality and ordering in the channel dimension that may not exist, analogous to applying a CNN to tabular data.

<details><summary>References</summary>
<ul>
<li><a href="https://arxiv.org/abs/1910.03151">[1910.03151] ECA-Net: Efficient Channel Attention for Deep Convolutional Neural Networks</a></li>
<li><a href="https://arxiv.org/abs/1709.01507">[1709.01507] Squeeze-and-Excitation Networks</a></li>

</ul>
</details>

**Tags**: `#attention`, `#efficient channel attention`, `#deep learning`, `#research critique`, `#machine learning`

---

<a id="item-8"></a>
## [Anthropic Q2 Revenue Surges 14-Fold to Over $11.5 Billion](https://www.cnbc.com/2026/08/15/anthropic-revenue-jumps-to-over-11point5-billion-in-q2-report.html) ⭐️ 8.0/10

Anthropic's preliminary Q2 revenue surpassed $11.5 billion, a year-over-year increase of more than 14 times, up from $787 million in the same period last year. The company also reported positive adjusted operating profit for the quarter, ahead of a potential IPO this fall. This financial milestone signals that leading AI labs can achieve rapid commercialization and profitability, not just heavy spending. It also sets the stage for what could be one of the most closely watched tech IPOs this year, affecting investor sentiment across the AI sector. The figures are preliminary and subject to adjustment, according to Bloomberg, citing documents. Sequential revenue growth was also steep: Q1 2026 revenue was $4.73 billion, meaning Q2 more than doubled quarter over quarter.

telegram · zaihuapd · Aug 16, 07:26

**Background**: Anthropic is a leading AI company, and its financial performance is closely watched in the AI industry. 'Adjusted operating profit' typically strips out one-time costs and stock-based compensation to show the profitability of ongoing operations, while 'preliminary revenue' means the figures may still be revised before final reporting. The company is reportedly preparing a large IPO that could launch this fall.

**Tags**: `#Anthropic`, `#AI industry`, `#Revenue`, `#IPO`, `#Business news`

---