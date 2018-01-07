---
layout: article
title:  "Tableau 图表类型详解"
date:   2017-12-13 23:55:12 +0800
categories: posts infovis
image:
  teaser: box配图.jpg
  feature: box配图.jpg
---
# 在tableau中总会有些图是晦涩难解的，本笔记解释盒形图。
---

## Tableau 盒行图
* 盒形图也称为盒 - 须图。 它们显示沿轴的值的分布。框表示中间50％的数据，即数据分布的中间两个四分位数。剩余50％的数据在两侧由线也称为晶须，以显示1.5倍四分位距范围内的所有点，该范围是邻接框宽度的1.5倍内的所有点，或在数据最大范围内的所有点。
箱形图采用一个或多个零个或多个维度的度量。


## 如何创建盒形图

* 第1步
   * 将维度类别拖放到列栏架，并在行框架中获利。还要将维度运输模式拖动到列栏框中的类别右侧。
* 第2步
   * 从Show me中选择Box-and-Whisker plot。显示下图显示框图。在这里，Tableau会自动将出货模式重新分配给标记卡。
   <span class="image left"><img src="{{ "/images/box1.jpg" | absolute_url }}" alt="" /></span>

 ## 具有两个尺寸的箱线图
* 我们可以通过向列栏架添加另一个维度来创建具有两个维度的箱线图。在上面的图表中，我们将区域维添加到列架。这将生成一个图表，显示每个区域的箱线图。
   <span class="image left"><img src="{{ "/images/box2.jpg" | absolute_url }}" alt="" /></span>
   
```图表来自w3school```