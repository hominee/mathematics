---
layout: post
title: Is there a function with infinite integral on every interval
tag:
 - real-analysis
 - measure-theory
 - examples-counterexamples

description: Is there a function with infinite integral on every interval

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Is there a function with infinite integral on every interval?

<!–-break-–>


Could give some examples of nonnegative measurable function $$f:\mathbb{R}\to[0,\infty)$$, such that its integral over any bounded interval is infinite?
.

# Answer 


The easiest example we know is constructed as follows. Let $$q_{n}$$ be an enumeration of the rational numbers in $$[0,1]$$. Consider 

$$

g(x) = \sum_{n=1}^{\infty} 2^{-n} \frac{1}{|x-q_{n}|^{1/2}}.

$$


Since each function  $$\dfrac{1}{|x-q_{n}|^{1/2}}$$ is integrable on $$[0,1]$$, so is $$g(x)$$ [verify this!]. Therefore $$g(x) < \infty$$ almost everywhere, so we can simply set $$g(x) = 0$$ in the points where the sum is infinite.
On the other hand, $$f = g^{2}$$ has infinite integral over each interval in $$[0,1]$$. Indeed, if $$0 \leq a \lt b \leq 1$$ then $$(a,b)$$ contains a number $$q_{n}$$, so 

$$

\int_{a}^{b} f(x)\,dx \geq \int_{a}^{b} \frac{1}{|x-q_{n}|}\,dx = \infty.

$$

 Now in order to get the function $$f$$ defined at every point of $$\mathbb{R}$$, simply define $$f(n + x) = f(x)$$ for $$0 \leq x \lt 1$$.

