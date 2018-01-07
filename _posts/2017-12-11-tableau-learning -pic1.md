---
layout: article
title:  "Tableau 图表类型详解"
date:   2017-12-11 23:55:12 +0800
categories: posts infovis
image:
  teaser: 凹凸4.jpg
  feature: 凹凸4.jpg
---
# 在tableau中总会有些图是晦涩难解的，本笔记解释本人不懂的图表。
---

## Tableau 凹凸图
* 凹凸图用于使用Measure值之一来比较两个尺寸。它们对于探索时间维度或地方维度或与分析相关的其他维度的值的变化非常有用。
凹凸图采用两个维度，零个或多个度量。

## 如何创建凹凸图

* 第1步
   * 将维子类别拖放到列框。还可将标注运输模式拖动到标记卡下的颜色货架。 将图表类型保留为自动。然后我们得到下面的图表。
   <span class="image left"><img src="{{ "/images/凹凸1.jpg" | absolute_url }}" alt="" /></span>
* 第2步
   * 接下来我们创建一个名为Rank的计算字段。转到分析创建计算字段。使用Rank作为字段名称，并在计算区域中写入表达式index()。它是一个内置函数，用于为分区中的当前行创建索引。单击确定，新字段将显示在度量部分。 右键单击字段Rank并将其转换为离散。
   <span class="image left"><img src="{{ "/images/凹凸2.jpg" | absolute_url }}" alt="" /></span>
* 第3步
   * 将Rank拖动到行搁板。下图显示尺寸子类别，每个船舶模式按其Rank值的升序排列。
   <span class="image left"><img src="{{ "/images/凹凸3.jpg" | absolute_url }}" alt="" /></span>
* 第4步
   * 接下来，我们使用度量利润对等级字段应用一些更多的计算。在排名上，选择编辑表计算。 选择按字段利润排序，使用按子类别划分和按船模式寻址。下图显示了应用的计算。
   <span class="image left"><img src="{{ "/images/凹凸配图.jpg" | absolute_url }}" alt="" /></span>
* 完成上述步骤后，我们得到凹凸图，如下所示。它显示了不同子类别下每种船舶模式的利润变化。

```图表来自w3school```