那年秋天，我听到了[巴特勒·拉姆泼逊（Butler Lampson）](http://baike.baidu.com/view/2009279.htm)一场精彩的谈话，内容是关于CAL-TSS，它是个基于用户能力的操作系统（capability-based operating system）([參考資料](discussion.md))，看上去十分具备“面向对象”的特性【拉姆泼逊 69】。
不可伪造的指针（ala B5000）由限制对象内部操作权限的位屏蔽（bit-mask）延伸。
这与我“对象即为服务者（objects as server）”的比喻不谋而合。
这个系统中异常情况处理（exception handling）的方法也很得宜，它提醒了我错误常常在模式匹配系统中解决。
这个系统唯一的问题就是——但CAL的设计者们从未把它看成是问题——只有几个对象（通常是那些占用内存大、运行慢的）。
而运行速度快、内存小的则不是对象。
我们需要改正这一点。
