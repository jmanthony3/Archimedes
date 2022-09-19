# Linear FEM (k = 1)

The nodal points coincide with the grid points $\{x_{j}\}$.
The [basis function](basis-function.md) associated with $x_{j}$ is defined as: $$\begin{equation}
\phi_{j}(x) = \begin{cases}
0 &, x < x_{j - 1} \\
\frac{1}{h_{j}}(x - x_{j - 1}) &, x \in [x_{j - 1}, x_{j}] \\
\frac{1}{h_{j + 1}}(x_{j + 1} - x) &, x \in [x_{j}, x_{j + 1}] \\
0 &, x_{j + 1} < x
\end{cases}
\end{equation}$$