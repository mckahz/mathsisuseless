---
title: "First Principles"
nav_order: 4
parent: "Kinematics"
grand_parent: "Calculus"
has_toc: false
---

# Differentiation from First Principles

## We Don't Need To Do This Twice!

In the last few parts, I described speed as being clamped bewteen 2 values, and I think that helps illustrate the point better, but it isn't necessary.

Notice, both sides of our equation were getting closer and closer to the same value, 6.
\\[\text{some function growing to 6} < \text{speed} < \text{some other function shrinking to 6}\\]
If they were getting closer to different value, like the lower bound never grows more than 5 and the upper bound never shrinks less than 8, 
instead of them both going closer and closer to 6, we wouldn't be able to define what our speed is.
In this sense, the speed is undefined. Most of what you'll look at when beginning calculus are nice functions, where speed is defined at all points.

The upshot is that the left and right sides of our equation almost always approach the same value, so let's just ignore the left hand side and focus on the right.

The speed at a point is whatever the speed over the next \\(h\\) hours approaches, as \\(h\\) approaches 0.
The speed over the *past* \\(h\\) hours will approach the same value as \\(h\\) approaches 0, as we saw in the last example where 5.9999 was getting closer to 6,
and 6.0001 was also getting closer to 6. For this reason, we don't actually have to consider one side, since both sides will (almost) always approach the same value.

## Any Moment in Time

For these reasons, we say
\\[\text{Speed at 3 hours} = \text{whatever }\frac{(3+h)^2-3^2}{h}\text{ closes in on as $h$ goes to 0}\\]
Which is a bit of a mouthful, so mathematicians write
\\[\text{Speed at 3 hours} = \lim{h\to 0}\frac{(3+h)^2-3^2}{h}\\]
Meaning the "limit" of \\(((3+h)^2-3^2)/h\\) as \\(h\\) goes to 0.

It would be annoying to do this every time we want to figure out speed at some point so, as mathematicians like to do, we generalise by replacing 3 with \\(t\\):
\\[\text{Speed at t hours} = \lim{h\to 0}\frac{(t+h)^2-t^2}{h}\\]
This is differentiation from first principles, and this was a long winded way to get there, but I think it's easier to accept as truth than the usual introduction.
