# state-of-strain-at-point-and-strain-transformations

| ![](../../attachments/engr-727-001-advanced-mechanics-of-materials/deformation_of_body_under_load_220203_132500_EST.png) |
|:--:|
| Consider body subjected to external loading that has been translated and rotated which can be measured as displacement. |

The percentage of this displacement with respect to the body’s original position is strain. There are two methods to measure this displacement: **Lagrangian** and **Eulerian**.

| ![](../../attachments/engr-727-001-advanced-mechanics-of-materials/strain_defined_220203_132613_EST.png) |
|:--:|
| Normal strain, the unit chage in length, is defined as: <span class="math inline">$\epsilon_{x} = \frac{\Delta L}{L_{0}}$</span>. |

**Plane Strain**

A 2D case in which all points in the body, before and after loading, remain in the same plane: *ϵ*<sub>*z*</sub> = 0, *γ*<sub>*x**z*</sub> = *γ*<sub>*y**z*</sub> = 0. We assume that the strains in the 3rd direction are infinetesimally small. Normal and longitudinal strains are given by:

$$\begin{split}
\epsilon_{x} &= \frac{\partial u}{\partial x} \\\
\epsilon_{y} &= \frac{\partial v}{\partial y}
\end{split}$$

By making a *small angles assumption*, the angle, *α*<sub>*x*</sub> between *A**B* and *A*′*B*′ is so small that *A**B* ≈ *A*′*B*′:

$$\begin{split}
\alpha_{x} &\approx \tan\dots \\\
 &=
\end{split}$$

**Three-Dimensional Strain**

The same principles from 2D are applied 3D but now includes the 3rd component.

FEA Codes

Most commercial softwares rely on *small angle assumptions* for their codes. While this assumption is suitable for mosst engineering problems, the codes do also include logic to handle those case with substantial strain.

Similar to [???](#eq-stress_tensor), a tensor for the strains can also be made:

$$\begin{equation}
\[\epsilon_{ij}\] = \begin{bmatrix}
\epsilon_{x} & \frac{1}{2}\gamma_{xy} & \frac{1}{2}\gamma_{xz} \\\
\frac{1}{2}\gamma_{xy} & \epsilon_{y} & \frac{1}{2}\gamma_{xz} \\\
\epsilon_{z} & \frac{1}{2}\gamma_{xy} & \frac{1}{2}\gamma_{xz}
\end{bmatrix}
\end{equation}$$

Green Strain  
An alternative definition for large strains. This is the application of **Green’s Theorem** from calculus.

| ![](../../attachments/engr-727-001-advanced-mechanics-of-materials/green_strain_220203_134218_EST.png) |
|:--:|
| foo |

$$\begin{equation}
\begin{split}
\epsilon_{x} &= \frac{(A'B')^{2} - (AB)^{2}}{2(AB)^{2}} \\\
 &= \frac{(dx + \frac{\partial u}{\partial x}dx)^{2} + (\frac{\partial v}{\partial x}dx)^{2} - (dx)^{2}}{2(dx)^{2}} \\\
 &= \frac{\partial u}{\partial x} + \frac{1}{2}\biggl\[ \Bigl(\frac{\partial u}{\partial x}\Bigr)^{2} + \Bigl(\frac{\partial v}{\partial x}\Bigr)^{2} \biggr\] \\\
 &= \frac{A'B' - AB}{AB} \\\
\implies \epsilon_{y} &= \frac{\partial v}{\partial y} + \frac{1}{2}\biggl\[ \Bigl(\frac{\partial u}{\partial y}\Bigr)^{2} + \Bigl(\frac{\partial v}{\partial y}\Bigr)^{2} \biggr\] \\\
\gamma_{xy} &= \frac{\partial v}{\partial x} + \frac{\partial u}{\partial y} + \dots
\end{split}
\end{equation}$$

The last equation for *ϵ*<sub>*x*</sub> is *engineering strain*.

**Equations of Compatibility**

Mathematically, it means that the displacements *u*, *v*, and *w* satisfy the boundary conditions, are single-valued, and are continuous functions of position. Physically, this means that the body must be peiced together: no voids are created in the deformed body. In the tensor notation, we have 3 strain components from 2 displacements (in 2D); therefore, we need a third equation to consider these effects separately. Kinematic equations connect six components of strain to only three components of displacement. We cannot, therefore, arbtrarily specify all the strains as functions of *x*, *y*, and *z*. In 2D strain, differentiation of *ϵ*<sub>*x*</sub> twice wrt *y*, …​

$$\begin{equation}
\begin{split}
\frac{\partial^{2}\epsilon_{x}}{\partial y^{2}} &= \frac{\partial^{3}u}{\partial x\\partial y^{2}} \\\
\frac{} &=
\end{split}
\end{equation}$$

This relation is the condition of compatibility of the 2D problem, expressed in terms of strain. The equations can be expanded to 3D:

| ![](../../attachments/engr-727-001-advanced-mechanics-of-materials/deformation_in_any_direction_220203_135448_EST.png) |
|:--:|
| A line segment with infinitesimal unit length is considered, whose orientation in relation to the coordinate axes is defined by the direction cosines: <span class="math inline"><em>l</em></span>, <span class="math inline"><em>m</em></span>, and <span class="math inline"><em>n</em></span>. |

The components in directions *x* and *y* of the displacement vector may be obtained directly. In tensor notation, $\begin{bmatrix}\delta_{x} \\\ \delta_{y} \\\ \delta_{z}\end{bmatrix} = {\delta} = \begin{bmatrix} \epsilon_{x} \dots \end{bmatrix}\begin{bmatrix}l \\\ m \\\ n\end{bmatrix}$. This reduces to ${\delta} = \[\epsilon_{ij}\begin{bmatrix}l \\\ m \\\ n\end{bmatrix}$\]. Since $\vec{OQ}$ has unit length and inly infinitesimal deformations, the longitudinal strain in its direction is obtained by the projection of *δ⃗* in the direction *n̂*: $\epsilon = \[\delta\]\cdot \hat{n} = \begin{bmatrix}\delta_{x} \\\ \delta_{y} \\\ \delta_{z}\end{bmatrix}\begin{bmatrix}l & m & n\end{bmatrix}^{T}$.

| ![](../../attachments/engr-727-001-advanced-mechanics-of-materials/rotation_between_two_line_segments_220203_140233_EST.png) |
|:--:|
| Consider two infinitesimal lines segments <span class="math inline"><em>P</em><em>A</em></span> and <span class="math inline"><em>P</em><em>B</em></span> of length emanating from point <span class="math inline"><em>P</em></span>. This direction of cosines between lines <span class="math inline"><em>P</em><em>A</em></span> and <span class="math inline"><em>P</em><em>B</em></span> are () and (), respectively. |

Here, the calculations for the dot product between these vectors becomes quite cumbersome:

*γ*<sub>12</sub> = 2*l*<sub>1</sub>*l*<sub>2</sub>*ϵ*<sub>*x*</sub> + 2*m*<sub>1</sub>*m*<sub>2</sub>*ϵ*<sub>*y*</sub> + 2*n*<sub>1</sub>*n*<sub>2</sub>*ϵ*<sub>*z*</sub> + 2(*l*<sub>1</sub>*m*<sub>2</sub> + *l*<sub>2</sub>*m*<sub>1</sub>)*ϵ*<sub>*x**y*</sub> + 2(*m*<sub>1</sub>*n*<sub>2</sub> + *m*<sub>2</sub>*n*<sub>1</sub>)*ϵ*<sub>*y**z*</sub> + 2(*l*<sub>1</sub>*n*<sub>2</sub> + *l*<sub>2</sub>*n*<sub>1</sub>)*ϵ*<sub>*x**z*</sub>

**Transformation of Three-Dimensional Strain**

The reference axes of the strain tensor may be transposed by means of the matrix operation. Using the corresponding stress relation by replacing *σ* by *ϵ* and *τ* by $\frac{\gamma}{2}$.

<table><caption><span class="math inline"><em>l</em><sub>1</sub> = cos (<em>x</em>′, <em>x</em>)</span></caption><colgroup><col style="width: 33%" /><col style="width: 33%" /><col style="width: 33%" /></colgroup><thead><tr class="header"><th style="text-align: left;"></th><th style="text-align: left;">x</th><th style="text-align: left;">y</th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><p>z</p></td><td style="text-align: left;"><p>x</p></td><td style="text-align: left;"><p><span class="math inline"><em>l</em><sub>1</sub></span></p></td></tr></tbody></table>

*l*<sub>1</sub> = cos (*x*′, *x*)

**Principal Strains in Three Dimensions**

These are *eigenvalue* problems. They are determined in a similar manner as principal stresses.

**Principal Strains in Two Dimensions**

…​

1.  Determine something

We check for compatibility:

$$\begin{split}
\epsilon_{x} &= c(x^{2} + y^{2}) \\\
\epsilon_{y} &= y^{2} \\\
\epsilon_{xy} &= cxy + \frac{1}{2}\gamma_{xy} \\\
\implies \gamma_{xy} &= 2cxy \\\
\frac{\partial\epsilon_{x}}{\partial y} &= 2cy \\\
\frac{\partial^{2}\epsilon_{x}}{\partial y^{2}} &= 2c \\\
\frac{\partial\epsilon_{y}}{\partial x} &= 0 \\\
\frac{\partial^{2}\epsilon_{y}}{\partial x^{2}} &= 0 \\\
\frac{\partial^{2}\epsilon_{y}}{\partial y^{2}}\dots
\end{split}$$

| ![](../../attachments/engr-727-001-advanced-mechanics-of-materials/problem_set_2-2-2_problem_statement_220203_142609_EST.png) |
|:--:|
| Problem 2: Rectangle <span class="math inline"><em>A</em><em>B</em><em>C</em><em>D</em></span> is inscribed on the surface of a member prior to loading. Following the application of the load, the displacement field is expressed by: <span class="math inline"><em>u</em> = <em>c</em>(2<em>x</em> + <em>y</em><sup>2</sup>)</span> and <span class="math inline"><em>v</em> = <em>c</em>(<em>x</em><sup>2</sup> − 3<em>y</em><sup>2</sup>)</span>. |

We are given *c* = 10<sup> − 4</sup>, and we must find *u* and *v*.

$$\begin{split}
\epsilon_{x} &= \frac{\partial u}{\partial x} = 2c = 2e-4 = ${engr(2e-4)} \\\
\epsilon_{y} &= \frac{\partial v}{\partial y} = -6cy = -(6e-4)(0.5) = ${-(6e-4)\*0.5} \\\
\gamma_{xy} &= \frac{\partial u}{\partial y} + \frac{\partial v}{\partial x} = 2cy + 2cx \\\
 &= (2e-4)(3 + 0.5) = ${engr((2e-4)\*(3 + 0.5))}~\frac{m}{m}
\end{split}$$

| ![](../../attachments/engr-727-001-advanced-mechanics-of-materials/problem_set_2-2-3_problem_statement_220208_135550_EST.png) |
|:--:|
| A <span class="math inline">3 <em>m</em></span> by <span class="math inline">2 <em>m</em></span> rectangular, thin plate is deformed by the movement of the <span class="math inline"><em>B</em></span> to <span class="math inline"><em>B</em>′</span> as shown by the dashed lines. Asuming a displacement field of the form <span class="math inline"><em>u</em> = <em>c</em><sub>1</sub><em>x</em><em>y</em></span> and <span class="math inline"><em>v</em> = <em>c</em><sub>2</sub><em>x</em><em>y</em></span>, wherein <span class="math inline"><em>c</em><sub>1</sub></span> and <span class="math inline"><em>c</em><sub>2</sub></span> are constants, determine (a) expressions for displacements <span class="math inline"><em>u</em></span> and <span class="math inline"><em>v</em></span>; (b) strain components <span class="math inline"><em>ϵ</em><sub><em>x</em></sub></span>, <span class="math inline"><em>ϵ</em><sub><em>y</em></sub></span>, and <span class="math inline"><em>γ</em><sub><em>x</em><em>y</em></sub></span> at point <span class="math inline"><em>B</em></span>; and, (c) the normal strain <span class="math inline"><em>ϵ</em><sub><em>x</em></sub></span> in the direction of line <span class="math inline"><em>Q</em><em>B</em></span>. Verify that the strain field is possible. |

From the initial conditions, we find that the constants are given by:

$$\begin{split}
0.003 &= c_{1}(3)(3) \\\
\implies c_{1} &= ${engr(3\*2/0.003)} \\\
0.0015 &= c_{2}(3)(6) \\\
\implies c_{2} &= ${engr(3\*6/0.0015)}
\end{split}$$

Therefore, the strain components can be found:

$$\begin{split}
\epsilon_{x} &= \frac{\partial u}{\partial x} = 0.005y = 0.001 \\\
\epsilon_{y} &= \frac{\partial v}{\partial y} = 0.00025x = 0.00075 \\\
\gamma_{xy} &= \frac{\partial u}{\partial y} + \frac{\partial v}{\partial x} = 0.002
\end{split}$$

By this, the strain tensor is:

$$\epsilon_{ij} = \begin{bmatrix}0.001 & 0.001 \\\ 0.001 & 0.00075\end{bmatrix}$$

The normal strain, *ϵ*<sub>*x*</sub> in the direction of line *Q**B* is:

$$\begin{split}
\hat{n} &= \frac{3\hat{i} + 2\hat{j}}{\sqrt{13}} \\\
\delta = \[\epsilon_{ij}\]\[n\] &= \begin{bmatrix}0.001 & 0.001 \\\ 0.001 & 0.00075\end{bmatrix}\begin{bmatrix}\frac{3}{\sqrt{13}} \\\ \frac{2}{\sqrt{13}}\end{bmatrix} = \begin{bmatrix}0.00138175 \\\ 0.00124808\end{bmatrix} \\\
\epsilon_{QB} = \delta \cdot \hat{n} &= \begin{bmatrix}0.00138175 \\\ 0.00124808\end{bmatrix} \cdot \begin{bmatrix}\frac{3}{\sqrt{13}} \\\ \frac{2}{\sqrt{13}}\end{bmatrix} = ${engr(np.matmul(np.array(\[0.00138675, 0.00124808\]), np.array(\[3/np.sqrt(13), 2/np.sqrt(13)\])))}
\end{split}$$

$$\begin{split}
J_{1} &= \epsilon_{x} + \epsilon_{y} + \epsilon_{z} = -300 \\\
J_{2} &= \epsilon_{x}\epsilon_{y} + \epsilon_{x}\epsilon_{z} + \epsilon_{y}\epsilon_{z} - \frac{1}{4}(\dots) \\\
 &= 200(-100) + 200(-400) + (-100)(-400) + \frac{1}{4}(400^{2} + 600^{2} + 1000^{2}) = -4.4e5 \\\
J_{3} &= \begin{vmatrix}\epsilon_{x} & \frac{1}{2}\gamma_{xy} & \frac{1}{2}\gamma_{xz} \\\ \frac{1}{2}\gamma_{xy} & \epsilon_{y} & \frac{1}{2}\gamma_{yz} \\\ \frac{1}{2}\gamma_{xz} & \frac{1}{2}\gamma_{yz} & \epsilon_{z}\end{vmatrix} = 5.8e7
\end{split}$$

<table><caption>To answer the strain in <span class="math inline"><em>x</em>′</span> direction, we do a strain transformation.</caption><colgroup><col style="width: 25%" /><col style="width: 25%" /><col style="width: 25%" /><col style="width: 25%" /></colgroup><thead><tr class="header"><th style="text-align: left;"></th><th style="text-align: left;"><span class="math inline"><em>x</em></span></th><th style="text-align: left;"><span class="math inline"><em>y</em></span></th><th style="text-align: left;"><span class="math inline"><em>z</em></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><p><span class="math inline"><em>x</em>′</span></p></td><td style="text-align: left;"><p><span class="math inline">$\frac{\sqrt{3}}{2}$</span></p></td><td style="text-align: left;"><p><span class="math inline">$\frac{1}{2}$</span></p></td><td style="text-align: left;"><p><span class="math inline">0</span></p></td></tr><tr class="even"><td style="text-align: left;"><p><span class="math inline"><em>y</em>′</span></p></td><td style="text-align: left;"><p><span class="math inline">$-\frac{1}{2}$</span></p></td><td style="text-align: left;"><p><span class="math inline">$\frac{\sqrt{3}}{2}$</span></p></td><td style="text-align: left;"><p><span class="math inline">0</span></p></td></tr><tr class="odd"><td style="text-align: left;"><p><span class="math inline"><em>z</em>′</span></p></td><td style="text-align: left;"><p><span class="math inline">0</span></p></td><td style="text-align: left;"><p><span class="math inline">0</span></p></td><td style="text-align: left;"><p><span class="math inline">1</span></p></td></tr></tbody></table>

To answer the strain in *x*′ direction, we do a strain transformation.

From [???](#tab-problem_set_2-2-5_strain_transformation), the strain in the *x*′ direction is:

$$\begin{split}
\epsilon_{ij}' &= \[T\]\[\epsilon_{ij}\]\[T\]^{T} \\\
 &= \begin{bmatrix}\frac{\sqrt{3}}{2} & \frac{1}{2} & 0 \\\ -\frac{1}{2} & \frac{\sqrt{3}}{2} & 0 \\\ 0 & 0 & 1\end{bmatrix}\begin{bmatrix}200 & 300 & 200 \\\ 300 & -100 & 500 \\\ 200 & 500 & -400\end{bmatrix}\[T\]^{T} \\\
 &= \begin{bmatrix}384.8 & -175 & 423.2 \\\ -175 & -134.8 & 76.8 \\\ 425.2 & 76.8 & -400\end{bmatrix}
\end{split}$$

| ![](../../attachments/engr-727-001-advanced-mechanics-of-materials/problem_set_2-2-7_problem_statement_220210_132445_EST.png) |
|:--:|
| Problem 7: A square panel in the side of a ship is loaded so that the panel is in a state of plane strain (<span class="math inline"><em>ϵ</em><sub><em>z</em><em>z</em></sub> = <em>ϵ</em><sub><em>z</em><em>x</em></sub> = <em>ϵ</em><sub><em>z</em><em>y</em></sub> = 0</span>). Determine the displacements for the panel given the deformations shown and the strain components for the <span class="math inline">(<em>x</em>, <em>y</em>)</span> coordinate axes. Determine the strain components for the <span class="math inline">(<em>x</em>′, <em>y</em>′)</span> axes. |

### Stress-Strain Relationships and Behavior Hooke’s Law

**Elastic Deformation: Hooke’s Law**

We like elastic behaviors because of the linear relationship. If the strains are small, then plastic deformation is not a major concern. Most materials exhibit this initial region of elasticity.

*σ*<sub>*x*</sub> = *E**ϵ*<sub>*x*</sub>,

where *E* is Young’s Modulus of Elasticity. Similarly for shear stresses:

*τ*<sub>*x**y*</sub> = *G**γ*<sub>*x**y*</sub>

**Hooke’s Law and Poisson’s Ratio**

A body, upon being pulled in tension, tends to contract laterally. Ergo, there is transverse deformation with longitudinal strain which is defined by Poisson’s Ratio, *ν*:

$$\begin{equation}
\nu = \frac{\text{lateral strain}}{\text{axial strain}} = -\frac{\epsilon_{y}}{\epsilon_{x}}
\end{equation}$$

Common Poisson’s Ratio

Most metal Poisson’s Ratios are approximate to each other: *ν* ≈ 0.3.

**Volume Change**

By **Law of Conservation of Mass**, there is also a volume change associated with Poisson’s Ratio.

$$\begin{split}
V_{f} &= (1 + \epsilon_{x})dx(1 - \nu\epsilon_{x})dy(1 - \nu\epsilon_{x}dz) \\\
 &= \[1 + (\epsilon_{x} - 2\nu\epsilon_{x}\dots)\]
\end{split}$$

**Elastic Deformation under Multiaxial Loads**

In the one-dimensional case, Hooke’s Law ([Eq. 4-3](#eq-hookes_law)) is very simple, and applied loads case linear changes in normal and transverse strains: *σ* = *E**ϵ* and *τ* = *G**γ*. However, these relationships can be expanded into tensor notation:

$$\begin{bmatrix}\sigma_{x} \\\ \sigma_{y} \\\ \sigma_{z} \\\ \tau_{xy} \\\ \tau_{yz} \\\ \tau_{zx}\end{bmatrix} = \begin{bmatrix}
S_{11} & S_{12} & S_{13} & S_{14} & S_{15} & S_{16} \\\
S_{21} & S_{22} & S_{23} & S_{24} & S_{25} & S_{26} \\\
S_{31} & S_{32} & S_{33} & S_{34} & S_{35} & S_{36} \\\
S_{41} & S_{42} & S_{43} & S_{44} & S_{45} & S_{46} \\\
S_{51} & S_{52} & S_{53} & S_{54} & S_{55} & S_{56} \\\
S_{61} & S_{62} & S_{63} & S_{64} & S_{65} & S_{66}
\end{bmatrix}\begin{bmatrix}\end{bmatrix}$$

Similarly, a compliance matrix can also be made for the multiaxial strains.

Stress-Strain Tensor Notations

These tensor define the stress or strain state at that point in the material. Typically, we like to assume materials exhibit *isotropic* deformation; however, real materials exhibit *anisotropically*.

**Isotropic Elastic Materials**

A materials mechanically *isotropic* if all of its mechanical properties are the same in all spatial directions. In the isotropic case, the constants do not depend on the orientation of the coordinate axes, and most of the constants are either zero or have the same values as other ones. In a two-dimensional case: $\epsilon_{x} = \frac{\sigma_{x}}{E} - \dots$

**Relationship Between Elastic Constants**

If two of the constants *ν*, *E*, and *G* are determined experimentally, the third may be found by:

$$\begin{equation}
G = \frac{E}{2(1 + \nu)}
\end{equation}$$

Alternatively, $\lambda = \frac{\nu E}{(1 + \nu)(1 - 2\nu)}$.

| ![](../../attachments/engr-727-001-advanced-mechanics-of-materials/principal_strain_gage_equations_220210_135335_EST.png) |
|:--:|
| foo |

**Problem 1: Strains are measured on the surface of a brass alloy part as follows: *ϵ*<sub>*x*</sub> = 1600*e* − 6, *ϵ*<sub>*y*</sub> = 1300*e* − 6, and *γ*<sub>*x**y*</sub> = 1500*e* − 6. Estimate the in-plane stresses *σ*<sub>*x*</sub>, *σ*<sub>*y*</sub>, and *τ*<sub>*x**y*</sub>, and also the strain, *ϵ*<sub>*z*</sub> normal to the surface. Assume that the gages were bonded to the metal when there was no load on the part, that there has been no yielding, and that no loading is applied directly to the surface so that *σ*<sub>*z*</sub> = *τ*<sub>*y**z*</sub> = *τ*<sub>*z**x*</sub> = 0.**

We are given the strain state and are asked to assume plane-strain conditions. Before we begin solving the stress state, we must find the material properties for typical brass alloys. Therefore, if we assume that *E* = 110 *G**P**a* and *ν* = 0.3, then $G := \frac{E}{2(1 + \nu)} = ${engr(110e9/(2\*(1 + 0.3)))}~Pa$. The compliance matrix:

$$\begin{split}
S_{ij} &= \begin{bmatrix}\frac{1}{E} & -\frac{\nu}{E} & 0 \\\ -\frac{\nu}{E} & \frac{1}{E} & 0 \\\ 0 & 0 & \frac{1}{G}\end{bmatrix} \\\
 &= \begin{bmatrix}9.091 & -2.727 & 0 \\\ -2.727 & 9.091 & 0 \\\ 0 & 0 & 0.2364\end{bmatrix}e-6
\end{split}$$

The strain vector:

$$\begin{split}
\epsilon &= \begin{bmatrix}\epsilon_{x} \\\ \epsilon_{y} \\\ \gamma_{xy}\end{bmatrix} \\\
 &= \begin{bmatrix}1600 \\\ 1300 \\\ 1500\end{bmatrix}e-6
\end{split}$$

From these matrices, the stress state is:

$$\begin{split}
\sigma &= \vec{c_{ij}}\vec{\epsilon} \\\
 &=
\end{split}$$