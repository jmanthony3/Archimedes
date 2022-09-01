# Mathematical Classifications

Information in physical problems:
- Equations (single or system) that admit wave-like solutions: hyperbolic.
- Equations that admit damped wave-like solutions: parabolic.
- Solution(s) are not wave-like: elliptic.

[[characteristic-path]]
: A line in 2D or surface in 3D that transfers the trajectory of a particle ("information") to physical problems governed by #PDE.
    - On this path, certain quantities remain constant or **certain derivatives may be discontinuous**.
    - E.g. shockwave in a fluid.

Throughout this chapter, each Second Order #PDE will be of the following form:

$$\begin{equation}
\begin{split}
a\phi_{xx} + b\phi_{xy} + c\phi_{yy} + d\phi_{x} + e\phi_{y} + f\phi &= g(x, y) \\
a\phi_{xx} + b\phi_{xy} + c\phi_{yy} &= -(d\phi_{x} + e\phi_{y} + f\phi - g(x, y)) = H
\end{split}
\end{equation}$$
\label{eq:pde_general_form}

If the characteristics of this equation exists (real curves within the solution domain), then that means there are **some locations where the second derivatives may be discontinuous** (shockwave in supersonic flow). We solve this by substituting $u = \phi_{xx}$, $\mathcal{v} = \phi_{xy}$, and $w = \phi_{yy}$ along this #characteristic-path and modifying the equation:

$$\begin{split}
\begin{bmatrix}
a & b & c \\
\frac{dx}{d\tau} & \frac{dy}{d\tau} & 0 \\
0 & \frac{dx}{d\tau} & \frac{dy}{d\tau}
\end{bmatrix}\begin{bmatrix}
u \\
\mathcal{v} \\
w
\end{bmatrix} &= \begin{bmatrix}
H \\
\frac{dp}{d\tau} \\
\frac{dq}{d\tau}
\end{bmatrix} \\
au + b\mathcal{v} + cw &= H \\
\frac{dp}{d\tau} &= \frac{dx}{d\tau}u + \frac{dy}{d\tau}\mathcal{v} \\
\frac{dq}{d\tau} &= \frac{dx}{d\tau}\mathcal{v} + \frac{dy}{d\tau}w
\end{split}$$

When the [[characteristic-path]] is discontinuous, then no unique solution for the second derivatives exist because the determinant of the coefficient matrix is zero.

*[LHS]: Left-Hand Side
*[RHS]: Right-Hand Side

$$\begin{split}
a\big(\frac{dy}{d\tau}\big)^{2} - b\big(\frac{dy}{d\tau}\big)\big(\frac{dx}{d\tau}\big) + c\big(\frac{dx}{d\tau}\big^{2}) &= 0 \\
a\big(\frac{dy}{dx}\big)^{2} - b\big(\frac{dy}{dx}\big) + c &= 0 \\
\implies h &= \frac{b \pm \sqrt{b^{2} - 4ac}}{2a}
\end{split}$$

## Hyperbolic PDE
For $b^{2} - 4ac > 0$.

[[domain-of-dependence]]
: That portion of the problem domain that influences the value of the solution at a given point of a #PDE.

Limited [[domain-of-dependence]] in solution. Bound by two [[characteristic-path]] and dependent on initial and boundary conditions. Generally involved with the second time derivative wrt time: e.g. oscillations and wave-like behavior, convection, vibration, etcetera.

## Parabolic PDE
For $b^{2} - 4ac = 0$. Associated with #diffusion and involved with first derivative wrt time. Starts with some initial domain to march forward in time or in a time-like direction. Does not show a limitation of [[domain-of-dependence]]. The solution at a certain time depends on the entire physical domain and any side boundary conditions: e.g. heat equations.

## Elliptic PDE
For $b^{2} - 4ac < 0$. Steady-state (no time involved) and dependent on boundary conditions: Laplace equation, Poisson equation, etcetera.