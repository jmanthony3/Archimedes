---
title: Mechanical Metallurgy
subject: ENGR 839-001
date: 210823-2112XX
place: DH 3274
speaker: Dr. Mark Atwater
student: Joby M. Anthony III
email: jmanthony1@liberty.edu
---
<!-- output:
  pdf_document:
    latex_engine: xelatex
    includes:
      in_header: "C:/Users/jmanthony1/Documents/GitHub/JobyAnthonyIII/LaTeX/preamble.tex"
bibliography: "biblio.bib"
link-citations: true -->
<!-- %%%%%%%% Document Metadata %%%%%%%% -->
# ENGR 704-001: Partial Differential Equations

- [ENGR 839-001: Mechanical Metallurgy](#engr-839-001-mechanical-metallurgy)
<!-- %%%%%%%%%%%%%%%%%%%%%%%%%%%%%% -->





<!-- START WRITING BELOW -->





<!-- %%%%%%%%%%%%%%%%%%%%%%%%%%%%%% -->
*Lecture: September 24, 2021*
## Chapter 5: Initial-Value Problems for Ordinary Differential Equations

### Euler Method
Solving [[Euler-Method]] in forward (using previous iteration to solve next iteration) gives lower accuracy in quicker time than solving backward (using future information to solve the future iteration), which gives great accuracy in much time.

$$\begin{align*}
\frac{du}{dt} &= f'(t, u), u(t_{0}) = u_{0}, h = t_{k+1} - t_{k} \\
u_{k+1} &= u_{k} + hf'(t_{k}, u_{k})
\end{align*}$$

| ![](../../attachments/engr-704-001-partial-differential-equations/euler_method_graph_example_210924_171911_EST.png) |
|:--:|
| The accuracy for curved functions can be improved with smaller $h$. #fig-euler_method_graph_example |

>**Example** 
![](../../attachments/engr-704-001-partial-differential-equations/euler_method_example_error_210924_172623_EST.png)
First order error proportional to step size. #fig-euler_method_example_error

### Taylor Method
[[Euler-Method]] is simple and easy to implement, but is only first-order. Higher-orders give better accuracy; however, [[Euler-Method]] is only a first-order [[Taylor-approximation]] to solution. $$\begin{align*}u(t_{k+1}) &= u(t_{k} + h) \\ &= u(t_{k}) + h\frac{du}{dt}(t_{k}) + \frac{h^{2}}{2}\frac{d^{2}u}{dt^{2}}(t_{k}) + \frac{h^{3}}{6}\frac{d^{3}u}{dt^{3}}(t_{k}) + \dots\end{align*}$$
The last two terms are the [[truncation-error]]. Defining $\frac{du}{dt} = f'(u, t)$, the second derivative term found by differentiating wrt $t$. $$\begin{align*}\frac{d^{2}u}{dt^{2}} = \frac{d}{dt}\frac{du}{dt} = \frac{d}{dt}f'(t, u) &= \frac{\partial f'}{\partial t}(t, u) + \frac{\partial f'}{\partial t}(t, u)\frac{\partial u}{\partial t} \\ &= \frac{\partial f'}{\partial t}(t, u)\end{align*}$$

>**Example** Solve the [[IVP]] $\frac{du}{dt} = (1 - \frac{4}{3}t)u, u(0) = 1$ using [[Taylor-Method]] and compare to exact solution.

**Drawbacks** [[Taylor-Method]] requires solving complex, partial derivatives. Furthermore, the differential equation must be smooth and continuous. Solving the partial derivatives and multiplications requires much computational power, which introduces much [[round-off-error]].

### Runge-Kutta Method
Higher-order local truncation error of [[Taylor-Method]] eliminates the need to compute derivatives. [[Runge-Kutta-Method]] is also the most popular and powerful *explicit* method to integrate [[ODE]]. $$u_{k+1} = u_{k} + h\sum_{i=1}^{m}c_{i}f'(t_{i, k}, u_{i, k}), f'(t, u) = \frac{du}{dt}$$ #eq-runge_kutta_method Flexibility in designing the method and choosing the coefficients, and order is limited to power of h. The selection of $0 \leq \lambda \leq 1$, choosing $\lambda = 1$, which is [[Euler-Method]], uses information at the next time step to solve the half-steps from the current step.


---


*Lecture: September 24, 2021*
#### RK2
Two Methods for [[RK2]]
1. Improved [[Euler-Method]]: $a = b = \frac{1}{2},~\lambda = 1$
2. Midpoint Method: $a = 0,~b = 1,~\lambda = \frac{1}{2}$

General form for [[RK2]]: 
$$\begin{align*}
u_{k+1} &= u_{k} + h[af'(t_{k}, u_{k}) + bf'(t_{k,2}, u_{k,2})] \\
&= u_{k} + h[af'(t_{k}, u_{k}) + bf'(t_{k} + \lambda h, u_{k} + \lambda hf'(t_{k}, u_{k}))]
\end{align*}$$ #eq-runge_kutta_2_method

#### RK4
$$\begin{align*}
k_{1} &= hf'(t_{k}, u_{k}) \\
k_{2} &= hf'(t_{k} + \frac{h}{2}, u_{k} + \frac{k_{1}}{2}) \\
k_{3} &= hf'(t_{k} + \frac{h}{2}, u_{k} + \frac{k_{2}}{2}) \\
k_{4} &= hf'(t_{k} + h, u_{k} + k_{3}) \\
u_{k+1} &= u_{k} + \frac{1}{6}(k_{1} + 2k_{2} + 2k_{3} + k_{4})
\end{align*}$$ #eq-runge_kutta_4_method

| ![](../../attachments/engr-704-001-partial-differential-equations/rk4_graphical_example_210927_171909_EST.png) |
|:--:|
| The $\frac{1}{6}$ term for averaging out $k^{th}$ points in [[RK4]]. #fig-rk4_graphical_example |

>**Q&A**
Q: What are the units of $k$?
A: Same units as $u$, because $f`$ is only wrt to time.

>**Example** If $\dot{u} = u - t^{2} + 1$, where $u(0) = 0.5$ and $h = 0.2$.
$$\begin{align*}
k_{1} &= hf'(t_{k}, u_{k}) = 0.2f'(0, 0.5) \\
&= 0.2(1.5) = 0.3 \\
k_{2} &= hf'(t_{k} + \frac{h}{2}, u_{k} + \frac{k_{1}}{2}) = 0.2f'(0.1, 0.65) \\
&= 0.328 \\
k_{3} &= hf'(t_{k} + \frac{h}{2}, u_{k} + \frac{k_{2}}{2}) = 0.2f'(0.1, 0.664) \\
&= 0.3308 \\
k_{4} &= hf'(t_{k} + h, u_{k} + k_{3}) = 0.2f'(0.1, 0.8308) \\
&= 0.35816 \\
u_{k+1} &= u_{k} + \frac{1}{6}(k_{1} + 2k_{2} + 2k_{3} + k_{4}) \\
&= 0.5 + \frac{1}{6}[0.3 + 2(0.328) + 2(0.3308) + 0.35816] \\
&= 0.8292933
\end{align*}$$
![](../../attachments/engr-704-001-partial-differential-equations/rk4_example_solution_210927_174230_EST.png)
bar #fig-rk4_example_solution
![](../../attachments/engr-704-001-partial-differential-equations/rk4_example_solution_error_comparison_210927_174336_EST.png)
bar #fig-rk4_example_solution_error_comparison

### Implicit Methods
#### Backward Euler
Explicit methods are well suited to handle large class of [[ODE]]. However, these methods perform poorly for class of "stiff" equations that occur frequently in real problems: e.g. exponential functions in vibrational motion. If there is a large difference between the most rapid and slowest changes in solution components, then the system is a [[stiff-equation]]. If [[RK4]] requires small time step for sufficient accuracy, then that problem is likely involved with a [[stiff-equation]]. Implicit methods are generally suited to a [[stiff-equation]] since they are conditionally "stable": i.e. required limitation on time stepping; otherwise, solution will diverge and crash.

>Multiple choice: Euler-method is first order O(h2). Forward and backward formulations are both first order. Backward has more error than forward, but more stable.

| ![](../../attachments/engr-704-001-partial-differential-equations/difference_between_explicit_implicit_euler_method_210927_175502_EST.png) |
|:--:|
| $u_{k+1} = u_{k} + hf'(t_{k}, u_{k})$ versus $u_{k+1} = u_{k} + hf'(t_{k+1}, u_{k+1})$ #fig-difference_between_explicit_implicit_euler_method |


---


*Lecture: September 29, 2021*
We can use the [[Newton-Raphson]], [[root-finding]] method to solve the unknown, $u_{k+1}$ from the unknown, $u_{k+11}$.

>**Example** Solve the [[IVP]], $\frac{du}{dt} = e^{u},~u(0) = 1,~h = 0.1$ using backward [[Euler-Method]].
$$\begin{align*}
u_{k+1} &= u_{k} + hf'(t_{k+1}, u_{k+1}) \\
&= u_{k} + he^{u_{k+1}} \\
F(u_{k+1}) &= u_{k+1} - he^{u_{k+1}} - u_{k} = 0 \\
F'(u_{k+1}) &= 1 - he^{u_{k+1}} = 0 \\
u_{k+1}^{n+1} &= u_{k+1}^{n} - \frac{F(u_{k+1}^{n})}{F'(u_{k+1}^{n})}
\end{align*}$$
**KNOW THIS FOR EXAM!!!**

#### Trapezoidal Method
This is a **second-order** method and sometimes called the "[[Crank-Nicholson]]" in [[PDE]] contexts. This method is derived from the trapezoidal integration rule using half contributions at current and future points. $$u_{k+1} = u_{k} + \frac{1}{2}h[f'(t_{k}, u_{k}) + f'(t_{k+1}, u_{k+1})]$$ Or a more a generalized form:

$$u_{k+1} = u_{k} + h[(1 - \theta)f'(t_{k}, u_{k}) + \theta f'(t_{k+1}, u_{k+1})]$$ #eq-implicit_trapezoidal_method

where, $$\theta = \begin{cases}
1 &, Backward Euler \\
-1 &, Forward Euler \\
0.5 &, Trapezoidal
\end{cases}$$

>**Q: What is the difference between *Trapezoidal* and *Improved Euler* methods?** <cite> Dr. Cho
*A: Improved Euler is still explicit, which uses a guess for the next iteration. Trapezoid uses next iteration information.*

>**Q: What is the benefit of using *Trapezoid* compared to *Backward Euler*?** <cite> Dr. Cho
*A: Trapezoid will be more accurate, because it is second-order. [[Euler-Method]] is first-order.*


---


*Lecture: October 1, 2021*
>**EXAM**: Bring one formula sheet for closed-book, in-class exam! Exam after covering the [[finite-element-method]], which may likely be next week.

>**Example** Solve the first [[Newton-Raphson]] iteration for $u_{k+1} = u_{k} + \frac{1}{2}h(e^{u_{k}} + e^{u_{k+1}}),~u_{0} = 1,~h = 0.1$.

#### Multistep Methods
We may use more accurate, previous information to approximate next grid's solution.

Multistep Methods
: Methods using more than one grid point to approximate next grid point.

[[Adam-Bashforth]] technique
: A $4^{th}$-order **explicit** method. $$\begin{align*}
u_{k+1} &= u_{k} \\
&+ \frac{h}{24}[55f'(t_{k}, u_{k}) - 59f'(t_{k- 1}, u_{k - 1}) + 37f'(t_{k - 2}, u_{k - 2}) - 9f'(t_{k - 3}, u_{k - 3})]
\end{align*}$$ #eq-adam_bashforth

[[Adam-Moulton technique]]
: A $4^{th}$-order **implicit** method.

In general, an implicit method has better stability and accuracy than explicit methods. Why? Because implicit methods use more information of the data. When linear, the equation can be algebraically solved...

>**Example** Solve [[IVP]] $\dot{u} = e^{u}$.

#### Predictor-Corrector Methods
[[Newton-Raphson]] (or secant) method complicates procedure and increases computational cost. We can use combination of explicit and implicit to predict and improve solve.

#### Stiff Differential Equations
Some diffeqs' error grows very rapidly for larger step sizes, which dominate the calculations. Many physical problems are involved with a [[stiff-equation]]. [[stiff-equation]] equations appear when they have an **exponential (with large, negative coefficients) forms in their solutions**.

>**Example** Low temperature, high strain-rate [[ISV]] equations are very much so [[stiff-equation]]s.

>**Example** Consider this linear, [[IVP]], $\frac{du}{dt} = -250u,~u(0) = 1$. The exact solution is $\dot{u} = e^{-250t}$ and $u(1) \approx 2.69e-109$. Comparing this against [[Euler-Method]] (either improved or not) and [[RK4]]:
![](../../attachments/engr-704-001-partial-differential-equations/stiff_differential_equation_method_comparisons_211001_173918_EST.png)
Large step size, i.e. large errors, dominate final solution. #fig-stiff_differential_equation_method_comparisons |

>**Example** Consider the [[IVP]], $\frac{du}{dt} = \gamma u,~u(0) = 1$ with exponential solution, $u(t) = e^{\gamma t}$.
Using a forward [[Euler-Method]],
$$\begin{align*}
u_{k+1} &= u_{k} + \gamma hu_{k} = (1 + \gamma h)u_{k} \\
&= (1 + \gamma h)^(k + 1)u_{0} = (1 + \gamma h)^{k + 1}
\end{align*}$$
The absolute error (exact - approximation) goes to zero:
$$E = |u_{k}(kh) - (1 - \gamma h)^{k}| = |(e^{\gamma h})^{k} - (1 + \gamma h)^{k}|$$
$$|1 + \gamma h| < 1 \implies -2<\gamma h < 0$$
When $\gamma < 0$, exact solution decays to $0$. When large, method diverges quickly with error growing. When large, step-size, $h$ must be very small. [[Euler-Method]] is expected to be stable only if $h < \frac{2}{|\gamma|}$. If $h$ satisfies this, then method converges, because error goes to $0$; otherwise, solution diverges, because error grows quickly.

In general, a function, $Q$ approximated by difference methods gives, $$u_{k + 1} = Q(\gamma h)u_{k}$$, where the error grows without bound if $|Q(\gamma h)| > 1$. $n^{th}$-order [[Taylor-Method]] has a stability condition, provided $h$ is chosen to satisfy: $$|1 + h\gamma + \frac{1}{2}\gamma^{2}h^{2} + \dots + \frac{1}{n}h^{n}\gamma^{n}| < 1$$ Stability analysis is generally very difficult to solve: heavily relies on mathematics.

Region, $R$ of absolute stability
: for a one-step method is $$R = \{h\gamma \in C:|Q(\gamma h)| < 1\}$$.

[[A-stable]] method
: The region of absolute stability contains entire, left half-plane of $\gamma h$ for $\gamma < 0$ on the complex plane, $\mathbi{I}$. Likely named for the absolute value property.

Forward [[Euler-Method]] is conditionally stable: $$|1 + \gamma h| < 1,~h<\frac{2}{|\gamma|},~\text{for}~\gamma < 0,~h < \frac{-2}{\gamma}$$ The region of stability...

| ![](../../attachments/engr-704-001-partial-differential-equations/a_stable_method_example_of_forward_euler_211001_175330_EST.png) |
|:--:|
| The region of stability, $\gamma h = z,~abs(1 + z) < 1$. **This is not [[A-stable]] method**, because the stability region is not entire, left half-plane. Stability is limited by step size, $h$. #fig-a_stable_method_example_of_forward_euler |

>**Q: Only called [[A-stable]] when left plane?** <cite> Reid Prichard
*A: Correct. The [[Crank-Nicholson]] is implicit and [[A-stable]].*


---


*Lecture: October 04, 2021*
Will discuss **Midterm Exam** Wednesday.

>**Q: When do we exit the *Conjugate Gradient* methods?** <cite> Bethany
*A: Method is a direct solver, but certainly may require more iterations to get within tolerance. Looking for experiment with various inputs and error handling.*

Implicit [[Trapezoidal-Method]] is the **only [[A-stable]], multistep method**!
$$\begin{align*}
u_{k+1} &= u_{k} + \frac{1}{2}h[\gamma u_{k} + \gamma u_{k+1}] \\
&= \frac{1 + \frac{1}{2}h\gamma}{1 - \frac{1}{2}h\gamma}u_{k}
\end{align*}$$
If $\gamma > 0$, then error exponentially grows. If $\gamma < 0$, then error does not grow with condition, $h < \frac{-2}{\gamma}$.

| ![](../../attachments/engr-704-001-partial-differential-equations/a_stable_method_example_of_implicit_trapezoidal_211004_172442_EST.png) |
|:--:|
| $abs()$ #fig-a_stable_method_example_of_implicit_trapezoidal |

##### Summary
- [[A-stable]] not affected by stiffness of [[ODE]].
- No explicit [[Runge-Kutta-Method]] is [[A-stable]].
- Implicit [[Trapezoidal-Method]] is simplest example of [[A-stable]], multistep method.
- Although the [[Trapezoidal-Method]] does give accurate approximations for large step sizes, its error will not grow exponentially.
- Techniques commonly used for [[stiff-equation]] will likely be implicit, multi-step methods.
- In most cases, $u_{k + 1}$ is obtained from non-linear equations; therefore, [[Newton-Raphson]] is typically used.

>Stability does not ensure accuracy. <cite> Dr. Cho

>**Know how to solve [[RK4]] for the exam!** <cite> Dr. Cho


---


*Lecture: October 06, 2021*
**Exam October 20, 2021 with review on the 18$^{th}$. HW2 assigned after that.**
## Boundary Value Problems in ODE
>**Example** A bridge that is fixed at both ends, find the height of the curvature.

Discuss approximation to [[BVP]] with conditions imposed at different points. First-order differential equations only require one condition. However, physical problems that are position-dependent rather than time-dependent are often described in terms of differential equations with conditions imposed at more than one point. Two-point [[BVP]] involve a second-order differential equation, which is generally of the form: $$\frac{d^{2}y}{dx^{2}} = y'' = f(x, y, y'),~a \leq x \leq b$$ and $y(a) = \alpha, y(b) = \beta$.

### Shooting Method
#### Linear Shooting Method
Let's consider a generalized, second-order diffeq: $$y'' = p(x)y' + q(x)y + r(x),~\text{for}~a \leq x \leq b$$ and $y(a) = \alpha,~y(b) = \beta$. To approximate unique solution, consider two initial problems:
$$\begin{align*}
y'' &= p(x)y' + q(x)y + r(x) &,~a \leq x \leq b &,~y(a) = \alpha &,~y'(a) = z1 \\
y'' &= p(x)y' + q(x)y &,~a \leq x \leq b &,~y(a) = 0 &,~y'(a) = z2
\end{align*}$$
The solutions of the two problems are denoted $y_{1}(x)$ and $y_{2}(x)$, where $z1$ and $z2$ are commonly $0$ and $1$, respectively.

| ![](../../attachments/engr-704-001-partial-differential-equations/linear_shooting_method_graph_rep_211006_173206_EST.png) |
|:--:|
| $y(x) = y_{1}(x) + \frac{\beta - y_{1}(b)}{y_{2}(b)}y_{2}(x)$ interpolates between two [[IVP]], $y_{1}(x)$ and $y_{2}(x)$. #fig-linear_shooting_method_graph_rep |

If we restrict, $y_{2}(b) \neq 0$, then the solution can be written as: $y(x) = y_{1}(x) + \frac{\beta - y_{1}(b)}{y_{2}(b)}y_{2}(x)$, where the equation interpolations between $y_{1}(x)$ as solution to $y'' = p(x)y' + q(x)y + r(x)$ and $y_{2}(x)$ as solution to $y'' = p(x)y' + q(x)y$. First and second derivatives follow as:
$$\begin{align*}
y'(x) &= y_{1}'(x) + \frac{\beta - y_{1}(b)}{y_{2}(b)}y_{2}'(x) \\
y''(x) &= y_{1}''(x) + \frac{\beta - y_{1}(b)}{y_{2}(b)}y_{2}''(x)
\end{align*}$$

>**Q: Is this root-bracketed?** <cite> Reid
*A: Next slide.*

If we substitute into $y''(x)$, then:
$$\begin{align*}
y''(x) &= y_{1}''(x) + \frac{\beta - y_{1}(b)}{y_{2}(b)}y_{2}''(x) \\
  &= p(x)y_{1}' + q(x)y_{1} + r(x)\frac{\beta - y_{1}(b)}{y_{2}(b)}(p(x)y_{2}' + q(x)y_{2}) \\
  &= p(x)(y_{1}' + \frac{\beta - y_{1}(b)}{y_{2}(b)}y_{2}') + q(x)(y_{1} + \frac{\beta - y_{1}(b)}{y_{2}(b)}y_{2}) + r(x) \\
  &= p(x)y'(x) + q(x)y(x) + r(x)
\end{align*}$$

>**Q: Is this like the bisection method?** <cite> Daniel K.
*A: This is not an iterative, [[root-finding]] problem. This interpolates between two, real solutions.*

The boundary conditions must satisfy:
$$\begin{align*}
y(a) &= y_{1}(a) + \frac{\beta - y_{1}(b)}{y_{2}(b)}y_{2}(a) = \alpha + \frac{\beta - y_{1}(b)}{y_{2}(b)}*0 = \alpha \\
&\dots
\end{align*}$$

>**Q: Why guess at the derivatives? Does this make it easier to solve?** <cite> Reid
*A: Certainly experiment with the guesses.*

- [[Linear-Shooting-Method]] uses two [[IVP]]
- The solutions to [[IVP]] are $y_{1}(x)$ and $y_{2}(x)$.
- These [[IVP]] are solved by typical [[ODE]] solvers.

>**Example** Apply [[Linear-Shooting-Method]] to [[BVP]]: $u'' = y'' = -\frac{2}{x}y' + \frac{2}{x^{2}}y + \frac{sin(ln(x))}{x^{2}}$, for $1 \leq x \leq 2$ if $y(1) = 1$, $y(2) = 2$, and $h = 0.1$.
First make first-order [[ODE]]: $y_{1} = u$, $u(1) = 1$, $T(1) = 0$. Therefore, $u' = T$ into $y_{1}$ and $T' = -\frac{2}{x} + \frac{2}{x^{2}}u + \frac{sin(ln(x))}{x^{2}}$ into $y_{2}$, and use forward [[Euler-Method]] to solve these equations. $$\begin{align*} u_{n + 1} &= u_{n} + hf_{1}(T_{n}) \\ t_{n + 1} &= T_{n} + hf_{2}(x_{n}, u_{n}, T_{n})\end{align*}$$. *Here, $h$ is physical spacing, not time increment.* At $n = 0$, set $x_{0} = 1.0$, then: $$\begin{bmatrix}u_{1} \\ T_{1}\end{bmatrix} = \begin{bmatrix}u_{0} \\ T_{0}\end{bmatrix} + h\begin{bmatrix}\end{bmatrix}\dots$$