---
title: "Inverse Exponentiation"
nav_order: 0
parent: "Logarithms"
grand_parent: "Algebra"
has_toc: false
---

# Inverse Exponentiation

## Inverse Function Approach

If you know what an inverse function is, that makes logarithms much easier to understand.
If you don't, skip to the [next section](#naive-approach).
In a sense, we define the logarithm like as the function which has the properties

$$\log_a(a^x) = x$$

and

$$a^{\log_a(x)} = x$$

That is, logarithms are the inverse functions of exponents.

$$
\begin{aligned}
f(x) &= a^x \\
f^{-1}(x) &= \log_a(x)
\end{aligned}
$$

## Naive Approach

Imagine we have the equation $$2^x = 4096$$. It might take a while to figure out, but you might eventually realise $$x=12$$.
Now imagine if I asked you what $$2^{12}$$ was. You could compute it manually but we just figured out that $$2^{12}=4096$$, so you could quickly answer 4096 without having to think about it.

If I asked you to solve for $$x$$ in $$10^x = 10,000$$, you'd say $$x=4$$. If I asked you what $$10^x$$ was, you'd say $$10^x=10^4=10,000$$.
Notice though, we didn't need to know what $$x$$ was to do this, because our original equation told us $$10^x=10,000$$.

We can re-write the equation $$10^x = 10,000$$ to $$\log_{10}(10,000) = x$$, which mean the same thing, just with the latter focussing on the exponent, $$x$$.
Because of this, $$10^x = 10^{\log_{10}(10,000)} = 10,000$$.
And this is a general rule with logarithms.

$$a^{\log_a(b)}=b$$

Meaning "$$a$$ to the power of [the power of $$a$$ which gets us $$b$$] gets us $$b$$".
There's not much substantively being said here, it's just confusing notation.
Sadly, it's confusing notation you should get used to, because it's used a lot.

The opposite is easier to see

$$\log_a(a^x) = x$$

$$a$$ to the power of what equals $$a^x$$? Well, $$x$$, because $$a^x=a^x$$. Duh.