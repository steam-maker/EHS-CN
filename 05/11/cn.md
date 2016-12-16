1972年11月22日，恰克（Chuck）开始了他“赌约”。
除了磁盘接口由艾德·麦克特（Ed McCreight）完成外，机器其余的部分都由两名技术人员负责。
它的位图显示器约有五十万像素（606x808），微码平均运行速度为6[MIPS](http://baike.baidu.com/item/MIPS/20188911#viewPageContent)，大小共计128k，整台机器（除内存外）都依托于两个160MSI芯片。
这台机器非常美丽【赛克 1972,1986】。
它突出的特点之一就是“zero-over-head”任务分配模式。
它有16个[程序计数器（program counter）](http://baike.baidu.com/item/%E7%A8%8B%E5%BA%8F%E8%AE%A1%E6%95%B0%E5%99%A8)，各负责一个任务。
[状态标志（condition flags）](http://baike.baidu.com/item/%E7%8A%B6%E6%80%81%E6%A0%87%E5%BF%97)与特殊的事件相关联（例如“水平回扫脉冲（horizonal retrace pulse）”和“磁盘扇区脉冲（disk sector pulse）”）。
在机器运行时，后备逻辑（lookaside logic）会扫描这些标志，并先选取优先级最高的程序计数器，依次类推。
整台机器在运行时无需等待，而大部分的硬件功能（尤其是涉及[i/o](http://baike.baidu.com/item/i%2Fo/84718)的，例如显示与控制磁盘）都能被微码取代。
一个任务甚至可以更新MOS动态[随机存取存储器（RAM）](http://baike.baidu.com/item/%E9%9A%8F%E6%9C%BA%E5%AD%98%E5%8F%96%E5%AD%98%E5%82%A8%E5%99%A8?fromtitle=RAM&fromid=144481&type=syn)。
换句话说就是，这是一种协同程序（coroutine）的架构。
恰克声称他的灵感来源于我几个月前关于协同程序的演讲，但在我的印象中则是韦斯·克拉克（Wes Clark）最先在TX-2（Sketchpad机器）中运用了这个想法，我可能只是在演讲中提到了它。

