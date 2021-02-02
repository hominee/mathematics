---
layout: post
title: Problem related to real analysis and sequences and series
tag:
 - real-analysis
 - sequences-and-series

description: Problem related to real analysis and sequences and series

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Self-Contained Proof that $$\sum\limits_{n=1}^{\infty} \frac1{n^p}$$ Converges for $$p > 1$$

<!–-break-–>


To prove the convergence of the p-series 

 $$ 
\sum_{n=1}^{\infty} \frac1{n^p}
 $$ 

for $$p > 1$$, one typically appeals to either the integral Test or the Cauchy Condensation Test.
we are  wondering if there is a self-contained proof that this series converges which does not rely on either test.  
we  suspect that any proof would have to use the ideas behind one of these two tests.

# Answer 


We can bound the partial sums by multiples of themselves:

 $$ 
\begin{eqnarray*}
S_{2k+1}
&=&
\sum_{n=1}^{2k+1}\frac{1}{n^p}\\
&=&
1+\sum_{i=1}^k\left(\frac{1}{(2i)^p}+\frac{1}{(2i+1)^p}\right)\\
&<&1+\sum_{i=1}^k\frac{2}{(2i)^p}\\
&=&1+2^{1-p}S_k\\
&<&1+2^{1-p}S_{2k+1}\;.
\end{eqnarray*}
 $$ 

Then solving for $$S_{2k+1}$$ yields

 $$ 
S_{2k+1}<\frac{1}{1-2^{1-p}}\;,
 $$ 

and since the sequence of partial sums is monotonically increasing and bounded from above, it converges.
(See also: Teresa Cohen & William J. Knight, Convergence and Divergence of $$\sum_{n=1}^{\infty} 1/n^p$$, Mathematics Magazine, 52(3), 1979, p.178. https://doi.org/10.1080/0025570X.1979.11976778)

