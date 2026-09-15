---
permalink: /
title: "About"
excerpt: "AI Framework Researcher at the Beijing Academy of Artificial Intelligence (BAAI), working on Torch-FL, LLM systems, and efficient inference."
author_profile: true
lang: en
lang_switch: /zh/
redirect_from:
  - /about/
  - /about.html
---
{% include base_path %}

I am an **AI Framework Researcher** at the [Beijing Academy of Artificial Intelligence (BAAI)](https://www.baai.ac.cn/). My current work is **[Torch-FL](https://github.com/flagos-ai/Torch-FL)**, a PyTorch device plugin in the FlagOS stack that exposes a single `flagos` device and routes operators across vendor kernels, portable compiler kernels, and CPU fallback.

From July 2021 to July 2026 I was a Senior AI Infrastructure Engineer at Huawei on the MindSpore team, working on LLM systems, efficient inference, Mixture-of-Experts (MoE) models, and software–hardware co-design on NPU and GPU. I previously received my M.S. and B.S. in Computer Science from Chongqing University.

News
------
* **2026.09** &emsp; Gave [Torch-FL: A Virtual Device Layer for PyTorch]({{ base_path }}/talks/2026-09-08-torch-fl-virtual-device-layer) at PyTorch Conference China 2026
* **2026.08** &emsp; FlagOS livestream [Torch-FL: Ending the Fragmentation Nightmare of Heterogeneous AI Chips]({{ base_path }}/talks/2026-08-16-torch-fl-bilibili-live)
* **2026.07** &emsp; Joined BAAI as an AI Framework Researcher; working on [Torch-FL](https://github.com/flagos-ai/Torch-FL)
* **2026.05** &emsp; Released [DeepSeek-V4-Flash inference on 4× RTX 2080 Ti](https://github.com/lvyufeng/deepseek-v4-2080ti)
* **2026.04** &emsp; Fate accepted to *The ACM Web Conference (WWW 2026)*
* **2025.03** &emsp; Klotski accepted to *ASPLOS 2025*
* **2024.12** &emsp; Led MSAdapter / MindTorch for PyTorch-to-Ascend migration

Selected publications
------
<ul>{% for post in site.publications reversed %}
  {% include archive-single-cv.html %}
{% endfor %}</ul>

Selected systems
------

1. **[Torch-FL](https://github.com/flagos-ai/Torch-FL)** (BAAI, Jul. 2026 – present): PyTorch device plugin for FlagOS. Registers a unified `flagos` device (PrivateUse1) and routes each operator to native vendor kernels, FlagGems/Triton compiler kernels, compatibility boxing, or CPU fallback, so the same PyTorch code can run across CUDA, Ascend, MetaX, and other accelerators.

1. **[MindNLP](https://github.com/mindspore-lab/mindnlp)** (Project lead, 2022 – 2026): Hugging Face compatibility on MindSpore across Ascend, GPU, and CPU. Optimized DeepSeek-OCR by consolidating expert graphs, raising NPU utilization from 8% to 30%. Built an Apache Arrow + mmap data pipeline with about **4×** throughput versus the native PyTorch DataLoader.

1. **MSAdapter / MindTorch** (Project lead, 2024.12 – 2026.07): Smooth migration from the PyTorch ecosystem to MindSpore + Ascend. Supports Pangu with no code changes and Day-0 ports of DeepSeek / Qwen. Dynamic-graph performance reaches about 95% of torch-npu, and exceeds it by about 10% after tuning.

1. **[DeepSeek-V4-Flash on legacy GPUs](https://github.com/lvyufeng/deepseek-v4-2080ti)** (2026): Heterogeneous CPU–GPU runtime serving a 284B / 13B-active MoE model on 4× RTX 2080 Ti, with custom CUDA kernels, expert staging, and a 64k-token context window. [Technical report](https://github.com/lvyufeng/deepseek-v4-2080ti/blob/master/dsv4_2080ti_report.pdf).

Teaching
------
<ul>{% for post in site.teaching reversed %}
  {% include archive-single-cv.html %}
{% endfor %}</ul>
