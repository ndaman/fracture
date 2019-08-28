# AE837
## Advanced Mechanics of Damage Tolerance
Dr. Nicholas Smith<br/>
Wichita State University, Department of Aerospace Engineering
September 10, 2019

----
## upcoming schedule

-		Sep 10 - Stress Intensity Solutions
-   Sep 12 - Finite Size Effects, K-Dominance, HW 2 Due
-   Sep 17 - Fracture Criterion 
-   Sep 19 - Exam Review, HW 3 Due

----
## outline

<!-- vim-markdown-toc GFM -->

* crack with discrete load
* arbitrary face loads
* edge crack
* finite specimen effects

<!-- vim-markdown-toc -->

---
# crack with discrete load

----
## fundamental stress intensity solutions

-   In general, we will not have infinite plates with uniform loading
-   We can combine previous results with superposition and general elasticity solution techniques to find more useful cases

![an illustration of the principle of superposition as used in fracture mechanics](..\images\superposition.png)

----
## concentrated splitting forces

![a pair of splitting forces acting inside the crack](..\images\splitting-forces.png)

----
## splitting forces

-   Consider the case shown on the previous slide, with concentrated splitting forces of magnitude *P* acting some distance *x=b* from the center of a centered crack in an infinite plate
-   The boundary conditions for this problem are
-   <!-- .element style="list-style-type:none" --> `$$\begin{align}
	\sigma_{yy} &= 0 \qquad \text{at} \qquad |x| \le a, x \ne b, \text{ and } y=0\\
	\int_{-a}^a \sigma_{yy} dx &= -P \qquad \text{at} \qquad y=0^{+} \text{ and } y=0^{-}\\
	\sigma_{xy} &= 0 \qquad \text{at} \qquad |x| \le a, \text{ and } y=0\\
\sigma_{xx} &= \sigma_{yy} = \sigma_{xy} \to 0 \qquad \text{at} \qquad x^2 + y^2 \to \infty \end{align}$$`

----
## splitting forces

-   Consider the Westergaard function
-   <!-- .element style="list-style-type:none" --> `$$ Z_I = \frac{P}{\pi(z-b)}\sqrt{\frac{a^2-b^2}{z^2-a^2}}$$`
-   We find that the boundary conditions are satisfied and the stress intensity factor at the right tip is
-   <!-- .element style="list-style-type:none" --> `$$ K_I = \frac{P}{\sqrt{\pi a}}\sqrt{\frac{a+b}{a-b}} $$`
-   And the left tip:
-   <!-- .element style="list-style-type:none" --> `$$ K_I = \frac{P}{\sqrt{\pi a}}\sqrt{\frac{a-b}{a+b}} $$`

----
## concentrated shear

-   We can formulate a similar problem for a concentrated shear force, *Q*, acting along the crack face
-   This gives boundary conditions of:
-   <!-- .element style="list-style-type:none" --> `$$\begin{align}
	\sigma_{xy} &= 0 \qquad \text{at} \qquad |x| \le a, x \ne b, \text{ and } y=0\\
	\int_{-a}^a \sigma_{xy} dx = -Q \qquad \text{at} \qquad y=0^{+} \text{ and } y=0^{-}\\
	\sigma_{yy} = 0 \qquad \text{at} \qquad |x| \le a, \text{ and } y=0\\
\sigma_{xx} = \sigma_{yy} = \sigma_{xy} \to 0 \qquad \text{at} \qquad x^2 + y^2 \to \infty \end{align}$$`

----
## concentrated shear

-   We can show that the following Westergaard function can satisfy the boundary conditions
-   <!-- .element style="list-style-type:none" --> `$$ Z_{II} = \frac{Q}{\pi(z-b)}\sqrt{\frac{a^2 - b^2}{z^2-a^2}}$$`
-   Which gives the following stress intensity factors
-   <!-- .element style="list-style-type:none" --> `$$ K_{II} = \frac{Q}{\sqrt{\pi a}}\sqrt{\frac{a+b}{a-b}} \text{ right }$$`
-   <!-- .element style="list-style-type:none" --> `$$ K_{II} = \frac{Q}{\sqrt{\pi a}}\sqrt{\frac{a-b}{a+b}} \text{ left }$$`

---
# arbitrary face loads

----
## arbitrary face load

-   Assume a crack is subjected to some arbitrary distributed pressure, *p(x)* at the crack face
-   To find the stress intensity factor, we consider an infinitesimal element *dξ* at *x=ξ* on the crack face
-   The force exerted on this element is *p(ξ) dξ* 

----
## arbitrary face load

-   We can now use the previous solution for a concentrated force and consider the incremental effect of many infinitesimally small forces
-   <!-- .element style="list-style-type:none" --> `$$ d K_I = \frac{p(ξ)dξ}{\sqrt{\pi a}}\sqrt{\frac{a+ξ}{a-ξ}} \text { right }$$`
-   <!-- .element style="list-style-type:none" --> `$$ d K_I = \frac{p(ξ)dξ}{\sqrt{\pi a}}\sqrt{\frac{a-ξ}{a+ξ}} \text { left }$$`

----
## arbitrary face load

-   We can find the total stress intensity factor by integrating from `$ξ = -a to a$`
-   The same procedure can be used to find the stress intensity for arbitrary shear loading along the crack face

---
# edge crack

----
## edge crack

-   We can also consider the case of splitting forces on an edge crack

![an edge cracked specimen with splitting forces applied a distance of b from the crack tip](..\images\single-edge.png)

----
## edge crack

-   The boundary conditions for this problem are:
-   <!-- .element style="list-style-type:none" --> `$$\begin{align}
	\sigma_{yy} &= 0 \qquad \text{at} \qquad -\infty < x < 0, x \ne b, \text{ and } y=0\\
	\int_{-a}^a \sigma_{yy} dx = -P \qquad \text{at} \qquad y=0^{+} \text{ and } y=0^{-}\\
	\sigma_{xy} = 0 \qquad \text{at} -\infty < x < 0 \text{ and } y=0\\
\sigma_{xx} = \sigma_{yy} = \sigma_{xy} \to 0 \qquad \text{at} \qquad x^2 + y^2 \to \infty \end{align}$$`

----
## edge crack

-   The Westergaard function to solve this problem is given by:
-   <!-- .element style="list-style-type:none" --> `$$ Z_{I} = \frac{P}{\pi(z+b)}\sqrt{\frac{b}{z}}$$`
-   Which gives a stress intensity factor of
-   <!-- .element style="list-style-type:none" --> `$$ K_I = P \sqrt{\frac{2}{\pi b}}`

---
# finite specimen effects

----
## finite specimen effects

-   Up to this point, we have considered infinitely large panels
-   In general, the effect of finite size is modeled using numerical techniques, such as finite elements
-   These corrections will generally take the form of some dimensionless factor that is multiplied with the infinite stress intensity factor
-   <!-- .element style="list-style-type:none" --> `$$ K_I = \sigma \sqrt{\pi a} F(a/b, a/H) $$`

