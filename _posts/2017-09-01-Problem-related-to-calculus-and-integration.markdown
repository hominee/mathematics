---
layout: post
title: Problem related to calculus and integration
tag:
 - calculus
 - integration

description: Problem related to calculus and integration

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Show $$\int_0^{2\pi} \exp\left(\frac{7+5 \cos x}{10+6\cos x}\right) \cos \left( \frac{\sin x}{10+6 \cos x} \right) dx = 2\pi e^{2/3}$$ Real Methods

<!–-break-–>


Taken from the post: The integral that Stumped Feynman?
i  want to know if the integral:

 $$ 
\int_0^{2\pi} \exp\left(\frac{7+5 \cos x}{10+6\cos x}\right) \cos \left( \frac{\sin x}{10+6 \cos x} \right) dx = 2\pi e^{2/3}
 $$ 

can be evaluated using strictly real methods. 
i 've tried series of $$e^x$$ and $$\cos x$$ but to no avail. i  tried differentiating under the integral, but nothing seemed to come out of it. is there any wizardry that can conjure up this answer without complex analysis.

# Answer 


Start with $$\tan \left(\frac{x}{2} \right)
=2\tan \left( \frac{t}{2} \right)
$$

$$ 
i =2\int_0^{\pi} \exp\left(\frac{7+5 \cos x}{10+6\cos x}\right) \cos \left( \frac{\sin x}{10+6 \cos x} \right) dx=8e^{5/8}\int_0^{\pi}\exp\left(\frac{\cos t}{8}\right)\cos\left(\frac{\sin t}{8}\right)\frac{dt}{5-3\cos t} 
 $$
 
 Using 
 
 $$ 
 \sum_{n=1}^{\infty} a^{n} \cos(nx) = \frac12\left(\frac{1-a^{2}}{1-2 a \cos x + a^{2}}-1\right)
 $$ 
 
 i can rewrite 
 
 $$ 
\frac{1}{5-3\cos x} =\frac14 +\frac12 \sum_{n=1}^\infty \frac{1}{3^n} \cos (nx) 
 $$ 
 
 thus i have 
 
 $$ 
i =2e^{5/8} \int_0^\pi \exp\left(\frac{\cos t}{8}\right)\cos\left(\frac{\sin t}{8}\right) dt +4e^{5/8} \sum_{n=1}^\infty \frac{1}{3^n} \int_0^\pi \exp\left(\frac{\cos t}{8}\right)\cos\left(\frac{\sin t}{8}\right) \cos(nt )dt 
 $$ 


 $$ 
=2\pi e^{5/8}+4e^{5/8}\sum_{n=1}^\infty \frac{1}{3^n} i (n)
 $$ 
 
 i  dont know how to evaluate $$i (n)$$, but maybe someone can help.

 $$ 
i (0)=\pi,i (1)=\frac{\pi}{2^4}, i (2)=\frac{\pi}{2^8}, i (3)=\frac{\pi}{3\cdot 2^{11}}, i (4)=\frac{\pi}{3\cdot2^{16}},i (5)=\frac{\pi}{3\cdot 5 \cdot 2^{19}}
 
$$
 
$$
 i (6)=\frac{\pi}{3^2\cdot5\cdot 2^{23}}, i (10)=\frac{\pi}{3^4\cdot5^2\cdot 7 \cdot 2^{39}}, i (20)=\frac{\pi}{3^8\cdot5^4 \cdot 7^2\cdot11\cdot 13\cdot 17\cdot 19\cdot 2^{79}}
 $$ 

Edit:  As seen here: https://math.stackexchange.com/a/2913057/515527 $$ i (n) =\frac{\pi} {2^{3n+1}n!}$$, plugging this into the sum and using the series for $$e^x$$ will give the result immediately..
Another approach to evaluate $$i (n)$$ is to use that 
 
 $$ 
\exp\left(\frac{\cos t}{8}\right)\cos\left(\frac{\sin t}{8}\right)=\sum_{n=0}^{\infty} \frac{\cos(nt)}{8^nn!}
 $$
 
 Since 
 
 $$ 
\int_0^\pi \cos(nx) \cos(mx) dx=\begin{cases} \frac{\pi} {2} & n=m \\ 0 & n \neq m\end{cases}
 $$ 
 
 i get that $$i (n) =\frac{\pi} {2} \frac{1} {8^n n!} $$ and the result follows. 

