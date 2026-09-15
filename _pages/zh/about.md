---
permalink: /zh/
title: "关于我"
excerpt: "北京智源人工智能研究院 AI 框架研究员。主要工作：Torch-FL、大语言模型系统与高效推理。"
author_profile: true
lang: zh
lang_switch: /
---
{% include base_path %}

我是[北京智源人工智能研究院（BAAI）](https://www.baai.ac.cn/)的 **AI 框架研究员**。目前主要工作是 **[Torch-FL](https://github.com/flagos-ai/Torch-FL)**：FlagOS 软件栈中的 PyTorch 设备插件，对外提供统一的 `flagos` 设备，并在厂商原生算子、可移植编译器算子与 CPU fallback 之间做算子路由。

2021 年 7 月至 2026 年 7 月，我在华为 **MindSpore** 团队担任 AI 基础设施高级工程师 / 关键项目负责人，从事大语言模型系统、高效推理、混合专家（MoE）模型优化，以及 NPU/GPU 上的软硬件协同设计。硕士与本科均毕业于重庆大学计算机科学与技术专业。

动态
------
* **2026.09** &emsp; 在 PyTorch Conference China 2026 做报告：[Torch-FL：面向 PyTorch 的虚拟设备层]({{ base_path }}/talks/2026-09-08-torch-fl-virtual-device-layer)
* **2026.08** &emsp; FlagOS 直播：[Torch-FL：终结多元芯片碎片化噩梦]({{ base_path }}/talks/2026-08-16-torch-fl-bilibili-live)
* **2026.07** &emsp; 加入智源，任 AI 框架研究员，负责 [Torch-FL](https://github.com/flagos-ai/Torch-FL)
* **2026.05** &emsp; 开源 [DeepSeek-V4-Flash 在 4× RTX 2080 Ti 上的推理运行时](https://github.com/lvyufeng/deepseek-v4-2080ti)
* **2026.04** &emsp; Fate 被 *The ACM Web Conference (WWW 2026)* 接收
* **2025.03** &emsp; Klotski 被 *ASPLOS 2025* 接收
* **2024.12** &emsp; 主导 MSAdapter / MindTorch，推进 PyTorch 到昇腾生态的迁移

代表性论文
------
<ul>{% for post in site.publications reversed %}
  {% include archive-single-cv.html %}
{% endfor %}</ul>

精选系统
------

1. **[Torch-FL](https://github.com/flagos-ai/Torch-FL)**（智源，2026 年 7 月至今）：面向 FlagOS 的 PyTorch 设备插件。通过 PrivateUse1 注册统一的 `flagos` 设备，按算子路由到厂商原生 kernel、FlagGems/Triton 编译器 kernel、兼容封装或 CPU fallback，使同一套 PyTorch 代码可在 CUDA、昇腾、沐曦等加速器上运行。

1. **[MindNLP](https://github.com/mindspore-lab/mindnlp)**（项目负责人，2022 – 2026）：在昇腾、GPU、CPU 上兼容 Hugging Face。针对 DeepSeek-OCR 合并 Expert 计算图，将 NPU 利用率由 8% 提升至 30%；基于 Apache Arrow 与 mmap 的数据管道相对原生 PyTorch DataLoader 约 **4 倍**吞吐。

1. **MSAdapter / MindTorch**（项目负责人，2024.12 – 2026.07）：PyTorch 生态向 MindSpore + 昇腾的平滑迁移。支持盘古模型零代码切换，以及 DeepSeek / Qwen 全系列 Day-0 迁移。动态图开箱性能约达 torch-npu 的 95%，深度调优后可超越约 10%。

1. **[DeepSeek-V4-Flash 老旧硬件推理](https://github.com/lvyufeng/deepseek-v4-2080ti)**（2026）：在 4× RTX 2080 Ti 上部署 284B 总参数 / 13B 激活的 MoE 模型，包含自定义 CUDA kernel、Expert staging 与 64k 上下文。[技术报告](https://github.com/lvyufeng/deepseek-v4-2080ti/blob/master/dsv4_2080ti_report.pdf)。

教学
------
<ul>{% for post in site.teaching reversed %}
  {% include archive-single-cv.html %}
{% endfor %}</ul>
