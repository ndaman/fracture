# AE837
## Advanced Mechanics of Damage Tolerance
Dr. Nicholas Smith<br/>
Wichita State University, Department of Aerospace Engineering
November 21, 2019

----
## upcoming schedule

-   Nov 21 - Peridynamics and Advanced Numerical Methods
-   Nov 26 - Impact Damage and Journal Club
-   Nov 28 - No Class (Thanksgiving)
-   Dec 3 - Project Work Day
-   Dec 5 - Interfacial Cracks or Project Work Day

----
## outline
 
<!-- vim-markdown-toc GFM -->

* peridynamics
* element free galerkin

<!-- vim-markdown-toc -->

---
# peridynamics

----
## peridynamics

-   new continuum mechanics formulation to account for discontinuity
-   a point interacts with other points some distance $\delta$ away
-   this is known as the "horizon" and points within it are in the same "family"
-   strain energy at the point depends on deformation of its family

----
## external links

-   Sandia page by original author of peridynamics [link](https://www.sandia.gov/~sasilli/)
-   LS-DYNA examples [link](https://www.lstc-cmmg.org/ex-meshfree)

---
# element free galerkin

----
## efg

-   based on moving least square interpolation
-   requires nodal data, but no element connectivity
-   geometry is described with a set of nodes, exterior boundaries and interior boundaries (cracks)
-   full paper describing the method [pdf](../handouts/efg.pdf)
