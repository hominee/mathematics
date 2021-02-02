---
layout: post
title: Problem related to real analysis
tag:
 - real-analysis

description: Problem related to real analysis

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Does $$f(n\theta) \to 0$$ for all $$\theta>0$$ and $$f$$ Darboux imply $$f(x) \to 0$$ as $$x \to \infty$$?

<!–-break-–>


Recall that a Darboux function $$f:\mathbb{R} \to \mathbb{R}$$ is one which satisfies the conclusion of the intermediate value theorem (i.e., connected sets are mapped to connected sets). Being Darboux is a weaker condition than continuity. if a theorem about continuous functions only uses the intermediate value theorem, then chances are it also holds for the entire class of Darboux functions. i  find it interesting to study which theorems about continuous functions also hold for Darboux functions. 
i have the following theorem, which is fairly well known and hinges on the Baire Categoery Theorem. 

if $$f:\mathbb{R} \to \mathbb{R}$$ is continuous and $$f(n\theta) \xrightarrow[n \in \mathbb{N}, \ n\to\infty]{} 0$$ for every $$\theta \in (0, \infty)$$, 

then

 $$
 f(x) \xrightarrow[x \in \mathbb{R}, \ \ x\to\infty]{} 0
 $$

A counterexample if i drop continuity is $$f(x) = \mathbf{1}_{\{ \exp(n) : n \in \mathbb{N}\}}$$. 

However, this counterexample isn't Darboux, and i  haven't been able to come up with any counterexample which is Darboux. Thus, this leads me to my question. 

Can the continuity condition in the theorem stated above be relaxed to Darboux? 

in searching for counterexamples of this sort, one approach is playing around with $$\sin \frac{1}{x}$$. An alternative approach is considering highly pathological functions with the property that every nonempty open set is mapped to $$\mathbb{R}$$ (for instance, Conway Base-13, or Brian's example here) and modifying these in such a way that they satisfy the hypotheses of the problem. 


# Answer 


Non-measurable example
By the axiom of choice there is a $$\mathbb Q$$-linear basis of $$\mathbb R.$$ This basis has the same cardinality as $$\mathbb R$$ so can be indexed as $$a_r$$ for $$r\in\mathbb R.$$ Define $$f$$ by setting $$f(x)=r$$ if $$x$$ is of the form $$a_0+qa_r$$ for some rational $$q$$ and real $$r,$$ and set $$f(x)=0$$ for $$x$$ not of this form. Then $$f$$ is Darboux because the set $$\{a_0+qa_r\mid q\in\mathbb Q\}$$ is dense for each $$r.$$ But for each $$\theta>0,$$ i can only have $$f(q\theta)\neq 0$$ for at most one rational $$q$$ - the reciprocal of the $$a_0$$ coefficient of $$\theta.$$ in particular $$f(n\theta)\to 0$$ as $$n\to\infty$$ with $$n\in\mathbb N.$$
Measurable example
For $$n\geq 2$$ let $$b_n=n!(n-1)!\dots 2!.$$ Each real has a unique "mixed radix" expression as

$$x=\lfloor x\rfloor + \sum_{n\geq 2}\frac{x_n}{b_n}$$ 

where $$x_n$$ is the unique representative of $$\lfloor b_n x\rfloor$$ modulo $$n!$$ lying in $$\{0,1,\dots,n!-1\}.$$ For non-negative $$x$$ define $$f(x)=\lim_{n\to\infty} \tfrac{1}{n}\sum_{m=2}^n x_m$$ if this limit exists and $$x_n\leq 1$$ for all sufficiently large $$n,$$ and take $$f(x)=0$$ otherwise. For negative $$x$$ define $$f(x)=f(-x).$$ Note $$f(x)\in[0,1].$$ it is straightforward to see that $$f$$ takes all values in $$[0,1]$$ in every interval and is hence Darboux.
Now consider a real $$x>0$$ with $$f(x)\neq 0$$ and let $$q<1$$ be rational. i will show that $$f(qx)=0.$$ i know there exists $$N$$ such that $$x_n\leq 1$$ for all $$n>N.$$ increasing $$N$$ if necessary i can assume that $$qN$$ is an integer. i also know that $$x_n=1$$ for infinitely many $$n>N$$ - otherwise i would have $$\lim_{n\to\infty} \tfrac{1}{n}\sum_{m=2}^n x_m=0.$$ 
Write 

$$x=x'/b_{n-1}+1/b_n+\epsilon/b_{n+1}$$ 

where $$x'$$ is an integer and $$0\leq\epsilon< 2.$$ 

So

 $$qx b_{n+1}=qx'n!(n+1)!+q(n+1)!+q\epsilon.$$ 
 
 The first term is a multiple of $$(n+1)!$$ because $$qn!$$ is an integer, and the second term $$q(n+1)!$$ is an integer, 
 and $$q\epsilon<2.$$ So $$(qx)_{n+1}$$ is either $$q(n+1)!$$ or $$q(n+1)!+1$$ (note this is less than $$(n+1)!$$). 
 Since $$q(n+1)!>1$$ and there are infinitely many such $$n,$$ i get $$f(qx)=0,$$ .

This shows that for each $$\theta>0,$$ the sequence $$f(n\theta)$$ takes at most one non-zero value, and in particular $$f(n\theta)\to 0.$$
Remark: this $$f$$ appears to be a counterexample to [https://arxiv.org/abs/1003.4673](https://arxiv.org/abs/1003.4673) Theorem 4.1.

