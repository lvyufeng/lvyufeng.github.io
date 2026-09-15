---
layout: archive
title: "论文"
permalink: /zh/publications/
author_profile: true
lang: zh
lang_switch: /publications/
---
{% include base_path %}

主要包括命名实体识别、图像描述生成，以及混合专家（MoE）高效推理。加粗作者为本人。

{% for post in site.publications reversed %}
  {% include archive-single.html %}
{% endfor %}
