---
layout: post
title: Problem related to sequences and series and zeta functions
tag:
 - sequences-and-series
 - zeta-functions

description: Problem related to sequences and series and zeta functions

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Is $$\sum_{n=1}^{\infty }\frac{8n\cdot\zeta (2n)}{3\cdot 2^{2n}}=\zeta (2)$$?

<!–-break-–>



# Answer 


Since:


$$

 \frac{1-\pi x\cot(\pi x)}{2}=\sum_{n\geq 1}\zeta(2n)\,x^{2n} \tag{1}

$$


we have, by differentiation:


$$

 \sum_{n\geq 1}2n\zeta(2n) x^{2n-1} = \frac{\pi}{4\sin^2(\pi x)}\left(2\pi x-\sin(2\pi x)\right) \tag{2}

$$


and by evaluating both sides at $$x=\frac{1}{2}$$ the claim follows.

