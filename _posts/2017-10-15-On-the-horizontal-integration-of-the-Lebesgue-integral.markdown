---
layout: post
title: On the horizontal integration of the Lebesgue integral
tag:
 - integration
 - lebesgue-integral
 - riemann-sum

description: On the horizontal integration of the Lebesgue integral

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

On the horizontal integration of the Lebesgue integral

<!–-break-–>


we are  studying Lebesgue integral and its difference with respect to the Riemann one.
we are  reading that the key difference (at least graphically speaking) is that the first slices the function horizontally, while the latter works vertically. This concept is summed in the figure.  

In Riemann integral definition the graphical procedure is trivial, as we have


$$

\int f(x) dx= \lim_{x\to+\infty}\sum_{i=1}^n f(x_i) (x_i-x_{i-1})

$$


and so the $$(x_i-x_{i-1})$$ is the basis of my rectangle while $$f(x_i)$$ is the height.
In Lebesgue we have (following Rudin pg.19)


$$

\int_E f d\mu = \sup\int_E s d\mu = \sup \sum_{i=1}^n \alpha_i \mu(A_i \bigcap E_i)

$$


but we can't get in any formulation of the Lebesgue integral which is the basis of the rectangle and which is the height, also because in Lebesgue there is no $$x$$ in the integral.
we think that $$d\mu$$ in this case become the small height of each rectangle but we don't figure out how $$f$$, which was the height in Riemann, now could become the basis. Vice versa, if $$d\mu$$ is still the basis and we integrate according to the variation of $$\mu$$, this technique does not seem to cut horizontally the function.
What is the idea behind this horizontal integration?
we read Lebesgue integral basics a possible answer but still we can't figured out a completely clear explanation.
Any suggestion is really appreciated.

# Answer 


In your example, $$\mu$$ would represent the base of the rectangle. But that's not the important part. The important part is the definition of the set you are taking the measure of.
Let's look at your image. Imagine each rectangle is height of exactly 1 unit. We might define the sets like this:


$$

E_n = \{ x : n \le f(x) < n+1\}.

$$


We look at the measure of each of these sets.
For $$n = 1$$, the set of numbers in $$E_1$$ is exactly the bottom-most rectangle projected onto the $$x$$-axis. It has measure $$\mu(E_1)$$. The second rectangle from the bottom is $$E_2$$, and so forth.
Each of these rectangles has height $$1$$, so we can approximate the integral as


$$

\int f\, d\mu = \sum 1\cdot \mu(E_n).

$$


What might be stumbling you up is that you are expecting that the location of those horizontal slices, as shown in the picture, is somehow embedded within the sum. It is not; rather, the rectangles are essentially sets, pulled upwards by steps of $$1$$.
Of course, we need not choose height $$1$$, and it need not be uniform. Instead, we can choose height $$a_n$$.

