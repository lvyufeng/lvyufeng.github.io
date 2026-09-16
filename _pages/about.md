---
permalink: /
title: "About"
excerpt: "AI Framework Researcher at BAAI, working on local LLMs, Torch-FL, and efficient inference."
author_profile: true
lang: en
lang_switch: /zh/
redirect_from:
  - /about/
  - /about.html
---
{% include base_path %}

I am an **AI Framework Researcher** at the [Beijing Academy of Artificial Intelligence (BAAI)](https://www.baai.ac.cn/). I care about **language models people can run locally**—privately, on hardware they own—and whether **small or compressed models** can still support **coding agents and multi-step reasoning**, instead of sending every prompt through an untrusted cloud API.

My current systems work is **[Torch-FL](https://github.com/flagos-ai/Torch-FL)**, a PyTorch device plugin in the FlagOS stack that exposes a unified `flagos` device across accelerators. I treat that stack as a way to *measure* what survives off datacenter GPUs, not as the research question itself.

From July 2021 to July 2026 I was a Senior AI Infrastructure Engineer at Huawei on the MindSpore team (MindNLP, MSAdapter / MindTorch). I received my M.S. and B.S. in Computer Science from Chongqing University; my thesis was on multi-domain abstractive summarization.

Research interests
------
Small and compressed language models under tight compute; agentic skills (tool use, coding agents, long-horizon tasks); efficient and heterogeneous LLM inference.

News
------
* **2026.09** &emsp; Gave [Torch-FL: A Virtual Device Layer for PyTorch]({{ base_path }}/talks/2026-09-08-torch-fl-virtual-device-layer) at PyTorch Conference China 2026
* **2026.07** &emsp; Joined BAAI as an AI Framework Researcher
* **2026.05** &emsp; Open-sourced [PocketLLM](https://github.com/lvyufeng/PocketLLM), starting from DeepSeek-V4-Flash on 4× RTX 2080 Ti
* **2026.04** &emsp; Fate accepted to *The ACM Web Conference (WWW 2026)*

Selected publications
------
* **[Klotski]({{ base_path }}/publication/2025-03-30-Klotski)** (ASPLOS 2025). Expert-aware multi-batch pipelining for MoE inference. I co-designed the prefetch and offload path. [arXiv](https://arxiv.org/abs/2502.06888) · [PDF](https://yuyue.github.io/res/paper/Klotski-ASPLOS2025.pdf)
* **[Fate]({{ base_path }}/publication/2026-04-13-Fate)** (WWW 2026). Cross-layer gating for faster MoE inference on edge devices. [arXiv](https://arxiv.org/abs/2502.12224)

[All publications →]({{ base_path }}/publications/)

Selected systems
------
* **[Torch-FL](https://github.com/flagos-ai/Torch-FL)** (BAAI, Jul. 2026 – present): PyTorch device plugin for FlagOS. One `flagos` device (PrivateUse1) with per-operator routing to vendor kernels, FlagGems/Triton, compatibility boxing, or CPU fallback.
* **[PocketLLM](https://github.com/lvyufeng/PocketLLM)** (2026 – present): C++/CUDA and PyTorch inference on consumer GPUs. Started as DeepSeek-V4-Flash on 4× RTX 2080 Ti; now also covers MiniMax-M2.7, GLM-5.2, and Qwen3.8-27B-FP8. On that 2080 Ti box, C++ FP4 decode is about **3.7 tok/s**—enough to run a large MoE at home, not enough for productive coding-agent work. [Docs](https://lvyufeng.github.io/PocketLLM/) · [Technical report (PDF)](https://github.com/lvyufeng/PocketLLM/blob/master/docs/reports/dsv4_2080ti_report.pdf)
