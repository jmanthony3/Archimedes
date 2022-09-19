# Consistency

An FDE is said to be consistent if, in the limit of vanishing mesh and time spacing size, $h$, the FDE approaches the #PDE:
$$\underset{h \rightarrow 0}{\lim}(pde - fde) = \underset{h \rightarrow 0}{\lim}(T.E.) = 0$$
Generally, it is true for most of problems; however, there may be some cases where it isn't.

!!! example #DuFort-Frankel-Method for #parabolic heat equation:
    $$\frac{u_{j}^{n + 1} - u_{j}^{n - 1}}{2\Delta t} = \frac{\alpha}{(\Delta x)^{2}}\bigg(u_{j + 1}^{n} - u_{j}^{n + 1} - u_{j}^{n - 1} + u_{j - 1}^{n}\bigg) + \frac{\alpha}{12}\frac{\partial^{4}u}{\partial x^{4}}(\Delta x)^{2} - \frac{\partial^{2}u}{\partial t^{2}}\overbrace{\cancel{\bigg(\frac{\Delta t}{\Delta x}\bigg)^{2}}}^{r^{2}} - \frac{1}{6}\frac{\partial^{3}u}{\partial t^{3}}(\Delta t)^{2}$$
    This method will be consistent if $\underset{\Delta x, \Delta t \rightarrow 0}{\lim}(\frac{\Delta t}{\Delta x}) = 0$ (strange...).
    But, what if $\Delta x$ and $\Delta t$ approach zero at an equal rate: $\frac{\Delta t}{\Delta x} = \gamma$.
    Then this method becomes consistent with the following #hyperbolic equation:
    $$\frac{\partial u}{\partial t} + \alpha\gamma^{2}\frac{\partial^{2}u}{\partial t^{2}} = \alpha\frac{\partial^{2}u}{\partial x^{2}}$$