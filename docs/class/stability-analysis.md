# stability-analysis

Let us consider a simple, #explicit approximation to the heat equation: $$u_{j}^{n + 1} = \alpha\frac{\Delta t}{(\Delta x)^{2}}\bigg(u_{j + 1}^{n} - 2u_{j}^{n} + u_{j - 1}^{n}\bigg) + u_{j}^{n}$$

- $D$: the exact solution of the #FDE.
- $N$: the numerical solution of the #FDE using a computer having finite digits.
- $A$: the analytical solution of the #PDE
- ==*Discretization Error = $A - D$*==
- ==*Round-Off Error (#ROE) = $N - D$*==

Determining #stability for a certain numerical scheme is easier rather than showing #convergence. Based on #Lax-Equivalence-Theorem, we focus on the #stability instead of directly analyzing the #convergence.

## von Neumann
!!! note Theorem
	An #FD scheme $Pu^{\*} = 0$, where $u^{\*}$ is an approximated solution to the true solution, $u$ is #stable if $$||{u^{\*}}^{n + 1}|| \leq (1 + c\Delta t)||u^{n}||\text{,}$$ for some $c \geq 0$ independent of $\Delta t$, and $n$ is the time step.

The exact solution, $D$ and the error, $\epsilon$ must both satisfy the same difference equation, which means that the *the #ROE and the exact, numerical solution both have the same growth property in time and either could be used to examine #stability*. Any perturbation of the input values at the $n^{th}$-time leve will either be prevented from growing without bound for a #stable system or will grow larger for an #unstable system.

==*Numerical Solution: $N = D + \epsilon$*==

We use the #Fourier-Transform that transfers a time-spatial domain to a frequency domain. Suppose $u_{j}$ is a function on grid points and $\hat{u}(\xi)$ the corresponding function on the frequency domain. The #Fourier-Transform of this function:...

We apply the function on the frequency domain: $$u_{j} = \frac{1}{\sqrt{2\pi}}\int_{-\infty}^{+\infty}\boxed{e^{ij\Delta x\xi}\hat{u}(\xi)}d\xi$$

!!! example Heat equation with Forward-Euler.
	$$\begin{split}
	\frac{(u_{j}^{n + 1} - u_{j}^{n})}{\Delta t} &= \frac{\alpha}{(\Delta x)^{2}}\bigg(u_{j + 1}^{n} - 2u_{j}^{n} + u_{j - 1}^{n}\bigg) \text{, } \mu = \frac{\alpha\Delta t}{(\Delta x)^{2}} \\\\
	u_{j}^{n + 1} &= \mu u_{j + 1}^{n} + (1 - 2\mu)u_{j}^{n} + \mu u_{j - 1}^{n} \\\\
	 &= \frac{1}{\sqrt{2\pi}}\int_{-\infty}^{+\infty}\boxed{e^{ij\Delta x\xi}\hat{u}^{n + 1}(\xi)}d\xi = \frac{1}{\sqrt{2\pi}}\int_{-\infty}^{+\infty}\mathscr{F}(\xi)d\xi \\\\
	\mathscr{F}(\xi) &= (\mu e^{i(j + 1)\Delta x}\hat{u}^{n}(\xi) + (1 - 2\mu)e^{i(j)\Delta x\xi}\hat{u}^{n}(\xi) + \mu e^{i(j - 1)\Delta x\xi}\hat{u}^{n}(\xi)) \\\\
	 &= \boxed{e^{ij\Delta x\xi}\hat{u}^{n}(\xi)\big(\mu e^{i\Delta x\xi} + (1 - 2\mu) + \mu e^{-i\Delta x\xi}\big)} \\\\
	\hat{u}^{n + 1} &= \big(\mu e^{i\Delta x\xi} + (1 - 2\mu) + \mu e^{-i\Delta x\xi}\big)\hat{u}^{n}
	\end{split}$$

	!!! question Is $i$ an indexing number? <cite> DK
		No. $i$ is the imaginary component for the #Fourier-Transform! **Only $j$ is the index here!**

	Subsituting $\nu = \Delta x\xi$,

	$$\begin{split}
	\hat{u}^{n + 1} &= \big(\mu e^{i\nu} + (1 - 2\mu) + \mu e^{-	i\nu}\big)\hat{u}^{n} \\\\
	 &= G\hat{u}^{n}
	\end{split}$$

	G is called the #amplification-factor. We would like to have $|G| \leq 1$ for #stability!

	$$\begin{split}
	G &= \mu e^{i\nu} + (1 - 2\mu) + \mu e^{-i\nu} \\\\
	 &= (1 - 2\mu) + 2\mu\cos(\nu) = 1 - 4\mu\sin^{2}(\frac{\nu}{2}) \\\\
	|G| &= \bigg|1 - 4\mu\sin^{2}(\frac{\nu}{2})\bigg| \leq 1
	\end{split}$$

	!!! info
		Recall that:
		$$\begin{split}
		e^{i\beta} &= \cos(\beta) + i\sin(\beta) \\\\
		\cos(\beta) &= \frac{e^{i\beta} + e^{-i\beta}}{2} \\\\
		\sin(\beta) &= \frac{e^{i\beta} - e^{-i\beta}}{2} \\\\
		\sin^{2}(x) &= \frac{1}{2}(1 - \cos(2x)
		\end{split}$$

	!!! attention
		This scheme is only stable **if and only if** $0 \leq \mu \leq \frac{1}{2}$

## Boundedness
Numerical solutions should lie within proper bounds. E.g. physical quantities such as density and kinetic energy of turbulence must be positive, while concentration should be between $0$ and $1$. In the absence of sources and sinks, some variables are required to have maximum and minimum values on the boundary of the domain. This property is also called the #maximum-principle.

## Equilibrium Problems
Many of the ideas for #marching-problems are applicable to equilibrium problems excepting the #stability. #convergence for equilibrium problems is a different concept:

- Algebraic system of equations that needs to be solved only once rather than marching (#stability not applicable).
- We need to control the error in solving the equations as the mesh is refined for "truncation convergence".
- Many common schemes are iterative: e.g. #Gauss-Seidel.
- Iteration convergence implies that the changes between successive iterations can be made as small as we wish for every gird point ($|u_{i, j}^{n + 1} - u_{i, j}^{n+1}| < \epsilon$).
- Direct solvers can also be used without iterations.

## Conservation
When the equations to be solved are from conservation laws, the numerical scheme should respect these laws both locally and globally. This means that the amount of a conserved quantity leaving a control volume is equal to the amount entering to adjacent control volumes. If divergence form of equations, $\nabla\dot{u}$, and a finite volume method is used, this is readily guaranteed for each, individual control volume and for the whole solution domain. Non-conservative schemes may produce some artificial sources or sinks, changing the balance locally or globally. However, non-conservative schemes can be consistent and stable, and may therefore elad to correct solutions in the limit of mesh refinement; error due to non-conservation is appreciable in most cases only when the mesh is not fine enough. *The problem is that it is difficult to know on which mesh the non-conservation error is small enough.* Conservative schemes are thus preferred.

This idea of #conservation may be more applicable to #CFD people using a control volume. Under limited conditions

*[CFD]: Computational Fluid Dynamics

#conservation is a property of #FDE. #PDE of interest are based on physical conservation statements and are valid for the local region around a point as well as globally. A #FD scheme that maintains a discrete version of the conservation statement exactly for any mesh size over an arbitrary, finite region has the conservative property. In essence, we check to see if the discretized version of the divergence theorem is satisfied: all internal points cancel and only boundary points representing boundary fluxes remain:

$$\begin{equation}
\nabla\cdot\rho\mathbf{V} = 0
\label{eq:steady_flow_continuity}
\end{equation}$$

$$\begin{equation}
\iiint\nabla\cdot\rho\mathbf{V}dR = \oiint\rho\mathbf{V}\cdot\mathbf{n}dS
\label{eq:application_of_divergence_theorem}
\end{equation}$$