---
title: Continuum Mechanics
subject: ENGR 725-001
date: 220822-221206
time: 14:10-15:00 (MWF)
place: DH 3274
speaker: Dr. Heechen Cho
---
# ENGR 725-001: Continuum Mechanics
!!! abstract Course Description
    An introduction to the general theory of continuous media and its application to the theories of elasticity and fluid mechanics.

Table of Contents
- [ENGR 725-001: Continuum Mechanics](#engr-725-001-continuum-mechanics)
  - [Preliminaries](#preliminaries)
  - [Continuum Mechanics](#continuum-mechanics)
  - [Notation](#notation)
  - [Scalar Product](#scalar-product)
  - [Tensor Symmetry](#tensor-symmetry)
  - [Eigenvalues and Eigenvectors of a Symmetric 2nd Rank Tensor](#eigenvalues-and-eigenvectors-of-a-symmetric-2nd-rank-tensor)
  - [Tensor Calculus](#tensor-calculus)
    - [Directional Derivative, $\frac{\partial \phi}{\partial n}$](#directional-derivative-fracpartial-phipartial-n)
    - [Divergence Theorem of Gauss](#divergence-theorem-of-gauss)
  - [Mechanics](#mechanics)
    - [Analysis of Stress](#analysis-of-stress)
    - [Define the "Traction Vector" ("Stress Vector")](#define-the-traction-vector-stress-vector)


---


*Lecture (1): August 22, 2022*

***Introduction***

This course will have a **Comprehensive Final Exam!** Homeworks will be word problems, mostly.

#constitutive
: Governing equation of state: e.g. defining relationship between stress and strain as in #ISV Theory

*[ISV]: Internal State Variable



## Preliminaries
## Continuum Mechanics
Based on the concept that there exists space between atoms at lower length scales, but this is summarized by some measurement of density wherein there are no gaps between atoms at the *continuum* length scale.
This assumptions works well at this length scale, and not necessarily for lower length scales.

[[knudsen-number]]

==Continuum mechanics cannot be applied if this ratio is close to unity.==
If the length scale of observation, $\lambda$ is much smaller than the specimen, then continuum can be applied.
If the *[[knudsen-number]]* is too large, then the theory cannot be applied.
The theory primarily relies on the assumption that matter is uniformly distributed throughout the material: i.e.
#FEM softwares rely on this assumption.


---


*Lecture (2): August 24, 2022*

## Notation

There exists many types of coordinate systems, but we typically think of *#Cartesian* coordinates.

Basis Vector
: A unit vector in the direction of an axis.

Tensor
: A mathematical representation of a physical quantity (more than a simple matrix):
  - Independent of chosen coordinate system
  - Must obey certain linear transformation laws

$\underset{\sim}{D}$ denotes tensor quantity.
Tensors also have a rank or order.
- 0: scalar
- 1: vector
- 2: 2nd order tensor (e.g. stress, strain)
- 4: 4th order tensor (e.g. elastic stiffness)

Indices denotes that component of vector or component of certain vector within a matrix.
The range of the indices is length of the vector or number of columns in a matrix.
A tensor has $$\text{number of independent components} = \text{range}^{\text{rank}}$$

Einstein Summation Convention
: Repeated/Dummy indices (on a single term) represents summation over the entire range of the indices.

!!! example Examples
    - Scaling a tensor: $B_{k}\underset{\sim}{e_{k}} = B_{1}\underset{\sim}{e_{1}} + B_{2}\underset{\sim}{e_{2}} + B_{3}\underset{\sim}{e_{3}}$
    - Multiplying Tensor by Tensor: $a_{i}b_{i}$ is simply the **Dot Product.**
    - A 2nd rank tensor: $[\underset{\sim}{B}] = [B_{ij}]$ is the sum along the trace of the tensor.

!!! question What is the rank of $B_{ij}n_{j}$? What type of tensor is it? <cite> lecture
    It starts as a second-rank tensor, because there are two free indices. This is matrix multiplication between matrix and vector that comes out to a vector which is rank 1.

!!! question What if the equation were $n_{j}B_{ij}$? <cite>#Maria-Lee
    This works out to the same matrix, but is transpose of $B_{ij}n_{j}$.


---


*Lecture (3): August 26, 2022*

!!! question What if the equation were $a_{i}b_{j}$? <cite> Joby
    Then the result is a second-rank tensor.

!!! example Example
    $$\begin{split}
    B_{ij}n_{j} &= \begin{bmatrix}
    B_{11} & B_{12} & B_{13} \\
    B_{21} & B_{22} & B_{23} \\
    B_{31} & B_{32} & B_{33}
    \end{bmatrix} \times \begin{bmatrix}
    n_{1} \\
    n_{2} \\
    n_{3}
    \end{bmatrix} \\
    &= \begin{bmatrix}
    B_{11}n_{1} + B_{12}n_{2} + B_{13}n_{3} \\
    B_{21}n_{1} + B_{22}n_{2} + B_{23}n_{3} \\
    B_{31}n_{1} + B_{32}n_{2} + B_{33}n_{3}
    \end{bmatrix}
    \end{split}$$

!!! example Example
    Being that there are no free indices, the result should be a scalar.
    $$\begin{split}
    T_{ij}p_{i}q_{j} &= (T_{11}p_{1}q_{1} + T_{12}p_{1}q_{2} + T_{13}p_{1}q_{3}) \\
    &\qquad+ (T_{11}p_{2}q_{1} + T_{12}p_{2}q_{2} + T_{13}p_{2}q_{3}) \\
    &\qquad+ (T_{11}p_{3}q_{1} + T_{12}p_{3}q_{2} + T_{13}p_{3}q_{3})
    \end{split}$$

[[kroneckers-delta]]

[[permutation-tensor]]


---


*Lecture (4): August 29, 2022*

$a_{i}b_{j}\delta_{ij} \equiv a_{i}\underset{\sim}{e_{i}}b_{j}\underset{\sim}{e_{j}}\underset{\sim}{e_{i}}\cdot\underset{\sim}{e_{j}} \implies a_{i}b_{j}\underset{\sim}{e_{i}}\underset{\sim}{e_{j}}\underset{\sim}{e_{i}}\cdot\underset{\sim}{e_{j}}$, where $\underset{\sim}{e_{j}}\underset{\sim}{e_{j}} = 1$ but the index will switch axes. This further implies $a_{i}b_{j}\underset{\sim}{e_{i}}\underset{\sim}{e_{i}} = a_{i}b_{i}$.

!!! attention Know this for exams!
    Remember how to substitute [[kroneckers-delta]].

!!! info Some useful identities
    See also Schaum’s
    * $\epsilon_{ijk} = -\epsilon_{kji} = \epsilon_{kij} = -\epsilon_{ikj}$
    * sign change property of $\underset{\sim}{\epsilon}$
    * $\epsilon_{miq}\epsilon_{jkq} = \delta_{mj}\delta_{ik} - \delta_{mk}\delta_{ij}$
    * $\underset{\sim}{\epsilon} - \underset{\sim}{\delta}$ identity can be proven by expansion.

    !!! attention
        **THESE ARE SUPER IMPORTANT!!!**

Also, from the sign change property of $\epsilon_{ijk}$:
$$\epsilon_{miq}\epsilon_{jkq} = \epsilon_{miq}\epsilon_{qjk} = \epsilon_{qmi}\epsilon_{qjk} = \epsilon_{qmi}\epsilon_{jkq}$$
In addition, it is easy to show from the $\epsilon_{ijk} - \delta_{pq}$ identity that:
$$\begin{split}
\epsilon_{jkq}\epsilon_{mkq} &= 2\delta_{jm} \quad\because \delta_{jm}\delta_{kk} - \delta_{jk}\delta_{km} \\
\epsilon_{jkq}\epsilon_{jkq} &= 6
\end{split}$$

***Transformation Laws for Tensors***

Let $a_{11}$ equal the direction cosine between the $x’$ and $x$ coordinate axes.
In general,
$$a_{ij} = \cos(\theta_{ij}) = \cos<x’, x>$$
The base vectors $\underset{\sim}{e_{i}’}$ and $\underset{\sim}{e_{i}}$ and coordinates of points defined in each coordinate system.

!!! warning
    ORDER MATTERS WHEN WRITING INDICES!!

This transformation matrix is not necessarily symmetric, but is “#proper-orthogonal”: $\det(a_{ij}) = 1$ which means the magnitude is equal and must be orthogonal:
$$\begin{split}
a_{ij}a_{kj} &= \delta_{ik} \\
a_{ji}a_{jk} &= \delta_{ik}
\end{split}$$
which reduces to $AA^{T} = I \equiv A^{T} = A^{-1}$.


---


*Lecture (5): August 31, 2022*

Transformation Law for 2nd-Order Tensor
: $B_{ij}' = a_{ik}a_{jl}B_{kl}$

: Note order of subscripts! Also, in matrix notation, $[\underset{\sim}{B'}] = [\underset{\sim}{a}][\underset{\sim}{B}][\underset{\sim}{a}]^{T}$.

!!! hint
    $a_{ij}B_{kl}a_{lj} = B_{ij}'$ is incorrect because of $a_{lj}$ which must be $a_{jl}$ to make this a correct statement!

!!! info
    Since the stress tensor is a 2nd-rank tensor, the preceding expression may be used to derive the [Mohr's Circle](engr-727-001-advanced-mechanics-of-materials/mohrs-circle.md) equations corresponding to a state of generalized [plane stress](engr-727-001-advanced-mechanics-of-materials/plane-stress.md).

!!! example Vector Coordinate Transformation
    | ![](../../attachments/engr-725-001-continuum-mechanics/example_vector_coordinate_transformation_220831_182441_EST.png) |
    |:--:|
    | Consider a pair of coordinate axes $x_{i}$ and $x_{i}'$ that share a common origin. Here, the $x_{3}$ and $x_{3}'$-axes are coincident and the remaining $x_{i}'$ axes are rotated $30^{\circ}$ about the $x_{3}$-axis, as shown. |
    Given: $\underset{\sim}{P} = 2e_{1} + 2e_{2} + 2e_{3}$ in $(x_{1}, x_{2}, x_{3})$, find $P_{i}'$ components of $\underset{\sim}{P}$ in $(x_{1}', x_{2}, x_{3},)$.

    !!! hint
        Must determine transformation tensor, $a_{ij} = \cos<x_{i}', x_{i}>$.

    $$\begin{split}
    a_{11} &= \cos<x_{1}', x_{1}> = \cos(30) = \frac{\sqrt{3}}{2} \\
    a_{12} &= \cos<x_{1}', x_{2}> = \cos(60) = \frac{1}{2} \\
    \dots
    \end{split}$$

    Ultimately, $[\underset{\sim}{a}] = \begin{bmatrix}
    \frac{\sqrt{3}}{2} & \frac{1}{2} & 0 \\
    -\frac{1}{2} & \frac{\sqrt{3}}{2} & 0 \\
    0 & 0 & 1
    \end{bmatrix}$ and we apply the vector transformation law: $P_{i}' = a_{ij}P_{j}$.

!!! attention Important for Exam
    Look at example for "Coordinate Transformation for a 2nd-rank Tensor".

!!! hint Rank in Tensor Multiplication
    Inner (dot) product reduces rank by 1, and dyadic (outer) product increases rank by 1.

    !!! example Outer Product of two vectors is a 2nd-Rank tensor.
        $a_{i} \otimes b_{j} = B_{ij}$

***Inner Product***

Suggests a _contraction_ of indices with the #Dot-Product between relevant base vectors.

!!! example For vectors $\underset{\sim}{a}$ and $\underset{\sim}{b}$
    $$\underbrace{\underset{\sim}{a} \cdot \underset{\sim}{b}}_{\text{Denotes Inner Product}} = a_{i}\underset{\sim}{e_{i}} \cdot b_{j}\underset{\sim}{e_{j}} = a_{i}b_{j}\overbrace{\underset{\sim}{e_{i}} \cdot \underset{\sim}{e_{j}}}^{\equiv \delta_{ij}} = a_{i}b_{j}\delta_{ij} = \underbrace{a_{i}b_{i}}_{\text{Scalar!}}$$

!!! tip
    When taking the #Dot-Product between two tensors and writing in standard notation, the dot product **always** goes between $\underset{\sim}{e_{i}}$ and $\underset{\sim}{e_{j}}$!

Properties of Inner Products
- Associate: $(\underset{\sim}{A} \cdot \underset{\sim}{B}) \cdot \underset{\sim}{C} = \underset{\sim}{A} \cdot (\underset{\sim}{B} \cdot \underset{\sim}{C})$
- Distributive
- Not commutative!!



---


*Lecture (6): September 02, 2022*

!!! note Homework 1
    Refer to recorded lecture. If possible, solve problems using indicial notation and not traditional matrix notation.

    Dr. Cho suggests making a study group for these homeworks, but to submit them separately.

    !!! todo Picking Groups
        Make your groups by next class.

## Scalar Product
Suggests a contraction of al indices associated with the product of two tensors of the same rank, resulting in a simple scalar value.

!!! hint
    The scalar product has important energy connotations.

!!! attention The scalar product of a tensor with _itself_ is the square of its norm (magnitude) in homogenous cartesian coordinates.
    $$
    \underbrace{\underset{\sim}{A}:\underset{\sim}{A}}_{\text{Denotes Scalar Product}} = \begin{cases}
    A_{i}A_{i} &, \text{ for vector } \underset{\sim}{A} \\
    A_{ij}A_{ij} &, \text{ for 2nd-rank tensor } \underset{\sim}{A} \\
    \vdots
    \end{cases}
    $$

    !!! example
        $$A:B = A_{ij}:B_{kl} = A_{ij}e_{i}e_{j}:B_{kl}e_{k}e_{l} = A_{ij}B_{kl}\underbrace{e_{i}e_{j}:e_{k}e_{l}}_{\underbrace{(e_{i} \cdot e_{k})}_{\delta_{ik}}\underbrace{(e_{j} \cdot e_{l})}_{\delta_{jl}}} = A_{ij}B_{ij}$$
        Because the final form has two dummy indices, the result is 0 rank which is a scalar.

        !!! attention Exam

==Sometimes, this is called the "Double Dot Product".
However, the definition of "Double Dot Product" only contracts the tensor two times which is not equivalent to a scalar products for tensors of rank greater than 2.==
Scalar product is a scalar for the number of dots!

!!! attention Scalar Product for 4th-rank Tensor
    $A::B$ contracts four times to a 0-rank tensor.
    $A:B$ would only contract two times.

Here, $\underset{\sim}{A}:\underset{\sim}{A} = ||\underset{\sim}{A}||_{2}$ and the result is a positive definite scalar $\geq 0$.
We may also...

!!! attention Exam
    $$\underset{\sim}{A}:\underset{\sim}{B}...$$

The scalar product is routinely used in energy-based formulations.
Example: strain energy density, $\frac{1}{2}\sigma_{ij}\epsilon_{ij} = \frac{1}{2}\sigma:\epsilon$, where $[\underset{\sim}{\sigma}]$ is the Cauchy Stress tensor and $[\underset{\sim}{\epsilon}]$ is the small strain tensor.

!!! question Is this only for the linear, elastic regime? <cite> Sam Scott
    Yes. Generally, we exclude the one half.

!!! note Energy Equation
    $\rho\dot{u} = \underset{\sim}{\sigma}:\underset{\sim}{\epsilon} - \nabla \cdot q + \rho r$. (LHS: kinetic energy) = (RHS: internal energy = mechanical, internal energy - thermal vibration energy + supplied heat)

One may define a second type of scalar product, but differs by a transpose when compared to the first scalar product.
If either A or B is symmetric, these are equivalent.
Originally, $e_{i}e_{j}:e_{k}e_{l} = (eiek ejel)$ but now $eij \cdot\cdot ekl = eilejk$

## Tensor Symmetry
Symmetry may exist between subsets of tensor indices: $A_{ijkl} = A_{ijlk}$ which is symmtric wrt $kl$.
Any 2nd-rank tensor can be decomponsed into symmetric and anti-symmetric (skew-symmetric) parts.

!!! attention Exam
    !!! quote <cite> Dr. Cho
        To me, this is the most important definition in Continuum Mechanics.
    Refer to recorded lecture.

    !!! tip
        $\underset{\sim}{A}:\underset{\sim}{B} = 0$ if $\underset{\sim}{A}$ is symmetric and $\underset{\sim}{B}$ is anti-symmetric.
        !!! question What if the first is anti-symmetric and the second is symmetric? <cite>#Maria-Lee
            Yes because scalar product is commutative.



---


*Lecture (7): September 05, 2022*

!!! todo Student Groups
    Make groups of 3 students and have one email Dr. Cho of the groups but submit homeworks individually.

## Eigenvalues and Eigenvectors of a Symmetric 2nd Rank Tensor
For any symmetric, 2nd rank tensor, $[\underset{\sim}{A}]$, defined relative to an arbitrary cartesion coordinate system, $\underset{\sim}{x}$, it is possible to define a special set of axes, $\underset{\sim}{x^{p}}$, such that the off-diagonal terms of $[\underset{\sim}{A}]$--i.e. $(A_{12}, A_{21}, A_{31}, \dots)$ vanish when the tensor components are referred to this special coordinate system.

!!! hint Mohr's Circle
    This is similar to Mohr's Circle, where the principal stresses occur where there exists no shear stresses, to find the set of coordinates such that the deviatoric of the $\underset{\sim}{A}$ goes to $0$.

![](../../attachments/engr-725-001-continuum-mechanics/principal_coordinates_220905_181827_EST.png)

The eigenvectors are mutually orthogonal.
The eigenvalues of $\underset{\sim}{A}$ are the principal values, and the corresponding eigenvectors are the principal vector directions those eigenvalues express themselves.
Eventually, this comes down a classic eigenvalue problem: $(A - \lambda I) \cdot \underset{\sim}{n} = 0$.
To keep a non-trivial solution, the $|A - \lambda I|$ must be zero to find the eigenvector, $\underset{\sim}{n}$.
This works itself down to the characteristic equation to find the invariants of the matrix: $$\lambda^{3} - I_{1}\lambda^{2} + I_{2}\lambda - I_{3} = 0$$ whose values do not change, even in different coordinate systems.


---


*Lecture (8): September 07, 2022*

!!! help Homework 1: Problem 3
    Show some available conditions for all possible values for [[kroneckers-delta]] on the RHS.

In the principal space, the off-diagonal components go to $0$.

## Tensor Calculus
Some tensors can be thought of as a "field" which can vary either spatially or temporally.
Because tensors represent physical, measurable things, certain operators have very different, physical ramifications.
Partial derivatives are denoted by a comma between dependent and independent variables.
If a subscript repeats, then take the derivative that many repetitions.

!!! example Partial Derivatives
    $\frac{\partial}{\partial x_{i}}() = \partial_{i}() = ()_{,i}$

    !!! example Examples
        $$\begin{split}
        \phi &=  \\
         &= 
        \end{split}$$


---


*Lecture (9): September 09, 2022*

When taking the gradient, there is an index added to the notation; therefore, the resultant tensor will increase a rank from the tensor the gradient is applied onto.

_Divergence_ of $\underset{\sim}{v}$
: $\text{div}(\underset{\sim}{v}) \equiv \underset{\sim}{\nabla}\underset{\sim}{v} = \underset{\sim}{e_{i}}\frac{\partial}{\partial x_{i}}\cdot v_{k}\underset{\sim}{e_{k}} = \frac{\partial v_{k}}{\partial x_{i}} \delta_{ik} = \frac{\partial v_{k}}{\partial x_{k}} \equiv v_{k, k}$.
The physical meaning of this might be seen in a source or sink pushing/pulling material in/out of a system.
Reduces rank of operated tensor by one.

Curl of $\underset{\sim}{v}$
: $\text{curl}(\underset{\sim}{v}) \equiv \underset{\sim}{\nabla}\times \underset{\sim}{v} = (\underset{\sim}{e_{i}}\frac{\partial}{\partial x_{i}}) \times (v_{j}\underset{\sim}{e_{j}}) = \frac{\partial v_{j}}{\partial x_{i}}\underbrace{\underset{\sim}{e_{i}} \times \underset{\sim}{e_{j}}}_{\epsilon_{ijk}\underset{\sim}{e_{k}}}$ wherein the $\epsilon_{ijk}$ is the [[permutation-tensor]].
The physical meaning of this might be the turbulence of a fluid.
This keeps the same rank as the tensor operated on.

!!! attention Dr. Cho's Stars
    Dr. Cho starred the definitions for divergence, curl, and the Laplacian operator.

!!! example Laplacian Operator
    Might be seen in heat equations....(go back to recording).

!!! hint Laplace Equation
    $$\Delta\phi = 0 = \nabla^{2}\phi$$
    which is the *divergence of the gradient of a tensor*.

### Directional Derivative, $\frac{\partial \phi}{\partial n}$
| ![](../../attachments/engr-725-001-continuum-mechanics/directional_derivative_220909_184418_EST.png) |
|:--:|
| Related to the flux of $\phi = \phi(\underset{\sim}{x}, x)$ (which is a scalar field) through a surface in 3D space. |

Consider the projection of the gradient of $\phi$ onto unit outward normal, $\underset{\sim}{n}$:
$$\underset{\sim}{n}\cdot\underset{\sim}{\nabla}\phi = (n_{i}\underset{\sim}{e_{i}}) \cdot (\underset{\sim}{e_{j}}\frac{\partial \phi}{\partial x_{j}}) = \phi_{, j}\delta_{ij}n_{i} = \phi_{, j}n_{i}$$
Ultimately, the directional derivative of $\phi$ can be expressed as:
$$\frac{\partial \phi}{\partial n} \equiv \phi_{, i}n_{i} = n_{i}\frac{\partial \phi}{\partial x_{i}}$$
In general, the directional derivative operator has the following form:
$$\frac{\partial}{\partial b}() = n_{i}\frac{\partial}{\partial x_{i}}()$$


### Divergence Theorem of Gauss
!!! attention Dr. Cho's Stars
    Memorize this!

Consider the tensor field $\underset{\sim}{A}(\underset{\sim}{x}, t)$ defined in the volume, $V$ (which is simply connected with no holes) bounded by surface, $S$.
This works by cancelling out internal surfaces since mass flow occurs at the boundary which represents the net change for the system.


---


*Lecture (10): September 12, 2022*

The divergence in a volume integral is equivalent to a surface integral with a normal vector which is the Divergence Theorem.



## Mechanics
| ![](../../attachments/engr-725-001-continuum-mechanics/mechanics_potato_220912_182401_EST.png) |
|:--:|
| In this section, consider that we are looking at a potato with the displayed notation. |

Surface forces
: those forces

Body forces
: those forces

In this class, we will assume that continuous media naturally satsify relevant concesrtation laws:
- conservation of mass
- conservation of linear and angular momentum
- conservation of energy (1st law of thermo)
- 2nd law of thermodynamics

The combination of the 1st and second law is the [Clausius-Duhem Inequality](https://en.wikipedia.org/wiki/Clausius%E2%80%93Duhem_inequality).

!!! info Quantum Mechanics
    The above list does not hold in quantum mechanics because mass can switch to energy and vice versa: $E = mc^{2}$.
    The above assumptions are length-scale dependent!


### Analysis of Stress
This will focus on the deformation component (and not rigid body motion) of static cases.
We learn about rigid body motion in Dynamics and deformation in MoM.

Stress
: Resistance to deformation.
Mathematically, a pressure which is a force per area.

This is an undergraduate definition.
We will show the graduate level definition today.

!!! quote <cite> Dr. Cho
    Stress comes from traction.
    This comes from Cauchy thinking about surface tractions and representing this as a tensor.

| ![](../../attachments/engr-725-001-continuum-mechanics/stress_potato_220912_183845_EST.png) |
|:--:|
| Consider an arbitrary body in space defined by cartesion coordinate system. |

| ![](../../attachments/engr-725-001-continuum-mechanics/cross-section_potato_220912_183923_EST.png) |
|:--:|
| A cross-section of the potato will have a unit area and normal vector describing the cross-section. |

| ![](../../attachments/engr-725-001-continuum-mechanics/internal_forces_potato_220912_184117_EST.png) |
|:--:|
| Internal forces act on the cross-section which are necessary for equilibrium conditions. |

### Define the "Traction Vector" ("Stress Vector")

*insert this definition later*

| ![](../../attachments/engr-725-001-continuum-mechanics/unit_element_of_potato_220912_184403_EST.png) |
|:--:|
| Consider the special case of a differential cub of material with side orthogonal to coordinate axes. |

The internal forces acting at each face can be decomposed into the coordinate directions which act on the corresponding face of the cube.

$$\begin{rcases}
\underset{\sim}{\Delta F_{1}} = \Delta F_{11}\underset{\sim}{e_{1}} + \Delta F_{12}\underset{\sim}{e_{2}} + \Delta F_{13}\underset{\sim}{e_{3}} \\\
\underset{\sim}{\Delta F_{2}} = \Delta F_{21}\underset{\sim}{e_{1}} + \Delta F_{22}\underset{\sim}{e_{2}} + \Delta F_{23}\underset{\sim}{e_{3}} \\\
\underset{\sim}{\Delta F_{3}} = \Delta F_{31}\underset{\sim}{e_{1}} + \Delta F_{32}\underset{\sim}{e_{2}} + \Delta F_{33}\underset{\sim}{e_{3}}
\end{rcases} = \underset{\sim}{\Delta}F_{i} = \Delta F_{ij}\underset{\sim}{e_{j}}$$

However, we need to denote these internal forces as stresses because these are forces per unit area which scales to any size body.


---


*Lecture (11): September 14, 2022*

!!! hint Homework 2
    | ![](../../attachments/engr-725-001-continuum-mechanics/homework_2_problem_6_visual_aid_220914_182010_EST.png) |
    |:--:|
    | Visual aid for what Problem (6) is asking for. |

!!! example Stress Tensor
    | ![](../../attachments/engr-725-001-continuum-mechanics/stress_tensor_on_cylinder_220914_182340_EST.png) |
    |:--:|
    | Consider a solid circular shaft with applied tensile force, $P$ and torque, $T$ as shown. |

    Take a cross-sectional cut perpendicular to $x_{1}$-axis and examine the internal stresses.
    Only two non-zero stresses arise (based upon #MoM).

    ![](../../attachments/engr-725-001-continuum-mechanics/cross-section_of_cylinder_220914_182506_EST.png)

The stress tensor was determined from the#Cartesian components of the traction vectors acting on three mutually orthogonal planes that are also perpendicular to coordinate axes.
Suppose that one wants to determine $\underset{\sim}{T}(\underset{\sim}{n})$ for the case where $\underset{\sim}{n}$ is not parallel to coordinate axes, consider the " #Cauchy-Tetrahedron ".

![](../../attachments/engr-725-001-continuum-mechanics/cauchy_tetrahedron_220914_184140_EST.png)

!!! attention Dr. Cho's Stars
    Cauchy Formula works with a symmetric tensor.


---


*Lecture (12): September 16, 2022*

!!! info
    Decomposing the traction vector is useful for BVP.

To find the scalar normal stress of the traction vector:
$$\begin{split}
\sigma &= \underset{\sim}{T}\cdot\underset{\sim}{n} = T_{1}n_{1} + T_{2}n_{2} + T_{3}n_{3} \\
 &= \sigma_{ji}n_{j}n_{i}
\end{split}$$

!!! example Rod Under Uniaxial Tension
    | ![](../../attachments/engr-725-001-continuum-mechanics/rod_under_uniaxial_tension_220916_182542_EST.png) |
    |:--:|
    | Given a stress tensor, determine the traction vectors acting on surfaces $AB$, $BC$, and $EF$. |

    Remember that the direction will flip when examining the other side of an internal surface because body is in static equilibrium.


### Differential Equations of Equilibrium
Assume that the stress tensor $[\underset{\sim}{\sigma}]$ is a smooth, varying, and continuous function of spatial position: $[\underset{\sim}{\sigma}] = [\underset{\sim}{\sigma}(\underset{\sim}{x})]$.

!!! hint Recall Taylor Series Expansion
    | ![](../../attachments/engr-725-001-continuum-mechanics/smooth_varying_continuous_function_220916_183233_EST.png) |
    |:--:|
    | $f(x_{2}) = f(x_{1}) + \frac{\partial f(x_{1})}{\partial x}\Delta x \underbrace{+ \frac{1}{2}\frac{\partial^{2}f(x_{1})}{\partial x^{2}}\Delta x^{2} + \dots}_{\text{ignore if } \Delta x \text{ is small}}$ |

    !!! info
        Ignoring the higher-order terms is Euler Method.

#### Force Equilibrium
| ![](../../attachments/engr-725-001-continuum-mechanics/diffeq_equilibrium_potato_220916_183800_EST.png) |
|:--:|
| Consider another loaded body (potato). |
- Look at an infinitesimal unit of dimensions $\Delta x_{1}$, $\Delta x_{2}$, and $\Delta x_{3}$
- Use a two-term Taylor Series Expansion to characterize the stress field.

| ![](../../attachments/engr-725-001-continuum-mechanics/unit_element_in_x1_direction_220916_183945_EST.png) |
|:--:|
| Consider the forces/stresses acting in the $x_{1}$-direction: remember the sign convention on $[\underset{\sim}{\sigma}]$. |

Perform a force equilibrium analysis in the $x_{1}$-direction.
There will by many common terms to simplify the equations.

!!! attention Dr. Cho's Stars
    Boxed Differential Equations of Equilibrium.

!!! note Navier-Stokes versus Stokes
    Navier-Stokes includes the inertial forces of the fluid.
    Stokes ignores these effects (such as low viscosity cases: Earth mantle).
    This chapter formulates the Stokes Equation.

#### Moment Equilibrium
| ![](../../attachments/engr-725-001-continuum-mechanics/moment_equilibrium_plane_stress_220916_185737_EST.png) |
|:--:|
| Consider the 2D case. |

!!! note
    The only surface forces or body forces that create a moment about point P are associated with shear stresses.

    !!! question Why does the stress tensor maintain conservation of angular mommentum? <cite> Dr. Cho
        ==**The stress tensor is always symmetric which conserves angular moementum!**==

        !!! example Simple Shear (Torsion)
            $\begin{bmatrix}
            0 & 1 & 0 \\
            0 & 0 & 0 \\
            0 & 0 & 0
            \end{bmatrix}$ which is not symmetric.

        !!! example Pure Shear
            $\begin{bmatrix}
            0 & 1 & 0 \\
            1 & 0 & 0 \\
            0 & 0 & 0
            \end{bmatrix}$ is symmetric.

!!! todo Formulating Stress Tensor
    Derive the flexure formula yourself from the loaded cantilever.


---


*Lecture (13): September 19, 2022*

!!! info Looking at Homework 2
    1. Expand these with indicial notation.

### Principal Stresses
This is an #eigenvalue problem.
Regardless of the state of stresa t apoint in deformable boddy (provided that $[\underset{\sim}{\sigma}] = [\underset{\sim}{\sigma}]^{T}), it is possible to choose a special set of coordinate axes passing through the point such that the shear stresses vanish when the stress components are referred to this system of axes.
These special axes are cllaed "princpial axes of stress" and seac defines a prinicpal directino.

![](../../attachments/engr-725-001-continuum-mechanics/principal_stresses_potato_220919_182201_EST.png)

#### Determination of prinicpal stresses and principal directions
Consider the special case where the traction vector Tsquiqqle is parallel to the unit normal vector to the surface upon which it acts.
IF Tsuiggle is colinear with n, then we can express trh traction vector as a scalar multiple of n which is embedeed in Cauhchy Formula.s

!!! hint Second Stress Invariant
    Aka distortion energy.
    Is von Mises yeild critetion (effective/equilibrium stress) if over deviatoric stress: $J_{2} = \sqrt{\frac{3}{2}\tau:\tau}$.

    !!! attention Dr. Cho's Stars
        Memorize the stress invariants.

!!! note Each principal stress (eigenvalue) has an associated unit vecotr (eiegevctor) that defines the line of action of the pinricpla stress.
    Recall that these eigenvectors are each row of the transofrmation matrix.

#### Maximum of in-plane shear stresses
principal stresses given the extemum normal stresses at a point in a deformationable body.
I tis also desirable to determine those planes where the in-plane shear stresses assume extremum values.
| ![](../../attachments/engr-725-001-continuum-mechanics/maximum_in-plane_shear_220919_184528_EST.png) |
|:--:|
| Therefore, consider a differential volume element defined relative to principal coordinates. This is similar to moving, angularlly, in ohr's circle. |

