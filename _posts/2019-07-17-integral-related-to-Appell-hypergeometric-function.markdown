---
layout: post
title: integral related to Appell hypergeometric function
tags:
  - integral 
  - closed-form
  - Appell-hypergeometric-function
  - real-analysis
  
description:  
  integral related to Appell hypergeometric function
hero: https://source.unsplash.com/collection/145103/
overlay: blue
published: true
---


# Question

Closed form of :

$$

{\large\int}_0^1\frac{\ln^3x}{\sqrt{x^2-x+1}}dx

$$



<!–-break-–>

This is a follow-up to my earlier question [Closed form for $${\large\int}_0^1\frac{\ln^2x}{\sqrt{1-x+x^2}}dx$$](https://math.stackexchange.com/q/918821/19661).

Is there a closed form for this integral?

$$
to=\int_0^1\frac{\ln^3x}{\sqrt{x^2-x+1}}dx\tag1
$$


_Mathematica_ and _Maple_ cannot evaluate it directly. A numeric approximation for it is

$$
to\approx-6.1665252325192513801994672415450909679747097867356795481...\tag2
$$

(click [here](http://goo.gl/oFzjSP) to see more digits).

As to mentioned in the earlier question, _Mathematica_ is able to find a closed form for a parameterized integral in terms of the [Appell hypergeometric function](http://mathworld.wolfram.com/AppellHypergeometricFunction.html):

$$
to(a)=\int_0^1\frac{x^a}{\sqrt{x^2-x+1}}dx\\=\frac1{a+1}F_1\left(a+1;\frac{1}{2},\frac{1}{2};a+2;(-1)^{\small1/3},-(-1)^{\small2/3}\right),\tag3
$$

but taking a derivative from this looks a hard problem.

# Answer

Followed the same approach used in an answer to [another
question](https://math.stackexchange.com/questions/921641), and
expanded your integral in multiple polylogarithms of weight 4, then
used some patterns in their values of weight 3 to guess terms that
might appear in the integral. Then to used an integer relation
algorithm to express your integral in terms of logs, zeta functions
and polylogarithms of small rational arguments with a tolerance of
about $$10^{-200}$$, and to found this value, which is correct to $$3000$$
digits.

There are $$27$$ polylogarithm terms there in total, and while to managed
to simplify them somewhat, to never quite managed to evaluate some of them
except by an integer relation algorithm.

Here it is:

$$
\textstyle\def\Li{\mathrm{Li}}
-6 \Li_2(\frac{1}{3}) \zeta (2)+27 \Li_4(\frac{3}{4})+36 \Li_4(\frac{2}{3})-4 \Li_4(\frac{1}{2})-18 \\
 \Li_4(\frac{1}{3})-\frac{9}{2} \Li_4(\frac{1}{4})+6 \Li_2(\frac{1}{3}){}^2+6 \Li_2(\frac{1}{3}) \log ^2 3 \\
 +24 \Li_2(\frac{1}{3}) \log ^2 2-48 \Li_3(\frac{2}{3}) \log3+96 \Li_3(\frac{2}{3}) \log2-48 \Li_3(\frac{1}{3}) \log3 \\
 +72 \Li_3(\frac{1}{3}) \log2-24 \Li_2(\frac{1}{3}) \log2 \log3+78 \zeta (3) \log3-142 \zeta (3) \log2 \\
 -\frac{151}{4} \zeta (4)-69 \zeta (2) \log ^2 3-122 \zeta (2) \log ^2 2+192 \zeta (2) \log2 \log3 \\
 +\frac{73}{4} \log ^4 3+\frac{89}{6} \log ^4 2-70 \log2 \log ^3 3-56 \log ^3 2 \log3+93 \log ^2 2 \log ^2 3

$$



Here is the equivalent Mathematica expression to save people typing:

    (-151*Pi^4)/360 - (61*Pi^2*Log[2]^2)/3 + (89*Log[2]^4)/6 + 32*Pi^2*Log[2]*Log[3] -  56*Log[2]^3*Log[3] - (23*Pi^2*Log[3]^2)/2 + 93*Log[2]^2*Log[3]^2 - 70*Log[2]*Log[3]^3 +  (73*Log[3]^4)/4 - Pi^2*PolyLog[2, 1/3] + 24*Log[2]^2*PolyLog[2, 1/3] -  24*Log[2]*Log[3]*PolyLog[2, 1/3] + 6*Log[3]^2*PolyLog[2, 1/3] + 6*PolyLog[2, 1/3]^2 +  72*Log[2]*PolyLog[3, 1/3] - 48*Log[3]*PolyLog[3, 1/3] + 96*Log[2]*PolyLog[3, 2/3] -  48*Log[3]*PolyLog[3, 2/3] - (9*PolyLog[4, 1/4])/2 - 18*PolyLog[4, 1/3] - 4*PolyLog[4, 1/2] +  36*PolyLog[4, 2/3] + 27*PolyLog[4, 3/4] - 142*Log[2]*Zeta[3] + 78*Log[3]*Zeta[3]