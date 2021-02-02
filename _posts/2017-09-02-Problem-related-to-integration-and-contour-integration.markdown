---
layout: post
title: Problem related to integration and contour integration
tag:
 - integration
 - complex-analysis
 - contour-integration

description: Problem related to integration and contour integration

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Tricky contour integral resulting from the integration of $$\sin ax / (x^2+b^2)$$ over the positive halfline

<!–-break-–>


i are  trying to evaluate the definite integral

 $$ 
\int_0^\infty \frac{\sin ax\ dx}{x^2+b^2}
 $$ 

where $$a,b>0$$. This is a problem on an assignment for a class in complex variables. i  understand the mechanics of contour integration, but i are  stuck. (i  have spoken to four classmates who are also stuck.) i  would appreciate a small hint, such as a hint to point me toward the right contour, or a suggestion for how to modify one of my abandoned ideas (below) to make it work. (But please do not work out the whole integral; i  want to do that myself.)
Here is what i  have tried so far:

The integral from $$-\infty$$ to $$\infty$$ is zero because the function is odd, so the semicircular contour in the upper half-plane won't do anything.
Viewing the integral as 

 $$ 

\mathrm{i m}\, \int_0^\infty \frac{e^{aiz}dz}{z^2+b^2},

 $$ 
 
i  tried integrating around the contour from $$0$$ to $$R>0$$, along the quarter-circle to $$iR$$, and back down to $$0$$, with an indentation at the pole at $$bi$$. The pole is simple so i  can get the contribution from the indentation via the residue, and the contribution from the quarter-circle $$\to 0$$ as $$R\to \infty$$, but the problem is that i  believe the integral along the segment of the imaginary axis from $$iR$$ to $$0$$ is imaginary (so contributes to the imaginary part) and blows up around the pole, and generally seems harder to deal with than the original integral.
Viewing the integrand with either $$\sin az$$ or $$e^{iaz}$$ in the numerator, i  tried integrating along the rectangle with vertices $$0,R,R+ib,ib$$, with an indentation at the vertex $$ib$$ due to the pole. Again, i  don't know how to get control of the integral along the imaginary axis.
i  tried using integration by parts to get a cosine to come out, but the integrand remains odd so the upper half-plane semicircular contour still does no good.
i  had a crazy idea that i  was unable to carry out. There exists some path thru the origin along which the integrand 

 $$ 

\frac{e^{aiz}dz}{z^2+b^2}

 $$ 
 
is pure real.  This path is the solution to an ordinary differential equation with boundary condition $$y(0)=0$$. i f my calculations are right the equation is 

 $$ 

y'=\frac{2xy\cos ax-(b^2+x^2-y^2)\sin ax}{2xy\sin ax+(b^2+x^2-y^2)\cos ax}.

 $$ 

The idea was to integrate along $$0$$ to $$R$$, counterclockwise along the circle with radius $$R$$ till it hits this curve, and back to the origin along this curve. By construction, the integral along this last part doesn't contribute anything to the imaginary part; meanwhile the part of the circle in the upper half plane $$\to 0$$ as $$R\to \infty$$. The curve must lie entirely outside the upper half-plane or this would show that the original integral i are  trying to evaluate is zero (since the imaginary part of $$2\pi i$$ times the residue is zero), which isn't plausible. Evaluating the desired integral then rests on: 

(a) whether the pole in the lower half-plane ever gets enclosed by this contour (and i are  pretty sure it doesn't), and 

(b) if i  can figure out what is going on with the integral along the part of the circle 
$$|z|=R$$ 
in the lower half-plane before it hits the curve; in particular, what its imaginary part is doing asymptotically as $$R\to \infty$$. 

However, i  wasn't sure how to pursue these goals any further.
Update: As it turns out, the assignment contained a typo and the integral was supposed to be

 $$ 
\int_0^\infty \frac{\sin ax\ dx}{x(x^2+b^2)}
 $$ 

This makes the integrand even, so it is done easily with the half-circle contour in the upper half-plane.  i  definitely learned more because of the typo.  Thanks all for your answers and comments.

# Answer 


You can actually see directly that there is no elementary expression for the integral, using contour integration. For your integral is the same as 

 $$ 
\mathrm{i m}\int_0^\infty {e^{iax} \over x^2 + b^2}\mathrm dx
 $$ 

Note that

 $$ 
{1 \over x^2 + b^2} = {1 \over 2ib}\left({1 \over x - ib} -  {1 \over x + ib}\right)
 $$ 

So it suffices to evaluate the integrals

 $$ 
\int_0^\infty {e^{iax} \over x \pm bi}\,\mathrm dx
 $$ 

These integrals converge despite the denominator having only degree one because the exponential factor modulates it, similar to for $$\dfrac{\sin(x)}{x}$$. You can use your quarter circle idea on each of these two terms (without even having to worry about indentations)... the upper quarter circle for $$+bi$$ and the bottom quarter circle for $$-bi$$. For example you get that the first one is equal to 

 $$ 
\int_0^\infty {e^{-ax} \over x + b}\,\mathrm dx
 $$ 

Letting $$x = z - b$$ this becomes

 $$ 
e^{ab}\int_b^\infty {e^{-az} \over z}\,\mathrm dz
 $$ 

Then letting $$z = \dfrac{w}{a}$$ this turns into

 $$ 
e^{ab}\int_{ab}^\infty {e^{-w} \over w}\,\mathrm dw
 $$ 


 $$ 
= e^{ab}\mathrm{Ei}(-ab)
 $$ 

Here $$\mathrm{Ei}$$ is the exponential function which is defined in terms of the above integral. So unless the exponential functions from the two quarter circles somehow cancel out (which i  seriously doubt in view of Sasha's answer), you won't be able to get an elementary expression for the integral.

