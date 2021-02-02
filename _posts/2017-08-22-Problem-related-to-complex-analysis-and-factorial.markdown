---
layout: post
title: Problem related to complex analysis and factorial
tag:
 - complex-analysis
 - complex-numbers
 - factorial

description: Problem related to complex analysis and factorial

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Why is $$i! = 0.498015668 - 0.154949828i$$?

<!–-break-–>


While moving my laptop the other day, we  ended up mashing the keyboard a little, and by pure chance managed to do a google search for i!.
Curiously, Google's calculator dutifully informed me that $$i!$$ was, in fact, $$0.498015668 - 0.154949828i$$.
Why is this?
we  know what a factorial is, so what does it actually mean to take the factorial of a complex number? Also, are those parts of the complex answer rational or irrational? Do complex factorials give rise to any interesting geometric shapes/curves on the complex plane?
.

# Answer 


it is sort of an abuse of what is meant by factorial. The usual definition of

 $$ 
n! = \prod_{k=1}^n k
 $$ 

obviously cannot apply because you can sit and count integers until the end of time and beyond and you'll never find $$i$$.
However, we can generalise what we mean by factorial by using a property of the gamma function, which is defined to be

 $$ 
\Gamma(z) = \int_0^{\infty} e^{-t}t^{z-1}\, dt
 $$ 

This has the useful property that, for any $$n \in \mathbb{N}$$,

 $$ 
\Gamma(n) = (n-1)!
 $$ 

which has an easy proof by induction on $$n$$. it also has lots of nice analytical properties which make it a good choice for an extension of the factorial function.
Anyway, since the gamma function can be defined (after analytic continuation; see LVK's comment) on the entire complex plane, minus the non-positive integers, for a general $$z \in \mathbb{C} - \{ -1, -2, \cdots \}$$ we can put

 $$ 
z! \overset{\text{def}}{=} \Gamma(z+1)
 $$ 

For this reason we get

 $$ 
i! = \Gamma(i+1) = \int_0^{\infty} e^{-t}t^{i}\, dt \approx 0.498015668−0.154949828i
 $$ 

See also here and here.

