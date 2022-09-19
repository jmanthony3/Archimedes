# Distortion Energy Theory: von Mises
Yielding occurs when the *distortion strain energy* per unit volume reaches the distortion strain energy per unit volume for yield in simple tension or compression of the same material.

!!! warning Limiting Assumptions
    Failure criterion does not account for [plasticity](../engr-839-001-mechanical-metallurgy/plasticity.md)!

[von Mises Failure Criterion](von-mises-failure-criterion.md)
: ~$$\begin{equation}
f(\sigma_{1}, \sigma_{2}, \sigma_{3}) = \frac{1}{6}[(\sigma_{1} - \sigma_{2})^{2} + (\sigma_{2} - \sigma_{3})^{2} + (\sigma_{1} - \sigma_{3})^{2}] = \frac{1}{3}\sigma_{yp}^{2}
\end{equation}$$

If $\sigma_{eq} = \sqrt{\frac{1}{2}(\sigma_{1} - \sigma_{2})^{2} + (\sigma_{2} - \sigma_{3})^{2} + (\sigma_{2} - \sigma_{3})^{2}} > \sigma_{yp}$, then yielding is predicted.