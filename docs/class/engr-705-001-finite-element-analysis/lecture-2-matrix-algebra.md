<!-- 20230119T08:26 -->
# Matrix Algebra
## Introduction to Matrix Notation
Matrix notation represents a simple system for writing and solving sets of simultaneous algebraic equations.

Matrix
: A rectangular array of quantities arranged in rows and columns that is used to express and solve a system of equations.

- Order/Dimension: $m \times n$ is the size of the matrix.
- A matrix $m \times n$ means a matrix with $m$ rows and $n$ columns. Rows always come first.
- If $m \neq n$, the matrix is called rectangular...

## Types of Matrices
- Null or Zero Matrix: A matrix in which each element is 0 is called a Null or Zero matrix. Zero matrices are generally denoted by the symbol $O$.
- Square Matrix: A matrix $A$ have same number of rows and columns is called a square matrix.
- Principal Diagonal ($a_{ii}$): Extends from the upper left-hand corner to the lower right-hand corner of the square matrix.
- Diagonal Matrix: A square matrix in which all elements are zero except the principal diagonal.
- Identity Matrix or Unit Matrix: A diagonal matrix in which each diagonal element is 1 (unity). An identity matrix is denoted as $I$.

## Operations with Matrices
- Multiplication of a matrix by a scaler: If $A$ is a matrix and $k$ is a scalar (constant), then $kA$ is a matrix whose elements are the elements of $A$, each multiplied by $k$.
- The addition of two matrices, $A$ [$a_{ij}$] and $B$ [$b_{ij}$] of the same order is obtained by adding the corresponding entries of $A$ and $B$.
### Matrix Multiplication
The product of a $m \times n$ matrix $A$ [$a_{ij}$] and $r \times p$ matrix $B$ [$b_{ij}$] is defined if $n = r$ and is the matrix $C$ of size $m \times p$.
- Is is, two matrices $A$ and $B$ are said to be conformable for the product $AB$ if the number of columns of $A$ is equal to the number of rows of $B$.
- The elements of $C$ are determined as follows: the element $c_{ij}$ in the $i$'th row and the $j$'th column of $C$ $m \times p$ is: $$c_{ij} = $$
- For instance, $c_{ij}$ is obtained by multiplying the elements of the first row of $A$ by the corresponding elements of the first column of $B$ and adding the product.

Properties of Matrix Multiplication
1. Multiplication of matrices is not commutative: i.e. $AB \neq BA$ in general.
2. A matrix $A$ can be multiplied by itself iff it is a square matrix. The product $A \cdot A$ in such cases is written as $A^{2}$. Similarly, we may define higher powers of a square matrix: i.e. $A \cdot A^{2} = A^{3}$.

### Transpose of a Matrix
The transpose of a matrix is obtained by interchanging its corresponding rows and columns.
Thus the first row of $A^{(T)}$ is the first of $A$, the second row of $A$ as its second column and so on.

## Special Matrices
- Symmetric Matrix: A square matrix $A$ is symmetric if $A = A^{(T)}$.
- Skew Symmetric: A square matrix $A$ is called skew symmetric if $A = -A^{(T)}$.
- Triangular Matrices
  - Upper: Square matrices that can have non-zero entries only on and above the main diagonal.
  - Lower: Square matrices that can have non-zero entries only on and below the main diagonal.

## Second and Third Order Determinants
The determinant of a matrix is a scalar (number), obtained from the elements of a matrix by specified operations, which is characteristic of the matrix.
The determinants are defined only for square matrices.
It is denoted by $\text{det}(A)$ or $|A|$ for a square matrix $A$.
- Second Order: $a_{11}a_{22} - a_{12}a_{21}$
- Third Order or greater: The determinant is found by find the product of the determinants of all sub-matrices.

## Minor and Cofactor of Element
Minor of the Elements: the minor $M_{ij}$ of the element $a_{ij}$ in a given matrix is the determinant of order ($n - 1 \times n - 1$) obtained by deleting the $i$'th row and $j$'th column of a matrix $A$ of size $n \times n$.

!!! note
    The minor of an element is the determinant of the appropriate sub-matrix.

Cofactor of Element: the scalars $C_{ij} = (-1)^{i + j}M_{ij}$ are called the cofactors of the element $a_{ij}$ of the matrix $A$.

## Inverse of Matrix
The inverse of a $n \times n$ matrix $[a]$ is denoted by $[a]^{-1}$ and is a matrix such that: $$[a]^{-1}[a] = [a][a]^{-1} = I$$
Where $I$ is the $n \times n$ unit matrix.
If $[a]$ has an inverse, it is called a non-singular matrix.
If $[a]$ has no inverse, then $[a]$ is called a singular matrix.
The inverse of a non-singular $n \times n$ matrix $[a]$ is given by: $$[a]^{-1} = \frac{1}{\text{det}(a)}Adj[a]$$
Where $Adj[a]$ is the **adjoint matrix**:= $$Adj[a] = [C_{ij}^]{(T)}$$
Where $[C_{ij}]$ is the **cofactor matrix**.

## Orthogonal Matrix
If the inverse of a matrix $[a]$ is equal to its transpose, the matrix is referred to as an *orthogonal matrix*.
In other words, a matrix $[a]$ is orthogonal if: $$[a]^{-1} = [a]^{(T)}$$
An orthogonal matrix frequently used is the transformation or rotation matrix $[T]$.
For instance, the displacement vector components of $d$ expressed in the $xy$ system are related to those in the $x'y'$ system by: $$\begin{split}
{d'} &= [T]{d} \\
\left\{\begin{matrix}
d_{x}' \\
d_{y}'
\end{matrix}\right\} &= \begin{bmatrix}
\cos(\theta) & \sin(\theta) \\
-\sin(\theta) & \cos(\theta)
\end{bmatrix}\left\{\begin{matrix}
d_{x} \\
d_{y}
\end{matrix}\right\}
\end{split}$$

## Differentiation and Integration of a Matrix
A matrix can be differentiated (or integrated) by differentiating (or integrating) each of its elements.

## Linear Systems of Equations
Linear systems of equations are associated with many problems in engineering and science.
A linear system of $n$ equations in $n$ variables is considered here:
$$\begin{split}
a_{11}x_{1} + a_{12}x_{2} + \dots + a_{1n}x_{n} &= b_{1} \\
a_{21}x_{1} + a_{22}x_{2} + \dots + a_{2n}x_{n} &= b_{2} \\
\vdots &= \vdots \\
a_{n1}x_{1} + a_{n2}x_{2} + \dots + a_{nn}x_{n} &= b_{n}
\end{split}$$
Where the matrix $[A]$ and the column vector ${b}$ contain the known constants.
If $A$ is a non-singular matrix, then the system $[A]{x} = {b}$ can be solved by multiplying both sides of the equation by $A^{-1}$.

## Naïve Gauss Elimination
Extension of *Method of Elimination* to large sets of equations by developed a systematic scheme or algorithm to eliminate...

The approach is designed to solve a general set of $n$ equations.
**Forward Elimination of Unknowns**: the first phase is designed...

The procedure is then repeated for the remaining equations.

For the foregoing steps, Eq. (1) is called the **pivot equation** and $a_{11}$ is called the **pivot constant**.

The procedure can be continued using the remaining pivot equations.
The final manipulation in the sequence is to use the $(n - 1)$'th equation to eliminate the $x_{n - 1}$ term from the $n$'th equation.
At this point, the system will have been transformed to an upper triangular system.

## Inverse of a Matrix by Row Reduction (Gauss-Jordan Method)
We begin by converting matrix $[a]$ to an upper triangular form by setting all elements below the main diagonal equal to zero, starting with the first column and continuing with succeeding columns.
We then proceed from the last column to the first, setting all elements above the main diagonal equal to zero.
