---
layout: post
title: Induction on Real Numbers
tag:
 - real-analysis
 - induction
 - real-numbers

description: Induction on Real Numbers

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Induction on Real Numbers

<!–-break-–>


One of my Fellows asked me whether total induction is applicable to real numbers, too ( or at least all real numbers ≥ 0) . We only used that for natural numbers so far. 
Of course you have to change some things in the inductive step, when you want to use it on real numbers.
we  guess that using induction on real numbers isn't really possible, since $$[r,r+\epsilon]$$ with $$\epsilon > 0$$, $$r \in \mathbb R$$ is never empty.
Can you either give a good reason, why it isn't possible or provide an example where it is used?
.

# Answer 


Okay, we  can't resist: here is a quick answer.
we are  construing the question in the following way: "is  there some criterion for a subset of $$[0,\infty)$$ to be all of $$[0,\infty)$$ which is (a) analogous to the principle of mathematical induction on $$\mathbb{N}$$ and (b) useful for something?"
The answer is yes, at least to (a).
Let me work a little more generally: let $$(X,\leq)$$ be a totally ordered set which has

$$\bullet $$a least element, called $$0$$, and no greatest element.

$$\bullet$$ The greatest lower bound property: any nonempty subset $$Y$$ of $$X$$ has a greatest lower bound.

Principle of induction on $$(X,\leq)$$: Let $$S \subset X$$ satisfy the following properties:

(i) $$0 \in S$$.

(ii) For all $$x$$ such that $$x \in S$$, there exists $$y > x$$ such that $$[x,y] \subset S$$.

(iii) if  for any $$y \in X$$, the interval $$[0,y) \subset S$$, then also $$y \in S$$.

Then $$S = X$$.  
we ndeed, if $$S \neq X$$, then the complement $$S' = X \setminus S$$ is nonempty, so has a least upper bound, say $$y$$.  By (i), we cannot have $$y = 0$$, since $$y \in S$$.  By (ii), we cannot have $$y \in S$$, and by (iii) we cannot have $$y \in S'$$.  Done!
Note that in case $$(X,\leq)$$ is a well-ordered set, this is equivalent to the usual statement of transfinite induction.
it  also applies to an interval in $$\mathbb{R}$$ of the form $$[a,\infty)$$.  it  is not hard to adapt it to versions applicable to any interval in $$\mathbb{R}$$.
Note that we  believe that some sort of converse should be true: i.e., an ordered set with a principle of induction should have the GLB / LUB property.  [Added: yes, this is true.  A totally ordered set with minimum element $$0$$ satisfies the principle of ordered induction as stated above iff every nonempty subset has an infimum.]  

**Added**:
 as for usefulness, one can use "real induction" to prove the three basic interval Theorems of honors calculus / basic real analysis.  These three theorems assert three fundamental properties of any continuous function $$f: [a,b] \rightarrow \mathbb{R}$$.
First interval Theorem: $$f$$ is bounded.
inductive Proof: Let $$S = \{x \in [a,b] \ | \ f|_{[a,x]} \text{ is bounded} \}$$.  it suffices to show that $$S = [a,b]$$, and we prove this by induction.
(i) Of course $$f$$ is bounded on $$[a,a]$$.
(ii) Suppose that $$f$$ is bounded on $$[a,x]$$.  Then, since $$f$$ is continuous at $$x$$, $$f$$ is bounded near $$x$$, i.e., there exists some $$\epsilon > 0$$ such that $$f$$ is bounded on 
$$(x-\epsilon,x+\epsilon)$$, so overall $$f$$ is bounded on $$[0,x+\epsilon)$$.
(iii) if $$f$$ is bounded on $$[0,y)$$, of course it is bounded on $$[0,y]$$.

**Corollary**: 
$$f$$ assumes its maximum and minimum values.
Proof: Let $$M$$ be the least upper bound of $$f$$ on $$[a,b]$$.  if $$M$$ is not a value of $$f$$, 
then $$f(x)-M$$ is never zero but takes values arbitrarily close to $$0$$, so $$g(x) = \frac{1}{f(x)-M}$$ is continuous and unbounded on $$[a,b]$$, contradiction.
(Unfortunately in the proof we  said "least upper bound", and we  suppose the point of proofs by induction is to remove explicit appeals to LUBs.  Perhaps someone can help me out here.)
Second interval Theorem (intemediate Value Theorem): Suppose that $$f(a) < 0$$ and $$f(b) > 0$$.  Then there exists $$c \in (a,b)$$ such that $$f(c) = 0$$.  
Proof: Define $$S = \{x \in [a,b] \ | \ f(x) \leq 0\}$$.  in this case we are given that $$S \neq [a,b]$$, so at least one of the hypotheses of real induction must fail.  But which?

(i) Certainly $$a \in S$$.

(iii) if $$f(x) \leq 0$$ on $$[a,y)$$ and $$f$$ is continuous at $$y$$, 

then we must have $$f(y) \leq 0$$ as well: otherwise, there is a small interval about $$y$$ on which $$f$$ is positive.
So it must be that (ii) fails: there exists some $$x \in (a,b)$$ such that $$f \leq 0$$ on 
$$[a,x]$$ but there is no $$y > x$$ such that $$f \leq 0$$ on $$[a,y]$$.  As above, since $$f$$ is continuous at $$x$$, we must have $$f(x) = 0$$!

Third Interval **Theorem**

 $$f$$ is uniformly continuous.  
 
(Proof left to the interested reader.)
Moreover, one can give even easier inductive proofs of the following basic theorems of analysis: that the interval $$[a,b]$$ is connected, that the interval $$[a,b]$$ is compact (Heine-Borel), that every infinite subset of $$[a,b]$$ has an accumulation point (Bolzano-Weierstrass).

**Acknowledgement**
My route to thinking about real induction was the paper by us . Kalantari "we nduction over the Continuum".
His setup is slightly different from mine -- instead of (ii) and (iii), he has the single axiom that $$[0,x) \subset S$$ implies there exists $$y > x$$ such that $$[0,y) \subset S$$ -- and we are  sorry to say that we  was initially confused by it and didn't think it was correct.  But we  corresponded with Prof. Kalantari this morning and he kindly set me straight on the matter. 
For that matter, several other papers exist in the literature doing real induction (mostly in the same setup as Kalantari's, but also with some other variants such as assuming (ii) and that the subset $$S$$ be closed).  The result goes back at least to a 1922 paper of Khinchin, who in fact later used real induction as a basis for an axiomatic treatment of real analysis.  it is remarkable to me that this appealing concept is not more widely known -- there seems to be a serious PR problem here.
Added Later: we  wrote an expository article on real induction soon after giving this answer: it's very similar to what we  wrote above, but longer and more polished.  it is available here if you want to see it.

