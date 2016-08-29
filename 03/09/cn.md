在Simula中，有一种协同程序控制结构（ coroutining control structure）【康韦 1963】用于悬挂和重新开始对象。
像文件夹和文档这样的永久对象，应当被当做悬挂进程（suspended process）处理，同时也应当按照与Algol类似的[静态变量（static variable）](http://baike.baidu.com/view/675642.htm)作用域进行存储。
这些文件夹和文档会显示在屏幕上，当指针指向它们时，便可被打开。
协同程序也可被当做控制结构用于循环（looping）中。
当发生器（generator）出现错误，无法提供新的价值时，我们会用一个算子来对其进行测试。
[布尔运算（Boolean）](http://baike.baidu.com/view/638530.htm)则用于连接各个发生器。
因此，一个[for为当型的循环语句（"for-type" loop）](http://baike.baidu.com/view/961969.htm)应当如下：

`while i <= 1 to 30 by 2 ^ j <= 2 to k by 3 do j<-j * i;`

其中，“... to ... by ...”这样的结构是一种协同程序对象。
后来，在加强版的Smalltalk中重新运用了不少这样的观点
