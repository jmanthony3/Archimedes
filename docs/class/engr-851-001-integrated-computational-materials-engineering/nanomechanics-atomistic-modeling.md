<!-- 220308 -->
# Nanomechanics: Atomistic Modeling

## Introduction
**Downscaling Issues**
Stress, strain, plasticity, strain rate effects, temperature effects, Bauschinger effects.

Methods used depend on the entity being modeled
| Method  | Entity   | Example   |
|-------------- | -------------- | -------------- |
| Item1    | Item1     | Item1     |

## Energy
Observing the relationship defined in [Eq. 2](#eq-eam) can be expanded into [Eq. 3](#eq-meam) by accounting for angular dependence of atoms within a background electron density.
1. Molecular dynamics (MD): based on $F = ma$ at finite temperatures
2. Molecular Statics (MS): quasi-static, rate-independent at absolute zero
3. Monte Carlo Simulations (MCS): quasi-static with random distributions at finite temperatures (e.g. Dr. Cho’s Earth mantle simulations)

**Determination of Atomic Stress Tensor**
We recall that Cauchy observed *traction forces* through vectors acting over some area to define *traction stress* within a **continuum** of material.
Atomistic simulations are dis-continuous in nature; therefore, stresses must be defined slightly differently.
(M)EAM potentials determined by $E = \sum_{\alpha}\Biggl(F(\bar{\rho_{\alpha}}) + \frac{1}{2}\sum_{\gamma \neq \alpha}\phi(r^{\alpha\gamma})\Biggr)$ ([Eq. 2](#eq-eam), [Eq. 3](#eq-meam)) with local forces ([Eq. 8-23](#eq-local_force)) determined from energy.

$f^{\alpha} = -\nabla_{\alpha}E$

$$\begin{equation}
\beta_{ij}^{\alpha} = -\frac{1}{V}m^{\alpha}v_{i}^{\alpha}v_{j}^{\alpha} - \frac{1}{2V}\sum_{\gamma \neq \alpha r_{i}^{\alpha\gamma}f_{j}^{\alpha\gamma}}
\end{equation}$$

The $V$ here is the atomic volume.
Note the difference between (M)EAM is the added degree of angular rotations that affect the electron density cloud $\bar{\rho_{\alpha}}$.
For EAM, this quantity is simply a scalar, but for MEAM it includes three terms that are physically motivated: $\bar{\rho_{\alpha}}$

## Kinetics
## 
## Kinematics