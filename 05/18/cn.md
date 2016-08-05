###Smalltalk和儿童

现在，Smalltalk发展到1976年，我已经总结了“成人”的活动（实际上只是半成人），让我回到73年，当我们和孩子准备开始实验的那个夏天。我们没有人知道如何与孩子们一起工作，但是我们知道Adele Goldberg和Steve Weyer与Pat Suppes一起在斯坦福已经做了相当多的工作，而且我们能够吸引他们加入我们。

因为我们不知道如何教孩子们（或其他人）面向对象编程，第一个实验Adele做模仿LOGO语言海龟画图形，她得到了似乎非常相似的结果。
也就是说，孩子们可以让海龟在屏幕上画画，但似乎很少有超越表面效果的事情发生。
当时我认为，由于个人电脑的计算机语言是交互式工具，这种新的编程能力的计算机语言，应该是由孩子创造的交互式工具。只是程序龟图形不是。

![turtle](https://raw.githubusercontent.com/steam-maker/EarlyHistoryOfSmalltalk/master/Images/turtle.png)
图示11.42 Adele在约旦中学滔滔不绝的讲

然后，Adele想出了一个绝妙的把Smalltalk作为一个面向对象语言的教学方法：“Joe Book.”。我相信这部分是受到了Minsky的想法的影响，你全面的教授教编程语言应该基于严谨程序的工作实例。

创建几个方框（class box），并向其发送消息，最后形成一个简单的多线程动画。让孩子们猜方框最终可能的样子，他们猜测的结果与实际显示令人惊讶的相近：

```
to box | x y size tilt
(○draw   »    (@place x y turn tilt. square size.
○undraw  »    (@ white. SELF draw. @black)
○turn    »    (SELF undraw. 'tilt <- tilt + :. SELF draw)
○grow    »    (SELF undraw. 'size <- size + :. SELF draw)
ISNEW    »    (SELF undraw. 'size <- size + :. SELF draw)
```

