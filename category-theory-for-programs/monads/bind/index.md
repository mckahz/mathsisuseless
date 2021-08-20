---
title: "Bind"
nav_order: 1
parent: "Monads"
grand_parent: "Haskell"
has_toc: false
---

# Bind

The bind function changes a function so it can accept it's output types as input types.
This is easier to understand with an example.
There are many good examples in [this wonderful article](http://blog.sigfpe.com/2006/08/you-could-have-invented-monads-and.html), but I'll be using my own to more directly address the bind function.

Imagine you had a function which took your name and returned a list of your relatives.

```hs
getRelatives :: String -> [String]
getRelatives name = ...
```

Let's say we wanted to know everyone a degree of seperation away from you, or the relatives of your relatives. We might do something like

```hs
getRelativeRelatives :: String -> [String]
getRelativeRelatives name = getRelatives (getRelatives name)
```

But this would throw a compiler error, since `getRelatives` doesn't accept lists of names, it just accepts names. In comes bind. If we bind our function (the bind function is `>>=` in Haskell), we make it accept the output type as it's input type. In this case `>>=getRelatives` accepts `[String]`s as input. `>>=` is actually an infix operator, because it makes code we write with it much nicer. For example, using bind we can write our `getRelativeRelatives` function like so

```hs
getRelativeRelatives :: String -> [String]
getRelativeRelatives name = 
    getRelatives name
    >>= getRelatives
```

Which can be read as "Take the value returned from `getRelatives name`, and input that into our bound function `>>= getRelatives`. We have now composed this function in a way that looks much more like a sequence of steps! You can further see how this imperitive looking code is beneficial with `do` notation, though I won't get into that here.

With the bind function, we can compose *all* functions which have a type of `String -> [String]`, because we bind them to functions which look like `[String] -> [String]`. This is our List Monad, because the monadic type is our output type, lists. In this case, our bind function is just an infix `concatMap`. Think about that! 

We actually also need to include an identity function for this to be a monad, but more on that later. We can generalise this to any type of function. The Maybe Monad binds functions which look like `a -> Maybe a` to functions which look like `Maybe a -> Maybe a`. The IO Monad binds functions which look like `a -> IO a` to functions which look like `IO a -> IO a`. You can see where this is going. The `m` Monad binds functions which look like `a -> m a`, into functions which look like `m a -> m a`

If you understood everything above, give it another read through and see if the sentence I started on makes more sense.

