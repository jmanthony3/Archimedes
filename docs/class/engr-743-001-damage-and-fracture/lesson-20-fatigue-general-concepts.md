# Lesson 20: Fatigue (General Concepts)

1. Most fatigue problems (which include thermal) are from vibrations: 1-20,000 Hz
   1. Vehicles are designed not to vibrate between 4-10 Hz, because that is the resonant frequency of the human body
   2. Presented at the 9th International Fatigue Congress.
   3. Early computers would be shipped to customers and not work, because the EE's never had ME's part of the design team.
   4. Ford uses the elastic limit, which means they are more concerned of fatigue, because of a shorter S-N curve.
2. Notch roots affect incubation rates of cracks.
   1. $\frac{da}{dN}$: the longer crack has a steeper slope, because its crack driving force is greater.
3. Long-cracks are visible when cracks no longer more around grain, but straight through. Sometimes labelled as Mode 1, 2, or 3
4. Local dislocations initially make the material harder at that location, but also where damage begins.
   1. Length scales matter, because when the ratio of diameter to length of a dislocation's shape exceeds 0.3, the results were equivalent.
   2. Macro-scale: doesn't matter. If looking for incubation in first few cycles, then yes. But this is all _high-cycle fatigue_.
   3. _High-cycle fatigue_: elastic regimes of material
   4. _Low-cycle fatigue_: all plastic range
   5. $R =\frac{\sigma_{min}}{\sigma_{max}}$ in the cycle. If $R < 0, R=-1$.
   6. Usually good in compression.
>Different phenomenological events require different expressions of math. <cite> MFH
5. Fatigue was thought to be a function of stress (for 80 yrs.); however, found to be **strain life**.
   1. Jim Newman (NASA) bridged the crack people from 1920 and the fatigue people working for 50 years with _stress life_ into using crack growth and strain life.
   2. MFH and Doug Buamann introduced "incubation". Previously, fatigue people called this initiation.
   3. Fatigue load is greater in real materials than ideal.
   4. Monotonic overload in the last half-cycle of a specimen indicated by striations and coupled with dimples.
   5. Fatigue needs a fatigue crack to be considered (necessary and sufficient). It is necessary to see dimples on the fracture surface, but not sufficient.
6. Intrinsic vs. Extrinsic toughening: resistance of a material within the material to deformation
   1. Intrinsic: before crack (internal to the material)
   2. Extrinsic: after (behind) the crack
   3. Also includes _grain bridging_
      1. Frictional effects (dissipative but into the crack tip). All energy transfer.
      2. Oxides are good examples of extrinsic: does formations of oxides on a reactive metal help to impede or increase crack growth?
         1. _It depends_ on the ductile material.
         2. If an already brittle material, no, because it will not yield much anyway.
         3. If a ductile material, it may help impede the crack growth.
      3. Anything that impedes the crack tip propagation, this reduces the crack driving force (can limit the crack tip from opening the material).
   4. Crack closure: 
      1. elastic regime and opening things up
      2. Where is the plastic regime, near the dislocations.
      3. Stress-strain curve: material goes back with "back" stress (kinematic hardening) if in plastic regime.
      4. This back stress will resist the crack wake from opening.
      5. Affected by the direction of dislocations.
   5. Plastic zone around crack tip is _intrinsic toughening_.
      1. Seen by misaligned grains/dislocations
      2. Difference between long-cracks and microstructure cracks is the length scale. If a crack is growing, then at some point (while still creating more intrinsic stresses by back stress) the crack driving force exceeds those back stresses and blows right through the material.
   6. San Andreas fault--super long crack--driven by tectonic plate movement, driven by the mantle, driven by convection currents, created by the Genesis flood.
7. Rob Richie creates "resistance curves", but excludes Jim Newman's wake plasticity (which we know that plasticity is ductile).
   1. Resistance can increase, locally while crack grows.
   2. If resisted by a dislocation/grain, then the crack goes around, which increases the crack length.
8. Stress-time curves
   1. minimum stresses are negative, and if asymmetric, there is a mean stress, ($R \neq -1$). Aka creep fatigue.
   2. Use FFT to move from the time domain to the frequency domain for random vibrations.
9. Cyclic stresses
   1.  Sometimes, these S-N curves are for "2N" for reversals.
   2.  **TEST/QUIZ**
   3.  Stress amplitude is usually what is plotted for S-N curves and stress-time curves.
   4.  $\sigma_{m} = \frac{\sigma_{max} + \sigma_{min}}{2}$
10. Fatigue limit: stress does not change for infinite cycles.
    1.  Dislocations affect the local yielding which will cause failure locally.
    2.  Companies will define these fatigue limits for marketing purposes.
    3.  **The limit at which the material can cycle forever.**
    4.  It can be right, if:
        1.  Single crystal of monolithic material with no defects.
        2.  But they are so small, difficult to test.
        3.  Real engineering includes all the phases of dislocations.
        4.  This, then, becomes a design limit.
11. Fatigue strength: the point at which fracture occurs after specified number of cycles. Not necessarily fatigue limit.
    1.  Fatigue life is how many cycles.
    2.  The termination of the curve is where the specimen will break, period.
    3.  Same shape for high-cycle, low amplitude or the converse.
12. Just use the modulus or cyclic stress-strain curve to move from stress-strain to fatigue life.
    1.  Crack size is associated with strain life curves (these ideas did not come together until MFH in the 90's).
13. Crack initiation/propagation (old terms)
    1.  **Not incubation**:
14. Stage I and II:
    1.  Differ from initiation/propagation
    2.  I is orthogonal to stress and parallel to crack (mechanics people: Mode II)
    3.  II (crack people saw fcc materials create cracks at $45^{\circ}$).
15. Crack gets pinned by hard grains or particles such that $\frac{da}{dN}$ goes to zero, then the crack moves around the resistant point to something else.
    1.  x-axis is cycle.
    2.  y-axis is $\frac{da}{dN}$ increment.
    3.  long-crack growth models cannot capture this propagation, because the increment is up and down
16. History of fatigue: **_Surface-driven failure_**
    1.  It depends.
    2.  There is also free surface from pores/dislocation/impurities
    3.  MFH does not argue with fatigue people, but include the free surfaces from pores, oxides, etcetera. 
    4.  Quality of surface was the main focus.
    5.  Fatigue specimens required 10 0.02" cuts on the gauge section, which makes it more expensive from the standard 0.05"
    6.  Polishing didn't want to induce residual stresses.
        1.  Accomplished by peening, to induce a mean stress by minimizing the max tensile load.
        2.  However, this also hardens the material by inducing more dislocations.
        3.  Case arming: diffusing carbon into the surface of steels to increase the yield strength.
        4.  Smooth, gentle curves in the geometry to minimize the notch root radius and subsequent stress.
17. Environment effects
    1.  Very different from mechanical cycles.
    2.  Nuclear reactors shutdown every 3 months:
        1.  Thermal cycles: expected 120 for a 30 yr. service life.
        2.  However, reactors are now asked to operate 100yrs.
        3.  Can AM induce compressive stresses to help increase fatigue life?
    3.  Corrosion can cause extrinsic forces, but it can also increase crack growth rate.
        1.  MFH's Magnesium specimens formed oxides layers around the whole surface and pushed the incubation point to much later.
        2.  Cracks would be inhibited by the oxide layer.
        3.  Similar to carburizing the surface (oxidizing).
18. Definitions
    1.  First fatigue specimens were in bending, which was found different from uniaxial tension specimens, even if identical materials.
    2.  When in bending, only half the material experiences tension (either above/below the neutral axis)
    3.  Furthermore, the maximum stress (moving radially from the neutral axis) is at the surface: almost no volume to allow failure.
19. Crack propagation rate
    1.  Use $K_{ic} = \sigma\sqrt{\pi a}Y$ (stress intensity factor) for elastic materials.
    2.  If $a$ increases, $K_{ic}$ increases. Long-crack growth if plotted $\frac{da}{dN}|_{K_{ic}}$.
    3.  Slopes are equivalent at the same crack length, but displaced by stress onto microstructure of material.
    4.  MFH's MSF model moves up from strain-like at the lower length scale to stress-like at the higher length scale, which people do not like.
20. $\frac{da}{dN} = A(\Delta K)^{m}, \Delta K = K_{max} - K_{min}$.
21. Crack propagation rate
    1.  Use a math trick with "log" to bring down from an exponential equation.
    2.  This to solve, by integration, to find $N$ to predict cycles to failure.
    3.  Whichever fatigue life is longer, you can save volume there to minimize weight, but may need to put some where the fatigue life is lowest.
22. To improve fatigue life:
    1.  Induce compressive stresses
    2.  Large, uniaxial tension will yield fewer cycles
    3.  Carburizing 
    4.  Polishing