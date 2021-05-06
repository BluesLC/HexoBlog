---
title: Markdown语法速查
url: 208.html
id: 208
categories:
  - Markdown
date: 2018-05-19 22:30:01
tags:
---

1\. 分级标题
========

语法： #一级标题 ##二级标题 ###多级标题 显示:

一级标题
====

二级标题
----

### 多级标题

* * *

2\. 强调
======

语法： \*斜体\* 或 _斜体_ ** 加粗 ** *** 斜体加粗 *** ~~删除线~~ 显示: _斜体_ 或 _斜体_ **加粗** **_斜体加粗_** 删除线

* * *

3\. 块引用
=======

语法： >一级缩进 >>二级缩进 >>>多级缩进 显示:

> 一级缩进
> 
> > 二级缩进
> > 
> > > 多级缩进

* * *

4\. 列表
======

4.1 符号列表
--------

语法： \- 符号列表1 + 符号列表2 * 符号列表3 显示:

*   符号列表1

*   符号列表2

*   符号列表3

4.2 数字列表
--------

语法： 1.数字列表1 2.数字列表2 3.数字列表3 显示:

1.  数字列表1
2.  数字列表2
3.  数字列表3

* * *

5\. 分割线
=======

语法: \* \* \* \*\*\* \*\*\*\*\*\* \- \- \- \-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\- 显示:

* * *

* * *

* * *

\- \- \- \-
-----------

* * *

6\. 代码块
=======

语法： `一行代码` ``` 一段代码 ``` 显示: `cout << count;`

```
    #include<iostream>
    #include<cmath>
    using namespace std;
    bool isprimnum(int i);
    bool isprimnum(int i) {
     for (int temp = 2; temp < sqrt(i)+1;++temp) {
     if (i%temp == 0) 
     return false;
     }
     return true;
    }
    int main() {
     int count, num;
     cin >> num;
     count = 0;
     if (num < 100000) {
     for (int i = 3; i <= num - 2;i += 2) {
     if (isprimnum(i) && isprimnum(i + 2)) 
     ++count;
     }
     cout << count;
     }
     return 0;
    }
	
```  

* * *

7\. 超链接
=======

7.1 行内式
-------

语法: 欢迎来到\[LC的博客\]([http://blog.luchong.xyz/](http://blog.luchong.xyz/)) 显示: 欢迎来到[LC的博客](http://blog.luchong.xyz/)

7.2 参考式
-------

语法: \[Redemption\]\[1\]是我的博客 \[1\]:[http://blog.luchong.xyz/](http://blog.luchong.xyz/) 显示: [LLC](http://blog.luchong.xyz/)是我的博客

* * *

8\. 转义符
=======

语法: \ + 任意Markdown符号 例:\\\[\\\] \\> \\* 显示: 输出原本的符号 例:\[\] > *