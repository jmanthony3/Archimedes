# Application of Numerical Methods on Elliptic PDE

## Laplace Equation
From the heat equation, the **[Laplace equation](laplace-equation.md)** sets the LHS to $0$:
$$\overbrace{\cancel{\frac{\partial T}{\partial t}}}^{0} = \alpha\nabla^{2}T$$

- Every point influences every other point.
- Solution of #PDE is desired in a closed domain subject to a prescribed set of boundary conditions (#BVP).
- #steady-state temperature distributions, incompressible inviscid flows, and equilibrium stress distributions in solids.

[Laplace Equation](laplace-equation.md)
: $\nabla^{2}u = \frac{\partial^{2}u}{\partial x^{2}} + \frac{\partial^{2}u}{\partial y^{2}} = 0$

[Poisson's Equation](poissons-equation.md)
: $\nabla^{2}u = \frac{\partial^{2}u}{\partial x^{2}} + \frac{\partial^{2}u}{\partial y^{2}} = f(x, y)$



## Finite Difference Approximations
Like the heat equation, the variations in methods for solving [Laplace's equation](laplace-equation.md) have to do with how the system of equation is solved, not the differencing.

[Five-point Formula](five-point-formula.md) ($h = \Delta x$, $k = \Delta y$)
: $\frac{u_{i + 1, j} - 2u_{i, j} + u_{i - 1, j}}{h^{2}} + \frac{u_{i, j + 1} - 2u_{i, j} + u_{i, j - 1}}{h^{2}} = 0$

We apply our difference equation at each mesh point in the interior of the domain (assuming #Dirichlet-Boundary-Condition) and end up with a linear #system-of-equations, A ($n \times n$ matrix).
To solve the linear #system-of-equations, we may use either direct or iterative methods.
#direct-solver give the solution (exactly if no #round-off-error; there is still #FD #discretization-error) in a finite...



## Iterative Techniques
Repeated application of an algorithm that produces an exact result only as the limit of a sequence.
#iterative-solver are also known as "**#residual-relaxation-method**".

- Point #iterative-solver in which the same, simple algorithm is applied to each point where the unknown function is to be determined in successive iterative sweeps: #Jacobi-Method, #Gauss-Seidel-Method, #SOR, #Coloring-Scheme, #Conjugate-Gradient-Method, etcetera.
- Block #iterative-solver in which subgroups of points are singled out for solution by elimination schemes in an overall iterative procedure (unknown in subgroups are set up so that the matrix of coefficients will be #tridiagonal form to allow the #Thomas-Algorithm to be used: e.g. SOR by lines).


### [Multigrid Method](multigrid-method.md)