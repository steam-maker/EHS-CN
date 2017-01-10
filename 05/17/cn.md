#### “面向对象”的模式

面向对象类型（OOP-type）和目前开始引起学术圈兴趣的[“抽象数据类型（abstract data type）”](http://baike.baidu.com/item/%E6%8A%BD%E8%B1%A1%E6%95%B0%E6%8D%AE%E7%B1%BB%E5%9E%8B)差别很大，后者从表面上看是一种[封装（encapsulation）](http://baike.baidu.com/subview/154910/12534703.htm#viewPageContent)。
我觉得我要在这里发表一些关于它们之间差别的观点。
我们先前对“LISP对（LISP pair）”的定义就是抽象数据类型的一个很好例子，因为它保留着“字段访问（ field access）”和“字段重绑（field rebinding）”两种功能，这两种功能皆是数据结构的特征。
60年代相当大一部分的工作重点都放在一般化这些结构上。
“官方”计算机科学界开始将Simula看做定义抽象数据类型的潜在工具（其中甚至有一名它的发明者【Dahl 1970】），后来它甚至成为了ADA基石的一部分。
它导致了堆栈数据类型（stack data-type）的例子如同幽灵般无处不在，数百份论文里都能看见它们的身影。
我们的态度，保守点来说就是大家对此感到很惊奇，因为在我们眼里，Simula向我们叙说的不仅仅是如何重新实现一个弱小又短暂的观点，而是一些更掷地有声的东西。
我从Simula中得出的是你可以用目标（goals）来取代[绑定（bindings）](https://msdn.microsoft.com/zh-cn/library/ms752347(v=vs.110).aspx?from=groupmessage)和[赋值（assignment）](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Operators/Assignment_Operators?from=groupmessage)。
你最不想看到程序员们做的就是将对象与内部状态（internal state）纠缠不清，即便是最终形象地呈现出来也不行。
取而代之，对象应当被视为执行更高级别行为的场所，这些行为更加适合作为动态组件（dynamic components）来使用。

我们甚至将这些关于对象的思考用在孩子们的教育上（与之前的教育方法相比）。
这种方法对编程的舒适度、所需代码的大小和设计的完整性等都有着一些启发，但并没有太过惊艳。
不幸的是，今天存在着太多被冠以“面向对象编程”的产品，它们本质上还是维持着老样子，唯一不同的只是换了一身更光鲜亮丽的外衣。
许多程序都载有“赋值类型（assignment style）”运算，它们现在都由价格更高昂的附加程序完成。

是什么让这些面向对象的设计带来了不同凡响的效率？
这个问题很值得深思，我们可以把这个根源看成是某种跟过去稍有不同的方法，它将程序应用在数据结构中。
它的一部分影响来自于其中复杂的系统通过比从前更加清晰的方式呈现。
这个方法中，约束（constrain）和普遍性（generality）同样有用。
有四种技术结合在一起消耗了大部分的能量——持续状态（persistent state）、[多态性（polymorphism）](http://baike.baidu.com/item/%E5%A4%9A%E6%80%81%E6%80%A7)、[实例化（instantion）](http://baike.baidu.com/item/%E5%AE%9E%E4%BE%8B%E5%8C%96)、对象的方法即对象的目标（methods-as-goals）。
其中，没有一种技术有采用“面向对象”语言的需要——ALGOL68可以大致转换成这种模式——这是一种面向对象的编程语言（OOPL）——它仅仅在一个特殊且卓有成效的方向上才关注设计者的思想。
当然了，包装也不是一无是处，它做出贡献的领域不仅限于状态的抽象，它还消除了编程中[面向状态](http://ishare.iask.sina.com.cn/f/18642642.html)的语句（state-oriented metaphor）。

也许我们要思考的最重要的原则——它也是从操作系统中来的——是当你给某个人一个结构时，你只想给那个人一些有限的权限。
要做到这个，光有类型匹配（type-matching）远远不够。
当然，保护一些对象而放任另一些对象也是没用的。
所有对象应当被一视同仁地重视，并全部受到保护。

我认为，要想做出一个优秀且更小的OOP系统，不能只敦促大家深思熟虑、做出一种设计。
在我眼中，OOP的**“每一行代码都必须掷地有声（bang per line of code）”**。
对象身上承载着许多意义和目的；它的[method类](http://www.apihome.cn/api/java/Method.html)告诉我们它可以实现的最大目标；与大多数基于数据的程序结构（procedures-on-data-structures）相比，它的[超类（superclass）](http://baike.baidu.com/item/%E8%B6%85%E7%B1%BB)能够激发更多代码功能（code-functionality）。
任务描述——甚至是最抽象的任务描述——表达的是低等级的目标，当需要完成某个任务时，我们需要它们中大部分的参与。
总的来说，我们不希望程序员浪费时间在状态上，不管是模拟出的状态还是其他状态。
是否具备将对象实例化的能力会对代码的大小产生相当大的影响。
关于这一切还有另一种思考方式：尽管自动内存配置延迟绑定（ late-binding of automatic storage allocations ）没有突破任何程序员无法做到的事，但有了它的呈现，代码变得更加简洁有力了。
在一些情况下，OOP是一种延迟绑定方案，与过去的方法论相比，它们结合在一起能够降低脆弱性，防止代码大小带来的崩溃（size explosion）。
换句话说就是，人类程序员不是[图灵机（Turing machine）](http://baike.baidu.com/item/%E5%9B%BE%E7%81%B5%E6%9C%BA)，他们的编程系统对图灵机的依赖越小越好。
