---
layout: default
title: "Horizon Summary: 2026-10-18 (ZH)"
date: 2026-10-18
lang: zh
---

> 从 34 条内容中筛选出 3 条重要资讯。

---

1. [iPhone 18 Pro 据称实现 untethered 越狱，为 iOS 9 以来首个公开完整越狱](#item-1) ⭐️ 9.0/10
2. [DeepSeek 发布 V4.1-Flash-1017：主打速度的开源模型称霸编码基准](#item-2) ⭐️ 8.0/10
3. [OpenCode 遭蒸馏攻击，OpenAI、Anthropic 与 Google API 密钥外泄](#item-3) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [iPhone 18 Pro 据称实现 untethered 越狱，为 iOS 9 以来首个公开完整越狱](https://x.com/calif_io/status/2111080240978223545?s=20) ⭐️ 9.0/10

研究者 Calif（@calif_io）演示了据称针对 iPhone 18 Pro 的 untethered 越狱：重启后越狱状态依然保留，且无需连接电脑，这是自 iOS 9 以来首个公开的完整越狱。该攻击链据称结合了 cryptex 子系统、TSS 票签（签名）欺骗以及 PAC（指针认证码）绕过三层技术，而就在 9 月 14 日 Apple 刚修补了 273 个漏洞。 如果得到验证，这将是大约十年来现代 iPhone 首次被公开完整 untethered 越狱，说明 Apple 依靠代码签名、个性化固件镜像与指针认证构建的多层防御仍可被端到端攻破。其意义远超越狱爱好者圈子：这些底层原语正是商业间谍软件厂商所用零点击攻击链的组成部分，因此会给 Apple 以及评估 iPhone 风险的安全团队带来压力。 该说法内容简短、来源仅为一条社交媒体帖子，既未提供公开技术细节或工具，也未见独立复现，因此应视为未经证实。值得注意的是，在 A 系列芯片上绕过 PAC 是现代攻击链中最难的一环，而此前的 TSS/cryptex 研究（如 cryptsn0w 项目）在 Apple 修补底层漏洞后即告失效，说明此类利用的生命周期非常短暂。

telegram · zaihuapd · 10月17日 10:34

**背景**: 越狱指突破 iOS 的沙盒与代码签名限制，以高权限运行未签名代码；其中 untethered（不完美/完全脱离）越狱在重启后仍能保持，无需借助电脑重新激活，自 2015 年的 iOS 9 之后已十分罕见。cryptex 是 Apple 用于分发系统组件和带特定权限应用的签名加密磁盘镜像容器；TSS（Tatsu 签名服务器）则是 Apple 按设备签发签名 blob 的服务器，确保只有 Apple 认可的固件才能启动。PAC 是 ARM 的指针认证机制，会对内存中的指针进行签名，因此劫持控制流必须伪造或绕过这些签名。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/0xjohnnydev/cryptsn0w?v=2">GitHub - 0xjohnnydev/cryptsn0w: Obsolete iOS jailbreak ...</a></li>

</ul>
</details>

**标签**: `#iOS jailbreak`, `#mobile security`, `#exploit chain`, `#Apple`, `#PAC bypass`

---

<a id="item-2"></a>
## [DeepSeek 发布 V4.1-Flash-1017：主打速度的开源模型称霸编码基准](https://huggingface.co/deepseek-ai/DeepSeek-V4.1-Flash-1017) ⭐️ 8.0/10

DeepSeek 发布了 DeepSeek-V4.1-Flash-1017，将模型权重上传至 Hugging Face，并在其 API 文档站点发布说明，同时在 OpenRouter 上线供第三方服务商提供推理。在自家新闻页上，DeepSeek 声称该版本在多数编码基准上显著高于竞品，据称在 11 项基准中的 10 项上超过了 Sol 5.6。 这次发布进一步印证了开发者选择模型的标准正在变化：相比单纯的基准分数，吞吐量、首 token 延迟、价格以及模型行为的开放程度更受重视，这也是多位评论者表示正把日常编码工作迁回 DeepSeek 的原因。在围绕监管门槛与生态多样性的争论升温之际，它也为市场提供了一个强有力的开放权重替代方案。 这些基准成绩来自 DeepSeek 自家的新闻页，而非独立第三方评测，因此其编码能力领先的说法目前仍应视为厂商自述。DeepSeek-V4.1-Flash 被描述为一个多模态混合专家（MoE）模型，主干参数规模为 552B，支持最高一百万 token 的上下文，并在 DeepSeek 官方平台上提供非高峰时段折扣定价。

hackernews · theykk · 10月17日 08:21 · [社区讨论](https://news.ycombinator.com/item?id=50129045)

**背景**: DeepSeek-V4.1-Flash 属于混合专家（MoE）模型家族，这类架构在处理每个 token 时只激活总参数中的一小部分，因此在参数规模极大的情况下仍能保持推理成本低、速度快。讨论中最受关注的两个指标是每秒生成 token 数（tok/s，即生成吞吐量）与首 token 延迟（TTFT，即开始输出前的等待时间），它们直接决定了一个智能体在编辑器里用起来是否顺手。另一个主题是开放程度：DeepSeek 公开可下载的模型权重（这属于“开放权重”，与完全开源并不等同，因为训练代码和数据通常不公开），并允许查看思维链（chain-of-thought，即模型的中间推理过程），而部分商业厂商会隐藏或过滤这部分内容。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.promptquorum.com/local-llms/open-weight-vs-open-source-ai-models">Open Weight vs Open Source AI Models 2026: Key Differences</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上的讨论整体偏正面但相当理性：评论者承认 DeepSeek 在基准上并未明显胜过 Sol 和 Gemini，但认为其更高的 tok/s、更低的 TTFT 以及不被随意拦截的可见思维链，让它在实际使用中体验更好。多位开发者表示如今大部分编码工作都交给 DeepSeek-Flash，只把 Claude 或 Sol 留给方案规划与代码审查；也有人把这款模型视为“多元生态优于监管门槛”的证据。

**标签**: `#LLM`, `#DeepSeek`, `#model-release`, `#benchmarks`, `#AI-ecosystem`

---

<a id="item-3"></a>
## [OpenCode 遭蒸馏攻击，OpenAI、Anthropic 与 Google API 密钥外泄](https://startupfortune.com/opencode-breach-exposes-stored-openai-and-anthropic-keys-prompts-urgent-key-rotation/) ⭐️ 8.0/10

OpenCode 证实，一起大规模蒸馏攻击导致约 1.4% 的 Console 用户所存储的 OpenAI、Anthropic 和 Google API 密钥被曝光，受影响账户已通过邮件收到通知。公司表示正在与这三家模型厂商协同处置，目前尚无法确认泄露的密钥是否已被恶意使用。 密钥泄露的用户面临未授权 API 消费、配额被耗尽以及潜在的数据暴露风险，对于通过第三方 LLM 网关转发编程智能体流量的开发者而言，这是一次切实的运营风险。该事件也凸显了一类新型攻击：攻击者滥用 API 访问权限来攫取模型行为，而非窃取传统意义上的用户数据。 OpenCode 建议受影响用户在对应平台后台吊销并重新签发密钥，检查 10 月 17 日以来的用量记录，并设置支出上限以限制进一步损失。官方通知未说明密钥的存储方式或外泄途径，因此除 1.4% 这一比例之外的实际影响范围仍不明确。

telegram · zaihuapd · 10月17日 23:43

**背景**: 蒸馏攻击是指攻击者大规模调用专有模型，收集其输出（有时还包括推理过程），再用这些数据训练一个更廉价的仿制模型，厂商通常将其视为违反服务条款的行为。OpenCode 是一个开源的终端/IDE 编程智能体，支持 OpenAI、Anthropic 和 Gemini 等模型，其 Console 允许用户存储各厂商的 API 密钥，以便智能体代为调用这些模型。凭据集中存放在服务端，使这类平台成为极具吸引力的攻击目标——一旦被攻破，就能一次性获得多家厂商的密钥。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.anthropic.com/news/detecting-and-preventing-distillation-attacks">Detecting and preventing distillation attacks \ Anthropic</a></li>
<li><a href="https://securityarsenal.com/blog/openai-distillation-attack-defending-llm-apis-against-model-extraction-and-encryption-bypass">OpenAI Distillation Attack: Defending LLM APIs Against Model ...</a></li>

</ul>
</details>

**标签**: `#security-breach`, `#api-keys`, `#llm-infrastructure`, `#opencode`, `#incident-response`

---