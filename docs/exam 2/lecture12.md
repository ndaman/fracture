# AE837
## Advanced Mechanics of Damage Tolerance
Dr. Nicholas Smith<br/>
Wichita State University, Department of Aerospace Engineering
October 1, 2019

----
## upcoming schedule

-   Oct 1 - Virtual Crack Closure, J-integral
-   Oct 3 - J-Integral, Cohesive Zone
-   Oct 8 - eXtended Finite Element Method (XFEM)
-   Oct 10 - XFEM, Homework 4 Due
-   Oct 15 - Fall Break (no class)

----
## outline

<!-- vim-markdown-toc GFM -->

* comsol setup
* finite element demo
* virtual crack closure
* j-integral

<!-- vim-markdown-toc -->

---
# comsol setup

----
## comsol install

-   I need your computer's "hostname" to whitelist you
-   You can download COMSOL [here](https://drive.google.com/open?id=1IT4IlM9j0nTDVDE9L8QhhhpKa7RXEjyw)
-   To run COMSOL, you either need to be on campus or you need to use a [VPN](https://vpn.wichita.edu) (to have an on-campus IP address)
-   When installing, choose "License Format -> port number @ hostname"
	-   port number 1718
	-   aecomsol.wichita.edu as hostname

----
## comsol tutorials

-   If you have not used COMSOL before, they have a pretty good library of tutorials
-   For example, to see how they perform the J-integral you can follow [this](https://www.comsol.com/model/single-edge-crack-988) tutorial
-   The [application gallery](https://www.comsol.com/models) has many more documented examples you can follow along with

---
# finite element demo

----
## objectives

-   We will use the direct method to find the stress intensity factor, $K_I$, of an edge crack
-   The analytic solution is

$$ K_I = (1.122 - 0.231 \frac{a}{W} + 10.55 \left(\frac{a}{W}\right)^2 - 21.71 \left(\frac{a}{W}\right)^3)\sigma \sqrt{\pi a} $$

-   And $K_I$ in terms of stress and displacement is

$$ \begin{aligned}
	K_I &= \sigma_{yy}\sqrt{2\pi x}\\
	K_I &= \frac{2\mu u_y}{\kappa + 1} \frac{2\pi x}{x}
\end{aligned}$$

----
## boundary conditions

-   The first thing to consider is symmetry
-   It is easiest to cut our model in half vertically and treat it as symmetric
-   If we don't do this, we need a way of cutting the nodes where the crack is (or joining them where it isn't)
-   For an edge crack, we will have a symmetry condition on the symmetric portion and a boundary load on top, otherwise everything else is traction free

----
## screencast

<section>
	<video controls id="directmethod" src="../images/direct-method.mp4" type="video/mp4" style="height: 50%; width: 50%;" />
</section>

---
# virtual crack closure

----
## vcct

-   As can be seen from the results previously found, the direct method leaves something to be desired, and is very mesh-dependent
-   An alternative approach is to use the same energy method (virtual crack closure) that we used to relate $G_I$ to $K_I$ in finite elements
-   We consider two cases, one before and one after some crack extension, $da$

----
## vcct illustration

![illustration of the vcct method](../images/vcct.png)

----
## vcct

-   

---
# j-integral
