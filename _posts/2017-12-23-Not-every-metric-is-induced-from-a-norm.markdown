---
layout: post
title: Not every metric is induced from a norm
tag:
 - functional-analysis
 - metric-spaces
 - norm
 - examples-counterexamples
 - normed-spaces

description: Not every metric is induced from a norm

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Not every metric is induced from a norm

<!–-break-–>


we have studied that every normed space $$(V, \lVert\cdot \lVert)$$ is a metric space with respect to distance function
$$d(u,v) = \lVert u - v \rVert$$, $$u,v \in V$$.
 
My question is whether every metric on a linear space can be induced by norm? we know answer is  no but we need proper justification.


# Answer 


Let $$V$$ be a vector space over the field $$\mathbb{F}$$. A norm


$$

\| \cdot \|: V \longrightarrow \mathbb{F}

$$


on $$V$$ satisfies the homogeneity condition


$$

\|ax\| = \|a\| \cdot \|x\|

$$


for all $$a \in \mathbb{F}$$ and $$x \in V$$. So the metric


$$

d: V \times V \longrightarrow \mathbb{F},

$$




$$

d(x,y) = \|x - y\|

$$


defined by the norm is such that


$$

d(ax,ay) = \|ax - ay\| = \|a\| \cdot \|x - y\| = \|a\| d(x,y)

$$


for all $$a \in \mathbb{F}$$ and $$x,y \in V$$. This property is not satisfied by general metrics. For example, let $$\delta$$ be the discrete metric


$$

\delta(x,y) = \begin{cases} 1, & x \neq y, \\ 0, & x = y. \end{cases}

$$


Then $$\delta$$ clearly does not satisfy the homogeneity property of the a metric induced by a norm.

To answer your edit, call a metric


$$

d: V \times V \longrightarrow \mathbb{F}

$$


homogeneous if


$$

d(ax, ay) = \|a\| d(x,y)

$$


for all $$a \in \mathbb{F}$$ and $$x,y \in V$$, and translation invariant if


$$

d(x + z, y + z) = d(x,y)

$$


for all $$x, y, z \in V$$. Then a homogeneous, translation invariant metric $$d$$ can be used to define a norm $$\| \cdot \|$$ by


$$

\|x\| = d(x,0)

$$


for all $$x \in V$$.

