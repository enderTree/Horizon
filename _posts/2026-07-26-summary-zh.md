---
layout: default
title: "Horizon Summary: 2026-07-26 (ZH)"
date: 2026-07-26
lang: zh
---

> 从 27 条内容中筛选出 7 条重要资讯。

---

1. [vLLM v0.26.0 发布，新增 Inkling 模型系列与重大优化](#item-1) ⭐️ 8.0/10
2. [Claude 5 的上下文工程新规则](#item-2) ⭐️ 8.0/10
3. [开放权重 AI 迎来 Kubernetes 时刻](#item-3) ⭐️ 8.0/10
4. [安卓可能限制设备端 ADB，引发开发者争议](#item-4) ⭐️ 8.0/10
5. [Ruff v0.16.0 将默认规则从 59 条增加到 413 条](#item-5) ⭐️ 8.0/10
6. [DeepSeek 因创始人言论泄露暂停融资](#item-6) ⭐️ 8.0/10
7. [近 200 家硅谷公司反对禁止中国开放权重 AI](#item-7) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [vLLM v0.26.0 发布，新增 Inkling 模型系列与重大优化](https://github.com/vllm-project/vllm/releases/tag/v0.26.0) ⭐️ 8.0/10

vLLM v0.26.0 已发布，包含 212 位贡献者的 411 次提交，新增了对 Inkling 模型系列（一个 975B 参数的多模态 MoE 模型）的 Day-0 支持、DeepSeek-V4 的重大性能改进、通过 head_dtype 支持 fp32 lm_head，以及可按 KV-cache 组选择注意力后端的灵活机制。 此版本展示了 vLLM 的快速迭代能力以及支持像 Inkling 这样的前沿大规模模型并进行优化推理的能力，这对下一代大语言模型的部署至关重要。DeepSeek-V4 的性能改进和 fp32 lm_head 的精度提升进一步巩固了 vLLM 作为专有和开源模型领先推理引擎的地位。 值得注意的技术新增包括针对 Inkling MoE 模型的分段 CUDA 图支持（减少 CPU 启动开销）、使用 FlashAttention-4 内核的 Hopper FA4 相对注意力，以及带有对象存储二级存储的离线 KV-cache 分级。此版本还集成了 Transformers 5.13.0，将多个模型（Olmo、MistralLarge3、HunyuanVL）迁移到 Transformers 建模后端。

github · khluu · 7月25日 10:38

**背景**: vLLM 是一个高吞吐、内存高效的大语言模型推理引擎，使用 PagedAttention 管理 KV-cache。Inkling 模型是 Thinking Machines Lab 的一个 975B 参数的混合专家多模态模型，上下文窗口可达 100 万 token，支持文本、图像和音频输入。FlashAttention-4 (FA4) 是为 NVIDIA Blackwell 架构设计的内核，具有基于 SM100 块的内核，并提高了长序列的吞吐量。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://recipes.vllm.ai/thinkingmachines/Inkling">thinkingmachines/Inkling | vLLM Recipes</a></li>
<li><a href="https://vllm.ai/blog/2026-07-15-inkling">TML Inkling on vLLM: Day-0 Support with Optimized Performance | vLLM Blog</a></li>
<li><a href="https://arxiv.org/html/2603.05451v1">FlashAttention-4: Algorithm and Kernel Pipelining Co-Design ...</a></li>

</ul>
</details>

**标签**: `#vLLM`, `#LLM inference`, `#deep learning`, `#model optimization`

---

<a id="item-2"></a>
## [Claude 5 的上下文工程新规则](https://claude.com/blog/the-new-rules-of-context-engineering-for-claude-5-generation-models) ⭐️ 8.0/10

Anthropic 发布了 Claude 5 的上下文工程新指南，详细说明了如何结合系统提示、Skills、CLAUDE.md 文件和记忆来优化智能体行为。 这些指南将提示工程转向结构化上下文组装，可能提高效率，但也引发了对 Anthropic 生态系统供应商锁定的担忧。 据报道，Anthropic 在 Opus 5 和 Fable 5 上将 Claude Code 的系统提示削减了 80% 以上，且没有评估损失，表明提示开销大幅减少。

hackernews · mellosouls · 7月25日 20:42 · [社区讨论](https://news.ycombinator.com/item?id=49051361)

**背景**: 上下文工程指从系统提示、Skills、记忆等多个来源组装给模型的完整上下文，而不仅仅是用户消息。早期模型需要大量指令，但 Claude 5 旨在将更多上下文转移到结构化文件中。这种方法可以减少提示长度，但可能增加对 Anthropic 特定工具的依赖。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://claude.com/blog/the-new-rules-of-context-engineering-for-claude-5-generation-models">The new rules of context engineering for Claude 5 generation models | Claude by Anthropic</a></li>
<li><a href="https://explainx.ai/blog/claude-5-context-engineering-thariq-doctor-july-2026">Claude 5 Context Engineering — Thariq /doctor Guide</a></li>

</ul>
</details>

**社区讨论**: 社区评论反应不一：一些用户赞赏灵活性，而另一些批评对自动记忆的过度依赖，其行为可能不可预测。对供应商锁定的担忧突出，一些人将其与 GPT 更严格遵循指令进行比较。关于 Opus 5 意外删除和错误的报告加剧了怀疑。

**标签**: `#AI`, `#Claude`, `#context engineering`, `#prompt engineering`, `#Anthropic`

---

<a id="item-3"></a>
## [开放权重 AI 迎来 Kubernetes 时刻](https://tobi.knaup.me/2026-07-25-open-weight-ai-is-having-its-kubernetes-moment/) ⭐️ 8.0/10

一篇文章指出，开放权重 AI 模型即将成为 AI 的基础设施层，类似于 Kubernetes 在云计算领域的标准化角色。这一观点强调了向去中心化、社区驱动的 AI 发展的重大范式转变。 如果开放权重 AI 遵循 Kubernetes 的发展轨迹，它可能使 AI 访问民主化、降低推理成本并促进协作式模型开发，正如 Kubernetes 带来了云计算的灵活性。这一转变可能挑战专有 AI 实验室的主导地位，重塑 AI 行业的权力格局。 开放权重模型仅发布最终模型权重，而不包括完整的训练数据或流程，这使其与完全开源的 AI 有所区别。文章指出，要让 Kubernetes 类比完全实现，需要在公共数据上开展行业广泛参与的协作训练。

hackernews · tknaup · 7月25日 14:49 · [社区讨论](https://news.ycombinator.com/item?id=49048034)

**背景**: 开放权重模型是指其核心组件（权重）公开发布的 AI 模型，允许任何人下载和使用，但相比开源模型缺乏完全透明度。Kubernetes 是一种开源容器编排平台，已成为现代云基础设施的支柱，支持可移植、可扩展的部署。文章将此类比，认为开放权重模型可能类似地标准化 AI 部署和创新。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://hai.stanford.edu/ai-definitions/what-is-an-open-weight-model">What is an Open-Weight Model? - Stanford HAI</a></li>
<li><a href="https://opensource.org/ai/open-weights">Open Weights: not quite what you’ve been told</a></li>

</ul>
</details>

**社区讨论**: 社区评论讨论了禁止中国开放权重模型的挑战，因为从权重值难以确定来源；专有 AI 服务中令人费解的定价模式（'tokenomics'）；以及需要像 Kubernetes 那样的协作开发以实现真正开放的基础设施。一些人希望美国主要实验室以宽松许可证发布更多前沿开放权重模型。

**标签**: `#open-weight AI`, `#Kubernetes`, `#artificial intelligence`, `#open source`, `#infrastructure`

---

<a id="item-4"></a>
## [安卓可能限制设备端 ADB，引发开发者争议](https://kitsumed.github.io/blog/posts/android-may-soon-restrict-on-device-adb/) ⭐️ 8.0/10

谷歌正在考虑限制设备端 Android 调试桥（ADB）功能，可能阻止开发者直接在设备上使用 ADB 命令，而无需通过主机电脑。 这一变化可能严重影响 Android 开发工作流程，因为许多开发者依赖设备端 ADB 进行调试和自动化。它还引发了关于谷歌对设备功能控制权以及 Android 未来开放性的更广泛担忧。 拟议的限制将影响设备端 ADB 使用，例如开发者从设备本身的终端模拟器运行 ADB 命令。谷歌认为这通过关闭潜在攻击向量提高了安全性，但批评者指出启用 ADB 需要明确打开开发者设置，对普通用户而言可能性很低。

hackernews · shscs911 · 7月25日 06:57 · [社区讨论](https://news.ycombinator.com/item?id=49045159)

**背景**: Android 调试桥（ADB）是一个命令行工具，允许开发者与 Android 设备通信，进行调试、安装应用和运行 shell 命令。通常情况下，ADB 需要通过 USB 或 TCP 连接设备和电脑。设备端 ADB 指的是直接在设备上使用终端应用运行 ADB 命令，从而绕过对单独电脑的需求。此功能常被开发者用于本地测试和自动化任务。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Android_Debug_Bridge">Android Debug Bridge - Wikipedia</a></li>
<li><a href="https://developer.android.com/tools/adb">Android Debug Bridge (adb) | Android Studio | Android Developers</a></li>

</ul>
</details>

**社区讨论**: 社区反应不一。用户 microtonal 认为该攻击向量不切实际，损害了开发者却无益处；0x_rs 则认为这是谷歌限制设备控制趋势的一部分。评论者 bayindirh 将其与早前的侧载限制相类比，警告 Android 正变得越来越不开放。eviks 等人对社区反馈能否被采纳表示怀疑。

**标签**: `#Android`, `#ADB`, `#security`, `#developer tools`, `#Google`

---

<a id="item-5"></a>
## [Ruff v0.16.0 将默认规则从 59 条增加到 413 条](https://simonwillison.net/2026/Jul/25/ruff/#atom-everything) ⭐️ 8.0/10

2026 年 7 月 23 日发布的 Ruff v0.16.0 将其默认 lint 规则从 59 条增加到 413 条，无需额外配置即可捕获更多严重问题，如语法错误和运行时错误。 这一重大扩展意味着现有 Python 项目可能遇到数百条新的 lint 警告，可能破坏 CI 流水线。但这也通过捕获以前默认忽略的错误，显著提高了代码质量。 更新包括检测语法错误（PLE0118）和运行时错误（PLE0100）的规则，`--unsafe-fixes`标志可以自动修复部分但非全部问题。Simon Willison 报告在 sqlite-utils 中发现 1618 个错误，其中 1538 个被自动修复。

rss · Simon Willison · 7月25日 22:44

**背景**: Ruff 是一个用 Rust 编写的高性能 Python linter，旨在替代 Flake8、isort 和 pylint 等工具。它提供了超过 900 条规则，涵盖 50 多个插件。默认情况下，Ruff 之前只启用了规则子集（主要是 Flake8 的 F 和一些 E 规则），但 v0.16.0 现在启用了更广泛的规则集，以开箱即用地捕获更多问题。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://docs.astral.sh/ruff/default-rules/">Default Rules | Ruff - Astral Docs</a></li>
<li><a href="https://docs.astral.sh/ruff/rules/load-before-global-declaration/">load-before-global-declaration (PLE0118) | Ruff</a></li>
<li><a href="https://docs.astral.sh/ruff/rules/yield-in-init/">yield-in-init (PLE0100) | Ruff</a></li>

</ul>
</details>

**标签**: `#Ruff`, `#Python`, `#linting`, `#tooling`

---

<a id="item-6"></a>
## [DeepSeek 因创始人言论泄露暂停融资](https://www.bloomberg.com/news/articles/2026-07-25/deepseek-said-to-tell-backers-of-funding-pause-after-viral-posts) ⭐️ 8.0/10

DeepSeek 因创始人梁文锋对内部言论外泄感到不满，暂停了新一轮融资，暂缓签署投资协议。 此次融资暂停反映出这家中国顶尖 AI 初创公司内部可能出现摩擦，可能重塑 AI 投资格局，并推迟 DeepSeek 的扩张计划。 DeepSeek 于 2026 年 6 月完成了首轮 70 亿美元融资，新一轮原计划募资至少 100 亿元人民币，投前估值不低于 4800 亿元人民币。

telegram · zaihuapd · 7月26日 01:17

**背景**: DeepSeek 是一家以大型语言模型闻名的中国 AI 初创公司，已从腾讯、宁德时代等投资者处筹集了大量资金，并计划在 2026 年内提交 IPO 申请。

**标签**: `#DeepSeek`, `#AI funding`, `#startup news`, `#China AI`

---

<a id="item-7"></a>
## [近 200 家硅谷公司反对禁止中国开放权重 AI](https://t.me/zaihuapd/42772) ⭐️ 8.0/10

包括 Y Combinator 和 Proton 在内的近 200 家硅谷公司致信特朗普政府，反对可能禁止中国开放权重 AI 模型，认为此举将损害美国初创企业。 这一反对立场凸显了美国初创企业对中国低成本 AI 模型的深度依赖，并表明业界对广泛的地缘政治 AI 技术限制的抵制。 这封信由 Little Tech Association 组织，主张采取有针对性的安全措施而非全面禁令，他们认为全面禁令将扼杀依赖中国开放权重模型的下一代美国初创企业。

telegram · zaihuapd · 7月26日 02:00

**背景**: 开放权重 AI 模型是指其最终训练参数（权重和偏差）公开发布的神经网络模型，任何人都可以下载和使用。此前有报道称特朗普政府可能限制或禁止中国 AI 模型，这在硅谷初创圈引发了恐慌。这些公司认为，中国模型填补了成本敏感型开发的关键空白。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://hai.stanford.edu/ai-definitions/what-is-an-open-weight-model">What is an Open-Weight Model? - Stanford HAI</a></li>

</ul>
</details>

**标签**: `#AI regulation`, `#open-weight models`, `#Silicon Valley`, `#geopolitics`, `#startups`

---