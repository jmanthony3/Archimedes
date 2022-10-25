# Stability

For a consistent numerical scheme to be convergent, a required property is stability.
A stable numerical scheme is one for which errors from any source (#round-off-error, #truncation-error, mistakes, etcetera) are not permitted to grow as the computation proceeds from one marching step to the next.

- Strictly only applicable for #marching problems.
- #Fourier-Stability-Analysis (a.k.a. [von-Neumann Stability Analysis](stability-analysis.md#von-neumann)

Can use the central-time difference scheme for heat equation:
$$\frac{u_{j}^{n + 1} - u_{j}^{n - 1}}{2\Delta t} = \frac{\alpha}{(\Delta x)^{2}}\bigg(i_{j + 1}^{n} - 2u_{j}^{n} + u_{j - 1}^{n}\bigg) + \mathscr{O}(\Delta t^{2}, \Delta x^{2})$$
This method is #unconditionally-unstable even though the error term has higher orders: will not converge.
Sometimes an #unstable method can be identified with physical implausibility because #unstable numerical procedures cause unacceptable modeling of the problem.

!!! attention
    Perform this [stability analysis](stability-analysis.md) in project.

A simple, explicit scheme would be #stable only if $r = \bigg[\frac{\alpha\Delta t}{(\Delta x)^{2}}\bigg] \leq \frac{1}{2}$.
Let's consider an explicit method for the heat equation:
$$\frac{u_{j}^{n + 1} - u_{j}^{n}}{\Delta t} = \frac{\alpha}{(\Delta x)^{2}}\bigg(u_{j + 1}^{n} - 2u_{j}^{n} + u_{j - 1}^{n}\bigg) \rightarrow u_{j}^{n + 1} = r(u_{j + 1}^{n} + u_{j - 1}^{n}) + (1 - 2r)u_{j}^{n}$$
If $r = 1$ (i.e. #unstable), then the temperature on grid point, $j$ will be $200\degreeC$ which is physically impossible because the temperatures of surrounding grid points are $100\degreeC$.

| ![](../../../attachments/engr-704-001-partial-differential-equations/stability_example_211108_183309_EST.png) |
|:--:|
| Neighboring grid points cannot be spontaneously different in temperature. |