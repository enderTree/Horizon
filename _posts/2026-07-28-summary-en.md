---
layout: default
title: "Horizon Summary: 2026-07-28 (EN)"
date: 2026-07-28
lang: en
---

> From 29 items, 8 important content pieces were selected

---

1. [Moonshot AI Releases 2.8 Trillion Parameter Kimi K3 Weights](#item-1) ⭐️ 9.0/10
2. [Fastjson 1.x High-Risk RCE Without Gadgets or AutoType](#item-2) ⭐️ 9.0/10
3. [SMIC Tests China's First Domestic DUV Lithography Machine](#item-3) ⭐️ 9.0/10
4. [Anthropic Advocates Mandatory Safety Testing for All Capable Models](#item-4) ⭐️ 8.0/10
5. [Missing Underscore in Username Leads to Wrongful 18-month Prison Term](#item-5) ⭐️ 8.0/10
6. [Paged Out #9 Released: Free Technical Zine](#item-6) ⭐️ 8.0/10
7. [Judge Rejects Google's DMCA Defense Against Scraping](#item-7) ⭐️ 8.0/10
8. [Solo Benchmark Finds All 6 Frontier LLMs Exhibit Left-Leaning Political Bias](#item-8) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Moonshot AI Releases 2.8 Trillion Parameter Kimi K3 Weights](https://simonwillison.net/2026/Jul/27/kimi-k3/#atom-everything) ⭐️ 9.0/10

Moonshot AI has released the weights for Kimi K3, a 2.8 trillion parameter open-weight model, on Hugging Face under a modified MIT license that imposes additional commercial restrictions for large enterprises. As the largest open-weight model ever released, Kimi K3 represents a major milestone in democratizing access to frontier AI capabilities, though its restrictive license may limit adoption by large commercial entities. The model weighs 1.56 TB on Hugging Face and is already available via OpenRouter from 7 providers at $3/million input tokens and $15/million output tokens; the K3 license requires a separate agreement for Model as a Service businesses with over $20 million annual revenue.

rss · Simon Willison · Jul 27, 23:39

**Background**: Kimi K3 is an open-weight model, meaning its trained parameters are publicly available, but it is not fully open-source due to licensing restrictions. At 2.8 trillion parameters, it surpasses previous large models and is designed for long-context programming, knowledge work, and complex reasoning tasks with agentic capabilities like tool use and web browsing.

<details><summary>References</summary>
<ul>
<li><a href="https://www.kimi.com/es-419/blog/kimi-k3">Kimi K3 Tech Blog: Open Frontier Intelligence</a></li>
<li><a href="https://huggingface.co/blog/ResterChed/kimi-k3-model-overview-mxfp4-quantization-open-wei">Kimi K3 Model Overview: 2.8T Parameters, MXFP4 Quantization, and What the Open Weights Mean for the Community</a></li>
<li><a href="https://www.tomshardware.com/tech-industry/artificial-intelligence/moonshot-releases-2-8-trillion-parameter-kimi-k3">China's 2.8-trillion-parameter Kimi K3 beats Claude Fable 5 in Frontend Code Arena benchmark— Moonshot AI delivers largest open-weight AI model ever, as China works around U.S. compute limits | Tom's Hardware</a></li>

</ul>
</details>

**Tags**: `#AI`, `#open-source`, `#large language models`, `#weights release`, `#Moonshot AI`

---

<a id="item-2"></a>
## [Fastjson 1.x High-Risk RCE Without Gadgets or AutoType](https://t.me/zaihuapd/42797) ⭐️ 9.0/10

Security researcher Kirill Firsov disclosed a high-risk remote code execution vulnerability in Fastjson versions 1.2.68 through 1.2.83 that does not require enabling autoType or any classpath gadgets. This vulnerability is critical because it affects all Fastjson 1.x users and can be exploited on JDK 8, 17, and 21. Since Fastjson 1.x is end-of-life, no official patch will be released, leaving upgrades to Fastjson 2 as the only mitigation. The vulnerability requires no special configuration (autoType disabled by default) and no pre-existing gadget chains, making it widely exploitable across different Java versions. The report suggests upgrading to Fastjson 2 or applying workarounds like disabling parse JSON with Feature.SupportAutoType.

telegram · zaihuapd · Jul 27, 10:31

**Background**: Fastjson is a popular Java library for JSON parsing and serialization, widely used in many applications. The autoType feature allows dynamic type resolution but has historically been a source of vulnerabilities. Gadget chains are sequences of classes that can be leveraged to execute arbitrary code during deserialization. This new vulnerability bypasses previous mitigations that depended on disabling autoType or removing dangerous gadgets.

<details><summary>References</summary>
<ul>
<li><a href="https://dev.to/tutorialboy/the-fastjson-auto-type-bypass-leads-to-rce-vulnerability-cve-2022-25845-19m0">The Fastjson “ Auto Type Bypass” leads to RCE... - DEV Community</a></li>
<li><a href="https://snyk.io/blog/serialization-and-deserialization-in-java/">Serialization and deserialization in Java | Snyk Blog | Snyk</a></li>

</ul>
</details>

**Tags**: `#security`, `#vulnerability`, `#fastjson`, `#rce`, `#java`

---

<a id="item-3"></a>
## [SMIC Tests China's First Domestic DUV Lithography Machine](https://t.me/zaihuapd/42800) ⭐️ 9.0/10

SMIC is trialing China's first domestically developed deep ultraviolet (DUV) lithography machine, built by Shanghai startup Yuliangsheng. The tool aims to produce 28nm chips and potentially 7nm chips using multi-patterning, with mass production expected by 2027. This development represents a critical step toward China's semiconductor self-sufficiency, reducing reliance on Dutch supplier ASML. If successful, it could reshape global chip supply chains by providing an alternative source for mature and advanced node lithography. Most components are domestically sourced, but some still rely on imports. SMIC is using the machine for 28nm production and exploring 7nm via multi-patterning, with potential low-yield 5nm capability. Industry insiders estimate it will take one to two years to achieve stable yields, with mass production possibly by 2027.

telegram · zaihuapd · Jul 27, 14:10

**Background**: Deep ultraviolet (DUV) lithography uses 193nm or 248nm light to pattern circuits on silicon wafers, enabling feature sizes down to about 50nm with single exposure. To reach smaller nodes like 7nm, manufacturers use multi-patterning, which splits a single layer into multiple exposures, effectively shrinking the printed features. Currently, China's most advanced chips rely on imported ASML DUV tools, while extreme ultraviolet (EUV) lithography, which uses 13.5nm light for finer patterns, is blocked by US export restrictions.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/DUV_lithography">DUV lithography</a></li>
<li><a href="https://semiengineering.com/knowledge_centers/manufacturing/patterning/multipatterning/">Multiple Patterning - Semiconductor Engineering</a></li>
<li><a href="https://en.wikipedia.org/wiki/Extreme_ultraviolet_lithography">EUV lithography - Wikipedia</a></li>

</ul>
</details>

**Tags**: `#semiconductor`, `#lithography`, `#china`, `#duv`, `#smic`

---

<a id="item-4"></a>
## [Anthropic Advocates Mandatory Safety Testing for All Capable Models](https://www.anthropic.com/news/position-open-weights-models) ⭐️ 8.0/10

Anthropic published a policy statement advocating mandatory safety testing for all sufficiently capable AI models, including both open-weights and closed models. Many in the community interpret this stance as effectively calling for a ban on open-weights models due to practical barriers like testing cost and access. This position could significantly impact the open-weights AI ecosystem, potentially limiting the release of capable open models if mandatory testing becomes law. It also highlights the growing tension between AI safety advocates and the open-source community over regulation and access. Anthropic explicitly states it has never advocated for a ban on open-weights models, but requires safety testing for all capable models. However, critics point out that the practical implementation—who conducts the test, costs, and potential administrative refusal—could effectively constitute a ban.

hackernews · surprisetalk · Jul 27, 22:03 · [Discussion](https://news.ycombinator.com/item?id=49076057)

**Background**: Open-weights models are AI models whose trained parameters (weights) are publicly released, allowing anyone to download and use them. Anthropic is an AI safety company that develops the Claude model series and has a Responsible Scaling Policy with tiered safety levels. The debate centers on whether government-mandated safety testing would disproportionately burden open-weights releases, effectively restricting them.

<details><summary>References</summary>
<ul>
<li><a href="https://hai.stanford.edu/ai-definitions/what-is-an-open-weight-model">What is an Open-Weight Model? - Stanford HAI</a></li>
<li><a href="https://www.anthropic.com/policy">AI policy \ Anthropic</a></li>
<li><a href="https://www.anthropic.com/responsible-scaling-policy">Anthropic’s Responsible Scaling Policy \ Anthropic</a></li>

</ul>
</details>

**Discussion**: The community comments are overwhelmingly critical, accusing Anthropic of hypocrisy and seeking to protect its business interests. Commenters argue that similar bans on chip sales to China have not worked, and that the testing requirements would disproportionately affect open models.

**Tags**: `#AI safety`, `#open-weights`, `#regulation`, `#Anthropic`, `#policy`

---

<a id="item-5"></a>
## [Missing Underscore in Username Leads to Wrongful 18-month Prison Term](https://arstechnica.com/tech-policy/2026/07/police-missed-one-underscore-and-sent-the-wrong-man-to-prison/) ⭐️ 8.0/10

A missing underscore in a Kik username caused police to arrest and convict an innocent man, resulting in an 18-month prison sentence before the error was discovered and his conviction was vacated. This case highlights how tiny technical errors in digital evidence can have devastating real-world consequences, and how confirmation bias among investigators can prevent the correction of such errors. It underscores the urgent need for better data integrity checks and human oversight in the justice system. The innocent man had no intimate images or evidence linking him to the crime, and police could not even show he accessed Kik during the relevant period. Despite this, he was convicted of luring a minor, providing explicit material, and child pornography possession.

hackernews · quantified · Jul 27, 22:10 · [Discussion](https://news.ycombinator.com/item?id=49076116)

**Background**: Kik is a messaging app that uses usernames. In this case, the perpetrator's username included an underscore that the innocent man's username lacked. Confirmation bias—the tendency to favor information that confirms one's preconceptions—led investigators to overlook this discrepancy and other exculpatory evidence. The case is a cautionary tale about the fallibility of human judgment in evaluating digital evidence.

**Discussion**: Commenters expressed outrage at the systemic failure, with many questioning why the man received no compensation for his lost income and reputational damage. Some proposed using LLMs to detect such discrepancies in legal cases, while others referenced classic stories like 'Computers Don't Argue' to illustrate the dangers of over-reliance on data without verification. The discussion also noted the cross-border aspect, as the victim was in the US and the defendant in Canada.

**Tags**: `#legal-system`, `#data-integrity`, `#wrongful-conviction`, `#confirmation-bias`, `#ethics`

---

<a id="item-6"></a>
## [Paged Out #9 Released: Free Technical Zine](https://pagedout.institute/download/PagedOut_009.pdf) ⭐️ 8.0/10

Issue #9 of Paged Out has been released as a free PDF, featuring deep technical articles and a beautifully designed layout. It continues the tradition of hacker zines like 2600 and Phrack, offering a high-quality, community-driven publication that appeals to technically curious readers. The PDF is available for free download; print editions are planned for future issues. The zine covers diverse topics such as C programming and subpixel rendering.

hackernews · laurensr · Jul 27, 14:22 · [Discussion](https://news.ycombinator.com/item?id=49070138)

**Background**: Paged Out is a free, community-driven technical magazine that focuses on deep, hacker-curious topics. It is designed to be visually appealing, similar to a modern 2600 or Phrack but with high-quality layout and illustrations.

**Discussion**: Commenters praised the zine for its humor (e.g., "Baby Steps in C"), technical depth (e.g., "The Subpixel Zoo"), and design. Some expressed interest in purchasing print editions. Comparisons were drawn to 2600 and Phrack.

**Tags**: `#programming`, `#hacking`, `#zine`, `#technical`, `#community`

---

<a id="item-7"></a>
## [Judge Rejects Google's DMCA Defense Against Scraping](https://www.techdirt.com/2026/07/27/judge-rejects-googles-attempt-to-dmca-its-way-out-of-being-scraped/) ⭐️ 8.0/10

A federal judge ruled that Google cannot use the DMCA to block third parties from scraping its search results, setting a significant legal precedent for web scraping and copyright law. This ruling clarifies that search engine results are not copyrightable compilations protected by the DMCA, potentially opening the door for more web scraping practices and affecting how companies protect their online data. The court rejected Google's argument that its search results qualify as a copyrighted database under the DMCA. Notably, Google had previously deprecated its search API, leaving third parties no official alternative but to scrape.

hackernews · cdrnsf · Jul 27, 18:15 · [Discussion](https://news.ycombinator.com/item?id=49073513)

**Background**: The DMCA (Digital Millennium Copyright Act) is a US law that criminalizes circumvention of technological measures protecting copyrighted works. Web scraping involves automated extraction of data from websites. Google's search results are ordered lists of links, and the company argued they were protected as a database under copyright law. This case (likely SerpAPI v. Google) tested whether scraping public search results constitutes copyright infringement.

**Discussion**: Community commenters largely supported the ruling, noting Google's hypocrisy in scraping the web while opposing scraping of its own results. Some pointed out that Google deprecated its search API, forcing reliance on third-party scrapers. Others raised technical points about database protection laws in the EU versus the US. A few commenters highlighted the practical importance of scraping for combatting advertising scams.

**Tags**: `#scraping`, `#DMCA`, `#Google`, `#legal`, `#copyright`

---

<a id="item-8"></a>
## [Solo Benchmark Finds All 6 Frontier LLMs Exhibit Left-Leaning Political Bias](https://www.reddit.com/r/MachineLearning/comments/1v8fnzw/evaluated_6_frontier_llms_gpt54_claude_sonnet_46/) ⭐️ 8.0/10

A solo evaluation of six frontier LLMs—GPT-5.4, Claude Sonnet 4.6, Claude Opus 4.7, Gemini Pro, Gemini Flash, and Grok 4.3—across eight bias benchmarks reveals that all models display left-leaning political bias, including Grok, which self-reports as right-leaning. The study also documents significant refusal rates on race-related questions, with GPT-5.4 refusing 20.3% of the time on BBQ race data. This finding is significant because it contradicts Grok's stated political orientation and suggests that even models claiming neutrality may harbor systematic biases. Understanding the direction and magnitude of bias in frontier LLMs is critical for deploying them in sensitive applications like content moderation, hiring, and political discourse. The evaluation used eight established bias/fairness datasets including WinoBias, BBQ (Race/Ethnicity), SeeGULL, OpinionsQA, cajcodes Political Bias, Hyperpartisan News, and Political Compass. The study is a solo, non-peer-reviewed project with no multi-run averaging and a single prompt template per task, which may limit generalizability.

reddit · r/MachineLearning · /u/marggggggggg · Jul 27, 22:37

**Background**: Bias benchmarks like BBQ (Bias Benchmark for QA) are designed to measure social biases in AI systems by presenting questions in ambiguous and disambiguated contexts. SeeGULL is a broad-coverage stereotype dataset covering identity groups across many countries. The Political Compass test is a common tool for mapping ideological positions on economic and social axes, and has been adapted to evaluate LLMs' political leanings.

<details><summary>References</summary>
<ul>
<li><a href="https://arxiv.org/abs/2110.08193">[2110.08193] BBQ: A Hand-Built Bias Benchmark for Question Answering</a></li>
<li><a href="https://github.com/google-research-datasets/seegull">GitHub - google-research-datasets/seegull: SeeGULL is a broad-coverage stereotype dataset in English containing stereotypes about identity groups spanning 178 countries across 8 different geo-political regions across 6 continents, as well as state-level identities within the US and India. · GitHub</a></li>
<li><a href="https://www.reddit.com/r/dataisbeautiful/comments/1jc7k1u/oc_political_compass_chart_for_all_major_ai_llm/">[OC] Political Compass chart for all major AI LLM models : ChatGPT, Claude, Gemini, Grok, DeepSeek. (Read submission comment for more details) : r/dataisbeautiful - Reddit</a></li>

</ul>
</details>

**Tags**: `#LLM bias`, `#fairness`, `#political bias`, `#frontier models`, `#evaluation`

---