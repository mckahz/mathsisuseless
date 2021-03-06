---
title: "Double Angle Theorem (CT1)"
nav_order: 1
parent: "Circle Theorems"
grand_parent: "Geometry"
has_toc: false
---

# Double Angle Theorem (CT1)

CT1, or the "Double Angle Theorem" as I'll be calling it, is the foundation for half the rest of the circle theorems. The theorem states that a shape like this:

That is, drawn on the inside of a circle where $$C$$ is the center, the blue angle is twice the red angle.

## Proof

Draw a line from the center to the smaller angle.
The 2 inner angles we'll call $$\alpha$$ and $$\beta$$.
Now we have 2 triangles, and since two side lengths of each triangle are radii of the circle, the 2 opposite angles must be the same.
I'm gonna quickly add more labels, but don't worry! We won't use them long!
This gives us that $$2\alpha + x = 180$$ and $$2\beta + y = 180$$. We can add these 2 equations together to get

$$
\begin{aligned}
(2\alpha + x) + (2\beta + y) &= 180 + 180 \\
2\alpha + 2\beta + x + y &= 360 \\
2(\alpha + \beta) + x + y &= 360 \\
2\theta + x + y &= 360
\end{aligned}
$$

We also know that $$x + y + \phi = 360$$, since that forms one full revolution. So we can determine that

$$ 2\theta + x + y = 360 = x + y + \phi $$

Remove the middle man 360 to get 

$$ 2\theta + x + y = x + y + \phi $$

Subtract $$x$$ and $$y$$ from both sides and we get $$2\theta = \phi$$, as desired.
