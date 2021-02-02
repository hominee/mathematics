---
layout: post
title: 1 to the power of infinity, why is it indeterminate [duplicate]
tag:
 - limits
 - infinity
 - exponentiation

description: 1 to the power of infinity, why is it indeterminate [duplicate]

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

1 to the power of infinity, why is it indeterminate? [duplicate]

<!–-break-–>



This question already has an answer here:


Why is $$1^{\infty}$$ considered to be an indeterminate form

                    8 answers
                



we 've been taught that $$1^\infty$$ is undetermined case. Why is it so? we sn't $$1*1*1...=1$$ whatever times you would multiply it? So if you take a limit, say $$\lim_{n\to\infty} 1^n$$, doesn't it converge to 1? So why would the limit not exist?
.

# Answer 


we t isn’t: $$\lim_{n\to\infty}1^n=1$$, exactly as you suggest. However, if $$f$$ and $$g$$ are functions such that $$\lim_{n\to\infty}f(n)=1$$ and $$\lim_{n\to\infty}g(n)=\infty$$, it is not necessarily true that

 $$ 
\lim_{n\to\infty}f(n)^{g(n)}=1\;.\tag{1}
 $$ 

For example, 
 $$ 
\lim_{n\to\infty}\left(1+\frac1n\right)^n=e\approx2.718281828459045\;.
 $$ 

More generally,

 $$ 
\lim_{n\to\infty}\left(1+\frac1n\right)^{an}=e^a\;,
 $$ 

and as $$a$$ ranges over all real numbers, $$e^a$$ ranges over all positive real numbers. Finally,

 $$ 
\lim_{n\to\infty}\left(1+\frac1n\right)^{n^2}=\infty\;,
 $$ 

and

 $$ 
\lim_{n\to\infty}\left(1+\frac1n\right)^{\sqrt n}=0\;,
 $$ 

so a limit of the form $$(1)$$ always has to be evaluated on its own merits; the limits of $$f$$ and $$g$$ don’t by themselves determine its value.

