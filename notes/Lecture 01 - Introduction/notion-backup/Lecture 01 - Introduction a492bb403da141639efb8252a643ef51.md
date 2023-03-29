# Lecture 01 - Introduction

<aside>
💡

</aside>

## 视频——笔记

### Topic:

### 关键词

- ****可扩展性（Scalability）****

- **可用性（Availability）**
- ****一致性（Consistency）****

### 笔记

- 四个目的：
    - 足够多的机器带来足够多的性能。但是并不是一千个硬盘带来一千倍数性能。
    - 解决物理上机器分隔的同步问题。但是并发执行同步异步等系统设计很复杂。
    - 在物理上不同机器隔离，避免恶意程序保证安全。但是计算机组成复杂，局部错误会带来更大的问题。
    - 容错的需要：一台坏了换成另外一台
- 存储，通信（网络），计算
- 性能：追求****可扩展性（Scalability）****，一台计算机一小时，两台计算机半小时。
    - 需要特殊的架构实现无限的扩展
- 容错：系统屏蔽错误，在错误下保持运行。
- **可用性（Availability）**，在特定的错误下继续提供服务
    - 可用系统，一定的错误内可以继续提供服务，例如两台服务器只坏一台。
    - 非易失存储
    - 复制到副本，但问题是不同不同副本之间不一定互为副本，我学过的另一个地方给出了解决方法：
        
        [NoSql有三大原理：CAP、BASE、最终一致性](Lecture%2001%20-%20Introduction%20a492bb403da141639efb8252a643ef51/NoSql%E6%9C%89%E4%B8%89%E5%A4%A7%E5%8E%9F%E7%90%86%EF%BC%9ACAP%E3%80%81BASE%E3%80%81%E6%9C%80%E7%BB%88%E4%B8%80%E8%87%B4%E6%80%A7%200d465cc97460483f8c066c6191103df8.md)
        
- ****一致性（Consistency）：例如redis先set一个k/y，推送到副本服务器A和B里，然后修改为k/y2，副本服务器A和B里，如果A故障了，可能在A服务器get到y而不是修改后的值y2。****
    - 弱一致：不一定是最近一次修改的内容。
    - 强一致：可以获取最近一次修改的内容。
        - 可以用读两个服务器的方法确定。
        - 通信成本太高。
- 自我可恢复性（recoverability）是一个更低的要求，出错后不影响整体服务，修复后任然可用，
- MapReduce：Map函数和Reduce函数。
    - 论文中的原例子：
        
        map (k1,v1) → list(k2,v2)
        reduce (k2,list(v2)) → list(v2)
        
    - 以一个字母计数器为例：
    - Map函数从输入中创建键值对，例如三个输入然后根据三个输入的内容创建键值对，输入1里得出有键值对(a/1 , b/1)，输入2里有键值对(a/1 , c/1)，输入1里有键值对( b/1)，
    - Reduce函数总结键值对，将上面的两个a/1归类在一起 得a/2，两个b/1归类在一起得b/2，一个c/1归类在一起得c/1
    - Map函数和Reduce函数是并行执行的，并且可以在数千台机器上同时运行

Job。整个MapReduce计算称为Job。

Task。每一次MapReduce调用称为Task。

一个完整的MapReduce Job，由一些Map Task和一些Reduce Task组成

## 摘要部分

<aside>
📌 一些概念。现在谷歌也不用这个了。只是有欣赏和学习的价值。

</aside>

## 论文——笔记

### Topic: 思维导图

### Recall

### Notes

[MapReduce-Simplified-Data-Processing-on-Large-Clusters.pdf](Lecture%2001%20-%20Introduction%20a492bb403da141639efb8252a643ef51/MapReduce-Simplified-Data-Processing-on-Large-Clusters.pdf)

<aside>
📌 **SUMMARY:**

</aside>

---

## 复习：常看常新

### Date: November 5, 2019

### Topic:

### Recall

### Notes

- ...
- ...

<aside>
📌 **SUMMARY:**

</aside>

---

### Date: November 5, 2019

### Topic:

### Recall

### Notes

- ...
- ...

<aside>
📌 **SUMMARY:**

</aside>

---