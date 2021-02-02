---
layout: post
title: Problem related to calculus and integration
tag:
 - calculus
 - real-analysis
 - integration

description: Problem related to calculus and integration

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Showing that $$\int\limits_{-a}^a \frac{f(x)}{1+e^{x}} \mathrm dx = \int\limits_0^a f(x) \mathrm dx$$, when $$f$$ is even

<!–-break-–>


we have a question:

Suppose $$f$$ is continuous and even on $$[-a,a]$$, $$a>0$$ then prove that
  

$$

\int\limits_{-a}^a \frac{f(x)}{1+e^{x}} \mathrm dx = \int\limits_0^a f(x) \mathrm dx

$$



How can we do this? Don't know how to start.


# Answer 


You have

$$
\begin{align*}
we &=\int\limits_{-a}^{a}\frac{f(x)}{1+e^{x}} \ dx \qquad\qquad \cdots (1)\\\ we &= \int\limits_{-a}^{a} \frac{f(x)}{1+e^{-x}} \ dx \qquad\qquad \Bigl[ \small\because \int\limits_{a}^{b}f(x)\ dx = \int\limits_{a}^{b}f(a+b-x)\ dx \ \Bigr] \quad \cdots (2) \\\ \Longrightarrow 2we &= \int\limits_{-a}^{a} \biggl[ \frac{f(x)}{1+e^{x}} + \frac{e^{x}\cdot f(x)}{1+e^{x}} \biggr] \ dx  \quad\qquad \cdots (1) + (2)\\\  &=\int\limits_{-a}^{a} f(x) \ dx = 2 \int\limits_{0}^{a} f(x) \ dx \qquad \Bigl[ \small  \text{since}\ f \  \text{is even so} \ \int\limits_{-a}^{a} f(x) = 2\int\limits_{0}^{a} f(x) \Bigr]
\end{align*}
$$

$$\textbf{Note.}$$ A similar problem, which uses result $$(2)$$ can be found here:

Integration of a trigonometric function


