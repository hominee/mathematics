---
layout: post
title: Problem related to derivatives
tag:
 - derivatives

description: Problem related to derivatives

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Showing $$f'(x) = f(x)$$ implies an exponential function 

<!–-break-–>



Possible Duplicate:
Proof that $$\exp(x)$$ is the only function for which $$f(x) = f'(x)$$ 

How can we show the statement $$f'(x) = f(x)$$ implies the function is defined as $$f: \mathbb{R} \rightarrow \mathbb{R} : x \rightarrow a\cdot \exp(x)$$ without using integrals.

My attempt at a solution:
we tried to show that the Taylor series of $$f$$ has the same structure as $$a\cdot \exp(x)$$, but we fail at showing that the error on the series converges to zero.


# Answer 


Let 


$$

G(x)=\frac{f(x)}{e^x}.

$$


Differentiate, and use $$f'(x)=f(x)$$ to conclude $$G'(x)$$ is identically $$0$$.
Then either quote the theorem that says that a function whose derivative is identically $$0$$ is constant. Or else alternately prove that theorem, by using the Mean Value Theorem. 


**Note** that more or less the same proof shows that if $$f'(x)=kf(x)$$, where $$k$$ is a constant, then $$f(x)=Ce^{kx}$$ for some constant $$C$$.

