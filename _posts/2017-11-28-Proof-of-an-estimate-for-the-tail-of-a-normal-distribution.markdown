---
layout: post
title: Proof of an estimate for the tail of a normal distribution
tag:
 - calculus
 - probability
 - faq

description: Proof of an estimate for the tail of a normal distribution

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Proof of an estimate for the tail of a normal distribution

<!–-break-–>


My advisor told me to look up the proof of the following standard estimate so that we can adapt it to the case where we are dealing with something similar but including the addition of a polynomial integrand.
  
we have yet to find a reference containing the proof and was wondering what the reference was or if someone knew a quick way to prove the following estimate:

How do you show  $$\exists c > 0$$ so that $$\int_u^\infty \exp(-z^2)\;\mathrm dz < \frac{c}{u} \exp{(-u^2)}$$?

.


# Answer 


The obvious thing to do is take the derivative with respect to $$u$$ of $$-\frac{c}{u} \exp{(-u^2)}$$ which is $$c\left(2+\frac{1}{u^2}\right) \exp{(-u^2)}$$.
So if $$u \gt 0$$ and $$c \ge \frac{1}{2}$$ then  $$c \left(2+\frac{1}{u^2}\right) \gt 1$$ and  $$c\left(2+\frac{1}{x^2}\right) \gt 1$$  for $$x \ge u$$ so 


$$

\int_{u}^{\infty} \exp{(-x^2)} dx \lt \int_{u}^{\infty} c\left(2+\frac{1}{x^2}\right) \exp{(-x^2)} dx  = \left[-\frac{c}{x} \exp{(-x^2)}\right]_{x=u}^\infty = \frac{c}{u} \exp{(-u^2)}.

$$



