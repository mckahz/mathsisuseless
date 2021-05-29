---
title: "First Principles"
nav_order: 4
parent: "Kinematics"
grand_parent: "Calculus"
has_toc: false
---

# Differentiation from First Principles

In the last few parts, I described speed as being clamped bewteen 2 values, and I think that helps illustrate the point better, but it isn't necessary.
The speed may not always be increasing (and probably won't be), but the same argument still holds.
The speed at a point is whatever the speed over the next \\(h\\) hours approaches, as \\(h\\) approaches 0.
The speed over the *past* \\(h\\) hours will approach the same value as \\(h\\) approaches 0, as we saw in the last example where 5.9999 was getting closer to 6,
and 6.0001 was also getting closer to 6. For this reason, we don't actually have to consider one side, since both sides will (almost) always approach the same value.

For these reasons, we say
\\[\text{Speed at 3 hours} = \text{whatever }\frac{(3+h)^2-3^2}{h}\text{ closes in on as $h$ goes to 0}\\]
Which is a bit of a mouthful, so mathematicians write
\\[\text{Speed at 3 hours} = \lim{h\to 0}\frac{(3+h)^2-3^2}{h}\\]
Meaning the "limit" of \\(((3+h)^2-3^2)/h\\) as \\(h\\) goes to 0.

It would be annoying to do this for every point in time we want to figure out velocity so, as mathematicians like to do, we generalise:
\\[\text{Speed at t hours} = \lim{h\to 0}\frac{(t+h)^2-t^2}{h}\\]
This is differentiation from first principles, and this was a long winded way to get there, but I think it's easier to accept as truth than the usual introduction.

One last note, if our function for our car's position isn't \\(t^2\\) (which it quite often isn't) and was some arbitrary function \\(f(t)\\), the same logic still applies and we get
\\[\text{Speed at time $t$} = \lim{h\to 0}\frac{f(t+h)-f(t)}{h}\\]
This is true differentiation from first principles.
