---
layout: default
title:  "Tableau 学习笔记"
date:   2017-12-07 23:55:12 +0800
categories: posts infovis
image:
  teaser: 配图7.jpg
  feature: 配图7.jpg
---
# Tableau中的图表归纳
---

## tableau中有哪些图表和特性归纳
* 条形图
    * 条形图位居最常见数据可视化方式之列。利用条形图，可迅速做出比较，一目了然地揭示高低点。如果数值数据能够顺畅归入不同类别，那么条形图就尤为有效，便于您快速看清数据中显示的趋势。
    * 何时使用：跨类别比较数据 。示例 ：不同尺寸衬衫的量 、按来源站点划分的网站流量 、按分区划分的消费比率。
* 折线图
    * 和条形图和饼图一样，折线图也是最常用的一种图表类型。折线图可连接各个单独的数值数据点，以简单、直接的方式可视化数值序列，其主要用途就是显示一段时间内的趋势。
    * 何时使用：查看数据中随时间推移的趋势。例如：五年期的股价变化、一个月内的网页查看数、逐季收入增长情况。
* 饼图
    * 饼图用来显示信息的相对比率（或百分率）。但饼图往往遭到无节制的滥用，置这一建议的限定情境于不顾。结果就是，饼图是误用最多的图表类型。
    * 何时使用：显示比率。例如：花费在不同部门的预算、对调查的回答类别、美国人度过休闲时光方式的细分情况。
* 地图
    * 无论是邮政编码、州简称、国名，还是自定义地理编码，有任意一种位置数据的情况下，您都需要在地图上查看数据。
    * 何时使用：显示地理编码数据。示例：按州划分的保险索赔、按国家划分的出口目的地、按邮政编码划分的车祸 、自定义销售区域 。
* 散布图
    * 散布图是大概了解趋势、集中度、极端数值的有效方式，可指导您应该进一步把考察工作着重在哪一方面。
    * 何时使用：考察不同变量之间的关系。示例：男女在不同年龄得肺癌可能性的比较情况、技术较早与较晚接纳者的智能手机购买模式、不同地区不同产品类别的配送成本。
* 甘特图
    * 甘特图对于说明项目各元素的起始与终止日期效果非常好，清楚看到需要完成的内容和截止时间对于项目的成功非常关键。
    * 何时使用：显示项目进度。例如：说明关键可交付成果、所有者、截止期限。
	* 何时使用：显示随时间推移的其他事物使用事项。例如：机器使用的持续时间、团队成员有空与否。
* 气泡图
    * 气泡图不是自成一类的可视化，而应视为强调散布图或地图上数据的手段。我们使用气泡图的原因是圆圈的不同大小揭示数据的意义。
    * 何时使用：显示数据沿两个轴的集中度。例如：按产品和地理划分的销售集中情况、按院系和一天中时间段划分的课程出勤情况。
* 直方图
    * 希望查看数据的跨组分布情况时使用直方图。举例来说，您有 100 只南瓜，希望了解有多少只是 2 磅或以下，多少只 3 到 5 磅，多少只 6 到 10 磅等等。把数据分组到这些类别中，然后使用直条形沿一根轴标绘，就能看到南瓜的重量分布情况。在以上过程中，直方图也就创建了出来。
    * 何时使用：了解数据的分布情况。示例：按公司大小划分的客户数量、学生的考试成绩、产品缺陷频率。
* 靶心图
    * 设定了目标并希望参照目标跟踪进展时，靶心图就是理想之选。就其核心而言，靶心图是另一种形式的条形图。其设计宗旨是替代仪表板量具、仪表和温度计，因为这些图像一般不能显示足够的信息，并且需要占用宝贵的仪表板空间。
    * 靶心图将主要度量值（比如年初迄今收入）与一个或多个其他度量值（比如年收入目标）比较，并且以明确的绩效指标为背景（例如销售配额），呈现比较情况。通过靶心图可立即看清主要度量值相对于总体目标的表现情况（例如某个销售代表距离完成年度配额还有多少）。
    * 何时使用：参照目标评估指标表现。例如：销售配额评估、实际花费与预算的比较情况、绩效优劣范围（优/良/差）。
* 热点图
    * 热点图是使用色彩跨两个类别比较数据的理想方式。作用是快速看清两个类别的交集哪里最强，哪里最弱。
    * 显示两种因素间的关系。例如：目标市场客户群分析、跨区域产品采用情况、按个人代表划分的销售线索。
* 突出显示表
    * 突出显示表让热点图更进一步。除了用色彩显示数据的交叉情况外，突出显示表还在上方添加数字，提供更多详细信息。
    * 何时使用：提供热点图相关详细信息。例如：不同细分市场占总体市场比例、按特定地区中代表划分的销售数字 、不同年份中的城市人口。
* 树形图
    * 是否希望一目了然看清您的数据，发现不同部分与整体的关系？那么，树形图就非常适合您。这些图表使用一系列的矩形，嵌套在其他矩形内，以相对于整体的比例显示分层数据。 
    * 何时使用：以相对于整体的比例显示分层数据：如各个电脑主机的存储空间使用情况，管理技术支持案例的数量与优先级，比较各年份之间的财务预算。







