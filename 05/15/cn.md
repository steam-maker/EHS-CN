### Smalltalk-72系统的发展与应用
Smalltalk真正应用在机器上开始于平行路径（parallel path）的激增，他们很难执行过去那些严格的命令。
让我先大致介绍一下Smalltalk-72向Smalltalk-76转变的过程，在此之后，我花了几年时间让孩子们使用它，这也是这个项目的首要动力。
在试验版的Dynabook上Smalltalk-72解释器运行的并不那么灵活（按巴特勒的说法就是“并不那么叹为观止（pronouncement）”），但它容易改变，并且，对于即将纳入系统中的实时互动系统来说，它运行得足够快了。

在写好了用于读取键盘输入和创造文本字符串（string of text）代码后，我们（与戴安娜·玛丽（Diana Merry））第一个解决的问题就是重叠窗口。
为了让屏幕显示不同高度的字体，并且大致做到一边写字一边显示，戴安娜创造了一个早期的位域块转换系统。
第一个窗口版本是2½D的可拖拽的对象，但它运行起来有点慢，用处不大。
我们打算再等一等，直到史蒂夫·珀赛尔（Steve Purcell）在他的动画系统中成功地实现了这个功能（它更接近“2¼D”），并且一直沿用至今。
窗口可能是我们在Smalltalk中返工次数最多的类了，因为我们既没有足够的计算能力来持续观察[“世界坐标（world coordinates）”](http://baike.baidu.com/item/%E4%B8%96%E7%95%8C%E5%9D%90%E6%A0%87%E7%B3%BB)，也无法一直对其进行更新，而我之前在犹他大学的同事正着手在伊万斯（Evans）& 苏泽兰(Sutherland)的飞行模拟器项目中对其进行实验。
这个模型简洁而有力，但却很难实时实现，甚至是在 2½D中。第一个实用的Smalltalk窗口使用了GRAIL中移动、调整大小、克隆和关闭功能。
调整窗口时运用了一种简单的“无环（loopless）”控制方式，它把所有的窗口都串联在一起。

（在完成了数字、字符串等基本要素后）下一个要应用在试验版Dynebook上的就是一个面向对象的LOGO [turtle语言](http://biancheng.dnbcw.info/python/443280.html)版本，由泰德（Ted）负责。
它可以制作出任何turtle语言实例，既可以用在绘画上，也可以作为值用在图形转换（graphic transformation）上。
丹（Dan）创造了一种“turtle指挥官”类，它可以操控整个turtle军队。
很快，这些turtle图案便制作好了，这样我们就可以用窗口对其进行剪切。

约翰·肖奇（John Shoch）为Smalltalk代码创造了一种已鼠标为驱动的结构编辑器。

![turtle](turtle.png)

[拉里·特斯勒（Larry Tesler）](http://www.baike.com/wiki/%E6%8B%89%E9%87%8C%C2%B7%E7%89%B9%E6%96%AF%E5%8B%92)（后来为POLOS工作）并不喜欢NSL函数的模式性（modiness）与一般方法，他希望向之前的NLS使用者们提供一个可替代的方案，并组织进行编辑方面的用户调查（那时几乎闻所未闻）。
这促使他用Smalltalk编写miniMOUSE程序，这是帕克中心第一个[WYSIWYG](http://baike.baidu.com/item/%E6%89%80%E8%A7%81%E5%8D%B3%E6%89%80%E5%BE%97)编辑器。它（几乎）没什么模式，用起来也很有趣，不仅我们有这种感受，许多测试它的人皆是如此（我用相机运行了一下从前拍的片子，唤起了其中的愉悦与欣喜）。很快，miniMOUSE就成为了Smalltalk代码和一些demo的替代编辑器。

1974年春天，我在成人班打算实验的“小型”项目之一就是单页段落编辑器。它非常复杂，但我展示给大家的例子是完全无模式的（它即将被人们所了解），并且在接下来的这些年里，它成为了许多Smalltalk文本的基础。丹和戴安娜·玛丽（Diana Merry）完成了其大部分改进。
当然，对象也是多媒体文件，大部分你都可以免费阅览。
我们在早期就意识到，这些文件中每个部分的对象都需要掌控自身的编辑任务。
史蒂夫·韦耶（Steve Weyer）建立了一些最早的多媒体文件，在之后的许多年里，鲍勃·弗莱戈（Bob Flegal）、戴安娜·玛丽（Diana Merry）、拉里·特斯勒（Larry Tesler）、蒂姆·莫特（Tim Mott）和[Trygve Reenskaug](http://www.umlchina.com/Chat/TrygveReenskaug.htm)极大地扩展了它们。

史蒂夫·韦耶（Steve Weyer）和我设计了Findit，这是一个“通过例子来检索（retrieval by example）”的界面，它将类与其实例进行类比，形成了检索请求。
为了控制图书馆书本的流通，帕克图书馆使用了它许多年。

