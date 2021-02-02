---
layout: post
title: sum related to zeta function 1
tags:
  - sum  
  - closed-form
  - hypergeometric-function
  - real-analysis
  
description:  
  sum related to zeta function 1
hero: https://source.unsplash.com/collection/145103/
overlay: blue
published: true
---


# Question

Sum of :

$$

 \sum_{n=1}^{\infty}{\zeta(2n)\over a^{2n}n}=\ln\left({\pi\over a\sin({\pi\over a})}\right)

$$

 
Using [Sum Calculator][1] on $$(1)$$,


$$
\sum_{n=1}^{\infty}{\zeta(2n)\over a^{2n}n}\tag1
$$

for $$a>1$$

we noticed that it takes a closed form of


$$
(1)=\ln\left({\pi\over a\sin({\pi\over a})}\right)\tag2
$$


How can we show that whether $$(1)$$ is correct or not?

We can see that


$$
{\sin x\over x}=\prod_{n=1}^{\infty}\left(1-{x^2\over n^2\pi^2}\right)\tag3
$$


It looks like that the product $$(3)$$ can we change into a sum, but how ?

  [1]: http://www.wolframalpha.com/widget/widgetPopup.jsp?p=v&id=dfaf1b7d15e572ae5a1b2fa172ce8657&title=Math%20Help%20Boards:%20Sum%20Calculator&theme=blue

<!–-break-–>


# Answer

With formula

$$
\sum_{n=1}^\infty\zeta(2n)x^{2n}=\dfrac12\left(1-\pi x\cot\pi x\right)
$$

we have

$$
\sum_{n=1}^\infty\zeta(2n)x^{n-1}=\dfrac12\left(\dfrac1x-\dfrac{\pi}{\sqrt{x}}\cot\pi\sqrt{x}\right)
$$

after integration

$$
\sum_{n=1}^\infty\zeta(2n)\dfrac{x^n}{n}=\log\dfrac{\sqrt{x}}{\sin\pi \sqrt{x}}+C
$$

then set $$x=\dfrac{1}{a^2}$$ where $$C=\log\pi$$ obtaining with limit as $$x\to0$$.