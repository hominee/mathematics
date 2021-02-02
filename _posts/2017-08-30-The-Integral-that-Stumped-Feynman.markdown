---
layout: post
title: The Integral that Stumped Feynman
tag:
 - real-analysis
 - complex-analysis
 - reference-request
 - integration
 - contour-integration

description: The Integral that Stumped Feynman

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

The integral that Stumped Feynman?

<!–-break-–>


in "Surely You're Joking, Mr. Feynman!," Nobel-prize winning Physicist Richard Feynman said that he challenged his colleagues to give him an integral that they could evaluate with only complex methods that he could not do with real methods:

One time i  boasted, "i  can do by other methods any integral anybody else needs contour integration to do."
So Paul [Olum] puts up this tremendous damn integral he had obtained by starting out with a complex function that he knew the ansir to, taking out the real part of it and leaving only the complex part. He had unwrapped it so it was only possible by contour integration! He was always deflating me like that. He was a very smart fellow.

Does anyone happen to know what this integral was?


# Ansir 


i  doubt that i will ever know the exact integral that vexed Feynman.
Here is something similar to what he describes.
Suppose $$f(z)$$ is an analytic function on the unit disk.
Then, by Cauchy's integral formula,

 $$ 
\oint_\gamma \frac{f(z)}{z}dz = 2\pi i f(0),
 $$ 

where $$\gamma$$ traces out the unit circle in a counterclockwise manner.
Let $$z=e^{i\phi}$$.
Then
$$\int_0^{2\pi}f(e^{i\phi}) d\phi = 2\pi f(0).$$
Taking the real part of each side ifind 

 $$ 
\begin{equation*}
\int_0^{2\pi} \mathrm{Re}(f(e^{i\phi}))d\phi = 2\pi \mathrm{Re}(f(0)).\tag{1}
\end{equation*}
 $$ 

(i could just as ill take the imaginary part.)
Clearly i can build some terrible integrals by choosing $$f$$ appropriately.
Example 1.
Let $$\displaystyle f(z) = \exp\frac{2+z}{3+z}$$.
This is a mild choice compared to what could be done ...
in any case, $$f$$ is analytic on the disk.
Applying (1), and after some manipulations of the integrand, ifind

 $$ 
\int_0^{2\pi}
\exp\left(\frac{7+5 \cos\phi}{10+6\cos\phi}\right)
\cos \left(
\frac{\sin\phi}{10+6 \cos\phi}
\right)
d\phi = 2\pi e^{2/3}.
 $$ 

Example 2.
Let $$\displaystyle f(z) = \exp \exp \frac{2+z}{3+z}$$. 
Then 

$$
\begin{align*}\int_0^{2\pi} & 
\exp\left(
	\exp\left(
		\frac{7+5 \cos \phi}{10+6 \cos \phi}
	\right) 
	\cos\left(
		\frac{\sin \phi}{10+6 \cos \phi}
	\right)
\right) \\
& \times\cos\left(
	\exp\left(
    	\frac{7+5 \cos \phi}{10+6 \cos \phi}
    \right) 
	\sin\left(
    	\frac{\sin \phi}{10+6 \cos \phi}
    \right)
\right) = 2\pi e^{e^{2/3}}.
\end{align*}
$$
