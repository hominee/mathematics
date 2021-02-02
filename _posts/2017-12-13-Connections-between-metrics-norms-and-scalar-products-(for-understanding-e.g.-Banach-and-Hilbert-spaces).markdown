---
layout: post
title: Connections between metrics, norms and scalar products (for understanding e.g. Banach and Hilbert spaces)
tag:
 - functional-analysis
 - vector-spaces
 - banach-spaces
 - hilbert-spaces
 - inner-product-space

description: Connections between metrics, norms and scalar products (for understanding e.g. Banach and Hilbert spaces)

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Connections between metrics, norms and scalar products (for understanding e.g. Banach and Hilbert spaces)

<!–-break-–>


we are  trying to understand the differences between 


$$


\begin{array}{\|l\|l\|l\|}
\textbf{vector space} & \textbf{general} & \textbf{+ completeness}\\\hline
\text{metric}& \text{metric space} & \text{complete space}\\
\text{norm} & \text{normed} & \text{Banach space}\\
\text{scalar product} & \text{pre-Hilbert space}  & \text{Hilbert space}\\\hline
\end{array}


$$


What we don't understand are the differences and connections between metric, norm and scalar product.
 Obviously, there is some kind of hierarchy but we don't get the full picture.


# Answer 


It seems to me that you've got the things quite right. we restrict attention to real or complex vector spaces. (

**Edit**: But see the update.)

Given a scalar product $$\langle \cdot, \cdot\rangle$$ we get a norm by setting $$\|x\| = \sqrt{\langle x,x \rangle}$$ by an application of the Cauchy-Schwarz inequality.
Conversely, a normed vector space structure comes from a pre-Hilbert space structure (as described in 1.) if and only if the norm satisfies the parallelogram law 

$$

2\|x\|^2 + 2\|y\|^2 = \|x-y\|^2 + \|x+y\|^2.

$$

 See Arturo's answer to this question  for an outline of the proof of the non-trivial direction (the trivial direction is just an exercise in expanding the scalar product). 

**Update**: we added a detailed solution to that same thread.
Given a norm on a vector space, we get a metric by putting $$d(x,y) = \|x - y\|$$.

This answers your question about the hierarchy as follows: We have inclusions



$$


\begin{array}{ccccc}
\\{\text{Pre-Hilbert spaces}\\} &\subset &\\{\text{normed spaces}\\} & \subset & \\{\text{metric vector spaces}\\}\\\
 \cup & & \cup & & \cup \\\
\\{\text{Hilbert spaces}\\} & \subset & \\{\text{Banach spaces}\\} & \subset & \\{\text{Complete metric vector spaces}\\}\end{array}


$$



where the second row is obtained from the first row by adding the purely metric property of completeness.
Now let me discuss the fact that these inclusions are in fact strict. Let me start with the second row.

The first observation we wish to make is that for $$1 \leq p \lt \infty$$ and an arbitrary positive integer $$n$$ the space $$\mathbb{R}^{n}$$ or $$\mathbb{C}^{n}$$ with the $$\ell^{p}$$-norm


$$

\Vert x \Vert_{p} = \Vert(x_{1},\ldots,x_{n})\Vert_{p} = \left(\sum_{k=1}^{n} \|x_{k}\|^{p}\right)^{1/p}

$$


is a Banach space. It is a Hilbert space if and only if $$p = 2$$ (or $$n = 1$$ where all $$\ell^p$$-norms coincide). If $$n \geq 2$$ and $$p \neq 2$$ the parallelogram law mentioned above fails: Take $$x = (1,0,\ldots,0)$$ and $$y = (0,\ldots,0,1)$$, then $$\Vert x\Vert_{p} = 1 = \Vert y\Vert_{p}$$ while $$\Vert x-y\Vert_{p} = 2^{1/p} = \Vert x + y\Vert_p$$, so we get


$$

4 = 2\Vert x\Vert_{p}^2 + 2\Vert y\Vert_{p}^{2} \neq \Vert x - y \Vert_{p}^2 + \Vert x + y \Vert_{p}^2 = 2 \cdot 2^{2/p}

$$


since $$p \neq 2$$. So we have already plenty of examples of Banach spaces that are not Hilbert spaces.
The space $$\mathbb{R}$$ with the metric $$d(x,y) = \dfrac{\|x-y\|}{1+\|x-y\|}$$ is a complete metric vector space (an illuminating exercise we urge you to do!), but clearly $$d(0,x)$$ does not define a norm (as claimed in another "answer"), since $$d(0,\lambda x) \neq \|\lambda\| d(0,x)$$ in general.

So far for the rather easy stuff.
Now let me discuss another example. Let $$\mathcal{P}([0,1])$$ (not quite a standard notation) be the space of polynomial functions $$f(x) = a_{n}x^n + \cdots + a_{1} x + a_0$$ of arbitrary degree on the interval $$[0,1]$$. The $$\ell^p$$-norm can be defined as above: $$\Vert f\Vert_{p} = \left(\sum_{k=1}^{n} \|a_{k}\|^{p}\right)^{1/p}$$.
And taking the polynomials $$x$$ and $$x^2$$, we see again that the parallelogram law fails if $$p \neq 2$$, so again this gives an example of a normed vector space that is not a Hilbert space.
The point of this example is that $$\mathcal{P}([0,1])$$ is never complete with respect to the $$\ell^{p}$$-norm.
There are many ways to see this. To keep this post as simple as possible, let me do this completely explicitly: Check that $$f_{n}(x) = \sum_{k = 0}^{n} \frac{(-1)^{k}}{(2k+1)!} x^{2k+1}$$ (the $$(2n+1)$$-st Taylor polynomial of $$\sin{x}$$) forms an $$\ell^{p}$$-Cauchy sequence and doesn't converge in $$\mathcal{P}([0,1])$$. A slightly more high-powered approach would be to appeal to the Weierstrass approximation theorem (this requires some trickery), or to the general fact that a Banach space has either finite or uncountable dimension—the latter is a standard consequence of the Baire category theorem (which amounts to even worse trickery in my opinion).
Therefore we have now an example of a normed vector space that isn't complete and for $$p = 2$$ this is an example of a pre-Hilbert space that isn't a Hilbert space. This family of examples settles strict inclusion $$\{\text{Hilbert spaces}\} \subsetneqq \{\text{pre-Hilbert spaces}\}$$, $$\{\text{Banach spaces}\} \subsetneqq \{\text{normed spaces}\}$$ and also $$\{\text{pre-Hilbert spaces}\} \subsetneqq \{\text{normed vector spaces}\}$$.
There are two inclusions we left open so far and we only gave a somewhat unsatisfactory example of a (complete) metric vector space that isn't a Banach space. Since this is a bit more subtle, we simply make some concluding remarks.

The first observation we would like to mention is that a normed vector space has an abundance of convex open sets. Indeed, the ball of radius $$r$$ around any point is convex. In a metric vector space, however, there is no reason that there be any convex open sets except the empty set and the space itself—this is due to the fact that the metric is not required to be homogeneous, only translation-invariant. One standard example for this is the space $$L_{0}([0,1])$$ of all (classes of) Lebesgue measurable functions modulo null sets, equipped with the topology of convergence in measure to be explicit, my preferred metric is $$\displaystyle d(f,g) = \int \frac{\|f - g\|}{1 + \|f-g\|}$$.
The difference between the first row and the second row is actually not that big and usually not of much importance, since there is the process of completion. Indeed, the completion of a metric vector space is again a metric vector space (and complete by definition), the completion of a normed space again has a norm and is thus a Banach space by definition and the completion of a pre-Hilbert space is a Hilbert space (since the parallelogram law holds true in the completion). To find examples that belong to the first row but not to the second, we can simply choose a dense subspace of our favourite (infinite-dimensional) example of the second row.
Finally, let me stress that all the topics above are encompassed in the theory of topological vector spaces of which the theory of locally convex spaces is the richest and most reasonable for most applications that need to go beyond normed vector spaces (e.g. the theory of distributions). But we would say that it is most reasonable to stick to Banach spaces and normed vector spaces first, to which a quite good introduction is given in Rudin's Real and complex analysis or any introduction to functional analysis. A decent knowledge of real analysis (in particular measure theory) seems to be the basic prerequisite for appreciating such a book, however.




**Update**: Here are two comments to a now deleted answer that deserve to be publicly viewable (we omitted references to the people involved and slightly changed the formatting):

Matt E writes:

[...] the notion of Hilbert space depends on $$F$$ being either $$\mathbb{R}$$ or $$\mathbb{C}$$. It requires a positive definite inner product (not an arbitrary one), and positive definite makes sense only for over $$\mathbb{R}$$ or $$\mathbb{C}$$. (And note that in the case of $$\mathbb{C}$$, it requires that the pairing be Hermitian, i.e. conjugate linear in the second variable, a concept which is particular to $$\mathbb{C}$$.) Again, in your formula for the norm, the square-root only makes sense because you are taking the square root of a positive real number — in a general field an element may not be a square, and even if it is, there won't be any way to extract a canonical square root. [...]

Qiaochu Yuan writes: 

[...] it is possible to define quaternionic Hilbert spaces. See http://math.ucr.edu/home/baez/symplectic.html


That you can't push matters much further can (in some sense) be seen from a nice theorem of Maria Pia Solèr, see John Baez's post at the nCafé for explanations, references and further thoughts.

