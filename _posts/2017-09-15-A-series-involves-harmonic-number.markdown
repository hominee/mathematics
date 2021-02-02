---
layout: post
title: A series involves harmonic number
tag:
 - real-analysis
 - sequences-and-series
 - riemann-zeta
 - harmonic-numbers

description: A series involves harmonic number

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

A series involves harmonic number

<!–-break-–>


How do we get a closed form for


$$

\sum_{n=1}^\infty\frac{H_n}{(2n+1)^2}

$$


.

# Answer 


Here's another solution. I'll denote various versions of the sum


$$


\sum_{k=1}^\infty\sum_{j=1}^k\frac1j\frac1{k^2}


$$


by an $$S$$ with two subscripts indicating which parities are included, the first subscript referring to the parity of $$j$$ and the second to the parity of $$k$$, with '$$\mathrm e$$' denoting only the even terms, '$$\mathrm o$$' denoting only the odd terms, '$$+$$' denoting the sum of the even and odd terms, i.e. the regular sum, and '$$-$$' denoting the difference between the even and the odd terms, i.e. the alternating sum. Then


$$





$$
\begin{align*}
\sum_{n=1}^\infty\frac{H_n}{(2n+1)^2}
&=
2\sum_{n=1}^\infty\sum_{i=1}^n\frac1{2i}\frac1{(2n+1)^2}
\\
&=
2S_{\mathrm{eo}}
\\
&=
2(S_{++}-S_{\mathrm o+}-S_{\mathrm{ee}})
\\
&=
2\left(S_{++}-S_{\mathrm o+}-\frac18S_{++}\right)
\\
&=
2\left(\frac38S_{++}+\left(\frac12S_{++}-S_{\mathrm o+}\right)\right)
\\
&=
\frac34S_{++}+S_{-+}
\\
&=
\frac32\zeta(3)+\sum_{k=1}^\infty\sum_{j=1}^k\frac{(-1)^j}j\frac1{k^2}\;,
\end{align*}


$$


$$


where we used the result $$\sum_nH_n/n^2=2\zeta(3)$$ from the blog post Aeolian linked to and reduced the present problem to finding the analogue of that result with the sign alternating with $$j$$, which we can rewrite as


$$





$$
\begin{align*}
\sum_{k=1}^\infty\sum_{j=1}^k\frac{(-1)^j}j\frac1{k^2}
&=
\sum_{k=1}^\infty\sum_{j=1}^\infty\frac{(-1)^j}j\frac1{k^2}-\sum_{k=1}^\infty\sum_{j=k+1}^\infty\frac{(-1)^j}j\frac1{k^2}
\\
&=
-\zeta(2)\log2+\sum_{j=1}^\infty\frac{(-1)^j}{j+1}\sum_{k=1}^j\frac1{k^2}\;.
\end{align*}


$$


$$


This last double sum can be evaluated by the method applied in the blog post, making use of the fact that summing the coefficients of a power series in $$x$$ corresponds to dividing it by $$1-x$$:


$$





$$
\begin{align*}
\sum_{j=1}^\infty x^j\sum_{k=1}^j\frac1{k^2}=\def\Li{\operatorname{Li}}\frac{\Li_2(x)}{1-x}\;,
\end{align*}


$$


$$


where $$\Li_2$$ is the dilogarithm. Thus


$$





$$
\begin{align*}
\sum_{j=1}^\infty\frac{(-1)^j}{j+1}\sum_{k=1}^j\frac1{k^2}
&=
\int_0^1\sum_{j=1}^\infty (-x)^j\sum_{k=1}^j\frac1{k^2}\mathrm dx
\\
&=
\int_0^1\frac{\Li_2(-x)}{1+x}\mathrm dx
\\
&=
\left[\Li_2(-x)\log(1+x)\right]_0^1+\int_0^1\frac{\log^2(1+x)}x\mathrm dx
\\
&=-\frac{\zeta(2)}2\log2+\frac{\zeta(3)}4\;,
\end{align*}


$$


$$


where the boundary term is evaluated using $$\Li_2(-1)=-\eta(2)=-\zeta(2)+2\zeta(2)/4=-\zeta(2)/2$$ and the integral in the second term is evaluated in this separate question. Putting it all together, we have


$$





$$
\begin{align*}
\sum_{n=1}^\infty\frac{H_n}{(2n+1)^2}
&=
\frac74\zeta(3)-\frac32\zeta(2)\log2
\\
&=
\frac74\zeta(3)-\frac{\pi^2}4\log2\;.
\end{align*}


$$


$$


we believe all the rearrangements can be justified, despite the series being only conditionally convergent in $$j$$, by considering the partial sums with $$j$$ and $$k$$ both going up to $$M$$; then all the rearrangements can be carried out within that finite square of the grid, and the sums of the remaining terms go to zero with $$M\to\infty$$.

