阿黛尔（Adele）打算发展新Smalltalk的文档功能并免除其处理过程，这就几乎摆脱了目标硬件的桎梏，起到拓展其应用范围的作用。
为了制作一个可免除的系统，只需对NoteTaker Smalltalk-78做出一些必要的改变。
也许图像上最大的改变就是将Smalltalk的自定义字体（这种字体使得Smalltalk的可读性更强，也是帕克文化的象征）改回至乏味的标准ASCII字体。
诚如彼得·多伊奇（Peter Deutsch）所言：这种改变“遭到了当时团队内部激烈的反对，却是让全球用户接受这种系统的关键因素”。
另一种改变则是让分程序更接近[Lambda表达式](http://baike.baidu.com/item/Lambda%E8%A1%A8%E8%BE%BE%E5%BC%8F?fr=aladdin)，但如同彼得·多伊奇9年后所观察到的：“回溯后发现，这种不同[实例化（instantiation）](http://baike.baidu.com/item/%E5%AE%9E%E4%BE%8B%E5%8C%96)与[辖域（scoping）](http://baike.baidu.com/item/%E8%BE%96%E5%9F%9F)上的增值也许并不是个好主意”。
至少对我——作为一个新的局外人——来说，把[元类（metaclass）](http://www.pythontab.com/html/2015/pythonhexinbiancheng_0906/961.html)（它只让实例初始化变得简单了一点——Smalltalk-76已然做到了此点，而它只是在此基础上稍作完善）介绍过来是最莫名其妙的想法。
彼得1989年做出的评论最为典型中肯：“许多用户都认为元类很令人费解，总的来说，也许它的费解大于它的价值”。
事实上，在PIE系统中，戈德斯坦（Goldstein）与博布罗（Bobrow）已经在Smalltalk中使用了一种“观察者模式语言（observer language）”，在某种程度上，这种语言遵照着我曾建议使用的面向视图的方法，而另一方面，它又与KRL【戈德斯坦】中的“视角（perspective）”类似。
一旦某人能够通过多重视角观察实例，他甚至都不需要“半元类（semi-metaclasses）”中的类-类（Class Class）与类-对象（Class Object）了。
这是由于对象角色与类中的实例角色只是来自不同的视角，而解决包含实例化的[生活史（life history）](http://baike.baidu.com/item/%E7%94%9F%E6%B4%BB%E5%8F%B2)问题也较为容易。
（同其他好主意一道）这曾是我们需要好好考虑的，但我们最后并没有采纳。
我猜Smalltalk已经进入了我在这个故事开头所提到的最后一个阶段，即人们最后把这种方法神化为了僵化的信仰结构。
