<span>schedule</span>

-   6 Apr - Crack Propagation, HW8 Due (Friday by 5:00 pm)

-   11 Apr - SPTE, Crack Retardation

-   13 Apr - Crack Retardation

-   18 Apr - Exam Review, HW9 Due

-   20 Apr - Exam 2

-   Damage Tolerance, Special Topics, Final Projects

### outline

\[sections numbered\]

crack growth rate
=================

<span>fracture surface</span>

<span>fracture surface</span>

<span>crack growth rate</span>

-   We can observe that fatigue damage occurs through crack propagation

-   “cracks” and fracture mechanics have been omitted from all our fatigue discussion thus far

-   It would be beneficial to predict at what rate a crack will extend

<span>crack growth rate</span>

-   Crack growth rate can be measured experimentally

-   Using a center-crack specimen, a fatigue load is applied

-   The crack length is measured and plotted vs. the number of cycles

-   The slope of this curve ($\\frac{da}{dN}$) is then plotted vs. either *K*<sub>*I*, *m**a**x*</sub> or *Δ**K*<sub>*I*</sub> on a log-log scale

-   This chart is then commonly divided into three regions

<span>da-dN vs K</span>

<span>region I</span>

-   In Region I crack growth is very slow and/or difficult to measure

-   In many cases, da/dN corresponds to the spacing between atoms!

-   The point at which the da/dN curve intersects the boundary between Region I and Region II is often called the fatigue threshold

-   Typically 3-15 $\\text{ ksi} \\sqrt{\\text{in}}$ for steel

-   3-6 $\\text{ ksi} \\sqrt{\\text{in}}$ for aluminum

<span>region II</span>

-   Most important region for general engineering analysis

-   Once a crack is present, most of the growth and life occurs in Region II

-   Generally linear in the log-log scale

<span>region III</span>

-   Unstable crack growth

-   Usually neglected (we expect failure before Region III fully develops in actual parts)

-   Can be significant for parts where we expect high stress and relatively short life

<span>crack growth rate curve</span>

-   The crack growth rate curve is considered a material property

-   The same considerations for thickness apply as with fracture toughness (*K*<sub>*c*</sub> vs. *K*<sub>*I**c*</sub>)

-   Is also a function of the load ratio, *R* = *σ*<sub>*m**i**n*</sub>/*σ*<sub>*m**a**x*</sub>

<span>R effects</span>

-   While the x-axis can be either *Δ**K* or *K*<sub>*m**a**x*</sub>, the shape of the data is the same

-   When we look at the effects of load ratio, *R*, the axis causes some differences on the plot

-   With *Δ**K* on the x-axis, increasing *R* will shift the curve up and to the left, shifting the fatigue threshold and fracture toughness on the graph as well

-   With *K*<sub>*m**a**x*</sub> on the x-axis, increasing *R* shifts the curve down and to the right, but fatigue threshold and fracture toughness keep same values

-   In general, *R* dependence vanishes for *R* &gt; 0.8 or *R* &lt; −0.3. This effect is known as the band width

crack growth rate equations
===========================

<span>crack growth rate equations</span>

-   There are many crack growth rate equations of varying complexity

-   The “best” form to use will depend on design needs

-   The important features in curve-fit equations are

    1.  Region II curve fit (linear on log-log scale)

    2.  Region I curve fit (fatigue threshold)

    3.  Region III curve fit (critical stress intensity)

    4.  Stress ratio effects

    5.  Band width of R-curves

<span>paris law</span>

-   The original

-   Fits the linear portion (Region II)

-   Does not fit Region I, Region III, or have R-dependence

-   
    $$\\frac{da}{dN} = C (\\Delta K)^n$$

-   Note: this assumes the x-axis is *Δ**K*, but *Δ**K* = (1 − *R*)*K*<sub>*m**a**x*</sub>, so we can easily convert

<span>paris example</span>

factors affecting crack propagation
===================================

<span>factors affecting crack propagation</span>

-   thickness

-   stress ratio

-   temperature

-   environment

-   frequency

-   crack orientation

-   manufacturer

-   heat treatment

<span>thickness</span>

-   We already discussed the effects of thickness on fracture toughness

-   The same effects are important in crack propagation

-   In thin (plane stress) plates, cracks can be treated as through cracks

-   In thick plates (plain strain), we generally need to consider the crack shape

<span>thickness</span>

-   Cyclic life is primarily a function of *K*<sub>*i*</sub>/*K*<sub>*c*</sub> where *K*<sub>*i*</sub> is the stress intensity factor in the first cycle

-   Other experiments indicate a relationship between $\\frac{d(a/Q)}{dN}$ and *K*<sub>*m**a**x*</sub>

-   *Q* is a shape parameter for elliptical flaws

<span>temperature</span>

-   In general (for most aluminum alloys) cracks propagate more slowly with a decrease in temperature

-   This trend is exactly opposite the trend for *K*<sub>*c*</sub>

-   The effect varies in different materials

-   Most materials benefit from slightly lower temperatures, but as temperatures are further decreased the crack growth rate increases again

<span>temperature</span>

<span>temperature</span>

-   In general, temperature effects can not be predicted well

-   Instead, materials should be tested at a range of temperatures to establish a range of operating temperatures with corresponding crack growth data

<span>environment</span>

-   There are many conditions in the environment that can affect crack growth

-   Moisture greatly increases the crack growth rate

-   Salt water increases crack growth rate even further

-   These effects have varying strength depending on the material used

<span>environment</span>

<span>environment</span>

-   Further, the shape of the applied load curve has a significant effect when combined with adverse environments

-   Crack growth is faster when the load increases slowly and decreases rapidly

-   Crack growth is slower when the load increases rapidly and decreases slowly

<span>environment</span>

-   When the environment is corrosive, the test frequency is of particular importance

-   At low frequencies, a corrosive environment increases the threshold, *K*<sup>*t**h*</sup>

-   However in Region II, crack growth is faster

-   This effect can be explained by the corrosive environment blunting the crack tip

<span>frequency</span>

-   There is conflicting information about the effect of frequency in the absence of a corrosive environment

-   Some experiments have found a frequency dependence, while others have not

-   Many claim that the frequency dependence is due to small amounts of water in air during frequency dependence experiment

<span>crack orientation</span>

-   For rolled plates, a crack will generally propagate faster parallel to the rolling direction

-   In many materials, however, the difference between orientations is not significant when compared to scatter, and it is often neglected

-   Some materials behave very differently with different crack orientations (i.e. the slope of the paris law curve is different), so care should be taken based on the material used

<span>manufacturer</span>

-   Different manufacturers of the same material can produce different crack growth rates

-   Some reasons for this may be

-   Slight variation in composition

-   Site cleanliness (inclusions)

-   Heat treatment/cold rolling variations

<span>heat and surface treatments</span>

-   Different heat and surface treatments are often applied

-   They provide various benefits (corrosion resistance, residual stress, residual stress relief)

-   But they will also affect the crack growth rate

numerical algorithm
===================

<span>numerical algorith</span>

-   While the Paris Law can be integrated directly (for simple load cases), many of the other formulas cannot

-   A simple numerical algorithm for determining incremental crack growth is

-   
    $$a\_{i+1} = a\_i + \\left(\\frac{da}{dN}\\right)\_i\\left(\\Delta N\\right)\_i$$

-   This method is quite tedious by hand (need many *a*<sub>*i*</sub> values for this to be accurate)

-   But is simple to do in Excel, MATLAB, Python, or many other codes

-   For most accurate results, use *Δ**N* = 1, but this is often unnecessary

-   When trying to use large *Δ**N*, check convergence by using larger and smaller *Δ**N* values

<span>boeing-walker example</span>

<span>convergence example</span>

<span>variable load cases</span>

-   In practice variable loads are often seen

-   The most basic way to handle these is to simply calculate the crack length after each block of loading

-   We will discuss an alternate method, which is more convenient for flight “blocks” next class

-   We will also discuss “retardation” models next class

<span>variable load example</span>
