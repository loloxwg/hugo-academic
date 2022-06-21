---
title: A fault-tolerant KV server on top of Raft
date: 2022-06-18T19:34:40.476Z
summary: TalentPlan(3)
draft: false
featured: true
tags:
  - database
  - PingCAP
image:
  filename: featured
  focal_point: Smart
  preview_only: true
---
分享一下前两天在 [Talent Plan Community](https://asktug.com/t/topic/665859) 华东师范大学孙佳丽做的有关 TinyKV 的介绍 

这次分享主要从TinyKV的整体架构,组件介绍,调用流程,raft优化四个方面展开，并给出了一些有用的参考

注：以下仅为图片，

![](A%20fault-tolerant%20KV%20server%20on%20top%20of%20Raft_01.png)
![](A%20fault-tolerant%20KV%20server%20on%20top%20of%20Raft_02.png)
![](A%20fault-tolerant%20KV%20server%20on%20top%20of%20Raft_03.png)
![](A%20fault-tolerant%20KV%20server%20on%20top%20of%20Raft_04.png)
![](A%20fault-tolerant%20KV%20server%20on%20top%20of%20Raft_05.png)
![](A%20fault-tolerant%20KV%20server%20on%20top%20of%20Raft_06.png)
![](A%20fault-tolerant%20KV%20server%20on%20top%20of%20Raft_07.png)
![](A%20fault-tolerant%20KV%20server%20on%20top%20of%20Raft_08.png)
![](A%20fault-tolerant%20KV%20server%20on%20top%20of%20Raft_09.png)
![](A%20fault-tolerant%20KV%20server%20on%20top%20of%20Raft_10.png)
![](A%20fault-tolerant%20KV%20server%20on%20top%20of%20Raft_11.png)
![](A%20fault-tolerant%20KV%20server%20on%20top%20of%20Raft_12.png)
![](A%20fault-tolerant%20KV%20server%20on%20top%20of%20Raft_13.png)
![](A%20fault-tolerant%20KV%20server%20on%20top%20of%20Raft_14.png)
![](A%20fault-tolerant%20KV%20server%20on%20top%20of%20Raft_15.png)
![](A%20fault-tolerant%20KV%20server%20on%20top%20of%20Raft_16.png)
![](A%20fault-tolerant%20KV%20server%20on%20top%20of%20Raft_17.png)
![](A%20fault-tolerant%20KV%20server%20on%20top%20of%20Raft_18.png)
![](A%20fault-tolerant%20KV%20server%20on%20top%20of%20Raft_19.png)
![](A%20fault-tolerant%20KV%20server%20on%20top%20of%20Raft_20.png)
![](A%20fault-tolerant%20KV%20server%20on%20top%20of%20Raft_21.png)
![](A%20fault-tolerant%20KV%20server%20on%20top%20of%20Raft_22.png)
![](A%20fault-tolerant%20KV%20server%20on%20top%20of%20Raft_23.png)
![](A%20fault-tolerant%20KV%20server%20on%20top%20of%20Raft_24.png)
## 参考资料
1. [Etcd 之 Lease read](https://z.itpub.net/article/detail/29B4D408D967AE015AF40C2C47F7E5AE)
2. [etcd-raft ReadIndex 线性一致性读源码简析](https://qtozeng.top/2019/01/15/etcd-raft-ReadIndex-%E7%BA%BF%E6%80%A7%E4%B8%80%E8%87%B4%E6%80%A7%E8%AF%BB%E6%BA%90%E7%A0%81%E7%AE%80%E6%9E%90/)
3. [TiKV 功能介绍 - Raft 的优化 | PingCAP](https://pingcap.com/zh/blog/optimizing-raft-in-tikv)
4. [TiKV 功能介绍 - Lease Read | PingCAP](https://pingcap.com/zh/blog/lease-read)
5. [TiKV 源码解析系列文章（十九）read index 和 local read 情景分析 | PingCAP](https://pingcap.com/zh/blog/tikv-source-code-reading-19)
6. [如何在 Raft 之上构建Key-Value Server](https://learn.pingcap.com/learner/course/510001/file/570002;offeringId=720002)
