---
layout: post
title: Lebesgue Measure - positive measure sets not containing intervals
tag:
 - measure-theory
 - lebesgue-measure

description: Lebesgue Measure - positive measure sets not containing intervals

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Lebesgue Measure - positive measure sets not containing intervals

<!–-break-–>


we have  encountered two statements regarding the Lebesgue measure that don't exactly contradict each other, but seem to me to be a little bit unintuitive when regarded with respect to one another.
The statements are:


For each interval $$[a,b]$$
  there exists a set $$K\subset[a,b]$$
  that is compact , totally disconnected and with positive measure (i.e. doesn't contain an interval).
Let $$A\subset\mathbb{R}$$
  be some measurable set, and $$0\leq\alpha<1$$
  such that for every interval $$I\subset\mathbb{R}$$
  it holds that $$m(A\cap I)\leq\alpha m(I)$$
  then $$m(A)=0$$


The second statement seems to imply that any positive measure set must contain an interval up to a set of arbitrary measure $$\epsilon>0$$ (since a suitable $$\alpha$$ can't be found for a positive measure set).
On the other hand the first statement says that for any interval we can find a subset of any desired positive "not-full" measure.
we realize these statements don't contradict, but they seem a little "contradictory in nature". Intuitively we would expect the first statement to somehow allow me to  construct a positive measure set with the property desired in the second statement.
we don't really have a question here but was hoping maybe someone can shed their own perspective on how they see these two properties of the Lebesgue measure co-existing. Maybe you can give me some further intuition. 
Thanks a lot!
.

# Answer 


My reaction is just to trace through some examples. The set $$K$$ in part $$1$$ is something like a Cantor set-just fattened up to maintain positive measure, say for concreteness $$1/2$$. While we're simplifying, may as well take $$[a,b]=[0,1]$$ as well. $$K$$ needn't be uniformly distributed-indeed the point of your part 2 is that it can't be-so we may suppose we can remove some interval and increase the proportional measure of $$K$$. In the most usual construction, we might have $$m(K\cap [0,3/8])=1/2$$. Then if $$K$$ is self-symmetrical, as it may certainly be, we immediately get arbitrarily large proportions of $$K$$ in sufficiently small intervals. 
This is all in contrast to the case of the usual Cantor set $$C$$: one way to prove $$m(C)=0$$ is to observe that for every interval $$I$$, $$C$$ is contained in a subset of $$I$$ of relative measure no more than $$2/3$$. For the construction of $$C$$ is uniform: at every stage we remove intervals of relative measure $$2/3$$. In contrast again this shows why we don't construct $$K$$ by uniform removal of even very small intervals.

