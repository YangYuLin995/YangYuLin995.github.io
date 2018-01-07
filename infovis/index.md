---
layout: archive
title: "信息可视化作品集"
date: 2018-1-1T14:25:45-04:00
modified:
excerpt: "期末可视化作品"
tags: []
image: 
  feature:test.jpg
  teaser:
---


#### 我的其他作品（期中项目和日常小练手）
<div class="tiles">
{% for post in site.categories.visualization %}
  {% include post-grid.html %}
{% endfor %}
</div><!-- /.tiles 把所有categories 有 visualization 的列出来-->