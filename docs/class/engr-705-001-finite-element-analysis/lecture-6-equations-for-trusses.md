<!-- 20230202T09:05 -->
# Lecture 6: Equations for Trusses
Truss
: It is a structure composed of slender members joined together at their end points by means of bolts, rivets, pins, or welding.

Assumptions:
1. All the members are two-force members.
2. All the loads are applied at the joints.
3. The members are joined together by smooth pins.

There exists only tensile and compressive forces: no shear, bending, torsion, etcetera.

## Analysis of Trusses
### Method of Joints
The method consists of applying the equilibrium conditions to each joint of the truss.
Algorithm:
1. Draw the FBD of the complete structure to determine the reaction forces.
2. Draw a FBD for each joint.
3. Label all the joints with the corresponding letter.
4. Apply equilibrium to each joint along with Newton's Third Law of Motion.
5. A member in compression (C) "pushes" on the joint, and a member in tension (T) "pulls" on the joint.
6. If the right sense direction of a force is unknown, assume tension.

#### Normal Stress: Axial Force
Consider a bar of constant cross-sectional area $A$.
The ends of the bar are subjected to load $P$ passing through the centroid.

#### Normal Strain: Axial Loading
Consider the deformation of a prismatic bar due to the applied axial load $P$.
Normal strain is the deformation per unit length in the axial direction.
- Normal strain is a dimensionless quantity, since it is a ratio of two lengths.
- It is sometimes stated in terms of a ratio of length units.
- If the SI system is used, the measurements of strain are in micrometers per meter....

<!-- 20230207T08:22 -->

## Strain Energy
!!! quote <cite> Dr. Lugo
    By deforming a body, we are storing mechanical energy in the body.
    When we unload the body, the body tries to recover some of that energy.

As a material is deformed by an external loading, it tends to store energy internally throughout its volume.
This is referred to as *strain energy*.
The volume element is subjected to uniaxial stress.
This stress develops a force on the top and bottom faces of the element after the element of length undergoes a vertical displacement $B$.
The work done on the element by the force is equal to the average force magnitude times the displacement: $$\begin{equation}
\Delta U = \Bigg( \frac{1}{2}\Delta F \Bigg)\epsilon\Delta z = \Bigg( \frac{1}{2}\sigma\Delta x\Delta y \Bigg)\epsilon\Delta z = \frac{1}{2}\sigma\epsilon\DeltaV
\end{equation}$$
The strain energy density, $u = \frac{\Delta U}{\Delta V}$.

### Derivation of the Stiffness Matrix for a Bar Element
Consider the following bar subjected to tensile forces.
For this derivation, assume that:
- The bar element has a constant cross-sectional area, $A$, modulus of elasticity, $E$, and initial length, $L$.
- The bar cannot sustain shear force or bending moments.
- Any effect of transverse displacement is ignored.
- Hooke's Law applies, axial stress is related to axial strain.
- No intermediate applied loads.

By combining the strain/displacement...

Express the two force equations in matrix form.
We now have the local matrix form...

**Solving for Element Forces of the Bar Element**
Next, the element equations...

**Shape Function**
Represents the physical behavior of an element; that is a continuous function that represents the approximate behavior (solution) of an element.
- The deflection $u$ can be approximated by using a series of linear function, describing the deflection over each element or each section of the column.
- If a linear displacement variation along the $x$-axis of the bar is assume, the shape function is: $$u = a_{1}x + a_{2}$$

- The total number of degress of freedom, here, is two.

## Problem Set 3-1
### Problem 5
Determine the deflections of point D and point F in the system in the accompanying figure.
Also compute the axial force and stress in each member.

**Solution**
The system is divided into five elements.
The individual stiffnesses are evaluated, $k_{i} := \Big( \frac{AE}{L} \Big)_{i}$.
$$\begin{split}
k_{1} &= 1.45e6 \\
k_{2} &= 0.725e6 \\
k_{3} &= 7.25e6 \\
k_{4} &= 0.483e6 \\
k_{5} &= k_{4} \\
\end{split}$$

!!! question Why do we not consider the thickness? <cite> Caleb Cassidy
    This is a first-degree approximation in the principal dimension.
    Of course, we can include more dimensions, but this makes the process more complex: i.e. take longer and more expensive.

The global matrix:
$$[K] = \begin{bmatrix}
1.45+2(0.4833) & -1.45 & -2(0.4833) & 0 \\
-1.45 & 1.45 + 7.25 & -0.725 & 0 \\
-2(0.4833) & -0.725 & 0.725 + 7.25 + 2(0.4833) & -7.25 \\
0 & 0 & -7.25 & 7.25
\end{bmatrix}e6$$

$$\begin{split}
u_{2} &= 553e-6 in \\
u_{3} &= 275.69e-6 in
\end{split}$$

$$\begin{split}
\sigma^{(1)} &= 2.67~ksi \\
\sigma^{(2)} &= 
\end{split}$$

## Derivation of the Stiffness Matrix for a Bar Element in Local Coordinates
!!! note Recall properties of proper orthogonal matrices.
    Because the transformation matrix is properly orthogonal, the transpose instead of the inverse is used for calculations.
    - determinant of 1.
    - transpose equals the inverse.

<!-- 20230209T08:17 -->

## Problem Set 3-2
### Problem 1
Determine the displacement components at node 3 and the element forces for the plane truss shown below.
Let $A = 3~in^{2}$ and $E = 30 \times 10^{6}~psi$ for all elements.
Verify force equilibrium at node 3.

!!! hint Statically Indeterminate
    While this problem seems simple enough, it is actually statically indeterminant and cannot be solved with simple statics.
    We could use Castigliano's Theorem from Advanced Mechanics, but Finite Element Analysis does not care.