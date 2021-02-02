---
layout: post
title: polynomial has no integer root
tags:
  - polynomial
  - integer root
  
description: >
  polynomial has no integer root
hero: https://source.unsplash.com/collection/145103/
overlay: blue
published: true
---


# Question

polynomial $$p(x)$$ with integer coefficients have 5 integer $$x_1, x_2,x_3,x_4,x_5$$ such that

$$
p(x_i) = 7
$$

show that $$p(x)$$ has no integer root.
<!–-break-–>

This problem is also not very hard if you write it down and analysis it for a while.

# Answer

Let 

$$
p(x) = 7 + (x-x_1)(x-x_2)(x-x_3)(x-x_4)(x-x_5) p'(x)
$$ 

if $$p(x)$$ has a integer root $$x_0$$ then

$$
(x_0-x_1)(x_0-x_2)(x_0-x_3)(x_0-x_4)(x_0-x_5) p'(x_0) = -7
$$

since -7 has only factor $$\pm 1, \pm 7$$, then $$p(x)$$ can not have integer root.