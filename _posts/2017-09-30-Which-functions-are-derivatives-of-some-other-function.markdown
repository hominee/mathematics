---
layout: post
title: Which functions are derivatives of some other function
tag:
 - real-analysis
 - integration

description: Which functions are derivatives of some other function

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Which functions are derivatives of some other function?

<!–-break-–>


There is a fundamental formula in integral calculus which states that $$\int_a^bF'(x)dx=F(b)-F(a)$$. This formula gives a connection between definite and indefinite integrals. There are plenty of functions which are integrable (in the definite sense)-for example each bounded measurable function is ok. However we don't know precisely which functions do have indefinite integral: in other words which functions are derivatives of some other function?
For example continuity is enough: on the other hand one cas show that each function being the derivative (although need not to be continuous) has the Darboux property. So my question is 

Which functions are derivatives of some other function? 

.

# Answer 


The problem is a rather famous (and natural) one.  It was first explicitly stated by W. H. Young in 1911. we like quoting this passage so much (even if only to find an excuse to use the word "mooted") that we won't resist that impulse here.

"Recent research [of Lebesgue and Vitali] has provided us with a set of
  necessary and sufficient conditions that a function may be the
  indefinite integral..., of another function and the way has thus been
  opened to important developments. The corresponding, much more
  difficult, problem of determining necessary and sufficient conditions
  that a function may be a differential coefficient, has barely been
  mooted; indeed, though we know a number of necessary conditions no set
  even of sufficient conditions has to my knowledge ever been
  formulated, except that involved in the obvious statement that a
  continuous function is a differential coefficient. The necessary
  conditions in question are of considerable importance and interest.
  A function which is a differential coefficient has, in fact, various
  striking properties. It must be pointwise discontinuous with respect
  to every perfect set; it can have no discontinuities of the first
  kind; it assumes in every interval all values between its upper and
  lower bounds in that interval; its value at every point is one of the
  limits on both sides of the values in the neighbourhood; its upper and
  lower bounds, when finite, are unaltered, if we omit the values at any
  countable set of points; the points at which it is infinite form an
  inner limiting set of content zero. From these necessary conditions
  we are able to deduce much valuable information as to when a function
  is certainly not a differential coefficient . . . . These conditions
  do not, however, render us any material assistance, even in answering
  the simple question as to whether the product of two differential
  coefficients is a differential coefficient, and this not even in the
  special case in which one of the differential coefficients is a
  continuous function." ...from W H Young,  A note on the property of being a differential coefficient. Proc. London Math. Soc. 1911
  (2) 9, 360-368.

In the monograph by  Andrew M. Bruckner, Differentiation of real functions, Chapter seven there is a discussion of the problem of characterizing derivatives.
Andy has updated his account of this problem in a survey article for the Real Analysis Exchange: 

Bruckner, Andrew M. The problem of characterizing derivatives
  revisited. Real Anal. Exchange 21 (1995/96), no. 1, 112--133.

Here are a few actual characterizations of derivatives:

C. Neugebauer, Darboux functions of Baire class 1 and derivatives,
  Proc. Amer. Math. Soc., 13 (1962), 838–843.
D. Preiss and M. Tartaglia, On Characterizing Derivatives, Proceedings
  of the American Mathematical Society, Vol. 123, No. 8 (Aug., 1995),
  2417-2420.
Chris Freiling, On the problem of characterizing derivatives, Real
  Analysis Exchange 23 (1997/98), no. 2, 805-812.
Brian S. Thomson, On Riemann Sums, Real Analysis Exchange 37
  (2011/12), 1-22.

My guess is that you won't find any of these satisfying in the way, for example, that "continuous" functions have multiple necessary and sufficient characterizations, most of them natural and compelling.

