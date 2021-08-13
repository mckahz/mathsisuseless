---
title: "First Principles Calculation"
nav_order: 2
parent: "Derivative"
grand_parent: "Calculus"
has_toc: false
---

# First Principles Calculation

We can calculate the rise over run (slope) of the following graph

{INSERT GRAPH}

like so:

We pick some point, let's say $t$, where we want to calculate the slope, and some point an infinitely small step in the future. Let's call this step $h$, for hours.
So now we're finding the rise over run between the following two points, or more precisely the line between the two points.

{INSERT PICTURE HERE}

The rise is $y_2 - y_1$, so the height of the later point, $f(t+h)$ minus the height of the earlier point, $f(t)$ to get $f(t+h)-f(t)$.
The run *by design* is $h$, or if you'd prefer $x_2-x_1 = (t+h)-t = h$.

So the rise over run of this graph is

$$ \frac{\text{RISE}}{\text{RUN}} = \frac{f(t+h) - f(t)}{h}$$

So for this graph, where the function is $t^2$, we get the slope as $2t + h$. 
I would recommend you get a pencil and paper and compute this ourself. 
So at time = 3 hours, we have the speed of our car as $2\times 3 + h = 6+h$km/h.
That $h$ is pescy though, we don't know what it's value is, we just know that it's infinitesmal. 
But if it's *infinitely* small, we can just ignore it.
For this reason, we say the speed of the car at some time $t$ for a car who's position is given by $t^2$ is $2t$. 
Since speed is the derivative / rate of change / slope of position, we can state this more mathematically as:
"The *derivative* of $t^2$ is $2t$."