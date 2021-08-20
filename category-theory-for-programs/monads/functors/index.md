---
title: "Functor"
nav_order: 5
parent: "Monads"
grand_parent: "Haskell"
has_toc: false
---

# Functor

[comment] : # (
Though a functor doesn't really have anything to do with monads, I've kept it here for reasons which will become apparent in the next few pages. A functor is simply a function which maps one category to another. 

A category, while pretty abstract is a simple idea. It's a set of objects (which could be numbers, strings, you name it. If it's a thing in maths, it's an object!) and arrows between them (usually functions. Just some way of getting from one object to another). 

So if we say, take the category of integers, we have all the integers, where each integer has an arrow going to other integers. 1 has the `+ 2` arrow going to `3`, and also the `* 3` arrow!

We could do the same thing but for `Maybe Int`s, where there's all of these `Just x`s and a `Nothing`, each with arrows, which connect `Just 8` to `Just 3` with the `-5` arrow, and so on.

So if a function maps one category to another, it can map `3` to `Just 3`. It can map `100` to `Just 100`. Not very interesting, we don't need to define a new concept in Haskell just to do that, we allready have `Just`. Where functors get interesting, is that we can map the arrows between the categories. We can map the `+ 3` function so that it can be applied to `Maybe Int`s! This is what a functor is used for, 
)