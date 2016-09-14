有一个小的插曲揭示了LISP的美妙之处，这发生在[艾伦·纽厄尔（Allen Newell）](http://baike.baidu.com/view/1633914.htm)访问PARC期间，那时他提出了分层思考（hierarchical thinking）的理论，我们请他证明。
为此，我们让他在[计算机协议（protocol）](http://baike.baidu.com/subview/36190/12517929.htm#viewPageContent)已经明确的情况下解决一个程序上的问题。
这个问题是：在提供了一系列项（item）的情况下，创造一个列表，里面区分所有的奇数项（odd indexed item）和偶数项（even indexed item）。
在纽厄尔的内部编程语言中，对指针的精确操控这一点和[IPL-V](http://baike.baidu.com/view/1199340.htm)相类似，并且在解决这个问题的过程中他遇到了麻烦。
而我则花了2秒：

```javascript
oddsEvens(x) = append(odds(x), evens(x))
```

我用的是兰丁（Landin）LISP语言的句法——这是解决办法的第一部分。
若干秒后我又写下了：

```javascript
where odds(x) = if null(x) ∨ null(tl(x)) then x
                   else hd(x) & odds(ttl(x))
     evens(x) = if null(x) ∨ null(tl(x)) then nil
                   else odds(tl(x))
```

这种用陈述形式表达解决办法以及把它们转化成程序的特性是这类语言迷人的地方之一。
看着一个比我聪明很多的人用他自己的办法（他的办法里有bug），花了30多分钟还未能完全解决问题，这着实令我印象深刻。
于是我再次深切地体会到：“视角（point of view）值80点的智商”。
我并没有很聪明，但是我的内部思考工具（internal thinking tool）拓展了我的能力。
这个插曲以及其它事情相互作用使得一点变得至关重要，那就是任何孩子使用的工具都必须具备极好的思维模式（thinking pattern），同时它的内置理当美丽且有内涵。
