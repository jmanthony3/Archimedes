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
  - [Continuum Mechanics](#continuum-mechanics)
  - [Notation](#notation)
  - [Scalar Product](#scalar-product)
  - [Tensor Symmetry](#tensor-symmetry)
  - [Eigenvalues and Eigenvectors of a Symmetric 2nd Rank Tensor](#eigenvalues-and-eigenvectors-of-a-symmetric-2nd-rank-tensor)


---


*Lecture (1): August 22, 2022*

***Introduction***

This course will have a **Comprehensive Final Exam!** Homeworks will be word problems, mostly.

#constitutive
: Governing equation of state: e.g. defining relationship between stress and strain as in #ISV Theory

*[ISV]: Internal State Variable

## Continuum Mechanics
Based on the concept that there exists space between atoms at lower length scales, but this is summarized by some measurement of density wherein there are no gaps between atoms at the *continuum* length scale. This assumptions works well at this length scale, and not necessarily for lower length scales.

[[knudsen-number]]

==Continuum mechanics cannot be applied if this ratio is close to unity.== If the length scale of observation, $\lambda$ is much smaller than the specimen, then continuum can be applied. If the *[[knudsen-number]]* is too large, then the theory cannot be applied. The theory primarily relies on the assumption that matter is uniformly distributed throughout the material: i.e. #Finite-Element-Method softwares rely on this assumption.


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

$\underset{\sim}{D}$ denotes tensor quantity. Tensors also have a rank or order.
- 0: scalar
- 1: vector
- 2: 2nd order tensor (e.g. stress, strain)
- 4: 4th order tensor (e.g. elastic stiffness)

Indices denotes that component of vector or component of certain vector within a matrix. The range of the indices is length of the vector or number of columns in a matrix. A tensor has $$\text{number of independent components} = \text{range}^{\text{rank}}$$

Einstein Summation Convention
: Repeated/Dummy indices (on a single term) represents summation over the entire range of the indices.

!!! example Examples
    - Scaling a tensor: $B_{k}\underset{\sim}{e_{k}} = B_{1}\underset{\sim}{e_{1}} + B_{2}\underset{\sim}{e_{2}} + B_{3}\underset{\sim}{e_{3}}$
    - Multiplying Tensor by Tensor: $a_{i}b_{i}$ is simply the **Dot Product.**
    - A 2nd rank tensor: $[\underset{\sim}{B}] = [B_{ij}]$ is the sum along the trace of the tensor.

!!! question What is the rank of $B_{ij}n_{j}$? What type of tensor is it? <cite> lecture
    It starts as a second-rank tensor, because there are two free indices. This is matrix multiplication between matrix and vector that comes out to a vector which is rank 1.

!!! question What if the equation were $n_{j}B_{ij}$? <cite> Maria
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

Let $a_{11}$ equal the direction cosine between the $x’$ and $x$ coordinate axes. In general,
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
    Since the stress tensor is a 2nd-rank tensor, the preceding expression may be used to derive the #Mohrs-Circle equations corresponding to a state of generalized #plane-stress.

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

==Sometimes, this is called the "Double Dot Product". However, the definition of "Double Dot Product" only contracts the tensor two times which is not equivalent to a scalar products for tensors of rank greater than 2.== Scalar product is a scalar for the number of dots!

!!! attention Scalar Product for 4th-rank Tensor
    $A::B$ contracts four times to a 0-rank tensor. $A:B$ would only contract two times.

Here, $\underset{\sim}{A}:\underset{\sim}{A} = ||\underset{\sim}{A}||_{2}$ and the result is a positive definite scalar $\geq 0$. We may also...

!!! attention Exam
    $$\underset{\sim}{A}:\underset{\sim}{B}...$$

The scalar product is routinely used in energy-based formulations. Example: strain energy density, $\frac{1}{2}\sigma_{ij}\epsilon_{ij} = \frac{1}{2}\sigma:\epsilon$, where $[\underset{\sim}{\sigma}]$ is the Cauchy Stress tensor and $[\underset{\sim}{\epsilon}]$ is the small strain tensor.

!!! question Is this only for the linear, elastic regime? <cite> Sam Scott
    Yes. Generally, we exclude the one half.

!!! note Energy Equation
    $\rho\dot{u} = \underset{\sim}{\sigma}:\underset{\sim}{\epsilon} - \nabla \cdot q + \rho r$. (LHS: kinetic energy) = (RHS: internal energy = mechanical, internal energy - thermal vibration energy + supplied heat)

One may define a second type of scalar product, but differs by a transpose when compared to the first scalar product. If either A or B is symmetric, these are equivalent. Originally, $e_{i}e_{j}:e_{k}e_{l} = (eiek ejel)$ but now $eij \cdot\cdot ekl = eilejk$

## Tensor Symmetry
Symmetry may exist between subsets of tensor indices: $A_{ijkl} = A_{ijlk}$ which is symmtric wrt $kl$. Any 2nd-rank tensor can be decomponsed into symmetric and anti-symmetric (skew-symmetric) parts.

!!! attention Exam
    !!! quote <cite> Dr. Cho
        To me, this is the most important definition in Continuum Mechanics.
    Refer to recorded lecture.

    !!! tip
        $\underset{\sim}{A}:\underset{\sim}{B} = 0$ if $\underset{\sim}{A}$ is symmetric and $\underset{\sim}{B}$ is anti-symmetric.
        !!! question What if the first is anti-symmetric and the second is symmetric? <cite> Maria
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

The eigenvectors are mutually orthogonal. The eigenvalues of $\underset{\sim}{A}$ are the principal values, and the corresponding eigenvectors are the principal vector directions those eigenvalues express themselves. Eventually, this comes down a classic eigenvalue problem: $(A - \lambda I) \cdot \underset{\sim}{n} = 0$. To keep a non-trivial solution, the $|A - \lambda I|$ must be zero to find the eigenvector, $\underset{\sim}{n}$. This works itself down to the characteristic equation to find the invariants of the matrix: $$\lambda^{3} - I_{1}\lambda^{2} + I_{2}\lambda - I_{3} = 0$$ whose values do not change, even in different coordinate systems.