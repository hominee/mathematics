---
layout: post
title: Problem related to calculus and elliptic integrals
tag:
 - calculus
 - definite-integrals
 - special-functions
 - closed-form
 - elliptic-integrals

description: Problem related to calculus and elliptic integrals

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

How to prove $$\int_0^\pi\frac{\ln(2+\cos\phi)}{\sqrt{2+\cos\phi}}d\phi=\frac{\ln3}{\sqrt3}K\left(\sqrt{\frac23}\right)$$?

<!–-break-–>


How can I prove the following conjectured identity?

 $$ 
\int_0^\pi\frac{\ln(2+\cos\phi)}{\sqrt{2+\cos\phi}}d\phi\stackrel?=\frac{\ln3}{\sqrt3}K\left(\sqrt{\frac23}\right),\tag1
 $$ 

where $$K(x)$$ is the complete elliptic integral of the 1ˢᵗ kind:

 $$ 
K(x)={_2F_1}\left(\frac12,\frac12;\ 1;\ x^2\right)\cdot\frac\pi2.\tag2
 $$ 

.

# Answer 


$$\int^{\pi}_0\cos^{2k+1}\phi d\phi=0$$, and 
 $$ 
\int^{\pi}_0\cos^{2k}\phi d\phi=\sqrt{\pi}\Gamma(k+1/2)/\Gamma(k+1)=2^{-2k}\pi\binom{2k}{k}.
 $$ 

Therefore
 
 $$ 
\begin{align*}
I(n) &=\int^{\pi}_0\sum_{m=0}^{\infty}2^{n-m}\binom{n}{m}\cos^m\phi~d\phi\\
&=2^n\sum_{m=0}^{\infty}2^{-m}\binom{n}{m}\int^{\pi}_0\cos^m\phi~d\phi\\
&=2^n\pi\sum_{k=0}^{\infty}2^{-2k}\binom{n}{2k}2^{-2k}\binom{2k}{k}\\
&=2^n\pi~{}_2F_1\left(\frac{1-n}2,-\frac{n}{2};1;\frac14 \right)\\
&=2^n\pi\left(\frac23\right)^{-n}~{}_2F_1\left(-n,\frac{1}{2};1;\frac23\right)\\
&=3^n\pi~{}_2F_1\left(-n,\frac{1}{2};1;\frac23\right)\\
\end{align*}
 $$ 

Using DLMF 15.8.13 with $$a=-n$$, $$b=1/2$$ and $$z=2/3$$.
We note that $$I(-1/2)=\frac{2}{\sqrt{3}}K(\sqrt{2/3})$$.
Edit: We have
 
 $$ 

I(n)=3^n\pi~{}_2F_1\left(-n,\frac{1}{2};1;\frac23\right)=\frac{\pi}{\sqrt{3}}~{}_2F_1\left(n+1,\frac{1}{2};1;\frac23\right)=3^{n+1/2}I(-n-1).
 $$ 

Therefore, If we write $$J(n)=3^{-n/2}I(n)$$, then $$J(n)=J(-n-1)$$, and consequently $$J'(-1/2)=0$$.
Thus
 
 $$ 

\begin{align*}
I'(-1/2) &=\left|\frac{d}{dn}3^{n/2}J(n)\right|_{n=-1/2}\\
&=\left|\left(3^{n/2}J'(n)+3^{n/2}\frac{\log 3}{2}J(n)\right)\right| _{n=-1/2}\\
&=3^{-1/4}\frac{\log 3}{2}J(-1/2)\\
&=\frac{\log 3}{2}I(-1/2)\\
&=\frac{\log 3}{\sqrt{3}}K(\sqrt{2/3}).
\end{align*}

 $$ 


