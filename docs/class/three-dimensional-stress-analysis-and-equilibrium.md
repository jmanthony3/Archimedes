# three-dimensional-stress-analysis-and-equilibrium

| ![](../../attachments/engr-727-001-advanced-mechanics-of-materials/stress_equilibrium_equations_2d_220120_133143_EST.png) |
|:--:|
| Consider an element of sides <span class="math inline"><em>d</em><em>x</em></span> and <span class="math inline"><em>d</em><em>y</em></span> of some unit thickness. It is assumed that <span class="math inline"><em>σ</em><sub><em>x</em></sub></span>, <span class="math inline"><em>σ</em><sub><em>y</em></sub></span>, <span class="math inline"><em>τ</em><sub><em>x</em><em>y</em></sub></span>, and <span class="math inline"><em>τ</em><sub><em>y</em><em>x</em></sub></span> are functions of <span class="math inline"><em>x</em></span> and <span class="math inline"><em>y</em></span>. Assume that the <span class="math inline"><em>x</em></span> and <span class="math inline"><em>y</em></span> components of the body forces per unit volume, <span class="math inline"><em>F</em><sub><em>x</em></sub></span> and <span class="math inline"><em>F</em><sub><em>y</em></sub></span>. |

In mechanics, there are 2 types of forces: external and internal loads. We often describe these as body forces and remote forces ([Fig. 3-1](#fig-stress_equilibrium_equations_2d)). If we take the sum of the moments about the lower-left corner, then $\sum M_{z} = 0 := (\frac{\partial\sigma_{y}}{\partial y}dxdy)\frac{dx}{2} - (\frac{\partial\sigma_{x}}{\partial x}dxdy)\frac{dy}{2} + (\tau_{xy} + \frac{\partial\tau_{xy}}{\partial x}dx)dxdy - (\tau_{yx} + \frac{\partial\tau_{yx}}{\partial y}dy)dxdy + F_{y}dxdy\frac{dx}{2} - F_{x}dxdy\frac{dy}{2} = 0$. This reduces to *τ*<sub>*x**y*</sub> = *τ*<sub>*y**x*</sub>. Similarly, in 3 dimensions, the following can be found *τ*<sub>*y**z*</sub> = *τ*<sub>*z**y*</sub> and *τ*<sub>*x**z*</sub> = *τ*<sub>*z**x*</sub>. From sum of the *x* forces: $\sum F_{x} = 0 := (\sigma_{x} + \frac{\partial\sigma_{x}\tau_{x}}dx)dy - \sigma_{x}dy + (\tau_{xy} + \frac{\partial\tau_{xy}}{\partial y}dy)dx + \tau_{xy}dx - F_{x}dxdy = 0$. This simplifies to: $(\frac{\partial\sigma_{x}}{\partial x} + \frac{\partial\sigma_{x}}{\partial y} + F_{x})dxdy = 0$. Because *d**x* and *d**y* are non-zero:

$$\begin{split}
\frac{\partial\sigma_{x}}{\partial x} + \frac{\partial\sigma_{x}}{\partial y} + F_{x} &= 0 \\\
\frac{\partial\sigma_{y}}{\partial y} + \frac{\partial\sigma_{y}}{\partial x} + F_{y} &= 0
\end{split}$$

By expanding to 3 dimensions:

$$\begin{split}
\frac{\partial\sigma_{x}}{\partial x} + \frac{\partial\tau_{xy}}{\partial y} + \frac{\partial\tau_{xz}}{\partial z} + F_{x} &= 0 \\\
\frac{\partial\sigma_{y}}{\partial x} + \frac{\partial\tau_{xy}}{\partial y} + \frac{\partial\tau_{xz}}{\partial z} + F_{x} &= 0 \\\
\frac{\partial\sigma_{z}}{\partial x} + \frac{\partial\tau_{xy}}{\partial y} + \frac{\partial\tau_{xz}}{\partial z} + F_{x} &= 0
\end{split}$$

| ![](../../attachments/engr-727-001-advanced-mechanics-of-materials/stress_equilibrium_equations_3d_220120_134715_EST.png) |
|:--:|
| The stress state of a point is defined by the stress components acting on the sides of a differential volume that encloses the point which requires 9 forces in total. |

Often times, we use a matrix to represent these 9 forces: $\[\sigma_{ij}\] = \\[\tau_{ij}\] = \mathbf{\tau}_{ij} = \bmatrix{\sigma_{x}, \tau_{xy}, \tau_{xz} \\ \tau_{yx}, \sigma_{y}, \tau_{yz} \\ \tau_{zx}, \tau_{zy}, \sigma_{z}}\bmatrix$\]. However, we must remember that this matrix is *symmetric*.

| ![](../../attachments/engr-727-001-advanced-mechanics-of-materials/stress_equilibrium_equations_plane_220120_135152_EST.png) |
|:--:|
| The equations governing the transformation of the stress in 3D are obtained using a similar approach to that applied to the 2D case. Therefore, we can follow a similar manner to consider a tetrahedron isolated from a continuous medium subjected to a general state of stress. |

The orientation of plane *A**B**C* is defined in terms of angles between a unit normal, *n* to the plane and the *x*, *y*, and *z* directions. The directions cosines associated with these angles are:

$$\begin{split}
\cos(\alpha) &= \cos(\mathbf{n}, ) \\\
 &=
\end{split}$$

The equilibrium forces can be obtained after canceling the area, *A*. The areas of perpendicular planes *Q**A**B*, *Q**A**C*, and *Q**B**C* can be expressed in terms of *A*, the area of *A**B**C* and the direction cosines:

$$\begin{split}
A_{AQB} &= A_{x} = \mathbf{A} \cdot \mathbf{i} = A(l\mathbf{i} + m\mathbf{j} + n\mathbf{k}) \cdot \mathbf{i} = Al \\\
 &= Al \\\
\implies A_{QAC} &= Am \\\
\implies A_{QBC} &= An
\end{split}$$

Using the stress tensor, we can represent these equilibrium equations by:

$$\begin{split}
p_{x} &= \sigma_{x}l + \tau_{xy}m + \tau_{xz}n \\\
 &=
\end{split}$$

Using matrix notation:

$$\bmatrix{p_{x} \\ p_{y} \\ p_{z}} = {\mathbf{p}} = \bmatrix{\dots}$$

| ![](../../attachments/engr-727-001-advanced-mechanics-of-materials/stress_equilibrium_equations_normal_and_shear_220120_140206_EST.png) |
|:--:|
| foo |

The normal stress, *σ* is the projection of the vector, *p⃗* in the direction of **n**.

$$\begin{split}
\sigma &= \vec{p} \cdot \mathbf{n} = \vec{p} \cdot \vec{n} \\\
\sigma &= p_{x}l + p_{y}m + p_{z}n \\\
\sigma &= \sigma_{x}l^{2} + \sigma_{y}m^{2} + \sigma_{z} + n^{2} + 2(\tau_{xy}lm + \tau_{yz}mn + \tau_{xz}ln)
\end{split}$$

The magnitude of the shear stress, *τ* on plane *A**B**C* can be computed by geometry:

$$\begin{split}
\tau &= \sqrt{p^{2} - \sigma^{2}} \\\
\tau &= \sqrt{p_{x}^{2} + p_{y}^{2} + p_{z}^{2} - \sigma^{2}} \\\
\tau &= \sqrt{(\sigma_{x}l + \tau_{xy}m + \tau_{xz}n)^{2} + (\tau_{xy}l + \sigma_{y}m + \tau_{yz}n)^{2} + (\tau_{xz}l + \tau_{yz}m + \sigma_{z}n)^{2} - \sigma^{2}}
\end{split}$$

| ![](../../attachments/engr-727-001-advanced-mechanics-of-materials/stress_transformation_in_cartesian_220120_140922_EST.png) |
|:--:|
| The variance of the stress with respect to surface orientation. |

The transformation matrix is composed by the direction cosines: *l*<sub>1</sub> = cos (*x*′, *x*), *m*<sub>1</sub> = cos (*x*′, *y*), and so on. The complete set of direction cosines is:

<table><colgroup><col style="width: 25%" /><col style="width: 25%" /><col style="width: 25%" /><col style="width: 25%" /></colgroup><thead><tr class="header"><th style="text-align: left;"></th><th style="text-align: left;">x</th><th style="text-align: left;">y</th><th style="text-align: left;">z</th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><p>x'</p></td><td style="text-align: left;"><p><span class="math inline"><em>l</em><sub>1</sub></span></p></td><td style="text-align: left;"><p><span class="math inline"><em>m</em><sub>1</sub></span></p></td><td style="text-align: left;"><p><span class="math inline"><em>n</em><sub>1</sub></span></p></td></tr><tr class="even"><td style="text-align: left;"><p>y'</p></td><td style="text-align: left;"><p><span class="math inline"><em>l</em><sub>2</sub></span></p></td><td style="text-align: left;"><p><span class="math inline"><em>m</em><sub>2</sub></span></p></td><td style="text-align: left;"><p><span class="math inline"><em>n</em><sub>2</sub></span></p></td></tr><tr class="odd"><td style="text-align: left;"><p>z'</p></td><td style="text-align: left;"><p><span class="math inline"><em>l</em><sub>3</sub></span></p></td><td style="text-align: left;"><p><span class="math inline"><em>m</em><sub>3</sub></span></p></td><td style="text-align: left;"><p><span class="math inline"><em>n</em><sub>3</sub></span></p></td></tr></tbody></table>

In tensor notation: …​

| ![](../../attachments/engr-727-001-advanced-mechanics-of-materials/stress_transformation_in_cartesian_with_new_axes_220120_141529_EST.png) |
|:--:|
| Using these transformation equations for stresses acting on a new axis, <span class="math inline"><em>p⃗</em> = [<em>τ</em><sub><em>i</em><em>j</em></sub>]<em>n⃗</em></span> on an oblique plane in this new coordinate system becomes <span class="math inline">$\vec{}' = [\tau_{ij}']\vec{n'}$</span>. |

These vectors can be related by: *p⃗*′ = *T⃗* ⋅ *p⃗*. This can be combined with the transformed stress tensor into: \[*τ*<sub>*i**j*</sub>′\vec{n}' = \vec{T}\[\tau_{ij}\]\vec{n}\]. The relationship between *n⃗* and *n⃗*′ can be obtained by the inversion of *n⃗*′ = *T⃗**n⃗* which is *n⃗* = *T⃗*<sup>*T*</sup>*n⃗*′.

$$\begin{split}
\vec{T_{ij}}\vec{n}' &= \ \\\
 &=
\end{split}$$

The book performs the same derivations with different notation. Ultimately, these two expressions are equivalent, but the book’s notation is longer and more expressive.

**Principal Stress in 3D**

Planes with zero shear stress are mutually perpendicular and have a (min)maximum which are called **principal stresses**. Therefore, the stress vector on principal planes is given by *p⃗* = *σ*<sub>*p*</sub>*n⃗* where *σ*<sub>*p*</sub> is the magnitude of the stress vector, *p⃗* and *n̂* = *l**î* + *m**ĵ* + *n**k̂* is the unit normal to a principal plane. By projecting *p⃗* along each axis and substituting into $\vec{p} = \vec{\tau_{ij}}\hat{n}$, we arrive to the identity matrix:

…​

This becomes an *eigenvalue problem*. A non-trivial solution for the direction cosines requires that the characteristics stress determinant vanish; therefore, we set this equal to zero.

…​

This gives the characteristic equation: *σ*<sub>*p*</sub><sup>3</sup> − *I*<sub>1</sub>*σ*<sub>*p*</sub><sup>2</sup> + *I*<sub>2</sub>*σ*<sub>*p*</sub> − *I*<sub>3</sub> = 0; wherein, *I*<sub>1</sub>, *I*<sub>2</sub>, *I*<sub>3</sub> are the stress invariants.

$$\begin{split}
I_{1} &= \sigma_{x} + \sigma_{y} + \sigma_{z} \\\
I_{2} &= \sigma_{x}\sigma_{y} + \sigma_{x}\sigma_{z} + \sigma_{y}\sigma_{z} - \tau_{xy}^{2} - \tau_{yz}^{2} - \tau_{xz}^{2} \\\
I_{3} &= \dots
\end{split}$$

| ![](../../attachments/engr-727-001-advanced-mechanics-of-materials/mohrs_circle_for_triaxial_stress_220120_143146_EST.png) |
|:--:|
| In general, using <strong>Mohr’s Circle</strong> is not helpful for 3D analyses but can helpful to double check work. |

$$\begin{split}
\sigma_{x} &= x^{2} + 2y \\\
\sigma_{y} &= xy - y^{2}z \\\
\sigma_{z} &= x^{2} - z^{2} \\\
\tau_{xy} &= -xy^{2} + 1 \\\
\tau_{yz} &= 0 \\\
\tau_{xz} &= xz - 2x^{2}y
\end{split}$$

These forces are body, not surface forces; therefore, we are findings forces per volume.

1.  First, we find the partials.

$$\begin{split}
\frac{\sigma_{x}}{\partial x} &= 2x \\\
\frac{\sigma_{y}}{\partial y} &= z - 2yz \\\
\frac{\sigma_{z}}{\partial z} &= -2z \\\
\frac{\tau_{xy}}{\partial x} &= -y^{2} \\\
\frac{\tau_{xy}}{\partial y} &= -2xy \\\
\frac{\tau_{yz}}{\partial y} &= 0 \\\
\frac{\tau_{yz}}{\partial z} & = 0 \\\
\frac{\tau_{xz}}{\partial x} &= z - 4xy \\\
\frac{\tau_{xz}}{\partial z} &= x
\end{split}$$

1.  Next, with these derivations and summing the forces in the *x*-direction, we find: $F_{x} := 2(-10) + (-2)(-10)(30) + (-10) + F_{x} = 0 \\ \implies F_{x} = 570~\frac{N}{m^{3}}$ Similarly: $F_{y} = 14.5~\frac{kN}{m^{3}}$ and $F_{z} = 50.8~\frac{N}{m^{3}}$.

<!-- -->

1.  To find the solution vector, *n⃗*:

\begin{split} \vec{n} &= \frac{1}{\sqrt{i^{2} + j^{2} + k^{2}}}(\hat{i} + 2\hat{j} + \hat{k}) \\\ &= \frac{1}{\sqrt{6}}(\hat{i} + 2\hat{j} + \hat{k}) \end{split}

Find *p⃗* according to appropriate equations…​

1.  Principal Stresses We find the stress invariants to be *I*<sub>1</sub> = 160 *M**P**a*, *I*<sub>2</sub> = 5500 *M**P**a*<sup>2</sup>, and *I*<sub>3</sub> = 0. ∴, we plug these into the characteristic, cubic equations. $\sigma_{p}^{3} - 160\sigma_{p}^{2} + 5500\sigma_{p} - 0 = 0 \\ \implies \sigma_{p} = \{0, 110, 50\}~MPa$. We check that *σ*<sub>1</sub> ≥ *σ*<sub>2</sub> ≥ *σ*<sub>3</sub> which maps $\vec{\sigma_{p}}$ to {110, 50, 0} *M**P**a*.

<!-- -->

1.  From these, we can draw Mohr’s Circle.

| ![](../../attachments/engr-727-001-advanced-mechanics-of-materials/example_problem_set_1-2_problem_2_mohrs_circle_220125_140842_EST.png) |
|:--:|
| Therefore, <span class="math inline"><em>τ</em><sub><em>m</em><em>a</em><em>x</em></sub> = 55 <em>M</em><em>P</em><em>a</em></span>. |

1.  Invariants of **T**

\begin{split} I_{1} &= 18~MPa \\\ I_{2} &= 99~MPa^{2} \\\ I_{3} &= 160~MPa^{3} \end{split}

1.  Finding the stress components in the new coordinate system .We must build the table of cosines.

<table><colgroup><col style="width: 25%" /><col style="width: 25%" /><col style="width: 25%" /><col style="width: 25%" /></colgroup><thead><tr class="header"><th style="text-align: left;"></th><th style="text-align: left;">x</th><th style="text-align: left;">y</th><th style="text-align: left;">z</th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><p>x'</p></td><td style="text-align: left;"><p><span class="math inline">$\frac{\sqrt{2}}{2}$</span></p></td><td style="text-align: left;"><p><span class="math inline">$\frac{\sqrt{2}}{2}$</span></p></td><td style="text-align: left;"><p>0</p></td></tr><tr class="even"><td style="text-align: left;"><p>y'</p></td><td style="text-align: left;"><p><span class="math inline">$\frac{\sqrt{2}}{2}$</span></p></td><td style="text-align: left;"><p><span class="math inline">$-\frac{\sqrt{2}}{2}$</span></p></td><td style="text-align: left;"><p>0</p></td></tr><tr class="odd"><td style="text-align: left;"><p>z'</p></td><td style="text-align: left;"><p>0</p></td><td style="text-align: left;"><p>0</p></td><td style="text-align: left;"><p>1</p></td></tr></tbody></table>

Therefore, the stress tensor in the new coordinate system can be found by: \[*τ*<sub>*i**j*</sub>′\] = \[*T*\]\[*τ*<sub>*i**j*</sub>\]\[*T*\]<sup>*T*</sup>. This yields, $\[\tau_{ij}'\] = \begin{bmatrix}6 & 1 & \sqrt{2} \\ 1 & 4 & -\sqrt{2} \\ \sqrt{2} & -\sqrt{2} & 8\end{bmatrix}~MPa$.