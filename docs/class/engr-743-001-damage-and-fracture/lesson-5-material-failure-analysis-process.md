# Lesson 5: Material Failure Analysis Process

- 12 Step Method of Failure Analysis
  - A: Failure Analysis Method
  - Case Study: Hartford Civic Center
    - Structure built in 1972 ($70 million) for 12.5k seats
    - 2.5 acres and roof weighed 1400 tons
    - With flat profile and 4-pt support with steel space truss
    - January 1978 with 4.8" of wet snow
    - Space frame were bolted together, not welded
    - What happened?
      - 1973: computerized design
      - Problem during construction
        - Sags (2X design)
        - Hole misalignment: welded instead of bolted
      - Weight of roof was 25% over spec
      - Buckling of longest span under weight of snow...BUT...weight of roof + snow < maximum load
      - "House of cards" effect
        - Usually not a single point of failure, but several
        - Need redundancies to counteract these
      - Impact
        - Loss of location
        - Loss of money
        - 2 years to rebuild
        - Greatly, adversely affected the community
    - This process does not blame people, but the process which was used.
      - Even if you blame yourself for something, do not blame yourself. Blame the process you used.
      - This is the secret of management and leading.
    - Why study failure?

Commercial Industry | % | Aircraft Industry | %
--- | --- | --- | ---
Stress Corrosion

## [12 Steps](12-steps-to-forensic-materials-engineering.md)
**KNOW THESE FOR THE FINAL**
- 0) Do nothing! Observe.
- 1) Collect background information
  - Service history: need to know everything
  - Any abnormal conditions
  - Begin to compile photo record
  - Any missing parts? 
- 2) Preliminary Visual Examination and Record Keeping
  - Low magnification or no mag photos
  - Observation skills are crucial: is there...
    - Chemical attack
    - Mechanical damage
    - Excessive deformation
    - No gross deformation
    - Cracking patterns
  - Boundary conditions
- 3) Non-destructive Evaluation
  - Stress analysis
  - X-ray (radiography)
  - Ultrasound
    - Best way to get materials [Young's Modulus](youngs-modulus.md)
  - Magnetic particle
    - Best way to find crack or void growth
  - Liquid penetrant
- 4) Mechanical Testing. BE JUDICIOUS!
  - Are standards up to spec? ASTM, ASME, etcetera
  - How is it loaded? Tensile, hardness, etcetera
- 5) Selection/Preservation of Fracture Surfaces
  - Avoid cleaning and touching
  - **DO NOT PUT MATING PIECES BACK TOGETHER!!!**
  - Beware of heat generated by cutting
- 6) Macroscopic Examination
  - #optical-microscope
  - Look for deformations
  - Crack directions
  - Textures
- 7) Looking for local failure mode
  - Smaller features
    - #fatigue-striations
    - Inclusions
- 8) Metallography
  - Cut and polish
  - Show grain growth and heat treatment
  - correct etchants are critical
  - Take samples from various areas
  - Is the material microstructure correct?
  - Is bad heat treatment, wrong material?
- 9) Determine Failure Mechanism
  - Ductile
  - Brittle
  - Wear
  - Fatigue
  - Cant it be re-located?
- 10) Chemical Analysis
  - What material do we have?
  - Use #SEM for x-ray scattering
- 11) Mechanical Failure Analysis
  - Back-of-envelope calculations
  - Look for notches and stress concentrations
- 12) Test Under Simulation Service Conditions
  - Useful, but time and money act against you
  - Be careful to accurately simulate situation
- 13) Final Analysis and Report
  - Your audience is typically a lawyer, which will criticize everything you do.
- Principles
  - Different methods: this a guide, not a laundry list
  - Be reasonable as some steps are impossible, but do them in order when available.
  - First, DO NOTHING! Observe!
  - Tolerances stack up!
  - Fracture and failure modes
  - Objectives
    - 1) Distinguish between the shear and cleavage modes of fracture
    - 2) REvie the five basic stress systems that cause failure
    - 3) Identify distinguishing visible features of stress states in brittle/ductile materials

## Case Study: World Trade Center "Twin Towers"
Observations
- Buildings collapsed vertically
- Buildings did not cantilever onto neighboring buildings

### Analysis
- 2 days after:
  - Envelope math
    - Tower initially hit low enough that above weight, upon collapse, acted as a bomb when combined with jet fuel
    - 135k BTU - jet fuel
    - 24k gallons
    - Kinetic energy, two planes: 9e9 J ~= 2 tons TNT
    - Collapse energy

### Eye Witness Account: a guy went down, against the flow of everyone else going up to a "proverbial helicopter".

### [NTSB](https://www.ntsb.gov/Pages/default.aspx): Uses the [12 Step Method](12-steps-to-forensic-materials-engineering.md) outlined here to perform their analysis.
- Very small group < 40 people.
- Rely on experts around country depending on accident.
  - Consulting fees applies.
- They focus on large-scale, national events
  - WTC
  - Plane reconstructions
- Boundary conditions are very complex.
  - 1. At SNL: >"Any scientist can give you the correct answer with all the information. An engineer provides the answer with the information given." <cite>MH
  - 2. Uncertainties are involved and is the core of **[#ICME](https://onlinelibrary.wiley.com/doi/pdf/10.1002/9781119018377)**
    - Statistics cannot capture all uncertainties of what the root cause is.
    - Process utilizes reverse cause-effect analysis to determine root cause, first. After, statistics use the uncertainties involved at root cause. _[Weibull](https://en.wikipedia.org/wiki/Weibull_distribution)_ for "shotgun" data.

*[ICME]: Integrated Computational Materials Engineering

**Find root cause of failure event, then use statistical uncertainty to find failure mechanism**
  - As the consultant, answers can be provided based on the desired quality of analysis = time and cost of analysis.


---


## Failure Analysis of Mountaineering Rope
### Dynamic Mountaineering Ropes
- Often called "Dynamic Mountaineering Ropes (DMR)", because of the falling motion. So the rope stretches to absorb falling energy.
- This implies that impact forces could exceed loading rating of gear, which is a static rating.

### Background
- Fall Factor, $F = \frac{fall~length}{active~length~of~rope}$
  - The ratio of available distance to travel to available length to arrest fall.
- Human body can withstand up to 15x its weight
- Sheave Effect
  - The "last point of protection" (the carabiner) must withstand 160% of the falling climber.
  - $W_{fall} + W_{belay} + f_{carabiner}$

### Mechanics of the Loading
- Overloading
  - Increase in temperature when viscoelastic material is under tension
  - Viscoelastic vs elastic
    - [Viscoelastic](viscoelasticity.md): Strain-rate dependent in forward loading, but does not _necessarily_ follow along the path of forward loading.
    - [Elastic](elasticity.md): Strain-rate independent and unloading path _exactly_ follows forward loading.
- DMR is **[viscoelastic](viscoelasticity.md)**

### Steps
- Review of application and condition of use
- Identify wear mechanisms
- Condition of rope
  - At point of failure.
  - In general.
  - In high-wear locations.
- Tensile testing of rope and strands.
- Tensile testing of _yarns_.
- Yarn examination and types of failure
  - foo
  - bar

### What properties are examined?
!!! example Spaghetti
    - Spaghetti is a polymer
    - If a fork is applied at either end of a mass of spaghetti strands, the noodles align to the direction of force applied.

- Absorption energy: $U = \frac{1}{2}\sigma\epsilon$
  - This assumes **linear [elasticity](elasticity.md)**.
  - Typically no _yield_ in polymers; therefore, linear [elasticity](elasticity.md) occurs at end of loading, because fibers are aligned.
  - Very rough, envelope math, but close compared to the highly non-linear nature of plasticity: e.g. metals.

### Which property is important?
- Failure stress
- Failure strain
- [Young's modulus](youngs-modulus.md)
- Density

Is this a force or strain-controlled failure?
In the lab, experimental modeling can control either the force or the strain-rate, but the curves are not necessarily equal.
Which controls is determined by application.
- #FEA codes rely on displacement: #strain-rate.
- Riddell (NFL football manufacturer): lost a lawsuit ($14 million), because design was with strain and not stress.
- Not cut-and-dry. Think through each application.

**Spider-line rope has greatest absorption energy.**

### What gage rope?
If worst case is $2L$, then assume that belayer is not helping.
- $U\frac{L\pi d^{2}}{4} = mg2L$
- $d > 2\sqrt{\frac{2mg}{U\pi}}$

### How many falls?
- [Fatigue](fatigue.md) problem.
- [Young's modulus](youngs-modulus.md) changes with each fall.
- You have to know the #strain-life curve, because the answer is not straightforward. [Young's modulus](youngs-modulus.md) is a means to an end, not design parameter: e.g. car crashes are impact energy absorption events and not high-strain rate viscoplastic nor rapid [fatigue](fatigue.md).
- Certain parameters are desired to be restricted, but ultimately it depends.