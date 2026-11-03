---
layout: default
title: "Horizon Summary: 2026-11-03 (ZH)"
date: 2026-11-03
lang: zh
---

> 从 46 条内容中筛选出 6 条重要资讯。

---

1. [Astra 直接改写 Qwen3.5-0.8B 权重，将 MATH-500 准确率从 7.9% 提升至 48.1%](#item-1) ⭐️ 8.0/10
2. [Subvocal 发布射频感知智能眼镜，可将无声口型解码为文字](#item-2) ⭐️ 8.0/10
3. [披露近三周后，Ubuntu LTS 内核仍未修复严重 0day 远程代码执行漏洞](#item-3) ⭐️ 8.0/10
4. [视频中微弱的飞机噪声可结合 ADS-B 数据精确定位拍摄地点](#item-4) ⭐️ 8.0/10
5. [树莓派 5 正式发布：2.4GHz Cortex-A76 与双路 4K60 HDMI](#item-5) ⭐️ 8.0/10
6. [Linux 内核 IPv4 TCP 高危释放后使用漏洞（CVE-2026-98432）可远程 RCE，请尽快更新内核](#item-6) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Astra 直接改写 Qwen3.5-0.8B 权重，将 MATH-500 准确率从 7.9% 提升至 48.1%](https://rikiyat.github.io/blog/weight-space-programming/) ⭐️ 8.0/10

一篇新博客文章介绍了 Astra —— 一个基于大语言模型的系统，它无需任何外部工具或梯度训练，就能检查并直接改写小型 Qwen 模型（Qwen3.5-0.8B）的权重，据作者自测可将该模型的 MATH-500 得分从 7.9% 提升到 48.1%。文章还声称，Astra 仅通过读取权重就能判断小型网络被训练去玩的是哪一款简单游戏。 如果该结果经得起检验，它指向一种“权重空间编程”的新范式：模型可以在一次操作中修复或升级另一个模型的能力，从而有可能取代成本高昂的数据整理与完整微调流程。这一前景牵涉到模型可解释性、安全监督，以及大语言模型是否正在走向递归自我改进的争论。 这些数据来自作者在单个 0.8B 参数模型和单一数学基准上的自测，尚未经过独立研究者验证；博客本身也提到部分编辑尝试是失败的。值得注意的��，文中声称 Astra 是“原生地”完成这一操作，而非借助传统的权重编辑优化器或 LoRA 式适配器，而这正是专家们质疑的焦点。

hackernews · dbreunig · 11月2日 18:21 · [社区讨论](https://news.ycombinator.com/item?id=50341174)

**背景**: 大语言模型通常只在 token 序列上工作：训练完成后权重就固定下来，要提升模型能力一般需要收集更多数据、进行进一步训练，或添加 LoRA 之类的低秩适配器。“权重空间学习”是一条相对小众的研究路线，它把网络参数本身当作可读取、可生成、可编辑的数据，此前已有工作证明可以对更大模型的权重进行修改。Qwen 是阿里巴巴的开源权重模型系列，其小参数版本因运行和实验成本低而广受欢迎。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://explainx.ai/blog/weight-space-programming-gpt-6-astra-edits-qwen3-5-0-8b-weights-math-7-9-to-48-1-mit-csail-2026">GPT-6 Astra Edits Qwen Weights: MATH-500 7.9% to 48.1% ...</a></li>
<li><a href="https://kingy.ai/blog/weight-space-programming-ai-agent-model-weights/">Weight-Space Programming: GPT-6 Astra Edits Qwen</a></li>
<li><a href="https://rikiyat.github.io/blog/weight-space-programming/">Sparks of Weight - Space Programming: LLMs can natively read & write...</a></li>

</ul>
</details>

**社区讨论**: 社区反应呈现明显分歧：有评论者称这一结果“疯狂”且具有范式意义，认为它表明大模型对自身权重具有堪比甚至超过人类对神经元直觉的原生理解。一位从事权重空间学习的研究者则反驳说，博客及其传播夸大了成果，权重编辑与生成早已可行；另有评论者推测，Astra 很可能是被刻意用权重数据训练出来的递归自我改进尝试，而非涌现能力。

**标签**: `#weight-space-learning`, `#LLM`, `#model-editing`, `#research`, `#Qwen`

---

<a id="item-2"></a>
## [Subvocal 发布射频感知智能眼镜，可将无声口型解码为文字](https://news.ycombinator.com/item?id=50340088) ⭐️ 8.0/10

YC F26 创业公司 The Subvocal Company（由前佐治亚理工学院计算机系学生 Aarush 和 Arnav 创立）展示了其智能眼镜：镜架内嵌天线，向佩戴者面部发射类似蓝牙的低功率无线电波，把无声口型解码成文字，速度接近正常说话。团队最早在 2 月的 Stanford TreeHacks 黑客松上用 EMG 电极做出粗糙原型，后来认定肌肉电信号方案不可行，转而采用射频方案，因为发现射频信号会被舌头、嘴唇和软腭调制，而且即便双唇完全闭合（他们称之为“内部言语”）也能工作。 无声语音接口有望消除 Wispr Flow 这类语音驱动 AI 听写工具最大的社交障碍——人们可以在图书馆、开放办公室和公共场所用“说话”来输入而不被旁人听见。如果这套硬件能走出实验室并稳定工作，它对有言语或运动障碍的用户也有明显的无障碍价值，同时这也是面向消费者的、非声学的常备计算机输入通道的早期尝试之一。 该产品目前处于预购阶段，并未公布准确率或词错误率数据；团队表示最大的难题是跨用户泛化，因为每个人的面部解剖结构会产生差异极大的射频信号模式，而他们找到的唯一办法就是大规模扩充数据采集。自研的低噪声射频感知链路和天线布局（必须让电磁场与发音器官最大程度重叠）是核心工程难点，创始人也承认，目前的“内部言语”模式做起来感觉有些别扭，尽管他们已经练习得比较熟练。

hackernews · aarushyadav · 11月2日 17:16

**背景**: 无声语音识别（SSR）是声学语音识别之外被长期研究的一条路径：它不去“听”声音，而是读取发声过程的生理活动——肌肉电信号，或者像本案这样，读取无线电波穿过舌头、嘴唇和软腭时被扰动的模式。最知名的先例是 MIT 媒体实验室的 AlterEgo，创始人称其是灵感来源，该项目在面部和颈部贴附表面 EMG 电极。另一个相关但不同的概念是“默读”（subvocalization），即阅读或思考时词语在脑内的“声音”——Subvocal 的系统并不读取这种不由自主的内心独白，而是读取用户主动做出的、闭唇的口型动作。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Subvocal_recognition">Subvocal recognition - Wikipedia</a></li>
<li><a href="https://pubmed.ncbi.nlm.nih.gov/29855428/">Development of sEMG sensors and algorithms for silent speech ...</a></li>
<li><a href="https://chaof94.github.io/Papers/EarSSR.pdf">EarSSR: Silent Speech Recognition via Earphones</a></li>

</ul>
</details>

**社区讨论**: 评论者总体热情高涨——有人称其“简直像从科幻小说里走出来的”，并称赞其无障碍价值——但对实用性提出了尖锐质疑：多人询问，小声低语是不是比完全不出声地做口型更自然，以及信号处理是在眼镜本地完成还是通过手机 App 完成。另一些人给出了具体的硬件建议，希望保留可调节的金属鼻托臂以适配非标准鼻梁，并提供可夹在现有近视眼镜上的配件版本；还有人担心常开感知带来的隐私风险，追问推理是否在设备端进行、能否离线使用。

**标签**: `#silent-speech-recognition`, `#smart-glasses`, `#RF-sensing`, `#human-computer-interaction`, `#accessibility`

---

<a id="item-3"></a>
## [披露近三周后，Ubuntu LTS 内核仍未修复严重 0day 远程代码执行漏洞](https://freenode.net/article/ubuntu-lts-kernels-still-unfixed-for-critical-cve-2026-98432) ⭐️ 8.0/10

在公开披露将近三周之后，Ubuntu LTS 内核仍未修复 CVE-2026-98432 这一 Linux 内核中的严重远程代码执行漏洞，Ubuntu 也没有发布任何缓解措施说明或更新后的已修复内核包。此事在 Hacker News 上引发高热度讨论（超过 800 分、400 多条评论），用户在其中交流临时规避方案并质疑修复为何迟迟不来。 Ubuntu LTS 是部署最广泛的服务器与云操作系统之一，因此一个尚未修复、可被远程利用的内核漏洞会让大量生产主机在相当长的时间内处于暴露状态。厂商未给出缓解建议，也迫使系统管理员自行临时编写过滤规则，一旦配置不当就可能误伤正常流量。 评论者指出，Ubuntu 安全跟踪页面将该漏洞定为“High”而非“Critical”，而后者通常会触发计划外的内核更新；同时 Ubuntu 未提供任何缓解说明，而 Red Hat 发布了一种缓解方法，但声称该方法“可降低暴露风险，却无法完全阻止该漏洞”。社区提出的临时方案是在 raw PREROUTING 表中使用 iptables/nftables 的 u32 匹配规则，在网络边界上丢弃符合条件的 TCP 数据包，但这只是非官方的权宜之计，并非真正的修复。

hackernews · majorchord · 11月2日 18:39 · [社区讨论](https://news.ycombinator.com/item?id=50341462)

**背景**: 0day（零日漏洞）指的是在官方修复出现之前就已公开、甚至可能已被利用的漏洞，因此从披露到修补之间的这段时间是防御方最危险的窗口期。远程代码执行（RCE）是一类允许攻击者通过网络在目标机器上运行任意代码、无需物理接触或用户交互的漏洞，属于最严重的安全问题之一。CVE-2026-98432 是分配给这个具体内核缺陷的标准化“通用漏洞与暴露”编号，使厂商、扫描工具和安全公告能够指向同一个问题。Ubuntu LTS（长期支持）版本的内核会在多年内获得安全维护，因此这段维护一旦出现空档，就会直接影响长期运行的服务器和云实例。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Zero-day_vulnerability">Zero-day vulnerability - Wikipedia</a></li>
<li><a href="https://www.crowdstrike.com/en-us/cybersecurity-101/cyberattacks/remote-code-execution/">What is Remote Code Execution (RCE)? | CrowdStrike</a></li>
<li><a href="https://en.wikipedia.org/wiki/Common_Vulnerabilities_and_Exposures">Common Vulnerabilities and Exposures - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 讨论情绪总体上对 Ubuntu 持批评态度：有评论者指出，在 raw PREROUTING 中添加一条简单的 u32 丢弃规则就能在内核漏洞可被利用之前拦截攻击流量，并抱怨没有人公开宣传这一做法；其他人则要求 Ubuntu 给出延迟修复的官方解释，并将其沉默与 Red Hat 的安全公告作对比。多位评论者质疑该漏洞为何被评为 High 而非 Critical；还有人把担忧扩大到运行 Linux 内核却从不获得安全更新的消费级路由器和无线接入点，尤其是在大语言模型降低了攻击门槛的背景下。

**标签**: `#linux-kernel`, `#security-vulnerability`, `#ubuntu`, `#cve`, `#rce`

---

<a id="item-4"></a>
## [视频中微弱的飞机噪声可结合 ADS-B 数据精确定位拍摄地点](https://simonwillison.net/2026/Nov/3/a-sound-that-leaks-your-exact-location/) ⭐️ 8.0/10

研究者 Colsto 发布了一段 YouTube 演示视频，展示如何把视频音轨中几乎听不见的飞机背景噪声分离出来、还原成多普勒曲线，再与公开的 ADS-B 航班数据进行交叉比对，从而精确定位视频的拍摄地点。该方法利用每架经过飞机的速度、距离以及前后航班之间的时间间隔来缩小位置范围，Simon Willison 将其称为“天才般的 OSINT 作品”。 这说明环境声音本身就是一条几乎没人在发布前处理过的定位侧信道，即便视频里没有可辨认的地标、路牌或天际线，视觉上的匿名化也可能被它攻破。由于航班数据免费公开，该技术同时降低了调查人员、记者以及恶意使用者的门槛，任何在家中或敏感场所拍摄视频的人，都应假设飞机噪声可能暴露自己的位置。 该方法的关键在于飞机掠过头顶时靠近与远离所产生的精确多普勒频移，匹配时依据的是空速、斜距以及连续航班之间的时间间隔，而不是某一段单独的声音。因此其精度取决于拍摄地上空 ADS-B 接收机覆盖是否密集，以及音频中是否包含足够多的微弱飞机噪声；目前已经出现了独立复现项目 doppler-locate 以及一个 Hermes agent 插件。

rss · Simon Willison · 11月3日 05:32

**背景**: ADS-B（广播式自动相关监视）是一种航空监视技术，飞机通过卫星导航自行确定位置，并周期性地广播位置、高度、速度与身份信息；Flightradar24 和 FlightAware 等众包接收机网络会近实时地将这些航迹公开。多普勒效应是指声源相对听者运动时感知频率发生偏移的现象，也就是飞机掠过时音调先升后降的那种熟悉变化，而这条曲线的形状编码了飞机的距离与速度。频谱图能把这些微弱频移显现为音频中漂移的线条，正是这一点让软件可以反推出每次飞掠的几何关系。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Automatic_Dependent_Surveillance–Broadcast">Automatic Dependent Surveillance–Broadcast - Wikipedia</a></li>
<li><a href="https://www.flightradar24.com/how-it-works/ads-b">Automatic Dependent Surveillance - Broadcast | Flightradar24</a></li>
<li><a href="https://github.com/digitalis-p/doppler-locate/tree/main">GitHub - digitalis-p/doppler-locate: Geolocate audio ...</a></li>

</ul>
</details>

**标签**: `#privacy`, `#OSINT`, `#geolocation`, `#signal-processing`, `#ADS-B`

---

<a id="item-5"></a>
## [树莓派 5 正式发布：2.4GHz Cortex-A76 与双路 4K60 HDMI](https://t.me/zaihuapd/44854) ⭐️ 8.0/10

树莓派 5 正式发布，4GB 型号售价 60 美元、8GB 版本售价 80 美元（另加当地税费），这是旗舰级树莓派首次改用 2.4GHz 四核 64 位 Arm Cortex-A76 CPU，并搭配支持 OpenGL ES 3.1 与 Vulkan 1.2 的 VideoCore VII GPU。新板还提供双路 4K60p HDMI 输出、4K60p HEVC 解码器、双频 802.11ac Wi-Fi、蓝牙 5.0/BLE、支持 SDR104 模式的高速 microSD 接口，以及两个可同时运行在 5Gbps 的 USB 3.0 端口。 对于应用最广泛的单板计算机而言，树莓派 5 是一次代际跨越：它用现代化的乱序执行核心与桌面级图形性能取代了老旧的 Cortex-A72 平台，直接惠及此前受限于 CPU 与 I/O 的嵌入式、边缘计算和创客项目。双路 4K60 HDMI 与 USB 3.0 的加入，也让这块板卡在远低于多数 Arm 开发板的价格上，更接近可日常使用的通用桌面电脑。 GPU 是博通 16nm 工艺 BCM2712 SoC 中的 VideoCore VII，主频约 800MHz，相比树莓派 4 所用的 VideoCore VI 是一次大幅提升。SDR104 模式的 microSD 接口值得关注，因为它把存储卡接口吞吐量提升到远超旧有 SDR50/DDR50 约 50MB/s 级别之上，不过要真正跑出这一速度，需要搭配兼容的 UHS-I 存储卡以及板端稳定的 1.8V 信号切换。

telegram · zaihuapd · 11月2日 12:00

**背景**: 树莓派是一系列低成本、信用卡大小的单板计算机，已成为创客电子、教育乃至众多工业嵌入式部署的事实标准；早期型号依赖 32 位或较老的 64 位核心（如 Cortex-A72）。Cortex-A76 是原本为智能手机与笔记本设计的 64 位 Armv8.2 乱序执行微架构，单时钟性能远高于 A72，分支预测器也经过大幅改进，因此被视为树莓派历史上最大的一次 CPU 升级。VideoCore 是博通集成在为树莓派提供动力的 SoC 中的移动 GPU 系列，因此每一代树莓派的图形能力都取决于其博通芯片中 VideoCore 的版本。SDR104 是 SD 卡 UHS-I 总线中最快的模式，接口时钟与读取吞吐量相比早期模式大约翻倍。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.androidauthority.com/cortex-a76-deep-dive-870896/">Arm Cortex - A 76 CPU microarchitecture deep dive</a></li>
<li><a href="https://community.st.com/stm32-mpus-products-and-hardware-related-39/how-to-enable-sdr104-mode-with-full-speed-on-stm32mp15x-platform-34607">How to enable SDR104 mode with full speed on STM32MP15x ...</a></li>

</ul>
</details>

**标签**: `#Raspberry Pi`, `#hardware`, `#embedded systems`, `#single-board computer`, `#Arm Cortex-A76`

---

<a id="item-6"></a>
## [Linux 内核 IPv4 TCP 高危释放后使用漏洞（CVE-2026-98432）可远程 RCE，请尽快更新内核](https://t.me/zaihuapd/44866) ⭐️ 8.0/10

近日 Telegram 上流传一条安全提醒：Linux 内核 IPv4 TCP 协议栈存在一个高危的释放后使用（use-after-free）漏洞，编号为 CVE-2026-98432，攻击者可从网络侧触发，既不需要认证也不需要用户交互。针对 MPTCP 监听端口的远程代码执行（RCE）利用示例已被公开，同时 Go 官方安全团队发布公告称，自 Go 1.24 起，Go 程序在 Linux 上默认对 listen socket 启用 MPTCP。 任何暴露在网络上且未打补丁的 Linux 服务器都可能面临风险，这几乎覆盖了绝大多数云主机、容器和边缘节点。影响面比表面看起来更大：由于 Go 1.24 及以上版本的服务默认继承了这一易受攻击的前提条件，即使团队从未主动使用 MPTCP，也可能需要打补丁或调整配置。 该漏洞并不只影响部署了 MPTCP 的场景——Go 官方公告指出，即使没有任何 MPTCP 监听，系统仍可能遭受同类攻击；此外 Go 仅对 listen socket 启用 MPTCP，对外发起的连接仍是普通 TCP。切实可行的缓解措施是升级内核（或以其他方式关闭默认的 MPTCP 监听行为），而不能寄希望于“没配置 MPTCP 就没事”。

telegram · zaihuapd · 11月3日 02:37

**背景**: 释放后使用（use-after-free）漏洞指的是程序在内存被释放之后仍然继续使用它，攻击者若能控制这块被复用的内存，往往就能劫持执行流并运行自己的代码。多路径 TCP（MPTCP）是 IETF 对标准 TCP 的扩展（RFC 8684），允许一条连接同时使用多条网络路径以提升吞吐量和冗余度；在 Linux 上，应用程序通常需要显式开启才会使用它。然而自 Go 1.24 起，Go 的 net 包在 Linux 上会自动为监听套接字请求 MPTCP，于是大量用 Go 编写的网络服务在开发者毫不知情的情况下具备了 MPTCP 能力——一个内核网络漏洞就这样变成了云原生生态中一大片服务的默认暴露面。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Multipath_TCP">Multipath TCP - Wikipedia</a></li>
<li><a href="https://docs.kernel.org/networking/mptcp.html">Multipath TCP (MPTCP) — The Linux Kernel documentation</a></li>
<li><a href="https://groups.google.com/g/golang-announce/c/PCoQcdxoScw">[security] Protecting against CVE-2026-98432 - Google Groups</a></li>

</ul>
</details>

**标签**: `#security`, `#linux-kernel`, `#vulnerability`, `#networking`, `#go`

---