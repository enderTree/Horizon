---
layout: default
title: "Horizon Summary: 2026-07-04 (EN)"
date: 2026-07-04
lang: en
---

> From 47 items, 9 important content pieces were selected

---

1. [EU Parliament Spyware Investigator Hacked with Pegasus](#item-1) ⭐️ 9.0/10
2. [SearXNG: A privacy-focused metasearch engine for AI agents](#item-2) ⭐️ 8.0/10
3. [Wordgard: New Rich-Text Editor by ProseMirror Creator](#item-3) ⭐️ 8.0/10
4. [CDD Recovers Verbatim Finetuning Data from Logits Alone](#item-4) ⭐️ 8.0/10
5. [H64LM: A 249M MoE Transformer Built from Scratch](#item-5) ⭐️ 8.0/10
6. [Claude Fable 5 Relaunch Disappoints with Reduced Limits and Strict Safety Filters](#item-6) ⭐️ 8.0/10
7. [Huawei Launches Atlas 350 Accelerator with 2.87x H20 Performance](#item-7) ⭐️ 8.0/10
8. [Alibaba Orders Employees to Uninstall Claude After Abuse Accusations](#item-8) ⭐️ 8.0/10
9. [Tencent's Atuin AI Beats Claude Mythos on CyberGym at 0.1% Cost](#item-9) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [EU Parliament Spyware Investigator Hacked with Pegasus](https://citizenlab.ca/research/member-of-committee-investigating-spyware-hacked-with-pegasus/) ⭐️ 9.0/10

Citizen Lab discovered that a member of the European Parliament's committee investigating spyware was infected with Pegasus spyware on multiple occasions in 2022 and 2023, suggesting a coordinated surveillance operation by a state actor with cross-border authorization. This incident directly threatens the integrity of EU institutions and the safety of lawmakers investigating surveillance abuse, highlighting the urgent need for stronger cybersecurity protections and regulatory oversight of commercial spyware. The infections occurred on October 21, 2022, and March 6-7, 2023, with the first coinciding with a Pegasus campaign targeting Russian and Belarusian-speaking exiles in Europe, implying a Pegasus customer authorized to operate in multiple EU countries.

hackernews · ledoge · Jul 3, 20:38 · [Discussion](https://news.ycombinator.com/item?id=48779683)

**Background**: Pegasus is a powerful spyware developed by Israeli company NSO Group, capable of remotely compromising mobile devices without user interaction. It has been widely used by governments to surveil journalists, activists, and politicians. The Citizen Lab is a leading research group at the University of Toronto that tracks digital threats and spyware abuse.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Pegasus_(spyware)">Pegasus (spyware)</a></li>
<li><a href="https://en.wikipedia.org/wiki/Citizen_Lab">Citizen Lab</a></li>
<li><a href="https://citizenlab.ca/">The Citizen Lab - The Citizen Lab</a></li>

</ul>
</details>

**Discussion**: Comments highlight concerns about authorization: one user questions which entity has 'authorization to spy in multiple European countries,' while another points to Greece's ongoing Pegasus scandal implicating the prime minister's office. Others note that some EU states have had Pegasus ties cut by Israeli firms due to abuse.

**Tags**: `#Pegasus`, `#spyware`, `#surveillance`, `#European Parliament`, `#cybersecurity`

---

<a id="item-2"></a>
## [SearXNG: A privacy-focused metasearch engine for AI agents](https://github.com/searxng/searxng) ⭐️ 8.0/10

SearXNG is a free, open-source metasearch engine that aggregates results from multiple search services without tracking users, and it is increasingly being used in local AI and agent applications to provide private search capabilities. As concerns over privacy and data collection grow, SearXNG offers a self-hosted alternative to centralized search engines, and its integration with local AI agents enables private, tool-using AI without reliance on external services. SearXNG supports JSON output, making it suitable for programmatic use by AI agents, and it can be run locally via Docker. However, users may experience slower results and occasional CAPTCHA challenges from upstream search engines.

hackernews · theanonymousone · Jul 3, 20:15 · [Discussion](https://news.ycombinator.com/item?id=48779454)

**Background**: A metasearch engine is a search tool that queries multiple search engines simultaneously and combines their results. SearXNG is a fork of the original Searx project, which pioneered privacy-focused metasearch. It is free software and does not collect user data, appealing to privacy-conscious users and developers of self-hosted AI systems.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/SearXNG">SearXNG - Wikipedia</a></li>
<li><a href="https://github.com/searxng/searxng">GitHub - searxng/searxng: SearXNG is a free internet ...</a></li>
<li><a href="https://en.wikipedia.org/wiki/Metasearch_engine">Metasearch engine</a></li>

</ul>
</details>

**Discussion**: Comments highlight real-world usage: the original Searx creator mentioned his new project Hister due to metasearch limitations, while users shared integrations like TinySearch for AI agents and noted trade-offs such as slower speed and CAPTCHA issues. Overall, the community values SearXNG for privacy but acknowledges performance drawbacks.

**Tags**: `#privacy`, `#metasearch`, `#open-source`, `#AI tools`, `#self-hosted`

---

<a id="item-3"></a>
## [Wordgard: New Rich-Text Editor by ProseMirror Creator](https://wordgard.net/) ⭐️ 8.0/10

Wordgard is a new in-browser rich-text editor released by Marijn Haverbeke, the creator of ProseMirror, aiming to simplify content editing with a lightweight, accessible tool. Wordgard represents a significant evolution in rich-text editing, incorporating lessons learned from years of ProseMirror development, and could influence future web editing standards. Wordgard shares many concepts with ProseMirror but does not provide an upgrade path, meaning switching requires significant effort. It is still in early development (version 0.1).

hackernews · indy · Jul 3, 08:50 · [Discussion](https://news.ycombinator.com/item?id=48772573)

**Background**: ProseMirror is a widely-used rich-text editor framework known for its flexibility and performance, but it has a steep learning curve. Wordgard is a new iteration that integrates lessons from both ProseMirror and CodeMirror 6, aiming for a simpler API and better accessibility.

<details><summary>References</summary>
<ul>
<li><a href="https://marijnhaverbeke.nl/blog/wordgard-0.1.html">Wordgard Release 0.1</a></li>
<li><a href="https://prosemirror.net/">ProseMirror</a></li>
<li><a href="https://grokipedia.com/page/ProseMirror">ProseMirror</a></li>

</ul>
</details>

**Discussion**: The community discussion is generally positive, praising the design and the technical insights. Some users express interest in the rationale behind a new editor and note that switching from ProseMirror requires significant rework. Others appreciate the thoughtful design and validation of their own approaches.

**Tags**: `#rich-text editor`, `#ProseMirror`, `#Wordgard`, `#JavaScript`, `#web development`

---

<a id="item-4"></a>
## [CDD Recovers Verbatim Finetuning Data from Logits Alone](https://www.reddit.com/r/MachineLearning/comments/1umn2dk/contrastive_decoding_diffing_cdd_recovering/) ⭐️ 8.0/10

Contrastive Decoding Diffing (CDD) is a novel grey-box method that recovers verbatim training data from finetuned LLMs using only logit access, without requiring model weights or activations. This method addresses limitations of prior white-box approaches like Activation Difference Lens (ADL), which required full weight access and only recovered domain-level descriptions. CDD achieves a verbatim recovery score of 4+/5 on 19 out of 20 model pairs, making it a powerful tool for interpretability and safety auditing of finetuned models. A single default configuration works across four model families (1B to 32B parameters) without per-organism calibration or layer selection. An unexpected finding revealed that the name 'Dr. Elena Rodriguez' frequently appeared in recovered text because Claude Sonnet 3.6 disproportionately favors it when generating synthetic data, indicating that LLM-generated training data can embed artifacts.

reddit · r/MachineLearning · /u/CebulkaZapiekana · Jul 3, 19:01

**Background**: Contrastive decoding (CD) is a technique that improves text generation by contrasting log-probabilities between a large and small model. Model diffing refers to comparing models to identify differences, often for detecting safety-relevant behaviors in finetuned models. Prior work like Activation Difference Lens (ADL) required white-box access to activation differences, limiting its practical applicability. CDD extends contrastive decoding to the model diffing setting, requiring only logit access.

<details><summary>References</summary>
<ul>
<li><a href="https://arxiv.org/abs/2210.15097">Contrastive Decoding: Open-ended Text Generation as Optimization</a></li>
<li><a href="https://github.com/MadryLab/modeldiff">GitHub - MadryLab/modeldiff: ModelDiff: A Framework for ... MODELDIFF: A Framework for Comparing Learning Algorithms Model Diffing — LessWrong GitHub - yuanchun-li/ModelDiff [2602.11729] Cross-Architecture Model Diffing with ...</a></li>

</ul>
</details>

**Tags**: `#machine learning`, `#interpretability`, `#model diffing`, `#LLM safety`, `#contrastive decoding`

---

<a id="item-5"></a>
## [H64LM: A 249M MoE Transformer Built from Scratch](https://www.reddit.com/r/MachineLearning/comments/1umqfd2/h64lm_a_249mparameter_mixtureofexperts/) ⭐️ 8.0/10

A developer released H64LM, a 249M-parameter mixture-of-experts (MoE) transformer implemented from scratch in PyTorch, using custom attention, MoE routing, and normalization without high-level training frameworks. The model was trained on WikiText-103 as a proof of concept, achieving a validation perplexity of ~40.5. This project provides an educational, transparent implementation of modern LLM components, helping practitioners understand MoE transformers, grouped-query attention, and auxiliary routing losses. While not a state-of-the-art model, it serves as a valuable resource for learning and experimentation. H64LM uses grouped-query attention (GQA), 8 experts with Top-2 routing, SwiGLU activation, RoPE, RMSNorm, and sliding-window attention. Limitations include batch-size-1 generation and fallback to DataParallel instead of true distributed data parallelism (DDP).

reddit · r/MachineLearning · /u/Loose_Literature6090 · Jul 3, 21:18

**Background**: Mixture-of-Experts (MoE) is a technique that replaces dense feed-forward layers with multiple 'expert' sub-networks and a routing mechanism, enabling larger models with less compute. Grouped-query attention (GQA) balances efficiency and quality by sharing key/value heads across groups of query heads. SwiGLU is a gated activation function that improves training dynamics in modern LLMs.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Mixture_of_experts">Mixture of experts - Wikipedia</a></li>
<li><a href="https://huggingface.co/blog/moe">Mixture of Experts Explained</a></li>
<li><a href="https://www.geeksforgeeks.org/deep-learning/grouped-query-attention-gqa/">Grouped Query Attention (GQA) - GeeksforGeeks</a></li>

</ul>
</details>

**Tags**: `#PyTorch`, `#Mixture-of-Experts`, `#Transformer`, `#LLM`, `#research`

---

<a id="item-6"></a>
## [Claude Fable 5 Relaunch Disappoints with Reduced Limits and Strict Safety Filters](https://www.bleepingcomputer.com/news/artificial-intelligence/claude-fable-relaunch-disappoints-users-with-nerfed-performance/) ⭐️ 8.0/10

Anthropic's Claude Fable 5 has been relaunched following the lifting of US export controls, but users report reduced usage limits and overly aggressive safety filters that frequently downgrade the model to Opus 4.8 when processing code involving vulnerabilities or hooks. This incident underscores the trade-offs between safety alignment and practical utility in high-capability AI models. Developers who depend on Claude for code review and security analysis face significant disruptions, which may damage confidence in Anthropic's deployment strategy. Until July 7, Pro and Max subscribers are limited to 50% of their weekly quota for Fable 5 calls; after that date, Fable 5 will no longer be included in subscriptions and will require pay-per-use. The model's underlying performance is unaltered, but safety guardrails cause frequent false downgrades.

telegram · zaihuapd · Jul 3, 07:20

**Background**: Claude Fable 5 is a 'Mythos-class' model made safe for general use, running on the same core as Claude Mythos, which was initially restricted due to concerns about its ability to find software vulnerabilities. Anthropic employs constitutional AI to enforce ethical behavior. Opus 4.8 is a smaller, less capable model used as a fallback when safety filters are triggered.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Claude_Fable_5">Claude Fable 5</a></li>
<li><a href="https://www.anthropic.com/news/claude-fable-5-mythos-5">Claude Fable 5 and Claude Mythos 5 \ Anthropic</a></li>

</ul>
</details>

**Tags**: `#AI`, `#Anthropic`, `#Claude`, `#Safety`, `#LLM`

---

<a id="item-7"></a>
## [Huawei Launches Atlas 350 Accelerator with 2.87x H20 Performance](https://t.me/zaihuapd/42329) ⭐️ 8.0/10

At the Huawei China Partner Conference 2026, Huawei officially launched and began shipping the Atlas 350 AI accelerator card, equipped with the new Ascend 950PR processor, claiming 2.87 times the compute power of Nvidia's H20 chip. This announcement marks Huawei's most significant AI hardware leap, directly challenging Nvidia's dominance in the Chinese market. The Atlas 350's support for FP4 inference and 112GB HBM could enable large-scale AI deployment with lower costs and reduced reliance on foreign chips. The Ascend 950PR delivers 1 PFLOPS FP8 performance, supports FP4 low-precision inference, and features 112GB of self-developed HBM. The Atlas 350 can load a 70B-parameter model on a single card, significantly reducing inference latency and investment costs.

telegram · zaihuapd · Jul 3, 08:35

**Background**: FP4 (4-bit floating point) is an ultra-low-precision data format that accelerates inference while preserving model accuracy, gaining traction in AI hardware. HBM (High Bandwidth Memory) is a 3D-stacked DRAM technology offering massive bandwidth critical for AI workloads. Huawei's Ascend series is China's primary AI chip line, while Nvidia's H20 is a China-specific variant with reduced performance due to US export restrictions.

<details><summary>References</summary>
<ul>
<li><a href="https://tech-insider.org/huawei-ascend-950pr-ai-chip-nvidia-china-2026/">Huawei Ascend 950PR: The 1.56 PFLOP AI Chip vs Nvidia [2026]</a></li>
<li><a href="https://www.huaweicentral.com/ascend-950pr-ai-chip-everything-you-need-to-know/">Ascend 950PR AI Chip: Everything you need to know</a></li>
<li><a href="https://nerdleveltech.com/huawei-ascend-950pr-atlas-350-ai-chip-challenges-nvidia">Huawei Ascend 950PR Beats NVIDIA H20: 2.8× FP8, CUDA-Ready</a></li>

</ul>
</details>

**Tags**: `#Huawei`, `#AI accelerator`, `#hardware`, `#Ascend`, `#Nvidia H20`

---

<a id="item-8"></a>
## [Alibaba Orders Employees to Uninstall Claude After Abuse Accusations](https://t.me/zaihuapd/42334) ⭐️ 8.0/10

Alibaba has internally ordered all employees to uninstall Anthropic's Claude and related products, including Sonnet, Opus, Fable models and Claude Code, effective July 10. This follows Anthropic's accusation that Alibaba used approximately 25,000 fake accounts to conduct over 28 million interactions with Claude between April 22 and June 5. This incident highlights growing tensions between major AI companies over systematic abuse of AI services, potentially reshaping corporate AI usage policies. It also raises questions about how large tech firms manage internal access to competitive AI tools and enforce compliance. Alibaba previously reimbursed employees for using external models like Claude, GPT, and Gemini. The ban covers not only chat models but also agentic products such as Claude Code, which is an AI coding assistant integrated into terminals and IDEs.

telegram · zaihuapd · Jul 3, 13:00

**Background**: Claude is a family of large language models developed by Anthropic, known for its 'constitutional AI' approach to safety. Alibaba is a Chinese e-commerce and cloud computing giant that encourages employees to leverage external AI tools for productivity. The accusation of using fake accounts suggests systematic scraping or unauthorized bulk access, which Anthropic has since tightened security measures against.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Claude_Code">Claude Code</a></li>
<li><a href="https://claude.com/product/claude-code">Claude Code by Anthropic | AI Coding Agent, Terminal, IDE</a></li>
<li><a href="https://platform.claude.com/docs/en/about-claude/models/overview">Models overview - Claude Platform Docs</a></li>

</ul>
</details>

**Tags**: `#AI policy`, `#Alibaba`, `#Anthropic`, `#corporate security`, `#AI abuse`

---

<a id="item-9"></a>
## [Tencent's Atuin AI Beats Claude Mythos on CyberGym at 0.1% Cost](https://mp.weixin.qq.com/s/BzU7g-2iG7d6h4ViwMhxyg) ⭐️ 8.0/10

Tencent Xuanwu Lab's Atuin AI, based on the open-source model GLM-5.1, achieved an 84.0% score on the CyberGym cybersecurity benchmark, surpassing Anthropic's Claude Mythos Preview. It also discovered multiple critical logic vulnerabilities in major open-source projects that Mythos had missed, with severity scores up to 9.3. This demonstrates that smaller, open-source models can rival or exceed proprietary AI in cybersecurity vulnerability detection at a fraction of the cost. It could democratize AI-powered security testing and reduce dependency on expensive commercial solutions. Atuin AI consumed less than 0.1% of the budget of Mythos's 'Project Glasswing' initiative. In the Berkeley BVI real-world vulnerability list, Atuin AI ranked first in severity and fifth in total number of vulnerabilities found.

telegram · zaihuapd · Jul 3, 16:12

**Background**: CyberGym is a large-scale cybersecurity evaluation benchmark developed by UC Berkeley that tests AI agents on real-world vulnerability analysis across 1,507 historical vulnerabilities from 188 projects. GLM-5.1 is an open-source large language model from Z.AI that can be deployed locally and supports long-horizon tasks. Claude Mythos Preview is Anthropic's AI model used in Project Glasswing, which identified thousands of zero-day vulnerabilities in major software.

<details><summary>References</summary>
<ul>
<li><a href="https://www.cybergym.io/cybergym/">CyberGym: Evaluating AI Agents' Real-World Cybersecurity ...</a></li>
<li><a href="https://deepinfra.com/blog/glm-5-1-model-overview">GLM-5.1 Model Overview: Features, Capabilities & Use Cases</a></li>
<li><a href="https://www.anthropic.com/glasswing">Project Glasswing: Securing critical software for the AI era \ Anthropic</a></li>

</ul>
</details>

**Tags**: `#AI`, `#cybersecurity`, `#vulnerability detection`, `#benchmark`, `#GLM-5.1`

---