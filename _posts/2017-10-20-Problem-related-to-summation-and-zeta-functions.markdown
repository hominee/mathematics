---
layout: post
title: Problem related to summation and zeta functions
tag:
 - summation
 - zeta-functions

description: Problem related to summation and zeta functions

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Prove that this summation evaluates out to $$\zeta(2)-1$$

<!–-break-–>


we are  aware of the following identity:


$$

\sum_{m=1}^\infty \left(\frac{1}{m}-\left(\zeta(2)-\sum_{n=1}^m \frac{1}{n^2}\right)\right)=\zeta(2)-1

$$


we can't quite figure out how to prove this result.
 Maybe this has to do with some specific properties of $$\zeta(x)$$, but we really don't know enough yet.
 If possible, as well, could one generalize this result for looking at more than just $$\zeta(2)$$
.


# Answer 


$$\sum_{m=1}^\infty \left(\frac{1}{m}-\left(\zeta(2)-\sum_{n=1}^m \frac{1}{n^2}\right)\right)=\zeta(2)-1
$$
Playing around
and seeing what happens.
Since
$$\zeta(2)
=\sum_{n=1}^{\infty} \frac{1}{n^2}
$$,
the left side is
$$\begin{array}\\
\sum_{m=1}^\infty \left(\frac{1}{m}-\left(\sum_{n=m+1}^{\infty} \frac{1}{n^2}\right)\right)
&=\sum_{m=1}^\infty \left(\sum_{n=m+1}^{\infty}\left(\frac{1}{n-1}-\frac1{n}\right)-\left(\sum_{n=m+1}^{\infty} \frac{1}{n^2}\right)\right)\\
&=\sum_{m=1}^\infty \left(\sum_{n=m+1}^{\infty}\left(\frac{1}{n(n-1)}\right)-\left(\sum_{n=m+1}^{\infty} \frac{1}{n^2}\right)\right)\\
&=\sum_{m=1}^\infty \left(\sum_{n=m+1}^{\infty} \left(\frac{1}{n(n-1)}-\frac{1}{n^2}\right)\right)\\
&=\sum_{m=1}^\infty \sum_{n=m+1}^{\infty} \frac{1}{n^2(n-1)}\\
&=\sum_{n=2}^{\infty}\sum_{m=1}^{n-1}  \frac{1}{n^2(n-1)}
\qquad\text{(Looking good!)}\\
&=\sum_{n=2}^{\infty}(n-1)  \frac{1}{n^2(n-1)}\\
&=\sum_{n=2}^{\infty} \frac{1}{n^2}\\
&=\zeta(2)-1
\qquad\text{Shazam!}
\end{array}
$$

