### Introduction
Stresses occur at varying scales within a material. Macro-stresses include component design and assemblage. Micro-stresses are found within the material and include those from defects: dislocations, alloying elements. etcetera. Stresses at smallest scale act cumulatively to produce the response to the largest scale. This all relates to the **#CPSPP** relationship.

### Elastic
- Reverse deformation, that instantaneously recovers to its original dimensions after force is removed.
- Analogous to a spring, the relationship was conveniently described by Robert Hooke: $F = k\delta x$

#### Stress
- Stress is the result of applied force and response of material to balance external force.
    - Area resisting force is perpendicular to applied force line of action.
    - Material response is determined by atomic bonds and orientation relative to crystal lattice.
    - !!! note
            Polycrystalline materials assumed #anisotropic.
    - Component response dictated by design and material properties.
    - Tensile stress often positive in sign and compression is negative, by convention.

#### Strain
- Physical result of stress.
- Linear proportional to stress in Hookean material up to its elastic limit/yield stress.
- !!! note
        [[proportional-limit]] is that when the stress-strain deviates from linear and yield stress is at the 0.02% strain offset.
- Metals often Hookean in nature and assumed until otherwise stated.
- True strain: $\begin{equation}\epsilon = \frac{dl}{l}, \epsilon = \int_{l_{0}}^{l_{1}}\frac{dl}{l} = ln(\frac{l_{1}}{l_{0}})\label{
true_strain}\end{equation}$
- Engineering strain: $\begin{equation}\epsilon = \frac{\delta l}{l}\label{eq:engineering_strain}\end{equation}$

#### Engineering vs True Stress
- Comes from initial conditions and easily measured.
- !!! note
        Area does not change, so the initial area determines the stress throughout the entire deformation.
- True stress and strain are more accurate and use an instantaneous cross-section.
- In the elastic region for metals, deformation is typically small and engineering and true stress-strain values are comparable.
- $\sigma_{T} = \sigma(1 + \epsilon)$
- $\epsilon_{T} = ln(1 + \epsilon)$

| ![](../../attachments/engr-839-001-mechanical-metallurgy/stress_strain_curve_210907_144454_EST.png) |
|:--:|
| $\label{fig:stress_strain_curve}$ |

#### Notation!
Notation is not always the same.

$$\begin{equation}
\begin{bmatrix}
\sigma_{xx}, \tau_{xy}, \tau_{xz} \\
\tau_{yx}, \sigma_{yy}, \tau_{yz} \\
\tau_{zx}, \tau_{zy}, \sigma_{zz}
\end{bmatrix}\begin{bmatrix}
(x) \\
(y) \\
(z)
\end{bmatrix}\equiv\begin{bmatrix}
\sigma_{11}, \tau_{12}, \tau_{13} \\
\tau_{21}, \sigma_{22}, \tau_{23} \\
\tau_{31}, \tau_{32}, \sigma_{33}
\end{bmatrix}\begin{bmatrix}
(1) \\
(2) \\
(3)
\end{bmatrix}
\label{eq:tensor_notation}
\end{equation}$$


| ![](../../attachments/engr-839-001-mechanical-metallurgy/tensor_notation_210907_145720_EST.png) |
|:--:|
| $\label{fig:tensor_notation}$ |

#### Strain Energy
- Work done during deformation is converted to heat and internal energy.
- $W = Fd$, but $F$ is not constant!
- Elastic deformation does not typically produce much heat, so most is stored internally.
- $dU = dQ - dQ$
- $U = W$ (without heat)
- $W = \frac{1}{2}\sigma_{ij}\epsilon_{ij} = \frac{1}{2}E\epsilon_{ij}^{2} = \frac{1}{2E}\sigma_{ij}^{2}$

#### Shear/Torsion
- Shear and torsional stress are handled similarly, but vary by configuration.

| ![](../../attachments/engr-839-001-mechanical-metallurgy/shear_stress_example_210907_150449_EST.png) |
|:--:|
| For a cylindrical punch, the average diameter of the punch and hole can be taken, and the area will be the circumference times the thickness of the material. $\label{fig:shear_stress_example}$ |

| ![](../../attachments/engr-839-001-mechanical-metallurgy/torsional_stress_example_210907_150530_EST.png) |
|:--:|
| For torsion of a rod, the stress and strain vary radially and axially. $\label{fig:torsional_stress_example}$ |

- $\tau = \frac{F}{A}$
- $\gamma = \frac{dl}{l} = tan\theta \cong \theta$
- $G = \frac{\tau}{\gamma}$

!!! question Why does $\gamma \cong \theta$?
    Small angle assumptions in radians mean that $sin\theta = \theta$.

#### Poisson's Ratio
$$\begin{equation}
\nu = -\frac{\epsilon_{11}}{\epsilon_{33}} = -\frac{\epsilon_{22}}{\epsilon_{33}}
\label{eq:poisson_ratio}
\end{equation}$$

| ![](../../attachments/engr-839-001-mechanical-metallurgy/poisson_ratio_210907_151239_EST.png) |
|:--:|
| $\label{fig:poisson_ratio}$ |

- Describes the consequent strains orthogonal to an applied stress.
- Most metals are 0.3.
- For constant volume without lateral contraction, the ratio is 0.5 (plastic only).

#### Summary
- Elasticity affects everything, because it is initial response to stress.
- Material behavior in elastic region dictates behavior in application.
- Components rarely useful in plastic region, so they will spend their lifetime in the elastic range.
- Although elastic properties are commonly discussed at a continuum scale, we will find it important to atomic scale phenomena.



---


*Lecture: September 03, 2021*

### Elasticity: Polycrystalline Materials and Bulk Metals
#### Introduction
- Stress may be applied in any arrangement, and we can determine the overall conditions of strain.
- This is often reduced to two dimensions, but it does not have to be (it is just simpler).
- We can determine the state of stress as a point in any orientation (not just aligned with the applied stress) by using transformation techniques.
- Certain orientations will result in only normal or shear stresses, which can be important for determining the resulting performance.

#### Stress Tensor Revisited

| ![](../../attachments/engr-839-001-mechanical-metallurgy/cauchy_stress_tensor_210907_152153_EST.png) |
|:--:|
| $\label{fig:cauchy_stress_tensor}$ |

- Cuachy stress tensor describes the complete state of stress in three dimensions.
- Valid for small deformations (Eq. \eqref{eq:tensor_notation}).

#### Hooke's Law Revisited
- Linear elastic response in homogeneous metals and alloys which allows us to relate stress and strain in three dimensions through the #poisson-ratio, $\nu$ \eqref{eq:poisson_ratio}.

$$\begin{split}
\epsilon_{11} &= \frac{1}{E}[\sigma_{11} - \nu(\sigma_{22} + \sigma_{33})] \\
\epsilon_{22} &= \frac{1}{E}[\sigma_{22} - \nu(\sigma_{11} + \sigma_{33})] \\
\epsilon_{33} &= \frac{1}{E}[\sigma_{33} - \nu(\sigma_{11} + \sigma_{22})] \\
\gamma_{12} &= \frac{\sigma_{12}}{G} \\
\gamma_{13} &= \frac{\sigma_{13}}{G} \\
\gamma_{23} &= \frac{\sigma_{23}}{G}
\end{split}$$

>**Example 1:** For the following stress tensor, what are the resulting normal strains if $E = 10e3 kip$ and $\nu = 0.3$?
$\sigma = \begin{bmatrix}5, 3, 2 \\ 3, -1, 0 \\ 2, 0, 4\end{bmatrix}kip$
$$\epsilon_{normal} = \begin{bmatrix}\frac{1}{10e3 ksi}[5 ksi - 0.3(-1 + 4)]ksi \\ \frac{1}{10e3 ksi}[1 ksi - 0.3(5 + 4)]ksi \\ \frac{1}{10e3 ksi}[4 ksi - 0.3(5 + (-1))]ksi\end{bmatrix}ksi = \begin{bmatrix}4.1e-4 \\ -3.7e-6 \\ 2.8e-6\end{bmatrix}$$

#### Simplifications
- To avoid complex tridimensional description of stress and strain, especially during plastic deformation, simplifications are possible.

[[plane-stress]]
: Strain and strain go to zero at free surface (normal and shear).

[[plane-strain]]
: One dimension is considered infinite.

- Conditions of [[pure-shear]] can also be considered, such that no normal forces are present.

$$\begin{bmatrix}
\sigma_{xx}, \tau_{xy} \\
\tau_{yx}, \sigma_{yy}
\end{bmatrix}\begin{bmatrix}
(x) \\
(y)
\end{bmatrix}$$

$$\begin{bmatrix}
\epsilon_{xx}, \gamma_{xy} \\
\gamma_{yx}, \epsilon_{yy}
\end{bmatrix}\begin{bmatrix}
(x) \\
(y)
\end{bmatrix}$$

#### #Mohrs-Circle Revisited
- A graphical way to represent stress transformation to alternative orientations.
- These are set of equations that describe stress transformation, but a graphical solution is often useful.

| ![](../../attachments/engr-839-001-mechanical-metallurgy/mohrs_circle_illustration_210907_153956_EST.png) |
|:--:|
| $\label{fig:mohrs_circle_illustration}$ |

- Principal stress: maximum/minimum normal stresses (no shear)

| ![](../../attachments/engr-839-001-mechanical-metallurgy/mohrs_circle_transformation_equation_illustration_210907_154859_EST.png) |
|:--:|
| $\label{fig:mohrs_circle_transformation_equation_illustration}$ |

- $R = \sqrt{(\frac{\sigma_{11} + \sigma_{22}}{2})^{2} + \tau_{12}^{2}}$
- $\sigma_{11}' = \frac{\sigma_{11} + \sigma_{22}}{2} + \frac{\sigma_{11} - \sigma_{22}}{2}cos(2\theta) + \sigma_{12}sin(2\theta)$
- $\sigma_{12}' = -\frac{\sigma_{11} - \sigma_{22}}{2}sin(2\theta) + \sigma_{12}cos(2\theta)$

!!! example What is the stress state if rotated $30\degree$ CCW?
    | ![](../../attachments/engr-839-001-mechanical-metallurgy/mohrs_circle_example_problem_1_210907_155042_EST.png) |
    |:--:|
    | $\label{fig:mohrs_circle_example_problem_1}$ |
    *Given: $\sigma_{11} = -8 ksi, \sigma_{22} = 12 ksi, \sigma_{12} = -6 ksi$*
    Center point, $C = \sigma_{avg} = \frac{\sigma_{11} + \sigma_{22}}{2} = \frac{-8 + 12}{2} = 2 ksi$
    | ![](../../attachments/engr-839-001-mechanical-metallurgy/mohrs_circle_example_1_problem_step_t_find_r_210907_155511_EST.png) |
    | $\label{fig:mohrs_circle_example_1_problem_step_t_find_r}$ |
    $R = \sqrt{10^{2} + 6^{2}} = 11.66$
    | ![](../../attachments/engr-839-001-mechanical-metallurgy/mohrs_cricle_example_1_problem_step_to_find_angle_210907_155632_EST.png) |
    | $\label{fig:mohrs_cricle_example_1_problem_step_to_find_angle}$ |

    Use trig to find $\phi$ and $\psi$: $\phi = tan^{-1}(\frac{6}{10}) = 30.96\degree, \psi = 60 - \phi = 29.04\degree$
    $\sigma_{11}' = 2 - 11.66cos(29.04) = -8.2 ksi$
    $\sigma_{12}' = -11.66sin(29.04) = 5.66 ksi$

    | ![](../../attachments/engr-839-001-mechanical-metallurgy/mohrs_circle_example_1_complete_210907_160049_EST.png) |
    |:--:|
    | Slight drop increase of normal stress and slight decrease of shear stress. $\label{fig:mohrs_circle_example_1_complete}$ |
    | ![](../../attachments/engr-839-001-mechanical-metallurgy/mohrs_circle_example_1_complete_clean_210908_192355_EST.png) |
    | Basic steps to find all stresses and strains at orientations relative to what you start with. $\label{fig:mohrs_circle_example_1_clean}$ |


---


*Lecture: September 06, 2021*

### Pure Shear
There exists a condition which has only shear stresses and no normal stress. This condition is called *[[pure-shear]]*, which means that $\sigma_{11} = -\sigma_{22}$. This implies that [[Mohrs-Circle]] is centered at the origin, because $\sigma_{avg} = 0$. Graphically, the maximum shear stress possible in this condition is the radius of [[Mohrs-Circle]] and at $90\degree$ from the horizontal. However, recall that angles in [[Mohrs-Circle]] are twice real angles: e.g. if $\theta_{Mohr} = 2*\theta_{real}$ and $\theta_{Mohr} = 90\degree$, then $\theta_{real} = 45\degree$.

| ![](../../attachments/engr-839-001-mechanical-metallurgy/pure_shear_depicted_210908_193214_EST.png) |
|:--:|
| If a component experiences compression in one axis and tension in a perpendicular axis, then elements within the component experience [[pure-shear]]. $\label{fig:pure_shear_depicted}$ |

Using knowledge of this condition, we can find stress and strain information with the following relations:

$$\begin{split}
\epsilon_{11} &= \frac{1}{E}(\sigma_{1} - \nu\sigma_{2}) = \frac{\sigma_{1}}{E}(1 + \nu) \\
\tau &= -\sigma_{1} (on~circle,~with~sign~convention) \\
\tau &= G\gamma \\
\epsilon_{11} &= -\frac{G\gamma}{E}(1 + \nu) \\
2\epsilon_{11} &= -\gamma \\
G &= \frac{E}{2}(1 + \nu)
\end{split}$$

"(on circle, with sign convention)" holds true because the radius, $R$ of [[Mohrs-Circle]] is $\sigma_{1} = - \sigma_{1}$. Some of these relationships are not limited to [[pure-shear]], because $E, G \text{and} \nu$ are material properties.

Expressing three-dimensional stress is important, but can be achieved with tensor notation. Analysis of stress states can be reduced from three to two dimensions if assuming [[plane-stress]] (zero stress in third axis) or [[plane-strain]] (zero strain in third axis). This simplified analysis can be transformed to desired stress states by equations or [[Mohrs-Circle]].
Recall that [[Mohrs-Circle]] is a graphical representation of all possible stress states, but it must be drawn accurately that trigonometric functions might be used effectively.

### Elasticity: Atomic Bonds
#### Introduction
What preceded was continuum elasticity. What follows is observing the previously explored behaviors at the atomistic level. These behaviors determine the way force, stress, and strain occur. Characterizing these behaviors informs the results of bond strength in materials: we focus on metals. There exist competing behaviors of attraction and repulsion.

Continuum looks and homogeneous units wherein stress states are described without knowing the exact material makeup. Here, we can continue to ignore anisotropic conditions, but must observe the source of elasticity: atomic bonds. Strength of bonds determined by electronic characteristics, but can be influenced by external conditions: heat, magnetic fields, etcetera.

| ![](../../attachments/engr-839-001-mechanical-metallurgy/electronic_bonds_simplified_210908_195046_EST.png) |
|:--:|
| We assume only planar, uniaxial attractions. $\label{fig:electronic_bonds_simplified}$ |

#### Atomic Bonding
Electronic bonds govern behavior of all material properties. All mechanical behavior first exhibits elastic behavior. These effects can be observed with a simple spring model between two atoms.

| ![](../../attachments/engr-839-001-mechanical-metallurgy/simple_spring_model_210908_195302_EST.png) |
|:--:|
| Simplified spring model to visually show attractive and repulsive forces of electronic bonds between atoms. $\label{fig:simple_spring_model}$ |

#### Bond Interaction and Force
Two atoms will have an equilibrium separation, $r_{0}$. We assume this until some external influence is applied. The minimum bonding energy also occurs here. Repulsion is caused by the *[[Pauli-Exclusion-Principle]]* and attraction is *[[Coulombic-forces]]* in nature.

$$\begin{equation}
    U_{i} = -\frac{A}{r^{m}} + \frac{B}{R^{n}}
    \label{eq:bonding_energy}
\begin{equation}$$

| ![](../../attachments/engr-839-001-mechanical-metallurgy/interaction_energy_and_force_210908_195751_EST.png) |
|:--:|
| Electronic bonding occurs according to these two curves between any two atoms. $\label{fig:interaction_energy_and_force}$ |

!!! example
    Potential energy of $Na^{+}Cl^{-}$, an ionic pair, at distance $r$ where $q_{0} = 1.6e-19~[C]$, $\epsilon_{0} = 8.85e-12~[\frac{C}{N-m^{2}}]$, and $U_{i} = 1.12~[eV]$. If $r_{0} = 0.276~[nm]$, then find: **a)** the value of B; and **b)** the total, attractive, and repulsive forces at $r = 0.25 [nm]$.
    $$\begin{split}
    U_{i} &= -\frac{A}{r^{m}} + \frac{B}{r^{n}} \\
    U &= U_{i} - \frac{q^{2}}{4\pi\epsilon_{0}r} + \frac{B}{r^{9}}
    \end{split}$$
    Because $\frac{dU}{dr} = 0$ at $r_{0}$,
    $$\begin{split}
    \frac{dU}{dr} &= 0 = \frac{q^{2}}{4\pi\epsilon_{0}r^{2}} - \frac{9B}{r_{0}^{10}} \\
    \frac{q^{2}}{4\pi\epsilon_{0}r^{2}} &= \frac{9B}{r_{0}^{10}} \\
    \implies B &= \frac{r_{0}^{8}q^{2}}{36\pi\epsilon_{0}}
    \end{split} \\
    \begin{split}
    B &= 8.61e-106 [N-m^{10}]
    \end{split}$$
    $B$, then, is simply plugged into the following equations to find electronic bond forces at not the equilibrium distance, $r = 0.25 [nm]$.
    $$\begin{split}
    F &= \frac{dU}{dr} = F_{A} - F_{R} \\
    F &= \frac{q^{2}}{4\pi\epsilon_{0}r^{2}} - \frac{9B}{r_{0}^{10}}
    \end{split} \\
    \begin{split}
    F_{A} &= \frac{q^{2}}{4\pi\epsilon_{0}r^{2}} = 3.68e-4 [N] \\
    F_{B} &= \frac{9B}{r_{0}^{10}} = -8.13e-9 [N] \\
    \implies F &= 4.44e-9 [N]
    \end{split}$$

#### Stress and Strain in Bonds
Force is proportional to atomic displacement and change in energy. Stress requires number of atoms involved in some area by estimating atomic spacing at equilibrium, $r_{0}^{2}$. Strain, then, is the change in spacing divided by the equilibrium spacing. [Young's Modulus](engr-743-damage-and-fracture/youngs-modulus.md) is a material property of stress over strain. These can be summarized by the following relations:

$$\begin{split}
F &= \frac{dU_{i}}{dr} \\
d\sigma &= NdF \\
d\sigma &= \frac{dF}{r_{0}^{2}} \\
d\epsilon &= \frac{dr}{r_{0}} \\
E &= \frac{Am(n-m)}{r_{0}^{m + 3}} \\
A &= \frac{q^{2}}{4\pi\epsilon_{0}} \\
E &= \frac{kq^{2}}{r_{0}^{4}}
\end{split}$$

| ![](../../attachments/engr-839-001-mechanical-metallurgy/outcomes_of_bonding_210908_203140_EST.png) |
|:--:|
| Stronger bonding can effect melting point, stiffness, etcetera. Understanding these effects informs how higher length scales behave under some condition. $\label{fig:outcomes_of_bonding}$ |

#### Summary
Bulk properties come from atomic bonds. Treatment of elasticity at atomic scale determines balances of attractive and repulsive forces; therefore, external forces cause a shift from the equilibrium state. Bond properties can be adjusted to preference with some processing technique: e.g. alloying.