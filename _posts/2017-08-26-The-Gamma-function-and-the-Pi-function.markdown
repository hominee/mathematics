---
layout: post
title: The Gamma function and the Pi function
tag:
 - soft-question
 - notation
 - special-functions
 - gamma-function

description: The Gamma function and the Pi function

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

The Gamma function and the Pi function

<!–-break-–>


we  have been studying differential equation, in particular special functions.
Euler's Gamma function, and Gauss's Pi function are essentially the same, differing only by an offset of one unit.
for  $$z\in\mathbb C,\qquad {\frak R} (z)>0$$
 
 $$
\Gamma(z)=\int\limits_0^\infty x^{z-1}e^{-x}\,\mathrm dx
 $$ 


 $$ 
\Pi(z)=\Gamma(z+1)=\int\limits_0^\infty x^ze^{-x}\,\mathrm dx
 $$ 

Both extend the notion of the factorial (which is only defined for positive integers).

 $$ 
\Gamma(z+1)=\Pi(z)=z!,\qquad z\in\mathbb Z \geq0
 $$ 


The Pi function appears to be a more natural analog of the factorial (it dosen't introduce the unit offset).
My text book exclusively uses the Gamma function, and dosen't mention the Pi function at all.
we  was wondering if there is any good reasons to focus on the Gamma function (presumably it makes some calculations simpler further down the line).

The best reason we  can come up with on my own is that for Laplace transforms 

 $$ 
\mathcal L\big\{ t^r\big\}=\frac{\Pi(r)}{s^{r+1}}=\frac{\Gamma(r+1)}{s^{r+1}},\qquad r\geq-1 \in\mathbb R
 $$ 

Using the Gamma function here preserves some symmetry.
we are  not sure it this is the reason or if there are some subtleties we are  completely missing.

# Answer 


Since you mention Laplace transforms, in its current form $$\Gamma(s)$$ is the Mellin transform of $$e^{-x}$$.  
Here is another reason which is perhaps the most convincing.  The Haar measure of a subset $$S\subset \mathbb{R}^\times$$ of the multiplicative group of real numbers is $$\int_{x\in S} \frac{dt}{t}$$, so the measure $$\frac{dt}{t}$$ over the real line is natural.  The Gamma function is an analogue of a Gauss sum, and is the integral of multiplicative function $$x^s$$ against the additive function $$e^{-x}$$ over the measure of the group.  
This problem was posed on Math Overflow, and received a large number of upvotes there.  Take a look at the answers appearing on this thread: https://mathoverflow.net/questions/20960/why-is-the-gamma-function-shifted-from-the-factorial-by-1

