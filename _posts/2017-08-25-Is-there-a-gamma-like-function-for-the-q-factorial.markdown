---
layout: post
title: Is there a gamma-like function for the q-factorial
tag:
 - calculus
 - special-functions
 - gamma-function
 - q-analogs
 - quantum-calculus

description: Is there a gamma-like function for the q-factorial

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

is there a gamma-like function for the q-factorial?

<!–-break-–>


we are  looking at quantum calculus and just trying to understand what is going with this subject. Looking at the q-factorial made me wonder if this function could take all real or even complex numbers in the same way that $$\Gamma (z)$$ works as an extension of $$f(n) =n!$$. Since, we  need practice with both $$\Gamma $$ and q-analogs, would it be a good project to try to recreate $$\Gamma (z)$$ in this new setting or is the whole project lacking in sanity, mathematical soundness?
Also, a minor question, why is there sometimes a coefficient in q-analog expansions as in this expression:
$$(a;q)_n = \prod_{k=0}^{n-1} (1-aq^k)=(1-a)(1-aq)(1-aq^2)\cdots(1-aq^{n-1}).$$
we are  a bit embarrassed not to know, but non of the lit. we  have explains it, we 'll just randomly see it tossed in there from time to time... and it really throws me off.

# Answer 


First of all, let me start by recommending an excellent book by Victor Kac, "Quantum calculus".
q-Gamma function $$\Gamma_q$$ generalized Euler $$\Gamma$$ function by replacing the recurrence identity with it's q-deformation:

 $$ 

   \Gamma(x+1) = x \Gamma(x)  \quad \Longrightarrow \quad \Gamma_q(x+1) = [x]_q \Gamma_q(x)

 $$ 

where $$[x]_q = \frac{1-q^x}{1-q}$$ is a q-number. 
When $$x$$ is a positive integer, and assuming $$\Gamma_q(1) = 1$$, we get 

 $$ 
\Gamma_q (n+1) = \prod_{k=1}^n \frac{1-q^k}{1-q} = \frac{(q,q)_n}{(1-q)^n} = 
\begin{array} 
\frac{(q,q)_\infty}{(1-q)^n (q,q^n)_\infty} & |q|<1 \\
\frac{ q^{n(n-1)/2} (q^{-1},q^{-1})_\infty}{(1-q^{-1})^n (q^{-1},q^{-n})_\infty} & |q|>1
\end{array}  

 $$ 

The last expression is now defined for $$n \in \mathbb{C}$$, as long as $$n$$ is not a non-positive integer, as $$(q,q^{-k})_\infty = 0$$ for $$k \in \mathbb{Z}^+$$.

