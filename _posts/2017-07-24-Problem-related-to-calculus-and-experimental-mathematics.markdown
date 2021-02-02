---
layout: post
title: Problem related to calculus and experimental mathematics
tag:
 - calculus
 - integration
 - definite-integrals
 - closed-form
 - experimental-mathematics

description: Problem related to calculus and experimental mathematics

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

On Reshetnikov's integral $$\int_0^1\frac{dx}{\sqrt[3]x\ \sqrt[6]{1-x}\ \sqrt{1-x\,\alpha^2}}=\frac{1}{N}\,\frac{2\pi}{\sqrt{3}\,\mid {} \alpha\mid {} }$$

<!–-break-–>


V. Reshetnikov gave the remarkable integral,

 $$ 
\int_0^1\frac{dx}{\sqrt[3]x\,\sqrt[6]{1-x}\,\sqrt{1-x\left(\sqrt{6}\sqrt{12+7\sqrt3}-3\sqrt3-6\right)^2}}=\frac\pi9(3+\sqrt2\sqrt[4]{27})\tag1
 $$ 

More generally, given some integer/rational $$N$$, we are to find an algebraic number $$\alpha$$ that solves,


 $$ 
\int_0^1\frac{dx}{\sqrt[3]x\ \sqrt[6]{1-x}\ \sqrt{1-x\,\alpha^2}}=\frac{1}{N}\,\frac{2\pi}{\sqrt{3}\,\mid {} \alpha\mid {} }\tag2
 $$ 


and absolute value $$\mid {} \alpha\mid {} $$. (Compare to the similar integral in this post.) Equivalently, to find $$\alpha$$ such that,

 $$ 
\begin{aligned}
\frac{1}{N}
&=I\left(\alpha^2;\ \tfrac12,\tfrac13\right)\\[1.8mm]
&= \frac{B\left(\alpha^2;\ \tfrac12,\tfrac13\right)}{B\left(\tfrac12,\tfrac13\right)}\\
&=B\left(\alpha^2;\ \tfrac12,\tfrac13\right)\frac{\Gamma\left(\frac56\right)}{\sqrt{\pi}\,\Gamma\left(\frac13\right)}\end{aligned} \tag3
 $$ 

with beta function $$\beta(a,b)$$, incomplete beta $$\beta(z;a,b)$$ and regularized beta $$I(z;a,b)$$. 
Solutions $$\alpha$$ for $$N=2,3,4,5,7$$ are known. Let,

 $$ 
\alpha=\frac{-3^{1/2}+v^{1/2}}{3^{-1/2}+v^{1/2}}\tag4
 $$ 

Then,

 $$ 
 - 3 + 6 v + v^2 = 0, \quad N = 2\\ 
- 3 + 27 v - 33v^2 + v^3 = 0, \quad N = 3\\
3^2 - 150 v^2 + 120 v^3 + 5 v^4 = 0, \quad N = 5\\ 
- 3^3 - 54 v + 1719 v^2 - 3492v^3 - 957 v^4 + 186 v^5 + v^6 = 0, \quad N = 7
 $$ 

and (added later),

 $$ 
3^4 - 648 v + 1836 v^2 + 1512 v^3 - 13770 v^4 + 12168 v^5 - 7476 v^6 + 408 v^7 + v^8 = 0,\quad N=4
 $$ 

using the largest positive root, respectively. The example was just $$N=2$$, while $$N=4$$ leads to,

 $$ 
I\left(\tfrac{1-\alpha}{2};\tfrac{1}{3},\tfrac{1}{3}\right)=\tfrac{3}{8},\quad\quad I\left(\tfrac{1+\alpha}{2};\tfrac{1}{3},\tfrac{1}{3}\right)=\tfrac{5}{8}
 $$ 

I found these using Mathematica's FindRoot command, and some hints from Reshetnikov's and other's works, but as much as I tried, I couldn't find prime $$N=11$$.

Q: Is it true one can find algebraic number $$\alpha$$ for all $$N$$? What is it for $$N=11$$? 

.

# Answer 


(Too long for a comment. And courtesy of V. Reshetnikov's result here, though as he points out it is tentative.)
The algebraic number $$\alpha$$ that solves,

 $$ 
\int_0^1\frac{dx}{\sqrt[3]x\ \sqrt[6]{1-x}\ \sqrt{1-x\,\alpha^2}}=\frac{1}{11}\,\frac{2\pi}{\sqrt{3}\;\alpha}
 $$ 

seems to have a $$40$$-deg minpoly. However, it turns out we can also reduce its degree and express it using the common form above. Let,

 $$ 
\alpha=\frac{3^{1/2}-v^{1/2}}{3^{-1/2}+v^{1/2}}
 $$ 

where $$v$$ is a the second largest positive root ($$r_9$$ in Mathematica syntax) of,

 $$ 
\small P(v)=-3^{10} + 23816430 v^2 - 323903448 v^3 + 2177615583 v^4 - 9297934272 v^5 + 25869358152 v^6 - 37475802144 v^7 - 16459141842 v^8 + 180065426112 v^9 - 
  338100745356 v^{10} + 329418595440 v^{11} - 211367836746 v^{12} + 
  102243404736 v^{13} - 8162926200 v^{14} - 9999738144 v^{15} + 
  1006439643 v^{16} - 134177472 v^{17} - 2246706 v^{18} + 30888 v^{19} + 
  11 v^{20} = 0
 $$ 

Also,

 $$ 
I\big(\alpha^2;\tfrac{1}{2},\tfrac{1}{3}\big)=\tfrac{1}{5}\,I\big(\tfrac{1-\alpha}{2};\tfrac{1}{3},\tfrac{1}{3}\big)=\tfrac{1}{6}\,I\big(\tfrac{1+\alpha}{2};\tfrac{1}{3},\tfrac{1}{3}\big)=\frac{1}{11}
 $$ 

with regularized beta function $$I(z;a,b)$$. Furthermore, if

 $$ 
y =\frac{r_1+r_9+r_{13}+r_{14}}{12}
 $$ 

then $$y$$ is a root of the solvable quintic,

 $$ 
67 - 1748 y - 7033 y^2 - 1378 y^3 + 234 y^4 + y^5=0
 $$ 

with discriminant divisible by $$11^4\times23^4$$. Using the other quartic symmetric polynomials show that the $$20$$-deg is just a quartic in disguise, hence is solvable. All these suggest that $$P(v)$$ is the correct polynomial for $$N=11$$.

