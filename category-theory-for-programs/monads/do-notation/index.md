---
title: "Do Notation"
nav_order: 4
parent: "Monads"
grand_parent: "Haskell"
has_toc: false
---

# Do Notation

Whilst I love [learnyouahaskell.com](http://learnyouahaskell.com), and it was fantastic to help in my journey to understanding of haskell, I believe they did a diservice in introducing do notation prior to Monads. You can't *really* understand what it's doing unless you understand the bind function. And by the point you've understood the bind function, you've already understood monads.

Put simply, do notation is just syntactic-sugar for a chain of bind functions. Take the following contrived example:

```hs
main :: IO ()
main = putStrLn "Hello"
```

What is `IO`? Well, it's a type that we can only really get by calling an Input Output (IO) function (like `putStrLn`). But more importantly, we can't really get rid of it either. An `IO String` will always be an `IO String`, and we can never use it as a `String`. This way, any function you declare with an `IO` type can't really be used anywhere unless we don't need to get rid of it. And the only place where we the presence of IO is irrelevant is something we call from outside the program, like main. After all it's not like we're using the value the main function returns, the program will be over by then!

This is why Haskell uses such a contrived method for input and output, because it forces input (like random generators based on time, keyboard inputs, time, anything chaotic like that) to only be used in this nieche context. So it seperates all of our pure functions from out messy input/output dependent functions.

The issue with our above example, is that it's rare that we would only want to print one word in our program. How do we print several things? We might be tempted to do something like this

```hs
main :: IO ()
main = 
    putStrLn "Hello"
    putStrLn "World" 
```

But putStrLn returns an `IO()`, so it doesn't know what to do with the value from `putStrLn "Hello"`. Let's tell Haskell to feed it into some function, and just ignore it.

```hs
main :: IO ()
main = (\_ -> putStrLn "World") putStrLn "Hello"
```

So we print "Hello" then "World", since Haskell executes `putStrLn "Hello"` before it's value (`IO ()`) is fed into the `(\_ -> putStrLn "World")` function. The issue with this code is that you'll get a compiler error! The reason for this is `(\_ -> putStrLn "World")` expects a `()`, but we're giving it the result of `putStrLn "Hello"`, which is an `IO ()`. Darn it! If only we had a way to make `(\_ -> putStrLn "World")` accept the same type of value it spits out! `IO ()` instead of `()`!

If you know what a bind is, you should be screeming by this point "use a bind!". And you'd be write, because the code would look more readable *and* work.

```hs
main :: IO ()
main = 
    putStrLn "Hello"
    >>= (\_ -> putStrLn "World") 
```

Now `>>= (\_ -> putStrLn "World")` *can* accept `IO ()` types. That's the point of the bind function after all. Having the input of our function come from the left also makes it more readable. Notice that we're feeding the result from `putStrLn "Hello"` as the (ignored) variable `_` for the function `(\_ -> putStrLn "World")`. 

This is nice and all, but wouldn't it be nice if we could link the value of `putStrLn "Hello"` into `_` more clearly? Well luckily, we have the `do` notation.

```hs
main :: IO ()
main = do
    _ <- putStrLn "Hello"
    putStrLn "World"
```

We can think of this as "Take the result of `putStrLn "Hello"`, and feed it into the bound version of `(\_ -> putStrLn "World")`. All of this logic is contained in the `do` syntax. 

If we wanted to actually use the result from `putStrLn "Hello"` in the next function, we *could* do something like

```hs
main :: IO ()
main = do
    x <- putStrLn "Hello"
    putStrLn ("World" ++ show x)
```

This is quite useful and you'll see examples everywhere. Including [learnyouahaskell.com](http://learnyouahaskell.com/input-and-output), where they give examples without the context of monads. All of the work going on behind the scenes here is a bit confusing, but it helps to understand.

As a side tangent, take the following code.

```hs
main :: IO ()
main = do
    yourName <- getLine
    putStrLn yourName
```

`getLine` returns an `IO String`, where the string is your name as typed into the console. We often view this as a shortcut way of getting rid of the `IO`, and just storing the `String` into `yourName`, which is handy but inaccurate. `yourName` is an `IO String` no matter what you do about it, but it's fed into our *binded* function which has been bount to accept `IO String`s instead of `String`s. So effectively we can treat `yourName` as a `String`. 

Anyways, returning to our example.

```hs
main :: IO ()
main = do
    _ <- putStrLn "Hello"
    putStrLn "World"
```

Since we don't need the value of `putStrLn "Hello"` (we've used an `_` after all) we can further simplify. Though the underlying structure is a bit obscured, we do get a more readable function.

```hs
main :: IO ()
main = do
    putStrLn "Hello"
    putStrLn "World"
```

The `_ <-` is still *there*, it's just implied and the compiler will put it in for you. It's worth noting that this is why we can't assign the last value into a variable like so:

```hs
main :: IO ()
main = do
    _ <- putStrLn "Hello"
    x <- putStrLn "World"
```

Because the compiler is gonna look for a binded function afterwards to use `x` in, but that doesn't exist!

After all that we've unraveled a somewhat complex string of ideas involving monads, types and bindns to get a simple, readable sequence of instructions. Compare:

```hs
>>=(\_ -> putStrLn "World") putStrLn "Hello"
```

to:

```hs
do
    putStrLn "Hello"
    putStrLn "World"
```

I don't know about you, but I think the second one is much nicer.

