---
layout: post
title: Definition of the gamma function for non-integer negative values
tag:
 - gamma-function

description: Definition of the gamma function for non-integer negative values

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Definition of the gamma function for non-integer negative values

<!–-break-–>


The gamma function is defined as 

 $$ 
\Gamma(x)=\int_0^\infty t^{x-1}e^{-t}dt
 $$ 

for $$x>0$$.
Through integration by parts, it can be shown that for $$x>0$$,

 $$ 
\Gamma(x)=\frac{1}{x}\Gamma(x+1).
 $$ 

Now, my textbook says we can use this definition to define $$\Gamma(x)$$ for non-integer negative values. we  don't understand why. The latter definition was derived by assuming $$x>0$$. So shouldn't the whole definition not be valid for any $$x$$ value less than zero?
P.S. we  have read other mathematical sources and most of them explain things in mathematical terms that are beyond my level. we t would be appreciated if things could be kept in relatively simple terms.

# Answer 


The definition you gave is valid only for $$x >0$$, has you have pointed out. However, you can extend $$\Gamma$$ to negative non integer values by defining 

 $$ 
\Gamma(x) := \frac{1}{x}\Gamma(x+1) 
 $$ 

whenever $$x <0$$, $$x \notin \mathbb Z$$. For example you get

 $$ 
\Gamma\left(-\frac{1}{2}\right) = -2 \Gamma\left(\frac{1}{2}\right) 
 $$ 

and $$\Gamma\left(\frac{1}{2}\right)$$ is given by the integral you have presented.

