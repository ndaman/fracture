# AE837
## Advanced Mechanics of Damage Tolerance
Dr. Nicholas Smith<br/>
Wichita State University, Department of Aerospace Engineering
August 29, 2019

----
## upcoming schedule

-   Aug 29 - Griffith Fracture
-		Sep 3 - Complex Airy Stress
-		Sep 5 - Mode II and III Westergaard, Homework 1 Due
-		Sep 10 - Stress Intensity Solutions
-   Sep 12 - Finite Size Effects, K-Dominance, HW 2 Due


----
## outline

<!-- vim-markdown-toc GFM -->

* relation among energies
* example - double contilever beam

<!-- vim-markdown-toc -->

---
# relation among energies

----
## energy balance

-   Griffith’s theory is founded on the principle of energy balance
-   During crack extension, the external work done, *dW*<sub>*e*</sub> must equal the increment of surface energy, *dW*<sub>*s*</sub>, and the increment of elastic strain energy, *dU*
- <!-- .element style="list-style-type:none" -->   
_dW_<sub>*s*</sub> + *dU* = *dW*<sub>*e*</sub>

----
## energy balance

-   For a conservative field we can write this as
- <!-- .element style="list-style-type:none" -->   
$$\\frac{\\partial}{\\partial a} (W\_s + U + V) = 0$$
-   Where a negative potential, *V*, implies positive external work done *dW*<sub>*e*</sub>

----
## example

![single edge notched tension specimen](../images/sent.png) <!-- .element width="70%" -->

----
## example

-   The displacement at the top edge will be proportional to the applied load by some elastic compliance of the specimen
- <!-- .element style="list-style-type:none" -->   
_δ_ = *SP*
-   Note that this compliance, *S*, will be a function of the crack length, *a*
-   The strain energy can be expressed as
- <!-- .element style="list-style-type:none" -->   
$$U = \\int\_{\\delta=0}^{\\delta=SP} P d\\delta = \\int\_{\\delta=0}^{\\delta=SP} \\frac{\\delta}{S} d\\delta$$

----
## example

-   After integrating
- <!-- .element style="list-style-type:none" -->   
$$U = \\frac{1}{2S}(\\delta^2)|\_0^{SP} = \\frac{1}{2}SP^2$$

----
## example

-   To find the incremental strain energy increase (where both *P* and *S* should be treated as variable), we find
- <!-- .element style="list-style-type:none" -->   
$$dU = \\frac{1}{2}P^2 dS + SP dP$$
-   We will now consider two loading cases, one with fixed displacement and the other with fixed loading force

----
## fixed displacement

-   Under constant displacement we have
- <!-- .element style="list-style-type:none" -->   
_δ_ = *SP* = constant
-   This means that the derivative of displacement will be zero, hence
- <!-- .element style="list-style-type:none" -->   
_dδ_ = *SdP* + *PdS* = 0
-   and
- <!-- .element style="list-style-type:none" -->   
_SdP_ = −*PdS*

----
## fixed displacement

-   Substituting into the previous equation gives
- <!-- .element style="list-style-type:none" -->   
$$dU = -\\frac{1}{2}P^2 dS$$
-   Since *dδ* = 0, the external work, *dW*<sub>*e*</sub> = 0 and we find
- <!-- .element style="list-style-type:none" -->   
$$dW\_s = -dU = \\frac{1}{2} P^2 dS$$

----
## fixed load

-   If instead of fixing displacement we fix the applied load we have
- <!-- .element style="list-style-type:none" -->   
_dP_ = 0
-   Which gives
- <!-- .element style="list-style-type:none" -->   
$$dU = \\frac{1}{2}P^2 dS$$
-   The strain energy increases (while under fixed displacement it decreased)

----
## fixed load

-   Further, we can find the external work done as
- <!-- .element style="list-style-type:none" -->   
_dW_<sub>*e*</sub> = *Pdδ* = *P*<sup>2</sup>*dS*
-   And thus, from energy balance, we find the surface energy
- <!-- .element style="list-style-type:none" -->   
$$dW\_s = \\frac{1}{2}P^2 dS$$
-   In this case the external work is equally split between strain energy and surface energy

----
## comparison

-   In both cases, the energy released is *dW* = *dW*<sub>*e*</sub> − *dU*

$$\\begin{aligned}
    dW &= 0 - (-\\frac{1}{2} P^2 dS) &\\text{fixed displacement}\\\\
    dW &= P^2 dS - \\frac{1}{2}P^2 dS &\\text{fixed load}
\\end{aligned}$$

-   And we see that the energy released is independent of the load type

---
# example - double contilever beam

----
## example - double cantilever beam

![double cantilever beam](../images/dcb.png) <!-- .element width="80%" -->

----
## example - stable crack 

-   During experimental characterization, it is often desirable to measure crack growth
-   To do this accurately, the crack growth must be stable
-   For crack growth to be stable, the strain energy should decrease as crack length increases (∂*G*/∂*a* ≤ 0)
-   If we recall *G* for the Double-Cantilever Beam (DCB) specimen
- <!-- .element style="list-style-type:none" -->   
$$G = \\frac{P^2a^2}{bEI}$$

----
## example - stable crack 

-   Under fixed-load conditions, we find
- <!-- .element style="list-style-type:none" -->   
$$\\frac{dG}{da} = \\frac{2P^2a}{bEI}$$
-   This is always positive, and thus results in unstable crack growth
-   Under fixed-displacement conditions, we substitute for *P* in terms of displacement using *P* = *δ*/*S*

----
## example - stable crack

-   From beam theory we can express *S* more precisely as
- <!-- .element style="list-style-type:none" -->   
$$S = \\frac{2a^3}{3EI}$$
- <!-- .element style="list-style-type:none" -->    
$$\\frac{dG}{da} = -\\frac{9\\delta^2EI}{ba^5}$$
-   Which is always stable, so for DCB tests, displacement control is generally used

----
## example - peel of thin film

![example problem demonstrating peeling of a thin film](../images/film-peel.png) <!-- .element width="70%" -->
