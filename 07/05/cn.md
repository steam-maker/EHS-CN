为了完全将对象包装起来，有两种情况必须得到有效控制——一种是需要经常计算a+b，或者a与b受约束，这都是很糟糕的。
例如，“3”和“4”在一种形式中需要由[算数逻辑单元（ALU）](http://baike.baidu.com/item/%E7%AE%97%E6%9C%AF%E9%80%BB%E8%BE%91%E5%8D%95%E5%85%83)控制。
如果运算对象与ALU不兼容，此时的操作应为：**全速使用后备逻辑（look-aside logic）（in the simplest scheme a single and gate）** 对其进行限制。
现在，在不降低机器运行速度的情况下，已对所有需要快速进行的最初级操作进行了包装。
