---
title: 操作系统中的锁
date: 2020-06-17T12:20:37.645Z
summary: 原子操作 中断
draft: false
featured: true
tags:
  - os
image:
  filename: featured
  focal_point: Smart
  preview_only: false
---
两个核心点

* 原子操作
* 中断

锁是解决并发同步问题的关键，从本文来看，锁有两个核心点，一个是原子操作，另一个则是中断；\
通过原子操作来实现临界区标志位的改变，关闭中断来避免CPU中途离开导致数据同步失败问题。\
自旋锁(spinlock)是锁的最小原型，其它锁都是以它为基础来实现的，自旋锁的实现也颇为简单，只需一个简单的原子标志位就可以实现了，当然还要妥善管理中断。\
在 xv6 中，对锁的实现只有两种，一种是刚才提到的 spinlock，而另外一种则是 sleeplock，spinlock 不会让出 CPU 执行权，而 sleeplock 则是在 spinlock 的基础上，增加 sleep 功能，即如果一个执行体(线程或者进程)加锁失败，就会进入休眠状态，让出 CPU 执行权，让其它的任务也能得以执行。\
本文中的信号量(sem)也是 sleeplock 的一种，sem 的实现更为精致，通过等待队列来记录加锁失败的执行体，并后续通过一定的策略来选择唤醒，这也是很多编程语言中信号量的实现方式。\
当然不同的语言会有不同的优化，比如 go 的 Mutex 是非公平的唤醒机制，但是针对非公平的场景，又设有饥饿补偿，总之本文中实现的 sem 几乎是任何信号量（锁）实现的基础蓝本。

```
 spinlock_t lock;
  x86_spin_lock_init(&lock);
  // 加锁，如果加锁成功则进入下面代码执行
  // 否则，一直自旋，不断检查 lock 值为否为 0
  x86_spin_lock_disable_irq(&lock);
  // 处理一些数据同步、协同场景
  doing_something();
  // 解锁
  x86_spin_unlock_enabled_irq(&lock);


  sem_t sem;
  x86_sem_init(&sem);
  // 加锁，减少信号量，如果信号量已经为 0
  // 则加锁失败，当前线程会改变为 sleeping 状态
  // 并让出 CPU 执行权
  krlsem_down(&sem);
  // 处理一些数据同步、协同场景
  doing_something();
  // 解锁，增加信号量，唤醒等待队列中的其它线程（若存在）
  krlsem_up(&sem);
```
