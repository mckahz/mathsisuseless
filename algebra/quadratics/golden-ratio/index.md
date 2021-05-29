---
title: "Golden Ratio"
nav_order: 1
parent: "Quadratics"
grand_parent: "Algebra"
has_toc: false
---

# Golden Ratio

People see things multiplicatively, like pitch for instance. When one pitch is 2 times another, we hear them as harmonious.
That is, their ratio is 2.

It would be nice if there was some ratio which could be found within itself. 
Some fractal like - self similarity we could see in an object.
Surely our multiplicative thinking minds would appreciate such a thing!
Let's try and find such a ratio.

Suppose we have a string with two parts. If the ratio of the whole string to the biggest part was the same as the ratio of the biggest part to the smallest,
that would yield the nice self similarty we're looking for.
Suppose the lengths of each part of the string were $A$ and $B$, with $A > B$.
The two afformentioned ratios are as followed-
1. The ratio of the whole string to the biggest part is the ratio of $A + B$ and $A$, so $\frac{A+B}{A}$
2. The ratio of the biggest part to the smallest is $\frac{A}{B}$

So if those two were equal we get
$$\frac{A+B}{A} = \frac{A}{B}$$
Let's call this ratio $\phi$ (a greek letter spelled "phi", pronounced "fai"), so
$$\phi = \frac{A}{B}$$
We can then solve for $\phi$

$$
\begin{aligned}
\frac{A+B}{A} &= \frac{A}{B} \\\\
\frac{A}{A} + \frac{B}{A} &= \frac{A}{B} \\\\
1 + \frac{1}{\phi} &= \phi \\\\
1\times\phi + \frac{1}{\phi}\times\phi &= \phi\times\phi \\\\
\phi + 1 &= \phi^2 \\\\
\phi^2 - \phi - 1 &= 0
\end{aligned}    
$$

Ah, this is why this is in the quadratics part of the website.
We can use the quadratic formula $a=1, b=-1, c=-1$
$$\phi = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a} = \frac{1 \pm \sqrt{1 - 4(1)(-1)}}{2(1)} = \frac{1 \pm \sqrt{5}}{2}$$
But our lengths are positive, so the ratio must be aswell, allowing us to ignore the negative solution.

Therefore
$$\phi = \frac{1 + \sqrt{5}}{2}$$