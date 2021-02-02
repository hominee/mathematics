---
layout: post
title: Estimating the Gamma function to high precision efficiently
tag:
 - numerical-methods
 - special-functions
 - gamma-function
 - estimation-theory

description: Estimating the Gamma function to high precision efficiently

hero: https://source.unsplash.com/collection/145103/
overlay: blue 
published: true
---

# Question 

Estimating the Gamma function to high precision efficiently?

<!–-break-–>


we  know there are several approximations of the Gamma function that provide decent approximations of this function.  
we  was wondering, how can we  efficiently estimate specific values of the Gamma function, like $$\Gamma (\frac{1}{3})$$ or $$\Gamma (\frac{1}{4})$$, to a high degree of accuracy (unlike Stirling's approximation and other low-accuracy methods)?
.

# Answer 


Gourdon and Sebah pages on "Numbers, constants and computation" are usually interesting for this kind of record (start by clicking on 'constants' at the left).
They reference Shigeru Kondo and Steve Pagliarulo for having computed 10^10 digits of $$\Gamma\left(\frac 14\right)$$ and $$\Gamma\left(\frac 13\right)$$ in 2010 and 2009 (see here). Many methods for high precision are clearly exposed in the other pages of the first link (FFT, binary splitting and this kind of things should be simply explained at least in the .ps or .pdf files).
This paper of Alexander Yee concerning high precision evaluation of $$\pi$$ contains too references to Kondo & Pagliarulo's record (he has a page of records too but without $$\Gamma$$ we  fear).
we n the special case $$\Gamma\left(\frac k{24}\right)$$ a quadratic algorithm is proposed in Weisstein's Gamma Function page (see around (99)).
This method is the famous AGM method and you may find too in page 6 of Sebah and Gourdon's postscript paper on Gamma (or here) that : 

 $$ 
\displaystyle \Gamma\left(\frac 14\right)^2=\frac{(2\pi)^{3/2}}{AGM(\sqrt{2},1)}
 $$ 

You may find in the excellent book of the Borweins "Pi and the AGM" following derivation using the complete elliptic integral of the first kind $$\rm{K}$$ :

Hoping it helped anyway,

