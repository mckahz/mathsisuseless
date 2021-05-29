---
title: "Speed At a Moment"
nav_order: 2
parent: "Kinematics"
grand_parent: "Calculus"
has_toc: false
---

# Speed At a Moment

Let's say we want to know the speed of our car from the last section, 3 hours into our journey. That is, at $$t=3$$.
The key insight here, is that the speed of the car after 3 hours, must be more than the average speed thus far.
Likewise, the speed of the car after 3 hours is *less* than the average speed over the *next* 3 hours.
We know the average speed for the first 3 hours is the distance travelled ($$9km$$) over the time taken, 3 hours, or

$$\frac{9\text{km}}{3\text{h}}=3\text{km}/\text{h} $$

So the speed at $$t=3$$ hours must be more than 3km/h.
Likewise, from $$t=3$$ to $$t=6$$, the average speed is the distance travelled $$6^2-3^2=36-9=27$$ over the time taken, 3 hours, or 

$$\frac{27\text{km}}{3\text{h}}=9\text{km}/\text{h} $$

This hasn't helped us too much. We now know the speed at 3 hours must be somewhere between 3 and 9 km/h.
Here's the clever part: the speed at 3 hours must be greater than the average speed over last 3 hours, *or* the average speed over the last 2 hours,
*or* 1 hour, *or* half hour *or* quadrillianth of an hour! It must be more than the average speed over the last *any* amount of hours!
Let's see what numbers pop out when we do this

$$
\begin{aligning}
\frac{\text{Change in position over last 1 hour}}{1 hour} &< \text{Speed at 3 hours} < \frac{\text{Change in position over next 1 hour}}{1 hour} \\
\frac{3^2 - (3-1)^2}{1}                                   &< \text{Speed at 3 hours} < \frac{(3+1)^2 - 3^2}{1} \\
9-4                                                       &< \text{Speed at 3 hours} < 16-9 \\
5                                                         &< \text{Speed at 3 hours} < 7
\end{aligning}
&&

Now we know the speed at 3 hours is between 5 and 7, much more precise than before! Let's try and shrink the boundaries even more, by testing
the average speed over the last and next 0.01 hours:

$$\frac{3^2 - (3-0.01)^2}{0.01} < \text{Speed at 3 hours} < \frac{(3+0.01)^2 - 3^2}{0.01} $$

Which (just use a calculator) is

$$5.99 < \text{Speed at 3 hours} < 6.01 $$

It's a pretty reasonable assumption at this point, to say that 3 hours into our trip the car is travelling 6km/h.