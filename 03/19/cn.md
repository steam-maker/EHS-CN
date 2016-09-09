1969年末，我在斯坦福人工智能实验室（SAIL）时遭受了极大的打击，这份打击来源于真正理解[LISP](http://baike.baidu.com/item/LISP/22083)。
诚然，每个学生都知道`car`、`cdr`和`cons`，但犹他大学的落后之处在于没人能真正洞悉[`eval`](http://baike.baidu.com/item/eval/9327484)`和apply`的奥秘。
我简直不敢相信LISP的美丽与动人【麦卡锡 1960】。
我之所以这么说是因为LISP不仅仅有一帮盲目的追随者，更严重的是，它的逻辑基础存在不少缺陷。
我想表达的是，纯正的语言理当基于功能，但它最重要的部分——如[Lambda表达式（lambda expression）](http://baike.baidu.com/view/3048187.htm)、引用（quotes）和[条件数（cond）](http://baike.baidu.com/view/1014731.htm)——他们完全不是功能，而是一些特殊形式（special form）。
兰丁（Landin）以及其它人可以耍些聪明又有用的小花招，用lambda表达式得到quote和cond，但是美中不足，宝石里的瑕疵仍然存在。
这在实用语言（practical language）中，会好那么一点。
里面不仅仅有[EXPR](http://baike.baidu.com/view/1229144.htm)（用于对争论进行评估），还有FEXPR（没有评估的功能）。
我的另一个问题是，为什么大家要称其为[函数式语言（functional language）](http://baike.baidu.com/view/10765316.htm)？
为什么不以FEXPR为基础，在需要的时候让接受端进行评估？
对此，我永远也无法给出一个完美的答案，但在发明Smalltalk的时候，这个问题给予了我极大的帮助，因为它让我想到了这样一句话：“**做好最难且意义最深远的部分，相对简单的问题随后便可迎刃而解**（take the hardest and most profound thing you need to do, make it great, and then build every easier thing out of it）”。
这是LISP的承诺，也是lampda的诱惑——我们所需的是一个更好的“最难且意义最深远的部分”。
对象应当是所谓的这个部分。
