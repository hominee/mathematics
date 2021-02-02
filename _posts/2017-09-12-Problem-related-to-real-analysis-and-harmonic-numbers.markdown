---
layout: post
title: Problem related to real analysis and harmonic numbers
tag:
 - real-analysis
 - sequences-and-series
 - complex-analysis
 - closed-form
 - harmonic-numbers

description: Problem related to real analysis and harmonic numbers

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Infinite Series $$\sum\limits_{n=1}^\infty\frac{(H_n)^2}{n^3}$$

<!–-break-–>


How to prove that


$$

\sum_{n=1}^{\infty}\frac{(H_n)^2}{n^3}=\frac{7}{2}\zeta(5)-\zeta(2)\zeta(3)

$$


$$H_n$$ denotes the harmonic numbers.

# Answer 


One systematic way of proving identities like this is to write everything in terms of multiple harmonic sums and multiple zeta values . For integers $$s_1,\ldots,s_k,n\geq 1$$, we define the multiple harmonic sum (or MHS)


$$


H_n(s_1,\ldots,s_k):=\sum_{n\geq n_1>\ldots>n_k\geq 1}\frac{1}{n_1^{s_1}\ldots n_k^{s_k}}\in\mathbb{Q}.


$$


The MHS $$H_n(1)$$ is what you call $$H_n$$.
We also define the multiple zeta value (or MZV)


$$


\zeta(s_1,\ldots,s_k):=\sum_{n_1>\ldots>n_k\geq 1}\frac{1}{n_1^{s_1}\ldots n_k^{s_k}}\in\mathbb{R},


$$


where we need $$s_1\geq 2$$ to ensure convergence.
The following relationship between MHS and MZV is easy to check, and will be useful:


$$


\sum_{n=1}^\infty \frac{H_n(s_1,\ldots,s_k)}{n^s}=\zeta(s,s_1,\ldots,s_k)+\zeta(s+s_1,s_2,\ldots,s_k).


$$


MHS's and MZV's satisfy what's called a quasi-shuffle identity. One instance of this is given by the following:

$$
\begin{eqnarray*}
H_n(1)^2&=&\left(\sum_{n_1=1}^n\frac{1}{n_1}\right)\left(\sum_{n_2=1}^n\frac{1}{n_2}\right)\\
&=&\left(\sum_{n\geq n_1>n_2}+\sum_{n\geq n_2>n_1}+\sum_{n\geq n_1=n_2}\right)\frac{1}{n_1n_2}\\
&=&2H_n(1,1)+H_n(2).
\end{eqnarray*}
$$

Using the relationship between MHS and MZV and the quasi-shuffle identity, the left hand side of your identity equals


$$


2\zeta(3,1,1)+2\zeta(4,1)+\zeta(3,2)+\zeta(5).


$$


The expression $$\zeta(2)\zeta(3)$$ can also be expanded with a quasi-shuffle identity:


$$


\zeta(2)\zeta(3)=\zeta(2,3)+\zeta(3,2)+\zeta(5).


$$


This means your identity is equivalent to the MZV identity


$$


2\zeta(3,1,1)+2\zeta(4,1)+2\zeta(3,2)+\zeta(2,3)=\frac{3}{2}\zeta(5).


$$


This identity is linear and homogeneous (that is, each MZV $$\zeta(s_1,\ldots,s_k)$$ that appears satisfies $$s_1+\ldots+s_k=5$$).
There is a ton of literature on producing homogeneous relations among multiple zeta values. One general class of relations, called the extended double shuffle relations, is conjectured to include all relations.
You identity follows by taking a linear combination of the following MZV relations, which can be found in the literature: the double shuffle relation applied to $$\zeta(2)\zeta(3)$$ (see Derivation and double shuffle relations for multiple zeta values, by Ihara, Kaneko, and Zagier):


$$


\zeta(5)=2\zeta(3,2)+6\zeta(4,1),


$$


duality applied to $$\zeta(3,1,1)$$ (this is a consequence of an expression of Konstsevich for MZV as iterated integrals, see The algebra of multiple harmonic series, by Hoffman):


$$


\zeta(3,1,1)=\zeta(4,1),


$$


and the sum formula (known in this case by Euler and proven in the general case independently by Granville and Zagier, the statement can also be found in The algebra of multiple harmonic series):


$$


\zeta(2,3)+\zeta(3,2)+\zeta(4,1)=\zeta(5).


$$



