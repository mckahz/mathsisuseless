---
title: "Monads"
nav_order: 1
parent: "Haskell"
has_children: true
has_toc: false
---

# Monads

After having understood monads, I don't get why there's so much tiptoeing around what they are.
Ultimately, monads are a pattern we use to compose functions.
Let's take a look at the list monad.
I'm going to borrow the complex root example from ![You Could Have Invented Monads!](http://blog.sigfpe.com/2006/08/you-could-have-invented-monads-and.html "this wonderful article").
Which you should read, if you haven't already.

Imagine we have a square root function which takes complex numbers, and return an array of it's square roots.
Likewise, imagine we have a cube root function which takes complex numbers and returns an array of it's square roots.
We would ideally like to be able to make a sixth root function which is the composition of the two.
But the issue is that if we try to compose these functions like

    complex_sxrt z = complex_sqrt (complex_cbrt z)

We run into the issue that complex_cbrt returns an array, but complex_sqrt only accepts root.
We want to bind complex_sqrt into a function which *can* take arrays.
Alternatively, we're *binding* the domain type of our function to the range type.
Whichever makes more sense to you.
For this reason, let's create a bind function:

    bind f xs = concat (map f xs)

This means that the binded version of complex_sqrt given by

    bind complex_sqrt

Is able to take the results from complex_cbrt, apply complex_sqrt to each of them, then flattens the array with concat to get what we'd expect; an array of all 6 of our roots.
Ultimately, what our bind function did was make turn the type of accepted values for complex_sqrt (complex numbers) into the type of output values (list of complex numbers).
If we had a group of functions that had the same accepted and output values (domain and range), we could use this to bind them all and compose them in whichever way we wanted.

The actual bind operation in Haskell (given by >>=) is an infix operator and also requires you to feed the value from behind

    value >>= function

This allows for longs chains which look like step by step logic, kind of like the pipeline operator in F#.
It also helps to define an identity function, a function which almost does nothing, except transform a complex number into an array of just that complex number.
This way we can feed any complex number into any binded function.
Haskell calls this identity function "return".

This set of these three things, a type (in this case a list), an identity function (in this case \z -> \[z\]), and a bind function (like we defined above), is a monad.
The "monadic type" is the output type of our functions (complex_sqrt/cbrt/sxrt etc.), in this case a list. For this reason we call this the "List Monad".
We can apply the same logic anywhere we want to compose functions with different output types to input types, not just lists. 
Hence why there are multiple types of monads.