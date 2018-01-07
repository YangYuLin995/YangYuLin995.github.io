---
layout: article
title:  "Tableau 图表类型详解"
date:   2017-12-12 23:55:12 +0800
categories: posts infovis
image:
  teaser: 甘特配图.jpg
  feature: 甘特配图.jpg
---
# 在tableau中总会有些图是晦涩难解的，本笔记解释甘特图。
---

## Tableau 甘特图
* 特图显示了一段时间内任务或资源的值的进度。它广泛用于项目管理和其他类型的变化在一段时间的研究。 因此，在甘特图中，时间维度是一个重要领域。
除了时间维度之外，甘特图至少还需要一个维度和一个度量。

## 如何创建凹凸图

* 第1步
   * 将维度订单日期拖动到列框架和子类别到行搁架。接下来，我们将订单日期添加到过滤器架。还要右键点击订单日期，将其转换为确切的日期值。它是如下图所示。
   <span class="image left"><img src="{{ "/images/甘特1.jpg" | absolute_url }}" alt="" /></span>
* 第2步
  * 接下来，我们编辑过滤条件以选择日期范围。这是因为我们需要单独的日期值，并且数据中有非常多的日期。创建范围如下所示。
   <span class="image left"><img src="{{ "/images/甘特2.jpg" | absolute_url }}" alt="" /></span>
* 第3步
  * 接下来，我们将尺寸出货模式拖动到颜色货架，将度量数量拖到标记卡下面的尺寸货架。这将产生甘特图，如下所示。
   <span class="image left"><img src="{{ "/images/甘特3.jpg" | absolute_url }}" alt="" /></span>

```图表来自w3school```