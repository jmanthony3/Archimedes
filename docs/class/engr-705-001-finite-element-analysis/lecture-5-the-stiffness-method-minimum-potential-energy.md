<!-- 20230131T09:07 -->
# Lecture 5: The Stiffness Method: Minimum Potential Energy
This a variational approach that relies on variational calculus.
We will not get into variational calculus, but we will see how to minimize functionals.

## Minimum Potential Energy Approach
Alternative method often used to derive the element equations and stiffness matrix.
More adaptable to the determination of element equations for complicated elements such as:
- Plane stress/strain element
- Axisymmetric stress element
- Plate bending element
- Three-dimensional solid stress element

Principle of minimum potential energy is only applicable to elastic materials.
The method of virtual work is applicable for any material behavior.
This minimum potential energy approach is classified as a variational method.

## Conservative Forces
Conservative Force
: A force $F$ acting on a particle is said to be conservative if the work done between two points is independent of the path.

It is: $$U_{1-2} = V_{1}(x_{1}, y_{1}, z_{1}) - V_{2}(x_{2}, y_{2}, z_{2})$$
Then, we can write: $$U_{1-2} = V{1} - V_{2}$$
Where $V = (x, y, z)$ is the potential energy function.
The work done by a conservative force along a closed path is zero...

### Gravitational Potential Energy
Consider a body of weight, $W$ which moves from point $q$ to $2$.
The work performed is: $$U_{1-2} = Wy_{1} - Wy_{2}$$
It is seen...

### Elastic Potential Energy
Consider a particle attached to a spring that is moving from position $1$ to $2$.
Previously, the work has been calculated as: $$U_{1-2} = \frac{1}{2}ks_{1}^{2} - \frac{1}{2}ks_{2}^{2}$$
...

### Total Potential Energy
The total potential energy, $\pi_{p}$ of a structure is expressed in terms of displacement.
In the finite element formulation, these will generally be nodal displacements such that $\pi_{p} = \pi_{p}(d_{1}, d_{2}, \dots, d_{n})$.
When $\pi_{p}$ is minimized with respect to these displacements, equilibrium equations result.

Principle of Minimum Potential Energy
: Of all the geometrically possible shapes that a body can assume, the true one, corresponding to the satisfaction of stable equilibrium of the body, is identified by a minimum value of the total potential energy.

The sum of the internal strain energy, $U$, and the potential energy of the external forces, $\Omega$.

$$\begin{equation}
\pi_{p} = U + \Omega
\end{equation}$$

Strain Energy
: The capacity of internal forces to do work through deformations in the structure.

The potential energy of external forces is the capacity of forces such as bode forces, surface traction forces, or applied nodal forces to do work through deformation of the structure.

## Concept of External Work
A force is applied to a spring and the force-deformation is given.
The external work is given by the area under the force-deformation curve where the slope is equal to....

## Total Potential Energy of Spring
The strain energy can be expressed:

The potential energy of the external force, being opposite in sign form the external work expression because the potential energy of the external force is lost when the work is done by the external force, is given by:

therefore, the total potential energy of a spring is:

<!-- 20230202T08:15 -->

!!! note
    Some of the methods discussed in this class are remarkably similar to each other, but ultimately produce the same equations.

## Example Set 2-3
### Problem 1
**Problem Statement**
The uniform rod has a mass of $100~kg$.
If the spring is unstretched when $\theta = 60 \degree$, determine the angle $\theta$ for equilibrium and investigate the stability at the equilibrium position.
The spring is always in the horizonal position due to the roller guide at $B$.

**Solution**
The internal strain energy of the system is: $$\begin{split}
U &= \frac{1}{2}kx^{2} - Wy \\
x &= 2\sin(60 \degree) - 2\sin(\theta) \\
y &= 2\cos(\theta)
\end{split}$$
The work of the internal forces: $$\begin{split}
\Omega &= 0 \\
\pi_{p} &= \frac{1}{2}k(2\sin(60 \degree) - 2\sin(\theta))^{2} - W(2\cos(\theta)) \\
 &= \frac{k}{2}(\sqrt{3} - 2\sin(\theta))^{2} - 2W\cos(\theta)
\end{split}$$
The principle of minimum potential energy is applied: $$\begin{split}
\frac{\partial \pi_{p}}{\partial \theta} &= 0 \\
0 &= k(\sqrt{3} - 2\sin(\theta))(-2\cos(\theta)) - 2W(-\sin(\theta)) \\
 &= -2k\sqrt{3}\cos(\theta) + 4k\sin(\theta)\cos(\theta) + 2W\sin(\theta) \\
0 &= -1000\sqrt{3}\cos(\theta) + 2000\sin(\theta)\cos(\theta) + 1962\sin(\theta) \\
\text{Solving for } \theta: \theta &\approx 0.43 rad \equiv 24.62 \degree
\end{split}$$

### Problem 2
**Problem Statement**
A slender rod, $AB$ of weight, $W$ is attached to two blocks $A$ and $B$ that can move freely in the guides shown.
Knowing that the spring is unstretched when $y = 0$, determine the value of $f$ corresponding to equilibrium when $W = 80~N$, $I = 500~mm$, and $k = 600~N/m$.

**Solution**
The internal strain energy is calculated: $$\begin{split}
U &= \frac{1}{2}ks^{2} - \frac{1}{2}W \\
s &= d - \ell \\
 &= \sqrt{y^{2} + \ell^{2}} - \ell \\
U &= \frac{1}{2}k[\sqrt{y^{2} + \ell^{2}} - \ell]^{2} - \frac{1}{2}Wy
\end{split}$$
The work of the external forces is: $$\Omega = 0$$
The total potential energy is: $$\pi_{p} = \frac{1}{2}k[\sqrt{y^{2} + \ell^{2}} - \ell]^{2} - \frac{1}{2}Wy$$
The principle of minimum potential energy is applied: $$\begin{split}
\frac{\partial \pi_{p}}{\partial y} &= 0 \\
0 &= \frac{k}{2}[\sqrt{y^{2} + \ell^{2}}](y^{2} + \ell^{2})^{-1/2}(2y) - \frac{1}{2}W \\
ky[1 - \ell/\sqrt{y^{2} + \ell^{2}}] &= \frac{W}{2} \\
(600)y[1 - 0.5/\sqrt{y^{2} + (0.5)^{2}}] &= \frac{80}{2} \\
\text{Solving for }y: y &\approx 0.537 m
\end{split}$$