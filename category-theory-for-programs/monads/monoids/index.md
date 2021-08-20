---
title: "Monoids"
nav_order: 2
parent: "Haskell"
has_children: false
has_toc: true
---

# Monoids

Monoids, like monads, are a scary word representing something simple. Before I state what a monoid is, let's take a look at some examples.

## + and Int

If you take the type `Int` and `+`, we can notice a few things about them. Firstly, when we apply `+` to two `Int`s, we get an `Int`. In Haskell notation; `(+) :: Int -> Int -> Int`. It also has a number unlike any other, 0. 0 has the property that `x + 0 = x`, or `0 + x = 0`. Neat. Also, `x+(y+z) = (x+y)+z`. It doesn't matter which pair I do first.

## * and Int

Multiplication does a similar things to numbers. It takes two `Int`s and returns an `Int`. We also have the number 1 with the property that `1 * x = x`, and `x * 1 = x`.
And from volumes in geometry, we can deduce that `x * (y * z) = (x * y) * z`.

## power and One

Let's derive a function which raises a number `x` to some power `n`. 

```hs
power :: One -> One -> One
power _ 0 = 1
power x 1 = x
power x n = x * power
```

We can take two numbers from out type. Wait, what is our type? Just 1? Okay. We can take two 1s, and apply them to eachother with this function. And 1 has the property such that for any value in our type, in this case just 1, we can do `power x 1 = x`, and `power 1 x = x`. Though that second one is only garunteed because x has to be 1. Because of our weird type signature, we also know that `power (power x y) z = power x (power y z)`.

## What does it all mean?

All of the headings above are examples of monoids. We say addition is a monoid over `Int`s (or the integers), or that multiplication is a monoid over `Int`s, or that `power` is a monoid over `One`. This is because they share the following properties:
- We have a type and an operation (`Int` and `+`, `Int` and `*`, `One` and `power`)
- That operation takes 2 arguments (All these operations are *bi*nary)
- The operation also returns something of our type (`+` and `*` return `Int` and `power` returns `One`)
- We can apply the operation to either pair first and it doesn't change the result. (x + (y+z) = (x + y) + z)
- They all have an element which, when applied alongside the operation, doesn't do anything. (`+ 0`, `* 1`, `power 1`).

These properties have a mathematical name to them, though they aren't important to remember. What I said above in mathematical jargon:
- A monoid is a set (type) and operation (function) such that
- the operation is closed under addition
- the operation is binary (takes 2 elements of our type)
- the function is associative (operation application order doesn't matter)
- there is an identity (the thing which applying our function with doesn't do anything).

## Monads

I don't believe all of this to be important, it's just here so you can smuggly say "a monad is just a monoid in the category of endofunctors" and know what it means.
