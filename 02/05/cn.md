兜兜转转，我终于找到了我的办公桌。
上面除了一堆磁带和清单，还有一则说明：“这是用于1108的[Algol](http://baike.baidu.com/view/459702.htm)程序，但是电脑无法运行，请解决这一问题。”
新来的研究生总的能得到最新的繁琐工作。

这份文件读起来令人费解。
据我推测，这原是[凯斯西储大学](http://baike.baidu.com/view/1123736.htm)为1107研发的Algol程序——但后来它被改成了一个新的语言，叫Simula;
整个文件读起来像从挪威语直译过来的一样，实际上就是如此。
这里面一些像“activity（活动）”和“process（过程）”这类词的用法似乎不符合正常使用英语的习惯。

最后，我和另一个研究生展开了这个份程序清单，它沿着大厅铺开，足足有80英尺长，我们就趴在上面研究，有了什么结果就向对方喊话。
最奇怪的地方在于它的储存分配程序部分（storage allocator），并没有按照Algol一贯的堆栈规则。
几天后，我们理出了些头绪。
Simula的分配结构和Sketchpad上的“实体（instances）”很像。
上面的“描述（discriptions）”有着“服务器（masters）”的功能，它们可以创造各自独立的“实体（instances）”。
在Sketchpad里面叫“服务器（masters）”和“实体（instances）”，在Simula里分别叫做“活动（activities）”和“过程（processes）”。
另外，Simula是种可以控制Sketchpad之类事物的程序性语言，因此它比起“约束（constraints）”更具灵活性（从语言的考究方面来看）。【尼高 1966；尼高 1983】

