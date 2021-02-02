---
layout: post
title: What are the differences and relations of Haar integrals, Lebesgue integrals, Riemann integrals
tag:
 - integration
 - harmonic-analysis

description: What are the differences and relations of Haar integrals, Lebesgue integrals, Riemann integrals

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

What are the differences and relations of Haar integrals, Lebesgue integrals, Riemann integrals?

<!–-break-–>


Are Riemann integrals special cases of Haar integrals? Why do we need the invariant property under some actions of groups in the definition of Haar integrals? 

For example, if we have a group of real matrices $$G$$ and we have an inner product $$\langle\>\ ,\ \rangle: G \times G \to \mathbb{R}$$, for any $$A, B$$ in $$G$$, $$C$$ in the subgroup $$O:=\{C\in G: C^{T}C=I\}$$, $$\langle A, B\rangle=\langle O^{T}AO,O^{T}BO\rangle$$, then we can define an integral $$\int_{G} f d\mu$$ over $$G$$.


**Edit**: we are  having a course about random matrices. The course is related to the lecture notes: http://arxiv.org/abs/0801.1858. On page 2, equation (2.4), we think that the integral is a haar integral. we don't know why we need (2.5) in the paper.

# Answer 


Lebesgue integration, in the sense of integration with respect to Lebesgue measure on $$\mathbb{R}^n$$, is a special case of Haar integration, because Lebesgue measure is the Haar measure on the abelian group $$\mathbb{R}^n$$ with addition and the usual topology (normalized so that the measure of a unit $$n$$-cube is $$1$$).  

Riemann integration is closely related to Lebesgue integration, but a fundamental difference is that the Riemann integral is not directly related to a measure, and as a result there are far fewer general results applicable.  

For example, a pointwise limit of uniformly bounded Riemann integrable functions on a bounded interval need not be Riemann integrable, even if the convergence is monotone. 

Lebesgue integration can be seen as a completion of Riemann integration.  

If $$(R)\int f$$ denotes the Riemann integral of a continuous function with compact support on $$\mathbb{R}^n$$, then $$f\mapsto(R)\int f$$ is a positive linear functional on $$C_c(\mathbb{R}^n)$$, and the Riesz representation theorem yields a positive Borel measure $$\mu$$ on $$\mathbb{R}^n$$ such that $$(R)\int f=\int fd\mu$$ for all $$f\in C_c(\mathbb{R}^n)$$.  

The completion of $$\mu$$ is Lebesgue measure.  For (proper) Riemann integrable functions, the Riemann and the Lebesgue integral are the same, but there are many functions that are "nice" from the measure theoretic perspective but not Riemann integrable, such as the characteristic function of the rationals on $$\mathbb{R}$$.  

On the other hand, there are functions whose improper Riemann integral exists but whose Lebesgue integral does not exist due to the positive and negative parts not being integrable, such as $$\frac{\sin(x)}{x}$$ on $$\mathbb{R}$$.  

In such cases, you could define an "improper" Lebesgue integral by taking limits as the domain increases to obtain the same result as with improper Riemann integrals, so there is no real loss in only considering Lebesgue integrals.

we recommend reading pages 195-197 of Körner's A companion to analysis for a nice discussion of the motivation of going beyond Riemann integration.

