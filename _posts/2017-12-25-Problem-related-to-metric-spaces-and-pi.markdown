---
layout: post
title: Problem related to metric spaces and pi
tag:
 - metric-spaces
 - norm
 - examples-counterexamples
 - pi

description: Problem related to metric spaces and pi

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

A metric on $$\mathbb{R}^n$$ such that $$d(\lambda x, \lambda y)=\|\lambda\| d(x,y)$$ which is not induced by a norm

<!–-break-–>



Let $$V=\mathbb{R}^n$$.

  Let $$d:V \times V\rightarrow \mathbb{R}$$ a metric on $$\mathbb{R}^n$$.

  Assume that for any $$x,y\in V$$ and $$\lambda \in \mathbb{R}$$, we have $$d(\lambda x, \lambda y) = \|\lambda\|d(x,y)$$.

  Is $$d$$ necessarily induced by a norm?

Motivation:  we have  been thinking of $$\pi$$ and thought about why the ratio between a circles's circumference and its radius is constant.
 The proof is easy and is applicable to any norm.
 we think the "positive homogeneity" condition we posed on the metric above is enough for this ratio to be constant.


# Answer 


The answer is no. You need translational invariance as well; then it's a pretty well-known theorem (see e.g. here).
As a counterexample when leaving out the translational invariance, consider:


$$

d: \mathbb{R}^n \times \mathbb{R}^n \to \mathbb{R}_{\ge 0}: d (x,y)=\begin{cases}
 \|x\|+\|y\| & \text{if} x \ne y\\
 0 & \text{otherwise.}
\end{cases}

$$


This metric is sometimes referred to as the "metric of the French railway system", although there are similar metrics with the same name (cf. the comments).

