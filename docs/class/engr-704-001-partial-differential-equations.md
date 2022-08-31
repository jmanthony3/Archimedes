---
title: Partial Differential Equations
subject: ENGR 704-001
date: 210823-211217
time: 13:05-13:55 (MWF)
place: DH 3276
speaker: Dr. Heechen Cho
---
# ENGR 704-001: Partial Differential Equations
Table of Contents
- [ENGR 704-001: Partial Differential Equations](#engr-704-001-partial-differential-equations)
  - [Chapter 5: Initial-Value Problems for Ordinary Differential Equations](#chapter-5-initial-value-problems-for-ordinary-differential-equations)
    - [Euler Method](#euler-method)
    - [Taylor Method](#taylor-method)
    - [Runge-Kutta Method](#runge-kutta-method)
    - [Implicit Methods](#implicit-methods)
    - [Summary](#summary)
  - [Boundary Value Problems in ODE](#boundary-value-problems-in-ode)
    - [Shooting Method](#shooting-method)
    - [Finite Difference Method](#finite-difference-method)
    - [FEM](#fem)
  - [Partial Differential Equations](#partial-differential-equations)
    - [Physical Classifications](#physical-classifications)
    - [Mathematical Classifications](#mathematical-classifications)
    - [Well-Posed Problem](#well-posed-problem)
    - [Properties of Numerical Methods for PDE](#properties-of-numerical-methods-for-pde)
    - [Stability Analysis](#stability-analysis)
    - [Application of Numerical Methods on Hyperbolic PDE](#application-of-numerical-methods-on-hyperbolic-pde)
    - [Application of Numerical Methods on Parabolic PDE](#application-of-numerical-methods-on-parabolic-pde)
    - [Application of Numerical Methods on Elliptic PDE](#application-of-numerical-methods-on-elliptic-pde)

*Lecture: September 24, 2021*
## Chapter 5: Initial-Value Problems for Ordinary Differential Equations

### Euler Method
See: [[euler-method]]

### Taylor Method
See: [[taylor-method]]

### Runge-Kutta Method
See: [[runge-kutta-method]]


---


*Lecture: September 24, 2021*

### Implicit Methods
See: [[implicit-methods]]


---


*Lecture: September 29, 2021*

!!! example Solve the #IVP, $\frac{du}{dt} = e^{u},~u(0) = 1,~h = 0.1$ using backward [[euler-method]].
    $$\begin{split}
    u_{k+1} &= u_{k} + hf'(t_{k+1}, u_{k+1}) \\
     &= u_{k} + he^{u_{k+1}} \\
    F(u_{k+1}) &= u_{k+1} - he^{u_{k+1}} - u_{k} = 0 \\
    F'(u_{k+1}) &= 1 - he^{u_{k+1}} = 0 \\
    u_{k+1}^{n+1} &= u_{k+1}^{n} - \frac{F(u_{k+1}^{n})}{F'(u_{k+1}^{n})}
    \end{split}$$

    !!! attention
        KNOW THIS FOR EXAM!!

*[IVP]: Initial Value Problem


---


*Lecture: October 1, 2021*

!!! attention EXAM Bring one formula sheet for closed-book, in-class exam! Exam after covering the #FEM, which may likely be next week.

*[FEM]: Finite Element Method

!!! example Solve the first #NR iteration for $u_{k+1} = u_{k} + \frac{1}{2}h(e^{u_{k}} + e^{u_{k+1}}),~u_{0} = 1,~h = 0.1$.


---


*Lecture: October 04, 2021*

Will discuss **Midterm Exam** Wednesday.

!!! question When do we exit the *Conjugate Gradient* methods? <cite> Bethany
    Method is a direct solver, but certainly may require more iterations to get within tolerance.
    Looking for experiment with various inputs and error handling.*

### Summary
- #A-stable not affected by stiffness of #ODE.
- No explicit [[runge-kutta-method]] is #A-stable.
- Implicit #Trapezoidal-Method is simplest example of #A-stable, multistep method.
- Although the #Trapezoidal-Method does give accurate approximations for large step sizes, its error will not grow exponentially.
- Techniques commonly used for #stiff-equation will likely be implicit, multi-step methods.
- In most cases, $u_{k + 1}$ is obtained from non-linear equations; therefore, #NR is typically used.

!!! quote Stability does not ensure accuracy. <cite> Dr. Cho

!!! tip Know how to solve #RK4 for the exam! <cite> Dr. Cho


---


*Lecture: October 06, 2021*

**Exam October 20, 2021 with review on the 18$^{th}$. HW2 assigned after that.**
## Boundary Value Problems in ODE
!!! hint A bridge that is fixed at both ends, find the height of the curvature.

Discuss approximation to #BVP with conditions imposed at different points.
First-order differential equations only require one condition.
However, physical problems that are position-dependent rather than time-dependent are often described in terms of differential equations with conditions imposed at more than one point.
Two-point #BVP involve a second-order differential equation, which is generally of the form: $$\frac{d^{2}y}{dx^{2}} = y'' = f(x, y, y'),~a \leq x \leq b$$ and $y(a) = \alpha, y(b) = \beta$.

*[BVP]: Boundary Value Problem

### Shooting Method
See: [[shooting-method]]


---


*Lecture: October 13, 2021*

!!! info
    Exam does not cover the preliminary (first 2 weeks) lecture; however, Newton-Raphson can still be on test. Today's lecture will be on exam. 1 formula sheet of formulas only is allowed. Computer not required. Review session next Monday.

### Finite Difference Method
See: [[finite-difference-method]]

### FEM
See: [[finite-element-method]]


---


*Lecture: October 18, 2021*

*[FFT]: Fast-Fourier Transform
*[DFT]: Discrete Fourier Transform
!!! summary EXAM REVIEW
    Know the concepts of each method and the pros and cons of those methods. You are allowed 1 page for a formula sheet: the formula only. *No calculator for inverse matrices!!* The exam material will come from slides for only that material covered. The exam tests your knowledge to apply what you have learned, assuming you have learned the material. 5-6 questions, where 3 may require solution.
    - #FFT
        - Theory: Inverse transform to find coefficients in frequency domain and then convert to real domain.
        - #DFT: uses discretized domain in Inverse transform; however, is very slow.
        - #FFT: algorithm to speed up solution of #DFT with symmetry in frequency domain. Use $W_{n/2}$ formula to find coefficients and convert back to original index (butterfly diagram).
    - Eigenvalues and Eigenvectors
        - $n~x~n$ matrix has characteristic polynomial of $n^{th}$ degree.
        - Computing this directly is expensive and may be difficult to solve quickly.
        - *Power Method* finds the dominant eigenvalue of the matrix. $\mu_{k}$ goes to the largest $\lambda$ and $\vec{x}$ goes to corresponding eigenvector.
        - *Inverse Power Method* does similar to *Power*, but this method finds the $\lambda$ closest to the target value.
        - *QR Method* assumes a **symmetric, diagonal matrix** has a similar, non-singular (invertible) matrix exists: i.e. some matrix with equivalent eigenvalues exists. **This method can find all the eigenvalues at once.** These eigenvalues are the long diagonal of $\mathbf{A}$. If asked to find the *rotation matrix*, then find it: do not use Gram-Schmidt method unless allowed or *$\mathbf{P}$* not given.
        - *Steepest Descent Method* solves the linear system of equations, $\mathbf{A}\vec{x} = \vec{b}$, *where $\mathbf{A}$ is a symmetric, positive-definite, square matrix*. This does not work well with sparse matrix (these are best solved with direct methods). Searches in the *negative gradient* direction to find optimal solution where the error converges rapidly toward the (max/min)imum of the "bowl", which is also the residual vector, $\vec{r_{k}} = -\nabla f(\vec{x_{k + 1}}) = \vec{b} - \mathbf{A}\vec{x}$.
        - ==*Conjugate Gradient Method*: extension of *Steepest Descent*; however, this solution search direction is *not* perpendicular to residual vector, which is negative gradient. The search direction is *A-orthogonal* (conjugate) to residual vector, and the two vectors are mutually orthogonal.== **This converges in maximum, $n$ iterations; however, this is not direct solution because of round-off error.**
        - *Pre-conditioned Conjugate Gradient Method* reduces round-off error and can solve *ill-conditioned (singular)* matrices whose condition number is high, which makes finding the inverse difficult and expensive. **By reducing the condition number, the matrix is easier to solve in $\sqrt{n}$ iterations.**

    Know how to apply and solve the following:
    - #IVP
        - Explicit
            - Forward Euler (first-order)
            - Higher-order Taylor (higher order), but very expensive to calculate higher order derivatives: round-off error increases.
            - #RKM is most popular and has the advantage of not needing derivatives: is a second-order method.
            - Improved/Midpoint Euler
            - #RK4 finds averages of slopes at various substep points with better accuracy than #RK2 because it is higher order.
        - Implicit: preferred for its stability and higher-order accuracy.
            - Backward Euler (first-order): relies on root-finding method to solve.
            - Trapezoidal (Crank-Nicholson): second-order
        - Predictor/Corrector Equations
        - Stiffness and A-stability.
    - #BVP
        - Linear Shooting method with two IVP by typical solution method.
        - #FDM: centered-difference formula to solve matrix.


---


*Lecture: October 22, 2021*

!!! info Group Project will be to develop #FDM because only half the semester remains. All groups will solve the same equation: [[eq-thermal-diffusion]].
    However, this is where the semester moves from #ODE to #PDE with a #BVP. Make the grid spacing, $h$ uniform for the whole domain.
    Dr. Cho will provide instruction on how to build discretized domain. For team assignments, Dr. Cho asks that we list our name and top two preferences of which project configuration where the first number is the most preferred: wrt [Project Description](C:\Users\jmanthony1\Liberty University\Group-Numerical Methods for ODE PDE-Fall2021 - Class Materials\Project\Group_Project_Plans.pdf). *I picked 2 and 3.*


---


*Lecture: October 25, 2021*

!!! note Final Project
    I picked 2 and 3: Backward Euler with Conjugate Gradient and Crank-Nicholson with SOR.
    Various deliverables:
    1. Draft
    2. Presentation
    3. Journal Article


---


*Lecture: October 27, 2021*

!!! summary Review from Exam 2
    - Do not share formula sheets.
    - If you did the homework, then you know how to double-check your answers and to use certain keywords in the explanation of that answer.
    - ==**Final Exam** will be similar to this exam.==


---


*Lecture: October 29, 2021*

!!! summary Group 2 Project Teams
    - Adam Rutherford
    - Joby M. Anthony III
    - Reid Prichard
    - Adriel Lau

    !!! info Project Expectations
        Dr. Cho will upload a #FDM tutorial later this afternoon. Make square domain with four, #dirichlet-boundary-condition temperature boundary conditions and solve temperature distribution in domain. Pick a metal more relevant to research. Play with initializing temperatures locally and see effects over time.


---


*Lecture: November 01, 2021*

!!! attention Know these weighting functions for exam!
    - #Galerkin uses #basis-function, $\phi_{i}$ as #trial-functions.
    - #least-squares method uses $w(x) = \frac{\partial}{\partial c_{i}}R(u_{h}) = P(\phi_{i})$ as the #trial-functions.
    - #Collocation method uses $w(x) = \delta(x - x_{i})$ (displaced Dirac delta function) as the #trial-functions, where $$\delta(x - x_{i}) = \begin{cases}\infty &, \text{ if } x = x_{i} \\ 0 &, \text{ else}\end{cases}$$.

## Partial Differential Equations
- Many physical processes processes in nature are governed by partial differential equations (#PDE)
- Knowledge of the mathematical properties and solution of the governing equations as needed.
- #PDE is distinguishable by its derivatives: e.g. $$\begin{cases}
\phi_{x} + \phi_{y}y\phi = 0 &, \text{First Order Linear} \\
\phi_{xx}^{2} + \phi_{xy} + \phi\phi_{yy} = 0 &, \text{Second Order Non-Linear} \\
\phi\phi_{xx} + \phi\phi_{x} + x\phi_{y} = 0 &, \text{Second Order Non-Linear}
\end{cases}$$
- The highest order derivative prescribes the order of #PDE.

Non-linear
: Wen the coefficient of the highest-order derivatives contains dependent variables or its derivatives.

!!! attention Know these categories for exam!
    3 Physical Categories:
    1. Equilibrium
    2. #eigenvalues
    3. Marching (propagation)

    3 Mathematical Classifications
    - Elliptic
    - Parabolic
    - Hyperbolic

### Physical Classifications
See: [[physical-classifications]]

### Mathematical Classifications
See: [[mathematical-classifications]]


---


*Lecture: November 03, 2021*

!!!  summary Project Introduction
    $$\begin{equation}
    \frac{\partial T}{\partial t} = \partial\bigg(\frac{\partial^{2}T}{\partial x^{2}} + \frac{\partial^{2}T}{\partial y^{2}}\bigg)
    \end{equation}$$

    - #dirichlet-boundary-condition problem.
    - *Uploaded to Teams.*
    - Each method handles the LHS differently, and the different equations handle the RHS differently.

    **1D Definition**

    - Multiple ways to implement #FDM codes. Refer to Eqs. (9)- in PDF for each nodal point, $j$ in $n$ nodes. These create a #tridiagonal system of equations.
    - This system of equations is solved by the prescribed method.
    - The matrix should be #positive-definite and #symmetric.
    - Attempt to solve directly and make sure that solution can be found. Then apply some method to find solution faster.

    **2D Definition**

    - Refer to Eqs. (26)-
    - Sometimes referred to as the *5-Point Stencil*.
    - Each term on the RHS is the derivative of $U$ wrt to $x$ and $y$, respectively.
    - The $\vec{U}$ is a flattened version of $U$ in the nodal space matrix.
    - Matrix will be #pentadiagonal.

### Well-Posed Problem
See: [[well-posed-problem]]


---


*Lecture: November 05, 2021*
### Properties of Numerical Methods for PDE
See: [[properties-of-numerical-methods-for-pde]]

!!! example Mantle Convection Problem
    Earth is broken into three substructures. Calculating grain size and growth with subsequent mechanical properties (which require different material definitions in these 3 groups) there exists very low values at interface boundaries. It turns out, this visualization problem automatically interpolates between grid points, which are not necessarily the same spacing or size. This made a bad transition between layers. Nothing wrong with code, just a bad visualization.


---


*Lecture: November 08, 2021*

### Stability Analysis
See: [[stability-analysis]]


---


*Lecture: November 10, 2021*

The #amplification-factor, $G$ is a function of the frequency (recalling that $\nu = \Delta x\xi$). IF we think of the solution being represented by a #Fourier-Series, we see that the #damping of a given term in that series depends on the $\nu$ associated with that term: potential distortion of the relationships between the terms in the series...

*insert image*

Simpler Steps:
1. Replace $u_{j}^{n}$ with $\hat{u}^{n}e^{ij\nu}$ for each $j$ and $n$.
2. Find the condition for the #stability.

!!! example Heat equation with *Forward-Euler*:
    !!! attention
        **This will be in the exam!!!**

    $$\begin{split}
    u_{j}^{n + 1} &= \mu u_{j + 1}^{n} + (1 - 2\mu)u_{j}^{n} + \mu u_{j - 1}^{n} \\
    e^{i(j)\nu}\hat{u}^{n + 1} &= \mu e^{i(j + 1)\nu}\hat{u}^{n} + (1 - 2\mu)e^{i(j)\nu}\hat{u}^{n} + \mu e^{i(j - 1)\nu}\hat{u}^{n} \\
    e^{i(j)\nu}\hat{u}^{n + 1} &= \mu e^{i(j)\nu}\big(\mu e^{i\nu} + (1 - 2\mu) + \mu e^{-i\nu}\hat{u}^{n}\big)\hat{u}^{n}
    \end{split}$$

!!! example Heat equation with the simple implicit: $$\frac{(u_{j}^{n + 1} - u_{j}^{n})}{\Delta t} = \frac{\alpha}{(\Delta x)^{2}}\big(u_{j + 1}^{n + 1} - 2u_{j}^{n + 1} + u_{j - 1}^{n + 1}\big)$$

    1. Replace $u_{j}^{n}$ with $\hat{u}^{n}e^{i(j)\nu}$ for each $j$ and $n$.

    $$\begin{split} u_{j}^{n + 1} &= \mu u_{j + 1}^{n + 1} - 2\mu u_{j}^{n + 1} + u_{j - 1}^{n + 1} + u_{j}^{n} \text{, } \mu = \frac{\alpha\Delta t}{(\Delta x)^{2}} \\
    \hat{u}^{n + 1}e^{i(j)\nu} &= \mu\hat{u}^{n + 1}e^{i(j + 1)\nu} - 2\mu\hat{u}^{n + 1}e^{i(j)\nu} + \mu\hat{u}^{n + 1}e^{i(j - 1)\nu} + \hat{u}^{n}e^{i(j)\nu} \\
    \hat{u}^{n + 1}e^{i(j)\nu} &= e^{i(j)\nu}\big(\mu e^{i(j)\nu} - 2\mu + \mu e^{-i\nu}\big)\hat{u}^{n + 1} + \hat{u}^{n}e^{i(j)\nu} \\
    \hat{u}^{n + 1} &= \frac{1}{-(\mu e^{i\nu} - 2\mu - 1 + \mu e^{-i\nu})}\hat{u}^{n} = \frac{1}{2\mu  + 1 - 2\mu\cos(\nu)}\hat{u}^{n} = \frac{1}{1 + 4\mu\sin^{2}(\frac{\nu}{2})}\hat{u}^{n} \\ \Bigg|\frac{1}{1 + 4\mu\sin^{2}(\frac{\nu}{2})}\Bigg| &\leq 1 \\
    1 + 4\mu\sin^{2}(\frac{\nu}{2}) &\leq -1 \\
    1 + 4\mu\sin^{2}(\frac{\nu}{2}) &\geq 1 \\
    \therefore \mu &\geq 0
    \end{split}$$

    **This is unconditionally stable!**


---


*Lecture: November 12, 2021*

!!! example Heat equation with the Crank-Nicholson: $$\frac{(u_{j}^{n + 1} - u_{j}^{n})}{\Delta t} = \frac{\alpha}{(\Delta x)^{2}}\bigg(\frac{\big(u_{j + 1}^{n + 1} - 2u_{j}^{n + 1} + u_{j - 1}^{n + 1}\big)}{(\Delta x)^{2}} + \frac{\big(u_{j + 1}^{n} - 2u_{j}^{n} + u_{j - 1}^{n}\big)}{(\Delta x)^{2}}\bigg)$$

    1. Replace $u_{j}^{n}$ with $\hat{u}^{n}e^{i(j)\nu}$ for each $j$ and $n$.

    $$\begin{split}
    u_{j}^{n + 1} &= \frac{1}{2}\bigg(\mu u_{j + 1}^{n + 1} - 2\mu u_{j}^{n + 1} + \mu u_{j - 1}^{n + 1} + \mu u_{j + 1}^{n} - 2\mu u_{j}^{n} + \mu u_{j - 1}^{n}\bigg) + u_{j}^{n} \text{, } \mu = \frac{\alpha\Delta t}{(\Delta x)^{2}} \\
    \hat{u}^{n + 1}e^{i(j)\nu} &= \frac{1}{2}\bigg(\mu\hat{u}^{n + 1}...e^{i(j + 1)\nu} - 2e^{i(j)\nu} + e^{i(j - 1)\nu}\big) + \mu\hat{u}^{n}\big(e^{i(j + 1)\nu} - 2e^{i(j)\nu} + e^{i(j - 1)\nu}\big) + \hat{u}_{j}^{n}e^{i(j + 1)\nu} \\
    \hat{u}^{n + 1}e^{i(j)\nu} &= e^{i(j)\nu}\big(\mu e^{i(j)\nu} - 2\mu + \mu e^{-i\nu}\big)\hat{u}^{n + 1} + \hat{u}^{n}e^{i(j)\nu} \\
    \hat{u}^{n + 1} &= \frac{1}{-(\mu e^{i\nu} - 2\mu - 1 + \mu e^{-i\nu})}\hat{u}^{n} = \frac{1}{2\mu  + 1 - 2\mu\cos(\nu)}\hat{u}^{n} = \frac{1}{1 + 4\mu\sin^{2}(\frac{\nu}{2})}\hat{u}^{n}
    \end{split}$$

    2. Find the condition for #stability.

    $$\begin{split}
    G = \Bigg|\frac{1 + \mu(\cos(\nu) - 1)}{1 - \mu(\cos(\nu) - 1)}\Bigg| &\leq 1 \\
     = \Bigg|\frac{1... + \mu(\cos(\nu) - 1)}{1 - \mu(\cos(\nu) - 1)}\Bigg| &\leq 1 \\
    1 + 4\mu\sin^{2}(\frac{\nu}{2}) &\geq 1 \\
    \therefore \mu &\geq 0
    \end{split}$$

!!! example 2D heat equation with *Forward-Euler*: $$\frac{(u_{i, j}^{n + 1} - u_{i, j}^{n})}{\Delta t} = \alpha\bigg(\frac{\big(u_{i + 1, j}^{n} - 2u_{i, j}^{n} + u_{i - 1, j}^{n}\big)}{(\Delta x)^{2}} + \frac{\big(u_{i, j + 1}^{n} - 2u_{i, j}^{n} + u_{i, j - 1}^{n}\big)}{(\Delta y)^{2}}\bigg)$$
    
    1. Replace $u_{k, l}^{n}$ with $\hat{u}^{n}e^{i((k)\nu + (l)w)}$ for each $k$, $l$, and $n$.

    $$\begin{split}
    u_{k, l} &= \frac{1}{\sqrt{2\pi}}\int\int_{-\infty}^{+\infty}\big(e^{i(k\Delta\xi_{x} + l\Delta y\xi_{y})}\big)\hat{u}(\xi)d\xi_{x}d\xi_{y} \\
    \implies \frac{(u_{i, j}^{n + 1} - u_{i, j}^{n})}{\Delta t} &= \alpha\bigg(\frac{\big(u_{i + 1, j}^{n} - 2u_{i, j}^{n} + u_{i - 1, j}^{n}\big)}{(\Delta x)^{2}} + \frac{\big(u_{i, j + 1}^{n} - 2u_{i, j}^{n} + u_{i, j - 1}^{n}\big)}{(\Delta y)^{2}}\bigg) \\
    u_{i, j}^{n + 1} &= \alpha\Delta t\bigg(\frac{\big(u_{i + 1, j}^{n} - 2u_{i, j}^{n} + u_{i - 1, j}^{n}\big)}{(\Delta x)^{2}} + \frac{\big(u_{i, j + 1}^{n} - 2u_{i, j}^{n} + u_{i, j - 1}^{n}\big)}{(\Delta y)^{2}}\bigg) + u_{i, j}^{n} \\
    \hat{u}^{n + n}e^{i((k)\nu + (l)w)} &= \mu\big(\hat{u}^{n}e^{i((k + 1)\nu + (l)w)} - 2\hat{u}^{n}e^{i((k)\nu + (l)w)} + \hat{u}^{n}e^{i((k - 1)\nu + (l)w}\big) + \rho\big(\hat{u}^{n}e^{i((k)\nu + (l + 1)w)} - 2\hat{u}^{n}e^{i((k)\nu + (l)w)} + \hat{u}^{n}e^{i((k)\nu + (l - 1)w)}\big) + \hat{u}^{n}e^{i((k)\nu + (l)w)} \text{, } \mu = \frac{alpha\Delta t}{(\Delta x)^{2}} \text{, } \rho = \frac{\alpha\Delta t}{(\Delta y)^{2}} \\
    \hat{u}^{n + n}e^{i((k)\nu + (l)w)} &= e^{i((k)\nu + (l)w)}\bigg(\mu\big(e^{i\nu} - 2 + e^{-i\nu}\big) + \rho\big(\dots\hat{u}^{n}e^{i((k)\nu + (l + 1)w)} - 2\hat{u}^{n}e^{i((k)\nu + (l)w)} + \hat{u}^{n}e^{i((k)\nu + (l - 1)w)}\big)\bigg)\hat{u}^{n} + \hat{u}^{n}e^{i((k)\nu + (l)w)} \text{, } \mu = \frac{alpha\Delta t}{(\Delta x)^{2}} \text{, } \rho = \frac{\alpha\Delta t}{(\Delta y)^{2}}
    \end{split}$$

    2. Find the condition for #stability.

!!! example Lax scheme for linear, convection equation: $$u_{j}^{n + 1} = \frac{u_{j + 1}^{n} + u_{j - 1}^{n}}{2} - c\frac{\Delta t}{\Delta x}\bigg(\frac{u_{j + 1}^{n} - u_{j - 1}^{n}}{2}\bigg) \text{, } c = \text{ wave speed}$$
    
    1. Replace $u_{j}^{n}$ with $\hat{u}^{n}e^{i(j)\nu}$ for each $j$ and $n$.

    2. Find the condition for #stability.

    | ![](../../attachments/engr-704-001-partial-differential-equations/lax_scheme_linear_convection_stability_example_211112_185052_EST.png) |
    |:--:|
    | [[eq-courant-number]] phase diagram. |

    $$\begin{split}
    \hat{u}^{n + 1} &= (\cos(\nu) - iC\sin(\nu))\hat{u}^{n} \\
    \big|G\big| &= \big|(\cos(\nu) - iC\sin(\nu))\big| \leq 1 \\
    1 + (C^{2} - 1)\sin^{2}(\nu) &\leq 1
    \end{split}$$

    We have a *complex* #amplification-factor. ==This scheme is #stable if $|G| \leq 1$!== This is also called the #Courant-Friedrichs-Lewy-Condition.

    *[CFL]: Courant-Friedrichs-Lewy Condition

    $$\begin{split}
    G &= \cos(\nu) - iC\sin(\nu) = \sqrt{\cos^{2}(\nu) + C^{2}\sin^{2}(\nu)} = |G|e^{i\phi} \\
     &= \sqrt{\cos^{2}(\nu) + C^{2}\sin^{2}(\nu)}\big(e^{i\tan^{-1}(-C\tan(\nu))}) \\
    \phi &= \tan^{-1}\bigg(\frac{-C\tan(\nu)}{\cos(\nu)}\bigg) = \boxed{\tan^{-1}(-C\tan(\nu))} \text{, } \phi = \text{ phase angle}
    \end{split}$$

    The imaginary part of $G$ represents the #phase-shift: a potential distortion of the relationships between the terms in a series that represents the solution. At $C = 1$, all frequency components are propagated without #attenuation. For $C < 1$, the midrange frequency components have severe #attenuation.

    | ![](../../attachments/engr-704-001-partial-differential-equations/polar_plot_for_lax_scheme_211115_181937_EST.png) |
    |:--:|
    | The radius is $|G|$, where each data set is a different $\nu$. |

    Physical interpretation of the #CFL: information cannot propagate more than one grid spacing during a time step.

    $$\begin{split}
    |C| &= \bigg|c\frac{\Delta t}{\Delta x} \leq 1 \\
    c\Delta t &\leq \Delta x \\
    \bigg(\frac{\Delta t}{\Delta x}\bigg)^{2} &\leq \frac{1}{c^{2}}
    \end{split}$$

    #CFL requires that the analytic domain of influence lie within the numerical domain of influence. The slope of propagation must be smaller than (within) the #characteristic-path: $\frac{dt}{dx} = \pm \frac{1}{c}$.

    !!! attention Exam Hint
        Content pertaining the definitions and differences of parabolic, elliptic, and hyperbolic equations will be included.


---


*Lecture: November 15, 2021*

!!! hint
    After sufficient time, project becomes steady-state. Compare this to elliptic solution!


---


*Lecture: November 17, 2021*

!!! attention Homework 3
    This will be the last one! Dr. Cho will send it today or tomorrow, and this will be due the Friday after Thanksgiving Week.

!!! note Final Project
    Presentation due and given Dec. XX. Write-up article will be due by exam.

!!! attention Final Exam
    Cumulative!!!

### Application of Numerical Methods on Hyperbolic PDE
See: [[application-of-numerical-methods-on-hyperbolic-pde]]


---


*Lecture: November 19, 2021*

!!! attention Closing Thoughts for Class
    - Prepare for a 10 min. presentation.
    - We will finish hyperbolic today.
    - We may get to multi-grid solver.
    - Dr. Cho wanted to get to Finite Element and Volume Methods.
    - However, there is a dedicated Finite Element class. The purpose of this #PDE course was give mathematical understanding to these solvers.


---


*Lecture: November 29, 2021*

!!! note Homework 3
    Only a single problem similar to that seen for the Final Project.
    Dr. Cho gave us the modified equation rather than us formulating it ourselves to see the dissipative/dispersive error.

    - #dispersive-error: oscillates
    - #dissipative-error: leans

    **For this problem, the CFL number can go up to 2.**
    The _#Beam-Warming-Method_ scheme should be flipped vertically wrt _#Lax-Wendroff-Method_.
    ==Somethings that we can do is plot the phase error.==

### Application of Numerical Methods on Parabolic PDE
See: [[application-of-numerical-methods-on-parabolic-pde]]


---


*Lecture: December 01, 2021*

!!! info Closing Class Remarks
    This Friday will be the last lecture because Final Project presentations will be next Monday.
    Our Final Exam is 12-09.
    The Final Project paper deadline pushed to 12-15.

!!! attention Professor Objectives
Dr. Cho only wants us to be familiar with the names and concepts of these scheme.
He will not ask us to solve a #PDE with these schemes.

### Application of Numerical Methods on Elliptic PDE
See: [[application-of-numerical-methods-on-elliptic-pde]]


---


*Lecture: December 03, 2021*

!!! info Important Dates
  1. Final Exam: 12/9 (Thursday) from 3:30 to 5:30 PM
  2. Project Presentation: 12/6 (Monday) for 10 min presentations
  3. Deadlines
    1. HW3: 12/5
    2. Project Report: 12/15
    3. Vision Statement: 12/15