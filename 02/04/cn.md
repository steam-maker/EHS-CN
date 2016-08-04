## Sketchpad和Simula

经历了几番波折，1966年的秋天，“懵懂无知”的我怀着激动的心情来到犹他大学攻读硕士学位。我所说的“懵懂无知”是指，我从未听过ARPA和它的项目，也不曾知晓犹他大学的主要目标是解决3D图案中的“隐藏线（hidden lines）”问题，直到我走进戴夫·埃文的办公室想要谋得一官半职。
戴夫的桌上堆着一英尺高的棕皮文件，他抽出了其中一本递给我：“拿去读一读。”

这份文件每个新来的人人手一本，它的题目叫《Sketchpad：一个人机图像交流系统》（Sketchpad: A man-machine graphical communication system）【苏泽兰 1963】。
这个机器的功能非常引人注目，并且我所认识的计算机用户对此一无所知。
这里有三个很好领悟的想法：这是一个现代交互式计算机制图方面的发明；那些“原图（master drawing）”最终都能够变成“实物（instance drawing）”；控制与动力都由“约束（constraints）”提供，它们以图形的方式存在，**这样就能被操作者应用在塑造相互关联的零部件中去**（that could be applied to the masters to shape an inter-related parts）。
**它的数据结构令人费解——唯一稍微有些熟悉的部分就是在程序中植入了指示器，并且用一种叫[“倒排索引（reverse index）”](http://baike.baidu.com/view/676861.htm)来运行程序**（the only vaguely familiar construct was the embedding of pointers to procedures and using a process called reverse indexing to jump through them to routines），就如同220的文件系统一般【罗斯 1961】。
它拥有第一个剪切和缩放窗口——缩略图在虚拟的纸张上实际面积能达到大约1/3平方英里。

![sketchpad](sketchpad.png)
