# AE837
## Advanced Mechanics of Damage Tolerance
Dr. Nicholas Smith<br/>
Wichita State University, Department of Aerospace Engineering
October 17, 2019

----
## upcoming schedule

-   Oct 17 - Mixed-Mode Fracture, Homework 4 & 5 Due
-   Oct 22 - XFEM
-   Oct 24 - XFEM, Project Abstract Due
-   Oct 29 - Crack Tip Plasticity

----
## outline
 
<!-- vim-markdown-toc GFM -->

* elliptical model
* maximum stress criterion
* strain energy criterion
* energy release rate criterion
* experimental work

<!-- vim-markdown-toc -->

---
# elliptical model

----
## simple approach

-   Some of the first work on mixed-mode fracture used a phenomenological approach
-   We know that fracture occurs when $K_I = K_{Ic}$ or $G_I = G_{Ic}$
-   We might assume some function of either $K_I$ and $K_{II}$ or $G_{I}$ and $G_{II}$ would cause fracture upon reaching some critical value

----
## total energy release rate

-   The total energy release rate was first suggested for this purpose with

$$ G = \frac{\kappa+1}{8\mu}(K_I^2 + K_{II}^2) $$

-   Rearranging terms and making some substitutions gives the following, which we can see is the equation of a circle in the $K_I - K_{II}$ plane

$$ \left( \frac{K_I}{K_{c}} \right)^2 + \left( \frac{K_II}{K_c} \right)^2 = 1 $$

----
## results

-   While the total energy release method makes some physical sense, it does not match experiments
-   It would predict $K_{IC} = K_{IIC}$, which is not the case
-   Instead we can modify the equation to an ellipse in the $K_I - K_{II}$ plane

$$ \left( \frac{K_I}{K_{Ic}} \right)^2 + \left( \frac{K_II}{K_{IIc}} \right)^2 = 1 $$

---
# maximum stress criterion

---
# strain energy criterion

---
# energy release rate criterion

---
# experimental work
