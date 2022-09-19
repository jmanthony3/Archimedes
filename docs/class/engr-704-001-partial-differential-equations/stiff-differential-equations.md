# Stiff Differential Equations

Some diffeqs' error grows very rapidly for larger step sizes, which dominate the calculations.
Many physical problems are involved with a stiff equation.
Stiff equations appear when they have an **exponential (with large, negative coefficients) forms in their solutions**.

!!! note Low temperature, high #strain-rate #ISV equations are very much so stiff equations.

*[ISV]: Internal State Variable

!!! example Consider this linear, #IVP, $\frac{du}{dt} = -250u,~u(0) = 1$. The exact solution is $\dot{u} = e^{-250t}$ and $u(1) \approx 2.69e-109$. Comparing this against [Euler Method](euler-method.md) (either #Improved-Euler-Method or not) and [RK4](engr-704-001-partial-differential-equations/runge-kutta-method.md#rk4):
    | ![](../../../attachments/engr-704-001-partial-differential-equations/stiff_differential_equation_method_comparisons_211001_173918_EST.png) |
    |:--:|
    | Large step size, i.e. large errors, dominate final solution. |

!!! example Consider the #IVP, $\frac{du}{dt} = \gamma u,~u(0) = 1$ with exponential solution, $u(t) = e^{\gamma t}$.
    Using a [Forward](forward-euler.md) [Euler Method](euler-method.md),
    $$\begin{split}
    u_{k+1} &= u_{k} + \gamma hu_{k} = (1 + \gamma h)u_{k} \\\\
    &= (1 + \gamma h)^(k + 1)u_{0} = (1 + \gamma h)^{k + 1}
    \end{split}$$
    The absolute error (exact - approximation) goes to zero:
    $$E = |u_{k}(kh) - (1 - \gamma h)^{k}| = |(e^{\gamma h})^{k} - (1 + \gamma h)^{k}|$$
    $$|1 + \gamma h| < 1 \implies -2<\gamma h < 0$$
    When $\gamma < 0$, exact solution decays to $0$.
    When large, method diverges quickly with error growing.
    When large, step-size, $h$ must be very small.
    [Euler Method](euler-method.md) is expected to be stable only if $h < \frac{2}{|\gamma|}$.
    If $h$ satisfies this, then method converges, because error goes to $0$; otherwise, solution diverges, because error grows quickly.

In general, a function, $Q$ approximated by difference methods gives, $$u_{k + 1} = Q(\gamma h)u_{k}$$, where the error grows without bound if $|Q(\gamma h)| > 1$.
$n^{th}$-order [Taylor Method](taylor-method.md) has a #stability-condition, provided $h$ is chosen to satisfy: $$|1 + h\gamma + \frac{1}{2}\gamma^{2}h^{2} + \dots + \frac{1}{n}h^{n}\gamma^{n}| < 1$$
#stability-analysis is generally very difficult to solve: heavily relies on mathematics.

[Region, $R$ of absolute stability](region-of-absolute-stability.md)
: for a one-step method is $$R = \{h\gamma \in C:|Q(\gamma h)| < 1\}$$

[A-Stable Method](a-stable-method.md)
: The region of absolute stability contains entire, left half-plane of $\gamma h$ for $\gamma < 0$ on the complex plane, $\mathbb{Z}$.
Likely named for the absolute value property.

!!! question Only called [A-stable](a-stable-method.md) when left plane? <cite>#Reid-Prichard
    Correct.
    The [Crank-Nicholson Method](trapezoidal-crank-nicholson-method.md) is implicit and [A-stable](a-stable-method.md).

!!! note
    Implicit [Trapezoidal Method](trapezoidal-crank-nicholson-method.md) is the **only [A-stable](a-stable-method.md), [multistep method](multistep-methods.md)**!

$$\begin{split}
u_{k+1} &= u_{k} + \frac{1}{2}h[\gamma u_{k} + \gamma u_{k+1}] \\\\
&= \frac{1 + \frac{1}{2}h\gamma}{1 - \frac{1}{2}h\gamma}u_{k}
\end{split}$$

If $\gamma > 0$, then error exponentially grows.
If $\gamma < 0$, then error does not grow with condition, $h < \frac{-2}{\gamma}$.

| ![](../../../attachments/engr-704-001-partial-differential-equations/a_stable_method_example_of_implicit_trapezoidal_211004_172442_EST.png) |
|:--:|
| $abs()$ |