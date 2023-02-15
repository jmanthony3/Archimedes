<!-- 20230209T13:42 -->
# Lecture 8: State Variables
## Chaboche Paper
State Variables
: The method of local state postulates that the thermodynamics state...

Observable Variables
: The formalism of continuum mechanics 

Internal Variables
: ... the current state...

The dissipation potential is assumed to be a continuous, convex function.
The gradient along this potential defines the conjugate pair of stress and plastic flow (which is orthogonal to the surface via the partial derivative wrt strain rate).
This means that the dissipation potential is always greater than equal to zero.
This relationship is the *flow rule* aka **plastic flow function**.

<!-- 20230214T12:49 -->

### Thermodynamics
Sub-structures are considered too low a length scale and internal to the overall structure.
Their effects are not directly observable: e.g. dislocation kinetics.
In the continuum length scale, we homogenize the lower length scale effects and consider these effects as state variables internal (hidden) to the local structures.
These variables evolve with time and are dependent on previous states.
Therefore, we must track the history of these local, internal variables.

Some variables can be simply observed: e.g. temperature.
Stress fields are not directly observable and do not give complete insight to material history because grain evolution changes the residual stresses.

Convexity
: The potential energy associated with some internal variable is a convex curve whose minimum occurs when the internal variables is zero.
A consequence of this is that the yield surface in the plastic flow rule is also convex (Drocker paper).

Associative Flow Rule
: The yield surface grows orthogonally in all directions which is *normality*.
==This assumption is used in the ISV codes.==

Normality
: We assume that the plastic strain rate and stress evolve in the same direction.

## Coleman-Gurtin Paper
The first paragraph outlines three different ways to approximate plastic dissipation:
1. Use only the current configuration and its observable variables.
2. Principle of Fading Memory tracks the history of observable variables but gives greater weight to more recent "memories" of variables.
3. Internal State Variables constituted by differential equations are postulated to exist whose entire history is in accordance to 2nd Law of Thermodynamics.

The principle of equipresence outlines that all internal state variables must be present in all constitutive equations.