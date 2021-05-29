---
title: "First Principles"
nav_order: 3
parent: "Kinematics"
grand_parent: "Calculus"
has_toc: false
---

# Differentiation from First Principles

What we did in the last part was essentially differentiation by first principles.
We calculated the change in position, \\(x\\), over the change in time \\(t\\).
So, if we wanted to know the speed at \\(t=3\\) hours, calculate the average speed in the last $h$ hours, with
the change in position being \\(t3^2-(3-h)^2\\) and the time it takes, \\(h\\)
\\[\frac{3^2-(3-h)^2}{h} < \text{Speed at time $t=3$} \\]
And the speed must be less than the average speed over the *next* \\(h\\) hours, with the change in position being \\((3+h)^2-3^2\\), and the same change in time being \\(h\\).
\\[\text{Speed at time $t=3$} < \frac{(3+h)^2-3^2}{h}\\]
Both equations put together gets us
\\[\frac{3^2-(3-h)^2}{h} < \text{Speed at time $t=3$} < \frac{(3+h)^2-3^2}{h}\\]
Which simplifies to
\\[\frac{3^2-3^2+2\cdot3h-h^2}{h} < \text{Speed at time $t=3$} < \frac{3^2+2\cdot3h+h^2-3^2}{h}\\]
\\[\frac{2\cdot3h-h^2}{h} < \text{Speed at time $t=3$} < \frac{2\cdot3h+h^2}{h}\\]
\\[\frac{h(2\cdot3-h)}{h} < \text{Speed at time $t=3$} < \frac{h(2\cdot3+h)}{h}\\]
\\[2\cdot3-h < \text{Speed at time $t=3$} < 2\cdot3+h\\]
\\[6-h < \text{Speed at time $t=3$} < 6+h\\]
Wouldn't you agree, that the speed 3 hours into our journey can't be anything other than 6?
If we consider the average speed over the last (and next) 0.000001 hours, we get that
\\[6-0.000001 < \text{Speed at time $t=3$} < 6+0.000001\\]
or
\\[5.999999 < \text{Speed at time $t=3$} < 6.000001\\]
And the only number for our speed which this is true for any \\(h\\), is 6.

That was a bit mouthfull, so take some time to digest that, and when you're ready, move onto the general formula

We can't meaninfully say there's a speed if the left boundary doesn't get closer to the same value the right boundary is getting closer to.
So we don't really need to consider the left value, since most functions you'll see in lower level maths they do approach the same value.
This is the idea behind differentiation from first principles, and we say it like this
\\[\text{Speed at time $t$} = \text{whatever }\frac{(t+h)^2-t^2}{h}\text{ closes in on as $h$ goes to 0}\\]
Which is a bit of a mouthful, so mathematicians write
\\[\text{Speed at time $t$} = \lim{h\to 0}\frac{(t+h)^2-t^2}{h}\\]
Meaning the "limit" of that equation as \\(h\\) goes to $0$.
But if our function for our car's position isn't \\(t^2\\) and was some arbitrary function \\(f(t)\\), the same logic still applies and we get
\\[\text{Speed at time $t$} = \lim{h\to 0}\frac{f(t+h)-f(t)}{h}\\]
