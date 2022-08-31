# Alternating-Direction Implicit

$$\begin{equation}
\begin{split}
\bigg(1 - \frac{\mu_{x}}{2}\delta_{x}^{2}\bigg)\bigg(1 - \frac{\mu_{y}}{2}\delta_{y}^{2}\bigg)\Delta u_{i, j} &= (\mu_{x}\delta_{x}^{2} + \mu_{y}\delta_{y}^{2})u_{i, j}^{n} \\
\bigg(1 - \frac{\mu_{x}}{2}\delta_{x}^{2}\bigg)\Delta u_{i, j}^{*} &= (\mu_{x}\delta_{x}^{2} + \mu_{y}\delta_{y}^{2})u_{i, j}^{n} \text{ Step 1} \\
\bigg(1 - \frac{\mu_{y}}{2}\delta_{y}^{2}\bigg)\Delta u_{i, j} &= \Delta u_{i, j}^{*} \text{ Step 2} \\
\boxed{u_{i, j}^{n + 1}} &= \boxed{u_{i, j}^{n} + \Delta u_{i, j}} \text{ Step 4}
\end{split}
\end{equation}$$