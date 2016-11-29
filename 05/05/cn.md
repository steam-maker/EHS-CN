第一种版本有些瑕疵，受到了小组成员的诟病。
但在早上8点多钟的时候，我们做出了一个似乎可用的版本（解释器的设计梗概见附录III）。
第一个版本与官方Smalltalk-72最大的不同在于这些符号都由[字节码（byte-code）](http://baike.baidu.com/item/%E5%AD%97%E8%8A%82%E7%A0%81)构成，而从发送方接收[返回值（return-value）](http://baike.baidu.com/item/%E8%BF%94%E5%9B%9E%E5%80%BC)这一过程是对称的——例如接收可像[参数绑定（parameter binding）](http://document.thinkphp.cn/manual_3_2.html#param_bind)那样——这对多个值的返回尤其有用。
为了追求一个更倾向以表达为导向的函数返回形式，我们放弃了它。

