---
layout: post
title: When can you interchange composition of a limit
tag:
 - limits
 - continuity

description: When can you interchange composition of a limit

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

When can you interchange composition of a limit?

<!–-break-–>


we 've seen some limit problems where you can do this:

 $$ 

\lim_{x \to \infty} \exp\left({g(x)}\right) = \exp \left( \lim_{x \to \infty }g(x)\right) .

 $$ 

So, we 've tried to generalize the result as:

 $$ 

\lim_{x \to \infty} f(g(x)) = f \left( \lim_{x \to \infty }g(x) \right)

 $$ 

and we  was just wondering if the result above is actually true, and on what conditions? Perhaps someone can point me to a theorem.

# Answer 


Continuity turns out to be the right condition. As long as $$f$$ is continuous and the limit of $$g$$ exists at the point in question, then the limit will commute with composition. That is, for a given $$x$$ in the domain of $$g$$,

 $$ 
 \lim_{x\to t} f(g(x)) = f (\lim_{x\to t} g(x))
 $$ 

When dealing with values at infinity, technically you want the functions to be continuous on the extended real line ( either two point or one point compactifications). we n practice, that amounts to proving 

 $$ 
 \lim_{x\to \infty} g(x)
 $$ 
 exists. 

