---
layout: post
title: Problem related to calculus and logarithms
tag:
 - calculus
 - logarithms

description: Problem related to calculus and logarithms

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

What are some methods to show $$\log$$ is not a rational function?

<!–-break-–>


It is easy to show $$\log$$ isn't a polynomial (no continuous extension to $$\mathbb{R}$$). More challenging is showing it isn't rational. 
Suppose it were a rational function. Then write, the fraction in lowest terms


$$

\log x =\frac{G(x)}{Q(x)} \Longleftrightarrow\frac{G(x)}{\log x} = Q(x)

$$


Clearly, as $$x \to 0$$, $$Q(x) \to 0$$. However, $$Q(x)$$ then has $$x$$ as factor so that 


$$

\frac{G(x)}{x\log x} = Q_2(x)

$$


It is well known that $$x \log x \to 0$$ as $$x \to 0$$, so for $$Q_2(x)$$ to have a finite limit as $$x \to 0$$, which it must since it is a polynomial, $$G(x) \to 0$$ as $$x \to 0$$ so that $$x$$ is a factor of $$G(x)$$. This contradicts the assumption that $$\frac{G}{Q}$$ was in lowest terms.
If there is something wrong with this, please comment, but my main question is 

What are some other ways to prove that $$\log x$$ isn't a rational function?

.

# Answer 


One reason is that a rational function is defined over all $$\mathbb R$$ except for a finite number of points, but $$\log$$ is not.
Let's prove that $$\log$$ is not even a rational function restricted to $$(0,+\infty)$$.
If $$\log = \dfrac GQ$$, then $$\dfrac 1x = \log' = \dfrac{G'Q-GQ'}{Q^2}$$.
This implies that $$G$$ and $$Q$$ have the same degree and therefore $$\displaystyle\lim_{x\to\infty} \dfrac{G(x)}{Q(x)}$$ is finite.
But $$\displaystyle\lim_{x\to\infty} \log(x) = \infty$$.

