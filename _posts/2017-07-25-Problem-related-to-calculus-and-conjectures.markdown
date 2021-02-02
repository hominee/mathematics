---
layout: post
title: Problem related to calculus and conjectures
tag:
 - calculus
 - special-functions
 - gamma-function
 - closed-form
 - conjectures

description: Problem related to calculus and conjectures

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Is $$K\left(\frac{\sqrt{2-\sqrt3}}2\right)\stackrel?=\frac{\Gamma\left(\frac16\right)\Gamma\left(\frac13\right)}{4\ \sqrt[4]3\ \sqrt\pi}$$

<!–-break-–>


Working on this conjecture, I found its corollary, which is also supported by numeric calculations up to at least $$10^5$$ decimal digits:

 $$ 
K\left(\frac{\sqrt{2-\sqrt3}}2\right)\stackrel?=\frac{\Gamma\left(\frac16\right)\Gamma\left(\frac13\right)}{4\ \sqrt[4]3\ \sqrt\pi},
 $$ 

where $$K(x)$$ is the complete elliptic integral of the 1st kind. I did not find this specific value at MathWorld, Wolfram Functions Site, Wikipedia or DLMF. 
Is it a known value?
.

# Answer 


See here: http://mathworld.wolfram.com/EllipticIntegralSingularValue.html and also here: http://mathworld.wolfram.com/EllipticIntegralSingularValuek3.html
Your value is actually

 $$ 
 \sin \frac\pi{12} = \frac{\sqrt{2-\sqrt3}}{2}, 
 $$ 

and according to MathWorld, it is known as the third singular value $$k_3$$. It satisfies

 $$ 
 K(\sqrt{1-k_3^2}) = \sqrt{3}K(k_3) 
 $$ 

and

 $$ 
 K(k_3) = \frac{\sqrt{\pi}\Gamma(1/6)}{2\cdot 3^{3/4}\Gamma(2/3)}. 
 $$ 

Mathematica says that the two closed forms are equal.

