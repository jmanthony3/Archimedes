# Lesson 12: Truck Steering Shaft

- Failure occurred in the bearings, but was blamed as torsional overload.
- What material is it?
  - You have to verify that the material you got was the material you asked for.
  - Material selection is the most common point of failure in a systems design.
- It was designed to be hardest at the outer-most edge, because that outer edge was experience the greatest loading.
- Spline was observed at $45^{\circ}$: which is common for a shear plane.
- #grain-phases -- #martensite, #bainite, #ferrite, or #pearlite --can change during applied strain.
  - Steels exhibit more #martensite when strained.
  - Then, there is a correlation to how much strain the metal has experienced based on how much #martensite is present.
- Remember that $\tau(r); \therefore, \tau(r=0) = 0$
- $\sigma_{TS}(MPa) = 3.2 HV$
  - Common equation to correlate #Vickers-Hardness to stress.
  - Fig. 11 shows a clue that outer edge of shaft could be another phase or chemical material altogether.
- Concluded as axial torque fracture by a [ductile mechanism](lesson-11-ductile-fracture.md): which would have left dimples (though possible in fatigue, which is still dominated by #fatigue-striations).
  - A small fraction of the impact force from collision could have caused failure.
  - Q: What if that small fraction was the applied force to steer the vehicle out of the way of the accident, which subsequently failed and further failed to re-direct the car.
  - A: Human nature. This paper is not good, because it lacks contextual information and analysis. Though, it did go through the [12 step method](12-steps-to-forensic-materials-engineering.md). The drawback here is begging the question.

---
**Breakout Questions for our Specimens**
- No idea how it is broke or if in a corrosive environment.
- Stephen knows the #BC, timelines, and where it broke.
- Q: What was it for? Cross-threading was present.
- A: Stephen, big notch root radius in there.
- Q: Material, loading, chemicals, location, manufacturer?
- A: Stephen.
- #FEA may be difficult for mesh profiles.
---

## Failure Analysis of a Bidet
1. Why do we need different analyses when material contains mesoscale defects: notches, cracks, and voids?
- Stress is concentrated by local defects.
- A handbook by _Peterson_--before #FEA and before computers--includes stress concentration formulas
2. 100 stitches and severe subsequent trauma
- Amorphous ceramic.
- Total flaw size 21-32 mm with some discoloration: who's fault is it?
- What happens to a rock when it hits a windshield?
  - It delaminates, because it is a composite.
  - Weird #residual-stress forms when the layers cool and become solid: cracks are never straight.
  - Windshields are designed for the abnormal environment like this.
  - Ceramics shatter.
3. User was $135 lbs (0.6 kN)$.
- Proof testing: an attempt to replicate the failure event.
  - Showed a max load of 12 kN
  - #fracture-toughness, $k_{f} = 1~MPa\sqrt{mm}$ is a material property. This is not stress concentration.
4. Non-destructive testing
- Weight of person.
- Impact loads.
- Residual stresses from glaze.
- Put a strain gage on the toilet.
  - Yields with no plasticity.
  - Static weight causes $0.4-0.65~MPa$
  - Dynamic impacts
5. Property testing
- #fracture-toughness was found to be $k_{f} = 1.3~MPa\sqrt{mm}$ when the book value was $1$.
6. #residual-stress near defect
- $4 MPa$ near defect
- Total stress, $3*0.4 + 4 = 5.2 MPa$
  - The $3$ is the stress concentration factor of a hole.
  - How big a flow can be with $5.2 MPa$?
7. If $(k_{1} = \sigma\sqrt{a\pi}Y) > k_{ic}$, then the crack will grow. $$k_{1} = \sigma\sqrt{a\pi}Y$$
- $\sigma$ is applied stress
- $a$ is flaw size
- $Y$ is a geometric factor
- This is an elastic solution, because ceramics experience little to no plasticity before failure.
8. $k_{1} = 62.6~MPa\sqrt{mm} >> 1.3 MPa\sqrt{mm}$
- Unfortunately, there is no inclusion of chemical #corrosion here.
- However, including a #corrosion-factor would only increase the applied load, which does not change the result that this catastrophically failed.
- #FEA could be used here to utilize von Mises, because there is no plasticity, which von Mises does not account for anyway.
9. Conclusion
- Cyclic stresses. #fatigue of #brittle material.
10. Failure modes
- This was a manufacturing defect, which is common in #brittle materials.
- Failure occurs not when something breaks, but when it fails to perform its intended function (unexpectedly). 
  - Fracture.
  - Yield.
  - Rust/Corrosion.
  - #fatigue.
  - Failure to fail.
- Failure mode depends on at least 3 critical combinations.
  - Material.
  - Overall load situation.
  - Details of the real structure.