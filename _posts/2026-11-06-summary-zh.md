---
layout: default
title: "Horizon Summary: 2026-11-06 (ZH)"
date: 2026-11-06
lang: zh
---

> 从 42 条内容中筛选出 7 条重要资讯。

---

1. [Alpine 上的 OpenSSH 密码认证绕过，根源在于 musl crypt() 的哨兵哈希值](#item-1) ⭐️ 9.0/10
2. [SemiAnalysis：谷歌 TPU 成为英伟达 CUDA 之外可行的推理替代方案](#item-2) ⭐️ 8.0/10
3. [Hugging Face 发布 Megatron-LM 训练 MoE 模型实用手册](#item-3) ⭐️ 8.0/10
4. [美国放行 H200 对华销售，约 10 家中国企业获准采购](#item-4) ⭐️ 8.0/10
5. [谷歌向开发者开放 Nano Banana 2 Lite 与 Gemini Omni Flash](#item-5) ⭐️ 8.0/10
6. [OpenAI 开始在 ChatGPT 中测试广告，面向免费及 Go 用户](#item-6) ⭐️ 8.0/10
7. [百度发布文心 5.0 全模态大模型，参数规模达 2.4 万亿](#item-7) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Alpine 上的 OpenSSH 密码认证绕过，根源在于 musl crypt() 的哨兵哈希值](https://sshhole.com/) ⭐️ 9.0/10

一个编号为 CVE-2026-123158、被戏称为“sshole”的 OpenSSH 密码认证绕过漏洞，使得当 sshd 运行在 musl libc 上（例如 Alpine Linux）时，攻击者无需知道密码即可登录。musl 的 crypt() 在失败时（例如密码过长）会返回哨兵字符串“*”，而 sshd 会把该返回值与 /etc/shadow 中存储的密码字段进行比较；对于被锁定或无密码的账户，该字段本身就是“*”或“!”，于是比较错误地判定为通过。 OpenSSH 是当今部署最广泛的安全基础设施之一，因此 sshd 中出现认证绕过属于范式级别的安全事件，可能让任何基于 musl 的主机——包括大量容器镜像、嵌入式设备以及基于 Alpine 的云部署——面临未认证的远程访问风险。该事件也严厉拷问了那种用“*”这类魔法字符串同时表示“无密码”和“哈希失败”的做法。 glibc 系统基本不受影响，因为它们使用 libxcrypt，失败时返回“*0”，比较不成立从而拒绝登录；易受攻击的路径仅限于 musl。Alpine 的安全公告指出，受影响的是那些没有任何账户使用 $ 开头密码哈希的配置（例如常将 PasswordAuthentication 设为 no 的 cloud-init 镜像），修复方式是升级 openssh 至 10.6p2 并重启 sshd，临时缓解措施则是把 PasswordAuthentication 设为 no。

hackernews · josemrb · 11月5日 12:19 · [社区讨论](https://news.ycombinator.com/item?id=50378228)

**背景**: 在 Unix 系统中，/etc/shadow 以哈希字符串形式保存每个账户的密码，其前缀标明算法（例如 $6$ 表示 SHA-512），sshd 验证登录时会用用户提交的密码和存储的哈希作为参数调用 crypt()，并检查返回值是否等于存储值。那些本不应能通过密码登录的账户，该字段通常不是哈希而是“*”或“!”。而 Alpine Linux 使用的 C 标准库 musl 在 crypt() 失败时会刻意返回一个无法匹配的哈希字符串而非 NULL，这一设计选择把哈希错误变成了可能意外匹配锁定账户字段的值。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.ox.security/blog/openssh-authentication-bypass-cve-2026-123158/">OpenSSH Bypass : CVE-2026-123158 | OX Security</a></li>
<li><a href="https://alpinelinux.org/posts/2026-11-05-openssh-password-authentication-bypass/">Security advisory: openssh -server password authentication bypass</a></li>
<li><a href="https://git.musl-libc.org/cgit/musl/commit/?id=b3c4cc121f70faea45389fe7ddc1127ed5cbd8bb">musl - musl - an implementation of the standard library for...</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上的讨论（约 2500 分、600 多条评论）更多是在追根溯源而非恐慌：有评论者完整梳理了 crypt() 与哈希值的比较过程，解释了为何锁定账户会被认证通过；也有人抨击用“*”作为哨兵值的带内信号设计；还有评论指出 musl 此前已在 crypt_des 中修补过这类失败模式，却漏掉了 crypt_sha 路径（而且已有的规避方案在盐值为“x”时本身也会出错）。另有观点对 musl 在缺乏应有审计的情况下对核心加密函数做“图方便”的改动表示失望。

**标签**: `#security`, `#openssh`, `#vulnerability`, `#authentication`, `#cryptography`

---

<a id="item-2"></a>
## [SemiAnalysis：谷歌 TPU 成为英伟达 CUDA 之外可行的推理替代方案](https://newsletter.semianalysis.com/p/tpu-strikes-the-king) ⭐️ 8.0/10

SemiAnalysis 发布深度分析文章，认为谷歌 TPU 在 AI 推理场景下已经成熟为英伟达 CUDA 护城河之外一个可行的替代方案，并称英伟达正对此威胁做出激烈回应。文章还梳理了周边软件生态，包括 TorchTPU、vLLM、SGLang、llm-d 和 Ray，并提及 Kimi K3、Qwen、GLM5.3 等一批新模型。 多年来 CUDA 的软件锁定让英伟达的利润率和市场份额几乎无人撼动，因此任何在 TPU 上可行且可信的推理替代方案都会直接冲击这一地位，并让大规模 AI 部署获得第二家供应商的选择。由于长期来看算力支出的大头预计在推理而非训练，即便 TPU 只获得部分采用，也可能改变整个 AI 基础设施栈的定价权与硬件选型。 该分析把这场竞争界定为软件栈之争而非单纯的芯片对比：TPU 过去主要依赖 XLA/JAX 编程，因此谷歌与 Meta 开源的 TorchTPU PyTorch 后端，以及对 vLLM、SGLang 和 Kubernetes 原生 llm-d 等推理引擎的支持，才让 TPU 对主流推理变得实用。值得注意的是，公开可见的文章版本只是预告，具体的基准测试数据和所声称的英伟达应对细节仅对付费订阅者开放。

rss · Semianalysis · 11月5日 19:03

**背景**: TPU（张量处理单元）是谷歌自研的 AI 加速器，通过谷歌云对外提供，与英伟达的通用 GPU 形成对照。英伟达真正的优势在于 CUDA——绝大多数 AI 软件都是针对这套专有编程模型和库生态编写的，使得更换硬件成本高昂。vLLM 和 SGLang 是开源的大模型推理服务引擎，通过分页注意力、前缀缓存等技术提升吞吐量，llm-d 则把它们扩展为分布式的 Kubernetes 原生服务栈；在 2026 年 PyTorch 大会上公布的 TorchTPU 则提供了原生 PyTorch 后端，使模型无需重写即可在 TPU 上运行。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://pytorch.org/blog/introducing-torchtpu/">Introducing TorchTPU - PyTorch</a></li>
<li><a href="https://cloud.google.com/blog/topics/ai-infrastructure/torchtpu-is-now-open-source-run-native-pytorch-on-tpus">TorchTPU is now open source: Run native PyTorch on TPUs</a></li>
<li><a href="https://llm-d.ai/">llm-d</a></li>

</ul>
</details>

**标签**: `#Google TPU`, `#NVIDIA CUDA`, `#AI inference`, `#AI infrastructure`, `#LLM serving`

---

<a id="item-3"></a>
## [Hugging Face 发布 Megatron-LM 训练 MoE 模型实用手册](https://www.reddit.com/r/MachineLearning/comments/1xorgq0/the_ultimate_moe_training_handbook_training/) ⭐️ 8.0/10

曾参与 Ultra-Scale 和 Smol Training Playbooks 的 Hugging Face 工程师 Nouamane 发布了一份详细手册，讲解如何用 NVIDIA 的 Megatron-LM 训练混合专家（MoE）模型。手册包含一份 Megatron-LM 操作流程（硬件测试、镜像构建、稠密基线模型训练、单节点首个 MoE 训练），对 MoE 层内部的深入拆解（路由器、路由、负载均衡、专家、块布局），并延伸到推理服务与强化学习，另附 55 张图表和可直接使用的脚本。 大多数公开的训练指南都假定使用稠密 Transformer 模型，因此转向 MoE（如今前沿开源模型的主流架构）的实践者在路由、负载均衡和专家并行方面几乎找不到代码级的指导。这份有实践支撑的端到端手册降低了 GPU 预算有限的团队采用 MoE 训练的门槛，并帮助他们避免代价高昂的配置错误。 这些建议基于在 CSCS 的 Alps 集群上约 80 万 GH200 GPU 小时的 MoE 训练经验；作者明确标注了哪些结果来自自己的实际运行、哪些引自前沿模型的论文/配置/代码、哪些只是玩具级模拟。第 3 章和第 4 章无需 GPU 即可跟随阅读，所有推荐使用的 Megatron-LM 参数都汇总在同一个配置块中。

reddit · r/MachineLearning · /u/Norlax_42 · 11月5日 19:13

**背景**: 混合专家（MoE）是一种架构：每个 Transformer 块中包含许多独立的“专家”前馈网络，由学习得到的路由器把每个 token 只分配给其中少数几个，因此总参数量可以扩大，而每个 token 的计算量基本不变。Megatron-LM 是 NVIDIA 开源的 PyTorch 库，用于训练超大规模 Transformer 模型，提供张量并行、流水线并行和专家并行能力。GH200 是 NVIDIA 的 Grace Hopper 超级芯片，把 Hopper GPU 与 Grace CPU 及大容量统一内存池结合，被广泛用于大规模训练集群。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/blog/moe">Mixture of Experts Explained</a></li>
<li><a href="https://grokipedia.com/page/Megatron-LM">Megatron-LM</a></li>
<li><a href="https://www.nvidia.com/en-us/data-center/grace-hopper-superchip/">NVIDIA Grace Hopper Superchip | NVIDIA</a></li>

</ul>
</details>

**标签**: `#MoE`, `#Megatron-LM`, `#LLM training`, `#Hugging Face`, `#systems`

---

<a id="item-4"></a>
## [美国放行 H200 对华销售，约 10 家中国企业获准采购](https://t.me/zaihuapd/44945) ⭐️ 8.0/10

据路透社报道，美国商务部已批准约 10 家中国企业购买英伟达 H200 芯片，买家包括阿里巴巴、腾讯、字节跳动和京东等，联想、富士康等分销商同样获得许可，单一客户最多可采购 7.5 万颗。但目前尚未有任何交付完成，部分中国企业在北京市方面的指导下转趋谨慎，黄仁勋此次访华被视为推动交易落地的重要尝试。 这是近年来美国对华先进 AI 芯片出口管制中最大的一次松动之一，可能为英伟达恢复数十亿美元级的收入来源，并缓解中国头部 AI 实验室的算力紧缺。与此同时，中方的谨慎态度表明，这一决定如今也受中国推动国产 AI 芯片替代的影响，H200 已不只是商品，更是中美博弈中的筹码。 许可证将单一客户的上限设为约 7.5 万颗 H200，并覆盖联想、富士康等分销商，但获批并不等于交付——目前尚无出货完成，据报中国企业仍在等待更明确的政府信号而保持观望。H200 是英伟达 Hopper 架构的数据中心 GPU，高带宽显存容量显著高于 H100，这正是它对大模型训练与推理具有吸引力的原因。

telegram · zaihuapd · 11月5日 14:42

**背景**: 自 2022 年起，美国逐步收紧对华先进半导体出口管制，英伟达则推出 H20 等中国特供的降规版本，而 H20 后来也被禁止出口。H200 的性能低于最新的 Blackwell 系列，但远强于此前的任何对华获批产品，因此这次批准被视为一次明显的政策转向。与此同时，中国一直在推动华为等国产替代方案，但在前沿 AI 研发上仍依赖英伟达硬件。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.nvidia.com/en-us/data-center/h200/">H 200 GPU | NVIDIA</a></li>
<li><a href="https://www.aquanode.io/gpu/nvidia-h200">NVIDIA H 200 GPU : Specs , VRAM, Price & Benchmarks (2026)</a></li>
<li><a href="https://www.worldjournal.com/wj/story/121477/8685685">不只 H 20 晶片被禁 傳 Nvidia 中 國 特 供 版 旗艦顯卡也暫停 供 應 | 世界新聞網</a></li>

</ul>
</details>

**标签**: `#AI chips`, `#export controls`, `#NVIDIA H200`, `#US-China tech policy`, `#semiconductor industry`

---

<a id="item-5"></a>
## [谷歌向开发者开放 Nano Banana 2 Lite 与 Gemini Omni Flash](https://t.me/zaihuapd/44952) ⭐️ 8.0/10

谷歌发布了两款生成媒体模型：Nano Banana 2 Lite 从文本生成 1K 图像，延迟约 4 秒，单张成本 0.034 美元；以及面向视频生成的快速模型 Gemini Omni Flash，官方称其可生成 10 秒视频。两者均已通过 Google AI Studio、Gemini API 和 Gemini Enterprise Agent Platform 开放，Nano Banana 2 Lite 还将进入搜索 AI Mode 和 Gemini app 等消费端产品。 这一定价和延迟水平把大批量图像生成推向“白菜价”区间，使开发者在单个工作流中生成成千上万张图片变得可行，而不必局限于少量高价调用。同时向开发者 API 与消费级产品开放，意味着同一模型家族如今覆盖了原型验证、生产流水线和终端用户功能三个层面。 Nano Banana 2 Lite 基于 Google DeepMind 的 Gemini 3.1 Flash-Lite Image，官方称其为 Gemini 3.1 图像家族中最快、最便宜的模型，并同时针对图像理解与生成做了优化。Gemini Omni Flash 被定位为“从任意输入创建和编辑任何内容”的过渡性模型，目前从视频起步，文档显示其可根据文本提示或静态图片生成带同步原生音频的 720p 片段。

telegram · zaihuapd · 11月6日 00:21

**背景**: Nano Banana 是谷歌图像模型沿用的昵称，源自其早期代号，如今已成为产品线名称，其中“Lite”版本以牺牲部分极致画质换取速度和成本优势。Gemini Omni Flash 属于较新的“omni”模型类别，目标是用一个模型处理多种媒体类型，而非将图像与视频拆成独立系统。Flash-Lite 的命名延续了谷歌既有的 Flash 层级惯例，代表旗舰 Gemini 模型中延迟更低、价格更便宜的版本。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://deepmind.google/models/gemini-image/flash-lite/">Gemini 3.1 Flash-Lite Image – Nano Banana 2 Lite — Google ...</a></li>
<li><a href="https://ai.google.dev/gemini-api/docs/models/gemini-omni-flash">Learn about the Gemini Omni Flash video generation and editing model</a></li>
<li><a href="https://deepmind.google/models/model-cards/gemini-omni-flash/">Gemini Omni Flash - Model Card — Google DeepMind</a></li>

</ul>
</details>

**标签**: `#Google`, `#generative-ai`, `#image-generation`, `#video-generation`, `#Gemini API`

---

<a id="item-6"></a>
## [OpenAI 开始在 ChatGPT 中测试广告，面向免费及 Go 用户](https://t.me/zaihuapd/44955) ⭐️ 8.0/10

OpenAI 于 2 月 9 日开始在 ChatGPT 中测试带有明确标记的广告，这些广告出现在对话框下方的独立区域，面向免费用户及 Go 订阅用户。首席执行官 Sam Altman 表示，OpenAI 预计广告长期将占总营收的 50% 以下。 这标志着全球使用最广泛的 AI 助手在商业化上的一次重大转向：从单纯依赖订阅，扩展到广告支持的模式，可能重塑 AI 产品的定价方式，以及为昂贵的模型训练与推理提供资金的方式。这也让 OpenAI 与谷歌基于广告的搜索业务正面竞争，同时对数亿免费用户的使用体验和信任提出新的疑问。 OpenAI 表示，广告将基于用户需求进行优化，不会接触私人对话，广告商也无法干预 ChatGPT 的回答内容。公司还透露，ChatGPT 的月增长率已回升至 10% 以上，并计划在本周发布更新版的聊天模型。

telegram · zaihuapd · 11月6日 03:15

**背景**: ChatGPT Go 是 OpenAI 于 2025 年 8 月率先在印度推出的低价订阅档位，随后推广至全球，目的是以更接近免费的价格让更多用户用上进阶功能。此前 OpenAI 的消费级业务主要依靠 Plus、Pro 和 Business 等订阅，而广告将带来类似谷歌资助免费搜索那样的第二条收入来源。大语言模型的训练与推理成本高昂，因此如何让免费用户层实现变现，已成为 AI 公司面临的核心难题。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openai.com/index/introducing-chatgpt-go/">Introducing ChatGPT Go, now available worldwide - OpenAI</a></li>
<li><a href="https://chatgpt.com/pricing/">Plans and Pricing | ChatGPT</a></li>

</ul>
</details>

**标签**: `#OpenAI`, `#ChatGPT`, `#advertising`, `#AI business model`, `#monetization`

---

<a id="item-7"></a>
## [百度发布文心 5.0 全模态大模型，参数规模达 2.4 万亿](https://t.me/zaihuapd/44959) ⭐️ 8.0/10

百度今日正式发布文心 5.0 全模态大模型，参数规模达 2.4 万亿，采用全模态统一建模技术，可同时处理文本、图像、音频和视频等多种信息类型。百度称该模型在超过 40 项权威基准测试中表现超越 Gemini-2.5-Pro 和 GPT-5-High 等国际顶尖模型，并邀请了来自科技、金融、文化、教育等领域的 835 位专家参与模型指导和校准。 2.4 万亿的参数规模使其成为目前公开宣布的最大模型之一，而百度直接将其定位为对标美国顶尖前沿模型的挑战者。如果这些基准测试成绩经得起验证，将进一步说明中国实验室在多模态能力上正在缩小差距，这对选择模型技术栈的企业和开发者具有实际意义。 文心 5.0 采用混合专家（MoE）结构，单次推理激活的参数量低于 3%，百度称这一设计在保持强大功能的同时提升了推理效率。不过其基准测试成绩目前只是笼统表述，既未公布逐项分数，也未经过独立验证；公告同时还提到，个人用户目前可通过文心平台使用该模型。

telegram · zaihuapd · 11月6日 05:41

**背景**: 混合专家（MoE）是一种模型架构：模型内部包含许多被称为“专家”的专用子网络，并配有一个可学习的路由网络，将每个输入 token 只分配给其中一小部分专家，因此每次推理只有一部分参数被激活。这使得实验室能够在相同的算力预算下把总参数量扩展到远超稠密模型所能承受的规模，这也是前沿模型往往同时公布巨大总参数和较小激活参数的原因。“全模态”则指用单一模型原生处理文本、图像、音频和视频，而不是拼接多个专用模型，Ola 等研究系统也在探索这一方向。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Mixture_of_experts">Mixture of experts - Wikipedia</a></li>
<li><a href="https://arxiv.org/abs/2507.11181">[2507.11181] Mixture of Experts in Large Language Models Mixture of Experts in Large Language Models - arXiv.org Mixture of experts - Wikipedia Mixture of Experts Explained - Hugging Face Applying Mixture of Experts in LLM Architectures | NVIDIA ... A Survey on Mixture of Experts in Large Language Models A Closer Look into Mixture-of-Experts in Large Language Models</a></li>
<li><a href="https://arxiv.org/abs/2502.04328">Ola: Pushing the Frontiers of Omni-Modal Language Model</a></li>

</ul>
</details>

**标签**: `#Baidu`, `#ERNIE 5.0`, `#large language models`, `#multimodal AI`, `#Mixture-of-Experts`

---