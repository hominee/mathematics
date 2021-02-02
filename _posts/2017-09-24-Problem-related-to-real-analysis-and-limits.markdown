---
layout: post
title: Problem related to real analysis and limits
tag:
 - real-analysis
 - limits

description: Problem related to real analysis and limits

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Finding $$\lim\limits_{n \rightarrow \infty}\left(\int_0^1(f(x))^n\,\mathrm dx\right)^\frac{1}{n}$$ for continuous $$f:[0,1]\to[0,\infty)$$ [duplicate]

<!–-break-–>



My attempt:
Say $$f(x)$$ has a max. value $$M$$. Then 

$$

\left(\int_0^1(f(x))^ndx\right)^\frac{1}{n}\leq\left(\int_0^1M^ndx\right)^\frac{1}{n} =M

$$


we cannot figure out what to do next.

# Answer 


Your guess that it should be the maximum is a good guess. You have shown that the limit must be $$\leq M$$. We will now show that the limit must be greater than or equal to $$M-\epsilon$$ for any $$\epsilon$$, from which you can conclude that the limit is indeed $$M$$.
Since $$f(x)$$ is continuous, given $$\epsilon > 0$$, there exists a $$\delta$$ such that


$$

f(x) > M - \epsilon

$$

 for all $$x \in (x_0 -\delta, x_0 + \delta)$$. Hence, we have


$$

\int_0^1 f(x)^n dx > \int_{x_0 - \delta}^{x_0 + \delta} f(x)^n dx > \int_{x_0 - \delta}^{x_0 + \delta} (M - \epsilon)^n dx = (M-\epsilon)^n 2\delta

$$


Hence for any $$\epsilon > 0$$,


$$

\left(\int_0^1 f(x)^n dx\right)^{1/n} > (M-\epsilon)(2 \delta)^{1/n}

$$


Letting $$n \to \infty$$, we get what we want, i.e.,


$$

\lim_{n \to \infty}\left(\int_0^1 f(x)^n dx\right)^{1/n} \geq (M-\epsilon)

$$



