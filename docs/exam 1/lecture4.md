<span>upcoming schedule</span>

-   Aug 31 - Griffith Fracture

-   Sep 5 - Elastic Stress Field, Homework 1 Due

-   Sep 7 - Elastic Stress Field

-   Sep 12 - Elastic Stress Field

relation among energies
=======================

<span>energy balance</span>

-   Griffith’s theory is founded on the principle of energy balance

-   During crack extension, the external work done, *d**W*<sub>*e*</sub> must equal the increment of surface energy, *d**W*<sub>*s*</sub>, and the increment of elastic strain energy, *d**U*
    *d**W*<sub>*s*</sub> + *d**U* = *d**W*<sub>*e*</sub>

-   For a conservative field we can write this as
    $$\\frac{\\partial}{\\partial a} (W\_s + U + V) = 0$$

-   Where a negative potential, *V*, implies positive external work done *d**W*<sub>*e*</sub>

<span>example</span>

<img src="../Figures/sent" alt="Single edge crack specimen" style="width:70.0%" />

<span>example</span>

-   The displacement at the top edge will be proportional to the applied load by some elastic compliance of the specimen
    *δ* = *S**P*

-   Note that this compliance, *S*, will be a function of the crack length, *a*

-   The strain energy can be expressed as
    $$U = \\int\_{\\delta=0}^{\\delta=SP} P d\\delta = \\int\_{\\delta=0}^{\\delta=SP} \\frac{\\delta}{S} d\\delta$$

-   After integrating
    $$U = \\frac{1}{2S}(\\delta^2)|\_0^{SP} = \\frac{1}{2}SP^2$$

<span>example</span>

-   To find the incremental strain energy increase (where both *P* and *S* should be treated as variable), we find
    $$dU = \\frac{1}{2}P^2 dS + SP dP
                \\label{eq:du}$$

-   We will now consider two loading cases, one with fixed displacement and the other with fixed loading force

<span>fixed displacement</span>

-   Under constant displacement we have
    *δ* = *S**P* = constant

-   This means that the derivative of displacement will be zero, hence
    *d**δ* = *S**d**P* + *P**d**S* = 0

-   and
    *S**d**P* = −*P**d**S*

<span>fixed displacement</span>

-   Substituting into the \[eq:du\] gives
    $$dU = -\\frac{1}{2}P^2 dS$$

-   Since *d**δ* = 0, the external work, *d**W*<sub>*e*</sub> = 0 and we find
    $$dW\_s = -dU = \\frac{1}{2} P^2 dS$$

<span>fixed load</span>

-   If instead of fixing displacement we fix the applied load we have
    *d**P* = 0

-   Which gives
    $$dU = \\frac{1}{2}P^2 dS$$

-   The strain energy increases (while under fixed displacement it decreased)

<span>fixed load</span>

-   Further, we can find the external work done as
    *d**W*<sub>*e*</sub> = *P**d**δ* = *P*<sup>2</sup>*d**S*

-   And thus, from energy balance, we find the surface energy
    $$dW\_s = \\frac{1}{2}P^2 dS$$

-   In this case the external work is equally split between strain energy and surface energy

<span>comparison</span>

-   In both cases, the energy released is *d**W* = *d**W*<sub>*e*</sub> − *d**U*
    $$\\begin{aligned}
                dW &= 0 - (-\\frac{1}{2} P^2 dS) &\\text{fixed displacement}\\\\
                dW &= P^2 dS - \\frac{1}{2}P^2 dS &\\text{fixed load}
            \\end{aligned}$$

-   And we see that the energy released is independent of the load type

<span>example - stable crack growth</span>

-   During experimental characterization, it is often desirable to measure crack growth

-   To do this accurately, the crack growth must be stable

-   For crack growth to be stable, the strain energy should decrease as crack length increases (∂*G*/∂*a* ≤ 0)

-   If we recall *G* for the Double-Cantilever Beam (DCB) specimen
    $$G = \\frac{P^2a^2}{bEI}$$

<span>example - stable crack growth</span>

-   Under fixed-load conditions, we find
    $$\\frac{dG}{da} = \\frac{2P^2a}{bEI}$$

-   This is always positive, and thus results in unstable crack growth

-   Under fixed-displacement conditions, we substitute for *P* in terms of displacement using *P* = *δ*/*S*

-   From beam theory we can express *S* more precisely as
    $$S = \\frac{2a^3}{3EI}$$
    $$\\frac{dG}{da} = -\\frac{9\\delta^2EI}{ba^5}$$

-   Which is always stable, so for DCB tests, displacement control is generally used

<span>example - peel of thin film</span>

<img src="../Figures/film-peel" alt="Peeling of a thin film" style="width:70.0%" />
