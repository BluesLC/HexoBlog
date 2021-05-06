---
title: 'public, protected, private关键字总结'
url: 235.html
id: 235
categories:
  - 面向对象
date: 2018-07-17 16:12:26
tags:
---

### 1\. 三种成员的区别

*   public : 在所有用户都可以直接调用
*   protected : 只有自己和子类可以调用
*   private : 只有自己可以调用

### 2\. 三种继承的区别

我们可以有一个大致的概念,就是private是权限最高的,protected次之,public权限最低.当权限低的成员遇到权限高的继承时,成员权限也会相应的变高.

关于public, protected, private 继承总结:

*   public继承:
    
    *   基类public成员依然为public成员
    *   基类protected成员依然为protected成员
    *   基类private成员不可访问
*   protected继承:
    
    *   基类public成员变为protected成员
    *   基类protected成员变为protected成员
    *   基类private成员不可访问
*   private继承:
    
    *   基类public成员变为private成员
    *   基类protected成员变为private成员
    *   基类private成员不可访问