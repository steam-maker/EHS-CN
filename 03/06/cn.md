NSL有个有趣的特性，就是它用户界面可以定制参量，并且终端用户可以使用TreeMeta编译器-编译器中的“交互语法（grammar of interaction）”来编辑界面。
这与威廉·纽曼（William Newman）早期的“Reaction Handler”定制界面有些相似，**终端用户或者开发者使用平板和触控笔、通过特定的程序，创建一种形象且有规律的表达语法**（construct through tablet and stylus an iconic regular expression grammar with action procedures at the states）（NSL允许用户根据其自由语境规则<context free rule>进行嵌入）。
这在很多方面都很引人注目，尤其是威廉的**组合（scheme）**，但在我看来，这里面还是有个大bug。
换句话说就是，**这些语法把用户局限在系统的状态（state）里，这个状态需要用户避免同时完成其他新的交互**（these grammars forced the user to be in a system state which required getting out of before any new kind of interaction could be done）。
因此，为了做另一件事情，用户必须通过等级菜单（hierarchical menus）或“屏幕（screen）”返回初始状态（master state）。
这里面似乎需要不同的状态，这些状态当中会有一个转移箭头（transition arrow）负责各个状态的切换——但在正式的语法理论中，这个概念并不有效。
也就是说，我们似乎需要一个“层次更少的（flatter）”界面——但是这个界面会更有趣、更丰富，也足够有用吗？

