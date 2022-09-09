# Rayleigh-Ritz Method

The solution $u$ is approximated by minimizing the integral not over all the functions, but over the piecewise set of functions ([[basis-function]]).
The [[basis-function]] are linearly independent and satisfy $\phi_{i}(0) = \phi{i}(1) = 0$. $$\begin{equation}
\begin{split}
\mathcal{v}(x) &= \sum_{j = 1}^{n}c_{j}\phi_{j}(x) \\
I(\mathcal{v}) &= \int_{0}^{1}[p(x)(\mathcal{v}'(x))^{2} - 2f(x)\mathcal{v}(x)]dx \\
\frac{dI}{dc_{i}} &= \int_{0}^{1}2p(x)\big(\sum_{j = 1}^{n}c_{j}\phi_{j}'\big)\phi_{j}'dx - \int_{0}^{1}2f(x)\phi_{j}(x)dx = 0
\end{split}
\end{equation}$$