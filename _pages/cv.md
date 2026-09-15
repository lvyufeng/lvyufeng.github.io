---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
lang: en
lang_switch: /zh/cv/
redirect_from:
  - /resume
---

{% include base_path %}

Education
------
* M.S. in Computer Science and Technology, Chongqing University, Sep. 2018 – Jun. 2021
  * Thesis: *Automatic Summarization System for Multi-domain Text*
  * Advisor: Prof. Jiang Zhong
* B.S. in Computer Science and Technology, Chongqing University, Sep. 2014 – Jun. 2018
* B.S. in Law (second degree), Chongqing University, 2018

Working experience
------
* **Jul. 2026 – present** &emsp; AI Framework Researcher
  * Beijing Academy of Artificial Intelligence (BAAI) &emsp; Beijing, China
  * Leading **[Torch-FL](https://github.com/flagos-ai/Torch-FL)**, a PyTorch device plugin for the FlagOS stack: a unified `flagos` device with per-operator routing across vendor kernels, FlagGems/Triton compiler kernels, compatibility boxing, and CPU fallback.

* **Jul. 2021 – Jul. 2026** &emsp; Senior AI Infrastructure Engineer / Project Lead
  * Huawei, MindSpore Team &emsp; Beijing, China

  * **MSAdapter / MindTorch** (Project lead, Dec. 2024 – Jul. 2026)
    * Designed the compatibility stack for migrating PyTorch workloads to MindSpore + Ascend.
    * Enabled Pangu with no code changes and Day-0 ports of DeepSeek / Qwen.
    * Dynamic-graph out-of-the-box performance reaches about 95% of torch-npu, and exceeds it by about 10% after tuning.
    * Combined MSAdapter with PIJIT so MoE models such as DeepSeek-V3 can run high-performance inference without graph splitting.

  * **MindNLP** (Project lead, Jul. 2022 – Jul. 2026)
    * Led architecture for pretrained model support and Hugging Face-style pipelines on MindSpore.
    * Optimized DeepSeek-OCR by consolidating expert computational graphs, raising NPU utilization from **8% to 30%**.
    * Built an Apache Arrow + mmap preprocessing pipeline with about **4×** throughput versus the native PyTorch DataLoader.
    * Supported official Hugging Face Transformers model classes on Ascend 910A/910B/310B, GPU, and CPU.

  * **MindSpore core engine** (Core engineer, Jul. 2021 – Jul. 2026)
    * Designed Automatic Mixed Precision (gradient scaling and overflow detection) for stable Float16 training on Ascend 910.
    * Worked on a hybrid functional / OOP programming paradigm with JIT optimization comparable to JAX.
    * Implemented MindSpore RNN operators and standardized Transformer Encoder / Decoder / MHA interfaces.

Selected projects
------
* **[Torch-FL](https://github.com/flagos-ai/Torch-FL)** &emsp; Jul. 2026 – present
  * PyTorch device plugin for FlagOS at BAAI. Users program against standard PyTorch APIs and `device="flagos"`; the plugin isolates vendor differences behind one logical device.
  * Per-operator backends: native vendor kernels (e.g. ACLNN), CUDA/compatibility boxing, portable FlagGems/Triton kernels, and explicit CPU fallback.
  * Covers eager execution, autograd, `torch.compile`, distributed collectives, and profiler integration, with support spanning CUDA, Ascend, MetaX, and other accelerators.

* **[DeepSeek-V4-Flash inference on legacy hardware](https://github.com/lvyufeng/deepseek-v4-2080ti)** &emsp; May 2026
  * Independent open-source runtime serving DeepSeek-V4-Flash (284B total / 13B active) on 4× RTX 2080 Ti without native FP4/FP8 tensor cores.
  * Custom CUDA kernels for MoE expert staging, sparse attention, and tensor-parallel decoding, plus an OpenAI-compatible API.
  * CPU-resident routed-expert storage with host-to-device staging; validated a 64k-token context window.
  * [Technical report (PDF)](https://github.com/lvyufeng/deepseek-v4-2080ti/blob/master/dsv4_2080ti_report.pdf)

Research experience
------
* **CAAI–MindSpore Academic Research Funding** &emsp; Jun. 2024 – Jul. 2025
  * Project: MoE inference optimization. Role: expert committee member and industrial mentor.
  * Authored the official application guide; co-designed expert-aware prefetch and expert offload in **Klotski**; guided unified-memory deployment and prefetcher launch-cost optimization in **Fate**.

* **National Key Research and Development Program of China** &emsp; Nov. 2017 – Dec. 2020
  * Project: key technologies for professional knowledge services. Role: machine learning algorithm engineer.
  * Led NER, relation extraction, and automatic summarization; published **DSMER** at ECIR 2021.
  * Built a labeling system and an internal NER dataset; about 80% NER accuracy and ROUGE 30+ on in-house summarization data.

Publications
======
<ul>{% for post in site.publications reversed %}
  {% include archive-single-cv.html %}
{% endfor %}</ul>

Teaching
------
<ul>{% for post in site.teaching reversed %}
  {% include archive-single-cv.html %}
{% endfor %}</ul>

Talks
------
<ul>{% for post in site.talks reversed %}
  {% include archive-single-talk-cv.html %}
{% endfor %}</ul>

Honors & awards
------
* First-Class Scholarship, Chongqing University &emsp; 2018 – 2020
* Excellent TA Award, Chongqing University &emsp; Mar. 2019
* Third Prize, NSCSCC, Chinese Ministry of Education &emsp; Sep. 2018
* Huawei Scholarship &emsp; Dec. 2017

Skills
------
* **Deep learning frameworks:** internals of PyTorch and MindSpore; custom operators and high-performance model implementation.
* **Large-scale LLM training:** Megatron-LM and DeepSpeed; pretraining and fine-tuning on clusters from 100 to 1,000+ GPUs/NPUs.
* **High-performance inference:** vLLM and SGLang; framework-level changes and kernel-level optimization.
