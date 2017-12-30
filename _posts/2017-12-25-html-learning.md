---
layout: post
title:  "HTML 学习笔记"
date:   2017-12-25
excerpt: "学习搭建网站离不开学习HTML，本篇笔记内容是关于HTML的元素语法。"
categories: rwd
image: "/images/pic02.jpg"
---

## HTML 元素语法
* HTML 元素以开始标签起始
* HTML 元素以结束标签终止
* 元素的内容是开始标签与结束标签之间的内容
* 某些 HTML 元素具有空内容（empty content）
* 空元素在开始标签中进行关闭（以开始标签的结束而结束）
* 大多数 HTML 元素可拥有属性

## 举例说明
*  < p > 元素：
```< p >This is my first paragraph.< /p >```
这个 ```< p >``` 元素定义了 HTML 文档中的一个段落。
这个元素拥有一个开始标签``` < p >```，以及一个结束标签``` < /p >```。
元素内容是：This is my first paragraph。

* < body > 元素：
```< body >
< p >This is my first paragraph.< /p >
< /body >```
```< body >``` 元素定义了 HTML 文档的主体。
这个元素拥有一个开始标签 ```< body >```，以及一个结束标签 ```< /body >```。
元素内容是另一个 HTML 元素（p 元素）。

* < html > 元素：
```< html >

< body >
< p >This is my first paragraph.< /p >
< /body >

< /html >```
```< html >```元素定义了整个 HTML 文档。
这个元素拥有一个开始标签 ```< html >```，以及一个结束标签 ```< /html >```。
元素内容是另一个 HTML 元素（body 元素）。

### 空的 HTML 元素
没有内容的 HTML 元素被称为空元素。空元素是在开始标签中关闭的。
```< br >``` 就是没有关闭标签的空元素（```< br >``` 标签定义换行）。
在 XHTML、XML 以及未来版本的 HTML 中，所有元素都必须被关闭。
在开始标签中添加斜杠，比如 ```< br / >```，是关闭空元素的正确方法，HTML、XHTML 和 XML 都接受这种方式。
即使 ```< br >``` 在所有浏览器中都是有效的，但使用 ```< br / >``` 其实是更长远的保障。