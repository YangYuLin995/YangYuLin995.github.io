---
layout: article
title:  "关于HTML链接的笔记"
date:   2017-12-23 23:55:12 +0800
categories: posts rwd
image:
  teaser: html彩色.jpg
  feature: html彩色.jpg
---
# 本笔记归纳了有关HTML超链接的笔记
---
{% include toc.html %}

## HTML 链接
* TML 超链接（链接）
  * HTML使用标签 < a >来设置超文本链接。
  * 超链接可以是一个字，一个词，或者一组词，也可以是一幅图像，您可以点击这些内容来跳转到新的文档或者当前文档中的某个部分。
  * 当您把鼠标指针移动到网页中的某个链接上时，箭头会变为一只小手。
  * 在标签< a > 中使用了href属性来描述链接的地址。
* 默认情况下，链接将以以下形式出现在浏览器中：
  * 一个未访问过的链接显示为蓝色字体并带有下划线。
  * 访问过的链接显示为紫色并带有下划线。
  * 点击链接时，链接显示为红色并带有下划线。

## HTML 链接语法
* 链接的 HTML 代码很简单。它类似这样：
```< a href="url" >链接文本< /a >```
* href 属性描述了链接的目标。

## HTML 链接 - target 属性
使用 target 属性，你可以定义被链接的文档在何处显示。
* 下面的这行会在新窗口打开文档：
```< a href="http://www.yangyulin995.github.io/" target="_blank">一直学习的学习博客< /a >```

## HTML 链接- id 属性
* id属性可用于创建在一个HTML文档书签标记。
* 提示: 书签是不以任何特殊的方式显示，在HTML文档中是不显示的，所以对于读者来说是隐藏的。

## 基本的注意事项 - 有用的提示
* 注释： 请始终将正斜杠添加到子文件夹。假如这样书写链接：href="http://www.runoob.com/html"，就会向服务器产生两次 HTTP 请求。这是因为服务器会添加正斜杠到这个地址，然后创建一个新的请求，就像这样：href="http://www.runoob.com/html/"。