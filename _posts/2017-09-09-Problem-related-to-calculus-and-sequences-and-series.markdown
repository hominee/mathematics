---
layout: post
title: Problem related to calculus and sequences and series
tag:
 - calculus
 - real-analysis
 - sequences-and-series

description: Problem related to calculus and sequences and series

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Proving an alternating Euler sum: $$\sum_{k=1}^{\infty} \frac{(-1)^{k+1} H_k}{k} = \frac{1}{2} \zeta(2) - \frac{1}{2} \log^2 2$$

<!–-break-–>


Let 

$$

A(p,q) = \sum_{k=1}^{\infty} \frac{(-1)^{k+1}H^{(p)}_k}{k^q},

$$


where $$H^{(p)}_n = \sum_{i=1}^n i^{-p}$$, the $$n$$th $$p$$-harmonic number.  The $$A(p,q)$$'s are known as alternating Euler sums.

Can someone provide a nice proof that 
  

$$

A(1,1) = \sum_{k=1}^{\infty} \frac{(-1)^{k+1} H_k}{k} = \frac{1}{2} \zeta(2) - \frac{1}{2} \log^2 2?

$$



we worked for a while on this today but was unsuccessful.  Summation by parts, swapping the order of summation, and approximating $$H_k$$ by $$\log k$$ were my best ideas, but we could not get any of them to work.  (Perhaps someone else can?)  we would like a nice proof in order to complete my answer here.
Bonus points for proving $$A(1,2) = \frac{5}{8} \zeta(3)$$ and $$A(2,1) =  \zeta(3) - \frac{1}{2}\zeta(2) \log 2$$, as those are the other two alternating Euler sums needed to complete my answer.

Added: we are  going to change the accepted answer to robjohn's $$A(1,1)$$ calculation as a proxy for the three answers he gave here.  Notwithstanding the other great answers (especially the currently most-upvoted one, the one we first accepted), robjohn's approach is the one we was originally trying.  we are  pleased to see that it can be used to do the $$A(1,1)$$, $$A(1,2)$$, and $$A(2,1)$$ derivations.
    .

# Answer 


$$A(1,1)$$:


$$





$$
\begin{align*}
\sum_{n=1}^N\frac{(-1)^{n-1}}{n}H_n
&=\sum_{n=1}^N\frac{(-1)^{n-1}}{n^2}+\sum_{n=2}^N\frac{(-1)^{n-1}}{n}H_{n-1}\\
&=\sum_{n=1}^N\frac{(-1)^{n-1}}{n^2}+\frac12\sum_{n=2}^N\sum_{k=1}^{n-1}\frac{(-1)^{n-1}}{n}\left(\frac1k+\frac1{n-k}\right)\\
&=\sum_{n=1}^N\frac{(-1)^{n-1}}{n^2}+\frac12\sum_{n=2}^N\sum_{k=1}^{n-1}\frac{(-1)^{n-1}}{k(n-k)}\\
&=\sum_{n=1}^N\frac{(-1)^{n-1}}{n^2}+\frac12\sum_{k=1}^{N-1}\sum_{n=k+1}^N\frac{(-1)^{n-1}}{k(n-k)}\\
&=\sum_{n=1}^N\frac{(-1)^{n-1}}{n^2}+\frac12\sum_{k=1}^{N-1}\sum_{n=1}^{N-k}\frac{(-1)^{n+k-1}}{kn}\\
&=\color{#00A000}{\sum_{n=1}^N\frac{(-1)^{n-1}}{n^2}}
-\color{#0000FF}{\frac12\sum_{k=1}^{N-1}\frac{(-1)^{k-1}}{k}\sum_{n=1}^{N-1}\frac{(-1)^{n-1}}{n}}\\
&+\color{#C00000}{\frac12\sum_{k=1}^{N-1}\frac{(-1)^{k-1}}{k}\sum_{n=N-k+1}^{N-1}\frac{(-1)^{n-1}}{n}}\tag{1}
\end{align*}


$$


$$


where, using the Alternating Series Test, we have


$$





$$
\begin{align*}
&\color{#C00000}{\frac12\left|\sum_{k=1}^{N-1}\frac{(-1)^{k-1}}{k}\sum_{n=N-k+1}^{N-1}\frac{(-1)^{n-1}}{n}\right|}\\
&\le\frac12\left|\sum_{k=1}^{N/2}\frac{(-1)^{k-1}}{k}\sum_{n=N-k+1}^{N-1}\frac{(-1)^{n-1}}{n}\right|
+\frac12\left|\sum_{k=N/2}^{N-1}\frac{(-1)^{k-1}}{k}\sum_{n=N-k+1}^{N-1}\frac{(-1)^{n-1}}{n}\right|\\
&\le\frac12\cdot1\cdot\frac2N+\frac12\cdot\frac2N\cdot1\\
&=\frac2N\tag{2}
\end{align*}


$$


$$


Applying $$(2)$$ to $$(1)$$ and letting $$N\to\infty$$, we get


$$


\sum_{n=1}^\infty\frac{(-1)^{n-1}}{n}H_n=\color{#00A000}{\frac12\zeta(2)}-\color{#0000FF}{\frac12\log(2)^2}\tag{3}


$$



