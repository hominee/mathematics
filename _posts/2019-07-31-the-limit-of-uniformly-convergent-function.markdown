---
layout: post
title: the limit of uniformly convergent function
tags:
  - real analysis
  - derivatives
description: >
  the limit of uniformly convergent function
hero: https://source.unsplash.com/collection/145103/
overlay: blue
published: true
---


# Question

$$f$$ is defined in $$\mathbb{R}$$, has $$n$$-order derivative for any $$n$$,
and for each $$x$$,
$$ \mid f^{(n)}(x) - f^{(n-1)}(x) \mid < \frac{1}{n^2} $$
show that $$\lim_{n \to \infty} f^{(n)}(x) = c \exp(x)$$ with constant $$c$$.

<!–-break-–>

when I first come acorss this question, I don't have a clue, but after put it in Mathematics stackexchange, 
serveral answer came out, and inspired me some new solution.

# Answer

Let $$h(x) = \lim_{n \to \infty } f^{(n)}(x)$$, since

$$
1+\frac{1}{2^2}+...+\frac{1}{n^2}+... = \frac{\pi ^2}{6}
$$

So $$\sup_{n \to \infty} \mid h(x) - f^{(n)} \mid =0 $$
and for 

$$
f^{(n)} (x) = f^{(n)}(0) + \int _{0} ^{x} f^{(n+1)} (t) \text{d} t
$$

take the limit of each side that may yield to

$$
h(x) = h(0) + \int_{0} ^x h(t) \text{d} t
$$

again take derivative ,we have 

$$
h'(x) = h(x)
$$

that gives the answer $$c \exp (x)$$.