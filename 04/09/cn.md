这个Smalltalk语言（现在叫做Smalltalk-71）受FLEX、PLANNER、LOGO、META II以及我从中衍生出的语言影响很深。
它是一种具有可以直接执行命令的对象属性的分析程序。
（我认为里面那些碍手碍脚的引用约定来自META）。
我对把程序看成是代数模式兴趣索然，但我却有个清晰的计划，关于用一种系统实现多种语言的编程。
**这个带图标的终端可以进行简单的延伸、可以检索到作为“数据”的图标、可以用简单的办法将行与对象相联系，它的eval虽然初级却表达清晰，这样我认为孩子们在有了几年的简单编程基础以后便可以理解它们。
程序的存储被分类到一个鉴别网络中，而评估则是直截了当地进行模式匹配**（The patterned front-end allowed simple extension, patterns as "data" to be retrieved, a simple way to attach behaviors to objects, and a rudimentary but clear expression of its eval in terms that I thought children could understand after a few years experience with simpler programming. Program storage was sorted into a discrimination net and evaluation was straightforward pattern-matching）

``` javascript
Smalltalk-71程序

to T 'and' :y do 'y'
to F 'and' :y do F

to 'factorial' 0 is 1
to 'factorial' :n do 'n*factorial n-1'

to 'fact' :n do 'to 'fact' n do factorial n. ^ fact n'

to :e 'is-member-of' [] do F
to :e 'is-member-of' :group
          do'if e = firstof group then T
                  else e is-member-of rest of group'

to 'cons' :x :y is self
to 'hd' ('cons' :a :b) do 'a'
to 'hd' ('cons' :a :b) '<-' :c do 'a <- c'
to 'tl' ('cons' :a :b) do 'b'
to 'tl' ('cons' :a :b) '<-' :c do 'b <- c'

to :robot 'pickup' :block
         do 'robot clear-top-of block.
         robot hand move-to block.
         robot hand lift block 50.
         to 'height-of' block do 50'
```
