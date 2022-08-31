# lesson-15-stress-concentration

3. Failure Modes
   1. Historical Perspective
      1. Fracture of molasses tank in Boston 1919.
      2. 2 million gallons.
      3. 12 dead, 40 injured, many horses shot.
      4. Litigation.
      5. Much technical disagreement on cause.
   2. Why do some structures fracture when others yield?
      1. Material selection.
      2. Overall load situation.
      3. Details.
4. Stress Concentrations
   1. When a "perfect" solid is loaded in tension, the normal stress is the same in an part of the specimen.
   2. If a flaw exists inside the specimen, then the free surface cannot transmit any load.
   3. The material adjacent to the crack must carry the load.
   4. The stress is **concentrated**.
5. Stress concentration
   1. Bending: $\sigma_{nom} = \frac{Md}{I}$.
      1. $\sigma_{max} = K_{t}(\frac{Md}{I})$.
      2. $K_{t}$ is the geometric stress concentration factor on the normal stress.
   2. Shear: $\tau_{nom}$
      1. $\tau_{max} = K_{ts}\tau_{nom}$.
      2. $K_{ts}$ is the geometric stress concentration factor on the shear stress.
   3. **Unitless*- **<<<<-------- _QUIZ!!!_**
6. The stress concentration factor, $K_{t}$
   1. Inglis showed the state of stress of a plate with an elliptical hole to be: $$\sigma_{max} = \sigma_{gross}(1 + \frac{2a}{b})$$
   3. When $a$ increases, $\sigma_{max}$ increases. More crack like.
   4. If $b$ increases, $K_{t}$ decreases to $1$. More void like.
   5. If $a = b$, $K_{t} = 3$.
7. cont...
   1. Radius of curvature, $\rho = \frac{b^{2}}{a}$.
   2. This can be combined to show, $\sigma_{max} = \sigma_{gross}(1 + 2\sqrt{1 + \frac{a}{\rho}}$),
   3. where $K_{t} = (1 + 2\sqrt{1 + \frac{a}{\rho}})$
8. Typical Stress Concentrations

$\frac{a}{b}$ | $K_{t}$
-|-
$\frac{1}{1}$ | 3.0
$\frac{1}{4}$ | 1.5
$\frac{4}{1}$ | 9.0
$\frac{10}{1}$ | 21
$\frac{100}{1}$ | 201

9. Stress Concentration: Hole
   1. Discontinuities of cross-section may result in high localized or _concentrated_ stresses.
   2. $K = \frac{\sigma_{max}}{\sigma_{avg}}$
   3. $\sigma_{avg}$ is that internal stress reacting to the remote force. 
   4. $\sigma_{max}$ is an increase of $\sigma_{avg}$ when a void is included within the cross-section, because there is less area to apply the internal stress load over and the increase of radius of curvature.
10. Stress Concentration: Fillet
    1.  Notch roots of fillets
11. cont...
    1.  $K_{t}$ is only geometry dependent, not the boundary conditions.
12. Designing to minimize notch roots
13. Stress intensity factor, $K_{I}$
    1.  Background
    2.  Griffith: F-111 Wing Pivot Fitting
14. Case Study
    1.  River marks at the dimple point to the location of failure.
    2.  Fatigue shows beach striations at the microstructure level.
    3.  However, river marks at the naked eye points to the initiation point.
15. Damage tolerance concept
    1.  All materials have flaws, so we'll live with it.
    2.  Largest flaw is just smaller than you can detect.
    3.  Inspection intervals set by smallest detectable flaw and crack growth rate expected based on flight loading
16. What this mean for failure analysis?
    1.  Brittle or mostly elastic materials
17. Ductile materials
    1.  Failure stress goes down, because it would have been elastic.
        1.  Notch facilitates growth of voids (triaxiality).
        2.  Locally increases stress.
    2.  Yield stress can go up (notch root strengthening).
        1.  When is "yield"? GM says failure, Ford says elastic yield.
    3.  In practice, notches are always bad since fatigue life always worsens with notches.