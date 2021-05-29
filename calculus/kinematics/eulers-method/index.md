---
title: "Fundamental Theorem of Calculus"
nav_order: 7
parent: "Kinematics"
grand_parent: "Calculus"
has_toc: false
---

# Fundamental Theorem of Calculus

## Euler's Method

Let's revisit our question of finding distance from speed.

It would be easy to calculate the position given the speed if it was just constant along each time interval.
Let's just pretend the speed, given by \\(s=t\\), only updates every second.
<iframe src="https://www.desmos.com/calculator/prsop7qjez?embed" width="500" height="500" style="border: 1px solid #ccc" frameborder=0></iframe>
The vertical axis is the position of the car, and the horizontal axis is the time we've been driving for. Imagine I update the velocity more and more often.
<iframe src="https://www.desmos.com/calculator/z65cps60m1?embed" width="500" height="500" style="border: 1px solid #ccc" frameborder=0></iframe>
It makes sense that as we update the velocity more and more often, the approximation of our distance travelled is more and more accurate.
And we can see the graph is getting closer and closer to a parabola!
<iframe src="https://www.desmos.com/calculator/0xu7lm0ugj?embed" width="500" height="500" style="border: 1px solid #ccc" frameborder=0></iframe>
That must represent the *true* position of the car, surely.

## Equation

Let's write the height of each point on the first graph as a formula. The first point at the origin has height 0.
The next has height 
\\[s(t_0)\Delta t\\]
Where \\(t_0\\) is the time we started, in this case 0 but I will leave it as is. \\(\Delta t\\) is the time between updating velocities. 
The next step has a height
\\[s(t_0)\Delta t + s(t_1)\Delta t + s(t_2)\Delta t\\]
And so on
\\[s(t_0)\Delta t + s(t_1)\Delta t + ... + s(t_N)\Delta t\\]
Where \\(t_N\\) is the point in time we want to know the cars position.

## Area Under Graph

We can visualize this as the sum as under our speed graph, between 0 and \\(t_N\\)
<iframe src="https://www.desmos.com/calculator/mykns2ipgq?embed" width="500" height="500" style="border: 1px solid #ccc" frameborder=0></iframe>
Where the vertical axis is the speed of the car, and the horizontal axis is the time we've been driving for.
This likewise, approaches the actual area of the graph as our time step \\(\Delta t\\) gets smaller and smaller.
<iframe src="https://www.desmos.com/calculator/tp6kwgxypa?embed" width="500" height="500" style="border: 1px solid #ccc" frameborder=0></iframe>

## FTC

We have 2 arguments that, the equation given by
\\[s(t_0)\Delta t + ... + s(t_N)\Delta t\\]
Is equal to *both* the area under the speed graph *and* the distance travelled between \\(t_0\\) and \\(t_N\\).
Well, they are more equal as our timestep between updating speeds shrinks.
This is the core idea behind the Fundemental Theorem of Calculus (FTC).
\\[\text{Area under speed graph between $t_0$ and $t_N$} = \text{Sum} = \text{Distance travelled between $t_0$ and $t_N$}\\]
So we remove the middle man and get
\\[\text{Area under speed graph between $t_0$ and $t_N$} = \text{Distance travelled between $t_0$ and $t_N$}\\]
We know the distance travelled, it's the difference between the final distance, \\(x(t_N)\\) and the initial distance, \\(x(t_0)\\), thus
\\[\text{Area under speed graph between $t_0$ and $t_N$} = x(t_N) - x(t_0)\\]

## Simplify the Left Side

We can simplify the sum
\\[s(t_0)\Delta t + ... + s(t_N)\Delta t\\]
as
\\[\sum_{n=0}^N s(t_n)\Delta t\\]
Which is fancy maths notation for "add up all the terms from \\(n=0\\) to \\(n=1\\), then \\(n=2\\) all the way up to \\(n=N\\), that look like \\(s(t_n)\Delta t\\)."
But what we're interested in is the behaviour as \\(\Delta t\\) gets smaller and smaller, since we know
\\[\text{Area under speed graph} = \lim_{\Delta t \to 0} \sum_{n=0}^N s(t_0)\Delta t = \text{Distance travelled}\\]
So we write \\(dt\\) to mean \\(\Delta t\\), but really, really small. So
\\[\sum_{n=0}^N s(t_n)\Delta t\\]
Becomes smoother,
\\[\int_{t_0}^{t_N} s(t)dt\\]
With a smooth \\(S\\) for "sum".

## FTC (Revised)

This is all just technicallities to describe the formula provided if you look up the Fundemental Theorem of Calculus:
\\[\int_{t_0}^{t_N} s(t)dt = x(t_N)-x(t_0)\\]
Though usually \\(t_0\\) and \\(t_N\\) (the terminals) are written as \\(a\\) and \\(b\\). 
Fair enough, that eliminates any sense of "partitioning" and just referres to 2 points in time.
And the speed, \\(s(t)\\) is written as the derivative of our displacement function, \\(x(t)\\).
Which makes sense, because everything we just discussed can be applied to any kind of derivative, so we can generalise.
And our displacement is stated generally as \\(f(t)\\).
Except our variable usually isn't time, it's generally just some \\(x\\).
So our final FTC looks like this!
\\[\int_a^b \dfrac{df}{dx}dx = f(b)-f(a)\\]
Ah, beautiful! That's the nicest way to present our equation!

## Except...

Yeah usually, for whatever reason the fundamental theorem is presented like this
\\[\int_a^b f(x) dx = F(b)-F(a)\\]
Where \\[\dfrac{dF}{dx} = f(x)\\]
For whatever reason. This is confusing and less intuitive, so I still premote
\\[\int_a^b \dfrac{df}{dx}dx = f(b)-f(a)\\]
I think it's way better