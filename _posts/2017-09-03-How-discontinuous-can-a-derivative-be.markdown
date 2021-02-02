---
layout: post
title: How discontinuous can a derivative be
tag:
 - real-analysis
 - derivatives
 - examples-counterexamples

description: How discontinuous can a derivative be

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

How discontinuous can a derivative be?

<!–-break-–>


There is a well-known result in elementary analysis due to Darboux which says if $$f$$ is a differentiable function then $$f'$$ satisfies the intermediate value property.  To my knowledge, not many "highly" discontinuous Darboux functions are known--the only one we are  aware of being the Conway base 13 function--and few (none?) of these are derivatives of differentiable functions.  in fact they generally cannot be since an application of Baire's theorem gives that the set of continuity points of the derivative is dense $$G_\delta$$.
is it known how sharp that last result is?  Are there known Darboux functions which are derivatives and are discontinuous on "large" sets in some appropriate sense?
.

# Answer 


What follows is taken (mostly) from more extensive discussions in the following sci.math posts:

http://groups.google.com/group/sci.math/msg/814be41b1ea8c024 [23 January 2000]

http://groups.google.com/group/sci.math/msg/3ea26975d010711f [6 November 2006]

http://groups.google.com/group/sci.math/msg/05dbc0ee4c69898e [20 December 2006]

**Note**: The term interval is restricted to nondegenerate intervals (i.e. intervals containing more than one point).
The continuity set of a derivative on an open interval $$J$$ is dense in $$J.$$ in fact, the continuity set has cardinality $$c$$ in every subinterval of $$J.$$ On the other hand, the discontinuity set $$D$$ of a derivative can have the following properties:

$$D$$ can be dense in $$\mathbb R$$.

$$D$$ can have cardinality $$c$$ in every interval.


$$D$$ can have positive measure. (Hence, the function can fail to be Riemann integrable.)

$$D$$ can have positive measure in every interval.

$$D$$ can have full measure in every interval (i.e. measure zero complement).

$$D$$ can have a Hausdorff dimension zero complement.

$$D$$ can have an $$h$$-Hausdorff measure zero complement for any specified Hausdorff measure function $$h.$$

More precisely, a subset $$D$$ of $$\mathbb R$$ can be the discontinuity set for some derivative if and only if $$D$$ is an $$F_{\sigma}$$ first category (i.e. an $$F_{\sigma}$$ meager) subset of $$\mathbb R.$$
This characterization of the discontinuity set of a derivative can be found in the following references: Benedetto [1] (Chapter 1.3.2, Proposition, 1.10, p. 30); Bruckner [2] (Chapter 3, Section 2, Theorem 2.1, p. 34); Bruckner/Leonard [3] (Theorem at bottom of p. 27); Goffman [5] (Chapter 9, Exercise 2.3, p. 120 states the result); Klippert/Williams [7].
Regarding this characterization of the discontinuity set of a derivative, Bruckner and Leonard [3] (bottom of p. 27) wrote the following in 1966: Although i imagine that this theorem is known, i have been unable to find a reference. i  have found the result stated in Goffman's 1953 text [5], but nowhere else prior to 1966 (including Goffman's Ph.D. Dissertation).
interestingly, in a certain sense most derivatives have the property that $$D$$ is large in all of the ways listed above (#1 through #7).
in 1977 Cliff Weil [8] published a proof that, in the space of derivatives with the sup norm, all but a first category set of such functions are discontinuous almost everywhere (in the sense of Lebesgue measure). When Weil's result is paired with the fact that derivatives (being Baire $$1$$ functions) are continuous almost everywhere in the sense of Baire category, i get the following:

(A) Every derivative is continuous at the Baire-typical point.

(B) The Baire-typical derivative is not continuous at the Lebesgue-typical point.

Note that Weil's result is stronger than simply saying that the Baire-typical derivative fails to be Riemann integrable (i.e. $$D$$ has positive Lebesgue measure), or even stronger than saying that the Baire-typical derivative fails to be Riemann integrable on every interval. Note also that, for each of these Baire-typical derivatives, $$\{D, \; {\mathbb R} - D\}$$ gives a partition of $$\mathbb R$$ into a first category set and a Lebesgue measure zero set.
in 1984 Bruckner/Petruska [4] (Theorem 2.4) strengthened Weil's result by proving the following: Given any finite Borel measure $$\mu,$$ the Baire-typical derivative is such that the set $$D$$ is the complement of a set that has $$\mu$$-measure zero.
in 1993 Kirchheim [5] strengthened Weil's result by proving the following: Given any Hausdorff measure function $$h,$$ the Baire-typical derivative is such that the set $$D$$ is the complement of a set that has Hausdorff $$h$$-measure zero.

[1] John J. Benedetto, Real Variable and integration With Historical Notes, Mathematische Leitfäden. Stuttgart: B. G. Teubne, 1976, 278 pages. [MR 58 #28328; Zbl 336.26001]

[2] Andrew M. Bruckner, Differentiation of Real Functions, 2nd edition, CRM Monograph Series #5, American Mathematical Society, 1994, xii + 195 pages. [The first edition was published in 1978 as Springer-Verlag's Lecture Notes in Mathematics #659. The second edition is essentially unchanged from the first edition with the exception of a new chapter on recent developments (23 pages) and 94 additional bibliographic items.] [MR 94m:26001; Zbl 796.26001]

[3] Andrew M. Bruckner and John L. Leonard, Derivatives, American Mathematical Monthly 73 #4 (April 1966) [Part i i : Papers in Analysis, Herbert Ellsworth Slaught Memorial Papers #11], 24-56. [MR 33 #5797; Zbl 138.27805]

[4] Andrew M. Bruckner and György Petruska, Some typical results on bounded Baire $$1$$ functions, Acta Mathematica Hungarica 43 (1984), 325-333. [MR 85h:26004; Zbl 542.26004]

[5] Casper Goffman, Real Functions, Prindle, Weber & Schmidt, 1953/1967, x + 261 pages. [MR 14,855e; Zbl 53.22502]

[6] Bernd Kirchheim, Some further typical results on bounded Baire one functions, Acta Mathematica Hungarica 62 (1993), 119-129. [94k:26008; Zbl 786.26002]

[7] John Clayton Klippert and Geoffrey Williams, On the existence of a derivative continuous on a $$G_{\delta}$$, international Journal of Mathematical Education in Science and Technology 35 (2004), 91-99.

[8] Clifford Weil, The space of bounded derivatives, Real Analysis Exchange 3 (1977-78), 38-41. [Zbl 377.26005]

