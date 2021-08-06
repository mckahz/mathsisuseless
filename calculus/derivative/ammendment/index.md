---
title: "First Principles Ammendment"
nav_order: 3
parent: "Derivative"
grand_parent: "Calculus"
has_toc: false
---

# First Principles Ammendment

The full description of differentiation from first principles is given by

$$\lim_{h\to 0} \frac{f(t+h) - f(t)}{h}$$

and is read as "The limit as h approaches 0 of \[that expression\]."
This simply encapsulates the idea of infinitely small $h$.
When $f(t)=t^2$, we want to know what

$$\frac{(t+h)^2 - (t)^2}{h}$$

Gets closer and closer to 0, or in other words, is infinitely small.
We can't just plug in 0, that would get a division by 0, but we *can* simplify the expression to $2t+h$ and deduce that $2t+h$ gets closer and closer to $2t$ as h gets infinitely small.

