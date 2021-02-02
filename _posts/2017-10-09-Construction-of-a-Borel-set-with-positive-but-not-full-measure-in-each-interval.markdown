---
layout: post
title: Construction of a Borel set with positive but not full measure in each interval
tag:
 - real-analysis
 - measure-theory

description: Construction of a Borel set with positive but not full measure in each interval

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Construction of a Borel set with positive but not full measure in each interval

<!–-break-–>


we was wondering how one can construct a Borel set that doesn't have full measure on any interval of the real line but does have positive measure everywhere. 
To be precise, if $$\mu$$ denotes Lebesgue measure, how would one construct a Borel set $$A \subset \mathbb{R}$$ such that


$$

0 < \mu(A \cap I) < \mu(I)

$$


for every interval $$I$$ in $$\mathbb{R}$$? 
Moreover, would such a set necessarily have to contain infinite measure?   
.

# Answer 


If you got this from Rudin (it is Exercise 8, Ch. 2 in his Real & Complex Analysis), here is his personal answer (excerpted from Amer. Math Monthly, Vol. 90, No.1 (Jan 1983) pp. 41-42). He works with the unit interval $$[0,1]$$, but of course this can be extended to $$\mathbb R$$ by doing the same thing in each interval (and by scaling these replications appropriately you can get the final set with finite measure). Anyways, here's how it goes:
"Let $$I=[0,1]$$, and let CTDP mean compact totally disconnected subset of $$I$$, having positive measure. Let $$\langle I_n\rangle$$ be an enumeration of all segments in $$I$$ whose endpoints are rational.
Construct sequences $$\langle A_n\rangle,\langle B_n\rangle$$ of CTDP's as follows: Start with disjoint CTDP's $$A_1$$ and $$B_1$$ in $$I_1$$. Once $$A_1,B_1,\dots,A_{n-1},B_{n-1}$$ are chosen, their union $$C_n$$ is CTD, hence $$I_n\setminus C_n$$ contains a nonempty segment $$J$$ and $$J$$ contains a pair $$A_n,B_n$$ of disjoint CTDP's. Continue in this way, and put


$$


A=\bigcup_{n=1}^{\infty}A_n.


$$


If $$V\subset I$$ is open and nonempty, then $$I_n\subset V$$ for some $$n$$, hence $$A_n\subset V$$ and $$B_n\subset V$$. Thus


$$


0<m(A_n)\leq m(A\cap V)<m(A\cap V)+m(B_n)\leq m(V);


$$


the last inequality holds because $$A$$ and $$B_n$$ are disjoint. Done.
The purpose of publishing this is to show that the highly computational construction of such a set in [another article] is much more complicated than necessary."  



**Edit**: In his excellent comment below, @ccc managed to isolate the necessary components of my solution, and after incorporating his observation it has been greatly simplified. (Actually, after trimming the fat, we have  realized that it is actually not entirely dissimilar from Rudin's.) Here it is:
Let $$\{r_n\}$$ be an enumeration of the rationals, let $$V_1$$ be a segment of finite length centered at $$r_1$$, and let $$V_n$$ be a segment of length $$m(V_{n-1})/3$$ centered at $$r_n$$. Set


$$


W_n=V_n-\bigcup_{k=1}^{\infty}V_{n+k},


$$


and observe that
\begin{equation}
m(W_n)\geq m(V_n)-\sum_{k=1}^{\infty}m(V_{n+k})=m(V_n)-m(V_n)\sum_{k=1}^{\infty}3^{-k}=\frac{m(V_n)}{2}.
\end{equation}
In particular, $$m(W_n)>0$$.
For each $$n$$, choose a Borel set $$A_n\subset W_n$$ with $$0<m(A_n)<m(W_n)$$. Finally, put $$A=\bigcup_{n=1}^{\infty}A_n$$. Because $$A_n\subset W_n$$ and the $$W_n$$ are disjoint,  $$m(A\cap W_n)=m(A_n)$$. That is to say,


$$


0<m(A\cap W_n)<m(W_n)


$$


for every $$n$$. But every interval contains a $$W_n$$, so $$A$$ meets the criteria, and has finite measure (specifically, $$m(A)\leq\sum_n m(V_n)=2 m(V_1)<\infty$$).

As a curiosity, here's my own "unnecessarily computational" way (though it's not quite as lengthy as that in the article Rudin was referring to), which we can't resist including because we slaved over it when we first came across this problem, before finding Rudin's solution: 
Let $$\{r_n\}$$ be an enumeration of the rationals, and put


$$


V_n=\left(r_n-3^{-n-1},r_n+3^{-n-1}\right),\qquad W_n=V_n-\bigcup_{k=1}^{\infty}V_{n+k}.


$$


Observe that
\begin{equation}
m(W_n)>m(V_n)-\sum_{k=1}^{\infty}m(V_{n+k})=m(V_n)-m(V_n)\sum_{k=1}^{\infty}3^{-k}=\frac{m(V_n)}{2}.\qquad\qquad(1)\label{8.1}
\end{equation}
(We have strict inequality because there exist rationals $$r_i$$, with $$i>n$$, in the complement of $$V_n$$.) 
For each $$n$$, let $$K_n$$ be a Borel set in $$V_n$$ with measure $$m(K_n)=m(V_n)/2$$.  Finally, put


$$

A_n=W_n\cap K_n,\qquad A=\bigcup_{n=1}^{\infty}A_n.

$$


To prove that $$A$$ has the desired property, it is enough to verify that the inequalities


$$

0<m(A\cap V_n)<m(V_n)\qquad\qquad(3)\label{8.3}

$$


hold for every $$n$$. (This is because every interval contains a $$V_n$$.) For the left inequality, it is enough to prove that $$m(A_n\cap V_n)=m(A_n)=m(W_n\cap K_n)>0$$. This follows from the relations


$$

m(W_n\cup K_n)\leq m(V_n)<m(W_n)+m(K_n)=m(W_n\cup K_n)+m(W_n\cap K_n),

$$


the second inequality being a consequence of (1) and the fact that $$m(K_n)=m(V_n)/2$$.
For the right inequality of (3), observe that $$V_n\subset W_i^c$$ for $$i<n$$, and that therefore


$$


m(A\cap V_n)=m\left(\bigcup_{k=0}^{\infty}A_{n+k}\cap V_n\right)\leq\sum_{k=0}^{\infty}m(K_{n+k}\cap V_n)


$$




$$


<\sum_{k=0}^{\infty}m(K_{n+k})=\sum_{k=0}^{\infty}\frac{m(V_{n+k})}{2}=\sum_{k=0}^{\infty}\frac{m(V_n)}{2^{k+1}}=m(V_n).


$$


The strict inequality above follows from three observations: 

(i) $$m(K_i)>0$$ for every $$i$$; 

(ii) $$K_i\subset V_i$$; and 

(iii) there exist neighborhoods $$V_i$$, with $$i>n$$, that are contained entirely in the complement of $$V_n$$.
So $$A$$ meets the criteria (and also has finite measure).

