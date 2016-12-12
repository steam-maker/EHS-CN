1. Everything is an object
2. Objects communicate by sending and receiving messages (in terms of objects)
3. Objects have their own memory (in terms of objects)
4. Every object is an instance of a class (which must be an object)
5. The class holds the shared behavior for its instances (in the form of objects in a program list)
6. To eval a program list, control is passed to the first object and the remainder is treated as its message

By this time most of Smalltalk's schemes had been sorted out into six main ideas that were in accord with the initial premises in designing the interpreter. The first three principles are what objects "are about"—how they are seen and used from "the outside." These did not require any modification over the years. The last three—objects from the inside—were tinkered with in every version of Smalltalk (and in subsequent OOP designs). In this scheme (1 & 4) imply that classes are objects and that they must be instances of themself. (6) implies a LISPlike universal syntax, but with the receiving object as the first item followed by the message. Thus c<sub>i</sub> <- de (with subscripting rendered as "°" and multiplication as "*") means:

```
receiver | message
c        | ° i <- d*e
```

The c is bound to the receiving object, and all of ° i <- d*e is the message to it. The message is made up of literal token "°", an expression to be evaluated in the sender's context (in this case i), another literal token <-, followed by an expression to be evaluated in the sender's context (d*e). Since "LISP" pairs are made from 2 element objects they can be indexed more simply: c hd, c tl, and c hd <- foo, etc.

"Simple" expressions like a+b and 3+4 seemed more troublesome at first. Did it really make sense to think of them as:

```
receiver | message
a        | + b
3        | + 4
```

It seemed silly if only integers were considered, but there are many other metaphoric readings of "+", such as:

![add](https://raw.githubusercontent.com/steam-maker/EarlyHistoryOfSmalltalk/master/Images/add.png)

This led to a style of finding generic behaviors for message symbols. "Polymorphism" is the official term (I believe derived from Strachey), but it is not really apt as its original meaning applied only to functions that could take more than one type of argument. An example class of objects in Smalltalk-72, such as a model of CONS pairs, would look like:

![conspairs](https://raw.githubusercontent.com/steam-maker/EarlyHistoryOfSmalltalk/master/Images/conspairs.png)

Since control is passed to the class before any of the rest of the message is considered—the class can decide not to receive at its discretion—complete protection is retained. Smalltalk-72 objects are "shiny" and impervious to attack. Part of the environment is the binding of the SENDER in the "messenger object" (a generalized activation record) which allows the receiver to determine differential privileges (see Appendix II for more details). This looked ahead to the eventual use of Smalltalk as a network OS (See [Goldstein & Bobrow 1980]), and I don't recall it being used very much in Smalltalk-72.

One of the styles retained from Smalltalk-71 was the comingling of function and class ideas. In other works, Smalltalk-72 classes looked like and could be used as functions, but it was easy to produce an instance (a kind of closure) by using the object ISNEW. Thus factorial could be written "extensionally" as:

```
to fact n (^if :n=0 then 1 else n*fact n-1)
```

or "intensionally," as part of class integer:

```
(... ○! » (^:n=1) » (1) (n-1)!)
```

Of course, the whole idea of Smalltalk (and OOP in general) is to define everything intensionally. And this was the direction of movement as we learned how to program in the new style. I never liked this syntax (too many parentheses and nestings) and wanted something flatter and more grammar-like as in Smalltalk-71. To the right is an example syntax from the notes of a talk I gave around then. We will see something more like this a few years later in Dan's design for Smalltalk-76. I think something similar happened with LISP—that the "reality" of the straightforward and practical syntax you could program in prevailed against the flights of fancy that never quite got built.

```
Proposed Smalltalk-72 Syntax

Pair :h :t
    hd <- :h
	hd              » h
	tl <- :t
	tl              » t
	isPair          » true
	print           » '( print. SELF mprint.
	mprint          » h print. if t isNil then ') print
                               else if t isPair then t mprint
                               else '* print. t print. ') print
	length          » 1 + if t isList then t length else 0
```

