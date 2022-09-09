# Lesson 20: Fatigue (General Concepts)

See also: [Lesson 18: Fatigue](lesson-18-fatigue.md)

1. Most #fatigue problems (which include thermal) are from vibrations: 1-20,000 Hz
   1. Vehicles are designed not to vibrate between 4-10 Hz, because that is the resonant frequency of the human body
   2. Presented at the 9th International Fatigue Congress.
   3. Early computers would be shipped to customers and not work, because the EE's never had ME's part of the design team.
   4. Ford uses the elastic limit, which means they are more concerned of #fatigue, because of a shorter S-N curve.
2. Notch roots affect incubation rates of cracks.
   1. $\frac{da}{dN}$: the longer crack has a steeper slope, because its crack driving force is greater.
3. #long-crack are visible when cracks no longer more around grain, but straight through. Sometimes labelled as Mode 1, 2, or 3
4. Local dislocations initially make the material harder at that location, but also where #damage begins.
   1. Length scales matter, because when the ratio of diameter to length of a dislocation's shape exceeds 0.3, the results were equivalent.
   2. Macro-scale: doesn't matter. If looking for incubation in first few cycles, then yes. But this is all *high-cycle fatigue*.
   3. *[high-cycle fatigue](high-cycle-fatigue.md)* (#HCF): elastic regimes of material
   4. *[Low-cycle fatigue](low-cycle-fatigue.md)* (#LCF): all plastic range
   5. $R =\frac{\sigma_{min}}{\sigma_{max}}$ in the cycle. If $R < 0, R=-1$.
   6. Usually good in compression.
>Different phenomenological events require different expressions of math. <cite> #Mark-F-Horstemeyer
5. #fatigue was thought to be a function of stress (for 80 yrs.); however, found to be **#strain-life**.
   1. Jim Newman (NASA) bridged the crack people from 1920 and the #fatigue people working for 50 years with *#stress-life* into using #crack-growth and #strain-life.
   2. #Mark-F-Horstemeyer and #Doug-Baumann introduced "[incubation](incubation.md)". Previously, #fatigue people called this #initiation.
   3. #fatigue load is greater in real materials than ideal.
   4. Monotonic overload in the last half-cycle of a specimen indicated by #striations and coupled with #dimples.
   5. #fatigue needs a [fatigue crack](fatigue-crack.md) to be considered (necessary and sufficient). It is necessary to see #dimples on the #fracture-surface, but not sufficient.
6. Intrinsic vs. Extrinsic toughening: resistance of a material within the material to deformation
   1. [Intrinsic](intrinsic-toughening.md): before crack (internal to the material)
   2. [Extrinsic](extrinsic-toughening.md): after (behind) the crack
   3. Also includes *#grain-bridging*
      1. Frictional effects (#dissipative but into the crack tip). All energy transfer.
      2. #oxides are good examples of extrinsic: does formations of oxides on a reactive metal help to impede or increase #crack-growth?
         1. _It depends_ on the #ductile material.
         2. If an already #brittle material, no, because it will not yield much anyway.
         3. If a #ductile material, it may help impede the #crack-growth.
      3. Anything that impedes the #crack-propagation at the tip, this reduces the crack driving force (can limit the #crack-tip from opening the material).
   4. Crack closure:
      1. elastic regime and opening things up
      2. Where is the plastic regime, near the dislocations.
      3. #stress-strain-curve: material goes back with "#back-stress" ( #kinematic-hardening ) if in plastic regime.
      4. This #back-stress will resist the #crack-wake from opening.
      5. Affected by the direction of dislocations.
   5. #plastic-zone around #crack-tip is _[intrinsic toughening](intrinsic-toughening.md)_.
      1. Seen by misaligned grains/dislocations
      2. Difference between #long-crack and #microstructure-crack is the length scale: [critical crack length](critical-crack-length.md).
   6. San Andreas fault--super long crack--driven by tectonic plate movement, driven by the mantle, driven by convection currents, created by the Genesis flood.
7. Rob Richie creates "resistance curves", but excludes Jim Newman's wake plasticity (which we know that plasticity is ductile).
   1. Resistance can increase, locally while crack grows.
   2. If resisted by a dislocation/grain, then the crack goes around, which increases the crack length.
8. Stress-time curves
   1. minimum stresses are negative, and if asymmetric, there is a mean stress, ($R \neq -1$). Aka creep fatigue.
   2. Use #FFT to move from the time domain to the frequency domain for random vibrations.
9. Cyclic stresses
   1.  Sometimes, these S-N curves are for "2N" for reversals.
   2.  **TEST/QUIZ**
   3.  Stress amplitude is usually what is plotted for S-N curves and stress-time curves.
   4.  $\sigma_{m} = \frac{\sigma_{max} + \sigma_{min}}{2}$
10. [Fatigue limit](fatigue-limit.md)
11. [Fatigue strength](fatigue-strength.md)
12. Just use the modulus or cyclic #stress-strain-curve to move from #stress-strain to #fatigue-life.
    1.  Crack size is associated with strain life curves (these ideas did not come together until MFH in the 90's).
13. #crack-initiation #crack-propagation (old terms)
    1.  **Not incubation**:
14. Stage I and II:
    1.  Differ from initiation/propagation
    2.  I is #orthogonal to stress and parallel to crack (mechanics people: Mode II)
    3.  II (crack people saw fcc materials create cracks at $45^{\circ}$).
15. Crack gets pinned by hard grains or particles such that $\frac{da}{dN}$ goes to zero, then the crack moves around the resistant point to something else.
    1.  x-axis is cycle.
    2.  y-axis is $\frac{da}{dN}$ increment.
    3.  #long-crack growth models cannot capture this #crack-propagation, because the increment is up and down
16. History of fatigue: **_Surface-driven failure_**
    1.  It depends.
    2.  There is also free surface from pores/dislocation/impurities
    3.  #Mark-F-Horstemeyer does not argue with fatigue people, but include the #free-surface from pores, #oxides, etcetera. 
    4.  Quality of surface was the main focus.
    5.  Fatigue specimens required 10 0.02" cuts on the gauge section, which makes it more expensive from the standard 0.05"
    6.  Polishing didn't want to induce #residual-stress.
        1.  Accomplished by #peening, to induce a #mean-stress by minimizing the max tensile load.
        2.  However, this also hardens the material by inducing more dislocations.
        3.  Case arming: diffusing carbon into the surface of steels to increase the yield strength.
        4.  Smooth, gentle curves in the geometry to minimize the notch root radius and subsequent stress.
17. Environment effects
    1.  Very different from mechanical cycles.
    2.  Nuclear reactors shutdown every 3 months:
        1.  Thermal cycles: expected 120 for a 30 yr. service life.
        2.  However, reactors are now asked to operate 100yrs.
        3.  Can AM induce compressive stresses to help increase #fatigue-life?
    3.  #corrosion can cause [extrinsic](extrinsic-toughening.md) forces, but it can also increase #crack-growth-rate.
        1.  MFH's Magnesium specimens formed #oxides layers around the whole surface and pushed the incubation point to much later.
        2.  Cracks would be inhibited by the oxide layer.
        3.  Similar to carburizing the surface (oxidizing).
18. Definitions
    1.  First #fatigue specimens were in #bending, which was found different from uniaxial tension specimens, even if identical materials.
    2.  When in #bending, only half the material experiences tension (either above/below the neutral axis)
    3.  Furthermore, the maximum stress (moving radially from the neutral axis) is at the surface: almost no volume to allow failure.
19. #crack-propagation-rate
    1.  Use $K_{ic} = \sigma\sqrt{\pi a}Y$ (stress intensity factor) for elastic materials.
    2.  If $a$ increases, $K_{ic}$ increases. Long-crack growth if plotted $\frac{da}{dN}|_{K_{ic}}$.
    3.  Slopes are equivalent at the same crack length, but displaced by stress onto microstructure of material.
    4.  #Mark-F-Horstemeyer [MSF](lesson-19-multi-stage-fatigue-msf.md) model moves up from strain-like at the lower length scale to stress-like at the higher length scale, which people do not like.
20. $\frac{da}{dN} = A(\Delta K)^{m}, \Delta K = K_{max} - K_{min}$.
21. #crack-propagation-rate
    1.  Use a math trick with "log" to bring down from an exponential equation.
    2.  This to solve, by integration, to find $N$ to predict cycles to failure.
    3.  Whichever #fatigue-life is longer, you can save volume there to minimize weight, but may need to put some where the #fatigue-life is lowest.
22. To improve #fatigue-life:
    1.  Induce compressive stresses
    2.  Large, uniaxial tension will yield fewer cycles
    3.  Carburizing 
    4.  Polishing