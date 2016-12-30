#### Smalltalk-72的演变
Smalltalk-74是Smalltalk-72的改良版（有时我们叫它FastTalk），与Smalltalk-72的不同之处在于它拥有真正的“消息发送器（messenger）”对象、关于类的消息字典（message dictionaries）（这使得我们离真正的类对象又进了一步）、戴安娜·玛丽的[bitblt](http://baike.baidu.com/item/BitBlt)（它现在是著名的2D位图图像[算子（operator）](http://baike.baidu.com/item/%E7%AE%97%E5%AD%90)）——后来由丹（Dan）重新设计并用微码操作，和一个更强大也更常规的窗口界面。
戴夫·罗宾森（Dave Robinson）那时还是[加州大学欧文分校](http://baike.baidu.com/item/UCI)的学生，他听说了我们的项目，并在使用面向对象的编程语言（OOPL）方面给予了我们极大的帮助。
我们热情地邀请他来“过暑假”，然后就一直把他“扣留着”——他在表达Smalltalk的语义上面功不可没。

其中最瞩目的当属加入了OOZE（面向对象的分区环境）[虚拟储存系统](http://baike.baidu.com/item/%E8%99%9A%E6%8B%9F%E5%AD%98%E5%82%A8%E7%B3%BB%E7%BB%9F)，与在Smalltalk-74上的应用相比，它在Smalltalk-76上的应用更为重要【英格尔斯，1978 凯勒，1981】。
ALTO内存并不大（128-256K），尤其是还要算上页面大小的显示（64k）和一些小程序，内存很快就不够用了。
与软盘相比，其中2.4兆字节的30号[磁盘驱动（disk drive）](http://baike.baidu.com/item/%E7%A3%81%E7%9B%98%E9%A9%B1%E5%8A%A8%E5%99%A8)速度更快也更大，而和今天的硬盘驱动（hard drive）相比则更慢也更小。
它和FLEX机器上的HP直接接触磁盘（direct contact disk）非常相似，关于后者，我曾在B5000的段交换进程（segment swapper）中试着安装了一个细粒（fine-grain）版。
但除了带来一些关于如何在清除时选择对象的好想法外，它没能达到我的预期。
于是，当大家提出想要使用它时，我反对道：“我还没能让它真正发光发热。”
我记得泰德·凯勒（Ted Kaehler）这样回答我：“别担心，我们会搞定的。”
