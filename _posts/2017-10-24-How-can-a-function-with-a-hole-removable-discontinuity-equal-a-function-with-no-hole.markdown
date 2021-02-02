---
layout: post
title: How can a function with a hole (removable discontinuity) equal a function with no hole
tag:
 - calculus
 - limits
 - discontinuous-functions
 - faq

description: How can a function with a hole (removable discontinuity) equal a function with no hole

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

How can a function with a hole (removable discontinuity) equal a function with no hole?

<!–-break-–>


we have  done some research, and we are  hoping someone can check me.
 My question was this:
Assume we have the function $$f(x) = \frac{(x-3)(x+2)}{(x-3)}$$, so it has removable discontinuity at $$x = 3$$.
 We remove that discontinuity with algebra: $$f(x) = \frac{(x-3)(x+2)}{(x-3)} = (x+2)$$.
 BUT, the graph of the first function has a hole at $$x = 3$$, and the graph of the second function is continuous everywhere.
 How can they be "equal" if one has a hole and the other does not?
we think that this is the answer: 
Because the original function is undefined at the point $$x = 3$$, we have to restrict the domain to $$\mathbb{R} \setminus 3$$.
 And when we manipulate that function with algebra, the final result, $$f(x) = (x +2)$$ is still using this restricted domain.
 
 So even though the function $$f(x) = (x+2)$$ would not have a hole if the domain were all of $$\mathbb{R}$$, we are sort of "imposing" a hole at $$x = 3$$ by continuing to throw that point out of the domain.
 
 But the reality is that the function $$f(x) = (x +2)$$ is actually NOT continuous everywhere when we restrict the domain by throwing out the point 3.


# Answer 


Two functions are typically defined to be equal if and only if they...

Share the same domain
Share the same codomain
Take on the same values for each input.

Thus, functions $$f,g : S \to T$$ for sets $$S,T$$ have $$f=g$$ if and only if $$f(x) = g(x)$$ for all $$x$$ in $$S$$.
For functions with holes, we typically restrict the domain by ensuring the values where the function is not defined at not included. For example, in the functions you have, you have


$$

f(x) = \frac{(x-3)(x+2)}{(x-3)} \;\;\;\;\; g(x) = x+2

$$


Are these equal? Yes, and no.
A function must be defined at all values of the domain. Thus, we can say $$3$$ is not in the domain of $$f$$ for sure. But we never specified otherwise the domains and codomains of these functions! Typically, unless stated otherwise, we often assume their domain to be $$\Bbb R$$ or $$\Bbb C$$, minus whatever points are causing problems - and of course, in such cases, $$f \neq g$$ since $$f(3)$$ is not defined, and thus $$f$$ normally has domain $$\Bbb R \setminus \{3\}$$ and $$g$$ generally has domain $$\Bbb R$$.
But that restriction is not necessary. For example, we could define the functions to be $$f,g : \Bbb R \setminus \Bbb Q \to \Bbb R$$. Notice that the domain of both functions are now all real numbers except rational numbers, i.e. the irrational numbers. This means $$3$$ is not in the domain of either function - and since that's the only "trouble spot," and the codomains are equal, and the values are equal at each point in the domain, $$f=g$$ here.
Or even more simply: we could have $$\Bbb R \setminus \{3\}$$ be the domain of $$f$$ and $$g$$ and again have equality! The key point in all this is that, just because $$f$$ or $$g$$ do attain defined values for certain inputs, doesn't mean they have to be in the domain.

In short, whether $$f=g$$ depends on your definitions of each. Under typical assumptions, $$f \neq g$$ in this case, but if we deviate from those assumptions even a little we don't necessarily have inequality. 

