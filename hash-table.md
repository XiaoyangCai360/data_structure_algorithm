# 哈希表 Hash Table

## 1. 哈希表基础

> 哈希表（Hash Table）：也叫做 **散列表**。
> 是一种根据**关键码值**(Key Value)直接进行访问的数据结构。

* 哈希表通过「键 `Key`」和「映射函数 `Hash(Key)`」计算出对应的「值 `Value`」，把关键码值映射到表中的一个位置来进行访问。映射函数叫做「哈希函数 Hash Function」，存放元素的数组叫做「哈希表（散列表）」。
* 一般哈希表用来判断 **一个元素是否出现在集合中**。

## 2. 哈希函数 Hash Function 
哈希函数应该满足以下特点：
* 易于计算，并使计算出的索引值 **均匀**分布
* 计算出来的哈希值 **长度固定**
* **单射**：如果`Hash(key1) != Hash(key2)` ，则`key1`和`key2`一定不相等

常用的哈希函数方法有：
* 直接寻址法
* 除留余数法
* 平方取中法
* 基数转换法

## 3. 哈希碰撞 Hash Collision

> 哈希碰撞 Hash Collision：不同的关键字（key）通过哈希函数后得到相同的哈希地址，即 key1 != key2，但是 hash(key1) == hash(key2)。

常用的解决哈希碰撞的方法有两类，分别是「**线性探测法**」和「**拉链法**」。

### 3.1 线性探测法
* 当发生哈希碰撞时，线性向后找一个空位放置。
* 使用线性探测法时，一定要保证哈希表的大小`table_size`大于数据大小`data_size`。

### 3.2 拉链法
* 当发生哈希碰撞时，将具有相同地址的元素存储在同一个线性 **链表**中。
* 拉链法会占用更多内存，所以要选择适当的哈希表大小，不要因为数组太长而浪费大量 **空间**，也不因为链表太长而在查找上浪费大量 **时间**。

## 4. 哈希表相关题目
| 题号 | 标题 | 标签 | 难度 |
| ----------- | ----------- | ----------- | ----------- |
| 0001 | [两数之和 Two Sum](https://leetcode.com/problems/two-sum/) | 哈希表 | 简单 |
| 0202 | [快乐数 Happy Number](https://leetcode.com/problems/happy-number/description/) | 哈希表 | 简单 |
| 0242| [有效的字母异位词 Valid Anagram](https://leetcode.com/problems/valid-anagram/) | 哈希表 | 简单
| 0349 | [两个数组的交集 Intersection of Two Arrays](https://leetcode.com/problems/intersection-of-two-arrays/) | 哈希表 | 简单
| 0383 | [赎金信 Ransom Note](https://leetcode.com/problems/ransom-note/description/) | 哈希表 | 简单
| 0015 | [三数之和 3Sum](https://leetcode.com/problems/3sum/description/) | 哈希表 | 中等 
| 0018 | [四数之和 4Sum](https://leetcode.com/problems/4sum/description/) | 哈希表 | 中等
| 0454 | [四数相加II 4Sum II](https://leetcode.com/problems/4sum-ii/description/) | 哈希表 | 中等
