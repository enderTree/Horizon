---
layout: default
title: "Horizon Summary: 2026-11-16 (ZH)"
date: 2026-11-16
lang: zh
---

> 从 38 条内容中筛选出 3 条重要资讯。

---

1. [uBlock Origin 元素选择器被网站驱动，导致通用 XSS 漏洞](#item-1) ⭐️ 8.0/10
2. [Qwen4-Max 发布：阿里新一代旗舰多模态模型](#item-2) ⭐️ 8.0/10
3. [Meta FAIR 与 NYU：视觉编码器预训练可选，但视觉专属参数不可或缺](#item-3) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [uBlock Origin 元素选择器被网站驱动，导致通用 XSS 漏洞](https://iter.ca/post/ubo-uxss/) ⭐️ 8.0/10

一位安全研究者披露了 uBlock Origin 中的一个通用 XSS（UXSS）漏洞，其成因是恶意网站能够操控该扩展的交互式元素选择器。该漏洞已被修复，社区成员提醒用户应升级到 uBlock Origin 1.75.4 或 uBO Lite 2026.1110.1816 及以上版本。 uBlock Origin 是部署最广泛的浏览器扩展之一，因此其中的 UXSS 漏洞可能让恶意页面借助扩展的高权限在任意网站上执行脚本，突破通常保护用户的同源边界。由于该利用是由普通网页内容驱动、而非需要特殊的攻击条件，其影响范围覆盖 Firefox 与 Chromium 上极其庞大的装机量。 根因属于架构层面：元素选择器的界面被注入到页面自身的 DOM 中，以便高亮和选取页面元素，这也意味着恶意页面脚本与选择器界面共享同一 DOM 上下文。缓解措施包括升级到已修复的版本，以及对强化配置的 Firefox 用户重建配置文件，避免残留存在漏洞的扩展状态。

hackernews · zaik · 11月16日 02:04 · [社区讨论](https://news.ycombinator.com/item?id=50513160)

**背景**: 通用 XSS（UXSS）与普通 XSS 不同：它并非利用某个网站输入处理不当的缺陷，而是利用浏览器或扩展本身，使脚本能在任意网站上执行，从而实质性地绕过同源策略。uBlock Origin 的元素选择器是一项让用户点击页面元素、进而生成永久隐藏该元素的装饰性或网络过滤规则的功能；为了实现这种交互，它会将自己的界面覆盖在正在浏览的页面上。uBO 这类扩展拥有远超页面脚本的权限，因此任何允许页面影响该注入界面的途径，都是对信任边界的严重破坏。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Universal_XSS">Universal XSS</a></li>
<li><a href="https://aszx87410.github.io/beyond-xss/en/ch2/universal-xss/">The Most Powerful XSS : Universal XSS | Beyond XSS</a></li>
<li><a href="https://github.com/gorhill/uBlock/wiki/Element-picker">Element picker · gorhill/uBlock Wiki · GitHub</a></li>

</ul>
</details>

**社区讨论**: 评论者聚焦于架构层面的根因，质疑为何选择器界面不能直接放在浏览器自身界面（browser chrome）中，而非页面 DOM 里。也有人指出密码管理器的自动填充下拉框存在同样问题，可能向监听新 DOM 节点的页面泄露用户的账号列表；还有多位读者给出了具体的修复建议，例如核对版本号、重建全新的 Firefox 配置文件。

**标签**: `#security`, `#xss`, `#browser-extensions`, `#uBlock-Origin`, `#web-security`

---

<a id="item-2"></a>
## [Qwen4-Max 发布：阿里新一代旗舰多模态模型](https://qwen.ai/blog?id=qwen4-max) ⭐️ 8.0/10

阿里巴巴发布了 Qwen 4 系列的旗舰模型 Qwen4-Max，支持文本、图像与视频输入并输出文本，配备约 100 万 token 的上下文窗口，且默认开启推理功能。该模型提供 none、low、high、xhigh 四档可选的推理强度，发布后在 Hacker News 上引发了大量讨论。 Qwen 是使用最广泛的模型家族之一，因此新的旗舰版本会直接影响在其之上构建编程助手、前端设计工具和智能体工作流的开发者。讨论的焦点也转向更严峻的竞争问题：不仅是基准跑分，还有与 OpenAI、Anthropic 闭源前沿模型相比的单任务成本和推理服务速度。 Artificial Analysis 给出的 Qwen4-Max 智能得分为 43，平均成本约 3.27 美元；有评论者指出 GPT-6.1 Sol 中等推理强度得分 46，平均成本仅约 0.36 美元，效率差距明显。社区成员还提到推理吞吐问题（有人称 Qwen 3.8 约为每秒 30 个 token，而 Opus 接近每秒 80 个），并指出 OpenRouter 上架了 qwen3.8-max-prime、qwen3.8-max-0902 等价格与速度各异的变体。

hackernews · ilreb · 11月16日 02:14 · [社区讨论](https://news.ycombinator.com/item?id=50513215)

**背景**: Qwen 是阿里巴巴的大语言模型家族，按代际迭代（Qwen 3、3.8，如今是 Qwen 4），包含旗舰的 “Max” 档以及更小更快的 “Flash” 变体。“推理强度”（reasoning effort）是一种控制参数，让调用方用额外的推理开销和延迟换取回答前更多的思考，这一模式因使用可验证奖励强化学习训练的推理模型而流行。Artificial Analysis 是一家独立评测机构，会把质量分数与价格数据并列展示，因此评论者常用它来比较模型的性价比，而不只是看能力上限。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://artificialanalysis.ai/models/qwen4-max">Qwen 4 Max - Intelligence, Performance & Price... | Artificial Analysis</a></li>
<li><a href="https://openrouter.ai/qwen/qwen4-max">Qwen 4 Max - API Pricing & Providers | OpenRouter</a></li>
<li><a href="https://www.qwencloud.com/models/qwen4-max?region=ap-southeast-1">Qwen 4 - Max - QwenCloud</a></li>

</ul>
</details>

**社区讨论**: Hacker News 的评论呈现热情与质疑并存的态势：有人赞赏其继续兼顾效率与质量，并期待 Flash 和 27B 版本；也有人质疑推理速度是否已成为瓶颈——一位开发者称，Qwen 在其智能体竞技场中得分偏低主要是因为 “太慢了”。另一个反复出现的担忧是，每次发布后开源权重生态是否正在被 Anthropic 和 OpenAI 越拉越远。

**标签**: `#Qwen`, `#LLM`, `#AI models`, `#benchmarking`, `#inference cost`

---

<a id="item-3"></a>
## [Meta FAIR 与 NYU：视觉编码器预训练可选，但视觉专属参数不可或缺](https://www.reddit.com/r/MachineLearning/comments/1xx1k2o/meta_fair_nyu_unbundling_multimodal_vision/) ⭐️ 8.0/10

Meta FAIR 与 NYU 完全从零训练了 200 多个多模态大语言模型，使用相同数据，并把编码器预训练计入同一份“全生命周期”算力预算，从而把三个通常被混在一起的设计选择分别拆开检验。结论是：独立的视觉编码器预训练是可选的（四种预训练编码器在同等算力下最多只能与从零训练的编码器打平）；视觉专属参数是必需的（无编码器模型在 0.6B 到 6.4B 每个规模上都落后，需要约 3 倍算力才能追平）；把视觉能力放在 LLM 之前也是可选的，其“in-fusion”方案在 1.7B 到 6.4B 上与标准编码器持平。 当前前沿实验室在视觉编码器上分歧明显：Gemma 4 12B 去掉了编码器，Kimi K3 从零训练编码器，而 Inkling 2 Small 又把编码器加了回来；但已发布模型在数据和算力上各不相同，直接比较无法分离出单一选择的影响。这项受控消融实验为模型开发者提供了证据：昂贵的编码器预训练阶段和独立编码器模块有可能被省去而不损失 VQA 质量，从而简化多模态模型配方并降低训练成本。 主要对比使用 Qwen3-1.7B 和 4B 主干、0.4B 视觉容量参数，并覆盖 0.6B 到 6.4B 的规模阶梯，在 16 个 Cambrian VQA 基准（448 像素）和 12 个语言基准上评测。值得注意的是，把 MetaCLIP 预训练延长 6.5 倍使 ImageNet 线性探针准确率从 80.4% 提升到 84.4%，却未带来 VQA 提升；在 1.7B 规模下，in-fusion 把视觉专属分支放在第 1–8 层可达到 45.0 VQA，而标准编码器为 44.4，文本共享这些参数时为 42.3，放在最后 8 层时仅 35.1，同时首 token 延迟降低约 13%。

reddit · r/MachineLearning · /u/trungh98 · 11月15日 17:38

**背景**: 典型的多模态大语言模型由三部分组成：一个视觉编码器（通常是使用 CLIP、MetaCLIP 等对比学习目标预训练的 ViT），负责把图像切成 patch 并生成嵌入；一个连接器，把视觉嵌入投影到语言模型的特征空间；以及 LLM 主干本身。这一设计其实捆绑了三个独立决策——编码器是否要有自己的上游预训练、视觉 token 是否使用专属参数、以及这部分容量是否放在 LLM 之前——而以往研究很少把它们拆开。VQA（视觉问答）基准衡量模型能否回答关于图像的问题，ImageNet 线性探针准确率衡量冻结编码器特征的线性可分性，首 token 延迟（TTFT）则是推理延迟指标。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/papers/date/2026-11-13">Daily Papers - Hugging Face</a></li>
<li><a href="https://github.com/gokayfem/awesome-vlm-architectures">GitHub - gokayfem/awesome-vlm- architectures : Curated visual...</a></li>
<li><a href="https://www.emergentmind.com/topics/mllm">MLLM : Architecture , Adaptation, & Applications</a></li>

</ul>
</details>

**标签**: `#multimodal-learning`, `#vision-encoders`, `#MLLM`, `#pretraining`, `#scaling-laws`

---