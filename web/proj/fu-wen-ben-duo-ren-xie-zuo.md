# 富文本多人协作

## 背景

## CDRT

### 幂等性

实现幂等性，最关键是要有一个涵盖所有协作方的全局id。

#### 实现思路

1、组件名+毫秒级时间戳 2、组件名+时间戳+uuid

```text
关于id长度优化
id中组件名具有可读性，不做优化。而后缀优化可以优化到最长6位。
id  = {组件名}_{collaboratorID}{compCreateCount}
1、编码使用36进制，比如3位编码对应数字空间是\[0,46656-1\]
2、collaboratorID：服务端对同一项目分发的协作者ID。最长编码3位，生成规则是count=(count+1)%46656
3、compCreatCount：该组件创建的次数。最长编码3位，即假设用户最多生成同一个组件46656次
```

## Reference

[source](https://github.com/haibazhang/lib/blob/master/src/web/proj/富文本多人协作.md) \| [edit-online](https://github.com/haibazhang/lib/edit/master/src/web/proj/富文本多人协作.md)

