---
title: Mechanical Metallurgy
subject: ENGR 839-001
date: 210823-211217
time: 14:10-15:00 (MWF)
place: DH 3274
speaker: Dr. Mark Atwater
---
# ENGR 839-001: Mechanical Metallurgy
Table of Contents
- [ENGR 839-001: Mechanical Metallurgy](#engr-839-001-mechanical-metallurgy)
    - [Materials: Structure, Properties, and Performance](#materials-structure-properties-and-performance)
        - [Introduction](#introduction)
        - [Review](#review)
        - [Metallic Crystal Structure](#metallic-crystal-structure)
            - [Energy and Packing](#energy-and-packing)
            - [Crystalline (Periodic) Structure](#crystalline-periodic-structure)
        - [Density Comparison of Materials](#density-comparison-of-materials)
            - [Polycrystalline Materials](#polycrystalline-materials)
            - [Anistropy](#anistropy)
            - [Istropy](#istropy)
            - [Miller Indices](#miller-indices)
                - [1) Point coordinates Algorithm](#1-point-coordinates-algorithm)
                - [2) Crystallographic Directions Algorithm](#2-crystallographic-directions-algorithm)
                - [3) Crystallographic Planes Algorithm](#3-crystallographic-planes-algorithm)
            - [Crystal Structure and Deformation](#crystal-structure-and-deformation)
            - [Slip System (fcc)](#slip-system-fcc)
            - [Polycrystalline Slip](#polycrystalline-slip)
        - [Summary](#summary)
    - [Elasticity](#elasticity)
        - [Introduction](#introduction-1)
        - [Elastic](#elastic)
            - [Stress](#stress)
            - [Strain](#strain)
            - [Engineering vs True Stress](#engineering-vs-true-stress)
            - [Notation!](#notation)
            - [Strain Energy](#strain-energy)
            - [Shear/Torsion](#sheartorsion)
            - [Poisson's Ratio](#poissons-ratio)
            - [Summary](#summary-1)
        - [Elasticity: Polycrystalline Materials and Bulk Metals](#elasticity-polycrystalline-materials-and-bulk-metals)
            - [Introduction](#introduction-2)
            - [Stress Tensor Revisited](#stress-tensor-revisited)
            - [Hooke's Law Revisited](#hookes-law-revisited)
            - [Simplifications](#simplifications)
            - [#Mohrs-Circle Revisited](#mohrs-circle-revisited)
        - [Pure Shear](#pure-shear)
        - [Elasticity: Atomic Bonds](#elasticity-atomic-bonds)
            - [Introduction](#introduction-3)
            - [Atomic Bonding](#atomic-bonding)
            - [Bond Interaction and Force](#bond-interaction-and-force)
            - [Stress and Strain in Bonds](#stress-and-strain-in-bonds)
            - [Summary](#summary-2)
    - [Exam Review](#exam-review)
    - [Plasticity](#plasticity)
        - [Introduction](#introduction-4)
            - [Engineering and true stress and strain](#engineering-and-true-stress-and-strain)
            - [Work-Hardening Basics](#work-hardening-basics)
            - [Summary](#summary-3)
        - [Tensile Curve Parameters, Necking, and Strain Rate](#tensile-curve-parameters-necking-and-strain-rate)
            - [Introduction](#introduction-5)
            - [Necking](#necking)
            - [Stress-strain and Necking](#stress-strain-and-necking)
                - [Bridgman Correction](#bridgman-correction)
                - [State of Stress in Deformation](#state-of-stress-in-deformation)
            - [Strain Rate](#strain-rate)
            - [Summary](#summary-4)
        - [Compression and Hardness](#compression-and-hardness)
            - [Introduction](#introduction-6)
            - [Practical Considerations](#practical-considerations)
            - [Compression Curve](#compression-curve)
            - [Compression Failure](#compression-failure)
            - [Bauschinger Effect](#bauschinger-effect)
            - [Hardness Testing](#hardness-testing)
            - [Hardness-Yield Relationship](#hardness-yield-relationship)
            - [Micro-Indentation Testing](#micro-indentation-testing)
            - [Nano-Indentation Testing](#nano-indentation-testing)
        - [Summary](#summary-5)
    - [Defects](#defects)
        - [Introduction](#introduction-7)
        - [Theoretical Shear Strength](#theoretical-shear-strength)
        - [Point Defects](#point-defects)
            - [Interstitial Defects](#interstitial-defects)
                - [#fcc sites](#fcc-sites)
                - [#bcc sites](#bcc-sites)
                - [#hcp sites](#hcp-sites)
            - [Equilibrium Concentration](#equilibrium-concentration)
            - [Vacancy or Self-Interstitial?](#vacancy-or-self-interstitial)
            - [Equilibrium Concentration](#equilibrium-concentration-1)
            - [Vacancy Formation](#vacancy-formation)
            - [Effect on Mechanical Properties](#effect-on-mechanical-properties)
            - [Summary](#summary-6)
        - [Line Defects](#line-defects)
        - [Types of Dislocations](#types-of-dislocations)
            - [Edge and Screw Character](#edge-and-screw-character)
            - [Dislocation Motion](#dislocation-motion)
            - [Bubble Rafts](#bubble-rafts)
            - [Dislocation Confirmation](#dislocation-confirmation)
            - [Dislocation Looping](#dislocation-looping)
            - [Prismatic Loops](#prismatic-loops)
            - [Loop Expansion](#loop-expansion)
            - [Stress Around Dislocations](#stress-around-dislocations)
            - [Stress Equations for [[screw-dislocations]]](#stress-equations-for-screw-dislocations)
            - [Stress Equations for [[edge-dislocations]]](#stress-equations-for-edge-dislocations)
        - [Summary](#summary-7)
        - [Imperfections: Dislocation Energy and Bowing](#imperfections-dislocation-energy-and-bowing)
            - [Energy Around A Dislocation](#energy-around-a-dislocation)
            - [Deformation Energy](#deformation-energy)
            - [Screw Versus Edge Dislocations Energy](#screw-versus-edge-dislocations-energy)
            - [Dislocation Density](#dislocation-density)
            - [Dislocation Bowing](#dislocation-bowing)
            - [Peach-Koehler Equation](#peach-koehler-equation)
        - [Partial Dislocations](#partial-dislocations)
            - [Introduction](#introduction-8)
            - [Real Dislocations](#real-dislocations)
            - [Partial Dislocations in Close-Packed Planes](#partial-dislocations-in-close-packed-planes)
            - [Visualizing fcc Partial Dislocations](#visualizing-fcc-partial-dislocations)
            - [Determining the Partial Direction and Magnitude](#determining-the-partial-direction-and-magnitude)
            - [Decomposition of $\burgers_{1}$](#decomposition-of-burgers_1)
            - [Partial Dislocation Energy](#partial-dislocation-energy)
            - [Stacking Faults](#stacking-faults)
            - [Sessile Dislocations](#sessile-dislocations)
            - [Lomer-Cotrell Locks](#lomer-cotrell-locks)
            - [HCP Dislocations](#hcp-dislocations)
            - [BCC Dislocations](#bcc-dislocations)
            - [Summary](#summary-8)
                - [Dislocation density, homogeneous nucleation](#dislocation-density-homogeneous-nucleation)
            - [Dislocation Sources](#dislocation-sources)
            - [Frank-Read Source](#frank-read-source)
            - [Cross-Slip and Dislocation Multiplication](#cross-slip-and-dislocation-multiplication)
            - [Dislocation Pileup](#dislocation-pileup)
            - [Summary](#summary-9)
        - [Imperfections: Dislocation Interactions](#imperfections-dislocation-interactions)
            - [Introduction](#introduction-9)
            - [Intersection of Dislocations and Forest Dislocations](#intersection-of-dislocations-and-forest-dislocations)
            - [Jogs and Kinks](#jogs-and-kinks)
            - [Effects on [[dislocation-motion]]](#effects-on-dislocation-motion)
            - [Dislocation Looping](#dislocation-looping-1)
            - [Orowan Equation](#orowan-equation)
            - [Peirels-Nabarro Stress (Lattice Friction)](#peirels-nabarro-stress-lattice-friction)
            - [Kink Pair Nucleation](#kink-pair-nucleation)
            - [Temperature and Strain Rate](#temperature-and-strain-rate)
        - [Interfacial Defects](#interfacial-defects)
            - [Grain Boundary](#grain-boundary)
            - [Tilt Boundary](#tilt-boundary)
            - [Twist Boundary](#twist-boundary)
            - [Grain Boundary Energy](#grain-boundary-energy)
                - [Parameter A](#parameter-a)
            - [Grain Boundary Misorientation-Energy Relation](#grain-boundary-misorientation-energy-relation)
            - [Coincident Site Lattice Boundary](#coincident-site-lattice-boundary)
            - [Triple Junctions](#triple-junctions)
            - [Grain Boundary Dislocations and Ledges](#grain-boundary-dislocations-and-ledges)
            - [Summary](#summary-10)
        - [Twinning](#twinning)
            - [Crystallography](#crystallography)
            - [Difference from Slip](#difference-from-slip)
            - [Twinning and Slip](#twinning-and-slip)
            - [Effect of the c/a Ratio](#effect-of-the-ca-ratio)
            - [Mechanical Effects](#mechanical-effects)
            - [Effects of Stacking Fault Free Energy](#effects-of-stacking-fault-free-energy)
            - [Twinning and Slip Stress](#twinning-and-slip-stress)
            - [Summary](#summary-11)
        - [Grain-Size Boundaries](#grain-size-boundaries)
            - [Hall-Petch Equation](#hall-petch-equation)
            - [Theories Behind the Mechanisms](#theories-behind-the-mechanisms)
            - [Cottrell Theory](#cottrell-theory)
            - [Li Theory](#li-theory)
            - [Meyers-Ashworth](#meyers-ashworth)
            - [Summary](#summary-12)
        - [Obstacles to Deformation](#obstacles-to-deformation)
            - [Substructural Effects](#substructural-effects)
            - [Iron-Carbon System Considerations](#iron-carbon-system-considerations)
            - [Nanocrystalline Materials](#nanocrystalline-materials)
                - [Strengthening Mechanisms](#strengthening-mechanisms)
            - [Volumetric Defects](#volumetric-defects)
    - [Deformation and Work Hardening](#deformation-and-work-hardening)
        - [Introduction and Stereographic Projections](#introduction-and-stereographic-projections)
        - [Hot Work versus Cold Work](#hot-work-versus-cold-work)
        - [Work-Hardening](#work-hardening)
        - [Affects of Temperature](#affects-of-temperature)
        - [High Temperature (#DBTT)](#high-temperature-dbtt)
        - [Stereographic Projections](#stereographic-projections)
            - [In Cubic Crystals](#in-cubic-crystals)
            - [Cubic Projections](#cubic-projections)
            - [Resolved Shear Stress](#resolved-shear-stress)
        - [Finding Orientations](#finding-orientations)
        - [Schmid Factor](#schmid-factor)
        - [Easy Glide](#easy-glide)
        - [Summary](#summary-13)
        - [Strain and Slip Reorientation](#strain-and-slip-reorientation)
            - [Resolved Shear Strain](#resolved-shear-strain)
            - [Slip Systems Stereographically](#slip-systems-stereographically)
            - [Reorientation](#reorientation)
            - [Shear Stress-Strain Curves](#shear-stress-strain-curves)
            - [Polycrystalline Slip](#polycrystalline-slip-1)
            - [Summary Slip](#summary-slip)
        - [Polycrystalline Slip](#polycrystalline-slip-2)
            - [Introduction](#introduction-10)
            - [Work-Hardening in Polycrystals](#work-hardening-in-polycrystals)
            - [Modeling Defect Accumulation](#modeling-defect-accumulation)
            - [Taylor Theory](#taylor-theory)
            - [Limitations of Taylor Theory](#limitations-of-taylor-theory)
            - [Seeger Theory](#seeger-theory)
            - [Kuhlmann-Wilsdorf Theory](#kuhlmann-wilsdorf-theory)
            - [Summary](#summary-14)
        - [Softening and Texture](#softening-and-texture)
            - [Thermal Softening](#thermal-softening)
            - [Adiabatic Shear Bands](#adiabatic-shear-bands)
            - [Texture](#texture)
            - [Texture Effects](#texture-effects)
            - [Measuring Texture](#measuring-texture)
    - [Solution and Second-Phase Strengthening](#solution-and-second-phase-strengthening)
        - [Elastic Interactions](#elastic-interactions)
            - [Introduction](#introduction-11)
            - [Substitutionals versus Interstitials](#substitutionals-versus-interstitials)
            - [Elastic Misfit](#elastic-misfit)
            - [Stress Fields in Polar Coordinates](#stress-fields-in-polar-coordinates)
            - [Interaction Energy](#interaction-energy)
            - [Interaction Force](#interaction-force)
            - [Dislocation Pinning](#dislocation-pinning)
            - [Screw Dislocations and Interstitials](#screw-dislocations-and-interstitials)
            - [Example from Research](#example-from-research)
            - [Summary](#summary-15)
        - [Dislocation-Solute Interactions](#dislocation-solute-interactions)
            - [Introduction](#introduction-12)
            - [Upper/Lower Yield Phenomenon](#upperlower-yield-phenomenon)
            - [Luders Banding](#luders-banding)
            - [Strain Aging](#strain-aging)
            - [Dynamic Strain Aging](#dynamic-strain-aging)
            - [Stress-Strain Serration](#stress-strain-serration)
            - [Snoek Effect](#snoek-effect)
            - [Blue Brittleness](#blue-brittleness)
            - [Summary](#summary-16)
        - [Precipitation and Dispersion Strengthening](#precipitation-and-dispersion-strengthening)
            - [Precipitation Hardening](#precipitation-hardening)
            - [Precipitation Process](#precipitation-process)
            - [Precipitation Mechanisms](#precipitation-mechanisms)
            - [Composition and Temperature Effects](#composition-and-temperature-effects)
            - [Coherency](#coherency)
            - [Preferential Precipitate](#preferential-precipitate)
        - [Dispersion Strengthening](#dispersion-strengthening)
        - [Dislocation-Particle Interactions](#dislocation-particle-interactions)
            - [Introduction](#introduction-13)
            - [Dislocation (Orowan) Bowing](#dislocation-orowan-bowing)
            - [Particle Shearing](#particle-shearing)
            - [Shear Stress in Particle Cutting](#shear-stress-in-particle-cutting)
            - [Volume Fraction](#volume-fraction)
            - [Considerations in Precipitation](#considerations-in-precipitation)
            - [Summary](#summary-17)
    - [Martensitic Transformation](#martensitic-transformation)
        - [Structure and Morphology](#structure-and-morphology)
            - [Objectives](#objectives)
            - [Introduction](#introduction-14)
            - [Martensite Process](#martensite-process)
            - [Quick Review](#quick-review)
            - [Other Systems](#other-systems)
            - [Transformation](#transformation)
            - [Morphologies](#morphologies)
            - [Defects in Martensite](#defects-in-martensite)
            - [The Habit Plane](#the-habit-plane)
            - [Summary](#summary-18)
        - [Stress and Strain Effects](#stress-and-strain-effects)
            - [Introduction](#introduction-15)
            - [Martensite Strength](#martensite-strength)
            - [Grain Size and Solution Strengthening](#grain-size-and-solution-strengthening)
            - [Interstitial Hardening](#interstitial-hardening)
            - [Carbon Effects](#carbon-effects)
            - [The Whole Enchilada](#the-whole-enchilada)
            - [Stress-Martensite Interaction](#stress-martensite-interaction)
            - [Martensitic Transformations and Stress](#martensitic-transformations-and-stress)
            - [Mechanical Effect](#mechanical-effect)
            - [Strain-Induced Martensite](#strain-induced-martensite)
            - [Martensite Fracture](#martensite-fracture)
            - [Summary](#summary-19)
        - [Shape Memory](#shape-memory)
            - [Objectives](#objectives-1)
            - [Introduction](#introduction-16)
            - [Overview](#overview)
            - [SME and Martensite](#sme-and-martensite)
            - [Pseudo (Super) Elasticity](#pseudo-super-elasticity)
            - [Martensitic Variants and Pseudoelasticity](#martensitic-variants-and-pseudoelasticity)
            - [Strain Memory](#strain-memory)
            - [SMA Applications](#sma-applications)
            - [Summary](#summary-20)
    - [Intermetallics](#intermetallics)
        - [Objectives](#objectives-2)
        - [Introduction](#introduction-17)
        - [Ordered Structures](#ordered-structures)
        - [Stoichiometry and Formation](#stoichiometry-and-formation)
        - [Intermetallic Phase Diagrams](#intermetallic-phase-diagrams)
        - [Dislocations in Intermetallics](#dislocations-in-intermetallics)
        - [APB Energy](#apb-energy)
        - [Kear-Wilsdorf Lock](#kear-wilsdorf-lock)
        - [Order Parameters](#order-parameters)
        - [Mechanical Effects of Ordering](#mechanical-effects-of-ordering)
        - [Grain Size and Fatigue Performance](#grain-size-and-fatigue-performance)
        - [Second Phase Particles](#second-phase-particles)
        - [Temperature Effects](#temperature-effects)
        - [Ductility](#ductility)
            - [Microalloying](#microalloying)
            - [Macroalloying](#macroalloying)
            - [Composites and Environment](#composites-and-environment)
        - [Summary](#summary-21)
    - [Porous Materials](#porous-materials)
        - [Objectives](#objectives-3)
        - [Introduction](#introduction-18)
        - [Metal Foams Overview](#metal-foams-overview)
        - [Solid State Foams](#solid-state-foams)
        - [Some Power Methods](#some-power-methods)
        - [Precursor Porosity](#precursor-porosity)
        - [Composite Structures](#composite-structures)
        - [Mechanical Considerations](#mechanical-considerations)
        - [Elasticity of Cellular Materials](#elasticity-of-cellular-materials)
    - [Corrosion](#corrosion)
        - [Objectives](#objectives-4)
        - [Introduction](#introduction-19)
        - [Modes of Corrosion](#modes-of-corrosion)
        - [Will It Corrode?](#will-it-corrode)
        - [Corrosion Electrochemistry](#corrosion-electrochemistry)
        - [Polarization and Passivity](#polarization-and-passivity)
        - [Electrochemical Series](#electrochemical-series)
        - [Galvanic Corrosion](#galvanic-corrosion)
        - [Galvanic Protection](#galvanic-protection)
        - [Sacrificial Anodes](#sacrificial-anodes)
        - [Concentration Cell Corrosion](#concentration-cell-corrosion)
        - [Pitting](#pitting)
        - [Intergranular Corrosion](#intergranular-corrosion)
        - [Dealloying](#dealloying)
        - [Oxidation](#oxidation)
        - [Ellingham Diagram](#ellingham-diagram)
        - [Oxidation Effects](#oxidation-effects)
        - [Summary](#summary-22)
        - [Mechanical Effects](#mechanical-effects-1)
            - [Objectives](#objectives-5)
            - [Introduction](#introduction-20)
            - [Stress Corrosion Cracking](#stress-corrosion-cracking)
            - [SCC Process](#scc-process)
            - [Crack Growth](#crack-growth)
            - [SCC Examples and Controls](#scc-examples-and-controls)
            - [Hydrogen Damage and Sources](#hydrogen-damage-and-sources)
            - [Hydrogen Introduction](#hydrogen-introduction)
            - [Mechanisms](#mechanisms)
            - [Control Mechanisms](#control-mechanisms)
            - [Metal Induced Embrittlement](#metal-induced-embrittlement)
            - [Summary](#summary-23)

*Lecture: August 23, 2021*
## Materials: Structure, Properties, and Performance


---


*Lecture: September 01, 2021*

## Elasticity


---


*Lecture: September 09, 2021*

## Exam Review
**Miller Indices**
When drawing Miller indices--coordinates, vectors, and planes--keep to Fig. @fig-milled_index_axis convention. This makes grading quicker, because a different orientation is not necessarily wrong but are harder to grade.

| ![](../../attachments/engr-839-001-mechanical-metallurgy/axes_for_milled_indices_210908_182057_EST.png) |
|:--:|
| Keep cubes with z-vertical and #hcp with c-vertical. $\label{fig:milled_index_axis}$ |

#apf will be used in the exam (per the provided table from earlier lectures). **The content of the homework is the template for the exam: no new content on exams.** WRT to calculating unit cell mass, follow this algorithm example for iron (Fe):

$$\begin{split}
\rho &= \frac{nA}{V_{c}N_{A}}
\end{split} \\
\begin{split}
\rho_{Fe} &= (55 amu) (\frac{g}{mol}/1 amu) / (N_{A}) \\
\rho_{Fe} &= 3.053e-22 g/atom \\
\rho_{Fe, {\#bcc}} &= \rho_{Fe}*2/a_{0}^{3}
\end{split}$$

**Tensorial vs. Engineering Strain**

| ![](../../attachments/engr-839-001-mechanical-metallurgy/engineering_vs_tensor_strains_210908_183912_EST.png) |
|:--:|
| Engineering strain keeps deformation in one axis. Actual strain is half that, but in two axes. $\label{fig:engineer_vs_tensor_strain}$ |

Because we know the relation, $\epsilon_{ij} = \frac{\gamma_{ij}}{2}$, we know $G = \frac{\tau}{\gamma} = \frac{E}{2(1 + \nu)}$. We can then know the deformation on some axis: e.g. $\gamma_{12} = \frac{\sigma_{12}}{G} = -37.1e-6$. But tensor notation for shear strain, $\gamma_{shear} = \frac{\gamma_{calc}}{2}$.

**Calculating Strains from Poisson's Ratio**
Because the compression test is performed in a single axis to squish some specimen, the other lateral strains can be calculated by assuming #plane-stress: zero stress in the direction normal to the thinnest dimension.

| ![](../../attachments/engr-839-001-mechanical-metallurgy/plane_stress_example_210908_185050_EST.png) |
|:--:|
| $\label{fig:plane_stress_example}$ |

[[pure-shear]] occurs when $\sigma_{22} = -\sigma_{11}$. The shear stress, $\tau$ is the radius of [[Mohrs-Circle]]. The principal stress are the maximum and minimum of [[Mohrs-Circle]]. A stress tensor is the sum of the [[hydrostatic-stress]] and [[deviatoric-stress]] tensors: $[\sigma] = [\sigma_{hydro}] + [\sigma_{dev}]$, where [[hydrostatic-stress]], $\sigma_{hydro} = \frac{\sigma_{11} + \sigma_{22} + \sigma_{33}}{3}$ goes on the diagonal of the tensor and will cause a change volume, but not the object's shape. [[deviatoric-stress]]: (elements not on the diagonal) will change an object's shape, but not its volume.

| ![](../../attachments/engr-839-001-mechanical-metallurgy/pure_shear_state_example_210908_185227_EST.png) |
|:--:|
| Remember that maximum shear on [[Mohrs-Circle]], at $90\degree$, is twice the angle in real space: i.e. [[pure-shear]] occurs $45\degree$ of the actual part. $\label{fig:pure_shear}$ |


---


*Lecture: September 13, 2021*

## Plasticity


## Defects



---


*Lecture: October 20, 2021*
## Deformation and Work Hardening



---


*Lecture: October 29, 2021*
## Solution and Second-Phase Strengthening
### Elastic Interactions
#### Introduction
Our treatment of metals and the defects within them has been primarily concerned with pure metals. The vast majority of "real" metals are alloys, and the role of alloying elements can be multi-faceted. The way alloying elements interact with dislocations depends on their size, what position they take in the lattice, and the amount (concentration) of those elements.

#### Substitutionals versus Interstitials
[[substitutionals]]
: The alloying element takes the lattice site of the matrix metal.
- Solvent: majority element in alloy.
- Solute: minority element(s) in alloy.
- | ![](../../attachments/engr-839-001-mechanical-metallurgy/substitutional_versus_interstitials_211029_182341_EST.png) |
|:--:|
| For example, in Cu-Zn, the zinc atoms, [[solute]] take the place of copper, [[solvent]]. \\(\tag{fig:substitutional_versus_interstitials} \label{fig:substitutional_versus_interstitials}\\) |

Alloying has a solid solution form, such that no precipitation of segregation of elements occur. [[Hume-Rothery-Rules]] apply in guiding whether elements stay in solution, practically speaking.

#### Elastic Misfit
$$\begin{equation}
\Delta V = \bigg(\frac{4}{3}\bigg)\pi r_{0}^{3}(1 + \epsilon)^{3} - \frac{4}{3}\pi r_{0}^{3} = \frac{4}{3}\pi r_{0}^{3}[(1 + \epsilon)^{3} - 1]
\label{eq:elastic_misfit}
\end{equation}$$

The insertion of an atom into an undersized [[lattice-site]] causes a volumetric expansion (spherical). If $\epsilon$ is small, then the total volume change can be estimated with Eq. \eqref{eq:elastic_misfit}: $$\Delta V \approx 4\pi r_{0}^{3}\epsilon$$ The reason for this approximation comes from squaring or cubing $\epsilon$ which becomes much smaller, $\require{cancel}\cancelto{0}{\epsilon^{n}} \text{, for } n \geq 2$.

| ![](../../attachments/engr-839-001-mechanical-metallurgy/elastic_misfit_211029_182830_EST.png) |
|:--:|
| The $\frac{4}{3}$ in these equations comes from the volume of a sphere, $\frac{4}{3}\pi R^{3}$. \\(\tag{fig:elastic_misfit} \label{fig:elastic_misfit}\\) |

#### Stress Fields in Polar Coordinates
Recalling Fig. \ref{fig:edge_dislocation_stress_equation_example} for [[edge-dislocations]]: $\stressTensor{-\frac{G\burgers\chi_{2}(3\chi_{1}^{2} + \chi_{2}^{2})}{2\pi(1 - \nu)(\chi_{1}^{2} + \chi_{2}^{2})^{2}}}{\frac{G\burgers\chi_{2}(\chi_{1}^{2} + \chi_{2}^{2})}{2\pi(1 - \nu)(\chi_{1}^{2} + \chi_{2}^{2})^{2}}}{-\frac{G\burgers\chi_{2}\nu}{\pi(1 - \nu)(\chi_{1}^{2} + \chi_{2}^{2})}}{\frac{G\burgers\chi_{1}(\chi_{1}^{2} + \chi_{2}^{2})}{2\pi(1 - \nu)(\chi_{1}^{2} + \chi_{2}^{2})^{2}}}$ yields:

$$\begin{split}
\sigma_{rr} = \sigma_{\theta\theta} &= -\frac{G\burgers}{2\pi(1 - \nu)}\frac{\sin(\theta)}{r} \\
\sigma_{zz} &= -\frac{\nu G\burgers}{\pi(1 - \nu)}{\sin(\theta)}{r} \\
\sigma_{r\theta} &= -\frac{G\burgers}{2\pi(1 - \nu)}\frac{\cos(\theta)}{r} \\
\sigma_{\theta z} &= \sigma_{zr} = 0 \\
\sigma_{p} &= \frac{1 + \nu}{1 - \nu}\frac{G\burgers}{3\pi}{\sni(\theta)}{r}
\end{split}$$

| ![](../../attachments/engr-839-001-mechanical-metallurgy/stress_field_in_polar_coordinates_211029_184041_EST.png) |
|:--:|
| Recall that the stress field is loosely related to $5\burgers$. If you can squish smaller atoms into the solute, then the smaller atoms want to rise to the top of the dislocation which minimizes the local stress to straighten the dislocation. \\(\tag{fig:stress_field_in_polar_coordinates} \label{fig:stress_field_in_polar_coordinates}\\) |

#### Interaction Energy
As described by Eshelby:

$$\begin{equation}
\begin{split}
U_{int} &= V\sigma_{ij}(\epsilon_{ij})_{T} \\
U_{misfit} &= \sigma_{p}\Delta V = \frac{1 + \nu}{1 - \nu}\frac{G\burgers}{3\pi}\frac{\sin(\theta)}{r}4\pi\epsilon r_{0}^{3} = A\frac{\sin(\theta)}{r} \\
A &= \frac{4}{3}\frac{1 + \nu}{1 - \nu}G\burgers\epsilon r_{0}^{3}
\end{split}
\label{eq:interaction_energy}
\end{equation}$$

#### Interaction Force
$$\begin{equation}
\begin{split}
F &= -\frac{\partial U_{misfit}}{\partial r} \\
 &= A\frac{\sin(\theta)}{r^{2}}
\end{split}
\label{eq:interaction_force}
\end{equation}$$

Force from derivative of energy wrt distance from dislocation (Eq. \eqref{eq:interaction_force}). This is true for the area surrounding the [[dislocation-core]]. !!! tip [[interaction-energy]] is positiv above the [[slip-plane]].

#### Dislocation Pinning
The number of [[solute]] atoms near the dislocation determines how strongly the dislocation is prevented from moving. Using the [[Peach-Koehler-Equation]] (Eq. \eqref{eq:peach_koehler_equation}) with solute spacing, $L$ and distance from dislocation, $b$, then $$\Delta\tau = \frac{F_{max}{bL}} = A\frac{\sin(\theta)}{r^{2}bL}$$ The linear dispersion of solute preferred along [[dislocation-density]], $\rho$... 

#### Screw Dislocations and Interstitials

!!! attention
    No [[hydrostatic-stress]] on [[screw-dislocations]].

$$\begin{equation}
U_{misfit} = \dots
\end{split}
\label{eq:screw_dislocation_misfit}
\end{equation}$$

[[interstitials]] do not dilate the structure like [[substitutionals]] where $\epsilon_{11} = \epsilon_{22} = \epsilon_{33} = 0$. Instead, interstitial misfit is found by ...

#### Example from Research
Dr. Atwater found by experiment that placing antimony at the grain boundary of copper lost the nanograins to the boundary near $400\degreeC$ and not the $900\degreeC$ from numerical simulations (Thermal Stability of Nanocrystalline Copper Alloyed with Antimony).

$$\begin{split}
\Delta H_{el, vol} &= \frac{-2N_{Av}K_{Sb}G_{Cu}(V_{Sb} - V_{Cu})^{2}}{3K_{Sb}V_{Cu} + 4G_{Cu}V_{Sb}} \\
\Delta H_{el, rad} &= \frac{-24\pi N_{Av}K_{Sb}G_{Cu}r_{Cu}r_{Sb}(r_{Sb} - r_{Cu})^{2}}{\dots 3K_{Sb}V_{Cu} + 4G_{Cu}V_{Sb}}
\end{split}$$

#### Summary
Solid solution strengthening is an important benefit of alloying. The concentration of solute ...


---


*Lecture: November 01, 2021*

!!! summary Homework Overview
    | ![](../../attachments/engr-839-001-mechanical-metallurgy/problem_5_10_solution_211101_181833_EST.png) |
    |:--:|
    | $L = 200 \mu m = 12cm$ comes out to exactly 600 magnification. Recall that $\bar{l} = \frac{L}{N_{l}M}$, where $M$ is scale ratio of the depicted scalebar to its physical length and length of drawn lines. **Remember to multiply by $\frac{3}{2}$ to get the grain size!** \\(\tag{fig:problem_5_10_solution} \label{fig:problem_5_10_solution}\\) |
    | ![](../../attachments/engr-839-001-mechanical-metallurgy/problem_5_xx_solution_211101_182631_EST.png) |
    |:--:|
    | Looking at Table 5.3 does not give AISI 304 Stainless Steel properties. Refer to Fig. 5.23 for slopes of annealed and work-hardened AISI 304 to solve the [[Hall-Petch-Equation]] \\(\tag{fig:problem_5_xx_solution} \label{fig:problem_5_xx_solution}\\) |
    **When speaking on ASTM grain number, look to Example 5.1! $N = 2^{n - 1}$.**
    | ![](../../attachments/engr-839-001-mechanical-metallurgy/problem_5_5_211101_185051_EST.png) |
    |:--:|
    | Think of planes that are equal, but of opposite signs. Hint: $\ln(\theta_{1}\theta_{2}) = \ln(\theta_{1}) + \ln(\theta{2}) < \ln(\theta_{1} + \theta_{2})$ \\(\tag{fig:problem_5_5} \label{fig:problem_5_5}\\) |

!!! summary Exam Review
    - Lecture 16 (Grain-boundaries)-23 (asdf)
    - Dr. Atwater is not concerned with work equations. Recall the difference between [[tilt-boundary]] and twist dislocations and their dislocation spacing: $D \approx \frac{\burgers}{\theta}$.
    - [[Schmid-Factor]] would also be included (Eq. \eqref{eq:schmid_factor}).
    - Know the generics about stereographic triangles: e.g. knowing which [[slip-system]] is active. Remember that the lens, triangle, and square connote the number of symmetric axes wrt the projection. **There will be drawing of stereographic projections! Only know the basics.** Use $\cos(\theta) = \frac{h_{1}h_{2} + \dots}$ to find the angle between slip-systems.
    - Taylor Hardening, Schmid Factor, pretty much anything from the slides and math from the homeworks. **Eq. 6.5** for dislocation density.


---


*Lecture: November 05, 2021*
### Dislocation-Solute Interactions
Solutes affect [[dislocation-mobility]]. [[stress-strain]] curves may be useful to determine the bulk effect and importance to processing. Phenomena of [[dislocation-solute-interaction]] and their parameters determine the magnitude of their influence.

#### Introduction
Every impoerfection in a crystal has some stress field associated with it. Pure, single crystals are "perfect", but could still include other dislocations. Point defects are [[interstitials]]. Overall energy can be lowered by [[diffusion]] to tensile side of dislocation. This enriched area is a localized "atmosphere" that causes a dislocation to be "trapped". The usefuleness and drawbacks of this behavior can be understood through alloy and processing decisions.

#### Upper/Lower Yield Phenomenon
Low carbon steels exhibit a differential yield stress, characterized by a lower stress plateau (not a common curve). This is caused by a Cottrell atmosphere around a dislocation that locks the dislocation in place: [[interstitials]] diffuse to the [[dislocation-core]] to reduce stress. The effect is most pronounced when the mobility of solute atoms and dislocations is similar: modest temperature required for [[diffusion]] to occur, but not rapidly.

| ![](../../attachments/engr-839-001-mechanical-metallurgy/solute_motion_211108_214228_EST.png) |
|:--:|
| The stress required to break them must exceed the yield strength; therefore, the stress will reduce once broken. However, this stress is higher than that required to move them. A solute will want to stick with the dislocation. This could be thought of as [[work-softening]]. \\(\tag{fig:solute_motion} \label{fig:solute_motion}\\) |

If they do are not locked together, then the yield would be the typical yield stress of material. The book often refers to "removing the yield point" does not mean there is no yielding, only that there is upper-yield point. ==Solutes pin dislocations because of overlapping stress fields.== Solutes need time to diffuse to dislocation for this to work. Once the solute breaks free, it will not immediately go to another dislocation during motion. Once stopped and given sufficient time, then the solute will diffuse.

Aging
: Typically means that some material was precipitate hardened.

The applied stress is greater than required to move dislocations, but is less than what is needed to unlock the dislocation from the solute: think similarly to other [[dislocation-obstacles]] where the dislocation would move if it could. The effect of [[substitutionals]] is limited in this regard and requires higher temperature to permit reasonable [[diffusion-rate]]. A solute "atmosphere" may also be called something similar: e.g. [[Cottrell-Bilby-Cloud]]. These solutes have no reason to remain orderly which is essentially an [[interstitials]] problem: think [[Second-Law-of-Thermodynamics]].

#### Luders Banding
The lower yield plateau exhibits an irregular stress, fluctuating around an average value. The strain during this stage is referred to as yield point elongations. This behavior is governed by the formation of [[deformation-bands]] ([[Luders-bands]]) where the material yields locally. As the strain increases, the bands multiply and the yielded volume extend through the sample. www.vimeo.com/4586024 *Starts off all clean, smooth, and polished, but these bands began to form under deformation along the preferential shear directions. These bands extend across the whole cross-section. Does not matter if angled down-left versus down-right: once one band forms, the stress field resolves to the same direction.*

Once fully accumulated, the [[stress-strain]] behavior takes a more normal [[strain-hardening]] character. This behavior is problematic for the geometrical perturbations it causes, especially in thin components. It can be reduced through 1) alloying: adding elements that will react with [[interstitials]] and bind them in a compound, or 2) pre-straining: deforming the material past the lower yield point so that is behaves uniformly in further deformation.

#### Strain Aging
When you break free of the solute but not quite totally. Dislocations have moved, but there is a hardening effect: usually in terms of precipitates present in alloys by heating and then giving time for diffusion of precipitation. This is the return of solutes through strain so far past the yield point, but then relax from loading. While the component sits on the shelf, carbon has time to diffuse to dislocations which hardens the material again. If held under constant stress, then this process happens much quicker to enhance diffusion. Pre-strained materials cannot be left that way for a long time: the material must be strained again.

#### Dynamic Strain Aging
Dislocations broke free, but carbon caught up over time. In this instance, the solute atoms can actually keep up with the dislocations: the dislocations are not moving that fast. The solutes have higher mobility than the dislocations which are repeatedly pinned hardening and leading to higher tensile strength. Higher temperatures for higher diffusion rates that the solute moves with the dislocation. This does not affect yield, per se, mainly the ultimate tensile strength.

!!! summary Solute-Dislocation Motion Relationships
    - Solutes are pinned to dislocations which break free at the lower yield.
    - Dislocations freed from pinning solutes, but the solutes return over time: strain aging.
    - Solutes keep up with dislocation: dynamic strain aging.
    - Or some mix of these.

#### Stress-Strain Serration
The "serrated" appearance in a [[stress-strain]] curve (sometimes seen in twinning experiments) can be described by various mechanisms of deformation: [[twinning]], martensitic transformation, and intermittent pinning of dislocations. This is known at the [[Portevin-Le-Chatelier-Effect]]. This depends on [[dislocation-density]], [[solute-concentration]], [[strain-rate]], etcetera.

#### Snoek Effect
This describes the effect of uniaxial stress on [[interstitials]] (internal friction). With [[poissons-ratio]] in mind, a stress on one axis will result in different stresses on the other axes. A *z-axis* stress will increase the *z-axis* [[interstitial-volume]] and contract the *x* and *y*. This only occurs for loading that results in differential effect: e.g. not for $\millerPlane{1}{1}{1}$ loading. [[interstitials]], which are regular site atoms and not those pinning dislocations, will then move to the more spacious location on *z*. Can be measured with torsional pendulum:

$$\begin{split}
\tan(\delta) &= \frac{\log(\text{decrement})}{\pi} = Q^{-1} \\
 &= \frac{\ln(\frac{1}{n})}{\pi vt}
\end{split}$$

| ![](../../attachments/engr-839-001-mechanical-metallurgy/snoek_effect_with_torsional_pendulum_example_211109_132842_EST.png) |
|:--:|
| Contractions within the *xy-plane* forces [[interstitials]] to the larger spaces along the *z-axis*: internal friction. This is similar to [[hydrogen-embrittlement]] or cast metals. Distributions of carbon vary when material is stressed. The number of cycles and rate of decay goes into the $\ln(\text{decrement})$. \\(\tag{fig:snoek_effect_with_torsional_pendulum_example} \label{fig:snoek_effect_with_torsional_pendulum_example}\\) |

#### Blue Brittleness
Dislocations are moving and solutes pin them, but the dislocations break free (similar to dynamic aging). However, this is a special case: within a specific temperature range the solute atoms will outpace the dislocations and induce dynamic strain aging. This lowers the ductility and increases the yield strength by dynamically pinning the dislocations. This is a special case of [[Portevin-Le-Chatelier-Effect]].

#### Summary
Dislocation and solute interactions of alloys have decisive effects on the mechanical properties. Temperature affects diffusion rate and strain rate determine rate of dislocation motion versus solute motion. **If, in the formulation of your *Critical Review*, you make an outline of what you want to say, then you can simply plug-n-play.**


---


*Lecture: November 08, 2021*

!!!  summary Exam Answers
    1. The goal was supposed to be simple...however, the trick was to multiply by $\frac{3}{2}$. If wrong number used in next problem, minimal points lost.
    2. Energy increases with angle with more dislocations and more energy; however, modeled as surface tension for higher angles. The energy drops because coincident lattice sites boundaries are more coherent. $\Sigma$ values are indicative of the coincident lattice sites. $\Sigma3$ is a twin boundary and completely coherent.
    3. A mirror.
    4. Low temperature and high strain rate.
    5. Orowan hardening: twin boundaries block slip and glide.
    6. Simply use the table values: $\sigma_{y} \approx 806 MPa$, $\sigma_{y, twin} \approx 1763 MPa$.
    7. $\tau \approx 597.2 MPa$. Only getting the number really mattered and showed tracking of units.
    8. As long as processed was followed (if wrong number from previous problem), then all was fine; however, Hall-Petch stress was the resolved shear stress: did not need to bring in dislocation density or anything like that.
    Bonus. <100>, <110>, <111> and 4 slip systems at <110>.

    The overall average was $\sim 92$.

### Precipitation and Dispersion Strengthening
*(Absolutely no math in this section.)*

#### Precipitation Hardening
Formation of a second phase by the separation or concentration of elements from the homogeneous mixture. Only select alloys can precipitation hardene, and the most important commercial alloys are based on aluminum and nick Aluminum alloys yield lightweight yet strong structural materials, and nickel alloys provide strong, heat-resistant options. The way elements separate from the mix (size, shape, location, etcetera) is determined by chemistry and processing, and the mechanical properties follow suit.

#### Precipitation Process
Basic process of [[precipitation-hardening]] involves three steps:

1. Solutionizing (Solubilization)
2. Quenching
3. Aging: reheating after quenching.

The time and temperature of these steps is determined by the alloy system, and both are important to the maximum hardness.

#### Precipitation Mechanisms
The rejection of a solute from a super-saturated solution will progress through various stages. Using Al-Cu as the archetype, the Cu will first form in clusters along Al $\millerPlaneFamily{1}{0}{0}$ planes: aka [[Guinier-Preston-Zones]] (#GPZ). The zones do not have a distinct crystallographic structure at first and are coherent with the matrix lattice, though a stress field is introduced. As the zones grow, the lattice mismatch increases until the planes are no longer fully coherent, and this required the formation of dislocations to accommodate the structure. As the precipitates grow and assume a distinct crystallography, all coherency may be lost. High temperature treatment may rapidly progress growth, such that early stages are effectively skipped. **This will normally happen outside of our control!**

*[GPZ]: Guinier-Preston Zone

#### Composition and Temperature Effects
Additional Cu will result in more #GPZ. Higher temperatures will accelerate precipitation. #GPZ are quickly transformed to precipitates. Those precipitates grow and become larger and farther apart. This allows for [[dislocation-bowing]] around them more easily. ==Lower temperatures allow for more uniform distribution of precipitates.==

#### Coherency
A second phase can exhibit varying degrees of coherency with the matrix. The lattice spacing must be exact to exhibit full coherency (unlikely). The more similar the phases are, the greater the degree of coherency and the greater the elastic strain is.

#### Preferential Precipitate
To accommodate strain more readily, grain boundaries may be preferred sites for precipitation, thereby depleting the surrounding material from solute. This leads to variability in properties, possibly leading to enhanced grain boundary corrosion or loss of strength. An example is given of the consequences of solute depletion and plan ol' bad design with de Havilland Comet.

### Dispersion Strengthening
Unlike precipitates, dispersions are second particles added to a metal that are often completely different in properties and structures. Much like other composites, the amount and characteristics of the second phase will determine the overall properties. A dilute dispersion will maintain the metallic nature of the mixture, but it will have added strength through dislocation obstacles. These should be small and uniformly dispersed: can be mixed in or created in situ by chemical reaction. Dispersions...


---


*Lecture: November 10, 2021*
### Dislocation-Particle Interactions
Introducing basic concepts of [[dislocation-particle-interactions]] and determining the primary parameters that determine how dislocations will interact with particles. [[dislocation-bowing]] and [[dislocation-shearing]] have factors that determine the mode of passage. Processing considerations and variations within and across compositions may be relevant to [[dislocation-particle-interactions]].

#### Introduction
The inclusion of precipitates and particle dispersions is an effective way to strengthen an alloy (especially non-ferrous alloys). Form of particles is determined by composition and processing, and that will determine the mechanical performance. The primary factors that determine degree of strengthening are the [[particle-size]], [[volume-fraction]], and [[shear-strength]]. There is a way to minimize [[dislocation-motion]] by the presence and size of particles.

#### Dislocation (Orowan) Bowing
If particles are within [[slip-plane]] of a dislocation, the dislocation will be impeded by their presence. 

\eqlab

*insert image*

Assume particles are impenetrable obstacles as basis for Orowan-model of strengthening. Particles are incoherent with matrix such that dislocations cannot pass through any glide-plane. Total shear stress to yield the material is then a combination of the pure matrix strength, $\tau_{m}$ and the dislocation-pinning:

\eqlabe

A more explicit treatment was subsequently developed by Ashby, where the particle radius is considered and predicts strengthening of $\sim0.5$ of the Orowan value: 

\eqlabe

#### Particle Shearing
This mechanism of strengthening assumes [[dislocation-motion]] may pass through particles. This will occur if the stress necessary to pass a dislocation through the particle is less than the stress required to bow the dislocation around the particle: a function of the particle properties and the spacing of the particles.

\eqlab

This indicates that small, hard particles (e.g. oxides, carbides, nitrides, etcetera) within a softer, metallic matrix will be more likely to be controlled by particle spacing than particle shearing. Precipitation occurs....

#### Shear Stress in Particle Cutting
IF the dislocation-glide-plane is coherent with the precipitate, then the stress needed to shear the particle will be determined by the energy of the surface created by passage of the dislocation. Assuming a sphereical particle, the work to cut the particle in two is equivalent ot the creation of the new surface: 

\eqalign

*insert imgae*

#### Volume Fraction
The higher the concentrated of the second phase, the more volume fraction there will be. The volume fraction is determined by composition and precoessing, and size and spacing are inversley proportional. With a uniform, cubic distribution, the volume fraction , $f$ will: 

\eqalign

*insert image*

#### Considerations in Precipitation
During precipitation, there are various conformations as the solute phase(s) come out of the solution during aging. As more particles are formed and grow, the relative abundance of them at these stages will control overall performance. The general behavior follows the relationship: $\tau \propto \sqrt{rf}$. As aging progresses, the radii of particles increases and the balance between bowing and shear changes: i.e.g Ostwald ripening. The critical radius is that where the transition from shear to bowing occurs.

*insert image*

!!! note (The thermal stability of nanocrystalline copper cryogenically milled with tungsten)[https://www.sciencedirect.com/science/article/pii/S092150931201101X?via%3Dihub]
    With some leftover, "pure" copper, its hardness drops dramatically with greater annealing temperatures but less so when tungsten is allowed precipitate into the copper. The characterization class next fall goes into this.

    $$\begin{split}
    P &= \frac{2\gamma}{R} \\
    P_{z} &= \frac{3f\gamma}{2r} \\
    D &= \frac{4r}{3f}
    \end{split}$$

    The more heating, the more the particles want to grow. ==Particles directly contribute to hardness or through dislocation blocking.== Ideally, particles would be aligned along the major axis to the grain boundary.

#### Summary
Dislocations can bow between bow or shear through particles. Small particles and those with coherency are more likely to be sheared. Incoherent, very hard, and larger particles are less likely to be sheared. The spacing of particles is also critical, as bowing is easier around widely spaced particles. The process of precipitation hardening ... ==Particles will either shear or bow, whichever is more favorable.==

!!! tip Critical Review
    Any topic covered can be discussed more than the others: not all topics need the same amount of explanation. Demonstrate your knowledge in those topics.


---


*Lecture: November 12, 2021*

!!! example (10.16) An aluminum alloy is strengthened by diffused, alumina particles with radius, $d = 15 \mu m$ at $3\\% Al_{2}O_{3}$ (weight-percent). Estimate the strength if $G_{Al} = 28 GPa$, $\rho_{Al} = 2700 \frac{kg}{m^{3}}$, and $\rho_{Al_{2}O_{3}} = 3960 \frac{kg}{m^{3}}$. Assume that there is no particle cutting.

    We want to find [[volume-fraction]]. Recall $V = \frac{m^{\*}}{\rho}$.

    $$\begin{split}
    f &= \frac{(\frac{m^{\*}}{\rho})_{\text{solute}}}{(\frac{m^{\*}}{\rho})_{\text{solvent}} + (\frac{m^{\*}}{\rho})_{\text{solute}}} \\
    &= \frac{(\frac{0.03}{3.96})}{(\frac{0.97}{2.70}) + (\frac{0.03}{3.96})} = 0.0207 \\
    \text{Recall: } f &= \frac{4\pi}{3}\frac{r^{3}}{x^{3}} \\
    \implies x &= \bigg(\frac{4\pi}{3f}r^{3}\bigg)^{\frac{1}{3}} \\
    &= \bigg(\frac{4\pi}{3(0.0207)}(15e-6)^{3}\bigg)^{\frac{1}{3}} \\
    &= \bigg(6.83e-13)^{\frac{1}{3}} \\
    &= 8.81e-5 [m] \\
    \text{Recall: } \tau &= \frac{G\burgers}{x} = \frac{(28e9)(0.286e-9)}{8.81e-5} \\
    &= \frac{8.008}{8.81e-5} \\
    &= 9.09e4 Pa \\
    \boxed{\tau &\approx 91 kPa}
    \end{split}$$

    This $\tau$ is not necessarily the shear stress of the material, but is the contribution of the particles to the overall shear stress.

## Martensitic Transformation
### Structure and Morphology
#### Objectives
- Introduce the concepts of martensitic transformations
- Detail various morhpologies of martensite
- review the TTT curves

#### Introduction
Martensite forms through a diffusionless (or nearly) process. Martensitic transformations have three primary applications:

1. Strengthening
2. Toughening
3. Shape-memory

The mechanisms and microstructure can take different forms depending on the composition. Processing and outcome will also vary depending on the material system.

#### Martensite Process
Usually, we think of steels because of its significance. This technique is widely used to strengthen steel and is most often found [OQ5lViYssko]. Not based on time because it is a diffusionless process which does not restructure the atom, but the displacement. The relationships will be informed by other alloying elements, but the general process follows a general process [[austenization]] $\rightarrow$...

#### Quick Review
| ![](../../attachments/engr-839-001-mechanical-metallurgy/quick_review_of_ttt_diagrams_211112_194306_EST.png) |
|:--:|
| We move from [[austenite]] (#fcc, also known as $\gamma$-iron) to [[martensite]] via temperature to erase the prior microstructures. \\(\tag{fig:quick_review_of_ttt_diagrams} \label{fig:quick_review_of_ttt_diagrams}\\) |

*[TTT]: Time-Temperature-Transformation

Quench does not need to be objectively rapid, but is a relative rate of cooling which depends on the material and its initial microstructure.

#### Other Systems
This analysis extends to material systems beyond steel and #BCT microstructures:
- #TRIP steel: retained austenite transformed during deformation
- Ausforming: deform metastable austenite and then 	quench
- Maraging: combination of martensite and intermetallic formation (think precipitation from martensite to austenite)

*[BCT]: Body Centered Tetragonal

#### Transformation
Martensitic transformation are (ideally) diffusionless, such that strain energy dominates the kinetics to make the material more brittle. The transformation may be competitive with diffusional elements, and cooling rate is important: diffusion will be favorable at high temperatures. Where austenite becomes unstable the #TTT diagram can map what phase(s) will form: high alloys will allow much more time for cooling.

| ![](../../attachments/engr-839-001-mechanical-metallurgy/martensite_austenite_competition_211112_195719_EST.png) |
|:--:|
| At higher temperatures, martensite requires much stress to form over austenite which is way martensite favors lower temperatures. \\(\tag{fig:martensite_austenite_competition} \label{fig:martensite_austenite_competition}\\) |

#### Morphologies
Martensitic phases take three general forms:

1. Lenticular
2. Lath
3. Acicular

The substructure of the lath is characterized by dislocations and/or twins. As these phases form, they block other formations which creates backstress. Lenticular is most common in high Ni (30%) and high C (0.6%) Fe alloys Lath martensite forms as "blocks" comprised of "laths" arranged in "packets" separated by low-angle grain boundaries: blocks are a few to tens of microns in size. Acicular martensite is needle-like and forms at the intersection of [[slip-bands]]: forms in austenitic stainless and has significant impact on strength, some steels can become tougher at cryogenic temperatures.

#### Defects in Martensite
Martensite will contain and interact with defects in the microstructure. Examples of twins inside and through martensite are given, but a combination of slip and twinning may occur. Dislocations may be introduced by the crystallographic reorientation and the consequent lattice differences. Twinned martensite (lenticular) will be more brittle than dislocation martensite (laths) due to the twins' blockage of slip.

#### The Habit Plane
All martensite has an undistorted, unrotated plane during transformation. This plane has the same indices in the parent and martensite phases: the plane does not move/change before to after transformation.

#### Summary
Martensitic transformations are diffusionless, but comes in many forms with many different impacts because of its dependence on temperature and the order in which the various phases form. The most common way to form martensite is through quenching.


---


*Lecture: November, 15, 2021*
### Stress and Strain Effects
Martensite in FeC has the biggest outcome to strengthening.

#### Introduction
Martensite is an effective way to increase strength in ferrous alloys. The composition determines the overall strengthening effect, by they share many commonalities. The formation of martensite creates dilation and distortion of the lattice, such that stress and strain results.

#### Martensite Strength
Ferrous martensitic phase provides the greatest strengthening effect. Formation of martensite in sufficient quantity will increase hardness from HRC (Rockwell Hardness, C-scale) 15 to 65. The mechanisms of hardening have been debated for decades, and are now attributed to a combination of factors:

- Dislocation density increases,
- Boundary strengthening,
- Solid Solution strengthening,
- Carbon clustering, etcetera.

#### Grain Size and Solution Strengthening
Hall-Petch hardening is reflected in martensite formation. Smaller grains produce finer martensitic lens. The slope of the Hall-Petch curve may not be affected, but it will be shifted up by increasing carbon content. Grain size is typically not a critical factor in hardened steels in the usual range: $> 100 \mu m$. Substitutional solid solution strengthening is also relatively *unimportant*, but interstitial is.

| ![](../../attachments/engr-839-001-mechanical-metallurgy/grain_size_solution_curves_211115_193457_EST.png) |
|:--:|
| Recall that the last two alloying number denote weight-percent carbon. The more carbon, the higher propensity for martensite hardening. \\(\tag{fig:grain_size_solution_curves} \label{fig:grain_size_solution_curves}\\) |

#### Interstitial Hardening
If martensite is considered as a supersaturated, interstitial solid solution, then it is the major contributor to strength. The strengthening, then, can be thought of as interactions between dislocations and single atoms, where the shear, yield stress is related to the maximum force, $F_\text{max}}$ dislocation line tension, $T$, solute concentration, $C$, and angle of displacement when passing through the solute, $\phi'$: $$\tau_{0} = \bigg(1 - \frac{\phi'}{5\pi}\bigg)C\bigg(\frac{F_{\text{max}}}{2T}\bigg)^{\frac{3}{2}}\sqrt{3C}$$ Strength increases with square root of the concentration. Snoek-ordering (single jump energy minimization) is quick; whereas, formaing a Cottrell atmosphere requires long-range diffusion.

#### Carbon Effects
Carbon causes lattice distortions and shear strain. They will move to regions around screw and edge dislocations that cancel these strains or reduce them. These Cottrell atomspheres will strengthen the alloy in static and dynamic "aging". Carbon may also cluster together and strengthen martensite (without changing its structure): this is most favorable at lower temperatures, as sufficient thermal energy will convert the phases to cementite or other structures. Precipitation can also occur, where some cementite particles are formed within martensite and is more effective at strengthening.

#### The Whole Enchilada
The presence of fine (nanoscale) twins within martensite will also prevent dislocation movement and aid strengthening even more effectively than the other solution or precipitation hardening mechanisms. High dislocation densities associated with martensite will also result in increased strength. Lattice stress (Peierels stress) also contributes to the total, and is highly temperature sensitive. Overall, the various strengthening mechanisms...

#### Stress-Martensite Interaction
The formation of the martensitic structure will induce a lattice stress and can be aided or inhibited by applied stress. Imagine a martensitic lath forming, such that, an initially straight line through it would be distorted. There are two strain: dilation (normal) and distortion (shear).

#### Martensitic Transformations and Stress
Because martensite induces stress to the lattice, stress can affect its formation (stress-assisted martensite). There is work required to transform the structure, both by normal and shear stress/strain. Uniaxial tensions and compression increases $M_{s}$. Hydrostatic stress lowers (suppresses) $M_{s}$. The martensitic transformation can be driven by stress at a temperature higher than it normally would occur.

#### Mechanical Effect
Martensitic transformation causes a distinct drop in load during tensile testing. In the elastic regime, the stress of formation is the yield stress. Grain size and pre-strain increase $M_{s}$.FU_{i}

#### Strain-Induced Martensite
#TRIP steels use strain-induced martensite formation to achieve high strength and ductility. Results in localized strengthening around necked regions, cracks, etcetera.

#### Martensite Fracture
Usually initiated at the martensite boundaries. The martensitic phase is harder in higher carbon alloys with cracks traversing the laths or plates. Microcracks form when one lens impinges another forming a stress concentration. Tempering can softern the overall structure, but impurities may segregate to boundaries and actually embrittle the material.

#### Summary
Martensite has important effects on the strength of materials....


---


*Lecture: November 17, 2021*
### Shape Memory
#### Objectives
Shape-memory effects from shape-memory alloys from certain, underlying principles: especially martensitic phase formation.

#### Introduction
Practical applications of shape memory alloys are numerous, and understanding the phenomena is critical to their control. A martensitic phase transformation is not for strengthening in this case, but rather it is used to exploit elasticity and plasticity effects.

#### Overview
Ti-Ni is a typical, shape-memory alloy. The shape-memory effect (#SME) is a mechanical response that restores a metal to its original shape after plastic deformation by heating: this is only possible if plastic deformation does not occur by slip. Other alloys have also been developed that exhibit this behavior: AgCd, AgZn, AuCd, CuAl, FeBe, NbTi, etcetera.

*[SME]: Shape-Memory Effect

| ![](../../attachments/engr-839-001-mechanical-metallurgy/nickel_phase_diagram_211117_192827_EST.png) |
|:--:|
| bar \\(\tag{fig:nickel_phase_diagram} \label{fig:nickel_phase_diagram}\\) |

#### SME and Martensite
Martensite is a diffusionless transformation: it can be induced or inhibited by applied stress/strain. In #SMA, the original shape is set at elevated temperature in a disordered state ($\beta$, #bcc). During cooling, the phase transforms to an ordered #bcc/orthorhombic structure. The formation of martensite occurs at "low" temperature or by applied stress.

*[SMA]: Shape-Memory Alloy

| ![](../../attachments/engr-839-001-mechanical-metallurgy/formation_of_martensite_from_austenite_211117_192854_EST.png) |
|:--:|
| bar \\(\tag{fig:formation_of_martensite_from_austenite} \label{fig:formation_of_martensite_from_austenite}\\) |

#### Pseudo (Super) Elasticity
[[pseudoelasticity]]
: Property where an alloy can undergo significant amounts of strain and return to its original dimensions.

Martensitic phase forms due to stress at a temperature above $M_{s}$. The austentite/martensite interfaces are [[glissile]], and move throughout the material with an increasing abundance of martensite. The transformation accommodates strain much greater than typically observed, because as stress is reduced, the martensite reverses (again, above $M_{s}$) and the sample returns to its original dimensions.

| ![](../../attachments/engr-839-001-mechanical-metallurgy/pseudoelasticity_211117_193339_EST.png) |
|:--:|
| bar \\(\tag{fig:pseudoelasticity} \label{fig:pseudoelasticity}\\) |

| ![](../../attachments/engr-839-001-mechanical-metallurgy/pseudoelasticity_example_211117_193921_EST.png) |
|:--:|
| Notice correlations with the martensite/austenite temperatures. Above $A_{s}$, the full [[pseudoelastic]]] effect is observed. Between $A_{s}$ and $M_{s}$, the deformation is permanent with little elastic recovery: austenite cannot be formed to reverse it. Below $M_{f}$, the structure is already fully martensitic, so the strain-memory effect is dominant. \\(\tag{fig:pseudoelasticity_example} \label{fig:pseudoelasticity_example}\\) |

#### Martensitic Variants and Pseudoelasticity
The structure of martensite is a "twinned" rhombehedral structure, such that it maintains the same shape. Strain occurs by straightening out these "kinks" such that one orientation (variant) is preferred. The preferred variant depends on applied stress resolved on the variants. There may be many variants, especially in polycrystalline materials, but the cumulative effect is to convert the martensite to a preferred one, until heating reverses the structural changes to a more uniform distribution.

| ![](../../attachments/engr-839-001-mechanical-metallurgy/martensitic_variants_211117_194532_EST.png) |
|:--:|
| bar \\(\tag{fig:martensitic_variants} \label{fig:martensitic_variants}\\) |

#### Strain Memory
[[pseudoelasticity]] is reversed by the austenite phase being in equilibrium. In the more popular #SME, strain memory, the variants do not reverse after stress is released. Strain is retained until heating allows the multi-variant structure to return: overheating will result in an austentic transformation. Some variants will prefer to form under tension/compression, and the localized response will be determined by that.

#### SMA Applications
- Sensors
- Actuators
- Dental wires
- Orthopedic implants
- Shrink-fit compression assemblies

#### Summary
#SMA have unique properties that mediated by martensitic transformation. The creation, modification, and reversal of martensite within these alloys allows unusual elastic and plastic behavior. In [[pseudoelasticity]], the primary mechanism is stress-induced martensitic transformation. In strain-memory, the primary mechanisms is de-[[twinning]] and re-[[twinning]]...


---


*Lecture: November 19, 2021*
## Intermetallics
!!! question What is an [[intermetallic]]? <cite> Atwater
    Effectively, an [[intermetallic]] is sort of a metal: metalloid. It is a metal with some ionic form to drive phase transformations.

### Objectives
Introducing this categroy, we will consider the various features that make an [[intermetallic]] unique. Their crystallographic structure is similar to metals, but their order is different. We will also determine mechanisms responsible for the unique behavior, and the limitations of these materials and strategies to overcome them.

### Introduction
An [[intermetallic]] are ordered metal alloys. They are energetically favorable with a negative bonding energy which introduces new possibilities and complexities to mechanical phenomena. The passage of dislocations creates a higher energy an		tiphase boundary...

The ordered alloys take on specific arrangement in equilibrium. It is important what elements are mixed, as not all will...

| ![](../../attachments/engr-839-001-mechanical-metallurgy/difference_between_intermetallic_and_metal_211119_193417_EST.png) |
|:--:|
| An [[intermetallic]] may have the same weight percentage of elements as a metal, but are well-ordered. |

### Ordered Structures
Crystallographic structures can be described by Strukturbericht or space group designations.

!!! example Ordered Structures
    - A pure #fcc crystal is A1 (Strukturbericht) or Fm3m (space group).
    - A rock salt structure (#fcc) is B1 (Strukturbericht) or Fm3m (space group).
    - $Cu_{3}Au$ [[intermetallic]] (also #fcc) is #L1_{2}$ (Strukturbericht) or Pm3m (space group).

    | ![](../../attachments/engr-839-001-mechanical-metallurgy/ordered_structure_examples_211119_193623_EST.png) |
    |:--:|
    | Space groups care about symmetry, not atomic position. |

Space group is more general, but doesn't give alloy information. Lattice type (P, F, L) followed by symmetry wrt the x, y, and z axes, then the threefold symmetry of the body diagonals, followed, lastly, by any symmetry wrt the face diagonals, if present.

### Stoichiometry and Formation
The typical reference to an [[intermetallic]] category may be $AB$, $AB_{2}$, $A_{3}B$, etcetera. The concentration of elements A and B is critical to the properties but some deviation of the exact chemistry may occur. Intentional elemental substitution may be used to affect ordering and thereby...

negative enthalpy of mixing by ordering; otherwise, phase separation.

### Intermetallic Phase Diagrams

| ![](../../attachments/engr-839-001-mechanical-metallurgy/intermetallic_phase_diagram_examples_211119_193704_EST.png) |
|:--:|
| Typically, an [[intermetallic]] is a binary, chemical composition. |

!!! note A Note on Silicides
    They are [[intermetallic]] with silicon, and they have relatively low densities and high melting points and high temperature strength, which sounds more like ceramics than metals.

### Dislocations in Intermetallics
Partial dislocations are a common feature in #fcc crystals, but they are not parellel to one anoth and cannot [[cross-slip]]. Recall that a high #SFE is characteristic of #bcc# metals and allows easy [[cross-slip]] because $\burgers$ lies in multiple [[slip-planes]] simultaneously. In an [[intermetallic]], two perfect dislocations are linked together by an #APB. The passage of the first dislocation disrupts the ordering, and the second dislocation restores it.

*[APB]: Anti-Phase Boundary

### APB Energy
Unlike partial dislocations, the leading dislocation and trailing dislocation are separated by a region of higher energy due to unfavorable order, but they are repelled by opposing stress fields. The combined dislocations are termed a [[super-dislocation]] since both are needed to fully translate the crystal structure: i.e. [[super-partials]].

| ![](../../attachments/engr-839-001-mechanical-metallurgy/burgers_vector_in_multiple_planes_211119_194851_EST.png) |
|:--:|
| They have high strength because the energy penalty of disordering. |

| ![](../../attachments/engr-839-001-mechanical-metallurgy/antiphase_boundary_depicted_211119_200251_EST.png) |
|:--:|
| As a dislocation moves, there is a restoration from the #APB by the dislocation reordering the edge-dislocation. |

Since each dislocation can thought to do half of the job, they can represented by $\frac{1}{2}\millerVectorFamily{0}{1}{0}$...

### Kear-Wilsdorf Lock
When [[super-partials]] cross-slip onto {100} it will inhibit mobility on {111}. When [cross-slip]] of a screw [[super-dislocation]] onto {100} planes occurs, [[glide]] of the remainder of the dislocation on the {111} system is restricted because the Peierels stress resisting [[glide]] on {100} is much higher than that on {111}.

| ![](../../attachments/engr-839-001-mechanical-metallurgy/kear_wilsdord_lock_211119_200330_EST.png) |
|:--:|
| The energy separation is based on the balance between the dislocations and #APB. The result is a hardening effect and can be reduved through heating. |

### Order Parameters
Long-range order (#LRO) will produce different mechanical properties than short-range order (#SRO). #SRO has higher strength. The ordering parameter is given as a fraction, r, or the total atoms of A in the A positions and the total fraction of A atoms in the alloys is $f_{A}$: $$S = \frac{r - f_{A}}{1 - f_{A}}$$

*[LRO]: Long-Range Order
*[SRO]: Short-Range Order

### Mechanical Effects of Ordering
Ordering produces three stages in [[stress-strain]] curve:
1. well-defined yield point.
2. Linear [[work-hardening]].
3. No [[work-hardening]].

Disordered alloys do not exhibit stages 1 or 2, and have a gradual yield followed by stage 3. However, take these figures with a grain of salt because they are not likely going out to 70\% strain.

### Grain Size and Fatigue Performance
Ordered alloys also behave according to Hall-Petch Equation.


---


*Lecture: November 29, 2021*

!!! note Critical Review Presentation
    Discuss what the paper topic was and what your main takeaway from the paper was.
    You can go into one of your 5 topics.

!!! attention Final Exam
    Not cummulative, but from the previous exam...

### Second Phase Particles
This intermetallic plays a critical role in high-strength, high-temperature applications. It possesses low-coherency stress with the austenite matrix. Dislocation  passage must satisfy the energy considerations described earlier: distances between superpartials is dependent on particle size and spacing, and the interaction of the matrix and particle (elastic stresses).

### Temperature Effects
Some intermetallics increase in strength with temperature. in $\gamma'$, the strength increases with temperature and the austenite decreases, leading to nearly constant yield stress. While not all intermetallic display this, it is attributed to the change in dislocations mechanisms.

### Ductility
Limited by ordering and low-symmetry. High-temperature strength can be offset by a lack of low-temperature ductility for practical applications. Brittleness is caused by:

- Low symmetry in the crystal structure
- Grain boundaries as preferred....

#### Microalloying
Relatively ductile at RT in single crystal form--i.e. useless for polycrystalline materials--but has almost no ductility as a polycrystalline aggregate. Instead, it exhibits intergranular fracture. Intergranular fracture is often attributed to impurities such as S and from environmental effects such as moisture and hydrogen embrittlement. Boron can improve ductility from $0-50\%$.

#### Macroalloying
By exchanging some elements in the ordered structure for other, the symmetry may be increased for more ductility. $(Ni, Co, Fe)_{3}V$ can be modified in composition...

#### Composites and Environment
Combing intermetallics with metals accommodates the brittleness of the intermetallic. There are different modes of incorporating multiple phases, but the overall effect is similar. This isn't really increasing ductility in the intermetallic, just the overall...

### Summary
Intermetallics have range of unique properties: mechanical behavior...

## Porous Materials
### Objectives
- Introduce metal foams in general
- Highlight the diverse processing strategies and outcomes
- Determine the relevant modeling techniques for simplifying the structure
- Determine the behavior trends with changing density
- Discuss limitations of the treatments

### Introduction
Low density materials utilized for intrinsic properties or by introducing a low-density phase with a higher-density matrix. Most often air or otherwise "empty" space is the second-phase, which provides little to no mechanical support.

### Metal Foams Overview
The mostly widely available metal foams are aluminum, and those are created through liquid-state forming (introducing gas into a liquid). This can produce large sheets in low densities: meters across 10s of centimeters thick and $90\%$ porous.

### Solid State Foams

### Some Power Methods

### Precursor Porosity
| ![](../../attachments/engr-839-001-mechanical-metallurgy/precursor_porosity_211129_194350_EST.png) |
|:--:|
| The constituents of the structure already contain open space. |

### Composite Structures
| ![](../../attachments/engr-839-001-mechanical-metallurgy/composite_structures_211129_195256_EST.png) |
|:--:|
| Metal foams can be incorporated into solid structures to combine a high strength with impact absorption or increased stiffness. |

### Mechanical Considerations
Initial density will affect the elasticity as well as plastic behavior. Most notable among low-density metal foams is the plateau stress where the "pores" collapse until a high density is achieved and it begins to behave as a solid material. This makes metal foams particularly interesting for their energy absorption capabilities.

### Elasticity of Cellular Materials
Pores can be simplified to a series of interconnected beams, creating a 3D network. When force is applied under compression, the force is carried by beam bending. The beams are assumed to be of square cross-section and modeled by an end-loaded cantilever.

\eqalign_sans

The elastic modulus is reduced in square propoertion to the density:

\eqalign_sans


---


*Lecture: December 01, 2021*
## Corrosion
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
Pilling-Bedworth Ratio: Equal ot 1, oxide is stable, <1 oxide cracks or forms pores; >> 1 oxides buckle or spall off.

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
- Enhanced plastic flow: the absorbed hydrogen can aid [[dislocation-motion]], making plastic deformation easier at the crack tip: this results in softening in the early stages and [[work-hardening]] in the later stages.
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