---
layout: post
title: integral related to zeta function
tags:
  - integral 
  - closed-form
  - zeta-function
  - real-analysis
  
description:  
  integral related to zeta function
hero: https://source.unsplash.com/collection/145103/
overlay: blue
published: true
---


# Question

Closed form of :

$$

{\large\int}_0^1\frac{\ln^3(1+x)\,\ln^2x}xdx

$$



<!–-break-–>

there are several very similar integrals having known closed forms:

$$
\int_0^1\frac{\ln^2(1+x)\,\ln^2x}xdx=\frac{\pi^2\,\zeta(3)}3-\frac{29\,\zeta(5)}8\tag3
$$




$$
\int_0^1\frac{\ln^3(1-x)\,\ln^2x}xdx=12\zeta^2(3)-\frac{23\pi^6}{1260}\tag4
$$



$$
\begin{align*}
\int_0^1\frac{\ln^3(1+x)\,\ln^2x}{x^2}dx
&=\,\frac{3\zeta(3)}2+2\pi^2\zeta(3)+\frac{3\zeta(5)}2-\frac{21\zeta(3)}2\ln^22\\
&-\,\frac{63\zeta(3)}2\ln2+\frac{23\pi^4}{60}-\frac{4\ln^52}5-\frac{3\ln^42}2\\
&-\,4\ln^32+\frac{2\pi^2}3\ln^32+\frac{3\pi^2}2\ln^22-24\operatorname{Li}_5\!\left(\tfrac12\right)\\
&-\,36\operatorname{Li}_4\!\left(\tfrac12\right)-24\operatorname{Li}_4\!\left(\tfrac12\right)\ln2\tag5
\end{align*}
$$

# Answer

Using the following results:

$$
2\sum^\infty_{n=1}\frac{H_n}{n^q}=(q+2)\zeta(q+1)-\sum^{q-2}_{j=1}\zeta(j+1)\zeta(q-j)\tag1
$$


$$
\sum^\infty_{n=1}\frac{H_n}{n^22^n}=\zeta(3)-\frac{\pi^2}{12}\ln{2}\tag2
$$


$$
\sum^\infty_{n=1}\frac{H_n}{n^32^n}={\rm Li}_4\left(\tfrac{1}{2}\right)+\frac{\pi^4}{720}-\frac{1}{8}\zeta(3)\ln{2}+\frac{1}{24}\ln^4{2}\tag3
$$

$$
\begin{align*}
\sum^\infty_{n=1}\frac{H_n}{n^42^n}
&=2{\rm Li}_5\left(\tfrac{1}{2}\right)+\frac{1}{32}\zeta(5)+{\rm Li}_4\left(\tfrac{1}{2}\right)\ln{2} \\
&-\frac{\pi^4}{720}\ln{2}+\frac{1}{2}\zeta(3)\ln^2{2}\\
&-\frac{\pi^2}{12}\zeta(3)-\frac{\pi^2}{36}\ln^3{2}+\frac{1}{40}\ln^5{2}\tag4
\end{align*}
$$

Proofs of $$(1)$$, $$(2)$$ and $$(4)$$ can be found [here][1], [here][2] and [here][3] respectively. Unfortunately, there has not been a mathematically sound proof of $$(3)$$ on MSE as of now.
___
Using $$\mathcal{I}$$ to denote the integral in question,

$$
\begin{align*}
\mathcal{I}
&=-\int^1_0\frac{\ln^3{x}\ln^2(1+x)}{1+x}{\rm d}x\\
&=-\int^2_1\frac{\ln^2{x}\ln^3(x-1)}{x}{\rm d}x\\
&=\underbrace{-\int^1_\frac{1}{2}\frac{\ln^2{x}\ln^3(1-x)}{x}{\rm d}x}_{\mathcal{I}_1}\underbrace{+3\int^1_{\frac{1}{2}}\frac{\ln^3{x}\ln^2(1-x)}{x}}_{\mathcal{I}_2}\underbrace{-3\int^1_{\frac{1}{2}}\frac{\ln^4{x}\ln(1-x)}{x}{\rm d}x}_{\mathcal{I}_3}-\frac{1}{6}\ln^6{2}
\end{align*}
$$

For $$\mathcal{I}_1$$, integration by parts gives

$$
\mathcal{I}_1=\frac{1}{3}\ln^6{2}-\int^1_\frac{1}{2}\frac{\ln^3{x}\ln^2(1-x)}{1-x}{\rm d}x
$$

On the other hand, $$x\mapsto1-x$$ yields

$$
\mathcal{I}_1=-\int^\frac{1}{2}_0\frac{\ln^3{x}\ln^2(1-x)}{1-x}{\rm d}x
$$

Combining these two equalities, we have

$$
\begin{align*}
\mathcal{I}_1
&=\frac{1}{6}\ln^6{2}-\frac{1}{2}\int^1_0\frac{\ln^3{x}\ln^2(1-x)}{1-x}{\rm d}x\\
&=\frac{1}{6}\ln^6{2}-\frac{1}{2}\frac{\partial^5\beta}{\partial a^3\partial b^2}(1,0^+)\\
&=\frac{1}{6}\ln^6{2}-\frac{1}{2}\left[\frac{1}{b}+\mathcal{O}(1)\right]\left[\left(12\zeta^2(3)-\frac{23\pi^6}{1260}\right)b+\mathcal{O}(b^2)\right]_{b=0}\\
&=\frac{23\pi^6}{2520}-6\zeta^2(3)+\frac{1}{6}\ln^6{2}
\end{align*}
$$

Even with the help of Wolfram Alpha, evaluating that fifth derivative was horribly unpleasant to say the least. As for $$\mathcal{I}_2$$,

$$
\begin{align*}
\mathcal{I}_2
=&6\sum^\infty_{n=1}\frac{H_n}{n+1}\int^1_\frac{1}{2}x^n\ln^3{x}\ {\rm d}x\\
=&6\sum^\infty_{n=1}\frac{H_n}{n+1}\frac{\partial^3}{\partial n^3}\left(\frac{1}{n+1}-\frac{1}{(n+1)2^{n+1}}\right)\\
=&\color{#E2062C}{-\sum^\infty_{n=1}\frac{36H_n}{(n+1)^5}}+\color{#FF4F00}{\sum^\infty_{n=1}\frac{36H_n}{(n+1)^52^{n+1}}}+\color{#00A000}{\sum^\infty_{n=1}\frac{36\ln{2}H_n}{(n+1)^42^{n+1}}}+\color{#21ABCD}{\sum^\infty_{n=1}\frac{18\ln^2{2}H_n}{(n+1)^32^{n+1}}}\\&+\color{#6F00FF}{\sum^\infty_{n=1}\frac{6\ln^3{2}H_n}{(n+1)^22^{n+1}}}\\
=&\color{#E2062C}{-\frac{\pi^6}{35}+18\zeta^2(3)}+\color{#FF4F00}{\sum^\infty_{n=1}\frac{36H_n}{n^52^{n}}-36{\rm Li}_6\left(\tfrac{1}{2}\right)}+\color{#00A000}{36{\rm Li}_5\left(\tfrac{1}{2}\right)\ln{2}+\frac{9}{8}\zeta(5)\ln{2}}\\
&+\color{#00A000}{36{\rm Li}_4\left(\tfrac{1}{2}\right)\ln^2{2}-\frac{\pi^4}{20}\ln^2{2}+18\zeta(3)\ln^3{2}-3\pi^2\zeta(3)\ln{2}-\pi^2\ln^4{2}+\frac{9}{10}\ln^6{2}}\\
&+\color{#21ABCD}{\frac{\pi^4}{40}\ln^2{2}-\frac{9}{4}\zeta(3)\ln^3{2}+\frac{3}{4}\ln^6{2}}+\color{#6F00FF}{\frac{3}{4}\zeta(3)\ln^3{2}-\ln^6{2}}\\
=&\sum^\infty_{n=1}\frac{36H_n}{n^52^{n}}-36{\rm Li}_6\left(\tfrac{1}{2}\right)-\frac{\pi^6}{35}+36{\rm Li}_5\left(\tfrac{1}{2}\right)\ln{2}+\frac{9}{8}\zeta(5)\ln{2}+36{\rm Li}_4\left(\tfrac{1}{2}\right)\ln^2{2}\\
&-\frac{\pi^4}{40}\ln^2{2}+18\zeta^2(3)-3\pi^2\zeta(3)\ln{2}+\frac{33}{2}\zeta(3)\ln^3{2}-\pi^2\ln^4{2}+\frac{13}{20}\ln^6{2}
\end{align*}
$$

For $$\mathcal{I}_3$$,

$$
\begin{align*}
\mathcal{I}_3
=&3\sum^\infty_{n=1}\frac{1}{n}\int^1_\frac{1}{2}x^{n-1}\ln^4{x}\ {\rm d}x\\
=&3\sum^\infty_{n=1}\frac{1}{n}\frac{\partial^4}{\partial n^4}\left(\frac{1}{n}-\frac{1}{n2^n}\right)\\
=&\sum^\infty_{n=1}\left(\frac{72}{n^6}-\frac{72}{n^62^n}-\frac{72\ln{2}}{n^52^n}-\frac{36\ln^2{2}}{n^42^n}-\frac{12\ln^3{2}}{n^32^n}-\frac{3\ln^4{2}}{n^22^n}\right)\\
=&-72{\rm Li}_6\left(\tfrac{1}{2}\right)+\frac{8\pi^6}{105}-72{\rm Li}_5\left(\tfrac{1}{2}\right)\ln{2}-36{\rm Li}_4\left(\tfrac{1}{2}\right)\ln^2{2}\\&-\frac{21}{2}\zeta(3)\ln^3{2}+\frac{3\pi^2}{4}\ln^4{2}-\frac{1}{2}\ln^6{2}
\end{align*}
$$

Thus

$$
\begin{align*}
\color{#BF00FF}{\mathcal{I}
=}&\color{#BF00FF}{36\sum^\infty_{n=1}\frac{H_n}{n^52^n}-108{\rm Li}_6\left(\tfrac{1}{2}\right)+\frac{143\pi^6}{2520}-36{\rm Li}_5\left(\tfrac{1}{2}\right)\ln{2}+\frac{9}{8}\zeta(5)\ln{2}-\frac{\pi^4}{40}\ln^2{2}}\\&\color{#BF00FF}{+12\zeta^2(3)-3\pi^2\zeta(3)\ln{2}+6\zeta(3)\ln^3{2}-\frac{\pi^2}{4}\ln^4{2}+\frac{3}{20}\ln^6{2}}
\end{align*}
$$

We note that

$$
\begin{align*}
\zeta(\bar{5},1)
=&\frac{1}{24}\int^1_0\frac{\ln^4{x}\ln(1+x)}{1+x}{\rm d}x\\
=&\frac{1}{24}\int^2_1\frac{\ln{x}\ln^4(x-1)}{x}{\rm d}x\\
=&-\frac{1}{24}\int^1_\frac{1}{2}\frac{\ln{x}\ln^4(1-x)}{x}{\rm d}x+\frac{1}{6}\int^1_\frac{1}{2}\frac{\ln^2{x}\ln^3(1-x)}{x}{\rm d}x-\frac{1}{4}\int^1_\frac{1}{2}\frac{\ln^3{x}\ln^2(1-x)}{x}{\rm d}x\\
&+\frac{1}{6}\int^1_\frac{1}{2}\frac{\ln^4{x}\ln(1-x)}{x}{\rm d}x+\frac{1}{144}\ln^6{2}\\
=&\underbrace{-\frac{1}{24}\int^\frac{1}{2}_0\frac{\ln^4{x}\ln(1-x)}{1-x}{\rm d}x}_{\mathcal{J}}-3\sum^\infty_{n=1}\frac{H_n}{n^52^n}+7{\rm Li}_6\left(\tfrac{1}{2}\right)-\frac{17\pi^6}{5040}+{\rm Li}_5\left(\tfrac{1}{2}\right)\ln{2}\\
&-\frac{3}{32}\zeta(5)\ln{2}-{\rm Li}_4\left(\tfrac{1}{2}\right)\ln^2{2}+\frac{\pi^4}{480}\ln^2{2}-\frac{1}{2}\zeta^2(3)+\frac{\pi^2}{4}\zeta(3)\ln{2}-\frac{19}{24}\zeta(3)\ln^3{2}\\
&+\frac{\pi^2}{24}\ln^4{2}-\frac{17}{360}\ln^6{2}
\end{align*}
$$

since we have already derived the values of the last three integrals. For the remaining integral,

$$
\begin{align*}
\mathcal{J}
=&\frac{1}{24}\sum^\infty_{n=1}H_n\frac{\partial^4}{\partial n^4}\left(\frac{1}{(n+1)2^{n+1}}\right)\\
=&\sum^\infty_{n=1}\frac{H_n}{(n+1)^52^{n+1}}+\sum^\infty_{n=1}\frac{\ln{2}H_n}{(n+1)^42^{n+1}}+\sum^\infty_{n=1}\frac{\ln^2{2}H_n}{2(n+1)^32^{n+1}}+\sum^\infty_{n=1}\frac{\ln^3{2}H_n}{6(n+1)^22^{n+1}}\\
&+\sum^\infty_{n=1}\frac{\ln^4{2}H_n}{24(n+1)2^{n+1}}\\
=&\sum^\infty_{n=1}\frac{H_n}{n^52^n}-{\rm Li}_6\left(\tfrac{1}{2}\right)+{\rm Li}_5\left(\tfrac{1}{2}\right)\ln{2}+\frac{1}{32}\zeta(5)\ln{2}+{\rm Li}_4\left(\tfrac{1}{2}\right)\ln^2{2}-\frac{\pi^4}{720}\ln^2{2}\\
&+\frac{1}{2}\zeta(3)\ln^3{2}-\frac{\pi^2}{12}\zeta(3)\ln{2}-\frac{\pi^2}{36}\ln^4{2}+\frac{1}{40}\ln^6{2}+\frac{\pi^4}{1440}\ln^2{2}-\frac{1}{16}\zeta(3)\ln^3{2}\\&+\frac{1}{48}\ln^6{2}+\frac{1}{48}\zeta(3)\ln^3{2}-\frac{1}{36}\ln^6{2}+\frac{1}{48}\ln^6{2}\\
=&\sum^\infty_{n=1}\frac{H_n}{n^52^n}-{\rm Li}_6\left(\tfrac{1}{2}\right)+{\rm Li}_5\left(\tfrac{1}{2}\right)\ln{2}+\frac{1}{32}\zeta(5)\ln{2}+{\rm Li}_4\left(\tfrac{1}{2}\right)\ln^2{2}-\frac{\pi^4}{1440}\ln^2{2}\\
&+\frac{11}{24}\zeta(3)\ln^3{2}-\frac{\pi^2}{12}\zeta(3)\ln{2}-\frac{\pi^2}{36}\ln^4{2}+\frac{7}{180}\ln^6{2}\\
\end{align*}
$$

Hence we can express $$\zeta(\bar{5},1)$$ as

$$
\begin{align*}
\zeta(\bar{5},1)
=&-2\sum^\infty_{n=1}\frac{H_n}{n^52^n}+6{\rm Li}_6\left(\tfrac{1}{2}\right)-\frac{17\pi^6}{5040}+2{\rm Li}_5\left(\tfrac{1}{2}\right)\ln{2}-\frac{1}{16}\zeta(5)\ln{2}+\frac{\pi^4}{720}\ln^2{2}\\
&-\frac{1}{2}\zeta^2(3)-\frac{1}{3}\zeta(3)\ln^3{2}+\frac{\pi^2}{6}\zeta(3)\ln{2}+\frac{\pi^2}{72}\ln^4{2}-\frac{1}{120}\ln^6{2}
\end{align*}
$$

This implies that

$$
\begin{align*}
\sum^\infty_{n=1}\frac{H_n}{n^52^n}
=&3{\rm Li}_6\left(\tfrac{1}{2}\right)-\frac{1}{2}\zeta(\bar{5},1)-\frac{17\pi^6}{10080}+{\rm Li}_5\left(\tfrac{1}{2}\right)\ln{2}-\frac{1}{32}\zeta(5)\ln{2}+\frac{\pi^4}{1440}\ln^2{2}\\
&-\frac{1}{4}\zeta^2(3)-\frac{1}{6}\zeta(3)\ln^3{2}+\frac{\pi^2}{12}\zeta(3)\ln{2}+\frac{\pi^2}{144}\ln^4{2}-\frac{1}{240}\ln^6{2}
\end{align*}
$$

Plucking this back into the original integral, we get another form in terms of $$\zeta(\bar{5},1)$$

$$
\begin{align*}
\color{#BF00FF}{\mathcal{I}
=}&\color{#BF00FF}{-\frac{\pi^6}{252}-18\zeta(\bar{5},1)+3\zeta^2(3)}
\end{align*}
$$

This is as close to a "closed form" as I can get. The sheer number of cancellations involved in the last step makes me think that my answer could be roundabout and inefficient. Note that no known simple closed form for $$\zeta(\bar{5},1)$$ exists, implying that closed forms for higher power integrals are unlikely to exist as well.


  [1]: https://math.stackexchange.com/questions/469023/generalized-euler-sum-sum-n-1-infty-frach-nnq
  [2]: https://math.stackexchange.com/questions/604316/sum-n-1-infty-frach-nn2-2n-zeta3-frac12-log2-zeta2/605602#605602
  [3]: https://math.stackexchange.com/questions/944065/find-the-closed-form-of-sum-n-1-infty-frach-n2nn4/973408#973408