# ENGR 725-001: Continuum Mechanics

*Lecture (1): August 22, 2022*

**Comprehensive Final Exam!**

**Constitutive :** governing equation of state: e.g. defining relationship between stress and strain as in ISV Theory

Homeworks will be word problems, mostly.

## Continuum Mechanics

Based on the concept that there exists space between atoms at lower length scales, but this is summarized by some measurement of density wherein there are no gaps between atoms at the *continuum* length scale. This assumptions works well at this length scale, and not necessarily for lower length scales.

> *Equation: Knudsen Number*
> 
> $$K_{n} = \frac{\lambda}{D}$$
> 
> Where $\lambda$ is the mean free path (e.g. distance between atoms) and $D$ is the characteristic dimension (e.g. molecular diameter).

Continuum mechanics cannot be applied if this ratio is close to unity.

If the length scale of observation, $\lambda$ is much smaller than the specimen, then continuum can be applied. If the *Knudsen Number* is too large, then the theory cannot be applied.

The theory primarily relies on the assumption that matter is uniformly distributed throughout the material: i.e. finite element method softwares rely on this assumption.

* * *

*Lecture (2): August 24, 2022*

## Notation

There exists many types of coordinate systems, but we typically think of *Cartesian* coordinates.

**Basis Vector**

    A unit vector in the direction of an axis.

**Tensor**

    A mathematical representation of a physical quantity (more than a simple matrix):

- Independent of chosen coordinate system
    
- Must obey certain linear transformation laws
    

$\underset{\sim}{D}$ denotes tensor quantity. Tensors also have a rank or order.

- 0: scalar
    
- 1: vector
    
- 2: 2nd order tensor (e.g. stress, strain)
    
- 4: 4th order tensor (e.g. elastic stiffness)
    

Indices denotes that component of vector or component of certain vector within a matrix. The range of the indices is length of the vector or number of columns in a matrix. A tensor has $$\text{number of independent components} = \text{range}^{\text{rank}}$$

<table><tbody><tr><td><p>Input example table of range to rank</p></td><td><p></p></td></tr><tr><td><p></p></td><td><p></p></td></tr></tbody></table>

**Einstein Summation Convention**

    Repeated/Dummy indices (on a single term) represents summation over the entire range of the indices.

Examples:

- Scaling a tensor: $B_{k}\underset{\sim}{e_{k}} = B_{1}\underset{\sim}{e_{1}} + B_{2}\underset{\sim}{e_{2}} + B_{3}\underset{\sim}{e_{3}}$
    
- Multiplying Tensor by Tensor: $a_{i}b_{i}$ is simply the **Dot Product.**
    
- A 2nd rank tensor: $[\underset{\sim}{B}] = [B_{ij}]$ is the sum along the trace of the tensor.
    

> Q: What is the rank of $B_{ij}n_{j}$? What type of tensor is it?  
> A: It starts as a second-rank tensor, because there are two free indices. This is matrix multiplication between matrix and vector that comes out to a vector which is rank 1.

> Q (Maria): What if the equation were $n_{j}B_{ij}$?  
> A: This works out to the same matrix, but is transpose of $B_{ij}n_{j}$.

* * *

*Lecture (3): August 26, 2022*

> Q(Joby): What if the equation were $a_{i}b_{j}$?  
> A: *Then the result is a second-rank tensor.*

> Example
> 
> $$\begin{split}  
> B_{ij}n_{j} &= \begin{bmatrix}  
> B_{11} & B_{12} & B_{13} \\  
> B_{21} & B_{22} & B_{23} \\  
> B_{31} & B_{32} & B_{33}  
> \end{bmatrix} \times \begin{bmatrix}  
> n_{1} \\  
> n_{2} \\  
> n_{3}  
> \end{bmatrix} \\  
> &= \begin{bmatrix}  
> B_{11}n_{1} + B_{12}n_{2} + B_{13}n_{3} \\  
> B_{21}n_{1} + B_{22}n_{2} + B_{23}n_{3} \\  
> B_{31}n_{1} + B_{32}n_{2} + B_{33}n_{3}  
> \end{bmatrix}  
> \end{split}$$

> Example
> 
> Being that there are no free indices, the result should be a scalar.
> 
> $$\begin{split}  
> T_{ij}p_{i}q_{j} = (T_{11}p_{1}q_{1} + T_{12}p_{1}q_{2} + T_{13}p_{1}q_{3}) \\  
> \qquad+ (T_{11}p_{2}q_{1} + T_{12}p_{2}q_{2} + T_{13}p_{2}q_{3}) \\  
> \qquad+ (T_{11}p_{3}q_{1} + T_{12}p_{3}q_{2} + T_{13}p_{3}q_{3})  
> \end{split}$$

**Kronecker’s Delta, $\delta_{ij}$**

> $$\begin{split}  
> \delta_{ij} &= \begin{cases}  
> 1 &, i = j \\  
> 0 &, i \neq j  
> \end{cases} \\  
> &= \underset{\sim}{e_{1}} \cdot \underset{\sim}{e_{2}} = \frac{\partial x_{i}}{\partial x_{j}}  
> \end{split}$$

Eventually, this becomes the identity matrix which is always a second rank tensor. The last statement in the above equation, is the inner product of the two vectors: $|\vec{a}||\vec{b}|\cos(\theta)$. This delta is sometimes called the **Substitution Operator**. This absorbs the repeating index and replaces with the remaining free index: $\delta_{ij}\underset{\sim}{e_{j}} \rightarrow \underset{\sim}{e_{i}}$.

***Permutation Tensor, $\epsilon_{ijk}$***

> $$\begin{split}  
> \epsilon_{ijk} &= \begin{cases}  
> 1 &, \text{ for even permutation of } i, j, k \\  
> \-1 &, \text{ for odd permutation of } i, j, k \\  
> 0 &, \text{ two or more equal indices }  
> \end{cases}  
> \end{split}$$

Essentially, if the indices increase, cyclically (left-right) then is 1, else if decrease left-right is -1, otherwise is 0.

> Example: Calculating a Moment
> 
> $M = x \times F \equiv \epsilon_{ijk}x_{j}F_{k}$

* * *

*Lecture (4): August 29, 2022*

$a_{i}b_{j}\delta_{ij} \equiv a_{i}\underset{\sim}{e_{i}}b_{j}\underset{\sim}{e_{j}}\underset{\sim}{e_{i}}\cdot\underset{\sim}{e_{j}} \implies a_{i}b_{j}\underset{\sim}{e_{i}}\underset{\sim}{e_{j}}\underset{\sim}{e_{i}}\cdot\underset{\sim}{e_{j}}$, where $\underset{\sim}{e_{j}}\underset{\sim}{e_{j}} = 1$ but the index will switch axes. This further implies $a_{i}b_{j}\underset{\sim}{e_{i}}\underset{\sim}{e_{i}} = a_{i}b_{i}$.

IMPORTANT:

    Remember how to subsitutue Kroenecker’s Delta.

***Some useful identities***

See als schaum’s

> $\epsilon_{ijk} = -\epsilon_{kji} = \epsilon_{kij} = -\epsilon_{ikj}$
> 
> sign change property of $\underset{\sim}{\epsilon}$.
> 
> $\epsilon_{miq}\epsilon_{jkq} = \delta_{mj}\delta_{ik} - \delta_{mk}\delta_{ij}$
> 
> $\underset{\sim}{\epsilon} - \underset{\sim}{\delta}$ identity can be proven by expansion.
> 
> **THESE ARE SUPER IMPORTANT!!!**

Also, from the sign change property of $\epsilon_{ijk}$: $$\epsilon_{miq}\epsilon_{jkq} = \epsilon_{miq}\epsilon_{qjk} = \epsilon_{qmi}\epsilon_{qjk} = \epsilon_{qmi}\epsilon_{jkq}$$

In addition, it is easy to show fro mthe $\epsilon_{ijk} - \delta_{pq}$ identity that: $$\begin{split}  
\epsilon_{jkq}\epsilon_{mkq} &= 2\delta_{jm} &\because \delta_{jm}\delta_{kk} - \delta_{jk}\delta_{km} \\  
\epsilon_{jkq}\epsilon_{jkq} &= 6  
\end{split}$$

***Transformation Laws for Tensors***

Let $a_{11}$ equal the direction cosine between the $x’$ and $x$ coordinate axes. In general, $$a_{ij} = \cos(\theta_{ij}) = \cos<x’, x>$$ The base vectors $\underset{\sim}{e_{i}’}$ and $\underset{\sim}{e_{i}}$ and coordinates of points defined in each coordinate system.

ORDER MATTERS WHEN WRITING INDICES!!

This transformation matrix is not necessarily symmetric, but is “proper orthogonal”: $det[a_{ij}] = 1$ which means the magnitude is equal and must be orthogonal: $$\begin{split}  
a_{ij}a_{kj} &= \delta_{ik} \\  
a_{ji}a_{jk} = \delta_{ik}  
\end{split}$$ which reduces to $AA^{T} = I \equiv A^{T} = A^{-1}$.