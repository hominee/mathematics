---
layout: post
title: How to prove Halmos’s Inequality
tag:
 - functional-analysis
 - inequality
 - hilbert-spaces
 - operator-theory
 - banach-algebras

description: How to prove Halmos’s Inequality

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

How to prove Halmos’s Inequality

<!–-break-–>


How to prove Halmos’s Inequality? 
If $$A$$ and $$B$$ are bounded linear operators on a Hilbert space
such that $$A$$, or $$B$$, commutes with $$AB-BA$$ then 

$$

\|I-(AB- BA)\|\ge 1.


$$


we found it from http://www.
staff.
vu.
edu.
au/rgmia/monographs/bullen/Dict-Ineq-Supp-Comb.
pdf at page 18.


# Answer 


There are several proofs and the inequality is given as problem 233 in Halmos's A Hilbert Space Problem Book. The inequality was originally proved in P.R. Halmos, Commutators of Operators, II, American Journal of Mathematics
Vol. 76, No. 1 (Jan., 1954), pp. 191–198. 
The following very nice proof is given by Philip Maher in A short commutator proof, International Journal of Science and Mathematics Education 27 (6) (1996), 934–935. If you have access, you find it online here.
Suppose $$\|I-(AB-BA)\| \lt 1$$. Then $$(AB-BA)$$ is invertible and as (without loss of generality) $$A$$ commutes with $$(AB-BA)$$ by hypothesis, we have that $$A$$ commutes with $$(AB-BA)^{-1}$$. Therefore


$$

we = (AB-BA)(AB-BA)^{-1} = A[B(AB-BA)^{-1}]  - [B(AB-BA)^{-1}]A

$$


and thus $$I$$ is exhibited as a commutator, and this is well-known to be impossible by a theorem of Wielandt and Wintner; see e.g. Qiaochu's question here for a proof of that fact. Therefore $$\|I-(AB-BA)\| \geq 1$$.


**Note** that this proof has nothing to do with bounded operators on a Hilbert space. It works just as well in any Banach algebra.

