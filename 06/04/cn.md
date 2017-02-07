#### 继承性

这里我想说一些关于继承性的事情。
Simula-I中既没有把类当做对象看待，又没有继承性。
Simula-67把继承性的一般化纳入了ALGOL-60的结构中。
这个主意其实挺棒的，但它有些缺点：如少数在多线程的列表中出现的命名冲突（name clash）（现在没人使用这种列表了），还有一些主要问题，如扩展类型结构太过僵化，它们需要我们对类型进行限制，而继承性只有单一的路径，且适应交互发展系统与增量编译（incremental compiling）相结合、满足即时变化的需要都是困难的。
当然还有一系列的问题独立于Simula的目标之外：我们得解决人工智能领域中关于建模（modeling）与推论（inferencing）的问题。
例如并不是只要追随静态链就能够找到所有有用问题的答案。
其中的一些问题需要我们在动态绑定的部分中（如：[实例变量【instance variable】](http://baike.baidu.com/item/%E5%AE%9E%E4%BE%8B%E5%8F%98%E9%87%8F)）进行“继承”或是“推论”。
[多继承（multiple inheritance）](http://baike.baidu.com/item/%E5%A4%9A%E7%BB%A7%E6%89%BF)看上去也很重要，但在[超类（superclass）](http://baike.baidu.com/item/%E8%B6%85%E7%B1%BB)中，有一些名字相同的方法（method），要解决同它们可能相对应的冲突貌似很困难。
当然还有其他问题，我就不一一赘述了。

在另一方面，由于动态语言可以解决静态编译语言所不能解决的问题，我并不打算把继承性看成是Smalltalk-72的一大特色，因为我知道我们可以用Smalltalk中与LISP类似的灵活性（flexibility）来模拟它。
对这些AI想法最大的贡献者非[拉里·特斯勒（Larry Tesler）](http://www.baike.com/wiki/%E6%8B%89%E9%87%8C%C2%B7%E7%89%B9%E6%96%AF%E5%8B%92&prd=button_doc_entry)莫属，他在其早期[桌面出版](http://baike.baidu.com/item/%E6%A1%8C%E9%9D%A2%E5%87%BA%E7%89%88)系统（desktop publishing system）的各个版本中都大范围地使用了现在叫做“Slot inheritance”的概念。
如今，我们把这个叫做“代表团式（delegation-style）”继承方案【利伯曼 84】。
在这个时期，丹尼·博布罗（Danny Bobrow）和特里·威诺格拉德（Terry Winograd）正着手设计一种“帧型”AI语言，叫做KRL。
这种语言是面向对象的，我认为它受到了早期Smalltalk的影响。
它有一种叫做“透视（perspectives）”的多重继承，这种继承能够让某个对象在清晰明了的方法下扮演多重角色。
许多年后，有不少这些想法延伸进了[PIE](http://css3pie.com/)中，这也是戈德斯坦（Goldstein）和博布罗齐心协力将Smalltalk向网络和更高级描述的有趣延伸【戈德斯坦&博布罗 1980】。
