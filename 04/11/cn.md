戴夫·费舍尔（Dave Fisher）在卡耐基梅隆大学发表过一篇关于控制结构集合的论文【Fisher 70】，里面提到了一种简洁明了的解决办法。
[ALGOL60 ](http://baike.baidu.com/view/1626317.htm)语言需要一种独立的链接，它既要保证动态调用子程序，又要调用[静态全局变量（static global state）](http://baike.baidu.com/view/14039160.htm)。
费舍尔在他的论文里揭示了如何将这些链接一般化，并用来模拟各式各样的控制环境。
解决LISP“函数变元问题（funarg problem）”的方法之一是将适当的全局变量链接与表达和功能相结合，之后会对这些表达和功能进行评估，因此，它所引用的[自由变量（free veriables）](http://baike.baidu.com/view/10522936.htm)实际上是由该语言的静态形式呈现的。
该论文中也提前描述了[“惰性计算（lazy evaluation）”](http://baike.baidu.com/view/2300535.htm)的概念。

