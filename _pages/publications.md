---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---
<!-- 
Sorry, I have no top conference accepted paper yet. Although one of my papers has been rejected by EMNLP, I still insist on submitting to top conferences, and I am currently submitting 3 other papers. -->

{% if author.googlescholar %}
  You can also find my articles on <u><a href="{{author.googlescholar}}">my Google Scholar profile</a>.</u>
{% endif %}

{% include base_path %}

{% for post in site.publications reversed %}
  {% include archive-single.html %}
{% endfor %}
