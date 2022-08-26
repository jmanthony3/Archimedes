# strain-deformation-and-mechanical-properties

**Introduction**

Most bodies undergo some amount of elastic deformation under some external loading.

Strain  
A geometric quantity that measures the deformation of a body.

This is one of the most important topics in solid mechanics because strain quantifies the changes in geometry during deformation from applied stresses.

Normal Strain, *ϵ*  
In a direction *n̂*, this is defined as the change in length per unit length of the fibers oriented in the *n*-direction.

$$\begin{equation}
\epsilon_{\text{avg}} = \frac{\Delta s' - \Delta s}{\Delta s}
\end{equation}$$

In solid mechanics, if we consider the deformation of a prismatic bar, then we represent average strain as $\epsilon_{\text{avg}} = \frac{L - L_{0}}{L_{0}} = \frac{\delta}{L_{0}}$.

**Pure Shear**

Shear strain is allowed by the shear forces balancing each other out on each face of differential elements.

Shear Strain, *γ*  
The change in angles between two originally perpendicular line segments.

**Q:** Why are there two different notations for normal strain? — dk

**A:** If you do not have enough information to perform the integral, then you assume the average strain.

**Tension Testing: Mechanical Properties of Materials**

This is most important test for us. Slowly applying axial loads unto a cylindrical bar, the specimen, the strain can be measure for some strain-rate. Typically, the yield point of a specimen is determined the 0.2%-offset Method.

**Q:** How do we know the difference between brittle and ductile materials? — Dr. Lugo

**A:** This distinction is subjective, but in general, ductile materials undergo much more plastic strain (absorb more energy) before failure than "brittle" materials. Typically, this defining limit is held as 5% strain.

If we unload the specimen before the applied stress exceeds the yield point, then the material will elastically return to its original length. This holds true to viscoelastic materials; however, "visco-" connotes some time-dependence, but, ultimately, the specimen does return to its original geometry.

**Linear Elasticity and Hooke’s Law**

Most engineering materials have an initially, linear elastic region on the stress-strain diagram. This linear relationship between stress and strain for a material in simple tension can be expressed by:

*σ* = *E**ϵ*

This constitutive relationship is to us what Newton’s Second Law of Motion is to physics.

**True Stress-Strain Curve**

This differs from engineering strain, which considers that the cross-sectional area remains constant, by considering that the cross-sectional area changes with changes in overall length.

$$\begin{equation}
s = \frac{F}{A_{0}}
\end{equation}$$

$$\begin{equation}
\sigma = \frac{F}{A}
\end{equation}$$

In Advanced Mechanics of Materials, we consider only the elastic region; therefore, *s* and *σ* are considered equivalent which is true until sufficient plastic deformation. *s* and *σ* are related by:

$$\begin{split}
\sigma &= s(1 + e) \\\
\epsilon &= \ln(1 + e)
\end{split}$$

Strain-Hardening  
True stress increases continuously until sufficient plastic strain allows for the material to begin necking.

<!-- -->

Axial Deformation  
When axial loads are applied to a member.

We must make key assumptions:

-   asdf

By these, we get an equilibrium equation: $\delta = \frac{PL}{AE}$. If the member has regions of different cross-sectional areas and loads applied not only at the ends of the body, then the Law of Superposition can be applied to find total elongation: $\delta = \sum\frac{PL}{AE}$.

| ![](../../attachments/engr-727-001-advanced-mechanics-of-materials/statically_indeterminate_220127_140135_EST.png) |
|:--:|
| Considering these two structures, we can solve the left-hand figure by summation of the forces to find the overall deformation. However, the right-hand figure is <em>statically indeterminate</em>. |

Reactions for the left-hand can be calculated from equilibrium equations, but left-hand cannot be solved this way. We must also include compatibility equations.

-   Equilibrium equations: ∑*F*<sub>*x*</sub> = *R*<sub>*A*</sub> + *R*<sub>*c*</sub>

-   Constitutive equations: $\delta = \frac{PL}{AE}$

-   Compatibility equations: *δ*<sub>*T*</sub> = 0

| ![](../../attachments/engr-727-001-advanced-mechanics-of-materials/statically_indeterminate_with_superposition_220127_140549_EST.png) |
|:--:|
| We can also use Law of Superposition. We temporarily remove one of the fixed points and consider each region of the body separately with constitutive equations that are coupled together with equilibrium and compatibility equations. |

**Thermal Effects on Axial Deformation**

Considering a homogeneous bar $\bar{AB}$ of uniform cross-section on a smooth, horizontal surface, there is a change in length with change in temperature.

$$\begin{equation}
\begin{split}
\delta &=  \\\
 &=
\end{split}
\end{equation}$$

| ![](../../attachments/engr-727-001-advanced-mechanics-of-materials/problem_set_2-1_problem_1_220127_141220_EST.png) |
|:--:|
| The rigid beam is supported by a pin at <span class="math inline"><em>A</em></span> and wires <span class="math inline">$\bar{BD}$</span> and <span class="math inline">$\bar{CE}$</span>. If the load P on the beam causes the end <span class="math inline"><em>C</em></span> to be displaced <span class="math inline">10 <em>m</em><em>m</em></span> downward, determine the normal strain developed in wires <span class="math inline">$\bar{CE}$</span> and <span class="math inline">$\bar{BD}$</span>. |

We are given *δ*<sub>*c*</sub> = 10 *m**m*, and we want to find *ϵ*<sub>*B**D*</sub> and *ϵ*<sub>*C**E*</sub>. Using a Law of Similar Triangles:

$$\begin{split}
\frac{\delta_{B}}{3} &= \frac{\delta_{c}}{7} \\\
\delta_{B} &= \frac{3}{7}(10~mm) = ${round(3\*10/7, 6)}~mm
\end{split}$$

The length of each cable is *L* = 4 *m*. To find $\epsilon_{BD} = \frac{\delta_{B}}{L} = ${round(30/7/4000, 6)}~\frac{mm}{mm}$. To find $\epsilon_{CE} = \frac{\delta_{C}}{L} = ${engr(10/4000)}~\frac{mm}{mm}$.

| ![](../../attachments/engr-727-001-advanced-mechanics-of-materials/problem_set_2-1_problem_2_220127_142358_EST.png) |
|:--:|
| The 2014-T6 aluminum rod of <span class="math inline">⌀20 <em>m</em><em>m</em></span> is subjected to the uniform distributed axial load. Determine the displacement of end <span class="math inline"><em>A</em></span>. |

We are given *d* = 20 *m**m* and that the rod is 2014-T6 aluminum.

$$\begin{split}
\delta &= \int\frac{P(x)dx}{A(x)E} \\\
 &= \frac{1}{AE}\int_{0}^{0.9}30xdx \\\
 &= \frac{30}{AE}\frac{x^{2}}{2}\biggr\]_{0}^{0.9} \\\
 &= ${round((30e3\*0.9\*\*2)/(2\*np.pi/4\*0.02\*\*2\*70e9), 6)}~m
\end{split}$$

| ![](../../attachments/engr-727-001-advanced-mechanics-of-materials/problem_set_2-1-3_problem_statement_220201_131900_EST.png) |
|:--:|
| The piece of rubber is originally rectangular. Determine the average shear strain, <span class="math inline"><em>γ</em><sub><em>x</em><em>y</em></sub></span> at <span class="math inline"><em>A</em></span> if the corners <span class="math inline"><em>B</em></span> and <span class="math inline"><em>D</em></span> are subjected to the displacements that cause the rubber to distort as shown by the dashed lines. |

We are given the displacements and we want to find *γ*<sub>*x**y*</sub>; therefore, we must find *θ*<sub>1</sub> = ∠*A**B* and *θ*<sub>2</sub> = ∠*A**D*.

$$\begin{split}
\theta_{1} &= \tan^{-1}\Bigl(\frac{u_{B}}{L_{AB}}\Bigr) = \tan^{-1}\Bigl(\frac{2~mm}{300~mm}\Bigr) = ${engr(np.arctan(2/300))}~rad \\\
\theta_{2} &= \tan^{-1}\Bigl(\frac{u_{D}}{L_{AD}}\Bigr) = \tan^{-1}\Bigl(\frac{3~mm}{400~mm}\Bigr) = ${engr(np.arctan(3/400))}~rad
\end{split}$$

Thus the shear strain at *A* is the sum of these two angles: $\gamma_{xy} = ${engr(np.arctan(2/300) + np.arctan(3/400))}~rad$

| ![](../../attachments/engr-727-001-advanced-mechanics-of-materials/problem_set_2-1-5_problem_statement_220201_132847_EST.png) |
|:--:|
| The timber member has a cross-sectional area of <span class="math inline">1750 <em>m</em><em>m</em><sup>2</sup></span> and its modulus of elasticity, <span class="math inline"><em>Y</em> = 12 <em>G</em><em>P</em><em>a</em></span>. Compute the change in the total length of the member after the loads shown are applied. |

We are given the area and elastic modulus, and we want to find the total deformation, *δ*<sub>*T*</sub>. We must apply the equilibrium equations to find the reaction force at point *A*, *R*<sub>*A*</sub>:

$$\begin{split}
\rightarrow\sum F_{x} = 0 := -R_{A} + 40 - 35 + 20 &= 0 \\\
\implies R_{A} &= 25~kN \\\
\end{split}$$

| ![](../../attachments/engr-727-001-advanced-mechanics-of-materials/force_diagram_220201_133711_EST.png) |
|:--:|
| Force diagram of beam. |

By examining shear-moment diagrams, we can find the total deformation, $\delta_{T} = \sum_{i} \frac{P_{i}L_{i}}{A_{i}E_{i}}$:

| ![](../../attachments/engr-727-001-advanced-mechanics-of-materials/problem_set_2-1-6_problem_statement_220201_133825_EST.png) |
|:--:|
| The composite bar consists of a <span class="math inline">⌀20 <em>m</em><em>m</em></span> A-36 steel segment, <span class="math inline"><em>A</em><em>B</em></span> and <span class="math inline">⌀50 <em>m</em><em>m</em></span> red brass C83400 end segments <span class="math inline"><em>D</em><em>A</em></span> and <span class="math inline"><em>C</em><em>B</em></span>. Determine the average normal stress in each segment due to the applied load. |

We are given the diameter and length of each segment of the bar. The elastic modulus of steel is commonly 200 *G**P**a* and for brass is 101 *G**P**a*. We need to find *σ*<sub>*s**t*</sub> and *σ*<sub>*b**r*</sub>, but this problem is *statically indeterminate*. We can use the **Law of Superposition** with compatibility and constitutive equations to find the reaction forces at points *C* and *D*.

$$\begin{split}
\delta_{P_{1}} &= \frac{P_{1}L_{AD}}{A_{AD}E_{br}} + \frac{P_{1}L_{AB}}{A_{AB}E_{st}} \\\
 &= \frac{(200~kN)(250~mm)}{(\frac{1}{4}\pi(50~mm)^{2})(101~GPa)} + \frac{(200~kN)(500~mm)}{(\frac{1}{4}\pi(20~mm)^{2})(200~GPa)} \\\
\implies \delta_{P_{1}} &= ${engr((200e3)\*(250e-3)/(0.25\*np.pi\*((50e-3)\*\*2)\*(101e9)) + (200e3)\*(500e-3)/(0.25\*np.pi\*((25e-3)\*\*2)\*200e9))}~m \\\
\delta_{P_{2}} &= \frac{P_{2}L_{AD}}{A_{AD}E_{br}} \\\
 &= ${engr((-150e3)\*(250e-3)/(0.25\*np.pi\*((50e-3)\*\*2)\*(101e9)))} \\\
 &= 0.00018909~m \\\
\delta_{R_{C}} &= 2\Bigl(\frac{R_{C}L_{AD}}{A_{AD}E_{br}}\Bigr) + \frac{R_{C}L_{AB}}{A_{AB}E_{st}} \\\
 &= 0.00000001048 R_{C}
\end{split}$$

By the compatibility equations, *δ*<sub>*T*</sub> = 0, because both ends of the bar are fixed which is *statically indeterminate*.

$$\begin{split}
\therefore \delta_{T} = 0 := \delta_{P_{1}} + \delta_{P_{2}} + \delta_{R_{C}} &= 0 \\\
0.0018436 - 0.00018909 + 0.00000001048 R_{c} &= 0 \\\
\implies R_{C} &= 157.88~kN
\end{split}$$

By sum of the forces, we can find *R*<sub>*D*</sub> = 107.88 *k**N*. Therefore, {*σ*<sub>*A**D*</sub>, *σ*<sub>*A**B*</sub>, *σ*<sub>*B**C*</sub>} = {54.96, 134.025, 80.4} *M**P**a*.

| ![](../../attachments/engr-727-001-advanced-mechanics-of-materials/problem_set_2-1-7_problem_statement_220201_142343_EST.png) |
|:--:|
| The assembly consists of two red brass C83400 copper rods <span class="math inline"><em>A</em><em>B</em></span> and <span class="math inline"><em>C</em><em>D</em></span> of diameter, <span class="math inline">⌀30 <em>m</em><em>m</em></span>, a stainless 304 steel alloy rod <span class="math inline"><em>E</em><em>F</em></span> of diameter, <span class="math inline">⌀40 <em>m</em><em>m</em></span>, and a rigid gap <span class="math inline"><em>G</em></span>. If the supports at <span class="math inline"><em>A</em></span>, <span class="math inline"><em>C</em></span>, and <span class="math inline"><em>F</em></span> are rigid, then determine the average, normal stress developed in the rods. |

| ![](../../attachments/engr-727-001-advanced-mechanics-of-materials/problem_set_2-1-8_problem_statement_220201_142621_EST.png) |
|:--:|
| Three bars each made of different…​ |

The temperature differences affects each bar segment differently: i.e. each bar will deform a certain length. However, this problem is *statically indeterminate*, so we can use the **Law of Superposition**. Recall: *δ* = *α**Δ**T**L*.

$$\begin{split}
\delta_{T} &= \sum_{i}\delta_{T_{i}} \\\
 &= \alpha_{st}\Delta TL_{st} + \alpha_{br}\Delta TL{br} \\\
 &\qquad + \alpha_{cu}\Delta TL_{cu}
\end{split}$$

By the compatibility equations: *δ*<sub>*T*</sub> = *δ*<sub>*F**C*</sub>.

$$\begin{split}
F_{C} &= 4.2~kN \\\
\sigma_{st} &= 21.01~MPa \\\
\sigma_{br} &= 9.3~MPa \\\
\sigma_{cu} &= 8.16~MPa
\end{split}$$