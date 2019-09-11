# AE837
## Advanced Mechanics of Damage Tolerance
Dr. Nicholas Smith<br/>
Wichita State University, Department of Aerospace Engineering
August 20, 2019

----
## upcoming schedule

-   Aug 20 - Syllabus, Elasticity Review
-   Aug 22 - Elasticity Review
-   Aug 27 - Griffith Fracture
-   Aug 29 - Griffith Fracture

----
## outline

<!-- vim-markdown-toc GFM -->

* introduction
* syllabus and schedule
* fracture introduction
* elasticity
* coordinate transformation
* examples
* principal values
* invariants
* principal directions
* examples

<!-- vim-markdown-toc -->

---
# introduction

----
## about me

![family picture](../images/family_photo.jpg) <!-- .element width="75%" -->

----
## education
  - B.S. in Mechanical Engineering from Brigham Young University
    - Worked with ATK to develop tab-less gripping system for tensile testing composite tow specimens
    - Needed to align the specimen, as well as grip it without causing a stress concentration

----
## education
  - M.S. and Ph.D. from School of Aeronautics and Astronautics at Purdue University
    - Worked with Boeing to simulate mold flows
    - First ever mold simulation with anisotropic viscosity

----
## research
![picture of chopped carbon fiber prepreg](../images/Formosa_Chopped_Carbon_Fiber_CSc_bw.jpg)

----
## research
![picture of lamborghini symbol made from compression molded chopped carbon fiber](../images/lamborghini-chopped-fiber-badges-rough.jpg)

----
## research

  <div class='left'>
![picture illustrating the fused deposition modeling 3D printing process, where plastic filament is melted and deposited next to other filament, and fuses together](../images/3D-printing.png)
  </div>

  <div class='right'>
  <ul>
  <li> Composites are being used in 3D printing now </li>
  <li> Printing patterns are optimized for isotropic materials </li>
  <li> Sometimes composites hurt more than they help when not utilized properly </li>
  </div>

----
## research

<div class="left">
	<ul>
		<li>Thermoplastic composites offer many advantages over thermoset</li>
		<li>Production speed, recyclability</li>
		<li>Also have challenges, such as bonding/welding</li>
	</ul>
</div>
<div class="right">
	![thermoplastic welding](../images/Welding-thermoplastic-composites.jpg)
</div>
 

----
## classes

-   AE 731 Elasticity Theory (odd years in fall)
-   AE 737 Mechanics of Damage Tolerance (every year in spring)
-   AE 837 Advanced Mechanics of Damage Tolerance (odd years in fall)
-   AE 760AA Micromechanics and Multiscale Modeling (odd years in spring)
-   AE 831 Continuum Mechanics (even years in fall)

----
## introductions

-   Name
-   Student status (Undergrad, Masters, Ph.D)
-   Full time or part time student?
-   One interesting thing to remember you by

---
# syllabus and schedule

----
## course textbook

-   Text is available as a pdf on Blackboard and the [class website](https://ndaman.github.io/fracture/), you may purchase any version if you prefer a hard copy
-   Homework will be given in handouts provided online
-   Supplemental textbooks are listed in the syllabus for further study

----
## office hours

-   I will e-mail everyone in the course a Doodle link we can use to find the optimal office hours
-   Let me know if you do not receive the e-mail, you may need to update your information in Blackboard
-   Take advantage of office hours, this is time that I have already set aside for you
-   If the regular office hours do not work for your schedule, send me an e-mail and we can work out a time to meet

----
## tentative course outline

-   Section 1 - linear elastic fracture mechanics
    -   Elasticity Review (Aug 20-22)
    -   Griffith Fracture (Aug 27-29)
    -   Elastic Stress Field (Sept 3-12)
    -   Exam 1 (Sept 19)

----
## tentative course outline

-   Section 2 - advanced analytical fracture
    -   Energy Approach (Sept 24-26)
    -   Finite Elements (Oct 1-12)
    -   Plasticity (Oct 17-24)
    -   Mixed-Mode Fracture (Oct 29-31)
    -   Exam 2 (Nov 7)

----
## tentative course outline

-   Section 3 - computational fracture
    -   XFEM (Nov 12-14)
    -   Cohesive Zone Modeling (Nov 19-28)
    -   Interfacial Cracks (Dec 3-5)
    -   Final project (due Dec 6)

----
## grades

-   Grade breakdown
    -   Homework 15%
    -   Exam 1 30%
    -   Exam 2 30%
    -   Final Project 25%
-   Follow a traditional grading scale

----
## final project

-   Perform computational fracture analysis on a real-life part (or test specimen) of your choosing
-   Use the principles developed in this class to provide an analytical validation of your computational methods
-   Examples: mixed-mode fracture study, progressive failure, adhesive bond failure, etc.
-   Individual project
-   More discussion after Exam 1

----
## class expectations

-   Consider the cost (to you or others) of your being in class
-   I ask that you refrain from distracting behaviors during class
-   When you have something more important than class to take care of, please take care of it outside of class

----
## software

-   You will be required to do finite element analysis in this class, we have a class kit license for COMSOL, but you are welcome to use any software package you want
-   The student version of Abaqus is also free and has a good XFEM module (not all FEA tools have XFEM)
-   Although we will not use FEA until later in the course, I advise you set up the software as soon as possible

---
# fracture introduction

----
## damage

-   In linear elasticity, we generally consider materials in their pristine state
-   Realities of manufacturing, cyclic loads, and unforeseen loads result in a material which is something other than pristine
-   When stress is uniform, simple analysis can often predict failure (*σ* &gt; *σ*<sub>*f*</sub>)
-   When damage or stress concentrations are present, however, failure is more accurately modeled as fracture

----
## fracture

-   There are two primary approaches to modeling fracture
-   In the first we examine the elastic stress and displacement fields near a crack tip
-   A fracture criterion is then defined based on the so-called stress intensity factor
-   The other approach considers the global energy of a body with a crack
-   We consider the potential energy of a cracked solid and consider its variation with a virtual crack extension
-   The energy release rate is then used to quantify failure

----
## fracture

-   Several other parameters have been used to quantify failure in addition to the stress intensity factor and the energy release rate, with somewhat less success
-   J-integral
-   Crack Tip Opening Displacement
-   Crack Tip Opening Angle

----
## fracture mechanics

-   In fracture mechanics we consider three different modes
-   Mode I is known as the “opening mode”
-   Mode II is known as the “sliding mode”
-   Mode III is known as the “tearing mode”

----
## fracture mechanics

![Illustration of fracture modes](../images/Fracture_modes_v2.svg)

---
# elasticity

----
## linear elasticity

-   We cannot cover everything from elasticity, and you can get by in this course without it, but we will be using many principles from elasticity in this course
-   Some of the things we will review are
    -   Index notation (briefly)
    -   Coordinate transformation
    -   Principal values/directions
    -   Spherical/cylindrical coordinates
    -   Strain energy
    -   General solution strategy

----
## big picture

-   Perhaps more important than the details we will review is to keep in mind the “big picture”
-   To solve any problem in elasticity, we need to satisfy:
    1.  The equilibrium equations (in the appropriate coordinate system)
    2.  The boundary conditions
    3.  Without violating strain compatibility

----
## big picture

-   Most often, we assume a state of plane stress or plane strain and solve the problem in 2D
-   Even “3D” problems (i.e. Mode III fracture) have reduced variables
-   Stress functions are often formulated to automatically satisfy equilibrium, or displacement functions to automatically satisfy compatibility

---
# coordinate transformation

----
## two dimensions

![2D axes to illustrated coordinate transformation](../images/transform2D.png) <!-- .element width="75%" -->

----
## two dimensions

-   The vector, *v*, remains fixed, but we transform our coordinate system
-   In the new coordinate system, the *x*<sub>2</sub><sup>′</sup> portion of *v* is zero.
-   To transform the coordinate system, we first define some unit vectors.
-   $\\hat{e}\_1$ is a unit vector in the direction of *x*<sub>1</sub>, while $\\hat{e}\_1^\\prime$ is a unit vector in the direction of *x*<sub>1</sub><sup>′</sup>

----
## two dimensions

![2D axes with unit direction vectors added](../images/transform2D-unit.png) <!-- .element width="75%" -->

----
## two dimensions

-   For this example, let us assume *v* = ⟨2, 2⟩ and *θ* = 45<sup>∘</sup>
-   We can write the transformed unit vectors, $\\hat{e}\_1^\\prime$ and $\\hat{e}\_2^\\prime$ in terms of $\\hat{e}\_1$, $\\hat{e}\_2$ and the angle of rotation, *θ*.
$$\\begin{aligned}
	\\hat{e}\_1^\\prime &= \\langle \\hat{e}\_1 \\cos \\theta , \\hat{e}\_2 \\sin \\theta\\rangle\\\\
	\\hat{e}\_2^\\prime &= \\langle -\\hat{e}\_1 \\sin \\theta , \\hat{e}\_2 \\cos \\theta \\rangle\\end{aligned}$$

----
## two dimensions

-   We can write the vector, *v*, in terms of the unit vectors describing our axis system
-   $v = v\_1 \\hat{e}\_1 + v\_2 \\hat{e}\_2$
-   (note: $\\hat{e}\_1=\\langle 1, 0 \\rangle$ and $\\hat{e}\_2 = \\langle 0,1 \\rangle$)
-   *v* = ⟨2, 2⟩=2⟨1, 0⟩+2⟨0, 1⟩

----
## two dimensions

-   When expressed in the transformed coordinate system, we refer to *v*<sup>′</sup>
-   *v*<sup>′</sup> = ⟨*v*<sub>1</sub>cos*θ* + *v*<sub>2</sub>sin*θ*, −*v*<sub>1</sub>sin*θ* + *v*<sub>2</sub>cos*θ*⟩
-   $v^\\prime = \\langle 2\\sqrt{2}, 0 \\rangle$
-   We can recover the original vector from the transformed coordinates:
-   $v = v\_1^\\prime \\hat{e}\_1^\\prime + v\_2^\\prime \\hat{e}\_2^\\prime$
-   (note: $\\hat{e}\_1^\\prime=\\langle \\frac{\\sqrt{2}}{2},\\frac{\\sqrt{2}}{2} \\rangle$ and $\\hat{e}\_2^\\prime = \\langle -\\frac{\\sqrt{2}}{2},\\frac{\\sqrt{2}}{2} \\rangle$)
-   $v = 2\\sqrt{2}\\langle \\frac{\\sqrt{2}}{2},\\frac{\\sqrt{2}}{2} \\rangle, 0 \\langle -\\frac{\\sqrt{2}}{2},\\frac{\\sqrt{2}}{2} \\rangle = \\langle 2, 2 \\rangle$

----
## general

-   Coordinate transformation can become much more complicated in three dimensions, and with higher-order tensors
-   It is convenient to define a general form of the coordinate transformation in index notation
-   We define *Q*<sub>*ij*</sub> as the cosine of the angle between the *x*<sub>*i*</sub><sup>′</sup> axis and the *x*<sub>*j*</sub> axis.
-   This is also referred to as the “direction cosine”
    *Q*<sub>*ij*</sub> = cos(*x*<sub>*i*</sub><sup>′</sup>, *x*<sub>*j*</sub>)

----
## general

-   We can use this form on our 2D transformation example

$$\\begin{aligned}
	Q\_{ij} &= \\cos (x\_i^\\prime, x\_j)\\\\ &= \\begin{bmatrix}
	\\cos (x\_1^\\prime, x\_1) & \\cos (x\_1^\\prime, x\_2)\\\\
	\\cos (x\_2^\\prime, x\_1) & \\cos (x\_2^\\prime, x\_2)
\\end{bmatrix}\\\\ &= \\begin{bmatrix}
	\\cos \\theta & \\cos (90-\\theta)\\\\
	\\cos (90+\\theta) & \\cos \\theta
\\end{bmatrix} \\\\ &= \\begin{bmatrix}
	\\cos \\theta & \\sin \\theta \\\\
	-\\sin \\theta & \\cos \\theta
\\end{bmatrix}\\end{aligned}$$

----
## general

-   We can transform any-order tensor using *Q*<sub>*ij*</sub>
-   Vectors (first-order tensors): *v*<sub>*i*</sub><sup>′</sup> = *Q*<sub>*ij*</sub>*v*<sub>*j*</sub>
-   Matrices (second-order tensors): *σ*<sub>*mn*</sub><sup>′</sup> = *Q*<sub>*mi*</sub>*Q*<sub>*nj*</sub>*σ*<sub>*ij*</sub>
-   Fourth-order tensors: *C*<sub>*ijkl*</sub><sup>′</sup> = *Q*<sub>*im*</sub>*Q*<sub>*jn*</sub>*Q*<sub>*ko*</sub>*Q*<sub>*lp*</sub>*C*<sub>*mnop*</sub>

----
## general

-   We can similarly use *Q*<sub>*ij*</sub> to find tensors in the original coordinate system
-   Vectors (first-order tensors): *v*<sub>*i*</sub> = *Q*<sub>*ji*</sub>*v*<sub>*j*</sub><sup>′</sup>
-   Matrices (second-order tensors): *σ*<sub>*mn*</sub> = *Q*<sub>*im*</sub>*Q*<sub>*jn*</sub>*σ*<sub>*ij*</sub><sup>′</sup>
-   Fourth-order tensors: *C*<sub>*ijkl*</sub> = *Q*<sub>*mi*</sub>*Q*<sub>*nj*</sub>*Q*<sub>*ok*</sub>*Q*<sub>*pl*</sub>*C*<sub>*mnop*</sub><sup>′</sup>

----
## mental/emotional health warning

-		Some texts flip the definition of *Q*<sub>*ij*</sub>, and then flip their transformation law accordingly
-		Any time you use tensor transformation, make sure you are following a consistent set of transformation laws

----
## general

-   We can derive some interesting properties of the transformation tensor, *Q*<sub>*ij*</sub>
-   We know that *v*<sub>*i*</sub> = *Q*<sub>*ji*</sub>*v*<sub>*j*</sub><sup>′</sup> and that *v*<sub>*i*</sub><sup>′</sup> = *Q*<sub>*ij*</sub>*v*<sub>*j*</sub>
-   If we substitute (changing the appropriate indexes) we find:
-   *v*<sub>*i*</sub> = *Q*<sub>*ji*</sub>*Q*<sub>*jk*</sub>*v*<sub>*k*</sub>
-   We can now use the Kronecker Delta to substitute *v*<sub>*i*</sub> = *δ*<sub>*ik*</sub>*v*<sub>*k*</sub> which gives
-   *δ*<sub>*ik*</sub>*v*<sub>*k*</sub> = *Q*<sub>*ji*</sub>*Q*<sub>*jk*</sub>*v*<sub>*k*</sub>

---
# examples

----
## example

<script type="text/template">
	<div class="left">
		![empty 3D coordinate system with axes labeled for example problem](../images/example-a.png)
	</div>
	<div class="right">
	  <ul>
	    	<li>Find *Q*<sub>*ij*</sub><sup>1</sup> for rotation of 60<sup>∘</sup> about *x*<sub>2</sub> </li>
				<li>Find *Q*<sub>*ij*</sub><sup>2</sup> for rotation of 30<sup>∘</sup> about *x*<sub>3</sub><sup>′</sup> </li>
				<li>Find *e*<sub>*i*</sub><sup>′′</sup> after both rotations </li>
	    </ul>
	</div>
</script>

----
## example

![3d coordinate system after first rotation](../images/example-b.png) <!-- .element width="50%" --> 

----
## example

![3d coordinate system after second rotation](../images/example-c.png)<!-- .element width="50%" --> 

----
## example

-   *Q*<sub>*ij*</sub><sup>1</sup> = cos(*x*<sub>*i*</sub><sup>′</sup>, *x*<sub>*j*</sub>)
-   *Q*<sub>*ij*</sub><sup>2</sup> = cos(*x*<sub>*i*</sub><sup>′′</sup>, *x*<sub>*j*</sub><sup>′</sup>)

$$Q\_{ij}^1 = \\begin{bmatrix}
\\cos 60 & \\cos 90 & \\cos 150\\\\
\\cos 90 & \\cos 0 & \\cos 90\\\\
\\cos 30 & \\cos 90 & \\cos 60
\\end{bmatrix}$$
$$Q\_{ij}^2 = \\begin{bmatrix}
\\cos 30 & \\cos 60 & \\cos 90\\\\
\\cos 120 & \\cos 30 & \\cos 90\\\\
\\cos 90 & \\cos 90 & \\cos 0
\\end{bmatrix}$$

----
## example

-   We now use *Q*<sub>*ij*</sub> to find $\\hat{e}\_i^\\prime$ and $\\hat{e}\_i^{\\prime \\prime}$
-   First, we need to write $\\hat{e}\_i$ in a manner more consistent with index notation
-   We will indicate axis direction with a superscript, e.g. $\\hat{e}\_1 = e\_i^1$
-   *e*<sub>*i*</sub><sup>′</sup> = *Q*<sub>*ij*</sub><sup>1</sup>*e*<sub>*j*</sub>
-   *e*<sub>*i*</sub><sup>′′</sup> = *Q*<sub>*ij*</sub><sup>2</sup>*e*<sub>*j*</sub><sup>′</sup>
-   How do we find *e*<sub>*i*</sub><sup>′′</sup> in terms of *e*<sub>*i*</sub>?
-   *e*<sub>*i*</sub><sup>′′</sup> = *Q*<sub>*ij*</sub><sup>2</sup>*Q*<sub>*jk*</sub><sup>1</sup>*e*<sub>*k*</sub>

---
# principal values

----
## principal values

-   In the 2D coordinate transformation example, we were able to eliminate one value from a vector using coordinate transformation
-   For second-order tensors, we desire to find the “principal values” where all non-diagonal terms are zero

----
## principal directions

-   The direction determined by the unit vector, *n*<sub>*j*</sub>, is said to be the *principal direction* or *eigenvector* of the symmetric second-order tensor, *a*<sub>*ij*</sub> if there exists a parameter, *λ*, such that
    *a*<sub>*ij*</sub>*n*<sub>*j*</sub> = *λn*<sub>*i*</sub>
-   Where *λ* is called the *principal value* or *eigenvalue* of the tensor

----
## principal values

-   We can re-write the equation
    (*a*<sub>*ij*</sub> − *λδ*<sub>*ij*</sub>)*n*<sub>*j*</sub> = 0

-   This system of equations has a non-trivial solution if and only if det[*a*<sub>*ij*</sub> − *λδ*<sub>*ij*</sub>]=0
-   This equation is known as the characteristic equation, and we solve it to find the principal values of a tensor

----
## example

-   Find the principal values of the tensor

$$A\_{ij} = \\begin{bmatrix}
	1 & 2\\\\
	2 & 4
\\end{bmatrix}$$

-   From the characteristic equation, we know that det[*A*<sub>*ij*</sub> − *λδ*<sub>*ij*</sub>]=0, or

$$\\begin{vmatrix}
	1-\\lambda & 2\\\\
	2 & 4 - \\lambda
\\end{vmatrix} = 0$$

----
## example

-   Calculating the determinant gives
    (1 − *λ*)(4 − *λ*)−4 = 0

-   Multiplying out and simplifying, we find
    *λ*<sup>2</sup> − 5*λ* = *λ*(*λ* − 5)=0

-   This has the solution *λ* = 0, 5

---
# invariants

----
## invariants

-   Every tensor has some invariants which do not change with coordinate transformation
-   These are known as *fundamental invariants*
-   The characteristic equation for a tensor in 3D can be written in terms of the invariants
    det[*a*<sub>*ij*</sub> − *λδ*<sub>*ij*</sub>]= − *λ*<sup>3</sup> + *I*<sub>*α*</sub>*λ*<sup>2</sup> − *II*<sub>*α*</sub>*λ* + *III*<sub>*α*</sub> = 0

----
## invariants

-   The invariants can be found by the following equations
$$\\begin{aligned}
	I\_\\alpha &= a\_{ii}\\\\
	II\_\\alpha &= \\frac{1}{2}(a\_{ii} a\_{jj} - a\_{ij}a\_{ij})\\\\
	III\_\\alpha &= \\det \[ a\_{ij}\]\\end{aligned}$$

----
## invariants

-   In the principal direction, *a*<sub>*ij*</sub><sup>′</sup> will be

$$a\_{ij}^\\prime = \\begin{bmatrix}
	\\lambda\_1 & 0 & 0\\\\
	0 & \\lambda\_2 & 0\\\\
	0 & 0 & \\lambda\_3
\\end{bmatrix}$$

-   Since invariants do not change with coordinate systems, we can also write the invariants as

$$\\begin{aligned}
	I\_\\alpha &= \\lambda\_1 + \\lambda\_2 + \\lambda\_3\\\\
	II\_\\alpha &= \\lambda\_1\\lambda\_2 + \\lambda\_2 \\lambda\_3 + \\lambda\_3 \\lambda\_1\\\\
	III\_\\alpha &= \\lambda\_1 \\lambda\_2 \\lambda\_3\\end{aligned}$$

---
# principal directions

----
## principal directions

-   We defined principal directions earlier
    (*a*<sub>*ij*</sub> − *λδ*<sub>*ij*</sub>)*n*<sub>*j*</sub> = 0

-   *λ* are the principal values and *n*<sub>*j*</sub> are the principal directions
-   For each eigenvalue there will be a principal direction
-   We find the principal direction by substituting the solution for *λ* back into this equation

----
## example

-   Find the principal directions for the earlier principal values example
-   Recall *λ* = 0, 5, let us say *λ*<sub>1</sub> = 5, we find *n*<sub>*j*</sub><sup>(1)</sup> by

$$\\begin{bmatrix}
	1-\\lambda\_1 & 2\\\\
	2 & 4-\\lambda\_1
\\end{bmatrix} \\begin{Bmatrix}
	n\_1 \\\\ n\_2
\\end{Bmatrix} = 0$$

-   This gives

$$\\begin{bmatrix}
	-4 & 2\\\\
	2 & -1
\\end{bmatrix} \\begin{Bmatrix}
	n\_1 \\\\ n\_2
\\end{Bmatrix} = 0$$

----
## example

-   We proceed to solve the equations using row-reduction, but we find

$$\\begin{bmatrix}
	2 & -1\\\\
	0 & 0
\\end{bmatrix} \\begin{Bmatrix}
	n\_1 \\\\ n\_2
\\end{Bmatrix} = 0$$

-   This means we cannot uniquely solve for *n*<sub>*j*</sub>
-   We are only concerned with the direction, magnitude is not important
-   Choose *n*<sub>2</sub> = 1, solve for *n*<sub>1</sub>
-   $n^{(1)} = \\langle \\frac{1}{2}, 1 \\rangle$

----
## example

-   Similarly, for *λ*<sub>2</sub> = 0, we find

$$\\begin{bmatrix}
	1 & 2\\\\
	2 & 4
\\end{bmatrix} \\begin{Bmatrix}
	n\_1 \\\\ n\_2
\\end{Bmatrix} = 0$$

-   Which, after row-reduction, becomes

$$\\begin{bmatrix}
	1 & 2\\\\
	0 & 0
\\end{bmatrix} \\begin{Bmatrix}
	n\_1 \\\\ n\_2
\\end{Bmatrix} = 0$$

-   If we choose *n*<sub>2</sub> = 1, we find *n*<sub>1</sub> = −2
-   This gives *n*<sup>(2)</sup> = ⟨ − 2, 1⟩

----
## example

-   We can assemble a transformation matrix, *Q*<sub>*ij*</sub>, from the principal directions
-   First we need to normalize them to unit vectors
-   $||n^{(1)}|| = \\sqrt{\\frac{5}{4}}$
-   $\\hat{n}^{(1)} = \\frac{2}{\\sqrt{5}} \\langle \\frac{1}{2}, 1 \\rangle = \\langle \\frac{1}{\\sqrt{5}}, \\frac{2}{\\sqrt{5}} \\rangle$
-   $||n^{(2)}|| = \\sqrt{5}$
-   $\\hat{n}^{(2)} = \\langle \\frac{-2}{\\sqrt{5}}, \\frac{1}{\\sqrt{5}} \\rangle $

----
## example

-   This gives

$$Q\_{ij} = \\frac{1}{\\sqrt{5}}\\begin{bmatrix}
	1 & 2\\\\
	-2 & 1
\\end{bmatrix}$$

-   And we find
    *A*<sub>*mn*</sub><sup>′</sup> = *Q*<sub>*mi*</sub>*Q*<sub>*nj*</sub>*A*<sub>*ij*</sub>

$$A\_{ij}^\\prime = \\begin{bmatrix}
	5 & 0 \\\\
	0 & 0
\\end{bmatrix}$$

---
# examples

----
## example

-   Find principal values, principal directions, and invariants for the tensor
		
$$c\_{ij} = \\begin{bmatrix}
	8 & 0 & 0\\\\
	0 & 3 & 1\\\\
	0 & 1 & 3
\\end{bmatrix}$$

----
## example

-   Characteristic equation simplifies to
-   −*λ*<sup>3</sup> + 14*λ*<sup>2</sup> − 56*λ* + 64 = 0
-   Which has the solutions *λ* = 2, 4, 8

----
## example

-   To find the principal direction for *λ*<sub>1</sub> = 8

$$\\begin{bmatrix}
	8-8 & 0 & 0\\\\
	0 & 3-8 & 1\\\\
	0 & 1 & 3-8
\\end{bmatrix}\\begin{Bmatrix}
	n\_1 \\\\ n\_2 \\\\ n\_3
\\end{Bmatrix} = 0$$

----
## example

-   After row-reduction, we find

$$\\begin{bmatrix}
	0 & 0 & 0\\\\
	0 & 0 & -24\\\\
	0 & 1 & -5
\\end{bmatrix}\\begin{Bmatrix}
	n\_1 \\\\ n\_2 \\\\ n\_3
\\end{Bmatrix} = 0$$

-   This means that *n*<sub>3</sub> = 0 and, as a result, *n*<sub>2</sub> = 0.

-   *n*<sub>1</sub> can be any value, we choose *n*<sub>1</sub> = 1 to give a unit vector.
-   *n*<sup>(1)</sup> = ⟨1, 0, 0⟩

----
## example

-   To find the principal direction for *λ*<sub>2</sub> = 4

$$\\begin{bmatrix}
	8-4 & 0 & 0\\\\
	0 & 3-4 & 1\\\\
	0 & 1 & 3-4
\\end{bmatrix}\\begin{Bmatrix}
	n\_1 \\\\ n\_2 \\\\ n\_3
\\end{Bmatrix} = 0$$

----
## example

-   After row-reduction, we find

$$\\begin{bmatrix}
	4 & 0 & 0\\\\
	0 & -1 & 1\\\\
	0 & 0 & 0
\\end{bmatrix}\\begin{Bmatrix}
	n\_1 \\\\ n\_2 \\\\ n\_3
\\end{Bmatrix} = 0$$

-   This means that *n*<sub>1</sub> = 0
-   We also know that *n*<sub>2</sub> = *n*<sub>3</sub>, so we choose *n*<sub>2</sub> = *n*<sub>1</sub> = 1
-   This gives $n^{(2)} = \\frac{1}{\\sqrt{2}}\\langle 0, 1, 1 \\rangle$ after normalization

----
## example

-   To find the principal direction for *λ*<sub>3</sub> = 2

$$\\begin{bmatrix}
	8-2 & 0 & 0\\\\
	0 & 3-2 & 1\\\\
	0 & 1 & 3-2
\\end{bmatrix}\\begin{Bmatrix}
	n\_1 \\\\ n\_2 \\\\ n\_3
\\end{Bmatrix} = 0$$

----
## example

-   After row-reduction, we find

$$\\begin{bmatrix}
	6 & 0 & 0\\\\
	0 & 1 & 1\\\\
	0 & 0 & 0
\\end{bmatrix}\\begin{Bmatrix}
	n\_1 \\\\ n\_2 \\\\ n\_3
\\end{Bmatrix} = 0$$

-   This means that *n*<sub>1</sub> = 0
-   We also know that *n*<sub>2</sub> = −*n*<sub>3</sub>, so we choose *n*<sub>2</sub> = 1 and *n*<sub>1</sub> = −1
-   This gives $n^{(3)} = \\frac{1}{\\sqrt{2}}\\langle 0, 1, -1 \\rangle$ after normalization

----
## example

-   In summary, for *c*<sub>*ij*</sub> we have:
-   *λ*<sub>1</sub> = 8 and *n*<sup>(1)</sup> = ⟨1, 0, 0⟩
-   *λ*<sub>2</sub> = 4 and $n^{(2)} = \\frac{1}{\\sqrt{2}}\\langle 0, 1, 1 \\rangle$
-   *λ*<sub>3</sub> = 2 and $n^{(3)} = \\frac{1}{\\sqrt{2}}\\langle 0, 1, -1 \\rangle$
-   We can assemble *n*<sup>(*i*)</sup> into a transformation tensor

$$Q\_{ij} = \\frac{1}{\\sqrt{2}}\\begin{bmatrix}
	\\sqrt{2} & 0 & 0\\\\
	0 & 1 & 1\\\\
	0 & 1 & -1
\\end{bmatrix}$$

----
## example

-   What is *c*<sub>*ij*</sub><sup>′</sup>?
-   *c*<sub>*ij*</sub><sup>′</sup> = *Q*<sub>*im*</sub>*Q*<sub>*jn*</sub>*c*<sub>*mn*</sub>

$$c\_{ij}^\\prime = \\begin{bmatrix}
	8 & 0 & 0 \\\\
	0 & 4 & 0 \\\\
	0 & 0 & 2
\\end{bmatrix}$$

----
## example

-   We can also find the invariants for

$$c\_{ij} = \\begin{bmatrix}
	8 & 0 & 0\\\\
	0 & 3 & 1\\\\
	0 & 1 & 3
\\end{bmatrix}$$

-   Recall:

$$\\begin{aligned}
	I\_\\alpha &= a\_{ii}\\\\
	II\_\\alpha &= \\frac{1}{2}(a\_{ii} a\_{jj} - a\_{ij}a\_{ij})\\\\
	III\_\\alpha &= \\det \[ a\_{ij}\]
\\end{aligned}$$

----
## example

-   First invariant
    *I*<sub>*α*</sub> = *a*<sub>*ii*</sub> = 8 + 3 + 3 = 14

-   Second invariant

$$II\_\\alpha = \\frac{1}{2}(a\_{ii} a\_{jj} - a\_{ij}a\_{ij})$$
    *a*<sub>*ii*</sub>*a*<sub>*jj*</sub> = 14 × 14
    *a*<sub>*ij*</sub>*a*<sub>*ij*</sub> = *a*<sub>11</sub>*a*<sub>11</sub> + *a*<sub>12</sub>*a*<sub>12</sub> + *a*<sub>13</sub>*a*<sub>13</sub> + ... + *a*<sub>33</sub>*a*<sub>33</sub>

$$II\_\\alpha = \\frac{1}{2}(196 - 84) = 56$$

----
## example

-   Third invariant
    *III*<sub>*α*</sub> = det[*a*<sub>*ij*</sub>\]
    *III*<sub>*α*</sub> = 8 × (3 × 3 − 1 × 1)=64


