一个消息发送结构的组成部分如下：

名称                | 注释
-------------------|---------------------------------------- 
GLOBAL             | **参数值环境**（the environment of the parameter values） 
SENDER             | 消息发送方
RECEIVER           | 消息接收方 
REPLY-STYLE        | 等待、分流......？
STATUS             | 发送进程
REPLY              | 最终结果 （如有）
OPERATION SELECTOR | 针对接收方
# OF PARAMETERS    | （参数编号）
P1                 | P1
...                | ......
Pn                 | Pn

这是堆栈结构的一般化，也应用于B5000。
当然，这也和CAL-TSS这样的操作系统所需的模块间的良好互动类似——每一次执行都有许多不同的方法来表达，但思考这些会带来些许帮助。

