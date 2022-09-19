---
aliases: Galerkin-Method
---
# Weighted-Residual Approach (Galerkin)

This starts with residual of the differential equations.
Approximate the solution with piecewise continuous [basis function](basis-function.md).
$$\begin{split}
-\frac{d}{dx}\bigg(p(x)\frac{du}{dx}\bigg) &= f(x) \\
-\frac{d}{dx}\bigg(p(x)\frac{du}{dx}\bigg) &= P(u) \\
R(u) &= P(u) - f \\
u_{h}(x) &= \sum_{j = 1}^{n}c_{j}\phi_{j}(x) \\
R(u_{h}) &= P(u_{h}) - f \neq 0
\end{split}$$