---
layout: post
title: Problem related to sequences and series and harmonic numbers
tag:
 - sequences-and-series
 - approximation
 - harmonic-numbers

description: Problem related to sequences and series and harmonic numbers

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Closed form for the harmonic approximation sum $$\sum _{k=1}^{\infty } \left(H_k^{(2)}-\zeta (2)\right){}^2$$

<!–-break-–>


Question
Is there a closed form of this harmonic approximation sum 


$$

s=\sum _{k=1}^{\infty } \left(H_k^{(2)}-\zeta (2)\right){}^2\tag{1}

$$


The notation is standard.
Motivation
This question concerns a field which was treated frequently by many contributors here  where, generally speaking, an appropriate functional of the difference of a summand an its asymptotic approximation is summed up, and mostly it is asked if there is a closed form of this sum in terms of "standard constants". The approximation as well as the functional must be chosen such that the resulting infinite sum in convergent. There are many examples of such "approximation sums".
Recently [1] we posted a question related to the approximation sum


$$

\sum _{k=1}^{\infty } \left(H_k-(\log(k) + \gamma)\right){}^2\tag{2}

$$


This led to the problem of a sum containing an uncommon $$\log$$-factor instead of the common polynomial in the index.
In an attempt to get rid of the $$\log$$ but still retain a non trivial problem we ask here to find a closed form for $$s$$ defined in (1).
A natural generalization is the generating function


$$

s_{m,p}(x)=\sum _{k=1}^{\infty } x^k \left(H_k^{(m)}-\zeta (m)\right){}^p\tag{3}

$$


To my knowledge, approximation sums containing modified harmonic numbers have not been investigated here.
The numerical value is


$$

N(s_2) = 0.900362625200937377409205241520956358081230891307664

$$


Solution attempt
We consider partial sums and write $$s = \sigma_1+\sigma_2+\sigma_3$$ where


$$

\sigma_1 = \sum _{k=1}^{n } \left(H_k^{(2)}\right){}^2\tag{4a}

$$




$$

\sigma_2 =-2 \zeta(2) \sum _{k=1}^{n } H_k^{(2)}{}\tag{4b}

$$




$$

\sigma_3 = n \zeta(2)^2\tag{4c}

$$


The sum in $$\sigma_2$$ can be calculated:


$$

\sum _{k=1}^n H_k^{(2)}=(n+1) H_{n+1}^{(2)}-H_{n+1}\tag{5}

$$


so that 


$$

\sigma_2 =-2 \zeta(2)\left( (n+1) H_{n+1}^{(2)}-H_{n+1}\right)\tag{6}

$$


and we are left with $$\sigma_1$$ which can be easily shown by the reader to reduce to the calculation of either


$$

h_2 = \sum _{k=1}^n \frac{H_k}{k^2}\tag{7}

$$


or


$$

h_4 = \sum _{k=1}^n \frac{H_{k}^{(2)}}{k}\tag{8}

$$


These sums have been discussed (and christianed) earlier in [2] where also this relation has been derived 


$$

h_2+h_4 =H_n  H_{n}^{(2)} + H_{n}^{(3)}\tag{9}

$$


which means that knowledge of one of these function is suffient.
It would be nice to see an explicit form for the (finite) sums $$h$$ in terms of the elements of the set containing (modified) harmonic numbers and scalars. 
But for the present task only the limit of large index must be determined.
References
[1] Generating function for harmonic number times log ($$H_k log(k)$$)
[2] Sum of powers of Harmonic Numbers
.

# Answer 


By summation by parts


$$

\begin{eqnarray*} -\sum_{k\geq 1}1\cdot\left(\zeta(2)-H_k^{(2)}\right)^2 &=& \sum_{n\geq 1}\frac{n}{(n+1)^4}+\frac{2n (H_n^{(2)}-\zeta(2))}{(n+1)^2}\\&=&\zeta(3)-\zeta(4)+2\sum_{n\geq 1}\frac{H_n^{(2)}-\zeta(2)}{n+1}-2\sum_{n\geq 1}\frac{H_n^{(2)}-\zeta(2)}{(n+1)^2}\\&=&\zeta(3)-\zeta(4)+2\zeta(2)-4\zeta(3)+\frac{7\pi^4-60\pi^2}{180}\end{eqnarray*}

$$


(the last identity follows from standard Euler sums) and by simplifying we get


$$

\boxed{ \sum_{n\geq 1}\left(\zeta(2)-H_k^{(2)}\right)^2 = \color{red}{3\,\zeta(3)-\zeta(2)^2.}}

$$


Similarly,


$$

\begin{eqnarray*}\sum_{k\geq 1}\left(\zeta(m)-H_k^{(m)}\right)^2 &=& \sum_{k\geq 1}\left[2\,\zeta(m)-H_{k}^{(m)}-H_{k+1}^{(m)}\right]\frac{k}{(k+1)^m}\\&=&\sum_{k\geq 1}\left[2\,\zeta(m)-2H_{k}^{(m)}-\frac{1}{(k+1)^m}\right]\cdot\left[\frac{1}{(k+1)^{m-1}}-\frac{1}{(k+1)^m}\right]\end{eqnarray*}

$$


boils down to computing few values of $$\zeta$$, recalling $$\sum_{k\geq 1}\frac{H_k^{(m)}}{k^m}=\frac{\zeta(2m)+\zeta(m)^2}{2} $$ (symmetry) and tackling $$\sum_{k\geq 1}\frac{H_k^{(m)}}{k^{m-1}}$$ or $$\sum_{k\geq 1}\frac{H_k^{(m-1)}}{k^m}$$. Flajolet and Salvy outline efficient ways through residues. The first cases are


$$

 \sum_{k\geq 1}\frac{H_k}{k^2}=2\,\zeta(3),\qquad \sum_{k\geq 1}\frac{H_k^{(2)}}{k^3} = 3\,\zeta(2)\,\zeta(3)-\frac{9}{2}\,\zeta(5) 

$$




$$

 \sum_{k\geq 1}\frac{H_k^{(3)}}{k^4} = -10\,\zeta(2)\,\zeta(5)+18\,\zeta(7). 

$$



