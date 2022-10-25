<!-- 220308 -->
# Dislocation Dynamics Methods

This gives insight to plasticity of dislocation motion.

## Introduction
Dislocations can be broken down into 3 categories: point (0D), line (1D), and volume defects (2D).
Edge and screw dislocations cause dislocations to move parallel and perpendicular to the burgers vector.
Critically resolved #shear-stress relies on the schmidt factor to calculate the #shear-stress required in plane to cause local yielding from some applied, external loading condition.
Dislocations typically move by either glide (plasticity/dynamic recovery) or climb (thermal/static recovery/creep).

## Molecular Dynamics
Strain hardening and ultimate failure comes form dislocations multiplying together.
This requires short time scale because of the thermal vibrations of atoms: in the order of femtoseconds.
Molecular dynamics operates at the microscale for #single-crystals to bridge the difficulty of the time scale limitations.

### Basic Geometry
Typically, dislocations are taught to be linear in shape, but, in actuality, dislocations are round.
$\xi$ is the sense of the dislocation velocity: solved by balancing Newton Laws of Motion during dislocation motion.

### Equation of Motion
This uses basis functions (think PDE) to solve for behavior between nodal points in the discretized space on the dislocation line.

$$\begin{equation}
\begin{split}
m_{s}\dot{v} + \frac{1}{M_{s}(T, P)}v &= F_{s} \\
\frac{1}{M_{s}} &= B \text{, Drag Coefficient} \\
F_{s} &= F_{Peierls} + F_{d} + F_{self} + F_{external} + F_{obstacle} + F_{image} + F_{osmotic} + F_{thermal}
\end{split}
\end{equation}$$

Dislocations do not actually have mass, but dislocation lines are assumed to be an entity of some effective mass per line length.
The drag coefficient is what is upscaled into MD.
As the lattice vibrates, **phonons** (a pseudoparticle) block dislocation motion.
Peierls stress is the #residual-stress (effectively is friction) at 0 *K* because some force is required to overcome this limit.
This is not equivalent to #yield-stress ; although, they are similar, Peierls stress does not into account local defects and is largely based on slip in pure crystals.

$$\begin{equation}
\begin{split}
m_{s, screw} &= \frac{W_{0}}{asdf} \\
 &=
\end{split}
\end{equation}$$

**Dislocation Stress and Force Field**
Stress induced by any dislocation at a point $P$ can be computed by the Peach-Koehler integral equation.
This will not be on the exam: Dr. Cho simply wants us to know what gets upscaled and what the big picture is.

$$\begin{equation}
\sigma_{ij}^{d} = \sum_{l = 1}^{N_{l}}\sum_{s = 1}^{N_{s}^(l)}\Biggl{-\frac{G}{8\pi}\intb_{p}\in_{mpi}\frac{\partial}{\partial x_{m}'}\nabla'^{2}...\Biggr}
\end{equation}$$

Stress as each nodal point, $P$ can be decomposed.
Locals forces can be found between nodes which are needed because this is the solution to $Ax = B$.

### Upscaling for Plasticity
$$\begin{equation}
\dot{\epsilon}^{p} = \sum_{s = 1}^{N_{s}}\frac{l_{s}v_{s}}{2V}(n_{s}\otimes b_{s} + b_{s}\otimes n_{s})
\end{equation}$$

$$\begin{equation}
\begin{split}
\dot{\kappa} &= h_{0}(\frac{\kappa_{s} - \kappa}{\kappa_{s} - \kappa_{0}}) \\
\kappa &= \begin{cases}
\kappa_{s} - (\kappa_{s} - \kappa_{0})\exp(-\frac{h_{0}}{\kappa_{s} - \kappa_{0}}Ct) & \text{Palm and Voce} \\
\alpha\mu b\sqrt{\rho_{f}}
\end{cases}
\end{split}
\end{equation}$$

### Downscaling to Atomistics
Dislocation velocity according to distlocation:

$$\begin{equation}
v = \begin{cases}
0 & \text{, if } \tau* \leq 0 \\
sign(\tau*)\frac{\tau*b}{B} & \text{, if } \tau* > 0
\end{cases}
\end{equation}$$

<!-- 220329 -->
<!-- 220331 -->