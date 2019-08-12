<span>upcoming schedule</span>

-   Aug 29 - Griffith Fracture

-   Aug 31 - Griffith Fracture

-   Sep 5 - Elastic Stress Field, Homework 1 Due

-   Sep 7 - Elastic Stress Field

theoretical strength
====================

<span>theoretical strength</span>

-   We can (theoretically) predict the strength of a material from the strength of its atomic bonds

-   As the distance between atoms increases (strain) so does the attractive force between them (stress) until some critical distance when they are no longer attracted to one another (failure)

<span>cohesive stress</span>

<img src="../Figures/cohesive-force" alt="image" style="width:70.0%" />

<span>theoretical strength</span>

-   Using a sinusoidal approximation of strength we have
    $$\\sigma = \\sigma\_c \\sin \\left(\\frac{2\\pi x}{\\lambda}\\right)$$

-   For small strains, sin(*x*)≈*x*

-   We can also write in terms of the modulus of elasticity, $E = \\frac{\\sigma}{\\epsilon} = \\frac{\\sigma}{x/a\_0}$

-   This means we can write $\\sigma = \\frac{E x}{a\_0}$, substituting into the original equation we find
    $$\\frac{E x}{a\_0} = \\sigma\_c \\frac{2\\pi x}{\\lambda}$$

-   solving for *σ*<sub>*c*</sub>, we find the theoretical strength as
    $$\\sigma\_c = \\frac{\\lambda E}{2\\pi a\_0}$$

-   In many materials, *λ* ≈ *a*<sub>0</sub>, in which case $\\sigma\_c = \\frac{E}{2 \\pi}$

<span>energy consideration</span>

-   Surface energy is the work done to create a new surface when an atomic bond breaks

-   We define *γ* as the surface energy (units of energy/area)

-   We can calcualte this surface energy in terms of the sinusoidal approximation of traction-separation
    $$2\\gamma = \\int\_0^{\\lambda/2} \\sigma\_c \\sin \\left(\\frac{2\\pi x}{\\lambda}\\right) dx = \\frac{\\lambda \\sigma\_c}{\\pi}$$

<span>energy consideration</span>

-   re-arranging a previous result, we know that
    $$\\lambda = \\frac{2\\pi a\_0 \\sigma\_c}{E}$$

-   from which we find
    $$\\sigma\_c^2 = \\frac{2\\pi\\gamma E}{2\\pi a\_0} = \\frac{\\gamma E}{a\_0}$$

-   For many materials, the surface energy is approximately *γ* = 0.01*E**a*<sub>0</sub>, which gives an approximate theoretical strength of
    $$\\sigma\_c = \\frac{E}{10}$$

griffith fracture
=================

<span>real failure</span>

-   In practice, materials fail at loads 10 to 100 times lower than the theoretical “atomic” strength

-   Griffith studied glass, which by the atomic strength models should be a very strong material, but in practice is often weaker than much less stiff materials

-   He hypothesized that there were many micro-cracks which coalesced to cause failure

<span>elliptic hole</span>

<img src="../Figures/elliptic" alt="image" style="width:70.0%" />

<span>elliptic hole</span>

-   Inglis solved the problem of an eliptic hole under remote tension, finding that at the edge of the major axis the stress is given by
    $$\\sigma\_{yy} = \\sigma \\left(1+\\frac{2a}{b}\\right)$$

-   For a crack as *b* → 0, we would get the unreasonable prediction that any stress, no matter how small, would produce failure as the stress at the edge of the ellipse would be infinite

-   Griffith, thus, chose to take an energy balance view of the fracture problem

<span>surface energy</span>

-   Griffith proposed that a crack would extend when the incremental release of energy, *d**W* associated with a crack extension of *d**a* in a body is greater than the energy required to create the new surfaces, *d**W*<sub>*s*</sub>

-   For a center crack, there are two crack tips and a total of 4 surfaces, thus
    *W*<sub>*s*</sub> = 2(2*a**γ*)=4*a**γ*

-   Griffith then used the Inglis solution to calculate the total energy released by a crack extension of *d**a*
    $$\\begin{aligned}
                W &= \\frac{\\pi a^2 \\sigma^2 (1-\\nu^2)}{E} &\\qquad \\text{plane strain}\\\\
                W &= \\frac{\\pi a^2 \\sigma^2} {E} &\\qquad \\text{plane stress}
            \\end{aligned}$$

<span>surface energy</span>

-   We can now substitute to find under what conditions *d**W* ≥ *d**W*<sub>*s*</sub>
    $$\\begin{aligned}
                \\frac{2 \\pi a^2 \\sigma\_{cr}^2 (1-\\nu^2)}{E}da &= 4\\gamma da &\\qquad \\text{plane strain}\\\\
                \\frac{2 \\pi a^2 \\sigma\_{cr}^2} {E} da &= 4\\gamma da&\\qquad \\text{plane stress}
            \\end{aligned}$$

-   Which gives the critical stress as
    $$\\begin{aligned}
                \\sigma\_{cr} &= \\sqrt{\\frac{2 E \\gamma}{\\pi (1-\\nu^2)a}} &\\qquad \\text{plane strain}\\\\
                \\sigma\_{cr} &= \\sqrt{\\frac{2 E \\gamma}{\\pi a}} &\\qquad \\text{plane stress}
            \\end{aligned}$$

<span>comparison</span>

-   We can compare this critical stress prediction with previous methods

-   We had found
    $$\\sigma\_c = \\sqrt{\\frac{\\gamma E}{a\_0}}$$

-   Thus when there is inherent damage in a materal larger than the twice the characteristic distance between atoms (*a*<sub>0</sub>), the fracture strength will be lower than the theoretical strength

energy release rate
===================

<span>energy release rate</span>

-   We can now define the energy release rate

-   More precisely, “strain energy release rate per crack tip”
    *d**W* = 2*G**d**a*

-   Which after substitution and integration gives
    $$\\begin{aligned}
                G &= \\frac{1}{2} \\frac{dW}{da} = \\frac{\\pi a \\sigma^2 (1-\\nu^2)}{E} &\\text{plane strain}\\\\
                &= \\frac{\\pi a \\sigma^2}{E} & \\text{plane stress}
            \\end{aligned}$$

<span>fracture toughness</span>

-   When *G* ≥ 2*γ* the strain energy from the applied load is greater than the energy required to propagate a crack, and thus a crack will propagate

-   The critical strain energy release rate is called *G*<sub>*c*</sub>, and is also referred to as the fracture toughness

-   Note: *K*<sub>*c*</sub> (the critical stress intensity factor) is also referred to as the “fracture toughness,” and although they give equivalent predictions, they have different units and are found baed

-   The *G*<sub>*c*</sub> predicted from the atomic surface energy will be somewhat conservative, since almost all materials will absorb at least some of the strain energy in plastic deformation

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

<span>example - double cantilever beam</span>

<img src="../Figures/dcb" alt="double-cantilever beam" style="width:80.0%" />
