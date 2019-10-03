 # AE837
## Advanced Mechanics of Damage Tolerance
Dr. Nicholas Smith<br/>
Wichita State University, Department of Aerospace Engineering
October 3, 2019

----
## upcoming schedule

-   Oct 3 - J-Integral, Cohesive Zone
-   Oct 8 - eXtended Finite Element Method (XFEM)
-   Oct 10 - XFEM, Homework 4 Due
-   Oct 15 - Fall Break (no class)

----
## outline
 
<!-- vim-markdown-toc GFM -->

* j-integral
* cohesive zone

<!-- vim-markdown-toc -->

---
# j-integral

----
## j-integral

-   The J-Integral is defined as

$$ \int_\Lambda \left( W dy - T_i \frac{\partial u_i}{\partial x} d\Lambda \right ) = \int_\Lambda \left( W n_1 - \sigma_{ij} \frac{\partial u_i}{\partial x} n_j \right ) d\Lambda $$

-   \Lambda is an arbitrary contour beginning at the lower crack surface and end on the upper crack surface

----
## j-integral

![illustration of path choice of J-integral](../images/j%2Dintegral.png)

----
## j-integral

-   The J-integral is path-idependent and represents the strain energy release rate
-   We can prove this using the following principles from elasticity

$$ \begin{aligned}
	\sigma_{ij,j} &= 0 \qquad \text{(equilibrium)} \\\\
	e_{ij} &= \frac{1}{2} (u_{i,j} + u_{j,i}) \qquad \text{(strain-displacement)} \\\\
	\sigma_{ij} &= \frac{\partial W}{\partial e_{ij}} \qquad \text{(stress-strain)}
\end{aligned}$$

----
## j-integral

![example countour for j-integral](../images/j%2Dintegral%2Dexample.png)

----
## j-integral

-   $A_0$ represents the area enclosed by the contour
-   The potential energy can then be expressed as

$$ \iint_{A_0} W dX dY - \int_{\Lambda_t} T_i u_i d\Lambda $$

-   (worked on board)

----
## examples

![example j-integral calculation](../images/example%2D4%2D1.png)
 

----
## finite element

-   many solvers have a built-in method for calculating the J-integral
-   ABAQUS
-   In COMSOL, we have some nice documentation for how to do it, but we need to set up the integral manually

----
## fea implementation

-   if you are using some other software, check the documentation, it may not be set up to calculate the J-integral for a symmetric model
-   In COMSOL, we will only be calculating half of the J-integral (then we will double it)
-   First we model the contours, then we will define local variables (the normal vector along various sections), local integrations (around the contour) and finally calculate $J$ and $K$

----
## screencast I

<section>
	<video controls id="jintegral1" src="../images/jintegral1.mp4" type="video/mp4" style="height: 50%; width: 50%;" />
</section>

----
## screencast II

<section>
	<video controls id="jintegral2" src="../images/jintegral2.mp4" type="video/mp4" style="height: 50%; width: 50%;" />
</section> 

---
# cohesive zone

----
## cohesive zone

-   
