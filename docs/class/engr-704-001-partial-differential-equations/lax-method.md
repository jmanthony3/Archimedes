# Lax Method

$$\begin{equation}
\begin{split}
\frac{u_{j}^{n + 1} - \frac{1}{2}(u_{j + 1}^{n} + u_{j - 1}^{n})}{\Delta t} + c\frac{(u_{j + 1}^{n} - u_{j - 1}^{n})}{2\Delta x} &= 0 \text{, where T.E.: } \converge{\Delta t, \frac{(\Delta x)^{2}}{\Delta t}} \\
u_{j}^{n + 1} &= \frac{1}{2}(u_{j + 1}^{n} + u_{j - 1}^{n}) - \frac{v}{2}(u_{j + 1}^{n} + u_{j - 1}^{n}) = \frac{1 - v}{2}u_{j + 1}^{n} + \frac{1 + v}{2}u_{j - 1}^{n} \text{, } v = \frac{c\Delta t}{\Delta x} \dots
\end{split}
\end{equation}$$