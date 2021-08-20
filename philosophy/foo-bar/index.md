---
title: "Foo Bar"
nav_order: 1
parent: "Philosophy"
has_children: false
has_toc: true
---

# Foo Bar

One of the biggest troubles I have with teaching is that I can feel my skin itch when watching someone else do it. I think "you're overloading them with information!" or "this isn't as obvious as you think it is!" or "engage with them a little bit more!"

But there is nothing more asinine than teaching people directly with abstract ideas. This isn't just a poor way to teach, you literally *can't* teach this way. If I tried to describe a function to you without some motivating examples like the `sqrt` or `abs` functions, then I wouldn't be doing my job. You won't be able to learn complex numbers until you solve a quadratic with complex roots, you won't know what a derivative is until you calculate the velocity of a non-linear trajectory, you won't know anything until you've dealt with the cases these things were grounded in.

Its even more insulting when you consider these ideas were introduced to make natural ideas easier to communicate. Why is it that one of the most infamous difficult subjects is literally a universal language designed to simplify ideas. Ideas which, might I add, aren't particularly complicated in the first place. After all, someone had to come up with them and have them stick.

This is particularly insidious when you're trying to teach yourself something. If you look up the definition for a monoid on Wikipedia, you'll get a set of complex diagrams which 1. I do not understand, for 2. an idea I *do* understand. So surely stack overflow would have better answers.

No. Of course not, hence the title. If you're going to write code, you want to name the variables, you name them in a way which makes the code more readable, and easier to understand. If you want to describe some code to someone, and I cannot stress this enough- make your damn code readable. `Foo` and `Bar` mean nothing, just because you're abstracting the details away doesn't mean you can't give it a name which describes it's purpose.

Now, chances are if you're reading this you know what a function is. But pretend like you didn't and see which of these 2 descriptions teaches you better:

## Description 1
A function is a chunk of code we can reuse.
```py
def some_function():
    print("Hello")
    print("World")
```
This defines (`def`) the function (`some_function`). Now, anywhere I run the code
```py
some_func()
```
It will go to the definition of `some_func()` and run what's inside. In this case
```
Hello
World
```
We can also input values to the function like so:
```py
def some_function(name):
    print("Hello")
    print(name)
```
This function now has an input, just like `sqrt`. So when I invoke
```py
some_function("mckahz")
```
It will treat `name` like `mckahz` in the function.
```
Hello
mckahz
```

## Description 2
A function is a chunk of code we can reuse.
```py
def foo():
    print("Hello")
    print("World")
```
This defines (`def`) the function (`foo`). Now, anywhere I run the code
```py
foo()
```
It will go to the definition of `foo()` and run what's inside. In this case
```
Hello
World
```
We can also input values to the function like so:
```py
def foo(bar):
    print("Hello")
    print(bar)
```
This function now has an input. So when I invoke
```py
foo("mckahz")
```
It will treat `bar` like `mckahz` in the function.
```
Hello
mckahz
```

## Conclusion
If you thought the second example was easier to understand then do the world a favour and never teach anyone ever again. In the first example we got variable names which supported the idea surrounding them- an incredibly helpful stepping stone for people learning stuff. It's so much harder to learn if I have to constantly remind myself of the unimportant details to understand the important ones. There's no moments where I think "Was foo the function or the variable?" or "How was this used?". No, I just know this stuff because it's obvious given the naming sceme. Obviously name is the thing we print after "Hello". We know this because greetings are familiar to people. In no world do `Foo` and `Bar` have any meaning whatsoever. Moreover, in the second example I didn't refer to the `sqrt` function. Now they aren't aware of how functions work from the other end, and have to learn it from scratch. Whereas before, it immediately makes the connection which teaches you implicitely how to call functions.

So if you use `Foo` or `Bar` in an explaination of some concept, or you teach things abstractly before you teach some concrete cases, I don't think you appreciate how difficult it was for you to learn the things which you know. Of course it seems obvious to you: you understand it, but they don't. So teach them as if they were as smart as you *were*, not as smart as you *are*.