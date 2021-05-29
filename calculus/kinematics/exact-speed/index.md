---
title: "Exact Speed"
nav_order: 3
parent: "Kinematics"
grand_parent: "Calculus"
has_toc: false
---

# Exact Speed

In the last part, if we wanted to know the speed at \\(t=3\\) hours, calculate the average speed in the last \\(h\\) hours, with
the change in position being \\(3^2-(3-h)^2\\) and the time it takes, \\(h\\)
\\[\frac{3^2-(3-h)^2}{h} < \text{Speed at time 3 hours} \\]
And the speed must be less than the average speed over the *next* \\(h\\) hours, with the change in position being \\((3+h)^2-3^2\\), and the same change in time being \\(h\\).
\\[\text{Speed at time 3 hours} < \frac{(3+h)^2-3^2}{h}\\]
Both equations put together gets us
\\[\frac{3^2-(3-h)^2}{h} < \text{Speed at time 3 hours} < \frac{(3+h)^2-3^2}{h}\\]
Which simplifies to
\\[\frac{3^2-3^2+2\cdot3h-h^2}{h} < \text{Speed at time 3 hours} < \frac{3^2+2\cdot3h+h^2-3^2}{h}\\]
\\[\frac{2\cdot3h-h^2}{h} < \text{Speed at time 3 hours} < \frac{2\cdot3h+h^2}{h}\\]
\\[\frac{h(2\cdot3-h)}{h} < \text{Speed at time 3 hours} < \frac{h(2\cdot3+h)}{h}\\]
\\[2\cdot3-h < \text{Speed at time 3 hours} < 2\cdot3+h\\]
\\[6-h < \text{Speed at time 3 hours} < 6+h\\]
Wouldn't you agree, that the speed 3 hours into our journey can't be anything other than 6?
If we consider the average speed over the last (and next) 0.000001 hours, we get that
\\[6-0.000001 < \text{Speed at time 3 hours} < 6+0.000001\\]
or
\\[5.999999 < \text{Speed at time 3 hours} < 6.000001\\]
And the only number for our speed which this is true for any \\(h\\), is 6.
