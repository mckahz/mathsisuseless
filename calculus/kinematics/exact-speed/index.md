---
title: "Exact Speed"
nav_order: 2
parent: "Kinematics"
grand_parent: "Calculus"
has_toc: false
---

# Exact Speed

Let's say we want to know the speed of our car from the last section, 3 hours into our journey. That is, at \\(t=3\\).
The key insight here, is that the speed of the car after 3 hours, must be more than the average speed thus far.
Likewise, the speed of the car after 3 hours is *less* than the average speed over the *next* 3 hours.
We know the average speed for the first 3 hours is the distance travelled (\\(9km\\)) over the time taken, 3 hours,
or \\[\frac{9km}{3h}=3km/h \\]
So the speed at \\(t=3\\) hours must be more than 3km/h.
Likewise, from \\(t=3\\) to \\(t=6\\), the speed is the distance travelled \\(6^2-3^2=36-9=27\\) over the time taken, 3 hours,
or \\[\frac{27km}{3h}=9km/h \\]
This hasn't helped us too much. We now know the speed at 3 hours must be somewhere between 3 and 9 km/h.
Here's the clever part: the speed at 3 hours must be greater than the average speed over last 3 hours, or the average speed over the last 2 hours,
or 1 hour, of half hour of quadrillianth of an hour! Let's see what numbers pop out when we do this
\\[\frac{\text{Change in position from $t=2$ to $t=3$}}{3-2} < text{Speed at $t=3$} < \frac{\text{Change in position from $t=3$ to $t=4$}}{4-3} \\]
\\[\frac{3^2 - (3-1)^2}{1} < text{Speed at $t=3$} < \frac{(3+1)^2 - 3^2}{1} \\]
\\[9-4 < text{Speed at $t=3$} < 16-9 \\]
\\[5 < text{Speed at $t=3$} < 7 \\]
Now we know the speed at $t=3$ is between 5 and 7, much more useful than before! Let's try and shrink the boundaries even more:
\\[\frac{3^2 - (3-0.01)^2}{0.01} < text{Speed at $t=3$} < \frac{(3+0.01)^2 - 3^2}{0.01} \\]
Which (just use a calculator) is
\\[5.99 < text{Speed at $t=3$} < 6.01 \\]
It's a pretty reasonable assumption at this point to say that 3 hours into our trip, the car is travelling 6km/h.