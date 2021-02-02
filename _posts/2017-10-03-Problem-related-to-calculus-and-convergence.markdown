---
layout: post
title: Problem related to calculus and convergence
tag:
 - calculus
 - real-analysis
 - integration
 - limits
 - convergence

description: Problem related to calculus and convergence

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Compute $$\lim_{n\to\infty}n^4\int_0^1\frac{x^n\ln^3x}{1+x^n}\ln(1-x)\,dx$$

<!–-break-–>


Compute

\begin{equation}
\lim_{n\to\infty}n^4\int_0^1\frac{x^n\ln^3x}{1+x^n}\ln(1-x)\,dx
\end{equation}

According to Wolfram Alpha, the limit is zero. we tried to make substitution $$x=\frac{t}{n}$$ and we got
\begin{equation}
\lim_{n\to\infty}\int_0^{\large\frac{1}{n}}\frac{t^n\ln^3t}{n^n+t^n}\ln\left(1-\frac{t}{n}\right)\,dx \to 0
\end{equation}
but we are  not sure this approach is correct.
we also tried to make substitution $$t=x^n$$ and we got
\begin{equation}
\lim_{n\to\infty}n^4\int_0^1\frac{x^n\ln^3x}{1+x^n}\ln(1-x)\,dx=\lim_{n\to\infty}\int_0^1\frac{t^{\large\frac{1}{n}}\ln^3t}{1+t}\ln\left(1-t^{\large\frac{1}{n}}\right)\,dt
\end{equation}
we used the bound 

$$

\left|\int_0^1\frac{t^{\large\frac{1}{n}}\ln^3t}{1+t}\ln\left(1-t^{\large\frac{1}{n}}\right)\,dt\right|\leq\int_0^1\left|t^{\large\frac{1}{n}}\ln^3t\ln\left(1-t^{\large\frac{1}{n}}\right)\right|\,dt

$$


because  $$1+t\ge1$$, so $$\frac{1}{1+t}\leq1$$. we can compute the integral using Taylor series for the logarithm but after taking the limit we got the result was infinity.

# Answer 


We will prove that the limit is $$+\infty$$.
Let 

$$

\eqalign{I_n&=n^4\int_0^1\frac{x^n}{1+x^n}\ln^3 x\ln(1-x)dx\cr
J_n&=n^4\int_0^1x^n\ln^3 x\ln(1-x)dx}

$$


Clearly 

$$

\frac{1}{2}J_n\leq I_n\leq J_n

$$


because $$\frac{1}{2}\leq\frac{1}{1+x^n}\leq1$$ and $$\ln^3x\ln(1-x)\geq0$$ for $$0<x<1$$.
So, let us consider $$J_n$$.
We have


$$

-\ln(1-x)=\sum_{k=1}^\infty\frac{x^k}{k}

$$


and


$$

\int_0^1x^{m}(-\ln x)^3dx=\frac{6}{(m+1)^4}

$$


Combining these two properties we see that


$$


J_n=\sum_{k=1}^\infty\frac{6n^4}{k(k+1+n)^4}


$$


for a given $$m\geq1$$ we have


$$


J_n\geq\sum_{k=1}^m\frac{6n^4}{k(k+1+n)^4}


$$


hence


$$

\liminf_{n\to\infty}J_n\geq 6 \sum_{k=1}^m\frac{1}{k}

$$


but $$m$$ is arbitrary and $$\sum \frac{1}{k}$$ is divergent, So


$$

\liminf_{n\to\infty}J_n=+\infty

$$


that is $$\lim\limits_{n\to\infty}J_n=+\infty$$, and consequently $$\lim\limits_{n\to\infty}I_n=+\infty$$.

