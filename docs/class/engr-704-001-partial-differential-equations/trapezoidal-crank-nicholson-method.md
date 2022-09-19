# Trapezoidal (Crank-Nicholson) Method

This is a **second-order** method and sometimes called the "#Crank-Nicholson" in #PDE contexts.
This method is derived from the trapezoidal integration rule using half contributions at current and future points.
$$u_{k+1} = u_{k} + \frac{1}{2}h[f'(t_{k}, u_{k}) + f'(t_{k+1}, u_{k+1})]$$
Or a more a generalized form:
$$\begin{equation}
u_{k+1} = u_{k} + h[(1 - \theta)f'(t_{k}, u_{k}) + \theta f'(t_{k+1}, u_{k+1})]
\end{equation}$$
where, $$\theta = \begin{cases}
1 &, \text{Backward Euler} \\
-1 &, \text{Forward Euler} \\
0.5 &, \text{Trapezoidal}
\end{cases}$$

*[PDE]: Partial Differential Equations


!!! question What is the difference between *Trapezoidal* and *Improved Euler* methods? <cite> Dr. Cho
    #Improved-Euler-Method is still explicit, which uses a guess for the next iteration.
    Trapezoid uses next iteration information.

!!! question What is the benefit of using *Trapezoid* compared to *[Backward Euler](backward-euler-method.md)*? <cite> Dr. Cho
    Trapezoid will be more accurate, because it is second-order.
    [Euler Method](euler-method.md) is first-order.