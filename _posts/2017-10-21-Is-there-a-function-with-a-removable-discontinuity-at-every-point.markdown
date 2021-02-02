---
layout: post
title: Is there a function with a removable discontinuity at every point
tag:
 - calculus
 - real-analysis

description: Is there a function with a removable discontinuity at every point

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Is there a function with a removable discontinuity at every point?

<!–-break-–>


If memory serves, ten years ago to the week (or so), we taught first semester freshman calculus for the first time.
  As many calculus instructors do, we decided we should ask some extra credit questions to get students to think more deeply about the material.
  The first one we asked was this:
1) Recall that a function $$f: \mathbb{R} \rightarrow \mathbb{R}$$ is said to have a removable discontinuity at a point $$x_0 \in \mathbb{R}$$ if $$\lim_{x \rightarrow x_0} f(x)$$ exists but not does not equal $$f(x_0)$$.
  Does there exist a function $$f$$ which has a removable discontinuity at $$x_0$$ for every $$x_0 \in \mathbb{R}$$?
Commentary: if so, we could define a new function $$\tilde{f}(x_0) = \lim_{x \rightarrow x_0} f(x)$$ and it seems at least that $$\tilde{f}$$ has a fighting chance to be continuous on $$\mathbb{R}$$.
  Thus we have successfully "removed the discontinuities" of $$f$$, but in so doing we have changed the value at every point!  

  **Remark**: Lest you think this is too silly to even seriously contemplate, consider the function $$f: \mathbb{Q} \rightarrow \mathbb{Q}$$ given by $$f(0) = 1$$ and for a nonzero 
rational number $$\frac{p}{q}$$, $$f(\frac{p}{q}) = \frac{1}{q}$$.
 
 It is easy to see that this function has limit $$0$$ at every (rational) point!
So we mentioned this problem to my students.
 
 A week later, the only person who asked me about it at all was my Teaching Assistant, who was an older undergraduate, not even a math major, we think.
  (we hasten to add that this was not in any sense an honors calculus class, i.e, we was pretty clueless back then.
)  Thinking about it a bit, we asked him if he knew about uncountable sets, and he said that he didn't.
 
 At that point we realized that we didn't have a solution in mind that he would understand (so still less so for the freshman calculus students) and we advised him to forget all about it.


So my actual question is: can you solve this problem using only the concepts in a non-honors freshman calculus textbook?  (In particular, without using notions of un/countability?)

[**Addendum**: Let me say explicitly that we would welcome an answer that proceeds directly in terms of the least upper bound axiom.
  Most freshman calculus books do include this, albeit somewhere hidden from view of the casual readers, i.e. , actual freshman calculus students.

2) Define a function $$f: \mathbb{R} \rightarrow \mathbb{R}$$ to be precontinuous if the limit exists at every point.
  For such a function, we can define $$\tilde{f}$$ as above.
  Prove/disprove that, as suggested above, $$\tilde{f}$$ is indeed continuous.
  [Then think about $$f - \tilde{f}$$.]
  
Now that we think about it, there is an entire little area here that we don't know anything about, e.g.

3) The set of discontinuities of an arbitrary function is known -- any $$F_{\sigma}$$ set inside $$\mathbb{R}$$ can serve.
  What can we say about the set of discontinuities of a "precontinuous function"?  [

**Edit**: from the link provided in Chandru1's answer, we see that it is countable.
  What else can we say?  

**Note** that taking the above example and extending by $$0$$ to the irrationals, we see that the set of points of discontinuity of a precontinuous function can be dense.
]



# Answer 


we think the following works:

Here is a sketch, we will fill in the details later if required.
Let $$g(x) = \lim_{t\rightarrow x} f(t)$$. Then we can show that $$g(x)$$ is continuous.
Let $$h(x) = f(x) - g(x)$$. Then $$\lim_{t \rightarrow x} h(t)$$ exists and is $$0$$ everywhere.
We will now show that $$h(c) = 0$$ for some $$c$$. 

This will imply that $$f(x)$$ is continuous at $$c$$ as then we will have $$f(c) = g(c) = \lim_{t->c} f(t)$$.
Consider any point $$x_0$$.

By limit of $$h$$ at $$x_0$$ being $$0$$, there is a closed interval $$I_0$$ (of length > 0) such that $$\|h(x)\| < 1$$ for all $$x \in I_0$$.
This is because, given an $$\epsilon > 0$$ there is a $$\delta > 0$$ such that $$\|h(x)\| < \epsilon$$ for all $$x$$ such that $$0 < \|x - x_{0}\| < \delta$$. Pick $$\epsilon = 1$$ and pick $$I_{0}$$ to be any closed interval of non-zero length in $$(x_{0}, x_{0} + \delta)$$.
Now pick any point $$x_1$$ in $$I_0$$.

By limit of $$h$$ at $$x_1$$ being $$0$$, there is a closed interval $$I_1 \subset I_0$$ (of length > 0) such that $$\|h(x)\| < 1/2$$ for all $$x \in I_1$$, by argument similar to above.
Continuing this way, we get a sequence of closed intervals $$I_n$$ such that

$$\|h(x)\| < \frac{1}{n+1}$$ for all $$x \in I_n$$. We also have that $$I_{n+1} \subset I_n$$ for each $$n$$, and that length $$I_n$$ > 0. We could also arrange so that length $$I_n \rightarrow 0$$.
Now there is a point $$c$$ (by completeness of $$\mathbb{R}$$) such that $$c \in \bigcap_{n=0}^{\infty}I_{n}$$.

Thus we have that $$\|h(c)\| < \frac{1}{n+1}$$ for all $$n$$ and so $$h(c) = 0$$ and $$f(c) = g(c)$$.

