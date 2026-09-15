---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
lang: en
lang_switch: /zh/publications/
---
{% include base_path %}

Selected papers on named entity recognition, image captioning, and efficient Mixture-of-Experts inference. Author names in **bold** are mine.

{% for post in site.publications reversed %}
  {% include archive-single.html %}
{% endfor %}
