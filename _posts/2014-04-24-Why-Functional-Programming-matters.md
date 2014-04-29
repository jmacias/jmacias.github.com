---
layout: post
title: Implementing Why Functional Programming Matters
published: false
---

From the list of [10 Technical Papers Every Programmer Should Read (At Least Twice)][10TechPapers] by [fogus] comes [Why Functional Programming Matters][WFPM]

The paper explains how 2 aspects of funtional programming, higher order functions and lazy evaluation, can contribute greatly to modularity. They focus on this two aspects becuase they belive that the way in which one can divide up the original problem dependes directly on the ways in which one can glue solutions together.  FP provides these two new kinds of "glue", as they call it, given the programmer  new ways to modularize programs.  With the promise that with this new modularization methods, smaller, simpler and more general modules can be created. 

They show examples that I will implement in clojure and groovy.

## First Glue: Higher Order Funtions

Summing Numbers in a [imperative programming][imp-prog] way and in a [functional programming][fp] way:

<script src="https://gist.github.com/jmacias/0541db611c8e1607c7f5.js"></script>

In here we see the composition of smaller functions. The power of reduce is that can also be used to test if a list of booleans is true or wheather they are all true as the last examples in sum-mult-fp.clj


From Paper: by modularising a simple function (sum) as a combination of a "higher order function" and some simple arguments, we arrive toat a part (reduce) that can be used to write down many other functions on lists with no programming efforts.

All this can be achieved because functional lenguages allow functions which are indivisible in conventional programming lenguages to be experesed as combination of parts - a general higher order function and  some particular specialising functions.


## Second Glue: Lazy Functions

Functional Programming is just a about functions from its input to its output.

```clojure
(g (f input))
```
the program f compites its output which is used as the input to program g. Here is the trick, __The two programs f and g are run together in stric synchronization__. F is only started once g tries to read some input and only runs for long enough to delive the output g is trying to read.

This allows termination condition to be separeted from loop bodies - a powerful modularisation.

Since this methis of evaluation runs f as little as possible, it is called __["lazy evaluation"][lazy]__. 


http://debasishg.blogspot.com/2010/05/laziness-in-clojure-some-thoughts.html
http://www.braveclojure.com/core-functions-in-depth/






[10TechPapers]: http://blog.fogus.me/2011/09/08/10-technical-papers-every-programmer-should-read-at-least-twice/ 
[fogus]: https://twitter.com/fogus
[WFPM]: http://www.cse.chalmers.se/~rjmh/Papers/whyfp.html
[imp-prog]: http://en.wikipedia.org/wiki/Imperative_programming
[fp]:http://en.wikipedia.org/wiki/Functional_programming
[lazy]:http://en.wikipedia.org/wiki/Lazy_evaluation