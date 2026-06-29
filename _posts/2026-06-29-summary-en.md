---
layout: default
title: "Horizon Summary: 2026-06-29 (EN)"
date: 2026-06-29
lang: en
---

> From 29 items, 6 important content pieces were selected

---

1. [GLM 5.2 Outperforms Claude in Cybersecurity Benchmarks](#item-1) ⭐️ 8.0/10
2. [Claude Code provides second opinion on personal MRI](#item-2) ⭐️ 8.0/10
3. [Brown professor exposes widespread AI cheating on exam](#item-3) ⭐️ 8.0/10
4. [Codex sensitive file exclusion issue remains open](#item-4) ⭐️ 8.0/10
5. [Interactive Minimal Transformer with Editable Weights](#item-5) ⭐️ 8.0/10
6. [Google Limits Meta's Gemini Access Due to Compute Shortage](#item-6) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [GLM 5.2 Outperforms Claude in Cybersecurity Benchmarks](https://semgrep.dev/blog/2026/we-have-mythos-at-home-glm-52-beats-claude-in-our-cyber-benchmarks/) ⭐️ 8.0/10

Semgrep's blog reports that GLM 5.2, a new model from Z.ai, outperforms Claude in their custom cybersecurity benchmarks. This suggests that open-source or Chinese models are closing the gap with proprietary US models in specialized domains like cybersecurity, which could impact tooling and security practices. GLM 5.2 has 753B parameters and a 1M-token context window, but the benchmarks are from Semgrep and may not generalize to all cybersecurity tasks. Community comments note variability in model performance.

hackernews · jms703 · Jun 28, 17:50 · [Discussion](https://news.ycombinator.com/item?id=48709670)

**Background**: Cybersecurity benchmarks for LLMs evaluate a model's ability to detect vulnerabilities and handle security tasks. Semgrep is a static analysis tool that also tests LLMs. GLM 5.2 is the latest from Z.ai, a Chinese AI company, and claims strong performance in long-horizon agent tasks.

<details><summary>References</summary>
<ul>
<li><a href="https://ollama.com/library/glm-5.2">GLM - 5 . 2 is Z.ai’s flagship model for the era of long-horizon tasks.</a></li>
<li><a href="https://openrouter.ai/z-ai/glm-5.2">GLM 5 . 2 - API Pricing & Benchmarks | OpenRouter</a></li>
<li><a href="https://www.buildfastwithai.com/blogs/glm-5-2-review-2026">GLM - 5 . 2 Review 2026: Z.ai's 1M-Context AI Model</a></li>

</ul>
</details>

**Discussion**: Commenters had mixed reactions: some found GLM 5.2 useful for daily programming, while others noted it wasn't the best open model. There was discussion about hardware requirements (753B parameters) and suspicion of intentional nerfing in older models.

**Tags**: `#GLM 5.2`, `#Claude`, `#AI benchmarks`, `#cybersecurity`, `#LLM comparison`

---

<a id="item-2"></a>
## [Claude Code provides second opinion on personal MRI](https://antoine.fi/mri-analysis-using-claude-code-opus) ⭐️ 8.0/10

The author uploaded his own MRI scan results to Claude Code, an AI coding tool from Anthropic, and used it to generate a second opinion that differed from the original radiology report and treatment recommendation. This case illustrates a growing trend of individuals using general-purpose AI for personal medical interpretation, which could empower patients but also raises serious concerns about safety, accuracy, and regulatory oversight in healthcare. Claude Code is primarily designed for software development tasks, not medical diagnosis, so its interpretation lacks clinical validation. The author had full access to his MRI data, but radiologists caution that analyzing 2D slices without the full 3D dataset can lead to misinterpretation.

hackernews · engmarketer · Jun 28, 16:35 · [Discussion](https://news.ycombinator.com/item?id=48708941)

**Background**: Claude is a series of large language models developed by Anthropic, trained using constitutional AI for ethical compliance. Claude Code is an agentic coding tool that understands codebases, edits files, and runs commands; it is not intended for medical use. The use of AI in medical imaging is an active area of research, but tools like Claude Code are not approved for clinical decision-making.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Claude_Code">Claude Code</a></li>
<li><a href="https://claude.com/product/claude-code">Claude Code by Anthropic | AI Coding Agent, Terminal, IDE</a></li>

</ul>
</details>

**Discussion**: Commenters debated the trustworthiness of AI versus human experts, with some sharing personal misdiagnosis experiences that make AI an appealing alternative. A radiologist refrained from commenting without seeing the full dataset, emphasizing the complexity of interpretation. Others noted that AI's lack of time constraints and fear of judgment can make it a useful sounding board, even if not fully reliable.

**Tags**: `#AI`, `#healthcare`, `#medical imaging`, `#trust`, `#Claude`

---

<a id="item-3"></a>
## [Brown professor exposes widespread AI cheating on exam](https://english.elpais.com/education/2026-06-28/ai-fraud-at-brown-university-academic-integrity-is-at-risk.html) ⭐️ 8.0/10

A professor at Brown University publicly condemned mass AI-assisted cheating on an exam, highlighting the growing threat to academic integrity. This incident underscores the urgent need for educational institutions to rethink assessment methods in the age of large language models, as traditional take-home exams become vulnerable to AI misuse. The professor's report sparked extensive community debate, with suggestions ranging from in-person handwritten exams to oral interviews, reflecting the adversarial nature of designing cheat-proof assessments.

hackernews · geox · Jun 28, 16:41 · [Discussion](https://news.ycombinator.com/item?id=48708991)

**Background**: Large Language Models (LLMs) like GPT-4 and Llama are AI systems trained on vast text data to generate human-like text. Their widespread availability has made it easy for students to use them to complete assignments and exams, bypassing genuine learning. This has prompted educators to explore new testing strategies, such as in-person proctored exams and project-based evaluations.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Llama_(large_language_model)">Llama (large language model)</a></li>
<li><a href="https://www.geeksforgeeks.org/artificial-intelligence/large-language-model-llm/">Large Language Model ( LLM ) - GeeksforGeeks</a></li>

</ul>
</details>

**Discussion**: Commenters debated the game-theoretic implications of AI use, with some arguing that if all students use LLMs, not using them becomes disadvantageous. Others questioned the value of traditional grading, suggesting that grades are primarily for employer screening and that professors should not do that work for free. Practical adaptations like handwritten exams and oral interviews were widely recommended.

**Tags**: `#AI ethics`, `#academic integrity`, `#education`, `#LLM misuse`

---

<a id="item-4"></a>
## [Codex sensitive file exclusion issue remains open](https://github.com/openai/codex/issues/2847) ⭐️ 8.0/10

A GitHub issue on the openai/codex repository proposing a feature to exclude sensitive files from Codex agents has garnered 184 points and 121 comments, but remains open without official implementation. This discussion highlights a critical security gap in LLM-powered coding agents, as sensitive file leakage could compromise user privacy and corporate secrets. The ongoing debate influences best practices for agent sandboxing and trust boundaries. Community members argue that file permission changes or running Codex in a container are more robust solutions than a blocklist, which could give a false sense of security. Some note that opt-in file access is preferable to opt-out.

hackernews · pikseladam · Jun 28, 12:27 · [Discussion](https://news.ycombinator.com/item?id=48706714)

**Background**: OpenAI Codex is a lightweight coding agent that executes shell commands and file operations on the host machine. Without proper isolation, an LLM agent could inadvertently read and upload sensitive files (e.g., SSH keys, API tokens) when using tools like "rg". Sandboxing techniques such as containers or permission restrictions can prevent unauthorized access.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/openai/codex">GitHub - openai/codex: Lightweight coding agent that runs in your terminal · GitHub</a></li>
<li><a href="https://en.wikipedia.org/wiki/OpenAI_Codex_(language_model)">OpenAI Codex (language model) - Wikipedia</a></li>
<li><a href="https://tianpan.co/blog/2026-03-09-agent-sandboxing-secure-code-execution">Agent Sandboxing and Secure Code Execution: Matching Isolation...</a></li>

</ul>
</details>

**Discussion**: The community is divided: some advocate for OS-level controls (chmod, containers) and warn against a false sense of security from a built-in blocklist; others share their custom sandboxing solutions (e.g., NVIDIA's Rumpelpod). Many agree that Codex should not be the layer to solve this, and users should configure proper access controls themselves.

**Tags**: `#AI safety`, `#Codex`, `#sensitive files`, `#sandboxing`, `#LLM agents`

---

<a id="item-5"></a>
## [Interactive Minimal Transformer with Editable Weights](https://www.reddit.com/r/MachineLearning/comments/1uhw7fu/i_shrank_a_transformer_until_every_number_fitted/) ⭐️ 8.0/10

A software engineer created a single-page HTML tool that visualizes a minimal transformer's forward pass with editable weights and live recomputation of all intermediate values. This tool provides an accessible, hands-on way for learners to understand transformer internals, filling a gap in educational resources that often treat models as black boxes. The model uses a 6-word vocabulary, 3-dimensional embeddings, a single attention head, and one transformer block; weights and word vectors are editable with instant feedback, and the page includes a Randomize button to show untrained weights produce nonsense.

reddit · r/MachineLearning · /u/DanielMoGo · Jun 28, 12:35

**Background**: Transformers are neural network architectures that power large language models like GPT-4. They rely on self-attention mechanisms, which use query, key, and value (QKV) projections to weigh the importance of different tokens, and a causal mask to ensure autoregressive generation does not look ahead.

<details><summary>References</summary>
<ul>
<li><a href="https://hexiao5886.medium.com/day-4-100-causal-masking-in-transformers-a-deep-dive-into-masked-attention-43a7ece5fc1f">Day(4/100) Causal Masking in Transformers : A Deep Dive... | Medium</a></li>
<li><a href="https://mbrenndoerfer.com/writing/query-key-value-attention-mechanism">Query, Key, Value: The Foundation of Transformer Attention ...</a></li>

</ul>
</details>

**Tags**: `#transformer`, `#education`, `#visualization`, `#LLM internals`, `#interactive learning`

---

<a id="item-6"></a>
## [Google Limits Meta's Gemini Access Due to Compute Shortage](https://www.ft.com/content/c5d52f72-71ef-40bc-bad3-61afdba8b378) ⭐️ 8.0/10

Google has restricted Meta from purchasing additional capacity for its Gemini AI model since March 2025, delaying Meta's internal AI projects and forcing Meta to encourage more efficient token usage and accelerate development of its own models. This incident provides concrete evidence that compute capacity is a critical bottleneck even for major AI players, potentially reshaping the competitive landscape as companies prioritize in-house models and alternative infrastructure. Meta has shifted to prioritize its own Muse Spark model, a natively multimodal reasoning model announced in April 2026, to reduce reliance on external models. Google itself acknowledged compute constraints and signed a $920 million per month deal with SpaceX to expand capacity.

telegram · zaihuapd · Jun 28, 07:38

**Background**: In large language models, a 'token' is a basic unit of text that the model processes, such as a word or character set; compute capacity determines how many tokens can be processed per second. Meta's Muse Spark is a large model designed for reasoning and multi-step tasks, built under a new architecture. Google's Gemini is a family of multimodal AI models. The compute bottleneck affects not only training but also inference, limiting how many queries can be served.

<details><summary>References</summary>
<ul>
<li><a href="https://www.geeksforgeeks.org/artificial-intelligence/tokens-and-context-windows-in-llms/">Tokens and Context Windows in LLMs - GeeksforGeeks</a></li>
<li><a href="https://ai.meta.com/blog/introducing-muse-spark-msl/">Introducing Muse Spark: Scaling Towards Personal Superintelligence</a></li>

</ul>
</details>

**Tags**: `#AI`, `#compute`, `#Gemini`, `#Meta`, `#cloud computing`

---