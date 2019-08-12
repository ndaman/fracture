<span>upcoming schedule</span>

-   Aug 24 - Elasticity Review

-   Aug 29 - Griffith Fracture

-   Aug 31 - Griffith Fracture

-   Sep 5 - Elastic Stress Field

### outline

\[sections numbered\]

tensor calculus
===============

<span>gradient</span>

-   The gradient operator, ∇, is often used to indicate partial differentiation in matrix and vector notation

-   We can represent ∇ as a vector
    $$\\nabla = \\left\\langle \\frac{\\partial}{\\partial x\_1}, \\frac{\\partial}{\\partial x\_2}, \\frac{\\partial}{\\partial x\_3} \\right \\rangle$$

-   ∇ is also referred to as the *del operator*

<span>gradient</span>

-   We can convert between vector notation and index notation for many common operations using the ∇.
    $$\\begin{aligned}
            \\nabla \\phi &= \\phi\_{,i}\\\\
            \\nabla^2 \\phi &= \\phi\_{,ii}\\\\
            \\nabla \\hat{u} &= u\_{i,j}\\\\
            \\nabla \\cdot \\hat{u} &= u\_{i,i} \\\\
            \\nabla \\times \\hat{u} &= \\epsilon\_{ijk} u\_{k,j} \\\\
            \\nabla^2 \\hat{u} &= u\_{i,kk}
            \\end{aligned}$$

<span>divergence theorem</span>

-   The Divergence Theorem (or Gauss Theorem) for a vector field, $\\hat{u}$,
    $$\\iint\_S \\hat{u} \\cdot \\hat{n} dS = \\iiint \\nabla \\cdot \\hat{u} dV$$

-   is also valid for tensors of any order
    ∬<sub>*S*</sub>*a*<sub>*i**j*...*k*</sub>*n*<sub>*k*</sub>*d**S* = ∭<sub>*V*</sub>*a*<sub>*i**j*...*k*, *k*</sub>*d**V*

<span>stokes theorem</span>

-   Stokes theorem for a vector field, $\\hat{u}$,
    $$\\oint \\hat{u}\\cdot d\\hat{r} = \\iint\_S \\left(\\nabla \\times \\hat{u}\\right)\\cdot \\hat{n} dS$$

-   also applies for tensors of any order
    ∮*a*<sub>*i**j*...*k*</sub>*d**x*<sub>*t*</sub> = ∬<sub>*S*</sub>*ϵ*<sub>*r**s**t*</sub>*a*<sub>*i**j*...*k*, *s*</sub>*n*<sub>*r*</sub>*d**S*

<span>green’s theorem</span>

-   Green’s theorem is merely a simplification of Stokes theorem in a planar domain.

-   If we write the vector field, $\\hat{u} = f \\hat{e\_1} + g\\hat{e\_2}$, we find
    $$\\iint\_S \\left( \\frac{\\partial g}{\\partial x\_1} - \\frac{\\partial f}{\\partial x\_2}\\right) dx dy = \\int\_C (f dx + g dy)$$

<span>zero-value theorem</span>

-   The zero-value theorem is particularly useful in variational calculus, which we will use later in the course

-   If we know that
    ∭<sub>*V*</sub>*f*<sub>*i**j*...*k*</sub>*d**V* = 0

-   then
    *f*<sub>*i**j*...*k*</sub> = 0

Other Coordinate Systems
========================

<span>curvilinear coordinates</span>

-   We discussed coordinate transformations earlier

-   However, we often desire to use other coordinate systems entirely

-   Polar coordinates (in 2D) are an example of this

-   In 3D, we can use cylindrical or spherical coordinates

<span>cylindrical coordinates</span>

(0,0,0) – (3,0,0) node\[below left\] <span>*x*<sub>1</sub></span>; (0,0,0) – (0,3,0) node\[right\] <span>*x*<sub>2</sub></span>; (0,0,0) – (0,0,3) node\[above\] <span>*x*<sub>3</sub></span>; (0,0,0) – (2,0,0) node\[below\] <span>*r*</span>; ; (0,0,0) – (0,0,2) node\[above left\] <span>*z*</span>;

<span>cylindrical coordinates</span>

-   We can convert between Cartesian and cylindrical coordinate systems
    $$\\begin{aligned}
            x\_1 &= r\\cos \\theta \\\\
            x\_2 &= r\\sin \\theta \\\\
            x\_3 &= z
            \\end{aligned}$$

-   Or to convert from Cartesian to cylindrical
    $$\\begin{aligned}
            r &= \\sqrt{x\_1^2 + x\_2^2}\\\\
            \\theta &= \\tan^{-1} \\left(\\frac{x\_2}{x\_1}\\right)\\\\
            z &= x\_3
            \\end{aligned}$$

<span>spherical coordinates</span>

(0,0,0) – (3,0,0) node\[below left\] <span>*x*<sub>1</sub></span>; (0,0,0) – (0,3,0) node\[right\] <span>*x*<sub>2</sub></span>; (0,0,0) – (0,0,3) node\[above\] <span>*x*<sub>3</sub></span>; (0,0,0) – (P) node\[above right\] <span>*r*</span>; (0,0,0) – (Pxy); (P) – (Pxy); ;

<span>spherical coordinates</span>

-   We can convert between Cartesian and spherical coordinate systems
    $$\\begin{aligned}
            x\_1 &= r\\cos \\theta \\sin \\phi \\\\
            x\_2 &= r\\sin \\theta \\sin \\phi \\\\
            x\_3 &= r\\cos \\phi
            \\end{aligned}$$

-   Or to convert from Cartesian to cylindrical
    $$\\begin{aligned}
            r &= \\sqrt{x\_1^2 + x\_2^2 + x\_3^2}\\\\
            \\phi &= \\cos ^{-1} \\left(\\frac{x\_3}{\\sqrt{x\_1^2 + x\_2^2 + x\_3^2}}\\right)\\\\
            \\theta &= \\tan^{-1} \\left(\\frac{x\_2}{x\_1}\\right)
            \\end{aligned}$$

<span>calculus in cylindrical coordinates</span>
$$\\begin{aligned}
    \\nabla f &= \\frac{\\partial f}{\\partial r} \\hat{r} + \\frac{1}{r}\\frac{\\partial f}{\\partial \\theta} \\hat{\\theta} + \\frac{\\partial f}{\\partial z}\\hat{z}\\\\
    \\nabla \\cdot \\mathbf{u} &= \\frac{1}{r} \\frac{\\partial (r u\_r)}{\\partial r} + \\frac{1}{r} \\frac{\\partial u\_\\theta}{\\partial \\theta} + \\frac{\\partial u\_z}{\\partial z}\\\\
    \\nabla \\times \\mathbf{u} &= \\left(\\frac{1}{r}\\frac{\\partial u\_z}{\\partial \\theta} - \\frac{\\partial u\_\\theta}{\\partial z}\\right)\\hat{r} +
    \\left(\\frac{\\partial u\_r}{\\partial z} - \\frac{\\partial u\_z}{\\partial r}\\right)\\hat{\\theta} +
    \\frac{1}{r}\\left(\\frac{\\partial (r u\_\\theta)}{\\partial r} - \\frac{\\partial u\_r}{\\partial \\theta}\\right) \\hat{z}
    \\end{aligned}$$

<span>calculus in spherical coordinates</span>
$$\\begin{aligned}
    \\nabla f =& \\frac{\\partial f}{\\partial r} \\hat{r} + \\frac{1}{r}\\frac{\\partial f}{\\partial \\phi} \\hat{\\phi} + \\frac{1}{r \\sin \\phi}\\frac{\\partial f}{\\partial \\theta}\\hat{\\theta}\\\\
    \\nabla \\cdot \\mathbf{u} =& \\frac{1}{r^2} \\frac{\\partial (r^2 u\_r)}{\\partial r} + \\frac{1}{r \\sin \\phi} \\frac{\\partial (u\_\\phi \\sin \\phi)}{\\partial \\phi} + \\frac{1}{r \\sin \\phi}\\frac{\\partial u\_\\theta}{\\partial \\theta}\\\\
    \\nabla \\times \\mathbf{u} =& \\frac{1}{r\\sin \\phi}\\left(\\frac{\\partial (u\_\\theta \\sin \\phi)}{\\partial \\phi} - \\frac{\\partial u\_\\phi}{\\partial \\theta}\\right)\\hat{r} +
    \\frac{1}{r}\\left(\\frac{1}{\\sin \\phi}\\frac{\\partial u\_r}{\\partial \\theta} - \\frac{\\partial (r u\_\\theta)}{\\partial r}\\right)\\hat{\\phi} + \\\\
    & \\frac{1}{r}\\left(\\frac{\\partial (r u\_\\phi)}{\\partial r} - \\frac{\\partial u\_r}{\\partial \\phi}\\right) \\hat{\\theta}
    \\end{aligned}$$

Equilibrium Equations
=====================

<span>static equilibrium</span>

<img src="../Figures/equilibrium" alt="image" /> \[fig:equilibrium\]

-   We primarily deal with bodies in static equilibrium

-   This means that all forces and moments must sum to zero

-   For a closed sub-domain of volume *V* and surface area *S* with internal body forces and applied tractions, we find
    ∬<sub>*S*</sub>*T*<sub>*i*</sub><sup>*n*</sup>*d**S* + ∭<sub>*V*</sub>*F*<sub>*i*</sub>*d**V* = 0

<span>static equilibrium</span>

-   Using the Cauchy stress theorem, we can replace the traction vector with the stress tensor
    ∬<sub>*S*</sub>*σ*<sub>*j**i*</sub>*n*<sub>*j*</sub>*d**S* + ∭<sub>*V*</sub>*F*<sub>*i*</sub>*d**V* = 0

-   We can also apply the divergence theorem to convert the surface integral to a volume integral
    ∭<sub>*V*</sub>(*σ*<sub>*j**i*, *j*</sub> + *F*<sub>*i*</sub>)*d**V* = 0

-   Since the volume is arbitrary (we could choose any volume and the conditions for equilibrium would still hold), the integrand must vanish
    *σ*<sub>*j**i*, *j*</sub> + *F*<sub>*i*</sub> = 0

<span>equilibrium equations</span>

-   Written in scalar form, the equilibrium equations are
    $$\\begin{aligned}
            \\frac{\\partial \\sigma\_x}{\\partial x} + \\frac{\\partial \\tau\_{xy}}{\\partial y} + \\frac{\\partial \\tau\_{xz}}{\\partial z} + F\_x &= 0\\\\
            \\frac{\\partial \\tau\_{xy}}{\\partial x} + \\frac{\\partial \\sigma\_y}{\\partial y} + \\frac{\\partial \\tau\_{yz}}{\\partial z} + F\_y &= 0\\\\
            \\frac{\\partial \\tau\_{xz}}{\\partial x} + \\frac{\\partial \\tau\_{yz}}{\\partial y} + \\frac{\\partial \\sigma\_z}{\\partial z} + F\_z &= 0\\\\
            \\end{aligned}$$

<span>angular momentum</span>

-   Similarly, the principle of angular momentum states that the moment forces must all sum to zero as well
    ∬<sub>*S*</sub>*ϵ*<sub>*i**j**k*</sub>*x*<sub>*j*</sub>*T*<sub>*k*</sub><sup>*n*</sup>*d**S* + ∭<sub>*V*</sub>*ϵ*<sub>*i**j**k*</sub>*x*<sub>*j*</sub>*F*<sub>*k*</sub>*d**V* = 0

-   Once again we use Cauchy’s stress theorem
    ∬<sub>*S*</sub>*ϵ*<sub>*i**j**k*</sub>*x*<sub>*j*</sub>*σ*<sub>*l**k*</sub>*n*<sub>*l*</sub>*d**S* + ∭<sub>*V*</sub>*ϵ*<sub>*i**j**k*</sub>*x*<sub>*j*</sub>*F*<sub>*k*</sub>*d**V* = 0

-   And the divergence theorem
    ∭<sub>*V*</sub>\[(*ϵ*<sub>*i**j**k*</sub>*x*<sub>*j*</sub>*σ*<sub>*l**k*</sub>)<sub>,*l*</sub> + *ϵ*<sub>*i**j**k*</sub>*x*<sub>*j*</sub>*F*<sub>*k*</sub>\]*d**V* = 0

<span>angular momentum</span>

-   Expanding the derivative using the chain rule gives
    ∭<sub>*V*</sub>\[*ϵ*<sub>*i**j**k*</sub>*x*<sub>*j*, *l*</sub>*σ*<sub>*l**k*</sub> + *ϵ*<sub>*i**j**k*</sub>*x*<sub>*j*</sub>*σ*<sub>*l**k*, *l*</sub> + *ϵ*<sub>*i**j**k*</sub>*x*<sub>*j*</sub>*F*<sub>*k*</sub>\]*d**V* = 0

-   Which can be simplified (recall that *σ*<sub>*j**i*, *j*</sub> + *F*<sub>*i*</sub> = 0)
    $$\\begin{aligned}
            \\iiint\_V \[ \\epsilon\_{ijk}\\delta\_{jl}\\sigma\_{lk} + \\epsilon\_{ijk}x\_j\\sigma\_{lk,l} + \\epsilon\_{ijk}x\_jF\_k \] dV &= 0\\\\
            \\iiint\_V \[ \\epsilon\_{ijk}\\sigma\_{jk} - \\epsilon\_{ijk}x\_jF\_k + \\epsilon\_{ijk}x\_jF\_k \] dV &= 0\\\\
            \\iiint\_V \\epsilon\_{ijk}\\sigma\_{jk} dV &= 0
            \\end{aligned}$$

<span>angular momentum</span>

-   Using the same argument as before (arbitrary volume) the integrand must vanish
    *ϵ*<sub>*i**j**k*</sub>*σ*<sub>*j**k*</sub> = 0

-   Since the alternating symbol is antisymmetric in *j**k*, *σ*<sub>*j**k*</sub> must be symmetric in *j**k* for this to vanish

-   And thus we have proved that the stress tensor is symmetric, thus equilibrium and angular momentum equations are satisfied when
    *σ*<sub>*j**i*, *j*</sub> + *F*<sub>*i*</sub> = 0

<span>example</span>

-   Under what circumstances is the following stress field in static equilibrium?

-   *σ*<sub>11</sub> = 3*x*<sub>1</sub> + *k*<sub>1</sub>*x*<sub>2</sub><sup>2</sup>, *σ*<sub>22</sub> = 2*x*<sub>1</sub> + 4*x*<sub>2</sub>, *σ*<sub>12</sub> = *σ*<sub>21</sub> = *a* + *b**x*<sub>1</sub> + *c**x*<sub>1</sub><sup>2</sup> + *d**x*<sub>2</sub> + *e**x*<sub>2</sub><sup>2</sup> + *f**x*<sub>1</sub>*x*<sub>2</sub>

-   We are only examining the stress field, so we neglect any internal body forces

-   The first equilibrium equation gives
    $$\\frac{\\partial \\sigma\_{11}}{\\partial x\_1} + \\frac{\\partial \\sigma\_{12}}{\\partial x\_2} = 0$$
    3 + *d* + 2*e**x*<sub>2</sub> + *f**x*<sub>1</sub> = 0

<span>example</span>

-   The second equilibrium equation gives
    $$\\frac{\\partial \\sigma\_{12}}{\\partial x\_1} + \\frac{\\partial \\sigma\_{22}}{\\partial x\_2} = 0$$
    *b* + 2*c**x*<sub>1</sub> + *f**x*<sub>2</sub> + 4 = 0

Spherical and Cylindrical Coordinates
=====================================

<span>cylindrical coordinates</span>

(0,0,0) – (3,0,0) node\[below left\] <span>*x*<sub>1</sub></span>; (0,0,0) – (0,3,0) node\[right\] <span>*x*<sub>2</sub></span>; (0,0,0) – (0,0,3) node\[above\] <span>*x*<sub>3</sub></span>; (0,0,0) – (2,0,0) node\[below\] <span>*r*</span>; ; (0,0,0) – (0,0,2) node\[above left\] <span>*z*</span>;

<span>stress in cylindrical coordinates</span>

-   We can also define stress in a cylindrical coordinate system

    <img src="../Figures/cylindrical" alt="image" /> \[fig:cylindrical\]

<span>stress in cylindrical coordinates</span>

-   The stress tensor in cylindrical coordinates is
    $$\\sigma\_{ij} = \\begin{bmatrix}
            \\sigma\_r & \\tau\_{r\\theta}& \\tau\_{rz} \\\\
            \\tau\_{r\\theta} & \\sigma\_{\\theta} & \\tau\_{\\theta z}\\\\
            \\tau\_{rz} & \\tau\_{\\theta z} & \\sigma\_z
            \\end{bmatrix}$$

<span>equilibrium in cylindrical coordinates</span>

-   Using the derivative relationships developed in Chapter 1, we can express the equilibrium equations as
    $$\\begin{aligned}
            \\frac{\\partial \\sigma\_r}{\\partial r} + \\frac{1}{r} \\frac{\\partial \\tau\_{r \\theta}}{\\partial \\theta} + \\frac{\\partial \\tau\_{rz}}{\\partial z} + \\frac{1}{r}(\\sigma\_r - \\sigma\_\\theta) + F\_r &= 0\\\\
            \\frac{\\partial \\tau\_{r \\theta}}{\\partial r} + \\frac{1}{r} \\frac{\\partial \\sigma\_\\theta}{\\partial \\theta} + \\frac{\\partial \\tau\_{\\theta z}}{\\partial z} + \\frac{2}{r}\\tau\_{r\\theta} + F\_\\theta &= 0\\\\
            \\frac{\\partial \\tau\_{r z}}{\\partial r} + \\frac{1}{r} \\frac{\\partial \\tau\_{\\theta z}}{\\partial \\theta} + \\frac{\\partial \\sigma\_z}{\\partial z} + \\frac{1}{r}\\tau\_{rz} + F\_z &= 0
            \\end{aligned}$$

<span>spherical coordinates</span>

-   We can do the same thing in spherical coordinates

<img src="../Figures/spherical" alt="image" /> \[fig:spherical\]

<span>spherical coordinates</span>

-   The stress tensor in spherical coordinates is
    $$\\sigma\_{ij} = \\begin{bmatrix}
            \\sigma\_r & \\tau\_{r\\phi}& \\tau\_{r\\theta} \\\\
            \\tau\_{r\\phi} & \\sigma\_{\\phi} & \\tau\_{\\phi \\theta}\\\\
            \\tau\_{r\\theta} & \\tau\_{\\phi \\theta} & \\sigma\_\\theta
            \\end{bmatrix}$$

<span>equilibrium in spherical coordinates</span>

-   Using the derivative relationships developed in Chapter 1, we can express the equilibrium equations as
    $$\\begin{aligned}
            \\frac{\\partial \\sigma\_r}{\\partial r} + \\frac{1}{r} \\frac{\\partial \\tau\_{r \\phi}}{\\partial \\phi} + \\frac{1}{r \\sin \\phi}\\frac{\\partial \\tau\_{r\\theta}}{\\partial \\theta} + \\frac{1}{r}(2\\sigma\_r - \\sigma\_\\phi - \\sigma\_\\theta + \\tau\_{r\\phi}\\cot \\phi) + F\_r &= 0\\\\
            \\frac{\\partial \\tau\_{r \\phi}}{\\partial r} + \\frac{1}{r} \\frac{\\partial \\sigma\_\\phi}{\\partial \\phi} + \\frac{1}{r \\sin \\phi}\\frac{\\partial \\tau\_{\\phi \\theta}}{\\partial \\theta} + \\frac{1}{r}\[(\\sigma\_\\phi -\\sigma\_\\theta)\\cot \\phi + 3\\tau\_{r\\phi}\] + F\_\\phi &= 0\\\\
            \\frac{\\partial \\tau\_{r \\theta}}{\\partial r} + \\frac{1}{r} \\frac{\\partial \\tau\_{\\phi \\theta}}{\\partial \\phi} + \\frac{1}{r \\sin \\phi}\\frac{\\partial \\sigma\_\\theta}{\\partial \\theta} + \\frac{1}{r}(2 \\tau\_{\\phi \\theta}\\cot \\phi + 3 \\tau\_{r \\theta}) + F\_\\theta &= 0
            \\end{aligned}$$

Field Equations
===============

<span>field equations</span>

-   Field equations that we have already found

-   Strain-displacement
    $$\\epsilon\_{ij} = \\frac{1}{2}(u\_{i,j} + u\_{j,i})$$

-   Equilibrium
    *σ*<sub>*i**j*, *j*</sub> + *F*<sub>*i*</sub> = 0

-   Constitutive (Hooke’s Law)
    $$\\begin{aligned}
            \\sigma\_{ij} &= \\lambda \\epsilon\_{kk}\\delta\_{ij} + 2\\mu \\epsilon\_{ij}\\\\
            \\epsilon\_{ij} &= \\frac{1+\\nu}{E}\\sigma\_{ij} - \\frac{\\nu}{E}\\sigma\_{kk} \\delta\_{ij}
            \\end{aligned}$$

<span>field equations</span>

-   There are 15 unique field equations to solve for the 15 unknowns

-   3 displacements (*u*<sub>*i*</sub>), 6 unique strain tensor terms (*ϵ*<sub>*i**j*</sub>), and 6 unique stress tensor terms (*σ*<sub>*i**j*</sub>)

-   These equations also depend on a knowledge of the material behavior (*λ*, *μ*) and body forces (usually gravity or zero)

<span>compatibility equations</span>

-   If continuous, single-valued displacements are specified, differentiation will result in well-behaved strain field

-   The inverse relationship, integration of a strain field to find displacement, may not always be true

-   There are cases where we can integrate a strain field to find a set of discontinuous displacements

<span>compatibility equations</span>

-   The compatibility equations enforce continuity of displacements to prevent this from occurring

-   To enforce this condition we consider the strain-displacement relations:
    $$\\epsilon\_{ij} = \\frac{1}{2}(u\_{i,j} + u\_{j,i})$$

-   and differentiate with respect to *x*<sub>*k*</sub> and *x*<sub>*l*</sub>
    $$\\epsilon\_{ij,kl} = \\frac{1}{2}(u\_{i,jkl} + u\_{j,ikl})$$

-   Or
    2*ϵ*<sub>*i**j*, *k**l*</sub> = *u*<sub>*i*, *j**k**l*</sub> + *u*<sub>*j*, *i**k**l*</sub>

<span>compatibility equations</span>

-   We can eliminate the displacement terms from the equation by interchanging the indexes to generate new equations
    $$\\begin{aligned}
            2\\epsilon\_{ik,jl} &= u\_{i,jkl} + u\_{k,ijl} \\\\
            2\\epsilon\_{jl,ik} &= u\_{j,ikl} + u\_{l,ijk}
            \\end{aligned}$$

-   Solving for *u*<sub>*i*, *j**k**l*</sub> and *u*<sub>*j*, *i**k**l*</sub>
    $$\\begin{aligned}
            u\_{i,jkl} &= 2\\epsilon\_{ik,jl} - u\_{k,ijl} \\\\
            u\_{j,ikl} &= 2\\epsilon\_{jl,ik} - u\_{l,ijk}
            \\end{aligned}$$

<span>compatibility equations</span>

-   Substituting these values into the equations gives
    2*ϵ*<sub>*i**j*, *k**l*</sub> = 2*ϵ*<sub>*i**k*, *j**l*</sub> − *u*<sub>*k*, *i**j**l*</sub> + 2*ϵ*<sub>*j**l*, *i**k*</sub> − *u*<sub>*l*, *i**j**k*</sub>

-   We now consider one more change of index equation
    2*ϵ*<sub>*k**l*, *i**j*</sub> = *u*<sub>*k*, *i**j**l*</sub> + *u*<sub>*l*, *i**j**k*</sub>

-   and substituting this result gives
    2*ϵ*<sub>*i**j*, *k**l*</sub> = 2*ϵ*<sub>*i**k*, *j**l*</sub> + 2*ϵ*<sub>*j**l*, *i**k*</sub> − 2*ϵ*<sub>*k**l*, *i**j*</sub>

-   Or, simplified
    *ϵ*<sub>*i**j*, *k**l*</sub> + *ϵ*<sub>*k**l*, *i**j*</sub> − *ϵ*<sub>*i**k*, *j**l*</sub> − *ϵ*<sub>*j**l*, *i**k*</sub> = 0

<span>compatibility equations</span>

-   The so-called *Saint-Venant compatibility equations* in full are a system of 81 equations, but only six are useful (although even these six are not entirely linearly independent)

-   These six are found by setting *k* = *l*, or in expanded form
    $$\\begin{aligned}
            \\frac{\\partial^2 \\epsilon\_x}{\\partial y^2} + \\frac{\\partial^2 \\epsilon\_y}{\\partial x^2} &= 2\\frac{\\partial^2 \\epsilon\_{xy}}{\\partial x \\partial y}\\\\
            \\frac{\\partial^2 \\epsilon\_y}{\\partial z^2} + \\frac{\\partial^2 \\epsilon\_z}{\\partial y^2} &= 2\\frac{\\partial^2 \\epsilon\_{yz}}{\\partial y \\partial z}\\\\
            \\frac{\\partial^2 \\epsilon\_z}{\\partial x^2} + \\frac{\\partial^2 \\epsilon\_x}{\\partial z^2} &= 2\\frac{\\partial^2 \\epsilon\_{zx}}{\\partial z \\partial x}\\\\
            \\frac{\\partial^2 \\epsilon\_x}{\\partial y \\partial z} &= \\frac{\\partial}{\\partial x} \\left(-\\frac{\\partial \\epsilon\_{yz}}{\\partial x} + \\frac{\\partial \\epsilon\_{zx}}{\\partial y} + \\frac{\\partial \\epsilon\_{xy}}{\\partial z}\\right)\\\\
            \\frac{\\partial^2 \\epsilon\_y}{\\partial z \\partial x} &= \\frac{\\partial}{\\partial y} \\left(-\\frac{\\partial \\epsilon\_{zx}}{\\partial y} + \\frac{\\partial \\epsilon\_{xy}}{\\partial z} + \\frac{\\partial \\epsilon\_{yz}}{\\partial x}\\right)\\\\
            \\frac{\\partial^2 \\epsilon\_z}{\\partial x \\partial y} &= \\frac{\\partial}{\\partial z} \\left(-\\frac{\\partial \\epsilon\_{xy}}{\\partial z} + \\frac{\\partial \\epsilon\_{yz}}{\\partial x} + \\frac{\\partial \\epsilon\_{zx}}{\\partial y}\\right)
            \\end{aligned}$$

<span>compatibility equations</span>

-   The compatibility equations are necessary to ensure that the strain field is valid and will produce a continuous displacement field

-   While these equations are important and necessary in solving elasticity problems, they are not sufficient

-   15 equations with 15 “unknowns” but each of these “unknowns” could actually be a function with many more unknowns, we need to develop framework for simplifying the problem into something we can solve

Boundary Conditions
===================

<span>boundary conditions</span>

-   Boundary conditions commonly specify how a body is supported and/or how it is loaded

-   Mathematically we treat this conditions as *displacements* or *tractions* at boundary points.

-   Symmetry boundary conditions are also common, can reduce computational cost and simplify analytic solutions.

<span>boundary conditions</span>

<img src="../Figures/bcs" alt="image" /> \[fig:bcs\]

<span>symmetric boundaries</span>

<img src="../Figures/symmetric" alt="image" /> \[fig:symmetric\]

<span>coordinate systems</span>

<img src="../Figures/coordinates" alt="image" /> \[fig:coordinates\]

<span>boundaries</span>

-   In many systems, the boundaries are parallel to the coordinate system, but this is not always the case

<img src="../Figures/noncoordinate" alt="image" /> \[fig:noncoordinate\]

<span>boundaries</span>

-   We often translate traction boundary conditions into stress boundary conditions using Cauchy’s Stress Theorem

-   When the condition is on a face parallel to the coordinate system, this gives a zero-stress condition
    *t*<sub>*j*</sub> = *σ*<sub>*i**j*</sub>*n*<sub>*i*</sub>

-   This results in *σ*<sub>*x**y*</sub> = *σ*<sub>*y**y*</sub> = 0

-   When the boundary is not parallel to the coordinate system, we do not necessarily have any zero-stress conditions
    $$\\begin{aligned}
            t\_x &= \\sigma\_x n\_x + \\tau\_{xy} n\_y = 0 \\\\
            t\_y &= \\tau\_{xy} n\_x + \\sigma\_y n\_y = 0 \\\\
            \\end{aligned}$$

<span>interfaces</span>

-   When we deal with multiple materials, we must prescribe conditions at the interface of these materials

-   Some common *interface conditions* are

    -   *Perfectly bonded interface* where displacements and tractions are continuous at the interface

    -   *Slip interface* where only normal displacements and tractions are continuous at the interface, with no tangential traction and potentially discontinuous tangential displacement

Stress Formulation
==================

<span>stress formulation</span>

-   For traction problems (i.e. traction is defined on all surfaces) it is convenient to re-formulate field equations in terms of stress only

-   Since displacements are eliminated, we will need to use the compatibility equations to ensure a continuous displacement field

-   It is desirable for this formulation to write the compatibility equations in terms of stress

<span>stress formulation</span>

-   We start by using Hooke’s law for each of the strain terms
    $$\\epsilon\_{ij} = \\frac{1+\\nu}{E}\\sigma\_{ij} - \\frac{\\nu}{E}\\sigma\_{kk} \\delta\_{ij}$$

-   After some tedious algebra, we find
    $$\\hspace{-1cm}
            \\sigma\_{ij,kk} + \\sigma\_{kk,ij} - \\sigma\_{ik,jk} - \\sigma\_{jk,ik} = \\frac{\\nu}{1+\\nu} (\\sigma\_{mm,kk}\\delta\_{ij} + \\sigma\_{mm,ij}\\delta\_{kk} - \\sigma\_{mm,jk}\\delta\_{ik} - \\sigma\_{mm,ik}\\delta\_{jk})$$

<span>stress formulation</span>

-   If we also include the equilibrium equations (*σ*<sub>*i**j*, *j*</sub> − *F*<sub>*i*</sub>) in the formulation, we find
    $$\\sigma\_{ij,kk} + \\frac{1}{1+\\nu}\\sigma\_{kk,ij} = \\frac{\\nu}{1+\\nu}\\sigma\_{mm,kk}\\delta\_{ij} - F\_{i,j} - F\_{j,i}$$

-   We can further simplify the equation by consider the case when *i* = *j* and nothing that
    $$\\sigma\_{ii,kk} = -\\frac{1+\\nu}{1-\\nu}F\_{i,i}$$

-   Which we can substitute into the equation to find
    $$\\sigma\_{ij,kk} + \\frac{1}{1+\\nu}\\sigma\_{kk,ij} = -\\frac{\\nu}{1+\\nu}\\delta\_{ij}F\_{k,k} - F\_{i,j} - F\_{j,i}$$

<span>beltrami-michell compatibility</span>

-   The compatibility equations in terms of stress are commonly known as the *Beltrami-Michell compatibility equations*

-   When there are no body forces, we can write the six expanded form equations as
    $$\\begin{aligned}
            (1+\\nu) \\nabla^2 \\sigma\_x + \\frac{\\partial^2}{\\partial x^2} (\\sigma\_x + \\sigma\_y + \\sigma\_z) &= 0\\\\
            (1+\\nu) \\nabla^2 \\sigma\_y + \\frac{\\partial^2}{\\partial y^2} (\\sigma\_x + \\sigma\_y + \\sigma\_z) &= 0\\\\
            (1+\\nu) \\nabla^2 \\sigma\_z + \\frac{\\partial^2}{\\partial z^2} (\\sigma\_x + \\sigma\_y + \\sigma\_z) &= 0\\\\
            (1+\\nu) \\nabla^2 \\tau\_{xy} + \\frac{\\partial^2}{\\partial x \\partial y} (\\sigma\_x + \\sigma\_y + \\sigma\_z) &= 0\\\\
            (1+\\nu) \\nabla^2 \\tau\_{yz} + \\frac{\\partial^2}{\\partial y \\partial z} (\\sigma\_x + \\sigma\_y + \\sigma\_z) &= 0\\\\
            (1+\\nu) \\nabla^2 \\tau\_{zx} + \\frac{\\partial^2}{\\partial z \\partial x} (\\sigma\_x + \\sigma\_y + \\sigma\_z) &= 0\\\\
            \\end{aligned}$$

<span>stress formulation</span>

-   When working with traction boundary problems, these compatibility equations, together with the equilibrium equations, are sufficient to solve the problem

-   These partial differential equations are not easy to solve, and analytic problems approached this way are often solved only in 2D

-   Solutions are also commonly based on *stress functions*, which gives a base equation form that automatically satisfies equilibrium

<span>solution methods</span>

-   Direct method

    -   Solved via direction integration

    -   Limited to very simple geometries

-   Inverse method

    -   Choose a basic form for the solution based on our knowledge of the problem

    -   Solve for coefficients

    -   Usually we know the answer before we know the problem, it can be difficult to find useful problems for our solution

-   Semi-inverse method

    -   Only part of the solution is assumed

    -   Use direct integration to find the rest

strain energy
=============

<span>strain energy</span>

-   Energy stored by deformation

-   In linear elasticity it is given as
    $$U = \\frac{1}{2}V \\sigma\_{ij} \\epsilon\_{ij}$$

<span>rod</span>

-   Strain energy in a 1D rod in tension can be expressed as
    $$U = \\int\_0^L \\frac {P^2}{EA} dx$$

<span>beam</span>

-   In a beam under pure bending we find the strain energy as
    $$U = \\int\_0^L \\frac{M^2}{2EI} dx$$

Example
=======

<span>Levy’s problem</span>

-   Find the stresses in a semi-infinite wedge due to fluid pressure and its own self-weight

<img src="../Figures/levee" alt="image" /> \[fig:levee\]

<span>Levy’s problem</span>

-   Since pressure varies linearly with depth, we will assume a linear state of stress
    $$\\begin{aligned}
            \\sigma\_{x} &= a\_1 x + b\_1 y + c\_1\\\\
            \\sigma\_{y} &= a\_2 x + b\_2 y + c\_2\\\\
            \\tau\_{xy} &= a\_{12}x + b\_{12} y + c\_{12}\\\\
            \\end{aligned}$$

-   This leaves 9 coefficients to be determined

<span>Levy’s problem</span>

-   First let us consider the boundary conditions at the apex of the dam

-   If we let the origin be at the apex of the dam, which must be traction free, we find
    *c*<sub>1</sub> = *c*<sub>2</sub> = *c*<sub>12</sub> = 0

<span>Levy’s problem</span>

-   Next let us consider the equilibrium equations
    $$\\begin{aligned}
            \\sigma\_{x,x} + \\tau\_{xy,y} + \\rho b\_x &= 0\\\\
            \\tau\_{xy,x} + \\sigma\_{y,y} + \\rho b\_y &= 0
            \\end{aligned}$$

-   Which in this case become
    $$\\begin{aligned}
            a\_1 + b\_{12} + 0 &= 0\\\\
            a\_{12} + b\_2 - \\rho g &= 0
            \\end{aligned}$$

<span>Levy’s problem</span>

-   The stresses can now be written as
    $$\\begin{aligned}
            \\sigma\_x &= a\_1 x + b\_1 y\\\\
            \\sigma\_y &= a\_2 x + b\_2 y\\\\
            \\tau\_{xy} &= -b\_2 x + \\rho g x - a\_1 y
            \\end{aligned}$$

<span>Levy’s problem</span>

-   The compatibility equations are all satisfied, as these linear functions will all go to zero when taking second derivatives

-   We now consider the boundary conditions along both faces

airy stress functions
=====================

<span>airy stress function</span>

-   A stress function technique that can be used to solve many planar problems is known as the *Airy stress function*

-   This method reduces the governing equations for a planar problem to a single unknown function

-   We assume first that body forces are derivable from a *potential function*, *V*
    $$\\begin{aligned}
            F\_x &= -\\frac{\\partial V}{\\partial x}\\\\
            F\_y &= -\\frac{\\partial V}{\\partial y}
            \\end{aligned}$$

-   How restrictive is this assumption?

-   Most body forces are linear (gravity) and can easily be represented this way

<span>airy stress function</span>

-   Consider the following
    $$\\begin{aligned}
            \\sigma\_{xx} &= \\frac{\\partial^2 \\phi}{\\partial y^2} + V\\\\
            \\sigma\_{yy} &= \\frac{\\partial^2 \\phi}{\\partial x^2} + V\\\\
            \\tau\_{xy} &= -\\frac{\\partial^2 \\phi}{\\partial x \\partial y}
            \\end{aligned}$$

-   The function *ϕ* = *ϕ*(*x*, *y*) is known as the Airy stress function

-   When constructed in this way, equilibrium is automatically satisfied

<span>compatibility</span>

-   Substituting the Airy Stress function and potential function into the relationships, we find
    $$\\begin{aligned}
            \\frac{\\partial^4 \\phi}{\\partial x^4} + 2\\frac{\\partial^4 \\phi}{\\partial x^2 \\partial y^2} + \\frac{\\partial^4 \\phi}{\\partial y^4} &= - \\frac{1-2\\nu}{1-\\nu}\\left(\\frac{\\partial^2 V}{\\partial x^2} + \\frac{\\partial^2 V}{\\partial y^2}\\right) &\\text{plane strain}\\\\
            \\frac{\\partial^4 \\phi}{\\partial x^4} + 2\\frac{\\partial^4 \\phi}{\\partial x^2 \\partial y^2} + \\frac{\\partial^4 \\phi}{\\partial y^4} &= - (1-\\nu)\\left(\\frac{\\partial^2 V}{\\partial x^2} + \\frac{\\partial^2 V}{\\partial y^2}\\right) &\\text{plane stress}
            \\end{aligned}$$

-   If there are no body forces, or the potential function satisfies Laplace’s Equation
    ∇<sup>2</sup>*V* = 0
     Then both plane stress and plane strain reduce to
    $$\\frac{\\partial^4 \\phi}{\\partial x^4} + 2\\frac{\\partial^4 \\phi}{\\partial x^2 \\partial y^2} + \\frac{\\partial^4 \\phi}{\\partial y^4} = 0$$

<span>polar coordinates</span>

-   Recall that an Airy Stress function must satisfy the Beltrami-Mitchell compatibility equations
    $$\\nabla^4 \\phi = \\left(\\frac{\\partial ^2}{\\partial r^2} + \\frac{1}{r} \\frac{\\partial}{\\partial r} + \\frac{1}{r^2}\\frac{\\partial ^2}{\\partial \\theta^2}\\right)^2\\phi = 0$$

-   One method which gives several useful solutions assumes that the Airy Stress function has the form *ϕ*(*r*, *θ*)=*f*(*r*)*e*<sup>*b**θ*</sup>

-   Substituting this into the compatibility equations (and canceling the common *e*<sup>*b**θ*</sup>) term gives
    $$f^{\\prime \\prime \\prime \\prime} + \\frac{2}{r} f^{\\prime \\prime \\prime} - \\frac{1-2b^2}{r^2}f^{\\prime \\prime} + \\frac{1-2b^2}{r^3}f^{\\prime} + \\frac{b^2(4+b^2)}{r^4}f = 0$$

<span>polar coordinates</span>

-   To solve this, we perform a change of variables, letting *r* = *e*<sup>*ξ*</sup>, which gives
    *f*<sup>′′′′</sup> − 4*f*<sup>′′′</sup> + (4 + 2*b*<sup>2</sup>)*f*<sup>′′</sup> − 4*b*<sup>2</sup>*f*<sup>′</sup> + *b*<sup>2</sup>(4 + *b*<sup>2</sup>)*f* = 0

-   We know consider *f* to have the form *f* = *e*<sup>*a**ξ*</sup> which generates the characteristic equation
    (*a*<sup>2</sup> + *b*<sup>2</sup>)(*a*<sup>2</sup> − 4*a* + 4 + *b*<sup>2</sup>)=0

-   And has solutions
    $$\\begin{aligned}
            a &= \\pm ib, \\pm 2ib\\\\
            \\text{OR}\\\\
            b &= \\pm ia, \\pm i(a-2)
            \\end{aligned}$$

<span>polar coordinates</span>

-   All solutions to the Beltrami-Mitchell equations in polar coordinates which are periodic in *θ* can be summarized as
    $$\\begin{aligned}
            \\phi &= a\_0 + a\_1 \\log r + a\_2 r^2 + a\_3 r^2 \\log r \\\\
            &+ (a\_4 + a\_5 \\log r + a\_6 r^2 + a\_7 r^2 \\log r)\\theta \\\\
            &+ \\left(a\_{11}r + a\_{12}r\\log r + \\frac{a\_{13}}{r} + a\_{14}r^3 + a\_{15}r\\theta + a\_{16} r\\theta \\log r\\right) \\cos \\theta\\\\
            &+  \\left(b\_{11}r + b\_{12}r\\log r + \\frac{b\_{13}}{r} + b\_{14}r^3 + b\_{15}r\\theta + b\_{16} r\\theta \\log r\\right) \\sin \\theta\\\\
            &+ \\sum\_{n=2}^{\\infty} (a\_{n1}r^n + a\_{n2}r^{2+n}+a\_{n3}r^{-n}+a\_{n4}r^{2-n})\\cos n\\theta\\\\
            &+ \\sum\_{n=2}^{\\infty} (b\_{n1}r^n + b\_{n2}r^{2+n}+a\_{n3}r^{-n}+b\_{n4}r^{2-n})\\sin n\\theta\\\\
            \\end{aligned}$$

<span>polar coordinates</span>

-   For axisymmetric problems, all field quantities are independent of *θ*

-   This reduces the general solution to
    *ϕ* = *a*<sub>0</sub> + *a*<sub>1</sub>log*r* + *a*<sub>2</sub>*r*<sup>2</sup> + *a*<sub>3</sub>*r*<sup>2</sup>log*r*

<span>polar coordinates</span>

<img src="../Figures/polar_table" alt="image" /> \[fig:polar\_table\]

<span>polar coordinates</span>

<img src="../Figures/polar_table2" alt="image" /> \[fig:polar\_table\]
