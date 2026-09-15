---
title: "Torch-FL: Ending the Fragmentation Nightmare of Heterogeneous AI Chips"
title_zh: "Torch-FL：终结多元芯片碎片化噩梦"
collection: talks
type: "Live"
type_zh: "直播"
permalink: /talks/2026-08-16-torch-fl-bilibili-live
venue: "Bilibili Live (FlagOS)"
venue_zh: "Bilibili 直播（FlagOS）"
date: 2026-08-16
location: "Beijing, China"
location_zh: "北京"
excerpt: "FlagOS livestream on Torch-FL, a unified PyTorch plugin that hides vendor differences across Chinese AI accelerators."
excerpt_zh: "FlagOS 直播：介绍 Torch-FL，用统一的 PyTorch 插件屏蔽国产 AI 芯片之间的软件栈差异。"
---
{% include base_path %}

FlagOS livestream (replay) on **[Torch-FL](https://github.com/flagos-ai/Torch-FL)** (`Pytorch-Plugin-FL`). Different accelerators currently need different `torch_*` plugins, which fragments training and inference. Torch-FL aims at one PyTorch experience across backends, using FlagOS libraries such as FlagGems and FlagCX.

* [Video (Bilibili)](https://www.bilibili.com/video/BV1SqbS6wEMU)
* Related conference talk: [Torch-FL: A Virtual Device Layer for PyTorch]({{ base_path }}/talks/2026-09-08-torch-fl-virtual-device-layer)

中文概要
------

国产 AI 芯片各自维护不同的 Torch 插件，科研和商用训推都要重复适配。这场 FlagOS 直播介绍 Torch-FL：对外提供统一的 PyTorch 使用体验，并借助 FlagGems / FlagCX 等 FlagOS 组件，把硬件差异挡在插件层后面。
