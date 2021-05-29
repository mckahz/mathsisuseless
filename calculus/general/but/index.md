---
title: "But"
nav_order: 8
parent: "Kinematics"
grand_parent: "Calculus"
has_toc: false
---

# But...

The *idea* of the FTC is this equation,
\\[\text{Area under speed graph between $t_0$ and $t_N$} = x(t_N) - x(t_0)\\]
but there is a lot of adjustments to get the formula you'll see when you look this up.
I've deliberately swept this under the rug, to this end of things, because I don't think any of these differences are that important.
I will give a more general description of these ideas in the abstract section of the calculus part of my website.

## Simplifying

We can simplify the sum
\\[s(t_0)\Delta t + ... + s(t_N)\Delta t\\]
as
\\[\sum_{n=0}^N s(t_n)\Delta t\\]
Which is fancy maths notation for "add up all the terms from \\(n=0\\) to \\(n=1\\), then \\(n=2\\) all the way up to \\(n=N\\), that look like \\(s(t_n)\Delta t\\)."
But what we're interested in is the behaviour as \\(\Delta t\\) gets smaller and smaller, since we know
\\[\text{Area under speed graph} = \lim_{\Delta t \to 0} \sum s(t)\Delta t = \text{Distance travelled}\\]
So we write \\(dt\\) to mean \\(\Delta t\\), but really, really small. So
\\[\sum_{n=0}^N s(t_n)\Delta t\\]
Becomes smoother,
\\[\int_{t_0}^{t_N} s(t)dt\\]
With a smooth \\(S\\) for "sum".

## Finally!

We now have the Fundemental Theorem of Calculus!
\\[\int_{t_0}^{t_N} s(t)dt = x(t_N)-x(t_0)\\]
Though usually \\(t_0\\) and \\(t_N\\) (the terminals) are written as \\(a\\) and \\(b\\). 
Fair enough, that eliminates any sense of "partitioning" and just refers to 2 points in time, \\(a\\) and \\(b\\).
The speed \\(s(t)\\) is usually written as the derivative of our displacement function, \\(x(t)\\).
Which makes sense, because everything we just discussed can be applied to any kind of derivative, so we generalise, sure.
And *actually* our displacement is stated generally as any function of time, \\(f(t)\\).
This allows us to make sense of any abstract function. Are we done yet? Haha, no.
Our variable usually isn't time, it's generally just some \\(x\\).
So our final FTC looks like this!
\\[\int_a^b \dfrac{df}{dx}dx = f(b)-f(a)\\]
Ah, beautiful! That's the nicest way to present our equation!

## Except...

Yeah usually, for whatever reason the fundamental theorem is presented like this

\\[\int_a^b f(x) dx = F(b)-F(a)\\]
Where \\[\dfrac{dF}{dx} = f(x)\\]
and \\[\int_a^b f(x) dx\\]
is the area under the graph \\(f(x)\\)

This statement is confusing and less intuitive, so I still premote
\\[\int_a^b \dfrac{df}{dx}dx = f(b)-f(a)\\]
I think it's way better.