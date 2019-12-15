# 数组

## 数据结构

内存模型：一段存储相同数据类型的连续内存空间。

```text
对于连续的内存空间，可通过偏移量来存取指定位置的数据。比如——
数组i元素的存取：baseAddr + i*sizeof (element)
结构体某字段存取：baseAddr + sizeof (subStrunt)
```

## 算法

### 指定位置存取

由内存模型知，计算偏移量即可。时间复杂度为O\(1\)。

### 指定位置插入

插入位置的右区间元素需要迁移。时间复杂度为O\(n\)。

```text
场景优化举例
1.有序数组m次插入，可全部插入尾部，最后一次排序。O(m*n) => O(m)+O(n*lgn)
```

### 指定位置删除

删除位置的右区间元素需要迁移。时间复杂度O\(1\)。

```text
场景优化举例
1.数组m次删除，可先标记后清除。O(m*n) => O(m+n)
```

## 注意事项

### 越界问题

### 扩容问题

### C语言中数组与指针的区别

## 工程应用

### NSArray是怎样优化数组性能的？

NSArray使用了一个环形数组，保证头尾插入删除都是O\(1\)时间复杂度。 而插入到其它位置，会选择插入位置左右区间中较小的那边来迁移数据。

## Reference

[https://ciechanow.ski/exposing-nsmutablearray/](https://ciechanow.ski/exposing-nsmutablearray/)

## 经典题目

## 参考答案

[source](https://github.com/haibazhang/lib/blob/master/src/cs/algorithm-and-data-structure/linear-list/数组.md) \| [edit-online](https://github.com/haibazhang/lib/edit/master/src/cs/algorithm-and-data-structure/linear-list/数组.md)

