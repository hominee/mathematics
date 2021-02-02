---
layout: post
title: Sum of infinite series with Harmonic numbers
tags:
  - infinite series
  - Euler Mascheroni constant
  - Harmonic numbers
  - double integral
  - way of convergence
  - limit
  - integral
description: >
  Sum of infinite series with Harmonic numbers
hero: https://source.unsplash.com/collection/145103/
overlay: blue
published: true
---


# Question

$$
\begin{equation*}
\sum _{i=1} ^{ \infty } \sum _{j=1} ^{ \infty } \frac{ (-1)^{ i+j }}{ i+j }
\end{equation*}
$$

<!–-break-–>

The definition of integrals suggests me that it is a double integrals, but does not trigger an solution 
easily. The most intuitive ideals we can think, in my opinion, are harmonic numbers.

This was a good question that connect harmonic numbers and integral. We know that 

$$  
\begin{equation}
H_{ n } = \sum _{ i=n } ^{n} \frac{1}{ i } = \gamma + \ln(n) + \epsilon_{n}
\end{equation}
\label{harmonic}
$$

where $$ \epsilon _n $$ is small.  

Let $$ k = i+j $$ be a fixed number combined with equation $$\eqref{harmonic}$$, the question may take on good properties as  

$$ 

\begin{equation}
\begin{aligned}
\sum _{i=1} ^{ \infty } \sum _{j=1} ^{ \infty } \frac{ (-1)^{ i+j }}{ i+j } 
& = \sum _{k=2} ^{ \infty } \frac{ (-1)^{ k }}{ k } (k-1) \\
& = \sum _{k=2} ^{ \infty } (1 - k^{-1}) (-1)^{k} \\
& = \sum _{k=2} ^{ \infty } k^{-1} (-1)^{k-1} + (-1)^{k}
\end{aligned} 
\end{equation}
\label{new}
$$

Recall that the taylor expansion of $$ \ln(2) $$ at point $$ x = 0 $$, 

$$
\label{sub}
\begin{equation}
\ln(2)  = \sum _{k=1} ^{ \infty } \frac{ (-1)^{k-1} }{ k } = 1 - 2^{-1} + 3^{-1} - ...
\end{equation}
$$

with formula $$ \eqref{new} $$ and $$ \eqref{sub} $$ one can deduce that 

$$ 
\label{result}
\begin{equation}
\begin{aligned}
\sum _{i=1} ^{ \infty } \sum _{j=1} ^{ \infty } \frac{ (-1)^{ i+j }}{ i+j } 
& = \sum _{k=2} ^{ \infty } k^{-1} (-1)^{k-1} + (-1)^{k} \\
& = \ln(2) - 1 + \frac{(-1)^k + 1}{2}
\end{aligned}
\end{equation}  
$$

you will gets a degrade if you think we are done with an answer $$ \ln(2) - \frac{1}{2} $$ even though it is, the 
way the original problem converge to the limit is not that we reshape in formula $$ \eqref{new} $$ , 

$$
\begin{matrix}
  2^{-1} &  3^{-1} &  4^{-1} &  ...\\
  3^{-1} &  4^{-1} &  5^{-1} &  ...\\
  4^{-1} &  5^{-1} &  6^{-1} &  ...\\
  ...    &  ...    &  ...    &  ...\\
\end{matrix}
$$

$$ \eqref{harmonic}$$ converge by the infinite sum of each row, whereas $$ \eqref{new} $$ approaches it via 
secondary diagonal. So what is the right way to tickle it will be the second part of the topic.


# Answer
$$ \ln(2) - \frac{1}{2}  $$
