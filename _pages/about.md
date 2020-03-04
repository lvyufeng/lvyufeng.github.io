---
permalink: /
title: "About Me"
excerpt: "About Me"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---
{% include base_path %}

Graduate student of Chongqing University. I obtained a bachelor of engineering degree from Chongqing University. At present, the main research directions is **Natural Language Processing**, including Named Entity Recognition, Relationship Extraction, and **Automatic Text Summarization**, etc.

Publications
------
Sorry, I have no top conference accepted paper yet. Although one of my papers has been rejected by EMNLP, I still insist on submitting to top conferences, and I am currently submitting 3 other papers.

Projects
------

1. [CQU Professional Content Annotation System](http://39.100.48.36/index.html):
  A self-defined information extraction annotation system, include sequence labeling and text classification functions. [Sources](https://github.com/cqunlp/annotation_sys)

1. [Graph-to-graph summarization](https://github.com/cqunlp/summarization_amr_graph): A simple implementation of "***Generating Subgraph: The Essence of Summarization Task***", which is a graph-to-graph framework for summarization task.

1. [Step into MIPS](https://github.com/cquca/step_into_mips): A tutorial of building a 5-level MIPS CPU based on FPGA(Which is also the guide book for students in Chongqing University). [Sources](https://github.com/cquca/step_into_mips)

1. [Agricultural products data crawling platform](https://elppa12138.coding.net/p/eb_crawler)(Privately owned by Chongqing Academy of Social Sciences): A Spider management platform for data crawling task. Aims to collect products' data from **Taobao, Tmall, JingDong, Suning and Pinduoduo**(With a self-built proxy pool). 

Honors & Awards
------
* 2019.03 &emsp; Excellent TA Award &emsp; Chongqing University

* 2018.09 &emsp; The Third Price of NSCSCC &emsp; Chinese Ministry of Education

* 2017.12 &emsp; Huawei Award &emsp; 


Talks
------
  <ul>{% for post in site.talks %}
    {% include archive-single-talk-cv.html %}
  {% endfor %}</ul>

Teaching
------
  <ul>{% for post in site.teaching %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>
