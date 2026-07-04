---
layout: default
title: "Horizon Summary: 2026-07-04 (ZH)"
date: 2026-07-04
lang: zh
---

> 从 47 条内容中筛选出 9 条重要资讯。

---

1. [欧盟议会间谍软件调查员遭飞马间谍软件入侵](#item-1) ⭐️ 9.0/10
2. [SearXNG：一个专注于隐私的元搜索引擎，适用于 AI 代理](#item-2) ⭐️ 8.0/10
3. [Wordgard: ProseMirror 作者发布的新富文本编辑器](#item-3) ⭐️ 8.0/10
4. [CDD 仅通过 logits 恢复微调数据的逐字内容](#item-4) ⭐️ 8.0/10
5. [H64LM：从头构建的 2.49 亿参数 MoE Transformer](#item-5) ⭐️ 8.0/10
6. [Claude Fable 5 重上线遇冷：用量缩减、安全误判频发](#item-6) ⭐️ 8.0/10
7. [华为发布 Atlas 350 加速卡，性能达 H20 的 2.87 倍](#item-7) ⭐️ 8.0/10
8. [阿里因滥用指控下令全员卸载 Claude](#item-8) ⭐️ 8.0/10
9. [腾讯阿图因 AI 以 0.1%成本在 CyberGym 测试中超越 Claude Mythos](#item-9) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [欧盟议会间谍软件调查员遭飞马间谍软件入侵](https://citizenlab.ca/research/member-of-committee-investigating-spyware-hacked-with-pegasus/) ⭐️ 9.0/10

公民实验室发现，一名参与调查间谍软件的欧洲议会议员的设备在 2022 年和 2023 年多次感染飞马间谍软件，表明有国家行为者在多个欧洲国家协调实施监控行动。 这一事件直接威胁到欧盟机构的完整性以及调查监控滥用的立法者的安全，突显出加强网络安全保护和商业间谍软件监管的紧迫性。 感染发生在 2022 年 10 月 21 日以及 2023 年 3 月 6 日至 7 日，第一次感染与一场针对欧洲俄语和白俄罗斯语流亡者的飞马行动相吻合，暗示一个获得授权在多个欧盟国家操作的飞马客户。

hackernews · ledoge · 7月3日 20:38 · [社区讨论](https://news.ycombinator.com/item?id=48779683)

**背景**: 飞马是由以色列 NSO 集团开发的强大间谍软件，能够远程侵入移动设备而无需用户交互。它被各国政府广泛用于监视记者、活动家和政治家。公民实验室是多伦多大学的一个领先研究小组，追踪数字威胁和间谍软件滥用。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Pegasus_(spyware)">Pegasus (spyware)</a></li>
<li><a href="https://en.wikipedia.org/wiki/Citizen_Lab">Citizen Lab</a></li>
<li><a href="https://citizenlab.ca/">The Citizen Lab - The Citizen Lab</a></li>

</ul>
</details>

**社区讨论**: 评论引发了对授权问题的关注：一位用户质疑哪个实体有权在多个欧洲国家进行间谍活动，另一位则指出希腊正在进行的飞马丑闻牵连到总理办公室。还有人提到，一些欧盟国家因滥用问题已被以色列公司切断飞马合作关系。

**标签**: `#Pegasus`, `#spyware`, `#surveillance`, `#European Parliament`, `#cybersecurity`

---

<a id="item-2"></a>
## [SearXNG：一个专注于隐私的元搜索引擎，适用于 AI 代理](https://github.com/searxng/searxng) ⭐️ 8.0/10

SearXNG 是一个免费、开源的元搜索引擎，它聚合多个搜索服务的结果而不追踪用户，并且越来越多地被用于本地 AI 和代理应用中，以提供私有的搜索能力。 随着对隐私和数据收集的担忧加剧，SearXNG 提供了一种自托管的替代方案来取代集中式搜索引擎，并且它与本地 AI 代理的集成使得无需依赖外部服务即可实现私有的、使用工具的 AI。 SearXNG 支持 JSON 输出，使其适合 AI 代理的程序化使用，并且可以通过 Docker 本地运行。然而，用户可能会遇到较慢的结果以及来自上游搜索引擎的偶尔验证码挑战。

hackernews · theanonymousone · 7月3日 20:15 · [社区讨论](https://news.ycombinator.com/item?id=48779454)

**背景**: 元搜索引擎是一种同时查询多个搜索引擎并合并其结果的搜索工具。SearXNG 是原始 Searx 项目的分支，后者开创了注重隐私的元搜索。它是一款自由软件，不收集用户数据，吸引了注重隐私的用户和自托管 AI 系统的开发者。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/SearXNG">SearXNG - Wikipedia</a></li>
<li><a href="https://github.com/searxng/searxng">GitHub - searxng/searxng: SearXNG is a free internet ...</a></li>
<li><a href="https://en.wikipedia.org/wiki/Metasearch_engine">Metasearch engine</a></li>

</ul>
</details>

**社区讨论**: 评论突出了实际使用情况：原始 Searx 的创建者提到了他的新项目 Hister，原因是元搜索的局限性，而用户分享了像 TinySearch 这样的 AI 代理集成，并指出了速度较慢和验证码问题等权衡。总体而言，社区重视 SearXNG 的隐私保护，但也承认其性能上的不足。

**标签**: `#privacy`, `#metasearch`, `#open-source`, `#AI tools`, `#self-hosted`

---

<a id="item-3"></a>
## [Wordgard: ProseMirror 作者发布的新富文本编辑器](https://wordgard.net/) ⭐️ 8.0/10

Wordgard 是由 ProseMirror 的创建者 Marijn Haverbeke 发布的一款新的浏览器内富文本编辑器，旨在通过轻量级、可访问的工具简化内容编辑。 Wordgard 代表了富文本编辑的重要演进，融合了 ProseMirror 多年开发的经验，可能影响未来的网络编辑标准。 Wordgard 与 ProseMirror 共享许多概念，但未提供升级路径，因此切换需要大量工作。它仍处于早期开发阶段（版本 0.1）。

hackernews · indy · 7月3日 08:50 · [社区讨论](https://news.ycombinator.com/item?id=48772573)

**背景**: ProseMirror 是一个广泛使用的富文本编辑器框架，以其灵活性和性能著称，但学习曲线陡峭。Wordgard 是结合了 ProseMirror 和 CodeMirror 6 经验的新一代编辑器，旨在提供更简单的 API 和更好的可访问性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://marijnhaverbeke.nl/blog/wordgard-0.1.html">Wordgard Release 0.1</a></li>
<li><a href="https://prosemirror.net/">ProseMirror</a></li>
<li><a href="https://grokipedia.com/page/ProseMirror">ProseMirror</a></li>

</ul>
</details>

**社区讨论**: 社区讨论总体积极，称赞其设计和技术洞察。一些用户对创建新编辑器的原因表示兴趣，并指出从 ProseMirror 迁移需要大量重构。另一些人欣赏其深思熟虑的设计，并认为这验证了他们自己的方法。

**标签**: `#rich-text editor`, `#ProseMirror`, `#Wordgard`, `#JavaScript`, `#web development`

---

<a id="item-4"></a>
## [CDD 仅通过 logits 恢复微调数据的逐字内容](https://www.reddit.com/r/MachineLearning/comments/1umn2dk/contrastive_decoding_diffing_cdd_recovering/) ⭐️ 8.0/10

对比解码差异分析（CDD）是一种新颖的灰盒方法，仅通过 logits 访问即可从微调的大型语言模型中恢复逐字的训练数据，无需模型权重或激活值。 该方法解决了先前白盒方法（如激活差异透镜 ADL）的局限性，后者需要完全权重访问且仅能恢复领域级描述。CDD 在 20 个模型对中的 19 个上达到了 4+/5 的逐字恢复评分，使其成为微调模型可解释性和安全审计的强大工具。 单一默认配置在四个模型家族（1B 到 32B 参数）上有效，无需每项校准或层选择。一个意外发现是，恢复的文本中频繁出现 'Dr. Elena Rodriguez' 这个名字，因为 Claude Sonnet 3.6 在生成合成数据时过度偏好该名字，这表明 LLM 生成的训练数据可能嵌入伪影。

reddit · r/MachineLearning · /u/CebulkaZapiekana · 7月3日 19:01

**背景**: 对比解码（CD）是一种通过对比大模型和小模型的 log 概率来改进文本生成的技术。模型差异分析（Model diffing）指比较模型以识别差异，常用于检测微调模型中的安全相关行为。先前的工作如激活差异透镜（ADL）需要白盒访问激活差异，限制了其实用性。CDD 将对比解码扩展到模型差异分析场景，仅需 logits 访问。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/2210.15097">Contrastive Decoding: Open-ended Text Generation as Optimization</a></li>
<li><a href="https://github.com/MadryLab/modeldiff">GitHub - MadryLab/modeldiff: ModelDiff: A Framework for ... MODELDIFF: A Framework for Comparing Learning Algorithms Model Diffing — LessWrong GitHub - yuanchun-li/ModelDiff [2602.11729] Cross-Architecture Model Diffing with ...</a></li>

</ul>
</details>

**标签**: `#machine learning`, `#interpretability`, `#model diffing`, `#LLM safety`, `#contrastive decoding`

---

<a id="item-5"></a>
## [H64LM：从头构建的 2.49 亿参数 MoE Transformer](https://www.reddit.com/r/MachineLearning/comments/1umqfd2/h64lm_a_249mparameter_mixtureofexperts/) ⭐️ 8.0/10

一位开发者发布了 H64LM，这是一个用 PyTorch 从零实现的 2.49 亿参数混合专家（MoE）Transformer，包含自定义注意力、MoE 路由和归一化，未使用高级训练框架。该模型在 WikiText-103 上作为概念验证进行训练，验证困惑度约为 40.5。 该项目提供了现代 LLM 组件的教育性透明实现，帮助从业者理解 MoE Transformer、分组查询注意力（GQA）和辅助路由损失。虽然不是最先进的模型，但它是一个有价值的学习和实验资源。 H64LM 采用分组查询注意力（GQA）、8 个专家和 Top-2 路由、SwiGLU 激活函数、RoPE、RMSNorm 和滑动窗口注意力。局限性包括仅支持批次大小为 1 的生成，以及使用 DataParallel 而非真正的分布式数据并行（DDP）。

reddit · r/MachineLearning · /u/Loose_Literature6090 · 7月3日 21:18

**背景**: 混合专家（MoE）是一种用多个“专家”子网络和路由机制替换密集前馈层的技术，能以更少计算量训练更大模型。分组查询注意力（GQA）通过在查询头组间共享键/值头来平衡效率与质量。SwiGLU 是一种门控激活函数，可改善现代 LLM 的训练动态。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Mixture_of_experts">Mixture of experts - Wikipedia</a></li>
<li><a href="https://huggingface.co/blog/moe">Mixture of Experts Explained</a></li>
<li><a href="https://www.geeksforgeeks.org/deep-learning/grouped-query-attention-gqa/">Grouped Query Attention (GQA) - GeeksforGeeks</a></li>

</ul>
</details>

**标签**: `#PyTorch`, `#Mixture-of-Experts`, `#Transformer`, `#LLM`, `#research`

---

<a id="item-6"></a>
## [Claude Fable 5 重上线遇冷：用量缩减、安全误判频发](https://www.bleepingcomputer.com/news/artificial-intelligence/claude-fable-relaunch-disappoints-users-with-nerfed-performance/) ⭐️ 8.0/10

美国解除出口管制后，Anthropic 的 Claude Fable 5 重新上线，但用户反映使用额度大幅缩减，安全过滤机制过于敏感，在处理涉及漏洞或 hook 的代码时，模型会自动降级至 Opus 4.8。 该事件凸显了高性能 AI 模型在安全对齐与实用价值之间的权衡。依赖 Claude 进行代码审查和安全分析的开发者面临严重干扰，可能损害对 Anthropic 部署策略的信心。 在 7 月 7 日前，Pro 和 Max 订阅用户每周仅能使用 50% 的配额调用 Fable 5；此后订阅中将不再包含 Fable 5，需按量付费。模型底层能力未变，但安全防护机制导致频繁误降级。

telegram · zaihuapd · 7月3日 07:20

**背景**: Claude Fable 5 是 'Mythos 级'模型的公开安全版本，与最初因安全顾虑而被限制的 Claude Mythos 共享底层架构。Anthropic 采用宪法 AI 来确保模型行为符合伦理。Opus 4.8 是较小、能力较弱的模型，当安全过滤被触发时作为降级替代。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Claude_Fable_5">Claude Fable 5</a></li>
<li><a href="https://www.anthropic.com/news/claude-fable-5-mythos-5">Claude Fable 5 and Claude Mythos 5 \ Anthropic</a></li>

</ul>
</details>

**标签**: `#AI`, `#Anthropic`, `#Claude`, `#Safety`, `#LLM`

---

<a id="item-7"></a>
## [华为发布 Atlas 350 加速卡，性能达 H20 的 2.87 倍](https://t.me/zaihuapd/42329) ⭐️ 8.0/10

在华为中国合作伙伴大会 2026 上，华为正式发布并开始出货搭载全新昇腾 950PR 处理器的 Atlas 350 AI 加速卡，声称其算力达到英伟达 H20 的 2.87 倍。 这一发布标志着华为在 AI 硬件上的最大突破，直接挑战英伟达在中国市场的主导地位。Atlas 350 支持 FP4 推理和 112GB HBM，可能以更低成本实现大规模 AI 部署，并减少对外国芯片的依赖。 昇腾 950PR 提供 1 PFLOPS FP8 性能，支持 FP4 低精度推理，并配备 112GB 自研 HBM。Atlas 350 可单卡加载 70B 参数模型，大幅降低推理延迟与投资成本。

telegram · zaihuapd · 7月3日 08:35

**背景**: FP4（4 位浮点）是一种超低精度数据格式，在保持模型精度的同时加速推理，在 AI 硬件中日益流行。HBM（高带宽内存）是一种 3D 堆叠 DRAM 技术，为 AI 工作负载提供巨大带宽。华为的昇腾系列是中国主要的 AI 芯片产品线，而英伟达 H20 是由于美国出口限制而性能削减的中国特供版。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://tech-insider.org/huawei-ascend-950pr-ai-chip-nvidia-china-2026/">Huawei Ascend 950PR: The 1.56 PFLOP AI Chip vs Nvidia [2026]</a></li>
<li><a href="https://www.huaweicentral.com/ascend-950pr-ai-chip-everything-you-need-to-know/">Ascend 950PR AI Chip: Everything you need to know</a></li>
<li><a href="https://nerdleveltech.com/huawei-ascend-950pr-atlas-350-ai-chip-challenges-nvidia">Huawei Ascend 950PR Beats NVIDIA H20: 2.8× FP8, CUDA-Ready</a></li>

</ul>
</details>

**标签**: `#Huawei`, `#AI accelerator`, `#hardware`, `#Ascend`, `#Nvidia H20`

---

<a id="item-8"></a>
## [阿里因滥用指控下令全员卸载 Claude](https://t.me/zaihuapd/42334) ⭐️ 8.0/10

阿里巴巴内部下令要求所有员工卸载 Anthropic 旗下的 Claude 及相关产品，包括 Sonnet、Opus、Fable 模型及 Claude Code 等 Agent 产品，禁令将于 7 月 10 日生效。此前 Anthropic 指控阿里在 4 月 22 日至 6 月 5 日期间使用了约 2.5 万个虚假账号与 Claude 进行了超过 2800 万次交互。 这一事件凸显了主要 AI 公司在系统性滥用 AI 服务问题上日益紧张的局势，可能重塑企业 AI 使用政策。它还引发了关于大型科技公司如何管理内部对竞争性 AI 工具的访问并执行合规的思考。 阿里此前曾报销员工使用 Claude、GPT、Gemini 等外部模型的费用。此次禁令不仅涵盖聊天模型，还包括 Claude Code 等 Agent 产品——Claude Code 是一款集成在终端和 IDE 中的 AI 编程助手。

telegram · zaihuapd · 7月3日 13:00

**背景**: Claude 是由美国公司 Anthropic 开发的一系列大语言模型，以其“宪法 AI”（constitutional AI）安全方法著称。阿里巴巴是中国电商和云计算巨头，鼓励员工利用外部 AI 工具提高生产力。使用虚假账号的指控暗示了系统性爬取或未授权批量访问，Anthropic 随后收紧了风控策略。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Claude_Code">Claude Code</a></li>
<li><a href="https://claude.com/product/claude-code">Claude Code by Anthropic | AI Coding Agent, Terminal, IDE</a></li>
<li><a href="https://platform.claude.com/docs/en/about-claude/models/overview">Models overview - Claude Platform Docs</a></li>

</ul>
</details>

**标签**: `#AI policy`, `#Alibaba`, `#Anthropic`, `#corporate security`, `#AI abuse`

---

<a id="item-9"></a>
## [腾讯阿图因 AI 以 0.1%成本在 CyberGym 测试中超越 Claude Mythos](https://mp.weixin.qq.com/s/BzU7g-2iG7d6h4ViwMhxyg) ⭐️ 8.0/10

腾讯玄武实验室的阿图因 AI 基于开源模型 GLM-5.1，在 CyberGym 网络安全基准测试中获得 84.0%的得分，超越 Anthropic 的 Claude Mythos Preview。它还在 curl、OpenSSL 等重要开源项目中发现了多个 Mythos 未检出的高危逻辑漏洞，严重程度最高达 9.3。 这表明较小的开源模型能够以极低的成本在网络安全漏洞检测方面媲美甚至超越专有 AI。这有望推动 AI 驱动的安全测试普及，减少对昂贵商业解决方案的依赖。 阿图因 AI 消耗的预算不到 Mythos「玻璃翼计划」的 0.1%。在伯克利 BVI 真实世界漏洞榜单中，阿图因 AI 的严重漏洞严重程度排名第一，总数排名第五。

telegram · zaihuapd · 7月3日 16:12

**背景**: CyberGym 是加州大学伯克利分校开发的大规模网络安全评估基准，通过 188 个项目中的 1507 个历史漏洞考验 AI 代理的真实漏洞分析能力。GLM-5.1 是智谱 AI 推出的开源大语言模型，可本地部署，支持长时间自主任务。Claude Mythos Preview 是 Anthropic 在「玻璃翼计划」中使用的 AI 模型，曾在主要软件中发现了数千个零日漏洞。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.cybergym.io/cybergym/">CyberGym: Evaluating AI Agents' Real-World Cybersecurity ...</a></li>
<li><a href="https://deepinfra.com/blog/glm-5-1-model-overview">GLM-5.1 Model Overview: Features, Capabilities & Use Cases</a></li>
<li><a href="https://www.anthropic.com/glasswing">Project Glasswing: Securing critical software for the AI era \ Anthropic</a></li>

</ul>
</details>

**标签**: `#AI`, `#cybersecurity`, `#vulnerability detection`, `#benchmark`, `#GLM-5.1`

---