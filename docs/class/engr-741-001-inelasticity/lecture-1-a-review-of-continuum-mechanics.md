<!-- 20230117T13:41 -->
# Lecture 1: A Review of Continuum Mechanics
We assume that materials are continuous without defects.
Inelasticity expands on this but focuses on the viscoplasticity of the material [^ContinuumCourse].

[^ContinuumCourse]: Refer to the [course notes](../engr-725-001-continuum-mechanics.md) on *ENGR 725: Continuum Mechanics* for more details.

| ![](../../../attachments/knudsen-number/knudsen_number_diagram_221003_153822_EST.png) |
|:--:|
| $K_{n} = \frac{\lambda}{D}$ where $D$ is the length-scale parameter. So if what you are measuring is larger than the inspected length-scale (i.e. $K_{n} > 1$), then continuum mechanics can be applied. |

We refer to matrices representing physical quantities as "tensors".
The rank of that tensor is the number of free indices in that tensor.
- 0: scalar
- 1: vector
- 2: matrix
- 4: stiffness matrix

<!-- 20230119T12:48 -->

## Useful Identities
[Kronecker's Delta](../engr-725-001-continuum-mechanics/kroneckers-delta.md) can essentially be thought of as an identity matrix.
The [Permutation Tensor](../engr-725-001-continuum-mechanics/permutation-tensor.md) is widely used in rotation tensors.
==Recall the Permutation Tensor Kronecker's Delta Property!==

The Transformation Tensor can be used to derive the Mohr's Circle formulae.
This tensor is commonly used to transform a stress state into the principal stress state, which may be represented as a 3D ellipsoid, for analysis.

A tensor is said to be orthogonal if the inverse of the transpose is equal to the transpose of the matrix.

## Tensor Multiplication and Matrix Manipulation

<!-- 20230124T12:51 -->

## Interpretation of the Scalar Product
The number of dots prescribes the number of Dot Products to perform down to a scalar.
Each Dot Product contracts the tensor and reduces it by one rank.

## Eigenvalues and Eigenvectors
These can be ascribed as the major and minor axes of an ellipsoid.

## Divergence
The gradient of the inner product over the del of a tensor.
Remember the Divergence Theorem to translate from surface traction forces to body forces acting on the volume.

## Cauchy Formula
Stress tensor acting in the direction of the normal of the traction vector.
The shear stress is the tangent component of the traction vector which could be found by the Pythagorean Theorem or rotate the stress state.

<!-- 20230126T12:49 -->

## Kinematics
Difficult to capture material behavior under deformation without kinematics.
Recall that *Eulerian* descriptions are instantaneous and do not record historical values; whereas, *Lagrangian* includes time-history.
The advection term in the material derivative brings the history into the current configuration for *Eulerian* descriptions.
The variables used for either *Lagrangian* or *Eulerian* descriptions are similar; however, *Lagrangian* variables will typically be capitalized.

!!! note Dr. Cho's Research
    Simulations showing the change in grain size initially showed no change because Dr. Cho had yet to include the advective term in the *Eulerian* description which had been originally excluded from the Abaqus codes.
    Some *Eulerian* codes get around this limitation with Lagrangian particle tracking of a few particles in the domain; however, this is computationally expensive.

## Deformation Gradient Tensor
Known as a two-point tensor because it connects the *Eulerian* and *Lagrangian* descriptions.
We care primarily about rigid body:
1. Translation
2. Stretching (Deformation)
3. Rotation

The deformation gradient tensor does NOT include translation.
This tensor can be decomposed into the Stretch and Rotation tensors by decoupling (directly) into symmetric and skew-symmetric tensors, respectively, for infinitesimal strains.
For large deformations, you must perform polar UR-decomposition or include Green/Almansi Strain to accommodate non-linearities due to plastic deformation.
The determinant of this tensor gives the change in volume.

### Stretch Ratio
The right deformation tensor can be used to find the stretch ratios using the direction vector in the reference configuration, $\underset{\sim}{N}$.
The Right Deformation Tensor is the stretch ratio squared.
The stretch ratio maps to the stretching of the axes in the ellipsoidal representation of a 2-rank tensor.

### Fundamental Theorem of Polar Decomposition
$\underset{\sim}{F} = \underset{\sim}{R} \cdot \underset{\sim}{U}d\underset{\sim}{\mathbf{X}}$ or $\underset{\sim}{F} = \underset{\sim}{V} \cdot \underset{\sim}{R}d\underset{\sim}{x}$ gives the deformation for Eulerian or Lagrangian, respectively.

<!-- 20230131T12:48 -->

## Eulerian Rate of Deformation and Vorticity
Analogously, strain is a displacement gradient and strain rate is the velocity gradient.

!!! question Does that mean vorticity is the time-rate derivative of spin? <cite> DK
    Vorticity is the (spin/rotation) rate, not necessarily the gradient.

## Conservation of Mass
This implies that density and volume are not necessarily conserved because density can vary.
The continuity equation is *Eulerian* description and must include the total time derivative of density (the time derivative plus material derivative).
The second term is the rate change of volume, because it is a scalar density applied over a scalar field of velocity gradient in the the axial directions.

## Conservation of Linear Momentum
This relies on the Divergence Theorem to convert surface traction forces to body forces as the Cauchy stress tensor.

## Conservation Energy
This is the First Law of Thermodynamics related to thermal energy.
Previously, the term had been defined as the sum of kinetic and potential energies.
In mechanics, we define this as the sum of kinetic and internal energies which includes the potential energy with the addition of atomic kinetic energy.
Atomic energy is locally kinetic, but contributes globally to internal energies.

Mechanical power is composed of the kinetic energy and stress power.
Stress power contributes to internal energy.

The energy equation assumes that internal heat generation is fully reversible.

!!! example Example
    If you stretch a rubber elastically and unload it, the material will go back.
    But if you stretch it inelastically, there is internal heat generated in the material that dissipates and is lost to the environment which is unrecoverable.

The Second Law of Thermodynamics limits the direction of heat flowing from the First Law.
Changes in entropy will be greater than heat contribution and contributes to plastic deformation because atom bonds are being broken.
This is where ISV comes in to track where else this heat dissipates to.

<!-- 20230209T12:49 -->

## Thermodynamics
!!! attention 2nd Law of Thermodynamics
    ISV codes must always consider thermodynamics first for the kinetics.
    Any new variables must satisfy this 2nd Law (physical admissibility).

## Physical Admissibility
1. asdf
2. Principle of Local Action: only the deformation with an infinitesimal neighborhood of the point $\underset{\sim}{x}$ affects the material behavior at $\underset{\sim}{x}$.
3. Principle of Equipresence
4. Material Symmetry