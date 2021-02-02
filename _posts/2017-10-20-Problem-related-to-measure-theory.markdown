---
layout: post
title: Problem related to measure theory
tag:
 - measure-theory

description: Problem related to measure theory

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Can $$\int\|f_n\|d\mu \to \int \|f\|d\mu$$ but not $$\int\|f_n - f\|d\mu \to 0$$? 

<!–-break-–>



Possible Duplicate:
Convergence a.
e.
 and of norms implies that in Lebesgue space 

we are  trying to show that if


$$


\int_X \|f_n\|d\mu \to \int_X\|f\|d\mu


$$


where $$f$$ and all the $$f_n$$ have finite integral and $$f_n \to f$$ pointwise, then


$$


\int_X \|f_n-f\|d\mu \to 0.



$$


we worked out a proof in the case that $$\mu(X) < \infty$$, but it relies on Egoroff's theorem which may fail if $$\mu(X) = \infty$$.
 we can't find a counterexample in the case $$\mu(X) = \infty$$ but we suspect that it may not be true.
 we was thinking of $$X=\mathbb{R}$$ but maybe there is a good counting measure counterexample on $$\mathbb{N}$$.

Does anyone know if this is true in the case $$\mu(X) = \infty$$, and if so, how might we get started in showing it?
.


# Answer 


Let $$g_n(x):=\|f(x)\|+\|f_n(x)\|-\|f(x)-f_n(x)\|$$. It defines an integrable function, and $$g_n\to 2\|f\|$$ pointwise. Furthermore, $$g_n\geq 0$$. By Fatou lemma,


$$

\int_X\liminf_{n\to+\infty}g_n(x)d\mu(x)\leq\liminf_{n\to+\infty}\int_Xg_n(x)d\mu(x).

$$

 
The LHS is $$2\int_X\|f(x)\|d\mu(x)$$, and the RHS is $$2\int_X\|f(x)\|d\mu(x)+\liminf_{n\to +\infty}-\int_X\|f-f_n\|d\mu$$. This gives 


$$

0\leq -\limsup_{n\to +\infty}\int_X\|f-f_n\|d\mu,

$$


which is the wanted result.
In particular, this works without the assumption of finiteness of the measure (we just need a positive measure).

