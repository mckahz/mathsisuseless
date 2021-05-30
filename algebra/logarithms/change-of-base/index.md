---
title: "Change of Base"
nav_order: 5
parent: "Logarithms"
grand_parent: "Algebra"
has_toc: false
---

# Change of Base

Say you're doing a maths question and you need a calculator to figure out some logarithm.
The question whats you to figure out $$\log_2(50)$$, which has to be somewhere between 5 and 6, since 50 is between $$2^5=32$$ and $$2^6=64$$,
but you can't determine what it is, exactly. With more advanced calculators you can just punch in $$\log_2(50) \approx 5.645856$$.
But here's the problem, your calculator only has $$\log_{10}$$! So how do we figure it out?

$$\log_2(50) = \frac{\log_{10}(50)}{\log_{10}(2)}$$

And if you plug that into your calculator, it'll work, but that's some black magic right there.
But we can just do some nice algebra to figure out why this is true

$$
\begin{aligned}
50 &= 2^{\log_2(50)} \\
50 &= \left(10^{\log_{10}(2)}\right)^{\log_2(50)} \\
50 &= 10^{\log_{10}(2)\log_2(50)} \\
10^{\log_{10}(50)} &= 10^{\log_{10}(2)\log_2(50)} \\
\implies \log_{10}(50) &= \log_{10}(2)\log_2(50) \\
\frac{\log_{10}(50)}{\log_{10}(2)} &= \log_2(50)
\end{aligned}
$$

As required. This works in general, and will yield the general change of base formula. 

$$
\begin{aligned}
a &= b^{\log_b(a)} \\
a &= \left(c^{\log_c(b)}\right)^{\log_b(a)} \\
a &= c^{\log_c(b)\log_b(a)} \\
c^{\log_c(a)} &= c^{\log_c(b)\log_b(a)} \\
\implies \log_c(a) &= \log_c(b)\log_b(a) \\
\frac{\log_c(a)}{\log_c(b)} &= \log_b(a)
\end{aligned}
$$

So there we have it, the change of base formula.

$$\log_b(a) = \frac{\log_c(a)}{\log_c(b)}$$