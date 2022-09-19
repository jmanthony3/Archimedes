# Lax Method

The [Euler Method](euler-method.md) can be changed to a stable form by replacing $u_{j}^{n}$ with the spatial, average value $\frac{u_{j + 1}^{n} + u_{j - 1}^{n}}{2}$ in time difference (explicit).

$$\begin{equation}
\begin{split}
\frac{u_{j}^{n + 1} - \frac{1}{2}(u_{j + 1}^{n} + u_{j - 1}^{n})}{\Delta t} + c\frac{(u_{j + 1}^{n} - u_{j - 1}^{n})}{2\Delta x} &= 0 \text{, where T.E.: } \mathscr{O}(\Delta t, \frac{(\Delta x)^{2}}{\Delta t}) \\
u_{j}^{n + 1} &= \frac{1}{2}(u_{j + 1}^{n} + u_{j - 1}^{n}) - \frac{v}{2}(u_{j + 1}^{n} + u_{j - 1}^{n}) = \frac{1 - v}{2}u_{j + 1}^{n} + \frac{1 + v}{2}u_{j - 1}^{n} \text{, } v = \frac{c\Delta t}{\Delta x} \dots
\end{split}
\end{equation}$$

This *Lax Method* is **not guaranteed to be consistent** because $\frac{(\Delta x)^{2}}{\Delta t}$ may not go to zero in the limit to zero of $\Delta x$ and $\Delta t$.
If $v$ is held constant, the method becomes #consistent.
When $v \neq 1$, the *Lax Method* has a large #dissipative-error (because #truncation-error RHS has even derivative).

| ![](../../../attachments/engr-704-001-partial-differential-equations/lax_method_amplification_factor_and_relative_phase_error_211119_184405_EST.png) |
|:--:|
| This can be observed in the #amplification-factor, $G = \cos(\beta) - iv\sin(\beta)$ and the #relative-phase-error, $\frac{\phi}{\phi_{e}} = \frac{\tan^{-1}(-v\tan(\beta))}{-\beta v}$. |