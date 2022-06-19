---
title: Cmu15445 课程介绍
subtitle: ""
date: 2022-02-09T22:28:09.315Z
summary: Cmu15445 Summary
draft: false
featured: true
tags:
  - database
image:
  filename: featured.png
  focal_point: Smart
  preview_only: false
---
# Cmu15445 课程介绍


## 大纲

简单介绍下 [cmu15445](https://15445.courses.cs.cmu.edu/fall2020/) 的[教学大纲](https://15445.courses.cs.cmu.edu/fall2020/syllabus.html)，该课以 [Database System Concepts](https://www.db-book.com/db7/index.html) 为辅助教材， 讲述了数据库管理系统（DBMS）设计和实现的方方面面，包括：

1.  数据模型（关系型，文档型，键值型）
2.  存储模型（n-ary，decomposition，可以理解为行式、列式）
3.  查询语言（sql，存储过程 stored procedures）
4.  存储结构（heaps，基于日志 log-structured）
5.  索引设计（排序树，哈希表）
6.  事务处理（ACID，并发控制）
7.  数据恢复（日志、快照）
8.  执行引擎（joins，排序，聚集，优化）
9.  并发架构（多核，分布式）

可以看出，内容十分翔实，课程使用一个开源的商业数据库作为案例进行讲解，以深入探讨数据库设计时，在上述各个方面进行取舍的过程。[代码实验](https://15445.courses.cs.cmu.edu/fall2020/assignments.html)。

## 计划

这次学习目标主要以实验为主，兼顾看点讲义和教科书。视频暂时就随缘了，不然战线会拉很长，导致最后都搞不完。一共有五个实验：

1.  环境准备：[C++ Primer](https://15445.courses.cs.cmu.edu/fall2020/project0/)
2.  缓冲控制：[Buffer Pool Manager](https://15445.courses.cs.cmu.edu/fall2020/project1/)
3.  B+ 树索引：[B+Tree Index](https://15445.courses.cs.cmu.edu/fall2020/project2/)
4.  查询引擎：[Query Execution](https://15445.courses.cs.cmu.edu/fall2020/project3/)
5.  并发控制：[Concurrency Control](https://15445.courses.cs.cmu.edu/fall2020/project4/)

五个实验组成了一个用于教学的简单的关系型数据库 —— [BusTub](https://github.com/cmu-db/bustub)。 实验方式基本都是实现一些规定的接口，跑通写好的测试用例。需要说明的是，代码中给的测试用例十分简单，基本只测试了一些主干路径，因此跑过了测试用例并不一定说明你代码写的没问题，这就要求在实现的过程中务必理解实验各个接口的关系、可以进行取舍实现的要点。为了达到此目的，当自己做完并跑过测试用例后，可以在网上找一些前人实现的材料，对比学习。

初步打算，除了第一个环境准备外，每个实验做完之后写一篇总结，探讨一些实现中遇到的问题和有趣的地方。

## 资料

课程本身相关的资料都可以去[课程网站](https://15445.courses.cs.cmu.edu/fall2020/syllabus.html)上寻找，我计划做 fall2020 年的实验，但[视频](https://www.youtube.com/playlist?list=PLSE8ODhjZXjbohkNBWQs_otTrBTrjyohi)似乎只有 2019 年的。

在实现过程中如果遇到比较好的博客或者资料，我会逐渐补充到这里。

