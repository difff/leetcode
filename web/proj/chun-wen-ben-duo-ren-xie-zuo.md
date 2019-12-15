# 纯文本多人协作

## 背景

在线多人协同编辑一份代码，最合理的文本协同应该是使用类似的Git，其它方案是是将文本包装成对象（富文本），然后讲文本操作的数据结构改成CRDT，还有有一个避免冲突的简单方案就是编辑锁。

## 细节

保存分为`结构`和`代码`两部分。 代码实时保存。结构被动保存，但需要保存代码保存成功后才继续保存结构。

## 编辑锁的设计

[source](https://github.com/haibazhang/lib/blob/master/src/web/proj/纯文本多人协作.md) \| [edit-online](https://github.com/haibazhang/lib/edit/master/src/web/proj/纯文本多人协作.md)

