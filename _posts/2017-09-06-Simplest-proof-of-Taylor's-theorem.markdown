---
layout: post
title: Simplest proof of Taylor's theorem
tag:
 - real-analysis
 - soft-question
 - taylor-expansion

description: Simplest proof of Taylor's theorem

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Simplest proof of Taylor's theorem

<!–-break-–>


we have for some time been trawling through the Internet looking for an aesthetic proof of Taylor's theorem.
By which we mean this: there are plenty of proofs that introduce some arbitrary construct: no mention is given of from whence this beast came.  and you can logically hack away line by line until the thing is solved. but this kind of proof is ugly.  a beautiful proof should rise naturally from the ground.
we have  seen one proof claiming to do it from the fundamental theorem of calculus. It looked messy.
we have  seen several attempts to use integration by parts repeatedly. But surely it would be tidier to do this without bringing in  all of that extra machinery.
The nicest two approaches seem to involve using the mean value theorem and Rolle's theorem.  but we can't find a lucid presentation of either approach.
Maybe my brain is unusually stupid, and the approaches on Wikipedia etc are perfectly good enough for everyone else. 
Does anyone have a crystal clear understanding of this phenomenon? Or a web-link to such an understanding?
*

**Edit***: Eventually a Cambridge mathematician explained it to me in a way that we could understand, and we have written up the proof here. To my mind it is the most instructional proof we have encountered, yet putting it as an answer received mostly downvotes. It seems strange to me that no one else seems to concur.  But it should be up to the keenest mathematical minds to choose which answer should be accepted. It shouldn't be up to me. Therefore we will bow to the wisdom of the community, and accept the currently most-upvoted answer. we have learned from Machine Learning that a "Committee of Experts" outperforms any one expert, and we are  certainly no expert.

# Answer 


Here is an approach that seems rather natural,
based on applying the fundamental theorem
of calculus successively to $$f(x)$$, $$f'(t_1)$$, $$f''(t_2)$$, etc.:
\begin{eqnarray*}
&& f(x)=f(a)+\int_a^x f'(t_1)\,dt_1
\\&&
= f(a)+ \int_a^x f'(a)\,dt_1 + \int_a^x \!\! \int_a^{t_1} f''(t_2)\,dt_2\,dt_1
\\&&
= f(a)+ \int_a^x f'(a)\,dt_1 + 
\int_a^x \!\! \int_a^{t_1}
 f''(a)
 \,dt_2\,dt_1
+\int_a^x 
\!\! \int_a^{t_1}
\!\! \int_a^{t_2}
f'''(t_3)
\,dt_3\,dt_2\,dt_1
\end{eqnarray*}
Notice that


$$


\int_a^x f'(a)\,dt_1=f'(a)\int_a^x dt_1=f'(a)(x-a),


$$



$$


\int_a^x \!\! \int_a^{t_1}
 f''(a)\,dt_2\,dt_1
 = f''(a)\int_a^x (t_1-a)\,dt_1 = f''(a)\frac{(x-a)^2}{2},
 

$$



$$


 \int_a^x 
\!\! \int_a^{t_1}
\!\! \int_a^{t_2}
f'''(a)\,dt_3\,dt_2\,dt_1
= f'''(a)\int_a^x \frac{(t_1-a)^2}{2}\,dt_1 = f'''(a)\frac{(x-a)^3}{3!},


$$


and in general


$$


 \int_a^x 
\!\! \int_a^{t_1}
\!\ldots \int_a^{t_{n-1}}
f^{(n)}(a)\,dt_n\ldots\,dt_2\,dt_1
= f^{(n)}(a)\frac{(x-a)^{n}}{n!}.


$$


By induction, then, one proves


$$


f(x) = P_n(x)+ R_n(x)


$$


where $$P_n$$ is the Taylor polynomial


$$


P_n(x) = f(a)+f'(a)(x-a)+f''(a)\frac{(x-a)^2}{2}+\ldots+ f^{(n)}(a) \frac{(x-a)^n}{n!},


$$


and the remainder $$R_n(x)$$ is represented by nested integrals as


$$

R_n (x) = 
 \int_a^x 
\!\! \int_a^{t_1}
\!\ldots \int_a^{t_{n}}
f^{(n+1)}(t_{n+1})
\,dt_{n+1}\ldots\,dt_2\,dt_1.


$$


We can establish the Lagrange form of the remainder by applying the intermediate 
and extreme value
theorems, using simple comparisons as follows.  Consider the case $$x>a$$ first. 
Let $$m$$ be the minimum value of $$f^{(n+1)}$$ on $$[a,x]$$, and $$M$$ the maximum value. 
Then since 


$$

 m\le f^{(n+1)}(t_{n+1}) \le M


$$


for all $$t_{n+1}$$ in $$[a,x]$$, after $$n+1$$ repeated integrations one finds


$$


m \frac{(x-a)^{n+1}}{(n+1)!} 
\le R_n(x) \le
M \frac{(x-a)^{n+1}}{(n+1)!}.


$$


But now, notice that the function 


$$


t\mapsto f^{(n+1)}(t) \frac{(x-a)^{n+1}}{(n+1)!} 


$$


attains the extreme values 


$$


m \frac{(x-a)^{n+1}}{(n+1)!} 
\quad\mbox{and} \quad 
M \frac{(x-a)^{n+1}}{(n+1)!}


$$


at some points in $$[a,x]$$. By the intermediate value theorem, there must be
some point $$t$$ between these two points (so $$t\in[a,x]$$) such that


$$


R_n(x) = f^{(n+1)}(t) \frac{(x-a)^{n+1}}{(n+1)!}.


$$


This is the Lagrange form of the remainder. 
If $$x<a$$ and $$n$$ is odd, the same proof works. If $$x<a$$ and $$n$$ is even,
$$(x-a)^{n+1}<0$$ and the same proof works after reversing some inequalities.
One can motivate this whole approach in a couple of different ways.
E.g., one can argue that 
$$
{(x-a)^n}/{n!}
$$
becomes small for large $$n$$, so the remainders $$R_n(x)$$ will become small
if the derivatives of $$f$$ stay bounded, say.  
Or, one can reason loosely as follows: $$f(x)\approx f(a)$$ for $$x$$ near $$a$$.
Ask, what is the remainder exactly? Apply the fundamental theorem as above, then 
approximate the first remainder using the approximation $$f'(t_1)\approx f'(a)$$. 
Repeating, one produces the Taylor polynomials by the pattern of the argument above.

