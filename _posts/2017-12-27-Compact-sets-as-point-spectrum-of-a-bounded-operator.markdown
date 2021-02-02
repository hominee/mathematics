---
layout: post
title: Compact sets as point spectrum of a bounded operator
tag:
 - functional-analysis
 - operator-theory

description: Compact sets as point spectrum of a bounded operator

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Compact sets as point spectrum of a bounded operator

<!–-break-–>


It is well known that if $$K$$ is any compact set in $$\mathbb{C}$$, then there exist a bounded linear operator $$T:l_2\to l_2$$ such that $$\sigma(T)=K$$.
 My questions are:
Q1) Does there exist $$T$$, a bounded linear operator on $$l_2$$ such that the point spectrum $$\sigma_p(T)$$ is the given $$K$$? That is, the only eigenvalues are the complex numbers in $$K$$?
Q2)  Does there exist $$T$$, a bounded linear operator on $$l_2$$ such that $$\sigma(T)=\sigma_p(T)=K$$.
 That is, there are no other points in the spectrum except the eigenvalues in $$K$$? 
Clearly a positive answer to Q2) implies a positive answer to Q1).
 
.


# Answer 


To answer Q1, we can say exactly when a subset of $$\mathbb{C}$$ can be realized as the point spectrum of a bounded linear operator on $$\ell^2$$.

Theorem: A set $$K\subseteq\mathbb{C}$$ is equal to the point spectrum of a bounded linear operator $$T\colon \ell^2\to \ell^2$$ if and only if $$K$$ is bounded and is the union of countably many closed sets (an Fσ set).

In fact, we can go a little bit further. If $$K$$ is contained in the open ball $$B_R(0)$$ for some $$R > 0$$ then it is possible to choose $$T$$ such that $$\Vert T\Vert=R$$.
Before constructing $$T$$ with the given point spectrum, I'll quickly prove the converse. If $$K=\sigma_p(T)$$ then $$K$$ is a bounded Fσ set (this will use the fact that $$\ell^2$$ is a Banach space whose dual is separable). First, $$K$$ is contained in the spectrum $$\sigma(T)$$, which is contained in the closed ball $$\bar B_R(0)$$ for $$R=\Vert T\Vert$$ (by standard properties of bounded operators), so is bounded. Next, let $$B=\lbrace x\in \ell^2\colon\Vert x\Vert\le 1\rbrace$$ be the closed unit ball in $$\ell^2$$ with the weak topology, which is compact. Then, $$B^0\equiv B\setminus\lbrace0\rbrace$$ is σ-compact. In fact, choosing any dense sequence $$u_1,u_2,\ldots$$ in $$\ell^2$$, we can explicitly write $$B^0$$ as the union of compact sets


$$


B^0=\bigcup_{n=1}^\infty\lbrace x\in B\colon\vert\langle u_n,x\rangle\vert\ge1\rbrace.


$$


Set $$C=\lbrace (x,\lambda)\in B^0\times\mathbb{C}\colon Tx=\lambda x\rbrace$$ with the product topology which, being a closed subset of $$B^0\times\mathbb{C}$$, is σ-compact. Defining the continuous map $$\pi\colon C\to\mathbb{C}$$ by $$\pi(x,\lambda)=\lambda$$, then, $$\sigma_p(T)=\pi(C)$$ is σ-compact and, hence, is an Fσ set.
Now, let's move on to constructing $$T$$ with norm $$\Vert T\Vert=R$$ and point spectrum a given bounded Fσ set $$K\subseteq B_R(0)$$. The general case follows from the case where $$K$$ is closed, since if we write $$K=\bigcup_{n=1}^\infty K_n$$ for closed $$K_n$$ then, choosing operators $$T_n$$ with $$\Vert T_n\Vert=R$$ and $$\sigma_p(T_n)=K_n$$, the direct sum $$T=\oplus_n T_n$$ is an operator on $$\oplus_n\ell^2\cong\ell^2$$ with $$\Vert T\Vert=R$$ and point spectrum $$K$$ as required.
So, suppose that $$K\subseteq B_R(0)$$ is closed. By scaling, we can assume that $$R > 1$$ and that $$K\subseteq B_1(0)$$. I'll construct a linear operator $$T$$ on the Hilbert space $$H=\ell^2(\mathbb{N}^2)\cong\ell^2$$ (we are  using $$\mathbb{N}=\lbrace0,1,2,\ldots\rbrace$$). Recall that $$H$$ consists of the functions $$f\colon\mathbb{N}^2\to\mathbb{C}$$ with finite norm $$\Vert f\Vert^2=\sum_{m,n}\vert f(m,n)\vert^2$$ and inner product $$\langle f,g\rangle=\sum_{m,n}\overline{f(m,n)}g(m,n)$$.
Now, choose sequences of positive real numbers $$r_i,\epsilon_i$$ and complex $$z_i$$ ($$i=1,2,\ldots$$) such that $$\bar B_{r_i}(z_i)$$ is disjoint from $$K$$ and such that $$K=\bar B_1(0)\setminus\bigcup_iB_{r_i}(z_i)$$. It doesn't matter exactly what values $$\epsilon_i$$ take at the moment, I'll choose these in more detail in a moment.
Define $$T\colon H\to H$$ by


$$


Tf(m,n)=\begin{cases}
f(m,n+1),&\textrm{if }m=0,\cr
r_mf(m,n-1)+z_mf(m,n),&\textrm{if }m,n > 0,\cr
\epsilon_m r_m f(0,0)+z_mf(m,n),&\textrm{if }m > 0, n=0.
\end{cases}


$$


The idea is that $$T$$ behaves as a left-shift (on $$m=0$$), so that the point spectrum is contained in $$\bar B_1(0)$$, joined to a set of right-shifts (on each $$m > 0$$) to remove the balls $$\bar B_{r_i}(z_i)$$ from the point spectrum. It can be seen that $$T$$ has norm


$$


\Vert T\Vert\le\max_m\left(1,\vert z_m\vert+r_m\right)+\left(\sum_m\epsilon_m^2r_m^2\right)^{1/2}.


$$


This satisfies $$\Vert T\Vert\le R$$ so long as we choose $$\bar B_{r_i}(z_i)\subseteq B_R(0)$$ and choose $$\epsilon_i$$ so that $$\sum_i\epsilon_i^2r_i^2$$ is small enough. And (if you like), by scaling $$\epsilon_i$$ up, we can ensure that $$\Vert T\Vert=R$$.
Now, a complex number $$\lambda$$ is in the point spectrum $$\sigma_p(T)$$ if and only if there is a nonzero $$f\in H$$ such that $$Tf=\lambda f$$. Plugging in $$Tf$$ from the definition above and solving the linear equations shows that, up to a scaling factor, $$f$$ must be given by


$$


f(m,n)=\begin{cases}
\lambda^n,&\textrm{if }m=0,\cr
\epsilon_m\left(r_m/(\lambda-z_m)\right)^{n+1},&\textrm{if }m > 0.
\end{cases}


$$


If $$\vert\lambda\vert\ge1$$ then $$\sum_n\vert f(0,n)\vert^2=\infty$$, so we must have $$\vert\lambda\vert < 1$$. Similarly, if $$\lambda\in\bar B_{r_i}(z_i)$$ then $$\sum_n\vert f(i,n)\vert^2=\infty$$. So, in order that $$f\in H$$ we must have $$\lambda\in K$$, in which case,


$$


\Vert f\Vert^2=\frac{1}{1-\vert\lambda\vert^2}+\sum_{m=1}^\infty\frac{\epsilon_m^2}{\vert\lambda-z_m\vert^2/r_m^2-1}.


$$


Now, as $$\bar B_{r_i}(z_i)$$ is disjoint from $$K$$, the term $$(\vert\lambda-z_i\vert^2/r_i^2-1)^{-1}$$ is a continuous positive function of $$\lambda\in K$$, so is bounded above by some $$d_i^2 > 0$$. Then,


$$


\Vert f\Vert^2\le\frac{1}{1-\vert\lambda\vert^2}+\sum_{m=1}^\infty\epsilon_m^2d_m^2.


$$


So long as we choose $$\epsilon_i$$ so that $$\sum_m\epsilon_m^2d_m^2 < \infty$$, this implies that $$f\in H$$ for all $$\lambda\in K$$, so $$\sigma_p(T)=K$$.


**Note**: The operator $$T$$ we constructed here does not give a positive answer to Q2. For any $$\omega\in S^1$$ and $$\epsilon > 0$$, setting $$f_\epsilon(m,n)=1_{\lbrace m=0\rbrace}\epsilon\omega^n(1+\epsilon)^{-n-1}$$ gives $$\Vert f_\epsilon\Vert=1$$ and $$\Vert(T-\omega)f_\epsilon\Vert\to0$$ as $$\epsilon\to0$$, so $$\omega\in\sigma(T)$$. Therefore, $$S^1\subseteq\sigma(T)$$.

