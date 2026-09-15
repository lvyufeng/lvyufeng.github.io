---
layout: archive
title: "简历"
permalink: /zh/cv/
author_profile: true
lang: zh
lang_switch: /cv/
---

{% include base_path %}

教育背景
------
* 重庆大学（985）计算机科学与技术 硕士研究生，2018 年 9 月 – 2021 年 6 月
  * 学位论文：《面向多领域文本的自动摘要系统》
  * 导师：钟将 教授
* 重庆大学（985）计算机科学与技术 学士，2014 年 9 月 – 2018 年 6 月
* 重庆大学 法学 学士（第二学位），2018 年

工作经历
------
* **2026 年 7 月 – 至今** &emsp; AI 框架研究员
  * 北京智源人工智能研究院（BAAI） &emsp; 北京
  * 负责 **[Torch-FL](https://github.com/flagos-ai/Torch-FL)**：FlagOS 软件栈中的 PyTorch 设备插件，提供统一 `flagos` 设备，并按算子路由到厂商原生 kernel、FlagGems/Triton 编译器 kernel、兼容封装或 CPU fallback。

* **2021 年 7 月 – 2026 年 7 月** &emsp; AI 基础设施高级工程师 / 关键项目负责人（SE）
  * 华为 & MindSpore 团队 &emsp; 北京

  * **项目一：MSAdapter / MindTorch**（项目负责人，2024 年 12 月 – 2026 年 7 月）
    * 主导兼容方案架构，实现 PyTorch 生态向 MindSpore + 昇腾的平滑迁移。
    * 支持盘古模型零代码切换，以及 DeepSeek / Qwen 全系列 Day-0 迁移。
    * 动态图开箱性能约达 torch-npu 的 95%，深度调优后可超越约 10%。
    * 打通 MSAdapter + PIJIT，攻克 MoE 图分支过多导致的裂图问题，实现 DeepSeek-V3 高性能不裂图推理。

  * **项目二：MindNLP**（项目负责人，2022 年 7 月 – 2026 年 7 月）
    * 负责预训练模型支持与面向 NLP / LLM 开发者的工具链。
    * 针对 DeepSeek-OCR 合并 Expert 计算图，将 NPU 利用率由 **8% 提升至 30%**。
    * 基于 Apache Arrow 与 mmap 的流水线数据预处理，相对原生 PyTorch DataLoader 约 **4 倍**吞吐。
    * 支持 Hugging Face Transformers 官方维护的模型类别，覆盖昇腾 910A/910B/310B、GPU 与 CPU。

  * **项目三：MindSpore 核心引擎**（核心研发工程师，2021 年 7 月 – 2026 年 7 月）
    * 设计自动混合精度（AMP）系统，在昇腾 910 上保证 Float16 训练的数值稳定性。
    * 研究功能式与 OOP 融合的混合编程范式，使静态图具备接近 JAX 的 JIT 优化能力。
    * 开发 RNN 算子，并提供 Encoder、Decoder 与多头注意力的标准化 Transformer 接口。

精选项目
------
* **[Torch-FL](https://github.com/flagos-ai/Torch-FL)** &emsp; 2026 年 7 月至今
  * 智源 FlagOS 的 PyTorch 设备插件。用户使用标准 PyTorch API 与 `device="flagos"`，由插件屏蔽各厂商设备差异。
  * 算子后端包括厂商原生 kernel（如 ACLNN）、CUDA/兼容封装、可移植 FlagGems/Triton kernel，以及显式 CPU fallback。
  * 覆盖 eager、autograd、`torch.compile`、分布式集合通信与 profiler，支持 CUDA、昇腾、沐曦等多种加速器。

* **[DeepSeek-V4-Flash 老旧硬件推理](https://github.com/lvyufeng/deepseek-v4-2080ti)** &emsp; 2026 年 5 月
  * 独立开源项目：在 4× RTX 2080 Ti 上部署 DeepSeek-V4-Flash（284B 总参数 / 13B 激活）。
  * 自定义 CUDA kernel，支持 MoE expert staging、稀疏 attention 与张量并行解码。
  * CPU 驻留 Routed-Expert + H2D 异步预取，验证 64k token 上下文。
  * [技术报告（PDF）](https://github.com/lvyufeng/deepseek-v4-2080ti/blob/master/dsv4_2080ti_report.pdf)

科研经历
------
* **CAAI-MindSpore 学术研究基金：MoE 推理优化** &emsp; 2024 年 6 月 – 2025 年 7 月
  * 专家委员 / 产业导师。撰写官方申请指南，指导 expert-aware 预取与 expert offload。
  * 共同作者论文：**Klotski**（ASPLOS 2025）、**Fate**（WWW 2026）。

* **国家重点研发计划：专业知识服务关键技术与商业模式研究** &emsp; 2017 年 11 月 – 2020 年 12 月
  * 机器学习算法工程师。主导 NER、关系抽取与自动摘要，在 ECIR 2021 发表 **DSMER**。
  * 设计标注系统并构建专有 NER 数据集；内部数据上 NER 平均准确率约 80%，摘要 ROUGE 30+。

代表性论文
======
<ul>{% for post in site.publications reversed %}
  {% include archive-single-cv.html %}
{% endfor %}</ul>

教学
------
<ul>{% for post in site.teaching reversed %}
  {% include archive-single-cv.html %}
{% endfor %}</ul>

报告
------
<ul>{% for post in site.talks reversed %}
  {% include archive-single-talk-cv.html %}
{% endfor %}</ul>

荣誉与奖项
------
* 重庆大学一等奖学金 &emsp; 2018 – 2020
* 重庆大学优秀助教奖 &emsp; 2019 年 3 月
* 全国大学生计算机系统能力大赛（NSCSCC）三等奖 &emsp; 2018 年 9 月
* 华为奖学金 &emsp; 2017 年 12 月

技能
------
* **深度学习框架：** 精通 PyTorch 与 MindSpore 内部机制，擅长自定义算子与高性能模型实现。
* **大规模 LLM 训练：** 熟悉 Megatron-LM、DeepSpeed；具备 100 至 1000+ GPU/NPU 集群上的预训练与微调经验。
* **高性能推理：** 熟悉 vLLM、SGLang，能够进行框架级改造与 kernel 级优化。
