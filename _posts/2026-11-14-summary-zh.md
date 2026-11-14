---
layout: default
title: "Horizon Summary: 2026-11-14 (ZH)"
date: 2026-11-14
lang: zh
---

> 从 40 条内容中筛选出 4 条重要资讯。

---

1. [《Science》独家：上海新华医院碱基编辑试验绕过监管致女童死亡](#item-1) ⭐️ 9.0/10
2. [爱好者微调小型 Transformer 预测个人血糖](#item-2) ⭐️ 8.0/10
3. [TorchTitan 在 JUPITER 上把 1T 参数 MoE 训练推到每 GPU 每秒 1300 token](#item-3) ⭐️ 8.0/10
4. [DeepSeek 开放全家桶应用 API：搜索、OCR、ASR、TTS 与工具调用齐上阵](#item-4) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [《Science》独家：上海新华医院碱基编辑试验绕过监管致女童死亡](https://t.me/zaihuapd/45103) ⭐️ 9.0/10

《Science》杂志于 2026 年 7 月 23 日发布独家调查，披露一名患有罕见单碱基突变遗传病的 6 岁女童，于 2025 年 3 月底在上海交通大学附属新华医院接受实验性碱基编辑基因治疗后死亡。研究团队通过向脊髓液注射数万亿个 AAV 病毒载体以靶向脑部神经元，女童在 7 天后因严重免疫反应死亡；该事件从未公开，且据称绕过了监管审批。 这一事件对中国实验性基因编辑疗法的审查与披露机制提出了根本性质疑，也让人回想起 2018 年贺建奎事件——正是那次事件首次让全球聚焦于不受监管的人类基因组编辑。它可能推动临床试验监管收紧、不良事件强制上报，以及对向绝望家庭提供未经验证编辑疗法的行为进行更严格审视。 该治疗通过鞘内注射数万亿个 AAV 载体以抵达脑部神经元，女童在 7 天后因严重免疫反应死亡。据报道，其父母自费超过 80 万美元，而该试验在美国临床试验注册库 ClinicalTrials.gov 上的记录已逾一年未更新。

telegram · zaihuapd · 11月13日 09:24

**背景**: 碱基编辑是一种源自 CRISPR 的技术，它通过化学方式将一个 DNA 碱基转换为另一个碱基，而无需切断双螺旋的两条链，因此对由单碱基突变引起的疾病颇具吸引力。腺相关病毒（AAV）是基因治疗中最常用的递送载体，因为它能高效感染细胞且通常免疫原性较低，但高剂量给药以及直接递送至中枢神经系统已被证实存在引发严重免疫激活和神经毒性的风险。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.synthego.com/crispr-base-editing-guide/">CRISPR Base Editing Explained | ABE & CBE in Gene Therapy</a></li>
<li><a href="https://www.addgene.org/guides/aav/">Addgene: Adeno-associated virus ( AAV ) Guide</a></li>
<li><a href="https://pmc.ncbi.nlm.nih.gov/articles/PMC11386282/">Immune responses to central nervous system directed...</a></li>

</ul>
</details>

**标签**: `#gene-editing`, `#bioethics`, `#clinical-trials`, `#regulation`, `#investigative-journalism`

---

<a id="item-2"></a>
## [爱好者微调小型 Transformer 预测个人血糖](https://www.reddit.com/r/MachineLearning/comments/1xvja5n/i_have_trained_a_model_to_predict_my_blood_sugar_p/) ⭐️ 8.0/10

一位爱好者先在大约 19,200 个 CGM-年的合成 1 型糖尿病数据上训练了一个仅 31,253 个参数的编码器 Transformer，再用 115 天个人 CGM 数据（80 天训练适配器、35 天测试）进行 LoRA 微调。该模型能提前两小时预测血糖、填补缺失的 CGM 轨迹并进行回溯预测，作者称其表现可与已发表模型竞争。 该项目表明，通过合成数据预训练加 LoRA 个性化，一个非常小的模型也能用于 CGM 预测，这可能降低血糖预测所需的数据和算力门槛。它还展示了对胰岛素和碳水化合物输入进行反事实推理的潜力，这对实用的糖尿病决策支持和边缘设备 AI 很重要。 该模型使用 3.5 到 7 天的可变上下文窗口，在上下文达到至少 48 小时后可从历史血糖预测一天中的时间，并在 Kovatchev 风险空间中用 DILATE/MSE 和 pinball 损失结合可学习的 Kendall-Gal 权重进行训练。局限包括尚未有下游基准来评估胰岛素/碳水反事实推理能力，作者还指出模型在预测未来约 30 分钟低血糖方面仍不如自己。

reddit · r/MachineLearning · /u/0xdeadf1sh · 11月13日 20:48

**背景**: 持续葡萄糖监测（CGM）设备会频繁测量组织间液葡萄糖，广泛用于 1 型糖尿病管理，并产生适合机器学习的时间序列数据。LoRA（低秩适应）是一种参数高效的微调技术，通过添加小型低秩权重而不是重新训练整个网络来适配预训练模型。Transformer 是一种基于注意力机制的神经序列模型，这里作者先用合成模拟器在大量模拟患者上预训练，再个性化到一个真实患者。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/LoRA_(machine_learning)">LoRA (machine learning) - Wikipedia</a></li>
<li><a href="https://www.nature.com/articles/s41586-025-09925-9">A foundation model for continuous glucose monitoring data</a></li>

</ul>
</details>

**标签**: `#machine-learning`, `#healthcare-ai`, `#time-series`, `#lora`, `#synthetic-data`

---

<a id="item-3"></a>
## [TorchTitan 在 JUPITER 上把 1T 参数 MoE 训练推到每 GPU 每秒 1300 token](https://www.reddit.com/r/MachineLearning/comments/1xvce5h/scaling_to_1t_moe_on_torchtitan_p/) ⭐️ 8.0/10

一个与 TorchTitan 和 PyTorch 维护者合作的工程团队报告称，他们在 JUPITER 超级计算机的 GH200 GPU 上，用 384 块 GPU 把约 1 万亿参数的混合专家（MoE）模型训练到每 GPU 每秒约 1300 个 token 的吞吐，相比起点提升了 14 倍；其基线单步耗时 84 秒，其中 68 秒都花在等待网络上。 这说明纯 PyTorch 原生技术栈（TorchTitan）能够在“算力强、跨节点网络相对弱”的硬件上，以高吞吐完成万亿参数 MoE 训练，为 ML 系统工程师提供了一套具体、可复现的工程方案，而不只是厂商的基准测试数字。 其配置是 384 路 FSDP 加 4 路专家并行，且专家并行严格限制在单节点内（有意跳过流水线并行，以避免步长过长和调试缓慢）；性能收益来自：完整激活重计算（约 4 倍）、把检查点激活通过 900 GB/s 的 C2C 链路卸载到 Grace 并提前一层预取、用 Muon 替代 Adam 以把优化器状态减半并支撑 64k token 序列，以及用 FlexShard 以“整个专家”为单位分片，使 Newton-Schulz 正交化可在本地零通信完成。

reddit · r/MachineLearning · /u/f14-bertolotti · 11月13日 16:28

**背景**: TorchTitan 是一个“干净房间”式、PyTorch 原生的大规模 LLM 预训练平台；混合专家（MoE）模型对每个 token 只激活一部分专家子网络，因此总参数量可以远超单 token 计算量。训练这类模型必须做分片：全分片数据并行（FSDP）把每个权重切分到各个 rank、需要时再即时聚合，而专家并行（EP）让每块 GPU 持有一部分专家，并通过网络把 token 路由过去。GH200 是 NVIDIA 的 Grace Hopper 超级芯片，通过 900 GB/s 的芯片间链路把 HBM3e GPU 与 Grace CPU 相连，JUPITER 正是由它构成的超级计算机；在 JUPITER 上，InfiniBand 每 GPU 仅约 25 GB/s，比 NVLink 慢约 6 倍。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/pytorch/torchtitan">GitHub - pytorch/ torchtitan : A PyTorch native platform for training...</a></li>
<li><a href="https://arxiv.org/abs/2410.06511">[2410.06511] TorchTitan : One-stop PyTorch native solution for...</a></li>
<li><a href="https://en.wikipedia.org/wiki/Mixture_of_experts">Mixture of experts - Wikipedia</a></li>

</ul>
</details>

**标签**: `#distributed-training`, `#MoE`, `#PyTorch`, `#HPC`, `#GPU-scaling`

---

<a id="item-4"></a>
## [DeepSeek 开放全家桶应用 API：搜索、OCR、ASR、TTS 与工具调用齐上阵](https://mp.weixin.qq.com/s/78KBHc4-4N5b2vfL9SkutQ) ⭐️ 8.0/10

DeepSeek 今天开放了“全家桶”应用 API，开发者只需在原有 API 中开启对应参数，就能获得深度思考搜索、文件输入、阅读链接和语音等对话能力，服务端会自动完成工具调用与上下文拼接。V4.1-Flash 模型已在三个接口中支持，Search、Fetch、OCR、ASR、TTS 也可单独调用；官方同时开源了可导入历史对话的前端 Demo（deepseek-ai/chat-demo）。 这让 DeepSeek 的 API 从单纯的文本补全接口升级为应用级平台：检索、视觉、语音和智能体式的工具编排都由服务端完成，大幅降低了开发者构建类 ChatGPT 助手的工程成本。这同时也会加剧与其他模型厂商的竞争，因为后者通常对搜索、OCR 和语音服务单独收费。 该前端 Demo 支持流式回复、深度思考、智能搜索、带来源引用的链接阅读、附件上传/粘贴/拖拽、语音输入和朗读回复，并且可以导入从 DeepSeek 网页端导出的聊天记录，配合自己的 API key 在本地继续对话。底层的 V4.1-Flash 是一个多模态混合专家（MoE）模型，拥有 552B 主干参数和最高 100 万 token 的上下文，预填充阶段仅激活 8B 参数、解码阶段激活 16B 参数。

telegram · zaihuapd · 11月13日 14:27

**背景**: DeepSeek-V4.1-Flash 是 DeepSeek 新架构家族中体量最小的模型，主打更快的推理速度与更高的吞吐，并能原生理解图像和文本。工具调用（也称函数调用）指的是模型针对用户请求自行决定调用哪种外部能力——网页搜索、页面抓取、OCR 识别或语音合成；通常这些工具需要开发者自己串联实现。OCR、ASR 和 TTS 分别指光学字符识别（从图片/PDF 中提取文字）、自动语音识别（语音转文字）和文本转语音合成。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.deepseek.com/en/news/deepseek-v4-1-flash/">DeepSeek | Introducing DeepSeek-V4.1-Flash: smarter, faster ...</a></li>
<li><a href="https://huggingface.co/deepseek-ai/DeepSeek-V4.1-Flash">deepseek-ai/DeepSeek-V4.1-Flash · Hugging Face</a></li>
<li><a href="https://github.com/deepseek-ai/chat-demo">GitHub - deepseek -ai/ chat - demo : Chat Demo · GitHub</a></li>

</ul>
</details>

**标签**: `#DeepSeek`, `#API`, `#LLM`, `#multimodal`, `#open-source`

---