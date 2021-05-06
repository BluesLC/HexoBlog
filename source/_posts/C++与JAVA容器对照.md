---
title: 'C++与JAVA容器对照'
url: C++与JAVA容器对照.html
categories:
  - C++
date: 2019-01-03 21:07:50
tags:
  - C++
---

| c++ | JAVA | 目的 |
| ------ | ------ | ------ |
|array|[ ]|固定大小的数组|
|vector|ArrayList|可变长度的数组|
||Vector|可变长度数组，支持同步操作，效率比ArraList略低|
|list|LinkedList|链表，便于增删|
|forward_list||单链表，注意不提供size()操作|
|deque|ArrayDeque|双端队列|
|stack|Stack|栈|
|queue|Queue|队列|
|priority_queue|PriorityQueue|支持优先级的队列|
|set|TreeSet|集合，数据有序，通过二叉树实现|
|multiset||集合，允许重复数据|
|unordered_set|HashSet|hash组织的set|
|unordered_multiset||hash组织的multiset|
||LinkedHashSet|按插入有序，支持hash查找|
|map|TreeMap|key_value映射，按照key有序|
|multimap||允许重复key的map|
|unordered_map|HashMap|hash组织的map|
|unordered_multimap||hash组织的multimap|
||LinkedHashMap|按插入有序，支持hash查找|
||HashTable|类似HashMap，支持同步操作|
|bitset|BitSet|位操作|



