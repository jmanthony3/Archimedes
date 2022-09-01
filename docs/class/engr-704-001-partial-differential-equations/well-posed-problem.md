# Well-Posed Problem

1. Solution to the problem must exist: #existence.
2. Solution to the problem must be unique: #uniqueness.
3. Solution to the problem must depend continuously on the initial or boundary data (small changes in the initial or boundary conditions result in small changes in the solution): #stability.

!!! example Laplace Equation
    $u_{xx} + u{yy} = 0$ for $-\infty < x \infty$ and $y \geq 0$. For a boundary condition at $y = 0$: $u(x, y) = 0$, the analytical solution may be found by using separation of variables: $u = \frac{1}{n^{2}}\sin(nx)\sinh(ny)$

    As $n$ increases, $u$ approaches $\frac{e^{ny}}{n^{2}}$ and grows rapidly even for small $y$. So the solution is NOT continuous with the boundary condition, and the problem is not #well-posed. Laplace equation requires boundary condition for closed domain. In this problem, only one side boundary condition is given at $y = 0$ and treated like an open domain.