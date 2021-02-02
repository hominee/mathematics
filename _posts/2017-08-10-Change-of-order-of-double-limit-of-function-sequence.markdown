---
layout: post
title: Change of order of double limit of function sequence
tag:
 - real-analysis
 - sequences-and-series
 - functions
 - limits

description: Change of order of double limit of function sequence

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Change of order of double limit of function sequence

<!–-break-–>


The more general quesion is under what conditions the folloing equality will hold (all functions are real valued):

 $$ 
\lim_{x \rightarrow a} \ \lim_{j \rightarrow \infty} f_j(x) = \lim_{j \rightarrow \infty} \ \lim_{x \rightarrow a} f_j(x)
 $$ 

A more specific question is if it will hold for non-continuous functions $$f_j$$ that are uniformly convergent to a non-continuous limit function $$f$$ and all the single and iterated double limits exist.
Also some references would be useful.

# Answer 


The answer to the specific question is Yes.
Since $$f_j$$ converges (uniformly and hence) pointwise to $$f$$,

 $$ 

\mathop {\lim }\limits_{x \to a} \mathop {\lim }\limits_{j \to \infty } f_j (x) = \mathop {\lim }\limits_{x \to a} f(x).

 $$ 

For any $$\varepsilon > 0$$, since $$f_j$$ converges uniformly to $$f$$, there exists $$N = N(\varepsilon)$$ such that

 $$ 

\sup _x |f_j (x) - f(x)| < \varepsilon 

 $$ 

for any $$j > N$$. We assume that all limits exist. Hence, for any $$j > N$$,

 $$ 

|\lim _{x \to a} f_j (x) - \lim _{x \to a} f(x)| = |\lim _{x \to a} (f_j (x) - f(x))| \le \varepsilon .

 $$ 

Define $$p_j = \lim _{x \to a} f_j (x)$$ and $$p = \lim _{x \to a} f(x)$$. Then,

 $$ 

|\lim _{j \to \infty } p_j  - p| = \lim _{j \to \infty } |p_j  - p| \le \varepsilon ,

 $$ 

since $$|p_j - p| \leq \varepsilon$$ for any $$j > N$$. Since $$\varepsilon$$ is arbitrary, $$
\lim _{j \to \infty } p_j  = p$$, hence

 $$ 

\mathop {\lim }\limits_{j \to \infty } \mathop {\lim }\limits_{x \to a} f_j (x) = \mathop {\lim }\limits_{x \to a} f(x) = \mathop {\lim }\limits_{x \to a} \mathop {\lim }\limits_{j \to \infty } f_j (x).

 $$ 


