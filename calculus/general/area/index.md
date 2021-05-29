---
title: "What is Area?"
nav_order: 6
parent: "General"
grand_parent: "Calculus"
has_toc: false
---

# What is Area?

What *is* area? This might seem out of nowhere, given the last part talking about speed, and distance, but bare with me.

We all have an idea of what area is. It's a way to measure how *big* a surface is, right?
But what does the measurement *specifically* mean?
It's a simple bit of math which often gets overlooked. 
Area is the amount of squares we can fit on the surface.
This is reflected in how we communicate area. For example, what is the area of a rectangle with width 3km and height 4km?
It's 12km$$^2$$, of course! Because we can fit 12 squares into the rectangle, where each square represents a square km.
But let's highlight the steps we just skipped over in our heads,

$$
\begin{aligned}
\text{Area}
&= 3\text{km}\times4\text{km} \\
&= 3\times4\times\text{km}\times\text{km} \\
&= 12\times\text{km}\times\text{km} \\
&= 12\times\text{km}^2 \\
&= 12\text{km}^2
\end{aligned}
$$

A bit verbose? Perhaps, but it's actually a good argument for 2 things; implicit multiplication and the order of operations, though that's for another day.
The reason I point this out is, what if we weren't dealing with kms? What if one axis was km/hour and the other hours?
For our speed graph:
<iframe src="https://www.desmos.com/calculator/o63f3z48vr?embed" width="500" height="500" style="border: 1px solid #ccc" frameborder=0></iframe>
This is exactly what each square is! It's height is measured in km/hour and width in hours.
So what is the area of this square? It's

$$
\begin{aligned}
\frac{1\text{km}}{\text{h}}\times 1\text{h}
$= 1\times1\times\frac{\text{km}}{\text{h}}\text{h} \\
$= 1\text{km}
\end{aligned}
$$

Which suggests that the area of this graph might have something to do with the distance travelled. 
This is the breadcrumb trail of one of the most brilliant discoveries of mankind; the integral.