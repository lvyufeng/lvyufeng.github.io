---
title: "Torch-FL: A Virtual Device Layer for PyTorch"
title_zh: "Torch-FL：面向 PyTorch 的虚拟设备层"
collection: talks
type: "Tutorial"
type_zh: "教程"
permalink: /talks/2026-09-08-torch-fl-virtual-device-layer
venue: "PyTorch Conference China 2026"
venue_zh: "PyTorch Conference China 2026"
date: 2026-09-08
location: "Shanghai, China"
location_zh: "上海"
excerpt: "Tutorial talk at PyTorch Conference China 2026 on turning PrivateUse1 into a reusable virtual device layer for multi-chip PyTorch."
excerpt_zh: "在 PyTorch Conference China 2026 的 FlagOS 教程中介绍 Torch-FL：把 PrivateUse1 做成可复用的虚拟设备层。"
---
{% include base_path %}

Part of the FlagOS tutorial **Building Portable Large Models on Heterogeneous AI Accelerators with FlagOS**, at KubeCon + CloudNativeCon + OpenInfra Summit + PyTorch Conference China 2026.

* **Time:** 8 September 2026, 11:00–12:15 (CST)
* **Room:** 7F \| Pearl Hall, Shanghai
* **Speakers:** Mengsi Lyu, Hongjun Zhang, and Yufeng Lyu (BAAI)
* **Language:** English
* [Session page](https://kubecon-cloudnativecon-openinfra-pytorch-2026.sessionize.com/session/1224095)
* [Day schedule](https://kubecon-cloudnativecon-openinfra-pytorch-2026.sessionize.com/schedule/day/20260908)
* Related livestream: [Torch-FL：终结多元芯片碎片化噩梦]({{ base_path }}/talks/2026-08-16-torch-fl-bilibili-live)

The talk presents **[Torch-FL](https://github.com/flagos-ai/Torch-FL)** as a virtual device layer for PyTorch. PyTorch’s `PrivateUse1` key is usually treated as one vendor’s private backend, so plugins such as `torch_npu` and `torch_musa` cannot share a process, and each chip stack reimplements runtime, allocator, and thousands of ATen operators.

Torch-FL turns `PrivateUse1` into a reusable layer:

* **One logical device.** Users program against standard PyTorch APIs and `device="flagos"`, with a unified Python API and `ProcessGroup`.
* **Per-operator routing.** A configuration-driven table selects native vendor kernels, compatibility boxing, FlagGems/Triton compiler kernels, or CPU fallback—without a rebuild when a backend has to change.
* **Thin HAL.** A new accelerator starts from a ~40-function C ABI (device, memory, stream). `torch.randn(..., device="flagos")` can run immediately via CPU fallback; operator coverage is incremental.
* **Codegen.** About 93% of the plugin code is generated against the ATen registry.
* **Compile path.** `torch.compile` registers a `flagos` Inductor backend, with a FlagTree multi-backend compiler on the roadmap.
* **Beyond conventional GPUs.** The same layer can drive embodied-AI chips through `torch.compile` graph execution, and emulate FP8/FP4 storage on hardware that only computes in BF16/Int8.

Code: [github.com/flagos-ai/Torch-FL](https://github.com/flagos-ai/Torch-FL).

中文概要
------

这场报告是 FlagOS 教程 **Building Portable Large Models on Heterogeneous AI Accelerators with FlagOS** 中的一部分，介绍如何把 PyTorch 的 `PrivateUse1` 从「某一厂商的私有后端」做成可复用的虚拟设备层。上层统一为 `flagos` 设备与 Python API，中层按算子做配置化路由，下层接入厂商 runtime，以及原生 kernel、兼容封装、FlagGems/Triton 三条算子路径。新加速器只需实现约 40 个 C ABI 即可先跑通，再逐步补齐算子；约 93% 代码由 ATen 注册表生成。

