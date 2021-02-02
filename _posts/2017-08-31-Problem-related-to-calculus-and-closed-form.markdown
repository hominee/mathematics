---
layout: post
title: Problem related to calculus and closed form
tag:
 - calculus
 - integration
 - definite-integrals
 - closed-form

description: Problem related to calculus and closed form

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Evaluating $$\int_0^{2\pi}\frac{dt}{\sqrt[4]{P(\cos t,\sin t)}}$$

<!–-break-–>




 $$ 
{\LARGE\int}_0^{2\pi}\frac{dt}{\sqrt[{\LARGE 4}]{A\Big(\sin^8t+\cos^8t\Big)+B\Big(\sin^6t\cos^2t+\sin^2t\cos^6t\Big)+C~\sin^4t\cos^4t}}~=~?
 $$ 


where $$A=0.3$$, $$B=-3.3$$, and $$C=10$$. its numerical value is about $$12.0165220075768590.$$ 
The inverse Symbolic Calculator seems baffled. Maple and Mathematica are both unable to 
return a closed form.

Motivation:

$$\qquad\qquad\qquad\quad$$ The above shape is given by the implicit polynomial equation 
 $$ 
A\Big(x^8+y^8\Big)+B\Big(x^6y^2+x^2y^6\Big)+C~x^4y^4=R^8,
 $$ 
 where $$A=0.3$$, $$B=-3.3$$, $$C=10$$, and $$R=2$$. Letting $$x=r\sin t$$ and $$y=r\cos t$$, we are finally able to express it in polar coordinates, since the Cartesian ones seem somewhat inadequate, given its extremely concave shape, which render it quite resistant to being parsed in terms of single-value functions, despite various sectionings and rotations. Thus the afore-mentioned integral is born. But whether it possesses a closed form, even one in terms of special functions, such as elliptic integrals, is beyond me. we  don't really see the tangent half-angle substitution going anywhere. Perhaps some complex integration methods are in order ?
.

# Answer 


in addition to the several equivalent integrals already published, this one is of interest :

 $$ 
{\LARGE\int}_0^{\infty}\frac{4~dt}{\sqrt[{\LARGE 4}]{4A\cosh^2t+2B\cosh t+C-2A}}
 $$ 

Suppose that a closed form exists for this integral. By "closed form" we  mean the combination of a limited number of standard functions. This closed form must be valid for particular values of $$A,B,C$$, for example $$A=1/4, B=1/2, C=1/2$$, i.e. the integral :

 $$ 
{\LARGE\int}_0^{\infty}\frac{dt}{\sqrt[{\LARGE 4}]{\cosh^2t+\cosh t}}
 $$ 

As far as we  know, there is no closed form for it, which is in contradiction with the above supposition. That is the reason why we  think that it is doubtful that a closed form exists for the first integral. May be, it might exists a closed form involving other special functions not referenced or not today considered as standard function in the publications.   

