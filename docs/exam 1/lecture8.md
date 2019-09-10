# AE837
## Advanced Mechanics of Damage Tolerance
Dr. Nicholas Smith<br/>
Wichita State University, Department of Aerospace Engineering
September 12, 2019

----
## upcoming schedule

-   Sep 12 - Finite Size Effects, K-Dominance, HW 2 Due
-   Sep 17 - Fracture Criterion 
-   Sep 19 - Exam Review, HW 3 Due
-   Sep 24 - Exam 1

----
## outline

<!-- vim-markdown-toc GFM -->

* finite specimen effects
* williams crack tip fields
* K-Dominance

<!-- vim-markdown-toc -->

---
# finite specimen effects

----
## finite effects

-   Up to this point, we have considered infinitely large panels
-   In general, the effect of finite size is modeled using numerical techniques, such as finite elements
-   These corrections will generally take the form of some dimensionless factor that is multiplied with the infinite stress intensity factor
-   <!-- .element style="list-style-type:none" --> $$ K_I = \sigma \sqrt{\pi a} F(a/b, a/H) $$

----
## finite specimen effects

-   Finite specimen correction factors are often found using finite element analysis
-   For finite width effects, Irwin proposed the following correction
-   <!-- .element style="list-style-type:none" --> $$ F(a/b) = 1 + 0.128\left( \frac{a}{b} \right ) -0.288 \left( \frac{a}{b} \right )^2 + 1.525 \left( \frac{a}{b} \right )^3 $$


---
# williams crack tip fields

----
## williams crack tip fields

-   All the solutions we have found for the stress field near the crack tip have a singularity
-   This singularity even has the same order (inverse square root)
-   Williams approached the solution in a slightly different way to expand the terms

----
## modes i and ii

-   We start by considering the Airy stress function in polar coordinates expanded as a general series
-   <!-- .element style="list-style-type:none" --> $$	\phi = \sum r^{\lambda_n+1}F_n(\theta) $$
-   Where $\lambda_n$ are the Eigenvalues and $F_n$ are the corresponding Eigenfunctions

----
## modes i and ii

-   To satisfy compatibility ($\nabla^2 \nabla^2 \phi = 0$) the Eigenfunctions must take the form
-   <!-- .element style="list-style-type:none" --> $$F_n(\theta) = A_n \sin (\lambda_n+1)\theta + B_n \cos(\lambda_n + 1)\theta + C_n\sin(\lambda_n-1)\theta + D_n \cos(\lambda_n-1)\theta$$
-   Next the forms for the series are determined by satisfying the boundary conditions

----
## mode i

-   In mode one the solutions for the first two terms are
$$ \begin{align}
\sigma_{rr} &= D_1 r^{-1/2} \left[ -\frac{1}{4}\cos \frac{3\theta}{2} + \frac{5}{4} \cos {\theta}{2}\right ] + 2 D_2 \cos 2\theta + 2 D_2 + O(r^{1/2})\\\\
\sigma_{\theta \theta} &= D_1 r^{-1/2} \left[ \frac{1}{4}\cos \frac{3\theta}{2} + \frac{3}{4} \cos {\theta}{2}\right ] - 2 D_2 \cos 2\theta + 2 D_2 + O(r^{1/2})\\\\
\sigma_{r\theta} &= D_1 r^{-1/2} \left[ \frac{1}{4}\sin\frac{3\theta}{2} + \frac{1}{4} \sin {\theta}{2}\right ] - 2 D_2 \cos 2\theta + O(r^{1/2}) \end{align}$$

----
## mode i

-   We can see that the constant $D_1$ corresponds to the stress intensity factor
-   The second term, $D_2$, corresponds to something known as the $T-\text{stress}$
-   The $T-\text{stress}$ influences the size and shape of the plastic zone

----
## mode ii

-   The Mode II problem can be solved in a similar fashion, but the Airy stress functions will be odd functions of $\theta$ (instead of even as in the mode I solution)

---
# K-Dominance

----
## K-Dominance

-   We have now established that there are two parts to the stress field near a crack tip, a singular part and a non-singular part
-   If we are sufficiently close to the crack tip, the singular part dominates fracture behavior
-   We define the "K-Dominance Zone" to determine how close to the crack tip we need to be to ignore non-singular behavior
-   <!-- .element style="list-style-type:none" --> $$ \Lambda = \frac{K_I/\sqrt{2\pi x}}{K_I/\sqrt{2\pi x} + |\text{non-singular part of }\sigma_{yy}|} = \frac{K_I/\sqrt{2\pi x}}{\sigma_{yy}}$$

----
## K-Dominance

-   The closer $\Lambda$ is to 1, the more dominant the singularity
-   We will consider an example case with a known solution for the stress field to see how the K-Dominance zone can be used

----
## example

-   For a Mode I crack under biaxial tension, we have 
-   <!-- .element style="list-style-type:none" --> $$ \sigma_{yy} = \frac{(x+a)\sigma_0}{\sqrt{x(x+2a)}} $$
-   We recall that the stress intensity factor is $K_I = \sigma_0 \sqrt{\pi a}$

----
## example

$$\begin{align}
	\frac{K_I}{\sqrt{2\pi x}} &= \frac{\sigma_0 \sqrt{\pi a}}{\sqrt{2\pi x}} = \frac{\sigma_0}{\sqrt{2}\sqrt{x/a}} \\\\
	\Lambda &= \frac{K_I/\sqrt{2\pi x}}{\sigma_{yy}} = \frac{\sigma_0}{\sqrt{2} \sqrt{x/a}} \frac{a \sqrt{x/a} \sqrt{x/a+2}}{a(x/a+1)\sigma_0} \\\\
	\Lambda &= \frac{\sqrt{x/a+2}}{\sqrt{2}(x/a+1)}
\end{align}$$

----
## example

-   We can now solve for $x/a$ for some $\Lambda$
-   Find the size of the K-Dominance zone of $\Lambda=0.95$
-   We find $x \approx 0.07a$
