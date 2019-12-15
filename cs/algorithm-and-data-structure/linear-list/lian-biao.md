# 链表

## 数据结构

内存模型：通过指针或引用前后依次串联起来的若干内存结点。

```text
从内存模型看，链表相比数组没有限制结点的数据类型，存储什么都行，灵活性很强。
但是单链表要存储后驱指针，双链表还需要存储前驱指针，存储空间要求更多。
```

## 算法

### 索引操作

不能直接访问指定元素，需要通过遍历来寻找。因此索引操作时间复杂是O\(n\)。

### 插入/删除操作

对于单链表，插入/删除下一个结点是常数级复杂度的操作，因此是O\(1\) 而删除指定结点，则需要寻找前驱结点，因此是O\(n\) 所以才引入了双链表。 严格来说，只有双链表的插入/删除操作才是O\(1\)，工程中通常都是使用双链表。

## 注意事项

## 工程应用

## 经典题目

## 参考答案

[source](https://github.com/haibazhang/lib/blob/master/src/cs/algorithm-and-data-structure/linear-list/链表.md) \| [edit-online](https://github.com/haibazhang/lib/edit/master/src/cs/algorithm-and-data-structure/linear-list/链表.md)

