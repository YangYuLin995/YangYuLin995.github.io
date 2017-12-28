---
layout: post
title:  "搭建博客 学习笔记"
date:   2017-12-24
excerpt: "学习markdown语法是搭建博客的基础，博客的所有文章都可以有markdown文本来构建。"
image: "/images/pic02.jpg"
---

## 如何使用Markdown 
先将jekyll下载并安装 [how to install Jekyll](https://jekyllrb.com/)。

将我们要复制的模板下载下来 [here](https://github.com/iwiedenm/jekyll-theme-massively) 将它存放在任意文档即可。

打开一个命令行工具并输入 ```cd``` 后面空格加文件路径。

然后输入： ```bundle exec jekyll serve```. 随后打开后面的网址就能拥有一个属于自己的博客 [http://127.0.0.1:4000/](http://127.0.0.1:4000/). Have fun exploring your new site!

##重点内容
当一个博客的页面出现后，要务必更改```_config.yml``` 文档，修改基本个人信息以及博客信息。
