---
layout: post
title: divisibility problem
tags:
  - polynomial
  - divisibility
description: >
  divisibility problem
hero: https://source.unsplash.com/collection/145103/
overlay: blue
published: true
---


# Question

show that

$$
\sum _{k=1} ^n \frac{(2x-x^2)^k - 2 x^k}{k}
$$

is divisible by $$x^{n+1}$$

<!–-break-–>

# Answer

Since 

$$
\ln (\frac{1}{1-x}) = \sum _{k=1} ^n \frac{x^k}{k} + o(x^n)
$$

and 

$$
\begin{equation}
\ln (\frac{1}{(1-x)^2}) = \sum _{k=1} ^n \frac{2 x^k}{k} + o(x^n)
\end{equation}
\label{first}
$$

Futhermore

$$
\begin{equation}
\begin{aligned}
\ln (\frac{1}{(1-x)^2}) &= - \ln (1-(2x - x^2)) \\
&= \sum _{k=1} ^n \frac{(2x-x^2)^k}{k} + o((2x-x^2)^n) \\
&= \sum _{k=1} ^n \frac{(2x-x^2)^k}{k} + o(x^n)
\end{aligned}
\end{equation}
\label{second}

$$

subtract $$\eqref{first}$$ with $$\eqref{second}$$ obtain the result.