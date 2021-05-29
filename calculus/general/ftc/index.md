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
<iframe src="https://www.desmos.com/calculator/emaxofy5cd?embed" width="500" height="500" style="border: 1px solid #ccc" frameborder=0></iframe>
The vertical axis is the position of the car, and the horizontal axis is the time we've been driving for. Imagine I update the speed more and more often.
<iframe src="https://www.desmos.com/calculator/z65cps60m1?embed" width="500" height="500" style="border: 1px solid #ccc" frameborder=0></iframe>
It makes sense that as we update the speed more and more often, the approximation of our distance travelled is more and more accurate.
And we can see the graph is getting closer and closer to a parabola!
<iframe src="https://www.desmos.com/calculator/0xu7lm0ugj?embed" width="500" height="500" style="border: 1px solid #ccc" frameborder=0></iframe>
That must represent the *true* position of the car, surely.

## Equation

Let's write the height of each point on the first graph as a formula. The first point (at the origin) has height 0.
The next has height
\\[s(t_0)\Delta t\\]
Where \\(t_0\\) is the time we started, in this case 0 but I will leave it as is. \\(\Delta t\\) is the time between updating speeds. 
This is just a different way to write \\((\text{speed at $t_0$})\times(\text{time we travel that speed for})\\)
The next step has a height
\\[s(t_0)\Delta t + s(t_1)\Delta t\\]
And so on
\\[s(t_0)\Delta t + s(t_1)\Delta t + ... + s(t_N)\Delta t\\]
Where \\(t_N\\) is the point in time we want to know the cars position.

## Area Under Graph

We can visualize this as the sum as under our speed graph, between \\(t_0\\) and \\(t_N\\)
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