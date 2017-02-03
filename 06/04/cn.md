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
