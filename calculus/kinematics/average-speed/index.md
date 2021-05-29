---
title: "Average Speed"
nav_order: 1
parent: "Kinematics"
grand_parent: "Calculus"
has_toc: false
---

# Average Speed

If our car is travelling at a constant speed, we know how to calculate the speed. It's
\\[\frac{\text{The change in position (km)}}{\text{The change in time (h)}}\\]
hence km/h. That is, if I travel 120km in 2 hours, we get 120km/2hours = 60km/hour.
But what if we were travelling at some non constant speed? What if the position of your car \\(x\\)
was given by the time squared, \\(t^2\\)? That is, at \\(t=0\\) your car is at \\(x=0^2=0\\)km.
After 1 hour, your car has travelled \\(x=1^2=1\\)km (a very slow car, I know), then after 2 hours,
\\(x=2^2=4\\)km and so on. In general:

| \\(x\\) (km) | \\(t\\) (h) |
|:------------:|:-----------:|
|       0      |      0      |
|       1      |      1      |
|       4      |      2      |
|       9      |      3      |
|       16     |      4      |

What is the speed of the car?
That's a ridiculus question! The speed is always changing! When you start moving our car, you can see
the speedometer moving upwards! Which naturally extends to the question: What is the speed at a given moment in time?
This question turns out to be quite involved, and we'll get to it in a bit, but first let's ask an easier question:
What is the *average* speed between 2 points in time? Average just means as if it were constant, and we already know how to solve for
constant speed. Between when we started, \\(t=0\\), and let's say, \\(t=3\\), we travelled \\(9\\)km. So the average
velocity for the first 3 hours of our journey is
\\[\frac{9\text{km}}{3\text{h}}=3\text{km/h} \\]