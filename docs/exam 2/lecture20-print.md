<span>schedule</span>

-   11 Apr - SPTE, Crack Retardation

-   13 Apr - Crack Retardation

-   18 Apr - Exam Review, HW9 Due

-   20 Apr - Exam 2

-   Damage Tolerance, Special Topics, Final Projects

### outline

\[sections numbered\]

boeing method
=============

<span>boeing method for variable amplitude loads</span>

-   Whether integrating numerically or analytically, it is time-consuming to consider multiple repeated loads

-   It is particularly difficult to consider flight loads, which can vary by “mission”

-   For example, an aircraft may fly three different routes, in no particular order, but with a known percentage of time spent in each route

-   Traditional methods would use a random mix of each load spectra

-   The Boeing Method combines each repeatable load spectrum into one single equivalent cycle

<span>boeing method</span>

-   The Boeing method is derived by separating the geometry effects from load and material effects in the Boeing-Walker equation.

-   
    $$\\frac{da}{dN} = \\left\[\\frac{1}{n}\\right\]\\frac{dL}{dN} = 10^{-4} \\left\[\\frac{k\_{max}Z}{m\_T}\\right\]^p$$

-   
    $$\\frac{dL}{dN} = n 10^{-4} \\left\[\\frac{k\_{max}Z}{m\_T}\\right\]^p$$

-   
    $$\\frac{dN}{dL} = \\frac{1}{n} 10^{4} \\left\[\\frac{m\_T}{k\_{max}Z}\\right\]^p$$

-   
    $$\\int\_{0}^{N}dN = \\frac{10^{4}}{n}  \\int\_{L\_0}^{L\_f} \\left\[\\frac{m\_T}{k\_{max}Z}\\right\]^p dL$$

-   
    $$N = 10^{4} \\left(\\frac{m\_t}{z\\sigma\_{max}}\\right)^p  \\int\_{L\_0}^{L\_f} \\frac{dL}{\\left( n\\sqrt{\\pi L/n}\\beta\\right)^p}$$

<span>boeing method</span>

-   In this form, the term $10^{4} \\left(\\frac{m\_t}{z\\sigma\_{max}}\\right)^p$ is strictly from the applied load and material, while $\\int\_{L\_0}^{L\_f} \\frac{dL}{\\left( n\\sqrt{\\pi L/n}\\beta\\right)^p}$ is from geometry

-   If we now define *G* to account for crack geometry

-   
    $$G = \\left\[ \\int\_{L\_0}^{L\_f} \\frac{dL}{\\left( n\\sqrt{\\pi L/n}\\beta\\right)^p} \\right\] ^{-1/p}$$

-   And define *z**σ*<sub>*m**a**x*</sub> = *S* as the equivalent load spectrum, then we have

-   
    $$\\label{eq:boeing}
            N = 10^4 \\left(\\frac{m\_t/G}{S}\\right)^p$$

-   Using this method, *G* is typically looked up from a chart (such as on p. 369)

<span>boeing method</span>

-   To replace a repeated load spectrum with an equivalent load, we need to invert the relationship

-   Equation \[eq:boeing\] gives cycles per crack growth, inverting gives crack growth per cycle

-   
    $$\\text{crack growth per cycle} = 10^{-4} \\left(\\frac{m\_t/G}{S}\\right)^{-p}$$

-   If we consider a general, repeatable “block”, we have

-   
    $$10^{-4} \\left( m\_t/G \\right)^{-p} \\sum\_i \\left( \\frac{1}{z\\sigma\_{max}} \\right)\_i^{-p} N\_i = 10^{-4} \\left( \\frac{m\_t/G}{S} \\right)^{-p}$$

-   Which simplifies to
    ∑<sub>*i*</sub>(*z**σ*<sub>*m**a**x*</sub>)<sub>*i*</sub><sup>*p*</sup>*N*<sub>*i*</sub> = (*S*)<sup>*p*</sup>

<span>boeing method example</span>

<span>boeing method example - cont.</span> cycle counting

cycle counting
==============

<span>cycle counting</span>

-   As illustrated in our previous example, cycle counting method can make a difference for variable amplitude loads

-   Two common methods for cycle counting that give similar results are known as the “rainflow” and “range-pair” methods

-   ASTM E1049-85 “Standard Practices for Cycle Counting in Fatigue Analysis”

<span>rain-flow method</span>

1.  Read next peak or valley. *S* is the starting point, *Y* is the first range, *X* is the second range

2.  If *X* &lt; *Y* advance points (*S* remains same, *Y* and *X* change)

3.  If *X* ≥ *Y* and *Y* contains *S*, count *Y* as 1/2-cycle, discard *S* and go to 1

4.  If *X* ≥ *Y* and *Y* does not contain *S*, count *Y* as 1 cycle, discard both points in *Y* and go to 1 (*S* remains same)

5.  When end of data is reached, count each range as 1/2-cycle

<span>range-pair method</span>

1.  Read next peak or valley. *Y* is the first range, *X* is the second range

2.  If *X* &lt; *Y* advance points

3.  If *X* ≥ *Y*, count *Y* as 1 cycle and discard both points in *Y*, go to 1

4.  Remaining cycles are counted backwards from end of history

<span>cycle counting example</span>

crack growth retardation
========================

<span>crack growth retardation</span>

-   When an overload is applied, the plastic zone is larger

-   This zone has residual compressive stresses, which slow crack growth until the crack grows beyond this over-sized plastic zone

-   We will discuss three retardation models, but no model has been shown to be perfect in all cases

-   The Wheeler method reduces *d**a*/*d**N*, the Willenborg model reduces *Δ**K*, and the Closure model increases *R* (increases *σ*<sub>*m**i**n*</sub>)

<span>wheeler retardation</span>

-   As long as crack is within overload plastic zone, we scale *d**a*/*d**N* by some *ϕ*

-   
    (*a*<sub>*i*</sub> + *r*<sub>*p**i*</sub>)=(*a*<sub>*o**l*</sub> + *r*<sub>*p**o**l*</sub>)

-   And *ϕ* is given by
    $$\\phi\_i = \\left\[\\frac{r\_{pi}}{a\_{ol}+r\_{pol}-a\_i}\\right\]^m$$

-   and the constant, *m* is to be determined experimentally

<span>wheeler example</span>

<span>willenborg retardation</span>

-   Once again, we consider that retardation occurs when (*a*<sub>*i*</sub> + *r*<sub>*p**i*</sub>)=(*a*<sub>*o**l*</sub> + *r*<sub>*p**o**l*</sub>)

-   Willenborg assumes that the residual compressive stress in the plastic zone creates an effective, *K*<sub>*m**a**x*, *e**f**f*</sub>, where *K*<sub>*m**a**x*, *e**f**f*</sub> = *K*<sub>*m**a**x*</sub> − *K*<sub>*c**o**m**p*</sub>

-   The effective stress intensity factor is given by
    $$K\_{max,eff} = K\_{max,i} - \\left\[K\_{max,OL}\\sqrt{1-\\frac{\\Delta a\_i}{r\_{pol}}} - K\_{max,i} \\right\]$$

<span>gallagher and hughes correction</span>

-   Galagher and Hughes observed that the Willenborg model stops cracks when they still propagate

-   They proposed a correction to the model

-   
    $$K\_{max,eff} = K\_{max,i} - \\phi\_i\\left\[K\_{max,OL}\\sqrt{1-\\frac{\\Delta a\_i}{r\_{pol}}} - K\_{max,i} \\right\]$$

-   And the correction factor, *ϕ*<sub>*i*</sub> is given by
    $$\\phi\_i \\frac{1-K\_{TH}/K\_{max,i}}{s\_{ol}-1}$$

<span>willenborg example</span>

<span>closure model</span>

-   Once again, we consider that retardation occurs when (*a*<sub>*i*</sub> + *r*<sub>*p**i*</sub>)=(*a*<sub>*o**l*</sub> + *r*<sub>*p**o**l*</sub>)

-   Within the overloaded plastic zone, the opening stress required can be expressed as
    *σ*<sub>*O**P*</sub> = *σ*<sub>*m**a**x*</sub>(1 − (1 − *C*<sub>*f*0</sub>)(1 + 0.6*R*)(1 − *R*))

-   Commonly this is expressed using the Closure Factor, *C*<sub>*f*</sub>

-   
    $$C\_f = \\frac{\\sigma\_{OP}}{\\sigma\_{max}} = (1-(1-C\_{f0})(1+0.6R)(1-R))$$

-   Where *C*<sub>*f*0</sub> is the value of the Closure Factor at *R* = 0

<span>closure model</span>

-   When using the closure model, we replace *R* with *C*<sub>*f*</sub>

-   If the model we are using is in terms of *Δ**K* we will also need to use *Δ**K* = (1 − *C*<sub>*f*</sub>)*K*<sub>*m**a**x*</sub>

<span>closure example</span>

<span>compressive under-loads</span>

-   Just as a tensile “overload” retards crack growth, we might expect a compressive “underload” to accelerate crack growth

-   This effect is not usually modeled for a few reasons

    1.  Compressive underloads are uncommon in airframes

    2.  The acceleration effect is minimal

    3.  Analysis is generally adjusted with experimental data, so acceleration can be built in to current model

    4.  Structures with large compressive loads are not generally subject to crack propagation problems


