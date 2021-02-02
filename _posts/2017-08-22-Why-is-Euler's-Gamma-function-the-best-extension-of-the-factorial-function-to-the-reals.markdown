---
layout: post
title: Why is Euler's Gamma function the “best” extension of the factorial function to the reals
tag:
 - real-analysis
 - education
 - gamma-function
 - special-functions

description: Why is Euler's Gamma function the “best” extension of the factorial function to the reals

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Why is Euler's Gamma function the “best” extension of the factorial function to the reals?

<!–-break-–>


There are lots (an infinitude) of smooth functions that coincide with f(n)=n! on the integers. we s there a simple reason why Euler's Gamma function $$\Gamma (z) = \int_0^\infty t^{z-1} e^{-t} dt$$ is the "best"?  we n particular, we are  looking for reasons that we  can explain to first-year calculus students.

# Answer 


The Bohr–Mollerup theorem shows that the gamma function is the only function that satisfies the properties 

$$f(1)=1$$;
$$f(x+1)=xf(x)$$ for every $$x\geq 0$$;
$$\log f$$ is a convex function. 

The condition of log-convexity is particularly important when one wants to prove various inequalities for the gamma function. 

By the way, the gamma function is not the only meromorphic function satisfying

 $$ 
f(z+1)=z f(z),\qquad f(1)=1,
 $$ 

with no zeroes and no poles other than the points $$z=-n$$, $$n=0,1,2\dots$$. There is a whole family of such functions, which, in general, have the form

 $$ 
f(z)=\exp{(-g(z))}\frac{1}{z\prod\limits_{m=1}^{\infty} \left(1+\frac{z}{m}\right)e^{-z/m}},
 $$ 

where $$g(z)$$ is an entire function such that

 $$ 
g(z+1)-g(z)=\gamma+2k\pi i,\quad k\in\mathbb Z, 
 $$ 

($$\gamma$$ is Euler's constant). The gamma function corresponds to the simplest choice
$$g(z)=\gamma z$$.
Edit: corrected index in the product.

