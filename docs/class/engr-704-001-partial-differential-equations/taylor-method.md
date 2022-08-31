# Taylor Method

[[euler-method]] is simple and easy to implement, but is only first-order.
Higher-orders give better accuracy; however, [[euler-method]] is only a first-order #Taylor-Approximation to solution.

$$\begin{split}
u(t_{k+1}) &= u(t_{k} + h) \\\\
 &= u(t_{k}) + h\frac{du}{dt}(t_{k}) + \frac{h^{2}}{2}\frac{d^{2}u}{dt^{2}}(t_{k}) + \frac{h^{3}}{6}\frac{d^{3}u}{dt^{3}}(t_{k}) + \dots
\end{split}$$

The last two terms are the #truncation-error.
Defining $\frac{du}{dt} = f'(u, t)$, the second derivative term found by differentiating wrt $t$.
$$\begin{split}\frac{d^{2}u}{dt^{2}} = \frac{d}{dt}\frac{du}{dt} = \frac{d}{dt}f'(t, u) &= \frac{\partial f'}{\partial t}(t, u) + \frac{\partial f'}{\partial t}(t, u)\frac{\partial u}{\partial t} \\\\ &= \frac{\partial f'}{\partial t}(t, u)\end{split}$$

*[wrt]: with respect to

!!! example
    Solve the #IVP $\frac{du}{dt} = (1 - \frac{4}{3}t)u, u(0) = 1$ using #Taylor-Method and compare to exact solution.

*[IVP]: Initial Value Problem

**Drawbacks** #taylor-method requires solving complex, partial derivatives.
Furthermore, the differential equation must be smooth and continuous.
Solving the partial derivatives and multiplications requires much computational power, which introduces much [[round-off-error]].