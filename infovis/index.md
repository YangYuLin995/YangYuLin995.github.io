---
layout: archive
title: "信息可视化作品集"
date: 2018-1-1T14:25:45-04:00
modified:
excerpt: ""
tags: []
image: 
  feature:
  teaser:
---
-  https:<a href="//public.tableau.com/views/_18343/sheet0?:embed=y&:display_count=yes">概要：母婴室，洗手间，公共厕所，残疾人厕所的全国分布对比</a>
<iframe src="https://public.tableau.com/views/_18343/sheet0?:embed=y&:display_count=yes" width="650px" height="530px" frameborder="0"></iframe>

#### 我的其他作品（期中项目和日常小练手）
<div class="tiles">
{% for post in site.categories.visualization %}
  {% include post-grid.html %}
{% endfor %}
</div><!-- /.tiles 把所有categories 有 visualization 的列出来-->