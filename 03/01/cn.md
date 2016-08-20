但EULER可以算得上是“几乎全新的事物”，它说明了这种技术可以用于简化Simula。
EULER的编译器是它形式定义的一部分，它能简单地将一种语言转化为与B5000类似的字节码（byte-code）。
这很引人注目，**因为这说明了艾德的小型机器能够在又长又慢的[微码（microcode）](http://baike.baidu.com/view/4883022.htm)中运行仿真的字节码**（Ed's little machine could run byte-codes emulated in the longish slow microcode that was then possible）。
但是EULER的编译器的使用却不合事宜，它被用在了一个“扩充优先（extended precedence）”的文法中，而实际上使用这种文法需要对语言句法进行让步（例如，“，”只能代表一种意思，因为这个优先级里没有[状态空间<state space>](http://baike.baidu.com/view/3821785.htm)）。
我最初采用了倒置的弗洛伊德-伊万斯解析（Floyd-Evans parser）（该解析改编自杰瑞·费尔德曼最初的编译器-编译器思想【费尔德曼 1977】），后来我又从各种严密的组合中寻求帮助，其中一些与Schorre的META II息息相关【Schorre 1963】，他最终在META II的[命名空间（name space）](http://baike.baidu.com/view/94233.htm?fromtitle=%E5%91%BD%E5%90%8D%E7%A9%BA%E9%97%B4&fromid=2887476&type=syn)里放置了翻译机（translater）。
