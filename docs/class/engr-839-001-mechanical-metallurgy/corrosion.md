# Corrosion

### Objectives
- Introduce concepts of corrosion
- Describe the electrochemical mechanisms in their general form
- Discuss various conditions for corrosion and practical work-arounds
- Determine the conditions of oxidation and the effects of it

==All very pressure/temperature dependent!!==

### Introduction
The affects of environment are universally important.
The temperature, moisture, acidity, ecetera will all play important roles determining the reactions that may occur with a metal or alloy.
The metal or alloy is equally important, and alloy design should at least consider corrosion, if not be thr primary consideration.
Practical consequences of environmental degradation are felt throughout daily life in the breakdown of materials: fading color, rusting metal, etcetera.

### Modes of Corrosion
Corrosion comes in many ofrms, with some being more troublesome than other.
All materials are subject to some environmental degradation, but metals are particularly susceptible because they are refined from their native state (ore) which is a ceramic and corrosion product.
The chemistry is critical, but other factors will influence corrosion type and rate as well.

| ![](../../attachments/engr-839-001-mechanical-metallurgy/modes_of_corrosion_211201_201501_EST.png) |
|:--:|
|  |

### Will It Corrode?
The tendency of a metal to corrode depends on the environment.
The environment determines the reaction products.
The reaction products determine their stability/ability to prevent further corrosion.
For instance, a _passive_ metal will form a protective layer that prevents further corrosion.
An _active_ metal will continue corroding as the corrosion products are not protective, and may even increase the corrosion rate.
The behavior of a single metal and reactant will determine by the _potential_ of the system.

### Corrosion Electrochemistry
The corrosion of a single metal or homogeneous alloy is ditacted by the chemical reaction(s) available with the given reactants.
Corrosion of metals involves chemical reaction and the exchange of electrons.
The way this occurs can vary, but in the most general sense, corrosion proceeds by the loss of electrons.

!!! example
$$\begin{split}
M &\rightarrow M^{n+} + ne^{-} \\
2Al + 6HCl &\rightarrow 2AlCl_{3} + 3H_{2} \\
Al \rightarrow Al^{3+} + 3e^{-}
\end{split}$$

### Polarization and Passivity
The availability of electrons determines the reaction rate:

- A negative potential (too many electrons) is **cathodic polarization**.
- A positive potential (too few electrons) is **anodic polarization**.

| ![](../../attachments/engr-839-001-mechanical-metallurgy/polarization_and_passivity_211201_201831_EST.png) |
|:--:|
| The steady-state potential is determined by the rate of electron exchange. Where a passive film is produced, the corrosion rate drops until extremely high potentials can break down passivity. |

### Electrochemical Series
Depending on the corrosion medium, there will be an associated order of activity or passivity for various metals.
The most active (**anodic**) metals will corrode  quickly, and the most passive (**cathodic**) metals will be stable.
When mixed, two metals of different activity will form a galvanic couple.
The more anodic metal will experience accelerated corrosion and the more cathodic will corrode evenly slower.
The magnitude of their difference will determine the rate of corrosion.

### Galvanic Corrosion
When dissimilar metals are in contact in an electrolyte (electron transfer can occur), the current flows from the anode to the cathode.
The anode continually corrodes, providing protection (electrons) to the cathode.
The current is equivalent, so area is critical where accelerated corrosion may be problematic.

### Galvanic Protection
The judicious use of a secondary metal can _improve_ the performance of the primary structural material.
Coating with a more active metal is common, such that the coating will uniformly first, or sacrificially, if the coating is damaged and the underlying metal is exposed.

### Sacrificial Anodes
Instead of coating a structure with an anodic metal, specific anodes can be electrically connected to the structure.
This is more practical for very large structures, those that are difficult to access with long service life expectations etcetera.
The anodes can be replaced as they are consumed to contiually provide protection.
An alternative method is to supply electrons to the structure by cathodic impression, such that it is artificially made cathodic.

### Concentration Cell Corrosion
A galvanic condition can be created in a structure where the conditions vary locally.
Certain areas become more anodic than others, even if they are the same metal alloy.
This is particularly problematic in normally passive metals/alloys where oxygen is needed to form an oxide layer.

| ![](../../attachments/engr-839-001-mechanical-metallurgy/concentration_cell_corrosion_211201_201947_EST.png) |
|:--:|
| Where the oxygen is depleted (in a crevice, for instance) the passive layer cannot be formed, and this results in localized corrosion. |

### Pitting
Pitting is a similar phenomenon to concentration cell corrosion, but the localized corrosion is often caused by deposits on a surface that create local anodic conditions.
The break-in-coating method can apply as well, but an alternative mechanism is build-up on the surface, including prior corrosion products that change the local chemistry.
This is best avoided by maintained clean surfaces and avoiding highly corrosive environments.

### Intergranular Corrosion
Grain boundaries are high energy surfaces that can be susceptible to localized corrosion.
The processing or exposure conditions of certain alloys may _sensitize_ the grain boundaries to intergranular corrosion.

| ![](../../attachments/engr-839-001-mechanical-metallurgy/intergranular_corrosion_211201_202018_EST.png) |
|:--:|
| Some stainless steel grades are a concern, especially when heated sufficiently to cause the chromium that normally passivates the metal to bond with $C$ and form carbides; thereby, lowering the effective $Cr$ concentration. |

!!! attention
==**No small anodes!!**==

### Dealloying
In certain alloys and corrosion media, one of the alloy components will be more active in the corrosion (even when fully mixed).
This causes preferential leaching of an element (e.g. zinc) from the alloy (e.g. brass).
This can actually be used to create nanoporous metals if the combination of metals and corrosion conditions are properly managed.

### Oxidation
The simplest corrosion reaction in metals is oxidation, where the metal bonds with oxygen in a dry environment: oxidation is a general chemistry term and does not need to involve $O_{2}$.
The number of oxygen atoms is determined by the valence number of the metal.

### Ellingham Diagram
Plots the free energy of formation of various oxides and conditions needed to reduce them.
Oxides lower on the diagram are more difficult to reduce, as their enthalpy of formation is very negative (large energy release upon formation).

### Oxidation Effects
As the metal oxidizes, the additional atoms, and more importatnly, the new crystal structure of the oxide will increase the volume of the metal.
This can cause goemetric issues (tolerances), but often the oxide layer is thin or unstable at increasing thickness.
Pilling-Bedworth Ratio: Equal ot 1, oxide is stable, <1 oxide cracks or forms #pores; >> 1 oxides buckle or spall off.

### Summary


---


*Lecture: December 03, 2021*
### Mechanical Effects
#### Objectives
- Introduce stress corrosion cracking
- Discuss the conditions under whic it occurs and mechanisms of operation
- Describe hydrogen damage mechanisms and means to avoid it
- Highlight the potential for metal-induced embrittlement and special considerations

#### Introduction
- Corrosion has significant mechanical effects, even if the corrosion is not widespread
- Uneven stress or chemistry can cause localized corrosion rate to increase and failure to be much quicker than expected
- The environment, the material, and stress conditions must all be suitable for stress corrosion cracking to occur
- Other effects that will cause embrittlement include hydrogen and certain metal combinations
- These can be controlled through...

#### Stress Corrosion Cracking
*[SCC]: Stress Corrosion Cracking

Also referred to Environmentally Assisted Fracture: this occurs where loaclized corrosion weakens a metal and accelerates crack growth below the typical stress intensity required in an inert environment.
Particularly important in normally passivated alloys, where the protective film is broken, such that localized corrosion occurs.

| ![](../../attachments/engr-839-001-mechanical-metallurgy/scc_211203_194352_EST.png) |
|:--:|
| This may be initiated by local variation in chemical concentration, applied tensile stress, surface impingement, or inhomogenities in the structure/composition. |

#### SCC Process
Under internal or applied stress, as the material corrodes, the crack propagates for the root of the pit.
Continued corrosion keeps the crack tip sharp and as the material cracks, fresh surface is exposed.
The crack tip becomes anodic and corrodes more.
The corrode-crack-corrode process occurs in steps.
Fracture can be transgranular (#TG) or intergranular (#IG) depending on the material and environment.
The crack will progress in a direction perpendicular to the stress: brancing is also characteristic...

#### Crack Growth
#SCC will occur below the typical stress determined through linear elastic fracture mechanics.
For a single edge notch (Y = 1.12): $K_{1} = Y\sigma\sqrt{\pi a}$.
$K_{1}$ is also represented as $K_{IC}$ and #SCC can be represented by $K_{ISCC}$.
Crack growth velocity ($\frac{da}{dt}$), varies with $K$, such that three regions may be observed during #SCC
1. Velocity depends on $K$ (bond attack)
2. Velocity is independent of $K$ (diffusion limited)
3. Rapid growth up to $K_{IC}$ (independent of environment)

| ![](../../attachments/engr-839-001-mechanical-metallurgy/crack_growth_211203_194153_EST.png) |
|:--:|
|  |

#### SCC Examples and Controls
- 7079 Aluminum up to Region II: note that temperature increases crack velocity in a constant environment.
- Processing affects susceptibility:
    - TD and RD are less prone to #SCC than ND
    - Smaller grains are more resistant
    - Impurities ($N_{2}$ in SS) can accelerate #SCC dramatically
- Al-Li alloys with varying Cu/Li ratio:
    - Ratio changes the precipitation characteristics, and over-aging produces higher resistances to #SCC
    - High Li content switches to #TG fracture

| ![](../../attachments/engr-839-001-mechanical-metallurgy/scc_examples_and_controls_211203_194750_EST.png) |
|:--:|
|  |

#### Hydrogen Damage and Sources
Hydrogen's small size allows it a rapid diffusion rate in metals.
It may be introduced during processing or service.
High temperature processes such as welding and casting in a moist environment can lead to the formation of ixes and the absorption of hydrogen.
Electroplating can also be a source of hydrogen, and it is used to create porous metals!
The generation of hydrogen during corrosion (nascent $H_{2}$, which is produced from a chemical reaction) can also be a source.
Hydrogen sulfide can also accelerate cracking in petroleum lines: e.g. natural gas.

#### Hydrogen Introduction
The rapid rate of diffusion ($10 \frac{\mu m}{s}$ in Fe at RT) allows hydrogen to quickly move through the structure.
Hydrogen will collect at areas of hydrostatic tension.
The steps include:

- Diffusion to the surface
- Absorption on the surface
- Dissociation at the surface
- Absorption into the surface
- Diffusion through the bulk

| ![](../../attachments/engr-839-001-mechanical-metallurgy/hydrogen_introduction_211203_195752_EST.png) |
|:--:|
|  |

#### Mechanisms
Hydrogen acts in different ways depending on the material, environment, and stress.
Lattice decohesion: hydrogen diffuses to the triaxial tensile stress region at a crack top, and weakens the lattice.
Pressure theory: atomic hydrogen forms diatomic hydrogen within the material, causing it to precipitate and create an internal pressure that adds to any external tensile stress.

| ![](../../attachments/engr-839-001-mechanical-metallurgy/mechanisms_211203_200548_EST.png) |
|:--:|
|  |

- The hydrogen tends to concentrate around defects such as inclusions or compositional heterogeneities (phase boundaries)
- Well annealed and high-purity steels holds much less hydrogen.
- Surface energy: hydrogen absorption decreases surface energy, making crack propagation easier.
- Enhanced plastic flow: the absorbed hydrogen can aid #dislocation-motion, making plastic deformation easier at the crack tip: this results in softening in the early stages and #work-hardening in the later stages.
- Hybride formation: some metals form stable hybrides, and the hybride is brittle: the crack progresses through the hybride into the metal where is arrested until more hybride forms.

| ![](../../attachments/engr-839-001-mechanical-metallurgy/mechanisms_continued_211203_200619_EST.png) |
|:--:|
|  |

#### Control Mechanisms
- Environment: removing chemical conditions where hydrogen exists or can be produced through reactions.
- Alloying: adding elements that reduce hydrogen solubility or prevent unwanted consequences.
- Purity: reduce the number of inclusions, amount of sulfur, and control inclusion geometry. Remove hydrogen before casting through the use of flux or use vacuum casting.

#### Metal Induced Embrittlement
Certain metals will embrittle others:

- Hg for brass and bronze
- Ga for aluminum
- Cd for low alloy steels

Occurs with no electrochemical dissolution, no stable intermetallics, one metals wets the surface of the other, little to no solubility.
Attributed to the lowering of surface nergy and bond wearking for crack initiation growth.

mEx4NuLn9Y

#### Summary
Metals may be obviously weakened through excessive corrosion through the mechanisms described last time, but they can also fail by less noticeable and more insidious means.
The accelerated corrosion...


---


*Lecture: December 06, 2021*

!!! summary Exam Topics to Review
    - Know any question from prior exams.
    - Mohr's circle.
    - Generalized Hooke's Law.
    - Etcetera.
    - Exams are the place to start studying.
        - Nothing about plotting.
        - Will be given any values/assumptions needed.
        - Equations should be on your formula sheet.
        - *Can have up to 4 formulas sheets: one for each prior exam.*
        - Ideally, FE should not take up whole time.
    - Be sure to finish the homeworks.
    - Homework 12.9: Eq. 12.22 and p.648, 650.
    - Dr. Atwater will likely focus on conceptual questions: e.g. stress-strain curves with upper/lower yielding by Cottrell atmosphere/cloud because solutes like to setup shop on dislocations.
    - To precipitate: solutionize, heat, quench. Over-aging is past the maximum of curve: softening past peak strength.
    - Bowing versus shearing in precipitate: will it bow or shear?
    - Dispersed (an alloy thrown in) versus precipitated (generated from alloying itself) phases.
    - Know how porous metals (foams) are formed.
    - Some introductory knowledge of adversion affects of passive layers and (an/cath)odic materials.