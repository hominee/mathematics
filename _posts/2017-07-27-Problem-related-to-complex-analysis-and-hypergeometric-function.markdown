---
layout: post
title: Problem related to complex analysis and hypergeometric function
tag:
 - complex-analysis
 - special-functions
 - closed-form
 - hypergeometric-function

description: Problem related to complex analysis and hypergeometric function

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Closed form for $$_2F_1\left(\frac12,\frac23;\,\frac32;\,\frac{8\,\sqrt{11}\,i-5}{27}\right)$$

<!–-break-–>


I'm trying to find a closed form (in terms of simpler functions) for the following hypergeometric function with a complex argument:

 $$ 
\mathcal{Q}=\,_2F_1\left(\frac12,\frac23;\,\frac32;\,\frac{8\,\sqrt{11}\,i-5}{27}\right).\tag1
 $$ 

I have a guess (supported by thousands of digits from numerical calculations) about its argument (phase), but no ideas about its absolute value yet:

 $$ 
\arg\mathcal{Q}\approx0.168669236010871306727578153...\stackrel?=\arccos\left(\frac{12+\sqrt{33}}{18}\right)\tag2
 $$ 


 $$ 
\mid {} \mathcal{Q}\mid {} \approx0.915170225773196416688677425...\tag3
 $$ 

Can you suggest any ideas how to prove the conjecture $$(2)$$? Is there a closed form for the absolute value?

As suggested by  gammatester in a comment, the conjecture $$(2)$$ is equivalent to

 $$ 
\arg\,B\left(\frac{8\,\sqrt{11}\,i-5}{27};\,\frac12,\frac13\right)\stackrel?=\frac\pi3,\tag4
 $$ 

where $$B$$ denotes the incomplete beta function.

Also, it can be shown that another equivalent form of the conjecture $$(2)$$ is

 $$ 
B\left(\frac19;\,\frac16,\frac13\right)\stackrel?=\frac{\Gamma\left(\frac16\right)\,\Gamma\left(\frac13\right)}{2\,\sqrt\pi}.\tag5
 $$ 

.

# Answer 


Not sure how to transform conjecture $$(2)$$ to $$(5)$$. However, $$(5)$$ is true.
Let $$\;\displaystyle t = \frac{1}{1+y^3}\;$$, we can
rewrite the integral $$\;\displaystyle B\left(\frac19;\frac13,\frac16\right)\;$$ as

 $$ 

\int_0^{1/9} t^{-5/6} (1-t)^{-2/3} dt
= \int_\infty^2 (1+y^3)^{5/6}\left(\frac{1+y^3}{y^3}\right)^{2/3}\frac{-3y^2 dy}{(1+y^3)^2}
= 3 \int_2^\infty \frac{dy}{\sqrt{1+y^3}}

 $$ 

Let $$\omega = e^{\pi i/3}$$ and $$\mathbb{T} = \big\{\; m+n\omega : m, n \in \mathbb{Z}\;\big\}$$ be the triangular lattice span by $$1$$ and $$\omega$$. Let $$\wp(z)$$ be the Weierstrass elliptic $$\wp$$ function with double poles on lattice $$\mathbb{T}$$:

 $$ 
\wp(z) = \frac{1}{z^2} + \sum_{\lambda \in \mathbb{T} \setminus \{ 0 \}} \left(\frac{1}{(z-\lambda)^2} - \frac{1}{\lambda^2}\right)
 $$ 

Let $$\;\displaystyle\eta = \frac{\Gamma\left(\frac13\right)\Gamma\left(\frac16\right)}{\sqrt{3\pi}}\;$$, it is known that $$\wp(z)$$ satisfies a differential equation of the form:

 $$ 
\wp'(z)^2 = 4 \wp(z)^3 - g_2 \wp(z) - g_3\quad\text{ where }\quad g_2 = 0 \;\text{ and }\;g_3 = \frac{\eta^6}{16}
 $$ 

Let $$\;\displaystyle y(z) = -\frac{4}{\eta^2} \wp\left(\frac{iz}{\eta}\right)$$. Using symmetry, it is not hard to see as $$z$$ varies from $$0$$ to $$\frac{\eta}{\sqrt{3}}$$ along the real axis, $$y(z)$$ remains real and positive, decreases from $$\infty$$ at $$z = 0$$ to $$0$$ at $$z = \frac{\eta}{\sqrt{3}}$$. 
In terms of $$z$$, we have:

 $$ 
\frac{dy}{\sqrt{1+y^3}} = 
\frac{-\frac{4i}{\eta^3}\wp'\left(\frac{iz}{\eta}\right)dz}{
\sqrt{1-\frac{64}{\eta^6}\wp\left(\frac{iz}{\eta}\right)^3}}
= 
\frac{-4i\wp'\left(\frac{iz}{\eta}\right)dz}{
\sqrt{16g_3-64\wp\left(\frac{iz}{\eta}\right)^3}}
= - dz

 $$ 

From this, we get

 $$ 
B\left(\frac19;\frac13,\frac16\right) = -3 \left[ y^{-1}(\infty) - y^{-1}(2)\right]
= 3y^{-1}(2)
 $$ 

This allow us to simplify conjecture $$(5)
$$
 
$$
B\left(\frac19;\frac13,\frac16\right) \stackrel{?}{=} 
\frac{\Gamma\left(\frac13\right)\Gamma\left(\frac16\right)}{2\sqrt{\pi}} = \frac{\sqrt{3}}{2}\eta
\iff y^{-1}(2) \stackrel{?}{=} \frac{\eta}{2\sqrt{3}}
\iff  \wp(\frac{i}{2\sqrt{3}}) \stackrel{?}{=} -\frac{\eta^2}{2}

 $$ 

Let $$u = \frac{i}{2\sqrt{3}}$$. Since $$\wp(2u) = \wp\left(\frac{i}{\sqrt{3}}\right) = 0$$, we can use the duplication formula for Weierstrass elliptic $$\wp$$ function to obtain

 
$$

\begin{align*}
& 0 = \wp(2u) = \frac14\left(\frac{(6\wp(u)^2-\frac12 g_2)^2}{4\wp(u)^3-g_2\wp(u)-g_3}\right) -2\wp(u) \\
\iff & \wp(u)\left(\frac{\wp(u)^3 + 2g_3}{4\wp(u)^3-g_3}\right) = 0\\
\implies & \wp(u) = (-2g_3)^{1/3} = \left(-\frac{\eta^6}{8}\right)^{1/3} = -\frac{\eta^2}{2}
\end{align*}

$$
 

i.e. the conjecture $$(5)$$ is true.

