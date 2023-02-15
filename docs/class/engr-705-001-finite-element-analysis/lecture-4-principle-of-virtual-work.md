<!-- 20230126T09:07 -->
# Lecture 4: Principle of Virtual Work
Work of Force
: The work done by a force acting on a particle moving along a path during a displacement $d\vec{r}$ is defined as the product of the component of the force in the direction of the displacement and the magnitude of the displacement.

Mathematically, work is expressed as: $$dU = F\cos(\theta)ds \text{ or } dU = \vec{F} \cdot d\vec{r}$$
In general, $$\begin{split}
U_{1 - 2} &= \int_{s1}^{s2}\vec{F} \cdot d\vec{r} \\
 &= \int_{s1}^{s2}(F_{x}\hat{i} + F_{y}\hat{j} + F_{z}\hat{k}) \cdot (dx\hat{i} + dy\hat{j} + dz\hat{k})
\end{split}$$

## Work in Terms of the Tangential Force
We observe that the component of the force in the direction of the displacement is the tangential force, $F_{t}$.
$$U_{1-2} = \int_{s1}^{s2}F\cos(\theta)ds = \int_{s1}^{s2}F_{t}ds$$

## Work of a Constant Force in Rectilinear Motion
For a particle moving along a straight line subjected to a constant force, the work is given by: $$U_{1-2} = \int_{s1}^{s2}F\cos(\theta)ds = F\cos(\theta)\Delta s$$

<!-- 20230131T08:21 -->

!!! note Minimum Principle Energy
    This is an example of a variational method but only applies to linear elastic systems.
    Unless stated otherwise, systems are typically assumed to be linear.

## Example Problem: Set 2-2
### 1
$$\begin{split}
x_{B} &= 0.9\cos(\theta) \\
x_{C} &= 2(0.9)\cos(\theta)
\end{split}$$
These two equations are differentiable.
$$\begin{split}
\delta x_{B} &= -0.9\sin(\theta)\delta\theta \\
\delta x_{C} &= -1.8\sin(\theta)\delta\theta
\end{split}$$
Virtual Work: the total work is determined at $\delta U = 0$.
$$\begin{split}
P\delta x_{B} + F_{sp}\delta x_{C} &= 0 \\
6(-0.9\sin(\theta)\delta\theta) + 20(0.9-1.8\cos(\theta))(-1.8\sin(\theta)\delta\theta) &= 0 \\
[-5.4\sin(\theta) - 36(0.9-1.8\cos(\theta))\sin(\theta)]\delta\theta &= 0 \\
\delta\theta \neq 0, \therefore -5.4\cancel{\sin(\theta)} - 36(0.9-1.8\cos(\theta))\cancel{\sin(\theta)} &= 0 \\
0.9-1.8\cos(\theta) &= \frac{5.4}{36} \\
-1.8\cos(\theta) &= \frac{5.4}{36} - 0.9 \\
\cos(\theta) &= \bigg(-\frac{5.4}{36} - 0.9\bigg)/-1.8 \\
\theta &= \cos^{-1}\Bigg[ \bigg(\frac{5.4}{36} + 0.9\bigg)/1.8 \Bigg] \\
\theta &\approx 54.31 \degree
\end{split}$$

### 2
A virtual displacement $\delta\theta$ is applied to the system.
Virtual displacements: the position coordinates are determined.
$$\begin{split}
x_{B} &= r\theta = 0.5\theta
\end{split}$$
Differentiating this expression:
$$\begin{split}
\delta x_{B} &= 0.5\delta\theta
\end{split}$$
The total virtual work is determined from $\delta U = 0$.
$$\begin{split}
-F_{sp}\delta x_{B} + M\delta\theta &= 0 \\
-4000(0.5\theta)(0.5\delta\theta) + 300\delta\theta &= 0 \\
[-1000\theta + 300]\delta\theta &= 0 \\
\delta\theta &\neq 0 \\
\therefore \theta &= 0.3 rad \equiv 17.2 \degree
\end{split}$$