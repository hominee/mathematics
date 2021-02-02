---
layout: post
title: Why is 1 raised to infinity Not defined and not 1
tag:
 - soft-question
 - education
 - exponentiation

description: Why is 1 raised to infinity Not defined and not 1

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Why is 1 raised to infinity Not defined and not 1

<!–-break-–>


Why is $$1^{\infty}$$ considered to be an indeterminate form

$$1$$ square is $$1$$, so is raised $$1$$ to $$123434234$$.
My maths teacher claims that $$1$$ raised to infinity is not $$1$$, but not defined. is there any reason for this?
we  know that any number raised to infinity is not defined, but shouldn't $$1$$ be an exception?
.

# Answer 


What $$1^\infty$$ is, or is not, is merely a matter of definition. Normally, one would only define $$a^b$$ for some specific class of pairs of $$a,b$$ - say $$b$$ - positive integer, $$a$$ - real number. 
When extending the definition of exponentiation to more general pairs, the key thing people keep in mind is that various nice properties are preserved. For instance, for $$ b$$ - positive integer, you want to put $$a^{-b} = \frac{1}{a^b}$$ so that the rule $$a^ba^c = a^{b+c}$$ is preserved.
it may make sense in some context to speak of infinities in the context of limits, but this is usually more a rule of thumb than rigorous mathematics. This may be seen as extending the rule that $$(a,b) \mapsto a^b$$ is continuous (i.e. if $$\lim_n a_n = a$$ and $$\lim_n b_n = b$$, then $$\lim_n a_n^{b_n} = a^b$$) to allow for $$b_n \to \infty$$. For instance, you may risk saying that:

 $$ 
\lim_{n} (2+\frac{1}{n})^n = 2^{\infty} = \infty
 $$ 
 
if you agree to use rules of this kind, you might be tempted to also say: 

 $$ 
\lim_{n} (1+\frac{1}{n})^n = 1^{\infty} = 1
 $$ 

 but this would lead you astray, since in reality: 

 $$ 
\lim_{n} (1+\frac{1}{n})^n = e \neq 1
 $$ 

Thus, it is safer to leave $$1^\infty$$ undefined.

A more thorough discussion can be found on Wikipedia.

