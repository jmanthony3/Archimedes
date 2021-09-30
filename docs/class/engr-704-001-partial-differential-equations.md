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
| ![](../../attachments/engr-704-001-partial-differential-equations/euler_method_example_error_210924_172623_EST.png) |
|:--:|
| First order error proportional to step size. #fig-euler_method_example_error |

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
| ![](../../attachments/engr-704-001-partial-differential-equations/rk4_example_solution_210927_174230_EST.png) |
|:--:|
| bar #fig-rk4_example_solution |
| ![](../../attachments/engr-704-001-partial-differential-equations/rk4_example_solution_error_comparison_210927_174336_EST.png) |
|:--:|
| bar #fig-rk4_example_solution_error_comparison |

### Implicit Methods
#### Backward Euler
Explicit methods are well suited to handle large class of [[ODE]]. However, these methods perform poorly for class of "stiff" equations that occur frequently in real problems: e.g. exponential functions in vibrational motion. If there is a large difference between the most rapid and slowest changes in solution components, then the system is a [[stiff-equation]]. If [[RK4]] requires small time step for sufficient accuracy, then that problem is likely involved with a [[stiff-equation]]. Implicit methods are generally suited to a [[stiff-equation]] since they are conditionally "stable": i.e. required limitation on time stepping; otherwise, solution will diverge and crash.

>Multiple choice: Euler-method is first order O(h2). Forward and backward formulations are both first order. Backward has more error than forward, but more stable.

| ![](../../attachments/engr-704-001-partial-differential-equations/difference_between_explicit_implicit_euler_method_210927_175502_EST.png) |
|:--:|
| $u_{k+1} = u_{k} + hf'(t_{k}, u_{k})$ versus $u_{k+1} = u_{k} + hf'(t_{k+1}, u_{k+1})$ #fig-difference_between_explicit_implicit_euler_method |


---


*Lecture: September 29, 2021*
We can use [[Newton-Raphson]], [[root-finding]] method to solve the unknown, $u_{k+1}$ from the unknown, $u_{k+11}$.

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