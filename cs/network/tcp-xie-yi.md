# tcp协议

tcp协议在网络层ip协议之上，在应用层协议之下的传输层，职责是传输。 tcp最早为军工网设计，网络丢包不稳定等问题严重，总的来说tcp协议解决的就是网络传输的不可靠。

tcp协议的任务：

* 基于端口的进程寻址
* 创建/管理/终止连接
* 处理并将字节流打包成报文段
* 传输数据
* 保持可靠性和传输质量
* 流控制和拥塞控制

  ```text
  流控制是针对发收两方，防止发送接收速度不匹配，拥塞控制是针对整个网络
  ```

## 连接

四元组定义一个连接

[source](https://github.com/haibazhang/lib/blob/master/src/cs/network/tcp协议.md) \| [edit-online](https://github.com/haibazhang/lib/edit/master/src/cs/network/tcp协议.md)

