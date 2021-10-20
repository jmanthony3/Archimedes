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

<script type='text/javascript'
	src='https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.0/MathJax.js?config=TeX-AMS_CHTML'>
</script>
<script type='text/x-mathjax-config'>
	MathJax.Ajax.config.path['Extra'] = 'https://jmanthony3.github.io/Codes/MathJax/extensions/TeX',
MathJax.Hub.Config({
		TeX: {
			equationNumbers: {
				autoNumber: 'AMS'
			},
			extensions: [
				'[Extra]/Taylor.js',
				'[Extra]/NumericalMethods.js'
			]
		},
		tex2jax: {
			inlineMath: [['$', '$'], ['\\(', '\\)']],
			blockMath: [['$$', '$$'], ['\\[', '\\]']]
		},
	});
</script>
<!-- %%%%%%%% Document Metadata %%%%%%%% -->
# ENGR 704-001: Partial Differential Equations

- [ENGR 704-001: Partial Differential Equations](#engr-704-001-partial-differential-equations)
	- [Chapter 5: Initial-Value Problems for Ordinary Differential Equations](#chapter-5-initial-value-problems-for-ordinary-differential-equations)
		- [Euler Method](#euler-method)
		- [Taylor Method](#taylor-method)
		- [Runge-Kutta Method](#runge-kutta-method)
			- [RK2](#rk2)
			- [RK4](#rk4)
		- [Implicit Methods](#implicit-methods)
			- [Backward Euler](#backward-euler)
			- [Trapezoidal Method](#trapezoidal-method)
			- [Multistep Methods](#multistep-methods)
			- [Predictor-Corrector Methods](#predictor-corrector-methods)
			- [Stiff Differential Equations](#stiff-differential-equations)
				- [Summary](#summary)
	- [Boundary Value Problems in ODE](#boundary-value-problems-in-ode)
		- [Shooting Method](#shooting-method)
			- [Linear Shooting Method](#linear-shooting-method)
		- [Finite Difference Method](#finite-difference-method)
		- [Finite Element Method](#finite-element-method)
<!-- %%%%%%%%%%%%%%%%%%%%%%%%%%%%%% -->





<!-- START WRITING BELOW -->





<!-- %%%%%%%%%%%%%%%%%%%%%%%%%%%%%% -->
*Lecture: September 24, 2021*
## Chapter 5: Initial-Value Problems for Ordinary Differential Equations

### Euler Method
Solving [[Euler-Method]] in forward (using previous iteration to solve next iteration) gives lower accuracy in quicker time than solving backward (using future information to solve the future iteration), which gives great accuracy in much time.

$$\begin{equation}
\begin{split}
\frac{du}{dt} &= f'(t, u), u(t_{0}) = u_{0}, h = t_{k+1} - t_{k} \\\\
u_{k+1} &= u_{k} + hf'(t_{k}, u_{k})
\end{split}
\label{eq:forward_euler}
\end{equation}$$

| ![](../../attachments/engr-704-001-partial-differential-equations/euler_method_graph_example_210924_171911_EST.png) |
|:--:|
| The accuracy for curved functions can be improved with smaller $h$. $\label{fig:euler_method_graph_example}$ |

>**Example
![](../../attachments/engr-704-001-partial-differential-equations/euler_method_example_error_210924_172623_EST.png)
First order error proportional to step size. $\label{fig:euler_method_example_error}$

### Taylor Method
[[Euler-Method]] is simple and easy to implement, but is only first-order. Higher-orders give better accuracy; however, [[Euler-Method]] is only a first-order [[Taylor-approximation]] to solution. $$\begin{split}u(t_{k+1}) &= u(t_{k} + h) \\\\ &= u(t_{k}) + h\frac{du}{dt}(t_{k}) + \frac{h^{2}}{2}\frac{d^{2}u}{dt^{2}}(t_{k}) + \frac{h^{3}}{6}\frac{d^{3}u}{dt^{3}}(t_{k}) + \dots\end{split}$$
The last two terms are the [[truncation-error]]. Defining $\frac{du}{dt} = f'(u, t)$, the second derivative term found by differentiating wrt $t$. $$\begin{split}\frac{d^{2}u}{dt^{2}} = \frac{d}{dt}\frac{du}{dt} = \frac{d}{dt}f'(t, u) &= \frac{\partial f'}{\partial t}(t, u) + \frac{\partial f'}{\partial t}(t, u)\frac{\partial u}{\partial t} \\\\ &= \frac{\partial f'}{\partial t}(t, u)\end{split}$$

>**Example** Solve the [[IVP]] $\frac{du}{dt} = (1 - \frac{4}{3}t)u, u(0) = 1$ using [[Taylor-Method]] and compare to exact solution.

**Drawbacks** [[Taylor-Method]] requires solving complex, partial derivatives. Furthermore, the differential equation must be smooth and continuous. Solving the partial derivatives and multiplications requires much computational power, which introduces much [[round-off-error]].

### Runge-Kutta Method
Higher-order local truncation error of [[Taylor-Method]] eliminates the need to compute derivatives. [[Runge-Kutta-Method]] is also the most popular and powerful *explicit* method to integrate [[ODE]].

$$\begin{equation}
u_{k+1} = u_{k} + h\sum_{i=1}^{m}c_{i}f'(t_{i, k}, u_{i, k}), f'(t, u) = \frac{du}{dt}
\label{eq:runge_kutta_method}
\end{equation}$$

Flexibility in designing the method and choosing the coefficients, and order is limited to power of h. The selection of $0 \leq \lambda \leq 1$, choosing $\lambda = 1$, which is [[Euler-Method]], uses information at the next time step to solve the half-steps from the current step.


---


*Lecture: September 24, 2021*
#### RK2
Two Methods for [[RK2]]
1. Improved [[Euler-Method]]: $a = b = \frac{1}{2},~\lambda = 1$
2. Midpoint Method: $a = 0,~b = 1,~\lambda = \frac{1}{2}$

General form for [[RK2]]: 
$$\begin{equation}
\begin{split}
u_{k+1} &= u_{k} &+ h[af'(t_{k}, u_{k}) + bf'(t_{k,2}, u_{k,2})] \\\\\\
&= u_{k} &+ h[af'(t_{k}, u_{k}) + \\\\
& & bf'(t_{k} + \lambda h, u_{k} + \lambda hf'(t_{k}, u_{k}))]
\end{split}
\label{eq:runge_kutta_2_method}
\end{equation}$$

#### RK4
$$\begin{equation}
\begin{split}
k_{1} &= hf'(t_{k}, u_{k}) \\\\\\
k_{2} &= hf'(t_{k} + \frac{h}{2}, u_{k} + \frac{k_{1}}{2}) \\\\\\
k_{3} &= hf'(t_{k} + \frac{h}{2}, u_{k} + \frac{k_{2}}{2}) \\\\\\
k_{4} &= hf'(t_{k} + h, u_{k} + k_{3}) \\\\\\
u_{k+1} &= u_{k} + \frac{1}{6}(k_{1} + 2k_{2} + 2k_{3} + k_{4})
\end{split}
\label{eq:rk4}
\end{equation}$$

| ![](../../attachments/engr-704-001-partial-differential-equations/rk4_graphical_example_210927_171909_EST.png) |
|:--:|
| The $\frac{1}{6}$ term for averaging out $k^{th}$ points in [[RK4]]. $\label{fig:rk4_graphical_example}$ |

>**Q&A**
Q: What are the units of $k$?
A: Same units as $u$, because $f`$ is only wrt to time.

>**Example** If $\dot{u} = u - t^{2} + 1$, where $u(0) = 0.5$ and $h = 0.2$.
$$\begin{split}
k_{1} &= hf'(t_{k}, u_{k}) = 0.2f'(0, 0.5) \\\\\\
&= 0.2(1.5) = 0.3 \\\\\\
k_{2} &= hf'(t_{k} + \frac{h}{2}, u_{k} + \frac{k_{1}}{2}) = 0.2f'(0.1, 0.65) \\\\\\
&= 0.328 \\\\\\
k_{3} &= hf'(t_{k} + \frac{h}{2}, u_{k} + \frac{k_{2}}{2}) = 0.2f'(0.1, 0.664) \\\\\\
&= 0.3308 \\\\\\
k_{4} &= hf'(t_{k} + h, u_{k} + k_{3}) = 0.2f'(0.1, 0.8308) \\\\\\
&= 0.35816 \\\\\\
u_{k+1} &= u_{k} + \frac{1}{6}(k_{1} + 2k_{2} + 2k_{3} + k_{4}) \\\\\\
&= 0.5 + \frac{1}{6}[0.3 + 2(0.328) + 2(0.3308) + 0.35816] \\\\\\
&= 0.8292933
\end{split}$$
![](../../attachments/engr-704-001-partial-differential-equations/rk4_example_solution_210927_174230_EST.png)
bar $\label{fig:rk4_example_solution}$
![](../../attachments/engr-704-001-partial-differential-equations/rk4_example_solution_error_comparison_210927_174336_EST.png)
bar $\label{fig:rk4_example_solution_error_comparison}$

### Implicit Methods
#### Backward Euler
Explicit methods are well suited to handle large class of [[ODE]]. However, these methods perform poorly for class of "stiff" equations that occur frequently in real problems: e.g. exponential functions in vibrational motion. If there is a large difference between the most rapid and slowest changes in solution components, then the system is a [[stiff-equation]]. If [[RK4]] requires small time step for sufficient accuracy, then that problem is likely involved with a [[stiff-equation]]. Implicit methods are generally suited to a [[stiff-equation]] since they are conditionally "stable": i.e. required limitation on time stepping; otherwise, solution will diverge and crash.

>Multiple choice: Euler-method is first order O(h2). Forward and backward formulations are both first order. Backward has more error than forward, but more stable.

| ![](../../attachments/engr-704-001-partial-differential-equations/difference_between_explicit_implicit_euler_method_210927_175502_EST.png) |
|:--:|
| $u_{k+1} = u_{k} + hf'(t_{k}, u_{k})$ versus $u_{k+1} = u_{k} + hf'(t_{k+1}, u_{k+1})$ $\label{fig:difference_between_explicit_implicit_euler_method}$ |


---


*Lecture: September 29, 2021*
We can use the [[Newton-Raphson]], [[root-finding]] method to solve the unknown, $u_{k+1}$ from the unknown, $u_{k+11}$.

>**Example** Solve the [[IVP]], $\frac{du}{dt} = e^{u},~u(0) = 1,~h = 0.1$ using backward [[Euler-Method]].
$$\begin{split}
u_{k+1} &= u_{k} + hf'(t_{k+1}, u_{k+1}) \\\\\\
&= u_{k} + he^{u_{k+1}} \\\\\\
F(u_{k+1}) &= u_{k+1} - he^{u_{k+1}} - u_{k} = 0 \\\\\\
F'(u_{k+1}) &= 1 - he^{u_{k+1}} = 0 \\\\\\
u_{k+1}^{n+1} &= u_{k+1}^{n} - \frac{F(u_{k+1}^{n})}{F'(u_{k+1}^{n})}
\end{split}$$
**KNOW THIS FOR EXAM!!!**

#### Trapezoidal Method
This is a **second-order** method and sometimes called the "[[Crank-Nicholson]]" in [[PDE]] contexts. This method is derived from the trapezoidal integration rule using half contributions at current and future points. $$u_{k+1} = u_{k} + \frac{1}{2}h[f'(t_{k}, u_{k}) + f'(t_{k+1}, u_{k+1})]$$ Or a more a generalized form:

$$u_{k+1} = u_{k} + h[(1 - \theta)f'(t_{k}, u_{k}) + \theta f'(t_{k+1}, u_{k+1})]$$ eq:implicit_trapezoidal_method

where, $$\theta = \begin{cases}
1 &, \text{Backward Euler} \\\\\\
-1 &, \text{Forward Euler} \\\\\\
0.5 &, \text{Trapezoidal}
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
: A $4^{th}$-order **explicit** method. $$\begin{equation}
\begin{split}
u_{k+1} &= u_{k} \\\\
&+ \frac{h}{24}[55f'(t_{k}, u_{k}) - 59f'(t_{k- 1}, u_{k - 1}) + 37f'(t_{k - 2}, u_{k - 2}) - 9f'(t_{k - 3}, u_{k - 3})]
\end{split}\label{eq:adam_bashforth}
\end{equation}$$

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
Large step size, i.e. large errors, dominate final solution. $\label{fig:stiff_differential_equation_method_comparisons} |

>**Example** Consider the [[IVP]], $\frac{du}{dt} = \gamma u,~u(0) = 1$ with exponential solution, $u(t) = e^{\gamma t}$.
Using a forward [[Euler-Method]],
$$\begin{split}
u_{k+1} &= u_{k} + \gamma hu_{k} = (1 + \gamma h)u_{k} \\\\
&= (1 + \gamma h)^(k + 1)u_{0} = (1 + \gamma h)^{k + 1}
\end{split}$$
The absolute error (exact - approximation) goes to zero:
$$E = |u_{k}(kh) - (1 - \gamma h)^{k}| = |(e^{\gamma h})^{k} - (1 + \gamma h)^{k}|$$
$$|1 + \gamma h| < 1 \implies -2<\gamma h < 0$$
When $\gamma < 0$, exact solution decays to $0$. When large, method diverges quickly with error growing. When large, step-size, $h$ must be very small. [[Euler-Method]] is expected to be stable only if $h < \frac{2}{|\gamma|}$. If $h$ satisfies this, then method converges, because error goes to $0$; otherwise, solution diverges, because error grows quickly.

In general, a function, $Q$ approximated by difference methods gives, $$u_{k + 1} = Q(\gamma h)u_{k}$$, where the error grows without bound if $|Q(\gamma h)| > 1$. $n^{th}$-order [[Taylor-Method]] has a stability condition, provided $h$ is chosen to satisfy: $$|1 + h\gamma + \frac{1}{2}\gamma^{2}h^{2} + \dots + \frac{1}{n}h^{n}\gamma^{n}| < 1$$ Stability analysis is generally very difficult to solve: heavily relies on mathematics.

Region, $R$ of absolute stability
: for a one-step method is $$R = \{h\gamma \in C:|Q(\gamma h)| < 1\}$$.

[[A-stable]] method
: The region of absolute stability contains entire, left half-plane of $\gamma h$ for $\gamma < 0$ on the complex plane, $\mathbb{Z}$. Likely named for the absolute value property.

Forward [[Euler-Method]] is conditionally stable: $$|1 + \gamma h| < 1,~h<\frac{2}{|\gamma|},~\text{for}~\gamma < 0,~h < \frac{-2}{\gamma}$$ The region of stability...

| ![](../../attachments/engr-704-001-partial-differential-equations/a_stable_method_example_of_forward_euler_211001_175330_EST.png) |
|:--:|
| The region of stability, $\gamma h = z,~abs(1 + z) < 1$. **This is not [[A-stable]] method**, because the stability region is not entire, left half-plane. Stability is limited by step size, $h$. $\label{fig:a_stable_method_example_of_forward_euler}$ |

>**Q: Only called [[A-stable]] when left plane?** <cite> Reid Prichard
*A: Correct. The [[Crank-Nicholson]] is implicit and [[A-stable]].*


---


*Lecture: October 04, 2021*
Will discuss **Midterm Exam** Wednesday.

>**Q: When do we exit the *Conjugate Gradient* methods?** <cite> Bethany
*A: Method is a direct solver, but certainly may require more iterations to get within tolerance. Looking for experiment with various inputs and error handling.*

Implicit [[Trapezoidal-Method]] is the **only [[A-stable]], multistep method**!
$$\begin{split}
u_{k+1} &= u_{k} + \frac{1}{2}h[\gamma u_{k} + \gamma u_{k+1}] \\\\
&= \frac{1 + \frac{1}{2}h\gamma}{1 - \frac{1}{2}h\gamma}u_{k}
\end{split}$$
If $\gamma > 0$, then error exponentially grows. If $\gamma < 0$, then error does not grow with condition, $h < \frac{-2}{\gamma}$.

| ![](../../attachments/engr-704-001-partial-differential-equations/a_stable_method_example_of_implicit_trapezoidal_211004_172442_EST.png) |
|:--:|
| $abs()$ $\label{fig:a_stable_method_example_of_implicit_trapezoidal}$ |

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
$$\begin{split}
y'' &= p(x)y' + q(x)y + r(x) &,~a \leq x \leq b &,~y(a) = \alpha &,~y'(a) = z1 \\\\
y'' &= p(x)y' + q(x)y &,~a \leq x \leq b &,~y(a) = 0 &,~y'(a) = z2
\end{split}$$
The solutions of the two problems are denoted $y_{1}(x)$ and $y_{2}(x)$, where $z1$ and $z2$ are commonly $0$ and $1$, respectively.

| ![](../../attachments/engr-704-001-partial-differential-equations/linear_shooting_method_graph_rep_211006_173206_EST.png) |
|:--:|
| $y(x) = y_{1}(x) + \frac{\beta - y_{1}(b)}{y_{2}(b)}y_{2}(x)$ interpolates between two [[IVP]], $y_{1}(x)$ and $y_{2}(x)$. $\label{fig:linear_shooting_method_graph_rep}$ |

If we restrict, $y_{2}(b) \neq 0$, then the solution can be written as: $y(x) = y_{1}(x) + \frac{\beta - y_{1}(b)}{y_{2}(b)}y_{2}(x)$, where the equation interpolations between $y_{1}(x)$ as solution to $y'' = p(x)y' + q(x)y + r(x)$ and $y_{2}(x)$ as solution to $y'' = p(x)y' + q(x)y$. First and second derivatives follow as:
$$\begin{split}
y'(x) &= y_{1}'(x) + \frac{\beta - y_{1}(b)}{y_{2}(b)}y_{2}'(x) \\\\
y''(x) &= y_{1}''(x) + \frac{\beta - y_{1}(b)}{y_{2}(b)}y_{2}''(x)
\end{split}$$

>**Q: Is this root-bracketed?** <cite> Reid
*A: Next slide.*

If we substitute into $y''(x)$, then:
$$\begin{split}
y''(x) &= y_{1}''(x) + \frac{\beta - y_{1}(b)}{y_{2}(b)}y_{2}''(x) \\\\
  &= p(x)y_{1}' + q(x)y_{1} + r(x) + \frac{\beta - y_{1}(b)}{y_{2}(b)}(p(x)y_{2}' + q(x)y_{2}) \\\\
  &= p(x)(y_{1}' + \frac{\beta - y_{1}(b)}{y_{2}(b)}y_{2}') + q(x)(y_{1} + \frac{\beta - y_{1}(b)}{y_{2}(b)}y_{2}) + r(x) \\\\
  &= p(x)y'(x) + q(x)y(x) + r(x)
\end{split}$$

>**Q: Is this like the bisection method?** <cite> Daniel K.
*A: This is not an iterative, [[root-finding]] problem. This interpolates between two, real solutions.*

The boundary conditions must satisfy:
$$\begin{split}
y(a) &= y_{1}(a) + \frac{\beta - y_{1}(b)}{y_{2}(b)}y_{2}(a) = \alpha + \frac{\beta - y_{1}(b)}{y_{2}(b)}*0 = \alpha \\\\
y(b) &= y_{1}(b) + \frac{\beta - y_{1}(b)}{y_{2}(b)}y_{2}(b) = \beta + 
\end{split}$$

>**Q: Why guess at the derivatives? Does this make it easier to solve?** <cite> Reid
*A: Certainly experiment with the guesses.*

- [[Linear-Shooting-Method]] uses two [[IVP]]
- The solutions to [[IVP]] are $y_{1}(x)$ and $y_{2}(x)$.
- These [[IVP]] are solved by typical [[ODE]] solvers.

>**Example** Apply [[Linear-Shooting-Method]] to [[BVP]]: $u'' = y'' = -\frac{2}{x}y' + \frac{2}{x^{2}}y + \frac{sin(ln(x))}{x^{2}}$, for $1 \leq x \leq 2$ if $y(1) = 1$, $y(2) = 2$, and $h = 0.1$.
First make first-order [[ODE]]: $y_{1} = u$, $u(1) = 1$, $T(1) = 0$. Therefore, $u' = T$ into $y_{1}$ and $T' = -\frac{2}{x} + \frac{2}{x^{2}}u + \frac{sin(ln(x))}{x^{2}}$ into $y_{2}$, and use forward [[Euler-Method]] to solve these equations. $$\begin{split} u_{n + 1} &= u_{n} + hf_{1}(T_{n}) \\\\ t_{n + 1} &= T_{n} + hf_{2}(x_{n}, u_{n}, T_{n})\end{split}$$ *Here, $h$ is spatial increment (physical spacing), not time increment.* At $n = 0$, set $x_{0} = 1.0$, then: $$\begin{split}\begin{bmatrix}u_{1} \\\\ T_{1}\end{bmatrix} &= \begin{bmatrix}u_{0} \\\\ T_{0}\end{bmatrix} + h\begin{bmatrix}f_{1}(T_{0}) \\\\ f_{2}(x_{0}, u_{0}, T_{0})\end{bmatrix} = \begin{bmatrix}u_{0} \\\\ T_{0}\end{bmatrix} + (0.1)\begin{bmatrix}T_{0} \\\\ -\frac{2}{x_{0}}T_{0} + \frac{2}{x_{0}^{2}}u_{0} + \frac{sin(ln(x_{0}))}{x_{0}^{2}}\end{bmatrix} \\\\ &= \begin{bmatrix}1 \\\\ 0\end{bmatrix} + (0.1)\begin{bmatrix}0 \\\\ -\frac{2}{1}(0) + \frac{2}{1}(1) + \frac{sin(ln(1))}{1}\end{bmatrix} = \boxed{\begin{bmatrix}1 \\\\ 0.2\end{bmatrix}} \longleftarrow \begin{bmatrix}u \\\\ T \end{bmatrix} \\\\ \begin{bmatrix}u_{2} \\\\ T_{2}\end{bmatrix} &= \begin{bmatrix}u_{1} \\\\ T_{1}\end{bmatrix} + h\begin{bmatrix}f_{1}(T_{1}) \\\\ f_{2}(x_{1}, u_{1}, T_{1})\end{bmatrix} = \begin{bmatrix}u_{1} \\\\ T_{1}\end{bmatrix} + (0.1)\begin{bmatrix}T_{1} \\\\ -\frac{2}{x_{1}}T_{1} + \frac{2}{x_{1}^{2}}u_{1} + \frac{sin(ln(x_{1}))}{x_{1}^{2}}\end{bmatrix} \\\\ &= \begin{bmatrix}1 \\\\ 0.2\end{bmatrix} + (0.1)\begin{bmatrix}1 \\\\ -\frac{2}{1.1}(0.2) + \frac{2}{1.1^{2}}(1) + \frac{sin(ln(1.1))}{1.1^{2}}\end{bmatrix} = \boxed{\begin{bmatrix}1.02 \\\\ 0.336791\end{bmatrix}} \longleftarrow \begin{bmatrix}u \\\\ T \end{bmatrix}\end{split}$$ Repeat this process for the second [[IVP]].
| ![](../../attachments/engr-704-001-partial-differential-equations/linear_shooting_method_solution_211011_174757_EST.png) |
|:--:|
| Converges on $\mathcal{O}(10^{-5})$. $\label{fig:linear_shooting_method_solution}$ |


---


*Lecture: October 13, 2021*
>**Exam does not cover the preliminary (first 2 weeks) lecture; however, Newton-Raphson can still be on test. Today's lecture will be on exam. 1 formula sheet of formulas only is allowed. Computer not required. Review session next Monday.** <cite> Cho

### Finite Difference Method
Differs from the [[finite-element-method]] and [[finite-volume-method]]. Example of [[dirichlet-boundary-condition]]. Approximates [[BVP]] with first-order equations requiring only one initial condition and second-order requiring two initial conditions. Recall a linear, second-order [[BVP]]: $y'' = p(x)y' + q(x)y + r(x)~\text{for}~a \leq x \leq b$, where $y(a) = \alpha$ and $y(b) = \beta$. Using a [[Taylor-polynomial]] about a point $x_{i}$ evaluated at $x_{i - 1}$ and $x_{i +1}$ and adding these two equations together, we find an approximation for for $y''$, $$\begin{split}y(x_{i - 1}) &= y(x_{i} + h) \approx y(x_{i}) + hy'(x_{i}) + \frac{h^{2}}{2}y''(x_{i}) + \frac{h^{3}}{3!}y'''(x_{i}) + \frac{h^{4}}{4!}y''''(x_{i}) \\\\\\ y(x_{i + 1}) &= y(x_{i} - h) \approx y(x_{i}) - hy'(x_{i}) + \frac{h^{2}}{2}y''(x_{i}) - \frac{h^{3}}{3!}y'''(x_{i}) + \frac{h^{4}}{4!}y''''(x_{i})\end{split}$$ When adding together and using a [[centered-difference-method]], $$\implies y''(x_{i}) \approx \frac{y(x_{i} + h) - 2y(x_{i}) + y(x_{i} - h)}{h^{2}} - 2\big(\frac{h^{2}}{4!}\big)y''''(x_{i})$$ Subtracting in the similar can approximate $y'(x_{i})$. $$y'(x_{i}) \approx \frac{y(x_{i} + h) - y(x_{i} - h)}{2h} - \big(\frac{h^{2}}{3!}\big)y'''(x_{i})$$ These converge $\mathcal{O}(h^{2})$.

Plugging these into the general form: $$\begin{split}y'' &= p(x)y' + q(x)y + r(x) \\\\ \implies -r(x_{i}) &= -\frac{w_{i + 1} - 2w_{i} + w_{i - 1}}{h^{2}} + p(x_{i})\frac{w_{i + 1} - w_{i - 1}}{2h} + q(x_{i})w_{i}\end{split}$$ where $w_{0} = \alpha,~w_{N+1} = \beta$. Finally, these equations can be represented in $\mathbb{R}^{N}$ with $\mathbf{A}\hat{w} = \hat{b}$

| ![](../../attachments/engr-704-001-partial-differential-equations/finite_difference_algorithm_explained_211013_173201_EST.png) |
|:--:|
| Be careful of indeces! The first and last elements of $\hat{b} = \alpha,~\beta$, respectively. $\tag{fig:finite_difference_algorithm_explained} \label{fig:finite_difference_algorithm_explained}$ |

#direct-solver or #iterative-solver can be used to solve system of equations, $\mathbf{A}\hat{w} = \hat{b}$.

### Finite Element Method
Sometimes called the [[variational-formulation]]. Often used when needing to minimize the free energy in systems. However, this method differs from what we have learned:
- [[Linear-Shooting-Method]]: uses entire domain to solve [[BVP]] with pair of [[IVP]].
- [[finite-difference-method]]: discretizes domain and finds the finite differences.

<dl>
<dt><strong>Differential Equation (two-point BVP)</strong></dt>
<dd>\begin{cases}-\frac{d}{dx}\bigg(p(x)\frac{du}{dx}\bigg) = f(x) &, 0 \leq x \leq 1 \\\\\\ u(0) = 0 &, u(1) = 0\end{cases}</dd>
</dl>

<dl>
<dt><strong>Linear Space</strong></dt>
<dd>\begin{equation*}V = \{\mathcal{v}: \mathcal{v} \in C^{0}[0,1],~\mathcal{v}'~\text{is piecewise continous on}~[0,1],~\text{and}~\mathcal{v}(0) = \mathcal{v}(1) = 0\}\end{equation*}</dd>
</dl>

This space can be solved by multiplying both sides by $\mathcal{v}$ and [[integration-by-parts]] over the domain $(0 \leq x \leq 1)$,

$$\begin{split}
\int_{0}^{1}-(pu')'\mathcal{v}dx &= \int_{0}^{1}f\mathcal{v}dx \\\\\\
foo &= bar
\end{split}$$


---


*Lecture: October 18, 2021*
>**EXAM REVIEW** Know the concepts of each method and the pros and cons of those methods. You are allowed 1 page for a formula sheet: the formula only. *No calculator for inverse matrices!!* The exam material will come from slides for only that material covered. The exam tests your knowledge to apply what you have learned, assuming you have learned the material. 5-6 questions, where 3 may require solution.
> - FFT
> 	- Theory: Inverse transform to find coefficients in frequency domain and then convert to real domain.
> 	- DFT: uses discretized domain in Inverse transform; however, is very slow.
> 	- FFT: algorithm to speed up solution of DFT with symmetry in frequency domain. Use $W_{n/2}$ formula to find coefficients and convert back to original index (butterfly diagram).
> - Eigenvalues and Eigenvectors
> 	- $n~x~n$ matrix has characteristic polynomial of $n^{th}$ degree.
> 	- Computing this directly is expensive and may be difficult to solve quickly.
> 	- *Power Method* finds the dominant eigenvalue of the matrix. $\mu_{k}$ goes to the largest $\lambda$ and $\vec{x}$ goes to corresponding eigenvector.
> 	- *Inverse Power Method* does similar to *Power*, but this method finds the $\lambda$ closest to the target value.
> 	- *QR Method* assumes a **symmetric, diagonal matrix** has a similar, non-singular (invertible) matrix exists: i.e. some matrix with equivalent eigenvalues exists. **This method can find all the eigenvalues at once.** These eigenvalues are the long diagonal of $\mathbf{A}$. If asked to find the *rotation matrix*, then find it: do not use Gram-Schmidt method unless allowed or *$\mathbf{P}$* not given.
> 	- *Steepest Descent Method* solves the linear system of equations, $\mathbf{A}\vec{x} = \vec{b}$, *where $\mathbf{A}$ is a symmetric, positive-definite, square matrix*. This does not work well with sparse matrix (these are best solved with direct methods). Searches in the *negative gradient* direction to find optimal solution where the error converges rapidly toward the (max/min)imum of the "bowl", which is also the residual vector, $\vec{r_{k}} = -\nabla f(\vec{x_{k + 1}}) = \vec{b} - \mathbf{A}\vec{x}$.
> 	- <mark style="background-color: yellow">*Conjugate Gradient Method*: extension of *Steepest Descent*; however, this solution search direction is *not* perpendicular to residual vector, which is negative gradient. The search direction is *A-orthogonal* (conjugate) to residual vector, and the two vectors are mutually orthogonal.</mark> **This converges in maximum, $n$ iterations; however, this is not direct solution because of round-off error.**
> 	- *Pre-conditioned Conjugate Gradient Method* reduces round-off error and can solve *ill-conditioned (singular)* matrices whose condition number is high, which makes finding the inverse difficult and expensive. **By reducing the condition number, the matrix is easier to solve in $\sqrt{n}$ iterations.**
> 
> Know how to apply and solve the following:
> - IVP
> 	- Explicit
> 		- Forward Euler (first-order)
> 		- Higher-order Taylor (higher order), but very expensive to calculate higher order derivatives: round-off error increases.
> 		- RK is most popular and has the advantage of not needing derivatives: is a second-order method.
> 		- Improved/Midpoint Euler
> 		- RK4 finds averages of slopes at varies substep points with better accuracy than RK2 because it is higher order.
> 	- Implicit: preferred for its stability and higher-order accuracy.
> 		- Backward Euler (first-order): relies on root-finding method to solve.
> 		- Trapezoidal (Crank-Nicholson): second-order
> 	- Predictor/Corrector Equations
> 	- Stiffness and A-stability.
> - BVP
> 	- Linear Shooting method with two IVP by typical solution method.
> 	- FDM: centered-difference formula to solve matrix.
