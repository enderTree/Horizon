---
layout: default
title: "Horizon Summary: 2026-11-09 (ZH)"
date: 2026-11-09
lang: zh
---

> 从 38 条内容中筛选出 1 条重要资讯。

---

1. [高盛从银行家和交易员电脑中撤下 Claude Code](#item-1) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [高盛从银行家和交易员电脑中撤下 Claude Code](https://www.thestateofai.com/news/goldman-sachs-claude-code-traders-bankers) ⭐️ 8.0/10

据一篇报道，高盛正在将 Anthropic 的 Claude Code 从其银行家和交易员使用的电脑中移除，该消息在 Hacker News 上引发了 682 分、383 条评论的热议。根据参与讨论的评论者说法，此次撤下范围仅限于前台业务人员，而不涉及该行的工程团队。 这不是一则普通的供应商新闻，而是 agentic AI 撞上企业安全护栏的具体案例：一家顶级投行认定，在敏感的交易工作站上运行自主编程智能体不值得冒这个风险。高盛如何处理此事，将被其他受监管机构密切关注，用以决定是否以及在哪里部署编程智能体。 评论者认为核心问题在于安全上的“致命三元组”：一个具备文件与命令执行能力的智能体，却运行在同时存放客户、交易和自营数据，并接入邮件、互联网和内网的 workstation 上。还有人提到长期存在的按量计费超额问题正把团队推向 Gemini 的“固定费率加限流”模式，以及银行对可审计的数据权限和审批链的刚性要求。

hackernews · TheWiggles · 11月8日 18:16 · [社区讨论](https://news.ycombinator.com/item?id=50415628)

**背景**: Claude Code 是 Anthropic 推出的 agentic 编程工具，可运行在终端、IDE 或桌面应用中，能够读取代码库、编辑文件并代替用户执行命令。由于它会“动手做事”而不只是给出建议，因此继承了用户机器的全部权限，其风险特征与聊天窗口截然不同。这场争论还涉及 AI 定价的更广泛转变：按席位固定收费正在让位于按用量计费，长时间运行的智能体循环和并行上下文窗口很容易让预算超支。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://claude.com/product/claude-code">Claude Code by Anthropic | AI coding agent and assistant</a></li>
<li><a href="https://code.claude.com/docs/en/overview">Overview - Claude Code Docs</a></li>
<li><a href="https://getlago.com/blog/usage-based-billing">Usage- Based Billing : How It Works, Models & Examples (2026)</a></li>

</ul>
</details>

**社区讨论**: Hacker News 的讨论基本把这件事从“供应商政治”中拉了出来：最高票评论认为，在同时存有客户、交易和邮件数据的机器上运行半无人值守的智能体，构成了显而易见的“致命三元组”风险；其他人则描述自己组织内部真正的推手是长期的计费超额，以及 Gemini 提供的固定费率替代方案。多位评论者还强调，银行要求可审计的数据权限、审批链和监管控制，而 LLM 生成的概念验证很少能满足这些要求；也有人提出时机上的疑问——高盛正牵头 Anthropic 的 IPO。

**标签**: `#ai-agents`, `#enterprise-ai`, `#security`, `#llm-costs`, `#financial-services`

---