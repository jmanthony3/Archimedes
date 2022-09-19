# Alternating-Direction Implicit

Method for 2D heat equation and recommended for 2D or 3D heat equations.
Developed by Douglas and Gunn in 1964.
Start from [Crank-Nicholson](trapezoidal-crank-nicholson-method.md) by substituting $\Delta u_{i, j} = u_{i, j}^{n + 1} - u_{i, j}^{n}$.
$$\begin{equation}
\begin{split}
\bigg(1 - \frac{\mu_{x}}{2}\delta_{x}^{2}\bigg)\bigg(1 - \frac{\mu_{y}}{2}\delta_{y}^{2}\bigg)\Delta u_{i, j} &= (\mu_{x}\delta_{x}^{2} + \mu_{y}\delta_{y}^{2})u_{i, j}^{n} \\
\bigg(1 - \frac{\mu_{x}}{2}\delta_{x}^{2}\bigg)\Delta u_{i, j}^{*} &= (\mu_{x}\delta_{x}^{2} + \mu_{y}\delta_{y}^{2})u_{i, j}^{n} \text{ Step 1} \\
\bigg(1 - \frac{\mu_{y}}{2}\delta_{y}^{2}\bigg)\Delta u_{i, j} &= \Delta u_{i, j}^{*} \text{ Step 2} \\
\boxed{u_{i, j}^{n + 1}} &= \boxed{u_{i, j}^{n} + \Delta u_{i, j}} \text{ Step 4}
\end{split}
\end{equation}$$
This equation requires #tridiagonal inversion.
The factorization error increases the #truncation-error, but the resulting scheme is still **second-order**.