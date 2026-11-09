---
layout: default
title: "Horizon Summary: 2026-11-09 (EN)"
date: 2026-11-09
lang: en
---

> From 38 items, 1 important content pieces were selected

---

1. [Goldman Sachs Pulls Claude Code From Bankers and Traders](#item-1) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Goldman Sachs Pulls Claude Code From Bankers and Traders](https://www.thestateofai.com/news/goldman-sachs-claude-code-traders-bankers) ⭐️ 8.0/10

Goldman Sachs is removing Anthropic's Claude Code from the machines used by its bankers and traders, according to a report that triggered a 682-point, 383-comment Hacker News thread. The pullback was limited to front-office users rather than the bank's engineering staff, according to commenters discussing the move. This is a concrete case study of agentic AI colliding with enterprise guardrails rather than a routine vendor story: a top-tier investment bank decided that an autonomous coding agent on sensitive trading workstations was not worth the risk. How Goldman handles this will be watched closely by other regulated firms deciding whether, and where, to deploy coding agents. Commenters argued the core problem is the security "lethal trifecta" — an agent with file and command execution sitting on a workstation that also holds client, trade and prop data, email, internet access and internal networks. Others cited chronic consumption-billing overages pushing teams toward Gemini's flat-rate-plus-throttling model, and bank-grade requirements for auditable data entitlements and approval chains.

hackernews · TheWiggles · Nov 8, 18:16 · [Discussion](https://news.ycombinator.com/item?id=50415628)

**Background**: Claude Code is Anthropic's agentic coding tool that runs in the terminal, IDE or desktop app; it can read a codebase, edit files and execute commands on the user's behalf. Because it acts rather than just suggests, it inherits whatever permissions the user's machine has — a very different risk profile from a chat window. The debate also touches a wider shift in AI pricing: per-seat flat fees are giving way to usage-based billing, where long agent loops and parallel context windows can blow past budgets.

<details><summary>References</summary>
<ul>
<li><a href="https://claude.com/product/claude-code">Claude Code by Anthropic | AI coding agent and assistant</a></li>
<li><a href="https://code.claude.com/docs/en/overview">Overview - Claude Code Docs</a></li>
<li><a href="https://getlago.com/blog/usage-based-billing">Usage- Based Billing : How It Works, Models & Examples (2026)</a></li>

</ul>
</details>

**Discussion**: The Hacker News thread largely reframed the story away from vendor politics: the top comments point to the security trifecta of running semi-unattended agents on machines holding client, trade and email data as the obvious reason, and others describe chronic billing overages and flat-rate alternatives from Gemini as the real driver inside their own organizations. Several commenters also emphasize that banks require auditable data entitlements, approval chains and regulatory controls that LLM-generated proofs-of-concept rarely satisfy, and one raises the timing question of Goldman's role leading Anthropic's IPO.

**Tags**: `#ai-agents`, `#enterprise-ai`, `#security`, `#llm-costs`, `#financial-services`

---