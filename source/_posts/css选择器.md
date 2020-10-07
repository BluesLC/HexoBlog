---
title: css学习笔记(一)
url: 258.html
id: 258
categories:
  - 前端
date: 2018-07-27 18:18:21
tags:
---

派生选择器
-----

### 标签派生选择器

    li strong {
    font-style: italic;
    font-weight: normal;
    }
    

可以理解为在`<li>`标签内的`<strong>`标签应用此样式.

### id派生选择器

    #sidebar p {
    font-style: italic;
    text-align: right;
    margin-top: 0.5em;
    }
    

可以理解为在id为sidebar的标签内的`<p>`标签应用此样式.

### 类派生选择器

    .fancy td {
    color: #f60;
    background: #666;
    }
    

在类名为fancy的标签内的`<td>`标签应用此样式

多值属性选择器
-------

    [title~=hello] { 
    color:red; 
    }
    

由空格分隔的属性应用此样式

    [lang|=en] { color:red; }
    

由-分隔的属性应用此样式

​