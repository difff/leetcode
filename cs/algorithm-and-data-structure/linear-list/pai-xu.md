# 排序

## 序

本篇介绍3种通用基本排序及其改进算法，然后介绍归并排序，最后介绍3种非通用的特殊排序方法。

| 排序算法 | 时间复杂度 | 空间复杂度 | 是否稳定 | 是否通用 |
| :--- | :--- | :--- | :--- | :--- |
| 冒泡排序 | $O\(n^2\)$ | $O\(1\)$ | Y | Y |
| 快速排序 | $O\(n\*log\(n\)\)$ | $O\(1\)$ | N | Y |
| 选择排序 | $O\(n^2\)$ | $O\(1\)$ |  | Y |
| 堆排序 | $O\(n\*log\(n\)\)$ | $O\(1\)$ |  | Y |
| 插入排序 |  | $O\(1\)$ |  | Y |
| 希尔排序 |  | $O\(1\)$ |  | Y（更适合相对有序） |
| 归并排序 | $O\(n\*log\(n\)\)$ | $O\(n\)$ |  | Y |
| 桶排序 |  |  |  | N |
| 计数排序 |  |  |  | N |
| 基数排序 |  |  |  | N |

## 基本排序算法以及改进算法

## 归并排序算法

## 特殊排序算法

### 桶排序

规模为n的数据集分割为m个有序子集，桶排序要求：

1、任意子集的数据个数接近$n/m$，即数据分布相对平均；

2、$n/m&lt;&lt;n$，即$log\(n/m\)$近似一个常数；

满足以上2个条件，排序时间复杂度$\(n/m\)_m_log\(n/m\)$近似为$O\(n\)$。

[source](https://github.com/haibazhang/lib/blob/master/src/cs/algorithm-and-data-structure/linear-list/排序.md) \| [edit-online](https://github.com/haibazhang/lib/edit/master/src/cs/algorithm-and-data-structure/linear-list/排序.md)

