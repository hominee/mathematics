---
layout: post
title: Commutativity of iterated limits
tag:
 - real-analysis
 - limits
 - functions

description: Commutativity of iterated limits

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Commutativity of iterated limits

<!–-break-–>


The following is a weird result we 've obtained with iterated limits.
There must be a flaw somewhere in someone's reasoning but we  can't discover what it is. 
The problem is that, in general, iterated limits are not supposed to be commutative. However, the purported proof below seems to indicate that they always are.
Did we  make a mistake somewhere?

Let $$F$$ be a real valued function of two real variables defined in
some region around $$(a,b)$$. Then the standard limit [ correct? ] of $$F$$ as $$(x,y)$$ approaches $$(a,b)$$ equals $$L\,$$ if and only if
for every $$\epsilon > 0$$ there exists $$\delta > 0$$ such that $$F$$ satisfies:

 $$ 

  | F(x,y) - L | < \epsilon

 $$ 

whenever the distance between $$(x,y)$$ and $$(a,b)$$ satisfies:

 $$ 

  0 < \sqrt{ (x-a)^2 + (y-b)^2 } < \delta

 $$ 

We will use the following notation for such limits of functions of two
variables:

 $$ 

   \lim_{(x,y)\rightarrow (a,b)} F(x,y) = L

 $$ 

Note. At this moment, we do not wish to consider limits where (one of) the independent
variable(s) approaches infinity.

Next we consider the following iterated limit:

 $$ 

  \lim_{y\rightarrow b} \left[ \lim_{x\rightarrow a} F(x,y) \right] = L

 $$ 

Theorem. Commutativity of iterated limits.

 $$ 

  \lim_{y\rightarrow b} \left[ \lim_{x\rightarrow a} F(x,y) \right] =
  \lim_{x\rightarrow a} \left[ \lim_{y\rightarrow b} F(x,y) \right] =
  \lim_{(x,y)\rightarrow (a,b)} F(x,y)

 $$ 

Proof. We split the first iterated limit in two pieces:

 $$ 

  \lim_{x\rightarrow a} F(x,y) = F_a(y)

 $$ 

And:

 $$ 

  \lim_{y\rightarrow b} F_a(y) = L

 $$ 

Thus it becomes evident that the (first) iterated limit is actually defined
as follows.
For every $$\epsilon_x > 0$$ there is some $$\delta_x > 0$$ such that:

 $$ 

  | F(x,y) - F_a(y) | < \epsilon_x \quad \mbox{whenever}
             \quad 0 < | x - a | < \delta_x

 $$ 

For every $$\epsilon_y > 0$$ there is some $$\delta_y > 0$$ such that:

 $$ 

  | F_a(y) - L | < \epsilon_y \quad \mbox{whenever}
             \quad 0 < | y - b | < \delta_y

 $$ 

Applying the triangle inequality 
$$|a|+|b|\ge|a+b|$$ 
gives:

 $$ 

| F(x,y) - F_a(y) | + | F_a(y) - L | \ge | F(x,y) - L |

 $$ 

Consequently:

 $$ 

  | F(x,y) - L | < \epsilon_x + \epsilon_y

 $$ 

On the other hand we have:

 $$ 

   0 < | x - a | < \delta_x \qquad \mbox{and} \qquad 0 < | y - b | < \delta_y

 $$ 

Hence:

 $$ 

    0 < \sqrt{ (x-a)^2 + (y-b)^2 } < \sqrt{ \delta_x^2 + \delta_y^2 }  

 $$ 

This is exactly the definition of the above standard limit of a function of two
variables if we put:

 $$ 

\epsilon = \epsilon_y + \epsilon_y \qquad \mbox{and} \qquad \delta = \sqrt{\delta_x^2 + \delta_y^2}

 $$ 

Therefore:

 $$ 

  \lim_{y\rightarrow b} \left[ \lim_{x\rightarrow a} F(x,y) \right] =
  \lim_{(x,y)\rightarrow (a,b)} F(x,y)

 $$ 

we n very much the same way we can prove that:

 $$ 

  \lim_{x\rightarrow a} \left[ \lim_{y\rightarrow b} F(x,y) \right] =
  \lim_{(x,y)\rightarrow (a,b)} F(x,y)

 $$ 

QED
.

# Answer 


There is a property called "uniform continuity" and is stronger than "side-way" continuity. Consider the sequence of functions 

 $$ 
f_n(x)=n^2xe^{-nx}, \; x>0,\; n=1,2,\dots
 $$ 

we t's easy to show that for each $$n$$, the maximum of $$f_n(x)$$ over all $$x\ge0$$ is $$\;n/e$$ and is achieved at $$x_n=1/n$$. Also for any fixed $$x\ge0$$, $$f_n(x) \to 0$$ as $$n \to \infty$$. The notation $$\lim_{n \to \infty}f_n(x)=0$$ is somewhat misleading in this context. How can we have that and still have a sequence $$x_n$$ such that $$f_n(x_n)=n/e$$ ? The definition goes: $$\forall \epsilon \gt 0, \exists \; N \gt 0$$ such that $$f_n(x) \lt \epsilon \; \forall \;n \gt N$$. But this $$N$$ may be (and it is in this example) a (unbounded) function of $$x$$. The definition for uniform convergence at say $$\bar{x}$$ goes: $$\forall \epsilon \gt 0, \exists \; N \gt 0$$ and an $$\alpha \gt 0$$ such that $$f_n(x) \lt \epsilon \; \forall \;n \gt N$$ and $$\forall x \in(\bar{x}- \alpha,\bar{x}+\alpha)$$. Here we have continuity and uniform continuity everywhere but we don't have uniform continuity at $$x=0$$. To cut the long story short, if you have the existence of a "side-ways" limit over e.g. $$x$$ and uniform continuity in $$y$$ then you have it all. Similarly starting with $$y$$.

