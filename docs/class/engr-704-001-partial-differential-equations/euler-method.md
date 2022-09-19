# Euler Method

## Forward
Solving *Euler Method* in forward (using previous iteration to solve next iteration) gives lower accuracy in quicker time than solving backward (using future information to solve the future iteration), which gives great accuracy in much time.

Forward Euler
: is expected to be stable only if $h < \frac{2}{|\gamma|}$.
If $h$ satisfies this, then method converges, because error goes to $0$; otherwise, solution diverges, because error grows quickly.
$$\begin{equation}
\begin{split}
\frac{du}{dt} &= f'(t, u), u(t_{0}) = u_{0}, h = t_{k+1} - t_{k} \\
u_{k+1} &= u_{k} + hf'(t_{k}, u_{k})
\end{split}
\end{equation}$$

| ![](../../../attachments/engr-704-001-partial-differential-equations/euler_method_graph_example_210924_171911_EST.png) |
|:--:|
| The accuracy for curved functions can be improved with smaller $h$. |

!!! example
    | ![](../../../attachments/engr-704-001-partial-differential-equations/euler_method_example_error_210924_172623_EST.png) |
    |:--:|
    | First order error proportional to step size. |



## Backward
Explicit methods are well suited to handle large class of #ODE.
However, these methods perform poorly for class of ["stiff" equations](stiff-differential-equations.md) that occur frequently in real problems: e.g. exponential functions in vibrational motion.
If there is a large difference between the most rapid and slowest changes in solution components, then the system is a [stiff equation](stiff-differential-equations.md).
If [RK4](engr-704-001-partial-differential-equations/runge-kutta-method.md#rk4) requires small time step for sufficient accuracy, then that problem is likely involved with a [stiff equation](stiff-differential-equations.md).
Implicit methods are generally suited to a [stiff equation](stiff-differential-equations.md) since they are conditionally "stable": i.e. required limitation on time stepping; otherwise, solution will diverge and crash.

> Multiple choice: Euler Method is first order $\mathscr{O}(h^{2})$.
Forward and backward formulations are both first order.
Backward has more error than forward, but more stable.

| ![](../../../attachments/engr-704-001-partial-differential-equations/difference_between_explicit_implicit_euler_method_210927_175502_EST.png) |
|:--:|
| $u_{k+1} = u_{k} + hf'(t_{k}, u_{k})$ versus $u_{k+1} = u_{k} + hf'(t_{k+1}, u_{k+1})$ |

We can use the #NR, #root-finding method to solve the unknown, $u_{k+1}$ from the unknown, $u_{k+1}$.

*[NR]: Newton-Raphson