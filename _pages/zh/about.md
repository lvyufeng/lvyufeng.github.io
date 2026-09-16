---
permalink: /zh/
title: "关于我"
excerpt: "北京智源人工智能研究院 AI 框架研究员。关注本地大模型、Torch-FL 与高效推理。"
author_profile: true
lang: zh
lang_switch: /
---
{% include base_path %}

我是[北京智源人工智能研究院（BAAI）](https://www.baai.ac.cn/)的 **AI 框架研究员**。关心的问题是：怎样让语言模型跑在 **用户自己的硬件上**——私密、可控——以及 **小模型 / 压缩模型** 能否支撑 **coding agent 和多步推理**，而不是把每次请求交给不可信的云端中继。

目前的系统工作是 **[Torch-FL](https://github.com/flagos-ai/Torch-FL)**：FlagOS 里的 PyTorch 设备插件，对外提供统一的 `flagos` 设备。对我来说，它是用来 **测量** 模型离开数据中心 GPU 之后还剩下什么能力，而不是研究问题本身。

2021 年 7 月至 2026 年 7 月，我在华为 **MindSpore** 团队担任 AI 基础设施高级工程师（MindNLP、MSAdapter / MindTorch）。硕士与本科均毕业于重庆大学计算机科学与技术专业；硕士论文是多领域自动摘要。

研究方向
------
资源受限下的小模型与压缩模型；agentic 能力（工具调用、coding agent、长程任务）；高效与异构 LLM 推理。

动态
------
* **2026.09** &emsp; 在 PyTorch Conference China 2026 做报告：[Torch-FL：面向 PyTorch 的虚拟设备层]({{ base_path }}/talks/2026-09-08-torch-fl-virtual-device-layer)
* **2026.07** &emsp; 加入智源，任 AI 框架研究员
* **2026.05** &emsp; 开源 [PocketLLM](https://github.com/lvyufeng/PocketLLM)，起点是 4× RTX 2080 Ti 上的 DeepSeek-V4-Flash
* **2026.04** &emsp; Fate 被 *The ACM Web Conference (WWW 2026)* 接收

代表性论文
------
* **[Klotski]({{ base_path }}/publication/2025-03-30-Klotski)**（ASPLOS 2025）。专家感知的多 batch 流水线 MoE 推理。我参与 prefetch / offload 路径设计。[arXiv](https://arxiv.org/abs/2502.06888) · [PDF](https://yuyue.github.io/res/paper/Klotski-ASPLOS2025.pdf)
* **[Fate]({{ base_path }}/publication/2026-04-13-Fate)**（WWW 2026）。用跨层门控加速端侧 MoE 推理。[arXiv](https://arxiv.org/abs/2502.12224)

[全部论文 →]({{ base_path }}/zh/publications/)

精选系统
------
* **[Torch-FL](https://github.com/flagos-ai/Torch-FL)**（智源，2026 年 7 月至今）：FlagOS 的 PyTorch 设备插件。统一 `flagos` 设备（PrivateUse1），按算子路由到厂商 kernel、FlagGems/Triton、兼容封装或 CPU fallback。
* **[PocketLLM](https://github.com/lvyufeng/PocketLLM)**（2026 年至今）：面向消费级多 GPU 的 C++/CUDA 与 PyTorch 推理栈。从 4× RTX 2080 Ti 上的 DeepSeek-V4-Flash 起步，现已覆盖 MiniMax-M2.7、GLM-5.2、Qwen3.8-27B-FP8。该配置下 C++ FP4 decode 约 **3.7 tok/s**——大 MoE 能在家里跑起来，但还撑不起真正的 coding-agent 工作。[文档](https://lvyufeng.github.io/PocketLLM/) · [技术报告（PDF）](https://github.com/lvyufeng/PocketLLM/blob/master/docs/reports/dsv4_2080ti_report.pdf)
