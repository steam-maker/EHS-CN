###Smalltalk和儿童

现在，Smalltalk发展到1976年，我已经总结了“成人”的活动(实际上只是半成人)，让我回到73年，当我们和孩子准备开始实验的那个夏天。我们没有人知道如何与孩子们一起工作，但是我们知道Adele Goldberg和Steve Weyer与Pat Suppes一起在斯坦福已经做了相当多的工作，而且我们能够吸引他们加入我们。

因为我们不知道如何教孩子们（或其他人）面向对象编程，第一个实验Adele做模仿LOGO语言海龟画图形，她得到了似乎非常相似的结果。
也就是说，孩子们可以让海龟在屏幕上画画，但似乎很少有超越表面效果的事情发生。
当时我认为，由于个人电脑的计算机语言是交互式工具，这种新的编程能力的计算机语言，应该是由孩子创造的交互式工具。只是程序龟图形不是。

![turtle](https://raw.githubusercontent.com/steam-maker/EarlyHistoryOfSmalltalk/master/Images/turtle.png)
图示11.42 Adele在约旦中学滔滔不绝的讲

然后，Adele想出了一个绝妙的把Smalltalk作为一个面向对象语言的教学方法：“Joe Book.”。我相信这部分是受到了Minsky的想法的影响，你全面的教授教编程语言应该基于严谨程序的工作实例。

创建几个模板(class box)的实例，并向其发送消息，最后形成一个简单的多线程动画。让孩子们猜方框最终可能的样子，他们猜测的结果与实际显示令人惊讶的相近：

```
to box | x y size tilt
(○draw   »    (@place x y turn tilt. square size.
○undraw  »    (@ white. SELF draw. @black)
○turn    »    (SELF undraw. 'tilt <- tilt + :. SELF draw)
○grow    »    (SELF undraw. 'size <- size + :. SELF draw)
ISNEW    »    (SELF undraw. 'size <- size + :. SELF draw)
```
  
多么美妙的方法，无数的儿童项目能够从简陋的模板(box)中喷薄而出。而且伴生出最早的一些工具，这时我们真的异常兴奋。例如，Marion Goldeen(12岁)的绘画系统就是一套完整的工具。几年后，Susan Hamet(12岁)的面向对象系统(带有MacDraw一样的设计功能)也一样。还有另外2个，Bruce Horn's (15岁)乐谱捕捉系统和Steve Putz(15岁)的电路设计系统。现在回想起来，这些可以称为“早期成功综合症”(early success syndrome)在计算机科学领域的另一个例子。成功是真实的，但他们并不像我们想象的那样普遍。他们不会像我们所希望的那样强烈地延伸到未来。从 帕洛阿尔托的学校选择的孩子们(几乎平均背景)，我们取得更加兴奋的成功越发的困难。在某种程度上，我们看到的是“黑客现象”，对于任何给定的工作，总有特定的5%的人天生沉浸其中，而80%左右的人，虽然最终会掌握，但是根本找不出一点天赋。
