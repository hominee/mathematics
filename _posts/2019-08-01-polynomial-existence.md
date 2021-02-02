---
layout: post
title: polynomial existence
tags:
  - polynomial
  
description: >
  polynomial existence
hero: https://source.unsplash.com/collection/145103/
overlay: blue
published: true
---


# Question

show that any polynomial $$p(x)$$ with integer coefficients can not satisfy 

$$
p(7) = 5,  p(15) = 9
$$

<!–-break-–>

This problem is not very hard if you write it down and subtract them.

# Answer

if $$p(x)$$ exists then 

$$
p(7) = a_n 7^n + ... + a_1 7 + a_0 = 5;
p(15) = a_n 15^n + ... + a_1 15 + a_0 = 9;
$$

subtract them we obtain

$$
p(7) = a_n (15^n - 7^n) + ... + a_1 (15 - 7) = 4;
$$

since $$ 8 \mid 15^k - 7^k $$ for $$1 \leq k \leq n$$, whereas 4 is not a multiple of 8, a contradiction.