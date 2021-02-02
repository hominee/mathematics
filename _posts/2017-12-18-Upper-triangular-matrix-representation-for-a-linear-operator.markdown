---
layout: post
title: Upper triangular matrix representation for a linear operator
tag:
 - linear-algebra

description: Upper triangular matrix representation for a linear operator

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Upper triangular matrix representation for a linear operator

<!–-break-–>


we just the read the proof that every linear operator over finite-dimensional complex vector space has an upper triangular matrix with respect to some basis of $$V$$ (pretty neat fact!).
 we are  using Linear Algebra Done Right by Sheldon Axler.
 My question is about the ending of the proof.
 Namely, $$Tv_k\in \textrm{span}(u_1, u_2, .
.
.
, u_m, v_k)$$ for every $$1\leq k\leq n$$.
 Correct? But the author just goes straight into saying that $$Tv_k\in \textrm{span}(u_1, u_2, .
.
.
, u_m, v_1, v_2, .
.
.
, v_k)$$.
 So my main question is:

Is my observation correct? 

If so, does this slightly stronger result leads to any useful fact? As far as we can tell, the matrix will have many more zeros in this case.
 
.


# Answer 


(we hate to ruin the mood --- but the pessimist's view of this theorem would be as follows.  The very fact that this theorem holds for all linear operators on finite dimensional complex vector spaces tells us that upper-triangularity is less of a "pretty neat fact" than we might have initially thought.)
Your observation is entirely correct.  
The author probably isn't highlighting it because, although formally it is stronger than what you would expect from upper-triangularity alone, there isn't much use for the stronger conclusion.  The problem with the stronger conclusion is that it occurs in the middle of an induction argument.  To see its effect on what it says about arbitrary operators on finite dimensional vector spaces, we have to consider what happens when we iterate the stronger conclusion, with a view toward coming up with a stronger statement about what the matrix of an arbitrary linear operator can be made to look like.  And if you think about this, the first thing you notice is that it's quite possible that, for a given $$T$$, the range of $$T - \lambda I$$ has dimension exactly one less than the space that $$T$$ acts on.  In this case, the "$$n$$" in the above argument is 1, and the "stronger" conclusion coincides with what you get from "upper triangular"...
To vaguely answer the question that you removed in this version of the question (asking whether there might be uses to putting more zeros in a matrix than "upper triangular" would assure you are there):
For theoretical purposes, generally it is not that useful to be able to have more zeros in a matrix, unless you have a lot more control over where those zeros are than this argument provides.  (In my experience, anything short of something that would give you a block decomposition, or something very close to it, is not going to be of much theoretical use.)  And there's a result that's far better than "upper triangular" in the complex case.  Later in Axler, he proves that if $$T$$ is an operator on a finite-dimensional complex vector space $$V$$, there is some basis of $$V$$ for which $$T$$ decomposes as a direct sum of Jordan blocks.  These matrices have tons more zeros in them than arbitrary upper triangular matrices do.  But for a lot of theoretical questions, the Jordan decomposition simply isn't that useful.  Again, the pessimist's view: if something is true of all linear operators on finite-dimensional complex vector spaces, it can't be that great, or all of linear algebra would be easier than we know it is.
For the purpose of numerical computations (on computers) with very large matrices, we think there is some advantage in having as many zeros in a matrix as possible.  But a proper evaluation of the numerical usefulness of the algorithm implicit in Axler's proof would require an analysis of the numerical cost of having to compute a basis for the range of an operator (known only numerically) at each step.  Once you take that into account, we don't know that this algorithm would have anything to recommend it over other algorithms (e.g. for approximating the Jordan form of a matrix given only numerically).

